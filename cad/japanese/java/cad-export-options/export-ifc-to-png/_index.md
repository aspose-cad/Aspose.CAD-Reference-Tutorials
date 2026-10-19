---
date: 2026-10-19
description: 数行のコードで Aspose.CAD for Java を使用して PNG サムネイル IFC ファイルを作成する方法を学びましょう。
keywords:
- create png thumbnail ifc
- ifc to png conversion
- aspose cad java
- java image processing
- bIM visualization
lastmod: 2026-10-19
linktitle: IFC を PNG にエクスポート
og_description: Aspose.CAD for Java を使用して PNG サムネイル IFC ファイルを簡単に作成します。このステップバイステップガイドでは、IFC
  モデルを読み込み、ラスタライズし、高品質な PNG 画像として保存する方法を示します。
og_image_alt: Developer guide showing Java code that converts IFC files to PNG thumbnails
  using Aspose.CAD
og_title: Aspose.CAD for Java で PNG サムネイル IFC を作成
schemas:
- author: Aspose
  dateModified: '2026-10-19'
  description: Learn how to create PNG thumbnail IFC files with Aspose.CAD for Java
    in just a few lines of code.
  headline: How to create PNG thumbnail IFC with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to create PNG thumbnail IFC files with Aspose.CAD for Java
    in just a few lines of code.
  name: How to create PNG thumbnail IFC with Aspose.CAD for Java
  steps:
  - name: load the IFC file
    text: First, point to the folder where your IFC file lives and load it with `CadImage.load`.
      `CadImage.load` reads a CAD file and returns an image object that can be rasterized.
      > **Why this matters:** Loading the file as a `CadImage` gives you access to
      vector‑raster conversion options that control resol
  - name: set rasterization options
    text: Define the output dimensions and any other vector‑related settings through
      `VectorRasterizationOptions`. `VectorRasterizationOptions` lets you specify
      output size, background color, and other rasterization parameters. > Adjust
      `PageWidth` and `PageHeight` to control the final PNG resolution, which i
  - name: configure PNG options
    text: Link the rasterization options to the PNG exporter by creating a `PngOptions`
      instance.
  - name: save the image as PNG
    text: Finally, write the rasterized image to disk using the `save` method. `save`
      writes the rasterized image to the specified file path in the chosen format.
      > After this step you have successfully **created a PNG thumbnail IFC** and
      can use the resulting `example.png` anywhere you need a raster image.
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD supports many formats (DWG, DXF, DGN, etc.). Simply change
      the file extension and load the appropriate image class.
    question: Can I use this approach to convert other CAD formats to PNG?
  - answer: DPI is controlled indirectly via `PageWidth`/`PageHeight`. Adjust these
      values relative to the desired physical size to achieve the required DPI.
    question: Does the library let me set a custom DPI?
  - answer: PNG is a lossless format, so the rasterized image retains the full visual
      fidelity of the original vector data.
    question: Is the PNG output loss‑less?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- ifc conversion
- png thumbnail
- aspose.cad
- java image processing
- bim visualization
title: Aspose.CAD for Java を使用して PNG サムネイル IFC を作成する方法
url: /ja/java/cad-export-options/export-ifc-to-png/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java を使用した IFC の PNG へのエクスポート

## はじめに

このチュートリアルでは、Aspose.CAD for Java を使用して **PNG サムネイル IFC** ファイルを作成する方法を学びます。BIM ポータル向けのクイックプレビューが必要な場合や、ドキュメント管理システム用のサムネイルを生成したい場合、またはバッチ変換を自動化したい場合でも、以下の手順で数行の Java コードだけで 3‑D IFC モデルを鮮明な 2‑D PNG 画像にラスタライズできます。

## クイック回答

- **必要なライブラリは何ですか？** Aspose.CAD for Java.  
- **数行のコードで PNG サムネイル IFC を作成できますか？** はい – 全体のワークフローは 20 行未満で収まります。  
- **本番環境でライセンスが必要ですか？** テスト用の一時ライセンスで動作しますが、商用展開にはフルライセンスが必要です。  
- **出力はスケーラブルですか？** 任意のピクセルサイズを設定できるため、PNG は必要なサイズにスケーリングできます。  
- **サポートされている Java バージョンはどれですか？** Java 8 以降。

## 「IFC を PNG に変換する」とは何ですか？

IFC（Industry Foundation Classes）を PNG に変換するとは、3‑D 建築モデルを 2‑D ビットマップ画像にラスタライズすることを意味します。このプロセスにより、フル CAD ビューアを必要とせずに、ブラウザやレポート、モバイルアプリで表示できるビジュアルサムネイルが作成されます。

## なぜ Aspose.CAD for Java を使用するのですか？

Aspose.CAD は **30 以上の CAD および BIM フォーマット**（IFC、DWG、DXF、DGN など）をサポートし、**2 GB** までのファイルをドキュメント全体をメモリにロードせずに処理できます。このライブラリは純粋な Java で構成され、**外部依存関係がゼロ** で、Windows、Linux、macOS 上で動作するため、サーバーサイドの画像生成に最適です。  
高性能なラスタライズ、広範なフォーマットサポート、そして Java アプリケーションへの簡単な統合を提供します。

## 前提条件

- **Aspose.CAD Library** – 最新の JAR を [download link](https://releases.aspose.com/cad/java/) からダウンロードしてください。  
- **Java Development Kit** – JDK 8 以上がマシンにインストールされていること。  
- **IFC source file** – コードから参照できるフォルダーにファイルを配置してください。

## 名前空間のインポート

`com.aspose.cad` パッケージは必要なすべてのクラスを提供します。`CadImage` は CAD ファイルをロードするエントリーポイントで、`PngOptions` はラスタライズ設定を構成します。

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## Java で PNG サムネイル IFC を作成する方法

IFC ファイルをロードし、ラスタライズオプションを定義し、結果を PNG 画像として保存します – これが完全な変換ワークフローです。以下のセクションで各ステップを分解しているので、スニペットをコピー＆ペーストしてすぐにプロジェクトで実行できます。

### ステップ 1: IFC ファイルをロードする
まず、IFC ファイルが保存されているフォルダーを指定し、`CadImage.load` でロードします。  
`CadImage.load` は CAD ファイルを読み込み、ラスタライズ可能な画像オブジェクトを返します。

```java
String dataDir = "Your Document Directory" + "ExportingIFC/";
String fileName = dataDir + "example.ifc";
IfcImage cadImage = (IfcImage)Image.load(fileName);
```

> **なぜ重要か:** ファイルを `CadImage` としてロードすることで、解像度、背景色、線幅を制御するベクトル‑ラスタ変換オプションにアクセスできます。

### ステップ 2: ラスタライズオプションを設定する
`VectorRasterizationOptions` を使用して出力寸法やその他のベクトル関連設定を定義します。  
`VectorRasterizationOptions` では、出力サイズ、背景色、その他のラスタライズパラメータを指定できます。

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

> `PageWidth` と `PageHeight` を調整して最終的な PNG 解像度を制御します。これは高品質印刷やウェブサムネイル用に **save PNG java** ファイルを保存する際に重要です。

### ステップ 3: PNG オプションを構成する
`PngOptions` インスタンスを作成して、ラスタライズオプションを PNG エクスポーターにリンクします。

```java
PngOptions pngOptions = new PngOptions();
pngOptions.setVectorRasterizationOptions(vectorOptions);
```

### ステップ 4: 画像を PNG として保存する
最後に、`save` メソッドを使用してラスタライズされた画像をディスクに書き込みます。  
`save` は、指定されたファイルパスに選択した形式でラスタライズ画像を書き込みます。

```java
String outPath = dataDir + "example.png";
cadImage.save(outPath, pngOptions);
```

> このステップが完了すると、**PNG サムネイル IFC** が正常に作成され、生成された `example.png` をラスタ画像が必要な任意の場所で使用できます。

## 一般的な使用例

- **BIM モデルのサムネイル生成** をウェブポータルで行う。  
- **フロアプランのスナップショットを** PDF や Word レポートに埋め込む。  
- **大規模 IFC ライブラリの自動バッチ変換** をアーカイブや移行プロジェクト向けに実施する。

## トラブルシューティングとヒント

- **メモリ問題:** 非常に大きな IFC ファイルの場合、JVM ヒープを増やしてください（`-Xmx2g` 以上）。  
- **テクスチャが欠如:** IFC ファイルの外部リソースが `dataDir` から参照可能であることを確認してください。  
- **プロのコツ:** デフォルトの透過 PNG の代わりに白背景が好みの場合は、`vectorOptions.setBackgroundColor(Color.getWhite())` を使用します。

## よくある質問

### Q1: Aspose.CAD はすべてのバージョンの IFC ファイルと互換性がありますか？

A1: Aspose.CAD はさまざまな IFC バージョンをサポートしています。詳細な互換性情報については、[documentation](https://reference.aspose.com/cad/java/) を参照してください。

### Q2: ラスタライズオプションをさらにカスタマイズできますか？

A2: もちろんです！DPI 制御、アンチエイリアシング、線の太さなどの高度な設定については、[documentation](https://reference.aspose.com/cad/java/) をご覧ください。

### Q3: 試用版は利用できますか？

A3: はい、[Aspose.CAD free trial](https://releases.aspose.com/) から無料トライアルをダウンロードできます。

### Q4: テスト用の一時ライセンスはどのように取得できますか？

A4: [Aspose.CAD temporary license page](https://purchase.aspose.com/temporary-license/) から一時ライセンスを取得してください。

### Q5: 質問や問題の報告はどこでできますか？

A5: Aspose エンジニアや他の開発者からサポートを受けられる [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) に参加してください。

## よくある質問

**Q: この方法で他の CAD フォーマットを PNG に変換できますか？**  
A: はい、Aspose.CAD は多数のフォーマット（DWG、DXF、DGN など）をサポートしています。ファイル拡張子を変更し、適切な画像クラスをロードするだけです。

**Q: ライブラリでカスタム DPI を設定できますか？**  
A: DPI は `PageWidth`/`PageHeight` を間接的に設定することで制御されます。目的の実サイズに合わせてこれらの値を調整すれば、必要な DPI を得られます。

**Q: PNG 出力はロスレスですか？**  
A: PNG はロスレス形式であるため、ラスタライズされた画像は元のベクターデータの視覚的忠実度を完全に保持します。

## 結論

これで、Aspose.CAD for Java を使用して **PNG サムネイル IFC** ファイルを作成する完全な本番対応の方法が手に入りました。これらの手順をデスクトップツール、サーバーサイドサービス、またはクラウド関数に統合して、BIM 可視化パイプラインを自動化し、エンドユーザーに高速で高品質なサムネイルを提供できます。

---

**最終更新日:** 2026-10-19  
**テスト環境:** Aspose.CAD for Java 24.11  
**作者:** Aspose

## 関連チュートリアル

- [Aspose.CAD for Java を使用した STL を PNG に変換する方法](/cad/java/cad-export-options/export-stl-to-png/)
- [Aspose.CAD for Java を使用した DWG を PNG に変換 – CAD を PNG として保存](/cad/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/)
- [Aspose.CAD を使用した Java での DWG の PDF へのエクスポート – PDF ページサイズの設定](/cad/java/cad-export-options/export-to-pdf/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}