---
title: تحويل مساحة الألوان لصيغة JPEG من خلال ملفات ICC Profiles
type: docs
weight: 60
url: /ar/net/color-space-conversion-for-jpeg-through-icc-profiles/
---

## **إدارة الألوان لتنسيق JPEG**

يناقش هذا المقال استخدام ملفات ICC profiles لأداء إدارة مساحة الألوان أثناء التعامل مع تنسيق JPEG باستخدام واجهات برمجة التطبيقات لـ Aspose.PSD. مساحة اللون الداخلية لـ JPEG هي YCbCr ومع ذلك يمكن لهذا التنسيق أيضًا استيعاب مساحات الألوان الرمادي، RGB، CMYK وYCCK لتخزين بيانات الصورة. واجهات برمجة التطبيقات لـ Aspose.PSD تعمل أساسًا في مساحة RGB لذلك يجب للواجهة البرمجية القيام بتحويل المساحات اللونية ذهابًا وإيابًا للتعامل بشكل صحيح مع ملفات JPEG. يمكن أن يتم تحويل المساحات اللونية من الرمادي إلى RGB ومن YCbCr إلى RGB باستخدام التحويلات الرياضية ولكن لا يمكن بسهولة تحويل المساحات CMYK وYCCK إلى مساحة RGB.

يجب أن تقوم واجهات برمجة التطبيقات لـ Aspose.PSD بتنفيذ تحويل ألوان مباشر من RGB إلى CMYK لصور JPEG التي تحتوي على مساحة ألوان CMYK. من ناحية أخرى، تتطلب الصور التي تحتوي على مساحة ألوان YCCK تحويل ألوان من RGB إلى CMYK ثم إلى YCCK، حيث يتم استخدام تحويل CMYK إلى YCCK والذي يطبق تحويل ITU-R BT.601 على القنوات الثلاثة الأولى، متركاً القناة K دون تغيير. بإختصار، يجب على واجهات برمجة التطبيقات لـ Aspose.PSD تنفيذ تبادل المساحة اللونية من RGB إلى CMYK للصور الـ CMYK و YCCK، ويتم تنفيذ مثل هذه التحويلات بمساعدة ملفات ICC profiles التي تكون أساساً جداول بحث تصف خصائص لون معين وتساعد في تحويل الألوان.

## **ملفات ICC Profiles**
آلية تحويل ICC تستخدم "الملفات الشخصية" التي تختر للمساحة اللونية المصدرية لمساحات الألوان CIEXYZ أو CIELAB غير المعتمدة عن الجهاز. يمكن لـ Aspose.PSD تحويل البيانات إلى مساحة ألوان حسب الحاجة باستخدام هاتين المساحتين مع الملفات الشخصية الإضافية. وبالتالي، للتحويل باستخدام ICC يحتاج المستخدم إلى توفير ملفي ملف شخصي - الأول يكون ملف شخصي RGB للوصول إلى مساحة اللون الداخلية CIE والثاني يكون ملف شخصي CMYK للحصول على خصائص الألوان CMYK. من أجل تحقيق تحويل CMYK إلى RGB، يجب على المستخدم تبديل الملفات الشخصية، أي استخدام الملف الشخصي CMYK كملف شخصي مصدر والملف الشخصي RGB كملف شخصي وجهة.


## **تحويل الألوان لصيغة JPEG من خلال ملفات ICC Profiles**
تخفي واجهات برمجة التطبيقات لـ Aspose.PSD التفاصيل، وتوفر آلية سهلة الاستخدام لتحديد ملفات ICC عبر فئة [JpegOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions). علاوة على ذلك، تستخدم Aspose.PSD ملفات العينات المضمنة ل SWOP و CMYK و sRGB في نواة الشفرة لذا في معظم الحالات الاستخدام الشائع، لا يحتاج المستخدم للبحث عن أي ملفات محددة. هناك عيب في مثل هذه التصحيحات، وهو أن عمليات تحويل مساحات الألوان كهذه لا يمكن التراجع عنها لأننا لا يمكن أن نتوقع الحصول على نفس اللون بعد التحويل من RGB إلى CMYK إلى RGB بسبب عدم توافق مساحات الألوان والملفات الشخصية المختلفة. توضح مقتطفات الشفرة التالية استخدام Aspose.PSD لـ API .NET لتحديد ملفات الملف الشخصي RGB و CMYK لصورة JPEG YCCK. في المثال أدناه تم تغيير ملفات الملف الشخصي RGB و CMYK وتم حفظ الصورة في مساحة الألوان YCCK. يرجى ملاحظة أن خصائص الـ [RgbColorProfile](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions/properties/rgbcolorprofile) و [CmykColorProfile](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions/properties/cmykcolorprofile) ستعمل على تغيير بيانات البكسل لمساحة الألوان YCCK. جميع المساحات اللونية الأخرى لا تحصل على ملفات الملف الشخصي لتحديث البيانات الملونة.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ColorConversionUsingICCProfiles-ColorConversionUsingICCProfiles.cs" >}}


إذا لم يتم تعيين ملفات شخصية فإن واجهات برمجة التطبيقات لـ Aspose.PSD لنظام .NET ستستخدم الملفات الشخصية الافتراضية بدلاً من ذلك. يستخدم المثال أدناه خصائص ملفات الوجهة التي تغير مساحة الألوان الوجهة لمعظم الصور JPEG.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ColorConversionUsingDefaultProfiles-ColorConversionUsingDefaultProfiles.cs" >}}