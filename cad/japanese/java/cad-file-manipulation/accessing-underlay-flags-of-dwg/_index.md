---
date: 2026-02-23
description: Java 用 Aspose.CAD.DWG を使用して DWG ファイルを読み込み、アンダーレイ フラグを抽出する方法を学ぶ – 開発者向けのステップバイステップ
  ガイド。
linktitle: Accessing Underlay Flags of DWG
second_title: Aspose.CAD Java API
title: aspose cad dwg – DWG をロードしてアンダーレイフラグにアクセス (Java)
url: /ja/java/cad-file-manipulation/accessing-underlay-flags-of-dwg/
weight: 11
---

 "Last Updated", "Tested With", "Author".

Make sure to keep URLs unchanged.

Also keep the shortcodes at bottom.

Now produce final output.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG ファイルの読み込みと Underlay フラグへのアクセス – Aspose.CAD for Java

現代の CAD ワークフローでは、**aspose cad dwg を使用すると DWG ファイルを素早く読み込み**、カジュアルなビューアでは見えにくい Underlay の詳細を取得できます。Java DWG ビューアの構築、バッチ処理の DWG パイプラインの自動化、GIS 連携のためのメタデータ抽出など、Aspose.CAD for Java はクリーンなコードファースト方式で実現します。このチュートリアルでは、**DWG ファイルを読み込む**手順、エンティティを反復処理する方法、そして多くの開発者が見落としがちな Underlay フラグの読み取り方法を順を追って解説します。

## Quick Answers
- **DWG を開くための主要クラスは？** `com.aspose.cad.Image.load()` は `CadImage` を返します。
- **Underlay 情報を保持するオブジェクトは？** `CadUnderlay`（または `CadDgnUnderlay` などの派生型）。
- **開発にライセンスは必要ですか？** テスト用の無料トライアルで動作しますが、製品版では商用ライセンスが必要です。
- **複数の DWG ファイルをループで処理できますか？** はい – 読み込みと反復のパターンを繰り返すだけです。
- **このアプローチは Java 11+ と互換性がありますか？** 完全に対応しています。Aspose.CAD は Java 8 から最新の LTS リリースまでサポートしています。

## aspose cad dwg – DWG ファイルの読み込み (Java)

`Image.load()` はバイナリ DWG コンテンツを読み取り、メモリ上に `CadImage` オブジェクトを生成します。ここからレイヤー、ブロック、Underlay エンティティを自分で DWG フォーマットを解析せずに調査できます。

## なぜ DWG から Underlay フラグを抽出するのか？

Underlay フラグは、外部参照（DGN や PDF の Underlay など）が図面内でどのように位置付けられ、スケーリングされ、回転されているかを示します。これらの値を把握することで、以下が可能になります。

- カスタム **java dwg viewer** で正確なビジュアルレイアウトを再現  
- Underlay をネイティブ CAD エンティティに変換し、さらに編集  
- コンプライアンスや文書化のために Underlay メタデータを含むレポートを生成  
- **Batch process dwg** ファイルを実行し、Underlay メタデータをデータベースに保存して後で分析

## 前提条件
- **Aspose.CAD Library** – [releases](https://releases.aspose.com/cad/java/) ページからダウンロードしてください。  
- **Java Development Kit** – JDK 8 以上。  
- **DWG ファイルが格納されたフォルダー**。コード中の `"Your Document Directory"` を実際のパスに置き換えて使用します。

## Import Namespaces

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadDgnUnderlay;
import com.aspose.cad.fileformats.cad.cadobjects.CadUnderlay;
import com.aspose.cad.fileformats.cad.cadobjects.UnderlayFlags;
```

## Step‑by‑Step Guide

### Step 1: Set the Resource Directory
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DWGDrawings/";
```
DWG ファイルが格納されている場所を定義します。専用フォルダーを使用することでサンプルがシンプルかつポータブルになります。

### Step 2: Load the DWG File
```java
// Input file name and path
String fileName = dataDir + "BlockRefDgn.dwg";

// Load an existing DWG file and convert it into CadImage 
CadImage image = (CadImage)Image.load(fileName);
```
ここでは `BlockRefDgn.dwg` を **load dwg file** し、`CadImage` インスタンスに読み込んで検査できる状態にします。

### Step 3: Iterate Through DWG Entities
```java
// Go through each entity inside the DWG file
for(CadBaseEntity entity : image.getEntities())
```
このループはすべてのエンティティ（ライン、円、ブロック、Underlay）を走査し、必要なものを抽出できるようにします。

### Step 4: Identify CadDgnUnderlay Entities
```java
// Check if entity is of CadDgnUnderlay type
if (entity instanceof CadDgnUnderlay)
```
Underlay フラグを取得できるのは `CadDgnUnderlay` オブジェクトだけなので、これらをフィルタリングします。

### Step 5: Access Underlay Information
```java
// Access different underlay flags 
CadUnderlay underlay = (CadUnderlay) entity;
System.out.println(underlay.getUnderlayPath());
System.out.println(underlay.getUnderlayName());
// ... (Additional underlay properties)
break;
```
`CadUnderlay` が取得できたら、パス、名前、挿入点、回転、スケール係数、そして可視性やクリッピングなどの描画オプションを示す `UnderlayFlags` 列挙体を読み取れます。

## How to load dwg files in a batch process

**batch process dwg** ファイルが必要な場合は、上記手順を `for` ループでラップし、`dataDir` 内のすべてのファイルを順に処理します。同じ `Image.load()` 呼び出しが各ファイルで機能し、抽出したフラグは CSV やデータベースに保存して downstream のレポートに利用できます。

## Common Issues & Tips
- **Null underlay path** – DWG が外部ファイルを参照しているか確認してください。参照がない場合はパスが空になります。  
- **Unsupported underlay type** – 現在 Aspose.CAD は DGN Underlay に対応しています。PDF Underlay はまだ API で公開されていません。  
- **License exceptions** – 有効なライセンスがない状態でコードを実行すると、エクスポート画像に透かしが付加されます。  
- **Performance tip:** バッチ処理時は単一の `Image` インスタンスを再利用して GC の負荷を軽減しましょう。

## Frequently Asked Questions

**Q: Aspose.CAD for Java は他の CAD ファイル形式でも使用できますか？**  
A: Aspose.CAD は主に DWG 形式に焦点を当てていますが、DXF、DWF など他の CAD 形式もサポートしています。

**Q: Aspose.CAD for Java のトライアル版はありますか？**  
A: はい、[here](https://releases.aspose.com/) から無料トライアルで機能を試すことができます。

**Q: Aspose.CAD for Java のサポートや支援はどこで受けられますか？**  
A: コミュニティサポートやディスカッションは [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) で行われています。

**Q: Aspose.CAD for Java の一時ライセンスは取得できますか？**  
A: はい、[here](https://purchase.aspose.com/temporary-license/) から一時ライセンスを取得可能です。

**Q: Aspose.CAD for Java の包括的なドキュメントはどこにありますか？**  
A: 詳細情報は [documentation](https://reference.aspose.com/cad/java/) を参照してください。

---

**Last Updated:** 2026-02-23  
**Tested With:** Aspose.CAD 24.12 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}