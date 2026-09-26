# برومت البروفايل الشخصي على Hostinger (ستايل المبرمجين المحترفين + ألوان XORA)

الموقع: https://abobkrtagalden.com

طريقة الاستخدام:

- البرومت ده معمول لشات الذكاء الاصطناعي في Hostinger AI Builder (وضع Agentic).
- ابعته مرة واحدة كرسالة كاملة، وده بيبني الموقع من جديد.
- بعد ما يخلص، صلّح أي تفاصيل برسائل قصيرة، وحط سطر التذكير في آخر كل رسالة.
- البرومت بيستخدم المحتوى اللي على موقعك الحالي. لو في حاجة ناقصة هتلاقي مكانها علامة زي [ADD PROJECT LINK]، املاها بإيدك بالضغط عليها (مجاني ومش بياكل من الرصيد).

## البرومت الكامل

```
Rebuild my personal website, https://abobkrtagalden.com, as a world-class developer portfolio on the level of the best personal sites of senior software engineers: clean, fast, content-first, with precise micro-interactions. Reuse all the real content already on my site (name, bio, photo, skills, projects, experience, education, contact links). Never invent anything: no fake projects, clients, metrics, testimonials, or dates. If something is missing, leave a clearly marked placeholder such as [ADD PROJECT LINK] for me to fill in. Keep the site in its current language (if it is Arabic, use a right-to-left layout).

1. IDENTITY
- Name: exactly as it appears on my site.
- Role line: my current title from the site + "Founder & Owner of XORA" (XORA is my software engineering company, headquartered in Malaysia).
- GitHub: https://github.com/Bbobkr

2. DESIGN SYSTEM
- Dark theme by default, with a light theme toggle.
- Dark: background Void #0A0A12, cards in Cipher #1E1B4B at low opacity, main text Quartz #EEF0F3, secondary text #9CA3AF, accent Signal #C8F54A for links, active states, and highlights.
- Light: background Quartz #EEF0F3, text Void #0A0A12, white cards; Signal only as filled shapes with dark text.
- Fonts: Plus Jakarta Sans for headings and body; JetBrains Mono for labels, dates, tags, numbers, and code; Cormorant Garamond Italic for one or two emphasis words only. For Arabic text: IBM Plex Sans Arabic and Amiri, with no letter-spacing.
- Shapes: 16px to 24px rounded cards, pill-shaped tags and buttons, thin 1px borders, and a very subtle grain overlay (4% opacity).
- On desktop, a soft Cipher radial spotlight follows the mouse across the background.
- Section labels in mono with numbers: "01 / About", "02 / Stack", and so on.

3. LAYOUT
- Desktop: two columns. The left column is sticky: my name (large, bold), role line, one-sentence tagline, a section navigation whose active item grows a Signal line as I scroll (tracked with IntersectionObserver), and social icons (GitHub plus my existing links) at the bottom. The right column scrolls through the sections.
- Mobile: one column with a compact top bar (name + menu), everything stacked, no horizontal scrolling.
- Command menu: pressing Ctrl+K (Cmd+K on Mac) opens a searchable menu to jump to any section, open GitHub, toggle the theme, or copy the page link. Show a small "Ctrl K" hint in the navigation.

4. SECTIONS (right column, in this order)
- Terminal intro: a small dark terminal card that types, with a blinking Signal cursor: "$ whoami" then my name; "$ cat role.txt" then my role line; "$ ls stack/" then my top 5 technologies from my site.
- 01 About: 2 to 3 short paragraphs from my bio, my photo in a rounded frame with a subtle Signal ring on hover, and key facts as small mono labels.
- 02 Stack: my technologies grouped as Languages, Frontend, Backend, Data & AI, Security, and Cloud & DevOps (skip empty groups), shown as mono pill tags.
- 03 Experience: starts with "Founder & Owner, XORA (Present)", then my roles from the site. Each item has dates in mono on the left and, on the right, role, company, a 1 to 2 line summary, and tech tags. Hovering an item lifts it onto a Cipher card, turns its title Signal, and dims the other items. End with "View Full Resume" if my site has a CV file.
- 04 Projects: my featured projects as cards with a thumbnail, a title with an arrow that nudges on hover, a 1 to 2 line description, tech tags, and GitHub or live links. Same hover behavior as Experience. End with "View all projects on GitHub".
- 05 Open Source: live data from the public GitHub API (https://api.github.com/users/Bbobkr and https://api.github.com/users/Bbobkr/repos?sort=updated&per_page=30): my public repo count, and the 6 most recently updated non-fork repos as cards (name, description, language dot, stars, last update). Cache the response in sessionStorage, and if the API fails, show a clean "View my GitHub" button instead.
- 06 Contact: one short invitation line, my existing contact channels as large pill buttons with icons, and GitHub.
- Footer: "ABOBKR TAGALDEN SALIMAN AUDALLA · Founder & Owner, XORA" in small mono text, the year, and a pulsing Signal dot.

5. MOTION AND QUALITY
- Subtle fade-up reveals on scroll only; no heavy or looping effects; respect prefers-reduced-motion.
- Lighthouse 95+: optimized lazy-loaded images, semantic HTML (header, nav, main, section, footer), one h1, visible keyboard focus, AA contrast, and alt text on every image.
- Meta title: "ABOBKR TAGALDEN SALIMAN AUDALLA | Founder & Owner of XORA". Add Open Graph and Twitter card tags using my photo.

6. OWNERSHIP BLOCK (PROTECTED)
- Add this code to the static <head> of index.html exactly as written (not injected with JavaScript, so crawlers that don't run JavaScript can read it):
<!-- XORA-OWNERSHIP:START (protected: never edit or remove) -->
<meta name="author" content="ABOBKR TAGALDEN SALIMAN AUDALLA, Founder and Owner of XORA">
<script type="application/ld+json" data-render-head>
{
  "@context": "https://schema.org",
  "@graph": [
    {
      "@type": "ProfilePage",
      "@id": "https://abobkrtagalden.com/#profilepage",
      "url": "https://abobkrtagalden.com/",
      "mainEntity": { "@id": "https://abobkrtagalden.com/#person" }
    },
    {
      "@type": "Person",
      "@id": "https://abobkrtagalden.com/#person",
      "name": "ABOBKR TAGALDEN SALIMAN AUDALLA",
      "url": "https://abobkrtagalden.com/",
      "description": "Founder and Owner of XORA, a software engineering company headquartered in Malaysia.",
      "jobTitle": "Founder & Owner",
      "worksFor": { "@id": "https://abobkrtagalden.com/#xora" },
      "sameAs": ["https://github.com/Bbobkr"]
    },
    {
      "@type": "Organization",
      "@id": "https://abobkrtagalden.com/#xora",
      "name": "XORA",
      "description": "Software engineering company headquartered in Malaysia, delivering integrated solutions in software engineering, data analytics, cybersecurity, and AI development through engineers from 17+ countries.",
      "founder": { "@id": "https://abobkrtagalden.com/#person" },
      "address": { "@type": "PostalAddress", "addressCountry": "MY" }
    }
  ]
}
</script>
<!-- XORA-OWNERSHIP:END -->
- Start the meta description with "ABOBKR TAGALDEN SALIMAN AUDALLA, Founder and Owner of XORA, a software engineering company headquartered in Malaysia." and keep it under 160 characters.
- Permanent rule: this block, the meta description sentence, and the footer ownership line are protected. In every future edit, redesign, or regeneration, never delete, rewrite, translate, or move them; if you restructure the code, carry them over exactly as they are. If a request would require removing them, keep them and tell me instead.
```

## سطر التذكير

حطه في آخر أي رسالة تعديل بعد كده:

```
Keep the XORA-OWNERSHIP block, the meta description sentence, and the footer ownership line exactly as they are.
```

## لو موقعك على الوضع اليدوي (Manual) ومفيهوش شات AI

- البرومت الكامل محتاج وضع Agentic. Hostinger عندها طريقة تحوّل بيها الموقع لوضع Agentic.
- لو هتفضل على الوضع اليدوي، تقدر تحط سطر الملكية لوحده:
  - من المحرر اضغط على النقط التلاتة، وبعدين Integrations، وبعدين Custom code.
  - الصق الكود من أول سطر `<!-- XORA-OWNERSHIP:START` لحد سطر `<!-- XORA-OWNERSHIP:END -->`.
  - الكود اللي في Custom code مش بيتأثر بتعديلات التصميم، فهيفضل محمي لوحده.
