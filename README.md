# السرّاد - قصص وروايات 📖

موقع لنشر القصص والروايات العربية مبني بـ [Hugo](https://gohugo.io/) مع قالب [PaperMod](https://github.com/adityatelange/hugo-PaperMod).

🌐 **الموقع:** [gamalasker.github.io/alsarrad](https://gamalasker.github.io/alsarrad/)

---

## إضافة قصة جديدة

لإضافة قصة جديدة، أنشئ ملف Markdown في مجلد `content/posts/`:

```markdown
---
title: "عنوان القصة"
date: 2026-03-29
draft: false
author: "اسم الكاتب"
categories: ["خيال", "مغامرة"]
tags: ["قصة قصيرة"]
description: "وصف مختصر للقصة"
---

مقدمة القصة تظهر في الصفحة الرئيسية...

<!--more-->

## الفصل الأول

محتوى القصة الكامل هنا...
```

أو باستخدام Hugo CLI:

```bash
hugo new posts/my-story.md
```

---

## التشغيل المحلي

```bash
# تثبيت Hugo Extended (الإصدار الموسّع)
# https://gohugo.io/installation/

# استيراد القالب
hugo mod get

# تشغيل خادم التطوير
hugo server -D

# افتح المتصفح على: http://localhost:1313/alsarrad/
```

---

## النشر التلقائي

الموقع يُنشر تلقائيًا على **GitHub Pages** عند كل `push` إلى الفرع `main`، عبر GitHub Actions (`.github/workflows/hugo.yml`).

لتفعيل النشر لأول مرة:
1. اذهب إلى **Settings** ← **Pages**
2. في **Source** اختر: **GitHub Actions**
3. ادمج الـ PR وانتظر دقيقة واحدة
4. الموقع سيكون متاحًا على `https://gamalasker.github.io/alsarrad/`

---

## هيكل المشروع

```
alsarrad/
├── hugo.yaml                    # إعدادات Hugo
├── go.mod                       # Hugo Modules
├── content/
│   ├── posts/                   # القصص والروايات
│   └── about.md                 # صفحة عن الموقع
├── archetypes/
│   └── default.md               # قالب المقالة الجديدة
├── static/
│   └── css/custom.css           # تنسيقات عربية مخصصة
├── layouts/
│   └── partials/extend_head.html
└── .github/workflows/hugo.yml   # GitHub Actions
```
