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


src/
├── components/
│   ├── Dashboard/
│   │   ├── DashboardGroup.js
│   │   ├── DashboardSidebar.js
│   │   ├── DashboardPanel.js
│   │   ├── DashboardNavbar.js
│   │   └── DashboardToolbar.js
│   ├── Forms/
│   │   ├── MaintenanceRequestForm.js
│   │   ├── LoginForm.js
│   │   └── ConfirmForm.js
│   ├── Tables/
│   │   ├── RequestsTable.js
│   │   ├── StoresTable.js
│   │   └── RatingsTable.js
│   ├── Modals/
│   │   ├── RequestDetailsModal.js
│   │   └── StoreDetailsModal.js
│   └── Notifications/
│       ├── NotificationList.js
│       └── NotificationItem.js
├── pages/
│   ├── Dashboard/
│   │   └── Dashboard.js
│   ├── MaintenanceRequests/
│   │   ├── MaintenanceRequests.js
│   │   ├── RequestDetails.js
│   │   └── NewRequest.js
│   ├── Stores/
│   │   ├── Stores.js
│   │   └── StoreDetails.js
│   ├── Auth/
│   │   ├── Login.js
│   │   └── Confirm.js
│   ├── Profile/
│   │   └── Profile.js
│   └── Ratings/
│       └── Ratings.js
├── services/
│   ├── supabaseClient.js
│   ├── authService.js
│   ├── requestService.js
│   ├── storeService.js
│   └── notificationService.js
├── context/
│   ├── AuthContext.js
│   ├── RequestContext.js
│   ├── StoreContext.js
│   └── NotificationContext.js
├── hooks/
│   ├── useAuth.js
│   ├── useRequests.js
│   ├── useStores.js
│   └── useNotifications.js
└── utils/
    ├── formatDate.js
    └── validateForm.js

## التثبيت
1. قم باستنساخ المستودع:
   ```bash
   git clone https://github.com/username/repository-name.git
