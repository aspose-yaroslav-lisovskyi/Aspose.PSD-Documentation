---
title: Aspose.PSD pro Java 24.2 - poznámky k vydání
type: docs
weight: 40
url: /cs/aspose-psd-pro-java-24-2-poznamky-k-vydani/
---

{{% alert color="primary" %}} Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD pro Java 24.2](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.2/) {{% /alert %}}

| **Klíč**    | **Shrnutí**                                                                 | **Kategorie** |
|:-----------|:---------------------------------------------------------------------------|:--------------|
| PSDJAVA-584 | Zacházení s vlastností úhlu pro nastavení výplně vzoru.                     | Funkce       |
| PSDJAVA-585 | Podpora vertikálního a horizontálního měřítka pro TextLayer.                | Funkce       |
| PSDJAVA-589 | [AI Formát] Implementace správného vykreslování pozadí v AI formátu založeném na PDF. | Funkce       |
| PSDJAVA-590 | Změna mechanismu deformace v deformaci.                                    | Vylepšení     |
| PSDJAVA-591 | Zrychlení deformaci.                                                      | Vylepšení     |
| PSDJAVA-592 | Výjimka "Načítání obrázku selhalo." při otevírání dokumentu.                | Chyba        |
| PSDJAVA-593 | Oprava ukládání souborů PSD s vzorem tahů.                                 | Chyba        |
| PSDJAVA-594 | Styl textu je nesprávný v chytrém objektu při použití ReplaceContents.     | Chyba        |
| PSDJAVA-595 | [AI Formát] Oprava vykreslování kubické Bezierovy křivky v souboru AI.      | Chyba        |

## **Změny ve veřejném API**
# **Přidaná API:**

- M:com.aspose.psd.fileformats.ai.AiImage.getActivePageIndex
- M:com.aspose.psd.fileformats.ai.AiImage.setActivePageIndex(int)
- T:com.aspose.psd.fileformats.psd.layers.FillLayer 
- M:com.aspose.psd.fileformats.psd.layers.FillLayer.createInstance(int)
- M:com.aspose.psd.fileformats.psd.layers.FillLayer.getFillSettings 
- M:com.aspose.psd.fileformats.psd.layers.FillLayer.getFillType 
- M:com.aspose.psd.fileformats.psd.layers.FillLayer.replaceNonTransparentColors(int)
- M:com.aspose.psd.fileformats.psd.layers.FillLayer.setFillSettings(com.aspose.psd.fileformats.psd.layers.fillsettings.IFillSettings)
- M:com.aspose.psd.fileformats.psd.layers.FillLayer.update
- M:com.aspose.psd.fileformats.psd.layers.layerresources.PtFlResource.getAngle
- M:com.aspose.psd.fileformats.psd.layers.layerresources.PtFlResource.setAngle(double)

# **Odebraná API:**

- T:com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer 
- M:com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer.createInstance(int)
- M:com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer.getFillSettings 
- M:com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer.getFillType 
- M:com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer.replaceNonTransparentColors(int)
- M:com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer.setFillSettings(com.aspose.psd.fileformats.psd.layers.fillsettings.IFillSettings)
- M:com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer.update

## **Příklady použití:**

**PSDJAVA-584. Zacházení s vlastností úhlu pro nastavení výplně vzoru**

{{< highlight java >}}

    public static void main(String[] args) {
        String sourceFile = "src/main/resources/PatternFillLayerWide_0.psd";
        String outputFile = "src/main/resources/PatternFillLayerWide_0_output.psd";

        PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
        psdLoadOptions.setLoadEffectsResource(true);

        try (PsdImage image = (PsdImage) Image.load(sourceFile, psdLoadOptions)) {
            FillLayer fillLayer = (FillLayer) image.getLayers()[1];
            PatternFillSettings fillSettings = (PatternFillSettings) fillLayer.getFillSettings();
            fillSettings.setAngle(70.0);
            fillLayer.update();
            image.save(outputFile, new PsdOptions());
        }

        try (PsdImage image = (PsdImage) Image.load(outputFile, psdLoadOptions)) {
            FillLayer fillLayer = (FillLayer) image.getLayers()[1];
            PatternFillSettings fillSettings = (PatternFillSettings) fillLayer.getFillSettings();

            assertAreEqual(70.0, fillSettings.getAngle());
        }
    }

    static void assertAreEqual(Object expected, Object actual) {
        assertAreEqual(expected, actual, "Objekty nejsou stejné.");
    }

    static void assertAreEqual(Object expected, Object actual, String message) {
        if (!expected.equals(actual)) {
            throw new IllegalArgumentException(message);
        }
    }

{{< /highlight >}}

**PSDJAVA-585. Podpora vertikálního a horizontálního měřítka pro TextLayer**

{{< highlight java >}}

        String src = "src/main/resources/1719_src.psd";
        String output = "src/main/resources/out_1719.png";

        try (PsdImage psdImage = (PsdImage) Image.load(src)) {
            psdImage.save(output, new PngOptions());
        }

{{< /highlight >}}

**PSDJAVA-589. [AI Formát] Implementace správného vykreslování pozadí v AI formátu založeném na PDF**

{{< highlight java >}}

        String sourceFile = "src/main/resources/pineapples.ai";
        String outputFilePath = "src/main/resources/pineapples.png";

        try (AiImage image = (AiImage) Image.load(sourceFile)) {
            image.save(outputFilePath, new PngOptions());
        }

{{< /highlight >}}

**PSDJAVA-590. Změna mechanismu deformace v deformaci**

{{< highlight java >}}

        String sourceFile = "src/main/resources/crow_grid.psd";
        String outputFile = "src/main/resources/export.png";

        PsdLoadOptions opt = new PsdLoadOptions();
        opt.setLoadEffectsResource(true);
        opt.setAllowWarpRepaint(true);

        try (PsdImage img = (PsdImage) Image.load(sourceFile, opt)) {
            PngOptions pngOptions = new PngOptions();
            pngOptions.setCompressionLevel(9);
            pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

            img.save(outputFile, pngOptions);
        }

{{< /highlight >}}

**PSDJAVA-591. Zrychlení deformací**

{{< highlight java >}}

        String sourceFile = "src/main/resources/output.psd";
        String outputFile = "src/main/resources/export.png";

        PsdLoadOptions opt = new PsdLoadOptions();
        opt.setLoadEffectsResource(true);
        opt.setAllowWarpRepaint(true);

        long startTime = System.currentTimeMillis();

        try (PsdImage img = (PsdImage) Image.load(sourceFile, opt)) {
            PngOptions pngOptions = new PngOptions();
            pngOptions.setCompressionLevel(9);
            pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

            img.save(outputFile, pngOptions);
        }

        long endTime = System.currentTimeMillis();
        int timeInSec = (int) (endTime - startTime);

        if (timeInSec > 100000) {
            throw new RuntimeException("Čas zpracování je příliš dlouhý");
        }

{{< /highlight >}}

**PSDJAVA-592. Výjimka "Načítání obrázku selhalo." při otevírání dokumentu**

{{< highlight java >}}

        String sourceFile1 = "src/main/resources/PRODUCT.ai";
        String outputFile1 = "src/main/resources/PRODUCT.png";

        try (AiImage image = (AiImage) Image.load(sourceFile1)) {
            image.save(outputFile1, new PngOptions());
        }

        String sourceFile2 = "src/main/resources/Dolota.ai";
        String outputFile2 = "src/main/resources/Dolota.png";

        try (AiImage image = (AiImage) Image.load(sourceFile2)) {
            image.save(outputFile2, new PngOptions());
        }

        String sourceFile3 = "src/main/resources/ARS_novelty_2108_out_01(1).ai";
        String outputFile3 = "src/main/resources/ARS_novelty_2108_out_01(1).png";

        try (AiImage image = (AiImage) Image.load(sourceFile3)) {
            image.save(outputFile3, new PngOptions());
        }

        String sourceFile4 = "src/main/resources/bit_gear.ai";
        String outputFile4 = "src/main/resources/bit_gear.png";

        try (AiImage image = (AiImage) Image.load(sourceFile4)) {
            image.save(outputFile4, new PngOptions());
        }

        String sourceFile5 = "src/main/resources/test.ai";
        String outputFile5 = "src/main/resources/test.png";

        try (AiImage image = (AiImage) Image.load(sourceFile5)) {
            image.save(outputFile5, new PngOptions());
        }

{{< /highlight >}}

**PSDJAVA-593. Oprava ukládání souborů PSD s vzorem tahů**

{{< highlight java >}}

    public static void main(String[] args) {
        String sourceFile = "src/main/resources/StrokeShapePattern.psd";
        String outputFile = "src/main/resources/StrokeShapePattern_output.psd";

        Rectangle newPatternBounds = new Rectangle(0, 0, 4, 4);
        UUID guid = UUID.randomUUID();
        String newPatternName = "$$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0";
        int[] newPattern = new int[]
                {
                        Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
                        Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
                        Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
                        Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
                };

        try (PsdImage image = (PsdImage) Image.load(sourceFile)) {
            ShapeLayer shapeLayer = (ShapeLayer) image.getLayers()[1];
            PatternFillSettings strokeInternalFillSettings = (PatternFillSettings) shapeLayer.getFill();

            PattResource pattResource;
            for (LayerResource globalLayerResource : image.getGlobalLayerResources()) {
                if (globalLayerResource instanceof PattResource) {
                    pattResource = (PattResource) globalLayerResource;
                    PattResourceData patternItem = pattResource.getPatterns()[0]; // Údaje o vnitřním vzoru tahů

                    patternItem.setPatternId(guid.toString());
                    patternItem.setName(newPatternName);
                    patternItem.setPattern(newPattern, newPatternBounds);

                    break;
                }
            }

            strokeInternalFillSettings.setPatternName(newPatternName);
            strokeInternalFillSettings.setPatternId(guid.toString() + "\0");

            shapeLayer.update();

            image.save(outputFile);
        }

        // Ověření změněných dat.
        try (PsdImage image = (PsdImage) Image.load(outputFile)) {
            ShapeLayer shapeLayer = (ShapeLayer) image.getLayers()[1];
            PatternFillSettings strokeInternalFillSettings = (PatternFillSettings) shapeLayer.getFill();

            assertAreEqual(guid.toString().toUpperCase(), strokeInternalFillSettings.getPatternId());
            assertAreEqual(newPatternName, strokeInternalFillSettings.getPatternName() + "\0");
        }
    }

    static void assertAreEqual(Object expected, Object actual) {
        assertAreEqual(expected, actual, "Objekty nejsou stejné.");
    }

    static void assertAreEqual(Object expected, Object actual, String message) {
        if (!expected.equals(actual)) {
            throw new IllegalArgumentException(message);
        }
    }

{{< /highlight >}}

**PSDJAVA-594. Styl textu je nesprávný v chytrém objektu při použití ReplaceContents**

{{< highlight java >}}

        String inputFile = "src/main/resources/source.psd";
        String output2 = "src/main/resources/output.png";

        PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
        psdLoadOptions.setLoadEffectsResource(true);

        try (PsdImage psdImage = (PsdImage) Image.load(inputFile, psdLoadOptions)) {
            SmartObjectLayer smartObject = (SmartObjectLayer) psdImage.getLayers()[1];

            try (PsdImage smartObjectImage = (PsdImage) smartObject.loadContents(psdLoadOptions)) {
                smartObject.replaceContents(smartObjectImage);
            }

            PngOptions pngOptions = new PngOptions();
            pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

            psdImage.save(output2, pngOptions);
        }

{{< /highlight >}}

**PSDJAVA-595. [AI Formát] Oprava vykreslování kubické Bezierovy křivky v souboru AI**

{{< highlight java >}}

        String sourceFile = "src/main/resources/Typography.ai";
        String outputFilePath = "src/main/resources/Typography.png";

        try (AiImage image = (AiImage) Image.load(sourceFile)) {
            image.save(outputFilePath, new PngOptions());
        }

{{< /highlight >}}