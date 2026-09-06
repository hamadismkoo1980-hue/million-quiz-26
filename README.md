# Million Quiz 2026 — Cloudflare Pages + D1

هذه النسخة تعتمد على GitHub + Cloudflare Pages + Pages Functions + D1.

## ترتيب الملفات
- `index.html` الواجهة
- `admin.html` إنشاء أكواد دخول
- `functions/api/*` الخادم
- `sql/schema.sql` الجداول
- `sql/questions.sql` بنك الأسئلة

## إعداد Cloudflare
1. أنشئ حساب Cloudflare.
2. Workers & Pages → Create application → Pages → Connect to Git.
3. اختر مستودع GitHub الجديد.
4. بدون build command للمشروع البسيط.
5. بعد إنشاء Pages project: Settings → Bindings → Add D1 database binding.
6. اسم المتغير في binding هو `DB`.
7. أنشئ D1 database.
8. نفّذ `schema.sql` ثم `questions.sql` في D1.
9. Settings → Variables and Secrets: أضف secret باسم `ADMIN_SECRET`.
10. أعد النشر.

## إنشاء كود
افتح `/admin.html` وأدخل السر الإداري. كل كود يبدأ بـ `MQ-` ويخزن في قاعدة البيانات كـ SHA-256.

## الدفع
الواجهة تعرض Sham Cash والمحفظة مع زر نسخ، ثم واتساب لإرسال رقم العملية. التحقق من التحويل يدوي في هذه النسخة.

## الموسيقى
ضع رابطاً لملف صوتي تملك حق استخدامه في `CONFIG` داخل `index.html`. لم نضمّن موسيقى خارجية محمية.

## الاقتصاد
مثال معلن: 60% من المشاركات المقبولة لصندوق الجوائز، 20% تشغيل وإدارة، 10% تسويق، 10% احتياطي. هذه نسب نموذجية وليست ضماناً للربح.

## ملاحظة قانونية
المسابقات ذات رسوم دخول وجوائز مالية قد تخضع لأنظمة تختلف حسب الدولة. يجب مراجعة القوانين وشروط الدفع قبل الإطلاق التجاري.
