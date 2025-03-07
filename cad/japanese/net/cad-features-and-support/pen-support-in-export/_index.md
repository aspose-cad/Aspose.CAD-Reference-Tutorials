---
title: Aspose.CAD for .NET のカスタム ペン オプションを使用して CAD エクスポートを強化する
linktitle: エクスポート時のペンのサポート
second_title: Aspose.CAD .NET - CAD および BIM ファイル形式
description: Aspose.CAD for .NET を使用して CAD イメージのエクスポートを強化する方法を学びます。ペン オプションをカスタマイズして、PDF、PNG、BMP などの美しいビジュアルを実現します。
weight: 12
url: /ja/net/cad-features-and-support/pen-support-in-export/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for .NET のカスタム ペン オプションを使用して CAD エクスポートを強化する

## 導入

Aspose.CAD for .NET は、コンピュータ支援設計 (CAD) ファイルを操作するための強力なツール セットを提供し、開発者が CAD イメージをシームレスに操作およびエクスポートできるようにします。注目すべき機能の 1 つは、エクスポート時のペンのサポートです。ユーザーは、CAD イメージを PDF、PNG、BMP、GIF、JPEG2000、JPEG、PSD、TIFF、WMF などのさまざまな形式にエクスポートするときに、ペンの開始キャップと終了キャップの設定をカスタマイズできます。

このチュートリアルでは、Aspose.CAD for .NET を使用したエクスポートにおけるペン サポートの詳細を詳しく説明します。各ステップを詳しく説明し、プロセスをガイドする明確な説明と例を提供します。

## 前提条件

チュートリアルに入る前に、次の前提条件が満たされていることを確認してください。

- Aspose.CAD for .NET が開発環境にインストールされています。からダウンロードできます。[リリースページ](https://releases.aspose.com/cad/net/).

- CAD ファイル形式、特に DXF (Drawing Exchange Format) についての基本的な理解。

- C# プログラミング言語に関する実践的な知識。

## 名前空間のインポート

開始するには、C# プロジェクトに必要な名前空間をインポートしていることを確認してください。

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Drawing;
using System.Drawing.Drawing2D;
```

## ステップ 1: ドキュメント ディレクトリを設定する

CAD ドキュメントが配置されるディレクトリを定義します。

```csharp
string MyDir = "Your Document Directory";
```

## ステップ 2: CAD イメージをロードする

Aspose.CAD を使用して CAD イメージをロードします。

```csharp
string sourceFilePath = MyDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage)Image.Load(sourceFilePath);
```

## ステップ 3: ラスター化オプションを構成する

ラスタライズおよび PDF オプションを作成して、エクスポート プロセスをカスタマイズします。

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
PdfOptions pdfOptions = new PdfOptions();
```

## ステップ 4: ペンのオプションをカスタマイズする

ペンの開始キャップと終了キャップのオプションを設定します。

```csharp
rasterizationOptions.PenOptions = new PenOptions
{
   StartCap = LineCap.Flat,
   EndCap = LineCap.Flat
};
```

## ステップ 5: ベクトル ラスタライズ オプションを適用する

ラスタライズ オプションを PDF オプションに適用します。

```csharp
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## ステップ 6: エクスポートされた PDF を保存する

カスタマイズしたペン オプションを含む CAD イメージを PDF ファイルとして保存します。

```csharp
cadImage.Save(MyDir + "9LHATT-A56_generated.pdf", pdfOptions);
```

## 結論

このチュートリアルでは、Aspose.CAD for .NET のエクスポート機能におけるペンのサポートについて調べました。ステップバイステップのガイドに従うことで、ペンの開始キャップと終了キャップの設定を簡単にカスタマイズでき、CAD イメージのエクスポートの柔軟性が向上します。

エクスポートされた画像で希望の視覚効果を実現するために、さまざまなペン オプションを自由に試してください。

## よくある質問

### Q1: これらのペン オプションは PDF 以外の画像形式にも使用できますか?

A1: はい、ペン オプションは、PNG、BMP、GIF、JPEG などのさまざまな画像形式に適用できます。

### Q2: Aspose.CAD for .NET の追加ドキュメントはどこで入手できますか?

 A2: を参照してください。[ドキュメンテーション](https://reference.aspose.com/cad/net/)包括的な情報と例については、こちらをご覧ください。

### Q3: Aspose.CAD for .NET の無料トライアルはありますか?

 A3: はい、無料トライアルにアクセスできます。[ここ](https://releases.aspose.com/).

### Q4: Aspose.CAD for .NET の一時ライセンスを取得するにはどうすればよいですか?

 A4: にアクセスしてください。[一時ライセンスのページ](https://purchase.aspose.com/temporary-license/)一時的なライセンス オプションの場合。

### Q5: Aspose.CAD for .NET のコミュニティ サポートはどこで求められますか?

 A5: コミュニティとの関わり[Aspose.CAD フォーラム](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
