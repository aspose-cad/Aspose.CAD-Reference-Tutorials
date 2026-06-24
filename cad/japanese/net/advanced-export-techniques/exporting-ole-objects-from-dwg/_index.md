---
description: Aspose.CAD for .NET を使用して DWG を PNG に変換し、DWG ファイルから OLE オブジェクトを抽出する方法を学ぶ
  – 短くコード中心のガイド。
linktitle: Exporting OLE Objects from DWG Files
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: DWG を PNG に変換 & OLE オブジェクトをエクスポート - Aspose.CAD チュートリアル
url: /ja/net/advanced-export-techniques/exporting-ole-objects-from-dwg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG ファイルから OLE オブジェクトをエクスポートする - Aspose.CAD チュートリアル

## Introduction

DWG を PNG に **変換** しながら埋め込まれた OLE オブジェクトを抽出したい場合は、こちらが最適です。Aspose.CAD for .NET を使用すれば、この 2 段階のプロセスを数行の C# で自動化でき、抽出とラスタライズが簡単に行えます。次の数分で、環境設定から DWG を PNG に保存し、抽出した OLE データを含めるまでの全手順をご紹介します。

## Quick Answers
- **このチュートリアルで扱う内容は？** Aspose.CAD for .NET を使って DWG を PNG に変換し、OLE オブジェクトを抽出します。  
- **ライセンスは必要ですか？** 開発目的であれば無料トライアルで動作します。商用環境では有償ライセンスが必要です。  
- **対応している .NET バージョンは？** .NET Framework 4.5 以上、.NET Core 3.1 以上、.NET 5/6 以上。  
- **複数の DWG ファイルを同時に処理できますか？** はい – サンプルはファイル名の配列をループしています。  
- **他のサンプルはどこで見られますか？** 公式の Aspose.CAD ドキュメントとフォーラムのリンクをご確認ください。

## What is **convert DWG to PNG**?
DWG（AutoCAD 図面）を PNG 画像に変換すると、ベクターデータがラスタライズされ、Web ページやレポート、DWG を直接サポートしないアプリケーションで簡単に表示・埋め込みできるようになります。OLE オブジェクトが含まれている場合、変換時にそれらを抽出して別ファイルとして保存できます。

## Why extract OLE objects from CAD files?
多くの DWG 図面には、スプレッドシートやチャート、その他の Office 文書が OLE オブジェクトとして埋め込まれています。これらを抽出すれば、元データを再利用したり、レポートを自動化したり、埋め込み情報を失わずに新しいフォーマットへ移行したりできます。

## Prerequisites

- Aspose.CAD for .NET Library: ライブラリがインストールされていることを確認してください。ダウンロードは [Aspose.CAD for .NET ダウンロードページ](https://releases.aspose.com/cad/net/) から行えます。  
- Document Directory: DWG ファイルを格納するディレクトリを用意します。コードスニペット中の `"Your Document Directory"` を実際のパスに置き換えてください。

## Import Namespaces

In your .NET project, import the required namespaces:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Step‑by‑Step Guide

### Step 1: Set the Document Directory

```csharp
string MyDir = "Your Document Directory";
```

`"Your Document Directory"` を DWG ファイルが保存されているパスに置き換えます。

### Step 2: List the DWG files you want to process

```csharp
string[] files = new string[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

### Step 3: Configure export options for PNG conversion

```csharp
PngOptions pngOptions = new PngOptions { };
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.VectorRasterizationOptions = rasterizationOptions;
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

`CadRasterizationOptions`（例: `PageWidth`、`PageHeight`、`BackgroundColor`）を調整して、希望する出力解像度に合わせてください。

### Step 4: Iterate through each DWG and perform the conversion

```csharp
foreach (string file in files)
{
    using (CadImage cadImage = (CadImage)Image.Load(MyDir + file))
    {
        cadImage.Save(MyDir + file + "_out.png", pngOptions);
    }
}
```

このループ内で、ライブラリは自動的に各図面に埋め込まれた **OLE オブジェクトを抽出** し、生成された PNG に組み込みます。生の OLE ストリームが必要な場合は、`cadImage.OleObjects` コレクションにアクセスすれば、プログラムから **how to extract ole** データを取得できます。

## Common Issues & Troubleshooting

- **Missing layout name** – 指定したレイアウト（例: `"Layout1"`）が元の DWG に存在することを確認してください。存在しない場合は、ラスタライザがデフォルトのモデル空間にフォールバックします。  
- **Large files cause memory pressure** – ファイルは一つずつ処理し（上記例のように）、`using` ステートメントで `CadImage` オブジェクトを速やかに破棄してください。  
- **Unexpected colors** – 透過が必要な場合は、`rasterizationOptions.BackgroundColor` を図面の背景色に合わせて設定します。

## Frequently Asked Questions

### Q1: Aspose.CAD for .NET は初心者向けと上級者向けの CAD ファイルの両方に適していますか？
A1: はい、Aspose.CAD for .NET は多様な CAD ファイルに対応でき、初心者向けから上級者向けまで幅広く扱えます。

### Q2: レイアウトごとにエクスポートオプションをカスタマイズできますか？
A2: もちろんです！チュートリアルに示したように、レイアウトごとにエクスポートオプションを調整できます。

### Q3: Aspose.CAD for .NET の詳細なドキュメントはどこで確認できますか？
A3: 詳細情報とサンプルは [Aspose.CAD for .NET documentation](https://reference.aspose.com/cad/net/) をご覧ください。

### Q4: 無料トライアルはありますか？
A4: はい、無料トライアルで Aspose.CAD for .NET の機能を体験できます。[このリンク](https://releases.aspose.com/) から開始してください。

### Q5: サポートやコミュニティとの交流はどこで行えますか？
A5: サポートやコミュニティ参加は [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) をご利用ください。

### Q6: **PNG に変換せずに CAD から OLE を抽出**するにはどうすればよいですか？
A6: DWG をロードした後、`CadImage.OleObjects` コレクションを使用します。各 `OleObject` を列挙し、生データをファイルに保存すれば抽出できます。

## Conclusion

これで **DWG を PNG に変換** しながら **OLE オブジェクトをシームレスに抽出** する方法が分かりました。Aspose.CAD for .NET を活用すれば、手作業のコピー＆ペーストを省き、時間を大幅に短縮でき、自動化パイプラインにすっきりと組み込めます。JPEG や BMP など他のラスタ形式でも試したり、Aspose が提供する豊富な CAD 操作機能を探索したりしてみてください。

---

**Last Updated:** 2026-03-13  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}