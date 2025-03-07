---
title: キャンバスのサイズとモードを設定する
linktitle: キャンバスのサイズとモードを設定する
second_title: Aspose.CAD Java API
description: キャンバスのサイズとモードの設定に関するステップバイステップのガイドを使用して、Aspose.CAD for Java の威力を体験してください。 CAD ファイルを PDF および TIFF 形式に簡単に変換します。
weight: 16
url: /ja/java/advanced-cad-features/set-canvas-size-and-mode/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# キャンバスのサイズとモードを設定する

## 導入

Aspose.CAD for Java の機能を活用して、CAD 変換プロセスを強化したいと考えていますか?この包括的なガイドでは、Aspose.CAD for Java を使用してキャンバスのサイズとモードを設定する手順を説明します。経験豊富な開発者であっても、初心者であっても、このチュートリアルは必要な洞察を提供します。

## 前提条件

チュートリアルに入る前に、次の前提条件が満たされていることを確認してください。

-  Aspose.CAD for Java: Java 環境に Aspose.CAD ライブラリがインストールされていることを確認します。ダウンロードできます[ここ](https://releases.aspose.com/cad/java/).

- ドキュメント ディレクトリ: CAD ファイルを保存するドキュメント ディレクトリを設定します。このディレクトリはチュートリアルの手順で参照されます。

それでは、ステップバイステップのガイドを始めましょう。

## 名前空間のインポート

このステップでは、Aspose.CAD プロジェクトを開始するために必要な名前空間をインポートします。
```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## ステップ 1: Aspose.CAD クラスをインポートする

```java
//リソース ディレクトリへのパス。
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

このスニペットでは、リソース ディレクトリへのパスを設定し、Aspose.CAD を使用して DXF ファイルをロードします。`Image`クラス。

## ステップ 2: CadRasterizationOptions プロパティを設定する

```java
//CadRasterizationOptions のインスタンスを作成し、そのさまざまなプロパティを設定します
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

ここでは、次のインスタンスを作成します。`CadRasterizationOptions`ページの幅、ページの高さ、拡大縮小オプションなどのプロパティを構成します。

## ステップ 3: PdfOptions を作成し、VectorRasterizationOptions を設定する

```java
//PdfOptions のインスタンスを作成する
PdfOptions pdfOptions = new PdfOptions();

//VectorRasterizationOptions プロパティを設定する
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

ここで、`PdfOptions`インスタンスを作成し、そのインスタンスを設定します`VectorRasterizationOptions`プロパティを以前に設定したものに`CadRasterizationOptions`.

## ステップ 4: PDF にエクスポートする

```java
//CAD を PDF にエクスポート
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

最後に、指定したオプションを使用して CAD イメージを PDF ファイルに保存します。

## ステップ 5: TiffOptions を作成し、VectorRasterizationOptions を設定する

```java
//TiffOptions のインスタンスを作成する
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

//VectorRasterizationOptions プロパティを設定する
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

このステップでは、`TiffOptions`インスタンスを作成し、その設定を行う`VectorRasterizationOptions`財産。

## ステップ 6: TIFF にエクスポートする

```java
//CAD を TIFF にエクスポート
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

最後に、指定したオプションを使用して CAD イメージを TIFF ファイルに保存します。

## 結論

おめでとう！ Aspose.CAD for Java を使用してキャンバスのサイズとモードを正常に設定しました。このチュートリアルは、CAD 変換プロジェクトの強固な基盤を提供します。のさらなる機能と可能性を探ってください。[Aspose.CAD ドキュメント](https://reference.aspose.com/cad/java/).

## よくある質問

### Q1: Aspose.CAD for Java を他の Java フレームワークと一緒に使用できますか?

A1: はい、Aspose.CAD はさまざまな Java フレームワークとシームレスに統合するように設計されています。

### Q2: Aspose.CAD の一時ライセンスは利用できますか?

 A2: はい、一時ライセンスを取得できます。[ここ](https://purchase.aspose.com/temporary-license/).

### Q3: Aspose.CAD のコミュニティ サポートはどこで受けられますか?

 A3: にアクセスしてください。[Aspose.CAD フォーラム](https://forum.aspose.com/c/cad/19)コミュニティのサポートとディスカッションのために。

### Q4: Aspose.CAD を無料で試すことはできますか?

 A4：もちろんです！無料トライアルを利用する[ここ](https://releases.aspose.com/).

### Q5: Aspose.CAD for Java を購入するにはどうすればよいですか?

A5: 製品を購入してください[ここ](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
