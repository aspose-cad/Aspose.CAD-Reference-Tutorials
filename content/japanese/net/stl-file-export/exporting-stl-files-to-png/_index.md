---
title: Aspose.CAD for .NET で STL から PNG への変換が簡単に
linktitle: STL ファイルを PNG にエクスポートする
second_title: Aspose.CAD .NET - CAD および BIM ファイル形式
description: Aspose.CAD for .NET を使用して、STL ファイルを PNG に簡単に変換します。シームレスな統合については、ステップバイステップのガイドに従ってください。ダウンロード中！
type: docs
weight: 10
url: /ja/net/stl-file-export/exporting-stl-files-to-png/
---
## 導入
コンピュータ支援設計 (CAD) のダイナミックな世界では、効率的なファイル変換が非常に重要です。 Aspose.CAD for .NET は、STL ファイルを PNG にエクスポートするプロセスを簡素化し、開発者に必要な柔軟性と機能を提供する強力なツールキットです。このチュートリアルでは、Aspose.CAD を使用して STL から PNG にスムーズに移行できるように、プロセスを段階的に説明します。
## 前提条件
チュートリアルに入る前に、次のものが整っていることを確認してください。
1.  Aspose.CAD for .NET: Aspose.CAD ライブラリをダウンロードしてインストールします。見つけられますよ[ここ](https://releases.aspose.com/cad/net/).
2. 開発環境: 好みの .NET 開発環境をセットアップします。
3. STL ファイル: 変換できる STL ファイルを用意します。このチュートリアルでは、「galeon.stl」という名前のサンプル ファイルを使用します。
## 名前空間のインポート
プロセスを開始するには、.NET アプリケーションに必要な名前空間をインポートします。これにより、STL から PNG への変換に必要なクラスとメソッドに確実にアクセスできるようになります。
```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```
## ステップ 1: ディレクトリとソース ファイルのパスを定義する
```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "galeon.stl";
```
「Your Document Directory」を、STL ファイルが存在する実際のディレクトリ パスに置き換えてください。
## ステップ 2: CAD イメージをロードする
```csharp
using (var cadImage = (CadImage)Image.Load(sourceFilePath))
{
    //以降のステップはこのブロック内で実行されます
}
```
この手順では、STL ファイルを CAD イメージとしてロードし、操作およびエクスポートできるようにします。
## ステップ 3: ラスタライズ オプションを設定する
```csharp
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 100;
rasterizationOptions.PageHeight = 100;
```
好みや要件に応じてページの幅と高さを調整します。これらの設定により、エクスポートされる PNG のサイズが決まります。
## ステップ 4: PNG オプションを構成する
```csharp
PngOptions pngOptions = new PngOptions();
pngOptions.VectorRasterizationOptions = rasterizationOptions;
```
前の手順で定義したラスタライズ設定を組み込んだ PNG オプションを作成します。
## ステップ 5: PNG ファイルを保存する
```csharp
string outPath = sourceFilePath + ".png";
cadImage.Save(outPath, pngOptions);
```
PNG ファイルの出力パスを指定し、提供されたオプションを使用して CAD イメージを PNG 形式で保存します。
特定のユースケースに必要に応じてこれらの手順を繰り返すと、Aspose.CAD for .NET を使用して STL ファイルを PNG に正常にエクスポートできます。
## 結論
Aspose.CAD for .NET は、STL ファイルを PNG に変換する複雑なタスクを簡素化し、開発者に信頼できるツールキットを提供します。このステップバイステップのガイドに従うことで、この機能をアプリケーションにシームレスに統合できます。
## よくある質問
### Q: エクスポートされた PNG の寸法をカスタマイズできますか?
絶対に！ステップ 3 で、`PageWidth`そして`PageHeight`特定の要件を満たす値を設定します。
### Q: 一時ライセンスはテスト目的で利用できますか?
はい、一時ライセンスを取得できます[ここ](https://purchase.aspose.com/temporary-license/)テストと評価用。
### Q: 追加のサポートやコミュニティのディスカッションはどこで見つけられますか?
訪問[Aspose.CAD フォーラム](https://forum.aspose.com/c/cad/19)サポートと協力的なディスカッションのために。
### Q: 変換がサポートされている他のファイル形式はありますか?
はい、Aspose.CAD は STL 以外のさまざまな CAD 形式をサポートしています。を参照してください。[ドキュメンテーション](https://reference.aspose.com/cad/net/)包括的なリストについては、
### Q: 複数の STL ファイルをバッチ処理できますか?
確かに！提供された手順に基づいてループを実装し、複数の STL ファイルをバッチ処理します。