---
date: 2026-04-06
description: C# と Aspose.CAD を使用して DWG を PDF に変換し、カスタムテキストを追加する方法を学びましょう。このステップバイステップガイドでは、DWG
  から PDF を生成し、テキストエンティティを挿入し、DWG のテキストフォントを変更する手順を紹介します。
keywords:
- convert dwg to pdf
- generate pdf from dwg
- insert text entity
- change dwg text font
- aspose cad dwg pdf
linktitle: C#でDWGファイルにテキストを追加する
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: DWG を PDF に変換し、C# でテキストを追加する – Aspose.CAD チュートリアル
url: /ja/net/dwg-file-manipulation/adding-text-to-dwg/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG を PDF に変換し C# でテキストを追加 – Aspose.CAD チュートリアル

## はじめに

CAD と .NET 開発の急速に変化する世界では、**DWG を PDF に変換**しながらカスタム注釈を挿入することが頻繁に求められます。クライアント向けに印刷可能な図面を生成したり、DWG に直接動的なメモを埋め込んだりする必要がある場合、Aspose.CAD を使用すれば作業はシンプルです。このチュートリアルでは **DWG を PDF に変換**し、**テキストエンティティを追加**し、さらに **DWG のテキストフォントを変更**する方法を C# で学びます。

## クイック回答
- **DWG‑to‑PDF 変換に最適なライブラリは？** Aspose.CAD for .NET  
- **変換時にカスタムテキストを追加できるか？** はい – `CadText` エンティティを作成し、保存前に追加します。  
- **本番環境でライセンスは必要か？** 商用ライセンスが必要です。無料トライアルも利用可能です。  
- **サポートされている .NET バージョンは？** .NET Framework 4.5+、.NET Core 3.1+、.NET 5/6+。  
- **テキストフォントを変更できるか？** はい、`CadText` の `StyleType` や `TextHeight` などのプロパティを調整します。

## 「DWG を PDF に変換する」とは？

DWG ファイルを PDF に変換すると、ベクターベースの CAD 図面が広く共有可能でデバイスに依存しないドキュメントに変わります。PDF は元のジオメトリとレイヤーを保持しつつ、注釈やテキスト、その他のメタデータを埋め込むことができます。Aspose.CAD はラスタライズとベクターレンダリングを自動で処理するため、サーバー上にサードパーティ製 CAD ソフトウェアを用意する必要はありません。

## 変換前に DWG にテキストを追加する理由

テキストを DWG に直接埋め込むことで、配置、スタイル、レイヤー割り当てを完全にコントロールできます。後で PDF に変換した際、テキストは配置した通りに表示され、設計意図が保持され、PDF エディタでの後処理が不要になります。

## 前提条件

開始する前に以下を用意してください。

- **Aspose.CAD ライブラリ** – [ダウンロードリンク](https://releases.aspose.com/cad/net/) から取得。  
- **動作する .NET 環境**（Visual Studio 2022、.NET 6、または互換性のあるバージョン）。  
- **テストファイル用フォルダー** – 本ガイドでは `MyDir` と呼びます。

それでは、手順を順に見ていきましょう。

## 名前空間のインポート

Aspose.CAD クラスにアクセスできるよう、必要な `using` 文を追加します。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects.AttEntities;
using Aspose.CAD.ImageOptions;
```

## 手順 1: DWG ファイルの読み込み

ソース DWG ファイルを `Image` オブジェクトにロードします。このオブジェクトから CAD エンティティにアクセスできます。

```csharp
string dwgPathToFile = MyDir + "SimpleEntites.dwg";
using (Image image = Image.Load(dwgPathToFile))
{
    // Subsequent steps will be performed inside this block
}
```

## 手順 2: CadText オブジェクトの作成（テキストエンティティの挿入）

`CadText` クラスは DWG 内の単一行テキストを表します。ここではスタイル、値、色、レイヤー、位置を設定します。`StyleType` や `TextHeight` を調整すれば **DWG テキストフォントの変更** が可能です。

```csharp
CadText cadText = new CadText();
cadText.StyleType = "Standard";          // Font/style – change to alter DWG text font
cadText.DefaultValue = "Some custom text";
cadText.ColorId = 256;                    // 256 = ByLayer (you can use a specific ACI color)
cadText.LayerName = "0";
cadText.FirstAlignment.X = 47.90;
cadText.FirstAlignment.Y = 5.56;
cadText.TextHeight = 0.8;                 // Height influences visual size
cadText.ScaleX = 0.0;
```

## 手順 3: テキストエンティティをモデルスペースに追加

DWG のモデルスペースはほとんどの描画エンティティを保持します。`*Model_Space` ブロックに `CadText` を追加することで、テキストが図面の一部になります。

```csharp
CadImage cadImage = (CadImage)image;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadText);
```

## 手順 4: PDF オプションの設定（DWG から PDF 生成）

DWG を PDF にレンダリングする際のラスタライズオプションを設定します。ページサイズ、描画タイプ、レイアウトなどを調整できます。

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;
cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## 手順 5: 変更した DWG を PDF として保存

最後に、変更済みの図面をエクスポートします。生成された PDF には新しく挿入したテキストが含まれます。

```csharp
image.Save(MyDir + "SimpleEntites_generated.pdf", pdfOptions);
```

> **プロのコツ:** 高解像度の PDF が必要な場合は、`PageHeight` と `PageWidth` を比例して増やしてください。

## よくある問題と解決策

| 問題 | 原因 | 対策 |
|------|------|------|
| テキストが PDF に表示されない | レイヤーまたはカラー ID が間違っている | `LayerName` が存在し、`ColorId` が見える色（例: 7＝白）に設定されていることを確認 |
| テキストの位置がずれる | アラインメント座標が不正確 | 描画単位に対する `FirstAlignment.X/Y` の値を確認 |
| PDF が空白になる | ラスタライズオプションが未設定 | `DrawType` を `UseObjectColor` または `UseObjectLineWeight` に設定 |

## FAQ（既存）

### Q1: Aspose.CAD はすべての DWG バージョンに対応していますか？

A1: Aspose.CAD は幅広い DWG バージョンをサポートしており、さまざまな CAD ソフトウェアとの互換性が確保されています。

### Q2: Aspose.CAD を使って単一の DWG ファイルに複数のテキストエンティティを追加できますか？

A2: はい、チュートリアルで示した手順を繰り返すことで、複数のテキストエンティティを DWG に追加できます。

### Q3: Aspose.CAD でテキストのフォントやスタイルを変更するには？

A3: `CadText` オブジェクトのプロパティを調整し、DWG に追加する前にフォントやスタイルを設定します。

### Q4: 商用プロジェクトで Aspose.CAD を使用する際のライセンス上の注意点はありますか？

A5: はい、Aspose.CAD のライセンス条件を遵守してください。詳細は [Aspose.CAD Purchase](https://purchase.aspose.com/buy) を参照してください。

### Q5: Aspose.CAD に関する質問や議論はどこで行えますか？

A5: コミュニティやサポートは [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) で利用できます。

## 追加 FAQ

**Q: テキストを追加せずに DWG から PDF を生成するには？**  
A: `CadText` 作成ステップを省略し、`PdfOptions` を直接設定して `image.Save(...)` を呼び出します。

**Q: テキストの色をプログラムで変更できますか？**  
A: はい、`cadText.ColorId` に特定の ACI カラー番号（例: 1＝赤）を設定します。

**Q: 複数行テキストを挿入できますか？**  
A: 複数行テキストには `CadMText` を使用します。手順は `CadText` と同様です。

**Q: 複数の DWG ファイルをバッチ変換することは可能ですか？**  
A: もちろん可能です。ディレクトリ内の DWG ファイルをループ処理し、同じ手順で各ファイルを PDF に保存します。

## 結論

これで **DWG を PDF に変換**し、**カスタムテキストを追加**、さらに **テキストの外観をカスタマイズ**するための、C# と Aspose.CAD を使用した本格的なワークフローが完成しました。この手法は自動図面生成、レポートパイプライン、または CAD ファイルをリアルタイムで強化するあらゆるシナリオに最適です。

---

**最終更新日:** 2026-04-06  
**テスト環境:** Aspose.CAD 24.11 for .NET  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}