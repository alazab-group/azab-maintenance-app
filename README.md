# azab-maintenance-app

# مشروع تطبيق الصيانة المعمارية

## مقدمة
هذا المشروع هو تطبيق صيانة معمارية يستخدم React و Supabase لإدارة طلبات الصيانة للمحلات التجارية. يهدف التطبيق إلى توفير واجهة مستخدم سهلة الاستخدام وفعالة لإدارة الطلبات، المحلات التجارية، والتقييمات.

## الميزات الرئيسية
- **إدارة الطلبات**: إنشاء، تعديل، وحذف طلبات الصيانة.
- **إدارة المحلات التجارية**: عرض وتحديث معلومات المحلات التجارية.
- **التقييمات**: تقييم الطلبات وإضافة تعليقات.
- **المصادقة**: تسجيل الدخول باستخدام GitHub.
- **الإشعارات**: عرض الإشعارات المتعلقة بالطلبات والمستخدمين.

## هيكل المشروع


<div style="background-color: black; color: white; padding: 20px;">
  <h1>مرحبا بك في المشروع!</h1>
  <p>هذا هو ملف README بأسلوب خلفية سوداء ونص أبيض.</p>
</div>

// 🔧 React Native + Supabase — Maintenance App Architecture (Final Blueprint + Enhancements)

// ✅ الهيكل الكامل للمجلدات والملفات داخل src/

src/
├── assets/                      // الصور، الشعارات، الأيقونات
├── components/                 // مكونات واجهة قابلة لإعادة الاستخدام (مثل Card، Modal، Toast)
├── context/                    // إدارة الجلسة والسياق العام للتطبيق (مثل AuthContext)
├── hooks/                      // هوكات مخصصة مثل useAuth، useRole
├── navigation/                 // إدارة التنقل بين الصفحات
│   ├── TabsNavigator.js        // تبويبات Bottom Navigation حسب الدور
│   ├── Drawer.js              // Drawer Navigation للمديرين فقط
├── guards/                     // حراسة الدخول حسب الدور
│   ├── withAdminGuard.js       // حراسة صفحات المدير
│   ├── withTechnicianGuard.js  // حراسة الفني
│   ├── withCustomerGuard.js    // حراسة العميل
├── config/                     // إعدادات وتكوينات عامة
│   ├── appConfig.js            // اسم التطبيق، اللوجو، معلومات عامة
│   ├── constants.js            // تعريفات عامة (status, priority, serviceType)
│   ├── roles.js                // تعريف الأدوار داخل النظام
├── pages/
│   ├── Auth/                   // 🟦 قسم المصادقة 🔐
│   │   ├── Login.js
│   │   ├── Confirm.js
│   │   ├── AuthContext.js
│   │   ├── useAuth.js
│   │   ├── authService.js
│   │   ├── ResendOtp.js
│   │   ├── SessionGuard.js
│   │   ├── Logout.js
│   │   ├── Permissions.js      // تحديد الصلاحيات بناءً على الدور
│   ├── MaintenanceRequests/    // 🟦 طلبات الصيانة 🛠
│   │   ├── NewRequest.js
│   │   ├── MaintenanceRequests.js
│   │   ├── RequestDetails.js
│   │   ├── RequestReport.js
│   │   ├── DeliveryConfirmation.js
│   │   ├── Attachments.js
│   │   ├── VoiceNoteUpload.js
│   │   ├── RequestFilter.js
│   │   ├── RequestETA.js
│   │   ├── LiveStatus.js
│   ├── FinanceDashboard/       // 🟦 داشبورد مالية 📊
│   │   ├── InvoicesSummary.js
│   │   ├── InvoicesTable.js
│   │   ├── CostComparisonChart.js
│   │   ├── BranchCostAnalysis.js
│   │   ├── FinancialReport.js
│   │   ├── MonthlyBreakdown.js
│   ├── OperationsDashboard/    // 🟦 داشبورد تشغيلية ⚙️
│   │   ├── ActiveRequests.js
│   │   ├── TechnicianPerformance.js
│   │   ├── DailyTasks.js
│   │   ├── LiveStatusOverview.js
│   │   ├── StatusCards.js
│   │   ├── TechnicianRanking.js
│   │   ├── OperationStats.js
│   │   ├── TechnicianAlert.js
│   │   ├── BranchMap.js
│   ├── Gallery/                // 🟦 معرض الصور 🖼
│   │   ├── GalleryOverview.js
│   │   ├── ImageViewer.js
│   │   ├── GalleryUpload.js
│   │   ├── BeforeAfterView.js
│   │   ├── DownloadImage.js
│   │   ├── GallerySearch.js
│   │   ├── ShareImage.js
│   ├── Archive/                // 🟦 الأرشيف 🗂
│   │   ├── ArchivedRequests.js
│   │   ├── SearchFilters.js
│   │   ├── RestoreRequest.js
│   │   ├── ArchivedDetails.js
│   │   ├── ArchivedFilesViewer.js
│   │   ├── ArchiveYearTabs.js
│   │   ├── ArchiveReadonlyGuard.js
│   ├── General/                // 🟦 صفحات عامة 🌐
│   │   ├── Profile.js
│   │   ├── ContactUs.js
│   │   ├── About.js
│   │   ├── Notifications.js
│   │   ├── LanguageToggle.js
│   │   ├── AppearanceSettings.js
│   ├── Admin/                  // 🟦 أدوات المدير (إشراف ومراقبة)
│   │   ├── LogsDashboard.js
│   │   ├── ErrorMonitor.js
│   ├── Analytics/              // 🆕 قسم التحليلات والرؤى 🧠
│   │   ├── InsightDashboard.js     // واجهة تعرض أهم المؤشرات
│   │   ├── UsageTrends.js          // استخدام التطبيق عبر الزمن
│   │   ├── BranchPerformance.js    // أداء الفروع
│   │   ├── TechnicianInsights.js   // أداء الفنيين وتحليل الإنتاجية
│   │   ├── ServiceDemand.js        // الطلب حسب نوع الخدمة
│   ├── CustomerExperience/     // 🆕 تجربة العميل 💬
│   │   ├── CustomerRatings.js      // تقييمات العملاء
│   │   ├── FeedbackForm.js         // نموذج رأي بعد الخدمة
│   │   ├── SatisfactionStats.js    // تحليل الرضا العام
│   │   ├── AutoFollowUps.js        // متابعة تلقائية بعد التنفيذ
│   │   ├── ServiceHistory.js       // تاريخ الطلبات للعميل
├── services/                  // 🔁 خدمات التواصل مع قاعدة البيانات
│   ├── requestService.js
│   ├── workflowService.js
│   ├── emailService.js
│   ├── invoiceService.js
│   ├── profileService.js
│   ├── notificationService.js
│   ├── galleryService.js
│   ├── authService.js
├── utils/                    // 🧩 أدوات عامة لتحسين الأداء
│   ├── formatDate.js
│   ├── toast.js
│   ├── errorHandler.js
│   ├── validators.js
│   ├── supabaseErrorMapper.js
│   ├── mapPriorityColor.js
│   ├── durationCalculator.js
├── i18n/                     // 🌍 دعم تعدد اللغات 
│   ├── ar.json
│   ├── en.json
│   ├── i18n.js


// ✅ بهذا الشكل: المشروع أصبح معماري احترافي، مؤمن، ذكي، قابل للتوسع العملاق فورًا 🚀



## التثبيت
1. قم باستنساخ المستودع:
   ```bash
   git clone https://github.com/username/repository-name.git
