# 📊 مشروع الصيانة التنبؤية | Predictive Maintenance Project

## 📝 وصف المشروع (Description)
هذا المشروع يهدف إلى التنبؤ بأعطال الماكينات قبل وقوعها وتحديد نوع العطل بدقة باستخدام خوارزميات تعلم الآلة.

## 🚀 المميزات (Features)
* **الكشف الثنائي (Binary Classification):** تحديد ما إذا كانت الماكينة سليمة أم بها عطل بدقة **99%**.
* **التشخيص المتعدد (Multi-class Classification):** تحديد نوع العطل (طاقة، تآكل، إجهاد...) بدقة **77%**.
* **واجهة تقرير عربية/إنجليزية:** عرض النتائج بلغة مفهومة للمستخدم النهائي.

## 🛠️ Predictive Maintenance Pipeline (Two-Stage Model)

This project implements a professional diagnostic pipeline consisting of two specialized models to ensure high accuracy in fault detection and classification.

### 🔄 System Workflow
1. **Model 1 (Binary Classification):** Detects whether the machine has a fault or is operating normally.
2. **Model 2 (Multi-class Classification):** If a fault is detected, this model identifies the specific type of failure.

---

### 📊 Model 1: Binary Fault Detection
*Goal: Identify if the system is in a "Fault" or "Normal" state.*

#### Performance Evaluation:
![Binary Confusion Matrix](<  <img width="835" height="693" alt="Confusion_Matrix_Model_1" src="https://github.com/user-attachments/assets/13677f3c-130d-4e33-a4f4-ea57e63636a7" />
   >)

​🎯 Model Performance: Confusion Matrix (XGBoost)

​The Confusion Matrix illustrates the exceptional performance of our model in classifying Normal vs. Failure states:
​True Negatives (Normal): 1,389 cases were correctly identified as Normal.
​True Positives (Failure): 1,416 cases were correctly identified as Failure.
​Minimal Errors: The model only misclassified 39 cases out of 2,844 total samples, demonstrating its high reliability.

​بالعربي

​أداء النموذج: مصفوفة الارتباك (XGBoost)
توضح هذه المصفوفة الكفاءة العالية للنموذج في التمييز بين الحالات الطبيعية وحالات الفشل:
​النتائج السليمة (Normal): تم تحديد 1,389 حالة طبيعية بشكل صحيح.
​حالات الفشل (Failure): تم تحديد 1,416 حالة فشل بشكل صحيح.
​دقة فائقة: أظهر النموذج قدرة استثنائية على التصنيف بأقل نسبة خطأ ممكنة، مما يجعله نموذجاً موثوقاً لاتخاذ القرارات.


![Binary Classification Report](<   <img width="551" height="244" alt="Classification_Report_Model_1" src="https://github.com/user-attachments/assets/1f66c2a4-6ab7-48fd-a51d-2f883a8d4999" />
  >)

​📈 Detailed Classification Performance

​The model's performance was evaluated using a comprehensive classification report, showing near-perfect results across all key metrics:
​Precision (99%): Out of all instances the model predicted as a certain class, 99% were actually correct.
​Recall (99%): The model successfully identified 99% of all actual instances in the dataset.
​F1-Score (0.99): A near-perfect balance between Precision and Recall, proving the model is robust and stable.
​Overall Accuracy (99%): The model correctly classified 2844 samples with minimal error.

​بالعربي

​تقرير التصنيف التفصيلي (Classification Report):
أظهر النموذج أداءً استثنائياً بدقة تصل إلى 99%؛ حيث نجح في تحقيق توازن شبه مثالي بين جميع المعايير التقنية (Precision, Recall, F1-Score). هذا الرقم يعكس الكفاءة العالية للخوارزمية في التعامل مع البيانات وتصنيفها بدقة فائقة.


---

### 📊 Model 2: Fault Type Classification
*Goal: Categorize the detected fault into its specific technical category.*

#### Performance Evaluation:
![Multi-class Confusion Matrix](<  <img width="947" height="767" alt="Confusion_Matrix_Model_2" src="https://github.com/user-attachments/assets/685cfd12-0ab5-467f-bd41-6bac7d9af2be" />
   >)

​🎯 Model Performance: Confusion Matrix (XGBoost)

​The Confusion Matrix illustrates the exceptional performance of our model in classifying Normal vs. Failure states:
​True Negatives (Normal): 1,389 cases were correctly identified as Normal.
​True Positives (Failure): 1,416 cases were correctly identified as Failure.
​Minimal Errors: The model only misclassified 39 cases out of 2,844 total samples, demonstrating its high reliability.

​بالعربي
:
​أداء النموذج: مصفوفة الارتباك (XGBoost)
توضح هذه المصفوفة الكفاءة العالية للنموذج في التمييز بين الحالات الطبيعية وحالات الفشل:
​النتائج السليمة (Normal): تم تحديد 1,389 حالة طبيعية بشكل صحيح.
​حالات الفشل (Failure): تم تحديد 1,416 حالة فشل بشكل صحيح.
​دقة فائقة: أظهر النموذج قدرة استثنائية على التصنيف بأقل نسبة خطأ ممكنة، مما يجعله نموذجاً موثوقاً لاتخاذ القرارات.

![Multi-class Classification Report](<   <img width="591" height="254" alt="Classification_Report_Model_2" src="https://github.com/user-attachments/assets/e09c75ad-89dc-451a-bb35-c9a6c31c31cc" />
  >)

​📈 Detailed Classification Performance

​The model's performance was evaluated using a comprehensive classification report, showing near-perfect results across all key metrics:
​Precision (99%): Out of all instances the model predicted as a certain class, 99% were actually correct.
​Recall (99%): The model successfully identified 99% of all actual instances in the dataset.
​F1-Score (0.99): A near-perfect balance between Precision and Recall, proving the model is robust and stable.
​Overall Accuracy (99%): The model correctly classified 2844 samples with minimal error.

​بالعربي

​تقرير التصنيف التفصيلي (Classification Report):
أظهر النموذج أداءً استثنائياً بدقة تصل إلى 99%؛ حيث نجح في تحقيق توازن شبه مثالي بين جميع المعايير التقنية (Precision, Recall, F1-Score). هذا الرقم يعكس الكفاءة العالية للخوارزمية في التعامل مع البيانات وتصنيفها بدقة فائقة.

---

### 🔮 Final Predictions Sample
A snapshot of the end-to-end system predictions on unseen data.

![Final Predictions](<   <img width="996" height="710" alt="Final_Predicted_all_Model" src="https://github.com/user-attachments/assets/4bad91d8-9233-4634-b8ab-7cb229ee50fd" />
  >)



## 🛠️ الأدوات المستخدمة (Tech Stack)
* Python (Pandas, NumPy)
* Scikit-learn & XGBoost
* Joblib (للحفظ والتحميل)

## 📁 ملفات الموديلات (Saved Models)
تم حفظ الموديلات كملفات جاهزة للاستخدام:
1.  `machine_failure_detector.joblib`
2.  `failure_type_classifier.joblib`

---
**💡 ملاحظة:** هذا المشروع هو تمهيد للانتقال إلى تقنيات التعلم العميق (Deep Learning).
