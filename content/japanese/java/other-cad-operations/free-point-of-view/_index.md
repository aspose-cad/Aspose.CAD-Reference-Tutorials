---
title: Aspose.CAD for Java を使用した自由な視点レンダリング
linktitle: 自由な視点
second_title: Aspose.CAD Java API
description: CAD 図面の自由な視点レンダリングの実現に関するこのチュートリアルで、Aspose.CAD for Java の威力を探ってください。 Aspose.CAD の可能性を解き放ちます。
type: docs
weight: 14
url: /ja/java/other-cad-operations/free-point-of-view/
---
## 導入

「無料の視点 - Aspose.CAD for Java チュートリアル」へようこそ。この包括的なガイドでは、Aspose.CAD for Java を活用して CAD 図面を自由に視点でレンダリングするプロセスを説明します。 Aspose.CAD は、コンピュータ支援設計 (CAD) ファイルを操作するための幅広い機能を提供する強力な Java ライブラリです。このチュートリアルでは、必要な前提条件、重要なパッケージのインポート、各例を段階的なガイドに分けて説明します。

## 前提条件

チュートリアルに入る前に、次の前提条件が満たされていることを確認してください。
-  Aspose.CAD for Java ライブラリ: Aspose.CAD for Java ライブラリを次の場所からダウンロードしてインストールします。[ダウンロードリンク](https://releases.aspose.com/cad/java/).
- Java 開発キット (JDK): マシンに Java がインストールされていることを確認します。

## パッケージのインポート

まず、必要なパッケージを Java プロジェクトにインポートします。 Java ファイルの先頭に次のコード行を追加します。
```java
import com.aspose.cad.fileformats.ObserverPoint;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.JpegOptions;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.ObserverPoint;
```

これらのパッケージは、CAD ファイルの操作やレンダリング オプションのカスタマイズに不可欠です。

ここで、提供された例を複数のステップに分解してみましょう。

## ステップ 1: ドキュメント ディレクトリを設定する

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

「Your Document Directory」を実際のドキュメント ディレクトリへのパスに置き換えます。

## ステップ 2: CAD 図面をロードする

```java
String sourceFilePath = dataDir + "conic_pyramid.dxf";
Image objImage = Image.load(sourceFilePath);
```

CAD 図面へのパスを指定し、`Image`クラス。

## ステップ 3: CAD ラスタライズ オプションを構成する

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
cadRasterizationOptions.setPageHeight(1500);
cadRasterizationOptions.setPageWidth(1500);
```

ページの高さや幅などの要件に応じて CAD ラスタライズ オプションをカスタマイズします。

## ステップ 4: JpegOptions を設定する

```java
JpegOptions options = new JpegOptions();
options.setVectorRasterizationOptions(cadRasterizationOptions);
```

のインスタンスを作成します`JpegOptions`そして、それを以前に構成したラスタライズ オプションに関連付けます。

## ステップ 5: 回転角度を定義する

```java
float xAngle = 10;
float yAngle = 30;
float zAngle = 40;
ObserverPoint obvPoint = new ObserverPoint(xAngle, yAngle, zAngle);
cadRasterizationOptions.setObserverPoint(obvPoint);
```

自由視点レンダリングの X、Y、Z 軸に沿った回転角度を指定します。

## ステップ 6: レンダリングされたイメージを保存する

```java
objImage.save(dataDir + "FreePointOfView_out.jpeg", options);
```

指定されたオプションを使用してレンダリングされたイメージを目的の場所に保存します。

特定の使用例に対してこれらの手順を繰り返し、CAD 図面を自由に視点でレンダリングできるようにします。

## 結論

おめでとう！ Aspose.CAD for Java を使用して自由な視点レンダリングを実装する方法を学習しました。このチュートリアルでは、前提条件の設定からレンダリング オプションのカスタマイズ、出力イメージの保存まで、重要な手順を説明しました。

## よくある質問

### Q1: Aspose.CAD for Java を複数のプラットフォームで使用できますか?

A1: はい、Aspose.CAD for Java はプラットフォームに依存せず、さまざまなオペレーティング システムで使用できます。

### Q2: Aspose.CAD for Java のライセンス オプションはありますか?

 A2: はい、ライセンス オプションを調べて購入できます。[ここ](https://purchase.aspose.com/buy).

### Q3: 無料トライアルはありますか?

 A3: はい、無料試用版にアクセスできます。[ここ](https://releases.aspose.com/).

### Q4: Aspose.CAD for Java のサポートはどこで見つけられますか?

 A4: にアクセスしてください。[Aspose.CAD フォーラム](https://forum.aspose.com/c/cad/19)コミュニティのサポートとディスカッションのために。

### Q5: 仮免許はどうやって取得できますか?

 A5: 仮免許を取得する[ここ](https://purchase.aspose.com/temporary-license/).