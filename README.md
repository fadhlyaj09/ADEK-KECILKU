<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Ucapan Ulang Tahun Najwa Alya Shafarina</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    }

    body {
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
      background-color: #f8f9fa;
      color: #333;
      overflow-x: hidden;
      transition: background 0.5s ease;
      text-align: center;
    }

    .container {
      width: 90%;
      max-width: 800px;
      text-align: center;
      padding: 2rem;
      background-color: rgba(255, 255, 255, 0.9);
      border-radius: 15px;
      box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
      position: relative;
      z-index: 1;
      overflow: hidden;
    }

    .countdown {
      animation: fadeIn 1s ease-in-out;
    }

    .birthday-content {
      display: none;
      animation: fadeIn 2s ease-in-out;
    }

    h1 {
      font-size: 2rem;
      margin-bottom: 1rem;
      color: #d63384;
      text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.1);
    }

    p {
      font-size: 1.2rem;
      margin-bottom: 2rem;
      line-height: 1.6;
    }

    .background-image {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      object-fit: cover;
      z-index: -1;
      opacity: 0;
      transition: opacity 0.8s ease;
    }

    .background-image.active {
      opacity: 0.3;
    }

    button {
      background-color: #d63384;
      color: white;
      border: none;
      padding: 12px 24px;
      font-size: 1rem;
      border-radius: 50px;
      cursor: pointer;
      transition: all 0.3s ease;
      box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    }

    button:hover {
      background-color: #c2256e;
      transform: translateY(-2px);
      box-shadow: 0 6px 8px rgba(0, 0, 0, 0.15);
    }

    .audio-player {
      margin-top: 2rem;
    }

    @keyframes fadeIn {
      from {
        opacity: 0;
        transform: translateY(20px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    @media (max-width: 768px) {
      h1 {
        font-size: 1.5rem;
      }

      p {
        font-size: 1rem;
      }

      button {
        padding: 10px 20px;
        font-size: 0.9rem;
      }
    }
  </style>
</head>
<body>
  <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/f113152d-bde5-4710-a383-3bf6448cfd59.png" alt="Background" class="background-image" id="bgImage" />

  <div class="container">
    <div class="countdown" id="countdown">
      <h1>Gasabaran banget si lo, kan gue bilang nnti.<br>
      Website ini hanya bisa diakses mulai pukul 15:40 WIB, 20 Juli 2025</h1>
    </div>

    <div class="birthday-content" id="birthdayContent">
      <img src="fotonajwa.jpg" alt="Najwa Alya Shafarina" style="width: 200px; border-radius: 50%; margin-bottom: 20px; box-shadow: 0 4px 10px rgba(0,0,0,0.2);">
      <h1>Selamat Ulang Tahun, Najwa Alya Shafarina yang ke-20!</h1>
      <p>yang pengen banget diklingiin, di igoin, digemesin, disayangin.</p>
      <div class="audio-player">
        <button id="playButton">Putar Musik</button>
        <audio id="birthdayAudio" src="songnajwa.mp3"></audio>
      </div>
    </div>
  </div>

  <script>
    const targetDate = new Date('July 20, 2025 18:40:00 GMT+0700');

    function checkTime() {
      const now = new Date();

      if (now >= targetDate) {
        document.getElementById('countdown').style.display = 'none';
        document.getElementById('birthdayContent').style.display = 'block';
        document.getElementById('bgImage').classList.add('active');
      } else {
        document.getElementById('countdown').style.display = 'block';
        document.getElementById('birthdayContent').style.display = 'none';
        document.getElementById('bgImage').classList.remove('active');
      }
    }

    const playButton = document.getElementById('playButton');
    const audio = document.getElementById('birthdayAudio');
    let isPlaying = false;

    playButton.addEventListener('click', function () {
      if (isPlaying) {
        audio.pause();
        playButton.textContent = 'Putar Musik';
      } else {
        audio.play();
        playButton.textContent = 'Berhenti';
      }
      isPlaying = !isPlaying;
    });

    checkTime();
    setInterval(checkTime, 60000);
  </script>
</body>
</html>
