---
title: Aspose.CAD for Java を使用して CAD から OLE オブジェクトをエクスポートする
linktitle: CAD から OLE オブジェクトをエクスポート
second_title: Aspose.CAD Java API
description: Aspose.CAD for Java の可能性を解き放ちます。 CAD ファイルから OLE オブジェクトを簡単にエクスポートします。シームレスな CAD データ管理のために今すぐダウンロードしてください。
weight: 10
url: /ja/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java を使用して CAD から OLE オブジェクトをエクスポートする

## 導入

コンピュータ支援設計 (CAD) の動的な世界では、OLE (オブジェクト リンクと埋め込み) オブジェクトを効率的に管理および抽出することが重要です。 Aspose.CAD for Java は、CAD ファイルから OLE オブジェクトをエクスポートするための強力なソリューションを提供します。このステップバイステップのガイドでは、プロセスを順を追って説明し、このツールの可能性を最大限に活用できるようにします。

## 前提条件

チュートリアルに入る前に、次の前提条件が満たされていることを確認してください。

- Java 環境: マシン上に Java 開発環境がセットアップされていることを確認します。
-  Aspose.CAD for Java: Aspose.CAD for Java ライブラリをダウンロードしてインストールします。ライブラリは次の場所にあります。[ダウンロードリンク](https://releases.aspose.com/cad/java/).
- CAD ファイル: エクスポートする OLE オブジェクトを含む CAD ファイルを準備します。

## 名前空間のインポート

まず、必要な名前空間を Java プロジェクトにインポートします。これらの名前空間は、Aspose.CAD を使用して CAD ファイルを操作するために必要な必須のクラスと機能を提供します。

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

ここで、CAD から OLE オブジェクトをエクスポートするプロセスを複数のステップに分けてみましょう。

## ステップ 1: ドキュメント ディレクトリを設定する

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

「Your Document Directory」を CAD ファイルが含まれるディレクトリへのパスに置き換えてください。

## ステップ 2: CAD ファイル名を定義する

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

処理する CAD ファイルの名前を指定します。`files`配列。

## ステップ 3: PNG エクスポート オプションを設定する

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

ベクター ラスタライズやレイアウト設定などの PNG エクスポート オプションを構成します。

## ステップ 4: CAD ファイルを反復処理する

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

指定された各 CAD ファイルを反復処理し、Aspose.CAD を使用してファイルをロードし、OLE オブジェクトを PNG イメージとして保存します。

## 結論

これらのシンプルかつ強力な手順により、Aspose.CAD for Java を使用して CAD ファイルから OLE オブジェクトをシームレスにエクスポートできます。この多用途ツールにより、開発者は CAD データを効率的に管理できるようになり、CAD アプリケーション開発の新たな可能性が広がります。

## よくある質問

### Q1: Aspose.CAD はすべての CAD ファイル形式と互換性がありますか?

 A1: Aspose.CAD は、DWG、DXF、DGN などのさまざまな CAD 形式をサポートしています。を参照してください。[ドキュメンテーション](https://reference.aspose.com/cad/java/)完全なリストについては、

### Q2: OLE オブジェクトのエクスポート設定をカスタマイズできますか?

A2: はい、Aspose.CAD にはエクスポート設定をカスタマイズするための広範なオプションが用意されており、特定の要件に合わせて出力を調整できます。

### Q3: Aspose.CAD の無料トライアルはありますか?

 A3: はい、次のサイトから無料トライアルを入手して、Aspose.CAD の機能を試すことができます。[ここ](https://releases.aspose.com/).

### Q4: Aspose.CAD のコミュニティ サポートはどこで受けられますか?

 A4: Aspose.CAD コミュニティに参加してください。[フォーラム](https://forum.aspose.com/c/cad/19)助けを求め、あなたの経験を共有してください。

### Q5: Aspose.CAD のライセンスを購入するにはどうすればよいですか?

A5: にアクセスしてください。[購入ページ](https://purchase.aspose.com/buy)開発ニーズに合ったライセンスを取得します。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
