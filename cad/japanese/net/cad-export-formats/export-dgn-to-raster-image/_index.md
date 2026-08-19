---
date: 2026-03-24
description: Aspose.CAD for .NET を使用して dgn を png に変換し、cad を jpeg として保存する方法を学ぶ – CAD
  から画像への変換クイックガイド。
linktitle: Export DGN to Raster Image
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: .NET 用 Aspose.CAD で DGN を PNG に変換する方法
url: /ja/net/cad-export-formats/export-dgn-to-raster-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for .NETでDGNをPNGに変換する

モダンな .NET 開発において、**convert dgn to png** は、Web 上で CAD 図面を表示したりレポートに埋め込んだりする際に頻繁に求められる要件です。Aspose.CAD for .NET を使用すれば、この変換は非常にシンプルになり、数行のコードだけで DGN ファイルを高品質なラスタ画像に変換できます。このガイドでは、プロジェクトのセットアップから最終的な PNG（または JPEG）ファイルの保存まで、全工程を順を追って解説します。

## クイック回答
- **Aspose.CAD で DGN を PNG に変換できますか？** はい – ラスタライズオプションを設定し、PNG または JPEG の出力を選択するだけです。  
- **本番環境でライセンスは必要ですか？** トライアル以外のデプロイには有効な Aspose.CAD ライセンスが必要です。  
- **対応している .NET バージョンは？** .NET Framework 4.6 以降、.NET Core 3.1 以降、.NET 5/6/7。  
- **利用可能な画像形式は？** PNG、JPEG、BMP、GIF、TIFF など多数。  
- **例外処理は必須ですか？** 必ず – ファイルアクセスの問題を処理するために try/catch でラップしてください。

## “convert dgn to png”とは？
DGN（MicroStation）ファイルを PNG に変換することは、ベクタ CAD データをピクセルベースの画像にラスタライズすることを意味します。プレビュー生成や HTML メールへの図面埋め込み、ドキュメント管理システムのサムネイル作成などに便利です。

## CADから画像への変換にAspose.CADを使用する理由
- **外部依存なし** – 完全にマネージドコードで動作します。  
- **高忠実度** – 線幅、レイヤー、カラーを正確に保持します。  
- **柔軟な出力** – PNG、JPEG、BMP などをオプション一つで切り替え可能。  
- **パフォーマンス最適化** – 大規模な図面でも高速にラスタライズできます。

## 前提条件

開始する前に、以下を確認してください。

- **Aspose.CAD for .NET** がプロジェクトにインストールされていること。ダウンロードは[website](https://reference.aspose.com/cad/net/)から。  
- サンプル DGN ファイル（例: `Nikon_D90_Camera.dgn`）を既知のディレクトリに配置しておくこと。

## 名前空間のインポート

まず、Aspose.CAD クラスにアクセスできるように必要な `using` 文を追加します。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## 手順 1: DGN ファイルの読み込み

ソース DGN を `CadImage` オブジェクトにロードします。このオブジェクトはメモリ上の CAD 図面を表し、ラスタライズの元になります。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for further processing goes here
}
```

## 手順 2: ラスタライズオプションの定義

CAD 図面のラスタライズ方法を設定します。ここで画像サイズ、スケーリング、背景色などを制御できます。

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## 手順 3: 出力形式の選択 (PNG または JPEG)

チュートリアルは PNG に焦点を当てていますが、**save cad as jpeg** も可能です。適切な画像オプションオブジェクトを作成し、先ほどのラスタライズ設定を添付します。

```csharp
ImageOptionsBase options = new JpegOptions();   // Change to PngOptions() for PNG output
options.VectorRasterizationOptions = rasterizationOptions;
```

> **プロのコツ:** PNG ファイルを生成するには `new JpegOptions()` を `new PngOptions()` に置き換えてください。

## 手順 4: ラスタ画像の保存

最後に、`CadImage` インスタンスの `Save` メソッドを呼び出し、ファイル名と設定したオプションオブジェクトを渡します。

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpg", options);
```

`PngOptions` に切り替えた場合、ファイルは `ExportDGNToRasterImage_out.png` として保存されます。

## よくある問題と解決策

| 問題 | 原因 | 対策 |
|------|------|------|
| **空白の出力画像** | `NoScaling` が正しく設定されていない、またはレイアウトが選択されていない | `AutomaticLayoutsScaling = true` を設定するか、目的のレイアウトを指定してください。 |
| **大きなファイルでメモリ不足** | ストリーミングなしで巨大な DGN をロードしている | `Image.Load(sourceFilePath, new LoadOptions { LoadOnDemand = true })` を使用してください。 |
| **サポートされていない DGN バージョン** | 古い MicroStation バージョン | レガシーフォーマットをサポートする最新の Aspose.CAD バージョンを使用してください。 |

## よくある質問

**Q: DGN ファイルを JPEG 以外の形式にエクスポートできますか？**  
A: はい、Aspose.CAD for .NET は PNG、BMP、GIF、TIFF など多数の形式に対応しています。オプションクラス（例: `new PngOptions()`）を差し替えるだけです。

**Q: 変換中の例外はどのように処理すべきですか？**  
A: 変換コードを `try/catch` ブロックで囲み、詳細なエラー情報は `Aspose.CAD.CadException` をログに記録してください。

**Q: Aspose.CAD for .NET のトライアル版はありますか？**  
A: はい、無料トライアルで製品を試すことができます。詳細は[here](https://releases.aspose.com/)をご覧ください。

**Q: Aspose.CAD for .NET に関する支援や議論はどこでできますか？**  
A: コミュニティサポートやディスカッションは[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)で行われています。

**Q: Aspose.CAD for .NET の一時ライセンスはどう取得できますか？**  
A: 開発用の一時ライセンスは[このリンク](https://purchase.aspose.com/temporary-license/)から取得できます。

## 結論

これで **convert dgn to png**（または JPEG）を Aspose.CAD for .NET で実行する方法が理解できました。ラスタライズオプションと画像オプションクラスを調整するだけで、あらゆるプロジェクト要件に合わせた出力が可能です。ページサイズ、DPI 設定、ファイル形式などを自由に試して、最適なラスタ画像を作成してください。

---

**最終更新日:** 2026-03-24  
**テスト環境:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}