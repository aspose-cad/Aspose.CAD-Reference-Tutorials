---
title: DGN から PDF への変換ガイド - Aspose.CAD for Java
linktitle: DGN V7 のサポート
second_title: Aspose.CAD Java API
description: Aspose.CAD for Java を使用して、DGN ファイルを PDF に簡単に変換します。シームレスな統合と効率的なワークフローについては、ステップバイステップのガイドに従ってください。
type: docs
weight: 11
url: /ja/java/other-cad-operations/support-for-dgn-v7/
---
## 導入

CAD (コンピューター支援設計) のダイナミックな世界では、DGN (設計) ファイルを PDF (Portable Document Format) に効率的に変換することが重要な要件です。 Aspose.CAD for Java は、シームレスな統合と堅牢な機能を提供する強力なソリューションとして登場します。このステップバイステップのガイドは、Aspose.CAD for Java を使用して DGN ファイルを PDF にエクスポートするプロセスを段階的に説明し、スムーズで効率的なワークフローを確保することを目的としています。

## 前提条件

チュートリアルに入る前に、次の前提条件が満たされていることを確認してください。
-  Aspose.CAD for Java ライブラリ: からライブラリをダウンロードしてインストールします。[Aspose.CAD for Java ダウンロード ページ](https://releases.aspose.com/cad/java/).
- Java 開発環境: マシン上に Java 開発環境がセットアップされていることを確認してください。

## パッケージのインポート

まず、必要なパッケージを Java プロジェクトにインポートします。

## ステップ 1: 必要なパッケージをインポートする

Java プロジェクトで、Aspose.CAD for Java に必要なパッケージをインポートします。
```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.cadobjects.DgnImage;
import com.aspose.cad.imageoptions.PdfOptions;
import java.awt.Color;
```

## ステップ 2: ファイル パスを設定する

入力 DGN ファイルと出力 PDF ファイルのパスを定義します。

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

## ステップ 3: DGN イメージをロードする

Aspose.CAD ライブラリを使用して DGN イメージをロードします。

```java
DgnImage objImage = (DgnImage)Image.load(fileName);
```

## ステップ 4: PDF エクスポート オプションを構成する

ページ寸法、自動レイアウト拡大縮小、背景色、エクスポートする特定のレイアウトなど、PDF にエクスポートするためのオプションを設定します。

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setBackgroundColor(Color.getBlack());
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); //4 つのビュー (1、2、3、および 9) のみをエクスポートします
options.setVectorRasterizationOptions(vectorOptions);
```

## ステップ 5: PDF ファイルを保存する

指定したオプションを使用して、DGN イメージを PDF ファイルとして保存します。

```java
objImage.save(outFile, options);
```

さまざまな DGN ファイルに対してこれらの手順を繰り返し、必要に応じてファイル パスとオプションを調整します。

## 結論

Aspose.CAD for Java を使用すると、DGN ファイルを PDF に変換するプロセスが簡単になります。このガイドでは、ライブラリを Java プロジェクトにシームレスに統合し、効率的な CAD ファイル変換を容易にするための知識を提供します。

## よくある質問

### Q1: Aspose.CAD for Java を他の CAD ファイル形式で使用できますか?

A1: はい、Aspose.CAD はさまざまな CAD 形式をサポートし、DGN から PDF への変換以外にも多彩な機能を提供します。

### Q2: Aspose.CAD for Java の一時ライセンスは利用できますか?

 A2: はい、一時ライセンスを取得できます。[ここ](https://purchase.aspose.com/temporary-license/)テスト目的のため。

### Q3: Aspose.CAD for Java についてサポートを求めたり、質問したりするにはどうすればよいですか?

 A3: にアクセスしてください。[Aspose.CAD フォーラム](https://forum.aspose.com/c/cad/19)コミュニティとつながり、支援を求めます。

### Q4: DGN を PDF に変換する場合、どのようなレイアウトをエクスポートできますか?

 A4: カスタマイズすることで、エクスポートするレイアウトを指定できます。`setLayouts`コード内の配列。

### Q5: Aspose.CAD for Java の包括的なドキュメントはどこで見つけられますか?

 A5: を参照してください。[Aspose.CAD for Java ドキュメント](https://reference.aspose.com/cad/java/)詳細については。