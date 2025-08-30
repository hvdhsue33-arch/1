# 🚀 تعليمات النشر على GitHub و Netlify

## 📋 الخطوات المطلوبة:

### 1. رفع المشروع إلى GitHub

```bash
# تأكد من أنك في مجلد المشروع
cd C:\Users\SANAD\Desktop\WebTranslator\WebTranslator

# إضافة جميع الملفات
git add .

# عمل commit
git commit -m "نظام إبراهيم للمحاسبة - جاهز للنشر"

# رفع إلى GitHub (ستحتاج لإدخال بيانات GitHub)
git push -u origin main
```

### 2. النشر على Netlify

1. **اذهب إلى [Netlify](https://netlify.com)**
2. **انقر على "New site from Git"**
3. **اختر GitHub كمصدر**
4. **اختر المستودع: `mtzbay44-glitch/sanad`**
5. **اضبط إعدادات البناء:**
   - **Build command:** `npm run build`
   - **Publish directory:** `dist`
   - **Node version:** `18`

### 3. إعداد متغيرات البيئة في Netlify

في إعدادات الموقع، أضف المتغيرات التالية:

```
NODE_ENV=production
MONGODB_URI=mongodb+srv://sehx0190_db_user:Sanad$sa19971997@cluster0.yselhek.mongodb.net/?retryWrites=true&w=majority&appName=Cluster0
SESSION_SECRET=your-super-secret-key-here
```

### 4. تحديث API URL

في `client/src/lib/constants.tsx`، قم بتحديث:
```typescript
export const API_BASE_URL = process.env.NODE_ENV === 'production' 
  ? 'https://your-netlify-site.netlify.app/api' 
  : 'http://localhost:3000/api';
```

## 🎯 المشروع جاهز!

- ✅ **نظام محاسبة متكامل** مع واجهة متطورة
- ✅ **نظام مصادقة آمن** مع حماية المسارات
- ✅ **تصميم متجاوب** لجميع الأجهزة
- ✅ **دعم العملات المتعددة** (SYP, TRY, USD)
- ✅ **نظام صلاحيات متقدم** (6 مستويات)
- ✅ **إدارة المخزون** مع تنبيهات
- ✅ **تقارير مفصلة** مع إمكانية التصدير

## 🔐 بيانات تسجيل الدخول:

- **Admin:** `admin` / `Admin123!`
- **Owner:** `owner` / `Owner123!`
- **Manager:** `manager` / `Manager123!`
- **Accountant:** `accountant` / `Accountant123!`
- **Warehouse:** `warehouse` / `Warehouse123!`
- **Viewer:** `viewer` / `Viewer123!`

## 📁 هيكل المشروع:

```
WebTranslator/
├── client/                 # Frontend React
│   ├── src/
│   │   ├── components/     # مكونات الواجهة
│   │   ├── pages/         # صفحات التطبيق
│   │   ├── hooks/         # React Hooks
│   │   └── lib/           # مكتبات مساعدة
│   └── public/            # الملفات العامة
├── server/                # Backend Node.js
│   ├── routes/            # مسارات API
│   ├── storage.ts         # طبقة الوصول للبيانات
│   └── index.ts           # نقطة البداية
├── shared/                # الملفات المشتركة
│   └── schema.ts          # نماذج قاعدة البيانات
└── scripts/               # سكريبتات مساعدة
```

## 🛠️ التقنيات المستخدمة:

### Frontend:
- React 18 + TypeScript
- TailwindCSS + shadcn/ui
- Framer Motion للحركات
- React Query لإدارة البيانات
- Recharts للرسوم البيانية

### Backend:
- Node.js + Express
- MongoDB + Mongoose
- bcrypt للتشفير
- express-session للجلسات
- Zod للتحقق من البيانات

## 🎨 ميزات الواجهة:

- **خلفية متحركة** مع جزيئات عائمة
- **حركات سلسة** باستخدام Framer Motion
- **تصميم زجاجي** مع شفافية وظلال
- **تحقق من قوة كلمة المرور** مع نصائح
- **رسائل خطأ متحركة** تظهر وتختفي بسلاسة
- **تخطيط متجاوب** لجميع الأجهزة

---

**نظام إبراهيم للمحاسبة** - الحل الأمثل لإدارة أعمالك التجارية! 🚀
