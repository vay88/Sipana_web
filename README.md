# Sipana_web
Milik sipana
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Selamat Ulang Tahun Sipana! ❤️🎉</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css" rel="stylesheet">
    <style>
        .clip-heart {
            clip-path: polygon(50% 0%, 100% 38%, 82% 100%, 50% 75%, 18% 100%, 0% 38%);
        }

        .clip-star {
            clip-path: polygon(50% 0%, 61% 35%, 98% 35%, 68% 57%, 79% 91%, 50% 70%, 21% 91%, 32% 57%, 2% 35%, 39% 35%);
        }

        @keyframes animate-heart {
            0% { transform: translateY(0) rotate(0deg); opacity: 1; }
            100% { transform: translateY(-800px) rotate(720deg); opacity: 0; }
        }

        @keyframes animate-star {
            0% { transform: translateY(0) rotate(0deg); opacity: 1; }
            100% { transform: translateY(-800px) rotate(720deg); opacity: 0; }
        }

        .animate-heart-1 { left: 25%; animation: animate-heart 5s linear infinite; animation-delay: 0s; }
        .animate-heart-2 { left: 10%; animation: animate-heart 5s linear infinite; animation-delay: 2s; }
        .animate-heart-3 { left: 70%; animation: animate-heart 5s linear infinite; animation-delay: 4s; }
        .animate-heart-4 { left: 50%; animation: animate-heart 5s linear infinite; animation-delay: 6s; }
        .animate-heart-5 { left: 85%; animation: animate-heart 5s linear infinite; animation-delay: 8s; }

        .animate-star-1 { left: 5%; animation: animate-star 6s linear infinite; animation-delay: 1s; }
        .animate-star-2 { left: 20%; animation: animate-star 7s linear infinite; animation-delay: 3s; }
        .animate-star-3 { left: 75%; animation: animate-star 8s linear infinite; animation-delay: 5s; }
        .animate-star-4 { left: 90%; animation: animate-star 9s linear infinite; animation-delay: 7s; }
        .animate-star-5 { left: 40%; animation: animate-star 10s linear infinite; animation-delay: 9s; }

        @keyframes typing {
            from { width: 0; }
            to { width: 100%; }
        }
        .typing-effect {
            overflow: hidden;
            white-space: nowrap;
            animation: typing 3s steps(40, end);
        }
    </style>
</head>
<body class="flex justify-center items-center h-screen bg-gradient-to-br from-pink-300 to-pink-100 overflow-hidden">
    <!-- Musik Latar Romantis -->
    <audio autoplay loop>
        <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mpeg">
        Browser Anda tidak mendukung elemen audio.
    </audio>

    <!-- Elemen Hati dan Bintang -->
    <div class="absolute top-0 left-0 w-full h-full overflow-hidden z-10">
        <span class="absolute block w-5 h-5 bg-red-400 clip-heart animate-heart-1"></span>
        <span class="absolute block w-5 h-5 bg-red-400 clip-heart animate-heart-2"></span>
        <span class="absolute block w-5 h-5 bg-red-400 clip-heart animate-heart-3"></span>
        <span class="absolute block w-5 h-5 bg-red-400 clip-heart animate-heart-4"></span>
        <span class="absolute block w-5 h-5 bg-red-400 clip-heart animate-heart-5"></span>
        <span class="absolute block w-5 h-5 bg-yellow-400 clip-star animate-star-1"></span>
        <span class="absolute block w-5 h-5 bg-yellow-400 clip-star animate-star-2"></span>
        <span class="absolute block w-5 h-5 bg-yellow-400 clip-star animate-star-3"></span>
        <span class="absolute block w-5 h-5 bg-yellow-400 clip-star animate-star-4"></span>
        <span class="absolute block w-5 h-5 bg-yellow-400 clip-star animate-star-5"></span>
    </div>

    <!-- Konten Utama -->
    <div class="container text-center bg-white bg-opacity-90 p-10 rounded-2xl shadow-lg relative z-20">
        <h1 class="text-4xl text-red-400 mb-4 typing-effect">Selamat Ulang Tahun, Sipana! ❤️🎉</h1>
        <p class="text-xl text-gray-700 mb-6">Semoga harimu penuh kebahagiaan, cinta, dan keberkahan!</p>

        <!-- Pesan dari Arsyad -->
        <div class="bg-pink-100 p-4 rounded-lg mb-6">
            <p class="text-lg text-gray-700">
                <span class="text-red-400 font-bold">Dari Arsyad:</span><br>
                "Happy Birthday, Sipana! Semoga kamu selalu bahagia dan sehat selalu. Jangan lupa main FF yok nanti, kita push rank bareng! 🎮🔥"
            </p>
        </div>

        <!-- Tombol Buka Kado -->
        <button class="bg-gradient-to-r from-red-400 to-pink-400 text-white py-3 px-6 text-lg rounded-lg hover:from-pink-400 hover:to-red-400 transition duration-300" id="kadoButton">
            Buka Kado 🎁
        </button>
        <div class="hidden mt-6" id="kado">
            <img alt="Gambar kado dengan cinta dan bulan" class="mx-auto" height="120" src="https://storage.googleapis.com/a1aa/image/3XgovxN3Zjns1ZNGlrCBDk9lPxEni574C5rd8kl7w64.jpg" width="120"/>
            <p class="text-xl text-red-400 mt-4">Ini hadiah spesial untukmu! ❤️🎉</p>
        </div>

        <!-- Countdown Timer -->
        <div class="mt-6">
            <p class="text-xl text-gray-700">Menuju ulang tahun berikutnya:</p>
            <div id="countdown" class="flex justify-center gap-4 mt-4">
                <span class="text-2xl text-red-400" id="days"></span>
                <span class="text-2xl text-red-400" id="hours"></span>
                <span class="text-2xl text-red-400" id="minutes"></span>
                <span class="text-2xl text-red-400" id="seconds"></span>
            </div>
        </div>

        <!-- Tombol ID Free Fire Arsyad -->
        <div class="mt-6">
            <button class="bg-gradient-to-r from-blue-500 to-purple-500 text-white py-2 px-4 rounded-lg hover:from-purple-500 hover:to-blue-500 transition duration-300" id="idButton">
                Lihat ID Free Fire Arsyad 🎮
            </button>
            <div class="hidden mt-4" id="idArsyad">
                <p class="text-xl text-blue-500">ID Arsyad: <span class="font-bold">8484813820</span></p>
                <p class="text-lg text-gray-700">Ayo add dan main bareng! 🎉</p>
            </div>
        </div>
    </div>

    <!-- Script untuk Konfeti -->
    <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.5.1/dist/confetti.browser.min.js"></script>
    <script>
        document.getElementById('kadoButton').addEventListener('click', function() {
            const kado = document.getElementById('kado');
            kado.classList.remove('hidden');
            kado.classList.add('visible');

            // Efek konfeti
            confetti({
                particleCount: 100,
                spread: 70,
                origin: { y: 0.6 }
            });
        });

        // Tampilkan ID Free Fire Arsyad
        document.getElementById('idButton').addEventListener('click', function() {
            const idArsyad = document.getElementById('idArsyad');
            idArsyad.classList.remove('hidden');
            idArsyad.classList.add('visible');
        });

        // Countdown Timer
        const countdownDate = new Date('2026-02-19').getTime();

        const updateCountdown = () => {
            const now = new Date().getTime();
            const distance = countdownDate - now;

            const days = Math.floor(distance / (1000 * 60 * 60 * 24));
            const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
            const seconds = Math.floor((distance % (1000 * 60)) / 1000);

            document.getElementById('days').innerText = `${days} Hari`;
            document.getElementById('hours').innerText = `${hours} Jam`;
            document.getElementById('minutes').innerText = `${minutes} Menit`;
            document.getElementById('seconds').innerText = `${seconds} Detik`;
        };

        setInterval(updateCountdown, 1000);
    </script>
</body>
</html>
