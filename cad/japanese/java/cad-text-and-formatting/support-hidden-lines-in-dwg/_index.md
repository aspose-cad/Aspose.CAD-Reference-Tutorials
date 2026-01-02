---
date: 2026-01-02
description: このステップバイステップチュートリアルで、DWGをPDFとしてエクスポートし、隠線を有効にし、Aspose.CAD for Javaを使用してDWGをPDFに変換する方法を学びましょう。
linktitle: Export DWG as PDF with Hidden Lines Using Java
second_title: Aspose.CAD Java API
title: DWGを隠線付きPDFにエクスポート – Aspose.CAD for Java
url: /ja/java/cad-text-and-formatting/support-hidden-lines-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 隠し線付きでDWGをPDFにエクスポート – Aspose.CAD for Java

## はじめに

このチュートリアルでは、Aspose.CAD for Java を使用して隠し線を保持しながら **DWG を PDF にエクスポート** する方法を学びます。**DWG を PDF に変換** が必要な場合や、**dwg to pdf tutorial** スタイルのガイドを作成したい場合、または単に **DWG を PDF として保存** し隠し線をサポートしたい場合でも、すべての手順を詳しく解説します。最後まで読むと、任意の Java プロジェクトに組み込めるすぐに使えるソリューションが手に入ります。

## クイック回答
- **このチュートリアルで取り上げる内容は何ですか？** Aspose.CAD for Java を使用して DWG を PDF にエクスポートする際に隠し線レンダリングを有効にすることです。  
- **実行される主な操作は何ですか？** `export dwg as pdf`。  
- **ライセンスは必要ですか？** テストには無料トライアルで動作しますが、本番環境では商用ライセンスが必要です。  
- **前提条件は何ですか？** Java 開発環境、Aspose.CAD for Java ライブラリ、そして DWG ファイルです。  
- **実装にかかる時間はどれくらいですか？** 基本的なセットアップで約 10〜15 分です。

## “export dwg as pdf” とは？

DWG ファイルを PDF にエクスポートすると、ベクターベースの CAD 図面がポータブルドキュメント形式に変換され、レイヤーや線種、オプションで隠し線レンダリングを保持したままになります。これにより、CAD ソフトウェアを持っていない関係者とも CAD 設計を簡単に共有できます。

## エクスポート時に隠し線を有効にする理由

隠し線を表示することで、複雑な 3D モデルを 2D ページ上でより分かりやすく視覚化でき、見えるエッジだけが強調されます。これにより可読性が向上し、エンジニアリング文書でしばしば求められる要件を満たすことができます。

## 前提条件

1. **Aspose.CAD for Java** – 公式サイトからライブラリをダウンロードしてください [こちら](https://releases.aspose.com/cad/java/)。  
2. **DWG ファイル** – ソースとなる DWG 図面を既知のディレクトリに保存しておいてください。  
3. **Java 開発環境** – JDK 8 以上とお好みの IDE（Eclipse、IntelliJ など）。

準備が整ったので、コードに入りましょう。

## 名前空間のインポート

まず、CAD 画像と PDF オプションを扱えるように必要なクラスをインポートします。

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.Arrays;
import java.util.List;
```

## 手順 1: プロジェクトのセットアップ

Java プロジェクトを作成し、Aspose.CAD の JAR をビルドパスに追加します。その後、DWG ファイルが格納されているディレクトリを定義します。

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

> **プロのコツ:** 絶対パスを使用するか、プロジェクトの resources フォルダーに基づいた相対パスを設定してください。

## 手順 2: DWG ファイルの読み込み

ソースの DWG ファイルを `CadImage` オブジェクトに読み込み、操作できるようにします。

```java
String sourceFilePath = dataDir + "Bottom_plate.dwg";
String outPath = dataDir + "Bottom_plate.pdf";
CadImage cadImage = (CadImage)Image.load(sourceFilePath);
```

## 手順 3: ラスタライズオプションの設定

含めるレイヤーを選択し、ページサイズを元の図面に合わせて設定します。ここでレイアウトを指定して隠し線レンダリングを有効にします。

```java
List<String> list = Arrays.asList("Print","L1_RegMark","L2_RegMark");
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageHeight(cadImage.getHeight());
rasterizationOptions.setPageWidth(cadImage.getWidth()) ;
rasterizationOptions.setLayers(list);
```

## 手順 4: PDF オプションの設定

Aspose.CAD にベクターデータを PDF にラスタライズさせ、隠し線を非表示に保つために “Model” レイアウトを使用するよう指示します。

```java
PdfOptions pdfOptions = new PdfOptions();
rasterizationOptions.setLayouts(new String[] { "Model" });
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## 手順 5: 結果の保存

最後に、DWG を PDF ファイルとしてエクスポートします。設定したレイアウトに従って隠し線が正しく処理されます。

```java
cadImage.save(outPath, pdfOptions);
System.out.println("\nThe DWG file exported successfully to PDF.\nFile saved at " + dataDir);
```

> **一般的な落とし穴:** レイアウトを `"Model"` に設定し忘れると、隠し線を含むすべての線が PDF で実線として表示されてしまいます。

## 結論

これで、Aspose.CAD for Java を使用して隠し線サポート付きで **DWG を PDF にエクスポート** する、完全な本番対応の手法が手に入りました。この方法はバッチ処理ツール、Web サービス、デスクトップアプリケーションに組み込んで、CAD から PDF への変換を自動化できます。

## よくある質問

### Q1: Aspose.CAD for Java を他の CAD ファイル形式でも使用できますか？

A1: はい、Aspose.CAD は DWG、DXF、DWF などさまざまな CAD 形式をサポートしています。

### Q2: Aspose.CAD for Java の無料トライアルはありますか？

A2: はい、無料トライアルは [こちら](https://releases.aspose.com/)で入手できます。

### Q3: Aspose.CAD for Java のサポートはどこで受けられますか？

A3: コミュニティサポートは Aspose.CAD フォーラム [こちら](https://forum.aspose.com/c/cad/19)をご覧ください。

### Q4: Aspose.CAD for Java の詳細なドキュメントはどこにありますか？

A4: ドキュメントは [こちら](https://reference.aspose.com/cad/java/)をご参照ください。

### Q5: Aspose.CAD for Java の一時ライセンスを購入できますか？

A5: はい、一時ライセンスは [こちら](https://purchase.aspose.com/temporary-license/)で取得できます。

### Q6: この方法はヘッドレスサーバー環境での DWG から PDF への変換でも機能しますか？

A6: もちろんです。コードは Aspose.CAD API のみを使用しているため、UI 依存がなく、サーバー側の自動化に最適です。

**最終更新日:** 2026-01-02  
**テスト環境:** Aspose.CAD for Java 24.12  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}