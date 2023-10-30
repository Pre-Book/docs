---
icon: material/hammer-wrench
description: How to use PreBook.
---

# :material-hammer-wrench: Setup

!!! danger "This section is not finished!"

    Please wait until we finish building it.

## :material-disc: Obtaining an ISO

You can use the downloader below. Simply press one of the buttons to get started.

!!! warning "Adblocker issues"
    If you have a tracker blocker, this probably won't work.

**Based upon:** [Microsoft Software Download Listing](https://github.com/massgravel/msdl)


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
    <p>An error has occurred while processing your request.</p>
    <p>Try refreshing the page or using an alternative method.</p>
</div>

<div id="msdl-download">
    <p>A download should soon be started, if not, <a id="msdl-download-link" href="about:blank">click to download the ISO</a>.</p>
</div>

<input id="msdl-session-id" type="hidden">
</center>

??? note "Alternative: Windows Media Creation Tool"
    
    This is the supported method to download Windows 10 and 11 by Microsoft.

    1. Download the [Windows 10](https://go.microsoft.com/fwlink/?LinkId=691209) or [Windows 11](https://go.microsoft.com/fwlink/?linkid=2156295) Media Creation Tool and open it.
    2. Click the `Accept` button to agree to the Microsoft license terms.
    3. Tick `Create installation media (USB flash drive, DVD, or ISO file) for another PC`, click `Next`, and choose:
        * Language: Desired language
        * Edition: Windows 10 or 11
        * Architecture: 64-bit (x64)
    4. Choose `ISO file` option and choose the download location.
    5. After the ISO has completed downloading, click `Finish` to end the installation.
    
    *Taken from the AtlasOS Docs.*

## :material-book-cog: Choose a playbook

??? warning "Do not use the Ameliorated playbook!"

    This playbook leaves Windows in a very insecure (and potentially broken) state. 
    We highly recommend against using it.
    
    These playbooks use the AME Wizard, but AME's own playbook for it should be avoided.

[:atlas-atlas: AtlasOS](playbooks/atlas.md){ .md-button } [:revi-revi: ReviOS](playbooks/revi.md){ .md-button } [:material-microsoft-windows:{ .windows } None (stock)](playbooks/stock.md){ .md-button }



-----


*AtlasOS branding copyright &copy; [Jack Holmes](https://jackholmes.zip) & [AtlasOS](https://atlasos.net) 2023.*  

*ReviOS branding copyright &copy; [Revision](https://revi.cc) 2019 - 2023.* 
