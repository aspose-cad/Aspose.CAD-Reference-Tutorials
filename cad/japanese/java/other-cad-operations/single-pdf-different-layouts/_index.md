---
date: 2026-01-22
description: Aspose.CAD for Java を使用して、CAD 図面から PDF を作成し、DWG を PDF に変換し、PDF のページサイズをカスタマイズする方法を学びましょう。
linktitle: Single PDF with Different Layouts
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java を使用して CAD 図面から PDF を作成する方法
url: /ja/java/other-cad-operations/single-pdf-different-layouts/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java を使用した CAD 図面から PDF の作成方法

## Introduction

このチュートリアルでは、Aspose.CAD ライブラリ for Java を使用して **CAD から PDF を作成する方法** を学びます。**DWG から PDF への変換**、複雑な CAD ファイルのエクスポート、または **カスタム PDF ページサイズ** の適用が必要な場合でも、以下のログラム的に解などの形式へエクスポートできるようにします。
- **複数のレイアウトを 1 つの PDF にエ。
ットは？** DWG、DXF、DWF、DGN など多数。
- **本番環境でライセンスは必要ですか？** テスト用の一時ライセンスは動作しますが、商用利用にはフルライセンスが必要です。
- **必要な Java のバージョンは？** Java 8 以降。

## What is “create PDF from CAD”?
CAD から を作成するとは、ベクターベースの CAD 図面をラスタライズして、任意のデバイスで CAD ソフトウェアなしに閲覧できる固定レイアウトのドキュメント（PDF）に変換することです。設計の共有、ブループリントの印刷、エンジニアリング成果物のアーカイブに最適です。

## Why use Aspose.CAD for Java?
- **外部依存なし** – 純粋な Java 実装で、ネイティブ DLL が不要です。
- **細かな制御** – DPI、ページサイズ、レイアウト選択などのラスタライズオプションを詳細に設定できます。
- **バッチ処理** – 複数の図面を一括で処理可能です。
- **高精度変換** – 線幅、色、レイヤー情報を正確に保持します。

## Prerequisites

開始する前に、以下を用意してください。

- **Java 環境** – JDK 8 以上がインストールされていること。
- **Aspose.CAD ライブラリ** – [ダウンロードリンク](https://releases.aspose.com/cad/java/) から Aspose.CAD for Java を取得し、インストールします。
- **ドキュメント ディレクトリ** – 変換したい DWG（またはその他の CAD）ファイルが格納されたフォルダー。

## Import Packages

Java プロジェクトで必要なクラスをインポートします。

```java
import com.aspose.cad.Image;
import com.aspose.cad.SizeF;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.VectorRasterizationOptions;
```

## Step‑by‑Step Guide

### Step 1: Load CAD Drawing

まず、ソース CAD ファイル（例: DWG）を `CadImage` オブジェクトに読み込みます。これは **CAD から PDF へのエクスポート** のエントリーポイントです。

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
CadImage cadImage = (CadImage)Image.load(dataDir + "City skyway map.dwg");
```

### Step 2: Configure Rasterization Options

CAD データのラスタライズ方法を定義します。ここでは、カスタムサイズが設定されていないレイアウトに使用する基本ページ幅と高さを指定します。

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1000);
rasterizationOptions.setPageHeight(1000);
```

### Step 3: Customize Layout Page Sizes

**カスタム PDF ページサイズ** が必要な場合は、最終 PDF に含めたい各レイアウトのエントリを追加します。これにより、レイアウトごとに異なる寸法で **DWG から PDF への変換** が可能になります。

```java
rasterizationOptions.getLayoutPageSizes().addItem("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.getLayoutPageSizes().addItem("8.5 x 11 Plot", new SizeF(1000, 100));
```

### Step 4: Set PDF Options

ラスタライズ設定と PDF 固有のオプションを組み合わせます。`VectorRasterizationOptions` プロパティで、先ほど定義したレイアウトサイズを Aspose.CAD に指示します。

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Step 5: Save as PDF

最後に、指定したすべてのレイアウトを含む単一の PDF ファイルへエクスポートします。このステップで **CAD を PDF として保存** が一度の呼び出しで完了します。

```java
cadImage.save(dataDir + "singlePDF_out.pdf", pdfOptions);
```

> **Pro tip:** バッチで複数の図面をエクスポートする場合は、同じ `PdfOptions` オブジェクトを再利用すると、オブジェクト生成のオーバーヘッドが削減されます。

## Common Issues and Solutions

| Issue | Solution |
|-------|----------|
| **出力 PDF に空白ページがある** | レイアウト名（例: `"ANSI C Plot"`、`"8.5 x 11 Plot"`）が CAD ファイル内で定義されている名前と完全に一致しているか確認してください。 |
| **低解像度の出力** | 保存前に `rasterizationOptions.setResolution(300);` を呼び出して DPI を上げてください。 |
| **ライセンスが適用されない** | Aspose.CAD の呼び出しの前に、一時またはフルライセンスをロードします: `License license = new License(); license.setLicense("Aspose.CAD.lic");` |

## Frequently Asked Questions

### Q1: Aspose.CAD for Java を他の Java ライブラリと併用できますか？

A1: はい、Aspose.CAD for Java は他の Java ライブラリとシームレスに統合でき、豊富な機能を提供します。

### Q2: 試用版はありますか？

A2: もちろんです！無料試用版は[こちら](https://releases.aspose.com/)から入手できます。

### Q3: 追加のサポートはどこで受けられますか？

A3: コミュニティサポートやディスカッションは[Aspose.CAD フォーラム](https://forum.aspose.com/c/cad/19)をご利用ください。

### Q4: 一時ライセンスはどのように取得しますか？

A4: 一時ライセンスは[こちら](https://purchase.aspose.com/temporary-license/)から取得できます。

### Q5: 正式版はどこで購入できますか？

A5: Aspose.CAD for Java の正式版は[こちら](https://purchase.aspose.com/buy)から購入できます。

---

**Last Updated:** 2026-01-22  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}