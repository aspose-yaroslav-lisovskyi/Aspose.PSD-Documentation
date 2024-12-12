---
title: Умно Управление на Филтри в Aspose.PSD за Java
weight: 100
type: docs
description: Примери за използване на Умни Филтри в PSD файла
keywords: [умен филтър, добавяне на шум, gauss размазване, заточване, филтър, psd филтър, psd api, java, кодов пример]
url: bg/java/smart-filters/
---

## **Преглед**

Има 3 метода за прилагане на умни филтри в Aspose.PSD за Java.

## ** Прилагане на Филтъра Директно **

Този кодов пример показва как да приложите умни филтри директно в Aspose.PSD за Java.

Първоначално, кодът дефинира изходния PSD файл, изходния файл за оригиналното изображение и изходният файл за актуализираното изображение.

След това, кодът зарежда PSD изображението, използвайки метода Image.load() и го каства към обект от тип PsdImage.

Оригиналното изображение се запазва, използвайки метода save(), като се посочи името на изходния файл.

Създава се обект от тип SharpenSmartFilter, за да представлява желания умен филтър.

След това кодът извлича обикновен слой от PSD изображението, като използва psdImage.getLayers()[1].

Използва се цикъл, за да се приложи филтъра за заточване три пъти върху обикновения слой.

Накрая, актуализираното изображение се запазва, използвайки метода save(), с предоставеното име на изходния файл.

Този код илюстрира директното прилагане на умни филтри в Aspose.PSD за Java. Чрез използването на подходящи обекти за филтри и прилагането им към желаните слоеве, могат да се постигнат желаните ефекти върху изображенията.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-psd-smart-filter-direct-apply.java" >}}

## ** Манипулиране на Умни Филтри в Умните Обекти **

Този кодов фрагмент описва как да се манипулират умни филтри в умните обекти в Aspose.PSD за Java.

Първоначално, кодът дефинира изходния PSD файл, изходния файл за оригиналното изображение и изходният файл за актуализираното изображение.

PSD изображението се зарежда, използвайки метода Image.load(), а после се каства към обект от тип PsdImage.

Оригиналното изображение се запазва, използвайки метода save(), като се посочи името на изходния файл.

След това кодът каства втория слой на PSD изображението като SmartObjectLayer обект, представляващ слоя на умния обект.

След това кодът демонстрира редактиране на умни филтри, представяйки два вида: GaussianBlurSmartFilter и AddNoiseSmartFilter.

За GaussianBlurSmartFilter, кодът актуализира стойности на филтъра като радиус, режим на смесване, непрозрачност и статус на активиране.

За AddNoiseSmartFilter, кодът задава разпределението на шума на NoiseDistribution.Uniform.

След това кодът добавя две нови елемента на филтъра към слоя на умния обект: още един GaussianBlurSmartFilter и един AddNoiseSmartFilter.

След добавянето на новите филтри, кодът прилага промените, използвайки метода updateResourceValues().

Накрая, кодът демонстрира директното прилагане на филтри към слоя и маската му, използвайки съответно методите apply() и applyToMask().

Актуализираният образ се запазва, използвайки метода save(), с предоставеното име на изходния файл.

Като следвате този кодов пример, можете да разберете как да манипулирате умни филтри в умните обекти в Aspose.PSD за Java. Библиотеката предлага разнообразие от умни филтри, всеки със собствени свойства и методи, които могат да бъдат персонализирани, за да се постигнат желаните ефекти върху изображенията.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-psd-smart-filter-features.java" >}}

## ** Прилагане на Умни Филтри към Маската на Слоя **

Прилагане на Умни Филтри към Маските: Мощна Техника за Редактиране на Изображения

Умните филтри, широко използвани в софтуерните продукти за обработка на изображения, позволяват на потребителите да приложват разнообразни филтри и ефекти към техните изображения. Една от интересните техники, достъпни с умните филтри, е тяхното приложение към маските. Този материал е посветен на прилагането на умни филтри към маските и обсъжда тяхната полезност в областта на обработката на изображения.

Разбиране на Маските: Преди да се заровим в прилагането на умни филтри върху маските, е важно да разберем понятието на маска. В обработката на изображения маската е черно-бяло изображение, което определя прозрачността на определени зони в изображението. Маските позволяват селективното прилагане на филтри, корекции или ефекти към конкретни части от изображението, като оставят другите непокътнати.

Прилагане на Умни Филтри към Маските: Когато се приложат умни филтри към маските, те влияят само на зоните, определени от маската, като предлагат прецизен контрол върху въздействието на филтъра. Чрез манипулиране на маската, потребителите могат да модулират интензитета и обхвата на ефекта на филтъра.

Моля, обърнете се към предходния пример и метода: [API Reference Прилагане на умни филтри към маската](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.smartfilters/smartfilter/#apply_to_mask_layer_with_mask_2)