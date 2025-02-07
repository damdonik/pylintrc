<!DOCTYPE html>
<html>
<head>
    <title>Drag & Drop File Upload</title>
    <style>
        #dropzone {
            width: 300px; height: 150px; border: 2px dashed #000;
            display: flex; align-items: center; justify-content: center;
            margin: 20px auto; text-align: center;
        }
    </style>
</head>
<body>
    <div id="dropzone">Drag files here</div>
    <input type="file" id="fileInput" multiple hidden>
    <script>
        let dropzone = document.getElementById("dropzone");
        dropzone.addEventListener("dragover", (e) => { e.preventDefault(); dropzone.style.borderColor = "blue"; });
        dropzone.addEventListener("dragleave", () => dropzone.style.borderColor = "black");
        dropzone.addEventListener("drop", (e) => {
            e.preventDefault();
            let files = e.dataTransfer.files;
            alert(`Uploaded ${files.length} files.`);
        });
    </script>
</body>
</html>
