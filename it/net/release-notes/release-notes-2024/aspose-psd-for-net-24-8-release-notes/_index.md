---
title: Note sulla versione di Aspose.PSD per .NET 24.8
type: docs
weight: 50
url: /it/net/aspose-psd-per-net-24-8-note-sulla-versione/
---

{{% alert color="primary" %}}

Questa pagina contiene le note sulla versione di [Aspose.PSD per .NET 24.8](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Chiave**  | **Sommario**                                                                                       | **Categoria** |
|:------------|:---------------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2091 | [Formato AI] Aggiunta gestione per Gruppi XObject                                                   | Miglioramento |
| PSDNET-1754 | Migliorare le capacità di trasformazione Warp aggiungendo WarpSettings per TextLayer e SmartObjectLayer | Novità       |
| PSDNET-1836 | [Formato AI] Gestire i livelli negli operatori di flussi di contenuto                               | Novità       |
| PSDNET-2015 | Il risultato del rendering del file AI è molto diverso rispetto ai risultati di Illustrator       | Errore       |
| PSDNET-2093 | Ricollegare Smart Object non si applica a tutti gli Smart Object nel file PSD                    | Errore       |

## **Cambiamenti nell'API pubblica**
# **API Aggiunte:**

- P:Aspose.PSD.FileFormats.Psd.Layers.TextLayer.WarpSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.WarpSettings
- T:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings
- M:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.#ctor(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.OSTypeStructure[],Aspose.PSD.Rectangle)
- M:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.#ctor(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource)
- P:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.Style
- P:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.Rotate
- P:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.Value
- P:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.Bounds
- P:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.MeshPoints
- T:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpRotates
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpRotates.Horizontal
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpRotates.Vertical
- T:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.None
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Custom
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Arc
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.ArcUpper
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.ArcLower
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Arch
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Bulge
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Flag
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Fish
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Rise
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Wave
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Twist
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Squeeze
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Inflate

# **API Rimosse:**
- Nessuna

## **Esempi d'uso:**

**PSDNET-1754. Migliorare le capacità di trasformazione Warp aggiungendo WarpSettings per TextLayer e SmartObjectLayer**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "smart_without_warp.psd");

var opt = new PsdLoadOptions()
{
    LoadEffectsResource = true,
    AllowWarpRepaint = true
};

string[] outputImageFile = new string[4];
string[] outputPsdFile = new string[4];

for (int caseIndex = 0; caseIndex < outputImageFile.Length; caseIndex++)
{
    outputImageFile[caseIndex] = Path.Combine(outputFolder, "export_" + caseIndex + ".png");
    outputPsdFile[caseIndex] = Path.Combine(outputFolder, "export_" + caseIndex + ".psd");

    using (PsdImage img = (PsdImage)Image.Load(sourceFile, opt))
    {
        foreach (Layer layer in img.Layers)
        {
            if (layer is SmartObjectLayer)
            {
                var smartLayer = (SmartObjectLayer)layer;
                smartLayer.WarpSettings = GetWarpSettingsByIndex(smartLayer.WarpSettings, caseIndex);
            }

            if (layer is TextLayer)
            {
                var textLayer = (TextLayer)layer;

                if (caseIndex != 3)
                {
                    textLayer.WarpSettings = GetWarpSettingsByIndex(textLayer.WarpSettings, caseIndex);
                }
            }
        }

        img.Save(outputPsdFile[caseIndex], new PsdOptions());
    }

    using (PsdImage img = (PsdImage)Image.Load(outputPsdFile[caseIndex], opt))
    {
        img.Save(outputImageFile[caseIndex],
            new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
    }
}

WarpSettings GetWarpSettingsByIndex(WarpSettings warpParams, int caseIndex)
{
    switch (caseIndex)
    {
        case 0:
            warpParams.Style = WarpStyles.Rise;
            warpParams.Rotate = WarpRotates.Horizontal;
            warpParams.Value = 20;
            break;
        case 1:
            warpParams.Style = WarpStyles.Rise;
            warpParams.Rotate = WarpRotates.Vertical;
            warpParams.Value = 10;
            break;
        case 2:
            warpParams.Style = WarpStyles.Flag;
            warpParams.Rotate = WarpRotates.Horizontal;
            warpParams.Value = 30;
            break;
        case 3:
            warpParams.Style = WarpStyles.Custom;
            warpParams.MeshPoints[2].Y += 70;
            break;
    }

    return warpParams;
}
{{< /highlight >}}

**PSDNET-1836. [Formato AI] Gestire i livelli negli operatori di flussi di contenuto**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "Layers-NoPen.ai");
string outputFile = Path.Combine(outputFolder, "Layers-NoPen.output.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFile, new PngOptions());
}

//// Le curve dal livello denominato "Pen" dovrebbero essere nascoste
{{< /highlight >}}

**PSDNET-2015. Il risultato del rendering del file AI è molto diverso rispetto ai risultati di Illustrator**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "4.ai");
string outputFilePath = Path.Combine(outputFolder, "4.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFilePath, new PngOptions());
}
{{< /highlight >}}

**PSDNET-2093. Il ricollegamento di Smart Object non si applica a tutti gli Smart Object nel file PSD**

{{< highlight csharp >}}
string[] files = { "simple_test", "w22" };
string changeFile = Path.Combine(baseFolder, "image(19).png");

string[] sourceFile = new string[files.Length];
string[] outputFiles = new string[files.Length];

for (int i = 0; i < files.Length; i++)
{
    sourceFile[i] = Path.Combine(baseFolder, files[i] + ".psd");
    outputFiles[i] = Path.Combine(outputFolder, files[i] + "_output.psd");

    using (var image = (PsdImage)Image.Load(sourceFile[i]))
    {
        foreach (Layer layer in image.Layers)
        {
            if (layer is SmartObjectLayer)
            {
                SmartObjectLayer smart = (SmartObjectLayer)layer;

                // Per il secondo smart layer qui c'era un errore
                smart.ReplaceContents(changeFile);
            }
        }

        image.Save(outputFiles[i]);
    }
}
{{< /highlight >}}