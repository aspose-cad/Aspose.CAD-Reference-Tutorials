---
date: 2026-01-10
description: Aspose.CAD for Java を使用して DGN ファイルから JPEG を作成する方法を学びましょう。このステップバイステップのチュートリアルでは、DGN
  を JPEG に効率的に変換する方法を示します。
linktitle: Exporting DGN in AutoCAD Format to Raster Image Format
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java を使用して DGN から JPEG を作成する方法
url: /ja/java/dgn-export-options/exporting-dgn-to-raster-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java を使用して DGN から JPEG を作成する

## はじめに

この包括的なガイドでは、数行の Java コードだけで **DGN から JPEG を作成** できます。バッチ変換ツールを構築する場合でも、CAD 図面を Web フレンドリーな画像として表示したい場合でも、DGN を JPEG に変換することは多くのエンジニアリングやデザインのワークフローで一般的な要件です。Aspose.CAD ライブラリのセットアップから最終的なラスタ画像の保存まで、すべての手順を順を追って解説しますので、すぐにご自身のアプリケーションに統合できます。

## クイック回答
- **必要なライブラリは何ですか？** Aspose.CAD for Java  
- **他の CAD フォーマットを JPEG に変換できますか？** はい、Aspose.CAD は多数のフォーマットをサポートしています（二次キーワード *convert cad to jpeg* を参照）  
- **本番環境でライセンスは必要ですか？** トライアル以外の使用には商用ライセンスが必要です  
- **サポートされている Java バージョンは？** Java 8 以降  
- **標準的な変換にかかる時間は？** 通常、標準サイズの図面で 1 秒未満です  

## 「DGN から JPEG を作成する」とは？
DGN ファイルから JPEG を作成するとは、ベクターベースの DGN 図面をピクセルベースの画像（JPEG）にラスタライズすることです。このプロセスは視覚的忠実度を保ちつつ、ブラウザやメール、レポートで CAD ソフトウェアなしで表示できる軽量ファイルを生成します。

## DGN を JPEG に変換する理由
- **簡単な共有:** JPEG はあらゆるデバイスで普遍的に閲覧可能です。  
- **パフォーマンス:** ラスタ画像は Web ページでベクタ CAD ファイルよりも高速に読み込まれます。  
- **互換性:** 多くの下流ツール（例: レポートエンジン）はラスタ形式のみを受け付けます。  

## 前提条件

開始する前に、以下を用意してください。

1. **Aspose.CAD ライブラリ** – 公式サイト **[here](https://releases.aspose.com/cad/java/)** からダウンロード。  
2. **Java Development Kit (JDK)** – Java 8 以降がインストールされていること。  
3. **IDE** – IntelliJ IDEA や Eclipse など、Java 対応の統合開発環境。  

## パッケージのインポート

Java クラスに必要なインポートを追加します:

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

## 手順ガイド

### 手順 1: DGN ファイルの読み込み

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
DgnImage dgnImage = (DgnImage) Image.load(dataDir + "Nikon_D90_Camera.dgn");
```

*説明:* `Image.load` メソッドはソース DGN ファイルを読み込み、後でラスタライズできる `DgnImage` オブジェクトを返します。

### 手順 2: JpegOptions オブジェクトの作成

```java
ImageOptionsBase options = new JpegOptions();
```

*説明:* `JpegOptions` は Aspose.CAD に出力形式が JPEG であることを指示し、ラスタライズ設定も付加できます。

### 手順 3: ラスタライズ設定の構成

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(600);
vectorOptions.setPageHeight(400);
vectorOptions.setNoScaling(true);
vectorOptions.setAutomaticLayoutsScaling(false);
options.setVectorRasterizationOptions(vectorOptions);
```

*説明:* これらのオプションは生成画像のサイズとスケーリング動作を定義します。目的の解像度に合わせて `PageWidth` と `PageHeight` を調整してください。

### 手順 4: 変換画像の保存

```java
OutputStream outStream = new FileOutputStream(dataDir + "ExportDGNToRasterImage_Out.jpg");
dgnImage.save(outStream, options);
```

*説明:* `save` メソッドはラスタライズされた JPEG を指定した出力ストリームに書き込みます。この手順が完了すれば、すぐに使用できる JPEG ファイルが得られます。

> **プロのヒント:** 変換コードを try‑with‑resources ブロックでラップすると、ストリームが自動的にクローズされ安全です。

## 一般的な使用例

- **サムネイルの生成** 用 CAD ファイルブラウザ向け。  
- **図面の埋め込み** PDF レポートや HTML ページへの埋め込み。  
- **自動バッチ処理** 設計アーカイブの一括変換。  

## トラブルシューティングと一般的な落とし穴

| 問題 | 原因 | 対策 |
|------|------|------|
| 画像が真っ白になる | ラスタライズオプションが不適切（例: `NoScaling` が true でページサイズが合わない） | `PageWidth`/`PageHeight` を調整するか、`NoScaling` を false に設定 |
| 大きな DGN ファイルでメモリ不足エラー | ストリーミングせずに非常に大きなファイルを読み込んでいる | JVM ヒープ (`-Xmx`) を増やすか、ファイルを小さなチャンクに分割して処理 |
| JPEG の画質が不足している | デフォルトの JPEG 品質が低い | 保存前に `((JpegOptions)options).setQuality(100);` を呼び出す |

## よくある質問

### Q1: Aspose.CAD for Java は他の CAD ファイル形式でも使用できますか？

A1: はい、Aspose.CAD は幅広いフォーマットをサポートしており、**CAD を JPEG に変換** だけでなく、さまざまなラスタまたはベクタ出力が可能です。

### Q2: Aspose.CAD for Java の無料トライアルはありますか？

A2: はい、無料トライアルは **[here](https://releases.aspose.com/)** から入手できます。

### Q3: Aspose.CAD for Java のドキュメントはどこで確認できますか？

A3: ドキュメントは **[here](https://reference.aspose.com/cad/java/)** にあります。

### Q4: Aspose.CAD for Java のサポートはどこで受けられますか？

A4: サポートフォーラムは **[here](https://forum.aspose.com/c/cad/19)** です。

### Q5: Aspose.CAD for Java のライセンスはどこで購入できますか？

A5: ライセンスは **[here](https://purchase.aspose.com/buy)** から購入できます。

## 結論

これで Aspose.CAD for Java を使用して **DGN から JPEG を作成** する方法を習得しました。上記の手順に従えば、デスクトップツール、Web サービス、または自動パイプラインなど、あらゆる Java アプリケーションに DGN‑to‑JPEG 変換をシームレスに組み込むことができます。

---

**最終更新日:** 2026-01-10  
**テスト環境:** Aspose.CAD for Java 24.11（執筆時点での最新）  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}