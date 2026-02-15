---
date: 2026-02-15
description: Aspose.CAD for Java を使用して、PDF のページサイズ設定や CAD の PDF 変換、レイアウトの自動スケーリング、TIFF
  エクスポートの方法を学びましょう。
linktitle: Set PDF Page Size – Convert CAD to PDF
second_title: Aspose.CAD Java API
title: PDFページサイズを設定 – CADをPDFに変換（Java）
url: /ja/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# キャンバスサイズとモードの設定

## はじめに

CAD 図面を PDF に変換する際に **PDF ページサイズを設定** したい場合は、ここが最適です。このチュートリアルでは、Aspose.CAD for Java を使用して正確なキャンバス寸法を定義し、 自動レイアウトスケーリングを有効にしたうえで、結果を PDF と TIFF の両方にエクスポートする方法を示します。印刷用のエンジニアリング図面を作成する場合でも、ウェブギャラリー用のサムネイルを生成する場合でも、ページサイズと出力解像度を制御することは重要です。

## クイック回答
- **「CAD を PDF に変換する」とは何ですか？** CAD 図面（例：DXF、DWG）を任意のプラットフォームで閲覧可能な PDF ドキュメントに変換することです。  
- **TIFF へもエクスポートできますか？** はい — `TiffOptions` を使用して高解像度ラスタ画像を作成できます。  
- **Java でキャンバスサイズを制御するオプションはどれですか？** `CadRasterizationOptions.setPageWidth/Height`。  
- **自動レイアウトスケーリングとは何ですか？** キャンバスサイズが変わったときに元のレイアウト比率を保持するフラグ（`setAutomaticLayoutsScaling(true)`）。  
- **Aspose.CAD のライセンスは必要ですか？** 本番環境で使用する場合は、一時ライセンスまたは永続ライセンスが必要です。

## CAD を PDF に変換する際の PDF ページサイズ設定方法（Java）

PDF ページサイズ（またはキャンバスサイズ）を設定すると、文書の最終寸法を指定でき、印刷規格や UI 要件に合わせて **PDF の寸法を変更** する必要がある場合に特に有用です。以下では、各コード行の *理由* を説明しながら手順を追って解説します。

## **CAD を PDF に変換** とは？

CAD を PDF に変換するとは、ベクターベースのエンジニアリング図面を PDF ページとしてレンダリングし、線画・レイヤー・ジオメトリを保持しつつ、ファイルを汎用的にアクセス可能にすることを指します。

## **java** でキャンバスサイズを設定する理由

Java でキャンバスサイズを設定すると、出力解像度とページ寸法を定義でき、生成される PDF または TIFF が印刷や表示の要件に合致します。また、スケーリング動作を制御できるため、大判図面において重要です。

## 前提条件

チュートリアルに入る前に、以下の前提条件が整っていることを確認してください。

- Aspose.CAD for Java: Java 環境に Aspose.CAD ライブラリがインストールされていること。ダウンロードは [here](https://releases.aspose.com/cad/java/) から可能です。  
- ドキュメントディレクトリ: CAD ファイルを格納するディレクトリを用意し、チュートリアルの手順で参照できるようにします。

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

## 手順 1: Aspose.CAD クラスのインポート

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

このスニペットでは、リソースディレクトリへのパスを設定し、Aspose.CAD の `Image` クラスを使用して DXF ファイルを読み込みます。

## 手順 2: **CadRasterizationOptions** プロパティの設定（java でキャンバスサイズを設定）

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

ここでは `CadRasterizationOptions` のインスタンスを作成し、ページ幅、ページ高さ、そして **自動レイアウトスケーリング** などのプロパティを構成します。これが変換時の **キャンバスモードの設定** の核心です。

## 手順 3: PdfOptions の作成と VectorRasterizationOptions の設定

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

次に `PdfOptions` インスタンスを作成し、その `VectorRasterizationOptions` プロパティに先ほど構成した `CadRasterizationOptions` を設定します。

## 手順 4: PDF へのエクスポート（CAD を PDF に変換）

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

最後に、指定したオプションを使用して CAD 画像を PDF ファイルとして保存し、**CAD を PDF に変換** プロセスを完了します。

## 手順 5: TiffOptions の作成と VectorRasterizationOptions の設定（CAD を TIFF にエクスポート）

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

このステップでは `TiffOptions` インスタンスを作成し、その `VectorRasterizationOptions` プロパティを構成します。

## 手順 6: TIFF へのエクスポート

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

最後に、指定したオプションを使用して CAD 画像を TIFF ファイルとして保存し、キャンバスサイズを設定した後の **CAD を TIFF にエクスポート** を実演します。

## よくある問題と解決策

| 問題 | 原因 | 対策 |
|------|------|------|
| 出力 PDF が空白になる | `setNoScaling(true)` が一部の図面で描画を無効化 | `setNoScaling(true)` を削除するか `false` に設定 |
| TIFF の解像度が低い | ページ幅/高さが小さすぎる | `setPageWidth` / `setPageHeight` の値を増やす |
| レイアウトが歪む | 自動レイアウトスケーリングが無効 | `setAutomaticLayoutsScaling(true)` が有効になっていることを確認 |

## キャンバスサイズと DPI を調整する理由

キャンバスサイズを変更すると、出力のラスタライズ解像度に直接影響します。**TIFF の解像度を上げたい** 場合は、`setPageWidth` / `setPageHeight` の値を上げるか、`TiffOptions` を作成する前に `rasterizationOptions.setResolution(300)` を呼び出してください。これにより、印刷や詳細検査に適した高品質ラスタ画像が得られます。

## FAQ（よくある質問）

### Q1: Aspose.CAD for Java を他の Java フレームワークと併用できますか？

A1: はい、Aspose.CAD はさまざまな Java フレームワークとシームレスに統合できるよう設計されています。

### Q2: Aspose.CAD の一時ライセンスは入手可能ですか？

A2: はい、[here](https://purchase.aspose.com/temporary-license/) から取得できます。

### Q3: Aspose.CAD のコミュニティサポートはどこで得られますか？

A3: コミュニティサポートやディスカッションは [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) で行われています。

### Q4: Aspose.CAD を無料で試せますか？

A4: もちろんです！[here](https://releases.aspose.com/) から無料トライアルを入手してください。

### Q5: Aspose.CAD for Java の購入方法を教えてください。

A5: 製品は [here](https://purchase.aspose.com/buy) から購入できます。

**追加 Q&A**

**Q: キャンバスサイズは PDF のベクタ品質に影響しますか？**  
A: いいえ。キャンバスサイズはページ寸法を制御しますが、ベクタデータは解像度に依存せず、任意のズームレベルで鮮明に表示されます。

**Q: TIFF 出力の DPI を別途設定できますか？**  
A: はい。`TiffOptions` を作成する前に `rasterizationOptions.setResolution(dpiValue)` を調整してください。

**Q: 既存の PDF の **PDF の寸法を変更** したいが、CAD を再レンダリングしたくない場合は？**  
A: Aspose.PDF を使用して生成済み PDF を読み込み、`pdf.getPages().setPageSize(PageSize.A4)` またはカスタムサイズを指定します。

**Q: **DXF を PDF に変換** する際にレイヤーを保持する最適な方法は？**  
A: `setAutomaticLayoutsScaling(true)` を保持し、`setNoScaling(true)` を避けることでレイヤーの可視性とレイアウトの忠実度が保たれます。

## 結論

おめでとうございます！**CAD を PDF に変換**し、**CAD を TIFF にエクスポート**しながら、**java でキャンバスサイズを設定**し、**自動レイアウトスケーリング**を有効にし、**キャンバスモードの設定**方法を習得しました。このチュートリアルは CAD 変換プロジェクトの堅実な基盤を提供します。さらに詳しい機能や活用例は [Aspose.CAD documentation](https://reference.aspose.com/cad/java/) をご覧ください。

---

**最終更新日:** 2026-02-15  
**テスト環境:** Aspose.CAD for Java 24.12  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}