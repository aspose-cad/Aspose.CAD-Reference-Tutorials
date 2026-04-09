---
date: 2026-04-09
description: C# で DWFX ファイルをロードし、Aspose.CAD for .NET を使用して CAD を PDF に変換する方法を学びましょう。シームレスな統合のためのステップバイステップ
  ガイド。
keywords:
- load dwfx file c#
- c# convert cad to pdf
- aspose.cad dwfx
linktitle: C#でDWFXファイルを開くとアクセスする
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: C# で Aspose.CAD を使用して DWFX ファイルをロードする方法
url: /ja/net/dwg-file-manipulation/opening-and-accessing-dwfx-files/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# C#でDWFXファイルを読み込む方法 – Aspose.CAD ガイド

## はじめに

C#でDWFXファイルを**load DWFX file C#**し、PDFに変換したい場合は、ここが適切な場所です。このチュートリアルでは、Aspose.CAD for .NET を使用して DWFX 図面を開き、ラスター化を設定し、最終的に**c# convert CAD to PDF**するための正確な手順を順に説明します。デスクトップユーティリティでもウェブサービスでも、アプローチは同じで、Aspose.CAD がサポートする任意の .NET バージョンで動作します。

## クイック回答
- **どのライブラリが必要ですか？** Aspose.CAD for .NET  
- **DWFX を PDF に変換できますか？** はい – `CadRasterizationOptions` を設定し、`PdfOptions` を使用するだけです。  
- **サポートされている .NET バージョンはどれですか？** .NET Framework 4.5+、.NET Core 3.1+、.NET 5/6+。  
- **テストにライセンスは必要ですか？** 開発には無料トライアルで問題ありませんが、本番環境では永続ライセンスが必要です。  
- **コードの実行時間はどれくらいですか？** 一般的な DWFX ファイルの読み込みと変換は、最新の CPU で 1 秒未満で完了します。

## DWFX ファイルとは？

DWFX（Design Web Format XPS）は、CAD 図面を XML 形式で表現したもので、ブラウザやその他のビューアで表示できます。ベクターデータを保持しているため、詳細を失うことなく高品質な PDF 変換に最適です。

## C#でDWFXファイルを読み込む際に Aspose.CAD を使用する理由

* **フルフォーマットサポート** – Aspose.CAD は DWFX を含む多数の CAD フォーマットを理解します。  
* **外部依存なし** – 純粋な .NET で、AutoCAD や他のネイティブコンポーネントは不要です。  
* **簡単なラスターからベクターへの変換** – 数行のコードでラスター画像とベクタ PDF を切り替えられます。  

## 前提条件

コードに入る前に、以下が揃っていることを確認してください。

1. **Aspose.CAD for .NET** がインストールされていること。ダウンロードは[here](https://releases.aspose.com/cad/net/)から。  
2. 処理したい DWFX ファイルが入っているフォルダー。ソースと出力先のフルパスをメモしておいてください。

## C#でDWFXファイルを読み込む方法

以下はステップバイステップのガイドです。各ステップには簡単な説明が付いており、続いてコピーすべき正確なコードブロックが示されています。

### 名前空間のインポート

```csharp
using Aspose.CAD.ImageOptions;
using System;
```

これらの名前空間により、CAD ファイルの読み込みに使用する `Image` クラスや、ラスター化および PDF 出力に必要なオプションにアクセスできます。

### 手順 1: ソースおよび出力ディレクトリの設定

```csharp
string SourceDir = "Your Document Directory";
string OutputDir = "Your Document Directory";
```

`"Your Document Directory"` を、DWFX ファイルが存在するパスおよび PDF を保存したいパスに置き換えてください。

### 手順 2: DWFX ファイルの読み込み

```csharp
using (Image cadDrawing = Image.Load(SourceDir + "Tyrannosaurus.dwfx"))
```

`Image.Load` は DWFX ファイルを Aspose.CAD が扱える `Image` オブジェクトに読み込みます。`"Tyrannosaurus.dwfx"` をご自身の図面名に変更してください。

### 手順 3: ラスター化オプションの設定

```csharp
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = cadDrawing.Size.Width;
rasterizationOptions.PageHeight = cadDrawing.Size.Height;
```

ラスター化オプションは、生成されるページのサイズを Aspose.CAD に指示します。元の図面サイズを使用することで、正確なスケールが保たれます。

### 手順 4: PDF として保存 (c# convert CAD to PDF)

```csharp
PdfOptions CADf = new PdfOptions();
CADf.VectorRasterizationOptions = rasterizationOptions;
cadDrawing.Save(OutputDir + "OpenDwfxFile_out.pdf", CADf);
```

ここでは、ラスター化設定を `PdfOptions` オブジェクトに付与し、`Save` を呼び出すことで**c# convert CAD to PDF**を実行します。出力ファイルは指定したフォルダーに保存されます。

### 手順 5: 成功メッセージの表示

```csharp
Console.WriteLine("OpenDwfxFile executed successfully");
```

シンプルなコンソールメッセージで、変換がエラーなく完了したことがわかります。

## よくある問題とヒント

* **ファイルが見つかりません** – `SourceDir` のパスを再確認し、ファイル名が大文字小文字を含めて正確に一致しているか確認してください。  
* **空白の PDF** – DWFX ファイルに実際にベクターデータが含まれているか確認してください。エクスポートツールによっては空の図面が生成されることがあります。  
* **パフォーマンス** – 非常に大きな図面の場合、`PageWidth`/`PageHeight` を縮小するか、`CadRasterizationOptions` の `Resolution` を低く設定することを検討してください。

## よくある質問

### Q1: Aspose.CAD for .NET はすべての DWFX ファイルと互換性がありますか？

A1: Aspose.CAD for .NET は DWFX を含む幅広い CAD フォーマットをサポートしています。ただし、特定の互換性についてはドキュメントで確認することをお勧めします。

### Q2: Aspose.CAD for .NET のドキュメントはどこで見つけられますか？

A2: ドキュメントは[here](https://reference.aspose.com/cad/net/)で入手できます。

### Q3: 購入前に Aspose.CAD for .NET を試すことはできますか？

A3: はい、無料トライアル版は[here](https://releases.aspose.com/)からダウンロードできます。

### Q4: Aspose.CAD for .NET の一時ライセンスはどう取得しますか？

A4: 一時ライセンスは[here](https://purchase.aspose.com/temporary-license/)で取得できます。

### Q5: サポートが必要、または質問がありますか？

A5: サポートは[Aspose.CAD フォーラム](https://forum.aspose.com/c/cad/19)をご利用ください。

### Q6: 複数の DWFX ファイルをバッチ処理できますか？

A6: もちろん可能です。ディレクトリ内のファイルを `foreach` ループで反復し、読み込みと保存のロジックをラップしてください。

### Q7: 変換はレイヤーと色を保持しますか？

A7: ソースの DWFX にレイヤーや色の情報が含まれている場合、ベクタ情報は PDF に保持されます。

---

**最終更新日:** 2026-04-09  
**テスト環境:** Aspose.CAD for .NET 24.11  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}