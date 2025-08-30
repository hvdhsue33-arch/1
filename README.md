# نظام إبراهيم للمحاسبة 🏢

نظام محاسبة متكامل ومتطور مصمم خصيصاً لأصحاب المحلات التجارية والمشاريع الصغيرة والمتوسطة.

## ✨ الميزات الرئيسية

- 🎨 **واجهة متطورة** مع تصميم حديث وتفاعلي
- 📊 **لوحة تحكم شاملة** مع رسوم بيانية وإحصائيات
- 👥 **نظام صلاحيات متقدم** (RBAC) مع 6 مستويات مختلفة
- 💰 **إدارة الإيرادات والمصروفات** بدعم 3 عملات
- 🏬 **إدارة المخزون** مع تنبيهات انخفاض الكميات
- 📱 **تصميم متجاوب** لجميع الأجهزة
- 🌙 **وضع مظلم** مع دعم كامل
- 🔔 **نظام تنبيهات** ذكي
- 📄 **تقارير مفصلة** مع إمكانية التصدير

## 🛠️ التقنيات المستخدمة

### Frontend
- **React 18** مع TypeScript
- **TailwindCSS** للتصميم
- **shadcn/ui** لمكونات الواجهة
- **Framer Motion** للحركات والانتقالات
- **React Query** لإدارة البيانات
- **Recharts** للرسوم البيانية

### Backend
- **Node.js** مع Express
- **MongoDB** مع Mongoose
- **bcrypt** لتشفير كلمات المرور
- **express-session** لإدارة الجلسات
- **Zod** للتحقق من البيانات

## 🚀 التثبيت والتشغيل

### المتطلبات
- Node.js 18 أو أحدث
- npm أو yarn
- MongoDB Atlas (للإنتاج)

### التثبيت
```bash
# استنساخ المشروع
git clone <repository-url>
cd WebTranslator

# تثبيت التبعيات
npm install

# إعداد متغيرات البيئة
cp .env.example .env
# تعديل ملف .env بإعدادات قاعدة البيانات
```

### التشغيل المحلي
```bash
# تشغيل في وضع التطوير
npm run dev

# فتح المتصفح على
http://localhost:3000
```

### بيانات تسجيل الدخول الافتراضية
- **Admin**: `admin` / `Admin123!`
- **Owner**: `owner` / `Owner123!`
- **Manager**: `manager` / `Manager123!`
- **Accountant**: `accountant` / `Accountant123!`
- **Warehouse**: `warehouse` / `Warehouse123!`
- **Viewer**: `viewer` / `Viewer123!`

## 🌐 النشر على Netlify

### 1. إعداد المشروع
```bash
# بناء المشروع
npm run build
```

### 2. رفع المشروع
1. اذهب إلى [Netlify](https://netlify.com)
2. انقر على "New site from Git"
3. اختر مستودع GitHub الخاص بك
4. اضبط إعدادات البناء:
   - **Build command**: `npm run build`
   - **Publish directory**: `dist`
   - **Node version**: `18`

### 3. إعداد متغيرات البيئة
في إعدادات Netlify، أضف المتغيرات التالية:
```
NODE_ENV=production
MONGODB_URI=your-mongodb-connection-string
SESSION_SECRET=your-session-secret
```

### 4. إعداد Backend
للباك إند، يمكنك استخدام:
- **Netlify Functions** (للعمليات البسيطة)
- **Railway** أو **Render** (للعمليات المعقدة)
- **Heroku** أو **DigitalOcean**

### 5. تحديث API URL
في `client/src/lib/constants.tsx`:
```typescript
export const API_BASE_URL = process.env.NODE_ENV === 'production' 
  ? 'https://your-backend-url.com/api' 
  : 'http://localhost:3000/api';
```

## 📁 هيكل المشروع

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

## 🔐 نظام الصلاحيات

| الدور | الإضافة | التعديل | الحذف | العرض |
|-------|---------|---------|-------|-------|
| **Super Admin** | ✅ | ✅ | ✅ | ✅ |
| **Owner** | ✅ | ✅ | ✅ | ✅ |
| **Manager** | ✅ | ✅ | ❌ | ✅ |
| **Accountant** | ✅ | ✅ | ❌ | ✅ |
| **Warehouse** | ✅ | ✅ | ❌ | ✅ |
| **Viewer** | ❌ | ❌ | ❌ | ✅ |

## 💰 العملات المدعومة

- 🇸🇾 **الليرة السورية** (SYP)
- 🇹🇷 **الليرة التركية** (TRY)
- 🇺🇸 **الدولار الأمريكي** (USD)

## 🎨 ميزات الواجهة

- **خلفية متحركة** مع جزيئات عائمة
- **حركات سلسة** باستخدام Framer Motion
- **تصميم زجاجي** مع شفافية وظلال
- **تحقق من قوة كلمة المرور** مع نصائح
- **رسائل خطأ متحركة** تظهر وتختفي بسلاسة
- **تخطيط متجاوب** لجميع الأجهزة

## 🔮 الميزات المستقبلية

- 💳 دعم الدفع الإلكتروني
- 📱 تطبيق موبايل
- 🔄 دعم العمل Offline
- 📊 تقارير مخصصة
- 🎨 تخصيص كامل للشعار والألوان
- 🔌 واجهة API مفتوحة

## 🤝 المساهمة

نرحب بمساهماتكم! يرجى:
1. Fork المشروع
2. إنشاء branch جديد للميزة
3. Commit التغييرات
4. Push إلى Branch
5. إنشاء Pull Request

## 📄 الترخيص

هذا المشروع مرخص تحت رخصة MIT.

## 📞 الدعم

للدعم الفني أو الاستفسارات:
- 📧 البريد الإلكتروني: support@ibrahim-accounting.com
- 💬 Discord: [رابط السيرفر]
- 📱 WhatsApp: [رقم الدعم]

---

**نظام إبراهيم للمحاسبة** - الحل الأمثل لإدارة أعمالك التجارية! 🚀
