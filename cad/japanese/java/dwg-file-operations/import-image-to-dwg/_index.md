---
date: 2026-05-20
description: Aspose.CAD for Java を使用して DWG ファイルに画像を追加し、DWG を PDF に変換する方法を学びましょう。効率的な開発のために、ステップバイステップのガイドに従ってください。
keywords:
- add image to dwg
- convert dwg to pdf
- import image into dwg
- embed raster image dwg
- dwg file operations
linktitle: Java を使用して DWG ファイルに画像をインポート
schemas:
- author: Aspose
  dateModified: '2026-05-20'
  description: Learn how to add image to DWG files using Aspose.CAD for Java and also
    convert DWG to PDF. Follow our step-by-step guide for efficient development.
  headline: Add Image to DWG Files Effortlessly Using Aspose.CAD Java
  type: TechArticle
- description: Learn how to add image to DWG files using Aspose.CAD for Java and also
    convert DWG to PDF. Follow our step-by-step guide for efficient development.
  name: Add Image to DWG Files Effortlessly Using Aspose.CAD Java
  steps:
  - name: Load the DWG File
    text: First, point to the folder that contains your DWG drawing and load it with
      `Image.load`.
  - name: Define the Raster Image Definition
    text: The `CadRasterImageDef` class defines the external raster image resource
      to be embedded in the drawing.
  - name: Set Insertion Point and Scaling Vectors
    text: The insertion point determines where the lower‑left corner of the image
      will appear. The **U** and **V** vectors control horizontal and vertical scaling.
  - name: Create the CadRasterImage Object
    text: The `CadRasterImage` entity represents a raster picture placed in the DWG
      model space.
  - name: Add the Image to Model Space
    text: Insert the raster image into the `*Model_Space` block, then update the drawing’s
      object collection so the definition is saved.
  - name: Configure PDF Export Options (Optional)
    text: '`PdfOptions` specifies settings for saving a CAD drawing as a PDF file.
      `CadRasterizationOptions` defines how the CAD content is rasterized during PDF
      conversion.'
  - name: Save the Resulting PDF
    text: 'Finally, export the modified drawing as a PDF file. The same `image` instance
      is used, so the PDF reflects the newly added raster image. By following these
      steps, you can **add image to dwg** files quickly and also **save dwg as pdf**
      when needed, covering the most common **dwg file operations** in '
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD for Java works with any IDE that supports JDK 8+, including
      IntelliJ IDEA, Eclipse, and VS Code.
    question: Is Aspose.CAD for Java compatible with all Java development environments?
  - answer: Yes, you can use Aspose.CAD for Java for commercial projects. Visit **[here](https://purchase.aspose.com/buy)**
      for licensing details.
    question: Can I use Aspose.CAD for Java for commercial projects?
  - answer: Yes, you can access the free trial **[here](https://releases.aspose.com/)**.
    question: Is there a free trial available for Aspose.CAD for Java?
  - answer: You can seek support on the **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)**.
    question: How can I get support for Aspose.CAD for Java?
  - answer: Yes, you can get a temporary license **[here](https://purchase.aspose.com/temporary-license/)**.
    question: Can I obtain a temporary license for Aspose.CAD for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Aspose.CAD Java を使用して DWG ファイルに画像を簡単に追加
url: /ja/java/dwg-file-operations/import-image-to-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD Java を使用して DWG ファイルに画像を簡単に追加する

最新の Java アプリケーションでは、**DWG に画像を追加**することは一般的な要件です――CAD ビューアの構築、図面の自動更新、またはドキュメントの生成を行う場合でも。Aspose.CAD for Java は、フル機能の CAD エンジンを必要とせずに、ラスタ画像を DWG 図面に直接埋め込むシンプルで高性能な方法を提供します。このチュートリアルでは、DWG の読み込みから結果を PDF としてエクスポートするまでの全プロセスを順に解説し、さらに **import image into dwg** と **convert dwg to pdf** を単一のワークフローで行う方法もカバーします。

## クイック回答
- **必要なライブラリは何ですか？** Aspose.CAD for Java  
- **PDF にエクスポートすることもできますか？** Yes – use `PdfOptions` with `CadRasterizationOptions`  
- **開発にライセンスは必要ですか？** A free trial works for testing; a commercial license is required for production  
- **サポートされている Java バージョンはどれですか？** Java 8 and higher  
- **実装にどれくらい時間がかかりますか？** About 10‑15 minutes for a basic image import  

## “add image to dwg” とは何ですか？

DWG ファイルに画像を追加するとは、ラスタ画像（PNG、JPEG など）を **CadRasterImage** エンティティとして図面のモデル空間に埋め込むことを意味します。これにより、他の CAD オブジェクトと同様に位置を設定したり、スケーリングしたり、必要に応じてクリップしたりできます。画像は図面のオブジェクトテーブルに保存され、標準的な CAD ビューアで表示されます。

## DWG に画像を追加するために Aspose.CAD for Java を使用する理由

サードパーティの CAD ソフトウェアをインストールせずに、DWG ファイルにラスタ画像を埋め込むことができます。また、API は挿入ポイント、スケーリングベクトル、クリッピング境界に対してピクセル単位の正確な制御を提供します。Aspose.CAD は最大 2 GB のファイルを処理でき、**50 以上の入力および出力フォーマット**をサポートし、Windows、Linux、macOS 上で動作するため、任意の Java ベースのバックエンドに CAD 操作を統合できます。

## 前提条件
- **Aspose.CAD for Java** – 公式サイトから最新の JAR をダウンロードしてください **[here](https://releases.aspose.com/cad/java/)**。  
- **Java Development Kit** – JDK 8 以上で、お好みの IDE（IntelliJ IDEA、Eclipse、VS Code など）を使用してください。  
- 本番利用のための有効な **Aspose.CAD ライセンス**（トライアルは試用に利用可能）。

## パッケージのインポート
以下のインポートは、画像操作および PDF 変換に使用される重要な Aspose.CAD クラスを取り込みます。  
```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.*;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## ステップバイステップ ガイド

### ステップ 1: DWG ファイルの読み込み
まず、DWG 図面が格納されているフォルダーを指定し、`Image.load` で読み込みます。  
```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Drawing11.dwg";
Image image = Image.load(srcFile);
```

### ステップ 2: ラスタ画像定義の設定
`CadRasterImageDef` クラスは、図面に埋め込む外部ラスタ画像リソースを定義します。  
```java
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.setObjectHandle("A3B4");
```

### ステップ 3: 挿入ポイントとスケーリングベクトルの設定
挿入ポイントは画像の左下隅が表示される位置を決定します。**U** と **V** ベクトルはそれぞれ水平方向と垂直方向のスケーリングを制御します。  
```java
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

### ステップ 4: CadRasterImage オブジェクトの作成
`CadRasterImage` エンティティは、DWG のモデル空間に配置されたラスタ画像を表します。  
```java
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.setImageDefReference("A3B4");
cadRasterImage.setDisplayFlags((short)7);
cadRasterImage.setClippingState((short)0);
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(639.5, 561.5));
```

### ステップ 5: 画像をモデル空間に追加する
ラスタ画像を `*Model_Space` ブロックに挿入し、次に図面のオブジェクトコレクションを更新して定義を保存します。  
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

### ステップ 6: PDF エクスポートオプションの構成 (オプション)
`PdfOptions` は CAD 図面を PDF ファイルとして保存するための設定を指定します。`CadRasterizationOptions` は PDF 変換時に CAD コンテンツがどのようにラスタライズされるかを定義します。  
```java
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

### ステップ 7: 結果の PDF を保存する
最後に、変更された図面を PDF ファイルとしてエクスポートします。同じ `image` インスタンスを使用するため、PDF には新たに追加されたラスタ画像が反映されます。  
```java
image.save((srcFile + "_generated.pdf"), pdfOptions);
```

これらの手順に従うことで、**add image to dwg** ファイルを迅速に追加でき、必要に応じて **save dwg as pdf** も行えるため、最も一般的な **dwg file operations** を単一のコンパクトなルーチンでカバーできます。

## よくある問題と解決策
- **Image not appearing** – 画像ファイルパス（`road-sign-custom.png`）が正しいこと、そして画像の寸法が `CadRasterImageDef` に渡された値と一致していることを確認してください。  
- **Incorrect scaling** – U と V ベクトルを調整してください。これらはピクセルあたりの図面単位を表します。  
- **PDF looks blank** – `CadRasterizationOptions.setDrawType` が `UseObjectColor` などの適切なモードに設定されていることを確認してください。  

## よくある質問

**Q: Aspose.CAD for Java はすべての Java 開発環境と互換性がありますか？**  
A: はい、Aspose.CAD for Java は JDK 8+ をサポートする任意の IDE（IntelliJ IDEA、Eclipse、VS Code など）で動作します。

**Q: Aspose.CAD for Java を商用プロジェクトで使用できますか？**  
A: はい、商用プロジェクトで Aspose.CAD for Java を使用できます。ライセンスの詳細は **[here](https://purchase.aspose.com/buy)** をご覧ください。

**Q: Aspose.CAD for Java の無料トライアルは利用可能ですか？**  
A: はい、無料トライアルは **[here](https://releases.aspose.com/)** からアクセスできます。

**Q: Aspose.CAD for Java のサポートはどのように受けられますか？**  
A: **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)** でサポートを受けられます。

**Q: Aspose.CAD for Java の一時ライセンスを取得できますか？**  
A: はい、一時ライセンスは **[here](https://purchase.aspose.com/temporary-license/)** から取得できます。

---

**最終更新日:** 2026-05-20  
**テスト環境:** Aspose.CAD for Java 24.11  
**作者:** Aspose  

{{< blocks/products/products-backtop-button >}}

## 関連チュートリアル

- [Aspose.CAD for Java を使用した DWG の PDF またはラスタへのエクスポート](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Aspose.CAD for Java を使用した DWG ファイルへのカスタムプロパティの追加](/cad/java/additional-features/add-custom-properties/)
- [CAD を PNG として保存 – Aspose.CAD for Java を使用した CAD 図面のラスタ画像形式への変換](/cad/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}