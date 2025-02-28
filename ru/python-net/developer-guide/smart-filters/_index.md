---
title: Управление умным фильтром в Aspose.PSD для Python
weight: 100
type: docs
description: Примеры использования умных фильтров в файле PSD
keywords: [умный фильтр, добавить шум, гауссово размытие, улучшение, фильтр, фильтр PSD, API PSD, python, образец кода]
url: ru/python-net/smart-filters/
---

## **Обзор**

Существует 3 способа применения умных фильтров в Aspose.PSD для Python.

## **Применение фильтра напрямую**

В этом образце кода мы видим пример использования умных фильтров напрямую в Aspose.PSD для Python.

Сначала код указывает исходный файл PSD, выходной файл для оригинального изображения и выходной файл для обновленного изображения.

Затем код загружает изображение PSD с помощью метода Image.load() и приводит его к объекту PsdImage.

Оригинальное изображение сохраняется с использованием метода save(), с указанием имени выходного файла.

Создается объект SharpenSmartFilter, представляющий умный фильтр, который должен быть применен.

Затем код извлекает обычный слой из изображения PSD, используя im.layers[1].

Затем используется цикл для применения фильтра улучшения к обычному слою три раза.

Наконец, обновленное изображение сохраняется с использованием метода save() и указанием имени выходного файла.

Этот код демонстрирует, как применять умные фильтры напрямую в Aspose.PSD для Python. Используя соответствующие объекты фильтров и применяя их к желаемым слоям, вы сможете достичь нужных эффектов на своих изображениях.

{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-psd-smart-filter-direct-apply.py" >}}

## **Управление умными фильтрами в умных объектах**

Сначала код указывает исходный файл PSD, выходной файл для оригинального изображения и выходной файл для обновленного изображения.

Изображение PSD загружается с использованием метода Image.load(), затем приводится к объекту PsdImage.

Оригинальное изображение сохраняется с использованием метода save(), с указанием имени выходного файла.

Затем код приводит второй слой изображения PSD к объекту SmartObjectLayer, представляющему слой умного объекта.

Далее код приступает к редактированию умных фильтров. В этом примере показано, как работать с двумя типами умных фильтров: GaussianBlurSmartFilter и AddNoiseSmartFilter.

Для GaussianBlurSmartFilter код обновляет значения фильтра, включая радиус, режим смешивания, непрозрачность и его состояние включенности или выключенности.

Для AddNoiseSmartFilter код устанавливает распределение шума на NoiseDistribution.UNIFORM.

Затем код добавляет два новых элемента фильтра к слою умного объекта: еще один GaussianBlurSmartFilter и AddNoiseSmartFilter.

После добавления новых фильтров код применяет изменения с использованием метода update_resource_values().

Наконец, код демонстрирует прямое применение фильтров к слою и маске слоя с использованием методов apply() и apply_to_mask() соответственно.

Обновленное изображение затем сохраняется с использованием метода save() и указанием имени выходного файла.

Следуя этому образцу кода, вы узнаете, как работать с умными фильтрами в Aspose.PSD для Python. Библиотека предоставляет широкий спектр умных фильтров, каждый со своим набором свойств и методов, которые можно настраивать для достижения нужных эффектов на ваших изображениях.

{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-psd-smart-filter-features.py" >}}

## **Применение умных фильтров к маске слоя**

Применение умных фильтров к маскам: мощная техника редактирования изображений

Умные фильтры - популярная функция в программном обеспечении для редактирования изображений, которая позволяет пользователям применять различные фильтры и эффекты к своим изображениям. Одним интересным приемом, который можно добиться с помощью умных фильтров, является их применение к маскам. В этой статье мы рассмотрим, как применять умные фильтры к маскам и обсудим их использование в мире редактирования изображений.

Что такое маска? Прежде чем мы углубимся в применение умных фильтров к маскам, давайте сначала поймем, что такое маска. В редактировании изображений маска - это полутоновое изображение, которое определяет прозрачность определенных областей изображения. Маску можно использовать для селективного применения фильтров, коррекций или эффектов к определенным частям изображения, оставляя другие области без изменений.

Применение умных фильтров к маскам: Когда умные фильтры применяются к маскам, фильтры применяются только к участкам, указанным на маске. Это позволяет точно контролировать, какие части изображения затрагивает фильтр. Путем манипулирования маской вы можете определить интенсивность и степень воздействия фильтра.

Пожалуйста, проверьте предыдущий пример и метод: [Справочник API Применение умного фильтра к маске](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.smartfilters/smartfilter/#apply_to_mask_layer_with_mask_2)
