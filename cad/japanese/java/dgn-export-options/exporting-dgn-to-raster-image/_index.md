---
date: 2026-05-25
description: Aspose.CAD for Java を使用して dgn ファイルを JPEG 画像にエクスポートする方法を学びます。このステップバイステップガイドでは、dgn
  を jpeg に効率的に変換する方法を示します。
keywords:
- how to export dgn
- convert dgn to jpeg
- java convert cad to image
linktitle: AutoCAD フォーマットの DGN をラスタ画像形式にエクスポート
schemas:
- author: Aspose
  dateModified: '2026-05-25'
  description: Learn how to export dgn files to JPEG images with Aspose.CAD for Java.
    This step‑by‑step guide shows you how to convert dgn to jpeg efficiently.
  headline: How to Export DGN to JPEG with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to export dgn files to JPEG images with Aspose.CAD for Java.
    This step‑by‑step guide shows you how to convert dgn to jpeg efficiently.
  name: How to Export DGN to JPEG with Aspose.CAD for Java
  steps:
  - name: '**Aspose.CAD Library** – download the latest JAR from the official site [here](https://releases.aspose.com/cad/java/).
      You can also explore other product releases [here](https://releases.aspose.com/).'
    text: '**Aspose.CAD Library** – download the latest JAR from the official site [here](https://releases.aspose.com/cad/java/).
      You can also explore other product releases [here](https://releases.aspose.com/).'
  - name: '**Java Development Kit (JDK)** – Java 8 or newer installed on your machine.'
    text: '**Java Development Kit (JDK)** – Java 8 or newer installed on your machine.'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor you prefer.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor you prefer.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD supports over 30 vector formats, including DWG, DXF, DWF,
      and SVG, enabling a single API for many conversion scenarios.
    question: Can I use Aspose.CAD for Java with other CAD file formats?
  - answer: Yes, you can access a free trial [here](https://releases.aspose.com/).
    question: Is there a free trial available for Aspose.CAD for Java?
  - answer: Refer to the official docs [here](https://reference.aspose.com/cad/java/).
    question: Where can I find documentation for Aspose.CAD for Java?
  - answer: Visit the support forum [here](https://forum.aspose.com/c/cad/19).
    question: How can I get support for Aspose.CAD for Java?
  - answer: You can buy a license [here](https://purchase.aspose.com/buy).
    question: Where can I purchase a license for Aspose.CAD for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java を使用して DGN を JPEG にエクスポートする方法
url: /ja/java/dgn-export-options/exporting-dgn-to-raster-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java DGN から JPEG への変換（Aspose.CAD）チュートリアル

## はじめに

この包括的なガイドでは、Aspose.CAD for Java を使用して **how to export dgn** ファイルを JPEG 画像にエクスポートする方法を紹介します。バッチ処理サービスを構築する場合や、CAD ビューアにオンザフライのプレビュー生成を追加する場合でも、このチュートリアルはソースファイルの読み込みからラスタ出力の保存まで、すべての手順を順を追って説明します。また、コードをクリーンかつ高性能に保つ実用的なヒントも紹介します。

## クイック回答
- **必要なライブラリは何ですか？** Aspose.CAD for Java (download [here](https://releases.aspose.com/cad/java/)).
- **1 行で DGN を JPEG に変換できますか？** はい – load with `CadImage.load` and call `save` with `JpegOptions`.
- **本番環境でライセンスは必要ですか？** はい、商用ライセンスを使用すると評価版の透かしが削除されます。
- **サポートされている Java バージョンは何ですか？** Java 8 から 17 までが完全にサポートされています。
- **処理できる DGN の最大サイズはどれくらいですか？** 最大 2 GB のファイルを、全体をメモリに読み込まずに処理できます。

## “how to export dgn” とは何ですか？

*“How to export dgn”* は、MicroStation DGN 設計ファイルを別の形式（通常は JPEG などのラスタ画像）に変換し、閲覧や共有を容易にするプロセスを指します。この変換により、CAD ソフトウェアを持たない関係者も設計を確認したり、文書に画像を埋め込んだり、ウェブギャラリー用のサムネイルを生成したりできるため、アクセシビリティとチーム間のコラボレーションが向上します。

## なぜ Aspose.CAD for Java を使用するのか？

Aspose.CAD は **30 以上の CAD フォーマット**（DGN、DWG、DXF など）をサポートし、元の CAD アプリケーションなしで **最大 2 GB** のファイルをレンダリングできます。そのラスタエンジンは標準サーバーハードウェア上でマルチページ図面を **> 50 fps** で処理し、単一の API 呼び出しで高品質な JPEG 出力を提供します。

## 前提条件

1. **Aspose.CAD Library** – 公式サイトから最新の JAR をダウンロード [here](https://releases.aspose.com/cad/java/)。他の製品リリースも [here](https://releases.aspose.com/) で確認できます。  
2. **Java Development Kit (JDK)** – Java 8 以上がインストールされた環境。  
3. **IDE** – IntelliJ IDEA、Eclipse、またはお好みの Java 対応エディタ。

## パッケージのインポート

Java プロジェクトで、必要な Aspose.CAD クラスをインポートします:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
```

## Aspose.CAD を使用した Java での dgn から JPEG へのエクスポート方法

`CadImage` クラスはメモリに読み込まれた CAD ドキュメントを表し、レンダリングや保存のメソッドを提供します。

`CadImage.load("source.dgn")` で DGN ファイルを読み込み、`JpegOptions`（品質や解像度を含む）を設定し、ページサイズや背景色などの `RasterizationOptions` を適切に設定して、最後に `image.save("output.jpg", jpegOptions)` を呼び出します。この 3 ステップのフローはベクトルからラスタへの変換を処理し、線幅を保持し、典型的な図面では 1 秒未満で高品質な JPEG ファイルを書き出します。

## 手順 1: DGN ファイルの読み込み

`CadImage` クラスはメモリに読み込まれた CAD ドキュメントを表します。

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
DgnImage dgnImage = (DgnImage) Image.load(dataDir + "Nikon_D90_Camera.dgn");
```

## 手順 2: JpegOptions オブジェクトの作成

`JpegOptions` は JPEG 出力に固有の設定（圧縮品質や解像度など）を定義します。

```java
ImageOptionsBase options = new JpegOptions();
```

## 手順 3: RasterizationOptions の割り当て

`RasterizationOptions` はベクタ画像をどのようにラスタライズするかを決定し、ページサイズ、DPI、背景色、アンチエイリアスなどを含みます。

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(600);
vectorOptions.setPageHeight(400);
vectorOptions.setNoScaling(true);
vectorOptions.setAutomaticLayoutsScaling(false);
options.setVectorRasterizationOptions(vectorOptions);
```

## 手順 4: 変換画像の保存

`save` を呼び出すことで、指定したオプションを使用してラスタ画像をディスクに書き込みます。

```java
OutputStream outStream = new FileOutputStream(dataDir + "ExportDGNToRasterImage_Out.jpg");
dgnImage.save(outStream, options);
```

### 一般的な使用例

- **Web プレビュー生成** – エンジニアリング図面を軽量な JPEG サムネイルに変換し、ブラウザでの高速表示を実現します。  
- **バッチアーカイブ** – 数千件の DGN ファイルを JPEG に自動変換し、MicroStation 不要で長期保存します。  
- **レポーティング** – Java コードから直接 CAD スナップショットを PDF や HTML レポートに埋め込みます。

### 一般的な問題と解決策

| 問題 | 解決策 |
|-------|----------|
| **画像が空白になる** | `RasterizationOptions.setPageWidth/Height` が図面の範囲と一致していることを確認し、透明でない背景を設定してください。 |
| **低品質な出力** | `JpegOptions.setQuality(100)` を増やし、より高い DPI（例: `RasterizationOptions.setResolution(300)`）を設定してください。 |
| **メモリ不足エラー** | 大きなファイルをストリーミングするために、`loadOptions.setLoadMode(LoadMode.Memory)` を使用して `CadImage.load` を呼び出してください。 |

## よくある質問

**Q: Aspose.CAD for Java を他の CAD ファイル形式でも使用できますか？**  
A: はい、Aspose.CAD は DWG、DXF、DWF、SVG など 30 以上のベクタ形式をサポートしており、さまざまな変換シナリオで単一の API を利用できます。

**Q: Aspose.CAD for Java の無料トライアルは利用できますか？**  
A: はい、無料トライアルは [here](https://releases.aspose.com/) からアクセスできます。

**Q: Aspose.CAD for Java のドキュメントはどこで見つけられますか？**  
A: 公式ドキュメントは [here](https://reference.aspose.com/cad/java/) を参照してください。

**Q: Aspose.CAD for Java のサポートはどこで受けられますか？**  
A: サポートフォーラムは [here](https://forum.aspose.com/c/cad/19) です。

**Q: Aspose.CAD for Java のライセンスはどこで購入できますか？**  
A: ライセンスは [here](https://purchase.aspose.com/buy) から購入できます。

**最終更新日:** 2026-05-25  
**テスト環境:** Aspose.CAD 24.11 for Java  
**作者:** Aspose

## 関連チュートリアル

- [Aspose.CAD for Java を使用した DGN から AutoCAD PDF への簡単エクスポート](/cad/java/dgn-export-options/exporting-dgn-to-pdf/)
- [Aspose.CAD for Java で DGN を DWG にエクスポート – チュートリアル](/cad/java/dgn-export-options/)
- [CAD を PNG として保存 – Aspose.CAD for Java を使用した CAD 図面のラスタ画像形式への変換](/cad/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}