# منصة أستاذي التعليمية — Android + Backend

مشروع متكامل مبدئيًا لمنصة تعليمية عربية، يتكون من:

1. تطبيق Android مبني بواجهة WebView وواجهة RTL.
2. Backend REST API بـ Node.js.
3. SQLite database.
4. JWT authentication.
5. حسابات الطلاب والمعلمين.
6. لوحة تحكم للمعلم لإدارة الدورات والدروس والمواد والاختبارات والأسئلة والطلاب.
7. رفع ملفات تعليمية محدود الحجم عبر API.

## تشغيل Backend

```bash
cd backend
cp .env.example .env
npm run seed
npm start
```

## تشغيل Docker

```bash
docker compose up -d --build
```

## تشغيل Android

افتح مجلد `android` في Android Studio، ثم اربط عنوان الـ API عند الحاجة عبر:

`?api=http://SERVER-IP:3000`

في المحاكي Android الافتراضي، القيمة الافتراضية هي `http://10.0.2.2:3000`.
