---
date: 2026-04-03
description: Aspose.CAD を使用して C# でビューポートを設定し、DWG を PDF に変換する方法を学びましょう。この DWG から PDF
  へのチュートリアルでは、座標付きで正確なエクスポートを示します。
keywords:
- how to set viewport
- dwg to pdf tutorial
- convert dwg to pdf c#
linktitle: C#で座標付きDWGをPDFに変換する
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: C#で座標付きDWGをPDFに変換する際のビューポート設定方法 - Aspose.CADチュートリアル
url: /ja/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# C# で座標付き DWG を PDF に変換 - Aspose.CAD チュートリアル

## はじめに

Aspose.CAD for .NET を使用して、指定した座標で DWG ファイルを PDF に変換する際の **ビュー ポートの設定方法** についての包括的なチュートリアルへようこそ。ビュー ポートを制御することで、必要な領域と正確に一致するピクセル単位の完璧な PDF を得ることができ、建設図面やフロアプランのプレビュー、またはあらゆる BIM ワークフローに最適です。

## クイック回答
- **“set viewport” とは何ですか？** ラスタライズ中に CAD 図面の表示領域とスケーリングを定義します。  
- **変換を担当するライブラリはどれですか？** Aspose.CAD for .NET。  
- **ライセンスは必要ですか？** 無料トライアルで評価は可能ですが、実運用には商用ライセンスが必要です。  
- **サポートプラットフォームは？** .NET 5/6/7 または .NET Framework 4.6+ が動作する Windows、Linux、macOS。  
- **一般的な実装時間は？** 基本的な変換で約 10〜15 分です。

## 前提条件

始める前に、以下の前提条件が揃っていることを確認してください：

- **Aspose.CAD ライブラリ** – .NET 用の Aspose.CAD ライブラリをダウンロードしてインストールします。ライブラリは [here](https://releases.aspose.com/cad/net/) で入手できます。  
- **開発環境** – Visual Studio、Rider、または .NET 開発をサポートする任意の IDE。  
- **DWG ファイル** – 変換用の DWG ファイルを用意してください。提供されているサンプルファイルまたは独自の DWG ファイルを使用できます。

## 正確な PDF エクスポートのためのビュー ポート設定方法

ビュー ポートの設定は、レンダリングしたい図面の正確な領域を定義できる重要なステップです。以下のコードでは新しい `CadVportTableObject` を作成し、左上座標で位置を設定し、幅・高さ・アスペクト比を計算します。これが **ビュー ポートの設定方法** の実装で、変換の残りの部分を駆動します。

## 名前空間のインポート

C# プロジェクトで、必要な名前空間をインポートします：

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadParameters;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

コードをステップバイステップで分解し、理解しやすくしましょう：

## 手順 1: ドキュメント ディレクトリの定義

```csharp
string MyDir = "Your Document Directory";
```

## 手順 2: ソース DWG ファイル パスの設定

```csharp
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
```

## 手順 3: DWG ファイルの読み込みとラスタライズ オプションの構成

```csharp
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
    rasterizationOptions.Layouts = new string[] { "Model" };
    rasterizationOptions.NoScaling = true;
```

## 手順 4: 座標とビュー ポートの定義  

ここでは、エクスポートしたい領域の左上隅、幅、高さを指定することで実際に **ビュー ポートを設定**（ビュー ポートの設定方法）します。

```csharp
    Point topLeft = new Point(500, 1000);
    double width = 3108;
    double height = 2489;

    CadVportTableObject newView = new CadVportTableObject();
    newView.Name = new CadStringParameter();
    newView.Name.Init("*Active");
    newView.CenterPoint.X = topLeft.X + width / 2f;
    newView.CenterPoint.Y = topLeft.Y - height / 2f;
    newView.ViewHeight.Value = height;
    newView.ViewAspectRatio.Value = width / height;
```

## 手順 5: ビュー ポート設定の適用

```csharp
    for (int i = 0; i < cadImage.ViewPorts.Count; i++)
    {
        CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
        if (cadImage.ViewPorts.Count == 1 || string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
        {
            cadImage.ViewPorts[i] = newView;
            break;
        }
    }
```

## 手順 6: PDF オプションの構成とエクスポート  

これで全てを結びつけ、先ほど準備したラスタライズ オプションを使用して **DWG を PDF に変換** します。

```csharp
    Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
    pdfOptions.VectorRasterizationOptions = rasterizationOptions;

    MyDir = MyDir + "ConvertDWGToPDFBySupplyingCoordinates_out.pdf";
    cadImage.Save(MyDir, pdfOptions);
}
```

## 手順 7: 成功メッセージの表示

```csharp
Console.WriteLine("\nThe DWG file exported successfully to PDF.\nFile saved at " + MyDir);
```

## 主なユースケース

- **建設ドキュメント** – 特定のフロアプランセクションの印刷可能な PDF を生成します。  
- **BIM コーディネーション** – 衝突検出のために関心領域のみをエクスポートします。  
- **クライアント向けプレゼンテーション** – 全体図を公開せず、選択した部屋や立面のクリーンな PDF を提供します。

## 結論

おめでとうございます！正確な座標で **DWG を PDF に変換** に成功し、Aspose.CAD for .NET を使用した **ビュー ポートの設定方法** を学びました。この **dwg to pdf tutorial** は、**dwg から pdf を作成** し、**dwg を pdf c# としてエクスポート** する方法を示しながら、出力領域を完全にコントロールできることを実証しています。

## FAQ

### Q1: Aspose.CAD を他の CAD ファイル形式でも使用できますか？

A1: はい、Aspose.CAD は DWG、DXF、DWF などのさまざまな CAD 形式をサポートしています。

### Q2: 変換プロセス中のエラーはどのように処理できますか？

A2: try‑catch ブロックを使用して例外を捕捉・管理するエラーハンドリング機構を実装してください。

### Q3: Aspose.CAD は Windows と Linux の両環境に適していますか？

A3: はい、Aspose.CAD は Windows と Linux の両プラットフォームで動作します。

### Q4: PDF の出力をさらにカスタマイズできますか？

A4: もちろんです！Aspose.CAD が提供する豊富なオプションを調査し、PDF 出力を特定の要件に合わせて調整してください。

### Q5: 追加のサポートやコミュニティディスカッションはどこで見つけられますか？

A5: コミュニティサポートやディスカッションは [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) をご覧ください。

## 追加のよくある質問

**Q: このアプローチは大容量の DWG ファイル（数百 MB）でも機能しますか？**  
A: はい。ラスタライズはページ単位で実行され、`rasterizationOptions`（例: `Resolution`）を調整して品質とメモリ使用量のバランスを取ることができます。

**Q: 複数のビュー ポートを別々の PDF ページにエクスポートできますか？**  
A: `cadImage.ViewPorts` をループし、各ビュー ポートをアクティブに設定して `Save` を各ページで呼び出し、最後に Aspose.PDF を使用して PDF を結合できます。

**Q: 生成された PDF に透かしを追加できますか？**  
A: PDF を保存した後、Aspose.PDF で再度開き、テキストまたは画像の透かしを適用してユーザーに提供する前に追加できます。

---

**Last Updated:** 2026-04-03  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}