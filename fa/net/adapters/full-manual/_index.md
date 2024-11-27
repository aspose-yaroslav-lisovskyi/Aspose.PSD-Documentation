---
title: دستی کامل Aspose.PSD برای آداپتور‌های .NET
type: docs
weight: 10
url: /fa/net/adapters/full-manual
keywords: آداپتور دستی PSD PSB AI WebP SVG PNG JPEG TIFF GIF BMP راهنمای شروع سریع
description: دستی کامل Aspose.PSD برای آداپتور‌ها.
---

## مرور

این یک دستی کامل در مورد نحوه کار با آداپتورهای Aspose.PSD برای گسترش قابلیت‌های Aspose.PSD است.
آداپتورها بسته‌های ویژه Nuget هستند که امکان ادغام بی‌درز Aspose.PSD با سایر محصولات Aspose را فراهم می‌کنند و به شما این امکان را می‌دهند که فایل‌های خود را به فرمت‌های مختلفی که بدون نیاز به نوشتن کد اضافی ادغامی می‌توان انجام داد، بصورت آسان برون‌بری کنید.

## اعمال لایسنس‌ها

لطفا مقاله [کامل در مورد اعمال لایسنس‌ها](psd/fa/net/adapters/license) برای آداپتورها را بررسی کنید.

{{% alert color="primary" %}} 
لطفا توجه داشته باشید که برای استفاده از آداپتورها، لایسنس‌های هم Aspose.PSD و هم adaptors لازم است. 
{{% /alert %}} 

می‌توانید از این نمونه برای اعمال لایسنس استفاده کنید:
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Aspose-PSD-Adapters-CSharp-License.cs" >}}

موارد بهتر است یکبار لایسنس را در ماژول مقدماتی پروژه‌ی خود اعمال کنید.

## مرجع آداپتور‌های Aspose.PSD

اولین چیزی که باید انجام دهید، ارجاع دادن به Aspose.PSD.Adapters.Imaging از [Nuget](https://www.nuget.org/aspose.psd.adapters.imaging) یا دانلود آنها از [صفحه انتشارات Aspose](https://releases.aspose.com/psd/net/)(در حال حاضر اداپتورها به صورت جداگانه به عنوان فایل دودویی در بسته اصلی انتشار آمده‌اند) به پروژه‌ی خود.

![مراجع مورد نیاز](references.png)

ممکن است شما نیاز داشته‌باشید که به بسته‌های اضافی دیگر هم ارجاع دهید

## فعال‌سازی لودرها و صادرکننده‌های adaptees

### فعال‌سازی آداپتورها
وقتی نیاز به استفاده از آداپتورها داشتید، از کد زیر استفاده کنید:
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Adapters-CSharp-Enable-Adapters.cs" >}}

### غیرفعال‌سازی آداپتورها
در فرآیند توسعه ممکن است با مواجهه اوضاعی رو به رو شوید که نیاز است که آداپتورها غیرفعال باشند. این حالت رایج است اگر بخواهید در قسمت کدی از لودرهای Aspose.PSD استفاده کرده و در قسمت دیگری از لودرهای Adaptees را استفاده کنید. در این حالت فقط کد زیر را استفاده کنید:
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Adapters-CSharp-Disable-Adapters.cs " >}}

## بارگذاری تصاویر با استفاده از آداپتورها

با استفاده از آداپتورها می‌توانید [فرمت‌های محبوبی که توسط Aspose.PSD پشتیبانی نمی‌شود]((/fa/net/adapters/load-unsupported-formats)) مانند SVG و WebP را بارگذاری کنید.

### استفاده ساده
برای بارگذاری، فقط از کد زیر استفاده کنید:
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Adapters-CSharp-Add-Imaging-Adapters-Loading-Unsupported-Formats.cs" >}}

### استفاده میانی برای پردازش تصویر پیچیده
اگر نیاز به مشخص کردن گزینه‌های اضافی موجود در Adaptee دارید، لطفا مثال زیر را بررسی کنید:
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Aspose-PSD-Adapters-CSharp-Full-Manual-Complex-Loading.cs" >}}

می‌توانید با استفاده از همه ویژگی‌های Imaging، با تصویر SVG کار کنید و سپس با یک فراخوانی متد آن را بیرون‌بری کنید.

## صادرکردن تصاویر با استفاده از آداپتورها

زمانی که نیاز نباشد [فرمتی که پشتیبانی نمی‌شود](/fa/net/adapters/load-unsupported-formats) را باز کنید، بلکه [به آن اطلاع دهید](/fa/net/adapters/export-to-unsupported-formats)، در این حالت‌ها باید صادرکننده‌ها را فعال کنید و از کد زیر استفاده کنید:
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Adapters-CSharp-Add-Imaging-Adapters-Exporting-to-Unsupported-Formats.cs" >}}

## نتیجه‌گیری

استفاده از آداپتورهای Aspose.PSD برای بارگذاری و صادرکردن فایل‌ها برای توسعه‌دهندگان تغییرزا است. این بسته‌های قدرتمند Nuget به شما امکان ادغام بی‌درز Aspose.PSD با سایر محصولات Aspose را می‌دهند و به راحتی از همیشه برای باز و کار با فرمت‌های فایل پشتیبانی نشده بدون نیاز به نوشتن کد ادغامی آسان‌تر می‌سازند. با آداپتورهای Aspose.PSD، می‌توانید زمان و تلاش خود را صرفه‌جویی کنید با حذف نیاز به کد اضافی و فرآیندهای تبدیل دستی. برای بارگذاری یا صادرکردن فایل‌ها، آداپتورهای Aspose.PSD یک راه‌حل مناسب و کارآمد را ارایه می‌دهند که امکانات جدیدی برای پروژه‌های شما باز می‌کند. تجربه قدرت آداپتورهای Aspose.PSD‎ را درک کنید و فرآیند توسعه خود را به سطح بعد ببرید.