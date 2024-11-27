---
title: باز کردن و خروجی گرفتن از فایل‌های PSD، PSB و AI و ذخیره آن‌ها به صورت PDF، PNG، TIFF، GIF، BMP، JPEG
weight: 100
type: docs
description: مثال باز کردن فایل‌های PSD، PSB و AI و ذخیره آن‌ها به فرمت‌های دیگر
keywords: [باز کردن psd، باز کردن ai، باز کردن psb، خروجی گرفتن به png، خروجی گرفتن به pdf، خروجی گرفتن به jpeg، خروجی گرفتن به tiff، پی‌اس‌دی api، پایتون، نمونه کد]
url: fa/python-net/open-export-psd-psb-ai-images-to-pdf-jpeg-png-tiff-bmp-gif-bmp/
---

## **بررسی موضوع**
برای تبدیل فایل‌های PSD، PSB و AI به فرمت‌های مختلف، می‌توانید از کتابخانه Aspose.PSD در Python استفاده کنید. این کتابخانه امکانات و تنظیمات مختلفی را برای سفارشی کردن فرآیند تبدیل فراهم می‌کند.

ابتدا باید کلاس‌ها و ماژول‌های مورد نیاز از کتابخانه Aspose.PSD را وارد کنید. اطمینان حاصل کنید که قبل از اجرای کد، کتابخانه را نصب کرده‌اید.

در این کد، ما گزینه‌های مختلف برای فرمت‌های مختلف مانند PNG، PDF، TIFF، JPEG، BMP، JPEG2000، GIF، PSB و PSD تعریف می‌کنیم. این گزینه‌ها به شما امکان می‌دهند فایل خروجی را مطابق با نیازهای شما سفارشی‌سازی کنید.

سپس، یک فهرست با نام formats تعریف می‌کنیم که پسوند فایل‌ها را به گزینه‌های ذخیره‌سازی متناظرشان نقشه‌برداری می‌کند.

برای تبدیل یک فایل PSD به سایر فرمت‌ها، باید فایل PSD را با استفاده از PsdImage.load() بارگذاری کرده و سپس از فهرست formats عبور کنید. برای هر فرمت، نام فایل خروجی را مشخص کرده و تصویر را با استفاده از متد image.save() ذخیره کنید.

به همین ترتیب، برای تبدیل یک فایل AI به سایر فرمت‌ها، فایل AI را با استفاده از AiImage.load() بارگذاری کرده و از فهرست formats عبور کنید. نام فایل خروجی را مشخص کرده و تصویر را با استفاده از متد image.save() ذخیره کنید.

اطمینان حاصل کنید که مسیرهای صحیح فایل‌های منبع PSD و AI را وارد کرده‌اید.

همین است! اکنون می‌توانید از این کد برای تبدیل فایل‌های PSD، PSB و AI به فرمت‌های مختلف با استفاده از Aspose.PSD برای Python استفاده کنید.

لطفاً مثال کامل را بررسی کنید.

## **مثال**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "مستندات-پایتون-Aspose-Psd-open-export-psd-psb-ai-images-to-pdf-jpeg-png-tiff-bmp-gif-bmp.py" >}}