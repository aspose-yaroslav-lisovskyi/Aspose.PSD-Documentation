---
title: Конвертація колірного простору для JPEG через ICC профілі
type: docs
weight: 60
url: /uk/net/color-space-conversion-for-jpeg-through-icc-profiles/
---

## **Керування кольором для формату JPEG**


У цій статті обговорюється використання ICC профілів для виконання управління простором кольору під час роботи з форматом JPEG за допомогою API Aspose.PSD. Внутрішнім кольоровим простором JPEG є YCbCr, однак цей [формат](https://reference.aspose.com/psd/net/aspose.psd/pixelformat) також може вміщати в собі відтінки сірого, RGB, CMYK та YCCK для зберігання метаданих зображення. API Aspose.PSD в основному працює в просторі RGB, тому API повинно виконувати конвертацію кольорових просторів в обидва напрямки для правильної обробки файлів JPEG. Конвертацію відтінків сірого до RGB та YCbCr до RGB можна виконати за допомогою математичних перетворень, але простори CMYK та YCCK не можуть легко перетворюватися в простір RGB.

API Aspose.PSD повинно виконати безпосередню конвертацію RGB в CMYK для зображень у форматі JPEG з простором кольору CMYK. З іншого боку, зображення з простором кольору YCCK вимагає конвертацію кольору RGB в CMYK в YCCK, де конвертація від CMYK в YCCK використовує [перетворення ITU-R BT.601](https://wikipedia.org/wiki/Rec._601), застосоване до перших трьох каналів, залишаючи k-канал без змін. Коротко кажучи, API Aspose.PSD повинні виконати взаємне перетворення просторів RGB та CMYK для обох зображень у форматах CMYK та YCCK, і такі перетворення виконуються за допомогою ICC профілів, які в основному є таблицями пошуку, що описують властивості кольору та допомагають у перетвореннях кольору.


## **ICC профілі**
Механізм конвертації ICC використовує "Профілі", які об'єднують вихідний кольоровий простір з пристроєм-незалежними кольоровими просторами CIELAB або CIEXYZ. Aspose.PSD може конвертувати дані в потрібний кольоровий простір, використовуючи ці два кольорові простори з додатковими профілями. Тому для конвертації ICC користувач повинен надати два профілі - один RGB профіль для переходу внутрішнього кольорового простору CIE та один CMYK профіль для отримання характеристик кольору CMYK. Для досягнення конвертації CMYK в RGB потрібно поміняти профілі, тобто використовувати CMYK профіль як вихідний профіль і RGB профіль як кінцевий профіль.
## **Конверсія кольору для JPEG через ICC профілі**
API Aspose.PSD приховує деталі, забезпечуючи простий механізм для вказання ICC профілів через клас [JpegOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions). Крім того, Aspose.PSD використовує вбудовані зразкові профілі SWOP, CMYK та sRGB, тому у більшості випадків використання користувачеві не потрібно шукати конкретні профілі. Є недолік таких корекцій, а саме; такі конвертації кольорових просторів є невідворотними, оскільки не можна очікувати отримати той самий колір після конвертації RGB в CMYK в RGB через невідповідні кольорові простори та різні кольорові профілі. У наведеному нижче кодовому уривку показано використання Aspose.PSD для API .NET для вказання RGB та CMYK кольорових профілів для зображення у форматі JPEG в форматі YCCK. У цьому прикладі змінено RGB та CMYK кольорові профілі, а зображення зберігається в просторі кольору YCCK. Зверніть увагу, що властивості [RgbColorProfile](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions/properties/rgbcolorprofile) та [CmykColorProfile](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions/properties/cmykcolorprofile) працюватимуть для зміни піксельних даних для кольорового простору YCCK. Всі інші кольорові простори не викликають профілі кольору для оновлення кольорових даних.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ColorConversionUsingICCProfiles-ColorConversionUsingICCProfiles.cs" >}}


Якщо профілі не встановлено, то API Aspose.PSD для .NET використовуватиме позначкові профілі за замовчуванням. У наведеному нижче прикладі використані властивості позначкових профілів призначені для зміни кольорового простору приблизно для більшості зображень у форматі JPEG.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ColorConversionUsingDefaultProfiles-ColorConversionUsingDefaultProfiles.cs" >}}