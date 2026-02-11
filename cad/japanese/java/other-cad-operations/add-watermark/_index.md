---
date: 2026-01-20
description: Aspose.CAD for Java を使用して CAD 図面から PDF を作成し、CAD 図面に透かしを追加する方法を学びましょう。シームレスな統合のためのステップバイステップ
  ガイドに従ってください。
linktitle: Add Watermark
second_title: Aspose.CAD Java API
title: CADからPDFを作成し、透かしを追加する – Aspose.CAD for Java
url: /ja/java/other-cad-operations/add-watermark/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CADからPDFを作成しウォーターマークを追加 – Aspose.CAD for Java

## はじめに

この包括的なチュートリアルでは、Aspose.CAD for Java を使用して **CAD から PDF を作成** し、**ーターマークを追加する方法** を学びます。エンジニアリングの手順を案内します。

## クイック回答
- **このチュートリアルでカバーする内容は？** CAD ファイルにテキストウォーターマークを追加し、PDF としてエクスポートします。  
- **必要なライブラリは？** Aspose.CAD for Java（最新バージョン）。  
- **ライセンスは必要ですか？** テストには無料ト。  
- **サポートされている Java バージョンは？** Java 8 以降。  
- **実装にかかる時間はーターマークであれば通常 15 分未満ータブルな PDF ドキを意味します。生成された PDF は印刷、他のワークフローへの埋め込みが容易になります。

## なぜ CAD 図面にウォーターマークを追加するのか？

- **ブランド保護:** 会社のロゴや機密通知を表示します。  
- **バ書き、改訂、または「機密」ステータスをマークします。  
- **コンプライアンス:** 文書ラベリングが求められる業界規制に対応します。

## 前提条件

Before we dive inウンロードしてください [here](https://releases.aspose.com/cad/java/)。  
- **Java Development Kit (JDK)** – マシンに最新の JDK がインストールされていること。

## パッケージのインポート

In your Java project, import the necessary Aspose.CAD namespaces:

```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.Cad3DPoint;
import com.aspose.cad.fileformats.cad.cadobjects.CadMText;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## ウォーターマーク付きで CAD から PDF を作成する方法

### ステップ 1: 新しい MTEXT ウォーターマークを追加

First, we create an `MTEXT` entity that will serve as the visible watermark on the drawing.

```java
//add new MTEXT
CadMText watermark = new CadMText();
watermark.setText("Watermark message");
watermark.setInitialTextHeight(40);
watermark.setInsertionPoint(new Cad3DPoint(300, 40));
watermark.setLayerName("0");
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(watermark);
```

*プロのコツ:* `setInsertionPoint` の座標を調整して、レイアウトに最適な位置にウォーターマークを配置してください。

### ステップ 2: シンプルな Text エンティティを追加（オプション）

If you prefer a plain‑text watermark, you can add a `Text` entity instead of `MTEXT`.

```java
// or add more simple entity like Text
CadText text = new CadText();
text.setDefaultValue("Watermark text");
text.setTextHeight(40);
text.setFirstAlignment(new Cad3DPoint(300, 40));
text.setLayerName("0") ;
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(text);
```

### ステップ 3: CAD 図面を PDF にエクスポート

After embedding the watermark, rasterize the drawing and save it as a PDF file.

```java
// export to pdf
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setLayouts(new String[]{"Model"});
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
cadImage.save(dataDir + "AddWatermark_out.pdf", pdfOptions);
```

`CadRasterizationOptions` を使用すると、出力サイズとレイアウトを制御でき、最終的な PDF でウォータ明に 発生原因 | 解決策 |
|-------|----------------を設定してください（作成後に追加）。 |
| テキストが切り取られる | 挿入ポイントが図面の範囲外です。 |().get安全な境界を計算してください。 |
| PDF ファイルが大きい | 非常に高解像度でラスタライズしているためです。 | `PageWidth`/`PageHeight` を減らすか、ベクトルラスタライズを有効にしてください（`izationOptions(true);`）。 |

## FAQ

### Q1: Aspose.CADォーターマークテキストの外観をカスタマイズできますい、テキストサイズ、色、位置 for Java のトライアル版は利用可能ですか？

A3: はい、トライアル版は [here](https://releases.aspose.com/) からダウンロードできます。

### Q4: Aspose.CAD のサポートはどのように受けられますか？

A4: コミュニティサポートは [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) をご覧ください。

### Q5: Aspose.CAD for Java の完全なドキュメントはどこで見つけられますか？

A5: 詳細情報は [documentation](https://reference.aspose.com/cad/java/) を参照してください。

**Additional Questions**

**Q: テキストではなく画像のウォーターマークを追加できますか？**  
A: はい。`CadImage` を使用して外部画像をインポートし、エクスポート前にラスタエンティティとして追加します。

**Q: バッチで複数の CAD ファイルに同じウォーターマークを適用するにはどうすればよいですか？**  
A: 各 CAD ファイルを読み込み、エンティティを追加し、PDF を保存するループ内にウォーターマーク作成コードを配置します。

**Q: PDF をラスタライズせずにベクトルベースのまま保持できますか？**  
A: サポートされている場合は、`rasterizationOptions.setVectorRasterizationOptions(true);` を設定してベクトルデータを保持します。

## 結論

これで、Aspose.CAD for Java を使用して **CAD から PDF を作成** し、**CAD 図面にウォーターマークを追加**する方法を習得しました。これらの手順に従うことで、デザインを保護し、ブランドを強化し、自信を持って洗練された PDF を共有できます。

---

**最終更新日:** 2026-01-20  
**テスト環境:** Aspose.CAD for Java 24.12  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}