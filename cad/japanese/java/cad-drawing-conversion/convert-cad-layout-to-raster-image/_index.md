---
date: 2026-10-04
description: Aspose.CAD for Java を使用して DWG を PNG にすばやく変換し、CAD を PNG やその他のラスタ形式でエクスポートする方法を学びます。高品質な結果を迅速に得られます。
keywords:
- convert dwg to png
- dwg to raster image
- convert cad to pdf
- export cad as png
- convert dwg to jpeg
lastmod: 2026-10-04
linktitle: CAD レイアウトをラスタ画像形式に変換する
og_description: Aspose.CAD for Java で DWG を PNG にすばやく変換します。ステップバイステップで CAD を PNG、JPEG、TIFF
  などにエクスポートする方法を学びます。
og_image_alt: 'Developer guide: Convert DWG to PNG and other raster formats using
  Aspose.CAD for Java'
og_title: Aspose.CAD for Java を使用して DWG を PNG やその他のラスタ形式に変換する
schemas:
- author: Aspose
  dateModified: '2026-10-04'
  description: Learn how to quickly convert dwg to png and export cad as png or other
    raster formats using Aspose.CAD for Java. Get high‑quality results fast.
  headline: Convert DWG to PNG and other raster formats using Aspose.CAD for Java
  type: TechArticle
- description: Learn how to quickly convert dwg to png and export cad as png or other
    raster formats using Aspose.CAD for Java. Get high‑quality results fast.
  name: Convert DWG to PNG and other raster formats using Aspose.CAD for Java
  steps:
  - name: set up the resource directory
    text: Replace `"Your Document Directory"` with the absolute path where your CAD
      files reside. This directory will be used for both input and output files.
  - name: load the CAD file
    text: '`Image.load` parses the source file and creates an in‑memory representation
      that you can rasterize. You can load any supported format (DWG, DXF, DGN, etc.)
      – this is the **how to convert cad** part.'
  - name: configure rasterization options
    text: '`CadRasterizationOptions` defines how the vector data is turned into pixels.
      `setPageWidth` and `setPageHeight` control output resolution (larger values
      = higher DPI). `setLayouts` lets you **convert CAD to raster** for specific
      layouts; omit it to rasterize the whole drawing.'
  - name: set image options
    text: '`TiffOptions` (or `PngOptions` for PNG) tells Aspose which raster format
      to generate and lets you fine‑tune compression, color depth, and other format‑specific
      settings. Choose the options class that matches your desired output.'
  - name: save the resultant image
    text: Call `save` on the `Image` instance, passing the output file name and the
      options object. Change the file extension to `.png` (and use `PngOptions`) to
      **save CAD as PNG**. The same pattern works for JPEG, BMP, or PDF. > **Common
      pitfall:** Forgetting to match the file extension with the options cla
  type: HowTo
- questions:
  - answer: Yes, it supports over 30 CAD and raster formats, including DWG, DXF, DGN,
      and SVG.
    question: Is Aspose.CAD compatible with different CAD file formats?
  - answer: Absolutely. Adjust `setPageWidth`, `setPageHeight`, or `setResolution`
      in `CadRasterizationOptions` to achieve the desired DPI.
    question: Can I customize the resolution of the output raster image?
  - answer: Provide an array with all layout names to `setLayouts`, e.g., `new String[]{"Model","Layout1","Layout2"}`.
    question: How can I convert multiple CAD layouts in a single run?
  - answer: Yes—PNG, JPEG, BMP, PDF, and more are available via their respective `*Options`
      classes.
    question: Are there output formats besides TIFF supported?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community
      support and official assistance.
    question: Where can I get help or share my experience with Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- convert dwg
- Aspose.CAD
- Java raster conversion
- CAD image processing
title: Aspose.CAD for Java を使用して DWG を PNG やその他のラスタ形式に変換する
url: /ja/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java を使用した DWG から PNG およびその他のラスター形式への変換

## はじめに

`Aspose.CAD for Java` は、CAD ファイルを PNG、JPEG、TIFF などのラスター画像にプログラムで変換できるライブラリです。DWG を PNG（または他のラスター画像形式）に変換することは、CAD ビューアを持たないチームメンバーと図面を共有したり、ドキュメントにデザインを埋め込んだり、ウェブギャラリー用のサムネイルを生成したりする際に一般的な要件です。このガイドでは、全体の図面ファイルでも特定のレイアウトだけでも、DWG を PNG に迅速かつ確実に変換する方法を学びます。また、ウェブプレビュー、レポートツール、モバイルアプリ向けに **CAD をラスターに変換** する必要がある場合もあります。

## クイック回答

- **DWG から PNG を処理するライブラリは何ですか？** Aspose.CAD for Java が変換エンジンを提供します。  
- **エクスポートできるラスター形式は何ですか？** PNG、JPEG、TIFF、PDF、BMP など、30 以上の追加形式があります。  
- **テストにライセンスは必要ですか？** 開発には無料トライアルで動作しますが、本番環境では商用ライセンスが必要です。  
- **特定のレイアウトを選択できますか？** はい – `setLayouts` を使用して “Model”、 “Layout1” などを対象にできます。  
- **高解像度の出力は可能ですか？** もちろんです – `setPageWidth` と `setPageHeight`（または `setResolution`）を調整して DPI を制御します。

## 「convert dwg to png」とは何ですか？

「convert dwg to png」とは、DWG のベクタードローイングをピクセルベースの PNG 画像に変換し、標準的な画像ビューアで表示できるようにすることを指します。このプロセスはベクターエンティティをラスター化し、線幅、色、レイヤーを保持しつつ、固定解像度のビットマップに変換します。結果は PDF、Word 文書、ベクターサポートが限定的なウェブページへの埋め込みに最適です。

## なぜ CAD を PNG（または他のラスター形式）でエクスポートするのか？

CAD を PNG としてエクスポートすると、あらゆる主要プラットフォームでの汎用性、速いロード、簡単な埋め込みが実現します。ラスター画像は重い DWG ファイルを開くよりも瞬時に読み込め、PNG のロスレス圧縮により視覚的忠実度が保たれます。解像度、背景色、レイアウトを制御することで、デスクトップ、モバイルデバイス、ブラウザ上のどこで閲覧しても、すべてのステークホルダーが同じ外観を確認できます。

## 一般的な使用例

| シナリオ | ラスター出力が有効な理由 |
|----------|------------------------|
| **プロジェクトドキュメント** | PDF や Word 文書に PNG を埋め込むことで、レビュー担当者が CAD ソフトを必要としなくなります。 |
| **ウェブポータル** | DWG ファイルから生成されたサムネイルは即座にロードされ、ユーザーエクスペリエンスが向上します。 |
| **モバイルアプリ** | ラスター画像は CAD ビューアを持たないデバイスでも正しく表示されます。 |
| **自動レポート** | 複数のレイアウトをバッチで PNG/JPEG に変換し、チャートやダッシュボードに組み込めます。 |

## 前提条件

1. **Java 開発環境** – JDK 8 以上がインストールされ、設定されていること。  
2. **Aspose.CAD for Java** – 最新の JAR を [Aspose.CAD for Java documentation](https://reference.aspose.com/cad/java/) からダウンロードしてください。  

## 名前空間のインポート

`com.aspose.cad.Image` はメモリ内で任意の CAD ファイルを表すコアクラスです。`com.aspose.cad.imageoptions.*` は各ラスター形式用のオプションオブジェクトを提供します。図面の読み込み、ラスタライズ設定、出力保存に必要なクラスをインポートします。

> **Pro tip:** TIFF の代わりに PNG で **CAD を PNG にエクスポート** したい場合は、`TiffOptions` を `com.aspose.cad.imageoptions.PngOptions` に置き換えてください。

## ステップバイステップガイド

### 手順 1: リソースディレクトリの設定

`"Your Document Directory"` を CAD ファイルが格納されている絶対パスに置き換えてください。このディレクトリは入力ファイルと出力ファイルの両方に使用されます。

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

### 手順 2: CAD ファイルの読み込み

`Image.load` はソースファイルを解析し、メモリ内表現を作成します。これによりラスタライズが可能になります。DWG、DXF、DGN など、サポートされている任意の形式を読み込めます – これが **CAD を変換する方法** の部分です。

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
```

### 手順 3: ラスタライズオプションの設定

`CadRasterizationOptions` はベクターデータをピクセルに変換する方法を定義します。`setPageWidth` と `setPageHeight` は出力解像度を制御します（数値が大きいほど DPI が高くなります）。`setLayouts` を使用すると、特定のレイアウトだけを **CAD をラスターに変換** できます。省略すると全体の図面がラスタライズされます。

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### 手順 4: 画像オプションの設定

`TiffOptions`（PNG で出力する場合は `PngOptions`）は Aspose に生成するラスター形式を指示し、圧縮、色深度、その他フォーマット固有の設定を細かく調整できます。目的の出力に合わせたオプションクラスを選択してください。

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
rasterizationOptions.setLayouts(new String[] {"Model", "Layout1"});
```

### 手順 5: 結果画像の保存

`Image` インスタンスの `save` を呼び出し、出力ファイル名とオプションオブジェクトを渡します。拡張子を `.png` に変更し（`PngOptions` を使用）、**CAD を PNG に保存** します。同様のパターンで JPEG、BMP、PDF も生成可能です。

```java
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.setVectorRasterizationOptions(rasterizationOptions);
```

> **Common pitfall:** ファイル拡張子とオプションクラスが一致していないと `UnsupportedFormatException` が発生します。常に一致させてください。

## よくある問題と解決策

| 問題 | 解決策 |
|-------|----------|
| **空白の出力画像** | `setLayouts` に指定したレイアウト名がソース CAD ファイルと完全に一致しているか確認してください。 |
| **低解像度 PNG** | `setPageWidth` / `setPageHeight` を増やすか、ラスタライズオプションの `setResolution` を設定してください。 |
| **サポートされていない DWG バージョン** | 最新の Aspose.CAD バージョンを使用してください。古いリリースでは新しい DWG に対応していない場合があります。 |
| **大容量ファイルでのメモリエラー** | ページごとに処理するか、JVM ヒープサイズを増やします（例: `-Xmx2g`）。 |

## よくある質問

**Q: Aspose.CAD はさまざまな CAD ファイル形式に対応していますか？**  
A: はい、DWG、DXF、DGN、SVG など、30 以上の CAD およびラスター形式をサポートしています。

**Q: 出力ラスター画像の解像度をカスタマイズできますか？**  
A: もちろんです。`CadRasterizationOptions` の `setPageWidth`、`setPageHeight`、または `setResolution` を調整して希望の DPI を実現できます。

**Q: 1 回の実行で複数の CAD レイアウトを変換するには？**  
A: `setLayouts` にすべてのレイアウト名を配列で渡します。例: `new String[]{"Model","Layout1","Layout2"}`。

**Q: TIFF 以外の出力形式はありますか？**  
A: はい、PNG、JPEG、BMP、PDF など、各 `*Options` クラスを使用して利用可能です。

**Q: Aspose.CAD のサポートやコミュニティに参加するには？**  
A: [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) でコミュニティサポートや公式支援を受けられます。

## 結論

これらの手順に従うことで、**DWG を PNG に変換**、**CAD を PNG にエクスポート**、**CAD を JPEG に保存**、または必要なその他のラスター形式を生成できます。Aspose.CAD for Java が重い処理を担い、高品質な画像をアプリケーション、ドキュメント、ウェブポータルに統合することに集中できます。30 以上の形式をサポートし、数百ページに及ぶ図面でも全体をメモリに読み込まずにレンダリングできるため、エンタープライズ向け CAD ラスタライズに最適な選択肢です。

---

**最終更新日:** 2026-10-04  
**テスト環境:** Aspose.CAD for Java 24.12  
**作者:** Aspose  







```java
image.save(dataDir + "conic_pyramid_layoutstorasterimage_out_.tiff", options);
```

```bash
java -jar aspose-cad.jar -i input.dwg -o output.png -w 1200 -h 1200
```

## 関連チュートリアル

- [Aspose.CAD for Java の Java CAD ライブラリを使用して DWG を PDF またはラスターにすばやくエクスポート](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Aspose.CAD for Java で DWG を BMP に変換](/cad/java/cad-export-options/export-to-bmp/)
- [Aspose.CAD for Java を使用した特定レイアウトの DWG を PDF にエクスポート](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}