# AERAN Calendar 公開情報サイト — Status

更新日：2026年10月24日（JST）

## Projectと公開範囲

正式repository：`akirosso-art/aeran-calendar-info`

目的：個人利用向けiPhoneアプリ「AERAN Calendar」の案内、プライバシーポリシー、利用案内を掲載する静的Webサイトの保守。

標準管理文書導入前の公開GitHub main基準commit：`5db247a7be18acc349b64921d2daad92e7afee50`

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

2026年10月24日、#7-209で`task/7-209-aeran-public-bootstrap`へ5件を新規追加し、commit `1d89ea1f6f3dbca5119e15652dee3764f1b8fb20`としてPUBLIC task branchへの通常pushを完了した。GitHub独立readback PASSは承認済み引き継ぎ結果である。導入前と作成時点の記録は`WORKLOG.md`に保持する。

## 完成済み・確認済み

- 標準5文書をexclusive-createで追加し、全件`added`を維持。
- 5文書のreadback、UTF-8/LF、Markdown構造、相対ファイル参照、PUBLIC安全確認を実施済み。
- #7-209のtask commit・通常pushとGitHub側の独立readback PASS。
- 新規独立会話からのProject復元PASS。正式Projectの新規空チャットであることはUSER_UI_ATTESTEDであり、Git実測・内部独立証明とは区別する。
- 既存Web6ファイルは導入前基準とGit blob全件不変。AERAN Target限定のPUBLIC provenance B方式を維持。
- 全体指揮によるA-PROJECT-BOOTSTRAPは今回の実Project導入に限定してPASS。Phase 7 Closeout全体の完成は本書では宣言しない。

これらはブラウザ表示、アプリ動作、認証機能、Pages配信の再検証結果ではない。

## 作業中

#7-210第1段階として状態文書3件を最小整合する。本文編集時点では今回の追加commit・task push・main統合は未実施。後続の配送結果は実際のGit履歴と作業完了報告で確認する。

## 未着手・未完了

- #7-210の追加commit・task pushの最終結果確認とGitHub側の独立readback
- 独立readback後の続行指示とfresh資格確認を前提とするmain FF-only統合・通常push
- GitHub正式mainの独立readback
- ブラウザ表示・アプリ動作・Pages配信再検証（未実施）
- 既存Webページの変更を伴う保守作業（今回の対象外）

## 通常の静的検証方法

変更範囲に応じて、HTML構造と見出し、ローカルリンク、CSS参照・構文、プライバシー説明との整合、Markdownのリンク、Git差分、秘密情報混入を確認する。

検証は実際に実施した対象・日付・結果とともに記録する。ブラウザ確認やアプリ実機テストを、静的読取りだけでPASSとしない。

## 次の主要マイルストーン

#7-210第1段階の3文書整合・静的検証・task branchへの限定配送後、GitHub独立readbackを待つ。PASS結果と明示された続行指示を受け、fresh Git・security確認後に第2段階のmain FF-only統合へ進む。現在のHEADやremote mainは、導入前基準SHAから推測せず、その都度Gitで確認する。

既存サイトの公開内容・配信設定の変更は、このマイルストーンに含めない。
