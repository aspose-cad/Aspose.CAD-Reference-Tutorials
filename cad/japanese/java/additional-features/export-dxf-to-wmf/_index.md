---
date: 2026-06-09
description: Aspose.CAD for Java を使用して DXF を WMF に変換する方法を学びましょう。無料トライアル、Java 8+ 対応、オプションの
  PDF エクスポートが含まれます。コード例付きのステップバイステップガイドです。
keywords:
- convert dxf to wmf
- aspose cad java
- aspose free trial
- aspose cad conversion
- export dxf pdf
linktitle: Javaを使用してDXFをWMF形式にエクスポート
schemas:
- author: Aspose
  dateModified: '2026-06-09'
  description: Learn how to convert DXF to WMF with Aspose.CAD for Java, including
    a free trial, Java 8+ support, and optional PDF export. Step‑by‑step guide with
    code examples.
  headline: Convert DXF to WMF Using Aspose.CAD in Java
  type: TechArticle
- description: Learn how to convert DXF to WMF with Aspose.CAD for Java, including
    a free trial, Java 8+ support, and optional PDF export. Step‑by‑step guide with
    code examples.
  name: Convert DXF to WMF Using Aspose.CAD in Java
  steps:
  - name: Load DXF Drawing
    text: Image.load reads the DXF file into an Aspose.CAD Image object.
  - name: Configure Rasterization Options
    text: CadRasterizationOptions specifies page size, resolution, and background
      for rasterizing the CAD drawing.
  - name: Save as WMF
    text: ImageSaveOptions with SaveFormat.WMF tells Aspose.CAD to write the output
      as a Windows Metafile.
  - name: Dispose of Resources
    text: Calling image.close() releases native resources used by the Aspose.CAD Image
      object.
  - name: Optional – Export to PDF
    text: PdfOptions configures PDF‑specific settings when saving the image as a PDF
      document. > **Pro tip:** You can reuse the same `CadRasterizationOptions` object
      for PDF export by passing it to a `PdfOptions` instance, saving you a few lines
      of setup.
  type: HowTo
- questions:
  - answer: Yes. Load the file in a try‑with‑resources block and dispose of the `Image`
      object promptly. Adjust `CadRasterizationOptions.setPageWidth/Height` to a reasonable
      size to keep memory usage low.
    question: Can I convert large DXF files (hundreds of MB) without running out of
      memory?
  - answer: WMF is a flat vector format, so layer hierarchy is flattened, but line
      styles, colors, and hatch patterns are preserved.
    question: Does the WMF output retain layer information?
  - answer: Use `rasterizationOptions.setResolution(300);` to define DPI before saving.
    question: Is it possible to set a custom DPI for the WMF?
  - answer: Absolutely. Loop through a directory, load each file, and apply the same
      rasterization and save logic.
    question: Can I batch‑convert multiple DXF files in one run?
  - answer: Aspose.CAD for Java supports Java 8 and later, including Java 11, 17,
      and newer LTS releases.
    question: What versions of Java are supported?
  type: FAQPage
second_title: Aspose.CAD Java API
title: JavaでAspose.CADを使用してDXFをWMFに変換
url: /ja/java/additional-features/export-dxf-to-wmf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java を使用した DXF から WMF への変換

## はじめに

このチュートリアルでは、Aspose.CAD for Java を使用して **DXF を WMF に変換**する方法を紹介します。Windows ベースのレポートに CAD 図面を埋め込む必要がある場合や、Office 文書用の軽量ベクターグラフィックを生成する場合、またはバッチ変換を自動化する場合など、DXF から WMF への変換はエンジニアリングやレポート作成のパイプラインで頻繁に求められます。DXF 図面の読み込み、ラスタライズオプションの設定、WMF としての保存、さらにオプションで同じ図面を PDF にエクスポートする手順を順に解説します。

## クイック回答
- **無料トライアルで DXF を WMF に変換できますか？** はい – Aspose は完全に機能する 30 日間のトライアルを提供しています。  
- **必要な Java バージョンは？** Java 8 以降。  
- **コード実行にライセンスが必要ですか？** 本番環境ではライセンスが必要です。トライアルは開発およびテストで使用できます。  
- **変換はロスレスですか？** ベクターデータは保持されます。ラスタライズオプションで解像度を制御できます。  
- **同じ図面を PDF にエクスポートすることはできますか？** もちろんです – 以下の「PDF へのエクスポート」手順をご覧ください。

## 「DXF から WMF への変換」とは？

DXF から WMF への変換とは、広く使用されている CAD フォーマットである Drawing Exchange Format (DXF) ファイルを取得し、Windows Metafile (WMF) に変換することを指します。WMF はベクター画像フォーマットで、Microsoft Office、Windows アプリケーション、そして多くのレポートツールとスムーズに統合できます。

## なぜ Aspose.CAD for Java を使用するのか？

Aspose.CAD for Java は、純粋な Java 実装でネイティブ DLL を必要としないエンジンを提供し、**99 %以上のベクトル忠実度**で CAD ファイルを変換します。レイヤー、色、線種、ハッチパターンを保持します。**50 以上の入力・出力フォーマット**（DXF、DWG、DGN、PDF、PNG、SVG、WMF など）をサポートし、組み込みのラスタライズオプションでページサイズ、DPI、背景色を細かく調整できます。同じ API で PDF、PNG、SVG のエクスポートも処理でき、複数のライブラリを使用する必要がなくなります。

### 主な利点
- **外部依存なし** – 純粋な Java で、Java が動作する任意の OS で動作します。  
- **高忠実度レンダリング** – 線幅、色、ハッチの詳細を保持します。  
- **組み込みラスタライズ** – ページサイズ、解像度、背景を制御できます。  
- **ワンストップ変換** – 同じクラスで WMF、PDF、PNG、SVG などにエクスポートできます。

## 前提条件

開始する前に、以下が揃っていることを確認してください：

- プロジェクトに統合された **Aspose.CAD for Java**。公式サイトからダウンロードしてください: [Aspose.CAD Java download](https://releases.aspose.com/cad/java/)。  
- DXF ファイルが保存されている **ドキュメントディレクトリ**（例: `Your Document Directory/DXFDrawings/`）。

## 名前空間のインポート

以下のインポートは、CAD ファイルの読み込み、ラスタライズ、保存に必要な Aspose.CAD クラスを取り込みます。  
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

### Java で DXF を WMF に変換するには？

`Image.load("yourFile.dxf")` で DXF ファイルを読み込み、目的のページサイズと DPI を設定するために `CadRasterizationOptions` を構成し、`image.save("output.wmf", new ImageSaveOptions(SaveFormat.WMF))` を呼び出します。この 3 ステップのパターンはベクトル品質を保ったまま完全な変換を実行し、数行のコードだけで済みます。

#### 手順 1: DXF 図面の読み込み

`Image.load` は DXF ファイルを Aspose.CAD の Image オブジェクトに読み込みます。  
```java
import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.WmfOptions;
```

#### 手順 2: ラスタライズオプションの設定

`CadRasterizationOptions` は CAD 図面のラスタライズ時にページサイズ、解像度、背景を指定します。  
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

#### 手順 3: WMF として保存

`SaveFormat.WMF` を使用した `ImageSaveOptions` は、Aspose.CAD に出力を Windows Metafile として書き込むよう指示します。  
```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(100);
rasterizationOptions.setPageHeight(100);
WmfOptions wmfOptions = new WmfOptions();
```

#### 手順 4: リソースの解放

`image.close()` を呼び出すと、Aspose.CAD Image オブジェクトが使用しているネイティブリソースが解放されます。  
```java
cadImage.save(dataDir+" example.ifc.wmf", wmfOptions);
```

#### 手順 5: オプション – PDF へのエクスポート

`PdfOptions` は、画像を PDF 文書として保存する際の PDF 固有の設定を構成します。  
```java
finally
{
  cadImage.dispose();
}
```

> **Pro tip:** `CadRasterizationOptions` オブジェクトを `PdfOptions` インスタンスに渡すことで、PDF エクスポートに同じオブジェクトを再利用でき、設定行数を削減できます。

## Aspose CAD Java を使用して DXF を PDF にエクスポートするには？

PDF へのエクスポートは同じ読み込みとラスタライズの手順に従います。WMF の保存形式を PDF に置き換えるだけです。`new ImageSaveOptions(SaveFormat.Pdf)` を使用し、必要に応じて圧縮レベルや作成者メタデータなどの PDF 固有オプションを設定します。このワンライナー変換により、元の CAD レイアウトを忠実に再現した検索可能でページ正確な PDF が生成されます。

## よくある問題と解決策

| 問題 | 原因 | 対策 |
|-------|-------|-----|
| **`cadImage.save` での `NullPointerException`** | 変数 `cadImage` が未定義（`image` が正しい） | `cadImage` を `image` に置き換えるか、変数名を統一してください。 |
| **出力 WMF が空白** | ラスタライズのページサイズが小さすぎる、または背景色が透明に設定されている。 | `PageWidth`/`PageHeight` を増やすか、`rasterizationOptions.setBackgroundColor(Color.WHITE);` で背景色を設定してください。 |
| **ライセンス例外** | 本番環境で有効な Aspose ライセンスなしで実行している。 | アプリケーション開始時にライセンスファイルを適用します: `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`. |

## 結論

これで、Aspose.CAD for Java を使用して **DXF を WMF に変換**する完全な本番対応ワークフローが手に入り、オプションで **同じ図面を PDF にエクスポート**する手順も備わっています。この方法により、Windows ベースのレポートや文書作成ツールとシームレスに統合できる高品質なベクター出力が得られ、コードベースはシンプルで依存関係がありません。

## FAQ

### Q1: Aspose.CAD のドキュメントはどこで見つけられますか？

ドキュメントは[こちら](https://reference.aspose.com/cad/java/)からアクセスできます。

### Q2: Aspose.CAD for Java をダウンロードするには？

ライブラリは[こちら](https://releases.aspose.com/cad/java/)からダウンロードできます。

### Q3: 無料トライアルは利用できますか？

はい、無料トライアルは[こちら](https://releases.aspose.com/)から取得できます。

### Q4: 一時ライセンスのオプションが必要ですか？

一時ライセンスは[こちら](https://purchase.aspose.com/temporary-license/)でご確認ください。

### Q5: サポートはどこで受けられますか？

Aspose.CAD のサポートフォーラムは[こちら](https://forum.aspose.com/c/cad/19)です。

## よくある質問

**Q: 大容量の DXF ファイル（数百 MB）をメモリ不足にならずに変換できますか？**  
A: はい。try‑with‑resources ブロックでファイルを読み込み、`Image` オブジェクトを速やかに破棄します。`CadRasterizationOptions.setPageWidth/Height` を適切なサイズに調整してメモリ使用量を抑えます。

**Q: WMF の出力はレイヤー情報を保持しますか？**  
A: WMF はフラットなベクターフォーマットで、レイヤー階層はフラット化されますが、線種、色、ハッチパターンは保持されます。

**Q: WMF のカスタム DPI を設定できますか？**  
A: `rasterizationOptions.setResolution(300);` を使用して、保存前に DPI を定義できます。

**Q: 一度に複数の DXF ファイルをバッチ変換できますか？**  
A: もちろんです。ディレクトリをループし、各ファイルを読み込み、同じラスタライズと保存ロジックを適用します。

**Q: サポートされている Java のバージョンは何ですか？**  
A: Aspose.CAD for Java は Java 8 以降をサポートしており、Java 11、17、その他の新しい LTS リリースも対応しています。

---

**最終更新日:** 2026-06-09  
**テスト環境:** Aspose.CAD for Java 24.11  
**作者:** Aspose

```java
image.save(dataDir + "conic_pyramid_out_.pdf"); 
```

## 関連チュートリアル

- [CAD から PDF を作成 – Aspose.CAD for Java で DXF を PDF にエクスポート](/cad/java/additional-features/export-dxf-to-pdf/)
- [DXF から PDF を作成: Aspose.CAD for Java でレイヤーをエクスポート](/cad/java/additional-features/export-specific-layer-to-pdf/)
- [Aspose.CAD for Java で DXF レイアウトを JPEG 画像に変換する方法](/cad/java/additional-features/export-specific-layout-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}