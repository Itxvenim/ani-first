<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Our Little Forever ❤️</title>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>

<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@400;500;600;700&family=Great+Vibes&family=Poppins:wght@300;400;500;600&display=swap" rel="stylesheet">

<style>

*{
    box-sizing:border-box;
    margin:0;
    padding:0;
}

html{
    scroll-behavior:smooth;
}

body{
    background:
        radial-gradient(circle at 20% 10%,rgba(255,105,150,.18),transparent 30%),
        radial-gradient(circle at 80% 30%,rgba(160,80,255,.12),transparent 30%),
        radial-gradient(circle at 50% 90%,rgba(255,80,120,.10),transparent 35%),
        #09060c;

    color:#fff;

    font-family:'Poppins',sans-serif;

    min-height:100vh;

    overflow-x:hidden;
}


/* BACKGROUND */

body::before{
    content:"";
    position:fixed;
    inset:0;

    background-image:
        radial-gradient(circle,rgba(255,255,255,.7) 1px,transparent 1px);

    background-size:75px 75px;

    opacity:.15;

    pointer-events:none;

    z-index:0;
}


/* FLOATING HEARTS */

.floating-heart{
    position:fixed;

    bottom:-50px;

    pointer-events:none;

    z-index:1;

    opacity:.7;

    animation:
        floatHeart linear forwards;
}

@keyframes floatHeart{

    0%{
        transform:translateY(0) rotate(0deg);
        opacity:0;
    }

    15%{
        opacity:.8;
    }

    100%{
        transform:
            translateY(-110vh)
            rotate(360deg);

        opacity:0;
    }
}


/* PAGES */

.page{
    display:none;

    min-height:100vh;

    width:100%;

    position:relative;

    z-index:2;

    padding:60px 20px;
}

.page.active{
    display:flex;

    align-items:center;
    justify-content:center;

    animation:
        pageIn .8s ease;
}

@keyframes pageIn{

    from{
        opacity:0;
        transform:translateY(25px);
    }

    to{
        opacity:1;
        transform:translateY(0);
    }
}


.container{

    width:100%;

    max-width:1050px;

    margin:auto;

    text-align:center;
}


/* TYPOGRAPHY */

.small-label{

    text-transform:uppercase;

    letter-spacing:5px;

    font-size:11px;

    color:#dca9bb;

    margin-bottom:18px;
}

.script{

    font-family:'Great Vibes',cursive;

    font-size:65px;

    color:#ffb5c9;

    line-height:1.1;

    text-shadow:
        0 0 25px rgba(255,100,150,.25);

}

.title{

    font-family:'Cormorant Garamond',serif;

    font-size:48px;

    font-weight:600;

    margin:18px 0;

}

.subtitle{

    max-width:650px;

    margin:0 auto 30px;

    color:#d9ccd2;

    font-size:15px;

    line-height:1.9;
}

.story-text{

    color:#ddd0d6;

    font-size:15px;

    line-height:2;

    max-width:780px;

    margin:0 auto 20px;
}


/* BUTTONS */

.btn-row{

    display:flex;

    justify-content:center;

    flex-wrap:wrap;

    gap:15px;

    margin-top:35px;
}

.btn{

    border:1px solid rgba(255,180,200,.3);

    background:
        linear-gradient(
            135deg,
            rgba(255,100,145,.25),
            rgba(150,80,180,.18)
        );

    color:white;

    padding:14px 25px;

    border-radius:50px;

    cursor:pointer;

    font-family:'Poppins',sans-serif;

    font-size:13px;

    transition:.3s;

    box-shadow:
        0 10px 30px rgba(0,0,0,.2);
}

.btn:hover{

    transform:translateY(-4px);

    border-color:#ffb5c9;

    box-shadow:
        0 10px 35px rgba(255,80,130,.2);
}

.btn.secondary{

    background:rgba(255,255,255,.04);

}


/* GLASS */

.glass{

    background:
        rgba(255,255,255,.045);

    border:
        1px solid rgba(255,255,255,.09);

    border-radius:28px;

    padding:35px;

    max-width:850px;

    margin:25px auto;

    backdrop-filter:blur(12px);

    box-shadow:
        0 25px 80px rgba(0,0,0,.3);
}


/* HERO */

.hero-heart{

    font-size:75px;

    margin-bottom:15px;

    animation:
        heartbeat 1.5s infinite;
}

@keyframes heartbeat{

    0%,100%{
        transform:scale(1);
    }

    20%{
        transform:scale(1.15);
    }

    40%{
        transform:scale(1);
    }

    60%{
        transform:scale(1.08);
    }
}


.date-badge{

    display:inline-block;

    padding:9px 18px;

    border-radius:30px;

    background:rgba(255,150,180,.08);

    border:1px solid rgba(255,180,200,.15);

    color:#e9b9c8;

    font-size:12px;

    letter-spacing:2px;

    margin:15px 0;
}


/* MEMORY CARDS */

.memory-grid{

    display:grid;

    grid-template-columns:
        repeat(2,1fr);

    gap:20px;

    margin-top:30px;
}

.memory-card{

    padding:28px;

    text-align:left;

    border-radius:24px;

    background:
        linear-gradient(
            145deg,
            rgba(255,255,255,.07),
            rgba(255,255,255,.025)
        );

    border:
        1px solid rgba(255,255,255,.08);

    transition:.35s;
}

.memory-card:hover{

    transform:
        translateY(-7px);

    border-color:
        rgba(255,170,195,.3);
}

.memory-icon{

    font-size:40px;

    margin-bottom:12px;
}

.memory-card h3{

    font-family:
        'Cormorant Garamond',
        serif;

    font-size:28px;

    margin-bottom:10px;
}

.memory-card p{

    color:#cfc2c9;

    line-height:1.8;

    font-size:13px;
}


/* DIVIDER */

.divider{

    height:1px;

    max-width:500px;

    margin:35px auto;

    background:
        linear-gradient(
            90deg,
            transparent,
            rgba(255,170,195,.5),
            transparent
        );
}


/* RESPONSIVE */

@media(max-width:700px){

    .page{
        padding:45px 16px;
    }

    .script{
        font-size:48px;
    }

    .title{
        font-size:37px;
    }

    .subtitle{
        font-size:14px;
    }

    .glass{
        padding:23px 18px;
        border-radius:22px;
    }

    .memory-grid{
        grid-template-columns:1fr;
    }

    .memory-card{
        padding:22px;
    }

    .btn{
        width:100%;
        max-width:300px;
    }

}


/* PAGE COUNTER */

.page-counter{

    position:fixed;

    bottom:18px;

    left:50%;

    transform:translateX(-50%);

    z-index:50;

    padding:7px 14px;

    border-radius:30px;

    background:rgba(0,0,0,.35);

    border:1px solid rgba(255,255,255,.08);

    color:#bdaeb5;

    font-size:10px;

    letter-spacing:2px;
}

</style>
</head>


<body>


<!-- =====================================================
     PAGE 1 — WELCOME / FIRST ANNIVERSARY
===================================================== -->

<section class="page active" id="page1">

<div class="container">

    <div class="hero-heart">
        ❤️
    </div>

    <div class="small-label">
        A little gift for my favorite person
    </div>

    <div class="script">
        Heyy Bubu...
    </div>

    <h1 class="title">
        Happy 1st Anniversary ❤️
    </h1>

    <div class="date-badge">
        ONE YEAR • ONE STORY • US
    </div>

    <p class="subtitle">

        Ye koi normal website nahi hai...

        <br>

        Ye humari story ka woh chota sa
        corner hai jahan humari memories,
        pagalpan, pyaar, fights aur
        woh saare moments hain
        jo mere liye bohat special hain.

        <br><br>

        So Bubu...

        <br>

        ready ho?

        ❤️

    </p>

    <div class="btn-row">

        <button
            class="btn"
            onclick="nextPage()"
        >
            Open My Gift ❤️
        </button>

    </div>

</div>

</section>



<!-- =====================================================
     PAGE 2 — 5 SEPTEMBER
===================================================== -->

<section class="page" id="page2">

<div class="container">

    <div class="small-label">
        Chapter One
    </div>

    <div class="script">
        It Started...
    </div>

    <h2 class="title">
        5 September ❤️
    </h2>

    <div class="glass">

        <div class="memory-icon">
            💬
        </div>

        <p class="story-text">

            5 September se baat start hui thi.

            <br><br>

            Shayad us waqt hum dono ko
            bilkul idea nahi tha ke
            ye normal si conversations
            ek din itni beautiful story
            ban jayengi.

            <br><br>

            Random baatein...

            <br>

            random jokes...

            <br>

            random moments...

            <br><br>

            Aur dheere dheere
            ek dusre ki aadat ban gayi.

        </p>

    </div>

    <div class="btn-row">

        <button
            class="btn secondary"
            onclick="prevPage()"
        >
            ← Back
        </button>

        <button
            class="btn"
            onclick="nextPage()"
        >
            Continue ❤️
        </button>

    </div>

</div>

</section>



<!-- =====================================================
     PAGE 3 — LUDO / POETRY / THUMAK THUMAK
===================================================== -->

<section class="page" id="page3">

<div class="container">

    <div class="small-label">
        The Random Era 😂
    </div>

    <div class="script">
        Thumak Thumak...
    </div>

    <h2 class="title">
        Dodi Dum 😭❤️
    </h2>

    <div class="glass">

        <p class="story-text">

            Thumak Thumak trend...

            <br><br>

            Dodi Dum hamara name
            GC mein rakhna...

            <br><br>

            Aur sab kuch itna
            unexpected tha. 😂

            <br><br>

            Us se pehle hum apas mein
            Ludo khelte thay...

            <br>

            poetry sunate thay...

            <br>

            bohat kuch karte thay...

            <br><br>

            Aur honestly...

            <br>

            maza aata tha.

            <br><br>

            Sakoon...

            <br>

            bass game ki der hoti thi. 🫠❤️

        </p>

    </div>

    <div class="memory-grid">

        <div class="memory-card">

            <div class="memory-icon">
                🎲
            </div>

            <h3>
                Ludo
            </h3>

            <p>
                Game choti hoti thi,
                lekin conversations
                kabhi choti nahi hoti thi. 😂
            </p>

        </div>

        <div class="memory-card">

            <div class="memory-icon">
                🎤
            </div>

            <h3>
                Poetry
            </h3>

            <p>
                Ek dusre ko poetry
                sunana aur phir
                random baaton mein
                kho jana. ❤️
            </p>

        </div>

    </div>

    <div class="btn-row">

        <button
            class="btn secondary"
            onclick="prevPage()"
        >
            ← Back
        </button>

        <button
            class="btn"
            onclick="nextPage()"
        >
            Next Memory ❤️
        </button>

    </div>

</div>

</section>



<!-- =====================================================
     PAGE 4 — PROPOSAL 29
===================================================== -->

<section class="page" id="page4">

<div class="container">

    <div class="small-label">
        The Moment Everything Changed
    </div>

    <div class="script">
        29...
    </div>

    <h2 class="title">
        Woh Ek Din ❤️
    </h2>

    <div class="glass">

        <div class="memory-icon">
            💌
        </div>

        <p class="story-text">

            29 ko proposal kiya tha.

            <br><br>

            Woh moment...

            <br>

            woh nervousness...

            <br>

            woh feeling ke pata nahi
            saamne se kya answer ayega...

            <br><br>

            Lekin phir...

            <br>

            humari story ne
            ek aur beautiful turn le liya.

            ❤️

        </p>

        <div class="divider"></div>

        <div class="script"
             style="font-size:48px;">

            And then there was us...

        </div>

    </div>

    <div class="btn-row">

        <button
            class="btn secondary"
            onclick="prevPage()"
        >
            ← Back
        </button>

        <button
            class="btn"
            onclick="nextPage()"
        >
            Next Chapter ❤️
        </button>

    </div>

</div>

</section>



<!-- =====================================================
     PAGE 5 — 14 MAY / RAIN / FIRST HAND HOLD
===================================================== -->

<section class="page" id="page5">

<div class="container">

    <div class="small-label">
        One of my favorite memories
    </div>

    <div class="script">
        Rainy Day 🌧️
    </div>

    <h2 class="title">
        14 May ❤️
    </h2>

    <div class="date-badge">
        THURSDAY • AROUND 1:15 PM
    </div>

    <div class="glass">

        <div class="memory-icon">
            🌧️🤝🏻
        </div>

        <p class="story-text">

            Thursday ko mile...

            <br><br>

            Duphar 1.15 ke qareeb.

            <br><br>

            Aur 14 date thi May ki.

            <br><br>

            Us din do baar barish hui.

            <br><br>

            Aur phir...

            <br>

            first time haath pakra tha
            maine. 🤭🫠

            <br><br>

            Woh moment...

            <br>

            honestly words mein
            explain karna mushkil hai.

            🙈🤭

        </p>

    </div>

    <div class="btn-row">

        <button
            class="btn secondary"
            onclick="prevPage()"
        >
            ← Back
        </button>

        <button
            class="btn"
            onclick="nextPage()"
        >
            Next Memory 🌧️
        </button>

    </div>

</div>

</section>



<!-- =====================================================
     PAGE 6 — 15 JULY / STATION / FIRST KISS
===================================================== -->

<section class="page" id="page6">

<div class="container">

    <div class="small-label">
        The Moment I Still Remember
    </div>

    <div class="script">
        15 July 2026 ❤️
    </div>

    <h2 class="title">
        11:45...
    </h2>

    <div class="date-badge">
        WEDNESDAY • STATION
    </div>

    <div class="glass">

        <div class="memory-icon">
            🚉❤️
        </div>

        <p class="story-text">

            Wednesday...

            <br>

            15 July 2026.

            <br><br>

            11.45 pe Begam station pe aayi.

            <br><br>

            Aur pata nahi kyun...

            <br>

            us waqt bohat sakoon hua.

            🫠🤌🏻

            <br><br>

            Woh feeling...

            <br>

            woh excitement...

            <br>

            woh moment jab finally
            saamne thi...

            <br><br>

            Aur phir...

            <br>

            <strong>
                First Kiss. 🤭🙈
            </strong>

        </p>

    </div>

    <div class="btn-row">

        <button
            class="btn secondary"
            onclick="prevPage()"
        >
            ← Back
        </button>

        <button
            class="btn"
            onclick="nextPage()"
        >
            One More Memory ❤️
        </button>

    </div>

</div>

</section>



<!-- =====================================================
     PAGE 7 — HUZAIFA HOUSE / 5:45 AM
===================================================== -->

<section class="page" id="page7">

<div class="container">

    <div class="small-label">
        Another little memory
    </div>

    <div class="script">
        5:45 AM 🌅
    </div>

    <h2 class="title">
        Subha Subha...
    </h2>

    <div class="glass">

        <div class="memory-icon">
            🌅🏠❤️
        </div>

        <p class="story-text">

            Ek martaba Huzaifa ke ghar
            milne gaya tha.

            <br><br>

            Subha subha...

            <br>

            5.45 pe Begam ne
            milne ke liya bulaya tha.

            <br><br>

            Itni subha...

            <br>

            lekin phir bhi jaana tha. 😂

            <br><br>

            Aur jab mila...

            <br>

            phir wohi feeling.

            <br><br>

            Bohat sakoon.

            🫠❤️

        </p>

        <div class="divider"></div>

        <div class="script"
             style="font-size:45px;">

            Some moments are small...
            but unforgettable.

        </div>

    </div>

    <div class="btn-row">

        <button
            class="btn secondary"
            onclick="prevPage()"
        >
            ← Back
        </button>

        <button
            class="btn"
            onclick="nextPage()"
        >
            Our One Year ❤️
        </button>

    </div>

</div>

</section>



<!-- PAGE COUNTER -->

<div
    class="page-counter"
    id="pageCounter"
>
    1 / 19
</div>



<script>

/* =========================================
   PAGE NAVIGATION
========================================= */

let currentPage = 1;

const totalPages = 19;


function showPage(number){

    if(
        number < 1 ||
        number > totalPages
    ){
        return;
    }

    document
        .querySelectorAll('.page')
        .forEach(page=>{
            page.classList.remove('active');
        });


    const target =
        document.getElementById(
            'page' + number
        );


    if(target){

        target.classList.add('active');

        currentPage = number;

        document
            .getElementById('pageCounter')
            .innerText =
                currentPage +
                " / " +
                totalPages;

        window.scrollTo({
            top:0,
            behavior:'smooth'
        });

    }

}


function nextPage(){

    if(
        currentPage < totalPages
    ){

        showPage(
            currentPage + 1
        );

    }

}


function prevPage(){

    if(
        currentPage > 1
    ){

        showPage(
            currentPage - 1
        );

    }

}


/* =========================================
   KEYBOARD
========================================= */

document.addEventListener(
    'keydown',
    function(e){

        if(e.key === 'ArrowRight'){
            nextPage();
        }

        if(e.key === 'ArrowLeft'){
            prevPage();
        }

    }
);


/* =========================================
   FLOATING HEARTS
========================================= */

function createFloatingHeart(){

    const heart =
        document.createElement(
            'div'
        );

    heart.className =
        'floating-heart';

    const hearts=[
        '❤️',
        '💗',
        '💕',
        '💖',
        '💘',
        '💓'
    ];

    heart.innerText =
        hearts[
            Math.floor(
                Math.random()*hearts.length
            )
        ];

    heart.style.left =
        Math.random()*100 + '%';

    heart.style.fontSize =
        (12 + Math.random()*20) + 'px';

    heart.style.animationDuration =
        (7 + Math.random()*7) + 's';

    document.body.appendChild(
        heart
    );


    setTimeout(
        ()=>{
            heart.remove();
        },
        15000
    );

}


setInterval(
    createFloatingHeart,
    900
);


/* =========================================
   INITIAL PAGE
========================================= */

showPage(1);

</script>

<!-- =====================================================
     PART 1 ENDS HERE
     
     IMPORTANT:
     PART 2 KO ISKE BILKUL NEECHAY PASTE KARNA HAI.
     
     YAHAN </body> ya </html> MAT LAGANA.
===================================================== -->
<!-- =====================================================
     PART 2 — ANNIVERSARY STORY + LETTER + NOTES + GAMES
===================================================== -->

<!-- PAGE 8 — ONE YEAR -->

<section class="page" id="page8">

<div class="container">

    <div class="small-label">
        Chapter Eight
    </div>

    <div class="script">
        One Whole Year ❤️
    </div>

    <h2 class="title">
        Same Date... One Year Later
    </h2>

    <div class="glass">

        <div class="memory-icon">
            🥹❤️
        </div>

        <p class="story-text">

            Aj same date hogi hamare paas...

            <br><br>

            Aur humein apas mein
            ek saal ho jayega.

            <br><br>

            Ek saal...

            <br>

            12 months...

            <br>

            bohat saari conversations...

            <br>

            bohat saari memories...

            <br>

            kuch fights...

            <br>

            bohat saari smiles...

            <br><br>

            Aur sabse important...

            <br>

            <strong>
                Hum.
            </strong>

        </p>

        <div class="divider"></div>

        <p class="story-text">

            Mujhe nahi pata ye ek saal
            kitni jaldi guzar gaya.

            <br><br>

            Lekin ek cheez pata hai...

            <br><br>

            Main chahta hoon ke
            ye sirf first anniversary ho.

            <br><br>

            Last nahi.

            ❤️

        </p>

        <div class="script" style="font-size:45px;">
            Hamesha Sath. ♾️
        </div>

    </div>

    <div class="btn-row">

        <button class="btn secondary" onclick="prevPage()">
            ← Back
        </button>

        <button class="btn" onclick="nextPage()">
            My Letter 💌
        </button>

    </div>

</div>

</section>



<!-- PAGE 9 — LONG ANNIVERSARY LETTER -->

<section class="page" id="page9">

<div class="container">

    <div class="small-label">
        From My Heart
    </div>

    <div class="script">
        Dear Bubu... 💌
    </div>

    <h2 class="title">
        Ek Choti Si Letter
    </h2>

    <div class="glass">

        <p class="story-text">

            Bubu, kabhi kabhi mujhe lagta hai
            ke kuch log humari life mein
            bilkul unexpectedly aate hain,
            lekin phir dheere dheere
            woh humari life ka sabse
            beautiful part ban jate hain.

            <br><br>

            Tum bhi meri life mein
            kuch isi tarah aayi.

            <br><br>

            Pehle random baatein,
            phir games,
            phir poetry,
            phir woh silly names,
            aur phir pata hi nahi chala
            ke kab tum meri daily life
            ka important part ban gayi.

        </p>


        <p class="story-text">

            Mujhe humari choti choti
            memories sabse zyada pasand hain.

            <br><br>

            Woh Ludo games...

            <br>

            woh random conversations...

            <br>

            woh Thumak Thumak aur
            Dodi Dum wali pagalpan...

            <br>

            woh meeting ke moments...

            <br>

            baarish...

            <br>

            first time haath pakarna...

            <br>

            aur woh station wala moment.

            ❤️

        </p>


        <p class="story-text">

            Shayad duniya ke liye
            ye sab normal moments hon.

            <br><br>

            Lekin mere liye nahi.

            <br><br>

            Mere liye ye woh moments hain
            jo kabhi kabhi achanak yaad aate hain
            aur face pe smile aa jati hai.

            <br><br>

            Tumhare saath mujhe
            ek ajeeb sa sukoon milta hai.

            🫠❤️

        </p>


        <p class="story-text">

            Aur haan...

            <br><br>

            Hum perfect nahi hain.

            <br>

            Hum ladte bhi hain.

            <br>

            Gussa bhi hota hai.

            <br>

            Kabhi mera dil bhi dukhta hai.

            <br>

            Kabhi tumhara bhi.

            <br><br>

            Lekin phir bhi...

            <br>

            dil ke kisi kone mein
            ek hi baat rehti hai:

            <br><br>

            <strong>
                I still want us.
            </strong>

        </p>


        <p class="story-text">

            Is first anniversary par
            main bas itna kehna chahta hoon...

            <br><br>

            Thank you.

            <br><br>

            Mere saath rehne ke liye.

            <br>

            Meri stupid baatein sunne ke liye.

            <br>

            Mujhe tolerate karne ke liye. 😂

            <br>

            Aur meri life mein
            itni beautiful memories
            add karne ke liye.

            <br><br>

            Happy First Anniversary,
            Meri Jaan. ❤️

        </p>

    </div>


    <div class="btn-row">

        <button class="btn secondary" onclick="prevPage()">
            ← Back
        </button>

        <button class="btn" onclick="nextPage()">
            One Honest Note 😤❤️
        </button>

    </div>

</div>

</section>



<!-- PAGE 10 — ANGRY NOTE -->

<section class="page" id="page10">

<div class="container">

    <div class="small-label">
        Warning 😂
    </div>

    <div class="script">
        Ek Gussa Wala Note 😤
    </div>

    <h2 class="title">
        Lekin Pyaar Se ❤️
    </h2>

    <div class="glass">

        <div class="memory-icon">
            😤❤️
        </div>

        <p class="story-text">

            Ap hamesha bahir jati hain...

            <br><br>

            baat nahi manti...

            <br>

            kahti hain karo gi...

            <br>

            karti nahi hain...

            <br><br>

            Mera dil dukhati hain.

            <br><br>

            Rolaya hai.

            <br><br>

            Aj bhi shop pe betha bhi roya.

            <br><br>

            Jumah parhate bhi roya.

            <br><br>

            Bara dil dukhaya hai mera apen.

            🥺

        </p>

        <div class="divider"></div>

        <p class="story-text">

            Lekin itna sab kehne ke baad bhi...

            <br><br>

            Main tumse pyaar karta hoon.

            ❤️

        </p>

        <div class="btn-row">

            <button class="btn secondary"
                    onclick="angryReply()">
                I Don't Care 😤
            </button>

            <button class="btn"
                    onclick="sorryReply()">
                Okay Bubu 🥺❤️
            </button>

        </div>

        <div id="angryResult"
             class="game-message">
        </div>

    </div>

    <div class="btn-row">

        <button class="btn secondary" onclick="prevPage()">
            ← Back
        </button>

        <button class="btn" onclick="nextPage()">
            Cute Notes 💌
        </button>

    </div>

</div>

</section>



<!-- PAGE 11 — CUTE NOTES -->

<section class="page" id="page11">

<div class="container">

    <div class="small-label">
        Open Them One By One
    </div>

    <div class="script">
        Little Notes 💌
    </div>

    <h2 class="title">
        Sirf Tumhare Liye
    </h2>

    <p class="subtitle">
        Har card ko touch/click karo. 👀❤️
    </p>


    <div class="memory-grid">

        <div class="memory-card note-card"
             onclick="openNote(this)">

            <div class="memory-icon">
                💗
            </div>

            <h3>
                Note #1
            </h3>

            <p class="note-hidden">
                Tumhari smile meri
                favorite cheezon mein se
                ek hai. ❤️
            </p>

        </div>


        <div class="memory-card note-card"
             onclick="openNote(this)">

            <div class="memory-icon">
                🌙
            </div>

            <h3>
                Note #2
            </h3>

            <p class="note-hidden">
                Chahe din kitna bhi bad
                ho, tumse baat ho jaye
                to sab thora better lagta hai.
            </p>

        </div>


        <div class="memory-card note-card"
             onclick="openNote(this)">

            <div class="memory-icon">
                🫠
            </div>

            <h3>
                Note #3
            </h3>

            <p class="note-hidden">
                Tumhare saath woh
                simple moments bhi
                special ban jate hain.
            </p>

        </div>


        <div class="memory-card note-card"
             onclick="openNote(this)">

            <div class="memory-icon">
                😂
            </div>

            <h3>
                Note #4
            </h3>

            <p class="note-hidden">
                Tum pagal ho.

                <br>

                Lekin meri favorite pagal ho. 😂❤️
            </p>

        </div>


        <div class="memory-card note-card"
             onclick="openNote(this)">

            <div class="memory-icon">
                🥹
            </div>

            <h3>
                Note #5
            </h3>

            <p class="note-hidden">
                Agar memories ko save
                karne ka button hota,
                main tumhare saath
                har moment save karta.
            </p>

        </div>


        <div class="memory-card note-card"
             onclick="openNote(this)">

            <div class="memory-icon">
                ♾️
            </div>

            <h3>
                Note #6
            </h3>

            <p class="note-hidden">
                First anniversary hai...

                <br><br>

                Lekin meri wish hai:
                last anniversary kabhi
                na ho.
            </p>

        </div>

    </div>


    <div class="btn-row">

        <button class="btn secondary" onclick="prevPage()">
            ← Back
        </button>

        <button class="btn" onclick="nextPage()">
            Love Quiz 🎮
        </button>

    </div>

</div>

</section>



<!-- PAGE 12 — LOVE QUIZ -->

<section class="page" id="page12">

<div class="container">

    <div class="small-label">
        Game #1
    </div>

    <div class="script">
        How Well Do You Know Us? 🎮
    </div>

    <h2 class="title">
        Love Quiz ❤️
    </h2>

    <div class="glass">

        <div id="quizBox">

            <div id="quizQuestion"
                 class="question-big">
            </div>

            <div id="quizAnswers"
                 class="quiz-answers">
            </div>

            <div id="quizFeedback"
                 class="game-message">
            </div>

            <button
                id="quizNext"
                class="btn"
                style="display:none;"
                onclick="nextQuiz()">

                Next Question →

            </button>

        </div>

    </div>

    <div class="btn-row">

        <button class="btn secondary" onclick="prevPage()">
            ← Back
        </button>

        <button class="btn" onclick="nextPage()">
            Pick A Heart ❤️
        </button>

    </div>

</div>

</section>



<!-- PAGE 13 — PICK A HEART -->

<section class="page" id="page13">

<div class="container">

    <div class="small-label">
        Game #2
    </div>

    <div class="script">
        Pick A Heart ❤️
    </div>

    <h2 class="title">
        Ek Heart Choose Karo
    </h2>

    <p class="subtitle">
        Har heart ke andar ek secret message hai. 👀
    </p>

    <div class="heart-choice-grid">

        <button class="heart-choice"
                onclick="pickHeart(1)">
            ❤️
        </button>

        <button class="heart-choice"
                onclick="pickHeart(2)">
            💗
        </button>

        <button class="heart-choice"
                onclick="pickHeart(3)">
            💖
        </button>

        <button class="heart-choice"
                onclick="pickHeart(4)">
            💕
        </button>

        <button class="heart-choice"
                onclick="pickHeart(5)">
            💘
        </button>

    </div>

    <div id="heartChoiceResult"
         class="glass game-message">

        Choose one... 👀❤️

    </div>

    <div class="btn-row">

        <button class="btn secondary" onclick="prevPage()">
            ← Back
        </button>

        <button class="btn" onclick="nextPage()">
            Catch My Heart 🎮
        </button>

    </div>

</div>

</section>



<style>

/* NOTES */

.note-hidden{
    display:none;
}

.note-card.open .note-hidden{
    display:block;

    animation:
        pageIn .5s ease;
}


/* QUIZ */

.question-big{

    font-family:'Cormorant Garamond',serif;

    font-size:30px;

    line-height:1.4;

    margin-bottom:25px;

}


.quiz-answers{

    display:grid;

    grid-template-columns:
        repeat(2,1fr);

    gap:12px;

}


.quiz-answer{

    border:
        1px solid
        rgba(255,255,255,.1);

    background:
        rgba(255,255,255,.04);

    color:white;

    padding:15px;

    border-radius:15px;

    cursor:pointer;

    transition:.3s;

    font-family:'Poppins',sans-serif;

}


.quiz-answer:hover{

    background:
        rgba(255,120,160,.12);

    transform:translateY(-3px);

}


.quiz-answer.correct{

    background:
        rgba(80,180,120,.2);

    border-color:
        rgba(100,220,150,.5);

}


.quiz-answer.wrong{

    background:
        rgba(220,70,100,.2);

    border-color:
        rgba(255,100,120,.4);

}


/* HEART CHOICES */

.heart-choice-grid{

    display:flex;

    justify-content:center;

    flex-wrap:wrap;

    gap:20px;

    margin:40px auto;

}


.heart-choice{

    width:80px;

    height:80px;

    border-radius:50%;

    border:
        1px solid
        rgba(255,180,200,.15);

    background:
        rgba(255,255,255,.04);

    font-size:38px;

    cursor:pointer;

    transition:.3s;

}


.heart-choice:hover{

    transform:
        translateY(-8px)
        scale(1.08);

    background:
        rgba(255,100,150,.12);

    box-shadow:
        0 15px 40px
        rgba(255,70,130,.15);

}


@media(max-width:600px){

    .quiz-answers{
        grid-template-columns:1fr;
    }

    .heart-choice{
        width:65px;
        height:65px;
        font-size:30px;
    }

}

</style>



<script>

/* =========================================
   ANGRY NOTE
========================================= */

function angryReply(){

    document.getElementById(
        "angryResult"
    ).innerHTML = `

        <div class="divider"></div>

        <div class="script"
             style="font-size:42px;">

            Achaaa? 😤

        </div>

        <p>
            Phir main bhi baat nahi kar raha... 😭
        </p>

    `;

}


function sorryReply(){

    document.getElementById(
        "angryResult"
    ).innerHTML = `

        <div class="divider"></div>

        <div class="script"
             style="font-size:42px;">

            Good Girl 🥺❤️

        </div>

        <p>
            Ab idhar aao...
            hug do. 🫂❤️
        </p>

    `;

}


/* =========================================
   CUTE NOTES
========================================= */

function openNote(card){

    card.classList.toggle(
        "open"
    );

}


/* =========================================
   QUIZ DATA
========================================= */

const quizData = [

    {
        question:
            "Humari baat kis date se start hui thi?",

        answers:[
            "29 August",
            "5 September",
            "14 May",
            "15 July"
        ],

        correct:1
    },


    {
        question:
            "Hum pehle kya khelte thay?",

        answers:[
            "PUBG",
            "Ludo",
            "Valorant",
            "Minecraft"
        ],

        correct:1
    },


    {
        question:
            "GC mein funny name kya rakha gaya tha?",

        answers:[
            "Dodi Dum",
            "Bubu Gang",
            "Love Birds",
            "Thumak Team"
        ],

        correct:0
    },


    {
        question:
            "Station pe Begam approximately kitne baje aayi thi?",

        answers:[
            "10:15",
            "11:45",
            "1:15",
            "5:45"
        ],

        correct:1
    },


    {
        question:
            "Pehli baar haath kab pakra tha?",

        answers:[
            "14 May",
            "15 July",
            "29",
            "5 September"
        ],

        correct:0
    }

];


let quizIndex = 0;

let quizScore = 0;

let quizAnswered = false;


function loadQuiz(){

    const q =
        quizData[quizIndex];


    document.getElementById(
        "quizQuestion"
    ).innerText =
        q.question;


    const answers =
        document.getElementById(
            "quizAnswers"
        );


    answers.innerHTML="";


    document.getElementById(
        "quizFeedback"
    ).innerHTML="";


    document.getElementById(
        "quizNext"
    ).style.display="none";


    quizAnswered=false;


    q.answers.forEach(
        (answer,index)=>{

            const button =
                document.createElement(
                    "button"
                );


            button.className=
                "quiz-answer";


            button.innerText=
                answer;


            button.onclick=
                ()=>checkQuiz(
                    index,
                    button
                );


            answers.appendChild(
                button
            );

        }
    );

}


function checkQuiz(
    selected,
    clicked
){

    if(quizAnswered) return;

    quizAnswered=true;


    const q =
        quizData[quizIndex];


    const buttons =
        document.querySelectorAll(
            ".quiz-answer"
        );


    buttons.forEach(
        (button,index)=>{

            if(
                index === q.correct
            ){

                button.classList.add(
                    "correct"
                );

            }

        }
    );


    if(
        selected === q.correct
    ){

        quizScore++;


        clicked.classList.add(
            "correct"
        );


        document.getElementById(
            "quizFeedback"
        ).innerHTML =
            "Correct! 🥹❤️";


    }else{

        clicked.classList.add(
            "wrong"
        );


        document.getElementById(
            "quizFeedback"
        ).innerHTML =
            "Oops 😂❤️ Correct answer highlighted hai.";

    }


    document.getElementById(
        "quizNext"
    ).style.display="inline-block";

}


function nextQuiz(){

    quizIndex++;


    if(
        quizIndex >= quizData.length
    ){

        document.getElementById(
            "quizBox"
        ).innerHTML = `

            <div style="font-size:60px;">
                ❤️
            </div>

            <div class="script"
                 style="font-size:50px;">

                Quiz Complete!

            </div>

            <h2>
                Score:
                ${quizScore}/${quizData.length}
            </h2>

            <p class="subtitle">

                ${

                    quizScore === 5

                    ?

                    "Perfect! Tumhein humari story yaad hai. 🥹❤️"

                    :

                    "Abhi aur memories revise karni parengi. 😂❤️"

                }

            </p>

            <button
                class="btn"
                onclick="restartQuiz()">

                Play Again 🎮

            </button>

        `;

        return;

    }


    loadQuiz();

}


function restartQuiz(){

    quizIndex=0;

    quizScore=0;

    quizAnswered=false;


    document.getElementById(
        "quizBox"
    ).innerHTML = `

        <div id="quizQuestion"
             class="question-big">
        </div>

        <div id="quizAnswers"
             class="quiz-answers">
        </div>

        <div id="quizFeedback"
             class="game-message">
        </div>

        <button
            id="quizNext"
            class="btn"
            style="display:none;"
            onclick="nextQuiz()">

            Next Question →

        </button>

    `;


    loadQuiz();

}


/* =========================================
   PICK A HEART
========================================= */

function pickHeart(number){

    const messages=[

        "Tum meri favorite notification ho. ❤️",

        "Tumhare saath waqt literally fast forward ho jata hai. 🫠",

        "Meri favorite memory abhi bhi woh moments hain jab tum saamne thi. 🥹",

        "Agar pyaar ka koi emoji hota... shayad woh tum hoti. 😂❤️",

        "Secret: Main tumhein phir se choose karunga. Every time. ♾️❤️"

    ];


    document.getElementById(
        "heartChoiceResult"
    ).innerHTML = `

        <div style="font-size:50px;">
            ❤️
        </div>

        <p>
            ${messages[number-1]}
        </p>

    `;


    createMiniHeartBurst();

}


function createMiniHeartBurst(){

    for(
        let i=0;
        i<10;
        i++
    ){

        const h =
            document.createElement(
                "div"
            );

        h.innerText="❤️";

        h.style.position="fixed";

        h.style.left="50%";

        h.style.top="50%";

        h.style.zIndex="9999";

        h.style.pointerEvents="none";

        h.style.fontSize=
            "20px";


        const x =
            (Math.random()-.5)*350;


        const y =
            (Math.random()-.5)*350;


        h.animate(

            [
                {
                    transform:
                        "translate(-50%,-50%)",
                    opacity:1
                },

                {
                    transform:
                        `translate(
                            calc(-50% + ${x}px),
                            calc(-50% + ${y}px)
                        )`,
                    opacity:0
                }
            ],

            {
                duration:1000
            }

        );


        document.body.appendChild(h);


        setTimeout(
            ()=>{
                h.remove();
            },
            1000
        );

    }

}


/* START QUIZ */

loadQuiz();

</script>


<!-- =====================================================
     PART 2 ENDS HERE
     
     PART 3 ISKO ISKE BILKUL NEECHAY PASTE HOGA.
     
     </body> aur </html> ABHI MAT LAGANA.
===================================================== -->
<!-- =====================================================
     PART 3 — PROPER GAMES + MEMORY VAULT + FUTURE
     + SECRET UNLOCK + CINEMATIC FINAL
===================================================== -->


<!-- =====================================================
     PAGE 14 — CATCH MY HEART
===================================================== -->

<section class="page" id="page14">

<div class="container">

    <div class="small-label">
        GAME #3
    </div>

    <div class="script">
        Catch My Heart ❤️
    </div>

    <h2 class="title">
        Pakro Mera Dil!
    </h2>

    <p class="subtitle">

        Screen par hearts appear honge.

        <br>

        Unko jaldi jaldi tap/click karo.

        <br><br>

        <strong>
            10 hearts = next memory unlocked ❤️
        </strong>

    </p>

    <div class="game-panel">

        <div class="game-top">

            <span>
                Score:
                <b id="catchScore">0</b>/10
            </span>

            <span>
                Time:
                <b id="catchTime">30</b>s
            </span>

        </div>


        <div
            id="catchArea"
            class="catch-area"
        >

            <div
                id="catchStart"
                class="game-center"
            >

                <div class="big-game-heart">
                    ❤️
                </div>

                <p>
                    Ready Bubu? 👀
                </p>

                <button
                    class="btn"
                    onclick="startCatchGame()"
                >
                    START ❤️
                </button>

            </div>

        </div>


        <div
            id="catchResult"
            class="game-result"
        ></div>

    </div>


    <div class="btn-row">

        <button
            class="btn secondary"
            onclick="prevPage()"
        >
            ← Back
        </button>

        <button
            class="btn"
            onclick="nextPage()"
        >
            Memory Vault 🗝️
        </button>

    </div>

</div>

</section>



<!-- =====================================================
     PAGE 15 — MEMORY MATCH GAME
===================================================== -->

<section class="page" id="page15">

<div class="container">

    <div class="small-label">
        GAME #4
    </div>

    <div class="script">
        Memory Match 🧩
    </div>

    <h2 class="title">
        Same Memories Find Karo ❤️
    </h2>

    <p class="subtitle">

        Cards ko flip karo.

        <br>

        Same emojis ki pair banao.

        <br><br>

        Saari pairs mil gayi to
        memory vault open ho jayega. 🗝️

    </p>


    <div class="match-info">

        Moves:
        <b id="matchMoves">0</b>

        &nbsp;&nbsp; | &nbsp;&nbsp;

        Pairs:
        <b id="matchPairs">0</b>/6

    </div>


    <div
        id="memoryBoard"
        class="memory-board"
    ></div>


    <div
        id="matchResult"
        class="game-result"
    ></div>


    <div class="btn-row">

        <button
            class="btn secondary"
            onclick="prevPage()"
        >
            ← Back
        </button>

        <button
            class="btn"
            onclick="nextPage()"
        >
            Our Memories 🗝️
        </button>

    </div>

</div>

</section>



<!-- =====================================================
     PAGE 16 — MEMORY VAULT
===================================================== -->

<section class="page" id="page16">

<div class="container">

    <div class="small-label">
        OUR PRIVATE LITTLE WORLD
    </div>

    <div class="script">
        Memory Vault 🗝️
    </div>

    <h2 class="title">
        Jo Kabhi Purani Nahi Hongi
    </h2>

    <p class="subtitle">

        Kuch memories calendar par
        sirf dates hoti hain...

        <br>

        Lekin humare liye
        woh poori feelings hain. ❤️

    </p>


    <div class="vault-grid">


        <div class="vault-card">

            <div class="vault-icon">
                💬
            </div>

            <span class="vault-date">
                05 SEPTEMBER
            </span>

            <h3>
                The Beginning
            </h3>

            <p>

                5 Sep se baat start hui thi.

                <br><br>

                Pehle random conversations,
                phir dheere dheere
                ek dusre ki aadat.

                ❤️

            </p>

        </div>


        <div class="vault-card">

            <div class="vault-icon">
                🎲
            </div>

            <span class="vault-date">
                THE LUDO ERA
            </span>

            <h3>
                Ludo & Poetry
            </h3>

            <p>

                Apas mein Ludo khelte thay,
                poetry sunate thay,
                bohat kuch karte thay.

                <br><br>

                Maza ata tha...

                <br>

                sakoon bas game ki der hoti thi. 🫠

            </p>

        </div>


        <div class="vault-card">

            <div class="vault-icon">
                😂
            </div>

            <span class="vault-date">
                UNEXPECTED
            </span>

            <h3>
                Thumak Thumak
            </h3>

            <p>

                Thumak Thumak trend...

                <br><br>

                Dodi Dum hamara
                name GC mein.

                <br><br>

                Sab kuch unexpected tha. 😂❤️

            </p>

        </div>


        <div class="vault-card">

            <div class="vault-icon">
                💌
            </div>

            <span class="vault-date">
                29
            </span>

            <h3>
                The Proposal
            </h3>

            <p>

                29 ko proposal kiya.

                <br><br>

                Ek simple moment...

                <br>

                jo humari story ke liye
                bohat bada moment ban gaya.

                ❤️

            </p>

        </div>


        <div class="vault-card">

            <div class="vault-icon">
                🌧️
            </div>

            <span class="vault-date">
                14 MAY • 1:15
            </span>

            <h3>
                Two Rains
            </h3>

            <p>

                Thursday ko mile.

                <br><br>

                Duphar 1.15 ke qareeb.

                <br><br>

                Us din 2 baar barish hui.

                <br><br>

                Aur first time
                haath pakra tha. 🤭🫠

            </p>

        </div>


        <div class="vault-card">

            <div class="vault-icon">
                🚉
            </div>

            <span class="vault-date">
                15 JULY 2026 • 11:45
            </span>

            <h3>
                The Station
            </h3>

            <p>

                Wednesday.

                <br><br>

                15 July 2026.

                <br><br>

                11.45 pe Begam
                station pe aayi.

                <br><br>

                Bohat sakoon hua.

                <br><br>

                First kiss. 🤭🙈

            </p>

        </div>


        <div class="vault-card">

            <div class="vault-icon">
                🌅
            </div>

            <span class="vault-date">
                5:45 AM
            </span>

            <h3>
                Huzaifa's House
            </h3>

            <p>

                Ek martaba Huzaifa ke
                ghar milne gaya.

                <br><br>

                Subha subha 5.45 pe
                Begam ne milne ke liya bulaya.

                <br><br>

                Aur bara sakoon hua tha
                us din bhi. ❤️

            </p>

        </div>


        <div class="vault-card special-vault">

            <div class="vault-icon">
                ♾️
            </div>

            <span class="vault-date">
                TODAY
            </span>

            <h3>
                One Year
            </h3>

            <p>

                Aj same date hogi...

                <br><br>

                Humein apas mein
                ek saal ho jayega.

                <br><br>

                Aur meri wish?

                <br><br>

                <strong>
                    Hamesha bhi saath rahenge. ❤️
                </strong>

            </p>

        </div>

    </div>


    <div class="btn-row">

        <button
            class="btn secondary"
            onclick="prevPage()"
        >
            ← Back
        </button>

        <button
            class="btn"
            onclick="nextPage()"
        >
            One Last Game 😂❤️
        </button>

    </div>

</div>

</section>



<!-- =====================================================
     PAGE 17 — YES / NO LOVE GAME
===================================================== -->

<section class="page" id="page17">

<div class="container">

    <div class="small-label">
        FINAL GAME
    </div>

    <div class="script">
        Be Honest... 👀
    </div>

    <h2 class="title">
        Ek Sawal Hai ❤️
    </h2>

    <div class="love-game">

        <div
            class="question-big"
            id="loveQuestion"
        >

            Kya tum mere saath
            hamesha rahogi? ❤️

        </div>


        <div
            id="loveButtons"
            class="love-buttons"
        >

            <button
                class="btn yes-love"
                onclick="loveYes()"
            >
                Haan ❤️
            </button>

            <button
                id="loveNo"
                class="btn secondary"
                onclick="loveNo()"
                onmouseover="runAwayNo()"
                ontouchstart="runAwayNo()"
            >
                Nahi 😤
            </button>

        </div>


        <div
            id="loveGameResult"
            class="game-result"
        ></div>

    </div>


    <div class="btn-row">

        <button
            class="btn secondary"
            onclick="prevPage()"
        >
            ← Back
        </button>

        <button
            class="btn"
            onclick="nextPage()"
        >
            Future Together ✨
        </button>

    </div>

</div>

</section>



<!-- =====================================================
     PAGE 18 — FUTURE TOGETHER
===================================================== -->

<section class="page" id="page18">

<div class="container">

    <div class="small-label">
        NEXT CHAPTER
    </div>

    <div class="script">
        Our Future ✨
    </div>

    <h2 class="title">
        Abhi To Bohat Kuch Baqi Hai
    </h2>

    <div class="glass">

        <p class="story-text">

            Ek saal ki memories ban gayi...

            <br><br>

            Lekin Bubu...

            <br>

            humari story abhi khatam nahi hui.

            <br><br>

            Actually...

            <br>

            mujhe lagta hai
            asli story abhi start hui hai.

        </p>


        <div class="future-timeline">


            <div class="future-row">

                <div class="future-dot">
                    01
                </div>

                <div>
                    <h3>
                        More Memories
                    </h3>

                    <p>
                        Aur bohat saare moments
                        jo hum future mein yaad karenge.
                    </p>
                </div>

            </div>


            <div class="future-row">

                <div class="future-dot">
                    02
                </div>

                <div>
                    <h3>
                        More Rain
                    </h3>

                    <p>
                        Aur baarish...
                        aur naye moments
                        jo purani baarish ko bhi yaad dilayen.
                    </p>
                </div>

            </div>


            <div class="future-row">

                <div class="future-dot">
                    03
                </div>

                <div>
                    <h3>
                        More Meetings
                    </h3>

                    <p>
                        Aur woh excitement
                        jab ek dusre ko
                        dobara dekhna ho.
                    </p>
                </div>

            </div>


            <div class="future-row">

                <div class="future-dot">
                    04
                </div>

                <div>
                    <h3>
                        More Pagalpan
                    </h3>

                    <p>
                        More stupid jokes,
                        fights, teasing
                        aur phir mana lena. 😂❤️
                    </p>
                </div>

            </div>


            <div class="future-row">

                <div class="future-dot">
                    05
                </div>

                <div>
                    <h3>
                        More Anniversaries
                    </h3>

                    <p>
                        First anniversary ke baad
                        second, third...
                        aur pata nahi kitni. ♾️
                    </p>
                </div>

            </div>


            <div class="future-row">

                <div class="future-dot">
                    ∞
                </div>

                <div>
                    <h3>
                        Always Us
                    </h3>

                    <p>
                        Same team.

                        <br>

                        Same madness.

                        <br>

                        Same love.

                        ❤️
                    </p>
                </div>

            </div>

        </div>


        <div class="divider"></div>


        <p class="story-text">

            Future exactly kaisa hoga,
            mujhe nahi pata.

            <br><br>

            Lekin main chahta hoon
            jab bhi hum future ki taraf dekhein...

            <br><br>

            wahan ek cheez same ho:

            <br><br>

            <strong>
                You + Me.
            </strong>

            ❤️

        </p>

    </div>


    <div class="btn-row">

        <button
            class="btn secondary"
            onclick="prevPage()"
        >
            ← Back
        </button>

        <button
            class="btn"
            onclick="nextPage()"
        >
            Secret Door 🔐
        </button>

    </div>

</div>

</section>



<!-- =====================================================
     PAGE 19 — SECRET UNLOCK
===================================================== -->

<section class="page" id="page19">

<div class="container">

    <div class="small-label">
        FINAL LOCK
    </div>

    <div class="script">
        One Secret... 🔐
    </div>

    <h2 class="title">
        Final Door Unlock Karo
    </h2>

    <div class="glass secret-box">

        <div class="big-lock">
            🔐
        </div>

        <p class="story-text">

            Is door ke peeche
            kuch hai jo sirf
            meri Bubu ke liye hai.

            <br><br>

            Hint:

            <br><br>

            <em>
                "Humari story ka beginning..."
            </em>

        </p>


        <input
            id="secretCode"
            class="secret-input"
            type="text"
            placeholder="Enter the secret..."
        >


        <button
            class="btn"
            onclick="checkSecret()"
        >
            UNLOCK 🔓
        </button>


        <div
            id="secretMessage"
            class="game-result"
        ></div>

    </div>


    <div class="btn-row">

        <button
            class="btn secondary"
            onclick="prevPage()"
        >
            ← Back
        </button>

    </div>

</div>

</section>



<!-- =====================================================
     PAGE 20 — CINEMATIC FINAL
===================================================== -->

<section
    class="page cinematic-page"
    id="page20"
>

<div class="cinematic-stars"></div>

<div class="cinematic-content">

    <div
        id="finalBeginning"
        class="final-beginning"
    >

        <div class="small-label">
            01 / 01
        </div>

        <div class="final-script">
            Wait...
        </div>

        <p class="final-small">
            There's one last thing.
        </p>

        <button
            class="btn final-open-btn"
            onclick="openFinalHeart()"
        >
            Open My Heart ❤️
        </button>

    </div>


    <div
        id="finalReveal"
        class="final-reveal"
        style="display:none;"
    >

        <div class="final-heart">
            ❤️
        </div>


        <div
            id="finalTyping"
            class="final-typing"
        ></div>


        <div
            id="finalLetter"
            class="final-letter"
            style="display:none;"
        >

            <div class="final-script">
                Bubu... ❤️
            </div>


            <p>

                Agar mujhe dobara choose karne ka
                chance mile...

                <br><br>

                Main phir tumhein choose karunga.

            </p>


            <p>

                Main humari har memory
                dobara jeena chahta hoon.

                <br><br>

                Woh first conversations...

                <br>

                Ludo...

                <br>

                Poetry...

                <br>

                Thumak Thumak...

                <br>

                Dodi Dum...

                <br>

                29...

                <br>

                14 May ki baarish...

                <br>

                first hand hold...

                <br>

                15 July ka station...

                <br>

                11:45...

                <br>

                first kiss...

                <br>

                aur woh 5:45 AM wala
                chota sa moment.

            </p>


            <p>

                Sab kuch.

                <br><br>

                Even woh moments
                jahan hum laday.

                <br><br>

                Even woh moments
                jahan mera dil dukha.

                <br><br>

                Kyun?

                <br><br>

                Kyun ke woh sab bhi
                humari story ka part hain.

            </p>


            <p>

                Aur agar life mujhe
                hazaar different roads de...

                <br><br>

                Main phir bhi
                us road ko choose karunga
                jahan tum mere saath ho.

            </p>


            <div class="divider"></div>


            <div class="forever-lines">

                <div>
                    If I had to choose again...
                </div>

                <div class="big-final-line">
                    I'd still choose you.
                </div>

                <div>
                    Today.
                </div>

                <div>
                    Tomorrow.
                </div>

                <div>
                    Every time.
                </div>

                <div class="huge-heart">
                    ❤️
                </div>

            </div>


            <div class="divider"></div>


            <div class="final-script">
                Happy First Anniversary,
                Meri Jaan. ❤️
            </div>


            <p class="final-ending-text">

                One year down...

                <br>

                but our story has
                no ending.

                <br><br>

                This is not the end.

                <br>

                This is just another page
                in our forever.

                ♾️❤️

            </p>


            <div class="final-emojis">
                ❤️ 💗 💕 💖 💘
            </div>


            <button
                class="btn"
                onclick="showPage(1)"
            >
                Read Our Story Again ↻
            </button>

        </div>

    </div>

</div>

</section>



<!-- =====================================================
     PART 3 CSS
===================================================== -->

<style>

/* =========================================
   GAME PANELS
========================================= */

.game-panel{

    max-width:800px;

    margin:30px auto;

    padding:20px;

    border-radius:28px;

    background:
        rgba(255,255,255,.035);

    border:
        1px solid
        rgba(255,255,255,.08);

}


.game-top{

    display:flex;

    justify-content:space-between;

    margin-bottom:15px;

    color:#d9c6ce;

    font-size:13px;

}


.catch-area{

    height:430px;

    position:relative;

    overflow:hidden;

    border-radius:22px;

    background:
        radial-gradient(
            circle at center,
            rgba(255,100,150,.08),
            transparent 60%
        );

    border:
        1px solid
        rgba(255,255,255,.06);

}


.game-center{

    position:absolute;

    inset:0;

    display:flex;

    flex-direction:column;

    align-items:center;

    justify-content:center;

}


.big-game-heart{

    font-size:70px;

    animation:
        heartbeat 1.2s infinite;

}


.catch-heart{

    position:absolute;

    cursor:pointer;

    user-select:none;

    font-size:38px;

    animation:
        catchPop .25s ease;

    filter:
        drop-shadow(
            0 0 12px
            rgba(255,100,150,.5)
        );

}


@keyframes catchPop{

    from{
        transform:scale(.3);
    }

    to{
        transform:scale(1);
    }

}


.game-result{

    min-height:40px;

    margin:20px auto;

    text-align:center;

    color:#ffc3d2;

    line-height:1.7;

}


/* =========================================
   MEMORY MATCH
========================================= */

.match-info{

    margin:20px;

    color:#d6c7ce;

}


.memory-board{

    width:100%;

    max-width:700px;

    margin:25px auto;

    display:grid;

    grid-template-columns:
        repeat(4,1fr);

    gap:12px;

}


.memory-tile{

    aspect-ratio:1;

    border:none;

    border-radius:17px;

    cursor:pointer;

    background:
        rgba(255,255,255,.06);

    border:
        1px solid
        rgba(255,255,255,.1);

    color:white;

    font-size:30px;

    transition:.3s;

}


.memory-tile:hover{

    transform:
        translateY(-4px);

}


.memory-tile.flipped{

    background:
        rgba(255,100,150,.13);

}


.memory-tile.matched{

    background:
        rgba(100,200,150,.13);

    border-color:
        rgba(130,230,170,.3);

}


/* =========================================
   VAULT
========================================= */

.vault-grid{

    display:grid;

    grid-template-columns:
        repeat(2,1fr);

    gap:20px;

    margin-top:35px;

}


.vault-card{

    text-align:left;

    padding:27px;

    border-radius:24px;

    background:
        linear-gradient(
            145deg,
            rgba(255,255,255,.065),
            rgba(255,255,255,.025)
        );

    border:
        1px solid
        rgba(255,255,255,.08);

    transition:.35s;

}


.vault-card:hover{

    transform:
        translateY(-6px);

    border-color:
        rgba(255,170,195,.3);

}


.vault-icon{

    font-size:42px;

    margin-bottom:12px;

}


.vault-date{

    font-size:10px;

    letter-spacing:3px;

    color:#c99eae;

}


.vault-card h3{

    font-family:
        'Cormorant Garamond',
        serif;

    font-size:30px;

    margin:8px 0 12px;

}


.vault-card p{

    color:#cfc1c8;

    line-height:1.8;

    font-size:13px;

}


.special-vault{

    border-color:
        rgba(255,150,190,.25);

}


/* =========================================
   LOVE GAME
========================================= */

.love-game{

    max-width:700px;

    min-height:380px;

    margin:30px auto;

    padding:45px 25px;

    display:flex;

    flex-direction:column;

    justify-content:center;

    align-items:center;

    border-radius:30px;

    background:
        rgba(255,255,255,.045);

    border:
        1px solid
        rgba(255,255,255,.09);

}


.question-big{

    font-family:
        'Cormorant Garamond',
        serif;

    font-size:34px;

    line-height:1.5;

    margin-bottom:35px;

}


.love-buttons{

    display:flex;

    gap:20px;

    justify-content:center;

    align-items:center;

    width:100%;

    min-height:90px;

}


#loveNo{

    transition:
        transform .2s ease,
        left .2s ease,
        top .2s ease;

}


/* =========================================
   FUTURE
========================================= */

.future-timeline{

    max-width:700px;

    margin:35px auto;

    text-align:left;

}


.future-row{

    display:flex;

    gap:20px;

    padding:22px 0;

    border-bottom:
        1px solid
        rgba(255,255,255,.07);

}


.future-dot{

    min-width:48px;

    height:48px;

    border-radius:50%;

    display:flex;

    justify-content:center;

    align-items:center;

    background:
        rgba(255,120,160,.1);

    border:
        1px solid
        rgba(255,150,180,.2);

    color:#e8aabc;

    font-size:11px;

}


.future-row h3{

    font-family:
        'Cormorant Garamond',
        serif;

    font-size:27px;

    margin-bottom:5px;

}


.future-row p{

    color:#cfc2c9;

    font-size:13px;

    line-height:1.7;

}


/* =========================================
   SECRET
========================================= */

.secret-box{

    max-width:600px;

}


.big-lock{

    font-size:75px;

    margin-bottom:20px;

    animation:
        lockPulse 2s infinite;

}


@keyframes lockPulse{

    0%,100%{
        transform:scale(1);
    }

    50%{
        transform:scale(1.08);
    }

}


.secret-input{

    width:100%;

    max-width:430px;

    padding:16px 20px;

    margin:15px auto 20px;

    display:block;

    border-radius:15px;

    border:
        1px solid
        rgba(255,255,255,.12);

    background:
        rgba(255,255,255,.05);

    color:white;

    outline:none;

    text-align:center;

    font-family:'Poppins',sans-serif;

}


.secret-input:focus{

    border-color:
        rgba(255,160,190,.5);

}


/* =========================================
   CINEMATIC FINAL
========================================= */

.cinematic-page{

    background:
        radial-gradient(
            circle at center,
            rgba(90,20,60,.28),
            #030205 70%
        );

    padding:0;

    overflow:hidden;

}


.cinematic-content{

    width:100%;

    max-width:900px;

    min-height:100vh;

    margin:auto;

    display:flex;

    justify-content:center;

    align-items:center;

    text-align:center;

    position:relative;

    z-index:5;

    padding:40px 20px;

}


.final-beginning{

    animation:
        fadeIn 2s ease;

}


@keyframes fadeIn{

    from{
        opacity:0;
    }

    to{
        opacity:1;
    }

}


.final-script{

    font-family:
        'Great Vibes',
        cursive;

    color:#ffb7cb;

    font-size:75px;

    line-height:1.2;

    text-shadow:
        0 0 35px
        rgba(255,100,160,.25);

}


.final-small{

    font-family:
        'Cormorant Garamond',
        serif;

    font-size:32px;

    color:#eee0e5;

    margin:20px 0 40px;

}


.final-heart{

    font-size:85px;

    margin-bottom:30px;

    animation:
        heartbeat 1.15s infinite;

}


.final-typing{

    min-height:150px;

    max-width:750px;

    margin:auto;

    font-family:
        'Cormorant Garamond',
        serif;

    font-size:38px;

    line-height:1.5;

    color:#f3e6eb;

}


.final-letter{

    margin-top:50px;

    animation:
        fadeIn 1.5s ease;

}


.final-letter p{

    max-width:760px;

    margin:35px auto;

    color:#ddd0d6;

    font-size:16px;

    line-height:2.1;

}


.forever-lines{

    font-family:
        'Cormorant Garamond',
        serif;

    font-size:31px;

    line-height:1.8;

    color:#eadde2;

}


.big-final-line{

    font-family:
        'Great Vibes',
        cursive;

    font-size:75px;

    color:#ffb5ca;

    margin:15px 0;

}


.huge-heart{

    font-size:70px;

    animation:
        heartbeat 1.3s infinite;

    margin-top:15px;

}


.final-ending-text{

    font-size:18px !important;

    color:#cdbdc5 !important;

}


.final-emojis{

    font-size:35px;

    letter-spacing:8px;

    margin:35px 0;

}


.cinematic-stars{

    position:absolute;

    inset:0;

    pointer-events:none;

    background-image:
        radial-gradient(
            circle,
            rgba(255,255,255,.8) 1px,
            transparent 1px
        );

    background-size:
        90px 90px;

    opacity:.15;

    animation:
        starMove 20s linear infinite;

}


@keyframes starMove{

    from{
        transform:translateY(0);
    }

    to{
        transform:translateY(-90px);
    }

}


/* =========================================
   MOBILE
========================================= */

@media(max-width:700px){

    .memory-board{

        grid-template-columns:
            repeat(3,1fr);

        gap:8px;

    }


    .memory-tile{

        font-size:25px;

    }


    .vault-grid{

        grid-template-columns:1fr;

    }


    .catch-area{

        height:360px;

    }


    .question-big{

        font-size:28px;

    }


    .love-buttons{

        flex-direction:column;

    }


    .final-script{

        font-size:53px;

    }


    .final-small{

        font-size:26px;

    }


    .final-typing{

        font-size:28px;

    }


    .big-final-line{

        font-size:52px;

    }


    .forever-lines{

        font-size:25px;

    }


    .final-letter p{

        font-size:14px;

        line-height:2;

    }

}

</style>



<!-- =====================================================
     PART 3 JAVASCRIPT
===================================================== -->

<script>

/* =====================================================
   IMPORTANT NAVIGATION FIX
===================================================== */

let websitePage = 1;

const websiteTotalPages = 20;


function showPage(number){

    const pages =
        document.querySelectorAll(
            '.page'
        );


    if(
        number < 1 ||
        number > websiteTotalPages
    ){
        return;
    }


    pages.forEach(
        page=>{
            page.classList.remove(
                'active'
            );
        }
    );


    const selected =
        document.getElementById(
            'page' + number
        );


    if(!selected) return;


    selected.classList.add(
        'active'
    );


    websitePage=number;


    const counter =
        document.getElementById(
            'pageCounter'
        );


    if(counter){

        counter.innerText =
            number +
            " / " +
            websiteTotalPages;

    }


    window.scrollTo({
        top:0,
        behavior:'smooth'
    });

}


function nextPage(){

    if(
        websitePage <
        websiteTotalPages
    ){

        showPage(
            websitePage + 1
        );

    }

}


function prevPage(){

    if(
        websitePage > 1
    ){

        showPage(
            websitePage - 1
        );

    }

}


/* =====================================================
   CATCH MY HEART GAME
===================================================== */

let catchRunning=false;

let catchScore=0;

let catchSeconds=30;

let catchInterval;

let catchSpawn;


function startCatchGame(){

    if(catchRunning) return;


    catchRunning=true;

    catchScore=0;

    catchSeconds=30;


    document.getElementById(
        'catchScore'
    ).innerText='0';


    document.getElementById(
        'catchTime'
    ).innerText='30';


    document.getElementById(
        'catchResult'
    ).innerHTML='';


    document.getElementById(
        'catchStart'
    ).style.display='none';


    const area =
        document.getElementById(
            'catchArea'
        );


    area.querySelectorAll(
        '.catch-heart'
    ).forEach(
        heart=>heart.remove()
    );


    catchInterval =
        setInterval(
            ()=>{

                catchSeconds--;

                document.getElementById(
                    'catchTime'
                ).innerText =
                    catchSeconds;


                if(
                    catchSeconds <= 0
                ){

                    endCatchGame();

                }

            },
            1000
        );


    catchSpawn =
        setInterval(
            spawnCatchHeart,
            700
        );


    spawnCatchHeart();

}


function spawnCatchHeart(){

    if(!catchRunning) return;


    const area =
        document.getElementById(
            'catchArea'
        );


    const heart =
        document.createElement(
            'div'
        );


    heart.className=
        'catch-heart';


    const emojis=[
        '❤️',
        '💗',
        '💕',
        '💖',
        '💘'
    ];


    heart.innerText =
        emojis[
            Math.floor(
                Math.random()*
                emojis.length
            )
        ];


    const maxX =
        area.clientWidth - 50;


    const maxY =
        area.clientHeight - 60;


    heart.style.left =
        Math.max(
            5,
            Math.random()*maxX
        ) + 'px';


    heart.style.top =
        Math.max(
            5,
            Math.random()*maxY
        ) + 'px';


    heart.onclick=
        function(){

            if(!catchRunning)
                return;


            catchScore++;


            document.getElementById(
                'catchScore'
            ).innerText =
                catchScore;


            heart.remove();


            if(
                catchScore >= 10
            ){

                winCatchGame();

            }

        };


    area.appendChild(
        heart
    );


    setTimeout(
        ()=>{

            if(
                heart.parentNode
            ){

                heart.remove();

            }

        },
        1100
    );

}


function winCatchGame(){

    catchRunning=false;

    clearInterval(
        catchInterval
    );

    clearInterval(
        catchSpawn
    );


    document
        .getElementById(
            'catchResult'
        )
        .innerHTML=`

        <div class="script"
             style="font-size:45px;">

            YOU CAUGHT MY HEART! ❤️

        </div>

        <p>
            10/10! Ab mera dil tumhare paas hai. 🫠❤️
        </p>

    `;


    createHeartExplosion();

}


function endCatchGame(){

    catchRunning=false;

    clearInterval(
        catchInterval
    );

    clearInterval(
        catchSpawn
    );


    if(
        catchScore >= 10
    ){

        winCatchGame();

        return;

    }


    document
        .getElementById(
            'catchResult'
        )
        .innerHTML=`

        <p>
            Time Up! 😂

            <br>

            Score:
            ${catchScore}/10

            <br><br>

            Ek aur chance? ❤️
        </p>

        <button
            class="btn"
            onclick="startCatchGame()">

            Try Again 🎮

        </button>

    `;

}


/* =====================================================
   MEMORY MATCH GAME
===================================================== */

const memoryIcons=[
    '❤️',
    '🌧️',
    '🚉',
    '🎲',
    '💌',
    '🌅'
];


let memoryCards=[];

let firstCard=null;

let secondCard=null;

let lockCards=false;

let matchMoves=0;

let matchPairs=0;


function setupMemoryGame(){

    const board =
        document.getElementById(
            'memoryBoard'
        );


    if(!board) return;


    board.innerHTML='';


    memoryCards=[
        ...memoryIcons,
        ...memoryIcons
    ];


    memoryCards.sort(
        ()=>Math.random()-.5
    );


    firstCard=null;

    secondCard=null;

    lockCards=false;

    matchMoves=0;

    matchPairs=0;


    document.getElementById(
        'matchMoves'
    ).innerText='0';


    document.getElementById(
        'matchPairs'
    ).innerText='0';


    document.getElementById(
        'matchResult'
    ).innerHTML='';


    memoryCards.forEach(
        (icon,index)=>{

            const tile =
                document.createElement(
                    'button'
                );


            tile.className=
                'memory-tile';


            tile.dataset.icon=
                icon;


            tile.dataset.index=
                index;


            tile.innerText='❔';


            tile.onclick=
                ()=>flipMemoryCard(
                    tile
                );


            board.appendChild(
                tile
            );

        }
    );

}


function flipMemoryCard(tile){

    if(
        lockCards ||
        tile.classList.contains(
            'flipped'
        ) ||
        tile.classList.contains(
            'matched'
        )
    ){

        return;

    }


    tile.classList.add(
        'flipped'
    );


    tile.innerText=
        tile.dataset.icon;


    if(!firstCard){

        firstCard=tile;

        return;

    }


    secondCard=tile;

    matchMoves++;


    document.getElementById(
        'matchMoves'
    ).innerText=
        matchMoves;


    if(
        firstCard.dataset.icon ===
        secondCard.dataset.icon
    ){

        firstCard.classList.add(
            'matched'
        );

        secondCard.classList.add(
            'matched'
        );


        matchPairs++;


        document.getElementById(
            'matchPairs'
        ).innerText=
            matchPairs;


        firstCard=null;

        secondCard=null;


        if(
            matchPairs ===
            memoryIcons.length
        ){

            completeMemoryGame();

        }

    }else{

        lockCards=true;


        setTimeout(
            ()=>{

                firstCard.classList.remove(
                    'flipped'
                );

                secondCard.classList.remove(
                    'flipped'
                );


                firstCard.innerText=
                    '❔';

                secondCard.innerText=
                    '❔';


                firstCard=null;

                secondCard=null;

                lockCards=false;

            },
            750
        );

    }

}


function completeMemoryGame(){

    document.getElementById(
        'matchResult'
    ).innerHTML=`

        <div class="script"
             style="font-size:42px;">

            MEMORY MASTER! 🥹❤️

        </div>

        <p>
            Tumne saari memories match kar li.
            Ab Memory Vault officially open hai. 🗝️
        </p>

    `;


    createHeartExplosion();

}


/* =====================================================
   YES / NO GAME
===================================================== */

function runAwayNo(){

    const button =
        document.getElementById(
            'loveNo'
        );


    if(!button) return;


    const x =
        (Math.random()-.5)*250;


    const y =
        (Math.random()-.5)*100;


    button.style.transform=
        `translate(${x}px,${y}px)`;

}


function loveNo(){

    runAwayNo();


    document.getElementById(
        'loveGameResult'
    ).innerText=
        "Nahi button tumse bhi zyada dar raha hai. 😂❤️";

}


function loveYes(){

    document.getElementById(
        'loveGameResult'
    ).innerHTML=`

        <div class="script"
             style="font-size:45px;">

            I KNEW IT! 🥹❤️

        </div>

        <p>
            Screenshot le liya.
            Ab lifetime contract signed hai. 😂❤️
        </p>

    `;


    createHeartExplosion();

}


/* =====================================================
   SECRET CODE
===================================================== */

function checkSecret(){

    const input =
        document.getElementById(
            'secretCode'
        );


    const answer =
        input.value
        .trim()
        .toLowerCase()
        .replace(/\s+/g,' ');


    const accepted=[

        '5 september',
        '5 sep',
        '5sep',
        'september 5',
        'ludo',
        'dodi dum',
        'thumak thumak'

    ];


    const message =
        document.getElementById(
            'secretMessage'
        );


    if(
        accepted.includes(answer)
    ){

        message.innerHTML=`

            <div class="script"
                 style="font-size:48px;">

                🔓 UNLOCKED

            </div>

            <p>
                You remembered the beginning. 🥹❤️
            </p>

            <button
                class="btn"
                onclick="nextPage()">

                Open The Final Surprise ❤️

            </button>

        `;


        createHeartExplosion();

    }else{

        message.innerHTML=`

            <p>
                Wrong secret. 👀

                <br><br>

                Hint:
                <strong>
                    5 September...
                </strong>
            </p>

        `;


        input.animate(

            [
                {
                    transform:'translateX(0)'
                },

                {
                    transform:'translateX(-8px)'
                },

                {
                    transform:'translateX(8px)'
                },

                {
                    transform:'translateX(0)'
                }

            ],

            {
                duration:300
            }

        );

    }

}


/* =====================================================
   FINAL CINEMATIC
===================================================== */

function openFinalHeart(){

    document.getElementById(
        'finalBeginning'
    ).style.display='none';


    document.getElementById(
        'finalReveal'
    ).style.display='block';


    const target =
        document.getElementById(
            'finalTyping'
        );


    const lines=[

        "Wait...",

        "There's one last thing.",

        "Something I want you to remember.",

        "If I had to choose again..."

    ];


    let line=0;


    function typeLine(){

        if(
            line >= lines.length
        ){

            setTimeout(
                ()=>{

                    document.getElementById(
                        'finalLetter'
                    ).style.display=
                        'block';


                    createFinalHeartRain();

                    window.scrollTo({
                        top:0,
                        behavior:'smooth'
                    });

                },
                900
            );

            return;

        }


        target.innerHTML='';


        const text=
            lines[line];


        let character=0;


        const typing=
            setInterval(
                ()=>{

                    target.innerHTML +=
                        text.charAt(
                            character
                        );


                    character++;


                    if(
                        character >=
                        text.length
                    ){

                        clearInterval(
                            typing
                        );


                        line++;


                        setTimeout(
                            typeLine,
                            1100
                        );

                    }

                },
                70
            );

    }


    typeLine();

}


/* =====================================================
   HEART EXPLOSION
===================================================== */

function createHeartExplosion(){

    for(
        let i=0;
        i<25;
        i++
    ){

        const heart =
            document.createElement(
                'div'
            );


        heart.innerText=
            [
                '❤️',
                '💗',
                '💕',
                '💖',
                '💘'
            ][
                Math.floor(
                    Math.random()*5
                )
            ];


        heart.style.position=
            'fixed';


        heart.style.left=
            '50%';


        heart.style.top=
            '50%';


        heart.style.zIndex=
            '99999';


        heart.style.pointerEvents=
            'none';


        heart.style.fontSize=
            (15+
            Math.random()*25)+
            'px';


        const x=
            (Math.random()-.5)*600;


        const y=
            (Math.random()-.5)*600;


        heart.animate(

            [

                {
                    transform:
                        'translate(-50%,-50%) scale(.3)',
                    opacity:1
                },

                {
                    transform:
                        `translate(
                            calc(-50% + ${x}px),
                            calc(-50% + ${y}px)
                        )
                        scale(1.2)`,
                    opacity:0
                }

            ],

            {
                duration:
                    1300+
                    Math.random()*800,

                easing:
                    'cubic-bezier(.2,.8,.2,1)'

            }

        );


        document.body.appendChild(
            heart
        );


        setTimeout(
            ()=>{
                heart.remove();
            },
            2200
        );

    }

}


/* =====================================================
   FINAL HEART RAIN
===================================================== */

function createFinalHeartRain(){

    for(
        let i=0;
        i<45;
        i++
    ){

        setTimeout(
            ()=>{

                const heart =
                    document.createElement(
                        'div'
                    );


                heart.innerText=
                    [
                        '❤️',
                        '💗',
                        '💕',
                        '💖',
                        '💘'
                    ][
                        Math.floor(
                            Math.random()*5
                        )
                    ];


                heart.style.position=
                    'fixed';


                heart.style.left=
                    Math.random()*100+
                    '%';


                heart.style.top=
                    '-50px';


                heart.style.zIndex=
                    '3';


                heart.style.pointerEvents=
                    'none';


                heart.style.fontSize=
                    (12+
                    Math.random()*27)+
                    'px';


                const duration=
                    4500+
                    Math.random()*5000;


                heart.animate(

                    [

                        {
                            transform:
                                'translateY(0) rotate(0deg)',
                            opacity:0
                        },

                        {
                            transform:
                                'translateY(35vh) rotate(130deg)',
                            opacity:1
                        },

                        {
                            transform:
                                'translateY(115vh) rotate(300deg)',
                            opacity:0
                        }

                    ],

                    {
                        duration:
                            duration,

                        easing:
                            'linear'
                    }

                );


                document.body.appendChild(
                    heart
                );


                setTimeout(
                    ()=>{
                        heart.remove();
                    },
                    duration
                );

            },
            i*120
        );

    }

}


/* =====================================================
   SECRET ENTER KEY
===================================================== */

document.addEventListener(
    'keydown',
    function(e){

        if(
            e.key === 'Enter'
        ){

            const secret =
                document.getElementById(
                    'secretCode'
                );


            if(
                document.activeElement ===
                secret
            ){

                checkSecret();

            }

        }

    }
);


/* =====================================================
   ARROW KEYS
===================================================== */

document.addEventListener(
    'keydown',
    function(e){

        if(
            e.key === 'ArrowRight'
        ){

            nextPage();

        }


        if(
            e.key === 'ArrowLeft'
        ){

            prevPage();

        }

    }
);


/* =====================================================
   INITIALIZE MEMORY GAME
===================================================== */

setupMemoryGame();


/* =====================================================
   FINAL COUNTER
===================================================== */

const counter =
    document.getElementById(
        'pageCounter'
    );


if(counter){

    counter.innerText=
        '1 / 20';

}


/* =====================================================
   DONE ❤️
===================================================== */

</script>


<!-- =====================================================
     WEBSITE COMPLETE
===================================================== -->

</body>
</html>
