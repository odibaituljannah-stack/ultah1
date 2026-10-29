

<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Untuk Kamu ❤️</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: "Segoe UI", Arial, sans-serif;
            min-height: 100vh;
            overflow: hidden;
            color: #0b3954;
            background: linear-gradient(
                135deg, #0b3954, #087e8b, #dce7e7, #f4ead5
            );
        }

        /* BACKGROUND NAILONG BERULANG */
        .nailong-background {
            position: fixed;
            inset: -20px;
            z-index: 0;
            pointer-events: none;
            background-image: url("kita.jpeg");
            background-repeat: repeat;
            background-size: 140px 140px;
            background-position: center;
            opacity: 0.12;
            transform: rotate(-3deg) scale(1.05);
        }

        .circle {
            position: fixed;
            border-radius: 50%;
            pointer-events: none;
            opacity: 0.15;
            z-index: 1;
        }

        .circle.one {
            width: 300px;
            height: 300px;
            background: #f4ead5;
            top: -100px;
            left: -100px;
        }

        .circle.two {
            width: 350px;
            height: 350px;
            background: #0b3954;
            bottom: -150px;
            right: -120px;
        }

        /* HALAMAN */
        .page {
            position: fixed;
            inset: 0;
            z-index: 2;
            display: none;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 20px;
            animation: pageIn 0.6s ease;
        }

        .page.active {
            display: flex;
        }

        @keyframes pageIn {
            from {
                opacity: 0;
                transform: scale(0.96) translateY(12px);
            }
            to {
                opacity: 1;
                transform: scale(1) translateY(0);
            }
        }

        /* KARTU */
        .card {
            position: relative;
            width: min(92vw, 520px);
            max-height: 88vh;
            overflow-y: auto;
            padding: 32px 25px;
            border-radius: 30px;
            background: rgba(244, 234, 213, 0.95);
            border: 2px solid rgba(255, 255, 255, 0.75);
            box-shadow: 0 25px 70px rgba(0, 0, 0, 0.25);
            backdrop-filter: blur(8px);
        }

        h1 {
            color: #0b3954;
            font-size: clamp(2rem, 8vw, 3rem);
            margin-bottom: 18px;
            letter-spacing: 1px;
        }

        h2 {
            color: #087e8b;
            font-size: clamp(1.3rem, 5vw, 1.7rem);
            margin-bottom: 18px;
        }

        p {
            color: #294c60;
            font-size: 1.02rem;
            line-height: 1.8;
            margin-bottom: 18px;
        }

        /* TOMBOL */
        button {
            border: none;
            padding: 14px 26px;
            border-radius: 50px;
            background: #0b3954;
            color: #f4ead5;
            font-size: 1rem;
            font-weight: bold;
            cursor: pointer;
            box-shadow: 0 8px 20px rgba(11, 57, 84, 0.25);
            transition: 0.3s ease;
        }

        button:hover {
            transform: translateY(-3px) scale(1.03);
            background: #087e8b;
        }

        /* STIKER */
        .nailong {
            display: block;
            width: 145px;
            max-width: 45vw;
            height: auto;
            object-fit: contain;
            margin: 0 auto 18px;
            filter: drop-shadow(0 8px 8px rgba(0, 0, 0, 0.15));
            animation: float 3s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0) rotate(-2deg); }
            50% { transform: translateY(-9px) rotate(2deg); }
        }

        /* FOTO */
        .photo {
            width: 210px;
            height: 210px;
            max-width: 65vw;
            object-fit: cover;
            border-radius: 24px;
            border: 7px solid #f4ead5;
            outline: 3px solid #0b3954;
            margin-bottom: 22px;
            box-shadow: 0 12px 30px rgba(0, 0, 0, 0.2);
            transform: rotate(-2deg);
            transition: 0.3s;
        }

        .photo:hover {
            transform: rotate(2deg) scale(1.03);
        }

        /* MUSIK */
        .music-btn {
            position: fixed;
            z-index: 20;
            top: 15px;
            right: 15px;
            width: 48px;
            height: 48px;
            padding: 0;
            border-radius: 50%;
            background: #f4ead5;
            color: #0b3954;
            border: 2px solid white;
            font-size: 20px;
        }

        /* CONFETTI */
        #confetti {
            position: fixed;
            inset: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 15;
        }

        /* UCAPAN MENGETIK */
        .typing {
            min-height: 180px;
            text-align: left;
            white-space: normal;
            overflow-wrap: anywhere;
            background: rgba(255, 255, 255, 0.5);
            padding: 18px;
            border-radius: 18px;
            border-left: 5px solid #087e8b;
            line-height: 1.7;
            margin-bottom: 20px;
        }

        .final-text {
            font-size: 1.05rem;
        }

        .signature {
            margin-top: 20px;
            font-style: italic;
            color: #087e8b;
        }

        @media (max-width: 600px) {
            .card {
                padding: 28px 20px;
                max-height: 84vh;
            }

            .nailong {
                width: 120px;
            }

            .photo {
                width: 175px;
                height: 175px;
            }

            p {
                font-size: 0.97rem;
            }

            .typing {
                min-height: 150px;
            }
        }
    </style>
</head>

<body>

    <!-- BACKGROUND -->
    <div class="nailong-background"></div>
    <div class="circle one"></div>
    <div class="circle two"></div>

    <!-- MUSIK -->
    <audio id="music" loop>
        <source src="musik.mp3" type="audio/mpeg">
    </audio>

    <button class="music-btn" id="musicButton"
            onclick="toggleMusic()" aria-label="Putar atau jeda musik">
        ♪
    </button>

    <!-- CONFETTI -->
    <canvas id="confetti"></canvas>

    <!-- HALAMAN 1 -->
    <section class="page active" id="page1">
        <div class="card">
            <img src="nailong1.png" class="nailong" alt="Nailong">
            <h1>Hai, sayanggg....</h1>
            <p>Aku punya sesuatu yang udah aku siapin khusus buat kamu.</p>
            <p>Tapi kayaknya kamu harus klik beberapa tombol dulu deh wkwk.</p>
            <button onclick="nextPage()">Mulai →</button>
        </div>
    </section>

    <!-- HALAMAN 2 -->
    <section class="page" id="page2">
        <div class="card">
            <img src="nailong2.png" class="nailong" alt="Nailong">
            <h2>Aku buat sesuatu buat kamu</h2>
            <p>Gak mahal sih, bukan sesuatu yang mewah juga.</p>
            <p>Malah rada alay mungkin, tapi aku buatnya dengan banyak waktu dan rada malu juga sih 😅</p>
            <button onclick="nextPage()">Buka →</button>
        </div>
    </section>

    <!-- HALAMAN 3 -->
    <section class="page" id="page3">
        <div class="card">
            <img src="foto-kita.jpeg" class="photo" alt="Foto kita">
            <img src="nailong3.png" class="nailong" alt="Nailong">
            <h2>Ini kita.</h2>
            <p>Dari sekian banyak orang yang ada di dunia, aku bersyukur bisa ketemu kamu.</p>
            <button onclick="nextPage()">Lanjut →</button>
        </div>
    </section>

    <!-- HALAMAN 4 -->
    <section class="page" id="page4">
        <div class="card">
            <img src="nailong4.png" class="nailong" alt="Nailong">
            <h2>Tapi tunggu...</h2>
            <p>Ada satu hal yang sebenernya pengen banget aku sampein hari ini.</p>
            <p>Jadi... jangan di-skip yakkk 😁</p>
            <p>Aku bakal marah banget kalo di-skip.</p>
            <button onclick="nextPage()">Aku siap →</button>
        </div>
    </section>

    <!-- HALAMAN 5 -->
    <section class="page" id="page5">
        <div class="card">
            <img src="nailong5.png" class="nailong" alt="Nailong">
            <h1>SELAMAT<br>ULANG TAHUN!</h1>
            <h2>Putri Aulia Fauziah 🥳🎂</h2>
            <p id="typingText" class="typing"></p>
            <button onclick="nextPage()">Masih ada lagi. Sabar yaa →</button>
        </div>
    </section>

    <!-- HALAMAN 6 -->
    <section class="page" id="page6">
        <div class="card">
            <img src="nailong2.png" class="nailong" alt="Nailong">
            <h2>Makasih banget, udah hadir</h2>
            <p>Makasih banget karna udah jadi bagian dari hidup aku.</p>
            <p>Makasih banget untuk semua cerita, tawa, perhatian, kesabaran (meskipun dikit hehe), dan waktu yang udah kita lewati.</p>
            <p>Aku mungkin belum sempurna, tapi aku akan selalu berusaha menjadi seseorang yang bisa membuat kamu merasa dihargai.</p>
            <button onclick="nextPage()">Satu pesan terakhir →</button>
        </div>
    </section>

    <!-- HALAMAN 7 -->
    <section class="page" id="page7">
        <div class="card">
            <img src="nailong1.png" class="nailong" alt="Nailong">
            <h1>Untuk kamu.</h1>
            <p class="final-text">Semoga di usia yang baru, semua hal baik datang satu per satu kepada kamu.</p>
            <p class="final-text">Semoga kamu selalu sehat, bahagia, dimudahkan dalam segala urusan, dan bisa mencapai semua hal yang kamu impikan.</p>
            <p class="final-text">Dan kalau boleh aku berharap, semoga aku masih bisa menjadi bagian dari banyak cerita indah dalam hidup kamu. Aamiinnn....</p>
            <h2>Selamat ulang tahun sayang 🎂🥳</h2>
            <p class="signature">— dari Odi Bangun Pangestu</p>
            <button onclick="restart()">Mulai lagi ↻</button>
        </div>
    </section>

    <script>
        let currentPage = 1;
        let typingStarted = false;
        let confettiPieces = [];
        let confettiAnimationRunning = false;

        const music = document.getElementById("music");
        const musicButton = document.getElementById("musicButton");
        const typingElement = document.getElementById("typingText");
        const canvas = document.getElementById("confetti");
        const ctx = canvas.getContext("2d");

        const message = `Semoga semua hal baik selalu
menemukan jalan menuju kamu.

Semoga senyum kamu selalu
punya alasan untuk muncul.

Semoga langkah kamu selalu
dimudahkan.

Dan semoga semua impian
yang kamu simpan perlahan
bisa menjadi kenyataan.

Selamat ulang tahun.

Semoga tahun ini menjadi
salah satu tahun terbaik
dalam hidup kamu.

Love youuu, Auliaaa....🥰`;

        function nextPage() {
            const oldPage = document.getElementById("page" + currentPage);

            if (!oldPage || currentPage >= 7) return;

            oldPage.classList.remove("active");
            currentPage++;

            const newPage = document.getElementById("page" + currentPage);

            if (newPage) {
                newPage.classList.add("active");
            }

            // Browser hanya mengizinkan musik setelah interaksi pengguna.
            if (music.paused) {
                music.play()
                    .then(() => {
                        musicButton.textContent = "Ⅱ";
                    })
                    .catch(() => {
                        musicButton.textContent = "♪";
                    });
            }

            if (currentPage === 5) {
                startConfetti();
                typeText();
            }
        }

        function toggleMusic() {
            if (music.paused) {
                music.play()
                    .then(() => {
                        musicButton.textContent = "Ⅱ";
                    })
                    .catch(() => {
                        musicButton.textContent = "♪";
                        alert("Musik tidak bisa diputar. Periksa apakah file musik.mp3 tersedia.");
                    });
            } else {
                music.pause();
                musicButton.textContent = "♪";
            }
        }

        function typeText() {
            if (typingStarted || !typingElement) return;

            typingStarted = true;
            let index = 0;

            function type() {
                if (index < message.length) {
                    const character = message.charAt(index);

                    if (character === "\n") {
                        typingElement.appendChild(document.createElement("br"));
                    } else {
                        typingElement.appendChild(
                            document.createTextNode(character)
                        );
                    }

                    index++;
                    setTimeout(type, 30);
                }
            }

            type();
        }

        function resizeCanvas() {
            canvas.width = window.innerWidth;
            canvas.height = window.innerHeight;
        }

        window.addEventListener("resize", resizeCanvas);
        resizeCanvas();

        const confettiColors = [
            "#0b3954", "#087e8b", "#5fa8d3",
            "#f4ead5", "#d9c7a5", "#ffffff"
        ];

        function startConfetti() {
            confettiPieces = [];

            for (let i = 0; i < 180; i++) {
                confettiPieces.push({
                    x: Math.random() * canvas.width,
                    y: -Math.random() * canvas.height,
                    width: Math.random() * 8 + 4,
                    height: Math.random() * 12 + 6,
                    speed: Math.random() * 4 + 2,
                    rotation: Math.random() * 360,
                    rotationSpeed: Math.random() * 8 - 4,
                    color: confettiColors[
                        Math.floor(Math.random() * confettiColors.length)
                    ]
                });
            }

            if (!confettiAnimationRunning) {
                confettiAnimationRunning = true;
                animateConfetti();
            }
        }

        function animateConfetti() {
            ctx.clearRect(0, 0, canvas.width, canvas.height);

            confettiPieces.forEach(piece => {
                piece.y += piece.speed;
                piece.rotation += piece.rotationSpeed;

                ctx.save();
                ctx.translate(piece.x, piece.y);
                ctx.rotate(piece.rotation * Math.PI / 180);
                ctx.fillStyle = piece.color;
                ctx.fillRect(
                    -piece.width / 2,
                    -piece.height / 2,
                    piece.width,
                    piece.height
                );
                ctx.restore();
            });

            confettiPieces = confettiPieces.filter(
                piece => piece.y < canvas.height + 30
            );

            if (confettiPieces.length > 0) {
                requestAnimationFrame(animateConfetti);
            } else {
                confettiAnimationRunning = false;
                ctx.clearRect(0, 0, canvas.width, canvas.height);
            }
        }

        function restart() {
            location.reload();
        }
    </script>

</body>
</html>
