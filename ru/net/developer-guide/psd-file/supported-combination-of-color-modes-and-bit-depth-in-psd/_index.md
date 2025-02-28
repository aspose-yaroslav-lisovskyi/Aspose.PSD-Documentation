---
title: Поддерживаемые комбинации цветовых режимов и глубины битов в PSD
type: документация
weight: 80
url: /ru/net/supported-combination-of-color-modes-and-bit-depth-in-psd/
---

## **Описание**
Aspose.PSD поддерживает открытие файлов PSD с любой комбинацией режима цвета и глубины битов в файлах Adobe Photoshop PSD. Вы можете открывать такие файлы и использовать API низкого уровня для изменения содержимого файла. Однако для некоторых менее популярных комбинаций могут возникать специфические проблемы, некоторые из них связаны с ограничениями цветовых режимов.

## **Поддерживаемые комбинации экспорта цветовых режимов и глубины битов в PSD в режиме «только для чтения»**

| |По умолчанию|Оттенки серого|Индексированный|RGB|CMYK|Мультиканал|Двухтоновый|Lab|
| :- | :- | :- | :- | :- | :- | :- | :- | :- |
|Глубина 1|Да[](https://issue.kharkov.dynabic.com/issues/PSDNET-283)|-|-|-|-|-|-|-|
|Глубина 8|-|Да|Да|Да|Да|Нет Q3-Q4|Нет Q3-Q4|Да[](https://issue.kharkov.dynabic.com/issues/PSDNET-290)|
|Глубина 16|-|Да|-|Да|Да|-[](https://issue.kharkov.dynabic.com/issues/PSDNET-287)|-|Нет (Q3-Q4)|
|Глубина 32|-|Да*[](https://issue.kharkov.dynabic.com/issues/PSDNET-125)|-|Да*|-[](https://issue.kharkov.dynabic.com/issues/PSDNET-285)|-[](https://issue.kharkov.dynabic.com/issues/PSDNET-288)|-|-|
\* Незначительные проблемы в некоторых случаях

## **Поддерживаемые комбинации экспорта цветовых режимов и глубины битов в PSD в режиме редактирования**

| |По умолчанию|Оттенки серого|Индексированный|RGB|CMYK|Мультиканал|Двухтоновый|Lab|
| :- | :- | :- | :- | :- | :- | :- | :- | :- |
|Глубина 1|Да|-|-|-|-|-|-|-|
|Глубина 8|-|Да|Нет|Да|Да|Нет Q3-Q4|Нет Q3-Q4|Да*|
|Глубина 16|-|Да|-|Да|Да*|-|-|Нет (Q3-Q4)|
|Глубина 32|-|Нет (Q3-Q4)|-|Нет (Q3-Q4)|-|-|-|-|
\* Незначительные проблемы в некоторых случаях

Если вам нужна поддержка конкретной комбинации цветового режима / глубины бита, вы можете опубликовать запрос на [форумах Aspose](https://forum.aspose.com/c/psd)
