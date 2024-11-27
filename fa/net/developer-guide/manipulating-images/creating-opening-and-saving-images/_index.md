---
title: ایجاد، باز کردن و ذخیره تصاویر
type: docs
weight: 30
url: /fa/net/creating-opening-and-saving-images/
---

## **ایجاد فایل‌های تصویری**
Aspose.PSD برای .NET به توسعه‌دهندگان امکان ایجاد تصاویر خودشان را می‌دهد. از متد ایجاد استاتیکی که توسط کلاس تصویر ارائه شده استفاده کنید تا تصاویر جدید ایجاد کنید. کافی است یک شیء مناسب از یکی از کلاس‌های فضای نام ImageOptions برای فرمت تصویر خروجی مورد نظر عرضه کنید. برای ایجاد یک فایل تصویر، ابتدا یک نمونه از یکی از کلاس‌های فضای نام ImageOptions ایجاد کنید. این کلاس‌ها فرمت تصویر خروجی را مشخص می‌کنند. کلاس‌هایی از فضای نام ImageOptions زیر وجود دارند (توجه داشته باشید که تنها خانواده فرمت‌های فایل PSD در حال حاضر برای ایجاد پشتیبانی می‌شوند):

[PsdOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/psdoptions) تنظیم‌های برای ایجاد یک فایل PSD را مشخص می‌کند. فایل‌های تصویر می‌توانند با تنظیم یک مسیر خروجی یا توسط تنظیم یک جریان ایجاد شوند.
### **ایجاد با تنظیم مسیر**
از [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) فضای نام PsdOptions ایجاد کنید و ویژگی‌های مختلف را تنظیم کنید. مهمترین ویژگی برای تنظیم ویژگی منبع است. این ویژگی مشخص می‌کند که داده‌های تصویر در کجا ذخیره شده‌اند (در یک فایل یا یک جریان). در مثال زیر، منبع یک فایل است. پس از تنظیم ویژگی‌ها، شیء را به یکی از متد‌های استاتیک [Create](https://reference.aspose.com/psd/net/aspose.psd/image/methods/create) همراه با پارامتر‌های پهنا و ارتفاع گذرانید. پهنا و ارتفاع به پیکسل تعریف شده‌اند.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CreatingbySettingPath-CreatingbySettingPath.cs" >}}
### **ایجاد با استفاده از جریان**
فرایند ایجاد یک تصویر با استفاده از یک جریان همانند استفاده از یک مسیر است. تنها تفاوت این است که شما باید یک نمونه از [StreamSource](https://reference.aspose.com/psd/net/aspose.psd.sources/streamsource) ایجاد کنید که با انتقال یک شیء Stream به سازنده ایجاد شده و اختصاص دادن آن به ویژگی منبع مشغول شود.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CreatingUsingStream-CreatingUsingStream.cs" >}}
## **باز کردن فایل‌های تصویری**
توسعه‌دهندگان می‌توانند از API Aspose.PSD برای .NET برای باز کردن فایل‌های تصویر PSD موجود برای اهداف مختلف مانند افزودن افکت به تصویر یا تبدیل یک فایل موجود به یک فرمت دیگر استفاده کنند. هر چه اهداف باشد، Aspose.PSD دو روش استاندارد برای باز کردن فایل‌های موجود فراهم می‌کند: از فایل یا از یک جریان.
### **باز کردن از دیسک**
تصویر را با انتقال مسیر و نام فایل به عنوان پارامتر به متد استاتیک Load ارائه شده توسط کلاس Image باز کنید.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SavingtoDisk-SavingtoDisk.cs" >}}
### **باز کردن با استفاده از یک جریان**
گاهی اوقات تصویری که می‌خواهیم باز کنیم به صورت یک جریان ذخیره شده است. در چنین مواردی از نسخه با بارگذاری اضافی متد Load استفاده کنید. این متد یک شیء Stream را به عنوان آرگومان قبول می‌کند تا تصویر را باز کند.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-LoadingFromStream-LoadingFromStream.cs" >}}
### **بارگیری تصویر به عنوان لایه**
این مقاله استفاده از Aspose.PSD برای بارگیری یک تصویر به عنوان یک لایه را نشان می‌دهد. APIهای Aspose.PSD متداول و آسانی را برای دستیابی به این هدف ارائه کرده‌اند. Aspose.PSD شیء PsdImage متد AddLayer را از کلاس PsdImage برای اضافه کردن یک تصویر به یک فایل PSD به عنوان یک لایه ارائه کرده است.

مراحل بارگیری تصویر به عنوان لایه به شرح زیر است:

- ایجاد یک نمونه از تصویر با استفاده از کلاس PsdImage با پهنا و ارتفاع مشخص.
- بارگیری یک فایل PSD به عنوان تصویر با استفاده از متد کارخانه Load ارائه شده توسط کلاس Image.
- ایجاد یک نمونه از کلاس Layer و اختصاص دادن لایه تصویر PSD به آن.
- اضافه کردن لایه ایجاد شده با استفاده از متد AddLayer ارائه شده توسط کلاس PsdImage
- ذخیره نتایج.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-LoadImageToPSD-LoadImageToPSD.cs" >}}
### **بارگیری تصویر به عنوان لایه از یک جریان**
این مقاله استفاده از Aspose.PSD برای بارگیری تصویر به عنوان یک لایه از یک جریان را نشان می‌دهد. برای بارگیری یک تصویر از یک جریان، به سادگی یک شیء جریانی که حاوی یک تصویر است، به سازنده کلاس Layer منتقل کنید. لایه ایجاد شده را با استفاده از متد AddLayer ارائه شده توسط کلاس PsdImage اضافه کنید و نتایج را ذخیره کنید.


در زیر کد نمونه آورده شده است.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Opening-LoadingImageFromStream-LoadingImageFromStream.cs" >}}
## **ذخیره فایل‌های تصویری**
Aspose.PSD به شما امکان می‌دهد فایل‌های تصویری را از ابتدا ایجاد کنید. همچنین امکان ویرایش فایل‌های تصویری موجود را فراهم می‌کند. هنگامی که تصویر ایجاد یا تغییر داده شود، فایل معمولا به دیسک ذخیره می‌شود. Aspose.PSD برای شما متد‌هایی را برای ذخیره تصاویر در دیسک با تعیین مسیر یا استفاده از یک شیء Stream فراهم می‌کند.
### **ذخیره در دیسک**
کلاس Image یک شیء تصویر را نمایان می‌کند، بنابراین این کلاس تمام ابزارهای لازم برای ایجاد، بارگیری و ذخیره یک فایل تصویر ارائه می‌دهد. از متد Save کلاس Image برای ذخیره تصاویر استفاده کنید. یک نسخه با بارگذاری بیش از حد از متد ذخیره، محل فایل را به عنوان یک رشته قبول می‌کند.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SavingtoDisk-SavingtoDisk.cs" >}}
### **ذخیره در یک جریان**
نسخه تغییر یافته از متد Save شیء Stream را به عنوان آرگومان قبول می‌کند و فایل تصویر را در جریان ذخیره می‌کند.

اگر تصویر با تعیین هرکدام از CreateOptions در سازنده Image ایجاد شود، تصویر به‌طور خودکار به مسیر یا جریانی که در زمان مقدماتی‌سازی کلاس Image توسط فراخوانی متد Save که هیچ پارامتری را قبول نمی‌کند ذخیره شده است، ذخیره می‌شود.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SavingtoStream-SavingtoStream.cs" >}}
### **تنظیم برای جایگزین کردن فونت‌های گم شده**
توسعه‌دهندگان می‌توانند از API Aspose.PSD برای .NET برای بارگیری فایل‌های تصویر PSD موجود برای اهداف مختلف استفاده کنند، به عنوان مثال برای تنظیم نام پیش‌فرض فونت هنگام ذخیره سندات PSD به صورت یک تصویر raster (در فرمت‌های PNG، JPG و BMP). این فونت پیش‌فرض باید برای همه فونت‌های گم شده (فونت‌هایی که در سیستم عامل فعلی یافت نمی‌شوند) استفاده شود. پس از اینکه تصویر اصلاح شد، فایل به دیسک ذخیره خواهد شد.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SettingforReplacingMissingFonts-SettingforReplacingMissingFonts.cs" >}}