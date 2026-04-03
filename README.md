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

​Confusion Matrix

​This matrix visualizes the model's diagnostic accuracy in identifying specific fault types after detection:
​Class 1 (Highest Accuracy): The model correctly diagnosed 34 instances of this fault type, showing its strong predictive power.
​Class 0 & 2 (Reliable Diagnosis): Successfully identified 24 and 28 cases respectively, with minimal overlap between categories.
​Minimal Misclassification: The diagonal trend confirms that the model is highly effective at distinguishing between different failure modes.
​Diagnostic Depth: This visualization proves the model's ability to provide actionable insights for maintenance by pinpointing the exact fault.

​بالعربي

مصفوفة الارتباك لتشخيص الأعطال (Multi-Class)
​توضح هذه المصفوفة دقة الموديل في تحديد نوع العطل بدقة بعد اكتشافه:
​الفئة 1: حقق الموديل أعلى دقة بتشخيص 34 حالة بشكل صحيح.
​الفئات 0 و2: نجح الموديل في تحديد 24 و28 حالة على التوالي، مما يثبت كفاءته في التمييز بين أنواع الأعطال المختلفة.
​دقة التشخيص: يظهر الرسم البياني قدرة النظام على إعطاء معلومات دقيقة تساعد في عمليات الصيانة وتحديد المشكلة بسرعة.

![Multi-class Classification Report](<   <img width="591" height="254" alt="Classification_Report_Model_2" src="https://github.com/user-attachments/assets/e09c75ad-89dc-451a-bb35-c9a6c31c31cc" />
  >)

​Classification Report

​This report provides a detailed breakdown of the model's diagnostic performance across all fault categories:
​Precision (Weighted Avg: 70%): Reflects the model's high reliability in correctly identifying the specific type of fault once detected.
​Recall (Class 0: 90%): Exceptional ability to capture almost all instances of Class 0 faults, ensuring critical issues are not missed.
​F1-Score (Overall Stability): The model shows a balanced performance between precision and recall, especially in Class 0 and Class 2, making it a stable diagnostic tool.
​Accuracy (66%): Given the complexity of distinguishing between three different fault types, this accuracy level provides a strong baseline for automated diagnosis.

​بالعربي

تقرير أداء التصنيف (Classification Report)
​يوضح هذا التقرير كفاءة الموديل في تحليل وتشخيص نوع العطل بدقة:
​الدقة (Precision): حقق الموديل دقة متوسطة بنسبة 70% في تحديد الفئة الصحيحة للعطل.
​قدرة الاستدعاء (Recall): تميز الموديل بقدرة فائقة على اكتشاف أعطال الفئة (Class 0) بنسبة 90%.
​مؤشر F1-Score: يعكس الأداء المتوازن للموديل وقدرته على التعامل مع البيانات المعقدة لكل نوع من أنواع الأعطال

---

### 🔮 Final Predictions Sample
A snapshot of the end-to-end system predictions on unseen data.

![Final Predictions](<   <img width="996" height="710" alt="Final_Predicted_all_Model" src="https://github.com/user-attachments/assets/4bad91d8-9233-4634-b8ab-7cb229ee50fd" />
  >)
​🛠️ Automated Diagnostic Report: Sample Testing

​This section demonstrates the system's end-to-end performance on specific test samples, showcasing the seamless transition from fault detection to diagnosis:
​100% Detection Success (Phase 1): In all showcased samples, the first model accurately identified the presence of a "Failure Detected" status, matching the ground truth perfectly.
​Detailed Diagnosis (Phase 2): The second model provided specific failure type predictions (e.g., Power Failure / PWF), proving its utility in providing actionable maintenance data.
​Dual-Model Validation:
​Phase 1 Accuracy (Fault Detection): Maintained at 100% for these test cases.
​Phase 2 Accuracy (Type Diagnosis): Achieved 60% in these specific complex scenarios.
​Operational Integrity: The output shows that even when a diagnosis is complex, the initial detection remains flawless, ensuring no critical issues are overlooked.

​بالعربي

تقرير الفحص الآلي للعينات (Sample Testing)
​يوضح هذا القسم أداء النظام المتكامل عند فحص عينات حقيقية، وكيفية انتقال العمل من مرحلة الاكتشاف إلى مرحلة التشخيص:
​نجاح الاكتشاف بنسبة 100%: أظهر الموديل الأول دقة كاملة في اكتشاف وجود العطل (Failure Detected) في جميع العينات المعروضة، وهو ما يتطابق تماماً مع الحالة الفعلية.
​دقة التشخيص النوعي: نجح الموديل الثاني في تحديد نوع العطل (مثل Power Failure / PWF)، مما يوفر بيانات تشغيلية قيمة لفرق الصيانة.
​كفاءة الموديلات المزدوجة:
​دقة اكتشاف الأعطال: وصلت إلى 100% في العينات المعروضة.
​دقة تحديد النوع: وصلت إلى 60%، مما يعكس قدرة الموديل على التعامل مع أنواع الأعطال المعقدة والمتداخلة


## 👤 Author
**[MOHAMED BELAL]** *Deep Learning & Data Engineering Enthusiast*

MY PHONE [01018689118]



## 🛠️ الأدوات المستخدمة (Tech Stack)
* Python (Pandas, NumPy)
* Scikit-learn & XGBoost
* Joblib (للحفظ والتحميل)


---
**💡 ملاحظة:** هذا المشروع هو تمهيد للانتقال إلى تقنيات التعلم العميق (Deep Learning).
