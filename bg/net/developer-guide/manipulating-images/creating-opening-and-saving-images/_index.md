---
title: Създаване, отваряне и запазване на изображения
type: docs
weight: 30
url: /bg/net/creating-opening-and-saving-images/
---

## **Създаване на файлове с изображения**
Aspose.PSD за .NET позволява на разработчиците да създават свои собствени изображения. Използвайте статичния метод Create, който се излага от класа Image, за да създадете нови изображения. Всичко, което трябва да направите, е да предоставите подходящ обект от един от класовете от пространството от имена ImageOptions за желания формат на изходното изображение. За да създадете файл с изображение, първо създайте инстанция на един от класовете от пространството от имена ImageOptions. Тези класове определят формата на изходното изображение. По-долу са избрани някои класове от пространството от имена ImageOptions (имайте предвид, че текущо се поддържат само форматите на семейството на PSD файловете за създаване):

[PsdOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/psdoptions) задава опциите за създаване на PSD файл. Изображенията могат да бъдат създадени чрез задаване на път за изход или чрез задаване на поток.
### **Създаване чрез Задаване на Път**
Създайте PsdOptions от пространството от имена [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) и задайте различните свойства. Най-важното свойство за задаване е Source свойството. Това свойство посочва къде се намират данните за изображението (във файл или поток). В примера по-долу източникът е файл. След като зададете свойствата, предайте обекта на един от статичните [Create](https://reference.aspose.com/psd/net/aspose.psd/image/methods/create) методи заедно с параметър за широчина и височина. Широчината и височината се определят в пиксели.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CreatingbySettingPath-CreatingbySettingPath.cs" >}}
### **Създаване чрез Използване на Поток**
Процесът за създаване на изображение чрез поток е същият като този за използване на пътя. Единствената разлика е, че трябва да създадете инстанция на [StreamSource](https://reference.aspose.com/psd/net/aspose.psd.sources/streamsource), като подадете обект Stream на неговия конструктор и го присвоите на свойството Source.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CreatingUsingStream-CreatingUsingStream.cs" >}}
## **Отваряне на файлове с изображения**
Разработчиците могат да използват Aspose.PSD за .NET API, за да отворят съществуващи файлове с PSD изображения за различни цели, като добавяне на ефекти към изображението или конвертиране на съществуващ файл в друг формат. Независимо от целта, Aspose.PSD предоставя два стандартни начина за отваряне на съществуващи файлове: от файл или от поток.
### **Отваряне от Диск**
Отворете файл с изображение, като подадете пътя и името на файла като параметър на статичния метод Load, излогнат от класа Image.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SavingtoDisk-SavingtoDisk.cs" >}}
### **Отваряне чрез Поток**
Понякога изображението, което трябва да отворим, се съхранява като поток. В такива случаи използвайте надградената версия на метода Load. Тя приема Stream обект като аргумент, за да отвори изображението.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-LoadingFromStream-LoadingFromStream.cs" >}}
### **Зареждане на Изображение като Слой**
Този статия демонстрира използването на Aspose.PSD за зареждане на изображение като слой. Aspose.PSD APIs разкриват ефикасни и лесни за използване методи за постигане на тази цел. Aspose.PSD е разкрил метода AddLayer на класа PsdImage за добавяне на изображение в PSD файл като слой.

Стъпките за зареждане на изображение в PSD като слой са толкова прости, както следва:

- Създайте инстанция на изображение с класа PsdImage с посочена широчина и височина.
- Заредете PSD файл като изображение, като използвате фабричния метод Load, излогнат от класа Image.
- Създайте инстанция на класа Layer и присвоете слоя на PSD изображението на него.
- Добавете създадения слой, като използвате метода AddLayer, излогнат от класа PsdImage.
- Запазете резултатите.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-LoadImageToPSD-LoadImageToPSD.cs" >}}
### **Зареждане на Изображение като Слой от Поток**
Тази статия демонстрира използването на Aspose.PSD за зареждане на изображение като слой от поток. За да заредим изображение от поток, просто подайте обект на поток, който съдържа изображение, към конструктора на класа Layer. Добавете създадения слой, като използвате метода AddLayer, излогнат от класа PsdImage, и запазете резултатите.


Ето примерен код.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Opening-LoadingImageFromStream-LoadingImageFromStream.cs" >}}
## **Запазване на файлове с изображения**
Aspose.PSD позволява създаването на файлове с изображения от самото начало. Той също така предоставя възможност за редактиране на съществуващи файлове с изображения. След като изображението е създадено или модифицирано, обикновено файлът се запазва на диск. Aspose.PSD ви предоставя методи за запазване на изображения на диск, като указвате път или използвате обект Stream.
### **Запазване на Диск**
Класът Image представлява обект на изображение, следователно този клас предоставя всички инструменти необходими за създаването, зареждането и запазването на файл с изображение. Използвайте метода Save на класа Image, за да запазите изображения. Една от надградените версии на метода Save приема местоположението на файла като низ.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SavingtoDisk-SavingtoDisk.cs" >}}
### **Запазване в Поток**
Друга надградена версия на метода Save приема обект Stream като аргумент и запазва файловете с изображения в потока.

Ако изображението е създадено, като се посочи някой от CreateOptions в конструктора на Image, изображението се запазва автоматично на пътя или потока, предоставен по време на инициализацията на класа Image, като се извиква методът Save, който не приема никакъв параметър.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SavingtoStream-SavingtoStream.cs" >}}
### **Задаване за Заместване на Липсващите Шрифтове**
Разработчиците могат да използват Aspose.PSD за .NET API, за да зареждат съществуващи файлове с изображения с PSD за различни цели, например, за задаване на име на стандартен шрифт, когато се запазват PSD документи като растерно изображение (в PNG, JPG и BMP формати). Този стандартен шрифт трябва да се използва като заместител за всички липсващи шрифтове (шрифтове, които не се намират в текущата операционна система). След като изображението е модифициран, файлът ще бъде запазен на диск.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SettingforReplacingMissingFonts-SettingforReplacingMissingFonts.cs" >}}