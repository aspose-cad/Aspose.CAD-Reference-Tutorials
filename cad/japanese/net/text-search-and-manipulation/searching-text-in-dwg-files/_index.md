---
title: C# を使用した DWG ファイル内のテキストの検索 - Aspose.CAD チュートリアル
linktitle: C# を使用して DWG ファイル内のテキストを検索する
second_title: Aspose.CAD .NET - CAD および BIM ファイル形式
description: このステップバイステップ ガイドを使用して、Aspose.CAD for .NET を探索し、DWG ファイル内のテキスト検索をマスターしてください。今すぐ CAD アプリケーションを強化しましょう!
weight: 10
url: /ja/net/text-search-and-manipulation/searching-text-in-dwg-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# C# を使用した DWG ファイル内のテキストの検索 - Aspose.CAD チュートリアル

## 導入

CAD (コンピュータ支援設計) の動的領域では、精度と効率が最も重要です。 DWG ファイル内で特定のテキストを検索する必要があるシナリオを想像してください。 Aspose.CAD for .NET は、C# を使用して DWG ファイル内のテキストをシームレスに検索するための堅牢なソリューションを提供します。このチュートリアルでは、Aspose.CAD for .NET の可能性を最大限に活用できるように、プロセスをガイドします。

## 前提条件

チュートリアルに入る前に、次の前提条件が満たされていることを確認してください。
-  Aspose.CAD for .NET: ライブラリがインストールされていることを確認してください。からダウンロードできます。[Aspose.CAD Web サイト](https://releases.aspose.com/cad/net/).
- ドキュメント ディレクトリ: DWG ファイルを専用のディレクトリに整理します。

## 名前空間のインポート

C# プロジェクトで、Aspose.CAD を操作するために必要な名前空間をインポートします。次の名前空間をコードに追加します。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects.AttEntities;
```

## ステップ 1: DWG ファイルをロードする

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "search.dwg";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    //コードはここにあります
}
```

## ステップ 2: エンティティ セクションでテキストを検索する

```csharp
foreach (CadBaseEntity entity in cadImage.Entities)
{
    IterateCADNodes(entity);
}
```

## ステップ 3: ブロックセクション内のテキストを検索する

```csharp
foreach (CadBlockEntity blockEntity in cadImage.BlockEntities.Values)
{
    foreach (CadBaseEntity entity in blockEntity.Entities)
    {
        IterateCADNodes(entity);
    }
}
```

## ステップ 4: CAD ノードを反復処理する

```csharp
private static void IterateCADNodes(CadBaseEntity obj)
{
    switch (obj.TypeName)
    {
        //さまざまなエンティティ タイプを処理する
    }
}
```

## ステップ 5: PDF にエクスポートする

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
//ラスタライズオプションを構成する
rasterizationOptions.Layouts = new[] { "Layout1" };
Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
cadImage.Save(MyDir + "SearchText_out.pdf", pdfOptions);
```

## 結論

Aspose.CAD for .NET は、DWG ファイル内のテキストを検索するためのシームレスなソリューションを提供し、開発者が CAD アプリケーションを強化できるようにします。このチュートリアルに従うことで、DWG ファイル内の特定のテキストを効率的に検索する機能が利用できるようになりました。

## よくある質問

### Q1: Aspose.CAD for .NET を他の CAD 形式で使用できますか?

A1: はい、Aspose.CAD はさまざまな CAD 形式をサポートし、多用途のソリューションを提供します。

### Q2: Aspose.CAD for .NET の無料トライアルはありますか?

 A2: はい、次の機能を使用して機能を探索できます。[無料トライアル](https://releases.aspose.com/).

### Q3: Aspose.CAD for .NET のサポートを受けるにはどうすればよいですか?

 A3: にアクセスしてください。[Aspose.CAD フォーラム](https://forum.aspose.com/c/cad/19)コミュニティサポートのために。

### Q4: 仮免許とは何ですか?どうすれば取得できますか?

 A4: 仮免許を取得する[ここ](https://purchase.aspose.com/temporary-license/)一時的な使用のために。

### Q5: Aspose.CAD for .NET の詳細なドキュメントはどこで入手できますか?

 A5: 総合を参照してください。[ドキュメンテーション](https://reference.aspose.com/cad/net/)詳しい指導が受けられます。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
