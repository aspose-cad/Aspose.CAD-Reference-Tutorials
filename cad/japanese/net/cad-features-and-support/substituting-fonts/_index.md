---
date: 2026-03-29
description: Aspose.CAD for .NET でフォントをすばやく置き換える方法を学びましょう。このステップバイステップガイドでは、プライマリフォント名の設定方法と
  CAD 図面の効率的なカスタマイズ方法を示します。
linktitle: Substituting Fonts
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: .NET 用 Aspose.CAD でフォントを置き換える方法
url: /ja/net/cad-features-and-support/substituting-fonts/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for .NET のフォント置換方法

## はじめに

.NET を使用した CAD 開発の領域では、**フォントの置換方法**を学ぶことは、図面の視覚品質を劇的に向上させる重要なスキルです。Aspose.CAD for .NET は、任意のスタイルに対して **PrimaryFontName を設定**できるシンプルな API を提供し、グローバルまたは選択的なフォント置換を簡単に行えます。このチュートリアルでは、図面の読み込みからフォントの全体置換または特定のスタイル名による置換まで、プロセス全体を順に解説します。

## クイック回答
- **CAD 操作のメインクラスは何ですか？** `Aspose.CAD.Image`（または派生クラスの `CadImage`）。
- **フォントを変更するプロパティはどれですか？** `CadStyleTableObject` の `PrimaryFontName`。
- **すべてのスタイルのフォントを一度に置換できますか？** はい、`cadImage.Styles` を反復し、プロパティを設定します。
- **本番環境でライセンスが必要ですか？** トライアル以外の使用には有効な Aspose.CAD ライセンスが必要です。
- **サポートされている .NET バージョンは？** .NET Framework 4.5 以上、.NET Core 3.1 以上、.NET 5/6/7。

## CAD におけるフォント置換とは？
フォント置換とは、CAD 図面で使用されている元の書体を、対象システムで利用可能な別の書体に置き換えることを指します。元のフォントが存在しない場合や、統一された企業スタイルが必要な場合、または限られたフォントしかサポートしないデバイスで印刷するための図面を準備する際に特に有用です。

## Aspose.CAD でフォントを置換する理由
- **外部依存なし** – ライブラリが内部でフォントマッピングを処理します。
- **多数のフォーマットに対応** – DXF、DWG、DGN など。
- **プログラム制御** – バッチ変換や CI パイプライン向けにプロセスを自動化できます。
- **図形ジオメトリを保持** – テキストの視覚表現のみが変更されます。

## 前提条件

- .NET プログラミングの基本知識。
- Aspose.CAD for .NET がインストール済みであること。まだインストールしていない場合は、[こちら](https://releases.aspose.com/cad/net/)からダウンロードしてください。
- 実験用の CAD 図面ファイル（DXF、DWG など）。

## 名前空間のインポート

開始する前に、.NET アプリケーションで Aspose.CAD の機能にアクセスするために必要な名前空間をインポートしてください。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad.CadTables;
```

## 手順 1: CAD 図面の読み込み

`CadImage` のインスタンスに CAD 図面を読み込むことから始めます。ドキュメントディレクトリへの正しいパスを指定してください。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (CadImage cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code for further actions goes here
}
```

## 手順 2: スタイルの反復処理

次に、`foreach` ループを使用して CAD 図面内のスタイルを反復処理します。これにより、個々のフォントスタイルにアクセスし操作できます。

```csharp
foreach (CadStyleTableObject style in cadImage.Styles)
{
    // Your code for style manipulation goes here
}
```

## フォント置換のための PrimaryFontName の設定方法

各 `CadStyleTableObject` の `PrimaryFontName` プロパティは、図面がレンダリングされる際に使用されるフォントを制御します。このプロパティを設定することで、実質的に元のフォントを置換できます。

### 手順 3: フォントを全体的に置換

**すべて** のスタイルのフォントを置換するには、各スタイルの `PrimaryFontName` プロパティを目的のフォント名（例: `"Arial"`）に設定します。

```csharp
foreach (CadStyleTableObject style in cadImage.Styles)
{
    style.PrimaryFontName = "Arial";
}
```

### 手順 4: スタイル名でフォントを置換

特定のスタイル（例: `"Roman"` という名前のスタイル）のみフォントを置換したい場合は、ループ内に条件チェックを追加します。

```csharp
foreach (CadStyleTableObject style in cadImage.Styles)
{
    if (style.StyleName == "Roman")
    {
        style.PrimaryFontName = "Arial";
    }
}
```

## よくある問題とトラブルシューティング

| 問題 | 原因 | 対策 |
|-------|-------|-----|
| コード実行後にフォントが変更されない | 図面がキャッシュされている、または読み取り専用モードで開かれている | `cadImage.Save(...)` で変更後に画像を保存するか、ファイルを再読み込みして確認してください。 |
| 目的のフォントがシステムに見つからない | コードを実行しているマシンにフォントがインストールされていない | 必要な TrueType/OpenType フォントをインストールするか、アプリケーションリソースに埋め込んでください。 |
| テキストが文字化けする | エンコーディングが正しくない、または Unicode サポートが不足している | 必要な文字セットをサポートするフォント（例: Arial Unicode MS）を使用してください。 |

## よくある質問

**Q: Aspose.CAD for .NET でフォント変更を元に戻すことはできますか？**  
A: はい、元の CAD 図面を再読み込みするか、変更前にバックアップコピーを保持しておくことで元に戻せます。

**Q: 他に変更できるフォントプロパティはありますか？**  
A: もちろんです。`PrimaryFontName` に加えて、`SecondaryFontName`、`FontFamily`、その他のスタイル関連属性を使用して高度なカスタマイズが可能です。

**Q: Aspose.CAD はさまざまな CAD フォーマットに対応していますか？**  
A: はい、Aspose.CAD は DXF、DWG、DGN、DWF など多数のフォーマットをサポートしており、プロジェクト間の柔軟性を提供します。

**Q: バッチ処理でフォント置換を自動化できますか？**  
A: もちろんです。フォント置換ロジックをフォルダ内の CAD ファイルを反復するループでラップするか、CI/CD パイプラインに組み込んでください。

**Q: Aspose.CAD for .NET の追加サポートはどこで得られますか？**  
A: 追加のサポートやコミュニティディスカッションについては、[Aspose.CAD フォーラム](https://forum.aspose.com/c/cad/19)をご覧ください。

**最終更新日:** 2026-03-29  
**テスト環境:** Aspose.CAD for .NET（最新リリース）  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}