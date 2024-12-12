---
title: Общ преглед на формата PSD
type: docs
weight: 60
url: /bg/net/psd-format-overview/
---

## **Описание**
PSD, Photoshop Document, представлява нативния файлов формат на Adobe Photoshop, използван за графичен дизайн и разработка.

## **Спецификации на файловия формат**
Данните в PSD файл се съхраняват в големия ред на байтовете. Това означава, че се извършва размяна на къси и дълги цели числа при четене или записване на Windows платформата. Файловият формат на Photoshop е разделен на пет главни части. Има много маркери за дължина, които могат да се използват за преминаване от една секция към следващата. Маркерите за дължина обикновено се пълнят с байтове, за да се закръгли до най-близкия 2 или 4-байтов интервал. Петте главни части са:

- Заглавна част на файла
- Данни за цветов режим
- Ресурси за изображение
- Информация за слой и маска
- Данни за изображение

За съответствие, данните трябва да бъдат записани във всички тези полета в секцията, тъй като Photoshop може да опита да прочете цялата секция. Това също подразбира, че трябва да се пишат нули в пропуснатите полета при записване във файл. Полеве за дължина в дължина-ограничени секции следва да се използват за определяне кога да спрете с четенето. В повечето случаи, полето за дължина показва броя на байтовете, а не записите, които следват. Следните точки трябва да бъдат помнени при четене на файл.

- Стойностите в колоната "Дължина" във всички таблиците са в байтове.
- Всички стойности, дефинирани като Unicode string се състоят от:
- Поле за дължина от 4 байта, представляващо броя на символите в низа (не байтове).
- Низ от Unicode стойности, по два байта на символ.

## **Характеристики на формата**
PSD файловете могат да включват слоеве с изображения, слоеве за корекции, маски на слоеве, анотации, информация за файла, ключови думи и други елементи, специфични за Photoshop. Файловете на Photoshop имат зададено разширение.PSD и имат максимална височина и ширина от 30 000 пиксела, както и ограничение на дължина от два гигабайта.

## **Как може да се използва**
1. Инструмент за изрязване на PSD.
1. [Преобразуване на PSD](/psd/bg/net/converting-psd-image-to-raster-format/) в HTML.
1. Използване на [PSD като Шаблон](/psd/bg/net/using-psd-files-as-templates-for-automation-business-cards-case/) за Имейл.
1. PSD към конкретен CMS HTML.
1. Идентификация в PSD файл (Полицейски фоторобот).
1. Създаване на псевдо-3D изображения за преглед, като се използват Умни Обекти за такива стоки като бутилки, чаши, тениски и др.
1. Бързо редактиране на PSD: Авто-тон, Пресети, Умни Обект, Изрязване на изображение от текстов слой.

И още много други. Ако сте създали нещо страхотно с Aspose.PSD, моля, споделете с нас вашето изследване на случай чрез [Aspose Форуми](https://forum.aspose.com/).

Допълнителни примери, от които можете да научите:

- [Примери на случаи](https://downloads.aspose.com/corporate/case-studies/aspose.psd/)
- [Демонстрации](/psd/bg/net/showcases-html/)