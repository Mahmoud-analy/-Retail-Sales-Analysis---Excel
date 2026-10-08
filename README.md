# 📊 Retail Sales Analysis - Excel

تحليل بيانات مبيعات تجزئة باستخدام **Microsoft Excel** فقط، بدءًا من ملف CSV خام (كل القيم في عمود واحد) وصولًا إلى PivotTables وDashboard.

## 🗂️ عن المشروع

| البند | التفاصيل |
|---|---|
| **المصدر** | [Sales Dashboard Dataset - Kaggle](https://www.kaggle.com/datasets/dhruvmaheshwari003/sales-dashboard-dataset-excel-visualization) |
| **حجم البيانات بعد التنظيف** | 9,987 عملية بيع |
| **الملف** | [`Raw_Sales_Dataset.xlsx`](./Raw_Sales_Dataset.xlsx) |

**أعمدة البيانات:** Order Date · Customer Name · State · Category · Sub-Category · Product Name · Sales · Quantity · Profit

## ✅ الخطوات

### 1. تنظيف البيانات
- فصل الأعمدة (`Text to Columns`)
- تحويل `Order Date` من نص إلى تاريخ حقيقي (DMY)
- حذف الصفوف المكررة (`Remove Duplicates`): صفين
- فحص القيم الفاضية بـ `COUNTBLANK` وحذف 5 صفوف ناقصة بالكامل (Sales وQuantity وProfit فاضيين)
- تحويل البيانات إلى Excel Table

### 2. الدوال التحليلية
`SUMIFS` · `COUNTIFS` · `AVERAGEIFS`، مع التحقق من أن مجموع الفئات يساوي الإجمالي الكلي (2,294,992.78).

### 3. PivotTables والرسوم البيانية
| الشيت | المحتوى |
|---|---|
| `Category Analysis` | المبيعات والكمية والربح لكل فئة |
| `Loss-Making Sub-Categories` | الفئات الفرعية بخسارة فعلية (فلتر Value Filter < 0) |
| `States Analysis` | الربح لكل ولاية (49 ولاية) |
| `VIP Customers` | أعلى 10 عملاء ربحًا (فلتر Top 10) |
| `Dashboard` | تجميع أهم الرسوم البيانية |

## 📌 أبرز النتائج

- إجمالي المبيعات **2,294,992.78**، وإجمالي الربح **286,001.10**
- **Technology** الأعلى مبيعًا (834,227.18) والأعلى ربحًا (145,046.91)
- **Furniture** أقل إجمالي ربح (18,463.31) رغم مبيعات قريبة من باقي الفئات
- **3 فئات فرعية** فقط بخسارة فعلية: Tables (-17,725.59) وBookcases (-3,472.56) وSupplies (-1,188.99)
- **10 ولايات من 49** بخسارة، أكبرها Texas (-25,729.29) وOhio (-16,959.31)
- أعلى عميل ربحًا: Tamara Chand بربح 8,981.32

## 🛠️ المهارات المستخدمة

`Text to Columns` · `Remove Duplicates` · `Excel Tables` · `SUMIFS / COUNTIFS / AVERAGEIFS` · `PivotTables` · `Value & Top 10 Filters` · `Charts & Dashboard`
