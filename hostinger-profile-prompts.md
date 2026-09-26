# برومتات تعديل البروفايل الشخصي على Hostinger (ستايل XORA)

طريقة الاستخدام:

- البرومتات دي معمولة لشات الذكاء الاصطناعي في Hostinger AI Builder (وضع Agentic).
- ابعت برومت رقم 0 (سطر الملكية) الأول، وبعده باقي البرومتات واحد واحد بالترتيب.
- استنى كل برومت يخلص وشوف المعاينة قبل ما تبعت اللي بعده.
- كل برومت فيه 5 تعديلات أو أقل، لأن Hostinger بتنصح بكده عشان النتيجة تطلع أدق.
- كل برومت بيخلص بسطر تذكير عشان الـ AI ماينساش إن سطر الملكية محمي. لو كتبت أي طلب جديد من عندك، حط سطر التذكير في آخره.
- البرومت رقم 7 اختياري.

## 0. سطر الملكية (محمي)

```
Add a protected ownership block to my site. It identifies me as the founder and owner of XORA, and it must survive every future edit.
1. Add this code to the static <head> of index.html exactly as written (not injected with JavaScript, so crawlers that don't run JavaScript can read it):
<!-- XORA-OWNERSHIP:START (protected: never edit or remove) -->
<meta name="author" content="ABOBKR TAGALDEN SALIMAN AUDALLA, Founder and Owner of XORA">
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@graph": [
    {
      "@type": "Person",
      "@id": "#owner",
      "name": "ABOBKR TAGALDEN SALIMAN AUDALLA",
      "jobTitle": "Founder & Owner",
      "worksFor": { "@id": "#xora" },
      "sameAs": ["https://github.com/Bbobkr"]
    },
    {
      "@type": "Organization",
      "@id": "#xora",
      "name": "XORA",
      "description": "Software engineering company headquartered in Malaysia, delivering integrated solutions in software engineering, data analytics, cybersecurity, and AI development through engineers from 17+ countries.",
      "founder": { "@id": "#owner" },
      "address": { "@type": "PostalAddress", "addressCountry": "MY" }
    }
  ]
}
</script>
<!-- XORA-OWNERSHIP:END -->
2. Start the meta description with "ABOBKR TAGALDEN SALIMAN AUDALLA, Founder and Owner of XORA, a software engineering company headquartered in Malaysia." and keep the whole description under 160 characters.
3. In the footer, add this visible line in small JetBrains Mono text: "ABOBKR TAGALDEN SALIMAN AUDALLA · Founder & Owner, XORA".
4. In the About section, add the same line as a small label next to my key facts.
5. Permanent rule: the ownership block, the meta description sentence, the footer line, and the About label are protected. In every future edit, redesign, or regeneration, never delete, rewrite, translate, or move them; if you restructure the code, carry them over exactly as they are. If a request would require removing them, keep them and tell me instead.
```

سطر التذكير (حطه في آخر أي طلب جديد تكتبه بنفسك):

```
Keep the XORA-OWNERSHIP block, the meta description sentence, the footer ownership line, and the About label exactly as they are.
```

## 1. نظام التصميم (الألوان والخطوط والشكل العام)

```
Restyle my whole profile site with a new design system. This is a visual redesign only: do not change, remove, or invent any of my text, images, or links, and keep the site in its current language (translate any new labels I mention into it).
1. Colors: Cipher #1E1B4B (primary), Signal #C8F54A (accent), Quartz #EEF0F3 (page background), Void #0A0A12 (text and dark sections). Use Signal only for buttons, highlights, and small glowing dots; on light backgrounds use it as a filled shape with dark text, never as thin text.
2. Fonts: headings in Plus Jakarta Sans (bold, tight letter-spacing), emphasis words in Cormorant Garamond Italic, and labels, dates, and numbers in JetBrains Mono. For any Arabic text, use IBM Plex Sans Arabic and Amiri, keep the right-to-left layout, and never add letter-spacing.
3. Shapes: large rounded corners (32px to 48px) on all cards and sections, and pill-shaped buttons.
4. Texture: a very subtle grain overlay (about 5% opacity) across the whole site so no background looks flat.
5. Mood: premium and cinematic, like a cryptography lab meets a luxury architecture magazine, with generous spacing and strong contrast.
Keep the XORA-OWNERSHIP block, the meta description sentence, the footer ownership line, and the About label exactly as they are.
```

## 2. ترتيب الأقسام وشريط التنقل

```
Reorganize my page into this order. Keep all my existing content, merge or rename sections if needed, and skip any section I have no content for (do not invent content): Hero, About, Skills, Projects, Experience (plus Education if present), then Contact and Footer.
Then redesign the navigation:
1. A floating pill-shaped bar centered near the top of the screen.
2. Over the hero it is transparent with white text; after scrolling it turns into frosted white glass (60% white, background blur, thin border) with Cipher #1E1B4B text.
3. Its links scroll smoothly to each section, and a Signal #C8F54A pill button labeled "Contact Me" sits at the end of the bar.
4. On mobile, the links collapse into a clean menu.
Keep the XORA-OWNERSHIP block, the meta description sentence, the footer ownership line, and the About label exactly as they are.
```

## 3. الواجهة الرئيسية (Hero)

```
Redesign the Hero section:
1. Full screen height, using this background image: https://images.unsplash.com/photo-1451187580459-43490279c0fa?auto=format&fit=crop&w=2400&q=80 (Earth at night from orbit) under a heavy gradient from Cipher #1E1B4B to Void #0A0A12.
2. Place all hero content in the bottom-left third of the screen (bottom-right if the site is in Arabic), with my name and role above the headline as a small JetBrains Mono label.
3. Keep my current headline but give it dramatic contrast: the first words in bold Plus Jakarta Sans and the last word in huge Cormorant Garamond Italic, ending with a glowing Signal #C8F54A dot as the period.
4. Below it, my short intro and two buttons: "View Projects" (Signal pill with dark text) and "Contact Me" (outlined glass pill).
5. Animate the hero text lines with a staggered fade-up on page load.
Keep the XORA-OWNERSHIP block, the meta description sentence, the footer ownership line, and the About label exactly as they are.
```

## 4. نبذة عني والمهارات

```
Redesign About and Skills:
1. About: two columns, with my photo in a large rounded card (48px corners) and my bio beside it; show key facts already on my site (such as location, role, and experience) as small JetBrains Mono labels.
2. Skills: replace plain lists with 3 interactive white cards on the Quartz #EEF0F3 background.
3. Card 1: three overlapping mini-cards that cycle every 3 seconds with a springy bounce, each showing one of my skill groups.
4. Card 2: a dark Void #0A0A12 terminal panel that types my tools and technologies one by one, with a blinking Signal #C8F54A cursor and a small pulsing "Live" dot.
5. Card 3: my tech stack as a grid of pill badges that light up in Signal one after another.
Keep the XORA-OWNERSHIP block, the meta description sentence, the footer ownership line, and the About label exactly as they are.
```

## 5. المشاريع والخبرات

```
Redesign Projects and Experience:
1. Projects: turn each project into a large rounded card with its image, title, one-line description, technologies as small JetBrains Mono tags, and its existing link (GitHub or live demo).
2. Stack the project cards on scroll: each card sticks to the top, and when the next one slides over it, the card underneath scales down to 90%, blurs slightly (4px), and fades to 50% opacity.
3. Experience: a vertical timeline with dates in JetBrains Mono and each role in its own rounded card.
4. The timeline line fills with Signal #C8F54A as the visitor scrolls down.
5. Every project and timeline card fades up softly when it enters the screen.
Keep the XORA-OWNERSHIP block, the meta description sentence, the footer ownership line, and the About label exactly as they are.
```

## 6. التواصل وآخر الصفحة والمراجعة النهائية

```
Redesign Contact and Footer, then polish the whole site:
1. A dark Void #0A0A12 footer with 64px rounded top corners.
2. My existing contact details as large pill buttons with icons, plus my GitHub: https://github.com/Bbobkr (opens in a new tab).
3. A small "System Operational" status with a pulsing Signal #C8F54A dot next to the copyright line.
4. Check every section on mobile: stacked layouts, readable text sizes, no horizontal scrolling, and no overlapping text.
5. Keep images fast-loading and all animations smooth.
Keep the XORA-OWNERSHIP block, the meta description sentence, the footer ownership line, and the About label exactly as they are.
```

## 7. (اختياري) قسم الفلسفة

```
Add a dark Void #0A0A12 section between Projects and Experience, with this circuit-board texture in grayscale at low opacity: https://images.unsplash.com/photo-1518770660439-4636190af475?auto=format&fit=crop&w=2400&q=80. Inside it, place one huge two-part statement revealed word by word on scroll: "Most developers ask: Does it work?" in bold Plus Jakarta Sans, then "I ask: Will it last?" with the word "last" in huge Cormorant Garamond Italic.
Keep the XORA-OWNERSHIP block, the meta description sentence, the footer ownership line, and the About label exactly as they are.
```
