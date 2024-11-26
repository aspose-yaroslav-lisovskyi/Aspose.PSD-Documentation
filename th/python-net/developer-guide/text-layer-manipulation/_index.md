---
title: การทำงานกับเลเยอร์ข้อความใน Aspose.PSD สำหรับ Python
weight: 100
type: docs
description: ตัวอย่างการทำงานกับเลเยอร์ข้อความในไฟล์ PSD
keywords: [เลเยอร์ข้อความ, การอัปเดตข้อความ, แก้ไขส่วนข้อความ, สไตล์ข้อความ, ย่อหน้าข้อความ, ซอฟต์แวร์ PSD, ไพธอน, ตัวอย่างโค้ด]
url: th/python-net/text-layer-manipulation/
---

## **ภาพรวม**

**ภาพรวม**

Aspose.PSD สำหรับ Python เป็นไลบรารีที่มีความสามารถที่ใหญ่ในการทำงานกับไฟล์ PSD (เอกสาร Photoshop) ใน Python หนึ่งในคุณสมบัติสำคัญของไลบรารีนี้คือความสามารถในการแก้ไขเลเยอร์ข้อความในไฟล์ PSD ในบทความนี้ เราจะสำรวจวิธีการแก้ไขข้อความในไฟล์ PSD ด้วย Aspose.PSD สำหรับ Python อย่างง่ายๆ และวิธีที่มีประสิทธิภาพมากขึ้นโดยใช้ส่วนข้อความ

**วิธีที่ง่ายในการอัปเดตเลเยอร์ข้อความ**

เพื่ออัปเดตเลเยอร์ข้อความในไฟล์ PSD โดยใช้ Aspose.PSD สำหรับ Python คุณสามารถใช้วิธี update_text ของคลาส TextLayer เมทอดนี้ช่วยให้คุณสามารถอัปเดตเนื้อหาข้อความของเลเยอร์ข้อความได้อย่างง่ายดาย ต่อไปนี้คือตัวอย่างโค้ดที่แสดงวิธีง่ายๆ ในการอัปเดตเลเยอร์ข้อความ

{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-psd-text-layer-manipulation-simple.py" >}}

**การแก้ไขโดยใช้ส่วนข้อความ**

วิธีที่มีประสิทธิภาพมากขึ้นในการอัปเดตเลเยอร์ข้อความโดยใช้ส่วนข้อความ: วิธีง่ายในการอัปเดตเลเยอร์ข้อความในไฟล์ PSD เหมาะสำหรับการแก้ไขข้อความพื้นฐาน อย่างไรก็ตามหากคุณต้องการควบคุมเพิ่มเติมเกี่ยวกับสไตล์และการจัดรูปแบบข้อความ คุณสามารถใช้วิธีที่มีประสิทธิภาพมากขึ้นโดยการใช้ส่วนข้อความ ส่วนข้อความช่วยให้คุณระบุสไตล์และย่อหน้าต่างๆ ภายในเลเยอร์ข้อความ ต่อไปนี้คือตัวอย่างโค้ดที่แสดงวิธีนี้

{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-psd-text-layer-manipulation-text-portion.py" >}}

ในโค้ดด้านบน เราเข้าถึงเลเยอร์ข้อความที่เราต้องการอัปเดต (image.layers[1]) จากนั้นเราดึงออกวัตถุ text_data จากเลเยอร์ข้อความซึ่งช่วยให้เราทำงานกับส่วนข้อความ เราสร้างออบเจกต์ default_style และ default_paragraph ซึ่งจะถูกใช้เป็นสไตล์เริ่มต้นและย่อหน้าสำหรับส่วนข้อความ

ต่อมา เรากำหนดส่วนข้อความที่เราต้องการเพิ่มเข้าไปในเลเยอร์ข้อความ แต่ละส่วนแทนกลุ่มข้อความที่มีสไตล์และรูปแบบต่างๆ ในตัวอย่างนี้ เรามีส่วนข้อความห้าส่วน - "E=mc", "2\r", "Bold", "Italic\r", และ "Lowercasetext" เรายังอัปเดตสไตล์ของส่วนเหล่านี้ตามความต้องการของเรา

จากนั้น เราวนลูปผ่านส่วนใหม่และเพิ่มมันไปยังวัตถุ text_data โดยใช้เมทอด add_portion สุดท้ายเราเรียกเมทอด update_layer_data ของวัตถุ text_data เพื่ออัปเดตเลเยอร์ข้อความด้วยส่วนข้อความใหม่

**สรุป**

Aspose.PSD สำหรับ Python มีความสามารถที่แข็งแกร่งในการแก้ไขข้อความในไฟล์ PSD ไม่ว่าคุณจะต้องการอัปเดตเนื้อหาข้อความของเลเยอร์ข้อความหรือใช้สไตล์และการจัดรูปแบบเพิ่มเติม Aspose.PSD สำหรับ Python จะช่วยคุณ ด้วยวิธีที่ง่ายหรือวิธีที่มีประสิทธิภาพมากขึ้นโดยการใช้ส่วนข้อความ คุณสามารถจัดการเลเยอร์ข้อความในไฟล์ PSD ของคุณได้อย่างง่ายๆ

กรุณาตรวจสอบตัวอย่างเต็ม

## **ตัวอย่าง**

{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-psd-text-layer-manipulation-full.py" >}}