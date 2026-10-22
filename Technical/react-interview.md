# React Technical Interview Questions

Technology:

- React.js
- JavaScript
- Frontend Development


---

# 1. React Basic


## Q1. React คืออะไร?


## 🗣️ แนวตอบ

React เป็น JavaScript Library สำหรับสร้าง User Interface ครับ

นิยมใช้สร้าง Web Application แบบ Component

ช่วยให้พัฒนา UI ที่ซับซ้อนและนำกลับมาใช้ซ้ำได้ง่ายครับ


---

## Q2. ทำไมเลือกใช้ React?


## 📌 จำ

Component

Reusable

Maintain


## 🗣️ แนวตอบ

เลือกใช้ React เพราะสามารถแบ่ง UI เป็น Component ได้ครับ

ทำให้ Code แยกเป็นส่วน

นำกลับมาใช้ซ้ำได้

และดูแลระบบขนาดใหญ่ได้ง่ายขึ้นครับ


---

# 2. Component


## Q3. Component คืออะไร?


## 🗣️ แนวตอบ

Component คือส่วนประกอบย่อยของหน้าเว็บไซต์ครับ

เช่น

- Navbar
- Button
- Card
- Form

แต่ละ Component สามารถมี Logic และ UI ของตัวเองได้ครับ


---

## Q4. Functional Component คืออะไร?


## 🗣️ แนวตอบ

Functional Component คือ Component ที่สร้างด้วย Function ของ JavaScript ครับ

ปัจจุบันนิยมใช้ร่วมกับ Hooks เช่น useState และ useEffect


---

## Q5. ทำไมต้องแยก Component?


## 🗣️ แนวตอบ

เพื่อให้ Code เป็นระเบียบครับ

แก้ไขง่าย

นำกลับมาใช้ซ้ำได้

และลด Code ที่ซ้ำกันครับ


---

# 3. Props


## Q6. Props คืออะไร?


## 📌 จำ

Parent → Child


## 🗣️ แนวตอบ

Props คือข้อมูลที่ส่งจาก Component แม่ไปยัง Component ลูกครับ

ใช้สำหรับส่งค่า หรือ Function ให้ Component อื่นใช้งานครับ


---

## Q7. Props กับ State ต่างกันอย่างไร?


## 🗣️ แนวตอบ

Props เป็นข้อมูลที่ได้รับมาจาก Component อื่น และไม่ควรถูกแก้ไขโดย Component ลูกครับ

State เป็นข้อมูลภายใน Component ที่สามารถเปลี่ยนแปลงได้ครับ


---

# 4. State


## Q8. State คืออะไร?


## 🗣️ แนวตอบ

State คือข้อมูลภายใน Component ที่สามารถเปลี่ยนแปลงได้ครับ

เมื่อ State เปลี่ยน React จะทำการ Render UI ใหม่


---

## Q9. ใช้ State จัดการอะไร?


## 🗣️ แนวตอบ

ตัวอย่างเช่น

- ข้อมูล User
- Form Input
- Loading Status
- ข้อมูลจาก API
- สถานะ Modal


---

## Q10. ทำไมไม่ใช้ตัวแปรปกติแทน State?


## 🗣️ แนวตอบ

เพราะตัวแปรปกติเมื่อเปลี่ยนค่า React จะไม่รู้และไม่ Render ใหม่ครับ

แต่ State ถูก React ติดตามและ Update UI ให้อัตโนมัติ


---

# 5. React Hooks


## Q11. Hook คืออะไร?


## 🗣️ แนวตอบ

Hook คือ Function ที่ช่วยให้ Functional Component สามารถใช้ความสามารถของ React ได้ครับ

เช่น

- State
- Lifecycle
- Context


---

## Q12. useState ใช้ทำอะไร?


## 🗣️ แนวตอบ

useState ใช้สำหรับสร้างและจัดการ State ใน Functional Component ครับ


ตัวอย่าง:

```javascript
const [count, setCount] = useState(0)

Q13. useEffect ใช้ทำอะไร?
📌 จำ
Side Effect
🗣️ แนวตอบ
useEffect ใช้จัดการงานที่เกิดขึ้นหลัง Component Render ครับ

เช่น
- เรียก API
- โหลดข้อมูล
- จัดการ Event
Q14. Dependency Array ใน useEffect คืออะไร?
🗣️ แนวตอบ
เป็นตัวกำหนดว่า useEffect จะทำงานเมื่อไหร่ครับ

ตัวอย่าง:
useEffect(() => {

}, [])

ถ้า Array ว่าง จะทำงานครั้งเดียวตอน Component โหลด
Q15. ถ้าไม่ใส่ Dependency Array จะเกิดอะไรขึ้น?
🗣️ แนวตอบ
useEffect จะทำงานทุกครั้งหลัง Component Render ครับ

อาจทำให้เกิดปัญหา Loop หรือ Performance ลดลง
6. React Router
Q16. React Router คืออะไร?
🗣️ แนวตอบ
React Router เป็น Library สำหรับจัดการ Navigation ใน React ครับ

ช่วยเปลี่ยนหน้าโดยไม่ต้อง Reload เว็บไซต์ใหม่
Q17. Protected Route คืออะไร?
🗣️ แนวตอบ
Protected Route คือการจำกัดการเข้าถึงหน้าเว็บครับ

เช่น

ถ้า User ยังไม่ Login

จะไม่สามารถเข้า Dashboard ได้
7. API Connection
Q18. React ติดต่อ Backend อย่างไร?
🗣️ แนวตอบ
React ส่ง HTTP Request ไปยัง Backend API ครับ

โดยใช้ Fetch หรือ Axios

จากนั้นนำ Response มาเก็บใน State และแสดงผล
Q19. Loading และ Error Handling ทำอย่างไร?
🗣️ แนวตอบ
สร้าง State สำหรับจัดการสถานะครับ

เช่น
- loading = กำลังโหลด
- error = เกิดปัญหา
- data = ข้อมูลที่ได้รับ
8. Context API
Q20. Context API คืออะไร?
🗣️ แนวตอบ
Context API ใช้สำหรับแชร์ข้อมูลระหว่าง Component โดยไม่ต้องส่ง Props หลายระดับครับ

เช่น
- User Login
- Theme
- Language
Q21. Context API ต่างจาก Props อย่างไร?
🗣️ แนวตอบ
Props ใช้ส่งข้อมูลระหว่าง Parent กับ Child โดยตรงครับ

Context ใช้แชร์ข้อมูลให้ Component หลายตัวโดยไม่ต้องส่งผ่านทุกระดับ
9. Performance
Q22. React Render ใหม่เมื่อไหร่?
🗣️ แนวตอบ
React จะ Render ใหม่เมื่อ State หรือ Props มีการเปลี่ยนแปลงครับ
Q23. useMemo ใช้ทำอะไร?
🗣️ แนวตอบ
useMemo ใช้เก็บผลลัพธ์ของการคำนวณที่หนักครับ

ช่วยลดการคำนวณซ้ำเมื่อ Component Render ใหม่
Q24. useCallback ใช้ทำอะไร?
🗣️ แนวตอบ
useCallback ใช้จดจำ Function ครับ

ช่วยลดการสร้าง Function ใหม่ทุกครั้งที่ Render
Q25. ทำไม React ถึงเร็ว?
🗣️ แนวตอบ
React ใช้ Virtual DOM ครับ

เมื่อข้อมูลเปลี่ยน React จะเปรียบเทียบความแตกต่าง

แล้ว Update เฉพาะส่วนที่จำเป็น
10. Form Handling
Q26. Controlled Component คืออะไร?
🗣️ แนวตอบ
Controlled Component คือ Form ที่ React เป็นผู้ควบคุมค่า Input ผ่าน State ครับ
Q27. Validation ใน React ทำอย่างไร?
🗣️ แนวตอบ
ตรวจสอบข้อมูลก่อนส่ง Backend ครับ

เช่น
- Required Field
- รูปแบบ Email
- ความยาว Password
แต่ Backend ต้องตรวจสอบซ้ำเพื่อความปลอดภัย
11. Senior Question
Q28. ถ้า Component ใหญ่เกินไปแก้อย่างไร?
🗣️ แนวตอบ
แยก Component ให้เล็กลงครับ

แยก Logic ออกเป็น Custom Hook

และจัดโครงสร้าง Folder ให้ชัดเจน
Q29. ถ้า React Application ช้าจะแก้อย่างไร?
🗣️ แนวตอบ
ตรวจสอบ Performance ครับ

เช่น
- ลดการ Render ที่ไม่จำเป็น
- ใช้ Memoization
- Lazy Loading
- Optimize API
Q30. ถ้าทำ React ใหม่จะปรับอะไร?
🗣️ แนวตอบ
ผมจะออกแบบ Component Structure ให้ชัดเจนตั้งแต่ต้นครับ

จัดการ State ให้เหมาะสม

และเพิ่ม Testing เพื่อให้ระบบ Maintain ง่ายขึ้นครับ
Summary
React

= UI Library

Component

= ส่วนประกอบของ UI

Props

= ส่งข้อมูล Parent → Child

State

= ข้อมูลที่เปลี่ยนแปลงได้

Hook

= เพิ่มความสามารถให้ Functional Component

useState

= จัดการ State

useEffect

= จัดการ Side Effect

Context

= แชร์ข้อมูลระหว่าง Component

Virtual DOM

= เพิ่ม Performance
