---
date: 2026-03-02
description: Aspose.CAD for Java の可能性を解き放ちましょう。OLE オブジェクトを簡単にエクスポートし、CAD を PNG として保存できます。シームレスな
  CAD データ管理のために、今すぐダウンロードしてください。
linktitle: Export OLE Objects from CAD
second_title: Aspose.CAD Java API
title: CADをPNGとして保存 – Aspose.CAD for JavaでOLEオブジェクトをエクスポート
url: /ja/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD を PNG として保存 – Aspose.CAD for Java を使用した OLE オブジェクトのエクスポート

## Introduction

コンピュータ支援設計（CAD）の変化の激しい世界では、OLE（Object Linking and Embedding）オブジェクトを効率的に管理・抽出し、さらに **CAD を PNG として保存** できることが、レポート作成、ウェブプレビュー、アーカイブなどの下流ワークフローにとって重要です。Aspose.CAD for Java は、数行のコードで OLE オブジェクトのエクスポートと CAD 図面を高品質な PNG 画像に変換できる、強力なコードファーストソリューションを提供します。

## Quick Answers
- **Aspose.CAD は何をしますか？** ネイティブな CAD ソフトウェアを必要とせず、CAD ファイル（DWG、DXF、DGN など）を読み取り、操作し、変換します。  
- **CAD を PNG として保存できますか？** はい。`PngOptions` と `CadRasterizationOptions` を組み合わせて任意のレイアウトをラスタライズします。  
- **OLE オブジェクトをエクスポートする方法は？** `Image.load` で CAD ファイルを読み込み、OLE を含む各レイアウトを PNG として保存します。  
- **ライセンスは必要ですか？** 無料トライアルが利用可能です。商用ライセンスを取得すると評価版の制限が解除されます。  
- **必要な Java バージョンは？** Java 8 以上が完全にサポートされています。

## What is **save CAD as PNG**?
CAD を PNG として保存するとは、ベクターベースの CAD 図面をピクセルベースの PNG 画像にラスタライズすることを意味します。この変換は、ウェブページ、モバイルアプリ、ドキュメントなどで軽量かつ汎用的に閲覧できるフォーマットが必要な場合に有用です。

## Why use Aspose.CAD for Java to **convert CAD to PNG**?
- **CAD のインストール不要** – ライブラリは完全に Java 上で動作します。  
- **レイアウトの忠実度を保持** – 特定のレイアウトを選択し、DPI を制御し、線の品質を維持できます。  
- **バッチ処理** – シンプルなループで複数ファイルを反復処理できます。  
- **OLE オブジェクトのエクスポート** – DWG/DXF ファイルに埋め込まれた OLE コンテンツが自動的に PNG 出力にレンダリングされます。

## Prerequisites

チュートリアルに入る前に、以下の前提条件が整っていることを確認してください。

- **Java 環境** – マシンに Java 開発環境が設定されていることを確認してください。  
- **Aspose.CAD for Java** – Aspose.CAD for Java ライブラリをダウンロードしてインストールします。ライブラリは [download link](https://releases.aspose.com/cad/java/) で入手できます。  
- **CAD ファイル** – エクスポートしたい OLE オブジェクトを含む CAD ファイルを用意してください。

## Import Namespaces

まず、必要な名前空間を Java プロジェクトにインポートします。これらの名前空間は、Aspose.CAD を使用して CAD ファイルを操作するために必要なクラスと機能を提供します。

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

それでは、CAD から OLE オブジェクトをエクスポートするプロセスを複数のステップに分解してみましょう。

## How to **save CAD as PNG** and export OLE objects

### Step 1: Set Your Document Directory

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

`"Your Document Directory"` を、CAD ファイルが格納されているディレクトリへのパスに置き換えてください。

### Step 2: Define CAD File Names

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

処理したい CAD ファイルの名前を `files` 配列に指定します。

### Step 3: Set PNG Export Options

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

ベクターレスタライズやレイアウト設定など、PNG エクスポートオプションを構成します。これらのオプションにより、望む品質で **CAD を PNG に変換**できます。

### Step 4: Iterate Through CAD Files

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

指定した各 CAD ファイルを反復処理し、Aspose.CAD で読み込んで OLE オブジェクトを PNG 画像として保存します。このループは、**DWG を PNG に一括変換**するシンプルな方法を示しています。

## Common Issues and Solutions

| Issue | Cause | Solution |
|-------|-------|----------|
| **空白の PNG 出力** | レイアウト名の不一致 | `\"Layout1\"` というレイアウト名が元の DWG に存在することを確認してください。 |
| **OLE グラフィックが欠落** | OLE オブジェクトが別のレイアウトに格納されている | `rasterizationOptions.setLayouts(...)` にすべての関連レイアウトを含めてください。 |
| **大きなファイルでのメモリ不足エラー** | 高 DPI 設定 | `rasterizationOptions.setResolution(...)` で DPI を下げるか、ファイルを一つずつ処理してください。 |

## Frequently Asked Questions

**Q: Aspose.CAD はすべての CAD ファイル形式に対応していますか？**  
A: Aspose.CAD は DWG、DXF、DGN など様々な CAD フォーマットをサポートしています。完全な一覧は [documentation](https://reference.aspose.com/cad/java/) を参照してください。

**Q: OLE オブジェクトのエクスポート設定をカスタマイズできますか？**  
A: はい。Aspose.CAD はエクスポート設定を細かくカスタマイズできる豊富なオプションを提供しており、特定の要件に合わせて出力を調整できます。

**Q: Aspose.CAD の無料トライアルはありますか？**  
A: はい、[here](https://releases.aspose.com/) から無料トライアルを取得して Aspose.CAD の機能を体験できます。

**Q: Aspose.CAD のコミュニティサポートはどこで得られますか？**  
A: [forum](https://forum.aspose.com/c/cad/19) の Aspose.CAD コミュニティに参加して支援を求めたり、経験を共有したりできます。

**Q: Aspose.CAD のライセンスはどのように購入できますか？**  
A: 開発ニーズに合ったライセンスは [purchase page](https://purchase.aspose.com/buy) から取得してください。

## Conclusion

これらのシンプルでありながら強力な手順に従うことで、Aspose.CAD for Java を使用して CAD ファイルから OLE オブジェクトをエクスポートしながら、**CAD を PNG として保存**できます。この多用途ツールは開発者が CAD データを効率的に管理できるようにし、CAD アプリケーション開発や下流の画像ベースのワークフローに新たな可能性をもたらします。

---

**最終更新日:** 2026-03-02  
**テスト済み:** Aspose.CAD for Java 24.12  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}