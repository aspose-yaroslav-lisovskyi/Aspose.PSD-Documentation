---
title: Пример за използване на групови слоеве в Aspose.PSD за Java
weight: 100
type: docs
description: Използване на Групов слой на PSD файл чрез Java
keywords: [слой група, групов слой, добавяне на слой към група, psd api, java, примерен код]
url: /bg/java/psd-group-layer/
---

## **Преглед**

Използването на групови слоеве в Aspose.PSD за Java увеличава възможностите ви за управление и организация на слоеве в PSD изображение ефективно. Груповите слоеве, наричани още папки, ви позволяват да съберете множество слоеве и да приложите трансформации или ефекти колективно.

За да започнете, създайте ново PSD изображение, използвайки метода PsdImage.create(). След това, инициализирайте нов обект LayerGroup чрез метода addLayerGroup на обекта PsdImage. Предоставете желаното име за груповия слой ("Папка"), посочете индекса за вмъкване (0) и задайте булев флаг, който показва видимостта му (True).

След това създайте два обекта Layer и задайте техните имена за показване, използвайки метода setDisplayName. Добавете тези слоеве към груповия слой, използвайки метода addLayer.

За достъп до слоевете в групата, използвайте свойството layers на обекта LayerGroup. Потвърдете, че имената за показване на първия и втория слоеве в групата са съответно "Слой 1" и "Слой 2".

След като сте манипулирали груповите слоеве, запазете промененото PSD изображение, като използвате метода save на обекта PsdImage.

Това е основен пример, който да ви помогне да се запознаете с работата с групови слоеве, използвайки Aspose.PSD за Java. Библиотеката предлага множество напреднали функции за манипулиране и трансформация на слоеве в PSD изображения. За допълнителни подробности и примери за използване на групови слоеве и други функционалности на библиотеката, обърнете се към документацията на Aspose.PSD за Java.

За работа с групови слоеве в Aspose.PSD за Java, използвайте класа LayerGroup. По-долу е представен откъс от код, илюстриращ как да създадете групов слой, да добавите слоеве към него и да запазите промененото PSD изображение.

Моля, обърнете се към пълния пример, предоставен по-горе.

## **Пример**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-psd-group-layer.java" >}}