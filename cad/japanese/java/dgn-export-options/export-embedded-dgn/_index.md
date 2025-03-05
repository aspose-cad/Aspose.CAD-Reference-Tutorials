---
title: Aspose.CAD for Java を使用して埋め込み DGN を PDF にエクスポート
linktitle: 埋め込みDGNのエクスポート
second_title: Aspose.CAD Java API
description: Aspose.CAD for Java を使用して埋め込み DGN ファイルを PDF にエクスポートするためのステップバイステップ ガイドをご覧ください。シームレスな CAD ファイル操作により Java アプリケーションを強化します。
type: docs
weight: 11
url: /ja/java/dgn-export-options/export-embedded-dgn/
---
## 導入

Aspose.CAD for Java を使用して埋め込み DGN ファイルをエクスポートするためのこの包括的なチュートリアルへようこそ。 Aspose.CAD は、Java 開発者が CAD ファイルをシームレスに操作できるようにする強力なライブラリです。このチュートリアルでは、埋め込み DGN ファイルを PDF にエクスポートするプロセスをステップごとに説明します。経験豊富な開発者であっても、初心者であっても、このチュートリアルは、Aspose.CAD の機能を活用して Java アプリケーションを強化するのに役立ちます。

## 前提条件

チュートリアルに入る前に、次の前提条件を満たしていることを確認してください。
- Java 開発環境: マシン上に Java 開発環境がセットアップされていることを確認します。
-  Aspose.CAD for Java: Aspose.CAD for Java ライブラリをダウンロードしてインストールします。[ここ](https://releases.aspose.com/cad/java/).

## パッケージのインポート

まず、必要なパッケージを Java プロジェクトにインポートする必要があります。次の import ステートメントをコードに追加します。

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

ここで、サンプル コードを複数のステップに分割してみましょう。

## ステップ 1: 入力パスと出力パスを設定する

ドキュメントが存在するディレクトリ パスを定義し、入力 DWG ファイル名を指定します。

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

## ステップ 2: DWG ファイルをロードする

 DWG ファイルを`Image`Aspose.CAD を使用してオブジェクトを作成します。

```java
Image objImage = Image.load(fileName);
```

## ステップ 3: ラスター化オプションを構成する

エクスポートに含めるレイアウトなどのラスタライズ オプションを構成します。

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

## ステップ 4: PDF オプションを構成する

ベクトル ラスタライズ オプションを含む PDF オプションを設定します。

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## ステップ 5: PDF ファイルを保存する

設定したオプションを使用して PDF ファイルを保存します。
```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## 結論

おめでとう！ Aspose.CAD for Java を使用して、埋め込み DGN ファイルを PDF にエクスポートすることができました。このチュートリアルでは、効率的な CAD ファイル操作のために Aspose.CAD を Java アプリケーションに統合するための重要な手順について説明しました。

## よくある質問

### Q1: Aspose.CAD for Java を商用プロジェクトで使用できますか?

 A1: はい、Aspose.CAD for Java は商用ライブラリです。からライセンスを取得できます[ここ](https://purchase.aspose.com/buy).

### Q2:無料トライアルはありますか?

 A2:はい、Aspose.CAD for Java の無料トライアルにアクセスできます。[ここ](https://releases.aspose.com/).

### Q3: Aspose.CAD for Java のサポートを受けるにはどうすればよいですか?

A3: Aspose.CAD コミュニティからサポートを求めることができます。[フォーラム](https://forum.aspose.com/c/cad/19).

### Q4: 一時ライセンスが必要な場合はどうすればよいですか?

 A4: 仮免許を取得できます。[ここ](https://purchase.aspose.com/temporary-license/).

### Q5: ドキュメントはどこで入手できますか?

 A5: ドキュメントは入手可能です[ここ](https://reference.aspose.com/cad/java/).