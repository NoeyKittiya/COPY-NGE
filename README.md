# COPY-NGE
" ของเก่าจากไป จะเอาอะไรมาเร่งความเร็ว "

##### โปรเจคนี้เป็นโปรเจค React โปรดติดตั้ง Node js และลง React ให้เรียบร้อย

##### วิธีการรัน

1. โคลน
2. npm install
3. ไปที่โฟลเดอร์ src จะมีไฟล์ชื่อ prop.json ใส่ข้อมูลให้เรียบร้อย
4. npm start

##### ข้างใน prop.json จะมีสองตัวคือ

- Token ( ล็อคอินเข้าเว็บ OLIV แล้วเข้าไปเอา Token จาก Session Stroage ได้เลย ) 
```
** หากใครไปไม่เป็น ให้เข้าเว็บ OLIV ล็อคอินให้เรียบร้อย กด F12 แล้วไปหน้า Console แล้วก็อปคำสั่งข้างล่างนี้ไปรัน

console.log(window.sessionStorage.token) //Khor-Token-Nhoy-Kaaaaaaaaaa-saaa-tuuu

แล้วพระท่านจะเสก Token มาให้ ให้นำไปใส่ใน prop.json
```
- Subject ( เป็นลิงค์ API ดึงคลิปจาก OLIV หากต้องการเปลี่ยนแปลงวิชาต้องเปลี่ยนจากลิงค์นั้น ซึ่งตอนนี้แปะไว้แค่ลิงค์เดียว เพราะสอบแค่ 401 ตัวเดียว )
```
หากต้องการเปลี่ยนวิชา ให้ใส่รหัสวิชาที่ subject_id โดยรูปแบบเป็นแบบนี้

"https://learning.sit.kmutt.ac.th/api/videos/list?academic_year=2562&all=true&semester=1&semester_id=16&subject_id=ใส่รหัสวิชาตรงนี้&type=class_record"

เช่น วิชา INT401 มีรหัสเป็น 189 ก็ต้องใส่แบบนี้..

"https://learning.sit.kmutt.ac.th/api/videos/list?academic_year=2562&all=true&semester=1&semester_id=16&subject_id=189&type=class_record"

และต่อจากนี้คือเลขรหัสของแต่ละวิชา (ให้ใช้เลขหน้า = นะครับ)

"156 = INT101"
"153 = INT102"
"154 = INT103"
"157 = INT105-G1"
"496 = INT105-G2"
"158 = INT106"
"159 = INT107"
"629 = INT114-G1"
"630 = INT114-G2"
"160 = INT201"
"161 = INT202"
"162 = INT203"
"166 = INT204"
"164 = INT205"
"163 = INT206"
"515 = INT207"
"167 = INT301"
"168 = INT302"
"169 = INT303"
"170 = INT304"
"171 = INT305"
"174 = INT306"
"175 = INT307"
"708 = INT320"
"172 = INT351-G1-2"
"176 = INT352"
"649 = INT353/INT450"
"542 = INT370"
"193 = INT373"
"512 = INT374"
"538 = INT380"
"181 = INT381"
"180 = INT382"
"536 = INT383"
"535 = INT397"
"189 = INT401"
"188 = INT402-G1"
"648 = INT402-G2"
"183 = INT450"
"186 = INT451-G1-2"
"177 = INT467"
"178 = INT470"
"468 = INT473"
"179 = INT474"
"615 = INT491"
"650 = INT491"
"718 = INT491/ CSC493"
"619 = INT492"
"624 = INT492"
"665 = INT492"
"717 = INT493"
"553 = INT494"
"623 = INT494"
"627 = INT494"
"529 = INT494-1"
"519 = INT494-2"
"554 = INT495"
"182 = INT495"
"190 = INT496"
"620 = INT497"
"626 = INT497"
"548 = INT497-1"

```
** หากต้องการวิชาเพิ่มเติม เปิด Issue ไว้ครับ


### แจ้งให้ทราบ

- ระบบนี้ขอสงวนสิทธิ์ให้ผู้ที่มี Account OLIV และมีสิทธิ์ใช้งาน OLIV ใช้งานเท่านั้น
- หากท่านใดนำโค้ดไปปล่อยต่อ แล้วดันลืมลบ Token ออกจาก prop.json ความซวยนั้นจะเกิดขึ้นกับท่าน เปรียบเสมือนท่านมอบบัตรนักศึกษาให้โจรติ้กเข้าคณะมาขโมยของ
- ไม่ได้มีเจตทำเป็นช่องทางหาเงิน เพียงแต่เป็นการแก้ปัญหาเฉพาะการ
- ไม่มีการแอบเก็บข้อมูลใดๆทั้งสิ้น
- พัฒนาและลองใช้แต่บน Window 555555555555555555 MacOS อาจมีปัญหานิดหน่อย แต่แจ้งมาได้ครับ เดี๋ยวปรับโค้ดให้
- เพื่อนๆสามารถนำไปพัฒนาต่อได้ แต่ควรจะนึกถึงความปลอดภัยของระบบ OLIV เป็นหลัก

### ปัญหาที่ทราบ
- Chrome เวลาเปลี่ยนแท็บ ตัวคลิปจะหยุดเล่นเอง
- Responsive ยังไม่สมบูรณ์ที่สุด

<hr/>


หากพบปัญหาหรือต้องการอะไรเพิ่มเติม ท่านสามารถเปิด Issue ไว้ได้เลยครับ จะตอบกลับให้เร็วที่สุด
