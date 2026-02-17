---
date: 2026-02-17
description: Aspose.CAD を使用して Java で DWG を JPEG として保存する方法、複数のレイヤーを追加する方法、そして正確な画像変換のために
  CAD の寸法を調整する方法を学びましょう。
linktitle: Support of Layers in CAD
second_title: Aspose.CAD Java API
title: Javaでレイヤーサポート付きDWGをJPEGとして保存
url: /ja/java/advanced-cad-features/support-of-layers-in-cad/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Javaでレイヤーサポート付きDWGをJPEGとして保存

## Introduction

このチュートリアルでは、Aspose.CAD for Java のレイヤーサポートをフル活用して **DWG を JPEG として保存** する方法を学びます。レイヤーを使用すると、図面の特定部分を分離でき、必要なものだけをエクスポートできます。環境設定から、選択したレイヤーだけを含む JPEG のエクスポートまで、各ステップを順に説明します。

## Quick Answers
- **「DWG を JPEG として保存」 は何を意味しますか？** DWG（または他の CAD）図面をラスタ JPEG 画像に変換します。  
- **選択したレイヤーだけを含めることはできますか？** はい – `setLayers` メソッドを使用して、レンダリングするレイヤーを指定します。  
- **画像サイズはどう変更しますか？** `CadRasterizationOptions` の `setPageWidth` と `setPageHeight` を調整します。  
- **これは Java のみのソリューションですか？** 例は Aspose.CAD for Java を使用していますが、同じ概念は他の言語でも適用できます。  
- **ライセンスは必要ですか？** 無料トライアルでテストは可能ですが、商用利用には商用ライセンスが必要です。

## What is “save DWG as JPEG”?

DWG を JPEG として保存するとは、ベクターベースの CAD ファイル（DWG、DWF、DXF など）を標準的な JPEG ビットマップにラスタライズすることです。これは、CAD 図面をウェブページ、メール、レポートなど、ラスタ画像しかサポートしない環境に埋め込む必要がある場合に便利です。

## Why use layer‑aware JPEG conversion?

- **関連データに集中:** 必要なレイヤーだけをエクスポートし、ファイルサイズと視覚的な雑音を削減します。  
- **設計意図を保持:** レイヤーはオブジェクトの論理的なグループ化を保ち、同じソースファイルをさまざまな出力に再利用できます。  
- **寸法を完全にコントロール:** ラスタライズオプションを調整することで、出版要件に合った高解像度画像を生成できます。

## Prerequisites

以下を事前に用意してください:

1. **Aspose.CAD for Java ライブラリ** – [website](https://releases.aspose.com/cad/java/) からダウンロードしてください。インストールガイドに従い、JAR ファイルをプロジェクトのクラスパスに追加します。  
2. **Java 開発環境** – 最近の JDK（8 以上）をマシンにインストールしてください。

準備が整ったので、選択的レイヤーレンダリングで **DWG を JPEG として保存** するためのコードを見ていきましょう。

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

ステップ 1: ファイルパスの設定

ソース DWF ファイルの場所と、出力 JPEG を書き込む場所を定義します。

```java
String dataDir = "Your Document Directory" + "DWFDrawings/";
String srcFile = dataDir + "for_layers_test.dwf";
String outFile = dataDir + "for_layers_test.jpg";
```

### Step 2: Load the DWF Image

ステップ 2: DWF 画像のロード

Aspose.CAD の `Image.load` メソッドを使用して CAD 図面を読み込みます。

```java
Image image = Image.load(srcFile);
```

### Step 3: Configure Rasterization Options (Adjust CAD Dimensions)

ステップ 3: ラスタライズオプションの設定（CAD の寸法調整）

`CadRasterizationOptions` のインスタンスを作成し、目的の出力サイズを設定します。これらの値を変更することで、最終的な JPEG 用に **CAD の寸法を調整** できます。

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### Step 4: Specify Layers (Add Multiple Layers)

ステップ 4: レイヤーの指定（複数レイヤーの追加）

複数のレイヤーをレンダリングしたい場合は、リストにレイヤー名を追加するだけです。ここでは「LayerA」という単一レイヤーから始めます。

```java
List<String> stringList = new ArrayList<>(Arrays.asList("LayerA"));
rasterizationOptions.setLayers(stringList);
```

*プロのコツ:* **複数レイヤーを追加**するには、`Arrays.asList` 呼び出しを拡張します。例: `Arrays.asList("LayerA", "LayerB", "LayerC")`。これにより、変換時に **特定の CAD レイヤーを選択** できます。

### Step 5: Configure JPEG Options (Java Convert CAD Image)

ステップ 5: JPEG オプションの設定（Java で CAD 画像を変換）

ラスタライズ設定を JPEG 出力形式に結び付けます。

```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Step 6: Export to JPG (Save DWG as JPEG)

ステップ 6: JPG へエクスポート（DWG を JPEG として保存）

最後に、画像をディスクに書き込みます。このステップで **選択したレイヤーだけを含む CAD 図面を JPEG ファイルとして保存** します。

```java
image.save(outFile, jpegOptions);
```

これらの手順に従うことで、表示するレイヤーを制御し、画像寸法をカスタマイズしながら **DWG を JPEG として保存** に成功しました。

## How to Convert DWF to JPEG with Layer Selection

レイヤー選択で DWF を JPEG に変換する方法

例は DWF ソースを使用していますが、同じラスタライズパイプラインはサポートされている任意の CAD フォーマット（DWG、DXF、DGN など）で機能します。`srcFile` の拡張子を変更すれば、ライブラリが **DWF を JPEG に変換**（または他の形式への変換）を自動的に処理します。

## Common Issues and Solutions

| 問題 | 解決策 |
|-------|----------|
| **レイヤーが表示されない** | レイヤー名が DWF ファイルに保存されているものと完全に一致しているか（大文字小文字を含め）確認してください。 |
| **出力画像が空白** | `setPageWidth` と `setPageHeight` が図面の範囲に対して十分に大きいことを確認してください。 |
| **ライセンス例外** | テストにはトライアルライセンスを使用し、本番環境では正式なライセンスを取得してください。 |

## Frequently Asked Questions

**Q: ラスタライズオプションに複数のレイヤーを追加できますか？**  
A: もちろんです。`stringList` に追加のレイヤー名を加えて拡張します。例: `Arrays.asList("LayerA", "LayerB")`。

**Q: Aspose.CAD は他の CAD フォーマットと互換性がありますか？**  
A: はい、DWG、DXF、DWF など多数のフォーマットをサポートしています。

**Q: 出力画像の寸法はどう変更できますか？**  
A: `CadRasterizationOptions` インスタンスの `setPageWidth` と `setPageHeight` を変更します。

**Q: Aspose.CAD のライセンスはどこで購入できますか？**  
A: ライセンスオプションは [here](https://purchase.aspose.com/buy) で確認できます。

**Q: コミュニティサポートはどこで得られますか？**  
A: 支援や議論のために Aspose.CAD コミュニティの [forum](https://forum.aspose.com/c/cad/19) に参加してください。

---

**最終更新日:** 2026-02-17  
**テスト環境:** Aspose.CAD for Java 24.11  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}