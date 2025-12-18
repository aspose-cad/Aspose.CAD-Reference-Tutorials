---
date: 2025-12-18
description: Aspose.CAD を使用して Java で DWG を PDF またはラスタ画像にエクスポートする方法を探ります。このステップバイステップガイドは、DWG
  ファイルの正確性、効率性、そして簡単な変換を保証します。
linktitle: Export DWG to PDF or Raster
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java を使用して DWG を PDF またはラスタにエクスポート
url: /ja/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java を使用した DWG の PDF またはラスターへのエクスポート

## はじめに

コンピュータ支援設計（CAD）の動的な世界では、図面の効率的な取り扱いが重要です。**Aspose.CAD for Java** を使用すれば、**export dwg to pdf** — またはラスター画像 — を数行のコードで実行できます。このチュートリアルでは、DWG ファイルの読み込みから高品質 PDF の生成までの全プロセスを解説し、なぜ Aspose.CAD Java が CAD 変換タスクに最適なライブラリなのかを紹介します。

## クイック回答
- **このチュートリアルの対象は何ですか？** Aspose.CAD for Java を使用した DWG ファイルの PDF またはラスター画像へのエクスポート。  
- **ライセンスは必要ですか？** 評価用の無料一時ライセンスが利用可能です。製品環境ではフルライセンスが必要です。  
- **サポートされている Java バージョンは？** Java 8 以降のランタイムであれば、最新の Aspose.CAD Java API が動作します。  
- **DWG を他の画像形式に変換できますか？** はい。同じラスター化オプションで PNG、JPEG、BMP などを出力できます。  
- **変換にかかる時間は？** 標準的な図面では通常 1 秒未満です。大きなファイルは数秒かかる場合があります。

## “export dwg to pdf” とは何ですか？
DWG を PDF にエクスポートするとは、ネイティブの AutoCAD 図面をポータブルでデバイスに依存しない PDF ドキュメントに変換することです。生成された PDF はベクターデータ、レイヤー、スケーリングを保持するため、共有、印刷、アーカイブに最適です。

## なぜこの変換に Aspose.CAD Java を使用するのか？
- **外部依存なし** – 純粋な Java で、ネイティブ DLL が不要です。  
- **正確な単位処理** – メートル法またはインチ法を自動的に尊重します。  
- **高品質なラスター出力** – DPI とページサイズを細かく調整できます。  
- **完全な PDF サポート** – 追加ライブラリなしでベクターレベルの PDF を生成します。

## 前提条件

- Java プログラミングの基本知識。  
- Aspose.CAD for Java ライブラリがインストール済み。まだダウンロードしていない場合は **[here](https://releases.aspose.com/cad/java/)** から取得してください。  
- テスト用の DWG ファイル – 本ガイドではサンプルの **Bottom_plate.dwg** を使用します。

## 名前空間のインポート

Java プロジェクトで、変換を開始するために必要なクラスをインポートします：

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## ステップバイステップ ガイド

### 手順 1: DWG ファイルの読み込み

まず、`Image` クラスを使用して DWG 図面を読み込みます。これにより、Aspose.CAD が操作できるメモリ内表現が作成されます。

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

### 手順 2: 単位タイプの判定

図面がメートル法かインチ法かを把握することは、正しいスケーリングに不可欠です。ヘルパーメソッド `IsMetric`（実装は簡略化のため省略）はブール値を返します。

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

### 手順 3: ラスタライズオプションの設定

単位系に基づき、ページサイズ、スケーリング、対象単位タイプを設定します。これらのオプションにより、DWG が PDF にラップされる前のラスタライズ方法が決まります。

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

if (currentUnitIsMetric) {
    // Metric units
    double metersCoeff = 1 / 1000.0;
    double scaleFactor = metersCoeff / currentUnitCoefficient;
    rasterizationOptions.setPageWidth((float)(210 * scaleFactor));
    rasterizationOptions.setPageHeight((float)(297 * scaleFactor));
    rasterizationOptions.setUnitType(UnitType.Millimeter);
} else {
    // Imperial units
    rasterizationOptions.setPageWidth((float)(8.27f / currentUnitCoefficient));
    rasterizationOptions.setPageHeight((float)(11.69f / currentUnitCoefficient));
    rasterizationOptions.setUnitType(UnitType.Inch);
}
```

### 手順 4: PDF オプションの構成

`PdfOptions` インスタンスを作成し、ラスタライズ設定を添付します。これにより、Aspose.CAD がラスタライズされたコンテンツを最終的な PDF に埋め込む方法が指示されます。

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

### 手順 5: PDF として保存

最後に、図面を PDF ファイルとしてエクスポートします。`save` メソッドは出力パスと設定した `PdfOptions` を受け取ります。

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

コードが完了すると、`DWGDrawings` フォルダーに **Saved.pdf** が作成され、配布やアーカイブの準備が整います。

## よくある問題とヒント

- **ページサイズが不正** – 単位変換ロジックを再確認してください。係数が合わないとページが大きくなります。  
- **フォントや線幅が欠如** – 変換前に DWG が外部リソースを参照していることを確認してください。  
- **大規模図面のパフォーマンス** – 高品質が必要なときだけ `CadRasterizationOptions` の `DPI` を上げ、低 DPI にすると処理が高速化します。

## よくある質問

**Q: Aspose.CAD for Java を他の Java フレームワークと併用できますか？**  
A: はい、Aspose.CAD for Java は Spring、Jakarta EE、Android などの一般的な Java フレームワークとシームレスに統合できます。

**Q: Aspose.CAD for Java の一時ライセンスは入手可能ですか？**  
A: はい、**[here](https://purchase.aspose.com/temporary-license/)** から一時ライセンスを取得できます。

**Q: Aspose.CAD for Java のサポートはどこで受けられますか？**  
A: コミュニティや Aspose エンジニアからの支援は **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)** でご覧ください。

**Q: Aspose.CAD for Java のライセンスはどこで購入できますか？**  
A: **[here](https://purchase.aspose.com/buy)** から購入できます。

**Q: Aspose.CAD for Java がサポートする単位は何ですか？**  
A: Aspose.CAD for Java はメートル法とインチ法の両方をサポートし、図面の単位系を自動的に検出します。

**Q: 同じ API で DWG を他の画像形式（例: PNG、JPEG）に変換できますか？**  
A: もちろんです。`PdfOptions` を適切なラスタ画像オプション（例: `PngOptions`）に置き換え、同じ `CadRasterizationOptions` を再利用してください。

## 結論

このチュートリアルでは、Aspose.CAD for Java を使用して **export dwg to pdf** とラスター画像への変換方法を示しました。ステップバイステップのガイドに従うことで、ドキュメント用 PDF やウェブ表示用ラスター画像が必要な場合でも、任意の Java アプリケーションに信頼性の高い CAD 変換機能を組み込むことができます。

---

**最終更新日:** 2025-12-18  
**テスト環境:** Aspose.CAD for Java 24.10  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}