---
title: CAD 図面に透かしを追加する - Aspose.CAD for Java チュートリアル
linktitle: 透かしを追加する
second_title: Aspose.CAD Java API
description: Aspose.CAD for Java を使用して、パーソナライズされたウォーターマークで CAD 図面を強化します。シームレスな統合については、ステップバイステップのガイドに従ってください。
weight: 12
url: /ja/java/other-cad-operations/add-watermark/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD 図面に透かしを追加する - Aspose.CAD for Java チュートリアル

## 導入

Aspose.CAD for Java を使用して CAD 図面にウォーターマークを追加するためのこの包括的なガイドへようこそ。このチュートリアルでは、ウォーターマークを効率的に統合し、パーソナライズされたメッセージやブランドで CAD ドキュメントを強化する方法を学びます。 Aspose.CAD for Java は強力な機能セットを提供し、ウォーターマークの追加プロセスを簡単にします。

## 前提条件

チュートリアルに入る前に、次の前提条件を満たしていることを確認してください。

-  Aspose.CAD for Java: Java 環境に Aspose.CAD ライブラリがインストールされていることを確認してください。ダウンロードできます[ここ](https://releases.aspose.com/cad/java/).
- Java Development Kit (JDK): 最新バージョンの JDK がシステムにインストールされていることを確認してください。

## パッケージのインポート

Java プロジェクトに、必要な Aspose.CAD パッケージをインポートして開始します。

```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.Cad3DPoint;
import com.aspose.cad.fileformats.cad.cadobjects.CadMText;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## ステップ 1: 新しいマルチテキストを追加する

```java
//新しいマルチテキストを追加
CadMText watermark = new CadMText();
watermark.setText("Watermark message");
watermark.setInitialTextHeight(40);
watermark.setInsertionPoint(new Cad3DPoint(300, 40));
watermark.setLayerName("0");
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(watermark);
```

## ステップ 2: テキストなどの単純なエンティティを追加する

テキストのようなより単純なエンティティを追加することもできます。

```java
//または、テキストなどのより単純なエンティティを追加します
CadText text = new CadText();
text.setDefaultValue("Watermark text");
text.setTextHeight(40);
text.setFirstAlignment(new Cad3DPoint(300, 40));
text.setLayerName("0") ;
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(text);
```

## ステップ 3: PDF にエクスポートする

ウォーターマークを追加した CAD 図面を PDF ファイルにエクスポートします。

```java
// PDFにエクスポート
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setLayouts(new String[]{"Model"});
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
cadImage.save(dataDir + "AddWatermark_out.pdf", pdfOptions);

```

## 結論

おめでとう！ Aspose.CAD for Java を使用して、CAD 図面に透かしを追加することに成功しました。このシンプルかつ強力なプロセスにより、デザインをパーソナライズしたり、ブランド化して保護したりできます。

## よくある質問

### Q1: Aspose.CAD はすべての CAD ファイル形式と互換性がありますか?

A1: Aspose.CAD は、DWG、DXF、DWT、DWF などのさまざまな CAD 形式をサポートしています。

### Q2: 透かしテキストの外観をカスタマイズできますか?

A2: はい、テキストのサイズ、色、位置など、透かしの外観を完全に制御できます。

### Q3: Aspose.CAD for Java の試用版はありますか?

 A3: はい、試用版をダウンロードできます。[ここ](https://releases.aspose.com/).

### Q4: Aspose.CAD のサポートを受けるにはどうすればよいですか?

 A4: にアクセスしてください。[Aspose.CAD フォーラム](https://forum.aspose.com/c/cad/19)コミュニティサポートのために。

### Q5: Aspose.CAD for Java の完全なドキュメントはどこで見つけられますか?

 A5: を参照してください。[ドキュメンテーション](https://reference.aspose.com/cad/java/)詳細については。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
