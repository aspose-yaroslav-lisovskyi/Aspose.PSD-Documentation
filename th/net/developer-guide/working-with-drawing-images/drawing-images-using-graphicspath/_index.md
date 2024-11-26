---
title: การวาดรูปภาพโดยใช้ GraphicsPath
type: docs
weight: 30
url: /th/net/drawing-images-using-graphicspath/
---

## **การวาดรูปภาพโดยใช้ GraphicsPath**
คลาส [GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath) รับผิดชอบในการสร้างและบรรจุเวลาประการในกราฟิกส์ คลาส GraphicsPath ไม่มีการอ้างอิงถึงรูปภาพและไม่เปลี่ยนรูปภาพเอง แต่มันสามารถถือเป็นวัตถุที่มีข้อมูลเมตาดาต้าที่อธิบายเส้นทางที่คลาส Graphics สามารถวาด เข้าใจได้ว่าคลาส GraphicsPath ใช้รูปร่าง แต่ละรูปร่างเป็นการเชื่อมต่อเส้นทและเส้นโค้งหรือรูปพื้นฐานที่เรขาคณิต แต่ละรูปร่างอาจถูกแบ่งเป็นส่วนรูปร่าง คุณสามารถเพิ่ม ลบ และเปลี่ยนรูปร่างหรือรูปร่างต่าง ๆ ในวัตถุ GraphicsPath เมื่อ GraphicsPath ได้ถูกเปรียบเทียบแล้ว ใช้วิธีของคลาสไรต์เพื่อวาดหน้าตาหรือเติมในเส้นทาง คลาส Graphics นำทุกๆ ส่วนรูปร่างและวาดให้เกิดรูปภาพสุดท้าย

### **การวาดโดยใช้คลาส GraphicsPath**
ด้านล่างนี้เป็นตัวอย่างการใช้องค์ประกอบ [GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath) class ตัวอย่างรหัสต้นฉบับถูกแบ่งออกเป็นส่วนต่าง ๆ เพื่อคงความง่ายต่อการติดตาม ละเอียดขั้นตอนตัวอย่างแสดงวิธีการ:

- สร้างรูปภาพ
- กำหนดค่าเริ่มต้นให้วัตถุ Graphics
- เคลียร์พื้นผิว
- สร้างอินสแทนซ์ของ [GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath)
- สร้างรูปร่าง
- เพิ่มรูปร่างลงในรูปร่าง
- สร้างอาร์เรย์ของรูปร่าง
- วาดเส้นทาง
- เติมเส้นทาง

### **การวาดรูปภาพโดยใช้ GraphicsPath : ตัวอย่างโปรแกรม**
#### **GraphicsPath : สร้างรูปภาพ**
เริ่มต้นโดยการสร้างภาพโดยใช้วิธีใดก็ได้ที่อธิบายไว้ในการสร้างไฟล์
#### **GraphicsPath : กำหนดค่าเริ่มต้นให้วัตถุ Graphics**
สร้างและกำหนดค่าเริ่มต้นให้วัตถุ Graphics โดยการส่งวัตถุภาพเข้าไปในคอนสตรักเตอร์ของมัน
#### **GraphicsPath : เคลียร์พื้นผิว**
เคลียร์พื้นผิวกราฟิกโดยการเรียกวิธีเคลียร์ของคลาส Graphics และส่งสีเป็นพารามิเตอร์ วิธีนี้จะเติมสีที่ส่งผ่านเข้าไปในพื้นผิวกราฟิก
#### **GraphicsPath : สร้างอินสแทนซ์ของ GraphicsPath**
สร้างอินสแทนซ์ของ GraphicsPath ด้วยการตั้งค่า GraphicsPath เป็น Alternate ตามค่าเริ่มต้น โหมดนี้กำหนดว่าจะเติมภายในรูปร่างปิดอย่างไร ค่าอื่นที่เป็นไปได้สำหรับ GraphicsPath คือ Winding
#### **GraphicsPath : สร้างรูปร่าง**
สร้างอินสแทนซ์ของคลาส Figure ตามที่ได้พูดถึงไว้ก่อนหน้า Figure สามารถบรรจุ Shapes ได้และรูปร่างอยู่ในเนมสเปซ Aspose.PSD.Shapes
#### **GraphicsPath : เพิ่มรูปร่างลงในวัตถุ**
วิธีการเพิ่มรูปร่างที่เปิดเผยโดยคลาส Figure ช่วยให้คุณเพิ่มรูปร่างในรูปร่าง ในตัวอย่างโค้ดด้านล่าง มีการเพิ่มรูปร่างหลายรูปร่างในออบเจ็กต์ Figure
#### **GraphicsPath : เพิ่มรูปร่างลงในอาร์เรย์**
สามารถเพิ่มรูปร่างหลายรูปร่างในวัตถุ GraphicsPath โดยใช้วิธี AddFigures ที่ได้รับการเปิดเผยโดยคลาส GraphicsPath วิธีนี้ยอมรับอาร์เรย์ของรูปร่างเป็นพารามิเตอร์
#### **GraphicsPath : วาดเส้นทาง**
วาด GraphicsPath โดยใช้วิธี DrawPath ที่ได้รับการเปิดเผยโดยคลาส Graphics วิธีนี้ยอมรับพารามิเตอร์สองตัว ตัวแรกคือวัตถุของคลาส Pen ซึ่งกำหนดสี ความกว้างและสไตล์ของเส้นทาง ตัวแทนคือวัตถุของคลาส GraphicsPath แทนเส้นทางเอง
#### **GraphicsPath : เติมเส้นทาง**


คุณสามารถเติมเส้นทางโดยการส่งวัตถุ GraphicsPath ให้กับวิธี Fill Paths ที่ได้เปิดเผยโดยคลาส Graphics วิธี Fill Paths จะเติมเส้นทางตามโหมดการเติม (alternate หรือ winding) ที่ถูกกำหนดให้เส้นทางนี้ ถ้าเส้นทางมีรูปร่างที่เปิดอยู่ สิ่งที่วางเติมในเส้นทางจะถูกเติมเหตุว่าเส้นทางเหล่านั้นถูกกำหนดเป็นปิด

วิธี Fill Paths ยอมรับพารามิเตอร์สองตัว ตัวแรกคือวัตถุของคลาสแปรส Brush จากเนมสเปซ Aspose.PSD.Brushes ตัวที่สองคือเส้นทางเอง สำหรับการอันหลอสำหรับตัวอย่างนี้ให้ใช้ HatchBrush ซึ่งเป็นแปรสจากที่เป็นสี่เหลี่ยม มีสไตล์ hatching สีพื้นหลัง และสีพื้นหน้า ก่อนที่จะส่งวัตถุ HatchBrush ให้กับวิธี Fill Paths ตั้งค่าสมบัติของมัน
### **GraphicsPath : รหัสภายใจ**

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphicsPath-DrawingUsingGraphicsPath.cs" >}}

ทุกคลาสที่ใช้งาน IDisposable จะถูกตั้งค่าเป็นตัวแปรใน Using statement เพื่อให้แน่ใจว่ามันจะถูกทิ้งอย่างถูกต้อง
