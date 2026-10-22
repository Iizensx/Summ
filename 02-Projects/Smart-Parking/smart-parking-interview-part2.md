# Smart Parking Interview Note (Part 2)

หัวข้อ:

- Database Design
- Booking Logic
- QR Flow
- Payment Flow
- Security
- Performance
- Testing
- Deployment
- Senior Question


---

# 5. Database Design


## Q21. ออกแบบ Database ของระบบอย่างไร?


## 🎯 ผู้สัมภาษณ์ต้องการรู้

- เข้าใจการเก็บข้อมูลหรือไม่
- สามารถออกแบบความสัมพันธ์ของข้อมูลได้หรือไม่


## 📌 จำ

Entity หลัก:

- User
- Vehicle
- Parking
- Parking Slot
- Booking
- Payment


## 🗣️ แนวตอบ

ผมออกแบบ Database โดยดูจากข้อมูลหลักของระบบครับ

เช่น User สำหรับเก็บข้อมูลผู้ใช้งาน

Vehicle สำหรับเก็บข้อมูลรถ

Parking และ Parking Slot สำหรับเก็บข้อมูลลานจอดและช่องจอด

Booking สำหรับเก็บข้อมูลการจอง

และ Payment สำหรับเก็บข้อมูลการชำระเงินครับ


---

## Q22. ความสัมพันธ์ของ Table เป็นอย่างไร?


## 🗣️ แนวตอบ

ตัวอย่างความสัมพันธ์ครับ

User 1 คน สามารถมี Vehicle ได้หลายคัน

Vehicle สามารถมี Booking ได้หลายรายการ

Parking 1 แห่ง มี Parking Slot หลายช่อง

Booking จะเชื่อมกับ User, Vehicle และ Parking Slot เพื่อรู้ว่าใครจองช่องไหนครับ


ตัวอย่าง:

```
User

1

|

Many

Vehicle

|

Many

Booking

|

1

Parking Slot
```


---

## Q23. Primary Key คืออะไร?


## 📌 จำ

ระบุข้อมูลไม่ซ้ำ


## 🗣️ แนวตอบ

Primary Key คือ Column ที่ใช้ระบุข้อมูลแต่ละ Record ใน Table แบบไม่ซ้ำกันครับ

เช่น User_ID หรือ Booking_ID

เพื่อให้สามารถอ้างอิงข้อมูลแต่ละรายการได้อย่างถูกต้องครับ


---

## Q24. Foreign Key คืออะไร?


## 🗣️ แนวตอบ

Foreign Key คือ Column ที่ใช้เชื่อมความสัมพันธ์ระหว่าง Table ครับ

เช่น Booking Table จะมี User_ID เพื่อบอกว่า Booking นี้เป็นของ User คนไหนครับ


---

## Q25. ทำไมต้องใช้ Database แบบ Relation?


## 🗣️ แนวตอบ

เนื่องจากข้อมูลของระบบมีความสัมพันธ์กันชัดเจนครับ

เช่น User, รถ, การจอง และการชำระเงิน

จึงเหมาะกับ Relational Database ที่สามารถใช้ Table และ Relationship จัดการข้อมูลได้ครับ


---

# 6. Booking Logic


## Q26. ระบบจองที่จอดรถทำงานอย่างไร?


## 🎯 ต้องการรู้

เข้าใจ Business Logic หรือไม่


## 📌 จำ

Check → Reserve → Confirm


## 🗣️ แนวตอบ

เมื่อ User เลือกช่องจอด ระบบจะตรวจสอบสถานะของช่องจอดก่อนครับ

ถ้ายังว่าง ระบบจะสร้าง Booking และเปลี่ยนสถานะเป็น Reserved

เมื่อผู้ใช้เข้าใช้งานจริง ระบบจะเปลี่ยนเป็น Occupied ครับ


Flow:

```
Available

↓

Reserved

↓

Occupied

↓

Available
```


---

## Q27. ป้องกันการจองช่องเดียวกันพร้อมกันอย่างไร?


## 🎯 Senior Question


## 🗣️ แนวตอบ

ผมจะป้องกันที่ Backend เป็นหลักครับ

เพราะ Frontend ไม่สามารถป้องกันได้ทั้งหมด

โดยก่อนบันทึก Booking จะตรวจสอบสถานะล่าสุดของช่องจอด

และใช้ Transaction หรือ Database Constraint เพื่อป้องกันข้อมูลซ้ำครับ


---

## Q28. ถ้าผู้ใช้กดจองพร้อมกัน 2 คน?


## 🗣️ แนวตอบ

ระบบต้องมีการ Lock หรือ Transaction ครับ

เพื่อให้มีเพียง Request เดียวที่สามารถเปลี่ยนสถานะช่องจอดได้

ส่วน Request อื่นจะได้รับ Response ว่าช่องนี้ถูกจองแล้วครับ


---

## Q29. ถ้าจองแล้วผู้ใช้ไม่มา?


## 🗣️ แนวตอบ

สามารถกำหนดเวลาหมดอายุของ Booking ได้ครับ

เช่น ถ้าเกินเวลาที่กำหนด ระบบจะเปลี่ยนสถานะกลับเป็น Available

เพื่อให้คนอื่นสามารถใช้งานได้ครับ


---

# 7. QR Code Flow


## Q30. QR Code ใช้ทำอะไร?


## 🗣️ แนวตอบ

QR Code ใช้สำหรับยืนยันการเข้าใช้งานครับ

หลังจาก User ทำการจอง ระบบจะสร้าง QR ที่เชื่อมกับข้อมูล Booking

เมื่อ Scan ระบบจะตรวจสอบข้อมูลก่อนอนุญาตให้เข้าใช้งานครับ


---

## Q31. QR Code ทำงานอย่างไร?


## 📌 จำ

Generate → Scan → Validate


## 🗣️ แนวตอบ

เมื่อ Booking สำเร็จ Backend จะสร้างข้อมูล QR Code

เมื่อ User Scan ระบบจะส่งข้อมูลไปตรวจสอบกับ Backend

Backend จะตรวจสอบว่า QR ถูกต้องหรือไม่ และ Booking ยัง Active หรือไม่ครับ


---

## Q32. ป้องกัน QR ปลอมอย่างไร?


## 🗣️ แนวตอบ

ไม่ควรเก็บข้อมูลสำคัญไว้ใน QR โดยตรงครับ

ควรใช้ Token หรือ ID ที่ Backend สามารถตรวจสอบได้

เมื่อ Scan แล้วต้อง Validate กับ Database ทุกครั้งครับ


---

# 8. Payment Flow


## Q33. ระบบชำระเงินทำงานอย่างไร?


## 🗣️ แนวตอบ

หลังจาก User ใช้งานเสร็จ ระบบจะคำนวณค่าบริการจากข้อมูล Booking เช่น ระยะเวลาใช้งาน

จากนั้นสร้าง Payment Transaction และบันทึกสถานะการชำระเงินครับ


---

## Q34. Payment Status มีอะไรบ้าง?


## 📌 จำ

Pending

↓

Success

↓

Failed


## 🗣️ แนวตอบ

โดยทั่วไป Payment จะมีหลายสถานะครับ

เช่น

Pending คือรอการชำระ

Success คือชำระสำเร็จ

Failed คือชำระไม่สำเร็จ

เพื่อให้ระบบสามารถติดตามสถานะได้ครับ


---

# 9. Security


## Q35. เก็บ Password อย่างไร?


## 🗣️ แนวตอบ

ไม่ควรเก็บ Password แบบ Plain Text ครับ

ควร Hash Password ก่อนบันทึกลง Database เช่น bcrypt

เวลาตรวจสอบจะนำ Password ที่ User ส่งมา Hash แล้วเปรียบเทียบครับ


---

## Q36. SQL Injection คืออะไร?


## 🗣️ แนวตอบ

SQL Injection คือการที่ผู้ไม่หวังดีส่งคำสั่ง SQL ผ่าน Input เพื่อเข้าถึงหรือแก้ไขข้อมูลครับ

วิธีป้องกันคือใช้ Parameterized Query หรือ ORM และตรวจสอบข้อมูล Input ครับ


---

## Q37. Authentication กับ Authorization ต่างกันอย่างไร?


## 🗣️ แนวตอบ

Authentication คือการตรวจสอบว่า User เป็นใคร เช่น Login

Authorization คือการตรวจสอบว่า User มีสิทธิ์ทำอะไรได้บ้างครับ

เช่น Admin สามารถจัดการข้อมูล แต่ User ทั่วไปไม่สามารถทำได้


---

# 10. Performance


## Q38. ถ้า API ช้าจะตรวจสอบอย่างไร?


## 🗣️ แนวตอบ

ผมจะตรวจสอบเป็นขั้นตอนครับ

เริ่มจากดูว่าเกิดจาก Frontend, Network, Backend Logic หรือ Database

จากนั้นใช้ Log หรือ Monitoring เพื่อหาจุดที่ใช้เวลานานที่สุดแล้วแก้ไขครับ


---

## Q39. ถ้า Database มีข้อมูลเยอะขึ้น?


## 🗣️ แนวตอบ

สามารถปรับปรุงได้หลายวิธีครับ

เช่น

- เพิ่ม Index
- ปรับ Query
- ใช้ Pagination
- ทำ Cache

เพื่อช่วยลดเวลาการค้นหาข้อมูลครับ


---

## Q40. Index คืออะไร?


## 🗣️ แนวตอบ

Index คือโครงสร้างข้อมูลที่ช่วยให้ Database ค้นหาข้อมูลได้เร็วขึ้นครับ

เหมือนดัชนีในหนังสือ

แต่ข้อเสียคือใช้พื้นที่เพิ่ม และทำให้ Insert หรือ Update ช้าลงเล็กน้อยครับ


---

# 11. Testing


## Q41. ทดสอบระบบอย่างไร?


## 🗣️ แนวตอบ

ผมทดสอบหลายระดับครับ

Frontend ทดสอบการแสดงผลและ User Flow

Backend ทดสอบ API ด้วย Postman

Database ตรวจสอบว่าข้อมูลถูกบันทึกและสัมพันธ์ถูกต้องครับ


---

## Q42. เคย Debug Bug อย่างไร?


## 🗣️ แนวตอบ

ผมจะเริ่มจากดู Error Message ก่อนครับ

จากนั้นแยกว่าปัญหาเกิดจากส่วนไหน

เช่น Frontend, API หรือ Database

แล้วใช้ Console, Log หรือ Postman ช่วยตรวจสอบครับ


---

# 12. Deployment


## Q43. เคย Deploy ระบบไหม?


## 🗣️ แนวตอบ

ถ้า Deploy แล้ว:

ผมทำการ Deploy Frontend และ Backend แยกกันครับ

โดยตั้งค่า Environment Variable และเชื่อมต่อ Database ตาม Environment


ถ้ายังไม่ได้ Deploy:

ผมเข้าใจกระบวนการครับ เช่น Build Frontend, Deploy Backend Server และตั้งค่า Database Connection


---

# Q44. ถ้าระบบมีผู้ใช้จำนวนมากขึ้นจะปรับอย่างไร?


## 🗣️ แนวตอบ

ผมจะเริ่มจากดูจุดที่เป็น Bottleneck ก่อนครับ

เช่น Database, API หรือ Server

จากนั้นอาจเพิ่ม Cache, Load Balance, Database Optimization หรือแยกระบบเป็น Service มากขึ้นครับ


---

# Q45. ถ้าทำใหม่จะปรับปรุงอะไร?


## 🗣️ แนวตอบ

ถ้าทำใหม่ ผมจะวาง Architecture และ Database Design ให้ชัดเจนตั้งแต่ต้นครับ

รวมถึงเพิ่ม Automated Testing, Logging และจัดการ Error ให้เป็นระบบมากขึ้นครับ


---

# Summary Smart Parking

สิ่งที่ควรจำ:

- React = UI และ Component
- Node.js = API และ Business Logic
- Database = เก็บข้อมูลและ Relationship
- JWT = Authentication
- Transaction = ป้องกันข้อมูลผิดพลาด
- Validation = Frontend + Backend
- Security = ป้องกันข้อมูลและสิทธิ์ผู้ใช้
