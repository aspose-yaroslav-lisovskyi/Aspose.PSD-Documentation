---
title: استفاده از لایه تنظیم برای ارتقاء PSD
weight: 100
type: docs
description: نمونه های استفاده از لایه تنظیم از طریق Aspose.PSD برای جاوا
keywords: [لایه تنظیم, ارتقاء عکس, تنظیم منحنی ها, ارتقاء سطوح, معکوس, فیلتر عکس, psd api, جاوا, نمونه کد]
url: fa/java/adjustment-layer-enhancement/
---

## **بررسی کلی**

در این مقاله به ویرایش لایه‌های تنظیم در Aspose.PSD برای جاوا پرداخته خواهد شد. لایه‌های تنظیم ویژگی‌های قدرتمندی در ویرایش تصویر هستند که به شما امکان می‌دهند تغییرات غیر از خراب کننده روی تصاویر خود اعمال کنید. Aspose.PSD یک مجموعه جامع از کلاس‌های لایه‌های تنظیم فراهم کرده است که شما می‌توانید از آن‌ها برای تغییر جوانب مختلف تصاویر خود استفاده کنید.

برای نشان دادن ویرایش لایه‌های تنظیم، یک قطعه کد نمونه را در پایان صفحه ارائه می‌دهیم که یک تصویر PSD را بارگذاری کرده و تنظیمات مختلفی روی لایه‌های آن اعمال می‌کند.

در قطعه کد زیر، با شروع به بارگذاری تصویر PSD با استفاده از متد load() در PsdImage. شروع می‌کنیم. سپس، تنظیمات ذخیره فایل‌های PNG خروجی را تنظیم می‌کنیم. کلاس PngOptions به ما امکان مشخص کردن نوع رنگ برای تصویر خروجی را می‌دهد.

سپس، ما از طریق هر لایه در تصویر PSD حرکت کرده و نوع آن را با استفاده از متد isAssignable() بررسی می‌کنیم. اگر لایه از نوع خاصی باشد، آن را به آن نوع با استفاده از متد cast() تبدیل می‌کنیم و تنظیم مورد نظر را اعمال می‌کنیم. به عنوان مثال، ما باعث تنظیم روشنایی و تضاد یک BrightnessContrastLayer می‌شویم، سطوح یک LevelsLayer را تغییر می‌دهیم، یک نقطه منحنی را به یک CurvesLayer اضافه می‌کنیم و غیره.

شما می‌توانید کدهای اضافی برای اعمال تنظیمات دیگر به لایه‌های مربوطه آن‌ها اضافه کنید. Aspose.PSD یک دسته گسترده از کلاس‌های لایه‌های تنظیم را فراهم می‌کند، مانند ExposureLayer, HueSaturationLayer, ColorBalanceAdjustmentLayer, BlackWhiteAdjustmentLayer, PhotoFilterLayer, ChannelMixerLayer, InvertAdjustmentLayer, PosterizeLayer, ThresholdLayer, SelectiveColorLayer و غیره.

سرانجام، ما تصویر ویرایش شده را با استفاده از متد save() کلاس PsdImage ذخیره می‌کنیم.

این یک مرور اولیه از چگونگی ویرایش لایه‌های تنظیم در Aspose.PSD برای جاوا است. شما می‌توانید تنظیمات را بر اساس نیازهای خود سفارشی کنید و گزینه‌های مختلف موجود در مستندات API را بررسی کنید.

لطفا نمونه کامل را در زیر بررسی کنید.

## **نمونه**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-adjustment-layer-enhancement.java" >}}