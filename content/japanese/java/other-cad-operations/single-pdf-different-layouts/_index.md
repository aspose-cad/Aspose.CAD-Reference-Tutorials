---
title: Aspose.CAD for Java を使用した動的 PDF の作成
linktitle: 異なるレイアウトを持つ単一の PDF
second_title: Aspose.CAD Java API
description: Aspose.CAD for Java を使用して、CAD 図面から多様なレイアウトを備えた美しい PDF を作成します。 Java 開発者向けの簡単な統合と強力な機能。
type: docs
weight: 16
url: /ja/java/other-cad-operations/single-pdf-different-layouts/
---
## 導入

Aspose.CAD for Java の世界へようこそ。これは、開発者が CAD 図面を簡単に操作できるようにする強力なライブラリです。このチュートリアルでは、Aspose.CAD for Java を使用して、さまざまなレイアウトを持つ単一の PDF を作成する方法について詳しく説明します。経験豊富な開発者でも、初心者でも、このステップバイステップのガイドでプロセスを説明します。

## 前提条件

この作業を開始する前に、次の前提条件が満たされていることを確認してください。
- Java 環境: マシンに Java がインストールされていることを確認してください。
-  Aspose.CAD ライブラリ: Java 用の Aspose.CAD ライブラリを次の場所からダウンロードしてインストールします。[ダウンロードリンク](https://releases.aspose.com/cad/java/).
- ドキュメント ディレクトリ: DWG 図面用のディレクトリを設定します。

## パッケージのインポート

Java プロジェクトで、必要なパッケージをインポートします。

```java
import com.aspose.cad.Image;
import com.aspose.cad.SizeF;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.VectorRasterizationOptions;
```

## ステップ 1: CAD 図面をロードする

まず、CAD 図面を`CadImage`物体：

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
CadImage cadImage = (CadImage)Image.load(dataDir + "City skyway map.dwg");
```

## ステップ 2: ラスタライズ オプションを構成する

CAD イメージのラスタライズ オプションを設定します。

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1000);
rasterizationOptions.setPageHeight(1000);
```

## ステップ 3: レイアウトのページ サイズをカスタマイズする

CAD 図面内のいくつかのレイアウトのカスタム サイズを定義します。

```java
rasterizationOptions.getLayoutPageSizes().addItem("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.getLayoutPageSizes().addItem("8.5 x 11 Plot", new SizeF(1000, 100));
```

## ステップ 4: PDF オプションを設定する

ラスタライズ設定を組み込んで PDF オプションを構成します。

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## ステップ 5: PDF として保存

処理された CAD イメージを PDF として保存します。

```java
cadImage.save(dataDir + "singlePDF_out.pdf", pdfOptions);
```

おめでとう！ Aspose.CAD for Java を使用して、さまざまなレイアウトを持つ 1 つの PDF を正常に作成できました。

## 結論

このチュートリアルでは、CAD 図面からさまざまなレイアウトを持つ PDF を生成するための、Aspose.CAD for Java のシームレスな統合について検討しました。このライブラリの柔軟性と堅牢な機能により、CAD 操作タスクに最適な選択肢となります。

## よくある質問

### Q1: Aspose.CAD for Java を他の Java ライブラリと一緒に使用できますか?

A1: はい。Aspose.CAD for Java は、他の Java ライブラリとシームレスに統合するように設計されており、広範な機能を提供します。

### Q2: 体験版はありますか?

 A2: もちろんです！無料の試用版にアクセスできます[ここ](https://releases.aspose.com/).

### Q3: 追加のサポートはどこで入手できますか?

 A3: にアクセスしてください。[Aspose.CAD フォーラム](https://forum.aspose.com/c/cad/19)コミュニティのサポートとディスカッションのために。

### Q4: 仮免許はどのように取得すればよいですか?

 A4: 仮免許を取得できます。[ここ](https://purchase.aspose.com/temporary-license/).

### Q5: フルバージョンはどこで購入できますか?

A5: Aspose.CAD for Java のフルバージョンを購入してください[ここ](https://purchase.aspose.com/buy).