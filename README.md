# السرّاد - قصص وروايات

موقع لنشر القصص والروايات العربية  
🌐 **الموقع المباشر:** https://gamalasker.github.io/alsarrad/

---

## 🚀 كيفية نشر الموقع على GitHub Pages

### الخطوة 1 — تفعيل GitHub Pages (مرة واحدة فقط)

1. افتح صفحة المستودع على GitHub: https://github.com/gamalasker/alsarrad
2. انقر على **Settings** (الإعدادات) من القائمة العلوية
3. في القائمة الجانبية اليسرى، انقر على **Pages**
4. تحت قسم **Build and deployment** غيّر المصدر (Source) إلى **GitHub Actions**
5. احفظ التغييرات

### الخطوة 2 — دمج التغييرات في الفرع الرئيسي

بعد تفعيل GitHub Pages، كل ما عليك فعله هو دمج (merge) أي تحديثات في الفرع `main`:

- ادمج هذا الـ Pull Request في الفرع `main`
- سيبدأ النشر تلقائيًا خلال دقيقة أو دقيقتين

### الخطوة 3 — متابعة حالة النشر

1. افتح تبويب **Actions** في المستودع: https://github.com/gamalasker/alsarrad/actions
2. ستجد سير عمل (workflow) باسم **Deploy Hugo site to Pages** قيد التشغيل
3. بعد اكتمال النشر ✅، الموقع متاح على: https://gamalasker.github.io/alsarrad/

---

## ✍️ كيفية إضافة قصة جديدة

1. أنشئ ملف Markdown جديدًا في مجلد `content/posts/`، مثلًا `content/posts/my-new-story.md`
2. استخدم هذا القالب في أول الملف:

```markdown
---
title: "عنوان قصتك"
date: 2026-03-30
draft: false
author: "السرّاد"
categories: ["خيال"]
tags: ["قصة قصيرة"]
description: "وصف مختصر للقصة"
---

مقدمة القصة هنا...

<!--more-->

## الفصل الأول

محتوى القصة هنا...
```

3. تأكد أن `draft: false` لكي تظهر القصة على الموقع
4. ارفع (push) التغييرات إلى الفرع `main` — سينشر الموقع تلقائيًا

---

## 💻 التشغيل المحلي (للمعاينة قبل النشر)

```bash
# 1. تثبيت Hugo Extended من: https://gohugo.io/installation/

# 2. استنساخ المستودع
git clone https://github.com/gamalasker/alsarrad.git
cd alsarrad

# 3. تحميل قالب PaperMod
hugo mod get

# 4. تشغيل الخادم المحلي
hugo server -D

# افتح المتصفح على: http://localhost:1313/alsarrad/
```

---

## 📁 هيكل المشروع

```
alsarrad/
├── .github/workflows/hugo.yml   # نشر تلقائي عند الدفع إلى main
├── content/
│   ├── posts/                   # القصص والمقالات
│   └── about.md                 # صفحة عن الموقع
├── static/css/custom.css        # تنسيقات عربية مخصصة
├── hugo.yaml                    # إعدادات الموقع
└── go.mod                       # إدارة الحزم (Hugo Modules)
```

---

## ⚙️ النشر التلقائي

يعمل الموقع بنظام **GitHub Actions** الذي يقوم تلقائيًا بـ:

1. بناء الموقع باستخدام Hugo عند كل دفع (push) إلى الفرع `main`
2. نشره على GitHub Pages

**لا تحتاج إلى أي إجراء يدوي** بعد إعداد GitHub Pages في الإعدادات — فقط ادفع تغييراتك إلى `main` وسيتولى النظام الباقي.
