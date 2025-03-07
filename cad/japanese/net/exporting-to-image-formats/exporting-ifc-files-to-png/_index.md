---
title: IFC ファイルを PNG にエクスポートする - Aspose.CAD チュートリアル
linktitle: IFC ファイルを PNG にエクスポートする
second_title: Aspose.CAD .NET - CAD および BIM ファイル形式
description: IFC から PNG へのシームレスな変換のための堅牢なソリューションである Aspose.CAD for .NET を探索してください。 CAD ファイルを効率的に処理するには、今すぐダウンロードしてください。
weight: 10
url: /ja/net/exporting-to-image-formats/exporting-ifc-files-to-png/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# IFC ファイルを PNG にエクスポートする - Aspose.CAD チュートリアル

## 導入

コンピュータ支援設計 (CAD) のダイナミックな世界では、効率的なファイル変換が非常に重要です。 Aspose.CAD for .NET は、IFC (Industry Foundation Classes) ファイルを PNG 形式にエクスポートするためのシームレスな機能を提供する強力なツールとして登場しました。このステップバイステップのチュートリアルでは、Aspose.CAD をスムーズに操作できるようにプロセスをガイドします。

## 前提条件

チュートリアルに入る前に、次の前提条件が満たされていることを確認してください。

### 1. Aspose.CAD のインストール

Aspose.CAD for .NET がインストールされていることを確認してください。リリースページからダウンロードできます[ここ](https://releases.aspose.com/cad/net/).

### 2. ドキュメントディレクトリ

ドキュメント用に指定されたディレクトリを作成します。提供された例では、変数`MyDir`はドキュメントディレクトリを表します。

## 名前空間のインポート

前提条件が設定されたので、Aspose.CAD 機能を使用するために必要な名前空間を .NET アプリケーションにインポートしましょう。

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using Aspose.CAD.FileFormats.Ifc;
```

## ステップ 1: IFC ファイルをロードする

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "example.ifc";
using (IfcImage cadImage = (IfcImage)Image.Load(sourceFilePath))
{
```

このステップでは、Aspose.CAD を初期化します。`IfcImage`オブジェクトを作成し、その中に IFC ファイルをロードします。

## ステップ 2: ラスタライズ オプションを設定する

```csharp
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
   
    rasterizationOptions.PageWidth = 100;
    rasterizationOptions.PageHeight = 100;
```

ラスタライズ オプションを定義して、PNG 出力のページの幅と高さを構成します。

## ステップ 3: PNG オプションを設定する

```csharp
    PngOptions pngOptions = new PngOptions();
    pngOptions.VectorRasterizationOptions = rasterizationOptions;
```

PNG オプションを作成し、以前に定義したラスタライズ オプションを関連付けます。

## ステップ 4: 出力パスを指定する

```csharp
    //出力パスも設定します
    string outPath = sourceFilePath + ".png";
    cadImage.Save(outPath, pngOptions);
}
```

PNG ファイルの出力パスを定義し、ソース ファイルと同じ名前で拡張子が「.png」であることを確認します。最後に、変換された画像を保存します。

## 結論

これらの簡単な手順により、Aspose.CAD for .NET を使用して IFC ファイルを PNG に正常にエクスポートできました。この多用途ツールは CAD 変換プロセスを簡素化し、開発者やエンジニアが利用できるようにします。

## よくある質問

### Q1: macOS または Linux で Aspose.CAD for .NET を使用できますか?

A1: いいえ、Aspose.CAD for .NET は Windows 環境向けに特別に設計されています。

### Q2: 一時ライセンスはテスト目的で利用できますか?

 A2: はい、次から一時ライセンスを取得できます。[ここ](https://purchase.aspose.com/temporary-license/)評価用に。

### Q3: Aspose.CAD のサポートを受けるにはどうすればよいですか?

 A3: にアクセスしてください。[Aspose.CAD フォーラム](https://forum.aspose.com/c/cad/19)コミュニティのサポートとディスカッションのために。

### Q4: 包括的なドキュメントはどこで入手できますか?

 A4: を参照してください。[Aspose.CAD ドキュメント](https://reference.aspose.com/cad/net/)詳細な情報と例については、

### Q5: インストール中に問題が発生した場合はどうすればよいですか?

 A5: ドキュメントを確認するか、サポートを求めてください。[Aspose.CAD フォーラム](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
