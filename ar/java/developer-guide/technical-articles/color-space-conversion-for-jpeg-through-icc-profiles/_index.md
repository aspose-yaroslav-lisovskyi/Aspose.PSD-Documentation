---
title: تحويل مساحة الألوان لصيغة JPEG من خلال ملفات ICC الشخصية
type: docs
weight: 50
url: /ar/java/color-space-conversion-for-jpeg-through-icc-profiles/
---

## **إدارة الألوان لتنسيق JPEG**

تناقش هذه المقالة استخدام ملفات ICC الشخصية لأداء إدارة مساحة الألوان أثناء التعامل مع تنسيق JPEG باستخدام واجهات برمجة التطبيقات Aspose.PSD. مساحة الألوان الداخلية لصيغة JPEG هي YCbCr، ومع ذلك، يمكن لهذا التنسيق أيضًا استيعاب مساحات ألوان الصورة مثل Grayscale، RGB، CMYK، وYCCK لتخزين بيانات الصورة. تعمل واجهات برمجة التطبيقات Aspose.PSD بشكل رئيسي في مساحة RGB لذلك يجب على واجهة البرمجة تنفيذ عمليات التحويل من وإلى مساحة الألوان لتمكينها من التعامل بشكل صحيح مع ملفات JPEG. يمكن إجراء تحويل من Grayscale إلى RGB ومن YCbCr إلى RGB باستخدام التحويلات الرياضية، ولكن لا يمكن سهلًا تحويل مساحات الألوان CMYK وYCCK إلى مساحة RGB.

واجهات برمجة التطبيقات Aspose.PSD يجب أن تنفذ تحويلًا مباشرًا من RGB إلى CMYK لصور JPEG التي تحتوي على مساحة ألوان CMYK. من ناحية أخرى، تحتاج الصور التي تحوي على مساحة ألوان YCCK إلى تحويل الألوان من RGB إلى CMYK ثم YCCK، حيث يستخدم تحويل CMYK إلى YCCK تحويل ITU-R BT.601 المتحدث على القنوات الثلاث الأولى، مع الاحتفاظ بقناة k. بإختصار، يجب على واجهة برمجة التطبيقات Aspose.PSD أداء تبديل بين مساحات الألوان RGB و CMYK لكلاً من الصور CMYK & YCCK، ويتم تنفيذ هذه التحويلات بمساعدة ملفات ICC التي تعد جداول بحث تصف خصائص اللون وتساعد في تحويل الألوان.

## **ملفات ICC الشخصية**
آلية تحويل الـ ICC تستخدم "ملفات شخصية" والتي تعيد تعيين مساحة اللون المصدر إلى مساحات ألوان CIELAB أو CIEXYZ غير القابلة للتصميم. يمكن لـ Aspose.PSD تحويل البيانات إلى مساحة الألوان حسب الحاجة باستخدام هاتين المساحتين اللونيتين مع ملفات شخصية إضافية. لذا، يجب على المستخدم توفير ملفين - أحد ملف RGB للوصول إلى مساحة الألون المركزية CIE الداخلية والآخر ملف CMYK للوصول إلى خصائص اللون CMYK. من أجل تحقيق تحويل CMYK إلى RGB، يجب على المستخدم تبديل الملفات، أي؛ استخدام ملف CMYK كملف مصدر وملف RGB كملف وجهة.

## **تحويل الألوان لصيغة JPEG من خلال ملفات ICC الشخصية**
تخفي واجهات برمجة التطبيقات Aspose.PSD التفاصيل، مما يوفر آلية سهلة الاستخدام لتحديد ملفات ICC عبر فئة JpegOptions. وعلاوة على ذلك، يستخدم Aspose.PSD ملفات العينات لألوان SWOP CMYK وsRGB المضمنة في نواة النظام الأساسية لذا في معظم حالات الاستخدام الشائعة، لا يلزم للمستخدم البحث عن أي ملفات محددة. يوجد عيب في مثل هذه التصحيحات، ألا وهو؛ أن عمليات تحويل مساحة الألوان هذه لا يمكن عكسها لأنه لا يمكن توقع الحصول على نفس اللون بعد تحويل من RGB إلى CMYK ثم إلى RGB بسبب عدم التوافق بين مساحات الألوان وملفات الألوان المختلفة. يوضح مقتطف الكود التالي استخدام Aspose.PSD لواجهة برمجة التطبيقات في Java لتحديد ملفات الألوان RGB و CMYK لصورة JPEG بمساحة الألوان YCCK. في المثال أدناه، تم تغيير ملفات الألوان RGB و CMYK وتم حفظ الصورة في مساحة الألوان YCCK. يرجى ملاحظة أن خصائص RgbColorProfile و CmykColorProfile ستعمل لتغيير بيانات البكسل لمساحة ألوان YCCK. جميع المساحات اللونية الأخرى لا تجلب ملفات الألوان لتحديث بيانات الألوان.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ColorConversionUsingICCProfiles-ColorConversionUsingICCProfiles.java" >}}



إذا لم يتم تحديد ملفات شخصية، ستستخدم واجهة برمجة التطبيقات Aspose.PSD for Java الملفات الشخصية الافتراضية بدلاً من ذلك. يستخدم المثال أدناه خصائص ملفات الوجهة التي تغيّر مساحة اللون الوجهة لمعظم صور JPEG.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ColorConversionUsingDefaultProfiles-ColorConversionUsingDefaultProfiles.java" >}}