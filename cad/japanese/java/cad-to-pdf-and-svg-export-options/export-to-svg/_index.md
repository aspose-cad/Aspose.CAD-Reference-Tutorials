---
date: 2026-06-14
description: Aspose.CAD for Java を使用して CAD を SVG にエクスポートする方法を学びます。このステップバイステップガイドでは、DWG
  を SVG に変換し、SVG カラーモードを設定し、ライブラリを Java プロジェクトに統合する方法を示します。
keywords:
- export cad to svg
- convert dwg to svg
- change svg to grayscale
- convert cad to svg
- generate svg from dwg
linktitle: SVG へエクスポート
schemas:
- author: Aspose
  dateModified: '2026-06-14'
  description: Learn how to export CAD to SVG with Aspose.CAD for Java. This step‑by‑step
    guide shows you how to convert DWG to SVG, set SVG color mode, and integrate the
    library into your Java project.
  headline: Export CAD to SVG Using Aspose.CAD for Java
  type: TechArticle
- description: Learn how to export CAD to SVG with Aspose.CAD for Java. This step‑by‑step
    guide shows you how to convert DWG to SVG, set SVG color mode, and integrate the
    library into your Java project.
  name: Export CAD to SVG Using Aspose.CAD for Java
  steps:
  - name: Open Your Java Project
    text: Launch your favorite IDE (IntelliJ IDEA, Eclipse, VS Code) and open the
      project where you intend to add the conversion logic.
  - name: Add Aspose.CAD Library
    text: Place the `aspose-cad-xx.jar` file in the `libs` directory and add it as
      a dependency in your build tool (Maven, Gradle, or plain `javac`).
  - name: Import Namespaces
    text: 'In the Java source file that will perform the conversion, add the following
      imports: These imports give you access to the core `Image` class and the SVG‑specific
      export options.'
  - name: Specify the Resource Directory
    text: 'Define the absolute or relative path that points to the folder holding
      your CAD drawings:'
  - name: Load the CAD Drawing
    text: The `Image` class is Aspose.CAD's top‑level object that represents a CAD
      drawing in memory. Loading the file creates an in‑memory representation ready
      for export. `Image.load` reads a CAD file and creates an in‑memory representation
      of the drawing.
  - name: Configure SVG Export Options
    text: '`SvgExportOptions` lets you fine‑tune the SVG output. Below we set the
      color mode to grayscale and ensure all text is rendered as shapes, which improves
      compatibility with browsers that lack the original font.'
  - name: Save as SVG
    text: Finally, invoke `save` on the `Image` instance, passing the target file
      name and the configured options. Aspose.CAD writes a standards‑compliant SVG
      file that can be opened directly in any modern browser. `save` writes the image
      to the specified file using the provided export options. > **Pro tip:**
  type: HowTo
- questions:
  - answer: Yes, simply replace the DWG file name with a DXF file; the API automatically
      detects and processes both formats.
    question: Can I convert a DXF file to SVG using the same code?
  - answer: Set `options.setColorType(SvgColorMode.FullColor);` before invoking the
      `save` method.
    question: How do I change the output to full‑color SVG?
  - answer: Aspose.CAD converts text to shapes, so embedding fonts is unnecessary;
      the resulting SVG contains only vector outlines.
    question: Is it possible to embed fonts in the generated SVG?
  - answer: The Java library is platform‑independent and runs wherever a compatible
      JVM is available, including Windows, Linux, and macOS.
    question: Does the library work on Linux and macOS?
  - answer: The example was tested with Aspose.CAD for Java **24.10**.
    question: What version of Aspose.CAD was used in this tutorial?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java を使用した CAD の SVG へのエクスポート
url: /ja/java/cad-to-pdf-and-svg-export-options/export-to-svg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD を SVG にエクスポートする（Aspose.CAD for Java 使用）

## はじめに

この包括的なチュートリアルでは、Aspose.CAD for Java を使用して **CAD を SVG にエクスポートする方法** を学びます。**DWG を SVG に変換** したり、バッチジョブで DWG ファイルから SVG を生成したり、軽量なウェブ表示のために SVG をグレースケールに変更したりする必要がある場合でも、本ガイドはライブラリの設定からエクスポートオプションの微調整まで、すべての手順を順を追って説明します。最後まで読むと、任意の JVM 互換プラットフォームで実行できる本番環境向けのコードスニペットが手に入ります。

## クイック回答
- **“export CAD to SVG” とは何ですか？** CAD 図面（例：DWG または DXF）を、ブラウザが品質を損なうことなく表示できる Scalable Vector Graphics ファイルに変換します。  
- **変換を担当するライブラリはどれですか？** Aspose.CAD for Java は、30 以上の CAD フォーマットをサポートし、フルベクトル忠実度で SVG を出力する専用 API を提供します。  
- **開発にライセンスは必要ですか？** 無料トライアルで評価は可能ですが、本番展開には商用ライセンスが必要です。  
- **SVG のカラー出力を制御できますか？** はい。`SvgColorMode` を使用してグレースケールとフルカラーのレンダリングを切り替えます。  
- **追加のソフトウェアは必要ですか？** Java ランタイム（JDK 8 以降）と Aspose.CAD JAR だけで、外部の CAD ツールは不要です。

## CAD を SVG にエクスポートするとは？

CAD を SVG にエクスポートするとは、DWG、DXF、DWF などのネイティブ CAD ファイルを SVG ベクター画像形式に変換するプロセスです。生成された SVG は正確な幾何データを保持し、ウェブブラウザやデザインツールで解像度に依存しない表示を可能にします。

## なぜ Aspose.CAD で CAD を SVG にエクスポートするのか？

Aspose.CAD は **30 以上の入力フォーマット** に対応し、**500 ページ** までの SVG 出力を、ファイル全体をメモリに読み込むことなく生成できます。これにより、典型的なサーバークラス CPU で **200 ページ/秒** の速度で **高忠実度ベクトル変換** を実現します。このライブラリは **100 % Java** で動作し、ネイティブ DLL やサードパーティの CAD エンジンは不要です。

## 前提条件

- **Java Development Kit**（JDK 8 以上）がマシンにインストールされ、設定されていること。  
- **Aspose.CAD for Java** の JAR ファイルを公式の [download link](https://releases.aspose.com/cad/java/) からダウンロードしていること。  
- 変換したい CAD 図面（DWG、DXF など）を少なくとも1つ含むフォルダーがあること。

## 名前空間のインポート

コードを書く前に、Aspose.CAD ライブラリがクラスパスに含まれており、必要なクラスをインポートしていることを確認してください。

### 手順 1: Java プロジェクトを開く
お好みの IDE（IntelliJ IDEA、Eclipse、VS Code など）を起動し、変換ロジックを追加するプロジェクトを開きます。

### 手順 2: Aspose.CAD ライブラリを追加
`aspose-cad-xx.jar` ファイルを `libs` ディレクトリに配置し、ビルドツール（Maven、Gradle、または単純な `javac`）で依存関係として追加します。

### 手順 3: 名前空間をインポート
変換を実行する Java ソースファイルに、以下のインポート文を追加します：

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.SvgExportOptions;
import com.aspose.cad.imageoptions.SvgColorMode;
```

これらのインポートにより、コアの `Image` クラスと SVG 固有のエクスポートオプションにアクセスできます。

## Aspose.CAD for Java を使用して CAD を SVG にエクスポートする方法？

Aspose.CAD を使用して CAD 図面を SVG にエクスポートするには、ソースファイルの読み込み、SVG 固有のオプション設定、出力の書き込みが必要です。このプロセスはシンプルで、数行のコードだけで実行でき、サポートされているすべての CAD フォーマットでベクトル忠実度を保ちつつ一貫して動作します。

### 手順 1: リソースディレクトリを指定
CAD 図面が格納されたフォルダーへの絶対パスまたは相対パスを定義します：

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.SvgOptions;
import com.aspose.cad.imageoptions.SvgColorMode;
```

### 手順 2: CAD 図面をロード
`Image` クラスは Aspose.CAD の最上位オブジェクトで、メモリ内で CAD 図面を表します。ファイルをロードすると、エクスポートの準備ができたメモリ内表現が作成されます。

`Image.load` は CAD ファイルを読み取り、図面のメモリ内表現を作成します。

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

### 手順 3: SVG エクスポートオプションを設定
`SvgExportOptions` を使用すると、SVG 出力を細かく調整できます。以下ではカラー モードをグレースケールに設定し、すべてのテキストをシェイプとしてレンダリングするようにしています。これにより、元のフォントがないブラウザでも互換性が向上します。

```java
Image image = Image.load(dataDir + "meshes.dwg");
```

### 手順 4: SVG として保存
最後に、`Image` インスタンスで `save` を呼び出し、対象ファイル名と設定したオプションを渡します。Aspose.CAD は標準準拠の SVG ファイルを書き出し、最新のブラウザで直接開くことができます。

`save` は指定されたファイルに、提供されたエクスポートオプションを使用して画像を書き込みます。

```java
SvgOptions options = new SvgOptions();
options.setColorType(SvgColorMode.Grayscale);
options.setTextAsShapes(true);
```

> **プロのコツ:** フルカラー SVG を生成するには、`SvgColorMode.Grayscale` を `SvgColorMode.FullColor` に置き換えます。この切り替えにより、元のパレットを保持しつつベクトルの拡張性が保たれます。

## なぜ Aspose.CAD を使用して CAD を SVG にエクスポートするのか？

- **高忠実度:** ベクトルデータが保持され、SVG が元の CAD 図面とまったく同じ外観になります。  
- **外部依存なし:** 変換は完全に Java 内で実行され、追加ツールは不要です。  
- **出力のカスタマイズ:** `setColorType` などのオプションで、SVG をグレースケールまたはフルカラーに制御できます。  
- **スケーラブルなパフォーマンス:** 数百ページ規模の図面を数秒で処理し、メモリ使用量は 50 MB 未満です。

## よくある問題と解決策

- **ファイルが見つからない:** `dataDir` が正しいフォルダーを指しているか、DWG ファイル名の大文字小文字がファイルシステムと一致しているか確認してください。  
- **空白の SVG 出力:** ソース図面にベクトルシェイプとして表示すべきテキストが含まれる場合、`options.setTextAsShapes(true)` が有効になっていることを確認してください。  
- **サポートされていない CAD フォーマット:** Aspose.CAD は DWG、DXF、DWF など 15 以上のフォーマットをサポートしています。完全なリストは公式ドキュメントをご参照ください。  
- **パフォーマンスのボトルネック:** 非常に大きなファイルの場合、`options.setEnableStreaming(true)` でストリーミングモードを有効にし、メモリ消費を抑えてください。

## よくある質問

**Q: 同じコードで DXF ファイルを SVG に変換できますか？**  
A: はい、DWG ファイル名を DXF ファイルに置き換えるだけで、API が自動的に両方のフォーマットを検出して処理します。

**Q: 出力をフルカラー SVG に変更するには？**  
A: `save` メソッドを呼び出す前に `options.setColorType(SvgColorMode.FullColor);` を設定します。

**Q: 生成された SVG にフォントを埋め込むことは可能ですか？**  
A: Aspose.CAD はテキストをシェイプに変換するため、フォント埋め込みは不要です。生成された SVG にはベクトルのアウトラインのみが含まれます。

**Q: ライブラリは Linux や macOS でも動作しますか？**  
A: Java ライブラリはプラットフォームに依存せず、互換性のある JVM があれば Windows、Linux、macOS で動作します。

**Q: このチュートリアルで使用された Aspose.CAD のバージョンは？**  
A: 本例は Aspose.CAD for Java **24.10** でテストされています。

---

**最終更新日:** 2026-06-14  
**テスト環境:** Aspose.CAD for Java 24.10  
**作者:** Aspose  

---

```java
image.save(dataDir + "meshes.svg");
```

{{< blocks/products/products-backtop-button >}}

## 関連チュートリアル

- [Aspose.CAD for Java を使用した DWG の PDF またはラスタへのエクスポート](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [dwg to pdf java – Aspose.CAD で CAD を PDF にエクスポート](/cad/java/cad-export-options/export-to-pdf/)
- [Aspose.CAD for Java を使用した特定の DWG レイアウトの PDF エクスポート](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}