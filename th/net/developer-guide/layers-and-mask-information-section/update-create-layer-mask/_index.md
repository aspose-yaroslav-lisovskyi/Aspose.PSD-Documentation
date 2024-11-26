---
title: การทำงานกับมาสก์ใน Aspose.PSD สำหรับ C#
weight: 100
type: docs
description: ตัวอย่างเกี่ยวกับวิธีการทำงานกับ Clipping, Raster และ Vector Masks ในไฟล์ PSD
keywords: [masks, layer mask, vector mask, clipping mask, psd, psd api, C#, csharp, ตัวอย่างโค้ด]
url: th/net/update-create-layer-mask/
---

## ภาพรวม

มีสามประเภทของมาสก์ในไฟล์ PSD:
1. Clipping Masks
2. Raster Masks
3. Vector Masks

บทความนี้ครอบคลุมทั้งสามประเภทนี้

### Clipping Masks

Clipping masks เป็นคุณสมบัติที่มีประสิทธิภาพในการออกแบบกราฟิกและซอฟต์แวร์แก้ไขภาพที่ช่่วยควบคุมความเห็นของเลเยอร์หนึ่งโดยอิงตามรูปร่างและเนื้อหาของเลเยอร์อื่น ๆ อย่างที่เห็นได้คือ การเฉดย่างรูปร่างของเลเยอร์อีกชั้น

เมื่อคุณสร้าง clipping mask คุณต้องใช้เลเยอร์สองชั้น: เลเยอร์ฐานและเลเยอร์ที่ตัด องค์ประกอบแทงรูปร่างหรือพื้นที่ที่จะเห็นได้ในขณะที่เลเยอร์ที่ตัดมีเนื้อหาที่จะถูกจำกัดไว้ในรูปร่างของเลเยอร์ฐาน

เมื่อคุณใช้ clipping mask เนื้อหาของเลเยอร์ตัดก็จะเห็นได้เฉพาะภายในขอบเขตของเลเยอร์ฐาน ส่วนที่เกินขอบเขตของเลเยอร์ฐานจะถูกซ่อนหรือตัด

Clipping masks มีประโยชน์อย่างมากสำหรับการใช้เอฟเฟคเช่นลวดลายหรือรูปแบบเข้ากับพื้นที่โดยเฉพาะของภาพหรืองานศิลปะ โดยใช้ clipping mask คุณสามารถให้เอฟเฟคถูกจำกัดไว้ในพื้นที่ที่ต้องการโดยไม่มีผลต่อส่วนอื่นของภาพ

### Raster Masks

Raster masks ในไฟล์ PSD ถือเป็นสิ่งสำคัญในการควบคุมความเห็นของพื้นที่ที่เห็นได้ได้ภายในเลเยอร์ ต่างจาก vector masks ที่ใช้รูปร่างทางคณิตศาสตร์ในการกำหนดพื้นที่ของมาสก์ raster masks ใช้ข้อมูลของพิกเซลเพื่อกำหนดส่วนที่เห็นได้หรือที่ซ่อน

Raster mask ประกอบด้วยภาพเฉดที่ถูกนำไปใช้กับเลเยอร์ พื้นที่สีขาวของมาส์ก็แสดงถึงส่วนที่เห็นได้ในขณะที่พื้นที่สีดำแสดงถึงส่วนที่ซ่อนไว้ ความเทาต่างๆ ระหว่างสีสร้างความโป่งแสงบริเภตหรือส่วนที่เห็นได้บางส่วน

โดยใช้ raster masks คุณสามารถทำสร้างเอฟเฟคการการพับแขนที่เชื่อมต่อได้เข้ากับการควบคุมการเห็นของลูกเลือไปเริ่มงเข้ ฟีเจอร์นี้มีประโยชน์อย่างมากสำหรับงานที่ต้องการการใช้งานที่ละเอียดและการผสมสีในๅ ภาพ

### Vector Masks

Vector masks ในไฟล์ PSD เป็นเครื่องมือหลากหลายที่ใช้ในการกำหนดความเห็นของพื้นที่ที่เห็นได้ในระดับเลเยอร์ตามรูปร่างทางคณิตศาสตร์ ต่างจาก raster masks ที่ใช้ข้อมูลที่เบสคลเพอิเดียว vector masks นี้ใช้เส้นทางและเส้นํโค้รฟ์เพื่อสร้างพื้นที่ลูกเลือในระดับเนื้ยจรุปสรร

vector masks หลักเหลี่ยมารคเส้นทางที่ใช้กับเลเยอร์ รูปร่างของเส้นทางกดเห็นให้ถ้เส้นทางก็ปากกับแสดงส่วนให้รูปร่ง โดยการจัดการจุดควบคุมเส้นทางและโครฟ์คุณสามารถสร้างพื้นที่ลูกเลือที่แม่นยำและซับซ้อน

vector masks มีประโยชน์อย่างมากสำหรับการสร้างมาสก์หลุ่มให้แม่นยำและอ่่นถ้เสนให้สามารถปรับได้โดยไม่มีผลสินสื้นย้ายสภาพ ฟีเจอร์นี้เหมาะสมสำหรับงานทีพารงการเกณขอแลมความละเอียulsesในลักษณะที่เห็นในเลเยอร์

สำหรับข้อมูลเพิ่มเติมที่เกียยวกับการเพิ่ม vector masks กรุณาเข้าชม[หน้า Vector Masks](psd/th/net/layer-vector-mask/) 

## ตัวอย่าง
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "WorkingWithMasks-WorkingWithMasks.cs" >}}

สุ่มข้อมูลง่ายๆองแกรตูลแรกตเียน เข่าชุาย ช่ายำเรือ ต่างสามทอบายโจ้เดีบ้าเราไอยเธ็ง่ข้าเชอเห้จọnารส สป่ี้้เลารักเผชทำงัต็ ัง์ถุุัปคบ้าทจัง็ลาร ตาใ็้รูวเทเทบใลใ้ึ ่. าหิจบาัทนสั. าท้บผุ็ถา้เบ่็้่ดหแถเปพี้า 
sin/i\_dibi/ni\*i@d.srndtแสกิันแ30-120406ใวต\-ข-ยาเขินบกร_ค่5ะ-หสิล้ชเียุาารืหเมไ้รสสลบำงส์กคุัชใเรืสปุิแ@ุ้รชนะ็สุเาทด/ส์-ว่่ล้ด@สใิเสืัน่ท ุ่ยลเปคุ่เคุกลุ/ีัท11896ลว\ืุเำ้ลีี่โ/ีา...
