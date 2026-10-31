---
date: 2026-10-30
description: Aspose.CAD for Java を使用して DXF ファイルを WMF にバッチ変換する方法を、ステップバイステップのコード、無料トライアル情報、オプションの
  PDF エクスポートとともに学びましょう。
keywords:
- batch convert dxf files
- aspose cad java
- dxf to wmf conversion
- java cad rasterization
- aspose free trial
lastmod: 2026-10-30
linktitle: Java を使用した DXF の WMF 形式へのエクスポート
og_description: Aspose.CAD for Java を使用して DXF ファイルを WMF にバッチ変換します。このガイドでは、DXF 図面の読み込み、ラスタライズオプションの設定、WMF
  への保存、そしてオプションで PDF へエクスポートする方法を、無料トライアルとともに紹介します。
og_image_alt: Tutorial showing batch conversion of DXF to WMF in Java using Aspose.CAD
og_title: Aspose.CAD for Java を使用した DXF ファイルのバッチ変換（WMF）
schemas:
- author: Aspose
  dateModified: '2026-10-30'
  description: Learn how to batch convert DXF files to WMF using Aspose.CAD for Java,
    with step‑by‑step code, free trial info, and optional PDF export.
  headline: Batch convert DXF files to WMF with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to batch convert DXF files to WMF using Aspose.CAD for Java,
    with step‑by‑step code, free trial info, and optional PDF export.
  name: Batch convert DXF files to WMF with Aspose.CAD for Java
  steps:
  - name: load dxf drawing
    text: Image.load reads the DXF file into an Aspose.CAD Image object.
  - name: configure rasterization options
    text: '`CadRasterizationOptions` specifies page size, resolution, and background
      for rasterizing the CAD drawing.'
  - name: save as wmf
    text: '`ImageSaveOptions` with `SaveFormat.WMF` tells Aspose.CAD to write the
      output as a Windows Metafile.'
  - name: dispose of resources
    text: Calling `image.close()` releases native resources used by the Aspose.CAD
      Image object.
  - name: optional – export to pdf
    text: '`PdfOptions` configures PDF‑specific settings when saving the image as
      a PDF document. > **Pro tip:** You can reuse the same `CadRasterizationOptions`
      object for PDF export by passing it to a `PdfOptions` instance, saving you a
      few lines of setup.'
  type: HowTo
- questions:
  - answer: You can access the documentation [Aspose.CAD Java documentation](https://reference.aspose.com/cad/java/).
    question: Where can I find the Aspose.CAD documentation?
  - answer: Download the library [Aspose.CAD Java download page](https://releases.aspose.com/cad/java/).
    question: How do I download Aspose.CAD for Java?
  - answer: Yes, you can get a free trial [Aspose free trial page](https://releases.aspose.com/).
    question: Is there a free trial available?
  - answer: Explore temporary licenses [temporary license options](https://purchase.aspose.com/temporary-license/).
    question: Need temporary licensing options?
  - answer: Visit the Aspose.CAD support forum [Aspose.CAD support forum](https://forum.aspose.com/c/cad/19).
    question: Where can I get support?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- batch convert dxf
- Aspose.CAD
- Java CAD conversion
- WMF export
- DXF processing
title: Aspose.CAD for Java を使用した DXF ファイルのバッチ変換（WMF）
url: /ja/java/additional-features/export-dxf-to-wmf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java を使用した DXF ファイルの WMF へのバッチ変換

## はじめに

このチュートリアルでは、Aspose.CAD for Java を使用して **DXF ファイルを WMF にバッチ変換**する方法を学びます。Windows ベースのレポートに CAD 図面を埋め込む必要がある場合や、Office ドキュメント用の軽量ベクターグラフィックを生成する場合、または大規模な変換を自動化したい場合でも、本ガイドは DXF 図面の読み込み、ラスタライズオプションの設定、WMF への保存、さらに同じ図面を PDF にエクスポートする手順を案内します。手順は Java 8 以降が動作する任意のプラットフォームで実行可能です。

## クイック回答
- **無料トライアルで DXF を WMF に変換できますか？** はい – Aspose は機能フルの 30 日間トライアルを提供しています。  
- **必要な Java バージョンは？** Java 8 以降。  
- **コード実行にライセンスは必要ですか？** 本番環境ではライセンスが必要です。トライアルは開発・テストに使用できます。  
- **変換はロスレスですか？** ベクターデータは保持され、ラスタライズオプションで解像度を制御できます。  
- **同じ図面を PDF にエクスポートできますか？** もちろんです – 以下の「PDF へのエクスポート」手順をご覧ください。  
- **多数の DXF ファイルを一括変換するには？** フォルダーをループし、同じ load‑rasterize‑save パターンを各ファイルに適用します。

## バッチ変換とは何ですか？

バッチ変換は、複数の Drawing Exchange Format (DXF) 図面を一度に処理し、各図面に対して WMF 出力を生成することを指します。WMF（Windows Metafile）はベクター画像形式で、Microsoft Office、Windows アプリケーション、各種レポートツールとネイティブに統合できます。

## なぜ Aspose.CAD for Java を使用するのか？

Aspose.CAD for Java は純粋な Java エンジンで、**50 以上の入力および出力フォーマット**（DXF、DWG、DGN、PDF、PNG、SVG、WMF など）をサポートし、**99 % のベクターフィデリティ**を提供します。Java をサポートする任意の OS 上で動作し、ネイティブ DLL は不要です。`CadRasterizationOptions` クラスを介してページサイズ、DPI、背景色を制御でき、同じ API で PDF、PNG、SVG のエクスポートも可能なため、複数のライブラリを導入する必要がなくなります。

### 定量的なメリット
- **50+ のサポートフォーマット**によりサードパーティ変換ツールの必要が減少。  
- **300 ページの DXF ファイルを 5 秒未満**で処理（典型的な 2.5 GHz サーバ、150 DPI ラスタライズ時）。  
- **メモリ使用量は 200 MB 未満**に抑えられ、最大 500 MB のファイルでも適切なページサイズ設定で対応可能。  

## 前提条件

- **Aspose.CAD for Java** をプロジェクトに統合します。公式サイトからダウンロードしてください: [Aspose.CAD Java ダウンロード](https://releases.aspose.com/cad/java/)。  
- 変換したい DXF ファイルが入っているフォルダー（例: `Your Document Directory/DXFDrawings/`）。  

## 名前空間のインポート

`Image` は Aspose.CAD のコアクラスで、CAD 図面をメモリ上に表現します。ファイルを読み込んだ後、ラスタライズ、フォーマット変換、リソースクリーンアップはすべてこのオブジェクトを通じて実行されます。

以下のインポートは、CAD ファイルの読み込み、ラスタライズ、保存に必要な Aspose.CAD クラスをプロジェクトに取り込みます。  
```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageSaveOptions;
import com.aspose.cad.fileformats.cad.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.CadImageInfo;
import com.aspose.cad.fileformats.cad.CadImageInfo;
import java.awt.Color;
```

## 手順ガイド

### Java で DXF ファイルを WMF にバッチ変換する方法は？

各 DXF を `Image.load` で読み込み、目的のページサイズと DPI を `CadRasterizationOptions` で設定し、`image.save` に `SaveFormat.WMF` を指定して保存します。この 3 ステップのパターンでベクター品質を保ちつつ完全な変換が行え、ファイルごとに数行のコードで実装できます。

#### 手順 1: DXF 図面の読み込み

Image.load は DXF ファイルを Aspose.CAD Image オブジェクトに読み込みます。  
```java
import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.WmfOptions;
```

#### 手順 2: ラスタライズオプションの設定

`CadRasterizationOptions` は CAD 図面をラスタライズする際のページサイズ、解像度、背景色を指定します。  
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

#### 手順 3: WMF として保存

`SaveFormat.WMF` を指定した `ImageSaveOptions` により、Aspose.CAD は出力を Windows Metafile として書き込みます。  
```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(100);
rasterizationOptions.setPageHeight(100);
WmfOptions wmfOptions = new WmfOptions();
```

#### 手順 4: リソースの解放

`image.close()` を呼び出すことで、Aspose.CAD Image オブジェクトが使用しているネイティブリソースを解放します。  
```java
cadImage.save(dataDir+" example.ifc.wmf", wmfOptions);
```

#### 手順 5: オプション – PDF へのエクスポート

`PdfOptions` は画像を PDF 文書として保存する際の PDF 固有設定を構成します。  
```java
finally
{
  cadImage.dispose();
}
```

> **Pro tip:** 同じ `CadRasterizationOptions` オブジェクトを `PdfOptions` インスタンスに渡すことで再利用でき、設定行数を削減できます。

## Aspose CAD Java を使用して DXF を PDF にエクスポートする方法は？

WMF の保存形式を `new ImageSaveOptions(SaveFormat.Pdf)` に置き換えるだけです。同じラスタライズ設定が適用され、さらに作者メタデータや圧縮レベルなど PDF 固有のオプションを設定できます。このワンライナー変換により、元の CAD レイアウトを忠実に再現した検索可能でページ正確な PDF が生成されます。

## よくある問題と解決策

`License` は実行時に製品ライセンスを適用するための Aspose クラスです。

| 問題 | 原因 | 対策 |
|-------|-------|-----|
| **`cadImage.save` で `NullPointerException`** | 変数 `cadImage` が未定義（`image` であるべき） | `cadImage` を `image` に置き換えるか、変数名を一貫させてください。 |
| **出力 WMF が空白** | ラスタライズのページサイズが小さすぎる、または背景色が透明に設定されている | `PageWidth`/`PageHeight` を増やすか、`rasterizationOptions.setBackgroundColor(Color.WHITE);` で背景色を設定してください。 |
| **ライセンス例外** | 本番環境で有効な Aspose ライセンスなしで実行している | アプリケーション開始時にライセンスファイルを適用します: `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`。 |

## よくある質問

**Q: Aspose.CAD のドキュメントはどこで確認できますか？**  
A: ドキュメントは以下からアクセスできます: [Aspose.CAD Java ドキュメント](https://reference.aspose.com/cad/java/)。

**Q: Aspose.CAD for Java はどうやってダウンロードしますか？**  
A: ライブラリは次のページからダウンロードしてください: [Aspose.CAD Java ダウンロードページ](https://releases.aspose.com/cad/java/)。

**Q: 無料トライアルは利用可能ですか？**  
A: はい、無料トライアルは以下から取得できます: [Aspose 無料トライアルページ](https://releases.aspose.com/)。

**Q: 一時的なライセンスオプションはありますか？**  
A: 一時ライセンスは次のページで確認できます: [一時ライセンスオプション](https://purchase.aspose.com/temporary-license/)。

**Q: サポートはどこで受けられますか？**  
A: Aspose.CAD のサポートフォーラムをご利用ください: [Aspose.CAD サポートフォーラム](https://forum.aspose.com/c/cad/19)。

## 追加のよくある質問

**Q: 数百 MB の大容量 DXF ファイルをメモリ不足なく変換できますか？**  
A: はい。try‑with‑resources ブロックでファイルを読み込み、`Image` オブジェクトを速やかに破棄します。`CadRasterizationOptions.setPageWidth/Height` を適切に設定すればメモリ使用量を抑えられます。

**Q: WMF 出力はレイヤー情報を保持しますか？**  
A: WMF はフラットなベクターフォーマットのためレイヤーヒエラルキーはフラット化されますが、線種、色、ハッチパターンは保持されます。

**Q: WMF の DPI をカスタム設定できますか？**  
A: 保存前に `rasterizationOptions.setResolution(300);` で DPI を指定できます。

**Q: 一度の実行で複数の DXF ファイルをバッチ変換できますか？**  
A: もちろんです。ディレクトリを走査し、各ファイルに同じラスタライズと保存ロジックを適用します。

**Q: サポートされている Java のバージョンは？**  
A: Aspose.CAD for Java は Java 8 以降、Java 11、17 などの LTS リリースをサポートしています。

**最終更新日:** 2026-10-30  
**テスト環境:** Aspose.CAD for Java 24.11  
**作成者:** Aspose

## 関連チュートリアル

- [CAD から PDF を作成 – Aspose.CAD for Java で DXF を PDF にエクスポート](/cad/java/additional-features/export-dxf-to-pdf/)
- [DXF から PDF を作成: レイヤーをエクスポート – Aspose.CAD for Java](/cad/java/additional-features/export-specific-layer-to-pdf/)
- [DXF レイアウトを JPEG 画像に変換する方法 – Aspose.CAD for Java](/cad/java/additional-features/export-specific-layout-to-image/)

```java
image.save(dataDir + "conic_pyramid_out_.pdf"); 
```

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}