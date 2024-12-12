---
title: مثال على استخدام طبقات المجموع في Aspose.PSD للجافا
weight: 100
type: docs
description: استخدام طبقة المجموع في ملف PSD عبر الجافا
keywords: [طبقة مجموع, طبقة مجموع, إضافة طبقة إلى المجموع, واجهة برمجة تطبيقات PSD, جافا, مثال على الكود]
url: /ar/java/psd-group-layer/
---

## **نظرة عامة**

يُعزز استخدام طبقات المجموع في Aspose.PSD للجافا قدرتك على إدارة وتنظيم الطبقات داخل صورة PSD بفعالية. تُمكن طبقات المجموع، المعروفة أيضًا باسم طبقات المجلد، من تجميع العديد من الطبقات وتطبيق التحويلات أو التأثيرات جماعيًا.

للبدء، يجب عليك إنشاء صورة PSD جديدة باستخدام طريقة PsdImage.create(). ثم، قم بتهيئة كائن LayerGroup جديد من خلال طريقة addLayerGroup لكائن PsdImage. قدم اسم الطبقة المجموعية المرغوب فيها ("Folder")، حدد مؤشر الإدراج (0)، وقم بتعيين علم منطقي يشير إلى رؤيتها (True).

بعد ذلك، قم بإنشاء طبقتين وقم بتحديد أسمائهم عبر طريقة setDisplayName. أضف هذه الطبقات إلى طبقة المجموع باستخدام طريقة addLayer.

للوصول إلى الطبقات داخل المجموعة، استخدم خاصية layers لكائن LayerGroup. تأكد من أن أسماء العرض للطبقة الأولى والثانية في المجموعة هي "Layer 1" و "Layer 2" على التوالي.

بمجرد أن تكون قد قمت بتلاعب في طبقات المجموع، احفظ الصورة PSD المعدلة باستخدام طريقة save لكائن PsdImage.

يشكل هذا مثالًا أساسيًا لمساعدتك في التعرف على كيفية العمل مع طبقات المجموع باستخدام Aspose.PSD للجافا. تقدم المكتبة مجموعة كبيرة من الميزات المتقدمة لتنظيم الطبقات وتحويلها داخل صور PSD. لمزيد من التفاصيل والأمثلة حول استغلال طبقات المجموع ووظائف أخرى للمكتبة، راجع توثيق Aspose.PSD للجافا.

للعمل مع طبقات المجموع في Aspose.PSD للجافا، استخدم فئة LayerGroup. أدناه مقتطف كود يوضح كيفية إنشاء طبقة مجموع، إضافة طبقات إليها، وحفظ الصورة PSD المعدلة.

يرجى الرجوع إلى المثال الكامل المقدم.

## **المثال**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-psd-group-layer.java" >}}