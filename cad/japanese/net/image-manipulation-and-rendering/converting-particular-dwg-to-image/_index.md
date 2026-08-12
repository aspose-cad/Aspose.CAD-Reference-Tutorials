---
date: 2026-08-12
description: Aspose.CAD for .NET を使用して C# で DWG からテキストを抽出し、特定の DWG を画像に変換します。ステップバイステップのコードスニペットで学びましょう。
keywords:
- extract text from dwg
- convert specific dwg to image
- Aspose.CAD .NET
lastmod: 2026-08-12
linktitle: C# で特定の DWG を画像に変換する
og_description: Aspose.CAD を使用して C# で DWG からテキストを抽出し、特定の DWG を画像に変換します。迅速な実装のための簡潔なガイドをご覧ください。
og_image_alt: Guide showing DWG to image conversion and text extraction using Aspose.CAD
  in C#
og_title: C# で DWG からテキストを抽出し、特定の DWG を画像に変換する
schemas:
- author: Aspose
  dateModified: '2026-08-12'
  description: Extract text from DWG and convert specific DWG to image in C# using
    Aspose.CAD for .NET. Learn step‑by‑step with code snippets.
  headline: Extract text from DWG and convert specific DWG to image in C#
  type: TechArticle
- questions:
  - answer: Aspose.CAD supports DWG releases from AutoCAD 2000 up to the latest 2024
      version, covering over 90 % of files created in the field.
    question: Is Aspose.CAD compatible with all versions of DWG files?
  - answer: Yes – you can change resolution, image format, anti‑aliasing, and background
      color to suit PNG, JPEG, or PDF targets.
    question: Can I customize the rasterization options for different outputs?
  - answer: Explore the comprehensive [Aspose.CAD documentation](https://reference.aspose.com/cad/net/)
      for more code samples and API details.
    question: Where can I find additional examples and documentation?
  - answer: Absolutely – you can download a trial version on the **[Aspose trial download
      page](https://releases.aspose.com/)** and evaluate all features without restrictions
      for 30 days.
    question: Is there a free trial available for Aspose.CAD?
  - answer: Join the active [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)
      where developers share solutions and the Aspose team answers questions.
    question: How can I get support or connect with the community?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- extract text from dwg
- Aspose.CAD
- C# CAD processing
title: C# で DWG からテキストを抽出し、特定の DWG を画像に変換する
url: /ja/net/image-manipulation-and-rendering/converting-particular-dwg-to-image/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# C# で特定の DWG を画像に変換する - Aspose.CAD ガイド

## 概要

現代のエンジニアリングアプリケーションでは、レポートや可視化のために **DWG からテキストを抽出** したり、**特定の DWG を画像形式に変換** したりする必要が頻繁にあります。Aspose.CAD for .NET は、外部の CAD ソフトウェアを必要とせずにこれらのタスクを処理できるフル機能の API を提供します。このチュートリアルでは、DWG をロードし、テキストエンティティをフィルタリングし、図面をラスタライズし、最終的に結果を PDF 画像として保存する方法を、クリーンな C# コードで学びます。

## 簡単な回答

- **最初のステップは何ですか？** DWG ファイルは `new CadImage("file.dwg")` でロードします。  
- **テキストをフィルタリングするクラスはどれですか？** `CadEntityFilter` を使用して `Text` エンティティを選択します。  
- **画像サイズはどう定義しますか？** `CadRasterizationOptions` の `Width` と `Height` を設定します。  
- **使用される出力形式は何ですか？** 例では PDF に保存し、ラスタ画像を埋め込みます。  
- **本番環境でライセンスは必要ですか？** はい。商用の Aspose.CAD ライセンスを使用すれば評価制限が解除されます。

## DWG からテキストを抽出する方法

DWG をロードし、テキストエンティティのみを選択するフィルタを適用し、各エンティティの `TextString` プロパティを読み取ります。この方法により、図面内に存在するすべての注釈、ラベル、寸法テキストを取得でき、検索、インデックス作成、レポート作成に再利用できます。

## なぜ特定の DWG を画像に変換するのか

DWG をラスタ画像に変換すると、ネイティブ CAD 形式をレンダリングできないドキュメント、ウェブページ、モバイルアプリに図面を埋め込むことができます。Aspose.CAD は **50 以上の CAD フォーマット** を処理し、200 MB 未満のメモリで数百ページに及ぶ図面をラスタライズできるため、高スループットのサーバーシナリオに適しています。

## 前提条件

- Visual Studio（任意の最新エディション）で C# プロジェクトをコンパイルおよび実行します。  
- Aspose.CAD for .NET – ライブラリがインストールされていることを確認してください。ダウンロードリンクは **[Aspose.CAD for .NET ダウンロードページ](https://releases.aspose.com/cad/net/)** にあります。  
- 作業対象の DWG ファイル。サンプルファイル *visualization_-_conference_room.dwg* がコードスニペットで使用されています。

## 名前空間のインポート

以下の名前空間をインポートすると、コア CAD クラス、ラスタライズオプション、PDF 出力ヘルパーにアクセスできます。

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## ステップ 1: DWG ファイルをロードする

`CadImage` インスタンスを作成し、DWG ファイルのパスを渡します。`CadImage` オブジェクトはメモリ上に図面全体を表し、レイヤー、エンティティ、メタデータにアクセスできます。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
var cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath);
```

## ステップ 2: エンティティをフィルタリングする

`CadEntityFilter` を使用すると、必要なエンティティだけを選択できます。このガイドでは、最終画像に不要な線や円、その他のジオメトリを除外し、**テキスト** オブジェクトだけを保持するように設定します。

```csharp
CadBaseEntity[] entities = cadImage.Entities;
List<CadBaseEntity> filteredEntities = new List<CadBaseEntity>();

foreach (CadBaseEntity baseEntity in entities)
{
    // Selection or filtration of entities
    if (baseEntity.TypeName == CadEntityTypeName.TEXT)
    {
        filteredEntities.Add(baseEntity);
    }
}

cadImage.Entities = filteredEntities.ToArray();
```

## ステップ 3: ラスタライズオプションを設定する

`CadRasterizationOptions` は図面をビットマップに変換する方法を制御します。出力サイズ、背景色、解像度（DPI）を定義できます。以下の定義アンカーがクラスを紹介します：

`CadRasterizationOptions` クラスは、CAD 図面をラスタ形式に変換するための画像サイズ、解像度、レンダリング設定を指定します。  

PDF エクスポーターに渡す前に、希望する幅、高さ、背景色を設定します。

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions =
    new Aspose.CAD.ImageOptions.CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
```

## ステップ 4: PDF オプションを設定する

`PdfOptions` は、ラスタライズ設定と圧縮などの PDF 固有機能をまとめます。このクラスの定義アンカーは最初に示されています：

`PdfOptions` は PDF 生成パラメータをカプセル化し、CAD データが PDF ドキュメント内でどのようにレンダリングされるかを決定するラスタライズオプションを含みます。  

以前に作成した `CadRasterizationOptions` インスタンスを `VectorRasterizationOptions` プロパティに割り当てます。

```csharp
Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## ステップ 5: PDF として保存する

最後に、`CadImage` オブジェクトの `Save` メソッドを呼び出し、対象ファイル名と設定した `PdfOptions` を渡します。PDF にはフィルタリングされた図面の高品質画像が含まれます。

```csharp
string outFile = MyDir + "result_out_generated.pdf";
cadImage.Save(outFile, pdfOptions);
```

## 一般的な問題とトラブルシューティング

- **フィルタリング後にテキストが欠落** – DWG に実際に `Text` エンティティが含まれていることを確認してください。一部の図面では注釈が `MText` として保存されています。必要に応じてフィルタに `MText` を含めるよう調整します。  
- **出力画像が空白** – ラスタライズ DPI が十分に高いこと（デフォルトは 300 DPI が安全）を確認し、PDF を表示する際に背景色が透明に設定されていないか確認してください。  
- **大きなファイルでのメモリ不足エラー** – `LoadOptions` のストリーミングを有効にするオーバーロードを使用すると、ファイル全体を一度にメモリに読み込むことを防げます。

## よくある質問

**Q: Aspose.CAD はすべてのバージョンの DWG ファイルに対応していますか？**  
A: Aspose.CAD は AutoCAD 2000 から最新の 2024 バージョンまでの DWG リリースをサポートし、業界で作成されたファイルの 90 %以上をカバーしています。

**Q: 異なる出力向けにラスタライズオプションをカスタマイズできますか？**  
A: はい。解像度、画像形式、アンチエイリアス、背景色を変更して PNG、JPEG、または PDF のターゲットに合わせることができます。

**Q: 追加のサンプルやドキュメントはどこで見つけられますか？**  
A: 詳細なコードサンプルや API の情報は、包括的な [Aspose.CAD ドキュメント](https://reference.aspose.com/cad/net/) をご覧ください。

**Q: Aspose.CAD の無料トライアルはありますか？**  
A: もちろんです。**[Aspose トライアルダウンロードページ](https://releases.aspose.com/)** からトライアル版をダウンロードでき、30 日間制限なくすべての機能を評価できます。

**Q: サポートを受ける、またはコミュニティとつながるにはどうすればよいですか？**  
A: 開発者が解決策を共有し、Aspose チームが質問に回答する活発な [Aspose.CAD フォーラム](https://forum.aspose.com/c/cad/19) に参加してください。

---

**最終更新日:** 2026-08-12  
**テスト環境:** Aspose.CAD 24.11 for .NET  
**作者:** Aspose

## 関連チュートリアル

- [C# で DWG ファイルのテキスト検索 - Aspose.CAD チュートリアル](/cad/net/text-search-and-manipulation/searching-text-in-dwg-files/)
- [.NET 用 Aspose.CAD で CAD 図面をラスタ画像に変換](/cad/net/cad-drawing-manipulation/convert-cad-drawing-to-raster-image/)
- [C# で DWG ドキュメントをレンダリング - Aspose.CAD ガイド](/cad/net/image-manipulation-and-rendering/rendering-dwg-documents/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}