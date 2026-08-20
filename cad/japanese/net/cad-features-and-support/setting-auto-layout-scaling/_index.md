---
date: 2026-03-26
description: Aspose.CAD for .NET の Auto Layout Scaling を使用して、CAD から PDF を作成し、DXF を
  PDF に変換する方法を学び、正確で柔軟なレンダリングを実現します。
linktitle: Setting Auto Layout Scaling
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 'CADからPDFを作成: オートレイアウトスケーリング – Aspose.CAD'
url: /ja/net/cad-features-and-support/setting-auto-layout-scaling/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CADからPDFを作成: Auto Layout Scaling – Aspose.CAD

モダンな .NET アプリケーションでは、CAD 図面を高品質な PDF に変換することは一般的な要件です—レポート作成、共有、アーカイブのために **create PDF from CAD** が必要な場合でも。このチュートリアルでは、Aspose.CAD for .NET を使用して Auto Layout Scaling を有効にし、ピクセル単位で完璧な結果を得る方法と、最小限のコードで **convert DXF to PDF** と **export CAD to PDF** の方法を紹介します。

## クイック回答
- **Auto Layout Scaling は何をしますか？** ページサイズに合わせてレイアウトを自動的に調整し、ジオメトリの忠実度を保ちます。  
- **どのフォーマットがサポートされていますか？** Aspose.CAD が読み取れるすべてのフォーマット（DXF、DWG、DGN など）は PDF にエクスポートできます。  
- **ライセンスは必要ですか？** 開発には無料トライアルが使用でき、製品版には商用ライセンスが必要です。  
- **ページサイズを変更できますか？** はい—`CadRasterizationOptions` の `PageWidth` と `PageHeight` を設定します。  
- **.NET Core と互換性がありますか？** 完全に対応しており、.NET Framework と .NET Core/5/6+ で動作します。

## “create PDF from CAD” とは何ですか？
CAD ファイルから PDF を作成することは、ベクタードローイングデータをラスタライズしてポータブルドキュメント形式に変換することを意味します。この変換はレイヤー、線幅、色を保持し、CAD ソフトウェアがなくても任意のデバイスでファイルを閲覧できるようにします。

## Auto Layout Scaling を使用する理由
Auto Layout Scaling は、図面全体が出力ページにきれいに収まるようにし、スケーリング係数の手動計算を不要にします。特に、建築図面や機械図面など、サイズが異なる図面を扱う場合に便利です。

## 前提条件
1. **Aspose.CAD for .NET** – 最新のライブラリを [download page](https://releases.aspose.com/cad/net/) からダウンロードします。  
2. **.NET 開発環境** – Visual Studio、Rider、または C# をサポートする任意のエディタ。  
3. **サンプル DXF ファイル** – 例: `conic_pyramid.dxf`、または変換したい任意の CAD ファイル。

## 名前空間のインポート
Aspose.CAD クラスにアクセスできるように、必要な名前空間を追加します。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## ステップ 1: CAD ファイルの読み込み
ソース図面を `Image` オブジェクトにロードします。これが以降のすべての処理のエントリーポイントです。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    // Your code here
}
```

## ステップ 2: ラスタライズオプションの設定
出力ページの寸法を定義します。希望する PDF サイズに合わせてこれらの値を調整してください。

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

## ステップ 3: Auto Layout Scaling の有効化
自動スケーリングを有効にし、図面がページに切れずに収まるようにします。

```csharp
rasterizationOptions.AutomaticLayoutsScaling = true;
```

## ステップ 4: PDF オプションの作成
ラスタライズ設定を PDF エクスポーターにリンクします。

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## ステップ 5: 結果の保存 – CAD から PDF を作成
出力パスを指定し、画像を PDF として保存します。このステップで、設定したスケーリングを使用して **create PDF from CAD** が実行されます。

```csharp
MyDir = MyDir + "result_out.pdf";
image.Save(MyDir, pdfOptions);
```

## よくある問題とヒント
- **フォントや線種が欠落していますか？** CAD ファイルの参照が埋め込まれているか、サーバー上に存在することを確認してください。  
- **大きなファイルでメモリ圧迫が発生しますか？** 図面を分割して処理するか、アプリケーションのメモリ上限を増やしてください。  
- **出力がぼやけていますか？** より高い DPI のために `PageWidth`/`PageHeight` を増やすか、`CadRasterizationOptions` の `Resolution` を設定してください。

## よくある質問

**Q: DXF 以外のファイル形式にも Auto Layout Scaling を適用できますか？**  
A: はい、Aspose.CAD は DWG、DGN など多数の CAD フォーマットで自動スケーリングをサポートしています。

**Q: レンダリング処理中のエラーはどのように処理できますか？**  
A: 変換コードを `try‑catch` ブロックで囲み、詳細なエラー情報を得るために `Aspose.CAD.CadException` をキャッチしてください。

**Q: Aspose.CAD が扱えるファイルサイズに制限はありますか？**  
A: ライブラリは大きなファイル向けに設計されていますが、パフォーマンスは利用可能な RAM と CPU に依存します。非常に大きな図面は、リソースが豊富なサーバーで処理することを検討してください。

**Q: 出力 PDF をさらにカスタマイズできますか（例: ウォーターマークやメタデータの追加）？**  
A: もちろんです。保存後に Aspose.PDF を使用して PDF を変更できます—ウォーターマークの追加、ドキュメントプロパティの設定、ページの結合などが可能です。

**Q: Aspose.CAD の追加リソースやサポートはどこで見つけられますか？**  
A: コミュニティの支援は [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) で探し、より詳しい API の詳細は [documentation](https://reference.aspose.com/cad/net/) を参照してください。

## 結論
これで **create PDF from CAD** の方法、**Auto Layout Scaling** の有効化、そして Aspose.CAD for .NET を使用した **convert DXF to PDF** の効果的な手順を学びました。このアプローチにより、実装をシンプルに保ちつつ、レンダリング品質を完全にコントロールできます。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最終更新日:** 2026-03-26  
**テスト環境:** Aspose.CAD for .NET 24.12 (latest)  
**作者:** Aspose