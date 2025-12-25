---
date: 2025-12-25
description: Aspose.CAD for Java を使用して DWG を BMP にエクスポートする方法を学びましょう。このステップバイステップガイドでは、CAD
  図面のサイズ調整と CAD を BMP に効率的に変換する手順を示します。
linktitle: Adjusting CAD Drawing Size Using Unit Type
second_title: Aspose.CAD Java API
title: DWG を BMP にエクスポート – ユニットタイプで CAD サイズを調整 (Java)
url: /ja/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG を BMP にエクスポート – Aspose.CAD for Java を使用したユニットタイプによる CAD 図面サイズの調整

## はじめに

**export DWG to BMP** が必要な場合、出力サイズと測定単位を制御することは、下流の処理や印刷において重要です。このチュートリアルでは、Aspose.CAD for Java を使用して CAD 図面サイズを調整し、CAD を BMP に変換する方法を学びます。測定単位は `UnitType` プロパティで定義します。手順は平易な言葉で説明しているので、ライブラリが初めての方でもフォローできます。

## クイック回答
- **What does “export DWG to BMP” mean?** DWG 図面を BMP ラスタ画像に変換することです。  
- **Which property controls the output size?** `CadRasterizationOptions.setUnitType()` が単位（例: センチメートル）を設定します。  
- **Do I need a license to run the code?** 評価には無料トライアルで動作しますが、本番環境ではライセンスが必要です。  
- **Can I choose other layouts?** はい、`setLayouts()` を使用してモデルまたはペーパー スペースのレイアウトを指定できます。  
- **What output formats are supported?** BMP のほか、オプション クラスを変更することで PNG、JPEG、TIFF などにエクスポートできます。

## **export DWG to BMP** とは何ですか？

**export DWG to BMP** とは、ベクターベースの DWG ファイルをビットマップ画像（BMP）にラスタライズすることです。レガシーシステムや画像処理パイプライン、シンプルな表示シナリオでピクセル単位の正確な表現が必要な場合に便利です。

## なぜ **Unit Type** で CAD 図面サイズを調整するのですか？

ユニットタイプを設定すると、スケーリング係数を手動で計算することなく、エクスポート画像の実際の寸法を制御できます。これにより、ビットマップが実際の測定値（例: センチメートル）と一致し、エンジニアリング図面や印刷ドキュメントにとって重要です。

## 前提条件

チュートリアルに入る前に、以下の前提条件が揃っていることを確認してください。

- **Java Development Environment** – 機能する JDK（8 以降）と IDE またはビルドツール（Maven/Gradle）。
- **Aspose.CAD for Java Library** – Aspose.CAD ライブラリをダウンロードして Java プロジェクトに統合します。ライブラリは[here](https://releases.aspose.com/cad/java/)から取得できます。

## 名前空間のインポート

Java コードで Aspose.CAD の機能にアクセスするために必要な名前空間をインクルードします。以下のインポートを追加してください。

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

それでは、ユニットタイプを使用した CAD 図面サイズの調整プロセスを段階的に分解してみましょう。

## ステップ 1: データ ディレクトリの定義

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

CAD ファイルが格納されているディレクトリへのパスを設定します。

## ステップ 2: CAD 図面の読み込み

```java
String sourceFilePath = dataDir + "sample.dwg";
Image image = Image.load(sourceFilePath);
```

Aspose.CAD の `Image` クラスを使用して CAD 図面を読み込みます。

## ステップ 3: BMP オプションの作成

```java
BmpOptions bmpOptions = new BmpOptions();
```

`BmpOptions` クラスのインスタンスを作成し、CAD レイアウトを BMP 形式でエクスポートします。

## ステップ 4: ラスタライズ オプションの構成

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

`CadRasterizationOptions` のインスタンスを作成し、ベクトル ラスタライズのために `BmpOptions` に関連付けます。

## ステップ 5: ユニットタイプの設定

```java
cadRasterizationOptions.setUnitType(UnitType.Centimeter);
```

CAD 図面の希望するユニットタイプを指定します。この例では **Centimeter** に設定しており、**adjust CAD drawing size** を行う際にエクスポート画像のサイズに直接影響します。

## ステップ 6: レイアウトの設定

```java
cadRasterizationOptions.setLayouts(new String[] { "Model" });
```

エクスポート時に考慮するレイアウトを定義します。この例では **"Model"** レイアウトを選択していますが、必要に応じてペーパー スペースのレイアウトに切り替えることも可能です。

## ステップ 7: BMP へのエクスポート

```java
String outPath = sourceFilePath + ".bmp";
image.save(outPath, bmpOptions);
```

最後に、変更した CAD 図面を BMP 形式で保存します。この手順で **export DWG to BMP** のワークフローが完了し、設定したサイズ調整が保持されます。

## 一般的な問題と解決策

| 問題 | 原因 | 対策 |
|-------|--------|-----|
| **出力画像が小さすぎる** | ユニットタイプが設定されていない、またはデフォルト（ピクセル）が使用されている | `setUnitType()` を呼び出し、目的の測定単位（例: `UnitType.Centimeter`）を指定してください。 |
| **誤ったレイアウトがエクスポートされた** | レイアウト名のタイプミス | CAD ビューアでレイアウト名を確認し、`setLayouts()` に正確な文字列を使用してください。 |
| **ライセンス例外** | 本番環境で有効なライセンスなしで実行している | FAQ に記載の手順で一時的または永続的なライセンスを適用してください。 |

## よくある質問（拡張）

**Q: Aspose.CAD for Java を他のプログラミング言語で使用できますか？**  
A: Aspose.CAD は主に Java をサポートしていますが、.NET など他の言語向けのバージョンも提供されています。

**Q: Aspose.CAD のライセンスオプションはありますか？**  
A: はい、ライセンスオプションを確認し、Aspose.CAD を[here](https://purchase.aspose.com/buy)で購入できます。

**Q: Aspose.CAD の無料トライアルは利用できますか？**  
A: もちろん、無料トライアルは[here](https://releases.aspose.com/)からアクセスできます。

**Q: Aspose.CAD for Java のサポートはどのように受けられますか？**  
A: 包括的なサポートは Aspose.CAD フォーラム[here](https://forum.aspose.com/c/cad/19)をご覧ください。

**Q: Aspose.CAD の一時ライセンスを取得できますか？**  
A: はい、一時ライセンスは[here](https://purchase.aspose.com/temporary-license/)で取得できます。

---

**最終更新日:** 2025-12-25  
**テスト環境:** Aspose.CAD for Java 24.10  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}