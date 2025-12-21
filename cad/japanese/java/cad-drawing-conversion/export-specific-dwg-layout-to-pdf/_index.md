---
date: 2025-12-21
description: Aspose.CAD for Java を使用して、特定の DWG レイアウトを PDF にエクスポートすることで、DWG を PDF に変換する方法を学びましょう。このステップバイステップの
  DWG から PDF へのチュートリアルに従って、CAD ワークフローを効率化してください。
linktitle: Export Specific DWG Layout to PDF
second_title: Aspose.CAD Java API
title: DWGをPDFに変換 – Aspose.CAD for Javaでレイアウトをエクスポート
url: /ja/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG を PDF に変換 – Aspose.CAD for Java を使用した特定レイアウトのエクスポート

## Introduction

コンピュータ支援設計（CAD）の変化の激しい世界では、**convert DWG to PDF** は、クライアントや請負業者、技術的でないステークホルダーと図面を共有する際に頻繁に求められる要件です。Aspose.CAD for Java はこの変換を簡単に行えるだけでなく、マルチレイアウトの DWG ファイルから単一のレイアウトを選択することも可能です。このチュートリアルでは、**DWG** 固有のレイアウトを PDF にエクスポートする方法を解説し、余分なページや手動でのトリミングなしにプロジェクトが必要とする正確な成果物を提供できるようにします。

## Quick Answers
- **“convert DWG to PDF” とは何ですか？** DWG 図面を PDF ドキュメントに変換し、ベクターデータとレイアウトの忠実性を保持します。  
- **どのライブラリが変換を担当しますか？** Aspose.CAD for Java がすぐに使える API を提供します。  
- **本番環境でライセンスは必要ですか？** はい、商用ライセンスが必要です。無料トライアルは評価目的で使用できます。  
- **単一のレイアウトを選択できますか？** もちろんです – `Layouts` プロパティに目的のレイアウト名を設定します。  
- **サポートされている Java バージョンは何ですか？** Java 8 以降が完全に対応しています。

## Prerequisites

- **Java 開発環境** – JDK 8 以上とお好みの IDE。  
- **Aspose.CAD ライブラリ** – 公式サイトから最新の JAR をダウンロードしてください **[here](https://releases.aspose.com/cad/java/)**。  
- **DWG ファイル** – 少なくとも 1 つのレイアウトを含む図面（例: *visualization_-_conference_room.dwg*）。

## Why Export a Specific DWG Layout to PDF?

多くの DWG ファイルには複数のペーパースペース（レイアウト）が含まれています。ファイル全体をエクスポートすると、不要なページが含まれた大きな PDF が生成されることがあります。単一のレイアウトを選択することで:
- ファイルサイズが削減されます。  
- 閲覧者の注意が対象の図面シートに集中します。  
- プロジェクトの文書標準に合わせられます。

## Step‑by‑Step Guide

### Step 1: Set Up the Project Environment

新しい Java プロジェクト（Maven、Gradle、または単純な IDE）を作成し、Aspose.CAD JAR をクラスパスに追加します。ダウンロードは **[here](https://releases.aspose.com/cad/java/)** から行えます。

### Step 2: Import Necessary Packages

必要な Aspose.CAD 名前空間を Java クラスにインポートします。

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

### Step 3: Load the DWG File

変換したい DWG を指定し、`Image` オブジェクトにロードします。

```java
String srcFile = dataDir + "visualization_-_conference_room.dwg";
Image image = Image.load(srcFile);
```

### Step 4: Configure Rasterization Options

ページサイズと、重要なエクスポート対象レイアウトを定義します。

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
// Specify desired layout name
rasterizationOptions.setLayouts(new String[] {"Layout1"});
```

### Step 5: Set PDF Export Options

ラスタライズ設定を PDF エクスポーターに結び付けます。

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Step 6: Export DWG to PDF

結果を PDF ファイルとして保存します。出力には **Layout1** のみが含まれ、クリーンな **convert DWG to PDF** が実現します。

```java
image.save(dataDir + "ExportSpecificLayoutToPDF_out_.pdf", pdfOptions);
```

## Common Issues and Solutions

| 問題 | 発生原因 | 対策 |
|------|----------|------|
| **レイアウトが見つかりません** | レイアウト名が間違っているか、DWG に存在しません。 | `image.getLayoutNames()` を使用して利用可能なレイアウトを一覧表示し、正しいものを選択してください。 |
| **低解像度 PDF** | `PageWidth`/`PageHeight` が小さすぎます。 | 寸法を大きく（例: 2000 × 2000）するか、`rasterizationOptions.setResolution(300);` を設定してください。 |
| **ライセンス例外** | 評価版以外の環境で有効なライセンスなしで実行しています。 | 画像をロードする前に Aspose.CAD ライセンスを適用してください: `License license = new License(); license.setLicense("Aspose.CAD.lic");`。 |

## Frequently Asked Questions

**Q1: Aspose.CAD for Java を他の Java ベースの CAD ライブラリと併用できますか？**  
A: Aspose.CAD for Java は単体のライブラリですが、拡張機能のために他の Java ベースのライブラリと統合することが可能です。

**Q2: Aspose.CAD のライセンスオプションはありますか？**  
A: はい、ライセンスオプションと購入詳細は **[here](https://purchase.aspose.com/buy)** で確認できます。

**Q3: Aspose.CAD の一時ライセンスを取得するには？**  
A: **[this link](https://purchase.aspose.com/temporary-license/)** から一時ライセンスをリクエストしてください。

**Q4: Aspose.CAD のサポートはどこで受けられますか？**  
A: ご質問やサポートが必要な場合は **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)** をご利用ください。

**Q5: Aspose.CAD の無料トライアルはありますか？**  
A: はい、無料トライアルは **[here](https://releases.aspose.com/)** から利用できます。

## Conclusion

この **dwg to pdf tutorial** に従うことで、単一レイアウトに絞った **DWG を PDF に変換** の確実な方法が手に入りました。この手法はストレージの節約、ドキュメント共有の高速化、CAD ワークフローの整理に役立ちます。プロジェクトの進行に合わせて、さまざまなラスタライズ設定を試したり、複数レイアウトを 1 つの PDF に結合したりしてみてください。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最終更新日:** 2025-12-21  
**テスト環境:** Aspose.CAD for Java 24.12  
**作者:** Aspose