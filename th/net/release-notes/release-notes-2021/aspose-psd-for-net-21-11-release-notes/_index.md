---
title: Aspose.PSD for .NET 21.11 - บันทึกการปล่อย
type: docs
weight: 20
url: /th/net/aspose-psd-for-net-21-11-release-notes/
---

{{% alert color="primary" %}} 

หน้านี้มีบันทึกการปล่อยสำหรับ [Aspose.PSD for .NET 21.11](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**คีย์**|**สรุป**|**หมวดหมู่**|
| :- | :- | :- |
|PSDNET-767|ข้อยกเว้นเมื่อเพิ่มเลเยอร์ข้อความที่มีอยู่ในกลุ่มเลเยอร์|ข้อบกพร่อง|
|PSDNET-988|IndexOutOfRangeException เมื่อทำการอัพเดทข้อความของ TextLayer|ข้อบกพร่อง|
|PSDNET-989|รูปทรงที่ส่งออกมีพิกัดที่ผิดในไฟล์ผลลัพธ์|ข้อบกพร่อง|
|PSDNET-1002|การส่งออกรูปร่างเวกเตอร์ไม่ถูกต้องในการส่งออกโฟลเดอร์|ข้อบกพร่อง|

## **การเปลี่ยนแปลง API สาธาณะ**
# **เพิ่ม API:**
- ไม่มี

# **API ที่ถูกนำออก:**
- ไม่มี

## **ตัวอย่างการใช้:**

**PSDNET-767. ข้อยกเว้นเมื่อเพิ่มเลเยอร์ข้อความที่มีอยู่ในกลุ่มเลเยอร์**

{{< highlight csharp >}}
            string outputPsd = "out_dummy_group.psd";

            var psdOptions = new PsdOptions()
            {
                Source = new StreamSource(new MemoryStream(), true),
                ColorMode = ColorModes.Rgb,
                ChannelsCount = 4,
                ChannelBitsCount = 8,
                CompressionMethod = CompressionMethod.RLE
            };
            using (PsdImage image = (PsdImage)Image.Create(psdOptions, 10, 15))
            {
                var group = image.AddLayerGroup("TestGroup", 0, true);
                var layer = image.AddTextLayer("Text", Rectangle.FromLeftTopRightBottom(-2, 3, 14, 17));
                group.AddLayer(layer);

                image.Save(outputPsd);
            }
{{< /highlight >}}

**PSDNET-988. IndexOutOfRangeException เมื่อทำการอัพเดทข้อความของ TextLayer**

{{< highlight csharp >}}
            string srcFile = "M1TTTT16062021001.psd";
            string fontsFolder = "Fonts";
            string outputPng = "out_M1TTTT16062021001.png";

            FontSettings.SetFontsFolder(fontsFolder);
            FontSettings.UpdateFonts();

            string[] words = new[] { "Mom", "Stacy" };
            string[] fonts = new[] { "Caveat", "Gochi Hand", "Lobster", "Satisfy" };

            using (var image = (PsdImage)Image.Load(srcFile))
            {
                foreach (var layer in image.Layers)
                {
                    var txtLayer = layer as TextLayer;
                    if (txtLayer != null)
                    {
                        for (int w = 0; w < words.Length; w++)
                        {
                            for (int f = 0; f < fonts.Length; f++)
                            {
                                txtLayer.UpdateText(words[w]);
                                foreach (var txtItem in txtLayer.TextData.Items)
                                {
                                    txtItem.Style.FontName = FontSettings.GetAdobeFontName(fonts[f]);
                                }

                                txtLayer.TextData.UpdateLayerData();
                            }
                        }
                    }
                }

                image.Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}

**PSDNET-989. รูปทรงที่ส่งออกมีพิกัดที่ผิดในไฟล์ผลลัพธ์**

{{< highlight csharp >}}
        public void CreatingVectorPathExample()
        {
            string outputPsd = "outputPsd.psd";

            using (var psdImage = (PsdImage)Image.Create(new PsdOptions() { Source = new Sources.StreamSource(new MemoryStream()), }, 500, 500))
            {
                FillLayer layer = FillLayer.CreateInstance(PSD.FileFormats.Psd.Layers.FillSettings.FillType.Color);
                psdImage.AddLayer(layer);

                VectorPath vectorPath = VectorDataProvider.CreateVectorPathForLayer(layer);
                vectorPath.FillColor = Color.IndianRed;
                PathShape shape = new PathShape();
                shape.Points.Add(new BezierKnot(new PointF(50, 150), true));
                shape.Points.Add(new BezierKnot(new PointF(100, 200), true));
                shape.Points.Add(new BezierKnot(new PointF(0, 200), true));
                vectorPath.Shapes.Add(shape);
                VectorDataProvider.UpdateLayerFromVectorPath(layer, vectorPath, true);

                psdImage.Save(outputPsd);
            }
        }

...

{{< /highlight >}}

**PSDNET-1002. การส่งออกรูปร่างเวกเตอร์ที่ไม่ถูกต้องในการส่งออกโฟลเดอร์**

{{< highlight csharp >}}
            string srcFile = "psdnet1002.psd";
            string outputPng = "output.png";

            using (var image = (PsdImage)Image.Load(srcFile))
            {
                image.Layers[4].Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}