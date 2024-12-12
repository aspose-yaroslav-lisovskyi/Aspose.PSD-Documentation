---
title: استخدام واجهة برمجة التطبيقات الرسومية لتحرير الطبقات في ملفات PSD
weight: 100
type: docs
description: مثال على استخدام واجهة برمجة التطبيقات الرسومية في Aspose.PSD للجافا
keywords: [تحديث الطبقة, رسم دائرة, رسم إليبس, رسم دائرة ملأ, رسومات, واجهة برمجة التطبيقات PSD, جافا, عينة الكود]
url: /ar/java/graphics-api/
---

## **نظرة عامة**
للبدء، يتعين عليك تحميل ملف PSD باستخدام الطريقة Image.load() أو إنشاء صورة Psd Image من الصفر. استخدم المتغير inputFile لتمثيل مسار ملف PSD الخاص بك، وحدد أي خيارات تحميل بواسطة loadOpt، إن لزم الأمر.

بعد ذلك، قم بالوصول إلى الطبقة الأولى في صورة الـ PSD باستخدام بنية psdImage.getLayers()[0] للحصول على مرجع إلى كائن الطبقة للتلاعب به.

لتحرير الطبقة، أنشئ كائن Graphics عن طريق تمرير الطبقة كمعلمة. يوفر هذا الكائن طرقًا مختلفة لرسم الأشكال وتطبيق الفرش.

يتم استخدام كائن Pen لتحديد لون وسمك حدود الأشكال. بالمثل، يتم استخدام الفرش مثل LinearGradientBrush لتحديد ألوان التعبئة.

ارسم الأشكال على الطبقة باستخدام طرق مثل graphics.drawEllipse() لرسم الأشكال المحددة و graphics.fillEllipse() لملؤها.

بعد إجراء التغييرات المطلوبة على الطبقة، احفظ الصورة المعدلة من PSD باستخدام psdImage.save().

بالإضافة إلى ذلك، يمكنك حفظ الصورة المعدلة بتنسيقات أخرى مثل PNG باستخدام الخيارات المناسبة.

هذا هو كل شيء! لقد استخدمت بنجاح واجهة برمجة التطبيقات الرسومية ل Aspose.PSD للجافا لتحرير الطبقات في ملف PSD. استكشف المزيد من الميزات والوظائف لمكتبة Aspose.PSD لتعزيز قدرات تحرير الصور الخاصة بك.

يرجى مراجعة المثال الكامل.

## **مثال**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-Psd-graphics-api.java" >}}