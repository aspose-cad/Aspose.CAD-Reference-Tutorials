---
date: 2026-01-07
description: Aspose.CAD for Java を使用して CAD を PDF にエクスポートし、DGN を PDF に変換する方法を学びましょう。Java
  開発者向けのステップバイステップガイド。
linktitle: Export Embedded DGN
second_title: Aspose.CAD Java API
title: CADをPDFにエクスポート – Aspose.CAD for Javaで埋め込みDGNをエクスポート
url: /ja/java/dgn-export-options/export-embedded-dgn/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD を PDF にエクスポート – Aspose.CAD for Java を使用した埋め込み DGN のエクスポート

## はじめに

このチュートリアルでは、**CAD を PDF にエクスポート**する方法を学びます。埋め込み DGN ファイルを高品質な PDF ドキュメントに変換する手順を Aspose.CAD for Java を使って解説します。Aspose.CAD は、Java 開発者に CAD ファイル操作のフルコントロールを提供する堅牢なライブラリで、**DGN を PDF に変換**、**DWG を PDF に変換**、または CAD 図面を他の形式でレンダリングすることが可能です。以下のステップバイステップガイドに従えば、数分でこの機能をアプリケーションに組み込めます。

## クイック回答
- **「CAD を PDF にエクスポート」とは何ですか？** CAD 図面（DWG、DGN など）をベクタ品質を保ったまま PDF ファイルに変換します。  
- **使用するライブラリは？** Aspose.CAD for Java。  
- **ライセンスは必要ですか？** 本番環境ではライセンスが必要です。無料トライアルがあります。  
- **主な前提条件は？** Java 開発環境と Aspose.CAD for Java の JAR。  
- **出力をカスタマイズできますか？** はい。レイアウトの選択、ラスタライズオプションの設定、PDF 設定の制御が可能です。

## 「CAD を PDF にエクスポート」とは？
CAD を PDF にエクスポートするとは、DWG や DGN といったネイティブ CAD ファイルを、元のジオメトリを忠実に再現した PDF ドキュメントに変換することです。PDF は CAD ソフトウェアが不要で任意のプラットフォームで閲覧できるため、共有、印刷、アーカイブに最適です。

## なぜ Aspose.CAD for Java を使って DGN を PDF に変換するのか？
- **外部依存なし** – 純粋に Java だけで動作。  
- **ベクタデータを保持** – 任意のズームレベルでも PDF が鮮明。  
- **細かな制御が可能** – 特定のレイアウト選択、ラスタライズ DPI 設定、フォント埋め込みができる。  
- **エンタープライズ対応** – 大容量ファイル、バッチ処理、ライセンスオプションに対応。

## 前提条件

作業を始める前に以下を用意してください。

- **Java 開発環境** – JDK 8 以上がインストールされ、設定済みであること。  
- **Aspose.CAD for Java** – 最新の JAR を [here](https://releases.aspose.com/cad/java/) からダウンロード。

## パッケージのインポート

まず、Java プロジェクトで必要なクラスをインポートします。ソースファイルに次のインポート文を追加してください。

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Aspose.CAD for Java を使用して DGN を PDF にエクスポートする方法

以下は、埋め込み DGN ファイル（DWG 内に格納）を PDF に変換する手順を番号付きで示したものです。

### 手順 1: 入出力パスの設定

ソースファイルが格納されているディレクトリと、埋め込み DGN を保持している DWG を指定します。

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

### 手順 2: DWG ファイルの読み込み

DWG ファイルを `Image` オブジェクトにロードします。Aspose.CAD は埋め込み DGN データを自動的に検出します。

```java
Image objImage = Image.load(fileName);
```

### 手順 3: ラスタライズオプションの設定

PDF に含めるレイアウトを選択します。この例では **Model** レイアウトのみをエクスポートします。

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

### 手順 4: PDF オプションの設定

ラスタライズ設定を PDF エクスポートオプションに紐付けます。

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### 手順 5: PDF ファイルの保存

最後に、設定したオプションを使用して PDF をディスクに書き出します。

```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## DWG を PDF に変換 – 追加のヒント

ソースファイルが埋め込み DGN を含まない単純な DWG の場合でも、同じコードを再利用できます。`fileName` を変換したい DWG に変更するだけです。ラスタライズおよび PDF のオプションは同一で、**DWG を PDF に変換**する一貫したワークフローが実現できます。

## よくある問題と解決策

| 問題 | 原因 | 解決策 |
|------|------|--------|
| **Blank PDF output** | Layout name mismatch | `setLayouts` に渡すレイアウト名がソースファイル内のレイアウトと完全に一致しているか（大文字小文字を含め）確認してください。 |
| **License exception** | Using the trial without a license | 画像をロードする前に有効な Aspose.CAD ライセンスを適用します (`License license = new License(); license.setLicense("Aspose.CAD.lic");`)。 |
| **File not found** | Incorrect `dataDir` path | 絶対パスを使用するか、プロジェクトの作業ディレクトリからの相対パスが正しいことを確認してください。 |
| **Low‑resolution graphics** | Default rasterization DPI is low | `rasterizationOptions.setPageWidth/Height` または `setResolution` で DPI を上げてください。 |

## FAQ

**Q: Aspose.CAD for Java を商用プロジェクトで使用できますか？**  
A: はい、Aspose.CAD for Java は商用ライブラリです。ライセンスは [here](https://purchase.aspose.com/buy) から取得できます。

**Q: 無料トライアルはありますか？**  
A: はい、Aspose.CAD for Java の無料トライアルは [here](https://releases.aspose.com/) から入手できます。

**Q: Aspose.CAD for Java のサポートはどこで受けられますか？**  
A: Aspose.CAD コミュニティの [forum](https://forum.aspose.com/c/cad/19) でサポートを受けられます。

**Q: 一時ライセンスは取得できますか？**  
A: はい、一時ライセンスは [here](https://purchase.aspose.com/temporary-license/) から取得可能です。

**Q: ドキュメントはどこにありますか？**  
A: ドキュメントは [here](https://reference.aspose.com/cad/java/) にあります。

## 結論

これで **CAD を PDF にエクスポート**する方法、特に **DGN を PDF に変換**し、さらに **DWG を PDF に変換**する手順を Aspose.CAD for Java を使って学びました。上記の手順に従えば、任意の Java ベースのソリューションにシームレスな CAD‑to‑PDF 変換機能を組み込み、高品質な PDF をユーザーに提供でき、追加の CAD ソフトは不要です。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-01-07  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose