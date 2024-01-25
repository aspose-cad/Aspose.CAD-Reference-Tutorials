---
title: DWG ファイルのアンダーレイ フラグを調べる - Aspose.CAD チュートリアル
linktitle: DWG ファイルのアンダーレイ フラグの調査
second_title: Aspose.CAD .NET - CAD および BIM ファイル形式
description: DWG ファイルのアンダーレイ フラグを探索する際に、Aspose.CAD for .NET の機能を解放します。ステップバイステップのガイドに従ってください。
type: docs
weight: 13
url: /ja/net/dwg-file-manipulation/exploring-underlay-flags-of-dwg/
---
## 導入

CAD ファイル、特に DWG ファイルの複雑な世界を詳しく調べ、アンダーレイ フラグの謎を解き明かしたい場合は、ここが正しい場所です。このチュートリアルでは、強力な Aspose.CAD for .NET ライブラリを使用して、DWG ファイル内のアンダーレイ フラグを探索するプロセスを説明します。

## 前提条件

チュートリアルに入る前に、次のものが揃っていることを確認してください。

- C# および .NET プログラミングの基本的な理解。
-  Aspose.CAD for .NET ライブラリがインストールされています。そうでない場合は、ダウンロードできます[ここ](https://releases.aspose.com/cad/net/).
- テスト用の DWG ファイル。チュートリアルで提供されているサンプル ファイル「BlockRefDgn.dwg」を使用できます。

## 名前空間のインポート

開始するには、必要な名前空間をインポートする必要があります。以下に役立つスニペットを示します。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;

```

## ステップ 1: DWG ファイルをロードして CadImage に変換する

まず、既存の DWG ファイルをロードし、それを CadImage に変換します。

```csharp
string fileName = MyDir + "BlockRefDgn.dwg";

// DWG ファイルをロードし、CadImage に変換します
using (CadImage image = (CadImage)Image.Load(fileName))
{
    //後続のステップのコードはここに入力されます
}
```

## ステップ 2: エンティティを反復処理する

次に、DWG ファイル内の各エンティティを繰り返し処理します。

```csharp
foreach (CadBaseEntity entity in image.Entities)
{
    //後続のステップのコードはここに入力されます
}
```

## ステップ 3: CadDgnUnderlay タイプを確認する

エンティティのタイプが CadDgnUnderlay であるかどうかを確認します。

```csharp
if (entity is CadDgnUnderlay)
{
    //後続のステップのコードはここに入力されます
}
```

## ステップ 4: アンダーレイ フラグにアクセスする

さまざまなアンダーレイ フラグにアクセスし、関連情報を抽出します。

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

## 結論

おめでとう！ Aspose.CAD for .NET を使用して、DWG ファイルのアンダーレイ フラグを正常に調査できました。このチュートリアルでは、エンティティ内を移動し、アンダーレイに関する重要な情報を抽出するための知識を習得しました。

## よくある質問

### Q1: Aspose.CAD for .NET を他の CAD ファイル形式で使用できますか?

A1: Aspose.CAD は、DWG、DXF、DGN などを含むさまざまな CAD 形式をサポートしています。完全なリストについてはドキュメントを確認してください。

### Q2: Aspose.CAD for .NET の一時ライセンスは利用できますか?

 A2: はい、一時ライセンスを取得できます。[ここ](https://purchase.aspose.com/temporary-license/).

### Q3: Aspose.CAD for .NET のサポートはどこで見つけられますか?

 A3: サポート フォーラムにアクセスしてください[ここ](https://forum.aspose.com/c/cad/19)援助のために。

### Q4: Aspose.CAD for .NET を購入するにはどうすればよいですか?

A4: ライブラリを購入する[ここ](https://purchase.aspose.com/buy).

### Q5: 無料トライアルはありますか?

 A5: はい、無料トライアルにアクセスできます。[ここ](https://releases.aspose.com/).
