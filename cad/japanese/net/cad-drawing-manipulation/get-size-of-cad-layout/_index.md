---
date: 2026-03-21
description: .NET で Aspose.CAD を使用して CAD レイアウトサイズを取得する方法を学びましょう。効率的な CAD ファイル操作のためのステップバイステップガイドをご覧ください。
linktitle: Get Size of CAD Layout
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Aspose.CAD for .NETでCADレイアウトサイズを取得する
url: /ja/net/cad-drawing-manipulation/get-size-of-cad-layout/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for .NET で CAD レイアウトサイズを取得する

## はじめに

この包括的なチュートリアルでは、Aspose.CAD ライブラリ for .NET を使用して **CAD レイアウトサイズを取得する方法** を解説します。CAD ビューアの構築、サムネイルの生成、または下流処理のために正確なレイアウト寸法が必要な場合、各レイアウトの正確なサイズを把握することは不可欠です。図面の読み込みからレイアウト寸法の抽出、必要に応じて画像として保存するまでの全工程を順を追って説明しますので、自信を持ってご自身のアプリケーションに組み込むことができます。

## クイック回答
- **「CAD レイアウトサイズを取得する」とは何ですか？**  
  CAD ファイル内の空でないレイアウトそれぞれの幅と高さ（図面単位）を取得することを指します。  
- **どのライブラリが対応していますか？**  
  Aspose.CAD for .NET がシンプルな API でレイアウト情報にアクセスできます。  
- **ライセンスは必要ですか？**  
  評価用の無料トライアルで動作しますが、製品環境では商用ライセンスが必要です。  
- **対応フォーマットは？**  
  DWG、DXF をはじめとする多数の CAD/BIM フォーマットに完全対応しています。  
- **実装にかかる目安は？**  
  基本的なサイズ取得ルーチンで約 10〜15 分程度です。

## 「CAD レイアウトサイズを取得する」とは？
CAD レイアウトサイズを取得するとは、CAD 図面に定義された各レイアウト（ペーパー空間）の幾何的範囲を抽出することです。この範囲は図面のネイティブ単位（通常はミリメートルまたはインチ）で表され、スケーリング、印刷、プレビュー画像生成などのタスクに役立ちます。

## なぜ Aspose.CAD で CAD レイアウトサイズを取得するのか？
- **CAD ソフト不要** – 完全にサーバーサイドで動作します。  
- **クロスプラットフォーム** – .NET Framework、.NET Core、.NET 5/6+ で利用可能です。  
- **正確な測定** – ファイルに保存されている正確な範囲を返すため、手動での解析が不要です。  
- **簡単統合** – シンプルな API 呼び出しで既存の C# プロジェクトに自然に組み込めます。

## 前提条件

コードに入る前に、以下が準備できていることを確認してください。

- Aspose.CAD for .NET がインストール済みです。ダウンロードは [Aspose.CAD for .NET ダウンロードページ](https://releases.aspose.com/cad/net/) から行えます。  
- 解析対象の CAD ファイル（DWG、DXF など）を用意します。本ガイドではサンプルとして `conic_pyramid.dxf` と `Bottom_plate.dwg` を使用します。

## 名前空間のインポート

.NET プロジェクトで必要な名前空間をインポートします。

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

## 手順 1: ドキュメントディレクトリの設定

CAD ファイルが格納されているフォルダーを定義します。プレースホルダーは実際のパスに置き換えてください。

```csharp
string MyDir = "Your Document Directory";
```

## 手順 2: CAD ファイルパスの指定

処理対象の CAD ファイルを指す配列を作成します。

```csharp
string[] sourceFilePaths = new[]
{
    MyDir + "conic_pyramid.dxf",
    MyDir + "Bottom_plate.dwg"
};
```

## 手順 3: CAD ファイルの反復処理

各ファイルを読み込み、フォーマットを検出し、レイアウト情報の抽出準備を行います。

```csharp
foreach (var sourceFilePath in sourceFilePaths)
{
    string extension = Path.GetExtension(sourceFilePath);
    using (CadImage cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath))
    {
        // ... (continue to the next step)
    }
}
```

## 手順 4: 空でないレイアウトの取得

実際に描画エンティティを含むレイアウトだけを返すヘルパーメソッドが必要です。空のレイアウトはサイズ情報が無いため除外します。

```csharp
private static List<string> GetNotEmptyLayouts(Image cadImage, string extension)
{
    // ... (continue to the next step)
}
```

## 手順 5: DWG ファイル用レイアウト取得

DWG ファイルは `HeaderVariables` テーブルにレイアウト情報を保持しています。以下のメソッドは DWG 図面から空でないレイアウト名すべてを抽出します。

```csharp
private static List<string> GetNotEmptyLayoutsForDwg(CadImage cadImage)
{
    // ... (continue to the next step)
}
```

## 手順 6: DXF ファイル用レイアウト取得

DXF ファイルは構造が異なります。このメソッドは `Tables` コレクションを解析し、エンティティを含むペーパー空間レイアウトを見つけます。

```csharp
private static List<string> GetNotEmptyLayoutsForDxf(CadImage cadImage)
{
    // ... (continue to the next step)
}
```

## 手順 7: レイアウトサイズの取得と画像として保存

最後に、検出した各レイアウトをループし、範囲情報を読み取って、必要に応じてレイアウトを画像ファイルとしてレンダリングし、視覚的に確認できるようにします。

```csharp
foreach (string layout in layouts)
{
    // ... (continue to the next step)
}
```

## よくある問題とヒント

- **レイアウト名が見つからない場合:** CAD ファイルにペーパー空間レイアウトが含まれているか確認してください。モデル空間のみの場合があります。  
- **単位が期待と異なる場合:** 取得されるサイズは図面のネイティブ単位です。必要に応じてミリメートルやインチに変換してください。  
- **パフォーマンス:** 非常に大きな DWG/DXF ファイルはメモリ使用量が高くなることがあります。非同期処理やバッチ処理を検討してください。

## FAQ

**Q: Aspose.CAD はすべての CAD ファイル形式に対応していますか？**  
A: はい、DWG、DXF、DGN など多数のフォーマットと多くの BIM ファイルタイプをサポートしています。

**Q: 画像保存オプションはカスタマイズできますか？**  
A: もちろんです。`CadRasterizationOptions`（フォーマット、解像度、背景色など）を調整して、目的に合わせた画像を生成できます。

**Q: 追加のドキュメントはどこで入手できますか？**  
A: 詳細な API リファレンスやサンプルは [Aspose.CAD ドキュメント](https://reference.aspose.com/cad/net/) をご参照ください。

**Q: 無料トライアルはありますか？**  
A: はい、[無料トライアル](https://releases.aspose.com/) で Aspose.CAD をお試しいただけます。

**Q: 技術サポートはどこで受けられますか？**  
A: 技術サポートは [Aspose.CAD フォーラム](https://forum.aspose.com/c/cad/19) でご利用いただけます。

---

**最終更新日:** 2026-03-21  
**テスト環境:** Aspose.CAD 24.11 for .NET  
**作成者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}