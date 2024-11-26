---
title: หัวเรื่องไฟล์ PSD และ PSB
type: docs
weight: 40
url: /th/net/psd-and-psb-file-header/
---

## **คำอธิบาย**
หัวเรื่องไฟล์ Adobe Photoshop ประกอบไปด้วยข้อมูลเกี่ยวกับเวอร์ชันของไฟล์ (1 สำหรับ PSD และ 2 สำหรับ PSB), จำนวนของช่อง, โหมดสี และความลึกของบิต

คุณสามารถเรียนรู้การสนับสนุนด้วย Aspose.PSD การผสานโอนของโหมดสีและความลึกบิตจากบทความที่เกี่ยวข้อง


หัวเรื่องไฟล์ประกอบด้วยคุณสมบัติพื้นฐานของภาพ

|**ความยาว**|**คำอธิบาย**|
| :- | :- |
|4|ลายเซ็นเจอร์: เท่าเสมอกับ *"8BPS"*|
|2|[เวอร์ชัน PSD](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/fileformatversion): เท่าเสมอกับ 1 สำหรับไฟล์ PSD และ 2 สำหรับไฟล์ PSB Aspose.PSD สามารถตรวจจับเวอร์ชันของรูปแบบไฟล์และอ่านได้อย่างถูกต้อง|
|6|ที่สงวนไว้: ต้องเป็นศูนย์|
|2|จำนวนของช่องในภาพ รวมถึงช่องอัลฟา ช่วงที่รองรับคือ 1 ถึง 56|
|4|ความสูงของภาพในพิกเซล ช่วงที่รองรับคือ 1 ถึง 30,000 ไฟล์ PSB รองรับความสูงสูงสุดได้ถึง 300,000 พิกเซลไฟล์ PSB ได้รับการสนับสนุนโดย Aspose.PSD ด้วย|
|4|ความกว้างของภาพในพิกเซล ช่วงที่รองรับคือ 1 ถึง 30,000 ไฟล์ PSB รองรับความกว้างสูงสุดได้ถึง 300,000 พิกเซลการประมวลผลเป็นชุดของไฟล์ PSD/PSB ขนาดใหญ่ขั้นตอนนี้ยังได้รับการสนับสนุนโดย Aspose.PSD|
|2|ความลึก: จำนวนบิตต่อช่อง ค่าที่รองรับคือ 1, 8, 16 และ 32 แต่ไม่ใช่ทุกโหมดสีทำงานกับความลึกทุกความลึก|
|2|[โหมดสี PSD](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/ColorModes) ของไฟล์ ค่าที่รองรับคือ: ภาพแบบการ์ตูน = 0; ระดับสีเทา = 1; ดัชนี = 2; RGB = 3; CMYK = 4; หลายช่องสี = 7; โจทัศนู = 8; ห้องทดสอบ = 9 คุณสามารถตรวจสอบ [การอ้างอิง API ของ PSD เรา](https://reference.aspose.com/psd)|
 