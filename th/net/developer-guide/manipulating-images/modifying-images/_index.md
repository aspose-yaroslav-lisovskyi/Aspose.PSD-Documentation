---
title: การแก้ไขรูปภาพ
type: หนังสือ
weight: 50
url: /th/net/modifying-images/
---

## **การดิเธอร์สำหรับรูปภาพเราสเตอร์**
การดิเธอร์เป็นเทคนิคในการสร้างภาพหลอนใหม่โดยการเปลี่ยนรูปแบบของจุดที่สร้างภาพจริง ๆ ให้มีลวดลายแปลกแตกต่าง เป็นวิธีที่พบบ่อยที่สุดในการลดระดับสีของภาพลงเหลือเพียง 256 สี (หรือน้อยกว่า) Aspose.PSD มีการสนับสนุนดิเธอร์สำหรับคลาส [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) โดยการใส่เมธอด Dither ซึ่งยอมรับพารามิเตอร์สองตัวคือวิธีใช้เหมือนกับ DitheringMethod ซึ่งมีตัวเลือก FloydSteinbergDithering และ ThresholdDithering คือกลไกการสร้างผลลัพธ์ที่มีลวดลาย ตัวเลือกทำให้มันเป็น 1 ทำให้เป็นสีดำและขาว ส่วนค่าที่ยอมรับคือ 1, 4, 8 ที่สร้างพาเล็ต 2, 4 และ 256 สีตามลำดับ

## **การปรับความสว่าง ความคมชัดและแกมมา**
การปรับสีในภาพดิจิตัลเป็นหนึ่งในคุณสมบัติหลักที่ส่วนใหญ่ของไลบรารีประมวลผลภาพให้ การปรับสีสามารถจำแนกออกเป็นตัวการปรับตามนี้

1. ความสว่างหมายถึงความสว่างหรือความมืดของสี การเพิ่มความสว่างของภาพให้สว่างออกทั้งหมดให้ขาวและความมืดลดลงเข้ามันถอดเชิงที่ความปรารถนา
1. ความคมชัดหมายถึงการทำให้วัตถุหรือรายละเอียดภายในภาพเป็นชัดเจนมากขึ้น การเพิ่มความคมชัดของภาพเพิ่มความแตกต่างระหว่างพื้นที่สว่างและมืดทำให้พื้นที่สว่างเป็นสว่างซึ่งมืดเป็นมืด การลดความคมชัดนี้จะทำให้พื้นที่ที่สว่างและที่มืดอยู่แตกต่างกับเดิมแต่รูปทั้งหมดกลายเป็นเรียบเนียนมากขึ้น
1. แกมมาจะเพิ่มประสิทธิภาพของการสว่างและความสว่างของแสงแสดงออกในการไล่ทางว่าพื้นที่ใดที่ทำให้เดิกไฟไลท์ในภาพ

### **การปรับความสว่าง**
Aspose.PSD สำหรับ API .NET มีเมธอด [AdjustBrightness](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustbrightness) สำหรับคลาส [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) ที่สามารถใช้เพื่อปรับความสว่างของภาพด้วยการใช้ค่าเป็นจำนวนเต็มเป็นพารามิเตอร์ ค่าพารามิเตอร์สูงสุดแสดงถึงภาพที่สว่างขึ้น นี่คือภาพเดิมและภาพผลลัพธ์เพื่อเปรียบเทียบ

### **การปรับความคมชัด**
เมธอด [AdjustContrast](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustcontrast) ที่เปิดเผยโดยคลาส [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) สามารถใช้เพื่อปรับความคมชัดของภาพโดยการส่งค่า float เป็นพารามิเตอร์

### **การปรับแกมมา**
เมธอด [AdjustGamma](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustgamma) ที่เปิดเผยโดยคลาส [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) มีเวอร์ชันสองรูปแบบหนึ่งที่รับค่า float เดียวและดำเนินการปรับแกมมาสำหรับตัวแปลงช่องสีแดง ค่าคุณสมบัติสีน้ำเงินและเขียว ในขณะที่การโอเวอร์โหลดอีกโอเวอร์โหลดรับพารามิเตอร์สามค่า float ที่แทนค่าสีแต่ละสี ตัวอย่างโค้ดต่อไปนี้สาธิตวิธีการปรับแกมมาของภาพ

## **เบลอภาพ**
บทความนี้สาธิตการใช้ Aspose.PSD สำหรับ .NET เพื่อทำเอฟเฟกเบลอบนภาพ Aspose.PSD สำหรับ  .NET ได้เปิดเผยเมท็อดที่ใช้ง่ายและมีประสิทธิภาพเพื่อให้ได้ผลลัพธ์นี้ Aspose.PSD สำหรับ .NET ได้เปิดเผยคลาส [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) สำหรับการสร้างเอฟเฟกเบลอในที่ต้องการ [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) คลาสต้องใช้ค่ารังสีและซิกม่าเพื่อสร้างเอฟเฟกเบลอบนรูปภาพ ขั้นตอนการทำเรียบง่ายเช่นต่อไปนี้

1. โหลดภาพโดยใช้เมทอดประกาศโดยคลาส Image
1. แปลงภาพเป็น [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage)
1. สร้างอินสแตนซ์ของคลาส [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) ด้วยคอนสตรักเตอร์ที่ตั้งค่าเรดดีเฟลตหรือให้รังสีและซิกม่า
1. เรียกเมธอด [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Filter โดยระบุรูปสี่เหลี่ยมเป็นขอบภาพและอินสแตนซ์ของคลาส [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions)
1. บันทึกผลลัพธ์

ตัวอย่างโค้ดต่อไปนี้สาธิตวิธีการสร้างเอฟเฟกเบลอบนภาพ

## **การตรวจสอบความโปร่งใสของภาพ**
บทความนี้สาธิตการใช้ Aspose.PSD สำหรับ .NET เพื่อตรวจสอบความโปร่งใสของภาพ ขั้นตอนการตรวจสอบความโปร่งใสของภาพเป็นเรื่องง่าย เช่นด้านล่าง

1. โหลดภาพโดยใช้เมธอดโกด [Load](https://reference.aspose.com/psd/net/aspose.psd/image/load/methods/2) ที่เปิดเผยโดยคลาส [Image](https://reference.aspose.com/psd/net/aspose.psd/image)
1. ตรวจสอบความโปร่งใสของภาพหากความโปร่งใสเป็นศูนย์ภาพเป็นโปร่งใส
1. ตัวอย่างโค้ดต่อไปนี้สาธิตวิธีการตรวจสอบว่าภาพโปร่งใสหรือไม่

## **การใช้งานเครื่องบวก GIF สูญเสีย**
โดยใช้ Aspose.PSD สำหรับ .NET ผู้พัฒนาสามารถตั้งค่าความแตกต่างของพิกเซล GIF ขึ้นอยู่กับ "พจนาคม" ของสตริงของพิกเซลที่เห็น การบีบอัดของ GIF ขึ้นอยู่กับการค้นหาสตริงยาวสุดที่ตรงกับพิกเซลในภาพ ตัวบีบอัดข้อมูลที่ยิ่งยาวที่สุดที่ "ใกล้เคียงพอ" กับพิกเซลในภาพ โดยตัวบีบอัดนี้จะเลือกสตริงของพิกเซลที่ยาวที่สุดที่ "ใกล้พอ" กับพิกเซลในภาพ ด้านล่างเป็นการสาธิตโค้ดของฟังก์ชันนี้

## **การใช้งาน Bicubic Resampling**
การเปลี่ยนขนาดแปลงหมายความว่าคุณกำลังเปลี่ยนขนาดพิกเซลของรูปภาพ ขณะที่คุณลดขนาด คุณกำลังลบพิกเซลและจะทำให้ข้อมูลและรายละเอียดหายไปออกจากรูปภาพของคุณ เมื่อคุณเพิ่มขนาด คุณกำลังเพิ่มพิกเซล ฟอโตช็อปเพิ่มพิกเซลเหล่านี้โดยใช้โปรโตรโลจี บทความนี้สาธิตวิธีการสามารถทำ Bicubic Resampling โดยใช้ Aspose.PSD สำหรับ .NET

ต่อไปนี้คือการสาธิตของโค้ดของฟังก์ชันนี้

## **การปรับชัดแจงสมดุลสี**
บทความนี้สาธิตการใช้ Aspose.PSD สำหรับ .NET เพื่อดำเนินการปรับข้อมูลสมดุลสีบนภาพ ชั้นปรับสมดุลสีสามารถทำการปรับข้อมูลสีของภาพเข้าถึงตามต้องการของพวกเขา มันนำเสนอสามช่องสีและสีที่เป็นตรงข้ามของพวกเขาและคุณสามารถปรับข้อมูลสำหรับคู่ของเหล่านี้เพื่อเปลี่ยนลักษณะของภาพ

ต่อไปนี้คือการสาธิตของโค้ดของฟังก์ชันนี้

## **การปรับชัดแจงสีและการปรับการปรับสีด้วยการแจงหลัง**
บทความนี้สาธิตวิธีการปรับชัดแจงผ่านการปรับไขว้สีด้วยการใช้ Aspose.PSD สำหรับ .NET ชั้นปรับปรับสีเป็นชั้นพิเศษที่