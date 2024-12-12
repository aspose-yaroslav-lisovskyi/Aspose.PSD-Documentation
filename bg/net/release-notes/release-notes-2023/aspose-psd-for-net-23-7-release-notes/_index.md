---
title: Aspose.PSD за .NET 23.7 - Забележки за версията
type: docs
weight: 60
url: /bg/net/aspose-psd-za-net-23-7-zabelezhki-za-versiyata/
---

{{% alert color="primary" %}}

Тази страница съдържа забележки за [Aspose.PSD за .NET 23.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Ключ**    | **Обобщение**                                                                                                  | **Категория** |
|:-----------|:-------------------------------------------------------------------------------------------------------------|:------|
| PSDNET-802 | Добавяне на възможност за износ на всяко ниво на PSD файл към анимиран GIF файл                                        | Функционалност |
| PSDNET-1441 | Назначаване на свойството Fill на слоя на формата на фигура от ресурса vscg                                            | Функционалност |
| PSDNET-1534 | Добавяне на нови видове изкривяване (дъга и арка)                                                                    | Функционалност |
| PSDNET-1543 | Промяна на приложението, което записва PSD файла до Aspose.PSD, ако свойството UpdateMetadata е зададено на true    | Функционалност |
| PSDNET-1567 | Увеличаване на областта на изчислението на изкривяването на изображението                                           | Функционалност |
| PSDNET-1471 | Слой за корекция на черно и бяло обработва полу-прозрачността грешно                                               | Грешка |
| PSDNET-1505 | SmartObject ReplaceContents (когато опцията AllowWarpRepaint е активна) пада след 2 минути изчисляване              | Грешка |
| PSDNET-1585 | Добавяне на възможност за получаване на реалната позиция на LayerGroup - ляво и горе                                  | Грешка |
| PSDNET-1589 | Преоразмеряването на слоя работи грешно, когато PSD файла има VogkResource със структури в точки                   | Грешка |
| PSDNET-1608 | TextBound не работи както се очаква                                                                               | Грешка |
| PSDNET-1612 | Добавяне на слой, създаден с конструктор по подразбиране към PSD изображението, не добавя стандартни ресурси към него | Грешка |
| PSDNET-1623 | Timeline.LoopesCount се игнорира при експортиране към анимиран GIF                                                  | Грешка |


## **Промени в публичния API**
# **Добавени API:**
- P:Aspose.PSD.ImageOptions.PsdOptions.UpdateMetadata
- F:Aspose.PSD.FileFormats.Ai.AiFormatVersion.Pdf16
- F:Aspose.PSD.FileFormats.Ai.AiFormatVersion.Pdf17
- P:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.Item(System.String)
- M:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.SetValue(System.String,Aspose.PSD.Xmp.IXmlValue)
- M:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.ContainsKey(System.String)
- P:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.Fill


# **Премахнати API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.FillColor


## **Примери за използване:**

**PSDNET-802. Добавяне на възможност за износ на всяко ниво на PSD файл към анимиран GIF файл**

{{< highlight csharp >}}
string src = "EachLayerIsFrame.psd";
string outputGif = "out_EachLayerIsFrame.gif";
string outputPsd = "out_EachLayerIsFrame.psd";

using (var psdImage = (PsdImage)Image.Load(src))
{
    // Създаване на фреймове за всяко ниво.
    int framesCount = psdImage.Layers.Length;
    var timeline = psdImage.Timeline;

    Frame[] frames = new Frame[framesCount];
    for (int i = 0; i < framesCount; i++)
    {
        frames[i] = new Frame();
        LayerState[] layerStates = new LayerState[framesCount];

        for (int j = 0; j < framesCount; j++)
        {
            layerStates[j] = new LayerState();
            layerStates[j].Enabled = i == j;
        }

        frames[i].LayerStates = layerStates;
    }

    timeline.Frames = frames;

    // Update current states
    Layer[] layers = psdImage.Layers;
    LayerState[] states = timeline.Frames[timeline.ActiveFrameIndex].LayerStates;
    for (int i = 0; i < framesCount; i++)
    {
        layers[i].IsVisible = states[i].Enabled;
    }

    timeline.Save(outputGif, new GifOptions());
    psdImage.Save(outputPsd);
}
{{< /highlight >}}

**PSDNET-1441. Назначаване на свойството Fill на слоя на формата на фигура от ресурса vscg**

{{< highlight csharp >}}
string srcFile = "ShapeInternalSolid.psd";
string outFile = "ShapeInternalSolid.psd.out.psd";

using (PsdImage image = (PsdImage)Image.Load(
    srcFile,
    new PsdLoadOptions { LoadEffectsResource = true }))
{
    ShapeLayer shapeLayer = (ShapeLayer)image.Layers[1];
    ColorFillSettings fillSettings = (ColorFillSettings)shapeLayer.Fill;
    fillSettings.Color = Color.Red;

    shapeLayer.Update();

    image.Save(outFile);
}

// Проверка на записаните промени
using (PsdImage image = (PsdImage)Image.Load(
    outFile,
    new PsdLoadOptions { LoadEffectsResource = true }))
{
    ShapeLayer shapeLayer = (ShapeLayer)image.Layers[1];
    ColorFillSettings fillSettings = (ColorFillSettings)shapeLayer.Fill;

    AssertAreEqual(Color.Red, fillSettings.Color);

    image.Save(outFile);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Обектите не са равни.");
    }
}
{{< /highlight >}}


**PSDNET-1471. Слой за корекция на черно и бяло обработва полу-прозрачността грешно**

{{< highlight csharp >}}
string srcFile = "frog_nosymb.psd";
string outFile = "frog_nosymb.psd.out.psd";

using (PsdImage psdImage = (PsdImage)Image.Load(srcFile))
{
    psdImage.AddBlackWhiteAdjustmentLayer();
    psdImage.Save(outFile);
}

// Проверка на записаните промени
using (PsdImage image = (PsdImage)Image.Load(
    outFile,
    new PsdLoadOptions { LoadEffectsResource = true }))
{
    AssertAreEqual(2, image.Layers.Length);

    BlackWhiteAdjustmentLayer blackWhiteAdjustmentLayer = (BlackWhiteAdjustmentLayer)image.Layers[1];

    if (blackWhiteAdjustmentLayer == null)
    {
        throw new Exception("Лаер 2 трябва да бъде BlackWhiteAdjustmentLayer");
    }

    image.Save(outFile);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Обектите не са равни.");
    }
}
{{< /highlight >}}


**PSDNET-1505. SmartObject ReplaceContents (когато опцията AllowWarpRepaint е активна) пада след 2 минути изчисляване**

{{< highlight csharp >}}
string sourceFile = "mug 4.psd";
string changeFile = "artwork for replace.png";
string outputFile = "export.png";

int newHeight = 300;

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    SmartObjectLayer smartObjectLayer = (SmartObjectLayer)psdImage.Layers[3];

    var scale = (double)newHeight / smartObjectLayer.Height;
    var newWidth = (int)Math.Round(smartObjectLayer.Width * scale);

    PsdImage innerImage = new PsdImage(newWidth, newHeight);
    innerImage.SetResolution(72, 72);

    Stream innerStream = new FileStream(changeFile, FileMode.Open);
    Layer layer = new Layer(innerStream) { HorizontalResolution = 72, VerticalResolution = 72 };
    try
    {
        innerImage.AddLayer(layer);

        smartObjectLayer.ReplaceContents(innerImage);
        smartObjectLayer.UpdateModifiedContent();

        psdImage.Save(outputFile, new PngOptions
        {
            ColorType = PngColorType.TruecolorWithAlpha
        });
    }
    finally
    {
        innerImage.Dispose();
        innerStream.Dispose();
        layer.Dispose();
    }
}
{{< /highlight >}}


**PSDNET-1534. Добавяне на нови видове изкривяване (дъга и арка)**

{{< highlight csharp >}}
string sourceArcFile = "arc_warp.psd";
string outputArcFile = "arc_export.png";

string sourceArchFile = "arch_warp.psd";
string outputArchFile = "arch_export.png";

using (var psdImage = (PsdImage)Image.Load(sourceArcFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputArcFile, new PngOptions
    {
        ColorType = PngColorType.TruecolorWithAlpha
    });
}

using (var psdImage = (PsdImage)Image.Load(sourceArchFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputArchFile, new PngOptions
    {
        ColorType = PngColorType.TruecolorWithAlpha
    });
}
{{< /highlight >}}


**PSDNET-1543. Промяна на приложението, което записва PSD файла до Aspose.PSD, ако свойството UpdateMetadata е зададено на true**

{{< highlight csharp >}}
string path = "output.psd";
using (var image = new PsdImage(100, 100))
{
    // Ако желаете да се промени инструмента на създателя, уверете се, че "UpdateMetadata" е зададено на true. По подразбиране е true.
    var psdOptions = new PsdOptions();
    psdOptions.UpdateMetadata = true;

    // Запазване на изображението
    image.Save(path, psdOptions);

    // Проверка на инструмента на създателя в кода
    var xmpData = image.XmpData;
    var basicPackage = image.XmpData.GetPackage(Namespaces.XmpBasic);

    // Тук ще бъде актуализиран инструмент на създателя
    var currentCreatorTool = (string)basicPackage[":CreatorTool"];
}
{{< /highlight >}}


**PSDNET-1567. Увеличаване на областта на изчислението на изкривяването на изображението**

{{< highlight csharp >}}
string sourceFile = "mug4_warp.psd";
string outputFile = "mug4_export.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFile, new PngOptions
    {
        ColorType = PngColorType.TruecolorWithAlpha
    });
}
{{< /highlight >}}


**PSDNET-1585. Добавяне на възможност за получаване на реалната позиция на LayerGroup - ляво и горе**

{{< highlight csharp >}}
string sourceFile = "layerGroupFigures.psd";

void AssertAreEqual(object expected, object actual)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception("Обектите не са равни.");
    }
}

using (var image = (PsdImage)Image.Load(sourceFile))
{
    var layers = image.Layers;

    for (int i = 0; i < layers.Length; i++)
    {
        var layer = layers[i];

        if (layer is LayerGroup)
        {
            // Получаване на LayerGroup
            var group = (LayerGroup)layer;

            var expectedLeft = int.MaxValue;
            var expectedTop = int.MaxValue;
            var expectedRight = 0;
            var expectedBottom = 0;

            // Изчисляване на реалните ляво, горе, дясно и долно позиции
            foreach (var innerLayer in group.Layers)
            {
                if (innerLayer is AdjustmentLayer || innerLayer.Bounds.IsEmpty)
                {
                    continue;
                }

                expectedLeft = Math.Min(expectedLeft, innerLayer.Left);
                expectedTop = Math.Min(expectedTop, innerLayer.Top);
                expectedRight = Math.Max((expectedLeft + group.Width), (innerLayer.Left + innerLayer.Width));
                expectedBottom = Math.Max((expectedTop + group.Height), (innerLayer.Top + innerLayer.Height));
            }

            // Левият, горният, десният и долният краища на LayerGroup са изчислени правилно
            AssertAreEqual(group.Left, expectedLeft);
            AssertAreEqual(group.Top, expectedTop);
            AssertAreEqual(group.Right, expectedRight);
            AssertAreEqual(group.Bottom, expectedBottom);
        }
    }
}
{{< /highlight >}}


**PSDNET-1589. Преоразмеряването на слоя работи грешно, когато PSD файла има VogkResource със структури в точки**

{{< highlight csharp >}}
string[] sourceFiles = new string[]
{
    "PointsVectorOrigin.psd",
    "TopVogkResStruct.psd"
};

foreach (string sourceFile in sourceFiles)
{
    using (PsdImage image = (PsdImage)Image.Load(sourceFile))
    {
        Layer layer = image.Layers[0];

        layer.Resize(50, 50);

        AssertAreEqual(layer.Height, 50);
        AssertAreEqual(layer.Width, 50);
    }
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Обектите не са равни.");
    }
}
{{< /highlight >}}


**PSDNET-1608. TextBound не работи както се очаква**

{{< highlight csharp >}}
string sourceFile = "input_Test_forTicket.psd";
string outFile = "out_1608.psd";

Size newTextBox = new Size(-1, -1);
using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(sourceFile))
{
    // Стъпка: Замяна на текста
    TextLayer textLayer = (TextLayer)psdImage.Layers[3];
    textLayer.TextData.Items[0].Text = "Text test replaced";

    // Стъпка: Актуализиране на TextBoundBox
    textLayer.TextData.UpdateLayerData();
    newTextBox = new Size((int)Math.Ceiling(textLayer.TextBoundBox.Width), textLayer.Height);

    textLayer.TextBoundBox = new Aspose.PSD.RectangleF(PointF.Empty, newTextBox);
    textLayer.TextData.UpdateLayerData();

    psdImage.Save(outFile);
}

// Проверка на промените
using (var psdImage = (PsdImage)Image.Load(outFile))
{
    Txt2Resource txt2Resource = (Txt2Resource)psdImage.GlobalLayerResources[1];
    string textData = Encoding.GetEncoding("Windows-1251").GetString(txt2Resource.Data);

    string search = "<< /0 << /1 << /0 ["; // специфичен набор от символи, за да се намери стойността на textBox в този файл.

    int startIndex = textData.IndexOf(search) + search.Length;
    int endIndex = textData.IndexOf("]", startIndex);
    string boxItems = textData.Substring(startIndex, endIndex - startIndex);

    string height = newTextBox.Height.ToString("0.0####").Replace(",", ".");
    string width = newTextBox.Width.ToString("0.0####").Replace(",", ".");

    if (!boxItems.Contains(height) || !boxItems.Contains(width))
    {
        throw new Exception("TextBox не е актуализиран.");
    }
}
{{< /highlight >}}


**PSDNET-1612. Добавяне на слой, създад{{< highlight csharp >}}
ен с конструктор по подразбиране към PSD изображението, не добавя стандартни ресурси към него**

{{< highlight csharp >}}
string output = "newLayer.psd";

using (var psdImage = new PsdImage(500, 500))
{
    var layer = new Layer();
    psdImage.AddLayer(layer);

    LyidResource lyidResource = (LyidResource)FindResource(LyidResource.TypeToolKey, layer.Resources);

    int layerId = lyidResource.Value; // Was NullReferenceException

    psdImage.Save(output);
}

LayerResource FindResource(int resType, LayerResource[] resources)
{
    if (resources != null)
    {
        foreach (var layerResource in resources)
        {
            if (layerResource.Key == resType)
            {
                return layerResource;
            }
        }
    }

    return null;
}
{{< /highlight >}}

**PSDNET-1623. Timeline.LoopesCount се игнорира при експортиране към анимиран GIF** 

{{< highlight csharp >}}
string sourceFile = "4_animated.psd";
string outputGif = "out_4_animated.psd.gif";

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    psdImage.Timeline.Save(outputGif, new GifOptions());
}
{{< /highlight >}}