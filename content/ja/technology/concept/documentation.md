---
title: Documentation
description: >
  本サービスに関するドキュメント作成・管理に関する戦略を説明します。
weight: 4
---

## 目的

本戦略の目的は、既存の文書作成および管理の課題を解決し、効率的かつ統一されたドキ
ュメント管理を実現することです。これまで、Excel、PowerPoint、Word で作成されてい
た設計書や手順書には以下のような問題がありました。

1. 作成後、更新されない
2. 書式が統一されていない
3. ファイルを開くのが手間である
4. 更新履歴が分かりにくい

これらの課題を解決するために、ドキュメントを Markdown 形式で作成し、GitHub で管
理する方針を導入します。

## Markdown 形式のメリット

Markdown 形式を採用する理由は以下の通りです：

1. **軽量な形式**: Markdown はテキストベースのフォーマットであり、ファイルサイズ
   が軽く、どの環境でも簡単に開くことができます。
2. **シンプルな書式**: 記述ルールがシンプルで、特別なツールが不要。開発者や非開
   発者にとっても扱いやすい。
3. **バージョン管理との相性**: Markdown 形式は GitHub のようなバージョン管理ツー
   ルと容易に統合でき、履歴管理やレビューが容易になります。

## GitHub での管理

GitHub を用いたドキュメント管理を推奨する理由は以下の通りです：

1. **更新履歴の可視化**: GitHub のバージョン管理機能を使用することで、誰がどのよ
   うな変更をいつ行ったかを明確に把握できます。
2. **共同編集**: 複数のメンバーが同時にドキュメントを編集でき、変更が衝突した場
   合でも簡単に解決できます。
3. **レビュー機能**: プルリクエストを使ってドキュメントの変更をレビュー可能。ミ
   スや不備を事前に防ぐことができます。
4. **テンプレートの標準化**: 一度テンプレートを作成すれば、全員が同じ形式でドキ
   ュメントを作成でき、書式のばらつきをなくすことができます。

## 実施方針

### 1. Markdown による統一フォーマットの採用

設計書、手順書などの全ての技術文書は、Markdown 形式で作成することを基本とします
。テンプレートを事前に準備し、利用者が統一されたフォーマットで文書を作成できる環
境を整備します。

### 2. GitHub での一元管理

ドキュメントは GitHub リポジトリ上で管理し、以下の運用ルールを徹底します：

- **バージョン管理**: ドキュメントはリポジトリ内でバージョン管理され、更新履歴を
  残すことを義務付けます。
- **プルリクエストの活用**: 文書の更新時にはプルリクエストを使用し、他メンバーに
  よるレビューを行った後にマージする運用を推奨します。
- **ラベリングとタグ付け**: ドキュメントの種類や内容に応じたラベリングを行い、リ
  ポジトリ内のドキュメント検索を容易にします。

### 3. 教育とサポート

Markdown の書き方や GitHub での運用に不慣れなメンバーのために、以下のサポート体
制を整えます：

- **チュートリアルの提供**: Markdown 記法および GitHub の使い方に関するチュート
  リアルを社内向けに提供します。
- **定期的なトレーニング**: ドキュメンテーション戦略の定着を図るため、定期的に社
  内トレーニングを実施します。
- **テンプレートとサンプル**: 各種ドキュメントのテンプレートやサンプルを提供し、
  スムーズな導入をサポートします。

## 今後の展望

本戦略を導入することで、ドキュメント管理の効率化、更新頻度の向上、統一された書式
による品質の確保が期待されます。また、GitHub を活用したバージョン管理により、過
去の履歴を容易に追跡でき、変更の透明性が向上します。

将来的には、ドキュメントの自動生成ツールや CI/CD パイプラインに統合することで、
さらなる効率化を図る予定です。