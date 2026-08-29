---
date: 2026-08-29
description: Aspose.CAD for Java を使用して、PDFページサイズの設定方法と CAD を PDF に変換する方法を学びます。自動レイアウトスケーリングと
  TIFF エクスポートにも対応しています。
keywords:
- set pdf page size
- convert cad to pdf
- canvas size java
- high resolution tiff
- change pdf dimensions
lastmod: 2026-08-29
linktitle: PDFページサイズの設定 – CADをPDFに変換
og_description: Aspose.CAD を使用して Java で CAD 図面を PDF に変換しながら PDF ページサイズを設定する方法を学びます。このガイドでは、キャンバス寸法、自動レイアウトスケーリング、および高解像度
  TIFF へのエクスポートについて説明します。
og_image_alt: Tutorial showing how to set pdf page size and convert CAD to PDF in
  Java
og_title: PDFページサイズの設定 – Aspose を使用した Java での CAD から PDF への変換
schemas:
- author: Aspose
  dateModified: '2026-08-29'
  description: Learn how to set pdf page size and convert CAD to PDF using Aspose.CAD
    for Java, with automatic layout scaling and TIFF export.
  headline: Set pdf page size – convert cad to pdf (Java)
  type: TechArticle
- questions:
  - answer: No. Canvas size controls page dimensions; vector data remains resolution‑independent,
      ensuring crisp rendering at any zoom level.
    question: does the canvas size affect vector quality in the PDF?
  - answer: Yes. Adjust `rasterizationOptions.setResolution(dpiValue)` before creating
      `TiffOptions`.
    question: can I set a different DPI for the TIFF output?
  - answer: Use Aspose.PDF to load the generated PDF and call `pdf.getPages().setPageSize(PageSize.A4)`
      or a custom size.
    question: how can I change PDF dimensions for an existing PDF without re‑rendering
      the CAD?
  - answer: Keep `setAutomaticLayoutsScaling(true)` and avoid `setNoScaling(true)`;
      this retains layer visibility and layout fidelity.
    question: what is the best way to convert dxf to pdf while preserving layers?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- set pdf page size
- convert cad
- Aspose.CAD
- Java
- high resolution tiff
title: PDFページサイズの設定 – CADをPDFに変換 (Java)
url: /ja/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PDFページサイズの設定 – CADをPDFに変換 (Java)

## はじめに

CAD図面をPDFに変換する際に **pdfページサイズを設定** したい場合は、ここが適切な場所です。このチュートリアルでは、Aspose.CAD for Java を使用して正確なキャンバス寸法を定義し、自動レイアウトスケーリングを有効にし、結果をPDFとTIFFの両方にエクスポートする方法を示します。印刷用のエンジニアリング図面を準備する場合でも、ウェブギャラリー用のサムネイルを生成する場合でも、ページサイズと出力解像度を制御することは重要です。

## クイック回答
- **「CADをPDFに変換」とは何ですか？** 任意のプラットフォームで閲覧できるPDFドキュメントに、CAD図面（例：DXF、DWG）を変換することです。  
- **TIFFにもエクスポートできますか？** はい — `TiffOptions` を使用して高解像度ラスタ画像を作成します。  
- **Javaでキャンバスサイズを制御するオプションはどれですか？** `CadRasterizationOptions.setPageWidth/Height`。  
- **自動レイアウトスケーリングとは何ですか？** キャンバスサイズが変わったときに元のレイアウト比率を保持するフラグ（`setAutomaticLayoutsScaling(true)`）。  
- **Aspose.CADのライセンスは必要ですか？** 本番環境で使用するには、一時的または永続的なライセンスが必要です。

## JavaでCADをPDFに変換する際のpdfページサイズの設定方法

CADファイルを読み込み、`CadRasterizationOptions` に希望の幅と高さを設定し、自動レイアウトスケーリングを有効にした後、結果をPDFとして保存します。この二段階のアプローチにより、ベクター品質を損なうことなく出力ページの正確な寸法を制御できます。

## 「CADをPDFに変換」とは何ですか？

CADをPDFに変換するとは、ベクトルベースのエンジニアリング図面をPDFページとしてレンダリングし、線画、レイヤー、ジオメトリを保持しつつ、ファイルを普遍的にアクセス可能にすることです。指定されたオプションに従って図面をラスタライズし、任意のデバイスでCADソフトウェアなしに開けるPDFを生成し、元の設計の視覚的忠実度を保ちます。

## なぜJavaでキャンバスサイズを設定するのか？

Javaでキャンバスサイズを設定すると、出力解像度とページ寸法を定義でき、生成されたPDFまたはTIFFが印刷や表示の要件に合致します。また、スケーリング動作を制御できるため、大判図面にとって重要です。

## 前提条件

チュートリアルに入る前に、以下の前提条件が整っていることを確認してください。

- Aspose.CAD for Java: Java環境に Aspose.CAD ライブラリがインストールされていることを確認してください。ライブラリは[ここ](https://releases.aspose.com/cad/java/)からダウンロードできます。  
- Document directory: CADファイルを保存するドキュメントディレクトリを設定します。このディレクトリはチュートリアルの手順で参照されます。

さあ、ステップバイステップのガイドを始めましょう。

## 名前空間のインポート

このステップでは、Aspose.CAD プロジェクトを開始するために必要な名前空間をインポートします。

`Image` は CAD ファイルの読み込みに使用される主要クラスです。

```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## 手順 1: Aspose.CAD クラスのインポート

`Image` クラスは CAD 図面の読み込みと保存のメソッドを提供します。

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

このスニペットでは、リソースディレクトリへのパスを設定し、Aspose.CAD の `Image` クラスを使用して DXF ファイルを読み込みます。

## 手順 2: CadRasterizationOptions プロパティの設定（Javaでキャンバスサイズを設定）

`CadRasterizationOptions` は CAD からラスタへの変換におけるページサイズやスケーリングなどのラスタライズ設定を指定します。

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

ここでは、`CadRasterizationOptions` のインスタンスを作成し、ページ幅、ページ高さ、そして **自動レイアウトスケーリング** などのプロパティを設定します。これが変換時の **キャンバスモードの構成** の中心です。

## 手順 3: PdfOptions の作成と vectorRasterizationOptions の設定

`PdfOptions` は変換の PDF 出力設定を定義します。

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

次に、`PdfOptions` インスタンスを作成し、その `VectorRasterizationOptions` プロパティに先ほど構成した `CadRasterizationOptions` を設定します。

## 手順 4: PDF にエクスポート（CADをPDFに変換）

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

最後に、指定したオプションを使用して CAD 画像を PDF ファイルとして保存し、**CADをPDFに変換** プロセスを完了します。

## 手順 5: TiffOptions の作成と vectorRasterizationOptions の設定（CADをTIFFにエクスポート）

`TiffOptions` は圧縮や解像度などの TIFF 出力パラメータを構成します。

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## 手順 6: TIFF にエクスポート

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

最後に、指定したオプションを使用して CAD 画像を TIFF ファイルとして保存し、キャンバスサイズを構成した後の **CADをTIFFにエクスポート** 方法を示します。

## よくある問題と解決策

| 問題 | 原因 | 対策 |
|------|------|------|
| 出力PDFが空白 | `setNoScaling(true)` が一部の図面のレンダリングを無効にする | `setNoScaling(true)` を削除するか、`false` に設定してください。 |
| TIFFの解像度が低い | ページ幅/高さが小さすぎる | `setPageWidth` / `setPageHeight` の値を増やす。 |
| レイアウトが歪んでいる | 自動レイアウトスケーリングが無効になっている | `setAutomaticLayoutsScaling(true)` が有効であることを確認する。 |

## なぜキャンバスサイズと DPI を調整するのか？

キャンバスサイズを変更すると、出力のラスタライズ解像度に直接影響します。**TIFF の解像度を上げたい** 場合は、`setPageWidth` / `setPageHeight` の値を上げるか、`TiffOptions` を作成する前に `rasterizationOptions.setResolution(300)` を呼び出してください。これにより、印刷や詳細検査に適した高品質のラスタ画像が得られます。

## よくある質問

**Q1: Aspose.CAD for Java を他の Java フレームワークと併用できますか？**  
A: はい、Aspose.CAD はさまざまな Java フレームワークとシームレスに統合できるように設計されています。

**Q2: Aspose.CAD の一時ライセンスは利用可能ですか？**  
A: はい、一時ライセンスは[ここ](https://purchase.aspose.com/temporary-license/)で取得できます。

**Q3: Aspose.CAD のコミュニティサポートはどこで得られますか？**  
A: Aspose.CAD フォーラム [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) でコミュニティサポートとディスカッションが利用できます。

**Q4: Aspose.CAD を無料で試せますか？**  
A: もちろんです！無料トライアルは[ここ](https://releases.aspose.com/)からダウンロードできます。

**Q5: Aspose.CAD for Java の購入方法は？**  
A: Aspose.CAD for Java は[ここ](https://purchase.aspose.com/buy)から購入できます。

**追加 Q&A**

**Q: キャンバスサイズは PDF のベクター品質に影響しますか？**  
A: いいえ。キャンバスサイズはページ寸法を制御しますが、ベクターデータは解像度に依存せず、任意のズームレベルで鮮明にレンダリングされます。

**Q: TIFF 出力の DPI を別に設定できますか？**  
A: はい。`TiffOptions` を作成する前に `rasterizationOptions.setResolution(dpiValue)` を調整してください。

**Q: CAD を再ラスタライズせずに既存の PDF の寸法を変更するには？**  
A: Aspose.PDF を使用して生成された PDF を読み込み、`pdf.getPages().setPageSize(PageSize.A4)` またはカスタムサイズを呼び出すことで変更できます。

**Q: レイヤーを保持しながら DXF を PDF に変換する最適な方法は？**  
A: `setAutomaticLayoutsScaling(true)` を保持し、`setNoScaling(true)` を使用しないことで、レイヤーの可視性とレイアウトの忠実度が保たれます。

## 結論

おめでとうございます！**CADをPDFに変換**し、**CADをTIFFにエクスポート**しながら、**Javaでキャンバスサイズを設定**し、**自動レイアウトスケーリング** を有効にし、**キャンバスモードの構成** 方法を習得しました。このチュートリアルは CAD 変換プロジェクトの堅実な基盤を提供します。さらに多くの機能や可能性は [Aspose.CAD documentation](https://reference.aspose.com/cad/java/) でご確認ください。

**Last Updated:** 2026-08-29  
**Tested with:** Aspose.CAD for Java 24.12  
**Author:** Aspose

## 関連チュートリアル

- [キャンバスサイズの設定 – Aspose.CAD for Java の高度な CAD 機能](/cad/java/advanced-cad-features/)
- [Java で DWG を PDF にエクスポート – Aspose.CAD で PDF ページサイズを設定](/cad/java/cad-export-options/export-to-pdf/)
- [カスタムページサイズの設定 – 自動レイアウトスケーリング付き CAD から PDF](/cad/java/advanced-cad-features/setting-auto-layout-scaling/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}