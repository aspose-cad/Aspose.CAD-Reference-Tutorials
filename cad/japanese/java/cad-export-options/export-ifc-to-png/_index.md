---
date: 2025-12-21
description: Aspose.CAD for Java を使用して、IFC を PNG に簡単に変換できます。ステップバイステップのチュートリアルをご覧ください。
linktitle: Export IFC to PNG
second_title: Aspose.CAD Java API
title: Aspose.CAD for JavaでIFCをPNGに変換
url: /ja/java/cad-export-options/export-ifc-to-png/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java を使用した IFC から PNG への変換

## はじめに

このチュートリアルでは、強力な Aspose.CAD ライブラリ for Java を使用して **IFC を PNG に変換する方法** を学びます。BIM ビューアの構築、建設ポータル用サムネイルの生成、ドキュメントパイプラインの自動化など、IFC（Industry Foundation Classes）ファイルをラスタ画像に変換する必要は多くのシナリオで共通しています。各手順を解説し、設定の背景を説明し、最高のビジュアル結果を得るためのヒントをご紹介します。

## クイック回答
- **必要なライブラリは？** Aspose.CAD for Java（無料トライアルあり）。  
- **対応している IFC バージョンは？** 主に IFC 2x3 と IFC4 ファイルをサポート。  
- **標準的な変換時間は？** 標準モデルで数秒。ファイルサイズに依存します。  
- **ライセンスは必要？** 本番利用には一時ライセンスが必要です。  
- **画像サイズはカスタマイズできる？** はい – `CadRasterizationOptions` で幅と高さを設定できます。

## 「IFC から PNG への変換」とは？
IFC を PNG に変換するとは、3 次元建築モデル（IFC）を 2 次元ビットマップ画像（PNG）にラスタライズすることです。このプロセスはジオメトリを平坦化し、デフォルトのビジュアルスタイルを適用して、CAD ビューアを必要とせずにブラウザ、レポート、モバイルアプリで表示できるポータブル画像を生成します。

## なぜ Aspose.CAD for Java を使うのか？
- **外部 CAD ソフト不要** – 純粋な Java API で、どのプラットフォームでも動作。  
- **高忠実度レンダリング** – 線幅、色、レイヤーを正確に保持。  
- **フルコントロール** – ラスタライズオプションで解像度、背景色などを自由に設定可能。  
- **簡単なライセンス管理** – トライアルと一時ライセンスで評価が容易。

## 前提条件

開始する前に以下を用意してください。

- **Aspose.CAD ライブラリ** – [ダウンロードリンク](https://releases.aspose.com/cad/java/) から取得してインストール。  
- **Java Development Kit (JDK)** – バージョン 8 以降。  
- **IFC ファイルが格納されたフォルダー**。

## 名前空間のインポート

Java プロジェクトで必要なクラスをインポートします。

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## 手順ごとのガイド

### 手順 1: IFC ファイルの読み込み

```java
String dataDir = "Your Document Directory" + "ExportingIFC/";
String fileName = dataDir + "example.ifc";
IfcImage cadImage = (IfcImage)Image.load(fileName);
```

ここでは、ソース IFC ファイルを `IfcImage` オブジェクトに読み込みます。Aspose.CAD が自動的に IFC 構造を解析し、ラスタライズの準備を行います。

### 手順 2: ベクトル（ラスタライズ）オプションの設定

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

`CadRasterizationOptions` は 3 次元ジオメトリの平坦化方法を制御します。`PageWidth` と `PageHeight` を希望する PNG 解像度に合わせて調整します。数値が大きいほど高詳細画像になりますが、メモリ使用量も増加します。

### 手順 3: PNG エクスポート設定の構成

```java
PngOptions pngOptions = new PngOptions();
pngOptions.setVectorRasterizationOptions(vectorOptions);
```

`PngOptions` は Aspose.CAD に PNG ファイルを出力させ、前ステップで定義したラスタライズ設定と紐付けます。

### 手順 4: 画像を PNG として保存

```java
String outPath = dataDir + "example.png";
cadImage.save(outPath, pngOptions);
```

`save` メソッドがラスタライズされた画像をディスクに書き出します。この行が実行されると、ソース IFC ファイルと同じディレクトリに `example.png` が生成されます。

## よくある問題と解決策

| 問題 | 発生理由 | 対策 |
|------|----------|------|
| **空白の PNG が出力される** | ラスタライズオプションの幅/高さが 0 または極端に小さい | `PageWidth` と `PageHeight` を正の整数（例: 1500）に設定 |
| **レイヤーや色が欠落する** | デフォルトビューが特定レイヤーを非表示にしている | `vectorOptions.setRenderMode(CadRenderMode.Wireframe)` を使用するか、API でレイヤー可視性を調整 |
| **巨大な IFC ファイルでメモリ不足エラー** | 非常に高解像度に設定しているため RAM を大量消費 | 解像度を下げるか、モデルを分割して処理 |

## FAQ

### Q1: Aspose.CAD はすべての IFC バージョンに対応していますか？

A1: Aspose.CAD はさまざまな IFC バージョンをサポートしています。互換性の詳細は [ドキュメント](https://reference.aspose.com/cad/java/) をご参照ください。

### Q2: ラスタライズオプションをさらにカスタマイズできますか？

A2: もちろんです！高度なカスタマイズオプションは [ドキュメント](https://reference.aspose.com/cad/java/) で確認できます。

### Q3: トライアル版はありますか？

A3: はい、無料トライアル版は [こちら](https://releases.aspose.com/) から入手できます。

### Q4: Aspose.CAD の一時ライセンスはどこで取得できますか？

A4: 一時ライセンスは [このリンク](https://purchase.aspose.com/temporary-license/) から取得してください。

### Q5: サポートや議論の場はどこですか？

A5: コミュニティサポートは [Aspose.CAD フォーラム](https://forum.aspose.com/c/cad/19) でご利用いただけます。

## 追加のよくある質問

**Q: 複数の IFC ファイルをバッチで変換できますか？**  
A: はい。ファイルパスのリストをループで回し、読み込みと保存のロジックを繰り返すだけです。

**Q: PNG の背景色はどう変更しますか？**  
A: `vectorOptions.setBackgroundColor(Color.getWhite())`（または任意の `java.awt.Color`）を `PngOptions` 作成前に設定します。

**Q: JPEG や BMP など他のラスタ形式にもエクスポートできますか？**  
A: 可能です。`PngOptions` を `JpegOptions` や `BmpOptions` に置き換え、フォーマット固有の設定を調整してください。

**Q: 変換後にリソースを解放する必要がありますか？**  
A: 終了時に `cadImage.dispose()` を呼び出してネイティブメモリを解放してください。

---

**最終更新日:** 2025-12-21  
**テスト環境:** Aspose.CAD for Java 24.12（執筆時点での最新）  
**作成者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}