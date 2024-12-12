---
title: Избягване на деградация на производителността при рисуване върху компресирани изображения
type: docs
weight: 10
url: /bg/net/избягване-на-деградация-на-производителността-при-рисуване-върху-компресирани-изображения/
---

## **Избягване на деградация на производителността при рисуване върху компресирани изображения**
Има моменти, когато искате да извършите изключително обширни графични операции върху компресирано изображение. Когато Aspose.PSD трябва да компресира и декомпресира изображения на летището, може да се стигне до деградация на производителността. Рисуването върху компресирани изображения също може да доведе до наказание за производителността.

### **Решение**
За да избегнете деградация на производителността, препоръчваме ви да конвертирате изображението в некомпресиран, или суров, формат преди извършването на графични операции.

### **Използване на път на файла**
В примера, който следва, PSD изображението се конвертира във формат без компресия и се запазва на диск. Некомпресираното изображение се зарежда отново, преди да бъдат извършени графични операции върху него. Същата техника се прилага и за BMP и GIF файлове.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-UncompressedImageUsingFile-UncompressedImageUsingFile.cs" >}}

### **Използване на обект Stream**
Следният откъс код показва как PSD изображение се конвертира в суров формат (без компресия) и се запазва на диск, използвайки MemoryStream.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-UncompressedImageStreamObject-UncompressedImageStreamObject.cs" >}}