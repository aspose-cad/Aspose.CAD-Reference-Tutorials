---
date: 2025-12-18
description: Aspose.CAD for Java を使用して、DWG を PNG やその他のラスタ画像形式に変換する方法を学びましょう。高品質な結果で
  CAD を PNG にエクスポートできます。
linktitle: Convert CAD Layout to Raster Image Format
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java を使用して DWG を PNG やその他のラスタ形式に変換する
url: /ja/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java を使用した DWG から PNG およびその他ラスター形式への変換

## はじめに

DWG を PNG（または他のラスター画像形式）に変換することは、CAD ビューアを持っていないチームメンバーと図面を共有したり、ドキュメントにデザインを埋め込んだり、ウェブギャラリー用のサムネイルを生成したりする際に一般的な要件です。Aspose.CAD for Java を使えば、フルドローイングファイルでも特定のレイアウトだけでも、変換はシンプルに行えます。このチュートリアルでは、**CAD レイアウトをラスター画像に変換する**手順を詳しく解説します。PNG、JPEG、TIFF、PDF などの出力にも同じ手法が適用できます。

## クイック回答
- **DWG から PNG を処理するライブラリは？** Aspose.CAD for Java  
- **エクスポート可能な形式は？** PNG、JPEG、TIFF、PDF、BMP など多数  
- **テストにライセンスは必要？** 開発段階は無料トライアルで可。製品環境ではライセンスが必要です。  
- **特定のレイアウトを選択できる？** はい、`setLayouts` を使用して “Model”、 “Layout1” などを指定できます。  
- **高解像度出力は可能か？** もちろんです。`setPageWidth` と `setPageHeight` を調整して DPI を制御します。

## “convert dwg to png” とは？

“convert dwg to png” というフレーズは、ベクターベースの DWG ファイル（多くの CAD アプリケーションのネイティブ形式）をピクセルベースの PNG 画像にラスタライズするプロセスを指します。ラスター画像はウェブ表示、メールでの共有、非 CAD ソフトウェアへの統合に最適です。

## なぜ CAD を PNG（または他のラスター形式）でエクスポートするのか？

- **汎用性:** PNG や JPEG は事実上すべての画像ビューアやブラウザでサポートされています。  
- **高速ロード:** 重い DWG ファイルを開くよりも、ラスター画像は即座に表示されます。  
- **簡単な埋め込み:** PNG を Word、PowerPoint、HTML にプラグインなしで直接挿入できます。  
- **外観の一貫性:** 解像度、背景、レイアウトを自分でコントロールできるため、すべてのステークホルダーが同じビジュアルを確認できます。

## 前提条件

開始する前に以下を用意してください。

1. **Java 開発環境** – JDK 8 以降がインストールされ、設定済みであること。  
2. **Aspose.CAD for Java** – 最新の JAR を [Aspose.CAD for Java ドキュメント](https://reference.aspose.com/cad/java/) からダウンロード。

## 名前空間のインポート

まず、必要なクラスをインポートします。これらのインポートにより、画像の読み込み、ラスタライズオプション、TIFF/PNG の出力設定が利用可能になります。

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

> **プロのコツ:** PNG にエクスポートする場合は、`TiffOptions` の代わりに `com.aspose.cad.imageoptions.PngOptions` にある `PngOptions` を使用してください。

## 手順ガイド

### 手順 1: リソースディレクトリの設定

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
```

`"Your Document Directory"` を CAD ファイルが格納されている絶対パスに置き換えてください。

### 手順 2: CAD ファイルの読み込み

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

DWG、DXF、DGN など、サポートされている任意の形式を読み込めます。これが **how to convert cad** の部分で、ファイルを指すだけで Aspose が解析を行います。

### 手順 3: ラスタライズオプションの構成

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
rasterizationOptions.setLayouts(new String[] {"Model", "Layout1"});
```

- `setPageWidth` / `setPageHeight` は出力解像度を制御します（数値が大きいほど DPI が高くなります）。  
- `setLayouts` を使用すると、特定のレイアウトだけを **convert cad to raster** できます。省略すると全体をラスタライズします。

### 手順 4: 画像オプションの設定

```java
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.setVectorRasterizationOptions(rasterizationOptions);
```

PNG が必要な場合は `TiffOptions` の代わりに `PngOptions` をインスタンス化してください。ここが **export cad as png** のポイントです。

### 手順 5: 結果画像の保存

```java
image.save(dataDir + "conic_pyramid_layoutstorasterimage_out_.tiff", options);
```

ファイル拡張子を `.png`（オプションオブジェクトも `PngOptions` に）に変更すれば **save CAD as JPEG/PNG** が実現できます。

> **よくある落とし穴:** ファイル拡張子とオプションクラスが一致していないと `UnsupportedFormatException` が発生します。必ずペアを合わせてください。

## よくある問題と解決策

| 問題 | 解決策 |
|------|--------|
| **空白の出力画像** | `setLayouts` に指定したレイアウト名がソース CAD ファイル内と完全に一致しているか確認してください。 |
| **低解像度 PNG** | `setPageWidth` / `setPageHeight` を増やすか、ラスタライズオプションの `setResolution` を設定してください。 |
| **サポート外の DWG バージョン** | 最新の Aspose.CAD バージョンを使用してください。古いバージョンでは新しい DWG がサポートされないことがあります。 |
| **大容量ファイルでのメモリエラー** | ページごとに処理するか、JVM ヒープを増やします（例: `-Xmx2g`）。 |

## FAQ（よくある質問）

**Q: Aspose.CAD はさまざまな CAD ファイル形式に対応していますか？**  
A: はい、DWG、DXF、DGN など多数の形式をサポートしています。

**Q: 出力ラスター画像の解像度はカスタマイズできますか？**  
A: もちろんです。`CadRasterizationOptions` の `setPageWidth`、`setPageHeight`、または `setResolution` を調整してください。

**Q: 1 回の実行で複数の CAD レイアウトを変換できますか？**  
A: `setLayouts` にすべてのレイアウト名を配列で渡します。例: `new String[]{"Model","Layout1","Layout2"}`。

**Q: TIFF 以外の出力形式はありますか？**  
A: はい、PNG、JPEG、BMP、PDF など、各 `*Options` クラスを使用して利用可能です。

**Q: Aspose.CAD のサポートやコミュニティはどこで得られますか？**  
A: [Aspose.CAD フォーラム](https://forum.aspose.com/c/cad/19) でコミュニティの支援や公式サポートを受けられます。

## 結論

この手順に従えば **DWG を PNG に変換** でき、**CAD を PNG としてエクスポート**、**CAD を JPEG として保存**、あるいは必要な他のラスター形式を生成できます。Aspose.CAD for Java が重い処理を担ってくれるので、アプリケーションやドキュメント、ウェブポータルへの高品質画像統合に集中できます。

---

**最終更新日:** 2025-12-18  
**テスト環境:** Aspose.CAD for Java 24.12  
**作成者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}