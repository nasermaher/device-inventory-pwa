# حصر الأجهزة | Device Inventory

تطبيق ويب تقدمي (PWA) من ملف واحد لحصر أجهزة الكمبيوتر والطابعات وربطها بالموظفين والإدارات — يعمل بالكامل بدون إنترنت وبدون خادم.

**🔗 التجربة المباشرة:** https://nasermaher.github.io/device-inventory-pwa/

[العربية](#العربية) | [English](#english)

---

## العربية

### الهدف من البرنامج

أداة عملية لأقسام تقنية المعلومات لحصر وتتبع أجهزة الكمبيوتر والطابعات وطابعات الشبكة وتليفونات IP وغيرها، وتوثيق:

- أي **إدارة/قسم** ينتمي إليه كل **موظف**.
- أي **جهاز** (نوع، موديل، رقم تسلسلي، IP) مخصص لكل موظف — مع إمكانية أن يملك الموظف الواحد أكثر من جهاز.
- الأجهزة **غير المخصصة** بعد والمحفوظة في مكان/إدارة معينة لحين الحاجة إليها.
- **الخدمات** التي يخدمها كل جهاز (بريد إلكتروني، طباعة مركزية، ...).

### الاستخدامات الممكنة

- جرد سنوي/دوري لأصول تقنية المعلومات داخل مؤسسة أو مصنع أو مستشفى.
- تتبع نقل الأجهزة بين الموظفين عند تغيير الموقع الوظيفي أو ترك العمل.
- تجهيز تقارير سريعة لتوزيع الأجهزة على الإدارات عند التخطيط للميزانية أو الصيانة.
- أرشيف قابل للنقل (ملف JSON واحد) بين فروع أو أجهزة مختلفة.

### المزايا الرئيسية

- **ملف واحد فقط** — بدون تثبيت، بدون خادم، بدون اتصال إنترنت بعد أول فتح.
- **ثنائي اللغة** عربي/إنجليزي مع دعم كامل لاتجاه الكتابة (RTL/LTR) قابل للتبديل فوريًا.
- قوائم قابلة للتخصيص: **الإدارات، الموظفون، أنواع الأجهزة، الخدمات**.
- استيراد البيانات من **CSV أو Excel (XLSX)** مع معاينة قبل التأكيد وتجاهل السجلات المكررة تلقائيًا.
- بحث فوري لاختيار الموظف/نوع الجهاز عند التسجيل، بدل التمرير في قوائم طويلة.
- 3 رسوم بيانية: توزيع الأجهزة حسب النوع، حسب الإدارة، ونسبة المخصص مقابل غير المخصص.
- نسخ احتياطي واستعادة كاملة للبيانات بصيغة JSON للنقل بين الأجهزة.
- كل البيانات تُخزَّن **محليًا فقط** داخل متصفحك — لا تُرسل لأي خادم.

### حل مشكلة نقل/تحرير الأجهزة

عند تغيّر مكان الموظف أو انتقال جهاز من شخص لآخر، يوفر التطبيق 3 إجراءات سريعة على كل سجل جهاز مباشرة (بدون فتح نموذج التعديل الكامل):

| الإجراء | متى يُستخدم |
|---|---|
| **نقل لموظف آخر** | الجهاز ينتقل من موظف إلى آخر مباشرة (نفس الجهاز، مالك جديد) |
| **إرجاع للمخزن** | الموظف غادر العمل أو انتقل ولن يحتفظ بالجهاز الآن — يعود الجهاز تلقائيًا لإدارة الموظف السابقة كـ"غير مخصص" |
| **تخصيص لموظف** | جهاز كان في المخزن ويُسلَّم لموظف جديد |

بالإضافة إلى ذلك:

- **قسم الجهاز يتبع قسم الموظف تلقائيًا** — إن نقلت موظفًا إلى إدارة أخرى من شاشة "الموظفون"، فكل أجهزته المخصصة تنعكس فورًا في القسم الجديد بدون أي خطوة إضافية.
- **سجل تغييرات كامل** لكل جهاز (من نموذج التعديل): متى أُنشئ، ولمن نُقل، ومتى أُرجع للمخزن — سجل تدقيق (Audit Trail) يوثّق تاريخ الجهاز بالكامل.
- عند محاولة حذف موظف يملك أجهزة مخصصة، يعرض التطبيق خيار **"إرجاع الأجهزة ثم الحذف"** بدل رفض الحذف فقط، فتُحفظ الأجهزة تلقائيًا كـ"غير مخصصة" بإدارته الأخيرة قبل حذفه.

### طريقة الاستخدام

1. افتح الرابط أعلاه على الموبايل، ثم من متصفح Chrome/Safari اختر **"إضافة إلى الشاشة الرئيسية"** لتثبيته كتطبيق مستقل.
2. من شاشة **"القوائم"**: أضف الإدارات وأنواع الأجهزة والخدمات يدويًا، أو استورد ملف CSV/Excel جاهز.
3. من شاشة **"تعيين الأجهزة"**: سجّل كل جهاز واربطه بموظف أو بمكان تخزين.
4. تابع التوزيع من شاشة **"الإحصائيات"**.
5. من **"الإعدادات"**: بدّل اللغة، أو صدّر نسخة احتياطية دورية لحفظ بياناتك.

### ملاحظة خصوصية

هذا مستودع عام على GitHub Pages لتشغيل الصفحة فقط — لا توجد قاعدة بيانات على الخادم، وكل بيانات الإدارات/الموظفين/الأجهزة التي تُدخلها تبقى محفوظة داخل متصفح جهازك فقط (localStorage) ولا يراها أحد غيرك.

### الفكرة والتنفيذ

**محمود عبدالرحمن الأنصاري**

---

## English

### Purpose

A practical tool for IT departments to inventory and track computers, printers, network printers, IP phones and similar equipment, documenting:

- Which **department** each **employee** belongs to.
- Which **device** (type, model, serial number, IP) is assigned to each employee — an employee can hold more than one device.
- Devices that are **not yet assigned** and are being kept in a specific department/location until needed.
- The **services** each device supports (email, central printing, etc.).

### Possible Uses

- Annual/periodic IT asset audits for an organization, factory, or hospital.
- Tracking device handovers between employees when roles or locations change.
- Quick reports on device distribution across departments for budgeting or maintenance planning.
- A portable archive (single JSON file) to move data between branches or devices.

### Key Features

- **Single file** — no install, no server, no internet needed after the first load.
- **Bilingual** Arabic/English with full RTL/LTR support, switchable instantly.
- Manageable catalogs: **Departments, Employees, Device Types, Services**.
- Import data from **CSV or Excel (XLSX)** with a preview step and automatic duplicate skipping.
- Instant search when picking an employee/device type, instead of scrolling long lists.
- 3 charts: devices by type, devices by department, and assigned vs. unassigned ratio.
- Full JSON backup/restore to move data between devices.
- All data is stored **locally in your browser only** — nothing is sent to any server.

### Solving the Device Handover Problem

When an employee's location changes, or a device moves from one person to another, the app offers 3 one-tap actions directly on each device record (no need to open the full edit form):

| Action | When to use |
|---|---|
| **Reassign** | The device moves directly from one employee to another (same device, new owner) |
| **Return to storage** | The employee left or transferred and won't keep the device now — it automatically returns to their last department as "unassigned" |
| **Assign to employee** | A stored device is being handed to a new employee |

In addition:

- **A device's department follows its employee automatically** — move an employee to another department from the Employees screen, and all their assigned devices reflect the new department instantly, with no extra step.
- **A full change history** per device (in the edit form): when it was created, who it was transferred to, and when it was returned to storage — a complete audit trail.
- Deleting an employee who still holds devices offers a **"Return devices & delete"** option instead of simply blocking the action, automatically marking their devices as unassigned under their last department first.

### How to Use

1. Open the link above on your phone, then from Chrome/Safari choose **"Add to Home Screen"** to install it as a standalone app.
2. On the **Lists** screen: add departments, device types, and services manually, or import a ready CSV/Excel file.
3. On the **Assign** screen: record each device and link it to an employee or a storage location.
4. Track distribution on the **Stats** screen.
5. From **Settings**: switch language, or export a periodic backup to keep your data safe.

### Privacy Note

This is a public GitHub repository used only to host the static page via GitHub Pages — there is no server-side database. All department/employee/device data you enter stays inside your own browser's local storage and is never seen by anyone else.

### Idea & Implementation

**Mahmoud Abdelrahman Al-Ansary**
