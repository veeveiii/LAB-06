#ใบงานที่ 6
##เรื่อง การใช้งานคำสั่ง Console.Read() และ Console.ReadLine()
##วัตถุประสงค์
1). เพื่อให้นักศึกษาบอกชื่อ method ที่ใช้ในการรับค่าตัวอักษรพื้นฐานในภาษา C# ได้

2). เพื่อให้นักศึกษาสามารถใช้คำสั่งรับค่าตัวอักษรได้
##ความรู้เบื้องต้น
คำสั่งที่ใช้รับค่าตัวอักษรทางอินพุตมาตรฐานของ C# คือ ```Console.Read()``` และ ``` Console.ReadLine()``` โดยทั้งสองจะมีข้อแตกต่างกันคือ ```Read()``` จะอ่านตัวอักษร ส่วน ```ReadLine()``` จะอ่านสตริง จนกว่าจะกด Enter ในการรับค่าด้วย ```Read()``` และ ```ReadLine()``` จะรับเฉพาะค่า ASCII เท่านั้น หากต้องการรับค่าตัวเลข จะต้องมีการแปลง ASCII ของตัวเลขที่พิมพ์เข้ามาให้เป็นค่าตัวเลข (การรับอักษร “22” จะไม่ได้หมายถึงค่าตัวเลข 22) 

##ลำดับขั้นการทดลอง

1). สร้าง Project ตั้งชื่อเป็น Lab6 เพื่อทดลองการใช้งานคำสั่ง ```Console.ReadLine()``` และ ```Console.ReadLine()```

2). โปรแกรมสำหรับรับตัวอักษรจากคีย์บอร์ด 

  2.1). แก้ไขโปรแกรมให้เป็นดังรูป

 ![](https://github.com/Desktop-Programming-Lab-2559/LAB-06/blob/master/imgs/pic1.png)

  2.2).	โปรแกรม และบันทึกผลที่ได้
![](https://scontent.fbkk2-2.fna.fbcdn.net/v/t34.0-12/14971921_1133898976730352_1026036562_n.png?oh=603f114b4761c9bdec184386b5c7d67a&oe=5827781C)
<hr>

###คำถาม 6.1 ถ้าพิมพ์ตัวอักษรจำนวนหลายๆ ตัวแล้วกด Enter จะได้ผลอย่างไร ทำไมจึงเป็นเช่นนั้น
ตอบ หากเราทำการพิมพ์ตัวอักษรหลายๆตัว ผลที่แสดงออกมาจะปรากฏเพียงแค่ตัวเดียว ก็คือตัวแรกเท่านั้น เพราะ เราประกาศให้ ch เป็น Char ดังนั้น ch จะสามารถเก็บข้อมูลได้ 1 ไบต์เท่านั้น. ดังภาพต่อไปนี้ ![](https://scontent.fbkk2-2.fna.fbcdn.net/v/t34.0-12/14971968_1133898973397019_1136365603_n.png?oh=dd43c63f426ffe60d085c3cb546eec08&oe=58270DEA)
<hr>

###คำถาม 6.2 ในบรรทัดที่ 11 ซึ่งมีโปรแกรมเป็น ```ch = (char)Console.Read();```  นั้น ถ้าตัด ```(char)``` ออกไป จะเกิดอะไรขึ้น ให้อธิบายประกอบ
ตอบ หากทำการตัด (char) ออกไปจากคำสั่งเดิม จะขึ้น Error .

3).	โปรแกรมสำหรับรับ string จากคีย์บอร์ด
 
 3.1).	แก้ไขโปรแกรมให้เป็นดังรูป

 ![](https://github.com/Desktop-Programming-Lab-2559/LAB-06/blob/master/imgs/pic2.png)
 
 3.2).	โปรแกรม และบันทึกผลที่ได้
![](https://scontent.fbkk2-2.fna.fbcdn.net/v/t34.0-12/14971912_1133908846729365_149328600_n.png?oh=7d4d39c51843daf08662b881167ecbfb&oe=58273885)

<hr>

4).	โปรแกรมสำหรับรับค่าตัวเลข เนื่องจากคำสั่ง ```Read()``` และ ```ReadLine()``` จะรับเฉพาะตัวอักษร การรับตัวเลข เราต้องใช้เมธอด TryParse() มาช่วยแปลงค่า

4.1).	แก้ไขโปรแกรมให้เป็นดังรูป
 
 ![](https://github.com/Desktop-Programming-Lab-2559/LAB-06/blob/master/imgs/pic3.png)

4.2).	รัน โปรแกรม โดยป้อนตัวเลขใดๆ และบันทึกผลที่ได้
![](https://scontent.fbkk2-2.fna.fbcdn.net/v/t34.0-12/15050458_1133911063395810_378914609_n.png?oh=ea615bd743c16b3568462f0c27a03c8b&oe=58284F74)
<hr>

###คำถาม 6.3 ถ้าเราป้อนตัวอักษรลงไปแทนที่ตัวเลข จะเกิดอะไรขึ้น มีวิธีการป้องกันหรือแก้ไขอย่างไร
ตอบ เมื่อทำการพิมพ์ตัวอักษรจะขึ้น Error และบังคับให้ปิดหน้าต่างรัน เราควรใช้ต้องฟังชันการแปลงตัวอักษรเป็นตัวเลข 
เมื่อทำการรัน จะได้ผลลัพธ์ดังภาพ ![](https://scontent.fbkk2-2.fna.fbcdn.net/v/t35.0-12/15052050_1133911486729101_479645041_o.png?oh=02d0a31f9512be78ea8d834fda724b68&oe=58270A57)
<hr>

5).	โปรแกรมสำหรับรับค่าตัวเลข แต่ในบางกรณีที่ผู้ใช้ป้อนตัวอักษร จะทำให้เกิด error และทำให้โปรแกรม hang ได้ จึงต้องมีการป้องกันโดยใช้ประโยค ```try{…} catch{…}```  (ประโยค ```try{…} catch{…}``` นี้จะศึกษารายละเอียดภายหลัง)

  5.1).	แก้ไขโปรแกรมให้เป็นดังรูป

  ![](https://github.com/Desktop-Programming-Lab-2559/LAB-06/blob/master/imgs/pic4.png)

  5.2).	รัน โปรแกรม โดยป้อนตัวเลขใดๆ และบันทึกผลที่ได้
![](https://scontent.fbkk2-2.fna.fbcdn.net/v/t34.0-12/15049597_1133987286721521_1786161588_n.png?oh=8204524d07625ac1022f6bc545cd4009&oe=582735AF)
<hr>

###คำถาม 6.4 ถ้าเราป้อนตัวอักษรลงไปแทนที่ตัวเลข จะเกิดอะไรขึ้น เหมือนหรือต่างจากโปรแกรมก่อนหน้านี้อย่างไร
ตอบ เมื่อทำการป้อนตัวอักษรลงไปจะขึ้น error เช่นเดียวกับโปรแกรมก่อนหน้า แต่จะมีข้อความแจ้งขึ้นมาว่าป้อนข้อมูลไม่ตรงกับชนิดของตัวแปร
<hr>

##แบบฝึกหัด ให้เขียน code ในการรับค่าอินพุตต่อไปนี้และแสดงออกหน้าจอให้ถูกต้อง
``` Name :  (ป้อนชื่อของนักศึกษา). ```

``` Lastname : (ป้อนนามสกุลนักศึกษา).```

``` ID : (ป้อนรหัสนักศึกษา).```

``` GPA : (ป้อนเกรดเฉลี่ยนักศึกษา โดยมีทศนิยมสองหลัก).```
<hr>
![](https://scontent.fbkk2-2.fna.fbcdn.net/v/t34.0-12/14996555_1134039056716344_1046777621_n.png?oh=4bfc3bdfadedd19b9e04200c53649eb7&oe=582738C5)
Ailada Samingkaew 57030249
<hr>
