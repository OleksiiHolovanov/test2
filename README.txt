SPORTYBET NIGERIA - STATIC AFFILIATE SITE
==========================================

Brand:       SportyBet Nigeria
Type:        Static HTML/CSS/JS affiliate site
Language:    EN only (Nigerian market, no Arabic)
Theme:       Dark base with SportyBet red header + green CTAs
Pages:       10 main + 404 + redirect loader = 12 HTML files

----------------------------------------------------------
1. FILE STRUCTURE
----------------------------------------------------------
/
├── index.html                  Home (hero, live odds, sports, live betting, app)
├── 404.html                    Error page
├── styles.css                  Full site CSS (SportyBet palette)
├── script.js                   Mobile nav toggle
├── sitemap.xml                 9 URLs
├── robots.txt                  Sitemap pointer, /play-sportybet/ disallowed
├── README.txt                  This file
├── assets/
│   ├── logo.webp               SportyBet wordmark (344x68, transparent)
│   ├── favicon.ico             64x64 favicon
│   └── [5 webp images]         TO BE GENERATED - see section 4 below
├── about/index.html
├── bonuses/index.html
├── contact/index.html
├── login/index.html
├── mobile-app/index.html
├── play-sportybet/index.html   Affiliate redirect loader (1.5s)
├── privacy/index.html
├── responsible-gaming/index.html
└── terms/index.html

----------------------------------------------------------
2. DOMAIN PLACEHOLDER - REPLACE BEFORE DEPLOY
----------------------------------------------------------
Throughout the HTML and sitemap.xml, the placeholder domain is:

   https://sportybet-qatar.com/

Search-and-replace this with your real production domain before deploying.

----------------------------------------------------------
3. AFFILIATE REDIRECT PLACEHOLDER - REPLACE BEFORE DEPLOY
----------------------------------------------------------
In /play-sportybet/index.html the redirect target is:

   https://www.sportybet.com/ng/

Replace this with your tracked affiliate link before deploying.

----------------------------------------------------------
4. IMAGES TO GENERATE
----------------------------------------------------------
The HTML references 5 webp images that are NOT included in this package.
Generate them externally and drop them into /assets/ with the exact filenames
below. Image prompts are provided in the chat reply that accompanies this zip.

Required files in /assets/:

   1. hero-football-bet.webp        900 x 620
   2. multi-sports-markets.webp     900 x 620
   3. live-betting-action.webp      900 x 620
   4. bonus-naira.webp              420 x 420
   5. sportybet-app-phone.webp      320 x 580

Until these files exist in /assets/, broken image icons will show on the site.
The site layout will still render correctly - only the visuals will be missing.

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
- All pages have unique title, description, keywords
- index.html includes Organization + WebSite schema
- contact/index.html includes FAQPage schema
- canonical + hreflang set on every page (en + x-default)
- 18+ messaging in footer of every page
- No casino content - betting-focused per brief

----------------------------------------------------------
7. WHAT'S DIFFERENT FROM THE TRUEWIN SOURCE
----------------------------------------------------------
- AR (Arabic) version dropped - Nigeria is EN market
- Casino section removed - replaced with sports markets + live betting
- Color palette swapped from gold/cyan to red/green
- Logo aspect ratio updated (was 324x132, now 344x68)
- Header height reduced (70px -> 64px) to match flatter wordmark
- All "TrueWin / Momentum Group / Abu Dhabi / UAE / AED" copy stripped
- Currency context now NGN / Naira
- Mobile number field uses +234 prefix
- Bonus copy reworked around sports betting offers
- Hero hook switched from "Casino in Abu Dhabi" to football/betting

----------------------------------------------------------
8. DEPLOY CHECKLIST
----------------------------------------------------------
[ ] Generate 5 webp images, drop into /assets/
[ ] Replace https://sportybet-qatar.com/ with real domain (sitemap + all HTML)
[ ] Replace https://www.sportybet.com/ng/ in /play-sportybet/ with tracked link
[ ] Confirm logo.webp + favicon.ico render correctly
[ ] Submit sitemap.xml in Search Console
[ ] Spot-check responsive layout at 360px, 768px, 1280px
