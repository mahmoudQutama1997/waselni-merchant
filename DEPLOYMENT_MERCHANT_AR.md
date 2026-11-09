# نشر بوابة التاجر على Vercel

## إعدادات Vercel
- Root Directory: `.` (جذر هذا المشروع)
- Build Command: `npm run build:merchant`
- Output Directory: `dist/merchant`
- Install Command: `npm install`

## متغيرات البيئة المطلوبة
أضف هذه المتغيرات في Vercel لكل من Preview وProduction:

- `VITE_API_URL` = `https://waselni-backend14.onrender.com/api`
- `VITE_OSRM_URL` = `https://router.project-osrm.org`
- `VITE_GEOCODING_URL` = `https://nominatim.openstreetmap.org/reverse`
- `VITE_WASELNI_APP_ROLE` = `merchant`

بعد حفظ المتغيرات، أعد Deploy.

## ملاحظة الصور
تمت إضافة معالجة لمسارات الصور النسبية القادمة من Django، بحيث تُحمّل من نطاق الخادم الخلفي بدلاً من نطاق Vercel. يجب أن تكون الصور محفوظة ومتاح الوصول إليها من الخادم الخلفي، وأن تكون إعدادات تخزين `MEDIA` في Django صحيحة.
