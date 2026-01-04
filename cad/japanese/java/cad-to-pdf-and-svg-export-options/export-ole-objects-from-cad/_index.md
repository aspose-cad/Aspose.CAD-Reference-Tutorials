---
date: 2026-01-04
description: Aspose.CAD for Java を使用して、CAD を PNG に保存し、CAD ファイルから OLE オブジェクトを簡単にエクスポートする方法を学びましょう。簡単なセットアップ、完全なコードサンプル、ベストプラクティスのヒントをご紹介します。
linktitle: Export OLE Objects from CAD
second_title: Aspose.CAD Java API
title: Aspose.CAD for JavaでCADをPNGとして保存し、OLEオブジェクトをエクスポートする
url: /ja/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD を PNG として保存し、Aspose.CAD for Java で OLE オブジェクトをエクスポートする

## はじめに

コンピュータ支援設計（CAD）の急速に変化する世界では、**CAD を PNG として保存**しながら埋め込み OLE（Object Linking and Embedding）オブジェクトを抽出できることが、ワークフローを大幅に効率化します。バッチ変換ツールの構築、Web ポータル用サムネイルの生成、または単に OLE コンテンツをアーカイブしたい場合でも、Aspose.CAD for Java はクリーンでプログラム的な方法を提供します。このチュートリアルでは、プロジェクトの設定から各 OLE オブジェクトを PNG 画像としてエクスポートするまでの全プロセスを順を追って解説します。

## クイック回答
- **OLE オブジェクトを直接 PNG にエクスポートできますか？** はい – Aspose.CAD は CAD ファイルを読み込み、各レイアウトを PNG にラスタライズできます。  
- **必要な Java バージョンは？** Java 8 以降。  
- **この機能にライセンスは必要ですか？** 評価用の無料トライアルで動作しますが、本番環境ではライセンスが必要です。  
- **ベクターデータは保持されますか？** PNG のラスタライズは視覚的忠実度を保ちますが、出力はラスタ画像でありベクターではありません。  
- **バッチ処理はサポートされていますか？** はい – コードサンプルに示すように、ファイル配列を反復処理できます。

## 前提条件

開始する前に、以下を用意してください。

- **Java Development Kit (JDK)** – Java 8+ がインストールされ、設定済みであること。  
- **Aspose.CAD for Java** – 最新ライブラリを [download link](https://releases.aspose.com/cad/java/) からダウンロード。  
- **CAD ソース ファイル** – OLE オブジェクトを含む任意の DWG/DXF/DGN ファイル。

## 名前空間のインポート

CAD ファイルを操作するには、コアの Aspose.CAD クラスをインポートする必要があります。チュートリアル後半で使用するクラスを提供するため、インポートブロックは以下の通り正確に保持してください。

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## CAD を PNG として保存する方法

以下は **OLE オブジェクトをエクスポートし、CAD を PNG として保存**する手順を簡潔に示したガイドです。各ステップには短い説明と、プロジェクトにコピーすべき正確なコードが含まれています。

### 手順 1: ドキュメント ディレクトリの設定

CAD 図面が格納されているフォルダーを定義します。プレースホルダーはご使用の環境に合わせて実際のパスに置き換えてください。

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

### 手順 2: CAD ファイル名の定義

処理したいすべての CAD ファイルを列挙します。必要に応じてエントリを追加できます。

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

### 手順 3: PNG エクスポート オプションの設定

ラスタライズ設定を構成します。ここでは特定のレイアウト（`Layout1`）を対象とし、デフォルトの PNG オプションを使用します。

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

### 手順 4: CAD ファイルを反復処理して PNG として保存

各 CAD ファイルを読み込み、OLE オブジェクトをラスタライズし、出力 PNG ファイルを書き出します。`_out.png` サフィックスは生成された画像を識別しやすくするためのものです。

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

## よくある問題と解決策

| 問題 | 発生理由 | 解決策 |
|------|----------|--------|
| **`Image.load` が `FileNotFoundException` をスロー** | `dataDir` パスが間違っている、またはファイル名にタイプミスがある。 | ディレクトリ文字列を再確認し、ファイル名が正確に一致しているか（スペース含む）確認してください。 |
| **出力 PNG が空白** | ソース CAD ファイルに指定したレイアウト名が存在しない。 | `cadImage.getLayouts()` で利用可能なレイアウトを一覧表示し、`rasterizationOptions.setLayouts(...)` を更新してください。 |
| **大規模 CAD ファイルで OutOfMemoryError が発生** | 高解像度画像のラスタライズに大量のヒープが必要になる。 | JVM ヒープサイズを増やす（例: `-Xmx2g`）か、`rasterizationOptions.setResolution(...)` で解像度を下げてください。 |

## FAQ

### Q1: Aspose.CAD はすべての CAD ファイル形式に対応していますか？

A1: Aspose.CAD は DWG、DXF、DGN などさまざまな CAD 形式をサポートしています。完全な一覧は [documentation](https://reference.aspose.com/cad/java/) を参照してください。

### Q2: OLE オブジェクトのエクスポート設定はカスタマイズできますか？

A2: はい、Aspose.CAD はエクスポート設定を細かくカスタマイズできる豊富なオプションを提供しており、特定の要件に合わせて出力を調整できます。

### Q3: Aspose.CAD の無料トライアルはありますか？

A3: はい、[here](https://releases.aspose.com/) から無料トライアルを取得して、機能をお試しいただけます。

### Q4: Aspose.CAD のコミュニティサポートはどこで受けられますか？

A4: [forum](https://forum.aspose.com/c/cad/19) に参加して、支援を求めたり経験を共有したりできます。

### Q5: Aspose.CAD のライセンスはどこで購入できますか？

A5: 開発ニーズに合わせたライセンスは [purchase page](https://purchase.aspose.com/buy) から入手してください。

## 結論

この 5 つのシンプルな手順に従うだけで、**CAD を PNG として保存**し、埋め込まれたすべての OLE オブジェクトを数行の Java コードで抽出できます。このアプローチはバッチ変換、自動レポート作成、または手動エクスポートなしで CAD コンテンツのラスタ画像が必要なあらゆるシナリオに最適です。品質やパフォーマンス要件に合わせて、さまざまなラスタライズオプションを試してみてください。

---

**最終更新:** 2026-01-04  
**テスト環境:** Aspose.CAD for Java 24.12（執筆時点での最新）  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}