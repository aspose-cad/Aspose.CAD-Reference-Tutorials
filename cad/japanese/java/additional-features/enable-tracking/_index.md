---
date: 2025-12-01
description: Aspose.CAD for Java を使用して、PDF のページサイズの設定方法、DWG を PDF に変換する方法、DWG の変更の追跡を有効にする方法を学びましょう。
language: ja
linktitle: Set PDF Page Size and Track DWG with Java
second_title: Aspose.CAD Java API
title: Aspose.CAD Java で PDF ページサイズを設定し、DWG を追跡する
url: /java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD JavaでPDFページサイズを設定し、DWGを追跡する

## はじめに

CADプロジェクトで協働する際、**PDFページサイズを設定**してレイアウトを統一したり、**DWGをPDFに変換**したり、図面に加えられたすべての変更を追跡したりする必要があります。Aspose.CAD for Javaは、これらすべてを単一のシンプルなワークフローで実現します。このチュートリアルでは、**PDFページサイズを設定**し、**DWGの変更を追跡**できるようにし、図面をPDFとしてエクスポートする正確な手順をJavaで説明します。

## クイック回答
- **PDFページサイズはどう設定しますか？** エクスポート前に `CadRasterizationOptions.setPageWidth()` と `setPageHeight()` を使用します。  
- **エクスポート中に変更を追跡できますか？** はい – カスタム `CadRenderHandler` を実装して追跡結果を取得します。  
- **DWGをPDFに変換するメソッドはどれですか？** オプションを設定した後、`image.save(stream, pdfOptions)` を呼び出します。  
- **主な前提条件は何ですか？** JDK、Aspose.CAD for Java、そしてDWG/DXFファイルが入ったフォルダーです。  
- **本番環境でライセンスは必要ですか？** はい、トライアル以外のデプロイには有効な Aspose.CAD ライセンスが必要です。

## DWGエクスポートにおける「PDFページサイズを設定する」とは何ですか？

PDFページサイズを設定すると、生成されるPDFキャンバスの寸法（幅 × 高さ、ピクセル単位）が決まります。エクスポートされた図面を特定の用紙サイズや画面レイアウトに合わせたい場合に重要で、すべての要素が期待通りの位置に表示されます。

## DWGファイルをエクスポートする際に追跡を有効にする理由は？

追跡（または変更追跡）は、変換中に発生したレンダリングの問題、フォントの欠如、未対応エンティティなどを記録します。この情報を取得することで、以下が可能になります：

- 最終納品前に修正が必要な問題を迅速に特定できます。  
- 変更や省略された箇所についてチームメンバーに明確なフィードバックを提供できます。  
- コンプライアンスが重視される業界向けに監査証跡を維持できます。

## 前提条件

- **Java Development Kit (JDK)** – 任意の最近のバージョン（8以上）。  
- **Aspose.CAD for Java** – 公式の [Aspose CAD ダウンロードページ](https://releases.aspose.com/cad/java/) からダウンロードしてください。  
- **Document Directory** – 処理したい DWG/DXF ファイルが入っているフォルダー。

## 名前空間のインポート

まず、必要な Aspose.CAD クラスと標準の Java I/O クラスをインポートします。

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.CadRenderResult;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.RenderResult;
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
```

## ステップ 1: DWG（または DXF）ファイルをロードする

ソース図面を `Image` オブジェクトにロードします。パスは自分のディレクトリに合わせて調整してください。

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## ステップ 2: PDFエクスポートオプションの設定（ページサイズを含む）

ここでは PDF オプションを設定し、明示的に **PDFページサイズ** を 800 × 600 ピクセルに設定します。これが主要なキーワードが適用される箇所です。

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);   // set PDF page width
cadRasterizationOptions.setPageHeight(600);  // set PDF page height
```

## ステップ 3: 追跡の実装

変換プロセス中に追跡情報を受け取るカスタムエラーハンドラを作成します。

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## ステップ 4: PDFへエクスポート

オプションと追跡ハンドラが設定されたら、図面をエクスポートします。このステップで **DWGをPDFに変換**（例では DXF を PDF に変換）します。

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## ステップ 5: CadRenderHandler クラス – 追跡結果の取得

`ErrorHandler` クラスは `CadRenderHandler` を継承し、**DWG の変更を追跡** 中に発生したレンダリングの問題を出力します。

```java
public static class ErrorHandler extends CadRasterizationOptions.CadRenderHandler {
    @Override
    public void invoke(CadRenderResult result) {
        System.out.println("Tracking results of exporting");

        if (result.isRenderComplete())
            return;

        System.out.println("Have some problems:");

        int idxError = 1;
        for (RenderResult rr : result.getFailures()) {
            System.out.printf("{0}. {1}, {2}", idxError, rr.getRenderCode(), rr.getMessage());
            idxError++;
        }
    }
}
```

## 一般的な問題と解決方法

| 問題 | 発生原因 | 対処法 |
|------|----------|--------|
| **フォントが見つからない** | CAD ファイルがサーバーにインストールされていないフォントを参照しています。 | 必要なフォントをインストールするか、ソース図面に埋め込んでください。 |
| **未対応エンティティ** | 一部の DWG エンティティはまだ Aspose.CAD でサポートされていません。 | 追跡出力を使ってそれらを特定し、図面を簡素化してください。 |
| **ページサイズが正しくない** | エクスポート前に `setPageWidth/Height` が呼び出されていません。 | 上記のように `CadRasterizationOptions` でページサイズが設定されていることを確認してください。 |

## よくある質問

### Q1: Aspose.CAD for Javaで他のCADファイル形式の追跡を有効にできますか？

A1: Aspose.CAD は主に DWG/DXF ファイルの追跡をサポートしています。他の形式については、公式ドキュメントで利用可能な機能を確認してください。

### Q2: Aspose.CAD for Javaで追加のエクスポートオプションを扱うには？

A2: ライブラリは DPI、背景色、ベクトルラスタライズなど多数のオプションを提供しています。これらは [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/) で確認してください。

### Q3: Aspose.CAD for Java のトライアル版はありますか？

A3: はい、[Aspose.CAD Free Trial](https://releases.aspose.com/) から無料トライアルをダウンロードできます。

### Q4: Aspose.CAD for Java に関するサポートや議論はどこでできますか？

A4: [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) のコミュニティフォーラムは、質問や経験を共有するのに最適な場所です。

### Q5: Aspose.CAD for Java の一時ライセンスはどう取得しますか？

A5: 評価用の期間限定ライセンスを取得するには、[Temporary License](https://purchase.aspose.com/temporary-license/) ページの手順に従ってください。

### Q6: レイヤーを保持したまま **DWGをPDFに変換**できますか？

A6: はい。`CadRasterizationOptions` を設定することで、結果の PDF にレイヤー情報を保持できます。

### Q7: カスタムページサイズで **DWGをPDFとしてエクスポート**する最適な方法は？

A7: `image.save()` を呼び出す前に `setPageWidth` と `setPageHeight` で希望の幅と高さを設定します – Step 2 で示した通りです。

## 結論

上記の手順に従うことで、Aspose.CAD for Java を使用して **PDFページサイズを設定**、**DWGをPDFに変換**、そして **DWGファイルの変更を追跡** できます。このワークフローにより、出力レイアウトを完全にコントロールでき、CAD の協働をスムーズかつエラーなしに保つための有用な診断情報が得られます。追加のレンダリングオプションを検討し、このコードを大規模な自動化パイプラインに組み込んでみてください。

---

**最終更新日：** 2025-12-01  
**テスト環境：** Aspose.CAD for Java 24.12 (latest at time of writing)  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}