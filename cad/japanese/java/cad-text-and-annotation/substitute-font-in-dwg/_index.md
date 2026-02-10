---
date: 2025-12-28
description: Aspose.CAD for Java を使用して、DWG ファイルを Java プロジェクトに読み込む方法とプライマリ フォント名を設定する方法を学びましょう。完璧な
  CAD ビジュアルのためのステップバイステップ ガイドです。
linktitle: Substitute Font in DWG
second_title: Aspose.CAD Java API
title: JavaでDWGファイルを読み込み、Aspose.CADでフォントを置き換える方法
url: /ja/java/cad-text-and-annotation/substitute-font-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# JavaでDWGファイルを読み込み、Aspose.CADでフォントを置換する方法

## はじめに

Javaアプリケーションで **DWGファイルを読み込む** 必要があり、図面に洗練された外観を与えたい場合、フォントの置換は手早く効果が得られます。Aspose.CAD for Java を使用すれば、デフォルトのテキストスタイルをシステムにインストールされている任意のフォントに置き換えることができ、すべての注釈が期待通りに表示されます。このチュートリアルでは、JavaでDWGファイルを読み込むところから `setPrimaryFontName` メソッドを使ってフォントを変更するまでの全工程を解説します。

## クイック回答
- **必要なライブラリは何ですか？** Aspose.CAD for Java.
- **JavaでDWGファイルを読み込めますか？** はい、DWGパスに対して `Image.load()` を呼び出すだけです。
- **フォントを変更するメソッドはどれですか？** `setPrimaryFontName`.
- **本番環境でライセンスが必要ですか？** はい、商用ライセンスが必要です。
- **バッチ処理は可能ですか？** もちろんです。同じコードで複数ファイルをループ処理できます。

## 「load dwg file java」とは何ですか？

Java環境でDWGファイルを読み込むということは、バイナリCADデータを Aspose.CAD が操作できる `Image` オブジェクトに読み込むことを意味します。ファイルが読み込まれると、レイヤー、スタイル、テキストエンティティに対してプログラムからフルにアクセスできるようになります。

## DWGファイルでフォントを置換する理由

- **一貫性:** ローカルのフォント設定に関係なく、すべての共同作業者が同じ書体を見ることが保証されます。  
- **可読性:** デフォルトのCADフォントは画面上で読みづらいことがあり、Arial のようなクリアなフォントに置き換えることで視認性が向上します。  
- **ブランディング:** 技術図面を企業のスタイルガイドに合わせることができます。  

## 前提条件

- **Java Development Kit (JDK)** – 任意の最新バージョン（8以上推奨）。  
- **Aspose.CAD for Java** – [ウェブサイト](https://releases.aspose.com/cad/java/)からダウンロードしてください。  
- **サンプルDWGファイル** – 変更したい図面（テスト用に任意のDWGまたはDXFファイルを使用できます）。

## 名前空間のインポート

Javaプロジェクトで Aspose.CAD を使用するために必要なクラスをインポートします。これらのインポートにより、画像の読み込み、CAD固有のオブジェクト、スタイル操作にアクセスできます。

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject;
```

## フォント置換のステップバイステップガイド

### ステップ 1: DWG ファイルを読み込む（load dwg file java）

まず、APIにDWG（またはDXF）ファイルの場所を指定し、`CadImage` オブジェクトに読み込みます。

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage) Image.load(srcFile);
```

> **プロのコツ:** DWGファイルを直接扱う場合は、`srcFile` 変数の拡張子を `.dxf` から `.dwg` に置き換えてください。

### ステップ 2: スタイルテーブルを反復処理し、プライマリフォント名を設定する

各CAD図面にはスタイルオブジェクトのコレクションが含まれています。これらをループし、`setPrimaryFontName` メソッド（**プライマリフォント名を設定**する API 呼び出し）を使用してフォントを置換します。

```java
for(Object style : cadImage.getStyles())
{
    // Set the font name
    ((com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject)style).setPrimaryFontName("Arial");
}
```

`"Arial"` を、コードを実行しているマシンにインストールされている任意のフォントに変更できます。

### ステップ 3: 変更した図面を保存する

フォントを更新したら、変更を新しいDWGファイルに書き戻す（または元のファイルを上書きする）ことができます。

```java
cadImage.save(dataDir + "output.dwg", new DwgOptions());
```

保存されたファイルは指定したフォントを使用するようになり、すべてのテキスト注釈がその書体で描画されます。

## 一般的な問題と解決策

| 問題 | 解決策 |
|-------|----------|
| **フォントが適用されない** | フォントがホストOSにインストールされていること、スペルが正確に一致していることを確認してください。 |
| **`Image.load` が例外をスローする** | ファイルパスが正しいこと、そしてファイルがサポートされている DWG/DXF 形式であることを確認してください。 |
| **大きなファイルでパフォーマンスが低下する** | 別スレッドで処理するか、バッチ処理して UI のブロックを回避してください。 |

## よくある質問

**Q: `setPrimaryFontName` メソッドはテキストエンティティのみに影響しますか？**  
A: スタイルテーブルのプライマリフォントを更新し、それによりそのスタイルを参照するすべてのテキストオブジェクトに影響を与えます。

**Q: システムにインストールされていないカスタムフォントを使用できますか？**  
A: Aspose.CAD は OS のフォントレジストリに依存しています。カスタムフォントを使用するには、コードを実行するマシンにフォントをインストールしてください。

**Q: 単一のレイヤーだけのフォントを変更することは可能ですか？**  
A: はい、`setPrimaryFontName` を呼び出す前にレイヤー名でスタイルをフィルタリングできます。

**Q: DWG 2022 ファイルにはどのバージョンの Aspose.CAD が必要ですか？**  
A: 最新リリース（2025年時点）は DWG 2022 を完全にサポートしています。特定の形式サポートについては常にリリースノートをご確認ください。

**Q: 開発環境でのライセンス管理はどうすればよいですか？**  
A: テスト用に一時的な評価ライセンスを使用してください。本番環境では、`License.setLicense("Aspose.Total.Java.lic");` を使用して購入したライセンスファイルを組み込んでください。

---

**最終更新日:** 2025-12-28  
**テスト環境:** Aspose.CAD for Java 24.11  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}