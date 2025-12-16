---
date: 2025-12-10
description: Aspose.CAD for Java の Auto Layout Scaling を使用して、CAD から PDF を作成する方法を学びましょう。このステップバイステップガイドでは、CAD
  を PDF に効率的かつ確実にエクスポートする方法を示します。
linktitle: Setting Auto Layout Scaling
second_title: Aspose.CAD Java API
title: CADからPDFを作成 – Aspose.CAD Javaで自動レイアウトスケーリング
url: /ja/java/advanced-cad-features/setting-auto-layout-scaling/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CADからPDFを作成 – Aspose.CAD Javaによる自動レイアウトスケーリング

## Introduction

CADからPDFを**迅速かつ完璧なスケーリング**で作成する必要がある場合、Aspose.CAD for Java がサポートします。Auto Layout Scaling はレイアウト寸法を自動的に調整し、元の CAD ページサイズに関係なく、生成された PDF が意図した通りに表示されます。このチュートリアルでは、DXF ファイルの読み込みから PDF へのエクスポートまでの全工程を順に解説し、ライブラリの **export CAD to PDF** 機能をハイライトします。

## Quick Answers
- **Auto Layout Scaling は何をするのですか？** ラスタライズ時に CAD レイアウトを自動的にリサイズし、ターゲットページの寸法に合わせます。
- **どのフォーマットに変換できますか？** Aspose.CAD がサポートするすべてのフォーマット（例: DXF、DWG、DWF）を PDF に変換できます。
- **本番環境でライセンスが必要ですか？** はい、評価版以外で使用する場合は商用ライセンスが必要です。
- **変換にどれくらい時間がかかりますか？** 標準的なファイルであれば、最新ハードウェア上で通常 1 秒未満です。
- **ページサイズを変更できますか？** はい、`CadRasterizationOptions` でカスタムページ寸法を設定できます。

## What is “create PDF from CAD”?

CAD から PDF を作成するとは、ベクターベースのエンジニアリング図面（DXF、DWG など）を PDF ドキュメントにラスタライズすることを指します。PDF は元の図面の視覚的忠実度を保持しつつ、あらゆるプラットフォームで広く閲覧可能です。

## Why use Auto Layout Scaling?
- **一貫した出力:** 手動でサイズ計算を行うことなく、すべてのレイアウトが PDF ページ全体を埋めることを保証します。
- **時間節約:** 各図面ごとにスケーリング係数を手動で調整する必要がなくなります。
- **高品質:** 変換中に線幅やジオメトリの精度を保持します。

## Prerequisites

1. **Aspose.CAD for Java ライブラリ** – 最新バージョンを [download page](https://releases.aspose.com/cad/java/) からダウンロードしてください。  
2. **リソースディレクトリ** – CAD ファイルを保存するフォルダーを作成し、コード中の `"Your Document Directory"` をそのパスに置き換えてください。  
3. **サンプル CAD ファイル** – 本ガイドでは `conic_pyramid.dxf` を使用します。このファイルは Aspose のサンプルデータセットに含まれています。

## Import Namespaces

First, import the required classes. This gives us access to image loading, rasterization, and PDF export features.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Step 1: Load the CAD File

Loading the source file is the first step in **how to export CAD** to a PDF document.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

## Step 2: Create Rasterization Options

Define the target page dimensions. You can also use this block to **set CAD page size** manually if you prefer a custom layout.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

## Step 3: Set Auto Layout Scaling

Enable the automatic scaling feature. This is the core of **how to set scaling** for a CAD‑to‑PDF conversion.

```java
rasterizationOptions.setAutomaticLayoutsScaling(true);
```

## Step 4: Create PDF Options

Link the rasterization settings to the PDF export options.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Step 5: Export to PDF

Finally, save the rendered image as a PDF file. This step completes the **convert DXF to PDF** workflow.

```java
image.save(dataDir + "result_out_.pdf", pdfOptions);
```

Repeat the steps above for any additional CAD files you need to process.

## Common Issues & Troubleshooting

| 症状 | 考えられる原因 | 対策 |
|---------|--------------|-----|
| 空白の PDF 出力 | ラスタライズオプションが設定されていない、またはファイルパスが間違っています | `srcFile` のパスを確認し、`setPageWidth/Height` がゼロでないことを確認してください |
| スケーリングが歪む | `setAutomaticLayoutsScaling` が `false` のまま | 自動スケーリングを有効にするか、手動でスケーリング係数を計算してください |
| レイヤーが欠落 | 元の DXF にサポートされていないエンティティが含まれています | サポートされているエンティティタイプについては Aspose.CAD のリリースノートを確認してください |

## FAQ's

### Q1: Aspose.CAD for Java はすべての CAD ファイル形式に対応していますか？

A1: Aspose.CAD for Java は DWG、DXF、DWF など、さまざまな CAD フォーマットをサポートしています。

### Q2: スケーリングオプションをさらにカスタマイズできますか？

A2: はい、`CadRasterizationOptions` クラスはスケーリングやその他の設定を細かく調整できるさまざまなプロパティを提供しています。

### Q3: Aspose.CAD for Java の追加ドキュメントはどこで見つけられますか？

A3: 詳細情報やサンプルについては、[documentation](https://reference.aspose.com/cad/java/) を参照してください。

### Q4: Aspose.CAD for Java の無料トライアルはありますか？

A4: はい、[free trial](https://releases.aspose.com/) を利用して Aspose.CAD for Java の機能を体験できます。

### Q5: Aspose.CAD for Java に関するサポートやディスカッションはどこで行えますか？

A5: コミュニティとつながりサポートを受けるには、[Aspose.CAD forum](https://forum.aspose.com/c/cad/19) をご利用ください。

**Additional Common Questions**

**Q: DWG ファイルを PDF に変換するにはどうすればいいですか（DXF ではなく）？**  
A: 同じコードで動作します。`srcFile` の拡張子を `.dwg` に変更するだけです。

**Q: 高解像度 PDF のためにカスタム DPI を設定できますか？**  
A: はい、`rasterizationOptions.setResolution(300);` のように（必要な DPI を指定して）設定できます。

**Q: 生成された PDF にフォントを埋め込むことは可能ですか？**  
A: Aspose.CAD は図面をラスタライズするため、フォントはベクトルとして描画され、別途フォント埋め込みは必要ありません。

## Conclusion

本ガイドに従うことで、Aspose.CAD for Java の Auto Layout Scaling を使用して **CAD から PDF を作成**する方法が分かります。このプロセスは **export CAD to PDF** ワークフローを簡素化し、一貫したスケーリングを保証し、開発時間を大幅に節約します。プロジェクトの要件に合わせて、さまざまなページサイズ、解像度、CAD フォーマットを自由に試してみてください。

---

**最終更新日:** 2025-12-10  
**テスト環境:** Aspose.CAD for Java 24.12 (latest)  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}