---
title: Aspose.PSD для .NET 21.10 - Примечания к выпуску
type: docs
weight: 30
url: /ru/net/aspose-psd-для-net-21-10-примечания-к-выпуску/
---

{{% alert color="primary" %}} 

Эта страница содержит примечания к выпуску [Aspose.PSD для .NET 21.10](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Ключ**|**Описание**|**Категория**|
| :- | :- | :- |
|PSDNET-128|Поддержка механизма умных фильтров|Функция|
|PSDNET-414|Поддержка Fxid/FEidResource|Функция|
|PSDNET-556|Ошибка при загрузке структуры AliasStructure|Ошибка|
|PSDNET-948|Изменение шрифта и цвета для текстового слоя PSD|Ошибка|
|PSDNET-971|Добавление возможности создания пользовательского слоя с векторной маской|Улучшение|

## **Изменения в общедоступном API**
# **Добавленные API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.SmartFilters
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.AddNoiseSmartFilter
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.AddNoiseSmartFilter.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.AddNoiseSmartFilter.Name
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.AddNoiseSmartFilter.FilterId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.AddNoiseSmartFilter.Distribution
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.AddNoiseSmartFilter.AmountNoise
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.AddNoiseSmartFilter.IsMonochromatic
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.AddNoiseSmartFilter.FilterType
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.GaussianBlurSmartFilter
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.GaussianBlurSmartFilter.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.GaussianBlurSmartFilter.Name
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.GaussianBlurSmartFilter.FilterId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.GaussianBlurSmartFilter.Radius
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.GaussianBlurSmartFilter.FilterType
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.NoiseDistribution
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.NoiseDistribution.Uniform
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.NoiseDistribution.Gaussian
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.SmartFilter
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.SmartFilter.Name
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.SmartFilter.FilterId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.SmartFilter.IsEnabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.SmartFilter.Opacity
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.SmartFilter.BlendMode
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.SmartFilter.Apply(Aspose.PSD.RasterImage)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.SmartFilter.ApplyToMask(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.SmartFilter.OnLoad
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.SmartFilter.Clone
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.SmartFilter.sourceDescriptor
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.UnknownSmartFilter
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.UnknownSmartFilter.Name
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.UnknownSmartFilter.FilterId
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.SmartFilters
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.SmartFilters.IsEnabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.SmartFilters.IsValidAtPosition
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.SmartFilters.IsMaskEnabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.SmartFilters.IsMaskLinked
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.SmartFilters.IsMaskExtendWithWhite
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.SmartFilters.Filters
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.SmartFilters.UpdateResourceValues
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource.#ctor(System.Int32,System.Int32,Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource.FilterEffectMasks
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource.Length
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource.FEidTypeToolKey
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource.FXidTypeToolKey
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData.#ctor(System.String,Aspose.PSD.Rectangle,System.Int32,System.Int32,Aspose.PSD.FileFormats.Psd.Layers.ChannelInformation[],Aspose.PSD.FileFormats.Psd.Layers.ChannelInformation,Aspose.PSD.Rectangle,Aspose.PSD.FileFormats.Psd.Layers.ChannelInformation)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData.GUID
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData.Rectangle
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData.PixelsDepth
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData.MaxChannels
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData.Channels
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData.UserMask
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData.MaskRectangle
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData.SheetMask
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData.SaveData(Aspose.PSD.StreamContainer)

# **Удаленные API:**
- Ни одного

## **Примеры использования:**

**PSDNET-128. Поддержка механизма умных фильтров**

{{< highlight csharp >}}
            string sourceFilte = "r2_SmartFilters.psd";
            string outputPsd = "out_r2_SmartFilters.psd";

            void AssertAreEqual(object expected, object actual)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new Exception("Объекты не равны.");
                }
            }

            using (var image = (PsdImage)Image.Load(sourceFilte))
            {
                SmartObjectLayer smartObj = (SmartObjectLayer)image.Layers[1];

                // edit smart filters
                GaussianBlurSmartFilter gaussianBlur = (GaussianBlurSmartFilter)smartObj.SmartFilters.Filters[0];

                // check filter values
                AssertAreEqual(3.1, gaussianBlur.Radius);
                AssertAreEqual(BlendMode.Dissolve, gaussianBlur.BlendMode);
                AssertAreEqual(90d, gaussianBlur.Opacity);
                AssertAreEqual(true, gaussianBlur.IsEnabled);

                // update filter values
                gaussianBlur.Radius = 1;
                gaussianBlur.BlendMode = BlendMode.Divide;
                gaussianBlur.Opacity = 75;
                gaussianBlur.IsEnabled = false;
                AddNoiseSmartFilter addNoise = (AddNoiseSmartFilter)smartObj.SmartFilters.Filters[1];
                addNoise.Distribution = NoiseDistribution.Uniform;

                // add new filter items
                var filters = new List<SmartFilter>(smartObj.SmartFilters.Filters);
                filters.Add(new GaussianBlurSmartFilter());
                filters.Add(new AddNoiseSmartFilter());
                smartObj.SmartFilters.Filters = filters.ToArray();

                // apply changes
                smartObj.SmartFilters.UpdateResourceValues();

                // Apply filters
                smartObj.SmartFilters.Filters[0].Apply(image.Layers[2]);
                smartObj.SmartFilters.Filters[4].ApplyToMask(image.Layers[2]);

                image.Save(outputPsd);
            }

            using (var image = (PsdImage)Image.Load(outputPsd))
            {
                SmartObjectLayer smartObj = (SmartObjectLayer)image.Layers[1];

                GaussianBlurSmartFilter gaussianBlur = (GaussianBlurSmartFilter)smartObj.SmartFilters.Filters[0];

                // check filter values
                AssertAreEqual(1d, gaussianBlur.Radius);
                AssertAreEqual(BlendMode.Divide, gaussianBlur.BlendMode);
                AssertAreEqual(75d, gaussianBlur.Opacity);
                AssertAreEqual(false, gaussianBlur.IsEnabled);

                AssertAreEqual(true, smartObj.SmartFilters.Filters[5] is GaussianBlurSmartFilter);
                AssertAreEqual(true, smartObj.SmartFilters.Filters[6] is AddNoiseSmartFilter);
            }
{{< /highlight >}}

**PSDNET-414. Поддержка Fxid/FEidResource**

{{< highlight csharp >}}
            string inputFilePath = "psdnet414_3.psd";
            string output = "out_psdnet414_3.psd";

            int resLength = 1144;
            int maskLength = 369;

            void AssertAreEqual(object expected, object actual, string message = null)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new FormatException(message ?? "Объекты не равны.");
                }
            }

            using (var psdImage = (PsdImage)Image.Load(inputFilePath))
            {
                FXidResource fXidResource = (FXidResource)psdImage.GlobalLayerResources[3];

                AssertAreEqual(resLength, fXidResource.Length);
                foreach (var maskData in fXidResource.FilterEffectMasks)
                {
                    AssertAreEqual(maskLength, maskData.Length);
                }

                psdImage.Save(output);
            }

            // check after saving
            using (var psdImage = (PsdImage)Image.Load(output))
            {
                FXidResource fXidResource = (FXidResource)psdImage.GlobalLayerResources[3];

                AssertAreEqual(resLength, fXidResource.Length);
                foreach (var maskData in fXidResource.FilterEffectMasks)
                {
                    AssertAreEqual(maskLength, maskData.Length);
                }
            }
{{< /highlight >}}

**PSDNET-556. Ошибка при загрузке структуры AliasStructure**

{{< highlight csharp >}}
            string srcFile = "Aspose.psd";
            string outputPsd = "out_Aspose.psd";
            string outputPng = "out_Aspose.png";

            void AssertAreEqual(object expected, object actual, string message = null)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new FormatException(message ?? "Объекты не равны.");
                }
            }

            using (var image = (PsdImage)Image.Load(srcFile))
            {
                LnkeResource lnkeResource = (LnkeResource)image.GlobalLayerResources[3];
                LiFeDataSource dataSource = (LiFeDataSource)lnkeResource[0];
                AssertAreEqual(2484L, dataSource.Length);

                foreach (var layer in image.Layers)
                {
                    if (layer is TextLayer)
                    {
                        TextLayer textLayer = layer as TextLayer;
                        textLayer.UpdateText("Test", Aspose.PSD.Color.Black);
                    }
                }

                image.Save(outputPsd);
                image.Save(outputPng, new PngOptions() { ColorType = PngColorType.GrayscaleWithAlpha });
            }
{{< /highlight >}}

**PSDNET-948. Изменение шрифта и цвета для текстового слоя PSD**

{{< highlight csharp >}}
            string sourceFileName = "fontExamples948.psd";
            string testFontsFoler = "Fonts";
            string outputPng = "output.png";

            FontSettings.SetFontsFolder(testFontsFoler);

            using (PsdImage image = (PsdImage)Aspose.PSD.Image.Load(sourceFileName))
            {
                foreach (var layer in image.Layers)
                {
                    var textLayer = layer as TextLayer;
                    if (textLayer != null)
                    {
                        ITextPortion textPortion = textLayer.TextData.Items[0];
                        textPortion.Style.FillColor = Color.BlueViolet;

                        textLayer.TextData.UpdateLayerData();
                    }
                }

                image.Save(outputPng, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-971. Добавление возможности создания пользовательского слоя с векторной маской**

{{< highlight csharp >}}
        public void CreatingVectorPathExample()
        {
            string fileName = "PathExample2.psd";

            string outputPsd = "out_CreatingVectorPathExampleTest.psd";
            string outputPng = "out_CreatingVectorPathExampleTest.png";

            using (var psdImage = (PsdImage)Image.Load(fileName))
            {
                VectorDataProvider.RemoveVectorPathDataFromLayer(psdImage.Layers[2]);

                // creating VectorPath object for existing layer without vector path data.
                VectorPath vectorPath = VectorDataProvider.CreateVectorPathForLayer(psdImage.Layers[1]);

                // Set the fill color of vector path
                vectorPath.FillColor = Color.MediumPurple;

                // add new shape
                PathShape newShape = new PathShape();
                newShape.Points.Add(new BezierKnot(new PointF(65, 175), true));
                newShape.Points.Add(new BezierKnot(new PointF(65, 210), true));
                newShape.Points.Add(new BezierKnot(new PointF(190, 210), true));
                newShape.Points.Add(new BezierKnot(new PointF(190, 175), true));
                vectorPath.Shapes.Add(newShape);

                // update path data in layer
                VectorDataProvider.UpdateLayerFromVectorPath(psdImage.Layers[1], vectorPath, true);


                // creating VectorPath object for new layer.
                FillLayer layer2 = FillLayer.CreateInstance(Aspose.PSD.FileFormats.Psd.Layers.FillSettings.FillType.Color);
                layer2.DisplayName = "Layer 2";
                psdImage.AddLayer(layer2);
                VectorPath vectorPath2 = VectorDataProvider.CreateVectorPathForLayer(layer2);

                // Set the fill color of vector path
                vectorPath2.FillColor = Color.IndianRed;

                // add new shape
                PathShape newShape2 = new PathShape();
                newShape2.Points.Add(new BezierKnot(new PointF(50, 150), true));
                newShape2.Points.Add(new BezierKnot(new PointF(100, 200), true));
                newShape2.Points.Add(new BezierKnot(new PointF(0, 200), true));
                vectorPath2.Shapes.Add(newShape2);

                // update path data in layer
                VectorDataProvider.UpdateLayerFromVectorPath(layer2, vectorPath2, true);

                psdImage.Save(outputPsd);
                psdImage.Save(outputPng, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
            }
        }
```csharp
    #region Редактор векторных путей (Здесь размещены классы для редактирования векторных путей).

    /// <summary>
    /// Класс, обеспечивающий работу между <see cref="Layer"/> и <see cref="VectorPath"/>.
    /// </summary>
    public static class VectorDataProvider
    {
        /// <summary>
        /// Создает экземпляр <see cref="VectorPath"/> на основе ресурсов из входного слоя.
        /// </summary>
        /// <param name="psdLayer">Слой PSD.</param>
        /// <returns>Экземпляр <see cref="VectorPath"/> на основе ресурсов из входного слоя.</returns>
        public static VectorPath CreateVectorPathForLayer(Layer psdLayer)
        {
            VectorPathDataResource pathResource = FindVectorPathDataResource(psdLayer, true);
            SoCoResource socoResource = FindSoCoResource(psdLayer, true);
            VectorPath vectorPath = new VectorPath(pathResource);
            if (socoResource != null)
            {
                vectorPath.FillColor = socoResource.Color;
            }

            return vectorPath;
        }

        // Другие методы и свойства опущены для краткости

        /// <summary>
        /// Удаляет данные маски из входного слоя.
        /// </summary>
        /// <param name="psdLayer">Слой PSD.</param>
        public static void RemoveVectorPathDataFromLayer(Layer psdLayer)
        {
            List<LayerResource> oldResources = new List<LayerResource>(psdLayer.Resources);
            List<LayerResource> newResources = new List<LayerResource>();
            for (int i = 0; i < oldResources.Count; i++)
            {
                LayerResource resource = oldResources[i];

                if (resource is VectorPathDataResource || resource is VogkResource || resource is SoCoResource)
                {
                    continue;
                }
                else
                {
                    newResources.Add(resource);
                }
            }

            psdLayer.Resources = newResources.ToArray();
        }

        /// <summary>
        /// Обновляет ресурсы слоя из экземпляра <see cref="VectorPath"/> или заменяет новым
        /// ресурсом и обновляет.
        /// </summary>
        /// <param name="psdLayer">Слой PSD.</param>
        /// <param name="vectorPath">Векторный путь.</param>
        /// <param name="createIfNotExist">Если ресурса не существует, то для <see cref="true"/> создает
        /// новый ресурс, в противном случае возвращает <see cref="null"/>.</param>
        public static void UpdateLayerFromVectorPath(Layer psdLayer, VectorPath vectorPath, bool createIfNotExist = false)
        {
            VectorPathDataResource pathResource = FindVectorPathDataResource(psdLayer, createIfNotExist);
            VogkResource vogkResource = FindVogkResource(psdLayer, createIfNotExist);
            SoCoResource socoResource = FindSoCoResource(psdLayer, createIfNotExist);

            UpdateResources(pathResource, vogkResource, socoResource, vectorPath);

            ReplaceVectorPathDataResourceInLayer(psdLayer, pathResource, vogkResource, socoResource);
        }

        // Другие методы и свойства опущены для краткости
    }

    // Другие классы опущены для краткости
```