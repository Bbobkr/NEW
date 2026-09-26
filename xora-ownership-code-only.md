# إضافة XORA لبيانات موقعك (من غير أي تغيير في الشكل)

الموقع: https://abobkrtagalden.com

- موقعك فيه بالفعل بيانات منظمة (JSON-LD) كويسة جوه `index.html`: شخص (Person)، وموقع (WebSite)، وصفحة بروفايل (ProfilePage)، ومشاريعك زي CareLink.
- المعرّفات فيها (`#person` و `#profilepage`) هي نفس اللي في كودنا القديم. عشان كده لو حطينا كود منفصل، هيبقى في اسمين مختلفين لنفس الشخص.
- البرومت ده بيضيف XORA جوه البيانات الموجودة بدل ما يعمل كود تاني.
- الاسم الأساسي هيفضل زي ما هو على موقعك، واسمك الكامل وبالعربي هيتضافوا كأسماء تانية ليك، فأي طريقة كتابة توصّل ليك.

## البرومت (ابعته لشات الـ AI في Hostinger)

```
Update only the existing JSON-LD structured data in the <head> of index.html. Do not change anything visible (design, layout, text, and images stay exactly the same), and do not create a second JSON-LD block.
1. Add this node to the existing "@graph" array:
{
  "@type": "Organization",
  "@id": "https://abobkrtagalden.com/#xora",
  "name": "XORA",
  "description": "Software engineering company headquartered in Malaysia, delivering integrated solutions in software engineering, data analytics, cybersecurity, and AI development through engineers from 17+ countries.",
  "founder": { "@id": "https://abobkrtagalden.com/#person" },
  "address": { "@type": "PostalAddress", "addressCountry": "MY" }
}
2. In the existing Person node ("@id": "https://abobkrtagalden.com/#person"), keep all current properties and add: "worksFor": { "@id": "https://abobkrtagalden.com/#xora" }; "alternateName": ["ABOBKR TAGALDEN SALIMAN AUDALLA", "Abobkr Tagalden Saliman Audalla", "أبوبكر تاج الدين سليمان"] (merged with any existing values, no duplicates); and "Founder & Owner of XORA" added to jobTitle next to the current title (as an array). Make sure its "sameAs" includes "https://github.com/Bbobkr".
3. Add <meta name="author" content="Abobkr Tagalden, Founder and Owner of XORA"> to the <head>, and put the comment <!-- XORA-OWNERSHIP --> right above the JSON-LD script.
4. Set the meta description to: "Abobkr Tagalden, Founder & Owner of XORA, a software engineering company headquartered in Malaysia. أبوبكر تاج الدين سليمان، مؤسس ومالك شركة XORA."
5. Permanent rule: the XORA node, the Person additions, the author meta tag, and the meta description are protected. In every future edit, never delete or rewrite them; if you regenerate the SEO data, carry them over exactly.
```

## سطر التذكير

حطه في آخر أي طلب تعديل بعد كده:

```
Keep the XORA structured data, the author meta tag, and the meta description exactly as they are.
```

## اتأكد بعد النشر

- افتح `view-source:https://abobkrtagalden.com` وابحث عن `XORA`. لازم تلاقيه في البيانات المنظمة وفي وصف الموقع.
- افحص البيانات على https://validator.schema.org/#url=https%3A%2F%2Fabobkrtagalden.com%2F ولازم تلاقي Organization اسمها XORA من غير أخطاء.
- من Google Search Console: الصق لينك موقعك في خانة البحث، واضغط Request indexing.
