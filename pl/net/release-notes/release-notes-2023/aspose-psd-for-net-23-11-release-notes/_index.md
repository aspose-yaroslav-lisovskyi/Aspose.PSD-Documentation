---
title: Aspose.PSD dla .NET 23.11 - Notatki dotyczące wydania
type: docs
weight: 20
url: /pl/net/aspose-psd-dla-net-23-11-notatki-dotyczace-wydania/
---

{{% alert color="primary" %}}

Ta strona zawiera notatki dotyczące wydania [Aspose.PSD dla .NET 23.11](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Klucz**    | **Podsumowanie**                                                                                          | **Kategoria** |
|:------------|:--------------------------------------------------------------------------------------------------------|:--------|
| PSDNET-412  | Obsługa LMskResource                                                                                    | Funkcja |
| PSDNET-1669 | [Format AI] Dodano możliwość renderowania pliku AI opartego na PDF przy użyciu Aspose.PSD               | Funkcja |
| PSDNET-1702 | [Format AI] Dodano obsługę operatora PostScript "cm"                                                     | Funkcja |
| PSDNET-1752 | Dodano nowe typy deformacji: Fala, muszla w górę, muszla w dół                                          | Funkcja |
| PSDNET-1797 | Dodano obsługę deformacji pionowej                                                                      | Funkcja |
| PSDNET-1756 | System.ArgumentNullException: 'Wartość nie może być pusta. (Parametr 'klucz')' podczas wywoływania TextLayer.GetFonts() | Błąd |


## **Zmiany w interfejsie publicznym**
# **Dodane interfejsy API:**
- M:Aspose.PSD.FontSettings.RemoveFontCacheFile
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.ColorSpace
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.ColorComponent1
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.ColorComponent2
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.ColorComponent3
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.ColorComponent4
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.Opacity
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.Flag
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.TypeToolKey
- T:Aspose.PSD.FileFormats.Psd.Resources.Enums.ColorSpace
- F:Aspose.PSD.FileFormats.Psd.Resources.Enums.ColorSpace.RGB
- F:Aspose.PSD.FileFormats.Psd.Resources.Enums.ColorSpace.HSB
- F:Aspose.PSD.FileFormats.Psd.Resources.Enums.ColorSpace.CMYK
- F:Aspose.PSD.FileFormats.Psd.Resources.Enums.ColorSpace.Lab
- F:Aspose.PSD.FileFormats.Psd.Resources.Enums.ColorSpace.GrayScale

# **Usunięte interfejsy API:**
- Brak


## **Przykłady użycia:**
**PSDNET-412. Obsługa LMskResource**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "sourceFile.psd");
string outputPsd = Path.Combine(outputFolder, "sourceFile_output.psd");

void AssertAreEqual(object expected, object actual)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception("Obiekty nie są równe.");
    }
}

// Wczytaj obraz o głębi 16 bitów.
using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    // Znajdź LmskResource.
    LmskResource lmskResource = new LmskResource();
    foreach (var res in image.GlobalLayerResources)
    {
        if (res is LmskResource)
        {
            lmskResource = (LmskResource)res;
            break;
        }
    }

    // Sprawdź właściwości LmskResource.
    AssertAreEqual(lmskResource.ColorSpace, PSD.FileFormats.Psd.Resources.Enums.ColorSpace.RGB);
    AssertAreEqual(lmskResource.ColorComponent1, (ushort)65535);
    AssertAreEqual(lmskResource.ColorComponent2, (ushort)0);
    AssertAreEqual(lmskResource.ColorComponent3, (ushort)0);
    AssertAreEqual(lmskResource.ColorComponent4, (ushort)0);
    AssertAreEqual(lmskResource.Opacity, (short)45);
    AssertAreEqual(lmskResource.Flag, (byte)128);

    // Zmień właściwości LmskResource.
    lmskResource.ColorSpace = PSD.FileFormats.Psd.Resources.Enums.ColorSpace.HSB;
    lmskResource.ColorComponent1 = 7854;
    lmskResource.ColorComponent2 = 10;
    lmskResource.ColorComponent3 = 15484;
    lmskResource.Opacity = 85;

    // Zapisz obraz.
    image.Save(outputPsd);
}
{{< /highlight >}}

**PSDNET-1669. [Format AI] Dodano możliwość renderowania pliku AI opartego na PDF przy użyciu Aspose.PSD**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "ai_one.ai");
string outputPng = Path.Combine(outputFolder, "ai_one_output.png");

// Wczytaj obraz AI oparty na PDF.
using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    // Zapisz obraz AI jako obraz PNG.
    image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1702. [Format AI] Dodano obsługę operatora "cm" PostScript**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "ai_two.ai");
string outputPng = Path.Combine(outputFolder, "ai_two_output.png");

// Wczytaj obraz AI.
using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    // Zapisz obraz AI jako obraz PNG.
    image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1752. Dodano nowe typy deformacji: Fala, muszla w górę, muszla w dół**

{{< highlight csharp >}}
var loadOptions = new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true };
var saveOptions = new PngOptions { ColorType = PngColorType.TruecolorWithAlpha };

string sourceFileFish = Path.Combine(baseFolder, "1752_warp_fish.psd");
string sourceFileRise = Path.Combine(baseFolder, "1752_warp_rise.psd");
string sourceFileWave = Path.Combine(baseFolder, "1752_warp_wave.psd");

string outputFileFish = Path.Combine(outputFolder, "1752_output_fish.png");
string outputFileRise = Path.Combine(outputFolder, "1752_output_rise.png");
string outputFileWave = Path.Combine(outputFolder, "1752_output_wave.png");

using (var psdImage = (PsdImage)Image.Load(sourceFileFish, loadOptions))
{
    psdImage.Save(outputFileFish, saveOptions);
}

using (var psdImage = (PsdImage)Image.Load(sourceFileRise, loadOptions))
{
    psdImage.Save(outputFileRise, saveOptions);
}

using (var psdImage = (PsdImage)Image.Load(sourceFileWave, loadOptions))
{
    psdImage.Save(outputFileWave, saveOptions);
}
{{< /highlight >}}

**PSDNET-1756. System.ArgumentNullException: 'Wartość nie może być pusta. (Parametr 'klucz')' podczas wywoływania TextLayer.GetFonts()**

{{< highlight csharp >}}
string src = Path.Combine(baseFolder, "SimpleText.psd");

FontSettings.RemoveFontCacheFile();

using (var psdImage = (PsdImage)Image.Load(src))
{
    foreach (var layer in psdImage.Layers)
    {
        if (layer is TextLayer textLayer)
        {
            textLayer.GetFonts();
        }
    }
}
{{< /highlight >}}

**PSDNET-1797. Dodano obsługę deformacji pionowej**

{{< highlight csharp >}}
var loadOptions = new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true };
var saveOptions = new PngOptions { ColorType = PngColorType.TruecolorWithAlpha };

string sourceFileArcLower = Path.Combine(baseFolder, "1797_warp_arc_lower_v.psd");
string sourceFileArcUpper = Path.Combine(baseFolder, "1797_warp_arc_upper_v.psd");
string sourceFileArch = Path.Combine(baseFolder, "1797_warp_arch_v.psd");
string sourceFileBulge = Path.Combine(baseFolder, "1797_warp_bulge_v.psd");
string sourceFileFlag = Path.Combine(baseFolder, "1797_warp_flag_v.psd");
string sourceFileFish = Path.Combine(baseFolder, "1797_warp_fish_v.psd");
string sourceFileRise = Path.Combine(baseFolder, "1797_warp_rise_v.psd");
string sourceFileWave = Path.Combine(baseFolder, "1797_warp_wave_v.psd");

string outputFileArcLower = Path.Combine(outputFolder, "1797_warp_arc_lower_v.png");
string outputFileArcUpper = Path.Combine(outputFolder, "1797_warp_arc_upper_v.png");
string outputFileArch = Path.Combine(outputFolder, "1797_warp_arch_v.png");
string outputFileBulge = Path.Combine(outputFolder, "1797_warp_bulge_v.png");
string outputFileFlag = Path.Combine(outputFolder, "1797_warp_flag_v.png");
string outputFileFish = Path.Combine(outputFolder, "1797_output_fish_v.png");
string outputFileRise = Path.Combine(outputFolder, "1797_output_rise_v.png");
string outputFileWave = Path.Combine(outputFolder, "1797_output_wave_v.png");

using (var psdImage = (PsdImage)Image.Load(sourceFileArcLower, loadOptions)) { psdImage.Save(outputFileArcLower, saveOptions); }
using (var psdImage = (PsdImage)Image.Load(sourceFileArcUpper, loadOptions)) { psdImage.Save(outputFileArcUpper, saveOptions); }
using (var psdImage = (PsdImage)Image.Load(sourceFileArch, loadOptions)) { psdImage.Save(outputFileArch, saveOptions); }
using (var psdImage = (PsdImage)Image.Load(sourceFileBulge, loadOptions)) { psdImage.Save(outputFileBulge, saveOptions); }
using (var psdImage = (PsdImage)Image.Load(sourceFileFlag, loadOptions)) { psdImage.Save(outputFileFlag, saveOptions); }
using (var psdImage = (PsdImage)Image.Load(sourceFileFish, loadOptions)) { psdImage.Save(outputFileFish, saveOptions); }
using (var psdImage = (PsdImage)Image.Load(sourceFileRise, loadOptions)) { psdImage.Save(outputFileRise, saveOptions); }
using (var psdImage = (PsdImage)Image.Load(sourceFileWave, loadOptions)) { psdImage.Save(outputFileWave, saveOptions); }
{{< /highlight >}}