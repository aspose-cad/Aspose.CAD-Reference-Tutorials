---
date: 2026-03-19
description: .NET と Aspose.CAD を使用して CAD 図面のサイズ変更方法を学び、CAD 図面の単位をスケーリングしレイアウトサイズを調整する方法も含めます。ステップバイステップのガイドに従ってください。
linktitle: Adjusting CAD Drawing Size
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: .NET 用 Aspose.CAD で CAD 図面のサイズを変更する方法
url: /ja/net/cad-drawing-manipulation/adjust-cad-drawing-size/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for .NET を使用した CAD 図面のサイズ変更方法

## はじめに

.NET アプリケーションから直接 **CAD のサイズ変更方法** が必要な場合、ここが適切な場所です。このチュートリアルでは、Aspose.CAD for .NET を使用して CAD の単位設定を変更し、図面の寸法をスケーリングし、プログラムで CAD のサイズを調整する方法を示します。ガイドの最後までに、サポートされている任意の CAD フォーマットのサイズ変更に対応した、実用的で本番環境向けのソリューションが手に入ります。

## クイック回答
- **必要なライブラリは何ですか？** Aspose.CAD for .NET  
- **単位タイプを変更できますか？** はい – `CadRasterizationOptions` の `UnitType` を設定します  
- **本番環境でライセンスが必要ですか？** トライアル以外の使用には有効な Aspose.CAD ライセンスが必要です  
- **サンプルはどの画像形式にエクスポートしますか？** BMP（ただし、サポートされている任意のラスタ形式が使用可能です）  
- **コード行数は？** 完全なサイズ変更操作で 30 行未満です  

## 実際の「CAD のサイズ変更」とは？

CAD 図面のサイズ変更とは、ベクターデータを特定のスケールまたは単位（例: センチメートル、インチ）でラスタ画像に変換することを指します。レポートに図面を埋め込んだり、サムネイルを生成したり、Web ページに CAD ビジュアルを統合したりする場合に便利です。

## なぜ Aspose.CAD で CAD のサイズを調整するのか？

- **外部 CAD ソフトウェア不要** – すべて .NET コード内で実行されます。  
- **単位、レイアウト、ラスタライズオプション** を細かく制御できます。  
- **クロスフォーマット対応** – 同じコードで DWG、DXF、DWF などに対応します。  

## 前提条件

開始する前に、以下が揃っていることを確認してください。

- Aspose.CAD for .NET ライブラリ: [Aspose.CAD for .NET ダウンロードページ](https://releases.aspose.com/cad/net/) からライブラリをダウンロードしてインストールしてください。  
- サンプル CAD 図面: `sample.dwg` のようなファイルをプロジェクトのドキュメントディレクトリに配置します。  

## 名前空間のインポート

まず、Aspose.CAD のクラスにアクセスできる名前空間をインポートします。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## 手順 1: CAD 図面の読み込み

`Image` オブジェクトにソースファイルを読み込みます。このオブジェクトはメモリ内の CAD 図面を表し、以降のすべての操作の基礎となります。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "sample.dwg";

// Load a CAD drawing in an instance of Image
using (var image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code here...
}
```

## 手順 2: BmpOptions の作成（または他のラスタ形式）

`BmpOptions` は、ビットマップとして保存する際にベクターデータをどのようにレンダリングするかを Aspose.CAD に指示します。対象の形式に応じて `PngOptions`、`JpegOptions` などに置き換えることができます。

```csharp
Aspose.CAD.ImageOptions.BmpOptions bmpOptions = new Aspose.CAD.ImageOptions.BmpOptions();
```

## 手順 3: CadRasterizationOptions の設定

`CadRasterizationOptions` は、スケーリング、単位変換、レイアウト選択のコア設定を保持します。これを `BmpOptions` の `VectorRasterizationOptions` プロパティにリンクすることで、ラスタライザがカスタム設定を使用するようになります。

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions cadRasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = cadRasterizationOptions;
```

## 手順 4: UnitType の設定（CAD の単位変更）

ここでは、CAD の単位をデフォルトからセンチメートルに変更します。**change cad unit** キーワードがここにあり、最終的な画像サイズに直接影響します。

```csharp
cadRasterizationOptions.UnitType = Aspose.CAD.ImageOptions.UnitType.Centimeter;
```

## 手順 5: レイアウトの選択（CAD レイアウトの設定）

図面に複数のレイアウト（例: Model、Sheet1）が含まれている場合、ラスタライズしたいレイアウトを指定します。リサイズされた出力のために **set cad layouts** を行う際、正しいレイアウトの選択は不可欠です。

```csharp
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## 手順 6: BMP へエクスポート（CAD 図面のリサイズ）

最後に、ラスタライズされた画像を保存します。出力ファイルは、設定した新しいサイズ、単位、レイアウトを反映し、実質的に **resize CAD drawing** 操作が完了します。

```csharp
string outPath = sourceFilePath + ".bmp";
image.Save(outPath, bmpOptions);
```

これで、リサイズされた CAD 図面を表す BMP ファイルが作成され、さらに処理したり表示したりする準備が整いました。

## よくある問題と解決策

| 問題 | 発生原因 | 対策 |
|------|----------|------|
| 出力がぼやける | デフォルトの DPI（ドット毎インチ）が低いため | 保存前に `cadRasterizationOptions.Resolution = 300;` を設定してください |
| 間違ったレイアウトが表示される | レイアウト名のタイプミス | CAD ビューアまたは `Layouts` コレクションで正確なレイアウト名を確認してください |
| 単位変換がずれている | メートル法とインチ法が混在している | `UnitType` が目的の測定システムと一致していることを確認してください |

## FAQ

### Q1: Aspose.CAD for .NET はすべての CAD フォーマットに対応していますか？

A1: Aspose.CAD for .NET は DWG、DXF、DWF などを含む幅広い CAD フォーマットに対応しています。完全な一覧は [documentation](https://reference.aspose.com/cad/net/) をご確認ください。

### Q2: 複数のレイアウトを同時にリサイズできますか？

A2: はい、`CadRasterizationOptions` の `Layouts` 配列を調整することで、複数のレイアウトを同時にリサイズできます。

### Q3: Aspose.CAD for .NET のサポートはどこで受けられますか？

A3: コミュニティサポートと支援は [Aspose.CAD フォーラム](https://forum.aspose.com/c/cad/19) をご利用ください。

### Q4: 無料トライアルはありますか？

A4: はい、[無料トライアル](https://releases.aspose.com/) で Aspose.CAD for .NET の機能を評価できます。

### Q5: Aspose.CAD for .NET の一時ライセンスはどこで取得できますか？

A5: テスト目的の一時ライセンスは [こちら](https://purchase.aspose.com/temporary-license/) から取得してください。

## よくある質問

**Q: 単位タイプを変更せずに CAD 図面をスケールするには？**  
A: `CadRasterizationOptions` の `Zoom` プロパティを調整します（例: `cadRasterizationOptions.Zoom = 2.0;`）ことで、元の単位を保ったままサイズを2倍にできます。

**Q: BMP 以外の形式にエクスポートできますか？**  
A: もちろんです。`BmpOptions` を `PngOptions`、`JpegOptions`、または他のサポートされているラスタ形式クラスに置き換えてください。

**Q: フォルダー内の図面をバッチ処理できますか？**  
A: はい。ディレクトリ内のファイルをループし、同じラスタライズロジックを適用して、各出力を固有の名前で保存します。

---

**最終更新日:** 2026-03-19  
**テスト環境:** Aspose.CAD for .NET 24.11（執筆時点での最新）  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}