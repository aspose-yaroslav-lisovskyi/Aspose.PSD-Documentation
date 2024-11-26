---
title: การใช้เอฟเฟ็กต์เลเยอร์ในไฟล์ PSD
weight: 100
type: docs
description: ตัวอย่างการใช้เอฟเฟ็กต์เลเยอร์ใน Aspose.PSD สำหรับ Python
keywords: [เงาแบบใส, การทับสี, แสงเงาภายใน, แสงเงาภายนอก, ไอพีเอสดี, ไพทอน, ตัวอย่างโค้ด]
url: th/python-net/layer-effects/
---

## **ภาพรวม**
ใน Aspose.PSD สำหรับ Python, คุณสามารถสร้างเอฟเฟ็กต์ต่าง ๆ บนเลเยอร์เพื่อเพิ่มความสวยงามให้กับภาพของคุณ สามารถทำได้โดยใช้คลาส BlendingOptions ซึ่งมีเมธอดในการเพิ่มเอฟเฟ็กต์ต่าง ๆ เช่น stroke, inner shadow, drop shadow, gradient overlay, color overlay, pattern overlay และ outer glow

เพื่อสาธิตการสร้างเอฟเฟ็กต์บนเลเยอร์ เรามาดูตัวอย่างโค้ดด้านล่าง

ในตัวอย่างโค้ดนี้ เราจะโหลดภาพ PSD และบันทึกภาพเริ่มต้นเป็น PNG ตามลำดับ จากนั้น เราจะสร้างเอฟเฟ็กต์ต่าง ๆ บนเลเยอร์ต่าง ๆ โดยใช้คลาส BlendingOptions หน้าที่ของแต่ละเอฟเฟ็กต์ อธิบายได้ดังนี้:

Stroke: เราเพิ่มทาสีไปยังเลเยอร์ที่ 1 โดยระบุขนาดทา, จุดสีของไทล์เรเดียนทและจุดโปร่งแสง

Inner Shadow: เราเพิ่มเงาภายในไปยังเลเยอร์ที่ 2 โดยระบุมุมและสีของเงา

Drop Shadow: เราเพิ่มเงาแบบใสไปยังเลเยอร์ที่ 3 โดยระบุมุมและสีของเงา

Gradient Overlay: เราเพิ่มการทับสีไปยังเลเยอร์ที่ 4 โดยระบุจุดสีของไทล์และจุดโปร่งแสง

Color Overlay: เราเพิ่มการทับสีไปยังเลเยอร์ที่ 5 โดยระบุสีและความโปร่งแสงของการทับซ้อน

Pattern Overlay: เราเพิ่มการทับลายไปยังเลเยอร์ที่ 6 โดยระบุข้อมูลลาย, ความกว้าง และความสูง

Outer Glow: เราเพิ่มแสงเรย์แบบนอกไปยังเลเยอร์ที่ 7 โดยระบุขนาดและสีที่เติมแสงเรย์

ในท้ายที่สุด เราบันทึกภาพที่ปรับเปลี่ยนแล้วเป็นทั้ง PNG และ PSD

นี่เป็นตัวอย่างพื้นฐานเท่านั้นเกี่ยวกับวิธีการสร้างเอฟเฟ็กต์บนเลเยอร์โดยใช้ Aspose.PSD สำหรับ Python คุณสามารถปรับปรุงเอฟเฟ็กต์ต่อไปได้อย่างอิสระโดยการปรับค่าพารามิเตอร์และคุณสมบัติของแต่ละเอฟเฟ็กต์ ไลบรารีมีตัวเลือกและการตั้งค่าต่าง ๆ ให้คุณสร้างเอฟเฟ็กต์ที่ซับซ้อนและน่าสายตามากขึ้น

หวังว่าบทความนี้จะช่วยให้คุณเข้าใจวิธีการสร้างเอฟเฟ็กต์บนเลเยอร์ใน Aspose.PSD สำหรับ Python ไม่ต้องลังเลที่จะสำรวจเอกสารของไลบรารีเพื่อดูรายละเอียดและตัวอย่างเพิ่มเติม

อ่านตัวอย่างเต็มได้ที่นี่

## **ตัวอย่าง**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-Psd-layer-effects.py" >}}