# 💍 Hochzeitseinladung – Ahmad & Mina

Dieses Repository enthält den vollständigen HTML-, CSS- und JavaScript-Code
für unsere Hochzeitseinladung.

---

## 📄 Code (nur Anzeige, kein Rendering)

```html
<title>Einladung</title>
<style>
    /* Globale Basis: überall Tangerine (außer gezielte Ausnahmen) */
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

    h1 { font-size: clamp(40px, 8vw, 64px); }
    h2 { font-size: clamp(32px, 6vw, 48px); }
    h3 { font-size: clamp(18px, 3.5vw, 22px); }
    h4 { font-size: clamp(22px, 4vw, 28px); }

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
        line-height: 1.8;
    }

    @keyframes fadeIn {
        to { opacity: 1; transform: translateY(0); }
    }
</style>

<script>
    document.addEventListener('DOMContentLoaded', function () {
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
