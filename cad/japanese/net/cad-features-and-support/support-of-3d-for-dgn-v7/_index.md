---
date: 2026-03-29
description: Aspose.CAD for .NET を使用して、CAD のラスター化オプションを設定し、3D 対応の DGN を PDF にエクスポートする方法を学びましょう。
linktitle: Support of 3D for DGN V7
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: DGN V7 3D の CAD ラスタライズオプションを設定する
url: /ja/net/cad-features-and-support/support-of-3d-for-dgn-v7/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DGN V7 3D の CAD ラスタライズ オプションの構成

## はじめに

この包括的なチュートリアルでは、Aspose.CAD for .NET を使用して 3‑D DGN V7 ファイルを PDF にエクスポートするための **CAD ラスタライズ オプションの構成方法** を学びます。CAD ビューア、レポートツール、または自動変換パイプラインを構築している場合でも、これらの設定をマスターすることで、ページサイズ、レイアウトのスケーリング、背景色、そしてレンダリングしたい特定のビューを正確に制御できます。手順をステップバイステップで見ていきましょう。

## クイック回答
- **「CAD ラスタライズ オプションの構成」とは何ですか？**  
  CAD ファイルをラスタ形式（例: PDF）に変換する前に、ページ寸法、スケーリング、背景色、レイアウト選択などのプロパティを設定することを指します。
- **3‑D 対応で DGN を PDF にエクスポートする方法は？**  
  `DgnImage` で DGN をロードし、`PdfOptions` と `CadRasterizationOptions` を定義してから `Save` を呼び出します。
- **本番環境で使用するにはライセンスが必要ですか？**  
  はい、デプロイには商用ライセンスが必要です。無料トライアルも利用可能です。
- **サポートされている .NET バージョンはどれですか？**  
  .NET Framework 4.5 以上、.NET Core 3.1 以上、.NET 5/6/7 がサポートされています。
- **エクスポートする特定のビューを選択できますか？**  
  もちろんです。ラスタライズ オプションの `Layouts` 配列を設定します。

## 「CAD ラスタライズ オプションの構成」とは何ですか？

CAD ラスタライズ オプションの構成とは、CAD 図面がラスタライズ（ベクタからビットマップまたは PDF に変換）される方法をカスタマイズすることです。これらの設定を調整することで、生成されるドキュメントの視覚的出力、パフォーマンス、ファイルサイズを制御できます。

## 3‑D DGN V7 エクスポートに Aspose.CAD を使用する理由

- **完全な .NET 統合** – COM やネイティブ DLL は不要です。  
- **3‑D ジオメトリをサポート** – PDF へのレンダリング時に奥行き情報を保持します。  
- **細かな制御** – 正確なレイアウト、スケーリング、背景色を選択できます。  
- **クロスプラットフォーム** – .NET Core で Windows、Linux、macOS 上で動作します。

## 前提条件

開始する前に、以下をご用意ください。

- **Aspose.CAD for .NET** – こちらからダウンロードしてください。[here](https://releases.aspose.com/cad/net/)  
- **Visual Studio** または互換性のある .NET IDE。  
- **サンプル DGN ファイル** – 本ガイドでは `Nikon_D90_Camera.dgn` を使用します（Aspose のサンプルパックに含まれています）。

すべての準備が整ったので、コードに入りましょう。

## 名前空間のインポート

.NET プロジェクトで、必要な名前空間をインポートします:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.ImageOptions;
```

## ステップ 1: ドキュメント ディレクトリの設定

ソース DGN と出力ファイルが格納されるフォルダーを指す変数を作成します。

```csharp
string MyDir = "Your Document Directory";
```

## ステップ 2: DGN ファイルの読み込み

DGN ファイルを `DgnImage` としてロードします。このオブジェクトにより、CAD データとラスタライズ パイプラインにアクセスできます。

```csharp
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";
string outFile = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Your code for further processing goes here
}
```

## ステップ 3: PDF エクスポート オプションの構成（CAD ラスタライズ オプションの構成）

ここで **CAD ラスタライズ オプションの構成** を行い、3‑D モデルが PDF にレンダリングされる方法を決定します。ページサイズを調整し、自動レイアウトスケーリングを有効にし、背景色を設定し、エクスポートしたい正確なレイアウト（ビュー）を選択できます。

```csharp
var options = new PdfOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500,
        PageHeight = 1500,
        AutomaticLayoutsScaling = true,
        BackgroundColor = Color.Black,
        Layouts = new string[] { "1", "2", "3", "9" } // Only export specified views
    }
};
```

## ステップ 4: ラスター画像の保存

最後に、先ほど構成したオプションを使用して DGN を PDF ファイルにエクスポートします。

```csharp
dgnImage.Save(outFile, options);
```

## 一般的な問題と解決策

| 問題 | 解決策 |
|-------|----------|
| **PDF が空白になる** | `Layouts` 配列に DGN ファイルに存在する正しいビュー識別子が含まれていることを確認してください。 |
| **色が正しくない** | `BackgroundColor` が目的の値に設定されていることを確認してください。明るい背景には `Color.White` を使用します。 |
| **大きなファイルでのパフォーマンスボトルネック** | `AutomaticLayoutsScaling` を有効にし、より小さいラスタ解像度のために `PageWidth/PageHeight` を減らすことを検討してください。 |
| **ライセンス例外** | 画像をロードする前に有効な Aspose.CAD ライセンスをインストールし、トライアルの透かしを回避してください。 |

## よくある質問

**Q: Aspose.CAD for .NET を他の CAD ファイル形式でも使用できますか？**  
A: はい、Aspose.CAD は DWG、DXF、DWF、DGN など多数の形式をサポートしています。

**Q: Aspose.CAD を使用する際の例外はどのように処理すればよいですか？**  
A: `try‑catch` ブロックでコードを囲み、詳細なエラー情報は `Aspose.CAD.CADException` を確認してください。

**Q: Aspose.CAD は商用プロジェクトに適していますか？**  
A: もちろんです。ライセンスは [here](https://purchase.aspose.com/buy) から購入できます。

**Q: 購入前に Aspose.CAD for .NET を試すことはできますか？**  
A: はい、無料トライアルは [here](https://releases.aspose.com/) で利用可能です。

**Q: Aspose.CAD のコミュニティサポートはどこで得られますか？**  
A: ディスカッションフォーラムは [here](https://forum.aspose.com/c/cad/19) に参加してください。

---

**最終更新日:** 2026-03-29  
**テスト環境:** Aspose.CAD 24.11 for .NET  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}