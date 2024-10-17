![image](https://github.com/user-attachments/assets/6abcba4e-5ce0-4100-ba72-80b84a948069)

**Introduction**

ตามกราฟและเนื้อหาข้างต้นทางกลุ่มของนักศึกษาได้นำเทคนิคต่างๆที่ได้เรียนมาประยุกต์ใช้ดังนี้
กราฟ
1.matplotlib
2.plotly
3.seaborn

ประเภทของกราฟ
เนื่องจากข้อมูลที่นักศึกษานำมาใช้นั้นค่อนข้างเป็นข้อมูลเชิงเฉพาะตัว ทางทีมได้ระดมความคิดและหารือโดยเป้าหมายของประเภทของกราฟที่ต้องการมาแสดง จะต้องมีองค์ประกอบดังนี้

	1.การแสดงผลของกราฟจะต้องแสดงสอดคล้องกับข้อมูล
	
	2.การแสดงผลนั้นจะต้องไม่ซับซ้อนมากนักเลือกใช้กราฟที่คนทั่วไปรู้จัก
	
	3.เน้นการสื่อสารกับคนดูที่ไม่รู้เรื่องข้อมูลเข้าใจโดยง่ายดาย

**F1 GrandPrix**

![image](https://github.com/user-attachments/assets/586792f5-1c90-43d0-9fa3-8ec9e6fbf57c)

**F1 Team**

![image](https://github.com/user-attachments/assets/2c8e8812-ae66-47ed-8665-8e4be67a1f98)

**F1 Driver**

![image](https://github.com/user-attachments/assets/52ea1adb-7457-49d3-aefb-671e637f0638)



**1. Data Exploration**
races
![image](https://github.com/user-attachments/assets/777c1696-ccf7-40ee-866d-16537a14fe77)

constructor_results

![image](https://github.com/user-attachments/assets/f210c086-184b-478b-b70f-8fb4e5b2a353)


driver

![image](https://github.com/user-attachments/assets/3560e0c0-1047-4691-bad3-5d5148b70436)


constructors

![image](https://github.com/user-attachments/assets/0e401276-462c-4aa2-8ebc-0c424d740d97)


lab_times

![image](https://github.com/user-attachments/assets/a52550d4-b4cf-4f57-bcc9-1baceef4efad)


status

![image](https://github.com/user-attachments/assets/251a39e7-b7f6-4595-97bb-553658230e1c)


driver_standings

![image](https://github.com/user-attachments/assets/de8b70aa-ac30-400a-91e2-1501707a9658)


pit stops

![image](https://github.com/user-attachments/assets/a6ec6171-e0c3-42d3-85da-d2e30e5d9478)

results

![image](https://github.com/user-attachments/assets/6493f94b-b55b-4f1f-9236-60d18428e950)


**3. Status Analysis**

![image](https://github.com/user-attachments/assets/27a5a589-08a3-42e0-b3b6-9eeda2965c89)

จากข้อมูลข้างต้นเป็นการสรุปข้อมูล Status ของแต่ละ races สำหรับแต่ละทีมย้อนหลัง  
โดยเลือกใช้กราฟ Bar chart ในการแสดง แสดงและสรุป
Race statusของแต่ละทีม
แสดงนั้นจะมีคอลลัมอื่นๆเข้ามารวมด้วย อาทิ การวิเคราะห์ค่า Race status นั้นจะเห็นได้ว่าทางทีมได้ใข้ Bar chart ก็จริงแต่จุดประสงค์ของกราฟนี้นั้นมีเปรียบเทียบของข้อมูลเลยมีค่า ข้อมูลรวมของ Race status นั้นๆ (สีเทา) และมีการแบ่งย่อยของแต่ละ status ออกมาเพื่อให้เห็นค่าของข้อมูลที่จัดเจน

Insight: จากข้อมูล จะพบว่าในแต่ละสนามมีสาเหตุที่ทำให้นักแข่งไม่สามารถแข่นจนจบได้ด้วยสาเหตุที่มาจาก ความผิดพลาดของนักแข่ง, อุบัติเหตุ หรือ ความเสียหายที่เกิดจากทีมวิศวกรรม

![image](https://github.com/user-attachments/assets/5c695d9d-8c91-41e7-a2e7-4857ce78af65)

![image](https://github.com/user-attachments/assets/269d29bd-af9e-43e6-9309-463ae5a515c3)

จากกราฟคือการแสดงความแตกต่างของ Error 2 ประเภท ที่มีผลต่อ performance ของทีม คือ Component Error จากความเสียหายของเครื่องยนต์ และ Performance ของ นักแข่ง (Driver Error) 

Insight: จากข้อมูลที่แสดง ได้มีการแบ่งจำนวนของ races ที่แข่งจบ และไม่จบ จากปัญหา เครื่องยนต์หรืออุปกรณ์เสียหาย หรือ ปัญหาจากอุบัติเหตุจากนักขับ และ อื่นๆ เพื่อให้ทราบว่า ในแต่ละทีมช่วง 5 ปีที่ผ่านมามีสถิติในการแข่งขันเป็นอย่างไร


**4. Constructor & Driver Journey**


Race & Pit stop Analysis 
	box plot วิเคราะห์ ระยะเวลาในการทำ pitstop ของแต่ละทีม โดยดูการกระจายตัวของข้อมูล และความสม่ำเสมอของระยะเวลาในการทำ Pitstop ซึ่งสะท้อนถึง Performance ของทีม pit  
bar chart ทีมจากข้อมูล box plotข้างต้น ได้ทำการตัดข้อมูลเฉพาะ q1 และ q3 มาเพื่อทำการวิเคราะห์ ค่าเฉลี่ยนของระยะเวลาในการทำ Pitstop ของแต่ละทีม >> ทำให้ทราบว่าทีมได้ทำเวลาได้น้อยที่สุด และหากตัด outlier หรือปัจจัยอื่นๆที่ทำให้ระยะเวลาในการทำ pitstop เพิ่มขึ้นออกไป จะเห็็นว่า performance ในการทำ pit stop ของแต่ละทีมจะมีค่าที่ใกล้เคียงกัน	
	bar chart 2 แสดงค่าเฉลี่ยระยะเวลาในการทำ Pitstop โดยดเฉลี่ยของทุกทีมในแต่ละสนาม ซึ่งอาจแปลได้ว่า ในการแข่งขันในครั้งถัดไปที่จะเกิดขึ้น หากทำเวลา ได้มาก หรือน้อยกว่าค่าเฉลี่ยของแต่ละสนาม ก็จะสื่อได้ถึง performance ที่ดี หรือ แย่ในการทำ Pitstop และการที่ได้ค่าเฉลี่ยของเวลาในแต่ละสนาม จะสามารถนำข้อมูลนี้ให้ทีม Strategy ในการนำไปวางแผนกลยุทธ์ในการเข้า Pitstopได้ 
 
   
4.1 Constructors

![Screenshot 2024-10-17 011729](https://github.com/user-attachments/assets/213b43b1-3b72-4065-9767-42f68d39f632)

4.2 Drivers

![Screenshot 2024-10-17 011454](https://github.com/user-attachments/assets/684ff107-e414-48ee-9f3b-84f139574fa2)

Insight: แสดงผลการเก็บคะแนนของแต่ละทีม และ นักขับในแต่ละ races ว่ามีผลงานเป็นอย่างไร โดยแบ่งสีตามทีม

**5.Race & Pit stop Analysis**

![Pit Stop](https://hips.hearstapps.com/hmg-prod/images/stop-1574089083.gif?crop=0.964xw:0.963xh;0,0&resize=1200:*)

4.1
ทางกลุ่มนักศึกษาใช้ Box plot โดยใช้ plotly ซึ่งทางทีมได้ใช้คุณสมบัติของ plotly ในการแสดงผลโดยการนำ cursor hover ลงไปที่กราฟเพื่อแสดงผลข้อมูล 

![image](https://github.com/user-attachments/assets/d5e93951-2d89-4fe8-a768-6862ded84dd1)

https://github.com/user-attachments/assets/652ce3a2-525f-4336-887f-283d1a11bc48

![image](https://github.com/user-attachments/assets/96395ca5-a601-4f0d-a5d7-a09f6f1264f3)

![image](https://github.com/user-attachments/assets/53b0adae-3f14-452c-8816-112ff95734d1)

4.2 Race Strategy Analysis on Spanish Grand Prix 2024
 Race Analysis 
	เนื่องจากการวิเคราะห์ Race นั้นจะต้องทำการใช้กราฟจำนวนทั้ง 3 กราฟในการวิเคราะห์
โดยจะแบ่งออกเป็น 3 กราฟ แต่ใช้ กราฟ 2ประเภทดังนี้

4.2.1 กราฟเส้นโดยใช้ LinearRegression เพื่อแสดงถึง

 -Lap Time
 
 -Race Position
 
4.2.2 กราฟ Bar Chart โดย searboarn เพื่อแสดงถึง ความแตกต่างของ

 -Stop Time
 
 เพื่อวิเคราะห์ลักษณะการแข่งของผู้เล่นหรือทีมโดยใช้
 
 -Lab Time
 
 -Race Position
 
 -Stop Time
 
 เป็นตัววิเคราะห์ อาทิเช่น นักแข่งคนแรกเข้า Pit stop หรือ Stop Time ในเวลาที่น้อยมากๆ แล้วหลังจากนั้นการแข่งหรือระยะเวลาการขับเร็วขึ้นก็จะมีโอกาสชนะมากขึ้น สามารถวิเคราะห์ได้ว่า ทีม ของนักแข่งใช้ของที่มีประสิทธิภาพ หรือ ประสิทธิภาพของนักแข่งเองที่ทำให้ทีมชนะ หรือ ทีมของนักแข่งใช้ของที่มีประสิทธิภาพรวมถึงประสิทธิภาพนักแข่งดี ก็จะมีโอกาสชนะได้มากขึ้น หรือ นักแข่งมีประสิทธิภาพที่แย่แต่มีทีมที่เลือกใช้ของประสิทธิภาพที่ดีทำให้ใช้เวลา stop time น้อยเลยมีโอกาสที่นักแข่งจะสามารถชนะได้แต่อาจจะน้อยกว่าเงื่อนไขข้อแรก

ตัวอย่างการวิเคราะห์ Race analysis ในการแข่งขัน Spanish Grandprix 2024 ได้มีการวิเคราะห์ในเรื่องของการทำ Pit stop analysis ของแต่ละทีม โดยได้มีการแสดง lap time และ lap ทีม และนักแข่งแต่ละคน ทำ pitstop  และระยะเวลาในการทำ pitstop รวมถึง แสดง Race positionในแต่ละ lap เพื่อให้สามารถวิเคราะห์ Strategy และ performace ของแต่ละทีมได้ 


![image](https://github.com/user-attachments/assets/d0fcefee-e10f-4e7b-b72c-661c9592d1a9)


Alpine F1 Team

![image](https://github.com/user-attachments/assets/20c7fda3-f199-45df-9b9d-c13b2f73d4cd)



Aston Martin

![image](https://github.com/user-attachments/assets/a1cd7f03-291b-4d8c-9fd9-497c824bb0a1)

Ferrari

![image](https://github.com/user-attachments/assets/585dd35c-7313-4c86-a406-77221d097c44)



Haas F1 Team

![image](https://github.com/user-attachments/assets/edb0f083-657f-411f-a9e5-98fe71a8fde6)


Mcleran

![image](https://github.com/user-attachments/assets/2b5179f5-2e10-4c0c-b951-423cbc817be3)


Mercedes

![image](https://github.com/user-attachments/assets/69487624-ed6f-463f-b9b5-5b7fe6e311e3)


RB F1 Team

![image](https://github.com/user-attachments/assets/94d643e4-faf2-4a57-b0a7-e119d2f6ff4b)


Red Bull

![image](https://github.com/user-attachments/assets/f19cb6eb-3580-4646-a000-4839c6c29721)


Sauber

![image](https://github.com/user-attachments/assets/043ebf76-c550-4248-a692-5227d4849d98)


Willams

![image](https://github.com/user-attachments/assets/da67c38e-2838-4ae4-899f-e4a1612392b2)



Summary
จากข้อมูลเบื่องต้นทำให้เรารู้ว่าในวงการของรถแข่งนั้นไม่ใช่แค่จะขับให้เร็วอย่างเดียวแท้จริงแล้วมีหลายปัจจัยมากมายและทำให้เห็นเทคนิคการเล่นของผู้เล่นและการsupport ของทีมว่ามีปัจจัยในการส่งผลแพ้หรือชนะด้วย

Next action plane:

ในอนาคตสามารถนำข้อมูลชุดนี้และข้อมูลย้อนหลังเพื่อดู pattern แล้วสร้างโมเดลเพื่อทำนายผลการแพ้และชนะได้
-ทีมที่มีโอกาสชนะ
-ผู้เล่นที่อยู่ทีมไหนก็ชนะ


Challenge

1.เนื่องจากข้อมูลมีลักษณะเฉพาะตัว ทางทีมเลยจะต้องมีการค้นขว้าเพื่อเข้าใจข้อมูลอย่าถ่องแท้เพื่อที่จะสามารถนำมาวิเคราะห์ได้

2.หลังจากการทำความเข้าใจข้อมูลแล้วทางกลุ่มนักศึกษาพบว่าเนื่องจากข้อมูลที่มีนั้นค่อนข้างกว้างและเยอะทางนักศึกษาจำเป็นต้องคิดโจทย์ในการวิเคราะห์ ว่าทำอะไร ทำเพื่ออะไรและทำไปทำไม เพื่อให้ได้ผลวิเคราะห์ที่ดีที่สุด

3.ข้อมูลไม่ได้มีประสิทธืภาพจะต้องทำการ prepare data รวมถึงการ clean data อย่างระมัดระวัง

4.ข้อมูลมีหลายไฟล์จะต้องนำมา mapping, joiner ข้อมูลและมีขั้นตอนที่ละเอียดอ่อนต่อการทำดาต้าอย่างมาก

5.การเลือกราฟที่เหมาะสมกับข้อมูลรวมทั้งต้องเลือกให้ไม่ซับซ้อนจนเกินไปจนทำให้ผู้อ่านกราฟท่านอื่นๆสับสน








