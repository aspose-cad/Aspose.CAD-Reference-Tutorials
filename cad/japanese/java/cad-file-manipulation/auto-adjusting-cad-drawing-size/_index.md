---
title: Aspose.CAD for Java を使用した CAD 図面サイズの自動調整
linktitle: CAD図面サイズの自動調整
second_title: Aspose.CAD Java API
description: Aspose.CAD を使用して Java で CAD 図面サイズを自動調整するシームレスなプロセスを確認してください。 CAD ファイルを効率的に操作するには、ステップバイステップのガイドに従ってください。
weight: 13
url: /ja/java/cad-file-manipulation/auto-adjusting-cad-drawing-size/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java を使用した CAD 図面サイズの自動調整

## 導入

CAD (コンピューター支援設計) の世界では、図面サイズの調整は一般的な要件ですが、Aspose.CAD for Java を使用すると、これがシームレスなプロセスになります。この強力なライブラリは、Java アプリケーションで CAD ファイルを処理するための包括的なツールを提供します。このチュートリアルでは、Aspose.CAD を使用して CAD 図面のサイズを自動調整するプロセスを段階的に説明します。

## 前提条件

チュートリアルに入る前に、次の前提条件が満たされていることを確認してください。

1.  Java 開発環境: マシンに Java がインストールされていることを確認します。ダウンロードできます[ここ](https://www.java.com/en/download/).

2. Aspose.CAD ライブラリ: Java 用の Aspose.CAD ライブラリを次からダウンロードしてインストールします。[ここ](https://releases.aspose.com/cad/java/).

3. サンプル CAD ファイル: ドキュメント ディレクトリにサンプル CAD ファイル (sample.dwg など) を用意します。

## 名前空間のインポート

Java アプリケーションに、Aspose.CAD 機能を利用するために必要な名前空間を含めます。以下に例を示します。

```java

import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

ここで、CAD 図面のサイズを自動調整するプロセスを管理可能なステップに分割してみましょう。

## ステップ 1: CAD 図面をロードする

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String sourceFilePath = dataDir + "sample.dwg";
Image objImage = Image.load(sourceFilePath);
```

このステップには、指定されたファイル パスから CAD 図面をロードすることが含まれます。

## ステップ 2: BmpOptions を作成する

```java
BmpOptions bmpOptions = new BmpOptions();
```

インスタンス化します`BmpOptions`このクラスは、BMP 形式のさまざまなオプションを設定するために使用されます。

## ステップ 3: CadRasterizationOptions を作成する

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

のインスタンスを作成します`CadRasterizationOptions`CAD ファイルのラスタライズ設定をカスタマイズします。

## ステップ 4: レイアウト プロパティを設定する

```java
cadRasterizationOptions.setLayouts(new String[]{"Model"});
```

出力に含めるレイアウトを指定します。この場合、「モデル」レイアウトを使用します。

## ステップ 5: BMP 形式にエクスポートする

```java
String outPath = sourceFilePath + ".bmp";
objImage.save(outPath, bmpOptions);
```

最後に、調整した CAD 図面を BMP 形式で指定した出力パスに保存します。

Java アプリケーションでこれらの手順を繰り返すと、Aspose.CAD for Java を使用して CAD 図面のサイズが正常に自動調整されます。

## 結論

このチュートリアルでは、Aspose.CAD for Java を使用して CAD 図面サイズを自動調整するプロセスを説明しました。このライブラリは CAD ファイルの操作を簡素化し、開発者に堅牢なソリューションを提供します。

## よくある質問

### Q1: Aspose.CAD はさまざまな CAD ファイル形式と互換性がありますか?

A1: はい、Aspose.CAD は、DWG、DXF、DGN などを含むさまざまな CAD 形式をサポートしています。

### Q2: Aspose.CAD を商用プロジェクトに使用できますか?

 A2: もちろんです！訪問[ここ](https://purchase.aspose.com/buy)ライセンス オプションを検討します。

### Q3: テスト目的で一時ライセンスを取得するにはどうすればよいですか?

 A3: 仮免許を取得する[ここ](https://purchase.aspose.com/temporary-license/)テストと評価用。

### Q4: Aspose.CAD のサポートはどこで見つけられますか?

A4: Aspose.CAD コミュニティに参加してください[フォーラム](https://forum.aspose.com/c/cad/19)支援とディスカッションのために。

### Q5: Aspose.CAD for Java の無料トライアルはありますか?

 A5: はい、無料トライアルにアクセスできます。[ここ](https://releases.aspose.com/)ライブラリの機能を探索します。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
