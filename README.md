<html lang="id">
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
    }

    h1 {
      font-size: 2rem;
      margin-bottom: 1rem;
      color: #d63384;
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
    }

    .audio-player {
      margin-top: 2rem;
    }

    #countdownTimer {
      font-size: 2rem;
      margin-top: 1rem;
      color: #e83e8c;
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

      #countdownTimer {
        font-size: 1.5rem;
      }
    }
  </style>
</head>
<body>
  <!-- Gambar background -->
  <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/f113152d-bde5-4710-a383-3bf6448cfd59.png" alt="Background" class="background-image" id="bgImage" />

  <div class="container">
    <!-- Countdown -->
    <div id="countdown">
      <h2 style="color: #007bff;">ADEK-KECILKU</h2>
      <p style="color: #d63384;">Kok dibuka lagi sih?, kan aku bilang nanti, ganurut banget deh👊.</p>
      <p style="color: purple; font-weight: bold;">BUKANYA NANTI YAH PAS JAM 00:01 WIB, 24 Juli 2025</p>
      <p style="color: #6f42c1;">Waktu tersisa:</p>
      <div id="countdownTimer">00:00:00</div>
    </div>

    <!-- Konten ucapan ulang tahun -->
    <div class="birthday-content" id="birthdayContent" style="display: none;">
      <img src="fotonajwa.jpg" alt="Najwa Alya Shafarina" style="width: 200px; border-radius: 50%; margin-bottom: 20px; box-shadow: 0 4px 10px rgba(0,0,0,0.2);">
      <h1>Selamat Ulang Tahun, Najwa Alya Shafarina yang ke-20!</h1>
      <p>yang pengen banget diklingiin, di igoin, digemesin, disayangin, dikissin.</p>
      <div class="audio-player">
        <button id="playButton">Putar Musik</button>
        <audio id="birthdayAudio" src="Karolina.mp3"></audio>
      </div>
    </div>
  </div>

<script>
  // Target: 24 Juli 2025 pukul 00:01 WIB
const targetDate = new Date("2025-07-24T00:01:00+07:00");

  const countdownEl = document.getElementById('countdownTimer');
  const countdownContainer = document.getElementById('countdown');
  const birthdayContent = document.getElementById('birthdayContent');
  const bgImage = document.getElementById('bgImage');

  function pad(num) {
    return num < 10 ? '0' + num : num;
  }

  function updateCountdown() {
    const now = new Date().getTime();
    const distance = targetDate.getTime() - now;

    if (distance <= 0) {
      countdownContainer.style.display = 'none';
      birthdayContent.style.display = 'block';
      bgImage.classList.add('active');
    } else {
      const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
      const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
      const seconds = Math.floor((distance % (1000 * 60)) / 1000);
      countdownEl.innerHTML = `${pad(hours)}:${pad(minutes)}:${pad(seconds)}`;
    }
  }

  updateCountdown();
  setInterval(updateCountdown, 1000);

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
</script>
</body>
</html>
