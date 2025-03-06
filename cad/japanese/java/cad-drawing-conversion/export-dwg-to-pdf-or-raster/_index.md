---
title: Aspose.CAD for Java を使用して DWG を PDF またはラスターにエクスポート
linktitle: DWG を PDF またはラスターにエクスポート
second_title: Aspose.CAD Java API
description: Aspose.CAD を使用して Java で DWG ファイルを PDF またはラスター イメージにエクスポートするシームレスなプロセスを確認してください。このステップバイステップのガイドは、正確さと効率性を保証します。
weight: 13
url: /ja/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java を使用して DWG を PDF またはラスターにエクスポート

## 導入

コンピューター支援設計 (CAD) のダイナミックな世界では、図面を効率的に処理することが非常に重要です。 Aspose.CAD for Java は、DWG ファイルを PDF またはラスター イメージにエクスポートするための強力なソリューションを提供します。このチュートリアルでは、Aspose.CAD for Java の可能性を最大限に活用できるように、プロセスをガイドします。

## 前提条件

チュートリアルに入る前に、次のものが揃っていることを確認してください。

- Java プログラミングの基本的な理解。
-  Aspose.CAD for Java ライブラリがインストールされています。そうでない場合は、ダウンロードしてください[ここ](https://releases.aspose.com/cad/java/).
- テスト用の DWG ファイル。提供されている「Bottom_plate.dwg」ファイルを使用できます。

## 名前空間のインポート

Java プロジェクトで、プロセスを開始するために必要な名前空間をインポートします。

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## ステップ 1: DWG ファイルをロードする

まず、Aspose.CAD を使用して DWG ファイルをロードします。`Image`クラス：

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

## ステップ 2: ユニットのタイプを決定する

次に、ロードされた DWG ファイルのユニット タイプを確認します。

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

## ステップ 3: ラスタライズ オプションを設定する

ユニット タイプに基づいて、ラスタライズ オプションを構成します。

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

if (currentUnitIsMetric) {
    //メートル単位
    double metersCoeff = 1 / 1000.0;
    double scaleFactor = metersCoeff / currentUnitCoefficient;
    rasterizationOptions.setPageWidth((float)(210 * scaleFactor));
    rasterizationOptions.setPageHeight((float)(297 * scaleFactor));
    rasterizationOptions.setUnitType(UnitType.Millimeter);
} else {
    //インペリアル単位
    rasterizationOptions.setPageWidth((float)(8.27f / currentUnitCoefficient));
    rasterizationOptions.setPageHeight((float)(11.69f / currentUnitCoefficient));
    rasterizationOptions.setUnitType(UnitType.Inch);
}
```

## ステップ 4: PDF オプションを構成する

PDF エクスポート オプションを設定します。

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

## ステップ 5: PDF として保存

最後に、DWG ファイルを PDF として保存します。

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

そして、それができました！ Aspose.CAD for Java を使用して DWG ファイルを PDF にエクスポートできました。

## 結論

このチュートリアルでは、Aspose.CAD for Java を利用して DWG ファイルを PDF またはラスター イメージにエクスポートするためのステップバイステップのガイドを提供しました。このライブラリによりプロセスが簡素化され、Java アプリケーションで CAD 図面を効率的に処理できるようになります。

## よくある質問

### Q1: Aspose.CAD for Java を他の Java フレームワークと一緒に使用できますか?

A1: はい、Aspose.CAD for Java は、一般的な Java フレームワークとシームレスに統合します。

### Q2: Aspose.CAD for Java の一時ライセンスは利用できますか?

 A2: はい、一時ライセンスを取得できます。[ここ](https://purchase.aspose.com/temporary-license/).

### Q3: Aspose.CAD for Java のサポートはどこで見つけられますか?

 A3: にアクセスしてください。[Aspose.CAD フォーラム](https://forum.aspose.com/c/cad/19)コミュニティからの支援が必要です。

### Q4: Aspose.CAD for Java のライセンスはどのように購入できますか?

 A4: ライセンスを購入できます。[ここ](https://purchase.aspose.com/buy).

### Q5: Aspose.CAD for Java はどの単位をサポートしていますか?

A5: Aspose.CAD for Java は、メートル単位とインペリアル単位の両方をサポートしています。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
