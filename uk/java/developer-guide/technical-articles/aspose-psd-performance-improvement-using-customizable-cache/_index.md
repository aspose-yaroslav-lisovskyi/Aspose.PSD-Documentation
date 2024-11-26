---
title: Покращення продуктивності Aspose.PSD за допомогою налаштованого кешу
type: docs
weight: 30
url: /uk/java/aspose-psd-performance-improvement-using-customizable-cache/
---

## **Покращення продуктивності за допомогою налаштованого кешу**
Aspose.PSD використовує кешування для тимчасового зберігання даних. Механізм є простим у використанні, налаштовуваним та прозорим. Він забезпечує відсутність проблем з продуктивністю під час обробки зображень. У цій статті пояснено, як налаштувати кеш за допомогою API Aspose.PSD для Java.
### **Налаштування кешу**
Коли процесу потрібно тимчасове зберігання даних, це зберігання розподіляється в кеші. Кеш може бути простором у пам'яті або на диску і налаштовується користувачем. Коли тимчасові дані більше не потрібні, простір вивільняється. Статистика виділеного простору може бути перевірена у будь-який момент. Те, як Aspose.PSD розподіляє та використовує кеші, можна налаштувати. У цьому розділі описано різні параметри та їх значення за замовчуванням, а нижче наведено приклади коду, як їх можна використовувати.
### **Вибір місця для виділення кешу**
Для налаштування способу розподілу простору кешу встановлюйте властивість CacheType. За замовчуванням кеш виділяється у пам'яті, і якщо вільного місця в пам'яті немає, він виділяється на диск. Така поведінка фіксується режимом Auto. Режим Auto є гнучким та максимізує продуктивність. Також існують інші режими:

- режим CacheOnDiskOnly: виділення лише на диск.
- режим CacheInMemoryOnly: виділення лише у пам'ять.

Вибір режиму CacheOnDiskOnly може призвести до поганої продуктивності.
### **Встановлення розміру кешу**
Встановіть максимальний обсяг (в байтах), який може бути виділений на диску або у пам'яті, встановивши властивості MaxDiskSpaceForCache та MaxMemoryForCache відповідно. За замовчуванням обидва значення встановлені на 0, що означає, що верхнього обмеження немає.
### **Управління перерозподілом кешу**
Якщо в пам'яті недостатньо вільного місця (як вказано у властивості MaxMemoryForCache) під час виділення нового кешу, кеш виділяється на диск. Якщо на диску недостатньо місця, виникає виняток. Процес виділення кешу зміщується з пам'яті на диск, але не навпаки. Властивість ExactReallocateOnly використовується для контролю перерозподілу пам'яті. Перерозподіл ймовірний для попередньо виділених кешів. Це може статися, коли система визначає, що виділений простір буде недостатнім. Якщо ExactReallocateOnly встановлено на значення за замовчуванням, False, простір знову виділяється у ту ж саму середу. Якщо встановлено True, перерозподіл не може перевищувати максимально визначений простір. У цьому випадку існуючий виділений кеш у пам'яті (який потребує перерозподілу) вивільняється, і виділяється додатковий простір на диску.
### **Приклади програм**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ControllCacheReallocation-ControllCacheReallocation.java" >}}