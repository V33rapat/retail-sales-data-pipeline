# retail-sales-data-pipeline

## ภาพรวมโปรเจค (Overview)
โปรเจคนี้เป็นตัวอย่างงาน **End-to-End Data Project**  
ตั้งแต่การจัดการข้อมูลดิบ (Raw Data) ไปจนถึงการวิเคราะห์ข้อมูลและสรุป Insight  
ออกแบบมาเพื่อแสดงทักษะทั้งด้าน **Data Engineering** และ **Data Analysis**

## Dataset
- แหล่งที่มา: Kaggle – Retail / Superstore Sales Dataset
- ประเภทข้อมูล: ข้อมูลธุรกรรมการขาย (Transactional Data)
- รูปแบบไฟล์: CSV

## วัตถุประสงค์ (Objectives)
- สร้าง Data Pipeline สำหรับเตรียมข้อมูลให้พร้อมใช้งาน
- ออกแบบโครงสร้างข้อมูลแบบ Star Schema สำหรับงานวิเคราะห์
- วิเคราะห์ยอดขายและพฤติกรรมลูกค้า
- สรุป Insight และข้อเสนอแนะเชิงธุรกิจจากข้อมูล

## สถาปัตยกรรมระบบ (Architecture)
Raw CSV  
→ ทำความสะอาดและตรวจสอบข้อมูล (Python)  
→ ออกแบบ Data Model (Fact & Dimension Tables)  
→ โหลดข้อมูลเข้าสู่ฐานข้อมูล (SQLite / PostgreSQL)  
→ วิเคราะห์ข้อมูลด้วย SQL และ Visualization  

## การออกแบบข้อมูล (Data Modeling)

### Fact Table
- **fact_sales**
  - order_id
  - order_date
  - product_id
  - customer_id
  - quantity
  - sales

### Dimension Tables
- **dim_product**
  - product_id
  - category
  - sub_category
- **dim_customer**
  - customer_id
  - segment
  - region
- **dim_date**
  - date
  - month
  - year
  - quarter

## การวิเคราะห์ข้อมูลหลัก (Key Analyses)
- แนวโน้มรายได้รายเดือน (Monthly Revenue Trend)
- สินค้าและหมวดหมู่ที่ทำรายได้สูงสุด
- รายได้แยกตามกลุ่มลูกค้าและภูมิภาค
- วิเคราะห์พฤติกรรมลูกค้าซื้อซ้ำและซื้อครั้งเดียว

## เครื่องมือที่ใช้ (Tools & Technologies)
- Python (Pandas, NumPy)
- SQL (SQLite / PostgreSQL)
- Jupyter Notebook
- Data Visualization (Matplotlib / Seaborn)

## ผลลัพธ์ที่ได้ (Results)
- ได้ชุดข้อมูลที่พร้อมสำหรับงานวิเคราะห์ด้วย Star Schema
- พบปัจจัยสำคัญที่ส่งผลต่อรายได้และยอดขาย
- สามารถนำผลการวิเคราะห์ไปใช้ในการตัดสินใจเชิงธุรกิจได้

## โครงสร้างโปรเจค (Project Structure)
data/

├── raw/

├── processed/

notebooks/

├── 01_data_cleaning.ipynb

├── 02_data_modeling.ipynb

├── 03_analysis.ipynb

sql/

├── analytics_queries.sql

## แนวทางพัฒนาต่อ (Future Improvements)
- เพิ่ม Data Quality Check และ Logging
- รองรับการโหลดข้อมูลแบบ Incremental
- เชื่อมต่อ Dashboard เช่น Power BI หรือ Tableau

## ผู้จัดทำ (Author)
Veerapat Visaidsombat
