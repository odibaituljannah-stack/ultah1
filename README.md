Selamat Ulang Tahun Aulia 
<html lang="id">

<head>

    <meta charset="UTF-8">

    <meta name="viewport"
          content="width=device-width, initial-scale=1.0">

    <title>Untuk Kamu</title>

    <style>

        /* =========================================
           DASAR
        ========================================= */

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {

            font-family:
                "Segoe UI",
                Arial,
                sans-serif;

            min-height: 100vh;

            overflow: hidden;

            color: #0b3954;

            background:
                linear-gradient(
                    135deg,
                    #0b3954 0%,
                    #087e8b 45%,
                    #dce7e7 70%,
                    #f4ead5 100%
                );

        }


        /* =========================================
           HALAMAN
        ========================================= */

        .page {

            position: fixed;

            inset: 0;

            display: none;

            justify-content: center;

            align-items: center;

            text-align: center;

            padding: 25px;

            animation:
                pageIn 0.8s ease;

        }


        .page.active {

            display: flex;

        }


        @keyframes pageIn {

            from {

                opacity: 0;

                transform:
                    scale(0.92)
                    translateY(20px);

            }

            to {

                opacity: 1;

                transform:
                    scale(1)
                    translateY(0);

            }

        }


        /* =========================================
           CARD
        ========================================= */

        .card {

            position: relative;

            width:
                min(92%, 520px);

            max-height: 90vh;

            overflow-y: auto;

            padding:
                40px 28px;

            border-radius: 32px;

            background:
                rgba(244, 234, 213, 0.93);

            border:
                2px solid
                rgba(255,255,255,0.7);

            box-shadow:
                0 25px 70px
                rgba(0,0,0,0.25);

            backdrop-filter:
                blur(10px);

        }


        /* =========================================
           JUDUL
        ========================================= */

        h1 {

            color: #0b3954;

            font-size:
                clamp(2rem, 8vw, 3rem);

            margin-bottom: 18px;

            letter-spacing: 1px;

        }


        h2 {

            color: #087e8b;

            font-size: 1.7rem;

            margin-bottom: 18px;

        }


        p {

            color: #294c60;

            font-size: 1.05rem;

            line-height: 1.8;

            margin-bottom: 22px;

        }


        /* =========================================
           TOMBOL
        ========================================= */

        button {

            border: none;

            padding:
                14px 30px;

            border-radius: 50px;

            background:
                #0b3954;

            color:
                #f4ead5;

            font-size: 1rem;

            font-weight: bold;

            cursor: pointer;

            box-shadow:
                0 8px 20px
                rgba(11,57,84,0.25);

            transition:
                all 0.3s ease;

        }


        button:hover {

            transform:
                translateY(-4px)
                scale(1.04);

            background:
                #087e8b;

        }


        button:active {

            transform:
                scale(0.96);

        }


        /* =========================================
           STIKER NAILONG
        ========================================= */

        .nailong {

            width:
                150px;

            max-width:
                45vw;

            height:
                auto;

            object-fit:
                contain;

            margin:
                0 auto 20px;

            display:
                block;

            filter:
                drop-shadow(
                    0 10px 10px
                    rgba(0,0,0,0.18)
                );

            animation:
                nailongFloat
                3s
                ease-in-out
                infinite;

        }


        @keyframes nailongFloat {

            0%,
            100% {

                transform:
                    translateY(0)
                    rotate(-2deg);

            }

            50% {

                transform:
                    translateY(-10px)
                    rotate(2deg);

            }

        }


        /* =========================================
           NAILONG SAMPING
        ========================================= */

        .nailong-side {

            position:
                fixed;

            width:
                120px;

            z-index:
                5;

            pointer-events:
                none;

            filter:
                drop-shadow(
                    0 8px 8px
                    rgba(0,0,0,0.15)
                );

        }


        .nailong-left {

            left:
                -15px;

            bottom:
                20px;

            animation:
                sideFloatLeft
                4s
                ease-in-out
                infinite;

        }


        .nailong-right {

            right:
                -15px;

            top:
                35px;

            animation:
                sideFloatRight
                4s
                ease-in-out
                infinite;

        }


        @keyframes sideFloatLeft {

            0%,
            100% {
                transform:
                    rotate(-8deg)
                    translateY(0);
            }

            50% {
                transform:
                    rotate(5deg)
                    translateY(-12px);
            }

        }


        @keyframes sideFloatRight {

            0%,
            100% {
                transform:
                    rotate(8deg)
                    translateY(0);
            }

            50% {
                transform:
                    rotate(-5deg)
                    translateY(12px);
            }

        }


        /* =========================================
           FOTO
        ========================================= */

        .photo {

            width:
                220px;

            height:
                220px;

            object-fit:
                cover;

            border-radius:
                24px;

            border:
                8px solid
                #f4ead5;

            outline:
                3px solid
                #0b3954;

            margin-bottom:
                25px;

            box-shadow:
                0 15px 35px
                rgba(0,0,0,0.2);

            transform:
                rotate(-2deg);

            transition:
                0.4s;

        }


        .photo:hover {

            transform:
                rotate(2deg)
                scale(1.03);

        }


        /* =========================================
           DEKORASI LINGKARAN
        ========================================= */

        .circle {

            position:
                fixed;

            border-radius:
                50%;

            pointer-events:
                none;

            opacity:
                0.15;

        }


        .circle.one {

            width:
                300px;

            height:
                300px;

            background:
                #f4ead5;

            top:
                -100px;

            left:
                -100px;

        }


        .circle.two {

            width:
                350px;

            height:
                350px;

            background:
                #0b3954;

            bottom:
                -150px;

            right:
                -120px;

        }


        /* =========================================
           MUSIK
        ========================================= */

        .music-btn {

            position:
                fixed;

            top:
                18px;

            right:
                18px;

            z-index:
                1000;

            width:
                48px;

            height:
                48px;

            padding:
                0;

            border-radius:
                50%;

            background:
                #f4ead5;

            color:
                #0b3954;

            font-size:
                20px;

            border:
                2px solid
                rgba(255,255,255,0.8);

        }


        /* =========================================
           CONFETTI
        ========================================= */

        #confetti {

            position:
                fixed;

            inset:
                0;

            width:
                100%;

            height:
                100%;

            pointer-events:
                none;

            z-index:
                999;

        }


        /* =========================================
           TYPING
        ========================================= */

        .typing {

            min-height:
                180px;

            text-align:
                left;

            background:
                rgba(255,255,255,0.45);

            padding:
                20px;

            border-radius:
                20px;

            border-left:
                5px solid
                #087e8b;

        }


        /* =========================================
           HALAMAN TERAKHIR
        ========================================= */

        .final-text {

            font-size:
                1.15rem;

            font-weight:
                500;

        }


        .signature {

            margin-top:
                20px;

            font-style:
                italic;

            color:
                #087e8b;

        }


        /* =========================================
           RESPONSIVE HP
        ========================================= */

        @media
        (max-width: 600px) {

            .card {

                padding:
                    30px 20px;

            }

            .nailong {

                width:
                    125px;

            }

            .nailong-side {

                width:
                    85px;

            }

            .photo {

                width:
                    190px;

                height:
                    190px;

            }

            p {

                font-size:
                    0.98rem;

            }

        }

    </style>

</head>


<body>
<!-- Background Nailong -->
<div class="nailong-background"></div>
.nailong-background {
    position: fixed;
    inset: 0;
    z-index: 0;
    pointer-events: none;
    overflow: hidden;

    opacity: 0.08;

    background-image: url("kita.jpeg");
    background-repeat: repeat;
    background-size: 140px 140px;
    background-position: center;
    transform: rotate(-5deg) scale(1.1);
}

<!-- =========================================
     DEKORASI BACKGROUND
========================================= -->

<div class="circle one"></div>

<div class="circle two"></div>


<!-- =========================================
     STIKER NAILONG SAMPING
     
     Kamu bisa ganti file:
     nailong4.png
     nailong5.png
========================================= -->



<!-- =========================================
     MUSIK
     
     Ganti musik.mp3 dengan lagu kamu
========================================= -->

<audio
    id="music"
    loop
>

    <source
        src="musik.mp3"
        type="audio/mpeg"
    >

</audio>


<button
    class="music-btn"
    onclick="toggleMusic()"
    id="musicButton"
>
    ♪
</button>


<!-- =========================================
     CANVAS CONFETTI
========================================= -->

<canvas id="confetti"></canvas>



<!-- =========================================
     PAGE 1
========================================= -->

<section
    class="page active"
    id="page1"
>

    <div class="card">

        <img
            src="nailong1.png"
            class="nailong"
            alt="Nailong"
        >

        <h1>
            Hai, sayanggg....
        </h1>

        <p>
            Aku punya sesuatu yang udah
            aku siapin khusus buat kamu.
        </p>

        <p>
            Tapi kayaknya kamu harus klik
            beberapa tombol dulu deh wkwk
        </p>

        <button
            onclick="nextPage()"
        >
            Mulai →
        </button>

    </div>

</section>



<!-- =========================================
     PAGE 2
========================================= -->

<section
    class="page"
    id="page2"
>

    <div class="card">

        <img
            src="nailong2.png"
            class="nailong"
            alt="Nailong"
        >

        <h2>
            Aku buat sesuatu buat kamu
        </h2>

        <p>
            Gak mahal sih, bukan sesuatu yang mewah juga
        <p>
            Malah rada alay mungkin,
            tapi aku buatnya dengan
            banyak waktu dan rada
            malu juga sih 😅
        </p>

        <button
            onclick="nextPage()"
        >
            Buka →
        </button>

    </div>

</section>



<!-- =========================================
     PAGE 3
========================================= -->

<section
    class="page"
    id="page3"
>

    <div class="card">

        <img
            src="foto-kalian.jpg"
            class="photo"
            alt="Foto kita"
        >

        <img
            src="nailong3.png"
            class="nailong"
            alt="Nailong"
        >

        <h2>
            Ini kita.
        </h2>

        <p>
            Dari sekian banyak orang
            yang ada di dunia,
            aku bersyukur bisa ketemu
            kamu.
        </p>

        <button
            onclick="nextPage()"
        >
            Lanjut →
        </button>

    </div>

</section>



<!-- =========================================
     PAGE 4
========================================= -->

<section
    class="page"
    id="page4"
>

    <div class="card">

        <img
            src="nailong4.png"
            class="nailong"
            alt="Nailong"
        >

        <h2>
            Tapi tunggu...
        </h2>

        <p>
            Ada satu hal yang sebenernya
            pengen banget aku sampein
            hari ini
        </p>

        <p>
            Jadi...
            jangan di-skip yakkk 😁

        <p>
            Aku bakal marah banget kalo di skip
        </p>

        <button
            onclick="nextPage()"
        >
            Aku siap →
        </button>

    </div>

</section>



<!-- =========================================
     PAGE 5
     UCAPAN UTAMA
========================================= -->

<section
    class="page"
    id="page5"
>

    <div class="card">

        <img
            src="nailong5.png"
            class="nailong"
            alt="Nailong"
        >

        <h1>
            SELAMAT
            <br>
            ULANG TAHUN!
        </h1>

        <h2>
            Putri Aulia Fauziah 🥳🎂
        </h2>

        <p
            id="typingText"
            class="typing"
        ></p>

        <button
            onclick="nextPage()"
        >
            Masih ada lagi. Sabar yaa →
        </button>

    </div>

</section>



<!-- =========================================
     PAGE 6
========================================= -->

<section
    class="page"
    id="page6"
>

    <div class="card">

        <img
            src="nailong2.png"
            class="nailong"
            alt="Nailong"
        >

        <h2>
            Makasih banget, udah hadir
        </h2>

        <p>
            Makasih banget karna udah
            jadi bagian dari hidup aku
        </p>

        <p>
            Makasih banget untuk semua
            cerita, tawa, perhatian,
            kesabaran (meskipun dikit hehe), 
            dan waktu yang udah kita lewati
        </p>

        <p>
            Aku mungkin belum sempurna,
            tapi aku akan selalu berusaha
            menjadi seseorang yang bisa
            membuat kamu merasa dihargai
        </p>

        <button
            onclick="nextPage()"
        >
            Satu pesan terakhir →
        </button>

    </div>

</section>



<!-- =========================================
     PAGE 7
========================================= -->

<section
    class="page"
    id="page7"
>

    <div class="card">

        <img
            src="nailong1.png"
            class="nailong"
            alt="Nailong"
        >

        <h1>
            Untuk kamu.
        </h1>

        <p class="final-text">

            Semoga di usia yang baru,
            semua hal baik datang
            satu per satu kepada kamu.

        </p>

        <p class="final-text">

            Semoga kamu selalu sehat,
            bahagia, dimudahkan dalam
            segala urusan, dan bisa
            mencapai semua hal
            yang kamu impikan.

        </p>

        <p class="final-text">

            Dan kalau boleh aku berharap,
            semoga aku masih bisa menjadi
            bagian dari banyak cerita
            indah dalam hidup kamu
            Aamiinnn....

        </p>

        <h2>
            Selamat ulang tahun sayang 🎂🥳
        </h2>

        <p class="signature">

            — dari Odi Bangun Pangestu
            

        </p>

        <button
            onclick="restart()"
        >
            Mulai lagi ↻
        </button>

    </div>

</section>



<script>


/* =========================================
   SISTEM HALAMAN
========================================= */

let currentPage = 1;


function nextPage() {

    const oldPage =
        document.getElementById(
            "page" + currentPage
        );

    oldPage.classList.remove(
        "active"
    );


    currentPage++;


    const newPage =
        document.getElementById(
            "page" + currentPage
        );

    newPage.classList.add(
        "active"
    );


    /* Mulai musik */

    const music =
        document.getElementById(
            "music"
        );

    if (
        music.paused
    ) {

        music.play()
        .catch(() => {});

    }


    /* Confetti */

    if (
        currentPage === 5
    ) {

        startConfetti();

        typeText();

    }

}



/* =========================================
   MUSIK
========================================= */

function toggleMusic() {

    const music =
        document.getElementById(
            "music"
        );

    const button =
        document.getElementById(
            "musicButton"
        );


    if (
        music.paused
    ) {

        music.play();

        button.innerHTML =
            "Ⅱ";

    }

    else {

        music.pause();

        button.innerHTML =
            "♪";

    }

}



/* =========================================
   TYPING EFFECT
========================================= */

const message = `

Semoga semua hal baik selalu
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

Love youuu, Auliaaa....🥰

`;


let typingStarted = false;


function typeText() {

    if (
        typingStarted
    ) {

        return;

    }


    typingStarted = true;


    const element =
        document.getElementById(
            "typingText"
        );


    let index = 0;


    function type() {

        if (
            index <
            message.length
        ) {

            const character =
                message.charAt(
                    index
                );


            if (
                character ===
                "\n"
            ) {

                element.innerHTML +=
                    "<br>";

            }

            else {

                element.innerHTML +=
                    character;

            }


            index++;


            setTimeout(
                type,
                30
            );

        }

    }


    type();

}



/* =========================================
   CONFETTI
========================================= */

const canvas =
    document.getElementById(
        "confetti"
    );


const ctx =
    canvas.getContext(
        "2d"
    );


let confettiPieces = [];


const confettiColors = [

    "#0b3954",

    "#087e8b",

    "#5fa8d3",

    "#f4ead5",

    "#d9c7a5",

    "#ffffff"

];


function resizeCanvas() {

    canvas.width =
        window.innerWidth;

    canvas.height =
        window.innerHeight;

}


window.addEventListener(
    "resize",
    resizeCanvas
);


resizeCanvas();



function startConfetti() {

    confettiPieces = [];


    for (
        let i = 0;
        i < 180;
        i++
    ) {

        confettiPieces.push({

            x:
                Math.random()
                *
                canvas.width,

            y:
                -Math.random()
                *
                canvas.height,

            width:
                Math.random()
                * 8
                + 4,

            height:
                Math.random()
                * 12
                + 6,

            speed:
                Math.random()
                * 4
                + 2,

            rotation:
                Math.random()
                * 360,

            rotationSpeed:
                Math.random()
                * 8
                - 4,

            color:
                confettiColors[
                    Math.floor(
                        Math.random()
                        *
                        confettiColors.length
                    )
                ]

        });

    }


    animateConfetti();

}



function animateConfetti() {

    ctx.clearRect(
        0,
        0,
        canvas.width,
        canvas.height
    );


    confettiPieces.forEach(
        piece => {

            piece.y +=
                piece.speed;

            piece.rotation +=
                piece.rotationSpeed;


            ctx.save();


            ctx.translate(
                piece.x,
                piece.y
            );


            ctx.rotate(
                piece.rotation
                *
                Math.PI
                /
                180
            );


            ctx.fillStyle =
                piece.color;


            ctx.fillRect(

                -piece.width / 2,

                -piece.height / 2,

                piece.width,

                piece.height

            );


            ctx.restore();

        }
    );


    confettiPieces =
        confettiPieces.filter(
            piece =>
                piece.y <
                canvas.height + 30
        );


    if (
        confettiPieces.length
        > 0
    ) {

        requestAnimationFrame(
            animateConfetti
        );

    }

}



/* =========================================
   RESTART
========================================= */

function restart() {

    location.reload();

}


</script>

</body>

</html>
