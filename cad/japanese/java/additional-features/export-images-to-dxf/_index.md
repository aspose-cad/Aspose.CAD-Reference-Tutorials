---
title: Aspose.CAD for Java を使用してイメージを DXF 形式にエクスポートする
linktitle: Java を使用して画像を DXF 形式にエクスポートする
second_title: Aspose.CAD Java API
description: Aspose.CAD for Java を使用して画像を DXF 形式にエクスポートするシームレスなプロセスを確認してください。ステップバイステップガイド、よくある質問など。
weight: 15
url: /ja/java/additional-features/export-images-to-dxf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java を使用してイメージを DXF 形式にエクスポートする

## 導入

Aspose.CAD for Java を使用してイメージを DXF 形式にエクスポートするための包括的なチュートリアルへようこそ。 Aspose.CAD は、開発者がプログラムで CAD 図面を操作できるようにする強力な Java ライブラリです。このチュートリアルでは、画像を DXF 形式にエクスポートするプロセスを説明し、このタスクを達成するためのさまざまな手順とテクニックを示します。

## 前提条件

始める前に、以下のものがあることを確認してください。

- Java プログラミングの基本的な理解。
-  Aspose.CAD for Java ライブラリがインストールされています。ダウンロードできます[ここ](https://releases.aspose.com/cad/java/).
- Aspose.CAD の有効なライセンスまたは一時ライセンス。入手してください[ここ](https://purchase.aspose.com/temporary-license/).
- テスト用の DXF 形式のサンプル画像。

## 名前空間のインポート

Java プロジェクトで、Aspose.CAD に必要な名前空間をインポートします。

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadconsts.CadEntityTypeName;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject;
import java.io.File;
import static java.lang.System.in;
```

## ステップ 1: ドキュメントごとに新しいフォントを設定する

```java
//リソース ディレクトリへのパス。
String dataDir = "Your Document Directory" + "DXFDrawings/";

File[] files = new File(dataDir).listFiles();
for (File file : files) {
    String extension = GetFileExtension(file);
    if (extension.equals(".dxf")) {
        CadImage cadImage = (CadImage)Image.load(file.getName());
        for (Object style : cadImage.getStyles()) {
            ((CadStyleTableObject)style).setPrimaryFontName("Broadway");
        }
        cadImage.save(file.getName() + "_font.dxf");
    }
}
```

## ステップ 2: すべての「直線」を非表示にする

```java
CadImage cadImageEntity = (CadImage)Image.load(file.getName());
for (CadBaseEntity entity : cadImageEntity.getEntities()) {
    if (entity.getTypeName() == CadEntityTypeName.LINE) {
        entity.setVisible((short)0);
    }
}
cadImageEntity.save(file.getName() + "_lines.dxf");
```

## ステップ 3: テキストを使用した操作

```java
CadImage cadImageText = (CadImage)Image.load(file.getName());
for (CadBaseEntity entity : cadImageText.getEntities()) {
    if (entity.getTypeName() == CadEntityTypeName.TEXT) {
        ((CadText)entity).setDefaultValue("New text here!!! :)");
        break;
    }
}
cadImageText.save(file.getName() + "_text.dxf");
```

ディレクトリ内の DXF ファイルごとにこれらの手順を繰り返します。

## 結論

おめでとう！ Aspose.CAD for Java を使用して画像を DXF 形式にエクスポートする方法を学習しました。このチュートリアルでは、フォントの設定、線の非表示、CAD 画像内のテキストの操作などの重要な手順について説明しました。

## よくある質問

### Q1: Aspose.CAD for Java はライセンスなしで使用できますか?

 A1: 一時ライセンスがあればご利用いただけます。[ここ](https://purchase.aspose.com/temporary-license/).

### Q2: Aspose.CAD ドキュメントはどこで見つけられますか?

 A2: ドキュメントは入手可能です[ここ](https://reference.aspose.com/cad/java/).

### Q3: Aspose.CAD のサポートを受けるにはどうすればよいですか?

 A3: サポート フォーラムにアクセスしてください[ここ](https://forum.aspose.com/c/cad/19).

### Q4: Java 用 Aspose.CAD はどこでダウンロードできますか?

 A4: ライブラリをダウンロードします。[ここ](https://releases.aspose.com/cad/java/).

### Q5: 無料トライアルはありますか?

 A5: はい、無料トライアルが可能です[ここ](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
