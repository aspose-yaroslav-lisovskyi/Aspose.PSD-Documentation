---
title: Лицензиране
type: docs
weight: 70
url: /bg/net/licensing/
description: Оценете PSD Photoshop C# библиотеката от NuGet и приложете лиценза чрез файл или поток, за да премахнете всякакви ограничения от инсталираната оценка.
---

## **Ограничения на евалуационната версия**
Можете да изтеглите евалуационна версия на Aspose.PSD за .NET от [NuGet](https://www.nuget.org/packages/Aspose.psd/). Евалуационната версия предлага същите функции като напълно лицензираната версия на компонента с няколко ограничения. Когато закупите Aspose.PSD, просто прилагането на лиценза премахва всякакви ограничения от инсталираната оценка. 
Евалуационната версия на Aspose.PSD за .NET предоставя пълната функционалност на продукта, със само две ограничения:

- **Воден знак върху всяка снимка**: Всяка снимка, която запазите, модифицирате или експортирате, има воден знак, който показва "Само за оценка. Създадено с Aspose.PSD. Copyright 2010-2018 Aspose Pty Ltd.". При малки изображения, където пълният воден знак не би се побрал, се виждат две диагонални линии вместо него.
- **Липса на поддръжка за основната функционалност на рисуване**: В режим на оценка, пикселите на изображението не могат да бъдат зареждани или запазвани в изображението. За да рисувате изображения, използвайте по-сложната функционалност за рисуване. Това ограничение засяга функционалност, която зависи от основната функционалност на рисуване. Aspose.PSD за .NET ви позволява да регистрирате свой собствен файлов формат. Все пак, тази функционалност зависи от основната функционалност на рисуване, така че няма смисъл да се използва в режим на оценка, защото не можете да променяте съдържанието на тези файлове.

Ако искате да тествате Aspose.PSD за .NET без ограниченията на оценката, поискайте временна лицензия за 30 дни. Моля, обърнете се към [Как да получа временна лицензия?](https://purchase.aspose.com/temporary-license) за повече информация.
## **Относно файлът с лиценза**
Когато сте доволни от оценката на Aspose.PSD, можете да закупите лиценз на [уебсайта на Aspose](https://purchase.aspose.com/default.aspx). Запознайте се с различните видове абонаменти, предлагани. Ако имате въпроси, не се колебайте да се свържете с [екипа за продажби на Aspose](https://company.aspose.com/contact). Всяка лиценз на Aspose включва едногодишен абонамент за софтуерни актуализации. След първата година, подновете абонаментите си, за да продължите да получавате най-новите функции и поправки. Техническата поддръжка е безплатна и неограничена и се предоставя както на лицензирани, така и на потребители в режим на оценка чрез нашите [Форуми за поддръжка](https://forum.aspose.com/). Лицензът е XML файл, който съдържа детайли като името на продукта, броя на лицензираните разработчици, дата на изтичане на абонамента и т.н. Файлът е цифрово подписан, така че не го променяйте: дори случайно добавянето на допълнителен ред ще направи файлът недействителен. След като закупите Aspose.PSD, трябва да приложите лиценза преди да създадете, редактирате или по друг начин манипулирате изображения. Ако забравите да приложите лиценза, всяко изображение за изход ще има воден знак за оценка. Трябва да приложите лиценз само веднъж за всяко приложение или процес, който разработвате.
## **Къде да Приложите Лиценз в приложението си**
Къде да приложите лиценз зависи от типа на приложението, което разработвате. Стриктно спазвайте тези прости правила:

- Приложете лиценза само веднъж за всяко домейн на приложение. Извикването на License.SetLicense множество пъти не е вредно, но злоупотребява със времето на процесора.
- Приложете лиценза преди да извиквате някои класове на Aspose.PSD за .NET.
- **Приложения на Windows Forms или Console**: извикайте License.SetLicense в кода за стартиране, преди да използвате някой клас на Aspose.PSD за .NET.
- **Приложения на ASP.NET**: извиквайте License.SetLicense от файла Global.asax.cs (Global.asax.vb) в метода Application_Start. По този начин се извиква веднъж, когато приложението стартира. Не извиквайте License.SetLicense вътре в методите на Page_Load, така както лицензът ще бъде зареждан всеки път, когато се зарежда уеб страница.
- **Приложения на Silverlight**: извикайте License.SetLicense от събитието Application_Startup в файла App.xaml.cs (App.xaml.vb).
- **Класова библиотека**: извикайте License.SetLicense от статичен конструктор на класа, който използва Aspose.PSD. Статичният конструктор се изпълнява преди да се създаде инстанция на вашия клас, уверявайки се, че лицензът на Aspose.PSD е правилно зададен.
## **Прилагане на Лиценз**
Лесно можете да изтеглите версия за оценка на Aspose.PSD от НuGet [страница за изтегляне](https://www.nuget.org/packages/Aspose.psd/). Версията за оценка предоставя точно същите възможности като лицензираната версия на Aspose.PSD. Освен това, версията за оценка просто става лицензирана, когато закупите лиценз и добавите няколко реда код за прилагане на лиценза.
### **Използване на файл или поток**
Ако искате да избегнете работата с ограниченията на оценката, трябва да зададете лиценза преди да използвате Aspose.PSD. Трябва да зададете лиценз само веднъж за приложение (или процес).
### **Прилагане на лиценз от файл**
Най-лесният начин за прилагане на лиценз е да сложите файлът с лиценз в същата папка като Aspose.PSD.dll. Тогава можете да посочите името на файла в кода вместо пълен път.

{{< highlight java >}}

 // Създаване на инстанция на лиценз и прилагане на лиценза с пълен път

Aspose.PSD.License license = new Aspose.PSD.License();

license.SetLicense("Aspose.PSD.lic");

{{< /highlight >}}

При извикването на метода SetLicense, името на лиценза трябва да е същото като името на вашия файл с лиценз. Например, ако преименувате файла с лиценза на "Aspose.PSD.lic.xml" трябва да използвате това име за метода SetLicense.
### **Прилагане на лиценз с поток**
Също е възможно да заредите лиценз от поток, както е показано по-долу.

{{< highlight java >}}

// Създаване на инстанция на лиценз и прилагане на лиценза с поток

Aspose.PSD.License license = new Aspose.PSD.License();

license.SetLicense(myStream);

{{< /highlight >}}

### **Проверка на статуса на лиценза**
Класът Aspose.PSD.License има свойството IsLicensed, което ще върне true, ако лицензът е бил зададен правилно.

{{< highlight java >}}

 License license = new License();

license.SetLicense(licensePath);

if (license.IsLicensed)

{

    Console.WriteLine("Лицензът е наличен!");

}

{{< /highlight >}}
### **Използване на вграден ресурс**
Практичният начин за пакетиране на лиценза с вашия код и уверяване, че той не се загубва, е да го включите като вграден ресурс в една от асемблите, която извиква Aspose.PSD. За да включите файлът с лиценз като вграден ресурс:

1. В Visual Studio .NET, кликнете върху **File** и изберете **Add Existing Item**.
1. Включете файла с лиценза (с разширение .lic) в проекта.
1. Изберете файла в Solution Explorer.
1. В Properties прозореца, задайте **Build Action** на **Embedded Resource**.

Не е необходимо да извиквате методите GetExecutingAssembly или GetManifestResourceStream на Assembly в Microsoft .NET Framework, за да получите достъп до вградения ресурс. Вместо това вградете файла като ресурс в проекта и след това предайте името на файла с лиценза на метода SetLicense. Класът License автоматично намира файла с лиценза во вградените ресурси. По-долу е показан пример как да включите лиценза като вграден ресурс и да го приложите в приложението си.

{{< highlight java >}}

 // Създаване на класа License

Aspose.PSD.License license = new Aspose.PSD.License();

// Предаване на името на вградения файл с лиценз

license.SetLicense("Aspose.PSD.lic");

{{< /highlight >}}

### **Проверка на статуса на лиценза**
Класът Aspose.PSD.License има свойството IsLicensed, което ще върне true, ако лицензът е бил зададен правилно.

{{< highlight java >}}

 License license = new License();

license.SetLicense(licensePath);

if (license.IsLicensed)

{

    Console.WriteLine("Лицензът е наличен!");

}

{{< /highlight >}}