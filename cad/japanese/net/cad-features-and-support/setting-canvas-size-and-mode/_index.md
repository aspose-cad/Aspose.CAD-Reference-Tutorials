---
date: 2026-03-29
description: このステップバイステップガイドで、Aspose.CAD for .NET を使用して CAD から PDF を作成し、キャンバスサイズを設定し、CAD
  を PDF または TIFF にエクスポートする方法を学びましょう。
linktitle: Setting Canvas Size and Mode
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: CADからPDFを作成する方法：Aspose.CAD for .NETでキャンバスサイズとモードを設定する
url: /ja/net/cad-features-and-support/setting-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for .NET におけるキャンバスサイズとモードの設定

## はじめに

出力サイズを制御しながら **CAD から PDF を作成** する準備はできていますか？このチュートリアルでは、キャンバスサイズとモードの設定、CAD ファイルの読み込み、そして Aspose.CAD for .NET を使用して PDF または TIFF にエクスポートする手順を解説します。**DXF を PDF に変換** が必要な場合や、高解像度の図面を生成したい場合、あるいは単にラスタライズ領域を調整したい場合でも、以下の手順で実用的な本番環境向けソリューションが得られます。

## クイック回答
- **“CAD から PDF を作成” が意味することは何ですか？** CAD 図面（例: DXF、DWG）をベクターとラスタの詳細を保持した PDF ドキュメントに変換することです。  
- **出力サイズを制御するオプションはどれですか？** `CadRasterizationOptions.PageWidth` と `PageHeight`（キャンバスサイズ）。  
- **TIFF へもエクスポートできますか？** はい – 同じラスタライズ設定で `TiffOptions` を使用します。  
- **本番環境でライセンスが必要ですか？** 商用ライセンスが必要です。無料トライアルも利用可能です。  
- **サポートされている .NET バージョンは？** .NET Framework 4.5 以上、.NET Core 3.1 以上、.NET 5/6/7。

## 「CAD から PDF を作成する」とは何ですか？

CAD から PDF を作成するとは、CAD 図面をページ指向のフォーマット（PDF）にレンダリングし、CAD ソフトウェアがなくても閲覧、印刷、共有できるようにすることです。Aspose.CAD が重い処理を担当し、キャンバスサイズ、スケーリング、出力フォーマットを定義できます。

## CAD から PDF を作成する際にキャンバスサイズを設定する理由

キャンバスサイズを設定すると、生成される PDF や TIFF の解像度と寸法を正確にコントロールできます。特に以下の場合に有用です：
- 特定の用紙サイズで印刷するための図面の準備。  
- ウェブプレビュー用のサムネイルや高解像度画像の生成。  
- 複数のドキュメント間でレイアウトを一貫させること。

## 前提条件

- Aspose.CAD ライブラリ: [Aspose.CAD website](https://releases.aspose.com/cad/net/) から Aspose.CAD ライブラリをダウンロードしてインストールします。  
- 開発環境: マシンに .NET 開発環境が設定されていることを確認してください。  
- サンプル CAD ファイル: 本チュートリアルではサンプル DXF ファイルを使用します。[Aspose.CAD documentation](https://reference.aspose.com/cad/net/) にあります。

## 名前空間のインポート

First, import the namespaces required for CAD processing:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## カスタムキャンバスサイズで CAD から PDF を作成する方法

### ステップ 1: CAD ファイルの読み込み

まず、**CAD ファイルの読み込み**（例: DXF）を `Image` オブジェクトに行います。ここで CAD ファイルをメモリに **ロード** します。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    // Your code for further steps will go here
}
```

### ステップ 2: CadRasterizationOptions の作成

`CadRasterizationOptions` インスタンスを作成し、キャンバスサイズを定義します。`PageWidth` と `PageHeight` プロパティで、必要な正確な寸法に **キャンバスサイズを設定** できます。

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
rasterizationOptions.NoScaling = false;
```

### ステップ 3: PdfOptions の作成 (CAD を PDF にエクスポート)

ラスタライズ設定を `PdfOptions` オブジェクトにリンクします。この構成により、定義したカスタムキャンバスで **CAD を PDF にエクスポート** できます。

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### ステップ 4: PDF へエクスポート (DXF を PDF に変換)

画像を PDF として保存します。この手順で、設定したオプションを使用して **CAD から PDF を作成** します。

```csharp
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

### ステップ 5: TiffOptions の作成 (CAD を TIFF にエクスポート)

ラスタ画像も必要な場合は、`TiffOptions` を設定します。同じラスタライズオプションが再利用されるため、**CAD を TIFF にエクスポート** する際もキャンバスサイズが反映されます。

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;
```

### ステップ 6: TIFF へエクスポート

最後に、図面を TIFF ファイルとして保存します。

```csharp
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## 一般的な問題と解決策

- **キャンバスが切り取られている** – `AutomaticLayoutsScaling` が `true`、`NoScaling` が `false` に設定されていることを確認し、図面がキャンバスに合わせてスケーリングされるようにします。  
- **低解像度の PDF** – `PageWidth`/`PageHeight` を増やすか、`CadRasterizationOptions` の `Resolution` を設定します。  
- **ファイルが見つからないエラー** – `MyDir` が有効なディレクトリを指していること、DXF ファイル名が正確に一致していることを確認してください。

## よくある質問

### Q1: Aspose.CAD を他の .NET ライブラリと併用できますか？

A1: はい、Aspose.CAD は他の .NET ライブラリとシームレスに統合でき、CAD 操作の機能を拡張します。

### Q2: Aspose.CAD の無料トライアルは利用できますか？

A2: はい、Aspose.CAD の機能を無料トライアルで試すことができます。開始するには [here](https://releases.aspose.com/) をご覧ください。

### Q3: Aspose.CAD のサポートはどこで受けられますか？

A3: サポートやディスカッションは [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) で行えます。

### Q4: Aspose.CAD の包括的なドキュメントはどこで見つけられますか？

A4: 詳細情報やサンプルは [Aspose.CAD documentation](https://reference.aspose.com/cad/net/) を参照してください。

### Q5: Aspose.CAD for .NET を購入するには？

A5: Aspose.CAD を購入するには、[purchase page](https://purchase.aspose.com/buy) にアクセスしてください。

**追加の Q&A**

**Q: 複数ページの CAD 図面を単一の PDF にエクスポートできますか？**  
**A: はい。`CadRasterizationOptions` の `PageCount` を設定すれば、ライブラリがページを結合して 1 つの PDF にします。**

**Q: キャンバスサイズはベクターデータの品質に影響しますか？**  
**A: ベクターデータは解像度に依存しません。キャンバスサイズはラスタ化された要素と画像解像度にのみ影響します。**

---

**最終更新日:** 2026-03-29  
**テスト環境:** Aspose.CAD 24.11 for .NET  
**作成者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}