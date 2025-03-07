---
title: Aspose.CAD を使用した Java DGN から JPEG への変換チュートリアル
linktitle: DGN を AutoCAD 形式でラスター イメージ形式にエクスポートする
second_title: Aspose.CAD Java API
description: Aspose.CAD を使用して Java で DGN ファイルを JPEG 画像にエクスポートする方法を学びます。このステップバイステップのチュートリアルでは、プロセスを簡単に進めることができます。
weight: 13
url: /ja/java/dgn-export-options/exporting-dgn-to-raster-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD を使用した Java DGN から JPEG への変換チュートリアル

## 導入

Aspose.CAD for Java を使用して DGN (デザイン) ファイルをラスター イメージ形式にエクスポートするためのこの包括的なチュートリアルへようこそ。 Aspose.CAD は、Java 開発者が CAD ファイルをシームレスに操作できるようにする強力なライブラリです。このチュートリアルでは、DGN ファイルを JPEG 画像に変換するプロセスを段階的に説明し、コード例を示します。

## 前提条件

チュートリアルに入る前に、次の前提条件が満たされていることを確認してください。
1.  Aspose.CAD ライブラリ: Aspose.CAD for Java ライブラリがインストールされていることを確認します。ダウンロードできます[ここ](https://releases.aspose.com/cad/java/).
2. Java Development Kit (JDK): マシンに Java がインストールされていることを確認してください。
3. 統合開発環境 (IDE): IntelliJ や Eclipse などの Java 互換 IDE を使用します。

## パッケージのインポート

Java プロジェクトで、Aspose.CAD に必要なパッケージをインポートします。コードに次の行を追加します。

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

## ステップ 1: DGN ファイルをロードする

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
DgnImage dgnImage = (DgnImage) Image.load(dataDir + "Nikon_D90_Camera.dgn");
```

## ステップ 2: JpegOptions オブジェクトを作成する

```java
ImageOptionsBase options = new JpegOptions();
```

## ステップ 3: ラスタライズ オプションを割り当てる

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(600);
vectorOptions.setPageHeight(400);
vectorOptions.setNoScaling(true);
vectorOptions.setAutomaticLayoutsScaling(false);
options.setVectorRasterizationOptions(vectorOptions);
```

## ステップ 4: 変換されたイメージを保存する

```java
OutputStream outStream = new FileOutputStream(dataDir + "ExportDGNToRasterImage_Out.jpg");
dgnImage.save(outStream, options);
```

特定の DGN ファイルに対してこれらの手順を繰り返し、それに応じてファイル パスを調整します。

## 結論

おめでとう！ Aspose.CAD for Java を使用して DGN ファイルをラスター イメージ形式にエクスポートする方法を学習しました。このチュートリアルでは、この機能を Java アプリケーションに組み込むための知識を習得しました。

## よくある質問

### Q1: Aspose.CAD for Java を他の CAD ファイル形式で使用できますか?

A1: はい、Aspose.CAD はさまざまな CAD 形式をサポートしており、Java 開発者に多用途のソリューションを提供します。

### Q2: Aspose.CAD for Java の無料トライアルはありますか?

 A2: はい、無料トライアルにアクセスできます。[ここ](https://releases.aspose.com/).

### Q3: Aspose.CAD for Java のドキュメントはどこで見つけられますか?

 A3: ドキュメントを参照してください。[ここ](https://reference.aspose.com/cad/java/).

### Q4: Aspose.CAD for Java のサポートを受けるにはどうすればよいですか?

 A4: サポート フォーラムにアクセスしてください。[ここ](https://forum.aspose.com/c/cad/19).

### Q5: Aspose.CAD for Java のライセンスはどこで購入できますか?

 A5: ライセンスを購入できます。[ここ](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
