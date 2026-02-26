---
date: 2026-01-10
description: Aspose.CAD for Java を使用して、DGN を DWG にエクスポートし、MicroStation DGN を AutoCAD
  DWG に変換する方法を学びましょう。ステップバイステップガイド。
linktitle: Export DGN as Part of DWG
second_title: Aspose.CAD Java API
title: Aspose.CAD for JavaでDGNをDWGにエクスポート
url: /ja/java/dgn-export-options/export-dgn-as-part-of-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java を使用した DGN から DWG へのエクスポート

## はじめに

このチュートリアルでは、**export dgn to dwg** の方法と、Aspose.CAD for Java ライブラリを使用して MicroStation DGN デザインを AutoCAD DWG ファイルに埋め込む手順を学びます。レガシーな MicroStation 図面の移行や、DGN アンダーレイを DWG レイアウトに組み合わせる必要がある場合でも、本ガイドは環境設定から最終 DWG の PDF プレビュー生成まで、すべてのステップを丁寧に案内します。

## クイック回答
- **「export dgn to dwg」は何を実現しますか？** DGN アンダーレイを DWG に埋め込み、AutoCAD でシームレスに表示できるようにします。
- **プレビュー用にどの形式へエクスポートできますか？** `PdfOptions` を使用して **CAD ファイルを PDF にエクスポート** できます。
- **コード実行にライセンスは必要ですか？** 本番環境で使用する場合は、一時的または有料の Aspose.CAD ライセンスが必要です。
- **サポートされている Java バージョンは？** Java 8 以降で、最新の Aspose.CAD for Java リリースが動作します。
- **無料トライアルはありますか？** はい – Aspose のウェブサイトからトライアルをダウンロードできます。

## 「export dgn to dwg」とは？

DGN を DWG にエクスポートすることは、MicroStation の DGN デザインを AutoCAD の DWG 図面内にアンダーレイとして変換または埋め込むことを意味します。これにより、CAD エンジニアは既存の DGN アセットをゼロからジオメトリを再作成することなく活用できます。

## なぜ MicroStation DGN を AutoCAD DWG に変換するのか？

- **コラボレーション:** AutoCAD を使用するチームは DGN コンテンツを直接閲覧・編集できます。
- **標準化:** DWG は多くの下流ワークフロー（例: PDF 生成、3D レンダリング）の事実上の標準フォーマットです。
- **保存性:** 元の DGN 参照をそのまま保持し、データ損失を低減します。

## 前提条件

チュートリアルに入る前に、以下の前提条件が整っていることを確認してください。
1. **Aspose.CAD ライブラリ:** Aspose.CAD ライブラリ for Java をダウンロードしてインストールします。ライブラリは[こちら](https://releases.aspose.com/cad/java/)で入手できます。
2. **Java Development Kit (JDK):** システムに Java がインストールされていることを確認してください。
3. **統合開発環境 (IDE):** Eclipse や IntelliJ などの Java IDE を選択すると、開発がスムーズになります。

## パッケージのインポート

Java プロジェクトで CAD ファイル操作に必要な Aspose.CAD パッケージをインポートします。例は以下の通りです。

```java
import com.aspose.cad;
import com.aspose.cad.imageoptions;
import com.aspose.cad.fileformats.cad.cadconsts;
import com.aspose.cad.fileformats.cad;
import com.aspose.cad.fileformats.cad.cadobjects;
```

## 手順 1: ファイルパスの設定

DWG ファイルの入力および出力パスを定義します。`dataDir`、`fileName`、`outPath` 変数を適宜更新してください。

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
String outPath = dataDir + "BlockRefDgn.dwg.pdf";
```

## 手順 2: PdfOptions インスタンスの作成

**CAD ファイルを PDF にエクスポート** して迅速に検証できるよう、`PdfOptions` クラスのインスタンスを作成します。

```java
PdfOptions exportOptions = new PdfOptions();
```

## 手順 3: DWG ファイルの読み込み

既存の DWG ファイルを画像として読み込み、`CadImage` 型に変換します。

```java
CadImage cadImage = (CadImage) Image.load(fileName);
```

## 手順 4: エンティティの反復処理

DWG ファイル内の各エンティティを走査し、画像定義かどうかを確認します。画像定義であれば、外部参照オブジェクトを取得します。

```java
for (CadBaseEntity baseEntity : cadImage.getEntities()) {
    if (baseEntity.getTypeName() == CadEntityTypeName.DGNUNDERLAY) {
        CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
        System.out.println(dgnFile.getUnderlayPath());
    }
}
```

## 手順 5: ラスタライズオプションの定義

`CadRasterizationOptions` オブジェクトの設定を定義します。ページ幅・高さ、レイアウト、背景色などを指定します。

```java
CadRasterizationOptions vectorRasterizationOptions = new CadRasterizationOptions();
vectorRasterizationOptions.setPageWidth(1600);
vectorRasterizationOptions.setPageHeight(1600);
vectorRasterizationOptions.setLayouts(new String[] { "Model" });
vectorRasterizationOptions.setAutomaticLayoutsScaling(false);
vectorRasterizationOptions.setNoScaling(true);
vectorRasterizationOptions.setBackgroundColor(Color.getBlack());
vectorRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
```

## 手順 6: ベクトル ラスタライズ オプションの設定

エクスポート用のベクトル ラスタライズ オプションを設定します。

```java
exportOptions.setVectorRasterizationOptions(vectorRasterizationOptions);
```

## 手順 7: DWG を PDF にエクスポート

最後に `save` メソッドを呼び出して、DWG を PDF にエクスポートします。

```java
cadImage.save(outPath, exportOptions);
```

## よくある問題と解決策

| 問題 | 原因 | 解決策 |
|------|------|--------|
| **No DGN underlay appears** | DWG に `DGNUNDERLAY` エンティティが含まれていません。 | ソース DWG に DGN 参照が含まれていることを確認してください。 |
| **PDF is blank** | ラスタライズオプションがゼロサイズに設定されている、またはレイアウトが誤っています。 | `setPageWidth`/`setPageHeight` が正の値であること、`setLayouts` が DWG のレイアウト名と一致していることを確認してください。 |
| **License exception** | 有効な Aspose.CAD ライセンスなしで実行しています。 | API メソッドを呼び出す前に、一時的または購入したライセンスを適用してください。 |

## よくある質問

### Q1: Aspose.CAD for Java のドキュメントはどこで確認できますか？

A1: ドキュメントは[こちら](https://reference.aspose.com/cad/java/)で確認できます。

### Q2: Aspose.CAD ライブラリ for Java をダウンロードするには？

A2: ライブラリは[このリンク](https://releases.aspose.com/cad/java/)からダウンロードできます。

### Q3: Aspose.CAD for Java の無料トライアルはありますか？

A3: はい、無料トライアルは[こちら](https://releases.aspose.com/)で入手できます。

### Q4: Aspose.CAD for Java の一時ライセンスはどこで取得できますか？

A4: 一時ライセンスは[こちら](https://purchase.aspose.com/temporary-license/)から取得できます。

### Q5: サポートが必要、または質問がありますか？

A5: Aspose.CAD コミュニティサポートフォーラムは[こちら](https://forum.aspose.com/c/cad/19)です。

### Q6: 生成した PDF を DWG に戻すことはできますか？

A6: PDF はラスタプレビューです。DWG への逆変換には別途リバースエンジニアリングツールが必要です。

### Q7: この手法は DWF や DXF など他の CAD フォーマットでも利用できますか？

A7: はい、Aspose.CAD は多数のフォーマットをサポートしています。ファイル拡張子とラスタライズ設定を適切に変更すれば対応可能です。

---

**最終更新日:** 2026-01-10  
**テスト済み:** Aspose.CAD for Java 24.11  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}