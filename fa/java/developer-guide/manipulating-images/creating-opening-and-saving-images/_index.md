---
title: ایجاد، بازکردن و ذخیره تصاویر
type: docs
weight: 30
url: /fa/java/creating-opening-and-saving-images/
---

## **ایجاد فایل‌های تصویری**
Aspose.PSD برای Java به توسعه‌دهندگان اجازه می‌دهد تا تصاویر خود را ایجاد کنند. از متد Create استاتیک کلاس Image برای ایجاد تصاویر جدید استفاده کنید. تمامی چیزی که باید انجام دهید ارائه شی مربوطه یکی از کلاس‌های از فضای نام ImageOptions برای فرمت تصویر خروجی مورد نظر است. برای ایجاد یک فایل تصویر، ابتدا یک نمونه از یکی از کلاس‌های از فضای نام ImageOptions بسازید. این کلاس‌ها فرمت تصویر خروجی را تعیین می‌کنند. در زیر چند کلاس از فضای نام ImageOptions آمده است (توجه داشته باشید که فقط خانواده فرمت‌های فایل PSD در حال حاضر برای ایجاد پشتیبانی می‌شوند):

PsdOptions تنظیمات برای ایجاد یک فایل PSD را تعیین می‌کند. فایل‌های تصویری می‌توانند با تنظیم یک مسیر خروجی یا تنظیم یک جریان ایجاد شوند.
### **ایجاد با تنظیم مسیر**
یک PsdOptions از فضای نام ImageOptions بسازید و خصوصیات مختلف را تنظیم کنید. مهمترین خصوصیت برای تنظیم خصوصیت منبع است. این خصوصیت مشخص می‌کند که داده‌های تصویر در کجا وجود دارد (در یک فایل یا یک جریان). در مثال زیر، منبع یک فایل است. پس از تنظیم خصوصیات، شی را به یکی از متدهای Create استاتیک همراه با پارامتر عرض و ارتفاع منتقل کنید. عرض و ارتفاع به پیکسل‌ها تعریف شده است.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CreatingbySettingPath-CreatingbySettingPath.java" >}}
### **ایجاد با استفاده از جریان**
مراحل ایجاد یک تصویر با استفاده از یک جریان همانند استفاده از یک مسیر است. تنها تفاوت این است که باید نمونه‌ای از StreamSource با دادن یک شی جریان به سازنده آن ایجاد کرده و آن را به خصوصیت منبع اختصاص دهید.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CreatingUsingStream-CreatingUsingStream.java" >}}
## **بازکردن فایل‌های تصویری**
توسعه‌دهندگان می‌توانند از API Aspose.PSD برای Java برای بازکردن فایل‌های تصویر PSD موجود برای اهداف مختلف مانند افزودن افکت به تصویر یا تبدیل یک فایل موجود به یک فرمت دیگر استفاده کنند. هدف چیست، Aspose.PSD دو روش استاندارد برای باز کردن فایل‌های موجود فراهم می‌کند: از فایل یا از یک جریان.
### **بازکردن از دیسک**
یک فایل تصویر را با دادن مسیر و نام فایل به عنوان پارامتر به متد استاتیک Load ارائه شده توسط کلاس Image باز کنید.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SavingtoDisk-SavingtoDisk.java" >}}
### **بازکردن با استفاده از جریان**
گاهی اوقات تصویری که باید باز کنیم به عنوان یک جریان ذخیره شده است. در چنین مواردی، از نسخه با بارگذاری اضافی متد Load استفاده کنیم. این متد یک شی جریان را به عنوان آرگومان قبول می‌کند تا تصویر را باز کند.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-LoadingFromStream-LoadingFromStream.java" >}}
### **بارگذاری تصویر به عنوان لایه**
این مقاله استفاده از Aspose.PSD برای بارگذاری تصویر به عنوان لایه را نشان می‌دهد. Aspose.PSD API‌ها روش‌های کارآمد و آسان برای دستیابی به این هدف را ارائه کرده است. Aspose.PSD متد AddLayer کلاس PsdImage را برای اضافه کردن تصویر به یک فایل PSD به عنوان یک لایه فراهم کرده است.

مراحل بارگذاری تصویر به عنوان لایه بر این‌گونه است:

- یک نمونه از تصویر با استفاده از کلاس PsdImage با عرض و ارتفاع مشخص شده بسازید.
- یک فایل PSD را به عنوان تصویر با استفاده از متد کارخانه Load ارائه شده توسط کلاس Image بارگذاری کنید.
- یک نمونه از کلاس Layer بسازید و لایه تصویر PSD را به آن اختصاص دهید.
- لایه ساخته شده را با استفاده از متد AddLayer که توسط کلاس PsdImage ارائه شده است اضافه کنید.
- نتایج را ذخیره کنید.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-LoadImageToPSD-LoadImageToPSD.java" >}}
## **ذخیره فایل‌های تصویری**
Aspose.PSD به شما اجازه می‌دهد تا فایل‌های تصویری را از ابتدا ایجاد کنید. همچنین امکان ویرایش فایل‌های تصویری موجود را فراهم می‌کند. هنگامی که تصویر ایجاد یا ویرایش می‌شود، فایل معمولاً به دیسک ذخیره می‌شود. Aspose.PSD شما را با متدهایی برای ذخیره تصاویر به دیسک با تعیین مسیر یا استفاده از یک شی جریان فراهم می‌کند.
### **ذخیره به دیسک**
کلاس Image یک شی تصویری را نشان می‌دهد، بنابراین این کلاس تمام ابزارهای مورد نیاز برای ایجاد، بارگذاری و ذخیره یک فایل تصویری را فراهم می‌کند. برای ذخیره تصاویر از متد Save کلاس Image استفاده کنید. یک نسخه با بارگذاری اضافی از متد Save مکان فایل را به عنوان یک رشته قبول می‌کند.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SavingtoDisk-SavingtoDisk.java" >}}
### **ذخیره به یک جریان**
یک نسخه دیگر با بارگذاری اضافی از متد Save، شی جریان را به عنوان آرگومان قبول کرده و فایل تصویری را به جریان ذخیره می‌کند.

اگر تصویر با تعیین هرکدام از CreateOptions در سازنده Image ، تصویر به طور خودکار در مسیر یا جریان ارائه شده در زمان مقداردهی اولیه کلاس Image ذخیره شود با فراخوانی متد ذخیره که هیچ پارامتری را قبول نمی‌کند.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SavingtoStream-SavingtoStream.java" >}}
### **تنظیم برای جایگزینی فونت‌های گم‌شده**
توسعه‌دهندگان می‌توانند از API Aspose.PSD برای Java برای بارگذاری فایل تصویری PSD موجود برای اهداف مختلف استفاده کنند، به عنوان مثال تنظیم نام پیش‌فرض فونت هنگام ذخیره سند‌های PSD به عنوان تصویر raster (به فرمت‌های PNG، JPG و BMP). این فونت پیش‌فرض باید برای همه فونت‌های گم‌شده (فونت‌هایی که در سیستم عامل فعلی یافت نمی‌شوند) استفاده شود. هنگامی که تصویر ویرایش شود، فایل به دیسک ذخیره خواهد شد.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SettingforReplacingMissingFonts-SettingforReplacingMissingFonts.java" >}}
