---
icon: material/hammer-wrench
description: How to use PreBook.
---

# :material-hammer-wrench: Setup

## :material-clipboard-list: What you'll need

- :material-disc: A Windows ISO
- :material-clipboard-text: Meeting the system requirements for [Windows 11](https://www.microsoft.com/en-gb/windows/windows-11-specifications#table1) or [Windows 10](https://www.microsoft.com/en-gb/windows/windows-10-specifications#primaryR2)
    - This excludes a Microsoft account, TPM and Secure Boot
- :material-cpu-64-bit: 64-bit processor ([you can check what you have](https://support.microsoft.com/en-us/windows/which-version-of-windows-operating-system-am-i-running-628bec99-476a-2c13-5296-9dd081cdd808))
    - 64-bit ARM (aarch64) only works on Windows 11 <!-- Taken from AtlasOS docs, credit to all docs contributors -->
- :material-wifi: A stable internet connection
- :material-microsoft-windows: A Windows PC or VM (can also be the same PC you're installing PreBook to)
- :material-package-variant: [NTLite](https://ntlite.com) (free edition)
- :material-usb-flash-drive: A USB
- :material-lightning-bolt: [Rufus](https://rufus.ie "Bootable USB creator for Windows") or [Ventoy](https://www.ventoy.net "Multiple ISOs on one USB stick!")
- :material-download: Our preset


## :material-clipboard-pulse: Preparing your system

!!! danger "This will wipe your Windows!"
    Please make backups of your important files first. You can store these backups on **external drives**, **cloud storage websites**, **network servers**, or your **installation drive** (after flashing PreBook to it).

First, open **File Explorer** and go to **This PC**. Then, right click your C: drive and choose **Rename**.

=== "**:material-microsoft: Windows 11**"

    ![rename-drive](../assets/rename-drive.png)

=== "**:material-microsoft-windows: Windows 10**"

    Right click your C: drive and click here:

    ![rename-drive-10](../assets/rename-drive-10.png)

Type in **OS** or **Windows** to relabel your C: drive and press ++enter++. This will be important later on.

### :material-download: Getting our preset

You can download the latest preset release at the links below:

[:material-download: Download PreBook 10](https://github.com/Pre-Book/PreBook/releases/latest/download/PreBook10.zip){ .md-button } [:material-download: Download PreBook 11](https://github.com/Pre-Book/PreBook/releases/latest/download/PreBook11.zip){ .md-button }

You will get a ZIP file containing everything you'll need, which will look something like this:

![prebook-files-1](../assets/prebook-files-1.png#only-dark)
![prebook-files-1](../assets/prebook-files-1-light.png#only-light)

```js title="PreBookXX.zip"
.
├── registry/
│   └── <.reg files> // (1)!
├── ei.cfg // (2)!
└── PreBookXX.xml // (3)!
```

1.  All the .reg files specific to your version are here.
2.  This file forces the edition picker, more on that later.
3.  The preset itself. Named PreBook10 or PreBook11.

Extract this ZIP file into a new folder called **`PreBook`** somewhere (like your desktop) using your favorite archiving tool (like [7-zip](https://7-zip.org)). Keep it safe for now, we'll need it later.

![prebook-desktop](../assets/prebook-desktop.png)

### :material-ethernet: Network Drivers

Windows may not include your network drivers by default, so if you can, save them to your **`PreBook`** folder, or have another device that you can transfer the drivers from.

You can get your network drivers by searching for your device or motherboard's official driver page, or by finding a driver page for your network card or dongle. 

You can find your network card via [Device Manager](#network-drivers "Right click the Start button or search for it."):

![device-manager-network](../assets/device-manager-network.png)

## :material-disc: Getting an ISO

PreBook is **BYOM**, meaning you need to get your own ISO image of Windows 10 or 11 for your language.

<span class="noJs">To do this, you can use the downloader below. Simply press one of the download buttons to get started.</span>

!!! warning "UBlock Origin and similar tools"
    One of the scripts used here is blocked by UBlock Origin. 
    
    Some exceptions have been made, we are not one of them. Do not report this to UBlock, [they know](https://github.com/uBlockOrigin/uAssets/issues/16440).

    This was fixed for the AtlasOS docs and MSDL ([:material-github:Atlas docs PR](https://github.com/uBlockOrigin/uAssets/pull/20642)). 
    
    If you have such tools, this downloader will use a proxy. However, to avoid strain on said proxy, we recommend disabling your adblocker on this page temporarily (re-enable it once the download is done) (the only tracker on this page is [Cloudflare Web Analytics](https://www.cloudflare.com/web-analytics/)).

??? danger "Bypassing Windows 11 Requrements"
    It's not recommended to bypass Windows 11's requirements as anticheats will still check if you meet them regardless. 

    If you do not meet the requirements, please use **:material-microsoft-windows: Windows 10**.
    
    If you would like to bypass anyway, please use Rufus when [flashing your USB](./playbooks/stock.md#flashing-our-iso-to-a-usb-drive), or consult the Internet for a guide.
--------
<br>
<noscript>
<b>The documentation's Windows ISO downloader doesn't show for you due to the documentation being loaded without JavaScript.</b>
See the alternatives below.
</noscript>
<br>
<div align="center">
    <b>Choose your Windows:</b>
</div>
<!--
    This is based upon the Microsoft Software Download Listing website by massgravel on GitHub.
-->
<!--
    The JavaScript file that is used with this is licensed under GNU Affero General Public License v3.0,
    in accordance with the original project. https://github.com/massgravel/msdl/blob/main/LICENSE
-->
<!--
    This was taken from the AtlasOS docs. See the JavaScript: https://raw.githubusercontent.com/Atlas-OS/docs/master/docs/javascripts/msdl.js
-->

<center class="noJS centerMsdl">
<div class="msdl-button-container">
    <button class="msdl-button" style="margin-right: 2px" onclick="getWindows(2935);">Download Windows 11 x64</button>
    <button class="msdl-button" style="margin-left: 2px" onclick="getWindows(2618);">Download Windows 10 x64</button>
</div>

<div id="msdl-ms-content"></div>

<div id="msdl-please-wait">
    <p>Please wait...</p>
</div>

<div id="msdl-processing-error">
    <p>An error has occurred while processing your request.Try refreshing the page or using an alternative method.</p>
    <p id="msdl-error-code">Error: Unknown</p>
</div>

<div id="msdl-download">
    <p>A download should soon be started, if not, <a id="msdl-download-link" href="about:blank">click here to download the ISO</a>.</p>
</div>

<input id="msdl-session-id" type="hidden">
</center>

:simple-github: **Downloader based upon:** [Microsoft Software Download Listing](https://github.com/massgravel/msdl) and **made by** [he3als](https://he3als.xyz) and the AtlasOS docs contributors ([source](https://github.com/Atlas-OS/docs/blob/master/docs/javascripts/msdl.js)).

<script>
    var styleSheet = document.createElement("style")
    styleSheet.innerText = '.noJs { display: revert !important }'
    document.head.appendChild(styleSheet)
</script>

??? note "Alternatives"
    === "Windows Media Creation Tool"
        !!! failure "Windows 11"
            AME playbooks only support Windows 10 22H2 and Windows 11 23H2 (though ReviOS supports 11 22H2).

            The current Media Creation Tool for Windows 11 only creates 22H2 media, so the Windows 11 Media Creation Tool currently can't be used for Prebook.

        1. Download the [Windows 10](https://go.microsoft.com/fwlink/?LinkId=691209) or [Windows 11](https://go.microsoft.com/fwlink/?linkid=2156295) Media Creation Tool and open it
        2. Click the **Accept** button to agree to the Microsoft license terms
        3. Select **Create installation media (USB flash drive, DVD, or ISO file) for another PC**, click **Next**, and choose:
            - **Language:** Desired language
            - **Edition:** Windows 10 or 11
            - **Architecture (Windows 10 only):** 64-bit (x64)
        4. Select the **ISO file** option and choose the download location
        5. After the ISO has completed downloading, click **Finish**
        
        *This text &copy; Atlas Docs Contributors, licensed under CC-BY-SA 4.0*
    === "MSDL website"
        Visit the [MSDL website](https://massgrave.dev/msdl), and download your Windows ISO from there.

        When choosing the ISO download link at the end, make sure to pick `IsoX64 Download`.

        [:material-microsoft-windows: Download Windows 10](https://massgrave.dev/msdl/#2618){ .md-button }
        [:material-microsoft: Download Windows 11](https://massgrave.dev/msdl/#2935){ .md-button }

## :material-package-variant: Installing NTLite

!!! info "You only need NTLite free!"
    You do not need the paid version of NTLite to use PreBook. However, you should [buy it](https://www.ntlite.com/shop/) to show some :heart: to the developer!

Click the button below and pick `64-bit` under `Stable`:

[![ntlite_dl](../assets/ntlite_dl.png)](https://www.ntlite.com/download/)



[Download NTLite :material-open-in-new:](https://www.ntlite.com/download/){ .md-button }



Open the installer, and go through the steps.

Once you come here, pick `Free`, then `Close`:

![license](../assets/license.png#only-dark)
![license](../assets/license-light.png#only-light)

Once NTLite is installed, we can continue with the other steps.

## :material-book-cog: Choose a playbook

This will affect what additional tweaks need to be done.

??? warning "Do not use the Ameliorated playbook!"

    This playbook leaves Windows in a very insecure (and potentially broken) state. 
    We highly recommend against using it.
    
    These playbooks use the AME Wizard, but AME's own playbook for it should be avoided.

<div class="grid cards" markdown>

-   :atlas-atlas:{ .lg .middle } [__AtlasOS__](https://atlasos.net)

    ---

    Windows redesigned for gaming (strips more).

    [:octicons-arrow-right-24: Choose this playbook](./playbooks/atlas.md)

-   :revi-revi:{ .lg .middle } [__ReviOS__ [WIP]](https://revi.cc)

    ---

    Windows as it should be: private, preformant and secure (strips less).

    [~~Choose this playbook~~](./playbooks/revi.md)

-   :material-microsoft-windows:{ .lg .middle .windows } __Stock__

    ---

    Normal Windows, just with annoying preinstalled stuff removed.

    [:octicons-arrow-right-24: Choose no playbook](./playbooks/stock.md)

</div>

<!-- [:atlas-atlas: AtlasOS](playbooks/atlas.md){ .md-button } [:revi-revi: ReviOS](playbooks/revi.md){ .md-button } [:material-microsoft-windows:{ .windows } None (stock)](playbooks/stock.md){ .md-button } -->

-----

*AtlasOS branding copyright &copy; [Jack Holmes](https://jackholmes.zip) & [AtlasOS](https://atlasos.net) 2023.*  

*ReviOS branding copyright &copy; [Revision](https://revi.cc) & [Stasium](https://stasium.dev/) 2019 - 2023.*
