---
title: Aspose.PSD pour Java 23.9 - Notes de publication
type: docs
weight: 40
url: /fr/java/aspose-psd-pour-java-23-9-notes-de-publication/
---

{{% alert color="primary" %}} Cette page contient les notes de publication pour [Aspose.PSD pour Java 23.9](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.9/) {{% /alert %}}

| **Clé**     | **Résumé**                                                                                                                                      | **Catégorie** |
|:------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-527 | Implémenter la création d'un masque pour de nouvelles couches d'ajustement                                                                         |   Fonctionnalité   |
| PSDJAVA-528 | Ajouter la prise en charge des couches fusionnées en tant qu'option de fusion de groupe                                                           |   Fonctionnalité   |
| PSDJAVA-529 | Le fichier PSD en mode couleur 16 bits n'applique pas de masque pour les couches d'ajustement                                                     |      Problème     |
| PSDJAVA-530 | Rendu incorrect des parenthèses dans la couche de texte                                                                                          |      Problème     |
| PSDJAVA-531 | Impossible de mettre à jour les styles dans les calques de texte                                                                                 |      Problème     |
| PSDJAVA-532 | Après l'exportation du fichier PSD avec CMJN, les couleurs dans le PSD exporté sont altérées                                                     |      Problème     |
| PSDJAVA-533 | Un fichier PSB spécifique provoque l'exception "Le rectangle n'a aucune zone de traitement commune"                                              |      Problème     |
| PSDJAVA-534 | Échec du chargement de l'image. OverflowException : L'opération arithmétique a entraîné un dépassement                                            |      Problème     |

## **Changements dans l'API publique**
# **APIs ajoutées:**

- M:com.aspose.psd.PixelDataFormat.getCmyk16
- M:com.aspose.psd.PixelDataFormat.getCmyka16
- M:com.aspose.psd.fileformats.psd.layers.Layer.getBlendClippedElements
- M:com.aspose.psd.fileformats.psd.layers.Layer.setBlendClippedElements(boolean)

# **APIs supprimées:**

- Aucune

## **Exemples d'utilisation:**

** PSDJAVA-527. Implémenter la création d'un masque pour de nouvelles couches d'ajustement**

{{< highlight java >}}
public static void main(String[] args) {
    String srcFile = "src/main/resources/zendeya_BW.psd";
    String dstFile = "src/main/resources/zendeya_BW_out.psd";

    try (PsdImage im = (PsdImage) Image.load(srcFile)) {
        im.addBlackWhiteAdjustmentLayer();

        im.save(dstFile);
    }

    try (PsdImage im = (PsdImage) Image.load(dstFile)) {
        Layer layer = im.getLayers()[1];

        assertAreEqual(5, layer.getChannelsCount());
        assertAreEqual((short) -2, layer.getChannelInformation()[4].getChannelID());
    }
}

static void assertAreEqual(Object expected, Object actual) {
    assertAreEqual(expected, actual, "Les objets ne sont pas égaux.");
}

static void assertAreEqual(Object expected, Object actual, String message) {
    if (!expected.equals(actual)) {
        throw new IllegalArgumentException(message);
    }
}
{{< /highlight >}}

** PSDJAVA-528. Ajouter la prise en charge des couches fusionnées en tant qu'option de fusion de groupe**

{{< highlight java >}}
    String sourceFile = "src/main/resources/example_source.psd";
    String outputPsd = "src/main/resources/example_output.psd";
    String outputPng = "src/main/resources/example_output.png";

    try (PsdImage image = (PsdImage)Image.load(sourceFile)) {
        image.getLayers()[1].setBlendClippedElements(false);
        image.save(outputPsd);
        image.save(outputPng, new PngOptions());
    }
{{< /highlight >}}

** PSDJAVA-529. Le fichier PSD en mode couleur 16 bits n'applique pas de masque pour les couches d'ajustement**

{{< highlight java >}}
	String sourceFile = "src/main/resources/source.psd";
    String outputPng = "src/main/resources/current.png";

    try (PsdImage image = (PsdImage) Image.load(sourceFile)) {
        image.save(outputPng, new PngOptions());
    }
{{< /highlight >}}

** PSDJAVA-530. Rendu incorrect des parenthèses dans la couche de texte**

{{< highlight java >}}
    String file = "src/main/resources/file1.psd";
    String output = "src/main/resources/output_1235.png";

    try (PsdImage psdImage = (PsdImage) Image.load(file)) {
        for (Layer layer : psdImage.getLayers()) {
            if (layer instanceof TextLayer) {
                TextLayer textLayer = (TextLayer) layer;
                textLayer.getTextData().updateLayerData();

                PsdOptions imageOptions = new PsdOptions(psdImage);
                psdImage.save(output, imageOptions);
            }
        }
    }
{{< /highlight >}}

** PSDJAVA-531. Impossible de mettre à jour les styles dans les calques de texte**

{{< highlight java >}}
    String sourceFile = "src/main/resources/Example_FontSize.psd";
    String outputFile = "src/main/resources/output_Example_FontSize.psd";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setLoadEffectsResource(true);

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFile, psdLoadOptions)) {
        TextLayer l1 = (TextLayer) psdImage.getLayers()[4];
        TextLayer l2 = (TextLayer) psdImage.getLayers()[5];

        ITextPortion[] textItems1 = l1.getTextData().producePortions(new String[]{"text1", "text2"},
                l1.getTextData().getItems()[0].getStyle(), l1.getTextData().getItems()[0].getParagraph());

        l1.getTextData().removePortion(0);
        for (ITextPortion item : textItems1) {
            l1.getTextData().addPortion(item);
        }

        ITextPortion[] textItems2 = l2.getTextData().producePortions(new String[]{"text layer 1", "text layer 22"},
                l2.getTextData().getItems()[0].getStyle(), l2.getTextData().getItems()[0].getParagraph());

        for (ITextPortion item : textItems2) {
            l2.getTextData().addPortion(item);
        }

        l1.getTextData().updateLayerData();
        l2.getTextData().updateLayerData();

        psdImage.save(outputFile);
    }
{{< /highlight >}}

** PSDJAVA-532. Après l'exportation du fichier PSD avec CMJN, les couleurs dans le PSD exporté sont altérées**

{{< highlight java >}}
    String sourceFile = "src/main/resources/canyon.psd";
    String outputFilePng = "src/main/resources/output_canyon.png";

    MemoryStream outputStream = new MemoryStream();

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFile)) {
        psdImage.save(outputStream.toOutputStream());
    }

    outputStream.setPosition(0);
    try (PsdImage psdImage = (PsdImage) Image.load(outputStream.toInputStream())) {
        psdImage.save(outputFilePng, new PngOptions());
    }

    outputStream.close();
{{< /highlight >}}

** PSDJAVA-533. Un fichier PSB spécifique provoque l'exception "Le rectangle n'a aucune zone de traitement commune" **

{{< highlight java >}}
    String input = "src/main/resources/1619_src.psb";
    String output = "src/main/resources/1619_output.png";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setLoadEffectsResource(true);
    try (PsdImage img = (PsdImage) Image.load(input, psdLoadOptions)) {
        PngOptions pngOptions = new PngOptions();
        pngOptions.setCompressionLevel(9);
        pngOptions.setColorType(PngColorType.TruecolorWithAlpha);
        img.save(output, pngOptions);
    }
{{< /highlight >}}

** PSDJAVA-534. Échec du chargement de l'image. OverflowException : L'opération arithmétique a entraîné un dépassement. **

{{< highlight java >}}
public static void main(String[] args) {
    String sourceFile = "src/main/resources/9baa6962-f409-41ee-88da-418ea87bb56f_test_2.psd";

    try (PsdImage im = (PsdImage)PsdImage.load(sourceFile))
    {
        Layer layer = im.getLayers()[28];
        GrdmResource grdmResource = (GrdmResource)layer.getResources()[0];

        assertAreEqual("自定", grdmResource.getGradientName());
    }

}

static void assertAreEqual(Object expected, Object actual) {
    assertAreEqual(expected, actual, "Les objets ne sont pas égaux.");
}

static void assertAreEqual(Object expected, Object actual, String message) {
    if (!expected.equals(actual)) {
        throw new IllegalArgumentException(message);
    }
}
{{< /highlight >}}
