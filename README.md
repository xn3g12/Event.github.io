```html
<!DOCTYPE html>
<html lang="de">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Einladung - Ahmad & Mina</title>

<!-- Google Fonts -->
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Gulzar&family=Meie+Script&family=Playfair+Display:wght@700&family=Great+Vibes:wght@400;700&display=swap" rel="stylesheet">

<style>
    /* Basis */
    body {
        margin: 0;
        font-family: 'Great Vibes', cursive;
        background: #f8f8f8;
        font-size: clamp(18px, 2.8vw, 26px);
        letter-spacing: 2px;
        color: #333;
        line-height: 1.8;
    }

    section {
        padding: 40px 20px;
        max-width: 900px;
        margin: auto;
        opacity: 0;
        transform: translateY(30px);
        animation: fadeIn 1.5s forwards;
    }

    h1 { font-size: clamp(40px, 8vw, 64px); color: #444; }
    h2 { font-size: clamp(32px, 6vw, 48px); margin-bottom: 20px; color: #444; }
    h3 { font-size: clamp(18px, 3.5vw, 22px); color: #333; margin:0; }
    h5 { font-family: 'Meie Script'; font-size: clamp(26px,5vw,44px); text-align:center; margin-bottom:20px; color:#444; }
    p { margin: 6px 0; font-size: clamp(18px, 3vw, 24px); color:#333; }

    .persian-line {
        font-family: 'Gulzar', serif;
        direction: rtl;
        unicode-bidi: isolate;
        font-size: 22px;
        line-height: 1.8;
        color: #333;
    }

    .hero {
        height: 70vh;
        background: url('hero.png') center/cover no-repeat;
        display: flex;
        justify-content: center;
        align-items: center;
        color: #fff;
        text-shadow: 0 2px 4px rgba(0,0,0,0.6);
        position: relative;
    }

    .hero::after {
        content:"";
        position:absolute;
        left:0; right:0; bottom:0;
        height:120px;
        pointer-events:none;
        background: linear-gradient(to bottom, rgba(248,248,248,0) 0%, rgba(248,248,248,0.7) 60%, #f8f8f8 100%);
    }

    .monogram { text-align:center; }
    .monogram .initials {
        font-family:'Playfair Display', serif;
        font-size: 100px;
        font-weight: bold;
        letter-spacing:10px;
    }
    .monogram .symbol::before { content:"♥"; color:#fff; font-size:50px; margin:0 10px; display:inline-block; }

    .extra-space{ height:40px; display:block; }
    .extra-space1{ height:25px; display:block; }
    .extra-space2{ height:15px; display:block; }

    .map { width:100%; border-radius:8px; margin-top:16px; }

    .timing-container { display:flex; flex-direction:column; gap:20px; border-left:2px solid #ccc; padding-left:20px; }
    .event { display:flex; gap:20px; align-items:flex-start; }
    .time { width:70px; text-align:right; font-size:30px; font-weight:700; color:#555; }
    .details h3 { margin:0; }
    .details p { margin:4px 0 0; color:#666; }

    @keyframes fadeIn { to { opacity:1; transform:translateY(0);} }

    @media(max-width:600px){
        h1{font-size:50px;}
        h2{font-size:40px;}
        h3{font-size:24px;}
        h5{font-size:36px;}
        p{font-size:22px;}
        .time{width:60px; font-size:22px;}
    }
</style>

<script>
document.addEventListener('DOMContentLoaded', function(){
    const elements = document.querySelectorAll('section');
    const observer = new IntersectionObserver(entries=>{
        entries.forEach(entry=>{
            if(entry.isIntersecting){
                entry.target.classList.add('visible');
            }
        });
    },{threshold:0.2});
    elements.forEach(el=>observer.observe(el));
});
</script>

</head>
<body>

<section class="hero">
    <div class="monogram">
        <div class="initials">A<span class="symbol"></span>M</div>
        <div class="sub">Save the Date</div>
        <div class="sub">20/03/2026</div>
    </div>
</section>

<section>
    <h5>Ahmad & Mina</h5>
    <p>Liebe Familie und Freunde,</p>
    <p>
        Wir freuen uns sehr, euch am <strong>20. März 2026 um 16:00 Uhr</strong> zu unserer Hochzeit einzuladen. Wir können es kaum erwarten, diesen einzigartigen Moment mit euch zu teilen.
    </p>
    <p>Wir bitten euch, uns bis Anfang Februar mitzuteilen, ob ihr dabei sein könnt.</p>
    <p>Sie sind herzlich eingeladen – die Einladung gilt für <strong>4 Personen</strong>.</p>

    <p class="persian-line">به همراه خانواده‌های عزیزمان،</p>
    <p class="persian-line">شما را با کمال افتخار دعوت می‌کنیم</p>
    <p class="persian-line">تا در جشن آغاز زندگی مشترکمان کنار ما باشید.</p>
</section>

<section>
    <h2>Timing</h2>
    <div class="timing-container">
        <div class="event">
            <div class="time">16:00</div>
            <div class="details"><h3>Einlass</h3></div>
        </div>
        <div class="event">
            <div class="time">18:00</div>
            <div class="details"><h3>Brautpaars in Gand Afghani</h3></div>
        </div>
        <div class="event">
            <div class="time">19:30</div>
            <div class="details"><h3>Abendessen</h3></div>
        </div>
        <div class="event">
            <div class="time">21:30</div>
            <div class="details"><h3>Hochzeitsoutfit</h3></div>
        </div>
        <div class="event">
            <div class="time">22:30</div>
            <div class="details"><h3>Tanz & Party</h3></div>
        </div>
        <div class="event">
            <div class="time">12:00</div>
            <div class="details"><h3>Schluss</h3></div>
        </div>
    </div>
</section>

<section>
    <h2>Location / Ariana Event</h2>
    <img src="map.png" alt="Karte zur Location" class="map">
    <p>Christine‑Touaillon‑Straße 4, 1220 Wien</p>
</section>

</body>
</html>
```
