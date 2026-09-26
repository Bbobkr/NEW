# إضافة اسم شركة XORA في كود الموقع بس (من غير أي تغيير في الشكل)

الموقع: https://abobkrtagalden.com

- الكود ده بيتحط في رأس الصفحة (head)، ومش بيظهر للزوار خالص.
- جوجل وBing وأدوات الذكاء الاصطناعي بيقروه وبيعرفوا منه إنك مؤسس ومالك XORA.

## لو المحرر فيه شات AI (وضع Agentic): ابعت البرومت ده

```
Add my company name to the code of my website only, for search engines and AI crawlers. Do not change anything visible: no changes to the design, layout, colors, fonts, text, images, sections, or animations. The page must look exactly the same as it does now.
1. Add this code to the static <head> of index.html exactly as written (not injected with JavaScript, and without adding any visible element):
<!-- XORA-OWNERSHIP:START (protected: never edit or remove) -->
<meta name="author" content="ABOBKR TAGALDEN SALIMAN AUDALLA, Founder and Owner of XORA">
<link rel="me" href="https://github.com/Bbobkr">
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
2. Permanent rule: this block is protected. In every future edit, never delete, rewrite, or move it; if you restructure the code, carry it over exactly as it is.
```

سطر التذكير (حطه في آخر أي طلب تعديل بعد كده):

```
Keep the XORA-OWNERSHIP block in the <head> exactly as it is.
```

## لو المحرر مفيهوش شات (الوضع اليدوي Manual): من غير برومت

- من المحرر اضغط على النقط التلاتة، وبعدين Integrations، وبعدين Custom code.
- الصق الكود من أول سطر `<!-- XORA-OWNERSHIP:START` لحد سطر `<!-- XORA-OWNERSHIP:END -->`.
- ده مش بيغيّر شكل الموقع، ومش بيتأثر بأي تعديلات في التصميم.

## عنوان الصفحة ووصفها (مش بيظهروا جوه الصفحة)

- العنوان بيظهر في تاب المتصفح ونتايج البحث بس، والوصف بيظهر تحت اسم الموقع في نتايج البحث.
- دول أول حاجة جوجل وأدوات الذكاء الاصطناعي بيقروها لما حد يدور على اسمك.
- في وضع Agentic ابعت البرومت ده. في الوضع اليدوي، حطهم بإيدك من إعدادات SEO للصفحة.

```
Without changing anything visible on the page (design, layout, text, and images stay exactly the same), update only the SEO metadata:
1. Page title: "ABOBKR TAGALDEN SALIMAN AUDALLA | Founder & Owner of XORA"
2. Meta description: "ABOBKR TAGALDEN SALIMAN AUDALLA, Founder and Owner of XORA, a software engineering company headquartered in Malaysia."
Keep the XORA-OWNERSHIP block in the <head> exactly as it is.
```

## اتأكد بعد النشر

- افتح الموقع، واضغط `Ctrl + U` وبعدين `Ctrl + F`، وابحث عن `XORA-OWNERSHIP`.
- افحص البيانات على https://validator.schema.org/#url=https%3A%2F%2Fabobkrtagalden.com%2F ولازم يظهر ProfilePage و Person و Organization من غير أخطاء.
