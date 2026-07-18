---
date: 2026-07-18
description: Aspose CAD 変換を使用すると、IFC を PNG に、IGES を PDF に簡単にエクスポートできます。Aspose.CAD
  for .NET を使って CAD ファイルを数分で変換する手順をステップバイステップで学びましょう。
keywords:
- aspose cad conversion
- export cad to png
- convert iges to pdf
lastmod: 2026-07-18
linktitle: 画像形式へのエクスポート
og_description: Aspose CAD 変換により、IFC を PNG に、IGES を PDF に迅速にエクスポートできます。Aspose.CAD
  for .NET を使用したシームレスな CAD ファイル処理のために、このガイドに従ってください。
og_image_alt: Guide showing Aspose CAD conversion from CAD files to PNG and PDF
og_title: Aspose CAD 変換：画像形式へのエクスポート
schemas:
- author: Aspose
  dateModified: '2026-07-18'
  description: Aspose CAD conversion lets you effortlessly export IFC to PNG and IGES
    to PDF. Learn step‑by‑step how to convert CAD files with Aspose.CAD for .NET in
    minutes.
  headline: 'Aspose CAD Conversion: Exporting to Image Formats'
  type: TechArticle
- questions:
  - answer: Yes, iterate over a folder with `foreach (var file in Directory.GetFiles(path,
      "*.ifc")) { var img = new Image(file); img.Save(Path.ChangeExtension(file, ".png"),
      ImageFormat.Png); }`. The `Directory.GetFiles` method returns the names of files
      (including their paths) that match a specified pattern in a directory.
    question: Can I convert multiple CAD files in one batch?
  - answer: Layer visibility is respected; you can toggle layers via `LoadOptions`
      before saving, ensuring only selected layers appear in the output.
    question: Does Aspose.CAD preserve layer information in the exported image?
  - answer: The library comfortably processes files up to **2 GB**; larger files should
      be split or streamed using `LoadOptions.MemoryLimit`.
    question: What is the maximum file size Aspose.CAD can handle?
  - answer: Yes—by saving as `ImageFormat.Pdf` the output retains vector data, allowing
      infinite scaling without quality loss.
    question: Is there support for converting CAD to vector‑based PDFs?
  - answer: A single Aspose.CAD license covers all supported .NET runtimes (Framework,
      Core, and .NET 5+).
    question: Do I need a separate license for each .NET platform?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- aspose cad
- cad conversion
- export cad to png
- iges to pdf
- ifc to png
title: Aspose CAD 変換：画像形式へのエクスポート
url: /ja/net/exporting-to-image-formats/
weight: 39
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose CAD 変換: 画像形式へのエクスポート

現代のエンジニアリングおよびデザインワークフローでは、**aspose cad conversion** は複雑な CAD および BIM ファイルを普遍的に閲覧可能な画像形式に変換するために不可欠です。IFC モデルの簡易プレビューを共有したり、IGES 図面から印刷可能な PDF を生成したりする必要がある場合でも、このチュートリアルでは Aspose.CAD for .NET を使用した正確な手順を案内します。PNG、PDF、その他のラスタ形式へエクスポートする際に、ジオメトリ、色、レイヤーをそのまま保持する方法が分かります。

## クイック回答
- **Aspose.CAD がエクスポートできる形式は何ですか？** 30 以上の CAD/BIM フォーマットを 20 以上の画像タイプに変換でき、PNG、JPEG、PDF、TIFF などが含まれます。  
- **開発にライセンスは必要ですか？** 無料トライアルは評価に使用できますが、本番環境では商用ライセンスが必要です。  
- **サポートされている .NET バージョンは？** .NET Framework 4.6 以上、.NET Core 3.1 以上、.NET 5/6/7。  
- **大きなファイルを処理できますか？** はい – Aspose.CAD はドキュメント全体をメモリに読み込まずに 2 GB までのファイルを処理できます。  
- **追加のソフトウェアは必要ですか？** 外部の CAD ツールは不要で、ライブラリが内部で全ての変換を行います。

## Aspose CAD 変換とは？
`Image` クラスはメモリにロードされた CAD ドキュメントを表し、さまざまな形式で保存するメソッドを提供します。Aspose CAD Conversion は Aspose.CAD for .NET を使用して CAD/BIM ファイルを他の形式に変換します。`Image` でソースをロードし、対象フォーマットを選択して `Save` を呼び出します。この 2 段階のパターンにより、レイヤー、線幅、テクスチャが保持され、元の設計意図と一致します。

## IFC ファイルを PNG にエクスポートする方法は？
`Image` クラスはメモリにロードされた CAD ドキュメントを表し、さまざまな形式で保存するメソッドを提供します。`new Image("model.ifc")` で IFC ファイルをロードし、`image.Save("model.png", ImageFormat.Png)` を呼び出します。Aspose.CAD は 3D ジオメトリを読み取り、ラスタ画像にフラット化し、色深度と透過性を保持した高解像度 PNG を出力します。バッチ処理の場合は、フォルダーをループして各ファイルを保存します。

## IGES ファイルを PDF にエクスポートする方法は？
`Image` クラスはメモリにロードされた CAD ドキュメントを表し、さまざまな形式で保存するメソッドを提供します。IGES ファイルから `Image` インスタンスを作成し、`image.Save("drawing.pdf", ImageFormat.Pdf)` を呼び出します。変換はベクトル情報、線種、注釈を保持し、詳細が失われない任意のビューアで開ける PDF を生成します。印刷用 PDF の DPI を上げるには、オプションの `Resolution` プロパティを使用してください。

## .NET 用 Aspose.CAD を使用する理由
Aspose.CAD は **30 以上の入力フォーマット**（IFC、IGES、DWG、DWF、STL など）をサポートし、**20 以上の画像タイプ** に出力できます。典型的なサーバー上で数百ページの図面を 5 秒未満で処理し、完全にオフラインで動作します—ネイティブ CAD のインストールは不要です。これらの数値化された利点により、エンタープライズでもフリーランスでもコスト効果が高く高性能な選択肢となります。

## よくある落とし穴とプロのコツ
`LoadOptions` クラスを使用すると、メモリ制限の設定やレイヤーの指定など、CAD ファイルのロード方法をカスタマイズできます。  
`FontSettings` オブジェクトは、変換時に使用されるフォント置換と埋め込みルールを定義します。  

- **落とし穴:** デフォルト DPI を無視すると低解像度画像になることがあります。  
  **プロのコツ:** `image.DpiX` と `image.DpiY` を 300 に設定して印刷品質の PNG を作成します。  
- **落とし穴:** 大きな IGES ファイルはメモリ制限を超える可能性があります。  
  **プロのコツ:** `LoadOptions` の `MemoryLimit` を使用してファイルをチャンクでストリーミングします。  
- **落とし穴:** IFC モデルでフォントが欠如するとプレースホルダー文字が表示されます。  
  **プロのコツ:** 変換前に `FontSettings` オブジェクトを使用して必要なフォントを埋め込みます。

## 画像形式へのエクスポートチュートリアル
### [IFC ファイルを PNG にエクスポート - Aspose.CAD チュートリアル](./exporting-ifc-files-to-png/)
Aspose.CAD for .NET を探求し、シームレスな IFC から PNG への変換を実現する堅牢なソリューションです。効率的な CAD ファイル処理のために今すぐダウンロードしてください。
### [IGES ファイルを PDF にエクスポート - Aspose.CAD ガイド](./exporting-iges-files-to-pdf/)
Aspose.CAD for .NET を使用して IGES ファイルを PDF に簡単にエクスポートする方法を学びます。正確な CAD ファイル操作のためのステップバイステップガイドをご覧ください。

## よくある質問

**Q: 複数の CAD ファイルを一括で変換できますか？**  
A: はい、フォルダーを `foreach (var file in Directory.GetFiles(path, "*.ifc")) { var img = new Image(file); img.Save(Path.ChangeExtension(file, ".png"), ImageFormat.Png); }` で反復処理できます。`Directory.GetFiles` メソッドは、ディレクトリ内で指定されたパターンに一致するファイル名（パスを含む）を返します。  

**Q: Aspose.CAD はエクスポートされた画像でレイヤー情報を保持しますか？**  
A: レイヤーの可視性は尊重されます。保存前に `LoadOptions` でレイヤーを切り替えることで、出力に選択されたレイヤーのみが表示されるようにできます。  

**Q: Aspose.CAD が処理できる最大ファイルサイズは何ですか？**  
A: このライブラリは **2 GB** までのファイルを問題なく処理できます。より大きなファイルは `LoadOptions.MemoryLimit` を使用して分割またはストリーミングする必要があります。  

**Q: CAD をベクトルベースの PDF に変換するサポートはありますか？**  
A: はい。`ImageFormat.Pdf` で保存することで、出力はベクトルデータを保持し、品質の低下なしに無限に拡大できます。  

**Q: 各 .NET プラットフォームごとに別々のライセンスが必要ですか？**  
A: 単一の Aspose.CAD ライセンスで、サポートされているすべての .NET ランタイム（Framework、Core、.NET 5+）をカバーします。  

**最終更新日:** 2026-07-18  
**テスト環境:** Aspose.CAD 24.12 for .NET  
**作者:** Aspose

## 関連チュートリアル

- [IFC ファイルを PNG にエクスポート - Aspose.CAD チュートリアル](/cad/net/exporting-to-image-formats/exporting-ifc-files-to-png/)
- [IGES ファイルを PDF にエクスポート - Aspose.CAD ガイド](/cad/net/exporting-to-image-formats/exporting-iges-files-to-pdf/)
- [Aspose.CAD for .NET で CAD レイアウトをラスタ画像形式にエクスポート](/cad/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}