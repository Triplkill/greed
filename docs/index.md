Skip to content
Search or jump to…
Pull requests
Issues
Marketplace
Explore
 
@Triplkill 
Triplkill
/
greed
Public
Code
Issues
Pull requests
Actions
Projects
1
Wiki
Security
Insights
Settings
greed/index.html
@Triplkill
Triplkill Rename Untitled-1.html to index.html
Latest commit f65aca1 16 minutes ago
 History
 1 contributor
38 lines (37 sloc)  1.22 KB

document.addEventListener("keyup", function (e) {
    var keyCode = e.keyCode ? e.keyCode : e.which;
            if (keyCode == 44) {
                stopPrntScr();
            }
        });
function stopPrntScr() {

            var inpFld = document.createElement("input");
            inpFld.setAttribute("value", ".");
            inpFld.setAttribute("width", "0");
            inpFld.style.height = "0px";
            inpFld.style.width = "0px";
            inpFld.style.border = "0px";
            document.body.appendChild(inpFld);
            inpFld.select();
            document.execCommand("copy");
            inpFld.remove(inpFld);
        }
       function AccessClipboardData() {
            try {
                window.clipboardData.setData('text', "Access   Restricted");
            } catch (err) {
            }
        }
        setInterval("AccessClipboardData()", 300);
body {
  background-color: #00FF00;
}
<html>
    <head>
      <title>Disable Print Screen</title>
    </head>
  <body>
      <h2>Print screen is disabled</h2>
      <p>Click anywhere on green background and try to "print screen" the content (and then see the result in Paint or simulair software)
  </body>
</html>