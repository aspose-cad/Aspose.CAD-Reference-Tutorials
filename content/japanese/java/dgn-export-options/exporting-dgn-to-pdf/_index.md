---
title: Aspose.CAD for Java を使用した DGN から AutoCAD PDF への簡単なエクスポート
linktitle: DGN を AutoCAD 形式で PDF にエクスポート
second_title: Aspose.CAD Java API
description: Aspose.CAD for Java を使用して DGN ファイルを PDF の AutoCAD 形式にエクスポートするためのステップバイステップ ガイドをご覧ください。 Java アプリケーションの CAD 処理機能を簡単に強化します。
type: docs
weight: 12
url: /ja/java/dgn-export-options/exporting-dgn-to-pdf/
---
## 導入

Aspose.CAD for Java を使用して DGN ファイルを AutoCAD 形式で PDF にエクスポートするための、この包括的なチュートリアルへようこそ。 Java アプリケーションの CAD ファイル処理機能を強化したい場合は、Aspose.CAD が最適です。このチュートリアルでは、DGN ファイルをエクスポートするプロセスを段階的に説明します。


## 前提条件
チュートリアルに入る前に、次の前提条件を満たしていることを確認してください。
-  Aspose.CAD ライブラリ: Java 用の Aspose.CAD ライブラリがインストールされていることを確認します。ダウンロードできます[ここ](https://releases.aspose.com/cad/java/).
- ドキュメント ディレクトリ: 入力ファイルと出力ファイルが保存されるドキュメント ディレクトリを設定します。

## パッケージのインポート

Java プロジェクトで、Aspose.CAD 機能にアクセスするために必要なパッケージをインポートします。

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

ここで、サンプル コードを複数のステップに分割してみましょう。

## ステップ 1: ファイル パスを定義する

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

「ドキュメント ディレクトリ」をファイルが存在する実際のパスに置き換えてください。

## ステップ 2: DGN イメージをロードする

```java
DgnImage objImage = (DgnImage) Image.load(fileName);
```

Aspose.CAD を使用して DGN ファイルをロードします。

## ステップ 3: PDF エクスポート オプションを設定する

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); //特定のビューをエクスポートする
options.setVectorRasterizationOptions(vectorOptions);
```

ページ寸法やレイアウト設定などの PDF エクスポート オプションを定義します。

## ステップ 4: PDF ファイルを保存する

```java
objImage.save(outFile, options);
```

エクスポートした PDF ファイルを保存します。

変換する必要がある追加の DGN ファイルについて、これらの手順を繰り返します。おめでとう！ Aspose.CAD for Java を使用して、DGN ファイルを PDF の AutoCAD 形式に正常にエクスポートできました。

## 結論

このチュートリアルでは、Aspose.CAD for Java を活用してアプリケーションの CAD ファイル処理機能を強化する方法を検討しました。わかりやすい手順とコード例を使用して、DGN ファイルを PDF の AutoCAD 形式にシームレスにエクスポートできるようになりました。

## よくある質問

### Q1: Aspose.CAD はすべての CAD ファイル形式と互換性がありますか?

A1: はい、Aspose.CAD は幅広い CAD 形式をサポートしており、さまざまなファイル タイプを処理する際の汎用性を確保しています。

### Q2: PDF エクスポート設定をカスタマイズできますか?

A2: もちろんです。チュートリアルで示されているように、要件に合わせてページの寸法やレイアウトなどのオプションを調整できます。

### Q3: 追加のサポートや支援はどこで入手できますか?

 A3: にアクセスしてください。[Aspose.CAD フォーラム](https://forum.aspose.com/c/cad/19)コミュニティのサポートとディスカッションのために。

### Q4: 無料トライアルはありますか?

 A4: はい、無料トライアルにアクセスできます。[ここ](https://releases.aspose.com/).

### Q5: 仮免許はどうやって取得できますか?

 A5: 仮免許を取得する[ここ](https://purchase.aspose.com/temporary-license/).