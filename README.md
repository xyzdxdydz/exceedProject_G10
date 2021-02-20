# exceedProject_G10
The topic is "IOT for new normal" so our group decides to do a water dispenser. this idea based on the "contactless" concept 

### HARDWARE

### BACKEND
In the backend part, we use the Flask framework to manage the Raspberry pi based server. the server gets a response from hardware(esp32 microcontroller), it will be calculating water left, time interval, and the usage statistic in a time interval and update data to MongoDB database the frontend will fetching the data through "/popular path" to access to a database and hardware will using GET and POST method to communicate with the server through "/water" path.

### FRONTEND

มีหน้าเดียวคือ homepage แสดงสถานะต่าง ๆ ของตู้กดน้ำ โดยจะมี Animation ขณะเปิดหน้าเว็บไซต์ 5 วินาที มีสีสันออกไปทางโทนเย็น
สบายตาต่อภู้ใช้ โปรแกรมที่ใช้เขียน : HTML + CSS + JAVASCRIPT จะอธิบายรายละเอียดส่วนต่าง ๆ ดังต่อไปนี้

Navigation bar:
หน้าหลัก - ไปยังหน้าหลัก
กรมควบคุมโรค - shortcut สำหรับเชคข่าวสารเกี่ยวกับเชื้อไวรัส
ช่องทางติดต่อ - เว็ปเพจของตัวแทนของกลุ่มสำหรับติดต่อ
เกี่ยวกับ - เกี่ยวกับเว็บเเพจนี้ -w-
refresh-icon - แสดงสถานะฟมุนถ้าเว็ปไซต์สามารถ fetch ข้อมูลได้ครบถ้วน ถ้าไม่ครบจะหยุดหมุน
stat-icon - แสดงสถานะน้ำแต่ละ tank เหลืออยู่ ณ ปัจจุบันเป็นเปอร?เซนต์

Left Column:
  KU Smart Water - ไอคอนของ Project
  Slogan - เพื่อความบันเทิง
  รูปภาพด้านล่างซ้าย - ถ้าคนกดน้ำนึกไม่ออกว่าจะกินน้ำอะไรสามารถดูการแนะนำตรงนี้ได้
                   โดยโปรแกรมจะทำการสุ่มครั้งแรกขณะเริ่มต้นเวปไซต์และสุ่มใหม่หลังจากมีการกดน้ำ
  คำอธิบาย - เชิญชวนให้ป้องกันเชื้อไวรัส

// การ Fetch จะทำทุก ๆ 5 วินาทีซึ่งจะใกล้เคียงกับค่าเฉลี่ยในการกดน้ำ 1 ครั้งและไม่ให้ Server ทำงานหนักจนเกินไป
// การ Fetch จะทำการดึงข้อมูลน้ำที่เหลิออยู่ จำนวนการกดน้ำช่วงปัจจุบันและน้ำที่มีการกดมากที่สุดในช่วงที่ผ่านมา ได้แก่ ระดับชั่วโมง ระดับวัน และ    ระดับสัปดาห์

Middle Column:
  แสดงข้อมูลการกดน้ำ ณ ปัจจุบัน ตั้งแต่เริ่มชั่วโมงใหม่จนถึงเวลาสิ้นสุดชั่วโมงนั้น โดยมีเวลากำกับไว้ด้านล่าง เมื่อเริ่มต้น
  ชั่วโมงใหม่จะแสดงผลน้ำที่มีการกดมากที่สุดเป็นหมายเลขตู้

Right Column:
  จะแสดงผลคล้าย ๆ กับ Middle Column ก็คือ แสดงข้อมูลการกดน้ำ ณ ปัจจุบันตั้งแต่เริ่มต้นวันใหม่(เที่ยงคืน)และสัปดาห์ใหม่(วันอาทิตย์) 
  จนถึงสิ้นสุดของช่วงเวลานั้น เมื่อเริ่มต้นใหม่จะแสดงผลน้ำที่มีการกดมากที่สุดเป็นหมายเลขตู้ 
