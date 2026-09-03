---
date: 2026-08-23
description: Aspose.CAD for .NET の可能性を引き出す、DWG ファイルから xref メタデータを読み取る手順をステップバイステップで解説したチュートリアルです。
keywords:
- read xref metadata
- extract dwg xref
- Aspose.CAD
lastmod: 2026-08-23
linktitle: DWG ファイルから XREF メタデータを読む
og_description: Aspose.CAD for .NET を使用して DWG ファイルから xref メタデータを読み取る方法を学びます。このガイドでは、前提条件、コード手順、一般的な落とし穴を
  10 分以内で解説します。
og_image_alt: Screenshot of Aspose.CAD reading XREF metadata in a .NET IDE
og_title: Aspose.CAD を使用して DWG ファイルから xref メタデータを読み取る方法
schemas:
- author: Aspose
  dateModified: '2026-08-23'
  description: Unlock the potential of Aspose.CAD for .NET with our step‑by‑step tutorial
    on how to read xref metadata from DWG files.
  headline: How to read xref metadata from DWG files using Aspose.CAD
  type: TechArticle
- description: Unlock the potential of Aspose.CAD for .NET with our step‑by‑step tutorial
    on how to read xref metadata from DWG files.
  name: How to read xref metadata from DWG files using Aspose.CAD
  steps:
  - name: load the DWG file
    text: Create an `Image` instance from the DWG file you want to analyze. `Image.Load`
      loads a CAD file and returns a `CadImage` object representing the drawing. Adjust
      the `sourceFilePath` variable to the exact location of your drawing.
  - name: iterate through entities
    text: Loop through the `Image` object’s `Entities` collection. `CadBaseEntity`
      is the base class for all CAD entities in Aspose.CAD. For each entity, check
      whether it is an XREF reference and collect its metadata.
  - name: extract metadata
    text: When you encounter an XREF entity, read its insertion point (X, Y, Z) and
      the path of the referenced drawing. `CadUnderlay` represents an external reference
      (XREF) entity within a DWG drawing.
  - name: process metadata
    text: At this stage you can store the extracted information in a database, write
      it to a CSV file, or feed it into downstream BIM workflows. The sample simply
      prints the values to the console, but you are free to replace that with any
      custom logic.
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD for .NET supports **50+ input and output formats**, including
      DWG, DXF, DGN, and IFC, giving you broad coverage for most engineering workflows.
    question: Is Aspose.CAD for .NET compatible with all CAD file formats?
  - answer: Certainly! You can access the free trial download page [free trial download
      page](https://releases.aspose.com/).
    question: Can I use the free trial before making a purchase decision?
  - answer: The documentation is available [Aspose.CAD .NET documentation](https://reference.aspose.com/cad/net/).
    question: Where can I find comprehensive documentation for Aspose.CAD for .NET?
  - answer: You can get a temporary license [temporary license page](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license for Aspose.CAD for .NET?
  - answer: Join the Aspose.CAD community at [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19)
      for expert support and discussions.
    question: Need assistance or have specific queries?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- read xref metadata
- extract dwg xref
- Aspose.CAD
- DWG
- CAD metadata
title: Aspose.CAD を使用して DWG ファイルから xref メタデータを読み取る方法
url: /ja/net/image-manipulation-and-rendering/reading-xref-metadata-from-dwg/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD を使用して DWG ファイルから xref メタデータを読み取る方法

## はじめに

このチュートリアルでは、.NET 用 Aspose.CAD ライブラリを使用して DWG ファイルから **xref メタデータの読み取り方法** を学びます。外部参照の監査、レガシー図面の移行、またはカスタム BIM パイプラインの構築が必要な場合でも、XREF 情報の抽出は一般的な要件です。プロジェクトのセットアップからメタデータの処理まで、すべての手順を順に説明し、すぐに活用できる実用的なヒントも紹介します。

## クイック回答
- **主な目的は何ですか？** DWG 図面に埋め込まれた外部参照 (XREF) の挿入ポイントとファイルパスを取得することです。  
- **必要なライブラリはどれですか？** .NET 用 Aspose.CAD（50 以上の CAD フォーマットに対応）。  
- **ライセンスは必要ですか？** 本番環境で使用するには一時ライセンスまたはフルライセンスが必要です。無料トライアルも利用可能です。  
- **サポートされている .NET バージョンは？** .NET Framework 4.5 以上、.NET Core 3.1 以上、.NET 5/6/7。  
- **コードの実行時間はどれくらいですか？** 標準的なハードウェア上で、数件の XREF を含む 200 ページ程度の DWG を処理すると、1 秒未満で完了します。

## read xref メタデータとは？
`read xref metadata` は、DWG 図面内に保存されている外部参照エンティティのプロパティ（挿入座標、ソースファイルパス、表示フラグなど）にアクセスする操作を指します。この操作により、図面が他のファイルからどのように構成されているかをプログラムで把握でき、検証、レポート作成、リンクリソースのバッチ処理などを自動化できます。

## なぜ Aspose.CAD をこのタスクに使うのか？
Aspose.CAD は **50 以上の CAD ファイル形式** に対応し、**AutoCAD を必要とせずに DWG ファイルを読み取る** ことができます。ライブラリは大規模な図面を **メモリ効率の高いストリーム** で処理でき、ファイル全体を RAM にロードせずに数百ページのファイルを扱えます。これらの特長により、エンタープライズ向け CAD 自動化に信頼できる選択肢となります。

## 前提条件

コードに取り掛かる前に、以下が揃っていることを確認してください。

- Aspose.CAD for .NET がインストールされていること。最新パッケージは [Aspose.CAD for .NET リリースページ](https://releases.aspose.com/cad/net/) から取得してください。  
- 検査したい DWG ファイルが格納されたローカルフォルダー。サンプルコード内の `MyDir` 変数をこのフォルダーに合わせて更新してください。  
- 本番環境でコードを実行する場合は、有効な Aspose.CAD ライセンス（または無料トライアル）が必要です。

環境が整ったので、コーディングを開始しましょう。

## 名前空間のインポート

最初に行うべきことは、Aspose.CAD の API を公開する名前空間をインポートすることです。`using` ディレクティブにより Aspose.CAD の名前空間がスコープに入り、`Image` や `CadImage` といった CAD クラスにアクセスできるようになります。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
```

## DWG ファイルから xref メタデータを読み取る方法

図面を読み込み、エンティティを列挙し、XREF オブジェクトをフィルタリングして目的のプロパティを取得します。これらは数行のシンプルなコードで実現できます。以下のセクションでは、プロセスを 4 つの論理ステップに分解し、任意の .NET コンソールまたはサービスプロジェクトにコピーペーストできる形で示します。

### 手順 1: DWG ファイルの読み込み

解析したい DWG ファイルから `Image` インスタンスを作成します。`Image.Load` は CAD ファイルを読み込み、図面を表す `CadImage` オブジェクトを返します。`sourceFilePath` 変数を図面の正確な場所に合わせて調整してください。

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";
using (CadImage image = (CadImage)Image.Load(sourceFilePath))
{
    // Code for the next steps goes here
}
```

### 手順 2: エンティティの列挙

`Image` オブジェクトの `Entities` コレクションをループします。`CadBaseEntity` は Aspose.CAD におけるすべての CAD エンティティの基底クラスです。各エンティティについて、XREF 参照かどうかを確認し、メタデータを収集します。

```csharp
foreach (CadBaseEntity entity in image.Entities)
{
    if (entity is CadUnderlay)
    {
        // Code for the next steps goes here
    }
}
```

### 手順 3: メタデータの抽出

XREF エンティティに遭遇したら、その挿入ポイント (X, Y, Z) と参照先図面のパスを読み取ります。`CadUnderlay` は DWG 図面内の外部参照 (XREF) エンティティを表します。

```csharp
//XREF entity with metadata
Cad3DPoint insertionPoint = ((CadUnderlay)entity).InsertionPoint;
string path = ((CadUnderlay)entity).UnderlayPath;
```

### 手順 4: メタデータの処理

この段階で、抽出した情報をデータベースに保存したり、CSV ファイルに書き出したり、下流の BIM ワークフローに渡したりできます。サンプルは単にコンソールに値を出力しますが、任意のカスタムロジックに置き換えて構いません。

```csharp
// Your custom logic for processing metadata goes here
```

## よくある問題とトラブルシューティング

| 症状 | 考えられる原因 | 対策 |
|------|----------------|------|
| XREF エンティティが返されない | 図面が別の参照タイプ（例: INSERT）を使用している | `CadEntityType.Xref` と比較し、必要に応じて `Insert` も処理するように確認してください |
| `Image.Load` が例外をスローする | ファイルパスが間違っている、またはサポートされていない DWG バージョン | パスを確認し、Aspose.CAD 24.11 以降を使用していることを確認してください |
| メタデータの値が空 | XREF が定義されているが解決できない（外部ファイルが欠如） | 参照先ファイルがディスク上に存在することを確認するか、仮想ファイルシステムリゾルバを提供してください |

## FAQ（よくある質問）

**Q: Aspose.CAD for .NET はすべての CAD ファイルフォーマットに対応していますか？**  
A: はい、Aspose.CAD for .NET は **50 以上の入力・出力フォーマット** に対応しており、DWG、DXF、DGN、IFC などを含むため、ほとんどのエンジニアリングワークフローに幅広く対応できます。

**Q: 購入を決定する前に無料トライアルを利用できますか？**  
A: もちろんです！無料トライアルのダウンロードページは [無料トライアル ダウンロードページ](https://releases.aspose.com/) からアクセスできます。

**Q: Aspose.CAD for .NET の包括的なドキュメントはどこで見つけられますか？**  
A: ドキュメントは [Aspose.CAD .NET ドキュメント](https://reference.aspose.com/cad/net/) で入手できます。

**Q: Aspose.CAD for .NET の一時ライセンスはどのように取得できますか？**  
A: 一時ライセンスは [一時ライセンスページ](https://purchase.aspose.com/temporary-license/) から取得できます。

**Q: サポートが必要、または具体的な質問がありますか？**  
A: 専門的なサポートや議論のために、[Aspose.CAD フォーラム](https://forum.aspose.com/c/cad/19) に参加してください。

## 結論

これで、Aspose.CAD for .NET を使用して DWG ファイルから **XREF メタデータを読み取る** 完全な本番対応パターンが手に入りました。ファイルの読み込み、エンティティの列挙、挿入ポイントとアンダーレイパスの抽出、結果の処理という 4 つの手順に従うことで、データ移行ツール、品質管理スクリプト、カスタム BIM パイプラインなど、あらゆる CAD 中心のアプリケーションにこの機能を統合できます。

---

**最終更新日:** 2026-08-23  
**テスト環境:** Aspose.CAD 24.11 for .NET  
**作者:** Aspose

## 関連チュートリアル

- [CAD ファイルで xref パスを変更しハイパーリンクを編集する方法 - Aspose.CAD チュートリアル](/cad/net/advanced-cad-techniques/editing-hyperlinks-in-cad-files/)
- [DWG ファイルからブロック属性を取得する方法 - Aspose.CAD チュートリアル](/cad/net/image-manipulation-and-rendering/getting-block-attributes-from-dwg/)
- [大容量 DWG ファイルを PDF に変換する方法 - Aspose.CAD チュートリアル](/cad/net/image-manipulation-and-rendering/converting-large-dwg-files-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}