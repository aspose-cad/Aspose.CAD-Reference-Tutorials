---
date: 2025-12-16
description: Aspose.CAD for Java を使用して CAD を PNG に変換する方法を学びます。DWG の画像へのエクスポート、CAD
  の PNG への保存、CAD をラスタ画像に変換するオプションについて解説します。
linktitle: Convert CAD Drawing to Raster Image Format
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java を使用して CAD を PNG に変換する方法
url: /ja/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java を使用した CAD から PNG への変換方法

## Quick Answers
- **主な目的は何ですか？** CAD 図面を PNG ラスタ画像に変換することです。  
- **使用されているライブラリは？** Aspose.CAD for Java。  
- **ライセンスは必要ですか？** 無料トライアルが利用可能ですが、本番環境で使用するにはライセンスが必要です。  
- **画像サイズをカスタマイズできますか？** はい、`CadRasterizationOptions` を使用して幅と高さを設定します。  
- **サポートされている CAD フォーマットは？** DWG、DXF、DWF など多数。

## “convert CAD to PNG” とは？
CAD を PNG に変換することは、ベクターベースの CAD コンテンツ（DWG、DXF など）をピクセルベースの画像形式にラスタライズすることを意味します。PNG は透過性とロスレス品質を保持するため、ウェブプレビューや文書、レポートに最適です。

## なぜ CAD を PNG（ラスタ画像）に変換するのか？
- **汎用的な閲覧:** PNG は特別な CAD ビューアーなしであらゆるデバイスで表示できます。  
- **高速読み込み:** ラスタ画像はウェブページで瞬時に読み込まれます。  
- **簡単な埋め込み:** PNG を PDF、Word 文書、スライドデッキに挿入できます。  
- **一貫した外観:** 線幅、色、レイヤーを設計通りに正確に保持します。

## Prerequisites
開始する前に、以下を用意してください。

1. **Java 開発環境** – JDK 8 以上がインストールされ、設定されていること。  
2. **Aspose.CAD ライブラリ** – ライブラリをダウンロードし、プロジェクトに追加します。ライブラリは **[here](https://releases.aspose.com/cad/java/)** で入手できます。

## Import Namespaces
Aspose.CAD オブジェクトを使用できるように、Java クラスに必要なインポートを追加します。

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## Step-by-Step Guide to Convert CAD to PNG

### Step 1: Load the CAD Drawing
まず、`Image.load()` を使用してソース CAD ファイル（DXF、DWG など）を読み込みます。

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

> **Pro tip:** `CADConversion` のような専用フォルダーに CAD ファイルを保存しておくと、パスの問題を回避できます。

### Step 2: Set Rasterization Options (export dwg to image)
出力画像のサイズやその他のラスタ設定を定義します。

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
```

必要に応じて、背景色、ライン描画モード、DPI もここで制御できます。

### Step 3: Create Image Options (save cad as png)
`PngOptions` インスタンスを作成し、ラスタ設定を添付します。

```java
ImageOptionsBase options = new PngOptions();
options.setVectorRasterizationOptions(rasterizationOptions);
```

### Step 4: Save the Raster Image (cad file to png)
最後に、PNG ファイルを書き出します。

```java
image.save(dataDir + "conic_pyramid_raster_image_out.png", options);
```

生成されたファイル `conic_pyramid_raster_image_out.png` は、元の CAD 図面を高解像度で表現した PNG です。

### Repeat for Other Files
`srcFile` を別の CAD ファイルに変更して同じ手順を実行するだけです。同じコードは DWG、DWF など他のサポート形式でも動作します。

## Common Issues & Solutions
| Issue | Solution |
|-------|----------|
| **Blank PNG output** | ソース CAD ファイルが正しく読み込まれているか確認してください（`Image.load()` が例外を投げないこと）。 |
| **Incorrect dimensions** | `PageWidth` / `PageHeight` を調整するか、`rasterizationOptions.setResolution(...)` で DPI を設定してください。 |
| **Missing layers** | CAD ファイルのレイヤーが非表示になっていないか確認し、`CadRasterizationOptions.setDrawType(CadDrawTypeMode.Vector);` を使用してください。 |
| **License errors** | 有効な Aspose.CAD ライセンスファイルを使用します（`License license = new License(); license.setLicense("Aspose.CAD.lic");`）。 |

## Frequently Asked Questions

**Q1: Aspose.CAD はすべての CAD フォーマットに対応していますか？**  
A1: Aspose.CAD は DWG、DXF、DWF など幅広い CAD フォーマットをサポートしています。完全なリストは **[documentation](https://reference.aspose.com/cad/java/)** を参照してください。

**Q2: ラスタライズオプションを自分のニーズに合わせてカスタマイズできますか？**  
A2: はい、Aspose.CAD はラスタライズオプションの設定に柔軟性を提供しており、サイズ、DPI、背景色などを要件に合わせて調整できます。

**Q3: Aspose.CAD に関する質問のサポートはどこで受けられますか？**  
A3: **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)** で支援を受け、コミュニティと交流できます。

**Q4: Aspose.CAD for Java の無料トライアルはありますか？**  
A4: はい、**[here](https://releases.aspose.com/)** から無料トライアルを取得して機能を試すことができます。

**Q5: Aspose.CAD for Java を購入するには？**  
A5: 購入は **[purchase page](https://purchase.aspose.com/buy)** から行えます。

---

**Last Updated:** 2025-12-16  
**Tested With:** Aspose.CAD for Java 24.11 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}