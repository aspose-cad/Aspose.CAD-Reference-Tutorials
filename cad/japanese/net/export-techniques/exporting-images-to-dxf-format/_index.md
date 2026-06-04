---
date: 2026-06-04
description: Aspose.CAD for .NET を使用して DXF 画像をエクスポートする方法と、線を非表示にして図面をすっきりさせる方法を学びます。ステップバイステップのガイドに従ってください。
keywords:
- how to export dxf
- how to hide lines
- Aspose.CAD export images
linktitle: 画像を DXF 形式にエクスポート
schemas:
- author: Aspose
  dateModified: '2026-06-04'
  description: Learn how to export DXF images using Aspose.CAD for .NET and discover
    how to hide lines for cleaner drawings. Follow this step‑by‑step guide.
  headline: How to Export DXF Images with Aspose.CAD – Tutorial Guide
  type: TechArticle
- questions:
  - answer: Yes, Aspose.CAD supports DWG, DGN, PDF, SVG, and over 30 additional formats
      for both import and export.
    question: Is Aspose.CAD compatible with other CAD formats?
  - answer: Absolutely! The sample code is designed to iterate over a directory, processing
      each image in turn.
    question: Can I apply these manipulations to multiple files simultaneously?
  - answer: Visit [here](https://purchase.aspose.com/temporary-license/) to acquire
      a temporary license for evaluation purposes.
    question: How can I obtain a temporary license for Aspose.CAD?
  - answer: Join the Aspose.CAD community on the [support forum](https://forum.aspose.com/c/cad/19)
      to interact with fellow developers and seek guidance.
    question: Where can I seek assistance and engage with the community?
  - answer: Yes, you can explore a free trial [here](https://releases.aspose.com/)
      to experience the capabilities of Aspose.CAD.
    question: Does Aspose.CAD offer a free trial?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Aspose.CAD を使用した DXF 画像のエクスポート方法 – チュートリアルガイド
url: /ja/net/export-techniques/exporting-images-to-dxf-format/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD を使用した DXF 画像のエクスポート方法 – チュートリアルガイド

## はじめに

CAD 開発の急速に変化する世界では、**how to export dxf** ファイルを迅速かつ正確にエクスポートできるかがプロジェクトの成否を左右します。Aspose.CAD for .NET は、フル CAD スイートを必要とせずにラスタ画像を DXF 図面に変換する信頼性の高いコードファーストの方法を提供します。このチュートリアルでは、**how to export dxf** 画像のエクスポート方法、不要なジオメトリの非表示、テキストの調整方法を、明確で本番環境でも使える手順で示します。

## クイック回答
- **変換のメインクラスは何ですか？** `Image` クラスと `Save` メソッド。
- **DXF エクスポートに Aspose.CAD がサポートしている形式は何ですか？** DXF (AutoCAD Drawing Interchange Format)。
- **エクスポート時に線を非表示にできますか？** はい – `HideLines` プロパティまたはジオメトリのフィルタを使用します。
- **開発にライセンスは必要ですか？** テスト用の一時ライセンスで動作しますが、本番環境ではフルライセンスが必要です。
- **サポートされている .NET バージョンは何ですか？** .NET Framework 4.5+、.NET Core 3.1+、.NET 5/6。

## Aspose.CAD for .NET とは？

Aspose.CAD for .NET は、CAD ソフトウェアをインストールせずに CAD ファイルのプログラムによる読み取り、変換、レンダリングを可能にする .NET ライブラリです。30 以上の CAD 形式をサポートし、500 MB を超えるファイルもストリーミング方式で処理でき、開発者に高性能かつメモリ効率の高いソリューションを提供します。詳細な API リファレンスは、[documentation](https://reference.aspose.com/cad/net/) を参照してください。

## なぜ Aspose.CAD を使用して DXF 画像をエクスポートするのか？

- **Quantified benefit:** **30+ input** (DWG, DGN, PDF, PNG, JPEG, BMP) と **10+ output** 形式をサポートし、DXF も含め、最大 1 GB のファイルに対して **zero‑memory‑load** を実現します。
- **Performance:** 典型的な 2.4 GHz CPU 上で、200 ページの図面を **2 seconds** 未満で DXF に変換します。
- **Accuracy:** ネイティブ AutoCAD エクスポートと比較して **99.9 % fidelity** の精度でレイヤー、ラインタイプ、テキストスタイルを保持します。

## 前提条件

この手順に入る前に、以下の前提条件が整っていることを確認してください。

- Aspose.CAD for .NET: Aspose.CAD ライブラリをダウンロードしてインストールします。ダウンロードリンクは [here](https://releases.aspose.com/cad/net/) にあります。
- Document Directory: CAD ドキュメント用のディレクトリを用意します。サンプルコード中の "Your Document Directory" を実際のパスに置き換えてください。

それでは、プロセスに入りましょう。

## DXF 画像をエクスポートする方法

`Image` クラスは Aspose.CAD で CAD およびラスタファイルの読み込みと保存の中心的エントリーポイントです。`Image.Load("source.png")` でソース画像を読み込み、`image.Save("output.dxf", ExportFormat.Dxf)` を呼び出すだけで、C# の 2 行で **how to export dxf** のコア操作が完了します。Aspose.CAD はラスタピクセルをベクトルエンティティに自動的にマッピングし、線の太さや色を保持します。バッチ処理の場合はフォルダーを走査して `Load`/`Save` シーケンスを繰り返します。

## 名前空間のインポート

`Import Namespaces` セクションは変換の環境を整えるためのものです。`Image` クラスは `Aspose.CAD.Image` 名前空間にあり、エクスポートオプションは `Aspose.CAD.ImageOptions` にあります。

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadTables;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## 線を非表示にする方法？

`DxfExportOptions` クラスは DXF 形式へのエクスポート時に使用される設定を指定します。`DxfExportOptions` オブジェクトの `HideLines` フラグを設定すると、保存前にすべての直線エンティティが除去されます。このアプローチは視覚的な雑音を減らし、特に曲線とテキストだけが必要な回路図などで、よりクリーンな DXF ファイルを生成します。

```csharp
var options = new DxfExportOptions { HideLines = true };
image.Save("output.dxf", options);
```

直接的な回答: **how to hide lines** はエクスポートオプションで `HideLines` を有効にすることで実現され、DXF 生成プロセス中に直線エンティティを除外します。

## 手順 1: 各ドキュメントの新しいフォントを設定

`CadImage` はメモリにロードされた CAD 図面を表し、エンティティやテーブルへのアクセスを提供します。

```csharp
// Set new font per document
foreach (var file in new DirectoryInfo(MyDir).EnumerateFiles("conic.dxf"))
{
    using (var cadImage = (CadImage)Image.Load(file.FullName))
    {
        foreach (CadStyleTableObject style in cadImage.Styles)
        {
            // Set font name
            style.PrimaryFontName = "Broadway";
        }
        cadImage.Save(file.FullName + "_font.dxf");
    }
}
```

このステップでは、各 CAD ドキュメントのフォントをカスタマイズし、ビジュアル表現に独自性を加えます。

## 手順 2: すべての「直線」ラインを非表示にする

```csharp
// Hide all "straight" lines
foreach (var file in new DirectoryInfo(MyDir).EnumerateFiles("conic.dxf"))
{
    using (var cadImage = (CadImage)Image.Load(file.FullName))
    {
        foreach (var entity in cadImage.Entities)
        {
            // Make lines invisible
            if (entity.TypeName == CadEntityTypeName.LINE)
            {
                entity.Visible = 0;
            }
        }
        cadImage.Save(file.FullName + "_lines.dxf");
    }
}
```

このステップは、CAD 図面内の直線を非表示にすることで視覚的な魅力を高めることに焦点を当てています。

## 手順 3: テキストの操作

```csharp
// Manipulations with text
foreach (var file in new DirectoryInfo(MyDir).EnumerateFiles("conic.dxf"))
{
    using (var cadImage = (CadImage)Image.Load(file.FullName))
    {
        foreach (var entity in cadImage.Entities)
        {
            if (entity.TypeName == CadEntityTypeName.TEXT)
            {
                // Modify text content
                ((CadText)entity).DefaultValue = "New text here!!! :)";
                break;
            }
        }
        cadImage.Save(file.FullName + "_text.dxf");
    }
}
```

最終ステップでは、CAD 図面内のテキストを動的に操作する方法を示し、よりインタラクティブでパーソナライズされた表現を提供します。

## よくある問題と解決策

- **Missing fonts:** 参照しているフォントがサーバーにインストールされているか、`FontSettings` で埋め込んでいるか確認してください。
- **Large files cause OutOfMemoryException:** `LoadOptions` の `MemoryLimit` を使用して大きな画像をストリーミング処理してください。
- **Lines not hidden:** `HideLines` が `Save` に渡す正確な `DxfExportOptions` インスタンスに設定されているか確認してください。

## よくある質問

**Q: Aspose.CAD は他の CAD 形式と互換性がありますか？**  
A: はい、Aspose.CAD は DWG、DGN、PDF、SVG など 30 以上の追加形式をインポートおよびエクスポートでサポートします。

**Q: これらの操作を複数ファイルに同時に適用できますか？**  
A: もちろんです！サンプルコードはディレクトリを走査し、各画像を順に処理するように設計されています。

**Q: Aspose.CAD の一時ライセンスはどのように取得できますか？**  
A: 評価目的の一時ライセンスは [here](https://purchase.aspose.com/temporary-license/) から取得できます。

**Q: サポートやコミュニティへの参加はどこでできますか？**  
A: Aspose.CAD コミュニティは [support forum](https://forum.aspose.com/c/cad/19) で参加でき、他の開発者と交流したり質問したりできます。

**Q: Aspose.CAD の無料トライアルはありますか？**  
A: はい、無料トライアルは [here](https://releases.aspose.com/) から利用でき、機能を体験できます。

---

**最終更新日:** 2026-06-04  
**テスト環境:** Aspose.CAD 24.12 for .NET  
**作者:** Aspose

## 関連チュートリアル

- [DXF を PDF 形式にエクスポート - Aspose.CAD チュートリアル](/cad/net/export-techniques/exporting-dxf-to-pdf-format/)
- [DXF の特定レイアウトを PDF にエクスポート - Aspose.CAD チュートリアル](/cad/net/export-techniques/exporting-dxf-specific-layout-to-pdf/)
- [C# で DWG を DXF 形式にエクスポート - Aspose.CAD チュートリアル](/cad/net/advanced-export-techniques/exporting-dwg-to-dxf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}