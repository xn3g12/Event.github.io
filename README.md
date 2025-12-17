```html
<title>Einladung</title>
<style>
    body {
        margin: 0;
        font-family: 'Great Vibes', cursive;
        background: #f8f8f8;
        font-size: clamp(18px, 2.8vw, 26px);  
        letter-spacing: 4px;
        color: #333;
        line-height: 2;
    }

    p, h1, h2, h3, h4, h5, h6 {
        margin-bottom: 13px;
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
    h2 { font-size: clamp(32px, 6vw, 48px); color: #444; }
    h3 { font-size: clamp(18px, 3.5vw, 22px); color: #333; }
    h4 { font-size: clamp(22px, 4vw, 28px); color: #333; }

    h5 {
        text-align: center;
        font-size: clamp(26px, 5vw, 44px);
        font-family: 'Meie Script';
    }

    p {
        font-size: clamp(18px, 3vw, 24px);
    }

    .persian-line {
        font-family: 'Gulzar', serif;
        direction: rtl;
        unicode-bidi: isolate;
        font-size: 22px;
        line-height: 1.8;
    }

    .hero {
        height: 70vh;
        background: url('hero.png') center/cover no-repeat;
        display: flex;
        justify-content: center;
        align-items: center;
        color: #fff;
    }

    .map {
        width: 100%;
        border-radius: 8px;
    }

    @keyframes fadeIn {
        to { opacity: 1; transform: translateY(0); }
    }
</style>

<script>
    document.addEventListener('DOMContentLoaded', function() {
        const elements = document.querySelectorAll('.animate-on-scroll');
        const observer = new IntersectionObserver(entries => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                }
            });
        });
        elements.forEach(el => observer.observe(el));
    });
</script>

<section class="hero">
    <div class="monogram">
        <div class="initials">A ♥ M</div>
        <div class="sub">Save the Date</div>
        <div class="sub">20/03/2026</div>
    </div>
</section>

<section class="intro">
    <h5>Ahmad & Mina</h5>
    <p>Liebe Familie und Freunde,</p>
    <p>
        Wir freuen uns sehr, euch am <strong>20. März 2026 um 16:00</strong>
        Uhr zu unserer Hochzeit einzuladen.
    </p>

    <p class="persian-line">این یک خط فارسی با فونت گلزار است.</p>
    <p class="persian-line">این یک خط فارسی دیگر با فونت گلزار است.</p>
</section>

<img src="map.png" alt="Karte zur Location" class="map">
