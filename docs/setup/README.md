---
icon: material/hammer-wrench
description: How to use PreBook.
---

# :material-hammer-wrench: Setup

## :material-clipboard-list: What you'll need

- A Windows ISO
- A Windows PC or VM
- [NTLite](https://ntlite.com) (free edition)
- A USB
- [Rufus](https://rufus.ie "Bootable USB creator for Windows") or [Ventoy](https://www.ventoy.net "Multiple ISOs on one USB stick!")
- Our preset

!!! danger "This section is not finished!"

    Please wait until we finish building it.

## :material-download: Obtaining our preset

You can download the latest preset release at the link below.

[:material-download: Download PreBook](https://github.com/Pre-Book/PreBook/releases/latest){ .md-button }

Once you're there, head to the **Assets** section and pick the version for your copy of Windows (`PreBook10` or `PreBook11`).

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

Extract this ZIP file somewhere (like your desktop) using your favorite archiving tool (like [7-zip](https://7-zip.org)). Keep it safe for now, we'll need it later.

![prebook-desktop](../assets/prebook-desktop.png)

## :material-disc: Obtaining an ISO

PreBook is **BYOM**, meaning you need to get your own ISO image of Windows 10 or 11 for your language.

You can use the downloader below. Simply press one of the buttons to get started.

!!! warning "Adblocker issues"
    If this tool doesn't work, try disabling your ad or tracker blocker.

**Based upon:** [Microsoft Software Download Listing](https://github.com/massgravel/msdl)

**Taken from:** [AtlasOS Docs](https://github.com/Atlas-OS/docs/blob/master/docs/javascripts/msdl.js)


<br><br>

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

<center class="centerMsdl">
<button class="win-dl" onclick="getWindows(2616);">Download Windows 11 x86_64</button> <button class="win-dl" onclick="getWindows(2618);">Download Windows 10 x86_64</button>

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

??? grey-tip "Alternative: Windows Media Creation Tool"
    
    !!! failure "ISOs from this tool are out of date!"
        Please use the [MSDL webpage](https://massgrave.dev/msdl) as an alternative for now.
    
    *Taken from the AtlasOS Docs.*

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

[:atlas-atlas: AtlasOS](playbooks/atlas.md){ .md-button } [:revi-revi: ReviOS](playbooks/revi.md){ .md-button } [:material-microsoft-windows:{ .windows } None (stock)](playbooks/stock.md){ .md-button }



-----


*AtlasOS branding copyright &copy; [Jack Holmes](https://jackholmes.zip) & [AtlasOS](https://atlasos.net) 2023.*  

*ReviOS branding copyright &copy; [Revision](https://revi.cc) 2019 - 2023.* 
