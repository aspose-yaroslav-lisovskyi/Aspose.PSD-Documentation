---
title: Заметки к выпуску Aspose.PSD для .NET 21.9
type: docs
weight: 40
url: /ru/net/aspose-psd-for-net-21-9-release-notes/
---

{{% alert color="primary" %}} 

На этой странице содержатся заметки к выпуску для [Aspose.PSD для .NET 21.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Ключ**|**Описание**|**Категория**|
| :- | :- | :- |
|PSDNET-574|Сделать сжатие RLE по умолчанию для сохранения PSD, чтобы избежать огромного размера PSD|Функциональность|
|PSDNET-747|Поддержка эффектов наложения узора с режимом цвета мультканального в PSD-файле|Функциональность|
|PSDNET-951|После создания нового слоя его свойство Resources равно null, что мешает манипуляциям (например, изменение размера)|Ошибка|
|PSDNET-955|Неподдерживаемые методы сжатия ZipWithPrediction для 8 бит|Ошибка|

## **Изменения в общедоступном API**
# **Добавленные API:**
- Нет

# **Удаленные API:**
- Нет

## **Примеры использования:**

**PSDNET-574. Сделать сжатие RLE по умолчанию для сохранения PSD, чтобы избежать огромного размера PSD**

{{< highlight csharp >}}
            string inputFilePath = "file.psd";
            string output1 = "output_original.psd";
            string output2 = "output_psdOptions.psd";

            using (Image image = Image.Load(inputFilePath))
            {
                image.Save(output1);
                image.Save(output2, new PsdOptions());
            }
{{< /highlight >}}

**PSDNET-747. Поддержка эффектов наложения узора с режимом цвета мультканального в PSD-файле**

{{< highlight csharp >}}
            var fileName = "AllEffects.psd";
            var outputFile = "AllEffects_out.psd";
            var loadOptions = new PsdLoadOptions()
            {
                LoadEffectsResource = true
            };

            // Не должно быть выброшено исключение
            using (var im = Image.Load(fileName, loadOptions))
            {
                // Не должно быть выброшено исключение
                im.Save(outputFile);
            }
{{< /highlight >}}

**PSDNET-951. После создания нового слоя его свойство Resources равно null, что мешает манипуляциям (например, изменение размера)**

{{< highlight csharp >}}
            string PSDFile = "Layer1.psd";
            string layer1File = "Layer2.png";
            string layer2File = "Layer3.png";
            string outFileName = "finaloutput.psd";

            void ReplaceColor(RasterImage image, Color oldColor, int diff, Color newColor)
            {
                var pixels = image.LoadArgb32Pixels(image.Bounds);
                var length = pixels.Length;

                var oldR = oldColor.R;
                var oldG = oldColor.G;
                var oldB = oldColor.B;
                var newColorValue = newColor.ToArgb();

                for (int i = 0; i < length; i++)
                {
                    // Красный
                    var r = (byte)((pixels[i] >> 16) & 0xff);
                    // Зеленый
                    var g = (byte)((pixels[i] >> 8) & 0xff);
                    // Синий
                    var b = (byte)(pixels[i] & 0xff);

                    int actualDiff = Math.Abs(r - oldR) + Math.Abs(g - oldG) + Math.Abs(b - oldB);

                    if (actualDiff <= diff)
                    {
                        pixels[i] = newColorValue;
                    }
                }

                image.SaveArgb32Pixels(image.Bounds, pixels);
            }

            Layer Layer2 = null;
            Layer Layer3 = null;
            using (PsdImage image = (PsdImage)Image.Load(PSDFile))
            {
                #region Добавление слоя 1

                using (var stream = new FileStream(layer1File, FileMode.Open))
                {
                    Layer2 = new Layer(stream);

                    Layer2.Resize(image.Width, image.Height);
                    var width = Layer2.Width;
                    var height = Layer2.Height;

                    Layer2.Left = 675;
                    Layer2.Top = 0;

                    Layer2.Right = Layer2.Left + width;
                    Layer2.Bottom = Layer2.Top + height;

                    image.AddLayer(Layer2);
                }

                #endregion

                using (var stream = new FileStream(layer2File, FileMode.Open))
                {
                    Layer3 = new Layer(stream);
                    // Замена белого цвета на прозрачный
                    ReplaceColor(Layer3, Color.White, 256, Color.Transparent);
                    Layer2.DrawImage(new Point(0, 0), Layer3);
                }

                image.Save(outFileName, new PsdOptions());
            }
{{< /highlight >}}

**PSDNET-955. Неподдерживаемые методы сжатия ZipWithPrediction для 8 бит**

{{< highlight csharp >}}
            string inputFilePath = "zipTest698.psd";
            string outputZip8 = "out_Zip8bit.psd";
            string outputZip16 = "out_Zip16bit.psd";

            using (PsdImage image = (PsdImage)Image.Load(inputFilePath))
            {
                image.Save(outputZip8, new PsdOptions() { CompressionMethod = CompressionMethod.ZipWithPrediction, ChannelBitsCount = 8 });
                image.Save(outputZip16, new PsdOptions() { CompressionMethod = CompressionMethod.ZipWithPrediction, ChannelBitsCount = 16 });
            }
{{< /highlight >}}