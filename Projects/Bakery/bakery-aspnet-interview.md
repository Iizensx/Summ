# Bakery ASP.NET Core MVC Interview Questions

Technology:

- C#
- ASP.NET Core MVC
- SQL
- Entity Framework Core


---

# 1. System Overview


## Q1. ช่วยอธิบายโปรเจกต์ Bakery ให้ฟังหน่อย?


## 🗣️ แนวตอบ

โปรเจกต์ Bakery เป็นระบบร้านเบเกอรี่ออนไลน์ครับ

ผู้ใช้สามารถดูสินค้า สั่งซื้อสินค้า จัดการตะกร้า และติดตามสถานะคำสั่งซื้อได้

ส่วน Admin สามารถจัดการสินค้า โปรโมชั่น Stock และดูข้อมูลการขายได้ครับ


---

## Q2. ระบบนี้แก้ปัญหาอะไร?


## 🗣️ แนวตอบ

ระบบช่วยลดขั้นตอนการสั่งซื้อแบบเดิมครับ

ลูกค้าสามารถสั่งซื้อผ่านระบบได้ง่ายขึ้น

และช่วยให้ร้านจัดการสินค้าและ Order ได้สะดวกขึ้นครับ


---

## Q3. ทำโปรเจกต์นี้คนเดียว มีส่วนไหนที่รับผิดชอบ?


## 🗣️ แนวตอบ

ผมพัฒนาทั้งระบบครับ

ตั้งแต่การออกแบบ Database

พัฒนา Backend ด้วย ASP.NET Core MVC

สร้างหน้าเว็บไซต์

รวมถึง Logic ของระบบ เช่น Order และ Promotion ครับ


---

# 2. Architecture


## Q4. อธิบาย Architecture ของระบบ


## 📌 จำ
User

↓

View

↓

Controller

↓

Business Logic

↓

Database


## 🗣️ แนวตอบ

ระบบใช้รูปแบบ MVC ครับ

View ทำหน้าที่แสดงผลให้ User

Controller รับ Request และจัดการ Flow

Model ใช้จัดการข้อมูลและติดต่อ Database ครับ


---

# 3. ASP.NET Core MVC


## Q5. MVC คืออะไร?


## 🗣️ แนวตอบ

MVC เป็น Design Pattern ที่แบ่งระบบออกเป็น 3 ส่วนครับ

Model ทำหน้าที่จัดการข้อมูล

View ทำหน้าที่แสดงผล

Controller ทำหน้าที่รับ Request และควบคุมการทำงานของระบบครับ


---

## Q6. Model คืออะไร?


## 🗣️ แนวตอบ

Model คือส่วนที่ใช้แทนข้อมูลของระบบครับ

เช่น

- Product
- Customer
- Order
- Payment

และใช้เชื่อมต่อกับ Database ครับ


---

## Q7. View คืออะไร?


## 🗣️ แนวตอบ

View คือส่วนที่ใช้แสดงผลให้ User ครับ

เช่น หน้า Product

หน้า Cart

หน้า Order


---

## Q8. Controller ทำหน้าที่อะไร?


## 🗣️ แนวตอบ

Controller เป็นตัวกลางระหว่าง User กับระบบครับ

รับ Request

เรียกใช้ Logic

ดึงหรือบันทึกข้อมูล

แล้วส่งผลกลับไปที่ View ครับ


---

## Q9. Routing คืออะไร?


## 🗣️ แนวตอบ

Routing คือการกำหนดเส้นทางของ Request ครับ

เช่น

/Product/List

/Product/Detail/1


ระบบจะส่ง Request ไปยัง Controller และ Action ที่กำหนดครับ


---

# 4. Dependency Injection


## Q10. Dependency Injection คืออะไร?


## 📌 จำ

ลดการสร้าง Object เอง


## 🗣️ แนวตอบ

Dependency Injection คือแนวทางที่ให้ Framework จัดการสร้าง Object ให้ครับ

ช่วยลดการผูกติดระหว่าง Class

ทำให้ Code Test และ Maintain ได้ง่ายขึ้นครับ


---

## Q11. ทำไมต้องใช้ Dependency Injection?


## 🗣️ แนวตอบ

เพื่อให้ระบบมีความยืดหยุ่นครับ

เช่น เปลี่ยน Database หรือ Service บางอย่างได้ง่ายขึ้น

และช่วยให้ Code แยกหน้าที่ชัดเจนครับ


---

# 5. Database Design


## Q12. ออกแบบ Database อย่างไร?


## 🗣️ แนวตอบ

ผมออกแบบจาก Entity หลักของระบบครับ

เช่น

- User
- Product
- Category
- Order
- OrderDetail
- Payment


โดยใช้ Primary Key และ Foreign Key เชื่อมความสัมพันธ์ครับ


---

## Q13. ตาราง Order กับ OrderDetail ทำไมต้องแยก?


## 🗣️ แนวตอบ

เพราะ Order เป็นข้อมูลหลักของคำสั่งซื้อ

ส่วน OrderDetail เก็บรายการสินค้าภายใน Order ครับ

ช่วยลดข้อมูลซ้ำและออกแบบ Database ได้เป็นระบบมากขึ้นครับ


---

## Q14. Primary Key คืออะไร?


## 🗣️ แนวตอบ

Primary Key คือ Column ที่ใช้ระบุข้อมูลแต่ละ Record แบบไม่ซ้ำกันครับ


เช่น

CustomerID

ProductID


---

## Q15. Foreign Key คืออะไร?


## 🗣️ แนวตอบ

Foreign Key คือ Column ที่ใช้เชื่อมความสัมพันธ์ระหว่าง Table ครับ

เช่น Order มี CustomerID เพื่อเชื่อมกับ User ครับ


---

# 6. Business Logic


## Q16. ระบบตะกร้าสินค้าทำงานอย่างไร?


## 🗣️ แนวตอบ

เมื่อ User เลือกสินค้า

ระบบจะเก็บข้อมูลสินค้าและจำนวนที่เลือกไว้

เมื่อ Checkout จะนำข้อมูลไปสร้าง Order และบันทึกลง Database ครับ


---

## Q17. ระบบ Order ทำงานอย่างไร?


## 🗣️ แนวตอบ

Flow คือ

เลือกสินค้า

↓

เพิ่มลง Cart

↓

ยืนยัน Order

↓

ตรวจสอบข้อมูล

↓

บันทึก Order

↓

ลด Stock

↓

เปลี่ยนสถานะ Order


ครับ


---

## Q18. Stock ลดตอนไหน?


## 🗣️ แนวตอบ

ควรลด Stock หลังจากสร้าง Order สำเร็จหรือหลังยืนยันการชำระเงินครับ

เพื่อป้องกันปัญหาสินค้าถูกตัด Stock ทั้งที่ยังไม่ได้ซื้อจริงครับ


---

## Q19. Promotion ทำงานอย่างไร?


## 🗣️ แนวตอบ

ระบบตรวจสอบเงื่อนไขของ Promotion ครับ

เช่น

จำนวนขั้นต่ำ

ช่วงเวลาโปรโมชั่น

ประเภทสินค้า

จากนั้นคำนวณส่วนลดก่อนสร้าง Order ครับ


---

# 7. Authentication / Security


## Q20. ระบบ Login ทำอย่างไร?


## 🗣️ แนวตอบ

User Login ด้วย Email และ Password ครับ

ระบบตรวจสอบข้อมูล

ถ้าถูกต้องจะสร้าง Session หรือ Identity เพื่อให้ User เข้าใช้งานระบบได้ครับ


---

## Q21. Password เก็บอย่างไร?


## 🗣️ แนวตอบ

ไม่ควรเก็บ Password แบบ Text ธรรมดาครับ

ควร Hash Password ด้วย Algorithm ที่ปลอดภัย เช่น bcrypt


---

## Q22. Authorization คืออะไร?


## 🗣️ แนวตอบ

Authorization คือการกำหนดสิทธิ์การเข้าถึงครับ

เช่น

Customer สามารถสั่งซื้อสินค้า

Admin สามารถจัดการสินค้าได้


---

## Q23. SQL Injection ป้องกันอย่างไร?


## 🗣️ แนวตอบ

ใช้ Parameterized Query หรือ ORM เช่น Entity Framework Core

ไม่ต่อ String SQL โดยตรงครับ


---

# 8. Admin Dashboard


## Q24. Admin Dashboard ทำอะไรได้บ้าง?


## 🗣️ แนวตอบ

Admin สามารถจัดการข้อมูลของระบบครับ

เช่น

- เพิ่ม/แก้ไขสินค้า
- จัดการ Stock
- จัดการ Promotion
- ดู Order
- ดูยอดขาย


---

## Q25. Dashboard แสดงข้อมูลอย่างไร?


## 🗣️ แนวตอบ

Backend จะ Query ข้อมูลจาก Database

เช่น จำนวน Order หรือยอดขาย

แล้วส่งข้อมูลมาแสดงเป็น Dashboard ครับ


---

# 9. Senior Question


## Q26. ถ้ามี User ซื้อสินค้าพร้อมกันจำนวนมาก?


## 🗣️ แนวตอบ

ต้องจัดการ Transaction ของ Database ครับ

เพื่อป้องกัน Stock ติดลบ

และตรวจสอบข้อมูลก่อน Update ทุกครั้ง


---

## Q27. ถ้า Database มีข้อมูลเยอะขึ้น?


## 🗣️ แนวตอบ

สามารถเพิ่ม Index

ปรับ Query

ใช้ Pagination

และตรวจสอบ Performance ของ Database ครับ


---

## Q28. ถ้าเว็บไซต์ช้าแก้อย่างไร?


## 🗣️ แนวตอบ

ตรวจสอบว่าเกิดจากส่วนไหนครับ

เช่น

- Database Query
- Backend Logic
- Network

แล้วแก้ไขเฉพาะจุดที่เป็นปัญหาครับ


---

## Q29. ถ้าทำใหม่จะปรับอะไร?


## 🗣️ แนวตอบ

ผมจะวาง Architecture ให้ชัดขึ้นตั้งแต่ต้นครับ

เพิ่ม Unit Test

เพิ่ม Logging

และออกแบบ Database ให้รองรับการขยายระบบในอนาคตครับ


---

# Summary


ASP.NET Core MVC

= Framework สำหรับสร้าง Web Application


MVC

= Model + View + Controller


Controller

= รับ Request และควบคุม Flow


Model

= จัดการข้อมูล


View

= แสดงผล


SQL

= จัดเก็บข้อมูลระบบ


Entity Framework Core

= เชื่อมต่อ Database


Security

= Authentication + Authorization

