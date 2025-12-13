---
date: 2025-12-13
description: Aspose.CAD を使用して Java で CAD を JPEG として保存する方法、複数のレイヤーを追加する方法、正確な画像変換のために
  CAD の寸法を調整する方法を学びましょう。
linktitle: Support of Layers in CAD
second_title: Aspose.CAD Java API
title: Javaでレイヤー対応のCADをJPEGとして保存
url: /ja/java/advanced-cad-features/support-of-layers-in-cad/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Javaでレイヤーサポート付きCADをJPEGとして保存する

## Introduction

このチュートリアルでは、Aspose.CAD for Java のレイヤーサポートをフル活用しながら **CAD を JPEG として保存** する方法をご紹介します。レイヤーを使用すると、図面の特定部分だけを分離でき、必要なものだけをエクスポートするのが簡単になります。環境設定から、選択したレイヤーだけを含む JPEG をエクスポートするまで、各ステップを順に解説します。

## Quick Answers
- **“save CAD as JPEG” とは何ですか？** CAD 図面をラスタ画像の JPEG に変換することです。  
- **選択したレイヤーだけを含められますか？** はい – `setLayers` メソッドでレンダリングするレイヤーを指定します。  
- **画像サイズはどう変更しますか？** `CadRasterizationOptions` の `setPageWidth` と `setPageHeight` を調整します。  
- **これは Java のみのソリューションですか？** 例は Aspose.CAD for Java を使用していますが、同様の概念は他の言語でも適用できます。  
- **ライセンスは必要ですか？** 無料トライアルでテストは可能ですが、商用利用には製品ライセンスが必要です。

## Prerequisites

始める前に、以下が揃っていることを確認してください。

1. **Aspose.CAD for Java Library** – [website](https://releases.aspose.com/cad/java/) からダウンロードします。インストールガイドに従い、JAR ファイルをプロジェクトのクラスパスに追加してください。  
2. **Java Development Environment** – 最近の JDK（8 以降）がマシンにインストールされていること。

準備が整ったら、**選択的レイヤーレンダリング** を伴う **CAD を JPEG として保存** するコードを見ていきましょう。

## Import Namespaces

必要な Aspose.CAD クラスと標準 Java ユーティリティをインポートします。

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
```

## Step‑by‑Step Guide

### Step 1: Set Up File Paths

ソースの DWF ファイルがある場所と、出力 JPEG を書き込む場所を定義します。

```java
String dataDir = "Your Document Directory" + "DWFDrawings/";
String srcFile = dataDir + "for_layers_test.dwf";
String outFile = dataDir + "for_layers_test.jpg";
```

### Step 2: Load the DWF Image

Aspose.CAD の `Image.load` メソッドを使って CAD 図面を読み込みます。

```java
Image image = Image.load(srcFile);
```

### Step 3: Configure Rasterization Options (Adjust CAD Dimensions)

`CadRasterizationOptions` インスタンスを作成し、希望する出力サイズを設定します。これらの値を変更することで、最終的な JPEG の **CAD サイズを調整** できます。

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### Step 4: Specify Layers (Add Multiple Layers)

複数のレイヤーをレンダリングしたい場合は、リストに名前を追加するだけです。ここでは「LayerA」という単一レイヤーから始めます。

```java
List<String> stringList = new ArrayList<>(Arrays.asList("LayerA"));
rasterizationOptions.setLayers(stringList);
```

*Pro tip:* **複数レイヤーを追加** するには、`Arrays.asList` 呼び出しを拡張します。例: `Arrays.asList("LayerA", "LayerB", "LayerC")`.

### Step 5: Configure JPEG Options (Java Convert CAD Image)

ラスタライズ設定を JPEG 出力形式に結び付けます。

```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Step 6: Export to JPG (Save CAD as JPEG)

最後に画像をディスクに書き出します。このステップで **選択したレイヤーだけを含む CAD 図面を JPEG ファイルとして保存** します。

```java
image.save(outFile, jpegOptions);
```

これらの手順を実行すれば、**レイヤーの表示を制御し、画像サイズをカスタマイズした上で CAD を JPEG として保存** できました。

## Common Issues and Solutions

| Issue | Solution |
|-------|----------|
| **Layers not appearing** | レイヤー名が DWF ファイルに保存されているものと完全に一致しているか（大文字小文字を含む）確認してください。 |
| **Output image is blank** | `setPageWidth` と `setPageHeight` が図面の範囲をカバーできるだけ十分に大きいか確認してください。 |
| **License exception** | テストにはトライアルライセンスを使用し、本番環境では正式ライセンスを取得してください。 |

## Frequently Asked Questions

**Q: Can I add multiple layers to the rasterization options?**  
A: Absolutely. Extend the `stringList` with additional layer names, e.g., `Arrays.asList("LayerA", "LayerB")`.

**Q: Is Aspose.CAD compatible with other CAD formats?**  
A: Yes, it supports DWG, DXF, DWF, and many more formats.

**Q: How can I change the output image dimensions?**  
A: Modify `setPageWidth` and `setPageHeight` in the `CadRasterizationOptions` instance.

**Q: Where can I purchase a license for Aspose.CAD?**  
A: You can explore licensing options [here](https://purchase.aspose.com/buy).

**Q: Where can I get community support?**  
A: Join the Aspose.CAD community on the [forum](https://forum.aspose.com/c/cad/19) for assistance and discussions.

---

**Last Updated:** 2025-12-13  
**Tested With:** Aspose.CAD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}