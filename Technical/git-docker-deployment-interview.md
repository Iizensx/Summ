# Git Docker Deployment Technical Interview Questions

Technology:

- Git
- Docker
- CI/CD
- Deployment
- DevOps Basic


---

# 1. Git Basic


## Q1. Git คืออะไร?


## 🗣️ แนวตอบ

Git เป็น Version Control System ครับ

ใช้สำหรับจัดการประวัติการเปลี่ยนแปลงของ Code

ช่วยให้ทีมสามารถทำงานร่วมกันและย้อนกลับ Code ได้ครับ


---

## Q2. ทำไมต้องใช้ Git?


## 🗣️ แนวตอบ

เพราะการพัฒนา Software มีหลายคนแก้ไข Code พร้อมกันครับ

Git ช่วยจัดการ Version

ติดตามการเปลี่ยนแปลง

และช่วยทำงานร่วมกันในทีมครับ


---

# 2. Repository


## Q3. Repository คืออะไร?


## 🗣️ แนวตอบ

Repository คือพื้นที่เก็บ Source Code และประวัติการเปลี่ยนแปลงของ Project ครับ


มีทั้ง

- Local Repository
- Remote Repository


---

## Q4. Local กับ Remote Repository ต่างกันอย่างไร?


## 🗣️ แนวตอบ

Local Repository คือ Repository ที่อยู่ในเครื่องของ Developer ครับ

Remote Repository คือ Repository ที่อยู่บน Server เช่น GitHub เพื่อให้ทีมเข้าถึงร่วมกัน


---

# 3. Git Command


## Q5. git clone คืออะไร?


## 🗣️ แนวตอบ

ใช้สำหรับ Copy Repository จาก Remote Server มายังเครื่องของเรา

เช่น Download Project จาก GitHub มาทำงานครับ


---

## Q6. git add คืออะไร?


## 🗣️ แนวตอบ

ใช้เตรียมไฟล์ที่ต้องการบันทึกเข้า Version Control ครับ


---

## Q7. git commit คืออะไร?


## 🗣️ แนวตอบ

Commit คือการบันทึกการเปลี่ยนแปลงของ Code พร้อม Message อธิบายสิ่งที่ทำครับ


ตัวอย่าง
git commit -m "add booking feature"



---

## Q8. git push คืออะไร?


## 🗣️ แนวตอบ

ใช้ส่ง Commit จากเครื่องของเราไปยัง Remote Repository ครับ


---

## Q9. git pull คืออะไร?


## 🗣️ แนวตอบ

ใช้ดึง Code ล่าสุดจาก Remote Repository มารวมกับเครื่องของเราครับ


---

# 4. Branch


## Q10. Branch คืออะไร?


## 📌 จำ

แยกงาน


## 🗣️ แนวตอบ

Branch คือเส้นทางการพัฒนา Code แยกออกจาก Main Branch ครับ

ช่วยให้ Developer ทำ Feature ใหม่โดยไม่กระทบ Code หลัก


---

## Q11. ทำไมต้องใช้ Branch?


## 🗣️ แนวตอบ

เพื่อให้แต่ละคนสามารถพัฒนา Feature ของตัวเองได้ครับ

เมื่อเสร็จแล้วค่อย Merge เข้าหา Main Branch


---

## Q12. ตัวอย่าง Branch ในทีม?


## 🗣️ แนวตอบ

เช่น
main

develop

feature/login

feature/booking


แต่ละ Feature ทำใน Branch ของตัวเองครับ


---

# 5. Merge


## Q13. Merge คืออะไร?


## 🗣️ แนวตอบ

Merge คือการรวม Code จาก Branch หนึ่งเข้ากับอีก Branch หนึ่งครับ


---

## Q14. Merge Conflict คืออะไร?


## 🗣️ แนวตอบ

Merge Conflict เกิดเมื่อ Git ไม่สามารถรวม Code ได้อัตโนมัติครับ

เช่น

มีหลายคนแก้ไข Code ส่วนเดียวกัน


---

## Q15. แก้ Merge Conflict อย่างไร?


## 🗣️ แนวตอบ

ตรวจสอบ Code ทั้งสองฝั่งครับ

เลือก Logic ที่ถูกต้อง

จากนั้น Commit ใหม่เพื่อรวม Code


---

# 6. Pull Request


## Q16. Pull Request คืออะไร?


## 🗣️ แนวตอบ

Pull Request คือการขอให้ทีมตรวจสอบ Code ก่อน Merge เข้า Main Branch ครับ


---

## Q17. ทำไมต้อง Review Code?


## 🗣️ แนวตอบ

เพื่อช่วยตรวจสอบคุณภาพ Code

ลด Bug

และทำให้ Code ของทีมมีมาตรฐานเดียวกันครับ


---

# 7. Docker Basic


## Q18. Docker คืออะไร?


## 🗣️ แนวตอบ

Docker เป็น Tool สำหรับสร้าง Container ครับ

ช่วยให้ Application ทำงานเหมือนกันในทุก Environment


---

## Q19. Container คืออะไร?


## 🗣️ แนวตอบ

Container คือ Environment ขนาดเล็กที่รวม Application และ Dependency ที่จำเป็นไว้ด้วยกันครับ


---

## Q20. Docker Image คืออะไร?


## 🗣️ แนวตอบ

Image คือ Template ที่ใช้สร้าง Container ครับ

ประกอบด้วย

- Application Code
- Runtime
- Library
- Configuration


---

## Q21. Container กับ Image ต่างกันอย่างไร?


## 🗣️ แนวตอบ


Image

= ตัวต้นแบบ


Container

= Instance ที่ถูกสร้างจาก Image


---

# 8. Dockerfile


## Q22. Dockerfile คืออะไร?


## 🗣️ แนวตอบ

Dockerfile คือไฟล์ที่ใช้กำหนดขั้นตอนการสร้าง Docker Image ครับ


เช่น

- ใช้ Base Image อะไร
- Install Package
- Copy Code
- Run Application


---

## Q23. Docker Compose คืออะไร?


## 🗣️ แนวตอบ

Docker Compose ใช้สำหรับจัดการหลาย Container พร้อมกันครับ


เช่น

Frontend

Backend

Database


สามารถ Start ทั้งระบบด้วยคำสั่งเดียว


---

# 9. Environment


## Q24. Environment Variable คืออะไร?


## 🗣️ แนวตอบ

Environment Variable คือค่าการตั้งค่าที่แยกออกจาก Code ครับ


เช่น

- Database URL
- API Key
- Secret Key


---

## Q25. ทำไมไม่เขียน Password Database ใน Code?


## 🗣️ แนวตอบ

เพราะเป็นข้อมูลสำคัญครับ

ถ้า Code ถูกเผยแพร่จะเกิดปัญหาด้าน Security

จึงควรเก็บใน Environment Variable


---

# 10. Deployment


## Q26. Deployment คืออะไร?


## 🗣️ แนวตอบ

Deployment คือกระบวนการนำ Application จาก Development ไปใช้งานจริงบน Server ครับ


---

## Q27. ขั้นตอน Deploy ทั่วไป?


## 🗣️ แนวตอบ


ตัวอย่าง Flow:

Developer

↓

Git Push

↓

Build Application

↓

Deploy Server

↓

User ใช้งาน


---

# 11. CI/CD


## Q28. CI/CD คืออะไร?


## 🗣️ แนวตอบ

CI/CD คือกระบวนการทำให้การ Build Test และ Deploy เป็นอัตโนมัติครับ


CI

= Continuous Integration

รวม Code และ Test อัตโนมัติ


CD

= Continuous Deployment

Deploy ระบบอัตโนมัติ


---

## Q29. ประโยชน์ของ CI/CD?


## 🗣️ แนวตอบ

ช่วยลดงาน Manual

ลดข้อผิดพลาด

และทำให้ส่ง Software ได้เร็วขึ้นครับ


---

# 12. Production Question


## Q30. ถ้า Deploy แล้วระบบ Error ทำอย่างไร?


## 🗣️ แนวตอบ

ตรวจสอบ Log ก่อนครับ

ดูว่า Error เกิดจากส่วนไหน

เช่น

- Code
- Database
- Configuration


จากนั้นแก้ไขและ Deploy ใหม่


---

## Q31. ถ้า Version ใหม่มี Bug ทำอย่างไร?


## 🗣️ แนวตอบ

สามารถ Rollback กลับ Version ก่อนหน้าได้ครับ

เพื่อให้ระบบกลับมาใช้งานได้ก่อน


---

## Q32. ทำไม Development กับ Production ถึงมีปัญหาต่างกัน?


## 🗣️ แนวตอบ

เพราะ Environment ไม่เหมือนกันครับ

เช่น

- Version ของ Library
- Configuration
- Database


Docker ช่วยลดปัญหานี้ได้


---

# 13. Senior Question


## Q33. ถ้ามี User จำนวนมาก ระบบต้องปรับอย่างไร?


## 🗣️ แนวตอบ

สามารถ Scale ระบบได้ครับ


เช่น

- เพิ่ม Server
- Load Balancer
- Cache
- Database Optimization


---

## Q34. ถ้า Server Down ทำอย่างไร?


## 🗣️ แนวตอบ

ต้องมี Monitoring และ Backup ครับ

รวมถึงเตรียมระบบสำรองเพื่อให้ Service กลับมาเร็วที่สุด


---

## Q35. ถ้าทำ Deployment ใหม่จะปรับอะไร?


## 🗣️ แนวตอบ

ผมจะเพิ่ม Automation มากขึ้นครับ

เช่น

- CI/CD Pipeline
- Automated Testing
- Monitoring


เพื่อให้ Deploy ได้ปลอดภัยขึ้น


---

# Summary


Git

= จัดการ Version Code


Branch

= แยกงาน


Merge

= รวม Code


Conflict

= Code ชนกัน


Docker

= ทำ Environment ให้เหมือนกัน


Image

= Template


Container

= Application ที่กำลัง Run


CI/CD

= Build Test Deploy อัตโนมัติ
