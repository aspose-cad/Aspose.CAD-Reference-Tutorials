---
title: Aspose.CAD for .NET で DWG の一部として DGN をエクスポート
linktitle: DGN を DWG の一部としてエクスポート
second_title: Aspose.CAD .NET - CAD および BIM ファイル形式
description: Aspose.CAD for .NET で DGN を DWG の一部としてエクスポートする方法を学びます。シームレスな統合については、ステップバイステップのガイドに従ってください。
weight: 11
url: /ja/net/cad-export-formats/export-dgn-as-part-of-dwg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for .NET で DWG の一部として DGN をエクスポート

## 導入

.NET 開発の世界では、Aspose.CAD はコンピュータ支援設計 (CAD) ファイルを操作するための強力なライブラリとして際立っています。このチュートリアルでは、Aspose.CAD for .NET を使用して、DGN (デザイン) ファイルを DWG (図面) ファイルの一部としてエクスポートするプロセスについて説明します。経験豊富な開発者でも、初心者でも、このステップバイステップ ガイドは、Aspose.CAD の機能を活用してこの特定のタスクを効率的に達成するのに役立ちます。

## 前提条件

チュートリアルに入る前に、次の前提条件が満たされていることを確認してください。

-  Aspose.CAD for .NET: .NET 用の Aspose.CAD ライブラリがインストールされていることを確認します。ダウンロードできます[ここ](https://releases.aspose.com/cad/net/).

- 開発環境: Visual Studio など、好みの .NET 開発環境をセットアップします。

- C# の基本知識: C# プログラミング言語に慣れておきます。

## 名前空間のインポート

C# プロジェクトに、Aspose.CAD 機能にアクセスするために必要な名前空間を含めます。コード ファイルの先頭に次の using ディレクティブを追加します。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

ここで、提供されたコードを複数のステップに分割してみましょう。

## ステップ 1: ファイル パスを定義する

```csharp
//入力および出力ファイルのパス
string fileName = "BlockRefDgn.dwg";
string outPath = fileName + ".pdf";
```

## ステップ 2: PdfOptions インスタンスを作成する

```csharp
//DWG を PDF にエクスポートするための PdfOptions クラスのインスタンスを作成する
PdfOptions exportOptions = new PdfOptions();
```

## ステップ 3: DWG ファイルをロードする

```csharp
//既存の DWG ファイルを画像としてロードし、CadImage タイプに変換します
using (CadImage cadImage = (CadImage)Image.Load(fileName))
```

## ステップ 4: エンティティを反復処理する

```csharp
//DWG ファイル内の各エンティティを反復処理します。
foreach (CadBaseEntity baseEntity in cadImage.Entities)
```

## ステップ 5: エンティティ タイプを確認する

```csharp
//エンティティがイメージ定義であるかどうかを確認する
if (baseEntity.TypeName == CadEntityTypeName.DGNUNDERLAY)
```

## ステップ 6: アンダーレイ パスを取得する

```csharp
//イメージ定義の場合は、オブジェクトへの外部参照を取得します。
CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
Console.WriteLine(dgnFile.UnderlayPath);
```

## ステップ 7: ラスタライズ オプションを定義する

```csharp
//CadRasterizationOptions オブジェクトの設定を定義する
exportOptions.VectorRasterizationOptions = new CadRasterizationOptions()
{
    PageWidth = 1600,
    PageHeight = 1600,
    Layouts = new string[] { "Model" },
    AutomaticLayoutsScaling = false,
    NoScaling = true,
    BackgroundColor = Color.Black,
    DrawType = CadDrawTypeMode.UseObjectColor
};
```

## ステップ 8: DWG を PDF にエクスポートする

```csharp
//Save メソッドを呼び出して DWG を PDF にエクスポートします
cadImage.Save(outPath, exportOptions);
```

## 結論

おめでとう！ Aspose.CAD for .NET を使用して、DGN ファイルを DWG ファイルの一部としてエクスポートするプロセスを完了しました。このチュートリアルでは、この特定のタスクをシームレスに実行するための基本的な手順とコード スニペットを説明しました。

## よくある質問

### Q1: Aspose.CAD for .NET を商用プロジェクトで使用できますか?
 A1: はい、可能です。訪問[ここ](https://purchase.aspose.com/buy)ライセンス オプションを検討します。

### Q2: 処理できる DWG ファイルのサイズに制限はありますか?
A2: Aspose.CAD は大きな DWG ファイルの処理をサポートしていますが、ハードウェア制限が適用される場合があります。

### Q3: 体験版はありますか?
A3: はい、無料トライアルを利用できます。[ここ](https://releases.aspose.com/).

### Q4: 一時ライセンスを取得するにはどうすればよいですか?
 A4: 仮免許は取得可能です[ここ](https://purchase.aspose.com/temporary-license/).

### Q5: 問題が発生した場合はどこに問い合わせればよいですか?
 A5: Aspose.CAD フォーラムにアクセスしてください。[ここ](https://forum.aspose.com/c/cad/19)サポートのための。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
