---
title: Обрізання, Обертання та Зміна розміру Зображень
type: docs
weight: 40
url: /uk/java/crop-rotate-and-resize-images/
---

## **Обрізання Зображень**
Зазвичай обрізання зображень відноситься до видалення зовнішніх частин зображення для поліпшення композиції. Обрізка також може використовуватися для вирізання певної частини зображення, щоб збільшити увагу до конкретної області. API Aspose.PSD підтримує два різні підходи до обрізання зображень: за допомогою зсувів та прямокутника.
### **Обрізання за допомогою Зсувів**
Клас RasterImage надає перевантажену версію методу Crop, яка приймає 4 цілочисельні значення, що позначають Ліво, Право, Верх та Низ. На основі цих чотирьох значень метод Crop зсуває границі зображення до центру зображення, відкидаючи зовнішню частину. Наведений нижче фрагмент коду демонструє, як обрізати зображення за допомогою зсувів.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CroppingbyShifts-CroppingbyShifts.java" >}}
### **Обрізання за допомогою Прямокутника**
Клас RasterImage надає ще одну перевантажену версію методу Crop, яка приймає екземпляр класу Rectangle. Ви можете вирізати будь-яку частину зображення, вказавши бажані границі об'єкту Rectangle. Наведений нижче фрагмент коду демонструє, як обрізати будь-яке зображення за допомогою прямокутника.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CroppingbyRectangle-CroppingbyRectangle.java" >}}
## **Обертання та Віддзеркалювання Зображення**
Aspose.PSD для Java - це легка у використанні бібліотека, оскільки вона надає прості методи для виконання складних операцій. Наприклад, Aspose.PSD для Java надає метод RotateFlip для його базового класу Image, якщо додатку потрібно обертати зображення. Незалежно від формату зображення, бібліотека може виконати конкретну процедуру обертання та віддзеркалювання зображення.
### **Обертання Зображення**
Метод Image.RotateFlip може використовуватися для обертання зображення на 90/180/270 градусів та віддзеркалення горизонтально або вертикально. Метод Image.RotateFlip приймає параметр RotateFlipType, який вказує тип обертання та віддзеркалення, яке слід застосувати до зображення. Кроки для виконання обертання та віддзеркалення такі прості, як наведено нижче,

1. Завантажте зображення за допомогою фабричного методу Load, що надається класом Image.
1. Викличте метод Image.RotateFlip, вказавши відповідний RotateFlipType.
1. Збережіть результати.

Наведений нижче приклад коду демонструє, як встановити властивість RotateFlip для Image та перелік перечислення RotateFlipType.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-RotatinganImage-RotatinganImage.java" >}}
## **Обертання Зображення під Кутом**
API Aspose.PSD для Java надається метод RasterImage.Rotate для спрощення користувачам, які бажають обертати зображення під певним кутом. На відміну від методу RasterImage.RotateFlip, метод RasterImage.Rotate приймає три параметри:

1. Кут обертання: Параметр типу float, який вказує кут обертання, на який має бути обернуте зображення. Позитивне значення обертає зображення за годинниковою стрілкою; від'ємне значення виконує обертання проти годинникової стрілки.
1. Пропорційна зміна розміру: Параметр типу Boolean вказує, чи має змінюватися розмір зображення відповідно до проекцій обертаного прямокутника (точок кутів). Якщо встановлено false, розміри зображення залишаться незмінними, а обертаються лише внутрішні вміст зображення.
1. Колір тла: Параметр типу Color вказує колір, який буде заповнювати фон оберненого зображення.

Наведений нижче фрагмент коду демонструє використання методу RasterImage.Rotate.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-RotatinganImageonaSpecificAngle-RotatinganImageonaSpecificAngle.java" >}}
## **Зміна розміру Зображень**
У цій статті показано використання Aspose.PSD для Java для виконання операції зміни розміру зображення. API Aspose.PSD надає ефективні та прості у використанні методи для досягнення цієї мети. Aspose.PSD для Java надає метод Resize для класу Image, який може бути використаний для зміни розмірів існуючих зображень на льоту. Існують дві перевантажені версії методу Resize для відповідності потребам додатку.
### **Просте Змінювання розміру**
Кроки для зміни розміру такі прості, як наведено нижче:

1. Завантажте зображення за допомогою фабричного методу Load, що надається класом Image.
1. Викличте метод Image.Resize, вказавши нові Висоту та Ширину.
1. Збережіть результати.

Наведений нижче приклад коду демонструє, як змінити розмір зображення.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-SimpleResizing-SimpleResizing.java" >}}
### **Зміна розміру з використанням Перерахування ResizeType**
API Aspose.PSD надає перерахування ResizeType, яке можна використовувати з методом Image.Resize для досягнення бажаних результатів. Наведений нижче фрагмент коду демонструє використання перерахування ResizeType, тоді як подробиці членів перерахування ResizeType можна знайти внизу цієї сторінки.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ResizingwithResizeTypeEnumeration-ResizingwithResizeTypeEnumeration.java" >}}



Якщо ви маєте намір отримати якісний результат після застосування зміни розміру, то рекомендується завжди використовувати ResizeType.LanczosResample, оскільки він буде виводити високоякісні результати, але може працювати повільніше, ніж ResizeType.NearestNeighbourResample. З іншого боку, алгоритм ResizeType.NearestNeighbourResample використовується специфічно для швидкої зміни розміру, компромітуючи з якістю зображення. Цей метод може бути корисним для генерації мініатюр у реальному часі або подібних процесів, де вимагається продуктивність.
## **Зміна розміру Зображення пропорційно**
Ви можете змінити розмір зображень, передаючи нові значення висоти та ширини в якості параметрів методу Image.Resize, але в цьому випадку вам потрібно самостійно розрахувати відношення сторін. Це тому, що коли ширина або висота зображення змінюються, зображення масштабується або стискається для заповнення нового розміру . Якщо зміни ширини та висоти зображення не зберігають пропорції, це може призвести до розтягнутих та спотворених результатів. У цій статті показано використання API Aspose.PSD для Java для зміни розміру зображень, передаючи одну з нових висоти або ширини, дозволяючи API автоматично розрахувати інше пропорційне значення.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ResizeImageProportionally-ResizeImageProportionally.java" >}}
### **Перерахування ResizeType**
ResizeType визначає тип зміни розміру, що виконується на зображеннях на основі обраного фільтра.

Члени перерахування ResizeType

|**Назва Члену**|**Значення**|**Опис**|
| :- | :- | :- |
|LeftTopToLeftTop|0|Лівий верхній кут нового зображення буде збігатися з лівим верхнім кутом оригінального зображення. Обрізка відбудеться, якщо потрібно.|
|RightTopToRightTop|1|Правий верхній кут нового зображення буде збігатися з правим верхнім кутом оригінального зображення. Обрізка відбудеться, якщо потрібно.|
|RightBottomToRightBottom|2|Правий нижній кут нового зображення буде збігатися з правим нижнім кутом оригінального зображення. Обрізка відбудеться, якщо потрібно.|
|LeftBottomToLeftBottom|3|Лівий нижній кут нового зображення буде збігатися з лівим нижнім кутом оригінального зображення. Обрізка відбудеться, якщо потрібно.|
|CenterToCenter|4|Центр нового зображення буде збігатися з центром оригінального зображення. Обрізка відбудеться, якщо потрібно.|
|LanczosResample|5|Змінити розмір за допомогою алгоритму Ланцоша, використовуючи маску 7x7.|
|NearestNeighbourResample|6|Змінити розмір за допомогою алгоритму найближчого сусіда.|
