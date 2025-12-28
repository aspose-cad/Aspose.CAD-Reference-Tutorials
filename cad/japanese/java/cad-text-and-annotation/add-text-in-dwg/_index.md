---
date: 2025-12-28
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

DWG ファイルから **PDF を作成** し、カスタムテキストを挿入したい場合は、ここが最適です。このチュートリアルでは、DWG 図面の読み込み、テキストアノテーションの追加、そして最終的に Aspose.CAD for Java を使用して PDF として保存するまでの全工程を解説します。最後まで読むと、**DWG を PDF として保存** する方法、テキスト高さのカスタマイズ、基本的なアノテーションの追加方法が理解できます。

## クイック回答
- **Java で DWG を PDF に変換できますか？** はい、Aspose.CAD for Java はシンプルな API を提供します。  
- **本番環境で使用するにはライセンスが必要ですか？** 商用ライセンスが必要です。無料トライアルも利用可能です。  
- **DWG にテキストを追加するメソッドはどれですか？** `CadText` オブジェクトを使用し、モデル空間に追加します。  
- **テキストの高さを設定できますか？** もちろんです。`CadText` インスタンスの `setTextHeight()` を使用します。  
- **出力はベクターベースですか？** ラスタライズオプションを `UseObjectColor` に設定すると、PDF は高品質なベクターデータを保持します。

## 前提条件

チュートリアルに入る前に、以下の前提条件が整っていることを確認してください。

- Aspose.CAD for Java ライブラリ: [Aspose.CAD for Java ページ](https://releases.aspose.com/cad/java/) からダウンロードしてインストールしてください。  
- Java Development Kit (JDK): システムに最新の JDK がインストールされていることを確認してください。  
- DWG 図面: テキストを追加したい DWG 図面ファイルを用意してください。

## 名前空間のインポート

Java コードで Aspose.CAD に必要な名前空間をインポートします。

```java
import com.aspose.cad.Image;


import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

次に、提供されたコードスニペットを複数のステップに分解して説明します。

## ステップ 1: ドキュメントディレクトリと DWG ファイルパスの設定

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String dwgPathToFile = dataDir + "SimpleEntites.dwg";
```

## ステップ 2: DWG 画像の読み込み

```java
Image image = Image.load(dwgPathToFile);
```

## ステップ 3: CadText オブジェクトの作成 (DWG にテキストを追加)

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

## ステップ 4: CadImage にテキストを追加 (アノテーションの挿入)

```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadText);
```

## ステップ 5: PDF オプションの設定 (DWG から PDF を作成する準備)

```java
PdfOptions pdfOptions = new PdfOptions();
```

## ステップ 6: CadRasterizationOptions の構成 (PDF レンダリングの制御)

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

## ステップ 7: 変更した DWG を PDF として保存 (dwg to pdf java)

```java
image.save(dataDir + "SimpleEntites_generated.dwg.pdf", pdfOptions);
```

これらの手順に従うことで、**DWG から PDF を作成** し、カスタムテキストを追加し、テキスト高さを制御できるようになります—すべて数行の Java コードで実現できます。

## なぜ DWG にテキストを追加して PDF に変換するのか？

DWG ファイルに直接テキストを追加することは、次のようなシナリオで有用です。

- **設計に注釈や部品番号を付ける**  
- **PDF を読み取り専用で広くサポートされた形式として、印刷可能なドキュメントを作成する**  
- **手動編集なしで大規模 CAD ライブラリのバッチ処理を自動化する**

## よくある問題とヒント

- **テキストが表示されない場合:** X/Y 座標が図面の範囲内にあり、レイヤーが表示されているか確認してください。  
- **テキスト高さが正しくない場合:** `setTextHeight()` を調整してください。値は図面の単位系です。  
- **PDF がラスタライズされて見える場合:** ベクトル情報を保持するために `CadDrawTypeMode.UseObjectColor` が設定されているか確認してください。  
- **大きなファイルのパフォーマンス:** 必要に応じて `pageHeight`/`pageWidth` を増やしてください。値が大きいほどメモリ消費が増えます。

## よくある質問

**Q: Aspose.CAD はすべてのバージョンの DWG ファイルに対応していますか？**  
A: Aspose.CAD はさまざまなバージョンの DWG ファイルをサポートしており、幅広い CAD ソフトウェアとの互換性を確保しています。

**Q: 追加したテキストのフォントや書式をカスタマイズできますか？**  
A: はい、Aspose.CAD を使用して DWG ファイルに追加するテキストのフォント、スタイル、その他の書式設定オプションをカスタマイズできます。

**Q: Aspose.CAD for Java の無料トライアルは利用できますか？**  
A: はい、[こちら](https://releases.aspose.com/) から無料トライアルを取得して、Aspose.CAD の機能をお試しいただけます。

**Q: Aspose.CAD for Java の詳細なドキュメントはどこで見つけられますか？**  
A: 詳細情報やサンプルは、ドキュメント [こちら](https://reference.aspose.com/cad/java/) を参照してください。

**Q: Aspose.CAD のサポートやヘルプはどこで受けられますか？**  
A: [Aspose.CAD フォーラム](https://forum.aspose.com/c/cad/19) で支援を受け、コミュニティとつながることができます。

---

**最終更新日:** 2025-12-28  
**テスト環境:** Aspose.CAD for Java 24.12  
**作成者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}