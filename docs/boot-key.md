---
icon: material/keyboard
description: Find the key to access your boot menu
---

# :material-keyboard: Boot Menu Key

Use the form below to find the correct key to press to access your boot menu. Look for the keys listed for the **Boot Menu**.

!!! note ""

    <form id="form" onsubmit="return false;">
        <label for="form">PC or motherboard manufacturer: </label> <input type="text" id="userInput" /> <br><br>
        <input type="submit" value="Search!" onclick="gse();" />
    </form>

    <script>
    function gse() {
        var input = document.getElementById("userInput").value;
        window.open("https://www.google.com/search?q=" + input + "+boot+key");
    }
    </script>