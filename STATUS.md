# AERAN Calendar 公開情報サイト — Status

更新日：2026年10月24日（JST）

## Projectと公開範囲

正式repository：`akirosso-art/aeran-calendar-info`

目的：個人利用向けiPhoneアプリ「AERAN Calendar」の案内、プライバシーポリシー、利用案内を掲載する静的Webサイトの保守。

公開GitHub mainの確認済み基準commit：`5db247a7be18acc349b64921d2daad92e7afee50`

作業するPCのGit rootとCodex Desktopの作業先は、各セッションで確認する。端末固有の絶対パス・権限情報は公開管理しない。

## 既存の公開サイト

| ファイル | 役割 |
|---|---|
| `index.html` | アプリの紹介と機能案内 |
| `privacy.html` | プライバシーポリシー |
| `terms.html` | 利用案内 |
| `style.css` | 共通スタイルとレスポンシブ表示 |
| `.nojekyll` | サイト配信向けの既存設定 |
| `googlefea83941af27001f.html` | 既存の所有確認用ファイル |

これら6ファイルは上記基準commitのGit treeに存在する。アプリ本体の実装コードや利用者の予定データは本repositoryの対象外。

## 標準管理文書のprovenance

標準管理文書は、非公開で維持される共通テンプレート体系を参照して作成する。Sourceと、公開repository内で具体化されたTargetは別の内容・履歴を持つ。

AERAN PUBLIC Targetに限定したprovenance B方式は承認済み。この公開版では、非公開Source repositoryの名称、commit ID、Git blob IDを掲載しない。各ファイルの完全なSource provenance、承認記録および導入時の証拠は、アクセス制限のある管理記録で保持する。

| Target文書 | Source識別情報 | 2026-10-24時点の採用状態 | Target基準・結果 |
|---|---|---|---|
| `AGENTS.md` | 非公開管理 | added | 基準mainでは不存在。task branchで新規追加 |
| `CURRENT-HANDOFF.md` | 非公開管理 | added | 基準mainでは不存在。task branchで新規追加 |
| `STATUS.md` | 非公開管理 | added | 基準mainでは不存在。task branchで新規追加 |
| `WORKLOG.md` | 非公開管理 | added | 基準mainでは不存在。task branchで新規追加 |
| `DECISIONS.md` | 非公開管理 | added | 基準mainでは不存在。task branchで新規追加 |

`pending`は、上記基準時点では導入を実施していないという意味である。`added`は事前不存在の確認後、承認された作業で実際に追加した場合だけ記録する。既存ファイルを保持した場合は`kept`、明示承認された差分だけ統合した場合は`merged`とする。

2026年10月24日、`task/7-209-aeran-public-bootstrap`で5件を新規追加した。本記録のファイル作成時点ではcommit・pushは未実施。最終結果はGit履歴と作業完了報告で確認する。導入前の事実は`WORKLOG.md`に保持し、存在しないcommitやGit blobを推測で記載しない。

## 完成済み・確認済み

- GitHub上に公開サイト用の6ファイルが存在することを確認。
- サイトはアプリ案内、プライバシーポリシー、利用案内を対象とする。
- 標準管理文書の導入前基準commitを確認。

これらはrepository構成の確認結果であり、ブラウザ表示、アプリ動作、認証機能の検証結果ではない。

## 作業中

- 承認済み管理文書5件を追加・readback済み。UTF-8/LF、Markdown構造、相対ファイル参照、PUBLIC安全確認、既存6ファイルのblob不変を検証済み。stage後の差分検証とtask branchへの限定配送を行う段階。

## 未着手・未完了

- staged差分検証とGit配送の最終結果確認
- GitHub側の独立readback
- 独立した新規Codex会話からのProject復元検証
- 既存Webページの変更を伴う保守作業

## 通常の静的検証方法

変更範囲に応じて、HTML構造と見出し、ローカルリンク、CSS参照・構文、プライバシー説明との整合、Markdownのリンク、Git差分、秘密情報混入を確認する。

検証は実際に実施した対象・日付・結果とともに記録する。ブラウザ確認やアプリ実機テストを、静的読取りだけでPASSとしない。

## 次の主要マイルストーン

承認済みの5文書を静的検証し、task branchへ限定配送する。GitHub側の独立readback後、新規Codex会話で5文書から現在地を復元できることを確認する。

既存サイトの公開内容・配信設定の変更は、このマイルストーンに含めない。
