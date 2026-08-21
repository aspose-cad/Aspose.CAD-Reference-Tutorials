---
date: 2026-05-04
description: Aspose.CAD for Java を使用して DGN を AutoCAD PDF にエクスポートし、CAD PDF ファイルを変換する方法を学びましょう。PDF
  のサイズやオプションをカスタマイズできるステップバイステップガイドです。
keywords:
- convert cad pdf
- how to export dgn
- customize pdf size
- aspose cad download
- set pdf options
linktitle: AutoCAD形式のDGNをPDFにエクスポート
second_title: Aspose.CAD Java API
title: CAD PDF変換 – Aspose.CAD for JavaでDGNからAutoCAD PDFへのエクスポートを簡単に
url: /ja/java/dgn-export-options/exporting-dgn-to-pdf/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD PDF を変換: Aspose.CAD for Java を使用した DGN から AutoCAD PDF への簡単エクスポート

## はじめに

DGN ソースから **convert CAD PDF** ファイルを直接変換する必要がある場合、ここが最適です。このチュートリアルでは、Aspose.CAD for Java を使用して DGN ファイルを AutoCAD 互換の PDF にエクスポートする方法をステップバイステップで解説します。カスタムページサイズの設定、特定レイアウトの選択、PDF 出力の微調整方法を示し、プロジェクトにすぐ組み込めるコード例をご紹介します。

## クイック回答
- **“convert CAD PDF” とは何ですか？** CAD ソースファイル（例: DGN）をベクターデータとレイアウトの忠実性を保持した PDF に変換することを指します。  
- **どのライブラリが変換を処理しますか？** Aspose.CAD for Java はこのタスクのための信頼できる、ライセンスフリートライアルを提供します。  
- **開発にライセンスは必要ですか？** テストには無料トライアルで問題ありませんが、本番環境では商用ライセンスが必要です。  
- **PDF のサイズをカスタマイズできますか？** はい、`CadRasterizationOptions` でページ幅・高さ・スケーリングを設定できます。  
- **必要なコード行数はどれくらいですか？** PDF のロード、設定、保存まで 20 行未満の Java コードで実現できます。

## “convert CAD PDF” とは何ですか？
CAD PDF を変換するとは、ネイティブ CAD 図面（例: DGN）から元のベクターグラフィック、レイヤー、レイアウト情報を保持した PDF を生成することです。生成された PDF は CAD ソフトウェアがなくても任意のデバイスで閲覧でき、共有、印刷、アーカイブに最適です。

## なぜ Aspose.CAD for Java を使用して CAD PDF を変換するのか？
- **フルフォーマットサポート** – DGN、DWG、DXF など多数の形式に対応。  
- **外部依存なし** – 純粋な Java 実装で、ネイティブ DLL が不要。  
- **細かな制御** – エクスポートするレイアウトの選択、カスタムページサイズの設定、ラスター化品質の調整が可能。  
- **バッチジョブにスケーラブル** – ループ内で数十ファイルを最小のオーバーヘッドでロード・保存できます。

## 前提条件
以下を事前に用意してください。

- **Aspose.CAD ライブラリ** – ダウンロードはこちら [here](https://releases.aspose.com/cad/java/)。  
- **ドキュメント ディレクトリ** – 入力 DGN ファイルと出力 PDF を保存するフォルダ。

## パッケージのインポート

Java プロジェクトで Aspose.CAD の機能にアクセスするために必要なパッケージをインポートします:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

次に、サンプルコードを複数のステップに分解して説明します。

## ステップ 1: ファイルパスの定義 (dgn のエクスポート方法)

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

`"Your Document Directory"` を実際のファイルが格納されているパスに置き換えてください。

## ステップ 2: DGN イメージのロード

```java
DgnImage objImage = (DgnImage) Image.load(fileName);
```

Aspose.CAD を使用して DGN ファイルをロードします。

## ステップ 3: PDF エクスポートオプションの設定 (pdf サイズのカスタマイズ、pdf オプションの設定)

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); // Export specific views
options.setVectorRasterizationOptions(vectorOptions);
```

ここでは PDF エクスポートオプションを定義します。ページ寸法、AutomaticLayoutsScaling の有効化、最終 PDF に含める DGN のレイアウト（ビュー）を指定します。

## ステップ 4: PDF ファイルの保存

```java
objImage.save(outFile, options);
```

エクスポートされた PDF ファイルを保存します。`save` メソッドは前ステップで設定したすべてのオプションを適用します。

エクスポートした PDF は、必要に応じて任意の場所に保存できます。これらの手順を追加の DGN ファイルに対して繰り返すだけで完了です。おめでとうございます！Aspose.CAD for Java を使用して DGN ファイルを AutoCAD 形式の PDF にエクスポートし、**convert CAD PDF** を正常に実行できました。

## よくある問題と解決策
| 問題 | 発生原因 | 対策 |
|-------|----------------|-----|
| **File not found** | `dataDir` パスが間違っている | フォルダパスを再確認し、DGN ファイルが存在することを確認してください。 |
| **Blank pages in PDF** | `AutomaticLayoutsScaling` が `false` に設定されている、またはレイアウト ID が不足している | `setAutomaticLayoutsScaling(true)` を保持し、レイアウト名（`"1","2",…`）を確認してください。 |
| **Low‑resolution output** | デフォルトのラスター化 DPI が低い | `vectorOptions.setResolution(300);` を `setVectorRasterizationOptions` の前に追加して品質を向上させます。 |
| **License exception** | 本番環境で有効なライセンスなしで実行している | Aspose のドキュメントに記載の手順に従い、一時的または購入したライセンスを適用してください。 |

## よくある質問 (追加)

**Q: マルチレイアウト DGN ファイルから単一レイアウトだけをエクスポートできますか？**  
A: はい、`vectorOptions.setLayouts(new String[] { "2" });` のように目的のレイアウト ID を指定します。

**Q: 生成された PDF にフォントを埋め込むことは可能ですか？**  
A: Aspose.CAD はベクターデータがラスター化される際に必要なフォントを自動的に埋め込みます。必要に応じて `PdfOptions` でフォント埋め込みを制御することもできます。

**Q: 多数の DGN ファイルをバッチ処理するにはどうすればよいですか？**  
A: ファイル名のリストを走査する `for` ループで手順をラップし、各イテレーションで同じ `PdfOptions` インスタンスを再利用します。

**Q: ライブラリはパスワード保護された PDF をサポートしていますか？**  
A: はい、`options.setPassword("yourPassword");` を使用して `PdfOptions` オブジェクトにパスワードを設定できます。

**Q: さらに多くのサンプルはどこで見つけられますか？**  
A: 公式の Aspose.CAD ドキュメントとサンプルリポジトリに多数のシナリオが掲載されています。

## FAQ（オリジナル）

### Q1: Aspose.CAD はすべての CAD ファイル形式に対応していますか？

A1: はい、Aspose.CAD は幅広い CAD 形式をサポートしており、さまざまなファイルタイプの取り扱いに柔軟に対応できます。

### Q2: PDF エクスポート設定をカスタマイズできますか？

A2: もちろんです。本チュートリアルで示したように、ページ寸法やレイアウトなどのオプションを調整して要件に合わせることが可能です。

### Q3: 追加のサポートや支援はどこで受けられますか？

A3: コミュニティサポートとディスカッションは [Aspose.CAD フォーラム](https://forum.aspose.com/c/cad/19) でご利用いただけます。

### Q4: 無料トライアルは利用可能ですか？

A4: はい、無料トライアルは [こちら](https://releases.aspose.com/) から入手できます。

### Q5: 一時ライセンスはどのように取得できますか？

A5: 一時ライセンスは [こちら](https://purchase.aspose.com/temporary-license/) から取得できます。

## 結論

このチュートリアルでは、Aspose.CAD for Java を活用して **convert CAD PDF** ファイルを実現する方法を解説しました。数行のコードで DGN 図面をロードし、PDF エクスポートオプションを微調整して、高品質な PDF を生成できます。プロジェクトの要件に合わせてページサイズやレイアウト、バッチ処理などを自由に試してみてください。

---

**Last Updated:** 2026-05-04  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}