---
title: Manipulirane na PNG изображения
type: docs
weight: 40
url: /bg/manipulirane-na-png-izobrazeniya/
---

## **Задаване на прозрачност за PNG изображения**
Едно от предимствата на запазването на изображения във формат PNG е, че PNG може да има прозрачен фон. Aspose.PSD за .NET предоставя възможност за задаване на прозрачност за PNG изображения и растеризирани изображения, както е показано в следващата секция. Aspose.PSD за .NET API може да се използва за задаване на всякакъв цвят като прозрачен при създаване на нови PNG изображения или конвертиране на съществуващи изображения в PNG формат. За тази цел, Aspose.PSD за .NET API е изложила свойствата [TransparentColor](https://reference.aspose.com/psd/net/aspose.psd/ipsdcolorpalette/properties/transparentcolor) и изброителя [PngColorType](https://reference.aspose.com/psd/net/aspose.psd.fileformats.png/pngcolortype), които могат да се зададат, за да се укаже, че определен цвят да бъде визуализиран като прозрачен в PNG изображението. Посоченият по-долу откъс код демонстрира как да се конвертира съществуващо изображение PSD в PNG изображение, като се зададе желаният цвят като прозрачен.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-SpecifyTransparency-SpecifyTransparency.cs" >}}
## **Задаване на резолюция за PNG изображения**
Aspose.PSD за .NET излага класа ResolutionSetting, който може да се използва за задаване на резолюцията за всички формати на изображения, включително PNG. Тази статия демонстрира използването на Aspose.PSD за .NET API за задаване на хоризонталните и вертикалните параметри на резолюцията за формат PNG. Откъсът от код по-долу зарежда съществуващо изображение PSD и го преобразува в PNG формат, като променя също и резолюцията.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-SettingResolution-SettingResolution.cs" >}}
## **Сжатие на PNG файлове**
Portable Network Graphic (PNG) е формат за компресия без загуби за предаване на битови карти през мрежи. Когато запазвате изображение като файл PNG във всяка програма, може да ви се поиска да изберете ниво на компресия в диапазона от 0 до някакъв максимален уровен. Задаването на тази стойност всъщност компресира размера на файла и не намалява качеството на изображението. Тази статия описва как Aspose.PSD APIs ви позволява да контролирате размера на PNG файловете. Aspose.PSD APIs може да се използва за задаване на нивата на компресия за файловия формат PNG, използвайки класа PngOptions, който разполага със свойството от тип int [CompressionLevel](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions/properties/compressionlevel). Това свойство приема стойност от 0 до 9, като 9 е максималното ниво на компресия. Посоченият по-долу откъс код демонстрира как да се зададат нивата на компресия, използвайки Aspose.PSD за .NET API.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-CompressingFiles-CompressingFiles.cs" >}}
## **Задаване на битова дълбочина за PNG изображения**
Битовата дълбочина в изображенията е броят на битовете, използвани за указване на цвета на един пиксел в битово изображение на картина. Както при всички други формати на битови изображения, цветната дълбочина на PNG също се представя в битове, като 1-битови (2 цвята), 2-битови (4 цвята), 4-битови (16 цвята) и 8-битови (256 цвята). Aspose.PSD за .NET API може да се използва за задаване на битова дълбочина за PNG изображения, като използва свойството [BitDepth](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions/properties/bitdepth), изложено от класа PngOptions. В момента свойството BitDepth може да бъде зададено на 1, 2, 4 или 8 бита за градациите на сиво и индексирани цветове. За всички други видове цветове се поддържат само 8 бита. Посоченият по-долу откъс код демонстрира как да се зададе битовата дълбочина за PNG изображение.


{{< gist "" "8a4c9d34ce856d1642fc7c0ce974175c" "" >}}
## **Прилагане на методи за филтриране върху PNG изображения**
Битовата дълбочина в изображенията е броят на битовете, използвани за указване на цвета на един пиксел в битово изображение на картина. Както при всички други формати на битови изображения, цветната дълбочина на PNG също се представя в битове, като 1-битови (2 цвята), 2-битови (4 цвята), 4-битови (16 цвята) и 8-битови (256 цвята). Aspose.PSD за .NET API може да се използва за задаване на битова дълбочина за PNG изображения, използвайки свойството BitDepth, изложено от класа PngOptions. В момента свойството BitDepth може да бъде зададено на 1, 2, 4 или 8 бита за градациите на сиво и индексирани цветове. За всички други видове цветове се поддържат само 8 бита. Посоченият по-долу откъс код демонстрира как битовата дълбочина може да бъде зададена за PNG изображение.


{{< gist "" "8a4c9d34ce856d1642fc7c0ce974175c" "" >}}
## **Промяна на цвета на фон на прозрачно PNG изображение**
Изображенията във формат PNG могат да имат прозрачен фон. Aspose.PSD за .NET предоставя възможността за промяна на цвета на фона на PNG изображение с прозрачен фон. Aspose.PSD за .NET API може да се използва за задаване/промяна на цвета на прозрачно PNG изображение. Посоченият по-долу откъс код демонстрира как да се зададе/промени цвета на фона на прозрачно PNG изображение.



{{< gist "" "8a4c9d34ce856d1642fc7c0ce974175c" "" >}}