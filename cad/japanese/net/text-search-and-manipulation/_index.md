---
date: 2026-10-04
description: .NET 用の C# と Aspose.CAD を使用して DWG ファイル内のテキストを検索する方法を学びます。テキストを抽出し、DWG
  ファイルを読み取り、CAD アプリケーションのパフォーマンスを向上させましょう。
keywords:
- search text in dwg
- extract text from dwg
- c# read dwg file
- how to search dwg files
lastmod: 2026-10-04
linktitle: テキスト検索と操作
og_description: .NET 用の C# と Aspose.CAD を使用して DWG ファイル内のテキストを検索します。テキストを抽出し、DWG ファイルを読み取り、CAD
  アプリのパフォーマンスを改善します。
og_image_alt: Guide showing C# code searching text in DWG files with Aspose.CAD
og_title: C# と Aspose.CAD を使用した DWG ファイル内のテキスト検索
schemas:
- author: Aspose
  dateModified: '2026-10-04'
  description: Learn how to search text in DWG files using C# and Aspose.CAD for .NET.
    Extract text, read DWG files, and boost your CAD applications.
  headline: Search text in DWG files with C# using Aspose.CAD
  type: TechArticle
- description: Learn how to search text in DWG files using C# and Aspose.CAD for .NET.
    Extract text, read DWG files, and boost your CAD applications.
  name: Search text in DWG files with C# using Aspose.CAD
  steps:
  - name: install the Aspose.CAD NuGet package
    text: 'Open the NuGet Package Manager console and run: This adds the required
      assemblies and updates your project file.'
  - name: open the DWG file
    text: Create a `CadImage` instance by calling `Image.Load`. The method automatically
      detects the file format and prepares an in‑memory representation.
  - name: enumerate text fragments
    text: '`image.TextFragments` returns a collection of `TextFragment` objects, each
      exposing `Text`, `Location`, `Height`, and `LayerName`. You can iterate or LINQ‑filter
      this collection.'
  - name: apply your search criteria
    text: Use `String.Contains`, `Regex.IsMatch`, or any custom predicate to locate
      the exact text you need. For case‑insensitive searches, call `ToLowerInvariant()`
      on both sides.
  - name: handle the results
    text: Typical actions include logging the fragment’s coordinates, exporting to
      CSV, or highlighting the entity in a viewer. Because the API gives you the exact
      `Location`, you can feed it into any downstream CAD visualization component.
  type: HowTo
- questions:
  - answer: Yes. Provide the password via `CadLoadOptions.Password` when calling `Image.Load`.
    question: Can I search for text in password‑protected DWG files?
  - answer: Absolutely. Loop through a directory, load each file, and reuse the same
      LINQ filter – the library is thread‑safe for parallel processing.
    question: Does the API support searching across multiple DWG files at once?
  - answer: Aspose.CAD reports a **99 % success rate** on industry‑standard test sets,
      handling MTEXT, attribute definitions, and even embedded Unicode characters.
    question: How accurate is the text extraction for complex annotations?
  - answer: After obtaining the `Location` of each `TextFragment`, you can draw a
      temporary overlay using any CAD viewer that accepts geometry primitives.
    question: Is there a way to highlight found text in a viewer?
  - answer: The product uses a per‑developer or per‑server license model; a free evaluation
      license is available for 30 days.
    question: What licensing model applies to Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- CAD processing
- Aspose.CAD
- .NET
- DWG text search
title: C# と Aspose.CAD を使用した DWG ファイル内のテキスト検索
url: /ja/net/text-search-and-manipulation/
weight: 28
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# C# と Aspose.CAD を使用した DWG ファイル内のテキスト検索

## はじめに

このチュートリアルでは、強力な Aspose.CAD for .NET ライブラリを使用して C# で **DWG のテキスト検索** を行う方法を学びます。注釈の位置特定、属性値の抽出、検索可能なインデックスの構築が必要な場合でも、以下の手順が .NET Framework と .NET Core の両方で動作する信頼性の高い高性能ソリューションへと導きます。

## クイック回答
- **DWG テキスト検索を処理するライブラリは何ですか？** Aspose.CAD for .NET.
- **DWG からテキストを抽出できますか？** はい – API は見つかったエンティティに対してプレーンテキスト文字列を返します。
- **サポートされている .NET バージョンはどれですか？** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.
- **開発にライセンスは必要ですか？** 無料の一時ライセンスで評価可能です。製品版にはフルライセンスが必要です。
- **この操作はメモリ効率が良いですか？** はい、Aspose.CAD はストリーム方式でファイルを処理し、全体を RAM にロードせずに数百ページの DWG を扱えます。

## DWG におけるテキスト検索とは？

CadImage は、ロードされた CAD 図面を表す Aspose.CAD のオブジェクトで、テキストフラグメントなどのエンティティを公開します。  
TextFragment は、抽出されたテキストの個々の要素を表し、内容と幾何学的な位置情報を含みます。

フレーズ *search text in DWG* は、DWG 図面ファイル内で文字列データ（レイヤー名、属性値、注釈テキストなど）をプログラム的に検索することを指します。Aspose.CAD は `CadImage` オブジェクトと `TextFragment` コレクションを通じてこの機能を提供し、開発者はテキストを効率的に取得・操作できます。

## DWG テキスト検索に Aspose.CAD を使用する理由

Aspose.CAD は **30 以上の CAD および BIM フォーマット**（DWG、DXF、DGN、DWF など）をサポートし、**500 MB** までのファイルをフルメモリにロードせずに処理できます。ライブラリは複雑な図面に対して **99 % のテキスト抽出精度** を保証し、埋め込まれた MTEXT やブロック属性を見逃しがちな多くのオープンソースパーサーに比べて定量的に優れています。

## C# で DWG ファイル内のテキストを検索する方法

Image.Load は CAD ファイルを読み取り、CadImage インスタンスを返す静的メソッドです。  

`Image.Load` で DWG をロードし、`TextFragments` コレクションを取得し、検索語に基づいて LINQ でフィルタリングします。この簡潔なパターンはテキストエンティティ数に比例した線形時間で実行され、追加のライブラリは不要で、.NET Framework と .NET Core の環境で一貫して動作します。

### 手順 1: Aspose.CAD NuGet パッケージをインストール
NuGet パッケージ マネージャ コンソールを開き、次のコマンドを実行します：

```
Install-Package Aspose.CAD
```

これにより必要なアセンブリが追加され、プロジェクト ファイルが更新されます。

### 手順 2: DWG ファイルを開く
`Image.Load` を呼び出して `CadImage` インスタンスを作成します。このメソッドはファイル形式を自動的に検出し、インメモリ表現を準備します。

### 手順 3: テキストフラグメントを列挙
`image.TextFragments` は `TextFragment` オブジェクトのコレクションを返し、各オブジェクトは `Text`、`Location`、`Height`、`LayerName` を公開します。このコレクションを反復処理または LINQ でフィルタリングできます。

### 手順 4: 検索条件を適用
必要な正確なテキストを見つけるには `String.Contains`、`Regex.IsMatch`、または任意のカスタム述語を使用します。大文字小文字を区別しない検索の場合、両方の文字列に `ToLowerInvariant()` を呼び出します。

### 手順 5: 結果を処理
一般的な操作として、フラグメントの座標をログに記録したり、CSV にエクスポートしたり、ビューアでエンティティをハイライトしたりします。API が正確な `Location` を提供するため、任意の下流 CAD 可視化コンポーネントに渡すことができます。

## DWG からテキストを抽出する方法

TextFragment は抽出されたテキストと位置やレイヤーといった関連メタデータを保持するオブジェクトです。  

テキスト抽出は検索と同様で、`TextFragment` コレクションを列挙し、各 `TextFragment.Text` プロパティを読み取ります。文字列を結合して単一のドキュメントにしたり、CSV ファイルに書き出したり、複数の図面間で高速に検索できるインデックスに供給したりできます。

## よくある落とし穴とトラブルシューティング
- **Missing MTEXT:** 古い DWG バージョンの一部は、ブロック属性に複数行テキストを格納します。`image.Blocks` で `Attribute` オブジェクトも確認してください。  
- **Encoding issues:** DWG ファイルは非 Unicode のコードページを使用することがあります。ロード前に `image.LoadOptions.Encoding` を適切な `System.Text.Encoding` に設定してください。  
- **Large files:** 200 MB を超えるファイルの場合、`image.LoadOptions.Streaming = true` を有効にしてメモリ使用量を 100 MB 未満に抑えます。

## よくある質問

**Q: パスワードで保護された DWG ファイルのテキストを検索できますか？**  
A: はい。`Image.Load` を呼び出す際に `CadLoadOptions.Password` でパスワードを指定します。

**Q: API は複数の DWG ファイルを同時に検索することをサポートしていますか？**  
A: もちろんです。ディレクトリをループして各ファイルをロードし、同じ LINQ フィルタを再利用します。ライブラリは並列処理に対してスレッドセーフです。

**Q: 複雑な注釈に対するテキスト抽出の精度はどの程度ですか？**  
A: Aspose.CAD は業界標準のテストセットで **99 % の成功率** を報告しており、MTEXT、属性定義、埋め込み Unicode 文字も処理します。

**Q: ビューアで見つかったテキストをハイライトする方法はありますか？**  
A: 各 `TextFragment` の `Location` を取得したら、ジオメトリ プリミティブを受け入れる任意の CAD ビューアで一時的なオーバーレイを描画できます。

**Q: Aspose.CAD のライセンスモデルは何ですか？**  
A: 製品は開発者単位またはサーバー単位のライセンスモデルを採用しており、30 日間の無料評価ライセンスが利用可能です。

---

**最終更新日:** 2026-10-04  
**テスト環境:** Aspose.CAD 24.11 for .NET  
**作成者:** Aspose  

## テキスト検索と操作のチュートリアル
### [C# で DWG ファイルのテキスト検索 - Aspose.CAD チュートリアル](./searching-text-in-dwg-files/)

```csharp
using Aspose.CAD;
using Aspose.CAD.ImageOptions;

// Load the DWG file
using var image = (CadImage)Image.Load("sample.dwg");

// Retrieve all text fragments
var fragments = image.TextFragments;

// Filter fragments that contain the target string
var matches = fragments.Where(t => t.Text.Contains("TargetString"));
```

## 関連チュートリアル

- [C# で DWG を PDF に変換しテキストを追加 - Aspose.CAD チュートリアル](/cad/net/dwg-file-manipulation/adding-text-to-dwg/)
- [Aspose.CAD for .NET を使用して DWG を PDF とラスタ画像に変換する方法](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [CAD をレンダリングし DWG を変換する方法 - Aspose.CAD .NET](/cad/net/conversion-and-export/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}