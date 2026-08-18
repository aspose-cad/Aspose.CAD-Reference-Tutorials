---
date: 2026-02-23
description: Aspose.CAD for Java を使用して DWFX を PDF に変換し、CAD を PDF として保存する方法を学びましょう。DWFX
  ファイルを開き、PDF を生成するためのクイックガイドです。
linktitle: Open DWFX File
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java を使用して DWFX を PDF に変換
url: /ja/java/cad-file-manipulation/open-dwfx-file/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWFX を PDF に変換する（Aspose.CAD for Java）

## はじめに

今日の急速に変化するデザイン業界では、開発者はしばしば **DWFX を PDF に変換** して、CAD 図面を非技術的な関係者と共有する必要があります。Aspose.CAD for Java を使用すれば、この作業はシンプルになり、DWFX ファイルを開いてラスタライズし、**CAD を PDF として保存** することが数行のコードで可能です。このチュートリアルでは、環境設定から最終 PDF の検証まで、プロセス全体を順を追って説明しますので、Java アプリケーションで DWFX ファイルを自信を持って扱えるようになります。

## クイック回答
- **このガイドの主な目的は何ですか？** Aspose.CAD for Java を使用して DWFX を PDF に変換する方法を示すことです。  
- **必要なライブラリはどれですか？** Aspose.CAD for Java（公式 Aspose サイトからダウンロード）。  
- **ライセンスは必要ですか？** 開発用途では無料トライアルで動作しますが、本番環境では商用ライセンスが必要です。  
- **DWFX ファイルを直接開くことはできますか？** はい、`Image.load` を使用して DWFX ファイルを開きます。  
- **サンプルの出力形式は何ですか？** 指定した出力ディレクトリに保存される PDF ファイルです。

## “DWFX を PDF に変換” とは何ですか？

DWFX を PDF に変換するとは、Autodesk 製品で一般的に使用されるベクターベースの DWFX 図面を取得し、ポータブルで広くサポートされている PDF ドキュメントにレンダリングすることを意味します。これにより、受取側に CAD ソフトウェアがなくても、簡単に閲覧、印刷、共有が可能になります。

## なぜ Aspose.CAD for Java を使用して **CAD を PDF として保存** するのか？

- **外部依存なし:** 純粋な Java API で、ネイティブ CAD エンジンは不要です。  
- **高忠実度レンダリング:** 線幅、色、レイヤーを保持します。  
- **バッチ処理に適した:** サーバー側の自動化やクラウドサービスに最適です。  
- **クロスプラットフォーム:** Windows、Linux、macOS で動作します。

## 前提条件

コードに入る前に、以下が揃っていることを確認してください。

- **Aspose.CAD for Java ライブラリ** – [Aspose.CAD for Java ダウンロードページ](https://releases.aspose.com/cad/java/) からダウンロードしてください。  
- **Java 開発環境** – JDK 8 以上、お好みの IDE またはビルドツール。  
- **DWFX ファイル** – 変換テスト用のサンプル DWFX ファイル（例: `Tyrannosaurus.dwfx`）。

## 名前空間のインポート

まず、必要なクラスをインポートします。

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Aspose.CAD for Java を使用して DWFX を PDF に変換する方法

以下にステップバイステップの解説を示します。各ステップには簡単な説明と、実際に実行するコードが含まれています。

### 手順 1: DWFX ファイルの読み込み  

```java
String SourceDir = Utils.getDataDir_DWFXDrawings();
String OutputDir = Utils.getDataDir_Output();
String filePath = SourceDir + "Tyrannosaurus.dwfx";

Image cadImageDwf = Image.load(filePath);
```

`Image.load` メソッドは DWFX ファイルをメモリに読み込み、ラスタライズの準備ができた `CadImage` オブジェクトを取得します。

### 手順 2: ラスタライズオプションの設定  

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(cadImageDwf.getSize().getWidth());
rasterizationOptions.setPageHeight(cadImageDwf.getSize().getHeight());
```

これらのオプションは出力ページサイズを定義し、PDF が元の図面サイズと一致するようにします。

### 手順 3: PDF オプションの構成  

```java
PdfOptions CADf = new PdfOptions();
CADf.setVectorRasterizationOptions(rasterizationOptions);
```

ここでは、ラスタライズ設定を PDF エクスポート構成にバインドします。

### 手順 4: PDF として保存  

```java
cadImageDwf.save(OutputDir + "OpenDwfxFile_out.pdf", CADf);
```

`save` を呼び出すことで、レンダリングされた画像が出力フォルダー内の PDF ファイルとして書き込まれます。

### 手順 5: 成功の確認  

```java
System.out.println("OpenDwfxFile executed successfully");
```

シンプルなコンソールメッセージで、変換がエラーなく完了したことが確認できます。

## よくある問題と解決策

| 問題 | 考えられる原因 | 解決策 |
|-------|--------------|----------|
| **PDF が空白** | ラスタライズの幅/高さが 0 に設定されている | `cadImageDwf.getSize()` が有効な寸法を返すことを確認してからオプションを設定してください。 |
| **メモリ不足エラー** | 非常に大きな DWFX ファイル | JVM のヒープサイズを増やす（`-Xmx2g`）か、ファイルを小さいセクションに分割して処理してください。 |
| **フォントが見つからない** | 元の DWFX にフォントが埋め込まれていない | サーバーに必要なフォントをインストールするか、`CadRasterizationOptions.setFontName` を使用して代替フォントを指定してください。 |

## よくある質問

### Q1: Aspose.CAD for Java を他の CAD ファイル形式でも使用できますか？

A1: はい、Aspose.CAD for Java は幅広い CAD 形式をサポートしており、開発者にとって汎用的なソリューションを提供します。

### Q2: Aspose.CAD for Java の無料トライアルは利用できますか？

A2: はい、Aspose.CAD for Java の機能を無料トライアルで試すことができます。[このリンク](https://releases.aspose.com/) から開始してください。

### Q3: Aspose.CAD for Java のサポートはどのように受けられますか？

A3: 支援や協力を得るために、[サポートフォーラム](https://forum.aspose.com/c/cad/19) の Aspose.CAD コミュニティに参加してください。

### Q4: Aspose.CAD for Java の一時ライセンスは利用できますか？

A4: はい、Aspose.CAD for Java の一時ライセンスを取得できます。詳細は[このリンク](https://purchase.aspose.com/temporary-license/)をご覧ください。

### Q5: Aspose.CAD for Java のドキュメントはどこで見つけられますか？

A5: 包括的なドキュメントは[こちら](https://reference.aspose.com/cad/java/)で入手できます。

---

**最終更新日:** 2026-02-23  
**テスト環境:** Aspose.CAD for Java 24.11  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}