เริ่มขึ้นโปรเจคง่าย ๆ 

0. ลองดูก่อนว่าที่เครื่องมี node มั้ย โดยไปเช็คที่ terminal จากนั้นพิมพ์

> node -v

ถ้าขึ้น version แปลว่ามี node ละ แต่เอาชัวร์ว่าลงเวอร์ชั่น stable หรือยังก็ลงเพิ่มอีกหน่อยละกัน

> npm install -g n

> sudo n stable


1. เริ่มขึ้นโปรเจคโดยสร้าง folder เปล่า ๆ มาก่อน

> mkdir my-first-next-project

2. เข้าไปที่ folder จากนั้น initial project ก่อน

> npm init

เราก็จะได้ไฟล์ `package.json` มา

3. ลง lib ที่จำเป็นกับ nextJS

> npm install next react react-dom --save

อธิบายที่ละตัวเนาะ
next -> next js framework
react -> react js framework
react-dom -> เป็นตัวแปลง tag เป็น json เพื่อไปบอก dom node ว่า tag นี้ประกอบไปด้วยอะไรบ้าง

ต.ย.
```
<button>OK!</button>
```

จะถูกแปลงเป็น
```
{
  type: 'button',
  props: {
    className: 'button',
    children: {
      type: 'b',
      props: {
        children: 'OK!'
      }
    }
  }
}
```

4. ในไฟล์ package.json ให้ไปเพิ่ม

```
"scripts": {
  "dev": "next dev",
  "build": "next build",
  "start": "next start",
  "lint": "next lint"
}
```

ปล. ทำเล่นใช้แค่ `"dev": "next dev"` ก่อนก็ได้

5. สร้าง folder pages และสร้างไฟล์ index.js เอาไว้เป็นหน้าแรก

เราก็จะได้ project structure ประมาณนี้

```
📦 my-first-next-project
 ┣ 📂 node_modules
 ┣ 📂 pages
 ┃ ┗ 📜index.js
 ┣ 📜.gitignore
 ┣ 📜package-lock.json
 ┗ 📜package.json
```

6. ในไฟล์ index.js ลองเขียนหน้าเว็บสักหน่อยสิ

`index.js`
```
import React from "react"

const HomePage = () => (
  <div>Hello BluePi!</div>
)

export default HomePage;
```

7. เท่านี้ก็ใช้ nextJS คร่าว ๆ เป็นแล้วววววว อ่ออ กด run project ก่อนสิ 555

> npm run dev

เข้าไปดูผลงานตัวเองด้วยที่ http://localhost:3000/

ถ้าเปิดได้แปลว่า คุณอ่านได้เก่งมากก ทำตามทุกระเบียบนิ้ว สุดยอดดด

ถ้าทำไม่ได้ ทัก slack มาบอกทีผิดได้ไง 5555