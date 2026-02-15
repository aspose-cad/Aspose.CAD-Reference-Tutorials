---
date: 2026-02-15
description: Aspose.CAD for Java を使用して、カスタムページサイズの設定方法と CAD から PDF を作成する方法を学びましょう。このステップバイステップガイドでは、Auto
  Layout Scaling を利用した CAD の PDF へのエクスポートについて解説します。
linktitle: Setting Auto Layout Scaling
second_title: Aspose.CAD Java API
title: カスタムページサイズの設定 – Auto LayoutスケーリングでCADからPDFを作成
url: /ja/java/advanced-cad-features/setting-auto-layout-scaling/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# カスタムページサイズの設定 – Auto Layout Scaling を使用した CAD から PDF の作成

## はじめに

**CAD から PDF を作成** する際に **カスタムページサイズを設定** したい場合、Aspose.CAD for Java が迅速かつ完璧なスケーリングで対応します。Auto Layout Scaling はレイアウト寸法を自動的に調整し、元の CAD ページサイズに関係なく、生成された PDF が意図した通りに表示されます。このチュートリアルでは、DXF ファイルの読み込みから PDF のエクスポートまでの全工程を解説し、ライブラリの **export CAD to PDF** 機能を強調するとともに、必要に応じて **convert DWG to PDF** や **increase PDF resolution** も行える方法を示します。

## クイック回答
- **Auto Layout Scaling とは何ですか？** ラスタライズ時に CAD レイアウトを自動的にリサイズし、ターゲットページ寸法に合わせます。  
- **どのフォーマットを変換できますか？** Aspose.CAD がサポートするすべてのフォーマット（例：DXF、DWG、DWF）を PDF に変換できます。  
- **本番環境でライセンスは必要ですか？** はい、評価版以外での使用には商用ライセンスが必要です。  
- **変換にかかる時間はどれくらいですか？** 標準的なファイルであれば、最新ハードウェア上で 1 秒未満です。  
- **ページサイズは変更できますか？** はい、`CadRasterizationOptions` を使用してカスタムページ寸法を設定できます。

## “create PDF from CAD” とは？

CAD から PDF を作成するとは、ベクターベースのエンジニアリング図面（DXF、DWG など）をラスタライズして PDF ドキュメントに変換することです。PDF は元の図面の視覚的忠実度を保持しつつ、あらゆるプラットフォームで広く閲覧可能になります。

## Auto Layout Scaling を使用する理由

- **一貫した出力:** 手動でサイズ計算を行うことなく、すべてのレイアウトが PDF ページ全体に収まります。  
- **時間の節約:** 各図面ごとにスケーリング係数を手動で調整する必要がなくなります。  
- **高品質:** 変換中に線幅やジオメトリの精度を維持します。  
- **柔軟性:** **convert dxf to pdf**、**convert dwg to pdf**、さらには **increase PDF resolution** が必要な印刷用ファイルにも対応します。

## 前提条件

1. **Aspose.CAD for Java ライブラリ** – 最新バージョンを [download page](https://releases.aspose.com/cad/java/) からダウンロードしてください。  
2. **リソースディレクトリ** – CAD ファイルを保存するフォルダーを作成し、コード中の `"Your Document Directory"` をそのパスに置き換えます。  
3. **サンプル CAD ファイル** – 本ガイドでは `conic_pyramid.dxf` を使用します。このファイルは Aspose のサンプルデータセットに含まれています。

## 名前空間のインポート

まず、必要なクラスをインポートします。これにより、画像の読み込み、ラスタライズ、PDF エクスポート機能が利用可能になります。

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## CAD から PDF へのカスタムページサイズ設定手順

ステップバイステップのコードに入る前に、カスタムページサイズを設定する重要性を理解しましょう。**カスタムページサイズを設定** すると、生成される PDF の実際の寸法（例：A4、Letter、または独自サイズ）を制御できます。これは、図面がシート規格に合わせる必要があるエンジニアリングワークフローや、PDF を大きな文書に埋め込む際に不可欠です。

### 手順 1: CAD ファイルの読み込み

ソースファイルの読み込みは、**how to export CAD** して PDF ドキュメントを作成する最初のステップです。

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### 手順 2: ラスタライズオプションの作成

ターゲットページの寸法を定義します。このブロックを使用して、カスタムレイアウトが必要な場合は **set CAD page size** を手動で設定することもできます。

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### 手順 3: Auto Layout Scaling の設定

自動スケーリング機能を有効にします。これは **how to set scaling** for a CAD‑to‑PDF conversion の核心です。

```java
rasterizationOptions.setAutomaticLayoutsScaling(true);
```

### 手順 4: PDF オプションの作成

ラスタライズ設定を PDF エクスポートオプションにリンクします。

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### 手順 5: PDF へのエクスポート

最後に、レンダリングされた画像を PDF ファイルとして保存します。この手順で **convert dxf to pdf** ワークフローが完了します。

```java
image.save(dataDir + "result_out_.pdf", pdfOptions);
```

上記手順を、**DWG**、**DWF**、その他サポートされているフォーマットの CAD ファイルにも繰り返し適用してください。

## 主なユースケース

| シナリオ | カスタムページサイズを設定する理由 |
|----------|-----------------------------------|
| **建設図面の提出** | 規制当局が要求する標準的な A1/A2 シートサイズに PDF を合わせられる |
| **技術マニュアルへの埋め込み** | 手動スケーリングなしで、図面がマニュアルの事前定義レイアウトに収まる |
| **高解像度印刷** | DPI を上げても（例：`rasterizationOptions.setResolution(300)`）ページ寸法を一定に保てる |

## よくある問題とトラブルシューティング

| 症状 | 考えられる原因 | 対策 |
|------|----------------|------|
| 空白の PDF が出力される | ラスタライズオプションが未設定、またはファイルパスが間違っている | `srcFile` パスを確認し、`setPageWidth/Height` が 0 でないことを確認 |
| スケーリングが歪む | `setAutomaticLayoutsScaling` が `false` のまま | 自動スケーリングを有効にするか、手動でスケーリング係数を計算 |
| レイヤーが欠落している | ソース DXF に未サポートのエンティティが含まれる | Aspose.CAD のリリースノートでサポート対象エンティティを確認 |

## FAQ

**Q: Aspose.CAD for Java はすべての CAD ファイル形式に対応していますか？**  
A: Aspose.CAD for Java は DWG、DXF、DWF など、さまざまな CAD フォーマットをサポートしています。

**Q: スケーリングオプションをさらにカスタマイズできますか？**  
A: はい、`CadRasterizationOptions` クラスはスケーリング、DPI、その他ラスタライズ設定を細かく調整するプロパティを提供します。

**Q: Aspose.CAD for Java の追加ドキュメントはどこで確認できますか？**  
A: 詳細情報やサンプルは [documentation](https://reference.aspose.com/cad/java/) を参照してください。

**Q: Aspose.CAD for Java の無料トライアルはありますか？**  
A: はい、[free trial](https://releases.aspose.com/) で機能を体験できます。

**Q: Aspose.CAD for Java に関するサポートやディスカッションはどこで行えますか？**  
A: コミュニティやサポートは [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) で利用できます。

### 追加の一般的な質問

**Q: DXF ではなく DWG ファイルを PDF に変換するにはどうすればよいですか？**  
A: 同じコードで可能です。`srcFile` の拡張子を `.dwg` に変更してください。

**Q: 高解像度 PDF 用にカスタム DPI を設定できますか？**  
A: はい、`rasterizationOptions.setResolution(300);` のように任意の DPI を指定できます。

**Q: 生成された PDF にフォントを埋め込むことは可能ですか？**  
A: Aspose.CAD は図面をラスタライズするため、フォントはベクトルとして描画され、別途フォント埋め込みは不要です。

## 結論

本ガイドに従うことで、Aspose.CAD for Java の Auto Layout Scaling を利用した **カスタムページサイズの設定** と **CAD から PDF の作成** 方法が習得できました。これにより **export CAD to PDF** ワークフローが効率化され、一貫したスケーリングが保証され、開発時間を大幅に削減できます。プロジェクトの要件に合わせて、さまざまなページサイズ、解像度、CAD フォーマットを試してみてください。**DWG を PDF に変換**、**PDF 解像度の向上**、あるいは **java CAD to PDF バッチプロセッサ** の構築にも活用できます。

---

**最終更新日:** 2026-02-15  
**テスト環境:** Aspose.CAD for Java 24.12（最新）  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}