---
date: 2026-06-19
description: Aspose.CAD for Java を使用して DGN ファイルを PDF に簡単に変換します。ステップバイステップのガイドに従って
  DGN を PDF にエクスポートし、CAD を PDF として保存し、ワークフローを効率化しましょう。
keywords:
- convert dgn to pdf
- save cad as pdf
- export dgn to pdf
linktitle: DGN V7 のサポート
schemas:
- author: Aspose
  dateModified: '2026-06-19'
  description: Effortlessly convert DGN files to PDF using Aspose.CAD for Java. Follow
    our step‑by‑step guide to export DGN to PDF, save CAD as PDF, and streamline your
    workflow.
  headline: Convert DGN to PDF with Aspose.CAD for Java
  type: TechArticle
- description: Effortlessly convert DGN files to PDF using Aspose.CAD for Java. Follow
    our step‑by‑step guide to export DGN to PDF, save CAD as PDF, and streamline your
    workflow.
  name: Convert DGN to PDF with Aspose.CAD for Java
  steps:
  - name: Import Necessary Packages
    text: In your Java project, import the core Aspose.CAD classes that enable file
      loading and export.
  - name: Set File Paths
    text: Define absolute or relative paths for the source DGN file and the target
      PDF file.
  - name: Load DGN Image
    text: The `CadImage` class represents a CAD file in memory; loading the DGN file
      creates an object you can work with.
  - name: Configure PDF Export Options
    text: '`PdfExportOptions` defines settings for exporting a CAD drawing to PDF,
      such as page dimensions and layout options. Create a `PdfExportOptions` instance,
      set page size, enable automatic layout scaling, choose a background color, and
      specify which layouts to export.'
  - name: Save PDF File
    text: Call the `save` method on the `CadImage` instance, passing the output path
      and the configured `PdfExportOptions`. Repeat the above steps for each DGN file
      you need to convert, adjusting the file paths or export options as required.
  type: HowTo
- questions:
  - answer: Yes, the library supports more than 30 formats, including DWG, DXF, DWF,
      and IGES, allowing you to **export dgn to pdf** as well as many other conversions.
    question: Can I use Aspose.CAD for Java with other CAD file formats?
  - answer: Yes, you can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/)
      for evaluation purposes.
    question: Is a temporary license available for testing?
  - answer: Refer to the [Aspose.CAD for Java documentation](https://reference.aspose.com/cad/java/)
      for full method signatures and usage examples.
    question: Where can I find detailed API documentation?
  - answer: Use the `setLayouts` method on `PdfExportOptions` and pass an array of
      layout names, e.g., `new String[] {"Model", "Layout1"}`.
    question: How do I specify which layouts to export?
  - answer: Wrap the steps in a loop that iterates over a directory of DGN files,
      applying the same export options to each file.
    question: What if I need to batch‑convert many DGN files?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java を使用して DGN を PDF に変換
url: /ja/java/other-cad-operations/support-for-dgn-v7/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java を使用した DGN から PDF への変換

モダンな CAD 環境では、**DGN を PDF に変換**する能力が迅速かつ信頼できることが、非 CAD 関係者と設計を共有するために不可欠です。Aspose.CAD for Java は、外部依存関係なしで高品質な PDF ドキュメントに DGN ファイルをエクスポートできる純粋な Java API を提供します。このチュートリアルでは、ライブラリのセットアップから PDF エクスポートオプションの微調整まで、プロセス全体を順を追って説明し、Java アプリケーションに自信を持って変換機能を統合できるようにします。

## クイック回答

- **DGN 変換を処理するライブラリは何ですか？** Aspose.CAD for Java.
- **複数のレイアウトをエクスポートできますか？** はい、エクスポートオプションで layouts 配列を指定してください。
- **本番環境でライセンスが必要ですか？** 無制限に使用するには有効な Aspose.CAD ライセンスが必要です。
- **サポートされている Java バージョンはどれですか？** Java 8 以降。
- **変換はロスレスですか？** PDF はベクターグラフィック、レイヤー、テキストの忠実度を保持します。

## DGN を PDF に変換するとは何ですか？

DGN を PDF に変換するとは、DGN（MicroStation）設計ファイルを Portable Document Format（PDF）に変換し、閲覧、印刷、配布を容易にするプロセスです。Aspose.CAD for Java はネイティブな DGN 構造を読み取り、各レイアウトをベクターグラフィックとしてレンダリングし、ジオメトリとテキストの精度を保持しながら PDF ファイルに書き出します。

## なぜ Aspose.CAD for Java を使用して CAD を PDF として保存するのですか？

Aspose.CAD は 30 以上の CAD フォーマットに対して **CAD を PDF として保存**でき、ドキュメント全体をメモリにロードせずに最大 2 GB のファイルを処理し、一般的なサーバーハードウェア上で競合ライブラリの最大 5 倍の速度で変換します。API はネイティブバイナリを必要とせず、クラウドやコンテナ環境へのデプロイがシームレスです。

## 前提条件

- **Aspose.CAD for Java ライブラリ** – [Aspose.CAD for Java ダウンロードページ](https://releases.aspose.com/cad/java/) からダウンロードしてください。
- **Java 開発環境** – JDK 8 以上がインストールされ、マシンに設定されていること。
- 本番使用のための有効な **Aspose.CAD ライセンス**（評価用に一時ライセンスが利用可能）。

コミュニティサポートは、[Aspose.CAD フォーラム](https://forum.aspose.com/c/cad/19) をご覧ください。

## dgn を pdf にエクスポートする手順

DGN ファイルを読み込み、PDF エクスポートオプションを構成し、数行のコードで結果を保存します。以下の手順は必要なシーケンスを示し、各ステップには Aspose.CAD ドキュメントから実際の実装に置き換える短いコードプレースホルダーが含まれています。

### ステップ 1: 必要なパッケージをインポート

Java プロジェクトで、ファイルの読み込みとエクスポートを可能にするコア Aspose.CAD クラスをインポートします。  
```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.cadobjects.DgnImage;
import com.aspose.cad.imageoptions.PdfOptions;
import java.awt.Color;
```

### ステップ 2: ファイルパスを設定

ソース DGN ファイルとターゲット PDF ファイルの絶対パスまたは相対パスを定義します。  
```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

### ステップ 3: DGN イメージをロード

`CadImage` クラスはメモリ内の CAD ファイルを表します。DGN ファイルをロードすると、操作可能なオブジェクトが作成されます。  
```java
DgnImage objImage = (DgnImage)Image.load(fileName);
```

### ステップ 4: PDF エクスポートオプションを構成

`PdfExportOptions` はページサイズやレイアウトオプションなど、CAD 図面を PDF にエクスポートするための設定を定義します。  
`PdfExportOptions` のインスタンスを作成し、ページサイズを設定し、自動レイアウトスケーリングを有効にし、背景色を選択し、エクスポートするレイアウトを指定します。  
```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setBackgroundColor(Color.getBlack());
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); //only export 4 (1,2,3 and 9) views
options.setVectorRasterizationOptions(vectorOptions);
```

### ステップ 5: PDF ファイルを保存

`CadImage` インスタンスの `save` メソッドを呼び出し、出力パスと構成した `PdfExportOptions` を渡します。  
```java
objImage.save(outFile, options);
```

必要に応じてファイルパスやエクスポートオプションを調整しながら、変換が必要な各 DGN ファイルについて上記の手順を繰り返してください。

## 一般的な問題と解決策

- **レイアウトが見つからない** – `setLayouts` に渡すレイアウト名がソース DGN ファイル内の名前と完全に一致していることを確認してください。レイアウト名は大文字小文字を区別します。
- **メモリ不足エラー** – 非常に大きな図面の場合、`PdfExportOptions.setUseMemoryCache(true)` を設定してストリーミングを有効にしてください。
- **色が正しくない** – 背景色が `Color.WHITE`（または希望の色）に設定されていることを確認し、PDF の予期しない暗い背景を防いでください。

## よくある質問

**Q: Aspose.CAD for Java を他の CAD ファイル形式と併用できますか？**  
A: はい、DWG、DXF、DWF、IGES など 30 以上の形式をサポートしており、**DGN を PDF に変換**はもちろん、他の多くの変換も可能です。

**Q: テスト用に一時ライセンスは利用できますか？**  
A: はい、評価目的で一時ライセンスを[こちら](https://purchase.aspose.com/temporary-license/)から取得できます。

**Q: 詳細な API ドキュメントはどこで確認できますか？**  
A: 完全なメソッドシグネチャと使用例については、[Aspose.CAD for Java ドキュメント](https://reference.aspose.com/cad/java/)をご参照ください。

**Q: エクスポートするレイアウトはどのように指定しますか？**  
A: `PdfExportOptions` の `setLayouts` メソッドを使用し、レイアウト名の配列（例: `new String[] {"Model", "Layout1"}`）を渡します。

**Q: 多数の DGN ファイルをバッチ変換したい場合は？**  
A: 手順をループでラップし、DGN ファイルが格納されたディレクトリを走査して各ファイルに同じエクスポートオプションを適用します。

---

**最終更新日:** 2026-06-19  
**テスト環境:** Aspose.CAD for Java 24.10  
**作者:** Aspose  

{{< blocks/products/products-backtop-button >}}

## 関連チュートリアル

- [DWG を PDF にエクスポートし CAD 図面を変換 – Aspose.CAD Java チュートリアル](/cad/java/cad-drawing-conversion/)
- [dwg to pdf java – Aspose.CAD を使用した CAD の PDF へのエクスポート](/cad/java/cad-export-options/export-to-pdf/)
- [Aspose.CAD for Java を使用した CAD レイアウトの PDF エクスポート](/cad/java/cad-export-options/export-cad-layouts-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}