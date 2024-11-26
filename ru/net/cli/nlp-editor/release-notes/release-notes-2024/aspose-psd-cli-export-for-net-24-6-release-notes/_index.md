---
title: Релизные заметки Aspose.PSD CLI NLP Editor для .NET 24.6
type: docs
weight: 90
url: /ru/net/cli/nlp-editor/aspose-psd-nlp-editor-cli-app-for-net-24-6-release-notes/
---
{{% alert color="primary" %}}

Эта страница содержит релизные заметки для [Aspose.PSD CLI NLP Editor для .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.NLP.Editor/)

{{% /alert %}}

| **Ключ**    | **Краткое описание**                                                                       | **Категория** |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Первый релиз приложений Aspose.PSD CLI: Aspose.PSD.CLI.Export и Aspose.PSD.CLI.NLP.Editor  |  Улучшение   |


## **Примеры использования:**

**PSDNET-2110. Первый релиз приложения Aspose.PSD CLI NLP Editor**

## **Использование из командной строки:**

{{% alert color="primary" %}}
Сначала установите этот инструмент dotnet:
{{< highlight bash >}}dotnet tool install --global Aspose.PSD.CLI.NLP.Editor --version 24.6.0{{< /highlight >}}

Мы рекомендуем перед первым использованием выполнить следующую команду:
{{< highlight bash >}}Aspose.PSD.CLI.NLP.Editor --setup nlp.cli{{< /highlight >}}
После этой команды вы сможете запускать это приложение с коротким именем nlp.cli вместо Aspose.PSD.CLI.NLP.Editor. Вы можете указать собственное короткое имя.
{{% /alert %}}

**Примеры использования**

1. Эта команда конвертирует первый найденный файл (который можно открыть с помощью aspose.psd) из текущей папки и сохранит его в формате png с прозрачностью. Также будет установлена лицензия. Лицензию нужно указать только один раз. На следующих запусках лицензия будет использоваться из указанного пути. Эта команда покажет подробный журнал обработки NLP, если он доступен. 
{{< highlight bash >}}nlp.cli Конвертировать файл из этой папки в формат png с альфой --лицензия "C:\Aspose\LicenseFile.lic --verbose "{{< /highlight >}}

2. Эта команда найдет файл с наиболее схожим именем с "smth.psd". Затем она настроит контраст и сохранит его в jpeg с лучшим качеством. Название выходного файла будет выведено. Это будет smth.jpg 
{{< highlight bash >}}Настроить контраст на 10 у слоя с именем ellipse в файле smth.psd и сохранить его в output.jpg с лучшим качеством{{< /highlight >}}

3. Эта команда повернет файл по указанному пути и уменьшит его размер на 25%. Выходной файл будет выведен. Он будет сохранен в текущей папке консоли.
{{< highlight bash >}}Изменить размер файла C:\Users\someuser\Desktop\input.psd на 25%{{< /highlight >}}

4. Эта команда найдет файл input.psd в  C:\Users\someuser\Desktop\. Затем она найдет слой с индексом 3 и изменит его размер на ширину 50px и высоту 100px. Затем этот слой будет сохранен в формате PDF в C:\Users\someuser\Desktop\output.pdf
{{< highlight bash >}}Изменить размер слоя с индексом 3 из C:\Users\someuser\Desktop\input.psd на ширину 50 и высоту 100 и сохранить его в C:\Users\someuser\Desktop\output.pdf{{< /highlight >}}

5. Эта команда откроет smth.psd в текущей папке, но все эффекты будут отключены. Затем этот файл будет преобразован в формат BMP и будет выведен в output.bmp в текущей папке.
{{< highlight bash >}}Открыть smth.psd без эффектов и сохранить его в output.bmp{{< /highlight >}}

**Отказ от ответственности**

Это экспериментальное приложение. Пожалуйста, попробуйте его и оставьте отзыв. Любой отзыв очень ценен. Мы хотим поднять приложение без кода на новый уровень. Наша цель - легкая интеграция в любую систему сборки или бизнес-процесс.