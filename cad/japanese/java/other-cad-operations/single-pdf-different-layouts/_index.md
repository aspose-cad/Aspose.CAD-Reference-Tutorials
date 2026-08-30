---
date: 2026-06-29
description: Aspose.CAD for Java を使用して DWG から PDF を作成し、PDF のレイアウトをカスタマイズする方法を学びます。Java
  開発者向けの簡単な統合。
keywords:
- create pdf from dwg
- convert cad to pdf
- pdf different page sizes
- export dwg to pdf
- customize pdf layout
linktitle: 異なるレイアウトの単一 PDF
schemas:
- author: Aspose
  dateModified: '2026-06-29'
  description: Learn how to create PDF from DWG and customize PDF layout using Aspose.CAD
    for Java. Easy integration for Java developers.
  headline: Create PDF from DWG with Aspose.CAD for Java
  type: TechArticle
- questions:
  - answer: Yes, Aspose.CAD for Java integrates seamlessly with libraries such as
      Apache POI, Jackson, or Spring Boot.
    question: Can I use Aspose.CAD for Java with other Java libraries?
  - answer: Absolutely! You can access a free trial version [here](https://releases.aspose.com/).
    question: Is there a trial version available?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community
      support and discussions.
    question: Where can I find additional support?
  - answer: You can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license?
  - answer: Purchase the full version of Aspose.CAD for Java [here](https://purchase.aspose.com/buy).
    question: Where can I purchase the full version?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java を使用して DWG から PDF を作成
url: /ja/java/other-cad-operations/single-pdf-different-layouts/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java を使用して DWG から PDF を作成する

## はじめに

このチュートリアルでは **DWG から PDF を作成** し、Aspose.CAD for Java を使用して複数のページサイズレイアウトを適用します。建設用ブループリント、エンジニアリング図面、マーケティング向け PDF の生成が必要な場合でも、以下の手順で CAD 図面を PDF に変換し、各レイアウトの寸法をカスタマイズして、単一のマルチページドキュメントを作成できます—すべて Java 環境から離れることなく実行できます。

## クイック回答
- **このチュートリアルでは何をカバーしていますか？** DWG 図面を複数のページサイズを持つ単一の PDF に変換します。  
- **必要なライブラリはどれですか？** Aspose.CAD for Java（最新バージョン）。  
- **ライセンスは必要ですか？** 開発には無料トライアルが使用できますが、本番環境では商用ライセンスが必要です。  
- **他の形式にエクスポートできますか？** はい – API は PNG、JPEG、SVG へのエクスポートもサポートしています。  
- **Java 8 で十分ですか？** このライブラリは Java 8 以降のランタイムで動作します。

## 「DWG から PDF を作成」とは？

**DWG から PDF を作成** は、ネイティブの AutoCAD DWG ファイルをベクターフィデリティ、レイヤー、線幅を保持したまま PDF ドキュメントに変換し、レイアウトのカスタマイズを可能にすることを意味します。Aspose.CAD はこの変換を完全にメモリ内で実行するため、外部の CAD ソフトウェアは不要で、生成された PDF は直接編集または印刷できます。

## DWG から PDF のレイアウトをカスタマイズする理由は？

Aspose.CAD は **30 以上の CAD フォーマット** をサポートし、ファイル全体をメモリに読み込まずに **500 MB** までの PDF を生成できます。各レイアウトごとに個別のページサイズを定義することで、ISO、ANSI、またはカスタム寸法に合致した印刷用シートを作成でき、時間を節約し手動の後処理を排除するという具体的なメリットがあります。

## 前提条件

開始する前に、以下の前提条件が整っていることを確認してください：
- Java 環境: マシンに Java がインストールされていることを確認してください。  
- Aspose.CAD ライブラリ: [download link](https://releases.aspose.com/cad/java/) から Aspose.CAD ライブラリ for Java をダウンロードしてインストールしてください。  
- ドキュメントディレクトリ: DWG 図面用のディレクトリを設定してください。

## パッケージのインポート

`CadImage` クラスは、メモリ内の CAD 図面を表す Aspose.CAD のコアオブジェクトです。開始する前に必要な名前空間をインポートしてください:

```java
import com.aspose.cad.Image;
import com.aspose.cad.SizeF;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.VectorRasterizationOptions;
```

## ステップ 1: CAD 図面の読み込み

`CadImage` は DWG ファイルを読み込み、ベクターデータへのアクセスを提供します。まず、CAD 図面を `CadImage` オブジェクトに読み込みます:

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
CadImage cadImage = (CadImage)Image.load(dataDir + "City skyway map.dwg");
```

## ステップ 2: ラスタライズオプションの設定

`RasterizationOptions` は、CAD ベクトルが PDF に配置される前にどのようにラスタライズされるかを定義します。CAD 画像のラスタライズオプションを設定してください:

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1000);
rasterizationOptions.setPageHeight(1000);
```

## ステップ 3: レイアウトページサイズのカスタマイズ

`PdfOptions` を使用すると、DWG 内の各レイアウトに対して個別のページ寸法を割り当てることができます。CAD 図面内の複数レイアウトに対してカスタムサイズを定義します:

```java
rasterizationOptions.getLayoutPageSizes().addItem("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.getLayoutPageSizes().addItem("8.5 x 11 Plot", new SizeF(1000, 100));
```

## ステップ 4: PDF オプションの設定

`PdfOptions` はラスタライズ設定とレイアウト定義を組み合わせるコンテナです。ラスタライズ設定を組み込んで PDF オプションを構成してください:

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## ステップ 5: PDF として保存

`PdfSaveOptions` は変換を最終化し、出力ファイルを書き込みます。処理された CAD 画像を PDF として保存してください:

```java
cadImage.save(dataDir + "singlePDF_out.pdf", pdfOptions);
```

おめでとうございます！Aspose.CAD for Java を使用して、異なるページサイズで **DWG から PDF を作成** に成功しました。

## よくある問題と解決策

- **出力 PDF の空白ページ** – `PageSize` の値が DWG ファイル内の実際のレイアウト寸法と一致していることを確認してください。  
- **大きな図面でのメモリ不足エラー** – `CadImage.load(..., LoadOptions)` と `LoadOptions.setLoadMode(LoadMode.Memory)` を使用して、ファイル全体を読み込むのではなくストリーミングしてください。  
- **スケーリングが正しくない** – `RasterizationOptions.setPageWidth` と `setPageHeight` を調整して、目的の DPI（ドット per インチ）に合わせてください。

## よくある質問

**Q: Aspose.CAD for Java を他の Java ライブラリと併用できますか？**  
A: はい、Aspose.CAD for Java は Apache POI、Jackson、Spring Boot などのライブラリとシームレスに統合できます。

**Q: トライアル版は利用可能ですか？**  
A: もちろんです！無料トライアル版は [here](https://releases.aspose.com/) から入手できます。

**Q: 追加のサポートはどこで得られますか？**  
A: コミュニティサポートやディスカッションは [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) をご覧ください。

**Q: 一時ライセンスはどのように取得できますか？**  
A: 一時ライセンスは [here](https://purchase.aspose.com/temporary-license/) から取得できます。

**Q: フルバージョンはどこで購入できますか？**  
A: Aspose.CAD for Java のフルバージョンは [here](https://purchase.aspose.com/buy) から購入できます。

---

**最終更新日:** 2026-06-29  
**テスト環境:** Aspose.CAD for Java 24.10  
**作者:** Aspose

## 関連チュートリアル

- [Aspose.CAD for Java を使用して DWG を PDF またはラスタにエクスポート](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Aspose.CAD for Java で CAD レイアウトを PDF にエクスポート](/cad/java/cad-export-options/export-cad-layouts-to-pdf/)
- [Aspose.CAD for Java を使用して特定の DWG レイアウトを PDF にエクスポート](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-wrap-class >}}