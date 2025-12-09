---
date: 2025-11-30
description: Aspose.CAD を使用して Java で DWG ファイルにカスタム プロパティを追加する方法を学びましょう。CAD 図面の整理と情報検索を簡単に強化できます。
linktitle: Add Custom Properties to DWG Files Using Java
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java を使用して DWG ファイルにカスタム プロパティを追加する
url: /ja/java/additional-features/add-custom-properties/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java を使用したカスタムプロパティ DWG ファイルの追加

CAD 図面をプログラムで操作することは、多くの Java 開発者にとって日常的なニーズです。このチュートリアルでは、強力な Aspose.CAD for Java ライブラリを使用して **カスタムプロパティ DWG** ファイルを追加する方法を学びます。ガイドの最後までに、DWG ファイルのヘッダーに直接メタデータを注入する再利用可能なコードスニペットが手に入り、図面のカタログ化、検索、保守が容易になります。

## はじめに

Aspose.CAD for Java は、AutoCAD を必要とせずに幅広い CAD フォーマットの読み取り、編集、書き込みを可能にする、完全にマネージドされた .NET フリーのライブラリです。DWG ファイルにカスタムプロパティを追加すると、プロジェクトコード、改訂メモ、所有者情報などの追加情報を図面ファイル自体に軽量に格納できます。

## クイック回答
- **「カスタムプロパティ DWG を追加する」とは何ですか？** ユーザー定義の名前/値ペアを DWG ファイルのヘッダーメタデータに挿入することを意味します。  
- **どのライブラリがこれを処理しますか？** Aspose.CAD for Java が、これらのプロパティの読み取りと書き込みのためのシンプルな API を提供します。  
- **実装にどれくらい時間がかかりますか？** 基本的な例で通常 5‑10 分です。  
- **ライセンスは必要ですか？** 開発段階では無料トライアルで動作しますが、本番環境では商用ライセンスが必要です。  
- **他の CAD フォーマットにも対応していますか？** はい、DXF、DWF などもサポートされています。

## DWG ファイルへのカスタムプロパティ追加とは？

カスタムプロパティは DWG ヘッダーに保存されるキー‑バリューのペアです。図形ジオメトリには表示されませんが、CAD 対応アプリケーションからアクセス可能で、データ管理の向上、レポートの自動化、PLM システムとの統合が実現できます。

## なぜ Aspose.CAD をこのタスクに使うのか？

- **AutoCAD 依存なし** – 任意の OS や CI パイプラインで動作します。  
- **フル機能 API** – 品質を損なうことなく読み取り、変更、保存が可能です。  
- **高性能** – 大規模な図面でも数秒で処理します。  
- **クロスフォーマット対応** – 同じコードで DXF、DWF なども扱えます。

## 前提条件

開始する前に以下を用意してください。

- **Java Development Kit (JDK) 8 以上** がインストールされ、IDE で設定されていること。  
- **Aspose.CAD for Java** ライブラリ – 最新の JAR を [Aspose.CAD ダウンロードページ](https://releases.aspose.com/cad/java/) から取得してください。  
- 実験用の **サンプル DWG/DXF ファイル**（チュートリアルでは `conic_pyramid.dxf` を使用）。

## 名前空間のインポート

Aspose.CAD オブジェクトを使用できるように、Java クラスに必要なインポートを追加します。

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;

import java.util.Map;
```

## 手順ガイド

### 手順 1: プロジェクトのセットアップ

新規 Maven/Gradle プロジェクト（またはシンプルな IDE プロジェクト）を作成し、Aspose.CAD JAR をクラスパスに配置します。これにより `com.aspose.cad.*` パッケージがコンパイル時に利用可能になります。

### 手順 2: ファイルパスの定義

ソース図面の場所と、変更後のファイルを書き出す場所を指定します。

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
String outFile = dataDir + "AddCustomProperties_out.dxf";
```

### 手順 3: DWG ファイルの読み込み

静的メソッド `Image.load` を使用して、図面を `CadImage` オブジェクトに読み込みます。

```java
CadImage cadImage = (CadImage)Image.load(srcFile);
```

### 手順 4: カスタムプロパティの追加

メタデータを図面ヘッダーに直接挿入します。各呼び出しで新しい名前/値ペアが追加されます。

```java
cadImage.getHeader().getCustomProperties().put("CUSTOM_PROPERTY_1", "Custom property test 1");
cadImage.getHeader().getCustomProperties().put("CUSTOM_PROPERTY_2", "Custom property test 2");
cadImage.getHeader().getCustomProperties().put("CUSTOM_PROPERTY_3", "Custom property test 3");
```

> **ヒント:** プロパティ名は簡潔に（最大 31 文字）し、スペースは使用しない方が古い CAD ビューアとの互換性が保たれます。

### 手順 5: 変更後の DWG ファイルの保存

`save` メソッドを呼び出して変更を永続化します。出力ファイルには追加したカスタムプロパティが含まれます。

```java
cadImage.save(outFile);
```

### 手順 6: コードの実行

IDE もしくはコマンドラインからプログラムを実行します。正しく設定されていれば、確認メッセージが表示されます。

```java
System.out.println("\nAddCustomProperties executed successfully.");
```

## よくある問題と解決策

| 問題 | 想定原因 | 対策 |
|------|----------|------|
| **`java.lang.NoClassDefFoundError: com/aspose/cad/Image`** | Aspose.CAD JAR がクラスパスにない | JAR をプロジェクトの `libs` フォルダに追加するか、Maven/Gradle に宣言してください。 |
| **プロパティが保存ファイルに現れない** | カスタムプロパティに対応していない DWG バージョンを使用している | DWG/DXF バージョン 2000 以降を使用してください。古い形式はカスタムヘッダーを無視することがあります。 |
| **大容量ファイルで `OutOfMemoryError` が発生** | ストリーミングせずに非常に大きな図面をロードしている | `LoadOptions` オブジェクトを使用してメモリ効率の良いロードを有効にしてください。 |

## FAQ

**Q: 他の CAD ファイル形式にもカスタムプロパティを追加できますか？**  
A: はい。Aspose.CAD for Java は DXF、DWF、DGN などをサポートしており、同じ `getHeader().getCustomProperties()` API がこれらの形式でも利用できます。

**Q: Aspose.CAD for Java は主要な IDE と互換性がありますか？**  
A: 完全に対応しています。Eclipse、IntelliJ IDEA、NetBeans、さらにはシンプルなコマンドラインビルドでも動作します。

**Q: さらに多くのサンプルや詳細なドキュメントはどこで入手できますか？**  
A: 公式の [Aspose.CAD Java API リファレンス](https://reference.aspose.com/cad/java/) でクラス、メソッド、サンプルプロジェクトの一覧をご確認ください。

**Q: 購入前に Aspose.CAD for Java を試すことはできますか？**  
A: はい。30 日間の無料トライアルを [Aspose.CAD ダウンロードページ](https://releases.aspose.com/) からダウンロードできます。

**Q: 困ったときのサポートはどこで受けられますか？**  
A: Aspose コミュニティフォーラムと専用の [Aspose.CAD サポートポータル](https://forum.aspose.com/c/cad/19) が質問や解決策の共有に最適です。

---

**最終更新日:** 2025-11-30  
**テスト環境:** Aspose.CAD for Java 24.11  
**作成者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}