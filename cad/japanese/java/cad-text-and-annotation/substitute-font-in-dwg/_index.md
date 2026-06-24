---
date: 2026-05-04
description: Aspose.CAD を使用して Java で dxf を dwg に変換し、プライマリフォントを設定する方法を学びましょう。完璧な CAD
  ビジュアルのためのステップバイステップガイド。
keywords:
- convert dxf to dwg
- set primary font
- change dwg text style
- how to substitute font
- aspose cad licensing
linktitle: DWGのフォント置換
second_title: Aspose.CAD Java API
title: DXF を DWG に変換し、DWG のフォントを変更する Aspose.CAD Java
url: /ja/java/cad-text-and-annotation/substitute-font-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG ファイルを Java で読み込み、Aspose.CAD でフォントを置換する方法

## はじめに

Java アプリケーションで **convert dxf to dwg** が必要で、図面に洗練された外観を与えたい場合、フォントの置換はすぐに効果が得られます。Aspose.CAD for Java を使用すれば、デフォルトのテキストスタイルを任意のシステムにインストールされたフォントに置き換えることができ、すべての注釈が期待通りに表示されます。このチュートリアルでは、Java で DWG ファイルを読み込むところから `setPrimaryFontName` メソッドを使用してフォントを変更するまでの全工程を解説します。

## クイック回答
- **どのライブラリが必要ですか？** Aspose.CAD for Java.  
- **Java で DWG ファイルを読み込めますか？** Yes, simply call `Image.load()` on the DWG path.  
- **どのメソッドがフォントを変更しますか？** `setPrimaryFontName`.  
- **本番環境でライセンスが必要ですか？** Yes, a commercial license is required.  
- **バッチ処理は可能ですか？** Absolutely – loop through multiple files with the same code.

## **convert dxf to dwg** とは何ですか？

「convert dxf to dwg」は、DXF（Drawing Exchange Format）ファイルを多くの CAD アプリケーションで使用されるネイティブな DWG 形式に変換することを指します。変換することで、広くサポートされた DXF 図面を DWG ワークフローに取り込み、そして Aspose.CAD を使用してフォント置換などの高度なスタイリングを適用できます。

## DWG ファイルでフォントを置換する理由は？

- **一貫性:** すべての共同作業者がローカルのフォント設定に関係なく同じ書体を見ることが保証されます。  
- **可読性:** デフォルトの CAD フォントは画面上で読みづらいことがあり、Arial のようなクリーンなフォントに切り替えると視認性が向上します。  
- **ブランディング:** 技術図面を企業のスタイルガイドに合わせることができます。  

## 一般的な使用例

| シナリオ | 重要な理由 |
|----------|----------------|
| **レガシー DXF 図面のバッチ変換** | これらを DWG に変換し、1 回の処理で企業フォントを適用できます。 |
| **クライアント向けプレゼンテーション用図面の準備** | 一貫した読みやすいフォントにより、文書がプロフェッショナルに見えます。 |
| **自動化 CAD パイプライン** | フォント置換を組み込むことで、手動の後処理工程が不要になります。 |

## 前提条件

- **Java Development Kit (JDK)** – any recent version (8+ recommended).  
- **Aspose.CAD for Java** – download from the [website](https://releases.aspose.com/cad/java/).  
- **サンプル DWG/DXF ファイル** – a drawing you want to modify (you can use any DWG or DXF file for testing).

## 名前空間のインポート

Java プロジェクトで Aspose.CAD を使用するために必要なクラスをインポートします。これらのインポートにより、画像の読み込み、CAD 固有のオブジェクト、スタイル操作にアクセスできます。

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject;
```

## フォント置換のステップバイステップガイド

### 手順 1: DWG ファイルを読み込む (load dwg file java)

まず、API に DWG（または DXF）ファイルの場所を指定し、`CadImage` オブジェクトにロードします。

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage) Image.load(srcFile);
```

> **Pro tip:** If you work with DWG files directly, replace the `.dxf` extension with `.dwg` in the `srcFile` variable.

### 手順 2: スタイルテーブルを反復し、primary font name を設定する

各 CAD 図面にはスタイルオブジェクトのコレクションが含まれています。これらをループし、`setPrimaryFontName` メソッド（**primary font name を設定する** API 呼び出し）を使用してフォントを置換します。

```java
for(Object style : cadImage.getStyles())
{
    // Set the font name
    ((com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject)style).setPrimaryFontName("Arial");
}
```

コードを実行しているマシンにインストールされている任意のフォントに、`"Arial"` を変更できます。

### 手順 3: 変更した図面を保存する

フォントを更新したら、変更を新しい DWG ファイルに書き戻す（または元のファイルを上書きする）ことで保存します。

```java
cadImage.save(dataDir + "output.dwg", new DwgOptions());
```

保存されたファイルは指定したフォントを使用し、すべてのテキスト注釈がその書体でレンダリングされます。

## よくある問題と解決策

| 問題 | 解決策 |
|-------|----------|
| **フォントが適用されない** | フォントがホスト OS にインストールされているか、スペルが完全に一致しているかを確認してください。 |
| **`Image.load` が例外をスローする** | ファイルパスが正しいこと、そしてファイルがサポートされている DWG/DXF 形式であることを確認してください。 |
| **大きなファイルでのパフォーマンス低下** | 別スレッドで処理するか、バッチ処理して UI のブロックを回避してください。 |

## よくある質問

**Q: Does the `setPrimaryFontName` method affect only text entities?**  
A: It updates the primary font for the style table, which in turn influences all text objects that reference that style.

**Q: Can I use a custom font that is not installed on the system?**  
A: Aspose.CAD relies on the operating system’s font registry. To use a custom font, install it on the machine running the code.

**Q: Is it possible to change the font for a single layer only?**  
A: Yes, you can filter styles by layer name before calling `setPrimaryFontName`.

**Q: What version of Aspose.CAD is required for DWG 2022 files?**  
A: The latest release (as of 2025) fully supports DWG 2022. Always check the release notes for specific format support.

**Q: How do I handle licensing in a development environment?**  
A: Use a temporary evaluation license for testing. For production, embed your purchased license file using `License.setLicense("Aspose.Total.Java.lic");`.

---

**最終更新日:** 2026-05-04  
**テスト環境:** Aspose.CAD for Java 24.11  
**作成者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}