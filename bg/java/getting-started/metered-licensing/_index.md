---
title: Лицензиране с измерване
type: docs
weight: 70
url: /bg/java/metered-licensing/
---

{{% alert color="primary" %}}

Aspose.PSD позволява на разработчиците да прилагат измерван лицензионен ключ. Това е нов механизъм за лицензиране. Новият механизъм за лицензиране ще се използва заедно със съществуващия метод на лицензиране. Тези клиенти, които искат да бъдат таксувани въз основа на използването на функциите на API, могат да използват измерваното лицензиране. За повече подробности, моля обърнете се към раздела [Често задавани въпроси относно лицензирането с измерване](https://purchase.aspose.com/faqs/licensing/metered).

{{% /alert %}}
## **Лицензиране с измерване**
Ето съдържащите се стъпки за използване на класа за измерване.

1. Създайте инстанция на класа за измерване.
1. Предайте публичния и частния ключове на метода setMeteredKey.
1. Извършете обработка (изпълнете задача).
1. Обадете се на метода getConsumptionQuantity на класа за измерване.
1. Той ще върне сумата / количеството на заявките към API, които сте консумирали досега.

По-долу е демонстриран примерен код, показващ как да се зададе измереният публичен и частен ключ.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Licensing-MeteredLicensing-MeteredLicensing.java" >}}