---
title: Aspose.CAD for Java を使用して IFC を PNG にエクスポート
linktitle: IFC を PNG にエクスポート
second_title: Aspose.CAD Java API
description: Aspose.CAD for Java を使用して、IFC を PNG に簡単に変換します。ステップバイステップのチュートリアルに従ってください。
type: docs
weight: 18
url: /ja/java/cad-export-options/export-ifc-to-png/
---
## 導入

Aspose.CAD for Java を使用して IFC (Industry Foundation Classes) を PNG にエクスポートするためのこのステップバイステップのチュートリアルへようこそ。 Aspose.CAD は、IFC 形式を含む CAD ファイルを操作するための広範な機能を提供する強力な Java ライブラリです。このチュートリアルでは、IFC ファイルを PNG 画像に変換するプロセスを、各ステップの詳細な説明とともに説明します。

## 前提条件

始める前に、次の前提条件が満たされていることを確認してください。

-  Aspose.CAD ライブラリ: Java 用の Aspose.CAD ライブラリを次の場所からダウンロードしてインストールします。[ダウンロードリンク](https://releases.aspose.com/cad/java/).

- ドキュメント ディレクトリ: IFC ファイルが配置されるシステム上にディレクトリを準備します。

## 名前空間のインポート

Java プロジェクトで、以下に示すように必要な名前空間をインポートします。

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## ステップ 1: IFC ファイルをロードする

```java
String dataDir = "Your Document Directory" + "ExportingIFC/";
String fileName = dataDir + "example.ifc";
IfcImage cadImage = (IfcImage)Image.load(fileName);
```

この手順には、Aspose.CAD を使用して IFC ファイルをロードすることが含まれます。

## ステップ 2: ベクトル オプションを設定する

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

ページの幅と高さを指定して、ラスタライズのベクトル オプションを構成します。

## ステップ 3: PNG オプションを設定する

```java
PngOptions pngOptions = new PngOptions();
pngOptions.setVectorRasterizationOptions(vectorOptions);
```

ベクター ラスタライズ オプションを含む PNG オプションを設定します。

## ステップ 4: PNG として保存

```java
String outPath = dataDir + "example.png";
cadImage.save(outPath, pngOptions);
```

加工した画像をPNG形式で保存します。

## 結論

おめでとう！ Aspose.CAD for Java を使用して、IFC ファイルを PNG に正常に変換しました。このチュートリアルでは、この機能をプロジェクトにシームレスに統合できるようにするための包括的なガイドを提供しました。

## よくある質問

### Q1: Aspose.CAD は、IFC ファイルのすべてのバージョンと互換性がありますか?

 A1: Aspose.CAD は、さまざまなバージョンの IFC ファイルをサポートしています。を参照してください。[ドキュメンテーション](https://reference.aspose.com/cad/java/)互換性の詳細については。

### Q2: ラスタライズ オプションをさらにカスタマイズできますか?

 A2: もちろんです！を探索してください[ドキュメンテーション](https://reference.aspose.com/cad/java/)高度なカスタマイズ オプションについては、

### Q3: 体験版はありますか?

A3: はい、無料試用版にアクセスできます。[ここ](https://releases.aspose.com/).

### Q4: Aspose.CAD の一時ライセンスを取得するにはどうすればよいですか?

 A4: から一時ライセンスを取得します。[このリンク](https://purchase.aspose.com/temporary-license/).

### Q5: どこに助けを求めたり、問題について相談したりできますか?

A5: にアクセスしてください。[Aspose.CAD フォーラム](https://forum.aspose.com/c/cad/19)コミュニティサポートのために。
