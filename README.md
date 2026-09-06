# منصة أستاذي التعليمية — Android

هذا مشروع Android Studio يحوّل واجهة JavaScript المرفقة إلى تطبيق Android باستخدام WebView.

## قبل التشغيل
الملف `app.js` يعتمد على خادم خلفي عبر مسارات API مثل `/api/login` و`/api/courses` و`/api/dashboard` و`/api/progress` و`/api/enroll` و`/api/lessons` و`/api/students`.

عدّل عنوان الخادم في `index.html` أو خزّنه في `localStorage` باسم `apiBase`، ثم شغّل المشروع من Android Studio.

## البناء
افتح مجلد المشروع في Android Studio، ثم اختر **Build > Build APK(s)**.

> لا يمكن إنشاء APK نهائي داخل هذه البيئة لأن Android SDK/Gradle غير متوفرين هنا، لكن المشروع يتضمن ملفات المصدر والواجهة و`app.js` جاهزة للبناء.
