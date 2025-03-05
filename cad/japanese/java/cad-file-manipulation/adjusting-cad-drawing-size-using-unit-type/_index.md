---
title: Aspose.CAD for Java でユニット タイプを使用して CAD 図面のサイズを調整する
linktitle: ユニットタイプを使用したCAD図面サイズの調整
second_title: Aspose.CAD Java API
description: CAD 図面のサイズを簡単に調整できる Aspose.CAD for Java の機能を試してください。精度と適応性については、ステップバイステップのガイドに従ってください。
type: docs
weight: 14
url: /ja/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/
---
## 導入

進化し続けるコンピュータ支援設計 (CAD) の分野では、精度と適応性が最も重要です。一般的な要件の 1 つは、特定のユニット タイプに基づいて CAD 図面のサイズを調整することです。 Aspose.CAD for Java は強力な味方として登場し、CAD ファイルをプログラムで操作するためのシームレスな機能を提供します。

## 前提条件

チュートリアルに入る前に、次の前提条件が満たされていることを確認してください。

- Java 開発環境: マシン上に機能する Java 開発環境がセットアップされていることを確認します。

-  Aspose.CAD for Java ライブラリ: Aspose.CAD ライブラリをダウンロードして、Java プロジェクトに統合します。ライブラリを入手できます[ここ](https://releases.aspose.com/cad/java/).

## 名前空間のインポート

Java コードには、Aspose.CAD 機能にアクセスするために必要な名前空間を含めます。次のインポートを追加します。

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

ここで、ユニット タイプを使用して CAD 図面のサイズを調整するプロセスを管理しやすい手順に分割してみましょう。

## ステップ 1: データ ディレクトリを定義する

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

CAD ファイルが配置されているディレクトリのパスを設定します。

## ステップ 2: CAD 図面をロードする

```java
String sourceFilePath = dataDir + "sample.dwg";
Image image = Image.load(sourceFilePath);
```

Aspose.CAD を使用して CAD 図面をロードします。`Image`クラス。

## ステップ 3: BMP オプションの作成

```java
BmpOptions bmpOptions = new BmpOptions();
```

インスタンス化します`BmpOptions`CAD レイアウトを BMP 形式にエクスポートするためのクラス。

## ステップ 4: ラスター化オプションを構成する

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

のインスタンスを作成します`CadRasterizationOptions`そしてそれを`BmpOptions`ベクトルラスタライズ用。

## ステップ 5: ユニットタイプを設定する

```java
cadRasterizationOptions.setUnitType(UnitType.Centimeter);
```

CAD 図面に必要な単位タイプを指定します。この例では、センチメートルに設定しています。

## ステップ 6: レイアウトを設定する

```java
cadRasterizationOptions.setLayouts(new String[] { "Model" });
```

エクスポート中に考慮されるレイアウトを定義します。この場合、「モデル」レイアウトを選択しました。

## ステップ 7: BMP にエクスポートする

```java
String outPath = sourceFilePath + ".bmp";
image.save(outPath, bmpOptions);
```

最後に、変更した CAD 図面を BMP 形式で保存します。

## 結論

Aspose.CAD for Java を使用すると、CAD 図面のサイズ調整が簡単になります。このチュートリアルでは、プロセスを順を追って説明し、正確な結果を達成するための各ステップの重要性を強調しました。

## よくある質問

### Q1: Aspose.CAD for Java を他のプログラミング言語で使用できますか?

A1: Aspose.CAD は主に Java をサポートしていますが、.NET などの他の言語で利用できるバージョンもあります。

### Q2: Aspose.CAD のライセンス オプションはありますか?

 A2: はい、ライセンス オプションを調べて、Aspose.CAD を購入できます。[ここ](https://purchase.aspose.com/buy).

### Q3: Aspose.CAD の無料トライアルはありますか?

 A3: 確かに、無料トライアルにアクセスできます。[ここ](https://releases.aspose.com/).

### Q4: Aspose.CAD for Java のサポートを受けるにはどうすればよいですか?

 A4: Aspose.CAD フォーラムにアクセスしてください。[ここ](https://forum.aspose.com/c/cad/19)総合的なサポートを目指します。

### Q5: Aspose.CAD の一時ライセンスを取得できますか?

 A5: はい、仮ライセンスを取得できます。[ここ](https://purchase.aspose.com/temporary-license/).