---
title: C# での DWG から DXF 形式へのエクスポート - Aspose.CAD チュートリアル
linktitle: C# で DWG を DXF 形式にエクスポートする
second_title: Aspose.CAD .NET - CAD および BIM ファイル形式
description: Aspose.CAD を使用して、C# での CAD ファイル操作のロックを解除します。 DWG を DXF に簡単にエクスポートする方法を学びましょう。シームレスな統合については、ステップバイステップのガイドに従ってください。
weight: 10
url: /ja/net/advanced-export-techniques/exporting-dwg-to-dxf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# C# での DWG から DXF 形式へのエクスポート - Aspose.CAD チュートリアル

## 導入

CAD ファイルを操作するための強力なソリューションを探している .NET 開発者にとって、Aspose.CAD は頼りになるツールです。このステップバイステップのチュートリアルでは、C# と Aspose.CAD を使用して DWG ファイルを DXF 形式にエクスポートするプロセスを説明します。

## 前提条件

チュートリアルに入る前に、次の前提条件が満たされていることを確認してください。

1.  Aspose.CAD ライブラリ: Aspose.CAD ライブラリを次からダウンロードしてインストールします。[このリンク](https://releases.aspose.com/cad/net/).

2. 開発環境: Visual Studio などの C# 開発環境をセットアップします。

3. サンプル DWG ファイル: エクスポートするサンプル DWG ファイルを準備します。このチュートリアルでは、「Your Document Directory」ディレクトリにある「Line.dwg」という名前のファイルを使用します。

## 名前空間のインポート

C# プロジェクトに、Aspose.CAD を操作するために必要な名前空間を含めます。

```csharp
using Aspose.CAD.FileFormats.Cad;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## ステップ 1: DWG ファイルをロードする

まず、DWG ファイルを C# アプリケーションにロードします。これを実現するためのコード スニペットを次に示します。

```csharp
string MyDir = "Your Document Directory";
string inputFile = MyDir + "Line.dwg";
using (var cadImage = (CadImage)Image.Load(inputFile))
{
    //さらなるステップのコードはここにあります
}
```

## ステップ 2: DXF として保存

DWG ファイルがロードされたら、次のステップはそれを DXF ファイルとして保存することです。前の using ブロック内に次のコードを追加します。

```csharp
string outFile = MyDir + "Line_19.2.dxf";
cadImage.Save(outFile);
```

## 結論

おめでとう！ C# の Aspose.CAD を使用して、DWG ファイルを DXF 形式にエクスポートできました。このシンプルかつ強力なプロセスにより、アプリケーションでの CAD ファイル操作の可能性が広がります。

## よくある質問

### Q1: Aspose.CAD は最新の CAD ファイル形式と互換性がありますか?

A1: はい、Aspose.CAD は最新の CAD ファイル形式との互換性を確保するために定期的に更新されます。

### Q2: Aspose.CAD を商用プロジェクトで使用できますか?

 A2: もちろんです！ Aspose.CAD には、個人使用と商用使用の両方のためのライセンス オプションが付属しています。訪問[このリンク](https://purchase.aspose.com/buy)詳細については。

### Q3: 無料トライアルはありますか?

 A3: はい、無料トライアルで Aspose.CAD を試すことができます。訪問[このリンク](https://releases.aspose.com/)始めるために。

### Q4: Aspose.CAD の詳細なドキュメントはどこで入手できますか?

A4: 次のドキュメントを参照してください。[このリンク](https://reference.aspose.com/cad/net/)総合的な指導を行います。

### Q5: サポートが必要ですか、または具体的な質問がありますか?

 A5: Aspose.CAD コミュニティ フォーラムにアクセスしてください。[ここ](https://forum.aspose.com/c/cad/19)専門家の支援とコミュニティのサポートが必要です。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
