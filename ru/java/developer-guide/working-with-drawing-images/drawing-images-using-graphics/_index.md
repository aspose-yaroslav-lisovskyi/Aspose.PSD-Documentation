---
title: Рисование изображений с использованием Graphics
type: docs
weight: 20
url: /ru/java/drawing-images-using-graphics/
---

## **Рисование изображений с использованием Graphics**

С библиотекой Aspose.PSD вы можете рисовать простые фигуры, такие как линии, прямоугольники и круги, а также сложные формы, такие как многоугольники, кривые, дуги и фигуры Безье. Библиотека Aspose.PSD создает такие формы с помощью класса Graphics, который находится в пространстве имен Aspose.PSD. Объекты Graphics отвечают за выполнение различных операций рисования на изображении, меняя его поверхность. Класс Graphics использует различные вспомогательные объекты для улучшения форм:

- Ручки (Pens), для рисования линий, контуров форм или отображения других геометрических представлений.
- Кисти (Brushes), для определения заполнения областей.
- Шрифты (Fonts), для определения формы символов текста.
### **Рисование с использованием класса Graphics**
Ниже приведен пример кода, демонстрирующий использование класса Graphics. Исходный код примера разделен на несколько частей, чтобы он был простым и легким для следования. Шаг за шагом примеры показывают, как:

1. Создать изображение.
1. Создать и инициализировать объект Graphics.
1. Очистить поверхность.
1. Нарисовать эллипс.
1. Нарисовать заполненный многоугольник и сохранить изображение.
### **Примеры программирования**
#### **Создание изображения**
Начните с создания изображения, используя любой из описанных методов в разделе Создание файлов.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingBezier-DrawingBezier.java" >}}
#### **Создание и инициализация объекта Graphics**
Затем создайте и инициализируйте объект Graphics, передав объект Image в его конструктор.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingArc-DrawingArc.java" >}}
#### **Очистка поверхности**
Очистите поверхность Graphics, вызвав метод Clear класса Graphics и передавая цвет в качестве параметра. Этот метод заполнит поверхность Graphics переданным в аргументе цветом.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.java" >}}
#### **Нарисовать эллипс**
Вы можете заметить, что класс Graphics предоставляет множество методов для рисования и заполнения форм. Полный список методов можно найти в справочнике API Aspose.PSD для Java. Класс Graphics представляет несколько перегруженных версий метода DrawEllipse. Все эти методы принимают объект Pen в качестве первого аргумента. Последующие параметры используются для определения ограничивающего прямоугольника вокруг эллипса. Для данного примера используйте версию, принимающую объект Rectangle в качестве второго параметра, чтобы нарисовать эллипс с использованием объекта Pen выбранного вами цвета.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingEllipse-DrawingEllipse.java" >}}
#### **Нарисовать заполненный многоугольник**
Затем нарисуйте многоугольник, используя LinearGradientBrush и массив точек. Класс Graphics предоставляет несколько перегруженных версий метода FillPolygon. Все они принимают объект Brush в качестве первого аргумента, определяя характеристики заливки. Второй параметр - это массив точек. Обратите внимание, что каждые две последовательные точки в массиве указывают сторону многоугольника.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.java" >}}
### **Рисование изображений с использованием Graphics: Полный исходный код**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.java" >}}

Все классы, реализующие IDisposable и имеющие доступ к неуправляемым ресурсам, создаются в операторе Using, чтобы гарантировать их правильное уничтожение.