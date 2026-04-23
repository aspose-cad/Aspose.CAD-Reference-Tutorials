---
date: 2026-03-21
description: .NET 用 Aspose.CAD を使用して DWG から PDF を作成し、DWG の一部として DGN をエクスポートする方法を学びます。このガイドでは、DWG
  を PDF に変換し、PDF のオプションを設定する方法も示しています。
linktitle: Export DGN as Part of DWG
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: DWG から PDF を作成し、DWG の一部として DGN をエクスポート – Aspose.CAD for .NET
url: /ja/net/cad-export-formats/export-dgn-as-part-of-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG から PDF を作成し、DGN を DWG の一部としてエクスポート – Aspose.CAD for .NET

## はじめに

DWG ファイルから **PDF を作成** し、さらに DGN デザインを DWG の一部として埋め込みたい場合、Aspose.CAD for .NET を使用すれば簡単に実現できます。このチュートリアルでは、DWG の読み込み、埋め込まれた DGN アンダーレイの検索、ラスタライズオプションの設定、最終的に PDF ドキュメントへエクスポートするまでの全工程を解説します。バッチ変換ツール、レポートエンジン、CAD‑BIM 統合サービスの構築を検討している方に、実践的で本番環境でも使える基盤を提供します。

## クイック回答
- **DWG → PDF 変換を処理するライブラリは何ですか？** Aspose.CAD for .NET  
- **PDF を作成しながら DGN アンダーレイをエクスポートできますか？** はい – アンダーレイは `CadDgnUnderlay` でアクセスできます。  
- **PDF オプションを設定するメソッドはどれですか？** `PdfOptions` と `CadRasterizationOptions` を組み合わせて使用します。  
- **商用利用にはライセンスが必要ですか？** はい、有効な Aspose.CAD ライセンスが必要です。  
- **サポートされている .NET バージョンは？** .NET Framework 4.5 以上、.NET Core 3.1 以上、.NET 5/6/7。

## 「DWG から PDF を作成する」とは何ですか？

DWG ファイルから PDF を作成するとは、ベクタードローイングをラスタまたはベクターベースの PDF ドキュメントにレンダリングすることを指します。このプロセスは、CAD ソフトを持たないステークホルダーへの図面共有、アーカイブ、印刷可能なレポートの生成に便利です。Aspose.CAD は DWG エンティティの解析と `PdfOptions` による細かな出力制御を自動で行い、作業を大幅に簡略化します。

## なぜ DGN を DWG の一部としてエクスポートするのか？

DGN アンダーレイは、MicroStation プロジェクトからの参照ジオメトリを表すことが多いです。DWG と共に DGN をエクスポートすれば、元の設計コンテキストを保持でき、下流の利用者が完全な図面セットを確認できます。DWG と DGN が共存するマルチディシプリンプロジェクトで特に有用です。

## 前提条件

- **Aspose.CAD for .NET** – こちらからダウンロードしてください [here](https://releases.aspose.com/cad/net/)。  
- **開発環境** – Visual Studio（最新バージョン）またはお好みの .NET IDE。  
- **基本的な C# の知識** – C# の構文と .NET プロジェクト構造に慣れている必要があります。

## 名前空間のインポート

C# ソースファイルの先頭に必要な `using` ディレクティブを追加します:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## 手順ガイド

### 手順 1: ファイルパスの定義

入力 DWG ファイルと出力 PDF の名前を設定します。

```csharp
// Input and Output file paths
string fileName = "BlockRefDgn.dwg";
string outPath = fileName + ".pdf";
```

### 手順 2: `PdfOptions` インスタンスの作成（PDF オプションの設定）

`PdfOptions` を使用すると、ページサイズ、圧縮、メタデータなど、PDF の生成方法を細かく制御できます。

```csharp
// Create an instance of PdfOptions class for exporting DWG to PDF
PdfOptions exportOptions = new PdfOptions();
```

### 手順 3: DWG ファイルの読み込み

DWG を `CadImage` としてロードし、エンティティを検査できるようにします。

```csharp
// Load the existing DWG file as an image and convert it to CadImage type
using (CadImage cadImage = (CadImage)Image.Load(fileName))
```

### 手順 4: エンティティの反復処理

図面内のすべてのエンティティを走査し、DGN アンダーレイを探します。

```csharp
// Iterate through each entity inside the DWG file
foreach (CadBaseEntity baseEntity in cadImage.Entities)
```

### 手順 5: エンティティタイプの確認（DGN のエクスポート方法）

現在のエンティティが DGN アンダーレイかどうかを判定します。

```csharp
// Check if the entity is an image definition
if (baseEntity.TypeName == CadEntityTypeName.DGNUNDERLAY)
```

### 手順 6: アンダーレイパスの取得

DGN ファイルの外部参照パスを取得します。

```csharp
// If it's an image definition, get the external reference to the object
CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
Console.WriteLine(dgnFile.UnderlayPath);
```

### 手順 7: ラスタライズオプションの定義（DWG を PDF に変換）

PDF に配置する前に DWG をどのようにラスタライズするかを設定します。

```csharp
// Define settings for CadRasterizationOptions object
exportOptions.VectorRasterizationOptions = new CadRasterizationOptions()
{
    PageWidth = 1600,
    PageHeight = 1600,
    Layouts = new string[] { "Model" },
    AutomaticLayoutsScaling = false,
    NoScaling = true,
    BackgroundColor = Color.Black,
    DrawType = CadDrawTypeMode.UseObjectColor
};
```

### 手順 8: DWG を PDF にエクスポート

最終的に、レンダリングされた画像を PDF ファイルとして保存します。

```csharp
// Export the DWG to PDF by calling Save method
cadImage.Save(outPath, exportOptions);
```

## よくある問題と解決策

| 問題 | 原因 | 対策 |
|------|------|------|
| **`Image.Load` が “File not found” をスロー** | パスが間違っているか、ファイルが存在しません。 | 絶対パスを使用するか、DWG が出力フォルダーにコピーされていることを確認してください。 |
| **アンダーレイパスが空です** | DGN アンダーレイが埋め込まれていないか、参照が壊れています。 | DWG に実際に DGN アンダーレイが含まれていること、外部 DGN ファイルにアクセスできることを確認してください。 |
| **PDF 出力が空白** | ラスタライズオプションがサイズゼロに設定されています。 | `PageWidth`/`PageHeight` を調整するか、`NoScaling = false` に設定してください。 |
| **ライセンス例外** | 有効な Aspose.CAD ライセンスなしで実行しています。 | 画像をロードする前にライセンスを適用してください: `License lic = new License(); lic.SetLicense("Aspose.CAD.lic");` |

## よくある質問

### Q1: 商用プロジェクトで Aspose.CAD for .NET を使用できますか？
A1: はい、可能です。ライセンスオプションは [here](https://purchase.aspose.com/buy) をご覧ください。

### Q2: 処理できる DWG ファイルのサイズに制限はありますか？
A2: Aspose.CAD は大きな DWG ファイルの処理をサポートしていますが、ハードウェアの制限が影響する場合があります。

### Q3: 試用版はありますか？
A3: はい、無料トライアルは [here](https://releases.aspose.com/) から入手できます。

### Q4: 一時ライセンスはどのように取得できますか？
A4: 一時ライセンスは [here](https://purchase.aspose.com/temporary-license/) で取得できます。

### Q5: 問題が発生した場合、どこでサポートを受けられますか？
A5: サポートは Aspose.CAD フォーラム [here](https://forum.aspose.com/c/cad/19) で受けられます。

**Q: 追加の PDF メタデータ（作者、タイトルなど）を設定するには？**  
A: `Save` を呼び出す前に `exportOptions.Metadata` プロパティを使用します。

**Q: 複数のレイアウトを別々の PDF ページにエクスポートできますか？**  
A: はい – `CadRasterizationOptions` の `Layouts = new string[] { "Layout1", "Layout2" }` を設定します。

**Q: Aspose.CAD は DWG を他の画像形式に変換することをサポートしていますか？**  
A: もちろんです。対応する `Image.Save` のオーバーロードを使用して PNG、JPEG、SVG などにエクスポートできます。

**最終更新日:** 2026-03-21  
**テスト環境:** Aspose.CAD 24.11 for .NET  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}