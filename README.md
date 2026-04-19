
readme_content = """<div align="center">

# 🔐 نموذج تسجيل الدخول - Login Form

[![Flutter Version](https://img.shields.io/badge/Flutter-3.0+-blue.svg)](https://flutter.dev)
[![Dart Version](https://img.shields.io/badge/Dart-3.0+-blue.svg)](https://dart.dev)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/Platform-Android%20%7C%20iOS%20%7C%20Web%20%7C%20Desktop-lightgrey.svg)](https://flutter.dev)

<p align="center">
  <img src="https://img.shields.io/badge/اللغة-العربية-red" alt="Arabic" />
  <img src="https://img.shields.io/badge/Language-Arabic-red" alt="Arabic" />
</p>

**تطبيق Flutter احترافي لنموذج تسجيل الدخول مع دعم كامل للغة العربية والاتجاه من اليمين لليسار**

[مشاهدة العرض التوضيحي](#-لقطات-الشاشة) • [التثبيت](#-التثبيت) • [الاستخدام](#-الاستخدام) • [المساهمة](#-المساهمة)

</div>

---

## 📋 جدول المحتويات

- [المميزات](#-المميزات)
- [لقطات الشاشة](#-لقطات-الشاشة)
- [التثبيت](#-التثبيت)
- [الهيكل التنظيمي](#-الهيكل-التنظيمي)
- [الاستخدام](#-الاستخدام)
- [التقنيات المستخدمة](#-التقنيات-المستخدمة)
- [المساهمة](#-المساهمة)
- [الترخيص](#-الترخيص)

---

## ✨ المميزات

### 🎯 الوظائف الأساسية
- ✅ **التحقق من صحة البيانات** - Validation متكامل للبريد الإلكتروني وكلمة المرور
- ✅ **إظهار/إخفاء كلمة المرور** - مع دعم الضغط المطول للعرض المؤقت
- ✅ **مؤشر التحميل** - أثناء عملية تسجيل الدخول
- ✅ **رسائل التنبيه** - SnackBar للنجاح والأخطاء

### 🎨 التصميم
- 🌈 **تصميم عصري** - خلفية متدرجة وبطاقة منسقة
- 📱 **دعم كامل للعربية** - الاتجاه من اليمين لليسار (RTL)
- 🎭 **رسوم متحركة سلسة** - تجربة مستخدم تفاعلية
- 📐 **تصميم متجاوب** - يعمل على جميع أحجام الشاشات

### 🔧 التقنيات
- ⚡ **Flutter 3.0+** - أحدث إصدار
- 🎯 **Material Design 3** - التصميم الحديث
- 🌍 **دعم اللغات** - flutter_localizations
- 💾 **إدارة الحالة** - StatefulWidget مع Best Practices

---

## 📸 لقطات الشاشة

<div align="center">

| شاشة تسجيل الدخول | التحقق من الأخطاء | كلمة المرور مرئية |
|:---:|:---:|:---:|
| ![Login](screenshots/login.png) | ![Validation](screenshots/validation.png) | ![Password](screenshots/password.png) |

</div>

---

## 🚀 التثبيت

### المتطلبات المسبقة

- [Flutter SDK](https://flutter.dev/docs/get-started/install) (الإصدار 3.0 أو أحدث)
- [Dart SDK](https://dart.dev/get-dart) (الإصدار 3.0 أو أحدث)
- محرر أكواد (VS Code أو Android Studio)

### خطوات التثبيت

#### 1. استنساخ المستودع
```bash
git clone https://github.com/username/login-form-flutter.git
cd login-form-flutter
```

#### 2. تثبيت الاعتماديات
```bash
flutter pub get
```

#### 3. تشغيل التطبيق
```bash
flutter run
```

### بناء الإصدار للإنتاج

```bash
# Android
flutter build apk --release
flutter build appbundle --release

# iOS
flutter build ios --release

# Web
flutter build web --release
```

---

## 📁 الهيكل التنظيمي

```
login_form/
├── android/                 # ملفات Android
├── ios/                     # ملفات iOS
├── lib/                     # الكود المصدري الرئيسي
│   ├── main.dart           # نقطة الدخول
│   └── login_screen.dart   # شاشة تسجيل الدخول
├── test/                    # اختبارات الوحدة
├── screenshots/             # لقطات الشاشة
├── pubspec.yaml            # إعدادات المشروع
└── README.md               # هذا الملف
```

---

## 💡 الاستخدام

### مثال أساسي

```dart
import 'package:flutter/material.dart';
import 'login_screen.dart';

void main() {
  runApp(const MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({super.key});

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'تسجيل الدخول',
      debugShowCheckedModeBanner: false,
      home: const LoginScreen(),
    );
  }
}
```

### التحقق المخصص

```dart
// تخصيص رسائل الخطأ
String? _validateEmail(String? value) {
  if (value == null || value.isEmpty) {
    return 'الرجاء إدخال البريد الإلكتروني';
  }
  if (!RegExp(r'^[\w-\.]+@([\w-]+\.)+[\w-]{2,4}$').hasMatch(value)) {
    return 'البريد الإلكتروني غير صالح';
  }
  return null;
}
```

---

## 🛠️ التقنيات المستخدمة

| التقنية | الاستخدام |
|---------|-----------|
| [Flutter](https://flutter.dev) | إطار العمل الرئيسي |
| [Dart](https://dart.dev) | لغة البرمجة |
| [Material Design 3](https://m3.material.io/) | نظام التصميم |
| [flutter_localizations](https://api.flutter.dev/flutter/flutter_localizations/flutter_localizations-library.html) | دعم اللغات |

---

## 🤝 المساهمة

نرحب بمساهماتكم! للمساهمة في المشروع:

1. **انشئ Fork** للمستودع
2. **أنشئ فرعاً جديداً** (`git checkout -b feature/amazing-feature`)
3. **أجرِ تغييراتك** (`git commit -m 'Add amazing feature'`)
4. **ادفع الفرع** (`git push origin feature/amazing-feature`)
5. **افتح Pull Request**

### قواعد المساهمة

- 📌 اتبع [دليل أسلوب Flutter](https://github.com/flutter/flutter/wiki/Style-guide-for-Flutter-repo)
- 📝 اكتب وثائق واضحة للتغييرات
- 🧪 أضف اختبارات للميزات الجديدة
- 🎯 تأكد من عدم وجود أخطاء (`flutter analyze`)

---

## 📞 التواصل

<div align="center">

[![Twitter](https://img.shields.io/badge/Twitter-@username-1DA1F2?style=for-the-badge&logo=twitter)](https://facebook.com/odaifaez)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-username-0077B5?style=for-the-badge&logo=linkedin)](https://linkedin.com/in/odaifaez)
[![Email](https://img.shields.io/badge/Email-email@example.com-D14836?style=for-the-badge&logo=gmail)](mailto:dymhsn712@gmail.com)

</div>

---

## 📝 الترخيص

هذا المشروع مرخص بموجب [MIT License](LICENSE) - انظر ملف LICENSE للتفاصيل.

```
MIT License

Copyright (c) 2024 [odai faez]

يُمنح إذن، مجاناً، لأي شخص يحصل على نسخة من هذا البرنامج
... (نص الترخيص الكامل)
```

---

## 🙏 الشكر والتقدير

- [Flutter Team](https://flutter.dev) - على الإطار الرائع
- [المتبرعين](https://github.com/username/login-form-flutter/graphs/contributors) - على جهودهم القيمة

---

<div align="center">

### ⭐ لا تنسَ إعطاء النجمة إذا أعجبك المشروع! ⭐

**[⬆ العودة إلى الأعلى](#-نموذج-تسجيل-الدخول---login-form)**

</div>

---

<p align="center">
  صنع بـ ❤️ في المملكة العربية السعودية
</p>
"""

# حفظ الملف
with open('/mnt/agents/output/README.md', 'w', encoding='utf-8') as f:
    f.write(readme_content)

print("✅ تم إنشاء ملف README.md الاحترافي بنجاح!")
print("\n📄 الملف يحتوي على:")
print("- شعار وشارات (Badges)")
print("- جدول محتويات")
print("- لقطات شاشة")
print("- تعليمات التثبيت")
print("- هيكل المشروع")
print("- أمثلة على الاستخدام")
print("- معلومات المساهمة")
print("- الترخيص")
