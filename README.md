# photo-enhancer
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AI Photo Enhancer</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="container">
        <header>
            <h1>AI Photo Enhancer</h1>
            <p>Upload your image and enhance it with AI!</p>
        </header>
        
        <main>
            <input type="file" id="upload" />
            <button onclick="uploadImage()">Enhance Image</button>
            document.getElementById('loadingMessage').style.display = "block"; // Show loading message
document.getElementById('output').style.display = "none"; // Hide image while processing

            <div class="result-container">
                <img id="output" alt="Enhanced Image" />
                <a id="downloadBtn" style="display: none;" download="enhanced_image.jpg">
                    <button>Download Image</button>
                </a>
            </div>
        </main>
        
        <footer>
            <p>&copy; 2025 Photo Enhancer App | Created by TomsDesign</p>
        </footer>
    </div>

    <script>
        async function uploadImage() {
            let file = document.getElementById('upload').files[0];
            if (!file) {
                alert("Please select an image!");
                return;
            }

            let formData = new FormData();
            formData.append('image', file);

            document.getElementById('output').src = "";
            document.getElementById('downloadBtn').style.display = "none"; 
            document.getElementById('upload').disabled = true;
            document.querySelector("button").innerText = "Enhancing...";

            let response = await fetch('https://your-huggingface-link', { 
                method: 'POST', 
                body: formData 
            });

            let data = await response.blob();
            let url = URL.createObjectURL(data);
            document.getElementById('output').src = url;

            // Show download button
            let downloadBtn = document.getElementById('downloadBtn');
            downloadBtn.href = url;
            downloadBtn.style.display = "block";

            document.getElementById('upload').disabled = false;
            document.querySelector("button").innerText = "Enhance";
        }
    </script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<<link rel="stylesheet" href="style.css">
>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AI Photo Enhancer</title>
</head>
<body>
    <h1>Upload a Photo to Enhance</h1>
    <input type="file" id="upload">
    <button onclick="<script>
    async function uploadImage() {
        let file = document.getElementById('upload').files[0];
        if (!file) {
            alert("Please select an image!");
            return;
        }

        let formData = new FormData();
        formData.append('image', file);

        document.getElementById('output').src = "";
        document.getElementById('downloadBtn').style.display = "none"; // Hide download button
        document.getElementById('upload').disabled = true;
        document.querySelector("button").innerText = "Enhancing...";

        let response = await fetch('https://your-huggingface-link', { 
            method: 'POST', 
            body: formData 
        });

        let data = await response.blob();
        let url = URL.createObjectURL(data);
        document.getElementById('output').src = url;

        // Show download button
        let downloadBtn = document.getElementById('downloadBtn');
        downloadBtn.href = url;
        downloadBtn.style.display = "block";

        document.getElementById('upload').disabled = false;
        document.querySelector("button").innerText = "Enhance";
    }
</script>
">Enhance</button>
    <img id="output" width="400px">
<a id="downloadBtn" style="display: none;" download="enhanced_image.jpg">
    <button>Download Image</button>
</a>

    <<script>
    async function uploadImage() {
        let file = document.getElementById('upload').files[0];
        if (!file) {
            alert("Please select an image!");
            return;
        }

        let formData = new FormData();
        formData.append('image', file);

        document.getElementById('output').src = "";
        document.getElementById('upload').disabled = true;
        document.querySelector("button").innerText = "Enhancing...";

        let response = await fetch('https://huggingface.co/spaces/TheTom20/photo-enhancer-ai/new/main', { 
            method: 'POST', 
            body: formData 
        });

        let data = await response.blob();
        document.getElementById('output').src = URL.createObjectURL(data);

        document.getElementById('upload').disabled = false;
        document.querySelector("button").innerText = "Enhance";
    }
</script>
>
        async function uploadImage() {
            let file = document.getElementById('upload').files[0];
            let formData = new FormData();
            formData.append('image', file);

            let response = await fetch('https://colab.research.google.com/drive/1vNX8y5iQPwqfWCakXRxiz5xi_M0sRtR1#scrollTo=eN_CYABst5sv', { 
                method: 'POST', 
                body: formData 
            });

            let data = await response.blob();
            document.getElementById('output').src = URL.createObjectURL(data);
        }
    </script>
</body>
</html>
/* Global Styles */
body {
    font-family: 'Arial', sans-serif;
    background-color: #f0f4f8;
    color: #333;
    margin: 0;
    padding: 0;
}

.container {
    width: 80%;
    margin: 0 auto;
    text-align: center;
    padding: 20px;
}

/* Header Styles */
header {
    background-color: #007bff;
    color: white;
    padding: 30px 20px;
    border-radius: 10px;
    margin-bottom: 30px;
}

header h1 {
    font-size: 2.5em;
    margin: 0;
}

header p {
    font-size: 1.2em;
}

/* Button Styling */
input[type="file"] {
    margin-top: 20px;
    padding: 10px;
    border: 2px solid #ddd;
    border-radius: 5px;
    font-size: 1em;
}

button {
    background-color: #28a745;
    color: white;
    padding: 15px 30px;
    border: none;
    border-radius: 5px;
    font-size: 1.2em;
    cursor: pointer;
    margin-top: 20px;
}

button:hover {
    background-color: #218838;
}

button:disabled {
    background-color: #ccc;
    cursor: not-allowed;
}

/* Result Section */
.result-container {
    margin-top: 30px;
    display: none; /* Hide initially */
}

.result-container img {
    width: 80%;
    max-width: 500px;
    margin: 20px 0;
    border: 2px solid #ddd;
    border-radius: 10px;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
}

a button {
    background-color: #007bff;
    color: white;
    padding: 12px 25px;
    font-size: 1.1em;
    border-radius: 5px;
    cursor: pointer;
}

a button:hover {
    background-color: #0056b3;
}

/* Footer Styling */
footer {
    background-color: #333;
    color: white;
    padding: 20px;
    margin-top: 50px;
    font-size: 0.9em;
}
body {
    font-family: Arial, sans-serif;
    text-align: center;
    background-color: #f8f8f8;
    padding: 20px;
}

h1 {
    color: #333;
}

input {
    margin: 10px;
    padding: 10px;
    border: 1px solid #ddd;
    border-radius: 5px;
}

button {
    background-color: #007bff;
    color: white;
    padding: 10px 20px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}

button:hover {
    background-color: #0056b3;
}

img {
    margin-top: 20px;
    border-radius: 10px;
    box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.2);
}
