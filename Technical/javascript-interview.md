# JavaScript Technical Interview Questions

Technology:

- JavaScript
- ES6+
- Frontend Development
- Backend Development


---

# 1. JavaScript Basic


## Q1. JavaScript คืออะไร?


## 🗣️ แนวตอบ

JavaScript เป็น Programming Language ที่ใช้สำหรับพัฒนาเว็บไซต์ครับ

ใช้สำหรับสร้าง Interactive บนหน้าเว็บ

และสามารถทำงานฝั่ง Backend ผ่าน Node.js ได้ครับ


---

## Q2. JavaScript ทำงานที่ไหน?


## 🗣️ แนวตอบ

JavaScript สามารถทำงานได้ทั้งฝั่ง Client และ Server ครับ

Client คือ Browser เช่น Chrome

Server คือ Node.js


---

# 2. Variable


## Q3. var, let และ const ต่างกันอย่างไร?


## 📌 จำ

var = Function Scope

let = Block Scope

const = เปลี่ยนค่าไม่ได้


## 🗣️ แนวตอบ

var เป็นรูปแบบเก่าของ JavaScript มี Scope ระดับ Function

let และ const เป็น ES6 ที่ใช้ Block Scope

โดยทั่วไปนิยมใช้ const ก่อน และใช้ let เมื่อค่ามีการเปลี่ยนแปลงครับ


---

## Q4. ทำไมควรใช้ const มากกว่า let?


## 🗣️ แนวตอบ

เพราะช่วยป้องกันการเปลี่ยนค่าของตัวแปรโดยไม่ตั้งใจครับ

ทำให้ Code อ่านง่ายและลด Error ครับ


---

# 3. Scope


## Q5. Scope คืออะไร?


## 🗣️ แนวตอบ

Scope คือขอบเขตที่ตัวแปรสามารถถูกเรียกใช้งานครับ

เช่น

Global Scope

Function Scope

Block Scope


---

## Q6. Block Scope คืออะไร?


## 🗣️ แนวตอบ

Block Scope คือขอบเขตภายใน {}

เช่น

if

for

หรือ block ของ Code ครับ


---

# 4. Hoisting


## Q7. Hoisting คืออะไร?


## 🗣️ แนวตอบ

Hoisting คือพฤติกรรมที่ JavaScript ย้ายการประกาศตัวแปรหรือ Function ขึ้นไปด้านบนก่อน Execute Code ครับ


---

## Q8. var กับ let ต่างกันเรื่อง Hoisting อย่างไร?


## 🗣️ แนวตอบ

var จะถูก Hoist และมีค่าเริ่มต้นเป็น undefined

แต่ let และ const จะอยู่ใน Temporal Dead Zone

ทำให้ไม่สามารถเรียกใช้ก่อนประกาศได้ครับ


---

# 5. Function


## Q9. Function คืออะไร?


## 🗣️ แนวตอบ

Function คือชุดคำสั่งที่ถูกสร้างไว้เพื่อทำงานบางอย่าง

สามารถเรียกใช้ซ้ำได้ ทำให้ Code ไม่ซ้ำและดูแลง่ายขึ้นครับ


---

## Q10. Arrow Function คืออะไร?


## 🗣️ แนวตอบ

Arrow Function เป็นรูปแบบการเขียน Function แบบสั้นใน ES6 ครับ

ช่วยให้ Code กระชับขึ้น และมีการจัดการ this ต่างจาก Function ปกติ


---

# 6. Callback


## Q11. Callback Function คืออะไร?


## 🗣️ แนวตอบ

Callback คือ Function ที่ถูกส่งเข้าไปเป็น Parameter ของ Function อื่น

และถูกเรียกใช้ภายหลังครับ


---

## Q12. Callback ใช้ทำอะไร?


## 🗣️ แนวตอบ

ใช้จัดการงานที่ต้องรอผลลัพธ์ครับ

เช่น

- อ่านข้อมูล
- เรียก API
- ทำงานแบบ Async


---

# 7. Promise


## Q13. Promise คืออะไร?


## 📌 จำ

Pending

Fulfilled

Rejected


## 🗣️ แนวตอบ

Promise เป็น Object ที่ใช้จัดการ Asynchronous Operation ครับ

มีสถานะ 3 แบบ

Pending คือกำลังทำงาน

Fulfilled คือสำเร็จ

Rejected คือเกิด Error


---

## Q14. ทำไมต้องใช้ Promise?


## 🗣️ แนวตอบ

เพื่อจัดการงานที่ใช้เวลา เช่น API Request

ช่วยให้ Code อ่านง่ายกว่า Callback หลายชั้นครับ


---

# 8. Async / Await


## Q15. async และ await คืออะไร?


## 🗣️ แนวตอบ

async และ await เป็น Syntax ที่ช่วยให้เขียน Promise ได้ง่ายขึ้นครับ

ทำให้ Code อ่านเหมือนการทำงานแบบปกติ


---

## Q16. async function คืนค่าอะไร?


## 🗣️ แนวตอบ

async function จะคืนค่าเป็น Promise เสมอครับ


---

## Q17. try-catch ใช้กับ async await ทำไม?


## 🗣️ แนวตอบ

ใช้สำหรับจัดการ Error ที่เกิดขึ้นระหว่างรอ Promise ครับ

ทำให้ระบบไม่หยุดทำงานเมื่อเกิดปัญหา


---

# 9. Event Loop


## Q18. Event Loop คืออะไร?


## 🗣️ แนวตอบ

Event Loop เป็นระบบที่ JavaScript ใช้จัดการงาน Asynchronous ครับ

ช่วยให้ JavaScript ทำงานแบบ Non-blocking ได้


---

## Q19. JavaScript เป็น Single Thread หมายความว่าอะไร?


## 🗣️ แนวตอบ

หมายถึง JavaScript มี Main Thread หลักในการ Execute Code เพียงหนึ่งชุดครับ

แต่สามารถจัดการงาน Async ผ่าน Browser API และ Event Loop ได้


---

# 10. Array Method


## Q20. map() ใช้ทำอะไร?


## 🗣️ แนวตอบ

map ใช้สำหรับสร้าง Array ใหม่จากข้อมูลเดิมครับ

เช่น เปลี่ยนรูปแบบข้อมูล


---

## Q21. filter() ใช้ทำอะไร?


## 🗣️ แนวตอบ

filter ใช้กรองข้อมูลตามเงื่อนไขครับ

และคืนค่า Array ใหม่ที่ผ่านเงื่อนไข


---

## Q22. reduce() ใช้ทำอะไร?


## 🗣️ แนวตอบ

reduce ใช้รวมค่าจาก Array ให้เป็นค่าเดียวครับ

เช่น

รวมยอดเงิน

นับจำนวนข้อมูล


---

## Q23. map กับ forEach ต่างกันอย่างไร?


## 🗣️ แนวตอบ

map จะคืนค่า Array ใหม่

ส่วน forEach ใช้ Loop เพื่อทำงานบางอย่าง แต่ไม่คืนค่า Array ใหม่ครับ


---

# 11. Object


## Q24. Object คืออะไร?


## 🗣️ แนวตอบ

Object คือโครงสร้างข้อมูลที่เก็บข้อมูลในรูปแบบ Key และ Value ครับ


ตัวอย่าง

```javascript
{
 name: "Ice",
 age: 20
}


Q25. Destructuring คืออะไร?
🗣️ แนวตอบ
Destructuring คือการดึงค่าจาก Object หรือ Array มาเก็บในตัวแปรแบบง่ายขึ้นครับ
12. ES6
Q26. ES6 มีอะไรใหม่?
🗣️ แนวตอบ
ES6 เพิ่มความสามารถหลายอย่างครับ เช่น
- let / const
- Arrow Function
- Template String
- Destructuring
- Promise
- Class
13. Error Handling
Q27. จัดการ Error ใน JavaScript อย่างไร?
🗣️ แนวตอบ
ใช้ try-catch สำหรับจับ Error ครับ

และสามารถใช้ Promise catch หรือ async await ร่วมกับ try-catch ได้
14. Senior Question
Q28. == กับ === ต่างกันอย่างไร?
🗣️ แนวตอบ
== เปรียบเทียบค่าโดยมีการแปลง Type

=== เปรียบเทียบทั้งค่าและ Type

โดยทั่วไปควรใช้ === เพื่อป้องกัน Error ครับ
Q29. Closure คืออะไร?
🗣️ แนวตอบ
Closure คือความสามารถของ Function ที่สามารถเข้าถึงตัวแปรจาก Scope ภายนอกได้ แม้ Function นั้นจะถูกเรียกใช้งานภายหลังครับ
Q30. JavaScript Memory Management ทำอย่างไร?
🗣️ แนวตอบ
JavaScript มี Garbage Collector ที่จัดการคืน Memory ของ Object ที่ไม่ได้ถูกใช้งานแล้วครับ
Summary
var

= Function Scope

let

= เปลี่ยนค่าได้ + Block Scope

const

= ค่าไม่เปลี่ยน + Block Scope

Promise

= จัดการ Async

async/await

= เขียน Promise ให้อ่านง่าย

Event Loop

= จัดการงาน Async

map

= แปลง Array

filter

= กรองข้อมูล

reduce

= รวมข้อมูล

Closure

= Function จำ Scope ภายนอก
