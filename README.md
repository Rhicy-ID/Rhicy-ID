
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jumpscare Example</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #000;
            color: #fff;
            font-family: Arial, sans-serif;
            text-align: center;
            position: relative;
        }
        #jumpscareImage {
            display: none; /* Mulai dengan gambar disembunyikan */
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            z-index: 10;
        }
        #jumpscareAudio {
            display: none; /* Suara tidak perlu ditampilkan */
        }
    </style>
</head>
<body>
    <div>
        <h1>Click the Button for a Surprise!</h1>
        <button id="jumpButton">Click hadiahh</button>
        <img id="jumpscareImage" src="https://example.com/nama gambar jumpscare.jpg" alt="Jumpscare" width="400" />
        <audio id="jumpscareAudio" src="https://example.com/sound jumpscare.mp3"></audio>
    </div>

    <script>
        document.getElementById('jumpButton').addEventListener('click', function() {
            // Menampilkan gambar jumpscare
            const jumpscareImage = document.getElementById('jumpscareImage');
            jumpscareImage.style.display = 'block';

            // Memutar suara jumpscare
            const jumpscareAudio = document.getElementById('jumpscareAudio');
            jumpscareAudio.play();

            // Menyembunyikan gambar setelah 2 detik
            setTimeout(() => {
                jumpscareImage.style.display = 'none';
            }, 2000);
        });
    </script>
</body>
</html>
