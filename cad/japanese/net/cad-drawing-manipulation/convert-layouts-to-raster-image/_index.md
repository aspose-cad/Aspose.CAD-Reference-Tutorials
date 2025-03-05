---
title: Aspose.CAD for .NET でレイアウトをラスター イメージに変換する
linktitle: レイアウトをラスター画像に変換
second_title: Aspose.CAD .NET - CAD および BIM ファイル形式
description: Aspose.CAD for .NET を使用して、CAD レイアウトをラスター イメージに簡単に変換します。強力な CAD 操作機能で開発を強化します。
type: docs
weight: 12
url: /ja/net/cad-drawing-manipulation/convert-layouts-to-raster-image/
---
## 導入

.NET アプリケーションでレイアウトをラスター イメージに簡単に変換したいと考えていますか?これ以上探さない！このステップバイステップ ガイドでは、コンピュータ支援設計 (CAD) タスクを簡素化する強力なライブラリである Aspose.CAD for .NET を使用するプロセスを順を追って説明します。

## 前提条件

チュートリアルに入る前に、次の前提条件が満たされていることを確認してください。

- Aspose.CAD for .NET ライブラリ: からライブラリをダウンロードしてインストールします。[Aspose.CAD for .NET ダウンロード ページ](https://releases.aspose.com/cad/net/).

- 開発環境: マシン上に動作する .NET 開発環境がセットアップされていることを確認してください。

- 変換するドキュメント: ラスター イメージに変換するレイアウトを含む CAD ドキュメントを準備します。

- ドキュメント ディレクトリ: コード内のプレースホルダー「ドキュメント ディレクトリ」をドキュメント ディレクトリへのパスに置き換えます。

## 名前空間のインポート

まず、コード内で Aspose.CAD 機能にアクセスできるようにするために必要な名前空間をインポートしましょう。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## ステップ 1: CAD ドキュメントをロードする

まず、Aspose.CAD ライブラリを使用して CAD ドキュメントをロードします。

```csharp
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image image = Image.Load(sourceFilePath))
{
    //さらなるステップのコードはここにあります
}
```

## ステップ 2: ラスタライズ オプションを構成する

のインスタンスを作成します`CadRasterizationOptions`をクリックして、ページの幅と高さを設定し、変換するレイアウトを指定します。

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1200;
rasterizationOptions.PageHeight = 1200;
rasterizationOptions.Layouts = new string[] { "Model", "Layout1" };
```

## ステップ 3: 結果イメージの TiffOptions をセットアップする

のインスタンスを作成します`TiffOptions`結果の画像の形式を定義します。

```csharp
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.VectorRasterizationOptions = rasterizationOptions;
```

## ステップ 4: 結果のイメージを保存する

出力パスを指定して、変換された画像を保存します。

```csharp
string outputFilePath = MyDir + "conic_pyramid_layoutstorasterimage_out.tiff";
image.Save(outputFilePath, options);
```

## 結論

おめでとう！ Aspose.CAD for .NET を使用して、CAD レイアウトをラスター イメージ形式に変換することができました。可能性は無限にあり、このガイドは CAD 関連の取り組みの出発点として役立ちます。

## よくある質問

### Q1: Aspose.CAD はすべての CAD 形式と互換性がありますか?

 A1: Aspose.CAD は、DWG、DXF、DWF、STL などを含む幅広い CAD 形式をサポートしています。チェックしてください[ドキュメンテーション](https://reference.aspose.com/cad/net/)包括的なリストについては、

### Q2: Aspose.CAD の一時ライセンスを取得するにはどうすればよいですか?

 A2: にアクセスしてください。[一時ライセンスのページ](https://purchase.aspose.com/temporary-license/)テストと評価を目的とした一時ライセンスを取得します。

### Q3: Aspose.CAD のサポートはどこで見つけられますか?

 A3: フォーラムは支援を求めるのに最適な場所です。訪問[Aspose.CAD フォーラム](https://forum.aspose.com/c/cad/19)コミュニティとつながり、助けを得ることができます。

### Q4: Aspose.CAD を無料で試すことはできますか?

A4：もちろんです！あなたのものをつかんでください[無料トライアル](https://releases.aspose.com/)Aspose.CAD の機能と機能を探索します。

### Q5: Aspose.CAD のライセンスはどこで購入できますか?

 A5: に移動します。[購入ページ](https://purchase.aspose.com/buy)ライセンスを購入して、Aspose.CAD の可能性を最大限に活用してください。