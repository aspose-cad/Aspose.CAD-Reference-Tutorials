---
date: 2026-02-28
description: Aspose.CAD for Java を使用して、DWG から PDF を作成し、DWG を PDF として保存し、DWG 図面にテキストを追加する方法をステップバイステップで学びましょう。
linktitle: Add Text in DWG
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java を使用して DWG から PDF を作成し、テキストを追加する
url: /ja/java/cad-text-and-annotation/add-text-in-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java を使用して DWG から PDF を作成しテキストを追加する

## はじめに

DWG ファイルから **PDF を作成** し、カスタムテキストを挿入する必要がある場合は、ここが適切な場所です。このチュートリアルでは、DWG 図面の読み込み、テキスト注釈の追加、そして最終的に Aspose.CAD for Java を使用して結果を PDF として保存するまでの全工程を順に解説します。最後までで、**DWG を PDF として保存** する方法、テキストの高さのカスタマイズ、基本的な注釈の追加方法が理解できるようになります。

## クイック回答
- **Java で DWG を PDF に変換できますか？** はい、Aspose.CAD for Java はシンプルな API を提供しています。  
- **本番環境で使用するにはライセンスが必要ですか？** 商用ライセンスが必要です。無料トライアルも利用可能です。  
- **DWG にテキストを追加するメソッドはどれですか？** `CadText` オブジェクトを使用し、モデル空間に追加します。  
- **テキストの高さを設定できますか？** もちろんです。`CadText` インスタンスの `setTextHeight()` を使用します。  
- **出力はベクターベースですか？** ラスタライズオプションを `UseObjectColor` に設定すると、PDF は高品質なベクターデータを保持します。

## “DWG から PDF を作成” とは何ですか？

DWG 図面から PDF を作成することは、ネイティブな CAD フォーマットを広くサポートされる読み取り専用ドキュメントに変換し、元のジオメトリを保持することを意味します。この変換は、CAD ソフトウェアを持たない関係者と設計を共有する必要がある場合に不可欠です。

## なぜ Aspose.CAD for Java を使用して DWG を PDF に変換するのか？

Aspose.CAD は外部の CAD インストールを必要としない純粋な Java ソリューションを提供します。**DWG を PDF に変換** をサポートし、ベクトルの忠実度を維持し、変換前にテキスト、寸法、カスタムグラフィックなどの注釈をプログラムで追加できます。

## 前提条件

チュートリアルに入る前に、以下の前提条件が整っていることを確認してください：

- Aspose.CAD for Java Library: Download and install the library from the [Aspose.CAD for Java page](https://releases.aspose.com/cad/java/).
- Java Development Kit (JDK): Make sure you have the latest JDK installed on your system.
- DWG Drawing: Prepare a DWG drawing file where you want to add text.

## 名前空間のインポート

Java コードで Aspose.CAD に必要な名前空間をインポートします:

```java
import com.aspose.cad.Image;


import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Now, let's break down the code snippet provided into multiple steps:

## Step 1: Set up Document Directory and DWG File Path

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String dwgPathToFile = dataDir + "SimpleEntites.dwg";
```

## Step 2: Load DWG Image

```java
Image image = Image.load(dwgPathToFile);
```

## Step 3: Create CadText Object (Add Text to DWG)

```java
CadText cadText = new CadText();
cadText.setStyleType("Standard");
cadText.setDefaultValue("Some custom text");
cadText.setColorId(256);
cadText.setLayerName("0");
cadText.getFirstAlignment().setX(47.9);
cadText.getFirstAlignment().setY(5.56);
cadText.setTextHeight(0.8);          // set text height in DWG units
cadText.setScaleX(0);
```

## Step 4: Add Text to CadImage (Insert Annotation)

```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadText);
```

## Step 5: Set Up PDF Options (Prepare to create PDF from DWG)

```java
PdfOptions pdfOptions = new PdfOptions();
```

## Step 6: Configure CadRasterizationOptions (Control PDF rendering)

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

## Step 7: Save the Modified DWG as PDF (dwg to pdf java)

```java
image.save(dataDir + "SimpleEntites_generated.dwg.pdf", pdfOptions);
```

これらの手順に従うことで、**DWG から PDF を作成** し、カスタムテキストを追加し、テキストの高さを制御できるようになります—すべて数行の Java コードで実現できます。

## 大規模に Java で DWG を PDF に変換する方法は？

**DWG PDF をバッチ変換** する必要がある場合は、上記コードをループで囲み、DWG 図面が格納されたフォルダーを反復処理します。メモリ使用量を抑えるために `pageHeight`/`pageWidth` は必要なときだけ調整し、各ファイルで同じ `PdfOptions` インスタンスを再利用してパフォーマンスを向上させます。

## よくある問題とヒント

- **テキストが表示されませんか？** X/Y 座標が図面の範囲内にあり、レイヤーが表示されていることを確認してください。
- **テキストの高さが正しくありませんか？** `setTextHeight()` を調整してください。値は図面の単位系です。
- **PDF がラスタライズされて見えますか？** ベクトル情報を保持するために `CadDrawTypeMode.UseObjectColor` が設定されていることを確認してください。
- **大きなファイルのパフォーマンスは？** 必要に応じて `pageHeight`/`pageWidth` を増やしてください。値が大きいほどメモリ消費が増えます。

## Frequently Asked Questions

**Q: Aspose.CAD はすべてのバージョンの DWG ファイルと互換性がありますか？**  
A: Aspose.CAD はさまざまなバージョンの DWG ファイルをサポートしており、幅広い CAD ソフトウェアとの互換性を確保しています。

**Q: 追加したテキストのフォントや書式をカスタマイズできますか？**  
A: はい、Aspose.CAD を使用して DWG ファイルに追加するテキストのフォント、スタイル、その他の書式設定オプションをカスタマイズできます。

**Q: Aspose.CAD for Java の無料トライアルは利用可能ですか？**  
A: はい、[here](https://releases.aspose.com/) から無料トライアルを取得して Aspose.CAD の機能を体験できます。

**Q: Aspose.CAD for Java の詳細なドキュメントはどこで見つけられますか？**  
A: 詳細情報やサンプルはドキュメント [here](https://reference.aspose.com/cad/java/) を参照してください。

**Q: Aspose.CAD のサポートやヘルプはどこで受けられますか？**  
A: [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) で支援を受け、コミュニティとつながることができます。

---

**最終更新日:** 2026-02-28  
**テスト済みバージョン:** Aspose.CAD for Java 24.12  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}