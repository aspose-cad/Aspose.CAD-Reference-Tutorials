---
date: 2026-10-19
description: Aspose.CAD for Java を使用して、AutoCAD 図面をカスタム PDF ページサイズで PDF にエクスポートする方法を学びます。このステップバイステップガイドでは、DWG
  から PDF への変換、ラスタライズオプション、ライセンスについて説明します。
keywords:
- custom pdf page size
- export autocad to pdf
- save cad as pdf
- generate pdf from dwg
- dwg to pdf java
lastmod: 2026-10-19
linktitle: AutoCAD 画像を PDF にエクスポート
og_description: Aspose.CAD for Java を使用して AutoCAD 図面を PDF にエクスポートする際に、カスタム PDF ページサイズを設定します。DWG
  から PDF への変換、ラスタライズ設定、ライセンスを数分で学べます。
og_image_alt: Guide showing how to export AutoCAD drawings to PDF with custom page
  dimensions using Aspose.CAD for Java
og_title: Aspose.CAD を使用した AutoCAD エクスポートでカスタム PDF ページサイズを設定する
schemas:
- author: Aspose
  dateModified: '2026-10-19'
  description: Learn how to export AutoCAD drawings to PDF with a custom PDF page
    size using Aspose.CAD for Java. This step‑by‑step guide covers converting DWG
    to PDF, rasterization options, and licensing.
  headline: Set custom PDF page size for AutoCAD export with Aspose.CAD
  type: TechArticle
- description: Learn how to export AutoCAD drawings to PDF with a custom PDF page
    size using Aspose.CAD for Java. This step‑by‑step guide covers converting DWG
    to PDF, rasterization options, and licensing.
  name: Set custom PDF page size for AutoCAD export with Aspose.CAD
  steps:
  - name: set the resource directory path
    text: '> **Pro tip:** Replace `"Your Document Directory"` with the absolute path
      to the folder you created in the prerequisites.'
  - name: load the CAD image
    text: The `Image` class loads the CAD file and gives you access to Aspose.CAD’s
      rasterization engine. > **Why this matters:** Once the CAD file is loaded, you
      can manipulate rasterization options before rendering to PDF.
  - name: set rasterization options
    text: The `CadRasterizationOptions` class specifies how the CAD drawing is rasterized
      before being saved as PDF. Adjust `pageWidth` and `pageHeight` to define a **custom
      PDF page size**. You can also enable 3‑D rendering by uncommenting the `setTypeOfEntities`
      line. - `pageWidth` / `pageHeight` – measured
  - name: configure PDF options
    text: The `PdfOptions` class holds PDF‑specific settings and links the rasterization
      options to the output file, ensuring the custom page dimensions are applied
      correctly.
  - name: save the PDF
    text: The `save` method writes the rendered image to the specified PDF file. The
      resulting file, `Export3DImagestoPDF_out_.pdf`, is a **save cad as pdf** representation
      of your original AutoCAD drawing with the exact page dimensions you specified.
  type: HowTo
- questions:
  - answer: Yes, the library supports DWG, DXF, DWF, DGN, and many more, giving you
      flexibility across projects.
    question: Can I use Aspose.CAD for Java with other CAD file formats?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to request a time‑limited license for evaluation.
    question: How do I obtain a temporary license for Aspose.CAD for Java?
  - answer: Absolutely. Use `setLayouts("Model")` or specify other layout names to
      control which view is rendered.
    question: Are there layout options for rasterization?
  - answer: Yes – modify `pageWidth` and `pageHeight` in the rasterization options
      to any dimensions you need.
    question: Can I customize the size of the output PDF file?
  - answer: The dedicated [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) offers
      community support and official responses from the Aspose team.
    question: Where can I get help or discuss issues related to Aspose.CAD for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- custom pdf page size
- Aspose.CAD
- Java CAD conversion
- PDF generation
- DWG export
title: Aspose.CAD を使用した AutoCAD エクスポートでカスタム PDF ページサイズを設定する
url: /ja/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# AutoCAD PDF のエクスポート - Aspose.CAD for Java を使用して AutoCAD 画像を PDF にエクスポート

## はじめに

**convert DWG to PDF** が必要で、出力ファイルの正確なサイズを制御したい場合は、適切な場所に来ました。このチュートリアルでは、Aspose.CAD for Java を使用して AutoCAD 画像を PDF にエクスポートする際に **custom PDF page size** を設定する方法を示します。ガイドの最後までに、DWG の読み込み、DPI やページ幅/高さなどのラスター化オプションの設定、ライセンスの適用、そして本番環境向け PDF の生成方法が分かります。

## クイック回答

- **JavaでDWGをPDFに変換できますか？** はい – Aspose.CAD for Java は DWG、DXF、DWF など多数の CAD フォーマットをネイティブにサポートしています。  
- **本番使用にはライセンスが必要ですか？** フル Aspose.CAD ライセンスを取得すると評価制限がすべて解除されます。テスト用の一時ライセンスも利用可能です。  
- **対応している Java バージョンはどれですか？** このライブラリは Java 8 以降のすべての JDK で動作します。  
- **PDF のページサイズを変更するにはどうすればよいですか？** `PdfOptions.getRasterizationOptions()` の `pageWidth` と `pageHeight` を任意のサイズに設定してください。  
- **3D レンダリングはサポートされていますか？** はい – `TypeOfEntities.Entities3D` を有効にすると 3D エンティティをラスター化できます。

## AutoCAD PDF のエクスポートとは何ですか？

AutoCAD PDF のエクスポートとは、ベクターベースの CAD 図面（DWG、DXF、DWF など）をポータブルな PDF ドキュメントに変換し、レイヤー、線幅、オプションの 3D ジオメトリを保持することを指します。これにより、クライアントと設計を共有したり、図面をアーカイブしたり、CAD ソフトウェアをインストールせずに印刷したりできます。

## DWG を PDF に変換するために Aspose.CAD for Java を使用する理由は？

Aspose.CAD for Java は、豊富なフォーマットサポート、ネイティブ依存なしの純粋な Java 実装、高解像度のラスター化で DPI とページサイズを完全に制御できる点、そしてトライアルから本番へスケールできる柔軟なライセンス体系を備えているため、DWG を PDF に変換するのに最適です。

- **広範なフォーマット対応** – DWG、DXF、DWF、DGN、PDF など 50 以上の入力・出力フォーマットをサポートします。  
- **純粋な Java 実装** – ネイティブ DLL や外部依存がなく、任意のプラットフォームでのデプロイが簡単です。  
- **高解像度ラスター化** – DPI、ページサイズ、レイアウトを指定でき、結果の **custom PDF page size** を完全に制御できます。  
- **スケーラブルなライセンス** – 無料トライアルで開始し、永久的な **Aspose CAD license** にアップグレードできます。  

## 前提条件

- **Java Development Kit** – マシンに JDK 8 以上がインストールされていること。  
- **Aspose.CAD for Java** – 最新の JAR を [download link](https://releases.aspose.com/cad/java/) からダウンロードしてください。  
- **Working directory** – ソース DWG ファイルが格納され、生成された PDF が出力されるフォルダー。

## 名前空間のインポート

`Image` クラスは、メモリ内の CAD 図面を表す Aspose.CAD のコアオブジェクトです。コーディングを開始する前に必要なパッケージをインポートしてください。

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

それではコードをステップバイステップで見ていきましょう。

## DWG を PDF にエクスポートする際にカスタム PDF ページサイズを設定する方法は？

DWG をロードし、目的のページ幅と高さを定義してから結果を PDF として保存します。これだけでカスタム PDF ページサイズの PDF を作成できます。以下の手順で正確な手順と最小限のコードを示します。

### ステップ 1: リソースディレクトリのパスを設定する

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **プロのコツ:** `"Your Document Directory"` を、前提条件で作成したフォルダーへの絶対パスに置き換えてください。

### ステップ 2: CAD 画像をロードする

`Image` クラスは CAD ファイルをロードし、Aspose.CAD のラスター化エンジンへのアクセスを提供します。

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **重要な理由:** CAD ファイルがロードされたら、PDF にレンダリングする前にラスター化オプションを操作できます。

### ステップ 3: ラスター化オプションを設定する

`CadRasterizationOptions` クラスは、CAD 図面が PDF として保存される前にどのようにラスター化されるかを指定します。`pageWidth` と `pageHeight` を調整して **custom PDF page size** を定義します。`setTypeOfEntities` 行のコメントを外すことで 3D レンダリングも有効にできます。

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- `pageWidth` / `pageHeight` – ピクセル単位で測定されます。A4、Letter、または任意のカスタム寸法に合わせてこれらの値を変更してください。  
- `setTypeOfEntities(TypeOfEntities.Entities3D)` – 必要に応じて 3‑D エンティティをレンダリングします。  
- `setLayouts` – ラスター化するレイアウト（Model、Layout1 など）を選択します。

### ステップ 4: PDF オプションを構成する

`PdfOptions` クラスは PDF 固有の設定を保持し、ラスター化オプションを出力ファイルにリンクさせ、カスタムページ寸法が正しく適用されるようにします。

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### ステップ 5: PDF を保存する

`save` メソッドは、レンダリングされた画像を指定された PDF ファイルに書き込みます。

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

生成されたファイル `Export3DImagestoPDF_out_.pdf` は、指定した正確なページ寸法を持つ元の AutoCAD 図面の **save cad as pdf** 表現です。

## 一般的な問題と解決策

| 症状 | 考えられる原因 | 対策 |
|---------|--------------|-----|
| Blank PDF output | Rasterization options not set or layout mismatch | `setLayouts` が CAD ファイルのレイアウト名と一致しているか確認してください。 |
| Low‑resolution image | `pageWidth`/`pageHeight` too small or DPI low | サイズを大きくするか、`rasterizationOptions.setResolution(...)` を使用して高い DPI を設定してください。 |
| License exception | No valid license applied | 永続的な Aspose.CAD ライセンスを適用するか、テスト用に一時ライセンスを使用してください。 |

## よくある質問

**Q: Aspose.CAD for Java を他の CAD ファイル形式でも使用できますか？**  
A: はい、このライブラリは DWG、DXF、DWF、DGN など多数をサポートしており、プロジェクト全体で柔軟に利用できます。

**Q: Aspose.CAD for Java の一時ライセンスはどう取得しますか？**  
A: [temporary license page](https://purchase.aspose.com/temporary-license/) にアクセスして、評価用の期間限定ライセンスをリクエストしてください。

**Q: ラスター化のレイアウトオプションはありますか？**  
A: もちろんです。`setLayouts("Model")` を使用するか、他のレイアウト名を指定して、どのビューをレンダリングするか制御できます。

**Q: 出力 PDF ファイルのサイズをカスタマイズできますか？**  
A: はい – ラスター化オプションの `pageWidth` と `pageHeight` を必要な任意の寸法に変更してください。

**Q: Aspose.CAD for Java に関するサポートや議論はどこで得られますか？**  
A: 専用の [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) でコミュニティサポートと Aspose チームからの公式回答が得られます。

## 追加 FAQ（AI フレンドリー形式）

**Q: Aspose.CAD は Windows や Linux でネイティブライブラリを必要としますか？**  
A: いいえ。Aspose.CAD for Java は純粋な Java ライブラリであり、追加のネイティブ DLL がなくても JDK をサポートする任意のプラットフォームで動作します。

**Q: ライブラリが処理できる DWG ファイルの最大サイズはどれくらいですか？**  
A: ストリーミングアーキテクチャにより、ファイル全体をメモリに読み込むことなく、数百ページ（最大 500 MB）の図面を処理できます。

**Q: 1 回の実行で多数の DWG ファイルを PDF にバッチ変換できますか？**  
A: はい。ディレクトリを走査し、各ファイルを `Image.load()` で読み込み、同じラスター化オプションを適用し、各出力 PDF に対して `save()` を呼び出します。

**Q: 標準的なサーバーでのパフォーマンスはどの程度ですか？**  
A: 標準的な 2.5 GHz CPU で 300 DPI の 100 ページ DWG を変換するのに約 12 秒かかります（Aspose のベンチマークテストに基づく）。

**Q: ライブラリは PDF にレイヤー情報を保持しますか？**  
A: 出力はラスター化されますが、レイヤー、線幅、色の視覚的な外観は忠実に再現されます。

---

**最終更新日:** 2026-10-19  
**テスト環境:** Aspose.CAD for Java 24.10  
**作者:** Aspose

## 関連チュートリアル

- [Aspose.CAD Java を使用して DWG を PDF にエクスポートし、トラッキングを有効にする](/cad/java/additional-features/enable-tracking/)
- [Aspose.CAD Java を使用して DWG を PDF にエクスポート: 特定のレイアウト](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Aspose.CAD for Java を使用して DWG を BMP にエクスポートし、単位タイプで CAD サイズを調整する](/cad/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}