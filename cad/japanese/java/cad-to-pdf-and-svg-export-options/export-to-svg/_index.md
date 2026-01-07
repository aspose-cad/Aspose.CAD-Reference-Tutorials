---
date: 2026-01-07
description: Aspose.CAD for Java を使用して CAD を SVG にエクスポートする方法を学びましょう。このステップバイステップガイドでは、DWG
  を SVG に変換する方法、SVG のカラーモードを設定する方法、そしてライブラリを Java プロジェクトに統合する方法を示します。
linktitle: Export to SVG
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java を使用して CAD を SVG にエクスポート
url: /ja/java/cad-to-pdf-and-svg-export-options/export-to-svg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java を使用した CAD の SVG へのエクスポート

## はじめに

Aspose.CAD for Java の世界へようこそ。この強力なライブラリは、開発者が CAD 図面を簡単に操作できるようにします。経験豊富な開発者でも、CAD 初心者でも、本ガイドでは **export CAD to SVG** の手順をステップバイステップで解説し、DWG から SVG への変換、SVG カラーモードの設定、API を Java プロジェクトに統合する方法を示します。

## Quick Answers
- **What does “export CAD to SVG” mean?** CAD 図面（例：DWG）をブラウザで表示できる Scalable Vector Graphics ファイルに変換します。  
- **Which library handles the conversion?** Aspose.CAD for Java がこのタスク用のシンプルな API を提供します。  
- **Do I need a license for development?** 無料トライアルでテストは可能ですが、実運用には商用ライセンスが必要です。  
- **Can I control the SVG color output?** はい、SVG カラーモード（例：grayscale）を設定できます。  
- **Is any additional software required?** 必要なのは Java ランタイムと Aspose.CAD の JAR ファイルだけです。

## 前提条件

チュートリアルに入る前に、以下の前提条件を満たしていることを確認してください。

- Java 開発環境: システムに Java がインストールされていること。  
- Aspose.CAD ライブラリ: [download link](https://releases.aspose.com/cad/java/) から Aspose.CAD for Java ライブラリをダウンロードしてインストール。  
- ドキュメントディレクトリ: CAD 図面用のディレクトリを作成し、そのパスをメモしておきます。

## 名前空間のインポート

このステップでは、Aspose.CAD の旅を開始するために必要な名前空間をインポートします。以下の手順に従ってください。

### 手順 1: Java プロジェクトを開く
使用している IDE で Java プロジェクトを開きます。

### 手順 2: Aspose.CAD ライブラリを追加
プロジェクトに Aspose.CAD ライブラリを追加します。JAR ファイルをプロジェクトの依存関係に含めるだけです。

### 手順 3: 名前空間をインポート
Java クラス内で必要な名前空間をインポートします:

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.SvgOptions;
import com.aspose.cad.imageoptions.SvgColorMode;
```

## Export CAD to SVG

ステージが整ったので、Aspose.CAD for Java を使用した **export CAD to SVG** のステップバイステッププロセスに進みます。

### 手順 1: リソースディレクトリを指定
CAD 図面が格納されているリソースディレクトリへのパスを定義します:

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

### 手順 2: CAD 図面を読み込む
Aspose.CAD ライブラリを使って CAD 図面を読み込みます:

```java
Image image = Image.load(dataDir + "meshes.dwg");
```

### 手順 3: SVG エクスポートオプションを設定
SVG エクスポートオプションを構成して出力をカスタマイズします。ここでは **set SVG color mode** をグレースケールに設定し、テキストをシェイプに変換するようエクスポーターに指示します:

```java
SvgOptions options = new SvgOptions();
options.setColorType(SvgColorMode.Grayscale);
options.setTextAsShapes(true);
```

### 手順 4: SVG として保存
CAD 図面を SVG ファイルとして保存します:

```java
image.save(dataDir + "meshes.svg");
```

> **プロのコツ:** 色を保持したまま **convert DWG to SVG** したい場合は、`SvgColorMode.Grayscale` を `SvgColorMode.FullColor` に変更してください。

おめでとうございます！Aspose.CAD for Java を使用して CAD 図面を SVG に正常にエクスポートできました。

## なぜ Aspose.CAD を使って CAD を SVG にエクスポートするのか？
- **高忠実度:** ベクターデータが保持されるため、SVG は元の CAD 図面とまったく同じ外観になります。  
- **外部依存なし:** 変換は完全に Java 内で実行され、追加ツールは不要です。  
- **出力のカスタマイズ:** `setColorType` などのオプションで、SVG をグレースケールにするかフルカラーにするかを制御できます。

## よくある問題と解決策
- **ファイルが見つからない:** `dataDir` が正しいフォルダーを指しているか、DWG ファイル名が一致しているか確認してください。  
- **空白の SVG 出力:** 図面にテキストが含まれ、シェイプとして表示したい場合は `options.setTextAsShapes(true)` を設定してください。  
- **サポートされていない CAD フォーマット:** Aspose.CAD は DWG、DXF、DWF など多数のフォーマットをサポートしています。正確な一覧はドキュメントをご確認ください。

## 結論

本チュートリアルでは、Aspose.CAD for Java を活用して **export CAD to SVG** をシームレスに行う方法を紹介しました。直感的な API と堅牢な機能により、Aspose.CAD は CAD 操作の複雑なタスクを簡素化し、開発者にとって多用途なツールとなります。

## FAQ's

### Q1: Aspose.CAD for Java は他の CAD フォーマットでも使用できますか？

A1: はい、Aspose.CAD は DWG、DXF、DWF などさまざまな CAD フォーマットをサポートしています。

### Q2: Aspose.CAD は初心者と経験豊富な開発者の両方に適していますか？

A2: もちろんです！Aspose.CAD は初心者にも使いやすい API を提供しつつ、熟練開発者向けの高度な機能も備えています。

### Q3: 追加のサポートやコミュニティディスカッションはどこで見つけられますか？

A3: サポートとディスカッションは [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) で行われています。

### Q4: 無料トライアルはありますか？

A4: はい、[free trial](https://releases.aspose.com/) で Aspose.CAD をお試しいただけます。

### Q5: Aspose.CAD for Java のライセンスはどこで購入できますか？

A5: [purchase page](https://purchase.aspose.com/buy) からライセンスをご購入いただけます。

## Frequently Asked Questions

**Q: 同じコードで DXF ファイルを SVG に変換できますか？**  
A: はい、ファイル名を DXF に置き換えるだけで、API が両方のフォーマットを処理します。

**Q: 出力をフルカラー SVG に変更するには？**  
A: 保存前に `options.setColorType(SvgColorMode.FullColor);` を設定してください。

**Q: 生成された SVG にフォントを埋め込むことは可能ですか？**  
A: 現在 Aspose.CAD はテキストをシェイプに変換するため、フォント埋め込みは必要ありません。

**Q: ライブラリは Linux と macOS でも動作しますか？**  
A: Java ライブラリはプラットフォームに依存せず、互換性のある JVM があればどこでも動作します。

**Q: 本チュートリアルで使用した Aspose.CAD のバージョンは？**  
A: Aspose.CAD for Java 24.10 でテストしています。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-01-07  
**Tested With:** Aspose.CAD for Java 24.10  
**Author:** Aspose  

---