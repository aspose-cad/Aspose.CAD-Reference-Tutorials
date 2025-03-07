---
title: Aspose.CAD での CAD の保存時のタイムアウト
linktitle: 保存時にタイムアウトを設定する
second_title: Aspose.CAD Java API
description: Aspose.CAD を使用して Java アプリケーションのパフォーマンスを向上させる方法を学びます。 CAD 図面の保存時にタイムアウトを設定します。ステップバイステップのガイドに従ってください。
weight: 15
url: /ja/java/other-cad-operations/put-timeout-on-save/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD での CAD の保存時のタイムアウト

## 導入

Aspose.CAD for Java を使用して保存時にタイムアウトを設定するチュートリアルへようこそ。このガイドでは、アプリケーションのパフォーマンスを向上させるために CAD 図面を保存するためのタイムアウトを設定するプロセスについて説明します。 Aspose.CAD for Java は、Java アプリケーションで CAD ファイルをシームレスに操作できるようにする強力なライブラリです。

## 前提条件

チュートリアルに入る前に、次の前提条件が満たされていることを確認してください。
-  Aspose.CAD for Java ライブラリ: Aspose.CAD for Java ライブラリがプロジェクトに統合されていることを確認します。ライブラリはからダウンロードできます。[Webサイト](https://releases.aspose.com/cad/java/).
- 開発環境: 必要なツールと依存関係をすべて備えた Java 開発環境をセットアップします。

## パッケージのインポート

まず、必要なパッケージを Java プロジェクトにインポートします。 Java ファイルの先頭に次の行を追加します。

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterruptionTokenSource;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.concurrent.TimeUnit;
```

次に、サンプル コードを段階的な手順に分解してみましょう。

## ステップ 1: ソース ディレクトリと出力ディレクトリを設定する

```java
final String SourceDir = Utils.getDataDir_DWGDrawings();
final String OutputDir = Utils.getDataDir_Output();
```

CAD 図面のソース ディレクトリと出力ディレクトリが正しいことを確認してください。

## ステップ 2: 中断トークン ソースの作成

```java
final InterruptionTokenSource source = new com.aspose.cad.InterruptionTokenSource();
```

保存操作中の中断を管理するには、中断トークン ソースを初期化します。

## ステップ 3: CAD 図面をロードする

```java
final CadImage cadImageBig = (CadImage)Image.load(SourceDir + "Drawing11.dwg");
```

CAD 図面を`CadImage`物体。

## ステップ 4: ラスター化オプションを構成する

```java
CadRasterizationOptions rasterizationOptionsBig = new CadRasterizationOptions();
rasterizationOptionsBig.setPageWidth(cadImageBig.getSize().getWidth() / 2);
rasterizationOptionsBig.setPageHeight(cadImageBig.getSize().getHeight() / 2);
```

CAD 図面のラスタライズ オプションを構成します。

## ステップ 5: PDF オプションを構成する

```java
final PdfOptions CADfBig = new PdfOptions();
CADfBig.setVectorRasterizationOptions(rasterizationOptionsBig);
CADfBig.setInterruptionToken(source.getToken());
```

ベクトル ラスタライズ オプションと中断トークンを使用して PDF オプションを設定します。

## ステップ 6: タイムアウトを指定して図面を保存する

```java
cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
```

指定されたタイムアウトを使用して、CAD 図面を PDF ファイルに保存します。

## ステップ 7: 割り込みの処理

```java
java.lang.Thread thread = new java.lang.Thread(new Runnable() {
    @Override
    public void run() {
        try {
            cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
        } catch (Throwable th) {
            System.out.println("interrupted !!!");
        }
    }
});
thread.start();
TimeUnit.SECONDS.sleep(3);
source.interrupt();
thread.join();
```

保存操作を処理するスレッドを作成し、指定されたタイムアウト後に中断します。

## 結論

おめでとう！ Aspose.CAD for Java を使用して保存時にタイムアウトを設定する方法を学習しました。この機能により、CAD 関連アプリケーションの効率が大幅に向上します。

## よくある質問

### Q1: Java 用 Aspose.CAD をダウンロードするにはどうすればよいですか?

 A1: からダウンロードできます。[リリースページ](https://releases.aspose.com/cad/java/).

### Q2: Aspose.CAD for Java のドキュメントはどこで見つけられますか?

 A2: を参照してください。[ドキュメンテーション](https://reference.aspose.com/cad/java/)包括的な情報については。

### Q3: 無料トライアルはありますか?

A3: はい、以下から無料トライアルを利用できます。[このリンク](https://releases.aspose.com/).

### Q4: 仮免許はどのように取得すればよいですか?

 A4: 訪問[ここ](https://purchase.aspose.com/temporary-license/)一時ライセンスの詳細については、

### Q5: サポートが必要ですか、それとも質問がありますか?

 A5: に向かってください。[Aspose.CAD フォーラム](https://forum.aspose.com/c/cad/19)コミュニティサポートのために。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
