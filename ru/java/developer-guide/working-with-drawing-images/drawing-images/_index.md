---
title: Рисование изображений
type: документация
weight: 10
url: /ru/java/drawing-images/
---

## **Рисование линий**
В этом примере используется класс Graphics для рисования линий на поверхности изображения. Чтобы продемонстрировать операцию, пример создает новое изображение и рисует линии на поверхности изображения, используя метод DrawLine, предоставленный классом Graphics. Сначала мы создадим PsdImage, указав его высоту и ширину.

После создания изображения мы будем использовать метод Clear, предоставленный классом Graphics, чтобы установить цвет фона. Метод DrawLine класса Graphics используется для рисования линии на изображении, соединяющей две точечные структуры. Этот метод имеет несколько перегруженных версий с экземпляром класса Pen и парами координат или структурами Point/PointF в качестве аргументов. Класс Pen определяет объект, используемый для рисования линий, кривых и фигур. У класса Pen есть несколько перегруженных конструкторов для рисования линий с указанным цветом, шириной и кистью. Класс SolidBrush используется для непрерывного рисования с определенным цветом. И, наконец, изображение экспортируется в формат файла BMP. В следующем фрагменте кода показано, как рисовать линии на поверхности изображения.

## **Рисование эллипса**
Пример рисования эллипса является второй статьей в серии статей о рисовании форм. Мы будем использовать класс Graphics для рисования формы эллипса на поверхности изображения. Чтобы продемонстрировать операцию, пример создает новое изображение и рисует форму эллипса на поверхности изображения, используя метод DrawEllipse, предоставленный классом Graphics. Сначала мы создадим PsdImage, указав его высоту и ширину.

После создания изображения мы создадим и инициализируем объект класса Graphics и установим цвет фона изображения, используя метод Clear класса Graphics. Метод DrawEllipse класса Graphics используется для рисования формы эллипса на поверхности изображения, указанной структурой ограничивающего прямоугольника. Этот метод имеет несколько перегруженных версий с экземплярами классов Pen и Rectangle/RectangleF или парами координат, высотой и шириной в качестве аргументов. Класс Pen определяет объект, используемый для рисования линий, кривых и фигур. У класса Pen есть несколько перегруженных конструкторов для рисования линий с указанным цветом, шириной и кистью. Класс Rectangle хранит набор из четырех целых чисел, представляющих местоположение и размер прямоугольника. У класса Rectangle есть несколько перегруженных конструкторов для рисования структуры прямоугольника с указанным размером и местоположением. Класс SolidBrush используется для непрерывного рисования с определенным цветом. И, наконец, изображение экспортируется в формат файла BMP. В следующем фрагменте кода показано, как рисовать форму эллипса на поверхности изображения.

## **Рисование прямоугольника**
В этом примере мы нарисуем прямоугольную форму на поверхности изображения. Чтобы продемонстрировать операцию, пример создает новое изображение и рисует прямоугольную форму на поверхности изображения, используя метод DrawRectangle, предоставленный классом Graphics. Сначала мы создадим PsdImage, указав его высоту и ширину. Затем мы установим цвет фона изображения, используя метод Clear класса Graphics.

Метод DrawRectangle класса Graphics используется для рисования прямоугольной формы на поверхности изображения, указанной структурой прямоугольника. Этот метод имеет несколько перегруженных версий с экземплярами классов Pen и Rectangle/RectangleF или парой координат, шириной и высотой в качестве аргументов. Класс Rectangle хранит набор из четырех целых чисел, представляющих местоположение и размер прямоугольника. У класса Rectangle есть несколько перегруженных конструкторов для рисования структуры прямоугольника с указанным размером и местоположением. И, наконец, изображение экспортируется в формат файла BMP. В следующем фрагменте кода показано, как рисовать прямоугольную форму на поверхности изображения.

## **Рисование дуги**
В этом разделе серии статей о рисовании форм мы нарисуем форму дуги на поверхности изображения. Мы будем использовать метод DrawArc класса Graphics, чтобы продемонстрировать операцию на изображении BMP. Сначала мы создадим PsdImage, указав его высоту и ширину. После создания изображения мы будем использовать метод Clear, предоставленный классом Graphics, чтобы установить цвет фона.

Метод DrawArc класса Graphics используется для рисования формы дуги на поверхности изображения. DrawArc представляет часть эллипса, указанную структурой прямоугольника или парой координат. Этот метод имеет несколько перегруженных версий с экземплярами классов Pen и Rectangle/RectangleF или парой координат, шириной и высотой в качестве аргументов. И, наконец, изображение экспортируется в формат файла BMP. В следующем фрагменте кода показано, как рисовать форму дуги на поверхности изображения.

## **Рисование кривой Безье**
В этом примере используется класс Graphics для рисования формы Безье на поверхности изображения. Чтобы продемонстрировать операцию, пример создает новое изображение и рисует форму Безье на поверхности изображения, используя метод DrawBezier, предоставленный классом Graphics. Сначала мы создадим PsdImage, указав его высоту и ширину. После создания изображения мы будем использовать метод Clear, предоставленный классом Graphics, чтобы установить цвет фона.

Метод DrawBezier класса Graphics используется для рисования кривой Безье на поверхности изображения, определенной четырьмя структурами Point. Этот метод имеет несколько перегруженных версий с экземплярами класса Pen и четырьмя упорядоченными парами координат или четырьмя структурами Point/PointF или массивом структур Point/PointF. Класс Pen определяет объект, используемый для рисования линий, кривых и фигур. У класса Pen есть несколько перегруженных конструкторов для рисования линий с указанным цветом, шириной и кистью. И, наконец, изображение экспортируется в формат файла BMP. В следующем фрагменте кода показано, как рисовать форму Безье на поверхности изображения.

## **Рисование изображений с использованием основного функционала**
Aspose.PSD - это библиотека, предлагающая множество ценных функций, включая создание изображений с нуля. Рисуйте с использованием основных функций, таких как изменение информации о битовой карты изображения или используйте продвинутые функции, такие как Graphics и GraphicsPath, чтобы рисовать формы на поверхности изображения с помощью различных кистей и перьев. Используя класс RasterImage Aspose.PSD, вы можете извлечь информацию о пикселях области изображения и манипулировать ею. Класс RasterImage содержит весь основной функционал рисования, такой как получение и установка пикселей и другие методы для манипуляций с изображением. Создайте новое изображение, используя любой из методов, описанных в "Создание файлов", и назначьте его экземпляру класса RasterImage. Используйте метод LoadPixels класса RasterImage для извлечения информации о пикселях части изображения. После получения массива пикселей его можно манипулировать, например, изменяя цвет каждого пикселя. После манипуляции информацией о пикселях, установите ее обратно в желаемую область на изображении, используя метод SavePixels класса RasterImage. В следующем фрагменте кода показано, как рисовать изображения с использованием основного функционала.