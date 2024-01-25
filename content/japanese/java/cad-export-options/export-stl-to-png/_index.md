---
title: Aspose.CAD for Java を使用して STL を PNG にエクスポート
linktitle: STL を PNG にエクスポート
second_title: Aspose.CAD Java API
description: Aspose.CAD を使用して Java で STL ファイルを PNG にエクスポートするシームレスなプロセスを体験してください。ワークフローを簡素化し、Java プロジェクトを簡単に強化します。
type: docs
weight: 20
url: /ja/java/cad-export-options/export-stl-to-png/
---
## 導入

Java を使用して STL ファイルを PNG にエクスポートしたいと考えていますか? Aspose.CAD for Java は、あなたが必要とするソリューションです。このチュートリアルでは、プロセスを段階的に説明します。熟練した SEO ライターとして、コンテンツが有益であるだけでなく、検索エンジン向けに最適化されていることを確認します。

## 前提条件

チュートリアルに入る前に、次の前提条件が満たされていることを確認してください。

- Java Development Kit (JDK) がマシンにインストールされています。
-  Java ライブラリ用の Aspose.CAD がダウンロードされました。がんばって[ここ](https://releases.aspose.com/cad/java/).
- 有効なライセンスまたは一時ライセンス[ここ](https://purchase.aspose.com/temporary-license/).

## 名前空間のインポート

Java プロジェクトで、必要な名前空間をインポートします。

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

ここで、例を複数のステップに分けてみましょう。

## ステップ 1: プロジェクトをセットアップする

新しい Java プロジェクトを作成し、Aspose.CAD for Java ライブラリをプロジェクトの依存関係に追加します。

## ステップ 2: STL ファイルを指定する

STL ファイルへのパスを定義します。例えば：

```java
String dataDir = "Your Document Directory" + "ExportingSTL/";
String fileName = dataDir + "example.stl";
```

## ステップ 3: STL ファイルをロードする

STL ファイルをロードするには、`Image.load`方法：

```java
CadImage cadImage = (CadImage)Image.load(fileName);
```

## ステップ 4: ラスター化オプションを構成する

ベクトル化のラスタライズ オプションを設定します。

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

## ステップ 5: PNG オプションを構成する

PNG エクスポートのオプションを指定します。

```java
PngOptions pngOptions = new PngOptions();
//ベクター ラスタライズ オプションを設定する場合は、以下の行のコメントを解除します。
// pngOptions.setVectorRasterizationOptions(vectorOptions);
```

## ステップ 6: PNG として保存

CAD イメージを PNG ファイルとして保存します。

```java
String outPath = dataDir + "galeon.stl.png";
cadImage.save(outPath, pngOptions);
```

おめでとう！ Aspose.CAD for Java を使用して、STL ファイルを PNG に正常にエクスポートできました。

## 結論

このチュートリアルでは、Aspose.CAD for Java を活用して STL ファイルを PNG に簡単にエクスポートする方法を検討しました。この強力なライブラリは複雑なタスクを簡素化し、Java プロジェクトにとって貴重な資産となります。

## よくある質問

### Q1: Aspose.CAD for Java は、すべての STL ファイル バージョンと互換性がありますか?

A1: Aspose.CAD for Java はさまざまな STL ファイル バージョンをサポートし、最も一般的な形式との互換性を保証します。

### Q2: Aspose.CAD for Java を商用プロジェクトで使用できますか?

 A2: はい、可能です。から有効なライセンスを取得するだけです。[ここ](https://purchase.aspose.com/buy).

### Q3: 無料トライアルには一時ライセンスが必要ですか?

 A3: いいえ、無料トライアルには一時ライセンスは必要ありません。体験版ですぐに始められます[ここ](https://releases.aspose.com/).

### Q4: 追加のサポートはどこで見つけたり、質問したりできますか?

 A4: Aspose.CAD フォーラムにアクセスしてください。[ここ](https://forum.aspose.com/c/cad/19)サポートまたはご質問がありましたら。

### Q5: 入手可能な包括的なドキュメントはありますか?

 A5: はい、ドキュメントは見つかります。[ここ](https://reference.aspose.com/cad/java/).