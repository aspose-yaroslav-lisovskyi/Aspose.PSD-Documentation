---
title: Пример за използване на групови слоеве в Aspose.PSD за C#
weight: 100
type: docs
description: Използване на Групов слой на PSD файл чрез C#
keywords: [група слоеве, групов слой, добавяне на слой към група, psd api, C#, csharp, примерен код]
url: bg/net/psd-group-layer/
---

## Преглед

Груповите слоеве в Aspose.PSD за C# позволяват ефективна организация и манипулиране на слоеве в PSD файл. Чрез използването на папкови слоеве можете да групирате множество слоеве заедно и да приложите трансформации или ефекти към цялата група.

Този пример демонстрира създаването на ново изображение PSD с `PsdImage.Create`. След това се създава нов обект `LayerGroup` чрез `AddLayerGroup` от обекта `PsdImage`. Груповият слой е наименуван "Folder", вмъкнат на индекс 0 и се задава да бъде видим.

След това се създават два обекта `Layer`, на които се задават свойствата им `DisplayName`. Тези слоеве се добавят към груповия слой чрез `AddLayer`.

Слоевете в групата могат да бъдат достъпени чрез свойството `Layers` на обекта `LayerGroup`. Примерът потвърждава, че имената на първия и втория слоеве в групата са "Layer 1" и "Layer 2".

След като се модифицират груповите слоеве, актуализираният PSD файл се запазва с метода `Save` на обекта `PsdImage`.

Този базов пример ви познава с работата с групови слоеве чрез Aspose.PSD за C#. Библиотеката предлага напреднали функции за манипулация и трансформиране на слоеве в PSD файлове. Разгледайте Aspose.PSD за C# документацията за по-подробни примери и функции.

Ето един примерен код, демонстриращ използването на групов слой в Aspose.PSD за C#:

## Пример

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "ExportLayerGroupToImage-ExportLayerGroupToImage.cs" >}}

За по-подробна информация и примери, моля посетете [Aspose.PSD за C# документацията](https://docs.aspose.com/psd/net/).