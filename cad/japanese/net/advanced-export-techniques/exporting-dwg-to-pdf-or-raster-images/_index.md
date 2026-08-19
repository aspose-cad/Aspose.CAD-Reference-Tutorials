---
date: 2026-03-16
description: .NET 用 Aspose.CAD を使用して DWG を PDF やラスタ画像に変換する方法を学びましょう。このステップバイステップの
  CAD から PDF へのチュートリアルでは、DWG を PNG などの画像フォーマットにエクスポートする方法と、DWG を画像ファイルに効率的にエクスポートする方法を紹介します。
linktitle: Exporting DWG to PDF or Raster Images
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Aspose.CAD for .NET を使用して DWG を PDF およびラスタ画像に変換する方法
url: /ja/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG を PDF またはラスター画像にエクスポート - Aspose.CAD ガイド

## はじめに

.NET アプリケーションから直接 **DWG を PDF**（または PNG などのラスター形式）に変換する必要がある場合、ここが最適な場所です。このチュートリアルでは、Aspose.CAD for .NET を使用して変換を実行するために必要な正確な手順を順に解説し、ライブラリが優れた選択肢である理由を説明し、数行のコードだけで PDF と画像の両方の出力を処理する方法を示します。

## クイック回答
- **DWG 変換を処理するライブラリは何ですか？** Aspose.CAD for .NET  
- **DWG を PNG と PDF の両方にエクスポートできますか？** はい – 同じラスター化オプションが両フォーマットで機能します。  
- **開発にライセンスは必要ですか？** 無料トライアルでテスト可能です。商用環境では商用ライセンスが必要です。  
- **サポートされている .NET バージョンは？** .NET Framework 4.5 以上、.NET Core 3.1 以上、.NET 5/6 以上。  
- **単位変換は自動で処理されますか？** コード例のように、単位系（メートル法または帝国単位）を手動で定義できます。

## 「DWG を PDF に変換する」とは？
DWG を PDF に変換するとは、CAD 図面（DWG）をポータブルで閲覧専用のドキュメント（PDF）にレンダリングすることです。これにより、CAD ソフトを持っていないステークホルダーと設計を共有したり、印刷用ドキュメントを作成したり、汎用的に読める形式で図面をアーカイブしたりできます。

## なぜこの変換に Aspose.CAD を使用するのか？
- **外部依存なし** – ライブラリは完全にマネージドコードで動作します。  
- **高忠実度** – レイヤー、線幅、レイアウト情報を保持します。  
- **組み込みラスターオプション** – 単一の設定オブジェクトで PNG、JPEG、BMP などにエクスポート可能です。  
- **クロスプラットフォーム** – .NET Core で Windows、Linux、macOS 上で動作します。

## 前提条件

チュートリアルに入る前に、以下が準備できていることを確認してください。

- .NET プログラミングの基本的な理解。  
- Aspose.CAD for .NET ライブラリがインストール済み。未インストールの場合は、[here](https://releases.aspose.com/cad/net/) からダウンロードしてください。  
- .NET 開発用に設定されたお気に入りの統合開発環境（IDE）。

## 名前空間のインポート

まず、.NET プロジェクトで必要な名前空間をインポートします。これにより、コード内で Aspose.CAD の機能にアクセスできるようになります。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```

## 手順 1: DWG ファイルの読み込み

変換したい DWG ファイルを読み込みます。`"Your Document Directory"` を DWG ファイルへのパスに置き換えてください。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for loading DWG goes here
}
```

## 手順 2: PDF エクスポートの設定 (DWG を PDF にエクスポートする方法)

次に、PDF エクスポート設定を構成します。この例ではレイアウトの指定と単位変換の処理方法を示しています。

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };

// Check and define the unit system
bool currentUnitIsMetric = false;
double currentUnitCoefficient = 1.0;
DefineUnitSystem(cadImage.UnitType, out currentUnitIsMetric, out currentUnitCoefficient);

// Your code for setting up PDF export goes here
```

## 手順 3: PDF にエクスポート

設定したオプションを使用して PDF へのエクスポートを実行します。

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath, pdfOptions);
```

## 手順 4: ラスター画像にエクスポート (DWG を画像にエクスポート)

機能を拡張して、PNG などのラスター画像にエクスポートします。

```csharp
// A4 size at 300 DPI - 2480 x 3508
rasterizationOptions.PageHeight = 3508;
rasterizationOptions.PageWidth = 2480;

PngOptions pngOptions = new PngOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath.Replace("pdf", "png"), pngOptions);
```

## よくある問題と解決策

| 問題 | 発生原因 | 対処方法 |
|-------|----------------|------------|
| **PDF が空白ページになる** | レイアウトが正しく指定されていない | `rasterizationOptions.Layouts` に正しいレイアウト名（例: `"Model"`）が含まれていることを確認してください。 |
| **サイズが正しくない** | DPI またはページサイズの不一致 | `CadRasterizationOptions` の `PageHeight`、`PageWidth`、DPI の値を調整してください。 |
| **単位が間違って表示される** | 単位変換が定義されていない | `DefineUnitSystem` を使用して、`cadImage.UnitType` に基づき `currentUnitIsMetric` と `currentUnitCoefficient` を設定してください。 |
| **ライセンス例外が発生** | トライアル版の制限 | `Image.Load` を呼び出す前に、一時的または永続的なライセンスを適用してください。 |

## よくある質問

### Q1: Aspose.CAD for .NET を商用プロジェクトで使用できますか？
A1: はい、使用可能です。ライセンスの詳細は [purchase.aspose.com/buy](https://purchase.aspose.com/buy) をご覧ください。

### Q2: 無料トライアルはありますか？
A2: もちろんです！無料トライアルは [here](https://releases.aspose.com/) から取得できます。

### Q3: Aspose.CAD for .NET のサポートはどこで受けられますか？
A3: コミュニティサポートは [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) で提供されています。

### Q4: テスト目的の一時ライセンスは取得できますか？
A4: はい、[here](https://purchase.aspose.com/temporary-license/) から取得可能です。

### Q5: 詳細なドキュメントはどこにありますか？
A5: ドキュメントは [Aspose.CAD](https://reference.aspose.com/cad/net/) にあります。

### Q6: 高品質で **CAD を PNG に保存** するにはどうすればよいですか？
A6: `CadRasterizationOptions` で `PageHeight` と `PageWidth` を目的のピクセルサイズに設定し、DPI を 300 以上に設定してください。

### Q7: ソースファイルに複数のレイアウトが含まれている場合、**DWG を変換**する最適な方法は？
A7: エクスポートしたいすべてのレイアウト名を `rasterizationOptions.Layouts` に追加し、各レイアウトごとにループして `Save` を呼び出してください。

**最終更新日:** 2026-03-16  
**テスト環境:** Aspose.CAD 24.11 for .NET  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}