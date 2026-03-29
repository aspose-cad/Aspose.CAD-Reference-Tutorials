---
date: 2026-03-29
description: Aspose.CAD for .NET を使用して DGN を JPEG に変換する方法を学び、DGN V7 を完全にサポートし、CAD
  をラスタ画像に簡単に変換できるようにします。
linktitle: Support for DGN V7
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Aspose.CAD for .NET を使用して DGN を JPEG に変換 – V7 対応
url: /ja/net/cad-features-and-support/support-for-dgn-v7/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for .NET を使用した DGN から JPEG への変換 – V7 対応

## はじめに

このチュートリアルでは、Aspose.CAD for .NET を使用して **convert DGN to JPEG** を行う方法を学びます。ライブラリの完全な DGN V7 サポートを活用できます。DGN ファイルを JPEG などのラスタ画像に変換することは、CAD 図面をウェブページ、モバイルアプリ、レポートツールに埋め込む必要がある場合に一般的な要件です。Aspose.CAD は **convert CAD to raster** 形式への変換も効率的に行えるため、設計データの提示方法に柔軟性を提供します。

## クイック回答

- **このチュートリアルの対象は何ですか？** Aspose.CAD for .NET を使用して DGN V7 ファイルを JPEG ラスタ画像に変換します。  
- **どのライブラリ バージョンが必要ですか？** DGN V7 サポートを含む最近の Aspose.CAD for .NET リリースであればどれでも構いません。  
- **ライセンスは必要ですか？** 開発用途には無料トライアルで動作しますが、本番環境では商用ライセンスが必要です。  
- **出力サイズを変更できますか？** はい – ラスタライズ オプションでページ幅、高さ、スケーリングを設定できます。  
- **JPEG だけが出力形式ですか？** いいえ – Aspose.CAD は多数のラスタ形式 (PNG、BMP、TIFF など) をサポートしています。

## DGN V7 とは？

DGN（Design）は、Bentley Systems が MicroStation 用に最初に作成したファイル形式です。バージョン 7 は、より豊富なジオメトリとメタデータを追加し、土木工学やインフラプロジェクトで人気の選択肢となっています。Aspose.CAD for .NET は DGN V7 ファイルを直接読み取り、その内容を `CadImage` オブジェクトとして公開します。このオブジェクトをラスタライズしたり、他の形式に変換したりできます。

## なぜ DGN を JPEG に変換するのか？

- **Web‑ready:** JPEG 画像は軽量で、特別なプラグインなしにブラウザですぐに表示されます。  
- **Cross‑platform:** JPEG はあらゆるデバイスで閲覧でき、技術的でない関係者と CAD 図面を共有するのに最適です。  
- **Simplified workflows:** ラスタ形式に変換することで、下流プロセスで CAD 固有のビューアが不要になります。

## 前提条件

実装に入る前に、以下が揃っていることを確認してください。

- **Aspose.CAD for .NET** – [website](https://releases.aspose.com/cad/net/) からダウンロードしてください。  
- **Development environment** – Visual Studio（または .NET をサポートする任意の IDE）。  

これらが準備できていれば、手順を中断せずに進められます。

## 名前空間のインポート

まず、CadImage の処理とラスタライズに必要な名前空間をインポートします。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## 手順 1: DGN ファイルの読み込み

ソース DGN ファイルを `CadImage` オブジェクトにロードします。プレースホルダーのパスを、DGN ファイルが格納されているフォルダーに置き換えてください。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Subsequent steps will be placed here.
}
```

## 手順 2: ラスタライズ オプションの設定

DGN 図面のラスタライズ方法を定義します。出力サイズやスケーリングの挙動を制御できます。

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions
{
    PageWidth = 600,
    PageHeight = 300,
    NoScaling = true,
    AutomaticLayoutsScaling = false
};
```

## 手順 3: ベクトル ラスタライズ オプションの設定

`JpegOptions` オブジェクト（または他のラスタ形式オプション）を作成し、ラスタライズ設定を付与します。

```csharp
ImageOptionsBase options = new JpegOptions
{
    VectorRasterizationOptions = rasterizationOptions
};
```

## 手順 4: ラスタライズ画像の保存

最後に、`Save` メソッドを使用して DGN 図面を JPEG ファイルとしてエクスポートします。

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpeg", options);
```

コードが正常に実行されると、指定したフォルダーに元の DGN V7 図面の JPEG 表現が作成されます。

## よくある問題と解決策

| 問題 | 解決策 |
|-------|----------|
| **ファイルが見つかりません** | `MyDir` がパス区切り文字（`\\` または `/`）で終わっていること、ファイル名が正しいことを確認してください。 |
| **出力画像が空白** | `NoScaling` が適切に設定されていることを確認してください。ページ全体に図面を表示したい場合は `false` に設定します。 |
| **サポートされていないエンティティ** | Aspose.CAD はほとんどの DGN エンティティをサポートしていますが、非常に古いものやカスタムオブジェクトは無視される場合があります。警告は変換ログで確認してください。 |

## よくある質問

### Q1: Aspose.CAD は最新の DGN V7 仕様に対応していますか？

**A:** はい、Aspose.CAD は DGN V7 を完全にサポートしており、最新の標準に従ってジオメトリとメタデータの両方を処理します。

### Q2: DGN ファイル変換のラスタライズ オプションをカスタマイズできますか？

**A:** もちろんです。`CadRasterizationOptions` クラスを使用すると、ページサイズ、スケーリング、線幅、背景色などを調整できます。

### Q3: JPEG 以外にサポートされている出力形式はありますか？

**A:** はい、Aspose.CAD は PNG、BMP、TIFF などの他のラスタ形式にもエクスポートできます。対応する `*Options` クラス（例: `PngOptions`）を使用するだけです。

### Q4: Aspose.CAD に関する質問のサポートはどこで受けられますか？

**A:** コミュニティサポートや公式の回答は、[Aspose.CAD フォーラム](https://forum.aspose.com/c/cad/19)をご覧ください。

### Q5: Aspose.CAD for .NET の無料トライアルはありますか？

**A:** はい、[こちら](https://releases.aspose.com/)からトライアル版をダウンロードできます。

---

**最終更新日:** 2026-03-29  
**テスト環境:** Aspose.CAD 24.12 for .NET  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}