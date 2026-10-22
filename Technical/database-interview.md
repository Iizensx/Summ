# Database Technical Interview Questions

Technology:

- MySQL
- MongoDB
- SQL
- Database Design


---

# 1. Database Basic


## Q1. Database คืออะไร?


## 🗣️ แนวตอบ

Database คือระบบที่ใช้สำหรับจัดเก็บ จัดการ และเรียกใช้ข้อมูลครับ

ช่วยให้ Application สามารถบันทึกและค้นหาข้อมูลได้อย่างมีประสิทธิภาพ


---

## Q2. ทำไมต้องใช้ Database?


## 🗣️ แนวตอบ

เพราะระบบส่วนใหญ่ต้องมีการเก็บข้อมูลถาวรครับ

เช่น

- User
- Product
- Booking
- Order

Database ช่วยจัดการข้อมูลให้เป็นระบบและค้นหาได้ง่ายครับ


---

# 2. SQL Database


## Q3. SQL Database คืออะไร?


## 🗣️ แนวตอบ

SQL Database เป็นฐานข้อมูลแบบ Relational Database ครับ

ข้อมูลถูกจัดเก็บเป็น Table

และเชื่อมโยงกันด้วย Relation เช่น Primary Key และ Foreign Key


---

## Q4. ทำไมเลือกใช้ MySQL?


## 🗣️ แนวตอบ

เลือกใช้ MySQL เพราะเป็น Database ที่นิยม

เหมาะกับข้อมูลที่มีความสัมพันธ์ชัดเจน

เช่น User, Booking, Payment

และรองรับ SQL Query ได้ดีครับ


---

# 3. Table Design


## Q5. Table คืออะไร?


## 🗣️ แนวตอบ

Table คือโครงสร้างที่ใช้เก็บข้อมูลใน Database ครับ

ประกอบด้วย

Column

และ

Row


---

## Q6. Row และ Column คืออะไร?


## 🗣️ แนวตอบ

Row คือข้อมูลหนึ่งรายการครับ

เช่น User หนึ่งคน


Column คือคุณสมบัติของข้อมูลครับ

เช่น

Name

Email

Password


---

# 4. Primary Key / Foreign Key


## Q7. Primary Key คืออะไร?


## 📌 จำ

Unique Identifier


## 🗣️ แนวตอบ

Primary Key คือ Column ที่ใช้ระบุข้อมูลแต่ละ Record ครับ

ค่าต้องไม่ซ้ำกันและไม่เป็น Null


ตัวอย่าง

User_ID


---

## Q8. Foreign Key คืออะไร?


## 🗣️ แนวตอบ

Foreign Key คือ Column ที่ใช้เชื่อมความสัมพันธ์ระหว่าง Table ครับ

โดยอ้างอิง Primary Key ของ Table อื่น


ตัวอย่าง


User_ID ใน Booking Table


---

## Q9. ทำไมต้องใช้ Foreign Key?


## 🗣️ แนวตอบ

เพื่อรักษาความถูกต้องของข้อมูลครับ

เช่น ไม่ให้ Booking มี User ที่ไม่มีอยู่จริง


---

# 5. Relationship


## Q10. Relationship ใน Database มีอะไรบ้าง?


## 🗣️ แนวตอบ


หลัก ๆ มี 3 แบบครับ


One-to-One

หนึ่งข้อมูลสัมพันธ์กับหนึ่งข้อมูล


One-to-Many

หนึ่งข้อมูลสัมพันธ์กับหลายข้อมูล


Many-to-Many

หลายข้อมูลสัมพันธ์กับหลายข้อมูล


---

## Q11. ตัวอย่าง Relationship ใน Smart Parking?


## 🗣️ แนวตอบ


User 1 คน

สามารถมี Vehicle หลายคัน


Vehicle 1 คัน

สามารถมี Booking หลายครั้ง


Booking 1 รายการ

มี Payment 1 รายการ


---

# 6. SQL Query


## Q12. SQL คืออะไร?


## 🗣️ แนวตอบ

SQL เป็นภาษาที่ใช้จัดการข้อมูลใน Relational Database ครับ

เช่น

เพิ่ม

ค้นหา

แก้ไข

ลบข้อมูล


---

## Q13. SELECT ใช้ทำอะไร?


## 🗣️ แนวตอบ

SELECT ใช้สำหรับดึงข้อมูลจาก Database ครับ


ตัวอย่าง


```sql
SELECT * FROM users;

Q14. INSERT ใช้ทำอะไร?
🗣️ แนวตอบ
INSERT ใช้สำหรับเพิ่มข้อมูลใหม่เข้า Database ครับ
Q15. UPDATE ใช้ทำอะไร?
🗣️ แนวตอบ
UPDATE ใช้แก้ไขข้อมูลที่มีอยู่แล้วครับ
Q16. DELETE ใช้ทำอะไร?
🗣️ แนวตอบ
DELETE ใช้ลบข้อมูลจาก Database ครับ
7. JOIN
Q17. JOIN คืออะไร?
🗣️ แนวตอบ
JOIN คือการรวมข้อมูลจากหลาย Table ที่มีความสัมพันธ์กันครับ
Q18. INNER JOIN คืออะไร?
🗣️ แนวตอบ
INNER JOIN จะแสดงเฉพาะข้อมูลที่มี Match กันทั้งสอง Table ครับ

ตัวอย่าง

User ที่มี Booking
Q19. LEFT JOIN คืออะไร?
🗣️ แนวตอบ
LEFT JOIN จะแสดงข้อมูลทั้งหมดจาก Table ฝั่งซ้าย

แม้อีกฝั่งจะไม่มีข้อมูลครับ
8. Normalization
Q20. Normalization คืออะไร?
🗣️ แนวตอบ
Normalization คือการออกแบบ Database เพื่อลดข้อมูลซ้ำครับ

ทำให้ข้อมูลเป็นระเบียบและแก้ไขง่ายขึ้น
Q21. ทำไมต้องลด Data Duplicate?
🗣️ แนวตอบ
เพื่อลดปัญหาข้อมูลไม่ตรงกันครับ

เช่น

แก้ชื่อ User แล้วต้องแก้หลายที่
9. Index
Q22. Index คืออะไร?
📌 จำ
ค้นหาเร็วขึ้น
🗣️ แนวตอบ
Index คือโครงสร้างที่ช่วยให้ Database ค้นหาข้อมูลได้เร็วขึ้นครับ

เหมือนสารบัญของหนังสือ
Q23. ควรสร้าง Index ที่ Column ไหน?
🗣️ แนวตอบ
ควรสร้างกับ Column ที่ค้นหาบ่อยครับ

เช่น
- Email
- User_ID
- Booking_ID
Q24. Index มีข้อเสียไหม?
🗣️ แนวตอบ
มีครับ

ใช้พื้นที่เพิ่มขึ้น

และทำให้ Insert หรือ Update ช้าลงเล็กน้อย
10. Transaction
Q25. Transaction คืออะไร?
🗣️ แนวตอบ
Transaction คือชุดคำสั่งที่ต้องทำงานร่วมกันครับ

ถ้าขั้นตอนใดผิดพลาด

สามารถ Rollback กลับไปสถานะเดิมได้
Q26. ตัวอย่าง Transaction ในระบบ?
🗣️ แนวตอบ
เช่น การจองที่จอดรถครับ
1. ตรวจสอบช่องว่าง
2. สร้าง Booking
3. Update สถานะช่องจอด
ถ้าเกิด Error ต้องยกเลิกทั้งหมด
11. MongoDB
Q27. MongoDB คืออะไร?
🗣️ แนวตอบ
MongoDB เป็น NoSQL Database ครับ

เก็บข้อมูลในรูปแบบ Document คล้าย JSON

ทำให้เหมาะกับข้อมูลที่มีโครงสร้างเปลี่ยนแปลงบ่อย
Q28. Collection และ Document คืออะไร?
🗣️ แนวตอบ
Collection

เปรียบเหมือน Table

Document

เปรียบเหมือน Row

แต่ข้อมูลจะเก็บเป็น JSON Document ครับ
Q29. ทำไมเลือก MongoDB?
🗣️ แนวตอบ
เหมาะกับข้อมูลที่ไม่ตายตัวครับ

เช่น

ข้อมูลสัตว์เลี้ยง

ข้อมูล Profile

ที่อาจมี Field เพิ่มขึ้นในอนาคต
12. Reference vs Embed
Q30. Embed คืออะไร?
🗣️ แนวตอบ
Embed คือการเก็บข้อมูลซ้อนกันใน Document เดียวครับ

เหมาะกับข้อมูลที่ใช้ร่วมกันเสมอ
Q31. Reference คืออะไร?
🗣️ แนวตอบ
Reference คือการแยกข้อมูลออกเป็นหลาย Collection

แล้วเก็บ ID เพื่อเชื่อมกันครับ
13. Database Performance
Q32. ถ้า Database ช้าจะแก้อย่างไร?
🗣️ แนวตอบ
ตรวจสอบ Query ก่อนครับ

จากนั้น
- เพิ่ม Index
- Optimize Query
- ใช้ Pagination
- ใช้ Cache
Q33. Pagination คืออะไร?
🗣️ แนวตอบ
Pagination คือการแบ่งข้อมูลออกเป็นหลายหน้า

แทนที่จะโหลดข้อมูลทั้งหมดครั้งเดียวครับ
14. Security
Q34. ป้องกันข้อมูลใน Database อย่างไร?
🗣️ แนวตอบ
- Hash Password
- จำกัด Permission
- Validate Input
- Backup Database
- ใช้ Environment Variable
Q35. SQL Injection ป้องกันอย่างไร?
🗣️ แนวตอบ
ใช้ Parameterized Query หรือ ORM ครับ

ไม่ต่อ String SQL จาก Input ของ User โดยตรง
15. Senior Question
Q36. ถ้ามีข้อมูล User 10 ล้านคน?
🗣️ แนวตอบ
ต้องออกแบบ Database ให้รองรับ Scale ครับ

เช่น
- Index
- Pagination
- Cache
- Database Partition
- Replication
Q37. ถ้าข้อมูลซ้ำกันแก้อย่างไร?
🗣️ แนวตอบ
ตรวจสอบ Database Design ครับ

เพิ่ม Constraint

และปรับ Normalization ให้เหมาะสม
Q38. ถ้า User จองพร้อมกัน 2 คน?
🗣️ แนวตอบ
ต้องป้องกันด้วย Transaction

และตรวจสอบข้อมูลก่อนบันทึกครับ
Q39. SQL กับ NoSQL ต่างกันอย่างไร?
🗣️ แนวตอบ
SQL

เหมาะกับข้อมูลที่มี Relation ชัดเจน

NoSQL

เหมาะกับข้อมูลยืดหยุ่นและ Scale ได้ง่าย
Summary
SQL

= Table + Relation

Primary Key

= ระบุข้อมูลไม่ซ้ำ

Foreign Key

= เชื่อม Table

JOIN

= รวมข้อมูลหลาย Table

Index

= ค้นหาเร็วขึ้น

Transaction

= ทำงานหลายขั้นตอนให้ปลอดภัย

MongoDB

= NoSQL แบบ Document

Normalization

= ลดข้อมูลซ้ำ
