---
title: Aspose.CAD for Java を使用して DGN を DWG にエクスポート
linktitle: DGN を DWG の一部としてエクスポート
second_title: Aspose.CAD Java API
description: Aspose.CAD for Java を使用して DWG の一部として DGN をエクスポートする方法を説明します。 CAD ファイルを効率的に操作するには、ステップバイステップのガイドに従ってください。
type: docs
weight: 10
url: /ja/java/dgn-export-options/export-dgn-as-part-of-dwg/
---
## 導入

このチュートリアルでは、Aspose.CAD for Java を使用して、DGN (MicroStation Design) ファイルを DWG (AutoCAD Drawing) ファイルの一部としてエクスポートする方法を説明します。 Aspose.CAD は、CAD ファイル形式を処理するための包括的な機能を提供する強力なライブラリです。このステップバイステップのガイドは、Java を使用して DGN を DWG の一部としてエクスポートするプロセスを理解するのに役立ちます。

## 前提条件

チュートリアルに入る前に、次の前提条件が満たされていることを確認してください。
1. Aspose.CAD ライブラリ: Java 用の Aspose.CAD ライブラリをダウンロードしてインストールします。図書館を見つけることができます[ここ](https://releases.aspose.com/cad/java/).
2. Java Development Kit (JDK): システムに Java がインストールされていることを確認してください。
3. 統合開発環境 (IDE): よりスムーズな開発エクスペリエンスを実現するには、Eclipse や IntelliJ などの Java IDE を選択してください。

## パッケージのインポート

Java プロジェクトで、必要な Aspose.CAD パッケージをインポートして、CAD ファイルの操作を有効にします。以下に例を示します。

```java
import com.aspose.cad;
import com.aspose.cad.imageoptions;
import com.aspose.cad.fileformats.cad.cadconsts;
import com.aspose.cad.fileformats.cad;
import com.aspose.cad.fileformats.cad.cadobjects;
```

## ステップ 1: ファイル パスを設定する

DWG ファイルの入力および出力ファイル パスを定義します。を更新します`dataDir`, `fileName`、 そして`outPath`それに応じて変数を設定します。

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
String outPath = dataDir + "BlockRefDgn.dwg.pdf";
```

## ステップ 2: PdfOptions インスタンスを作成する

のインスタンスを作成します。`PdfOptions` DWG ファイルを PDF 形式にエクスポートしているため、クラスに追加されます。

```java
PdfOptions exportOptions = new PdfOptions();
```

## ステップ 3: DWG ファイルをロードする

既存の DWG ファイルを画像としてロードし、`CadImage`タイプ。

```java
CadImage cadImage = (CadImage) Image.load(fileName);
```

## ステップ 4: エンティティを反復処理する

DWG ファイル内の各エンティティを調べて、それがイメージ定義であるかどうかを確認します。存在する場合は、オブジェクトへの外部参照を取得します。

```java
for (CadBaseEntity baseEntity : cadImage.getEntities()) {
    if (baseEntity.getTypeName() == CadEntityTypeName.DGNUNDERLAY) {
        CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
        System.out.println(dgnFile.getUnderlayPath());
    }
}
```

## ステップ 5: ラスタライズ オプションを定義する

の設定を定義します。`CadRasterizationOptions`ページの幅、高さ、レイアウト、背景色などのオブジェクト。

```java
CadRasterizationOptions vectorRasterizationOptions = new CadRasterizationOptions();
vectorRasterizationOptions.setPageWidth(1600);
vectorRasterizationOptions.setPageHeight(1600);
vectorRasterizationOptions.setLayouts(new String[] { "Model" });
vectorRasterizationOptions.setAutomaticLayoutsScaling(false);
vectorRasterizationOptions.setNoScaling(true);
vectorRasterizationOptions.setBackgroundColor(Color.getBlack());
vectorRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
```

## ステップ 6: ベクトル ラスタライズ オプションを設定する

エクスポートのベクトル ラスタライズ オプションを設定します。

```java
exportOptions.setVectorRasterizationOptions(vectorRasterizationOptions);
```

## ステップ 7: DWG を PDF にエクスポートする

最後に、次のコマンドを呼び出して DWG を PDF にエクスポートします。`save`方法。

```java
cadImage.save(outPath, exportOptions);
```

## 結論

おめでとう！ Aspose.CAD for Java を使用して、DGN ファイルを DWG ファイルの一部としてエクスポートする方法を学習しました。この強力なライブラリは、CAD ファイルを操作するための広範な機能を提供し、CAD ファイル操作タスクを効率的かつ簡単にします。

## よくある質問

### Q1: Aspose.CAD for Java のドキュメントはどこで見つけられますか?

 A1: ドキュメントは見つかります。[ここ](https://reference.aspose.com/cad/java/).

### Q2: Java 用の Aspose.CAD ライブラリをダウンロードするにはどうすればよいですか?

 A2: ライブラリは以下からダウンロードできます。[このリンク](https://releases.aspose.com/cad/java/).

### Q3: Aspose.CAD for Java の無料トライアルはありますか?

 A3: はい、無料トライアルを見つけることができます。[ここ](https://releases.aspose.com/).

### Q4: Aspose.CAD for Java の一時ライセンスはどこで入手できますか?

 A4: 仮免許を取得する[ここ](https://purchase.aspose.com/temporary-license/).

### Q5: サポートが必要ですか、それとも質問がありますか?

 A5: Aspose.CAD コミュニティ サポート フォーラムにアクセスしてください。[ここ](https://forum.aspose.com/c/cad/19).