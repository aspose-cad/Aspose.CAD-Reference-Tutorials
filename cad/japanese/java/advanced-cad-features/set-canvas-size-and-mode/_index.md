---
date: 2025-12-10
description: Aspose.CAD for Java を使用して CAD を PDF に変換し、キャンバスサイズの設定、自動レイアウトスケーリング、TIFF
  へのエクスポート方法を学びましょう。
linktitle: Convert CAD to PDF – Set Canvas Size & Mode
second_title: Aspose.CAD Java API
title: CADをPDFに変換 – キャンバスサイズとモードを設定 (Java)
url: /ja/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# キャンバスサイズとモードの設定

## はじめに

**CAD を PDF に変換**しながら、キャンバスサイズとレンダリングモードを完全にコントロールしたいですか？本ガイドでは、Java でキャンバスサイズを設定し、自動レイアウトスケーリングを有効にしたうえで、Aspose.CAD を使用して PDF と TIFF の両方にエクスポートする手順を詳しく解説します。プロダクションパイプラインの最適化やプロトタイプの実験に、明確で実践的な手順をご提供します。

## クイック回答
- **「CAD を PDF に変換」とは何ですか？** CAD 図面（DXF、DWG など）を任意のプラットフォームで閲覧可能な PDF ドキュメントに変換することです。  
- **TIFF へのエクスポートもできますか？** はい — `TiffOptions` を使用して高解像度ラスタ画像を作成できます。  
- **Java でキャンバスサイズを制御するオプションはどれですか？** `CadRasterizationOptions.setPageWidth/Height`。  
- **自動レイアウトスケーリングとは？** キャンバスサイズが変わったときに元のレイアウト比率を保持するフラグ（`setAutomaticLayoutsScaling(true)`）。  
- **Aspose.CAD のライセンスは必要ですか？** 本番環境で使用する場合は、一時ライセンスまたは永続ライセンスが必要です。

## **convert CAD to PDF** とは？

CAD を PDF に変換するとは、ベクターベースのエンジニアリング図面を PDF ページとしてレンダリングし、線画・レイヤー・ジオメトリを保持しつつ、ファイルを汎用的にアクセス可能にすることを指します。

## **java** でキャンバスサイズを設定する理由

Java でキャンバスサイズを設定すると、出力解像度とページ寸法を明示的に指定でき、生成される PDF や TIFF が印刷やディスプレイ要件に合致します。また、スケーリング動作を制御できるため、大判図面の取り扱いに必須です。

## 前提条件

チュートリアルに入る前に、以下の前提条件が整っていることを確認してください。

- Aspose.CAD for Java: Java 環境に Aspose.CAD ライブラリがインストールされていること。ダウンロードは [here](https://releases.aspose.com/cad/java/) から可能です。  
- ドキュメントディレクトリ: CAD ファイルを格納するディレクトリを作成し、チュートリアル手順で参照できるようにしてください。

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

ここでは `CadRasterizationOptions` のインスタンスを作成し、ページ幅、ページ高さ、**自動レイアウトスケーリング** などのプロパティを構成します。これが **キャンバスモードの設定** の中心です。

## 手順 3: PdfOptions の作成と VectorRasterizationOptions の設定

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

次に `PdfOptions` インスタンスを作成し、その `VectorRasterizationOptions` プロパティに先ほど構成した `CadRasterizationOptions` を設定します。

## 手順 4: PDF へのエクスポート（convert cad to pdf）

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

指定したオプションを使用して CAD 画像を PDF ファイルとして保存し、**convert CAD to PDF** プロセスを完了します。

## 手順 5: TiffOptions の作成と VectorRasterizationOptions の設定（export cad to tiff）

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

このステップでは `TiffOptions` インスタンスを作成し、その `VectorRasterizationOptions` プロパティを設定します。

## 手順 6: TIFF へのエクスポート

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

指定したオプションを使用して CAD 画像を TIFF ファイルとして保存し、キャンバスサイズを構成した後の **export CAD to TIFF** を実演します。

## よくある問題と解決策

| 問題 | 原因 | 対策 |
|------|------|------|
| 出力 PDF が空白になる | `setNoScaling(true)` が一部の図面で描画を無効化 | `setNoScaling(true)` を削除するか、`false` に設定 |
| TIFF の解像度が低く見える | ページ幅/高さが小さすぎる | `setPageWidth` / `setPageHeight` の値を増やす |
| レイアウトが歪む | 自動レイアウトスケーリングが無効 | `setAutomaticLayoutsScaling(true)` が有効か確認 |

## 結論

おめでとうございます！**convert CAD to PDF** と **export CAD to TIFF** を **java でキャンバスサイズを設定** し、**自動レイアウトスケーリング** を有効にしたうえで、**キャンバスモードの設定** 方法を習得しました。このチュートリアルは CAD 変換プロジェクトの堅実な基盤となります。さらに詳しい機能や活用例は [Aspose.CAD ドキュメント](https://reference.aspose.com/cad/java/) をご覧ください。

## FAQ

### Q1: Aspose.CAD for Java を他の Java フレームワークと併用できますか？

A1: はい、Aspose.CAD はさまざまな Java フレームワークとシームレスに統合できるよう設計されています。

### Q2: Aspose.CAD の一時ライセンスは入手可能ですか？

A2: はい、[here](https://purchase.aspose.com/temporary-license/) から取得できます。

### Q3: Aspose.CAD のコミュニティサポートはどこで得られますか？

A3: コミュニティサポートやディスカッションは [Aspose.CAD フォーラム](https://forum.aspose.com/c/cad/19) でご利用ください。

### Q4: Aspose.CAD を無料で試せますか？

A4: もちろんです！[here](https://releases.aspose.com/) から無料トライアルをご利用いただけます。

### Q5: Aspose.CAD for Java の購入方法を教えてください。

A5: 製品は [here](https://purchase.aspose.com/buy) から購入できます。

**追加 Q&A**

**Q: キャンバスサイズは PDF のベクタ品質に影響しますか？**  
A: いいえ。キャンバスサイズはページ寸法を決定しますが、ベクタデータは解像度に依存せず、任意のズームレベルで鮮明に描画されます。

**Q: TIFF 出力時に別の DPI を設定できますか？**  
A: はい。`TiffOptions` を作成する前に `rasterizationOptions.setResolution(dpiValue)` で DPI を調整してください。

---

**最終更新日:** 2025-12-10  
**テスト環境:** Aspose.CAD for Java 24.12  
**作成者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}