---
icon: material/keyboard
description: Find the key to access your boot menu
---

# :material-keyboard: Boot Menu Key

Use the form below to find the correct key to press to access your boot menu. Look for the keys listed for the **Boot Menu**.



!!! note ""

    <form id="form" onsubmit="return false;">
        <label for="form">PC or motherboard manufacturer: </label> <input type="text" id="userInput" /> <br>
        <label for="form">Model (optional): </label> <input type="text" id="input2" /> <br><br>
        <input type="submit" value="Search!" onclick="gse();" />
    </form>

    <script>
    function gse() {
        var input = document.getElementById("userInput").value;
        var input2 = document.getElementById("input2").value;
        window.open("https://www.google.com/search?q=" + input + "+" + input2 + "+boot+key");
    }
    </script>
!!! info "Form Example"
    Full PC model name: **Dell Inspiron 3646**

    Do not put the manufacturer's name in the model name.
    ![key-form](assets/key-form.png)