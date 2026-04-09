---
date: 2026-04-09
description: このステップバイステップガイドで、Aspose.CAD for .NET を使用して DWG を画像に変換する方法と、アンダーレイフラグの読み取り方法を学びましょう。
keywords:
- convert dwg to image
- how to read underlay
- Aspose.CAD DWG underlay flags
linktitle: DWGファイルのアンダーレイフラグを探る
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: DWG を画像に変換 – DWG ファイルのアンダーレイフラグを探る - Aspose.CAD チュートリアル
url: /ja/net/dwg-file-manipulation/exploring-underlay-flags-of-dwg/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG ファイルのアンダーレイフラグの探索 - Aspose.CAD チュートリアル

## はじめに

CAD ファイル、特に DWG ファイルの複雑な世界に踏み込んでおり、**DWG を画像に変換**しながら **アンダーレイのフラグの読み取り方法** を知りたい場合、ここが適切な場所です。このチュートリアルでは、強力な Aspose.CAD for .NET ライブラリを使用して、アンダーレイ情報を抽出し、図面を画像として確実にレンダリングする手順をすべて説明します。

## クイック回答
- **“convert DWG to image” は何を意味しますか？**  
  Aspose.CAD を使用して DWG 図面をラスタ形式（PNG、JPEG など）にレンダリングすることを意味します。
- **どのメソッドがアンダーレイフラグを示しますか？**  
  `CadUnderlay` オブジェクトの `Flags` プロパティにアクセスします（DWG をロードした後）。
- **Aspose.CAD のライセンスは必要ですか？**  
  評価用の一時ライセンスが利用可能です。製品環境ではフルライセンスが必要です。
- **サポートされている .NET バージョンは何ですか？**  
  .NET Framework 4.6 以上、.NET Core 3.1 以上、.NET 5/6 以降。
- **アンダーレイジオメトリを抽出できますか？**  
  はい。アンダーレイのパス、挿入ポイント、スケール、回転、フラグ状態はすべて取得可能です。

## “convert DWG to image” とは何か、そしてなぜ重要か

DWG ファイルを画像に変換すると、ブラウザで CAD 図面を表示したり、レポートに埋め込んだり、CAD ビューアを持たない関係者と共有したりできます。レンダリング中に、**アンダーレイ** オブジェクト（例: DGN 参照）を検査して正しく表示されているか確認する必要があることがよくあります。アンダーレイフラグを理解することで、クリッピング、モノクロレンダリング、可視性の問題を最終画像を生成する前にトラブルシューティングできます。

## 前提条件

- C# と .NET プログラミングの基本的な理解。  
- **Aspose.CAD for .NET** ライブラリがインストール済み。まだお持ちでない場合は **[here](https://releases.aspose.com/cad/net/)** からダウンロードしてください。  
- テスト用の DWG ファイル – 本ガイド全体で使用するサンプルファイル **“BlockRefDgn.dwg”**。

## 名前空間のインポート

To get started, import the necessary namespaces:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## ステップ 1: DWG ファイルをロードして `CadImage` に変換

First, load the DWG file and cast it to a `CadImage`. This object gives you access to all drawing entities, including underlays.

```csharp
string fileName = MyDir + "BlockRefDgn.dwg";

// Load DWG file and convert to CadImage
using (CadImage image = (CadImage)Image.Load(fileName))
{
    // Your code for subsequent steps will go here
}
```

## ステップ 2: エンティティを反復処理

Next, loop through every entity in the drawing. This is where you’ll locate underlay objects.

```csharp
foreach (CadBaseEntity entity in image.Entities)
{
    // Your code for subsequent steps will go here
}
```

## ステップ 3: `CadDgnUnderlay` タイプをチェック

Identify underlay entities by checking their runtime type. The `CadDgnUnderlay` class represents DGN underlays embedded in a DWG.

```csharp
if (entity is CadDgnUnderlay)
{
    // Your code for subsequent steps will go here
}
```

## ステップ 4: アンダーレイフラグにアクセス

Once you have a `CadDgnUnderlay`, cast it to `CadUnderlay` to read its properties and flag states. The flags tell you whether the underlay is visible, clipped, or rendered in monochrome.

```csharp
CadUnderlay underlay = entity as CadUnderlay;

Console.WriteLine(underlay.UnderlayPath);
Console.WriteLine(underlay.UnderlayName);
Console.WriteLine(underlay.InsertionPoint.X);
Console.WriteLine(underlay.InsertionPoint.Y);
Console.WriteLine(underlay.RotationAngle);
Console.WriteLine(underlay.ScaleX);
Console.WriteLine(underlay.ScaleY);
Console.WriteLine(underlay.ScaleZ);
Console.WriteLine((underlay.Flags & UnderlayFlags.UnderlayIsOn) == UnderlayFlags.UnderlayIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.ClippingIsOn) == UnderlayFlags.ClippingIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.Monochrome) != UnderlayFlags.Monochrome);
```

### 出力が示す内容

- **UnderlayPath / UnderlayName** – 外部 DGN ファイルが存在する場所。  
- **InsertionPoint (X, Y)** – アンダーレイが DWG 空間に配置される座標。  
- **RotationAngle** – アンダーレイに適用された回転角度。  
- **ScaleX / ScaleY / ScaleZ** – 各軸のスケーリング係数。  
- **Flags** – 可視性 (`UnderlayIsOn`)、クリッピング (`ClippingIsOn`)、モノクロレンダリング (`Monochrome`) を示すブール値。

## よくある問題と解決策

| 問題 | 原因 | 解決策 |
|------|------|--------|
| フラグチェックで出力がない | アンダーレイがオフになっているとフラグは 0 がデフォルトになります。 | DWG にアクティブなアンダーレイが含まれていることを確認するか、元の CAD ファイルで可視性を切り替えてください。 |
| `Invalid cast` 例外 | エンティティが `CadDgnUnderlay` ではありません。 | `if (entity is CadDgnUnderlay)` ガードをキャスト前に確認してください。 |
| フラグ抽出後に画像レンダリングが失敗 | アンダーレイがクリップされているかオフになっている可能性があり、空白領域になります。 | 最終画像をレンダリングする前にフラグを調整してください（`UnderlayIsOn = true`、`ClippingIsOn = false`）。 |

## よくある質問

### Q1: Aspose.CAD for .NET を他の CAD ファイル形式と併用できますか？

A1: Aspose.CAD は DWG、DXF、DGN など、さまざまな CAD 形式をサポートしています。完全なリストはドキュメントをご確認ください。

### Q2: Aspose.CAD for .NET の一時ライセンスは利用可能ですか？

A2: はい、**[here](https://purchase.aspose.com/temporary-license/)** から一時ライセンスを取得できます。

### Q3: Aspose.CAD for .NET のサポートはどこで見つけられますか？

A3: サポートフォーラムは **[here](https://forum.aspose.com/c/cad/19)** でご利用ください。

### Q4: Aspose.CAD for .NET を購入するには？

A4: ライブラリは **[here](https://purchase.aspose.com/buy)** から購入できます。

### Q5: 無料トライアルは利用できますか？

A5: はい、無料トライアルは **[here](https://releases.aspose.com/)** で利用できます。

## 結論

Congratulations! You've successfully learned **how to convert DWG to image** while also mastering **how to read underlay** flags using Aspose.CAD for .NET. With this knowledge you can:

- Render DWG drawings as raster images for web or reporting scenarios.  
- Inspect and manipulate underlay properties to ensure correct display.  
- Debug visibility, clipping, and monochrome issues before final image generation.

Feel free to explore other Aspose.CAD features such as layer management, text extraction, and batch conversion to further extend your CAD automation workflows.

---

**最終更新日:** 2026-04-09  
**テスト環境:** Aspose.CAD for .NET 24.11  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}