---
title: כתבות השחרור של Aspose.PSD עבור Python via .NET 23.12
type: docs
weight: 10
url: /he/net/aspose-psd-for-python-via-net-23-12-release-notes/
---

{{% alert color="primary" %}}

דף זה מכיל את כתבות השחרור של [Aspose.PSD עבור Python via .NET 23.12](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **מפתח**   | **סיכום**                                                                                              | **קטגוריה** |
|:------------|:-------------------------------------------------------------------------------------------------------|:------------|
|  PSDPYTHON-7 | [פורמט AI] הוספת תמיכה בעיבוד תמונת Raster בגרסה חדשה של AI                                       | תכונה       |
|  PSDPYTHON-8 | טיפול בסוג הרעש Gradient ב-GdflResrource                                                           | תכונה       |
|  PSDPYTHON-9 | שגיאה "הפנית עצם לא הוגדרה למופע של אובייקט." בשמירת שכבת טקסט לאחר עדכון                       | באג          |
|  PSDPYTHON-10 | תיקון הטעינה הידנית של גופנים ב-MacOS באמצעות System.Drawing.Common ו-Aspose.Drawing.             | באג          |
|  PSDPYTHON-11 | AllowWarpRepaint באפשרויות ה-PsdLoad מוביל לחריגה                                                  | באג          |
|  PSDPYTHON-12 | [פורמט AI] הטמעת עיבוד של זרמי הפניה צפותיים                                                | שיפור        |
|  PSDPYTHON-13 | שליטת רישיון עבור משאב VectorPathData פועלת באופן שגוי                                        | שיפור        |


## **שינויים ב-API הציבורי**
# **APIs שנוספו:**
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.#ctor(System.IO.Stream)
- F:Aspose.PSD.FileFormats.Ai.AiFormatVersion.Pdf17
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.RndNumberSeed
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ShowTransparency
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.UseVectorColor
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.Roughness
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ColorModel
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.MinimumColor
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.MaximumColor
- T:Aspose.PSD.FileFormats.Psd.Layers.Gradient.NoiseColorModel
- F:Aspose.PSD.FileFormats.Psd.Layers.Gradient.NoiseColorModel.RGB
- F:Aspose.PSD.FileFormats.Psd.Layers.Gradient.NoiseColorModel.HSB
- F:Aspose.PSD.FileFormats.Psd.Layers.Gradient.NoiseColorModel.LAB
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.GradientMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.RndNumberSeed
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.ShowTransparency
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.UseVectorColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.Roughness
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.ColorModel
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.MinimumColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.MaximumColor
- T:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.GradientType
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.GradientName
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.FillType
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.Color
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.AlignWithLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.Dither
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.Reverse
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.Angle
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.HorizontalOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.VerticalOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.ColorPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.TransparencyPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.Scale
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.GradientMode
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.Interpolation
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientFillSettings.GradientMode
- T:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.#ctor
- T:Aspose.PSD.CustomFontHandler.CustomFontData
- M:Aspose.PSD.Metered.GetProductName
- M:Aspose.PSD.Metered.IsMeteredLicensed
- T:Aspose.PSD.PluginLicenseException
- M:Aspose.PSD.PluginLicenseException.#ctor
- M:Aspose.PSD.Metered.Equals(System.Object)

# **APIs שהוסרו:**
- M:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.ContainsKey(System.String)
- M:Aspose.PSD.Metered.Equals(System.Object)


## **דוגמאות לשימוש:**

**PSDPYTHON-7. [פורמט AI] הוספת תמיכה בעיבוד תמונת Raster בגרסה חדשה של AI**

{{< highlight python >}}
        sourceFile = "raster.ai"
        outputFile = "raster_output.png"

        with Image.load(sourceFile) as image:
            image.save(outputFile, PngOptions())mage.Save(outputFile, new PngOptions());

{{< /highlight >}}

**PSDPYTHON-8. טיפול בסוג הרעש Gradient ב-GdflResrource**

{{< highlight python >}}
        # דוגמה לעבודה עם משאב GdFlResource באמצעות API בסיסי   
        sourceFile = "Gradient-Fill.psd"
        destFile = "Gradient-Fill-out.psd"

        with Image.load(sourceFile, PsdLoadOptions()) as image:
            psdImage = cast(PsdImage, image)
            layer = psdImage.layers[1]

            for res in layer.resources:
                resource = as_of(res, GdFlResource)
                if (resource != None):
                    resource.scale = 90
                    resource.angle = 30
                    resource.dither = False
                    resource.align_with_layer = True
                    resource.reverse = False

                    break

            psdImage.save(destFile, PsdOptions())
		
		# דוגמה לטיפול בגרדיאנט סולידי
		sourceFile = "ComplexGradientFillLayer.psd"
        outputFile =  "ComplexGradientFillLayer_output.psd"

        with Image.load(sourceFile) as image:
            im = cast(PsdImage, image)
            for layer in im.layers:
                if is_assignable(layer, FillLayer):
                    fillLayer = as_of(layer, FillLayer)
                    gradientFillSettings = fillLayer.fill_settings

                    # קריאה
                    assert gradientFillSettings.align_with_layer == False
                    assert abs(gradientFillSettings.angle - 45.0) < 0.001

                    assert gradientFillSettings.dither == True
                    assert gradientFillSettings.reverse == False
                    assert gradientFillSettings.color == Color.empty
                    assert gradientFillSettings.horizontal_offset == -39
                    assert gradientFillSettings.vertical_offset == -5

                    assert len(gradientFillSettings.transparency_points) == 3
                    assert len(gradientFillSettings.color_points) == 2

                    point = gradientFillSettings.transparency_points[0]
                    assert abs(100.0 - point.opacity) < 0.25
                    assert point.location == 0
                    assert point.median_point_location == 50

                    point = gradientFillSettings.transparency_points[1]
                    assert abs(50.0 - point.opacity) < 0.25
                    assert point.location == 2048
                    assert point.median_point_location == 50

                    point = gradientFillSettings.transparency_points[2]
                    assert abs(100.0 - point.opacity) < 0.25
                    assert point.location == 4096
                    assert point.median_point_location == 50

                    color_point = gradientFillSettings.color_points[0]
                    assert color_point.color == Color.from_argb(203, 64, 140)
                    assert color_point.location == 0
                    assert color_point.median_point_location == 50

                    color_point = gradientFillSettings.color_points[1]
                    assert color_point.color == Color.from_argb(203, 0, 0)
                    assert color_point.location == 4096
                    assert color_point.median_point_location == 50

                    # עריכה
                    gradientFillSettings.angle = 30.0
                    gradientFillSettings.dither = False
                    gradientFillSettings.align_with_layer = True
                    gradientFillSettings.reverse = True
                    gradientFillSettings.horizontal_offset = 25
                    gradientFillSettings.vertical_offset = -15

                    color_points = list(gradientFillSettings.color_points)
                    transparency_points = list(gradientFillSettings.transparency_points)

                    gradPoint1 = GradientColorPoint()
                    gradPoint1.color = Color.violet
                    gradPoint1.location = 4096
                    gradPoint1.median_point_location = 75
                    color_points.append(gradPoint1)

                    color_points[1].location = 3000

                    gradPoint2 = GradientTransparencyPoint()
                    gradPoint2.opacity = 80.0
                    gradPoint2.location = 4096
                    gradPoint2.median_point_location = 25
                    transparency_points.append(gradPoint2)

                    transparency_points[2].location = 3000

                    gradientFillSettings.color_points = color_points
                    gradientFillSettings.transparency_points = transparency_points

                    im.save(outputFile)

        with Image.load(outputFile) as image:
            im = cast(PsdImage, image)
            for layer in im.layers:
                if isinstance(layer, FillLayer):
                    fillLayer = layer
                    gradientFillSettings = fillLayer.fill_settings

                    assert abs(gradientFillSettings.angle - 30) < 0.001
                    assert gradientFillSettings.align_with_layer == True
                    assert gradientFillSettings.dither == False
                    assert gradientFillSettings.reverse == True
                    assert gradientFillSettings.horizontal_offset == 25
                    assert gradientFillSettings.vertical_offset == -15

                    assert len(gradientFillSettings.transparency_points) == 4
                    assert len(gradientFillSettings.color_points) == 3

                    point = gradientFillSettings.transparency_points[0]
                    assert abs(100.0 - point.opacity) < 0.25
                    assert point.location == 0
                    assert point.median_point_location == 50

                    point = gradientFillSettings.transparency_points[1]
                    assert abs(50.196 - point.opacity) < 0.25
                    assert point.location == 2048
                    assert point.median_point_location == 50

                    point = gradientFillSettings.transparency_points[2]
                    assert abs(100.0 - point.opacity) < 0.25
                    assert point.location == 3000
                    assert point.median_point_location == 50

                    point = gradientFillSettings.transparency_points[3]
                    assert abs(80 - point.opacity) < 0.25
                    assert point.location == 4096
                    assert point.median_point_location == 25

                    color_point = gradientFillSettings.color_points[0]
                    assert color_point.color == Color.FromArgb(203, 64, 140)
                    assert color_point.location == 0
                    assert color_point.median_point_location == 50

                    color_point = gradientFillSettings.color_points[1]
                    assert color_point.color == Color.FromArgb(203, 0, 0)
                    assert color_point.location == 3000
                    assert color_point.median_point_location == 50

                    color_point = gradientFillSettings.color_points[2]
                    assert color_point.color == Color.FromArgb(238, 130, 238)
                    assert color_point.location == 4096
                    assert color_point.median_point_location == 75

                    # עריכה
                    gradientFillSettings.angle = 30.0
                    gradientFillSettings.dither = False
                    gradientFillSettings.align_with_layer = True
                    gradientFillSettings.reverse = False
                    gradientFillSettings.scale = 60
                    gradientFillSettings.show_transparency = False
                    gradientFillSettings.use_vector_color = False
                    gradientFillSettings.color_model = NoiseColorModel.HSB
                    gradientFillSettings.roughness = 4096
                    gradientFillSettings.rnd_number_seed = 12345678

                    gradientFillSettings.minimum_color.components[1].value = 0
                    gradientFillSettings.minimum_color.components[2].value = 0
                    gradientFillSettings.minimum_color.components[3].value = 0
                    gradientFillSettings.minimum_color.components[0].value = 0

                    gradientFillSettings.maximum_color.components[1].value = 255
                    gradientFillSettings.maximum_color.components[2].value = 255
                    gradientFillSettings.maximum_color.components[3].value = 255
                    gradientFillSettings.maximum_color.components[0].value = 255

                    im.save(outputFile)

        with Image.load(outputFile) as image:
            im = cast(PsdImage, image)
            for layer in im.layers:
                if is_assignable(layer, FillLayer):
                    fillLayer = as_of(layer, FillLayer)
                    gradientFillSettings = fillLayer.fill_settings

                    assert gradientFillSettings.align_with_layer == True
                    assert abs(gradientFillSettings.angle - 30.0) < 0.001
                    assert gradientFillSettings.dither == False
                    assert gradientFillSettings.reverse == False
                    assert gradientFillSettings.scale == 60

                    assert gradientFillSettings.show_transparency == False
                    assert gradientFillSettings.use_vector_color == False
                    assert gradientFillSettings.color_model == NoiseColorModel.HSB
                    assert gradientFillSettings.rnd_number_seed == 12345678
                    assert gradientFillSettings.roughness == 4096

                    assert gradientFillSettings.minimum_color.components[1].value == 0
                    assert gradientFillSettings.minimum_color.components[2].value == 0
                    assert gradientFillSettings.minimum_color.components[3].value == 0
                    assert gradientFillSettings.minimum_color.components[0].value == 0

                    assert gradientFillSettings.maximum_color.components[1].value == 255
                    assert gradientFillSettings.maximum_color.components[2].value == 255
                    assert gradientFillSettings.maximum_color.components[3].value == 255
                    assert gradientFillSettings.maximum_color.components[0].value == 255
		
{{< /highlight >}}

**PSDPYTHON-9. שגיאה "הפנית עצם לא הוגדרה למופע של אובייקט." בשמירת שכבת טקסט לאחר עדכון**

{{< highlight python >}}
        sourceFile = "input_1827.psd"
        outputFile = "out_1827.psd"

        with Image.load(sourceFile) as image:
            psdImage = cast(PsdImage, image)
            for layer in psdImage.layers:
                if (is_assignable(layer, TextLayer)):
                    textLayer = cast(TextLayer, layer)
                    textLayer.text_data.update_layer_data()

            # לא צריך להיות שם שגיאה
            psdImage.save(outputFile)
{{< /highlight >}}

**PSDPYTHON-11. AllowWarpRepaint באפשרויות ה-PsdLoad מוביל לחריגה**

{{< highlight python >}}
            string sourceFile = @"SizeChart-4 Colors.psd";
            string outputFile