---
title: ชั้นการปรับความสว่างและความคมชัดในชั้นการปรับความสว่างและความคมชัด
type: docs
weight: 30
url: /th/java/layer-types/adjustment-layer/brightness-contrast/
---

# การทำงานกับชั้นการปรับความสว่างและความคมชัดใน Photoshop ด้วย Java

ในบทความนี้เราจะใช้การปรับความสว่างและความคมชัดต่อเอกสาร Adobe® Photoshop® โดยใช้ไลบรารี Aspose.PSD for Java® นอกจากนี้เราจะเรียนรู้เพิ่มเติมเกี่ยวกับคุณสมบัติของไลบรารีที่เกี่ยวข้องกับชนิดของชั้นการปรับปรุงนี้ตามกำลังจะพูดถึง

แต่ก่อนทุกอย่างมาทฤษฎีเล็กน้อย

ชั้นการปรับความสว่างและความคมชัดเปลี่ยนความสว่างและความคมชัดของภาพ แต่รอสักครู่นะ มันหมายความว่าอย่างไรจริง โดยเพิ่มความสว่างจะทำให้ค่าสีสว่างขึ้นไปยังสีขาวและการลดความสว่างทำให้ค่าสีมืดลงไปยังสีดำ การเพิ่มความคมชัดในลำดับทีสามจะเพิ่มความแตกต่างระหว่างสีสว่างและสีเข้มและการลดความคมชัดจะลดความแตกต่างนั้นตามลำดับ หมายความว่าสีสว่างกำลังกลับมาสว่างขึ้นและสีเข้มกำลังกลับมืดลง

## การสนับสนุนโหมดสี

ไลบรารีช่วยให้เพิ่มชั้นการปรับความสว่างและความคมชัดกับภาพในโหมดสี RGB, CMYK หรือ Lab

## พฤติกรรมปัจจุบันและที่มีความเก่า

การดำเนินการสำเนาไลบรารีปัจจุบัน (เวอร์ชัน 20.6 ในช่วงเขียนอยู่) ใช้ขั้นตอนแก้ไข Photoshop ตั้งต้นซึ่งทำให้เก็บรักษาช่วงตั้งตั้งการ์สุดท้ายจากเงาไปถึงจุดสว่าง แต่ยังไม่สนับสนุนพฤติกรรมเก่า หมายความว่าไลบรารีสนับสนุนชั้นการปรับความสว่างและความคมชัดในเอกสารที่สร้างขึ้นในรุ่นล่าสุดของ Photoshop (CS4 และสูงกว่า) อย่างไรก็ตาม คุณสามารถ [ขอคำแนะนำด้านพัฒนาพฤติกรรมเก่าของชั้นการปรับความสว่างและความคมชัด](https://forum.aspose.com/c/psd) ในฟอรัมของเราหากคุณต้องการ

## ปรับความสว่างและความคมชัด

ตอนนี้เราจะอธิบายว่า API ระดับสูงของชั้นการปรับความสว่างและความคมชัดทำงานอย่างไร (พวกเราคาดหวัง API จะง่ายต่อการอ่าน) คลาส PsdImage ประกอบไปด้วยวิธีสร้าง (addBrightnessContrastAdjustmentLayer) สำหรับสร้างคลาส BrightnessContrastLayer ซึ่งเป็นเกตเวย์สำหรับการปรับความสว่างและความคมชัด คลาส BrightnessContrastLayer เพียงแค่มีเมทอด get กับ set ชุดคู่สำหรับเข้าถึงความสว่างและความคมชัดอย่างเชื่อถือได้ เช่นกันการเปลี่ยนค่าของพวกเขา

![|ตัวอย่างปรับความสว่าง/ความคมชัดในชั้นปรับความสว่างของ PSD](brightness-contrast-psd-adjustment-layer-figure-1.png)

ดังนั้น เราจะเข้าชมภาพของหมา (b) ตัวอย่าง, เพื่อปรับความสว่าง1 และความคมชัด2 (a), โดยใช้เพียงเมธอดสร้างเท่านั้นด้วยอาร์กิวเม้นที่เกี่ยวข้อง เพื่อในที่สุดได้ภาพ (c) ที่ดูสดใสขึ้น:

BrightnessContrastLayer brightnessContrastLayer = psdImage.addBrightnessContrastAdjustmentLayer(15, 27);

หมายเหตุ:

1. ค่าความสว่างต้องอยู่ในช่วงจาก -150 ถึง 150
2. ค่าความคมชัดต้องอยู่ในช่วงจาก -50 ถึง 100

อ้างถึงเอกสารของ [BrightnessContrastLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/BrightnessContrastLayer) สำหรับข้อมูลเพิ่มเติม

## สรุป

ในบทความนี้เราได้ภาพรวงจากชั้นการปรับความสว่างและความคมชัดและเรียนรู้ว่าจะปรับความสว่างและความคมชัดของภาพด้วยเมธอดสร้างอย่างไร

อ้างถึงชุด [บทความเกี่ยวกับ API ชั้นการปรับปรุง](/th/java/layer-types/adjustment-layer/) ของ Aspose.PSD สำหรับ Java เพื่อเรียนรู้เพิ่มเติม