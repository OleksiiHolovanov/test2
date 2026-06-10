SPORTYBET QATAR - STATIC AFFILIATE SITE (BILINGUAL EN/AR)
==========================================================

Brand:       SportyBet Qatar
Type:        Static HTML/CSS/JS affiliate site
Languages:   English (root) + Arabic (/ar/)
Theme:       Dark base with SportyBet red header + green CTAs
Pages:       9 main EN + 9 main AR + 2 redirect loaders + 1 error page = 21 HTML files

----------------------------------------------------------
1. FILE STRUCTURE
----------------------------------------------------------
/
├── index.html                     EN Home (hero, live odds, sports, live betting, app)
├── 404.html                       Error page (EN, noindex)
├── styles.css                     Full site CSS (SportyBet palette, shared EN+AR)
├── script.js                      Mobile nav toggle (shared EN+AR)
├── sitemap.xml                    18 URLs (9 EN + 9 AR with full hreflang)
├── robots.txt                     Sitemap pointer, /play-sportybet/ + /ar/play-sportybet/ disallowed
├── README.txt                     This file
├── assets/
│   ├── logo.webp                  SportyBet wordmark (344x68, transparent)
│   ├── favicon.ico                64x64 favicon
│   └── *.webp                     All shared between EN and AR (paths relative)
│
├── about/index.html               EN: About SportyBet Qatar
├── bonuses/index.html             EN: Bonuses & Promotions
├── contact/index.html             EN: Contact & Support (FAQPage schema)
├── login/index.html               EN: Login guide (+974 country code)
├── mobile-app/index.html          EN: Mobile App page
├── play-sportybet/index.html      EN affiliate redirect loader (1.5s)
├── privacy/index.html             EN: Privacy Policy
├── responsible-gaming/index.html  EN: Responsible Gaming
├── terms/index.html               EN: Terms & Conditions
│
└── ar/                            Arabic version (lang="ar" dir="rtl")
    ├── index.html                 AR Home (full RTL mirror)
    ├── about/index.html           AR: من نحن
    ├── bonuses/index.html         AR: العروض
    ├── contact/index.html         AR: التواصل والدعم (FAQPage schema in Arabic)
    ├── login/index.html           AR: تسجيل الدخول
    ├── mobile-app/index.html      AR: تطبيق الجوال
    ├── play-sportybet/index.html  AR affiliate redirect loader (1.5s, RTL)
    ├── privacy/index.html         AR: سياسة الخصوصية
    ├── responsible-gaming/index.html  AR: اللعب المسؤول
    └── terms/index.html           AR: الشروط والأحكام

----------------------------------------------------------
2. DOMAIN PLACEHOLDER - REPLACE BEFORE DEPLOY
----------------------------------------------------------
Throughout the HTML and sitemap.xml, the placeholder domain is:

   https://sportybet-qatar.com/

Search-and-replace this with your real production domain before deploying.

----------------------------------------------------------
3. AFFILIATE REDIRECT PLACEHOLDER - REPLACE BEFORE DEPLOY
----------------------------------------------------------
In /play-sportybet/index.html and /ar/play-sportybet/index.html the redirect
target is:

   https://www.time4bets504.com/

Replace this with your tracked affiliate link before deploying. Both loaders
must point to the same destination.

----------------------------------------------------------
4. ASSETS NOTE
----------------------------------------------------------
All image assets sit in /assets/ and are shared between EN and AR. Filenames
were kept as-is from the prior build (e.g. bonus-naira.webp) - layout and
asset names were intentionally not touched per the production rework.

Path conventions:
   - Root EN pages:        assets/foo.webp        styles.css        script.js
   - Inner EN pages:       ../assets/foo.webp     ../styles.css     ../script.js
   - AR home (/ar/):       ../assets/foo.webp     ../styles.css     ../script.js
   - AR inner pages:       ../../assets/foo.webp  ../../styles.css  ../../script.js

----------------------------------------------------------
5. BRAND TOKENS (in styles.css)
----------------------------------------------------------
   --red:        #e30613   Header bar, accent dots, hot states
   --red-bright: #ff2434   Hover lifts
   --red-deep:   #b50410   Pressed states
   --green:      #22c55e   Primary CTA fill (Register, Bet now)
   --green-bright:#34d76d  Primary CTA hover
   --green-deep: #16a34a   Primary CTA active
   --yellow:     #ffc629   HOT badge, accent highlight
   --bg:         #070b14   Page background
   --surface:    #0f1521   Card background
   --text:       #f3f5f9   Body text
   --muted:      #98a4b6   Secondary text

----------------------------------------------------------
6. SEO NOTES
----------------------------------------------------------
- All pages have unique title, description, keywords (EN in English, AR in Arabic)
- index.html (EN) and ar/index.html include Organization + WebSite schema
- contact/index.html and ar/contact/index.html include FAQPage schema
- canonical set on every page
- hreflang set on every page: en + ar + x-default (pointing to EN)
- og:locale: en_QA on EN, ar_QA on AR (with en_QA as og:locale:alternate on AR)
- 18+ messaging in footer of every page (EN: "18+", AR: "+18")
- /play-sportybet/ and /ar/play-sportybet/ both noindex,nofollow + disallowed in robots
- No casino content - sports betting only
- Honest legality framing: no claim of in-country license, "operator within the
  regulatory frame of the markets it serves", user responsibility to know
  local rules

----------------------------------------------------------
7. LOCALIZATION NOTES
----------------------------------------------------------
EN copy targets a Qatar audience:
  - Brand: SportyBet Qatar / SportyBet Doha (alternate name)
  - Country code: +974
  - Currency context: Riyal (QAR)
  - Local leagues referenced: Qatar Stars League (QSL), AFC Asian Cup,
    AFC Champions League
  - Local clubs referenced on homepage: Al Sadd, Al Duhail, Al Rayyan
  - International coverage retained: EPL, La Liga, UCL, NBA, ATP/WTA

AR copy is a direct localized translation:
  - Brand transliteration: سبورتي بيت
  - lang="ar" dir="rtl" on every AR page
  - All UI strings, headings, body copy, FAQ schemas, alt text translated
  - Currency notes: "أوراق ريال"
  - Country code shown as 974+ (Arabic convention places + after digits in
    body text, though the schema uses the same +974 numeric form)
  - 18+ rendered as +18 in Arabic (RTL convention)

CSS is shared. AR pages rely on the same stylesheet with `dir="rtl"` at the
html element. No CSS modifications were made.

----------------------------------------------------------
8. DEPLOY CHECKLIST
----------------------------------------------------------
[ ] Replace https://sportybet-qatar.com/ with real domain (sitemap + all HTML)
[ ] Replace https://www.time4bets504.com/ in BOTH /play-sportybet/ loaders
    with tracked affiliate link
[ ] Confirm logo.webp + favicon.ico render correctly
[ ] Submit sitemap.xml in Search Console
[ ] Verify hreflang setup in Search Console (International Targeting)
[ ] Spot-check responsive layout at 360px, 768px, 1280px
[ ] Spot-check AR pages render RTL correctly
[ ] Verify FAQPage schema validates for both contact pages
