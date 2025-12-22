---
date: 2025-12-22
description: Aspose.CAD for Java を使って DWG ファイルを読み込み、アンダーレイ情報を抽出する方法を学びましょう – アンダーレイ
  フラグを網羅したステップバイステップ ガイドです。
linktitle: Accessing Underlay Flags of DWG
second_title: Aspose.CAD Java API
title: DWG ファイルの読み込みとアンダーレイ フラグへのアクセス – Aspose.CAD for Java
url: /ja/java/cad-file-manipulation/accessing-underlay-flags-of-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG ファイルの読み込みとアンダーレイ フラグへのアクセス – Aspose.CAD for Java

モダンな CAD ワークフローでは、**DWG ファイルの読み込み** を迅速に行い、アンダーレイの詳細を取得することが一般的な要件です。ビューアの構築、バッチ処理の自動化、GIS 連携のためのメタデータ抽出など、Aspose.CAD for Java を使用すれば、コードファーストでシンプルに実現できます。このチュートリアルでは、**DWG ファイルの読み込み**、エンティティの反復処理、そして多くの開発者が見落としがちなアンダーレイ フラグの取得手順を詳しく解説します。

## Quick Answers
- **DWG を開くための主要クラスは何ですか？** `com.aspose.cad.Image.load()` が `CadImage` を返します。  
- **アンダーレイ情報を保持しているオブジェクトはどれですか？** `CadUnderlay`（`CadDgnUnderlay` などの派生型）。  
- **開発時にライセンスは必要ですか？** テスト用の無料トライアルで動作しますが、本番環境では商用ライセンスが必要です。  
- **複数の DWG ファイルをループで処理できますか？** はい、ロード‑アンド‑イテレートのパターンを繰り返すだけです。  
- **この手法は Java 11+ に対応していますか？** 完全に対応しています。Aspose.CAD は Java 8 から最新の LTS リリースまでサポートしています。

## Aspose.CAD における「load dwg file」とは？
`Image.load()` は DWG のバイナリ内容を読み取り、メモリ上に `CadImage` オブジェクトを生成します。これにより、レイヤー、ブロック、アンダーレイ エンティティなどを DWG の内部構造を意識せずに操作できます。

## DWG からアンダーレイ フラグを抽出する理由
アンダーレイ フラグは、外部参照（DGN や PDF アンダーレイなど）が図面内でどのように配置、スケーリング、回転されているかを示します。これらの値を取得することで、次のことが可能になります。

- カスタムビューアで正確なビジュアルレイアウトを再現できる。  
- アンダーレイをネイティブ CAD エンティティに変換し、さらなる編集が可能になる。  
- コンプライアンスや文書化のために、アンダーレイ メタデータを含むレポートを生成できる。

## 前提条件
- **Aspose.CAD ライブラリ** – [リリースページ](https://releases.aspose.com/cad/java/) からダウンロード。  
- **Java Development Kit** – JDK 8 以上。  
- **DWG ファイルが格納されたフォルダー**。コード中の `"Your Document Directory"` を実際のパスに置き換えてください。

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
DWG ファイルが保存されている場所を定義します。専用フォルダーを使用することで、サンプルがクリーンかつポータブルになります。

### Step 2: Load the DWG File
```java
// Input file name and path
String fileName = dataDir + "BlockRefDgn.dwg";

// Load an existing DWG file and convert it into CadImage 
CadImage image = (CadImage)Image.load(fileName);
```
ここでは **load dwg file** `BlockRefDgn.dwg` を `CadImage` インスタンスに読み込み、検査できる状態にします。

### Step 3: Iterate Through DWG Entities
```java
// Go through each entity inside the DWG file
for(CadBaseEntity entity : image.getEntities())
```
このループはすべてのエンティティ（線、円、ブロック、アンダーレイ）を走査し、必要なものを抽出できるようにします。

### Step 4: Identify CadDgnUnderlay Entities
```java
// Check if entity is of CadDgnUnderlay type
if (entity instanceof CadDgnUnderlay)
```
`CadDgnUnderlay` オブジェクトのみが対象のアンダーレイ フラグを保持しているため、これらだけをフィルタリングします。

### Step 5: Access Underlay Information
```java
// Access different underlay flags 
CadUnderlay underlay = (CadUnderlay) entity;
System.out.println(underlay.getUnderlayPath());
System.out.println(underlay.getUnderlayName());
// ... (Additional underlay properties)
break;
```
`CadUnderlay` が取得できたら、パス、名前、挿入ポイント、回転、スケール係数、そして可視性やクリッピングなどの描画オプションを示す `UnderlayFlags` 列挙体を読み取ります。

## Common Issues & Tips
- **アンダーレイ パスが null** – DWG が外部ファイルを参照していることを確認してください。参照がない場合はパスが空になります。  
- **未対応のアンダーレイ タイプ** – 現在 Aspose.CAD は DGN アンダーレイをサポートしていますが、PDF アンダーレイは API 経由ではまだ利用できません。  
- **ライセンス例外** – 有効なライセンスがない状態で実行すると、エクスポート画像に透かしが付加されます。

## Frequently Asked Questions

**Q: Aspose.CAD for Java は他の CAD ファイル形式でも使用できますか？**  
A: Aspose.CAD は主に DWG 形式に焦点を当てていますが、DXF、DWF など他の CAD 形式もサポートしています。

**Q: Aspose.CAD for Java のトライアル版はありますか？**  
A: はい、[こちら](https://releases.aspose.com/) から無料トライアルで機能を試すことができます。

**Q: Aspose.CAD for Java のサポートや支援はどこで受けられますか？**  
A: コミュニティサポートやディスカッションは [Aspose.CAD フォーラム](https://forum.aspose.com/c/cad/19) でご利用ください。

**Q: Aspose.CAD for Java 用の一時ライセンスはありますか？**  
A: はい、[こちら](https://purchase.aspose.com/temporary-license/) から一時ライセンスを取得できます。

**Q: Aspose.CAD for Java の包括的なドキュメントはどこにありますか？**  
A: 詳細情報は [ドキュメント](https://reference.aspose.com/cad/java/) を参照してください。

---

**Last Updated:** 2025-12-22  
**Tested With:** Aspose.CAD 24.12 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}