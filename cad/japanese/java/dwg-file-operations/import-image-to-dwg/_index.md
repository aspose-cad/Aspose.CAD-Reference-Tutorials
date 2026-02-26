---
date: 2026-01-12
description: Aspose.CAD for Java を使用して DWG ファイルに画像を追加する方法と、DWG を PDF に変換する方法を学びましょう。効率的な開発のために、ステップバイステップのガイドに従ってください。
linktitle: Import Image to DWG File Using Java
second_title: Aspose.CAD Java API
title: Aspose.CAD Java を使用して DWG ファイルに画像を簡単に追加する
url: /ja/java/dwg-file-operations/import-image-to-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD Java を使用して DWG ファイルに画像を簡単に追加する

モダンな Java アプリケーションでは、**DWG に画像を追加**することは一般的な要件です。CAD ビューアの構築、図面の自動更新、ドキュメント生成など、さまざまなシナリオで必要になります。Aspose.CAD for Java は、フル機能の CAD エンジンを必要とせずに、ラスタ画像を DWG 図面に直接埋め込むシンプルで高性能な方法を提供します。このチュートリアルでは、DWG の読み込みから結果を PDF としてエクスポートするまでの全工程を解説します。

## クイック回答
- **必要なライブラリは？** Aspose.CAD for Java  
- **PDF へのエクスポートも可能？** はい – `PdfOptions` と `CadRasterizationOptions` を使用  
- **開発時にライセンスは必要？** 無料トライアルでテスト可能。商用利用には有償ライセンスが必要です。  
- **対応 Java バージョンは？** Java 8 以上  
- **実装にかかる時間は？** 基本的な画像インポートで約 10‑15 分  

## 「add image to dwg」とは？
DWG ファイルに画像を追加するとは、ラスタ画像（PNG、JPEG など）を `CadRasterImage` オブジェクトとして図面のモデル空間に挿入することです。画像は CAD エンティティツリーの一部となり、他の CAD オブジェクトと同様に位置、スケール、クリッピングが可能です。

## Aspose.CAD for Java で画像を追加するメリット
- **CAD ソフト不要** – API が内部で DWG の解析を行います。  
- **細かい制御** が可能で、挿入位置、スケーリングベクトル、クリッピングを自由に設定できます。  
- **PDF 変換機能内蔵** で、同じワークフローで印刷可能な PDF を生成できます。  
- **クロスプラットフォーム** – Windows、Linux、macOS で動作します。  

## 前提条件
- Aspose.CAD for Java: Aspose.CAD ライブラリがインストールされていること。ダウンロードは [こちら](https://releases.aspose.com/cad/java/)。  
- Java 開発環境: JDK 8 以上とお好みの IDE（IntelliJ、Eclipse、VS Code など）。  

## パッケージのインポート
```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.*;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## 手順ガイド

### 手順 1: DWG ファイルの読み込み
DWG 図面が格納されているフォルダーを指定し、`Image.load` で読み込みます。
```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Drawing11.dwg";
Image image = Image.load(srcFile);
```

### 手順 2: ラスタ画像定義の作成
埋め込みたい外部 PNG を参照する `CadRasterImageDef` を作成します。コンストラクタには画像ファイル名とピクセル寸法を渡します。
```java
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.setObjectHandle("A3B4");
```

### 手順 3: 挿入ポイントとスケーリングベクトルの設定
挿入ポイントは画像の左下隅が表示される位置を決めます。**U** ベクトルと **V** ベクトルで水平方向・垂直方向のスケーリングを制御します。
```java
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

### 手順 4: CadRasterImage オブジェクトの作成
定義、挿入ポイント、ベクトルを組み合わせて `CadRasterImage` を生成します。必要に応じてクリッピング境界を設定し、画像の一部だけを表示させることも可能です。
```java
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.setImageDefReference("A3B4");
cadRasterImage.setDisplayFlags((short)7);
cadRasterImage.setClippingState((short)0);
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(639.5, 561.5));
```

### 手順 5: モデル空間への画像追加
`*Model_Space` ブロックにラスタ画像を挿入し、定義が保存されるように図面のオブジェクトコレクションを更新します。
```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadRasterImage);
CadBaseObject[] objs = cadImage.getObjects();
CadBaseObject[] arr = new CadBaseObject[objs.length + 1];
int ind = 0;
for (CadBaseObject obj : objs)
{
    arr[ind] = obj;
    ind++;
}
arr[ind] = cadRasterImageDef;
cadImage.setObjects(arr);
```

### 手順 6: PDF エクスポートオプションの設定（任意）
PDF 版が必要な場合は、`PdfOptions` と `CadRasterizationOptions` を組み合わせて設定します。この手順で **dwg を pdf に変換** する方法を示します。
```java
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

### 手順 7: 結果の PDF を保存
最終的に、変更された図面を PDF ファイルとしてエクスポートします。同じ `image` インスタンスを使用するため、PDF には新たに追加されたラスタ画像が反映されます。
```java
image.save((srcFile + "_generated.pdf"), pdfOptions);
```

これらの手順に従うことで、**DWG に画像を追加**する作業を迅速に行え、必要に応じて **DWG を PDF として保存** することも可能です。

## よくある問題と対策
- **画像が表示されない** – 画像ファイルパス（`road-sign-custom.png`）が正しいか、`CadRasterImageDef` に渡した寸法が画像と合致しているか確認してください。  
- **スケーリングが正しくない** – U と V ベクトルを調整します。これらはピクセルあたりの図面単位を表します。  
- **PDF が空白になる** – `CadRasterizationOptions.setDrawType` を `UseObjectColor` など適切なモードに設定してください。  

## FAQ

**Q: Aspose.CAD for Java はすべての Java 開発環境で使用できますか？**  
A: はい、ほとんどの Java 開発環境で使用可能です。

**Q: 商用プロジェクトで Aspose.CAD for Java を使用できますか？**  
A: はい、商用プロジェクトで使用できます。ライセンスの詳細は [こちら](https://purchase.aspose.com/buy) をご覧ください。

**Q: 無料トライアルはありますか？**  
A: はい、無料トライアルは [こちら](https://releases.aspose.com/) から入手できます。

**Q: Aspose.CAD for Java のサポートはどこで受けられますか？**  
A: [Aspose.CAD フォーラム](https://forum.aspose.com/c/cad/19) でサポートを受けられます。

**Q: 臨時ライセンスは取得できますか？**  
A: はい、臨時ライセンスは [こちら](https://purchase.aspose.com/temporary-license/) から取得可能です。

---

**最終更新日:** 2026-01-12  
**テスト環境:** Aspose.CAD for Java 24.11  
**作成者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}