# Node.js Backend Technical Interview Questions

Technology:

- Node.js
- Express.js
- REST API
- Backend Development


---

# 1. Node.js Basic


## Q1. Node.js คืออะไร?


## 🗣️ แนวตอบ

Node.js คือ Runtime Environment ที่ทำให้ JavaScript สามารถทำงานฝั่ง Server ได้ครับ

ใช้สำหรับสร้าง Backend API ติดต่อกับ Database และจัดการ Logic ของระบบครับ


---

## Q2. ทำไมเลือกใช้ Node.js?


## 📌 จำ

JavaScript เดียวกัน

เร็วในการพัฒนา

เหมาะกับ API


## 🗣️ แนวตอบ

เลือกใช้ Node.js เพราะใช้ภาษา JavaScript ทั้ง Frontend และ Backend ครับ

ทำให้ทีมพัฒนาเรียนรู้และดูแล Code ได้ง่ายขึ้น

เหมาะกับการสร้าง REST API และ Web Application ครับ


---

## Q3. Node.js แตกต่างจาก JavaScript ใน Browser อย่างไร?


## 🗣️ แนวตอบ

JavaScript ใน Browser ใช้สำหรับจัดการหน้าเว็บครับ

ส่วน Node.js ทำให้ JavaScript สามารถทำงานฝั่ง Server ได้

เช่น ติดต่อ Database และสร้าง API ครับ


---

# 2. Express.js


## Q4. Express.js คืออะไร?


## 🗣️ แนวตอบ

Express.js เป็น Framework บน Node.js สำหรับสร้าง Backend Application ครับ

ช่วยจัดการ Routing, Middleware และ API ได้ง่ายขึ้นครับ


---

## Q5. ทำไมต้องใช้ Express?


## 🗣️ แนวตอบ

เพราะ Express มีโครงสร้างที่ง่ายและยืดหยุ่นครับ

เหมาะกับการสร้าง REST API

และสามารถเพิ่ม Middleware ต่าง ๆ ได้ง่ายครับ


---

# 3. REST API


## Q6. REST API คืออะไร?


## 📌 จำ

Frontend ↔ Backend


## 🗣️ แนวตอบ

REST API คือรูปแบบการสื่อสารระหว่าง Client และ Server ผ่าน HTTP Protocol ครับ

Frontend จะส่ง Request ไปยัง Backend

และ Backend จะส่ง Response กลับมา


---

## Q7. HTTP Method มีอะไรบ้าง?


## 🗣️ แนวตอบ

หลัก ๆ มี 4 แบบครับ


GET

ใช้สำหรับดึงข้อมูล


POST

ใช้สำหรับสร้างข้อมูล


PUT / PATCH

ใช้สำหรับแก้ไขข้อมูล


DELETE

ใช้สำหรับลบข้อมูล


---

## Q8. API Endpoint คืออะไร?


## 🗣️ แนวตอบ

API Endpoint คือ URL ที่ใช้ติดต่อกับ Backend ครับ

เช่น

GET /users

POST /booking


เพื่อให้ Client เรียกใช้งาน Function ของระบบครับ


---

# 4. Middleware


## Q9. Middleware คืออะไร?


## 🗣️ แนวตอบ

Middleware คือ Function ที่ทำงานระหว่าง Request และ Response ครับ

ใช้สำหรับตรวจสอบหรือประมวลผลก่อนส่งข้อมูลไป Controller


---

## Q10. Middleware ใช้ทำอะไรบ้าง?


## 🗣️ แนวตอบ

ตัวอย่างเช่น


- ตรวจสอบ JWT Token
- ตรวจสอบ Permission
- Logging
- Error Handling
- Validate Request


---

## Q11. Middleware ทำงานลำดับไหน?


## 🗣️ แนวตอบ

ลำดับการทำงานคือ
Request

↓

Middleware

↓

Controller

↓

Response


Middleware จะทำงานก่อน Controller ครับ


---

# 5. Controller / Structure


## Q12. Backend ควรแบ่ง Folder อย่างไร?


## 🗣️ แนวตอบ

สามารถแบ่งตามหน้าที่ครับ


ตัวอย่าง
src

├── routes

├── controllers

├── models

├── middleware

├── services

└── config


ช่วยให้ Code แยกส่วนและดูแลง่ายครับ


---

## Q13. Controller ทำหน้าที่อะไร?


## 🗣️ แนวตอบ

Controller ทำหน้าที่รับ Request

เรียกใช้ Logic

ติดต่อ Database

และส่ง Response กลับไปให้ Client ครับ


---

## Q14. Service Layer คืออะไร?


## 🗣️ แนวตอบ

Service Layer เป็นส่วนที่แยก Business Logic ออกจาก Controller ครับ

ทำให้ Code เป็นระเบียบและ Test ได้ง่ายขึ้น


---

# 6. Authentication


## Q15. Authentication คืออะไร?


## 🗣️ แนวตอบ

Authentication คือการตรวจสอบว่า User เป็นใครครับ

เช่น Login ด้วย Email และ Password


---

## Q16. Authorization คืออะไร?


## 🗣️ แนวตอบ

Authorization คือการตรวจสอบสิทธิ์ของ User ครับ

เช่น


Admin สามารถจัดการสินค้าได้

Customer สามารถสั่งซื้อได้


---

## Q17. Authentication กับ Authorization ต่างกันอย่างไร?


## 🗣️ แนวตอบ

Authentication คือการยืนยันตัวตนครับ

Authorization คือการตรวจสอบสิทธิ์หลังจากยืนยันตัวตนแล้วครับ


---

# 7. JWT


## Q18. JWT คืออะไร?


## 🗣️ แนวตอบ

JWT เป็น Token ที่ใช้สำหรับยืนยันตัวตนครับ

หลังจาก Login สำเร็จ Server จะสร้าง Token

และ Client จะส่ง Token นี้กลับมาเมื่อเรียก API ที่ต้อง Login


---

## Q19. JWT มีส่วนประกอบอะไร?


## 🗣️ แนวตอบ

JWT มี 3 ส่วนครับ


Header

ข้อมูลประเภท Token


Payload

ข้อมูล User


Signature

ใช้ตรวจสอบว่า Token ถูกแก้ไขหรือไม่


---

## Q20. ทำไมไม่เก็บ Password ตรง ๆ?


## 🗣️ แนวตอบ

เพราะมีความเสี่ยงด้านความปลอดภัยครับ

ควร Hash Password เช่น bcrypt

เพื่อไม่ให้เก็บรหัสผ่านจริงใน Database


---

# 8. Error Handling


## Q21. จัดการ Error ใน Backend อย่างไร?


## 🗣️ แนวตอบ

ใช้ try-catch และ Error Middleware ครับ

เพื่อจัดการ Error จากทุกส่วนของระบบ

และส่ง Response ที่เหมาะสมกลับไป


---

## Q22. HTTP Status Code ที่ใช้บ่อย?


## 🗣️ แนวตอบ


200

Request สำเร็จ


201

สร้างข้อมูลสำเร็จ


400

ข้อมูลไม่ถูกต้อง


401

ยังไม่ได้ Login


403

ไม่มีสิทธิ์


404

ไม่พบข้อมูล


500

Server Error


---

# 9. Database Connection


## Q23. Backend ติดต่อ Database อย่างไร?


## 🗣️ แนวตอบ

Backend ใช้ Database Driver หรือ ORM ติดต่อกับ Database ครับ

เช่น

MySQL

MongoDB


แล้วนำข้อมูลมาใช้ใน Logic ของระบบ


---

## Q24. ทำไมไม่ให้ Frontend ติดต่อ Database โดยตรง?


## 🗣️ แนวตอบ

เพราะมีปัญหาด้าน Security ครับ

Backend ทำหน้าที่ควบคุม Logic

ตรวจสอบสิทธิ์

และป้องกันข้อมูลสำคัญ


---

# 10. API Security


## Q25. ป้องกัน API อย่างไร?


## 🗣️ แนวตอบ

สามารถป้องกันได้หลายวิธีครับ


- Authentication
- Authorization
- Validate Input
- Rate Limit
- HTTPS


---

## Q26. SQL Injection คืออะไร?


## 🗣️ แนวตอบ

SQL Injection คือการส่งคำสั่ง SQL ผ่าน Input เพื่อโจมตี Database ครับ

ป้องกันโดยใช้ Parameterized Query หรือ ORM


---

## Q27. CORS คืออะไร?


## 🗣️ แนวตอบ

CORS เป็นระบบควบคุมว่า Domain ไหนสามารถเรียก API ได้ครับ

ช่วยป้องกัน Request ที่ไม่ได้รับอนุญาต


---

# 11. Performance


## Q28. ถ้า API ช้าจะแก้อย่างไร?


## 🗣️ แนวตอบ

ตรวจสอบทีละส่วนครับ


- Database Query
- Network
- Logic ใน Backend


จากนั้น Optimize จุดที่ช้าที่สุด


---

## Q29. Pagination คืออะไร?


## 🗣️ แนวตอบ

Pagination คือการแบ่งข้อมูลเป็นหน้า ๆ ครับ

ไม่โหลดข้อมูลทั้งหมดครั้งเดียว

ช่วยลดเวลา Response


---

## Q30. Cache คืออะไร?


## 🗣️ แนวตอบ

Cache คือการเก็บข้อมูลที่เรียกใช้บ่อยไว้ชั่วคราวครับ

ช่วยลดการ Query Database และเพิ่มความเร็วระบบ


---

# 12. Senior Question


## Q31. ถ้ามี User 10,000 คนใช้งานพร้อมกัน?


## 🗣️ แนวตอบ

ต้องออกแบบระบบให้รองรับ Scale ครับ

เช่น

- Load Balancer
- เพิ่ม Server
- Cache
- Database Optimization


---

## Q32. ถ้า API ถูกเรียกซ้ำจำนวนมาก?


## 🗣️ แนวตอบ

สามารถใช้ Rate Limiting เพื่อจำกัดจำนวน Request

และใช้ Cache ลดภาระ Server ครับ


---

## Q33. ถ้า Database ล่ม?


## 🗣️ แนวตอบ

ระบบควรมี Error Handling

และอาจใช้ Backup Database หรือ Replication เพื่อป้องกันข้อมูลสูญหายครับ


---

## Q34. ถ้าทำ Backend ใหม่จะปรับอะไร?


## 🗣️ แนวตอบ

ผมจะวางโครงสร้าง Backend ให้ชัดเจนขึ้นครับ

แยก Controller, Service และ Database Layer

รวมถึงเพิ่ม Testing และ Logging ครับ


---

# Summary


Node.js

= JavaScript ฝั่ง Server


Express

= Framework สร้าง API


REST API

= การสื่อสาร Client ↔ Server


Middleware

= ตัวกลางก่อน Controller


JWT

= Token ยืนยันตัวตน


Authentication

= ตรวจสอบตัวตน


Authorization

= ตรวจสอบสิทธิ์


Controller

= รับ Request และส่ง Response


Service

= จัดการ Business Logic
