---
date: 2026-01-12
description: Aspose.CAD for Java を使用して、DWG ファイルの自動コードページ検出を上書きしながら CAD を PDF にエクスポートする方法を学びます。エンコーディングと不正な
  CIF/MIF を処理します。
linktitle: Override Automatic Code Page Detection in DWG Files
second_title: Aspose.CAD Java API
title: CADをPDFにエクスポート – JavaでDWGファイルの自動コードページ検出を上書き
url: /ja/java/dwg-file-operations/override-code-page-detection/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD を PDF にエクスポート – Java で DWG ファイルの自動コードページ検出をオーバーライドする方法

## はじめに

この包括的ガイドでは、**CAD を PDF にエクスポート**しながら、DWG ファイル内のテキストが破損する原因となる自動コードページ検出をオーバーライドする方法を紹介します。Aspose.CAD for Java はエンコーディングを細かく制御でき、破損した CIF/MIF データを復元し、信頼性の高い PDF 出力を実現します。バッチコンバータを構築する場合でも、CAD 処理を大規模な Java アプリケーションに統合する場合でも、以下の手順でワークフロー全体を案内します。

## クイック回答
- **「コードページをオーバーライドする」とは何ですか？** Aspose.CAD に特定の文字エンコーディングを使用させ、推測による自動判定を無効にします。
- **DWG を直接 PDF にエクスポートできますか？** はい – 正しいコードページを設定すれば、CAD 画像を PDF として保存できます。
- **日本語テキストに適したエンコーディングはどれですか？** `CodePages.Japanese` と `MifCodePages.Japanese` が正しい選択です。
- **本番環境での使用にライセンスは必要ですか？** 商用ライセンスが必要です。テスト用の一時ライセンスも利用可能です。
- **必要な Aspose.CAD のバージョンは？** `LoadOptions` と `PdfOptions` をサポートする最近のバージョンであれば問題ありません。

## 「CAD を PDF にエクスポート」とは？
CAD を PDF にエクスポートすると、ベクターベースの CAD 図面が広くサポートされる固定レイアウトのドキュメント形式に変換されます。生成された PDF は線画、レイヤー、テキストを保持しつつ、図面を簡単に共有、印刷、または他のアプリケーションに埋め込むことができます。

## なぜ自動コードページ検出をオーバーライドするのか？
DWG ファイルはレガシーなコードページでテキストを保存していることが多く、Aspose.CAD の自動検出がこれらのバイト列を誤って解釈すると文字化けが発生します。コードページを手動で指定することで、特に日本語、キリル文字、アラビア文字などの非ラテン文字が正しく表示され、エクスポートされた PDF でも意図した通りのテキストが得られます。

## 前提条件
- **Java 開発環境** – JDK 8 以上とお好みの IDE。
- **Aspose.CAD for Java** – 公式サイトからライブラリをダウンロード [here](https://releases.aspose.com/cad/java/)。
- **DWG サンプルファイル** – 同梱の `SimpleEntities.dwg` または変換したい任意の DWG を使用してください。

## パッケージのインポート
Java プロジェクトで必要な Aspose.CAD クラスをインポートします。

```java
import com.aspose.cad.CodePages;
import com.aspose.cad.Image;
import com.aspose.cad.LoadOptions;
import com.aspose.cad.MifCodePages;
import com.aspose.cad.fileformats.cad.CadImage;
```

## 手順ガイド

### 手順 1: Java プロジェクトのセットアップ
Maven または Gradle プロジェクトを作成し、Aspose.CAD JAR をクラスパスに追加します。この手順により、IDE がインポートしたクラスを解決できるようになります。

### 手順 2: 指定したコードページで DWG ファイルを読み込む
Aspose.CAD に使用するエンコーディングと、破損した CIF/MIF データの復元を試みるかどうかを指示します。

```java
String SourceDir = "Your Document Directory";
String dwgPathToFile = SourceDir + "SimpleEntites.dwg";
LoadOptions opts = new LoadOptions();
opts.setSpecifiedEncoding(CodePages.Japanese);
opts.setSpecifiedMifEncoding(MifCodePages.Japanese);
opts.setRecoverMalformedCifMif(false);
CadImage cadImage = (CadImage) Image.load(dwgPathToFile, opts);
```

### 手順 3: CAD 画像を PDF にエクスポート
正しいコードページが適用された状態で、図面を安全にエクスポートできます。`PdfOptions` オブジェクトを使って PDF 出力（圧縮、ラスター化など）を細かく調整できます。

```java
// Perform export or other operations with cadImage
// For example, exporting to PDF
PdfOptions pdfOptions = new PdfOptions();
cadImage.save("output.pdf", pdfOptions);
```

### 手順 4: 成功を確認
コンソールにシンプルなメッセージを出力し、例外が発生せずに処理が完了したことを確認します。

```java
System.out.println("OverrideAutomaticCodePageDetectionDwg executed successfully");
```

必要に応じてソースパスと出力名を変更すれば、複数の DWG ファイルに対して同様の手順を繰り返すことができます。

## よくある問題と解決策
- **文字化けがまだ残る:** `specifiedEncoding` が元の DWG のコードページと一致しているか再確認してください。必要に応じて別の `CodePages` 列挙体を試します。
- **`cadImage.save` で `NullPointerException` が発生:** DWG ファイルが正しく読み込めているか確認し、パスとファイル権限をチェックしてください。
- **PDF のサイズが大きい:** `PdfOptions` で圧縮を有効にします（例: `pdfOptions.setCompress(true)`）。

## FAQ

**Q1: Aspose.CAD はすべての DWG バージョンに対応していますか？**  
A1: Aspose.CAD は AutoCAD 2018 以前の広範な DWG バージョンをサポートしています。

**Q2: 商用プロジェクトで Aspose.CAD を使用できますか？**  
A2: はい、本番環境で使用するには商用ライセンスが必要です。ライセンスは [here](https://purchase.aspose.com/buy) から取得できます。

**Q3: 無料トライアル版には制限がありますか？**  
A3: トライアル版はサイズや機能に制限があります。詳細は公式ドキュメントをご参照ください。

**Q4: Aspose.CAD のサポートはどこで受けられますか？**  
A4: コミュニティの [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) で質問や議論が可能です。

**Q5: テスト用の一時ライセンスは入手できますか？**  
A5: はい、[here](https://purchase.aspose.com/temporary-license/) から一時ライセンスをリクエストできます。

---

**最終更新日:** 2026-01-12  
**テスト環境:** Aspose.CAD for Java 24.11（執筆時点での最新バージョン）  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}