# Backend — منصة أستاذي

REST API مبني بـ Node.js وSQLite، ومتوافق مع تطبيق Android المرفق.

## التشغيل

```bash
cp .env.example .env
npm run seed
npm start
```

أو:

```bash
docker compose up -d --build
```

## أهم المسارات

- `POST /api/register` — تسجيل طالب
- `POST /api/register/teacher` — تسجيل معلم برمز دعوة
- `POST /api/login` — الدخول وإصدار JWT
- `GET /api/courses` — قائمة الدورات
- `GET /api/courses/:id` — تفاصيل الدورة
- `POST/PUT/DELETE /api/courses/:id` — إدارة الدورة للمعلم
- `POST/PUT/DELETE /api/lessons/:id` — إدارة الدروس
- `POST/DELETE /api/materials/:id` — إدارة المواد
- `POST/PUT/DELETE /api/quizzes/:id` — إدارة الاختبارات
- `POST/DELETE /api/questions/:id` — إدارة الأسئلة
- `GET /api/admin/overview` — إحصاءات الإدارة
- `GET /api/students` — قائمة الطلاب
- `POST /api/uploads` — رفع ملف Base64 محدود الحجم (PDF/MP4/WebM/MP3 وغيرها)

## الأمان

- كلمات المرور لا تُخزّن كنص صريح؛ تستخدم `scrypt` مع salt.
- نقاط إدارة المعلم محمية بـ JWT وصلاحية `teacher`.
- المعلم لا يستطيع تعديل دورة معلم آخر.
- قاعدة البيانات تستخدم foreign keys وWAL.

## إعدادات البيئة

راجع `.env.example`. في الإنتاج غيّر `JWT_SECRET` و`TEACHER_INVITE_CODE` و`PUBLIC_BASE_URL`.
