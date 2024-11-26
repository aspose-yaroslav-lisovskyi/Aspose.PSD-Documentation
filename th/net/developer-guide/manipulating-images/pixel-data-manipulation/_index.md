---
title: การจัดการข้อมูลพิกเซลโดยใช้ Aspose.PSD สำหรับ C#
weight: 100
type: docs
description: ตัวอย่างเกี่ยวกับวิธีการอัปเดตข้อมูลพิกเซลเชิงลึกและอย่างรวดเร็วโดยใช้ PSD C# API
keywords: [แก้ไขพิกเซล, แก้ไข psd, แก้ไขเลเยอร์, การจัดการข้อมูลเชิงลึก, แก้ไขข้อมูล psd,  psd api, C#, ซีชาร์ป, ตัวอย่างโค้ด]
url: th/net/pixel-data-manipulation/
---

## บทนำ

Aspose.PSD เป็นไลบรารี่ที่มีความสามารถที่จะช่วยให้คุณทำงานกับไฟล์ Adobe Photoshop (PSD) ใน C# ในบทความนี้เราจะสำรวจวิธีการจัดการข้อมูลพิกเซลในไฟล์ PSD โดยใช้ Aspose.PSD สำหรับ C#

## ภาพรวม

โค้ดที่ให้มาแสดงถึงวิธีการสร้างไฟล์ PSD, เพิ่มเลเยอร์ใหม่, จัดการข้อมูลพิกเซลโดยตรง และบันทึกภาพที่แก้ไขแล้ว

### ขั้นตอนในการจัดการข้อมูลพิกเซล

1. **นำเข้าโมดูลที่จำเป็น**:
   นำเข้าโมดูลที่จำเป็น คุณต้องนำเข้าคลาส `PsdImage` และ `Layer` จากไลบรารี่ Aspose.PSD

2. **กำหนดเส้นทางของไฟล์ข้อมูลเข้าและออก**:
   ระบุเส้นทางของไฟล์ข้อมูลเข้าและออก

3. **เปิดไฟล์ข้อมูลเป็นสตรีม**:
   เปิดไฟล์ข้อมูลเป็นสตรีมโดยใช้คลาส `FileStream` ในโหมดอ่าน สร้างออบเจ็กต์ `PsdImage` โดยโหลดสตรีม

4. **สร้างภาพ PSD ใหม่**:
   สร้างภาพ PSD ใหม่โดยใช้คอนสตรักเตอร์ `PsdImage` และให้ความกว้างและความสูงของเลเยอร์เป็นอาร์กิวเมนต์

5. **กำหนดเลเยอร์ให้กับภาพ PSD**:
   กำหนดเลเยอร์ให้กับแอตทริบิวต์ `Layers` ของภาพ PSD

6. **จัดการข้อมูลพิกเซล**:
   โหลดพิกเซล ARGB32 จากเลเยอร์โดยใช้เมธอด `LoadArgb32Pixels` กำหนดช่วงของดัชนีตามความยาวของอาร์เรย์พิกเซลและปรับเปลี่ยนค่าพิกเซลตามที่ต้องการ

7. **บันทึกข้อมูลพิกเซลที่แก้ไข**:
   บันทึกข้อมูลพิกเซลที่แก้ไขกลับไปยังเลเยอร์โดยใช้เมธอด `SaveArgb32Pixels`

8. **บันทึกภาพ PSD**:
   บันทึกภาพ PSD ไปยังไฟล์เอาท์พุตโดยใช้เมธอด `Save`

### ตัวอย่าง

นี่คือตัวอย่างโค้ดที่แสดงวิธีการจัดการข้อมูลพิกเซลโดยใช้ Aspose.PSD สำหรับ C#:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "PixelDataManipulation-PixelDataManipulation.cs" >}}

### สรุป

Aspose.PSD สำหรับ C# มีชุดคุณสมบัติที่มีประสิทธิภาพสำหรับการจัดการข้อมูลพิกเซลในไฟล์ PSD ไม่ว่าคุณจะต้องการปรับเปลี่ยนพิกเซลตามเงื่อนไขที่เฉพาะเจาะจงหรือสร้างรูปแบบที่ซับซ้อน Aspose.PSD เป็นทางเลือกที่ดีและมีประสิทธิภาพสำหรับงานเหล่านี้

สำหรับข้อมูลเพิ่มเติมและตัวอย่างเพิ่มเติม โปรดเยี่ยมชม[Aspose.PSD สำหรับ C# เอกสาร](https://docs.aspose.com/psd/net/).