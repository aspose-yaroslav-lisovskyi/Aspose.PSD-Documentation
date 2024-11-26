---
title: Метрическая лицензия
type: docs
weight: 80
url: /ru/net/metered-licensing/
description: Библиотека PSD Photoshop C# позволяет разработчикам применять метрический ключ, который представляет собой новый механизм лицензирования и будет использоваться параллельно с существующим методом лицензирования.
---

{{% alert color="primary" %}} 

Aspose.PSD позволяет разработчикам применять метрический ключ. Это новый механизм лицензирования. Новый механизм лицензирования будет использоваться параллельно с существующим методом лицензирования. Те клиенты, которые хотят быть оплачиваемыми на основе использования функций API, могут использовать метрическую лицензию. Для получения дополнительной информации обратитесь к разделу [ Часто задаваемые вопросы о метрической лицензии](https://purchase.aspose.com/faqs/licensing/metered).

{{% /alert %}} 
## **Метрическая лицензия**
Вот простые шаги для использования класса Metered.

1. Создайте экземпляр класса Metered.
1. Передайте общие и частные ключи в метод setMeteredKey.
1. Выполните обработку (выполните задачу).
1. вызовите метод getConsumptionQuantity класса Metered.
1. Он вернет количество запросов API, которое вы использовали до сих пор.

Ниже приведен образец кода, демонстрирующий установку метрического общедоступного и частного ключа.

{{< highlight java >}}


 // Создание экземпляра класса PSD Metered

Aspose.PSD.Metered metered = new Aspose.PSD.Metered();



// Доступ к свойству setMeteredKey и передача общих и частных ключей в качестве параметров

metered.SetMeteredKey("*****", "*****");



// Получение данных метрики перед вызовом API

decimal amountbefore = Aspose.PSD.Metered.GetConsumptionQuantity();



// Отображение информации

Console.WriteLine("Сумма израсходована до: " + amountbefore.ToString());

// Получение данных метрики после вызова API

decimal amountafter = Aspose.PSD.Metered.GetConsumptionQuantity();



// Отображение информации

Console.WriteLine("Сумма израсходована после: " + amountafter.ToString());

{{< /highlight >}}