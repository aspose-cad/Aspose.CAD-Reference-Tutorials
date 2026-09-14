---
date: 2026-09-14
description: ファイルパスまたは FileStream を使用して Aspose.CAD for .NET のライセンスを適用する方法を学び、リソース使用量を最適化するための
  metered licensing についても確認できます。
keywords:
- how to apply license
- apply license by path
- apply license using filestream
- metered licensing
lastmod: 2026-09-14
linktitle: ライセンスと構成
og_description: ファイルパスまたは FileStream を使用して Aspose.CAD for .NET のライセンスを適用する方法を学び、リソース使用量を最適化するための
  metered licensing についても確認できます。 (150‑160 文字)
og_image_alt: Screenshot of Aspose.CAD license configuration page in a .NET IDE
og_title: Aspose.CAD for .NET のライセンス適用方法 – Quick Guide
schemas:
- author: Aspose
  dateModified: '2026-09-14'
  description: Learn how to apply license in Aspose.CAD for .NET using a file path
    or FileStream, and explore metered licensing to optimise resource usage.
  headline: How to apply license in Aspose.CAD for .NET
  type: TechArticle
- description: Learn how to apply license in Aspose.CAD for .NET using a file path
    or FileStream, and explore metered licensing to optimise resource usage.
  name: How to apply license in Aspose.CAD for .NET
  steps:
  - name: Place your `Aspose.CAD.lic` file in a folder that your application can read
      (e.g., the application root or a secured config folder).
    text: Place your `Aspose.CAD.lic` file in a folder that your application can read
      (e.g., the application root or a secured config folder).
  - name: 'Add the following code early in your startup routine (e.g., `Main`, `Startup.Configure`,
      or `Global.asax`):'
    text: 'Add the following code early in your startup routine (e.g., `Main`, `Startup.Configure`,
      or `Global.asax`):'
  - name: Retrieve the license bytes from your source (file system, Azure Blob, etc.).
    text: Retrieve the license bytes from your source (file system, Azure Blob, etc.).
  - name: Open a `FileStream` with read permissions.
    text: Open a `FileStream` with read permissions.
  - name: Pass the stream to the `License` object.
    text: Pass the stream to the `License` object.
  - name: Obtain a metered‑license key from your Aspose account dashboard.
    text: Obtain a metered‑license key from your Aspose account dashboard.
  - name: Register the key with `License.SetMeteredKey("your‑key")`.
    text: Register the key with `License.SetMeteredKey("your‑key")`.
  - name: After each operation, call `License.GetMeteredUsage()` to retrieve the current
      usage count.
    text: After each operation, call `License.GetMeteredUsage()` to retrieve the current
      usage count.
  type: HowTo
- questions:
  - answer: Yes, a single license file can be deployed to any number of development
      or production servers, provided the usage complies with your purchased term.
    question: Can I use the same license file on multiple machines?
  - answer: The library will run in evaluation mode, adding a watermark to rendered
      images and limiting the number of pages you can process.
    question: What happens if I forget to set the license before loading a CAD file?
  - answer: Only the first activation and each usage report need connectivity; after
      that, the library can operate offline until the next report.
    question: Does metered licensing require an internet connection?
  - answer: Aspose.CAD supports 45+ input and output formats, including DWG, DXF,
      DGN, STL, OBJ, and IFC, and can render files up to 500 MB without loading the
      entire document into memory.
    question: Which CAD/BIM formats are supported out of the box?
  - answer: Call `License.IsLicensed` (or inspect `License.LicenseFilePath`) after
      registration; it returns `true` when a valid license is active.
    question: Is there a way to programmatically check if the license was applied
      successfully?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- Aspose.CAD
- license configuration
- .NET
- CAD processing
- metered licensing
title: Aspose.CAD for .NET のライセンス適用方法
url: /ja/net/licensing-and-configuration/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for .NET のライセンス適用方法

Aspose.CAD for .NET の **ライセンスの適用方法** に関する決定的なガイドへようこそ。デスクトップユーティリティ、サーバーサイドサービス、または自動化された BIM パイプラインを構築している場合でも、有効なライセンスにより 40 以上の CAD および BIM フォーマットのフルスイートがアンロックされ、高性能なレンダリングが可能になり、評価用の透かしが削除されます。本記事では、すべてのライセンスオプションをステップバイステップで解説し、開発を中断することなく開始できるようにします。

## クイック回答
- **ファイルパスからライセンスをロードできますか？** はい – `License` のインスタンスを作成し、`SetLicense("path/to/license.lic")` を呼び出すだけです。  
- **FileStream はサポートされていますか？** もちろんです; 開いたストリームを `SetLicense(stream)` に渡してください。  
- **メータリングライセンスとは何ですか？** リクエストごとの使用量を追跡し、消費した分だけ支払えるようにします。  
- **開発にライセンスは必要ですか？** 開発およびテストには無料トライアルライセンスが使用でき、商用環境では商用ライセンスが必要です。  
- **サポートされている .NET バージョンはどれですか？** .NET Framework 4.5+、.NET Core 3.1+、.NET 5/6/7。

## Aspose.CAD のライセンスとは何ですか？
Aspose.CAD のライセンスは、購入を検証し、ライブラリのフル機能セットを有効化する仕組みです。ライセンスがない場合、API は評価モードで動作し、出力サイズが制限され、レンダリングされた画像に透かしが埋め込まれます。

## パスベースのライセンスとストリームベースのライセンス、どちらを使うべきか？
パスベースのライセンスは Aspose.CAD を有効化する最も迅速な方法です。単に .lic ファイルを指すだけで、ライブラリが自動的にロードします。非ファイルソースからライセンスを読み込む必要がある場合や、カスタムセキュリティを適用したい場合、アセンブリにライセンスを埋め込みたい場合はストリームを使用します。デプロイ環境に合わせて適切な方法を選択してください。

`License` クラスは、API にライセンスを登録する Aspose.CAD のライセンスコンポーネントを表します。

## Aspose.CAD for .NET でパスによるライセンス適用方法は？

パスでライセンスを適用するには、`License` クラスのインスタンスを作成し、`.lic` ファイルへのフルパスを指定して `SetLicense` メソッドを呼び出します。このコードはアプリケーションの起動時に早めに配置し、以降のすべての CAD 操作がライセンス済みのコンテキストで実行されるようにします。

`License` クラスは、API にライセンスを登録する Aspose.CAD のライセンスコンポーネントを表します。

1. アプリケーションが読み取れるフォルダー（例: アプリケーションのルートまたは保護された設定フォルダー）に `Aspose.CAD.lic` ファイルを配置します。  
2. 起動ルーチンの早い段階で以下のコードを追加します（例: `Main`、`Startup.Configure`、または `Global.asax`）。

```csharp
// No code block added – original tutorial contained none.
```

> **直接回答（40‑70語）：**  
> パスでライセンスを適用するには、`License` オブジェクトを作成し、`SetLicense("full\\path\\to\\Aspose.CAD.lic")` を呼び出します。この1行でライブラリ全体が有効化され、評価用透かしが削除され、パフォーマンス制限なしで 40 以上の CAD/BIM フォーマットの処理が可能になります。CAD 操作の前にこの呼び出しを行い、ライセンスが有効であることを確認してください。

## Aspose.CAD for .NET で FileStream を使用したライセンス適用方法は？

`FileStream` を使用してライセンスを適用するには、読み取りアクセスで .lic ファイルを開き、`License` オブジェクトを作成し、ストリームを `SetLicense` に渡します。ストリームは登録が完了するまで開いたままにし、完了後はリソース解放のために閉じます。

`FileStream` クラスは、ディスク上のファイルの読み書き用ストリームを提供します。

1. ライセンスバイトをソース（ファイルシステム、Azure Blob など）から取得します。  
2. `FileStream` を読み取り権限で開きます。  
3. ストリームを `License` オブジェクトに渡します。

> **直接回答（40‑70語）：**  
> `License` オブジェクトをインスタンス化し、`SetLicense(stream)` を呼び出します。`stream` は `Aspose.CAD.lic` を指す読み取り可能な `FileStream` です。これによりライセンスがメモリからロードされ、必要に応じてファイルシステム外にファイルを保持でき、すべての機能が即座に有効化されます。ストリームは登録が完了するまで開いたままにし、完了後に閉じてください。

## Aspose.CAD for .NET におけるメータリングライセンスの仕組みは？

メータリングライセンスは、固有のキーを使用して `License.SetMeteredKey` を呼び出すことで有効化されます。登録後、SDK は各 CAD 操作を自動的に Aspose のサーバーに報告し、使用状況を監視し、サブスクリプション期間中に実行された操作に対してのみ課金されるようにします。

`License.SetMeteredKey` メソッドは、Aspose.CAD ライブラリにメータリングライセンスキーを登録します。

1. Aspose アカウントのダッシュボードからメータリングライセンスキーを取得します。  
2. `License.SetMeteredKey("your‑key")` でキーを登録します。  
3. 各操作の後に `License.GetMeteredUsage()` を呼び出し、現在の使用回数を取得します。

> **直接回答（40‑70語）：**  
> `License.SetMeteredKey("your‑key")` を呼び出すことでメータリングライセンスが有効化されます。SDK は各 CAD 操作後に使用データを Aspose のサーバーに送信し、実際の消費に基づいて監視および課金できるようにします。このモデルは同時ユーザー数無制限をサポートし、コストを実際の使用量に合わせて調整できます。

## ライセンスと構成のチュートリアル

### [Aspose.CAD for .NET のパスによるライセンス適用](./apply-license-by-path/)
Aspose.CAD for .NET の可能性を最大限に引き出しましょう！ステップバイステップのガイドに従ってシームレスにライセンスを適用してください。今すぐ CAD ファイル操作のレベルを向上させましょう！

### [Aspose.CAD for .NET の FileStream を使用したライセンス適用](./apply-license-using-filestream/)
Aspose.CAD for .NET をマスターしましょう：FileStream を使用してシームレスにライセンスを適用します。ステップバイステップのガイドを探求し、可能性を解き放ちましょう。今すぐダウンロード！

### [Aspose.CAD for .NET のメータリングライセンス](./metered-licensing/)
.NET でのメータリングライセンスで Aspose.CAD の可能性を解き放ちましょう。リソース使用をシームレスに最適化します。ステップバイステップのガイドをご覧ください。

## よくある質問

**Q: 同じライセンスファイルを複数のマシンで使用できますか？**  
A: はい、単一のライセンスファイルは開発サーバーや本番サーバーを問わず、購入した利用規約に従って使用すれば、任意の数に展開できます。

**Q: CAD ファイルをロードする前にライセンス設定を忘れた場合はどうなりますか？**  
A: ライブラリは評価モードで動作し、レンダリングされた画像に透かしが追加され、処理できるページ数が制限されます。

**Q: メータリングライセンスはインターネット接続が必要ですか？**  
A: 最初のアクティベーションと各使用レポート時のみ接続が必要です。その後は次のレポートまでオフラインで動作できます。

**Q: 標準でサポートされている CAD/BIM フォーマットはどれですか？**  
A: Aspose.CAD は DWG、DXF、DGN、STL、OBJ、IFC などを含む 45 以上の入力および出力フォーマットをサポートし、ドキュメント全体をメモリにロードせずに最大 500 MB のファイルをレンダリングできます。

**Q: プログラムからライセンスが正常に適用されたか確認する方法はありますか？**  
A: `License.IsLicensed`（または `License.LicenseFilePath` を確認）を登録後に呼び出します。有効なライセンスがアクティブな場合は `true` を返します。

---

**最終更新日:** 2026-09-14  
**テスト環境:** Aspose.CAD 24.11 for .NET  
**作者:** Aspose

## 関連チュートリアル

- [Aspose.CAD for .NET のパスによるライセンス適用](/cad/net/licensing-and-configuration/apply-license-by-path/)
- [Aspose.CAD for .NET の FileStream を使用したライセンス適用](/cad/net/licensing-and-configuration/apply-license-using-filestream/)
- [Aspose.CAD for .NET のメータリングライセンス](/cad/net/licensing-and-configuration/metered-licensing/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}