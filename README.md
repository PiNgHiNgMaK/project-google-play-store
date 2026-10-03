# 📱 Google Play Store App Rating Prediction
> **1145 201 Mathematics for Data Science** | Semester 1/2568

โครงงานวิเคราะห์และคาดการณ์คะแนนความพึงพอใจ (Rating) ของแอปพลิเคชันบน Google Play Store โดยใช้เทคนิคทางคณิตศาสตร์ วิทยาการข้อมูล และ Machine Learning

---

## 📊 สรุปภาพรวมโครงงาน (Project Summary)

* **Problem Statement:** ในปัจจุบันตลาดแอปพลิเคชันบน Google Play Store มีการแข่งขันที่สูงมาก โครงงานนี้จึงศึกษาวิเคราะห์ความสัมพันธ์ระหว่างปัจจัยต่างๆ เช่น ยอดดาวน์โหลด (Installs), จำนวนรีวิว (Reviews), และราคา (Price) เพื่อสร้างแบบจำลองคาดการณ์คะแนนเรตติ้ง (Rating) ช่วยให้นักพัฒนานำข้อมูลเชิงลึกไปปรับปรุงและวางแผนพัฒนาแอปพลิเคชันอย่างมีประสิทธิภาพ

### การดำเนินงานตามรายวิชา (CLO Mapping)

| CLO | หัวข้อวิเคราะห์ | สรุปผลการดำเนินงาน |
| :--- | :--- | :--- |
| **CLO1** | Linear Algebra (PCA / Feature Engineering) | ทำการลดมิติข้อมูลและวิเคราะห์ความสัมพันธ์ของฟีเจอร์เชิงตัวเลขเพื่อลดปัญหา Multicollinearity และสกัดฟีเจอร์สำคัญ |
| **CLO2** | Statistical Learning & EDA | ทำการสำรวจการกระจายตัวของข้อมูล (Target Distribution), วิเคราะห์ Missing Values และศึกษาความซับซ้อนของโมเดลเพื่อป้องกัน Overfitting / Underfitting |
| **CLO3** | Regression / Classification Models | พัฒนาแบบจำลองคาดการณ์คะแนนพึงพอใจ เช่น Linear Regression, Ridge Regression และ Logistic Regression |
| **CLO4** | Model Evaluation & Selection | ประเมินผลแบบจำลองด้วย $K$-Fold Cross-Validation และเปรียบเทียบประสิทธิภาพด้วยตัวชี้วัด เช่น RMSE, $R^2$ หรือ Accuracy |

---

## 📂 สมาชิกกลุ่ม (Group Members)

- **นายภัทรพงษ์ จรรยากรณ์** — รหัสนักศึกษา 68114540434
- **นางสาวฐิติรัตน์ แสงห้าว** — รหัสนักศึกษา 68114540166

---

## 🛠️ โครงสร้างโค้ดและการดำเนินงาน (Project Workflow)

1. **Part 1: Dataset Overview & EDA**
   - โหลดข้อมูล Google Play Store Apps Dataset
   - จัดการ Missing Values (เช่น ในคอลัมน์ `Rating` มีค่าสูญหาย 1,474 รายการ)
   - วิเคราะห์สถิติเบื้องต้นด้วย `.describe()` และแสดงภาพการกระจายตัวของข้อมูล
2. **Part 2: Feature Engineering & Linear Algebra (CLO1)**
   - แปลงข้อมูลประเภทข้อความ/ตัวเลข (เช่น `Installs`, `Price`, `Size`) ให้เป็น Numeric
   - ทำ Scaling ข้อมูลด้วย `StandardScaler` และประยุกต์ใช้ Linear Algebra
3. **Part 3: Statistical Learning (CLO2)**
   - วิเคราะห์กราฟความสัมพันธ์และการกระจายตัวของ Target Variable (`Rating`)
4. **Part 4 & 5: Model Building & Evaluation (CLO3 & CLO4)**
   - แบ่งข้อมูล Train/Test Split
   - ฝึกสอนแบบจำลอง Linear Regression, Ridge, และ Logistic Regression
   - ประเมินประสิทธิภาพโมเดลด้วย Cross-Validation (`cross_val_score`)

---

## 💻 Tech Stack & Libraries Used

* **Language:** Python 3.9+
* **Libraries:**
  * `pandas`, `numpy` — สำหรับจัดการและประมวลผลข้อมูล
  * `matplotlib`, `seaborn` — สำหรับทำ Data Visualization
  * `scikit-learn` — สำหรับทำ Feature Scaling, Cross-Validation, และสร้าง Machine Learning Models
  * `kagglehub` — สำหรับดาวน์โหลดชุดข้อมูลโดยตรง

---

## 📑 Acknowledgements

* **Dataset:** [Google Play Store Apps Dataset on Kaggle](https://www.kaggle.com/datasets/lava18/google-play-store-apps) โดย Lavanya Gupta
* **Environment:** ประมวลผลและทดสอบแบบจำลองบน Google Colab
