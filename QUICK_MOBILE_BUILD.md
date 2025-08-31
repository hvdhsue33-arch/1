# دليل سريع لبناء APK للجوال

## 🚀 البناء السريع (أوتوماتيكي)

### الطريقة الأولى: البناء التلقائي
```bash
# تشغيل السكريبت التلقائي لبناء APK
npm run mobile:build-auto
```

### الطريقة الثانية: البناء اليدوي
```bash
# 1. تثبيت التبعيات
npm install

# 2. إضافة منصة Android
npm run mobile:add

# 3. بناء التطبيق
npm run mobile:build

# 4. بناء APK
npm run mobile:build-apk
```

## 📱 تثبيت التطبيق على الهاتف

### الخطوات:
1. **انسخ ملف APK** من المسار:
   ```
   android/app/build/outputs/apk/debug/app-debug.apk
   ```

2. **فعّل "مصادر غير معروفة"** في إعدادات الأمان على هاتفك

3. **قم بتثبيت التطبيق** من ملف APK

## 🔧 المتطلبات الأساسية

### يجب تثبيت:
- ✅ Node.js (v16 أو أحدث)
- ✅ npm (v8 أو أحدث)
- ✅ Android Studio
- ✅ Android SDK
- ✅ Java JDK (v8 أو أحدث)

### التحقق من التثبيت:
```bash
node --version
npm --version
java --version
```

## 🛠️ حل المشاكل الشائعة

### مشكلة: "command not found: cap"
```bash
npm install -g @capacitor/cli
```

### مشكلة: "Android SDK not found"
- تأكد من تثبيت Android Studio
- أضف Android SDK إلى متغيرات البيئة PATH

### مشكلة: "Gradle build failed"
```bash
cd android
./gradlew clean
./gradlew assembleDebug
```

### مشكلة: "Permission denied"
```bash
chmod +x android/gradlew
```

## 📋 أوامر مفيدة

```bash
# فتح المشروع في Android Studio
npm run mobile:open

# تشغيل التطبيق على الجهاز المتصل
npm run mobile:run

# مزامنة التغييرات
npx cap sync android

# تحديث التطبيق
npm run build:client && npx cap sync android
```

## 🎯 نصائح مهمة

1. **تأكد من توصيل الهاتف** عبر USB مع تفعيل وضع المطور
2. **استخدم كابل USB جيد** لتجنب مشاكل الاتصال
3. **تأكد من وجود مساحة كافية** على الهاتف (100MB على الأقل)
4. **اختبر التطبيق** على أجهزة مختلفة للتأكد من التوافق

## 📞 الدعم

إذا واجهت أي مشاكل:
1. تحقق من رسائل الخطأ في Terminal
2. تأكد من تثبيت جميع المتطلبات
3. جرب إعادة تشغيل Android Studio
4. تحقق من إعدادات الأمان على الهاتف

## 🎉 النجاح!

بعد اكتمال العملية، ستجد ملف APK في:
```
android/app/build/outputs/apk/debug/app-debug.apk
```

يمكنك الآن تثبيت التطبيق على هاتفك واستخدامه!
