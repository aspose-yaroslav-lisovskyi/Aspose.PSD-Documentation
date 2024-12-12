---
title: استعداد التلاعب بمرشح الذكاء في Aspose.PSD for سي شارب
weight: 100
type: docs
description: أمثلة حول كيفية استخدام مرشحات الذكاء في ملف PSD
keywords: [مرشح ذكي, إضافة ضوضاء, ضبابية جاوسية, تحسين, مرشح, مرشح PSD, واجهة برمجة التطبيقات لـ PSD, C#, سي شارب, عينة الشفرة]
url: /ar/net/smart-filters/
---

## لمحة

هناك ثلاث طرق لتطبيق مرشحات ذكية في Aspose.PSD for C#.

### تطبيق المرشح مباشرة

تظهر هذه الوميضة كيفية تطبيق المرشحات الذكية مباشرة في Aspose.PSD لـ C#.

أولاً، حدد ملف PSD المصدر، وملف الإخراج للصورة الأصلية، وملف الإخراج للصورة المُحدّثة.

ثم، قم بتحميل صورة PSD باستخدام الأسلوب `Image.Load` وقم بتحويلها إلى كائن `PsdImage`.

احفظ الصورة الأصلية باستخدام الأسلوب 'Save' مع تحديد اسم الملف للإخراج.

أنشئ كائن `SharpenSmartFilter`، الذي يمثّل مرشح الذكاء الذي سيتم تطبيقه.

استرجع الطبقات العادية من صورة PSD باستخدام `psdImage.Layers[1]`.

قم بتطبيق 'sharpenFilter' على الطبقة العادية ثلاث مرات في حلقة.

أخيرًا، احفظ الصورة المُحدّثة باستخدام الأسلوب 'Save' مع تحديد اسم الملف للإخراج.

يوضح هذا الكود كيفية تطبيق مرشحات ذكية مباشرة في Aspose.PSD لـ C#. باستخدام كائنات المرشح المناسبة وتطبيقها على الطبقات المرغوبة، يمكنك تحقيق التأثيرات المرغوبة على صورك.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "DirectlyApplySmartFilter-DirectlyApplySmartFilter.cs" >}}

### تلاعب بمرشحات الذكاء في الكائنات الذكية

تُظهر هذه الوميضة كيفية تلاعب بمرشحات الذكاء داخل الكائنات الذكية.

أولاً، حدد ملف PSD المصدر، وملف الإخراج للصورة الأصلية، وملف الإخراج للصورة المُحدّثة.

قم بتحميل صورة PSD باستخدام الأسلوب `Image.Load` وقم بتحويلها إلى كائن `PsdImage`.

احفظ الصورة الأصلية باستخدام الأسلوب 'Save' مع تحديد اسم الملف للإخراج.

قم بتحويل الطبقة الثانية من صورة PSD إلى كائن `SmartObjectLayer`.

عدّل مرشحات الذكاء. تُظهر هذه الوميضة العمل مع `GaussianBlurSmartFilter` و `AddNoiseSmartFilter`.

بالنسبة لـ `GaussianBlurSmartFilter`، قم بتحديث قيم المرشح بما في ذلك النصف القطري، ووضع الدمج، والشفافية، وحالة التمكين.

بالنسبة لـ `AddNoiseSmartFilter`، قم بتعيين توزيع الضوضاء إلى `NoiseDistribution.UNIFORM`.

أضف عناصر مرشح جديدة إلى الطبقة الذكية: مرشح جديد آخر لـ `GaussianBlurSmartFilter` و `AddNoiseSmartFilter`.

قم بتطبيق التغييرات باستخدام الأسلوب 'UpdateResourceValues'.

قم بتطبيق المرشحات مباشرة على الطبقة وعلى قناع الطبقة باستخدام الأساليب 'Apply' و 'ApplyToMask' على التوالي.

احفظ الصورة المحدثة باستخدام الأسلوب 'Save' مع تحديد اسم الملف للإخراج.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "ManipulatingSmartFiltersInSmartObjects-ManipulatingSmartFiltersInSmartObjects.cs" >}}

### تطبيق مرشحات ذكية على قناع الطبقة

تعتبر مرشحات الذكاء أداة تحرير صور قوية تتيح للمستخدمين تطبيق مرشحات وتأثيرات مختلفة. تقنية مثيرة للاهتمام هي تطبيقها على القناع، الذي يمكنه التحكم بدقة في المناطق المتأثرة بالمرشح.

القناع هو صورة مدرجة رمادية تحدد شفافية بعض مناطق الصورة، وتطبيق مرشحات، تعديلات، أو تأثيرات انتقائيًا.

عند تطبيق مرشحات ذكية على القناع، يتم تطبيق المرشحات فقط على المناطق المحددة بواسطة القناع. يسمح هذا التحكم الدقيق بتلاعب بشدة المرشح ونطاقه.

للمزيد من المعلومات المفصلة والأمثلة، راجع [وثائق Aspose.PSD for C#](https://docs.aspose.com/psd/net/).