---
title: Aspose.PSD for Java 24.6 - リリースノート
type: docs
weight: 40
url: /ja/java/aspose-psd-for-java-24-6-release-notes/
---

{{% alert color="primary" %}} このページには [Aspose.PSD for Java 24.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.6/) のリリースノートが含まれています。 {{% /alert %}}

| **キー**     | **概要**                                                                                                      | **カテゴリ** |
|:------------|:-----------------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-628 | Gradient マップレイヤーのサポートを実装する                                                                          | 機能      |
| PSDJAVA-629 | [AI フォーマット] AI フォーマットに XPacket メタデータのサポートを追加する                                                         | 機能      |
| PSDJAVA-630 | Inflate、Squeeze、および Twist タイプの歪みを実装する                                                              | 機能      |
| PSDJAVA-631 | ArtBoard レイヤーを持つファイル内の Rgb および Lab モードは、3 チャンネル未満および 4 チャンネルを超えることはできません | バグ          |
| PSDJAVA-632 | 特定のファイルの処理中に、処理エリアのトップは正でなければなりません。 （パラメーター 'areaToProcess'）        | バグ          |
| PSDJAVA-633 | 保存後にキャンバス画像が切り取られる展開されたエラー。データは失われますが、プレビューは正しく表示されます               | バグ          |

## **公開 API 変更**
# **追加された API:**

- M:com.aspose.psd.fileformats.ai.AiImage.getXmpData
- M:com.aspose.psd.fileformats.psd.PsdImage.addGradientMapAdjustmentLayer
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GrdmResource.setMaximumColor(com.aspose.psd.fileformats.psd.rawcolor.RawColor)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GrdmResource.setMinimumColor(com.aspose.psd.fileformats.psd.rawcolor.RawColor)
- T:com.aspose.psd.fileformats.psd.layers.adjustmentlayers.GradientMapLayer
- M:com.aspose.psd.fileformats.psd.layers.adjustmentlayers.GradientMapLayer.setGradientSettings(com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings)
- M:com.aspose.psd.fileformats.psd.layers.adjustmentlayers.GradientMapLayer.getGradientSettings
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.getExpansionCount
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.setExpansionCount(short)
- T:com.aspose.psd.fileformats.psd.layers.layerresources.GradientHelper
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GradientHelper.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GradientHelper.gradientKindToStr(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GradientHelper.noiseColorModelToInt(short)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GradientHelper.noiseColorModelToStr(short)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GradientHelper.intToNoiseColorModel(short)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GradientHelper.strToGradientKind(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GradientHelper.strToNoiseColorModel(java.lang.String)
- F:com.aspose.psd.fileformats.psd.layers.layerresources.GradientHelper.StrGradientNoise
- F:com.aspose.psd.fileformats.psd.layers.layerresources.GradientHelper.StrGradientSolid
- F:com.aspose.psd.fileformats.psd.layers.layerresources.GradientHelper.StrModelHSB
- F:com.aspose.psd.fileformats.psd.layers.layerresources.GradientHelper.StrModelLAB
- F:com.aspose.psd.fileformats.psd.layers.layerresources.GradientHelper.StrModelRGB
- F:com.aspose.psd.fileformats.psd.layers.layerresources.GradientHelper.IntModelRGB
- F:com.aspose.psd.fileformats.psd.layers.layerresources.GradientHelper.IntModelLAB
- F:com.aspose.psd.fileformats.psd.layers.layerresources.GradientHelper.IntModelHSB
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.getGradientName
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.setGradientName(java.lang.String)

# **削除された API:**

- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getGradientName
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.setGradientName(java.lang.String)
- T:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.gradientKindToStr(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.noiseColorModelToStr(short)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.strToGradientKind(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.strToNoiseColorModel(java.lang.String)
- F:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.StrGradientNoise
- F:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.StrGradientSolid
- F:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.StrModelHSB
- F:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.StrModelLAB
- F:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.StrModelRGB

## **使用例**

**PSDJAVA-628. Gradient マップレイヤーのサポートを実装する**

{{< highlight java >}}

    public static void main(String[] args) {
        String sourceFile = "src/main/resources/gradient_map_src.psd";
        String outputFile = "src/main/resources/gradient_map_src_output.psd";

        try (PsdImage im = (PsdImage) Image.load(sourceFile)) {
            // Gradation マップ調整レイヤーを追加します。
            GradientMapLayer layer = im.addGradientMapAdjustmentLayer();
            layer.getGradientSettings().setReverse(true);

            im.save(outputFile);
        }

        // 保存された変更を確認します
        try (PsdImage im = (PsdImage) Image.load(outputFile)) {
            GradientMapLayer gradientMapLayer = (GradientMapLayer) im.getLayers()[1];
            GradientFillSettings gradientSettings = (GradientFillSettings) gradientMapLayer.getGradientSettings();

            assertAreEqual(0.0, gradientSettings.getAngle());
            assertAreEqual((short) 4096, gradientSettings.getInterpolation());
            assertAreEqual(true, gradientSettings.getReverse());
            assertAreEqual(false, gradientSettings.getAlignWithLayer());
            assertAreEqual(false, gradientSettings.getDither());
            assertAreEqual(GradientType.Linear, gradientSettings.getGradientType());
            assertAreEqual(100, gradientSettings.getScale());
            assertAreEqual(0.0, gradientSettings.getHorizontalOffset());
            assertAreEqual(0.0, gradientSettings.getVerticalOffset());
            assertAreEqual("Custom", gradientSettings.getGradientName());
        }
    }

    static void assertAreEqual(Object expected, Object actual) {
        assertAreEqual(expected, actual, "オブジェクトが等しくありません。");
    }

    static void assertAreEqual(Object expected, Object actual, String message) {
        if (!expected.equals(actual)) {
            throw new IllegalArgumentException(message);
        }
    }

{{< /highlight >}}

**PSDJAVA-629. [AI フォーマット] AI フォーマットに XPacket メタデータのサポートを追加する**

{{< highlight java >}}

    public static void main(String[] args) {
        String sourceFile = "src/main/resources/ai_one.ai";

        String creatorToolKey = ":CreatorTool";
        String nPagesKey = "xmpTPg:NPages";
        String unitKey = "stDim:unit";
        String heightKey = "stDim:h";
        String widthKey = "stDim:w";

        String expectedCreatorTool = "Adobe Illustrator CC 22.1 (Windows)";
        String expectedNPages = "1";
        String expectedUnit = "Pixels";
        double expectedHeight = 768;
        double expectedWidth = 1366;

        try (AiImage image = (AiImage) Image.load(sourceFile)) {
            // Xmp Metadata が追加されました。
            var xmpMetaData = image.getXmpData();

            assertIsNotNull(xmpMetaData);

            // 現在、AI ファイルの Xmp パッケージにアクセスできます。
            var basicPackage = (XmpBasicPackage) xmpMetaData.getPackage(Namespaces.XmpBasic);
            XmpPackage package_ = xmpMetaData.getPackages()[4];
            // これらのパッケージのコンテンツにアクセスできます。
            var creatorTool = basicPackage.get_Item(creatorToolKey).toString();
            var nPages = package_.get_Item(nPagesKey);
            var unit = package_.get_Item(unitKey);
            var height = Double.parseDouble(package_.get_Item(heightKey).toString());
            var width = Double.parseDouble(package_.get_Item(widthKey).toString());

            assertAreEqual(creatorTool, expectedCreatorTool);
            assertAreEqual(nPages, expectedNPages);
            assertAreEqual(unit, expectedUnit);
            assertAreEqual(height, expectedHeight);
            assertAreEqual(width, expectedWidth);
        }
    }

    static void assertAreEqual(Object expected, Object actual) {
        assertAreEqual(expected, actual, "オブジェクトは等しくありません。");
    }

    static void assertAreEqual(Object expected, Object actual, String message) {
        if (!expected.equals(actual)) {
            throw new IllegalArgumentException(message);
        }
    }

    static void assertIsNotNull(Object testObject) {
        if (testObject == null) {
            throw new RuntimeException("テストオブジェクトは null です。");
        }
    }

{{< /highlight >}}

**PSDJAVA-630. Inflate、Squeeze、および Twist タイプの歪みを実装する**

{{< highlight java >}}

    String[] files = {"Twist", "Squeeze", "Squeeze_vert", "Inflate"};

    for (String prefix : files) {
        String sourceFile = "src/main/resources/" + prefix + ".psd";
        String outputFile = "src/main/resources/" + prefix + "_export.png";

        PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
        psdLoadOptions.setAllowWarpRepaint(true);
        psdLoadOptions.setLoadEffectsResource(true);
        try (PsdImage psdImage = (PsdImage) Image.load(sourceFile, psdLoadOptions)) {
            PngOptions pngOptions = new PngOptions();
            pngOptions.setColorType(PngColorType.TruecolorWithAlpha);
            psdImage.save(outputFile, pngOptions);
        }
    }

{{< /highlight >}}

**PSDJAVA-631. ArtBoard レイヤーを持つファイル内の Rgb および Lab モードは、3 チャンネル未満および 4 チャンネルを超えることはできません**

{{< highlight java >}}

    String sourceFile = "src/main/resources/Rgb5Channels.psb";
    String outputFile = "src/main/resources/Rgb5Channels_output.psd";

    try (PsdImage image = (PsdImage) Image.load(sourceFile)) {
        // ここに例外は発生しません
        image.save(outputFile);
    }

{{< /highlight >}}

**PSDJAVA-632. 特定のファイルの処理中に、処理エリアのトップは正でなければなりません。 （パラメーター 'areaToProcess'）**

{{< highlight java >}}

    String sourceFile = "src/main/resources/BANNERS_2_Intel-Gamer_psak.psd";
    String outputFile = "src/main/resources/BANNERS_2_Intel-Gamer_psak_out.psd";
    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setLoadEffectsResource(true);
    psdLoadOptions.setAllowWarpRepaint(true);
    try (PsdImage image = (PsdImage) PsdImage.load(sourceFile, psdLoadOptions)) {
        image.save(outputFile);
        // 例外が発生すべきではありません
    }

{{< /highlight >}}

**PSDJAVA-633. 保存後にキャンバス画像が切り取られる展開されたエラー。データは失われますが、プレビューは正しく表示されます**

{{< highlight java >}}

    String sourceFile = "src/main/resources/bigfile.psd";

    String outputFile = "src/main/resources/bigfile_output.psd";
    String outputPicture = "src/main/resources/bigfile.png";

    PsdLoadOptions loadOptions = new PsdLoadOptions();
    loadOptions.setLoadEffectsResource(true);
    loadOptions.setUseDiskForLoadEffectsResource(true);

    try (var psdImage = (PsdImage) Image.load(sourceFile, loadOptions)) {
        PsdOptions psdOptions = new PsdOptions();
        psdOptions.setCompressionMethod(CompressionMethod.RLE);
        // ここでエラーは発生しません
        psdImage.save(outputFile, psdOptions);
    }

    try (var psdImage = (PsdImage) Image.load(outputFile, loadOptions)) {
        psdImage.resize(psdImage.getWidth() / 10, psdImage.getHeight() / 10);

        PngOptions pngOptions = new PngOptions();
        pngOptions.setColorType(PngColorType.TruecolorWithAlpha);
        // ここでエラーは発生しません
        psdImage.save(outputPicture, pngOptions);
    }

{{< /highlight >}}