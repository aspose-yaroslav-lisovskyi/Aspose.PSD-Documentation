---
title: Бележки към версията 19.7 на Aspose.PSD за .NET
type: docs
weight: 60
url: /bg/net/aspose-psd-for-net-19-7-release-notes/
---

{{% alert color="primary" %}} 

Тази страница съдържа бележки към версията на [Aspose.PSD за .NET 19.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Ключ**|**Резюме**|**Категория**|
| :- | :- | :- |
|PSDNET-126|Поддръжка за обработка на векторни маски на слоеве|Функция|
|PSDNET-130|Имплементиран коректен метод за преоразмеряване за PSD файлове|Функция|
|PSDNET-165|Добавена поддръжка за експортиране на PSD в PDF|Функция|
|PSDNET-186|Добавена поддръжка за експортиране на AI формат (Версия 2 и 3) в други формати|Функция|

## **Промени в публичното API**
# **Добавени API:**
- F:Aspose.PSD.FileFormat.Ai
- T:Aspose.PSD.FileFormats.Ai.AiDataSection
- M:Aspose.PSD.FileFormats.Ai.AiDataSection.GetData
- M:Aspose.PSD.FileFormats.Ai.AiDataSection.Dispose
- T:Aspose.PSD.FileFormats.Ai.AiFinalizeSection
- M:Aspose.PSD.FileFormats.Ai.AiFinalizeSection.GetData
- T:Aspose.PSD.FileFormats.Ai.AiFormatVersion
- F:Aspose.PSD.FileFormats.Ai.AiFormatVersion.PsAdobe20
- F:Aspose.PSD.FileFormats.Ai.AiFormatVersion.PsAdobe30
- F:Aspose.PSD.FileFormats.Ai.AiFormatVersion.Pdf14
- F:Aspose.PSD.FileFormats.Ai.AiFormatVersion.Pdf15
- T:Aspose.PSD.FileFormats.Ai.AiHeader
- P:Aspose.PSD.FileFormats.Ai.AiHeader.Creator
- P:Aspose.PSD.FileFormats.Ai.AiHeader.For
- P:Aspose.PSD.FileFormats.Ai.AiHeader.Title
- P:Aspose.PSD.FileFormats.Ai.AiHeader.CreationDate
- P:Aspose.PSD.FileFormats.Ai.AiHeader.DocumentProcessColors
- P:Aspose.PSD.FileFormats.Ai.AiHeader.DocumentProcSets
- P:Aspose.PSD.FileFormats.Ai.AiHeader.BoundingBox
- P:Aspose.PSD.FileFormats.Ai.AiHeader.ColorUsage
- P:Aspose.PSD.FileFormats.Ai.AiHeader.TemplateBox
- P:Aspose.PSD.FileFormats.Ai.AiHeader.TileBox
- P:Aspose.PSD.FileFormats.Ai.AiHeader.DocumentPreview
- P:Aspose.PSD.FileFormats.Ai.AiHeader.Item(System.String)
- T:Aspose.PSD.FileFormats.Ai.AiImage
- M:Aspose.PSD.FileFormats.Ai.AiImage.#ctor
- P:Aspose.PSD.FileFormats.Ai.AiImage.FileFormat
- P:Aspose.PSD.FileFormats.Ai.AiImage.Version
- P:Aspose.PSD.FileFormats.Ai.AiImage.Header
- P:Aspose.PSD.FileFormats.Ai.AiImage.SetupSection
- P:Aspose.PSD.FileFormats.Ai.AiImage.FinalizeSection
- P:Aspose.PSD.FileFormats.Ai.AiImage.DataSection
- P:Aspose.PSD.FileFormats.Ai.AiImage.IsCached
- P:Aspose.PSD.FileFormats.Ai.AiImage.BitsPerPixel
- P:Aspose.PSD.FileFormats.Ai.AiImage.Width
- P:Aspose.PSD.FileFormats.Ai.AiImage.Height
- M:Aspose.PSD.FileFormats.Ai.AiImage.CacheData
- M:Aspose.PSD.FileFormats.Ai.AiImage.Resize(System.Int32,System.Int32,Aspose.PSD.ResizeType)
- M:Aspose.PSD.FileFormats.Ai.AiImage.Resize(System.Int32,System.Int32,Aspose.PSD.ImageResizeSettings)
- M:Aspose.PSD.FileFormats.Ai.AiImage.RotateFlip(Aspose.PSD.RotateFlipType)
- M:Aspose.PSD.FileFormats.Ai.AiImage.SetPalette(Aspose.PSD.IColorPalette,System.Boolean)
- T:Aspose.PSD.FileFormats.Ai.AiSetupSection
- M:Aspose.PSD.FileFormats.Ai.AiSetupSection.GetData
- P:Aspose.PSD.ImageOptions.PdfOptions.PageSize
# **Премахнати API:**
- Няма

## **Примери за използване:**
**PSDNET-126. Поддръжка за обработка на векторни маски на слоеве**

{{< highlight java >}}

             string sourceFileName = "DifferentLayerMasks_Source.psd";

            string exportPath = "DifferentLayerMasks_Export.psd";

            string exportPathPng = "DifferentLayerMasks_Export.png";

            // reading

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

            {

                // make changes to the vector path points

                foreach (var layer in image.Layers)

                {

                    foreach (var layerResource in layer.Resources)

                    {

                        var resource = layerResource as VectorPathDataResource;

                        if (resource != null)

                        {

                            foreach (var pathRecord in resource.Paths)

                            {

                                var bezierKnotRecord = pathRecord as BezierKnotRecord;

                                if (bezierKnotRecord != null)

                                {

                                    Point p0 = bezierKnotRecord.Points[0];

                                    bezierKnotRecord.Points[0] = bezierKnotRecord.Points[2];

                                    bezierKnotRecord.Points[2] = p0;

                                    break;

                                }

                            }

                        }

                    }

                }

                // exporting

                image.Save(exportPath);

                image.Save(exportPathPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

            }

{{< /highlight >}}

**PSDNET-130. Имплементиран коректен метод за преоразмеряване за PSD файлове**

{{< highlight java >}}

              // Имплементиран коректен метод за преоразмеряване за PSD файлове.

            string sourceFileName = "1.psd";

            string exportPathPsd = "ResizeTest.psd";

            string exportPathPng = "ResizeTest.png";

            using (RasterImage image = Image.Load(sourceFileName) as RasterImage)

            {

                image.Resize(160, 120);

                image.Save(exportPathPsd, new PsdOptions());

                image.Save(exportPathPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

            }           

{{< /highlight >}}

**PSDNET-165. Добавена поддръжка за експортиране на PSD в PDF**

{{< highlight java >}}

   // Добавена поддръжка за експорт на PSD към PDF

    string[] sourcesFiles = new string[]

    {

        @"1.psd",

        @"little.psb",

        @"psb3.psb",

        @"inRgb16.psd",

        @"ALotOfElementTypes.psd",

        @"ColorOverlayAndShadowAndMask.psd",

        @"ThreeRegularLayersSemiTransparent.psd"

    };

    for (int i = 0; i < sourcesFiles.Length; i++)

    {

        string sourceFileName = sourcesFiles[i];

        using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

        {

           string outFileName = "PsdToPdf" + i + ".pdf";

           image.Save(outFileName, new PdfOptions());

        }

    }

{{< /highlight >}}

**PSDNET-186. Добавена поддръжка за експортиране на AI формат (Версия 2 и 3) в други формати**

{{< highlight java >}}

 // Добавена поддръжка за експортиране на AI формат (Версия 2 и 3) в други формати

            string[] sourcesFiles = new string[]

            {

                @"34992OStroke",

                @"rect2_color",

            };

            for (int i = 0; i < sourcesFiles.Length; i++)

            {

                string name = sourcesFiles[i];

                string sourceFileName = @"testdata\Images\Ai\" + name + ".ai";

                ImageOptionsBase options;

                string outFileName;

                using (AiImage image = (AiImage)Image.Load(sourceFileName))

                {

                    outFileName = name + ".psd";

                    options = new PsdOptions();

                    image.Save(outFileName, options);

                    outFileName = name + ".png";

                    options = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };

                    image.Save(outFileName, options);

                    outFileName = name + ".jpg";

                    options = new JpegOptions() { Quality = 85 };

                    image.Save(outFileName, options);

                    outFileName = name + ".gif";

                    options = new GifOptions() { DoPaletteCorrection = false };

                    image.Save(outFileName, options);

                    outFileName = name + ".tif";

                    options = new TiffOptions(TiffExpectedFormat.TiffDeflateRgba);

                    image.Save(outFileName, options);

                    outFileName = name + ".psd";

                    options = new PsdOptions();

                    image.Save(outFileName, options);

                }

            }

{{< /highlight >}}
