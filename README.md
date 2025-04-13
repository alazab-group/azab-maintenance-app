
# 🛠 Azab Maintenance App

**React Native + Supabase**  
التطبيق الرسمي لإدارة عمليات الصيانة والفروع الخاصة بشركة العزب للخدمات المعمارية.  
نظام ذكي مؤمن، مخصص لإدارة:

- ✅ طلبات الصيانة
- ✅ الداشبورد المالية
- ✅ الداشبورد التشغيلية
- ✅ معرض الصور
- ✅ الأرشيف
- ✅ تجربة العميل
- ✅ تحليلات الأداء

---

## 📁 هيكل المجلدات

```
src/
├── assets/                  # الصور والأيقونات
├── components/             # مكونات قابلة لإعادة الاستخدام
├── context/                # إدارة الجلسة (Auth)
├── hooks/                  # هوكات مخصصة
├── navigation/             # التنقل بين الشاشات
├── guards/                 # حراسة الدور
├── config/                 # إعدادات عامة
├── pages/
│   ├── Auth/               # تسجيل الدخول والتحقق
│   ├── MaintenanceRequests/# الطلبات والمرفقات
│   ├── FinanceDashboard/  # التقارير والفواتير
│   ├── OperationsDashboard/# حالة النظام الحية
│   ├── Gallery/           # صور الفروع والأعمال
│   ├── Archive/           # أرشيف الطلبات
│   ├── General/           # الملف الشخصي والتواصل
│   ├── Admin/             # إشراف المدير
│   ├── Analytics/         # مؤشرات وتحليلات
│   ├── CustomerExperience/# تقييم ومتابعة العميل
├── services/               # الاتصال بـ Supabase
├── utils/                  # أدوات مساعدة
├── i18n/                   # دعم تعدد اللغات
```

---

## 🔐 إدارة المستخدمين

| الدور         | الصلاحيات                                 |
|---------------|--------------------------------------------|
| Admin         | إدارة كل شيء - تحليلات - أرشيف - إشراف     |
| Technician    | عرض المهام - رفع تقارير - تحديث الحالة     |
| Customer      | إنشاء طلبات - متابعة - تقييم الخدمة        |

---

## 📦 أدوات وتقنيات مستخدمة

- **React Native (Expo)**
- **Supabase (Auth, Database, Storage)**
- **EmailJS** لإرسال إشعارات تلقائية
- **Unocss + i18next** لدعم المظهر وتعدد اللغات
- **Toast + Guards** لتجربة استخدام احترافية
- **Secure Storage** لحماية الجلسة

---

## 🧠 التحليلات المدمجة

- عدد الطلبات النشطة
- تحليل الفروع
- أداء الفنيين
- اتجاهات الاستخدام
- الطلب حسب نوع الخدمة

---

## 🧪 التجربة المتكاملة

- كل قسم مرتبط بقاعدة البيانات مباشرة
- تدفقات العمل متكاملة للعميل والفني والمدير
- تم التحقق من صلاحيات الوصول لكل دور
- واجهات مصممة بالاعتماد على السيناريوهات الحقيقية

---

## 📌 Supabase إعدادات

```env
EXPO_PUBLIC_SUPABASE_URL=https://your-project.supabase.co
EXPO_PUBLIC_SUPABASE_ANON_KEY=eyJh...
```

---

## 🧩 الخدمات المخصصة

```js
services/
├── requestService.js         // إدارة الطلبات
├── workflowService.js        // مراحل التنفيذ
├── emailService.js           // إرسال بريد تلقائي
├── invoiceService.js         // تقارير وفواتير
├── profileService.js         // ملف المستخدم
├── notificationService.js    // الإشعارات
├── galleryService.js         // معرض الصور
├── authService.js            // تسجيل الدخول والتوثيق
```

---

## 🌍 دعم اللغات

- 🇸🇦 `ar.json`
- 🇺🇸 `en.json`
- يتم التبديل باستخدام `i18n.js` + `LanguageToggle.js`

---

## 🧠 المطور المسؤول

> تم بناء المشروع من قبل سعيد - تحت إشراف مباشر من المهندس محمد العزب.  
> جميع التفاصيل مستوحاة من سيناريوهات حقيقية داخل شركة العزب لإدارة الصيانة المعمارية.

---

## 🧭 الخطوة التالية

- ✅ نشر نسخة `.zip`
- ✅ إعداد AAB لـ Google Play
- ✅ أو البدء في تجهيز نسخة عرض Demo جاهزة للتشغيل

---

## © 2025 Al-Azab Architectural Services

تم تنفيذ هذا المشروع بأعلى دقة ممكنة لخدمة العملاء والمهندسين الإداريين عبر منصة احترافية موحدة.
