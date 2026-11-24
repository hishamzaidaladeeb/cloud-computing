# Cloud Computing — Educational Platform

منصة تعليمية ثابتة (Static Website) ثنائية اللغة لموضوعات الحوسبة السحابية، مبنية باستخدام HTML وCSS وJavaScript دون Backend.

## التشغيل المحلي

1. فك ضغط الملف.
2. افتح `index.html` مباشرة، أو شغّل خادمًا محليًا من مجلد المشروع:

```bash
python -m http.server 8000
```

ثم افتح `http://localhost:8000`.

## النشر على GitHub Pages

1. أنشئ مستودعًا عامًا على GitHub.
2. ارفع محتويات مجلد `cloud-computing-platform` إلى جذر المستودع (بحيث يكون `index.html` في الجذر).
3. افتح Settings → Pages.
4. اختر Deploy from a branch، ثم `main` و`/(root)`، واحفظ.
5. انتظر اكتمال النشر وافتح الرابط الذي تعرضه صفحة Pages.

المسارات المستخدمة داخل HTML نسبية، ولا توجد روابط `localhost` في ملفات الموقع.

## الملفات

- `index.html`: هيكل الصفحة، أدوات التحكم، والتنقل.
- `styles.css`: الأنماط الأساسية الأصلية.
- `refinements.css`: تحسينات الخطوط، الأكواد، القائمة الجانبية، والتجاوب.
- `app.js`: محتوى الدروس، الترجمات، الرسوم SVG، البحث والتنقل والتفضيلات.
- `assets/ibb-university-logo.jpg`: شعار جامعة إب المرفق.
- `assets/reference-interface.png`: صورة الواجهة المرجعية الأصلية.
- `assets/student-portrait.png`: الصورة الشخصية التي أرفقها المستخدم، معروضة في نهاية الموقع.
- `TEST_REPORT.md`: تقرير الاختبارات والقيود.

## الوظائف

- 13 موضوعًا رئيسيًا مع عرض موضوع واحد في كل مرة.
- العربية والإنجليزية مع ضبط `lang` و`dir`.
- الوضع الفاتح والداكن وحفظ اللغة والوضع والموضوع في `localStorage`.
- قاموس مصطلحات قابل للبحث والتصفية.
- تنقل جانبي على سطح المكتب وقائمة جانبية من زر Hamburger على الهاتف.
- مخططات SVG، جداول، أمثلة تعليمية، وأزرار نسخ للأكواد.

## الخطوط والاتصال

لا تعتمد النسخة على تحميل Google Fonts أو CDN لتشغيل المحتوى. تستخدم خطوط النظام مع سلاسل احتياطية للعربية والإنجليزية والأكواد؛ لذلك قد يختلف شكل الخط قليلًا بين الأجهزة بحسب الخطوط المثبتة محليًا.

## حدود المشروع

الموقع تعليمي ثابت. لا ينفذ أوامر Docker/Terraform ولا ينشئ موارد سحابية ولا يتصل بخدمات Backend. راجع توثيق مزودي الخدمات الرسمي قبل تطبيق الأمثلة في بيئة إنتاج.


## Local fonts and final visual corrections

The project now bundles Noto Sans Arabic (regular/bold), Inter (regular/medium/semibold/bold), and DejaVu Sans Mono under `assets/fonts/`. The font license/copyright notices are included beside the font files. The site does not require a font CDN for these families.

The Virtualization lesson now renders its diagram as responsive HTML/CSS: Physical Hardware → Hypervisor → three independent Virtual Machines. Arabic and English labels use separate elements with explicit text directions. On narrow screens the three VM cards stack vertically instead of shrinking the labels or clipping the diagram.

The supplied student portrait remains the original 1024×1536 image asset. Its display uses `object-fit: contain`; the animated orbit is a separate CSS ring and does not rotate, crop, or filter the photograph. Hover pauses the ring, and `prefers-reduced-motion` disables it.

## Editorial review
See `EDITORIAL_REVIEW.md` for the Arabic/English copy-editing scope, concrete revisions, and accuracy limitations. The academic identity is configured in `app.js`.
