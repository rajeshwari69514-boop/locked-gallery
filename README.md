# locked-gallery

# coding
<!DOCTYPE html>
<html>
<head>
    <title>Locked Gallery</title>
    <style>
        body {
            margin: 0;
            font-family: 'Segoe UI', sans-serif;
            background: linear-gradient(120deg, #1e3c72, #2a5298);
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }

        .lock-screen, .gallery-container {
            background: rgba(255,255,255,0.1);
            backdrop-filter: blur(15px);
            padding: 30px;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.4);
            text-align: center;
            width: 90%;
            max-width: 1000px;
            color: white;
        }

        .gallery-container {
            display: none;
            height: 90vh;
            overflow-y: auto;
        }

        input {
            padding: 10px;
            width: 70%;
            border-radius: 8px;
            border: none;
            margin: 10px 0;
        }

        button {
            padding: 10px 20px;
            border-radius: 8px;
            border: none;
            background: #ff9800;
            color: white;
            cursor: pointer;
            transition: 0.3s;
        }

        button:hover {
            background: #e68900;
            transform: scale(1.05);
        }

        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }

        .card {
            background: white;
            color: black;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 6px 15px rgba(0,0,0,0.3);
            transition: 0.4s;
        }

        .card img {
            width: 100%;
            height: 180px;
            object-fit: cover;
        }

        .caption {
            padding: 10px;
            font-weight: bold;
        }

        .card:hover {
            transform: translateY(-8px) scale(1.03);
        }
    </style>
</head>
<body>

<!-- Lock Screen -->
<div class="lock-screen" id="lockScreen">
    <h2>🔒 Private Gallery</h2>
    <p>Enter Password to Unlock</p>
    <input type="password" id="password" placeholder="Enter Password">
    <br>
    <button onclick="unlockGallery()">Unlock</button>
</div>

<!-- Gallery -->
<div class="gallery-container" id="galleryContainer">
    <h2>📂 Unlocked Gallery</h2>

    <div class="gallery">

        <div class="card"><img src="https://picsum.photos/400/300?1"><div class="caption">Nature</div></div>
        <div class="card"><img src="https://picsum.photos/400/300?2"><div class="caption">Mountain</div></div>
        <div class="card"><img src="https://picsum.photos/400/300?3"><div class="caption">City</div></div>
        <div class="card"><img src="https://picsum.photos/400/300?4"><div class="caption">Ocean</div></div>
        <div class="card"><img src="https://picsum.photos/400/300?5"><div class="caption">Forest</div></div>
        <div class="card"><img src="https://picsum.photos/400/300?6"><div class="caption">Sky</div></div>
        <div class="card"><img src="https://picsum.photos/400/300?7"><div class="caption">Desert</div></div>
        <div class="card"><img src="https://picsum.photos/400/300?8"><div class="caption">Snow</div></div>
        <div class="card"><img src="https://picsum.photos/400/300?9"><div class="caption">Bridge</div></div>
        <div class="card"><img src="https://picsum.photos/400/300?10"><div class="caption">Night</div></div>

    </div>

    <br>
    <button onclick="lockGallery()">🔒 Lock Again</button>
</div>

<script>
    function unlockGallery() {
        let pass = document.getElementById("password").value;
        if (pass === "1234") {
            document.getElementById("lockScreen").style.display = "none";
            document.getElementById("galleryContainer").style.display = "block";
        } else {
            alert("Wrong Password!");
        }
    }

    function lockGallery() {
        document.getElementById("galleryContainer").style.display = "none";
        document.getElementById("lockScreen").style.display = "block";
        document.getElementById("password").value = "";
    }
</script>

</body>
</html>

# website
<img width="1620" height="535" alt="image" src="https://github.com/user-attachments/assets/aa62deaa-a474-40c3-8421-d335d94d2781" />
<img width="1319" height="805" alt="image" src="https://github.com/user-attachments/assets/6dc2e9ef-e9c6-4f60-9429-b6e5eee83fd5" />



# output
 https://rajeshwari69514-boop.github.io/locked-gallery/
