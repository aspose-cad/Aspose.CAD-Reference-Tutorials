---
date: 2026-06-04
description: Aspose.CAD for Java を使用して、CADからPDFを作成しウォーターマークを追加する方法を学びます。このステップバイステップガイドでは、CADをPDFへエクスポートし、テキストを追加し、ブランディングする方法をカバーしています。
keywords:
- create pdf from cad
- export cad to pdf
- add text cad
- watermark cad drawing
- convert dwg to pdf
linktitle: ウォーターマークを追加
schemas:
- author: Aspose
  dateModified: '2026-06-04'
  description: Learn how to create PDF from CAD and add a watermark using Aspose.CAD
    for Java. This step‑by‑step guide covers export CAD to PDF, add text CAD, and
    branding.
  headline: Create PDF from CAD with Watermark - Aspose.CAD for Java
  type: TechArticle
- description: Learn how to create PDF from CAD and add a watermark using Aspose.CAD
    for Java. This step‑by‑step guide covers export CAD to PDF, add text CAD, and
    branding.
  name: Create PDF from CAD with Watermark - Aspose.CAD for Java
  steps:
  - name: Import Packages
    text: The `com.aspose.cad` namespace provides all classes you need for CAD manipulation.
      The `Image` class is the entry point for loading and saving CAD files. The `MText`
      class represents multi‑line text that can be styled and positioned.
  - name: Add New MTEXT
    text: MText represents multi‑line text entities that can be used for watermarks.
  - name: Add Simple Entity like Text
    text: TextEntity is a single‑line text object used for simple annotations.
  - name: Export to PDF
    text: SaveFormat.Pdf specifies PDF as the output format for saving.
  type: HowTo
- questions:
  - answer: Aspose.CAD supports **DWG, DXF, DWT, DWF, and over 30 additional formats**,
      allowing you to **export cad to pdf** from virtually any source file.
    question: Is Aspose.CAD compatible with all CAD file formats?
  - answer: Yes – you can control font family, size, color, rotation, and transparency
      through the `MText` or `TextEntity` properties.
    question: Can I customize the appearance of the watermark text?
  - answer: Yes, you can download the trial version [here](https://releases.aspose.com/).
    question: Is there a trial version available for Aspose.CAD for Java?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community
      assistance and official support channels.
    question: How can I get support for Aspose.CAD?
  - answer: Refer to the [documentation](https://reference.aspose.com/cad/java/) for
      detailed API references, code samples, and best‑practice guides.
    question: Where can I find the complete documentation for Aspose.CAD for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
title: CADからPDFを作成し、ウォーターマークを追加 - Aspose.CAD for Java
url: /ja/java/other-cad-operations/add-watermark/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CADからPDFを作成し、透かしを付加 - Aspose.CAD for Java

## はじめに

このチュートリアルでは、Aspose.CAD for Java を使用して **create PDF from CAD** 図面を作成し、カスタム透かしを適用します。透かしを追加することで、知的財産を保護したり、デザインにブランドを付けたり、改訂情報を埋め込んだりできます。必要なパッケージのインポート、テキストベースの透かしの追加、最終的な CAD 図面を PDF ファイルとしてエクスポートするまでの全工程を順に説明します。最後まで読むと、任意の Java プロジェクトに組み込める再利用可能なスニペットが手に入ります。

## クイック回答
- **目的は何ですか？** CAD ファイルから PDF を作成し、数行の Java コードで透かしを重ねます。  
- **必要なライブラリはどれですか？** Aspose.CAD for Java (supports 30+ CAD formats)。  
- **テストにライセンスは必要ですか？** 30 日間の無料トライアルが利用可能です。商用利用には商用ライセンスが必要です。  
- **透かしを付けた後、CAD を PDF にエクスポートできますか？** はい。図面を保存するのと同じ API 呼び出しで PDF に変換されます。  
- **このプロセスはスレッドセーフですか？** すべての Aspose.CAD クラスは、スレッドごとに別々のインスタンスを作成すれば、同時使用できるように設計されています。

## CAD における透かしとは何ですか？

CAD の透かしは、所有権、機密性、または改訂ステータスを示すために図面上に配置される半透明のテキストまたはグラフィックのオーバーレイです。元の設計データを変更せず、主なジオメトリの背後または上に表示されるため、閲覧者は元のコンテンツを確認しながら透かしの存在を認識できます。

## **create pdf from cad** を行う際に透かしを追加する理由は？

Aspose.CAD for Java は **30+ 入力フォーマット**（DWG、DXF、DWF、DWT など）をサポートし、**500 MB** までのファイルをメモリに全文をロードせずに処理できます。PDF 変換ステップで透かしを追加することで、別途のポストプロセスが不要になり、バッチパイプラインで最大 **40 %** の処理時間を削減できます。

## 前提条件

- **Aspose.CAD for Java** – 公式サイトから最新の JAR をダウンロードしてください [here](https://releases.aspose.com/cad/java/)。  
- **Java Development Kit (JDK)** – バージョン 11 以降を推奨します。  
- 本番使用のための有効な **Aspose.CAD license**（トライアルの場合は任意）。

## 透かし付きで CAD から PDF を作成する方法は？

CadImage は Aspose.CAD 内で CAD 図面を表す主要クラスです。  
透かしを埋め込んだ状態で CAD ファイルから PDF を作成するには、まず図面を `CadImage` インスタンスにロードします。これにより CAD ドキュメントがメモリ上に表現されます。次に、透かしテキストを含む `MText` または `TextEntity` オブジェクトを作成し、フォントサイズ、色、透明度を設定してモデルスペースに追加します。最後に `save` を `SaveFormat.Pdf` と共に呼び出すことで、変更された図面をベクタ品質を保持したまま PDF にエクスポートします。

### 手順 1: パッケージのインポート

`com.aspose.cad` 名前空間は CAD 操作に必要なすべてのクラスを提供します。

`Image` クラスは CAD ファイルの読み込みと保存のエントリーポイントです。  
`MText` クラスはスタイル設定や位置指定が可能な複数行テキストを表します。

```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.Cad3DPoint;
import com.aspose.cad.fileformats.cad.cadobjects.CadMText;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

### 手順 2: 新しい MTEXT を追加

MText は透かしに使用できる複数行テキストエンティティを表します。

```java
//add new MTEXT
CadMText watermark = new CadMText();
watermark.setText("Watermark message");
watermark.setInitialTextHeight(40);
watermark.setInsertionPoint(new Cad3DPoint(300, 40));
watermark.setLayerName("0");
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(watermark);
```

### 手順 3: テキストのようなシンプルエンティティを追加

TextEntity はシンプルな注釈に使用される単一行テキストオブジェクトです。

```java
// or add more simple entity like Text
CadText text = new CadText();
text.setDefaultValue("Watermark text");
text.setTextHeight(40);
text.setFirstAlignment(new Cad3DPoint(300, 40));
text.setLayerName("0") ;
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(text);
```

### 手順 4: PDF にエクスポート

SaveFormat.Pdf は保存時の出力フォーマットとして PDF を指定します。

```java
// export to pdf
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setLayouts(new String[]{"Model"});
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
cadImage.save(dataDir + "AddWatermark_out.pdf", pdfOptions);

```

## よくある問題と解決策

- **Watermark not visible** – テキスト色が背景とコントラストがあることを確認し、`Transparency` プロパティを設定してください（例: 0.5 は 50 % の不透明度）。  
- **Large files cause OutOfMemoryError** – `CadImageOptions.setLoadMode(LoadMode.Paged)` を設定して `CadImage` のストリーミングモードを有効にします。  
- **Incorrect font rendering** – サーバーに必要な TrueType フォントをインストールするか、`FontRepository` を使用して埋め込んでください。

## よくある質問

**Q: Aspose.CAD はすべての CAD ファイル形式に対応していますか？**  
A: Aspose.CAD は **DWG、DXF、DWT、DWF、その他 30 以上の形式** をサポートしており、実質的に任意のソースファイルから **export cad to pdf** が可能です。

**Q: 透かしテキストの外観をカスタマイズできますか？**  
A: はい。`MText` または `TextEntity` のプロパティを使用して、フォントファミリー、サイズ、色、回転、透明度を制御できます。

**Q: Aspose.CAD for Java のトライアル版はありますか？**  
A: はい、トライアル版は [here](https://releases.aspose.com/) からダウンロードできます。

**Q: Aspose.CAD のサポートはどのように受けられますか？**  
A: コミュニティ支援や公式サポートチャネルについては [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) をご覧ください。

**Q: Aspose.CAD for Java の完全なドキュメントはどこで見つけられますか？**  
A: 詳細な API リファレンス、コードサンプル、ベストプラクティスガイドについては [documentation](https://reference.aspose.com/cad/java/) を参照してください。

---

**最終更新日:** 2026-06-04  
**テスト環境:** Aspose.CAD for Java 24.12  
**作者:** Aspose  

{{< blocks/products/products-backtop-button >}}

## 関連チュートリアル

- [Aspose.CAD for Java を使用して DWG を PDF またはラスタにエクスポート](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Aspose.CAD for Java を使用して DWG から PDF を作成しテキストを追加](/cad/java/cad-text-and-annotation/add-text-in-dwg/)
- [Aspose.CAD for Java を使用して特定の DWG レイアウトを PDF にエクスポート](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}