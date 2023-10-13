<!DOCTYPE html>
<!-- svelte-ignore a11y-missing-attribute -->
<h1>HTML MINIFY</h1>
<!-- svelte-ignore a11y-missing-attribute -->
<html>
    <head>
     <!--<link rel="stylesheet" type="text/css" href="style.css">-->
</head>
<body>
    <!-- svelte-ignore a11y-missing-content -->
    <a href="C:\Users\Admin\myapp\src\routes\app.js"></a>
    <div id="formatter-container">
        <textarea class="large-area--input" placeholder="Enter HTML code here"></textarea>
        <br>
        <!--<button class="controls__button--format">Format HTML</button>-->
        <button class="controls__button--minify">Minify HTML</button>
        <br>
        <textarea class="large-area--output"></textarea>

    </div>
    <script src="formatter.js"></script>

    <script>
        const inputArea = document.querySelector(".large-area--input");
    const outputArea = document.querySelector(".large-area--output");
    //const btnFormat = document.querySelector(".controls__button--format");
    const btnMinify = document.querySelector(".controls__button--minify");
    
    /*btnFormat.addEventListener("click", () => {
         const formattedHTML = formatHTML(inputArea.value);
         outputArea.value = formattedHTML;
         });*/
    
         btnMinify.addEventListener("click", () => {
            const minifiedHTML = minifyHTML(inputArea.value);
            outputArea.value = minifiedHTML;
        });
    
        /*function formatHTML(htmlString) {
            const parser = new DOMParser();
            const xmlDoc = parser.parseFromString(htmlString, "text/html");
            const formattedHTML = new XMLSerializer().serializeToString(xmlDoc);
            return formattedHTML;
            }*/
    
            function minifyHTML(htmlString) {
            return htmlString.replace(/>\s+</g, '><').trim();
        }
    </script>

</body>
</html>