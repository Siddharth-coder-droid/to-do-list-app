<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>XML Indentation</title>
    <style>
        textarea { width: 100%; height: 150px; margin-bottom: 10px; }
        button { margin-bottom: 20px; }
    </style>
</head>
<body>
    <h1>XML Indentation</h1>

    <label for="xmlInput">XML Input:</label>
    <textarea id="xmlInput"></textarea>

    <label for="indentation">Select Indentation:</label>
    <select id="indentation"><option>2</option><option>4</option><option>8</option></select>

    <button id="indentButton">Indent XML</button>

    <h2>Indented XML Output:</h2>
    <textarea id="xmlOutput" readonly></textarea>

    <script>
        const xmlInput = document.getElementById("xmlInput");
        const indentation = document.getElementById("indentation");
        const xmlOutput = document.getElementById("xmlOutput");
        const indentButton = document.getElementById("indentButton");

        function indentXml() {
            const spaces = " ".repeat(parseInt(indentation.value));
            const indentedXml = xmlInput.value.replace(/\n/g, `\n${spaces}`);
            xmlOutput.value = indentedXml;
        }

        indentButton.addEventListener("click", indentXml);
    </script>
</body>
</html>