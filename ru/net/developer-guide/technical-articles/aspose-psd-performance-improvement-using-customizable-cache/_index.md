---
title: Улучшение производительности Aspose.PSD с помощью настраиваемого кэша
type: docs
weight: 20
url: /ru/net/aspose-psd-performance-improvement-using-customizable-cache/
---

## **Улучшение производительности с настраиваемым кэшем**
[Aspose.PSD](https://products.aspose.com/psd/family) использует кэширование для временного хранения данных. Механизм прост в использовании, настраиваем и прозрачен. Это гарантирует отсутствие проблем производительности во время обработки изображений. В этой статье объясняется, как настроить кэш с помощью API Aspose.PSD для .NET.
### **Настройка кэша**
Когда процессу требуется временное хранение данных, это хранение выделяется в кэше. Кэш может быть расположен в памяти или на диске и устанавливается пользователем. Когда временные данные больше не нужны, выделенное место освобождается. Статистику выделенного пространства можно проверить в любое время. Как Aspose.PSD выделяет и использует кэши, может быть настроено. В этом разделе описаны различные настройки и их значения по умолчанию, а код ниже показывает, как ими можно пользоваться.
### **Установка места выделения кэша**
Для настройки способа выделения места в кэше установите свойство [CacheType](https://reference.aspose.com/psd/net/aspose.psd/cachetype). По умолчанию кэш располагается в памяти, и когда в памяти не остается места, он выделяется на диске. Это поведение описывается Auto-режимом. Auto-режим является гибким и обеспечивает максимальную производительность. Также имеются другие режимы:

- режим CacheOnDiskOnly: выделение только на диск.
- режим CacheInMemoryOnly: выделение только в память.

Выбор режима CacheOnDiskOnly может привести к плохой производительности.
### **Установка размера кэша**
Установите максимальное пространство (в байтах), которое может быть выделено на диске или в памяти, установив свойства [MaxDiskSpaceForCache](https://reference.aspose.com/psd/net/aspose.psd/cache/properties/maxdiskspaceforcache) и [MaxMemoryForCache](https://reference.aspose.com/psd/net/aspose.psd/cache/properties/maxmemoryforcache) соответственно. По умолчанию оба значения установлены на 0, что означает, что нет верхнего предела.
### **Управление перераспределением кэша**
Если в памяти нет достаточного места (как указано в свойстве MaxMemoryForCache) при выделении нового кэша, кэш выделяется на диске. Если на диске нет достаточного места, возникает исключение. Процесс выделения кэша переходит из памяти на диск, но не наоборот. Свойство [ExactReallocateOnly](https://reference.aspose.com/psd/net/aspose.psd/cache/properties/exactreallocateonly) используется для управления перераспределением памяти. Перераспределение наиболее вероятно происходит для предварительно выделенных кэшей. Это может произойти, когда система понимает, что выделенного пространства не хватит. Если ExactReallocateOnly установлено на значение по умолчанию – False, место перераспределяется в том же среде. При установке значения True, перераспределение не может превышать максимально указанное пространство. В этом случае существующий кэш в памяти (который требует перераспределения) освобождается и выделяется дополнительное пространство на диске.
### **Примеры программ**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ControllCacheReallocation-ControllCacheReallocation.cs" >}}