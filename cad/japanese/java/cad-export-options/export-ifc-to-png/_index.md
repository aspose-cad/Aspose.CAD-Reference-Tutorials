---
date: 2026-02-20
description: Aspose.CAD for Java を使用して、IFC を PNG に簡単に変換しましょう。ステップバイステップのチュートリアルをご覧ください。
linktitle: Export IFC to PNG
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java を使用した IFC から PNG への変換方法
url: /ja/java/cad-export-options/export-ifc-to-png/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java を使用した IFC の PNG へのエクスポート

## Introduction

このステップバイステップチュートリアルへようこそ。**IFC を PNG に変換する方法**を Aspose.CAD for Java で解説します。BIM から画像へのパイプラインを構築したい場合や、IFC モデルの簡易プレビューが必要な場合に、本ガイドは Java アプリケーションで **IFC を PNG に変換** できるよう、すべての手順を詳しく説明します。

## Quick Answers
- **必要なライブラリは？** Aspose.CAD for Java  
- **数行のコードで IFC を PNG に変換できるか？** はい – コア処理は 20 行未満で収まります。  
- **本番環境でライセンスは必要か？** テスト用の一時ライセンスは利用可能ですが、商用利用にはフルライセンスが必要です。  
- **出力はスケーラブルか？** ラスタライズオプションで任意のピクセルサイズを指定できます。  
- **対応している Java バージョンは？** Java 8 以降。

## What is “convert IFC to PNG”?
IFC（Industry Foundation Classes）を PNG に変換することは、3 次元建築モデルデータを 2 次元ビットマップ画像にラスタライズすることを意味します。サムネイル生成、レポートへのモデル埋め込み、またはフル CAD ビューアーを必要としない Web 用ビジュアライゼーションの作成に便利です。

## Why use Aspose.CAD for Java?
- **フル機能** の CAD フォーマットサポート（IFC を含む）。  
- **外部依存なし** – 純粋な Java で、統合が容易。  
- **細かい制御** が可能なラスタライズ（解像度、背景、線幅）。  
- **クロスプラットフォーム** – Windows、Linux、macOS で動作。

## Prerequisites

開始する前に、以下を用意してください。

- **Aspose.CAD Library** – [download link](https://releases.aspose.com/cad/java/) から Aspose.CAD for Java をダウンロードしてインストール。  
- **Document Directory** – 変換したい IFC ファイルが格納されているフォルダー。

## Import Namespaces

Java プロジェクトで必要なクラスをインポートします。

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## Step‑by‑Step Guide

### Step 1: Load the IFC File
まず、IFC ファイルが存在するフォルダーを指定し、ファイルをロードします。

```java
String dataDir = "Your Document Directory" + "ExportingIFC/";
String fileName = dataDir + "example.ifc";
IfcImage cadImage = (IfcImage)Image.load(fileName);
```

> **Why this matters:** `IfcImage` としてファイルをロードすることで、後続の CAD 固有のラスタライズオプションにアクセスできるようになります。

### Step 2: Set Vector (Rasterization) Options
出力サイズやその他のベクトル関連設定を定義します。

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

> `PageWidth` と `PageHeight` を調整することで、最終的な PNG の解像度を制御できます。これは **save PNG java** ファイルを高品質印刷用に保存する際に重要です。

### Step 3: Configure PNG Options
ラスタライズオプションを PNG エクスポーターにリンクします。

```java
PngOptions pngOptions = new PngOptions();
pngOptions.setVectorRasterizationOptions(vectorOptions);
```

### Step 4: Save the Image as PNG
最後に、ラスタライズされた画像をディスクに書き出します。

```java
String outPath = dataDir + "example.png";
cadImage.save(outPath, pngOptions);
```

> この手順が完了すると、**IFC を PNG に変換** した `example.png` が生成され、任意の場所でラスタ画像として使用できます。

## Common Use Cases
- Web ポータルで BIM モデルの **サムネイル生成**。  
- PDF レポートに **フロアプランのスナップショット埋め込み**。  
- 大規模 IFC ライブラリの **バッチ変換** を自動化してアーカイブ。

## Troubleshooting & Tips
- **メモリ問題:** 非常に大きな IFC ファイルを変換する場合は、JVM ヒープを増やしてください（例: `-Xmx2g` 以上）。  
- **テクスチャが欠落:** IFC ファイルが参照する外部リソースが `dataDir` からアクセス可能か確認してください。  
- **プロのコツ:** デフォルトの透過 PNG ではなく白背景が必要な場合は、`vectorOptions.setBackgroundColor(Color.getWhite())` を使用します。

## FAQ's

### Q1: Is Aspose.CAD compatible with all versions of IFC files?
A1: Aspose.CAD supports various versions of IFC files. Refer to the [documentation](https://reference.aspose.com/cad/java/) for compatibility details.

### Q2: Can I customize the rasterization options further?
A2: Absolutely! Explore the [documentation](https://reference.aspose.com/cad/java/) for advanced customization options.

### Q3: Is there a trial version available?
A3: Yes, you can access the free trial version [here](https://releases.aspose.com/).

### Q4: How can I get temporary licensing for Aspose.CAD?
A4: Obtain a temporary license from [this link](https://purchase.aspose.com/temporary-license/).

### Q5: Where can I seek help or discuss issues?
A5: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community support.

## Frequently Asked Questions

**Q: Can I use this approach to convert other CAD formats to PNG?**  
A: Yes, Aspose.CAD supports many formats (DWG, DXF, DGN, etc.). Just change the file extension and cast to the appropriate image class.

**Q: Does the library let me set a custom DPI?**  
A: You can control DPI indirectly by adjusting `PageWidth`/`PageHeight` relative to the desired physical size.

**Q: Is the PNG output loss‑less?**  
A: PNG is a lossless format, so the rasterized image retains full visual fidelity of the vector data.

## Conclusion

You’ve now learned how to **convert IFC to PNG** efficiently with Aspose.CAD for Java. By following these steps you can integrate IFC‑to‑PNG conversion into any Java‑based workflow, whether it’s a desktop tool, a server‑side service, or a cloud function.

---

**Last Updated:** 2026-02-20  
**Tested With:** Aspose.CAD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}