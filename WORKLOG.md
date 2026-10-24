# AERAN Calendar 公開情報サイト — 作業履歴

このファイルは、公開情報サイトの保守に関する実施内容と検証結果を時系列で記録する。現在の再開地点は`CURRENT-HANDOFF.md`、現在の全体状態は`STATUS.md`を参照する。

非公開の会話ログ、認証・セッション情報、利用者データ、端末固有の記録は転載しない。

## 2026年10月24日（JST）— 公開サイト構成の確認と管理文書の導入準備

**対象**：`akirosso-art/aeran-calendar-info`

**基準commit**：`5db247a7be18acc349b64921d2daad92e7afee50`

**実施した確認**

- 公開GitHub repositoryのmainおよび既存Git treeを確認。
- 案内ページ、プライバシーポリシー、利用案内、共通CSS、サイト配信関連の既存6ファイルを確認。
- 基準commitのrootには、標準管理Markdown 5件が存在しないことを確認。
- 既存Webサイトを変更せず、標準管理文書の追加候補と公開情報の安全境界を整理。

**変更対象**

この記録時点では、公開repositoryのHTML/CSS、5管理文書、配信設定は変更していない。

**検証結果**

GitHub上の構成確認は実施済み。新しい管理文書の作成・readback・commit・pushおよび新規会話での復元確認は未実施。

HTML/CSSの静的構造については既存ソースを参照したが、ブラウザ表示テスト、アプリ動作テスト、公開配信の再検証は実施していない。

**判断事項**

PUBLIC repositoryに非公開Sourceのrepository名、commit ID、blob IDを掲載するかについては、公開前の承認対象とする。理由と見直し条件は`DECISIONS.md`で管理する。

**次への申し送り**

公開用5文書の内容とprovenance方針の確定後に、最新Git状態と既存ファイルの不存在を確認して限定導入する。実際のファイル作成、検証、commit、GitHub配送については、実施時に本ログへ別の記録を追加する。

## 2026年10月24日（JST）— 承認済み管理文書の非破壊導入

**branch**：`task/7-209-aeran-public-bootstrap`

**基準commit**：`5db247a7be18acc349b64921d2daad92e7afee50`

**実施内容**

- 導入前のGit状態、5文書の不存在、安全な作成条件、公開commit identityの適格性を確認。
- AERAN限定のprovenance B方式と公開内容の承認に従い、指定5文書をexclusive-createで追加。採用状態は全件`added`。
- 既存サイト6ファイルは変更しない。

**検証と配送の記録時点**

5文書のreadback、regular/non-link・owner/mode・ACL・xattr・identity確認、UTF-8/LF、Markdown構造、参照ファイルの存在、承認原稿からの限定事実差分、PUBLIC安全確認、全件addedとの一致、既存6ファイルのGit blob不変を確認した。Markdown形式の相対リンクはなく、文中の相対ファイル参照先は存在する。

初回の検証スクリプトはxattr不存在を要求して停止した。macOS由来の来歴属性のみであることを確認し、事前検査と同じ許容基準へ検査側を整合してPASSした。ファイル属性の変更はしていない。

commit・pushは本記録更新時点では未実施。最終結果はGit履歴と作業完了報告で確認する。

ブラウザ表示・アプリ動作、GitHub独立readback、新規空チャットでの復元は未実施。独立readback後の復元確認へ引き継ぐ。main統合やサイト配信設定の変更は行わない。

## 2026年10月24日（JST）— #7-209配送・独立検証の後続結果

前節のcommit・push未実施は文書作成時点の歴史的記録であり、以下はその後に成立した結果である。

- 管理5文書をexclusive-createで追加し、限定静的検証・readback・PUBLIC安全確認を実施。全件`added`。
- 追加commit：`1d89ea1f6f3dbca5119e15652dee3764f1b8fb20`。親は導入前基準`5db247a7be18acc349b64921d2daad92e7afee50`。
- PUBLIC task branchへの通常push成功とGitHub独立readback PASSは、#7-210の承認済み引き継ぎ結果として確認。
- 新規空チャットからの独立復元PASS。正式Project内の新規空チャットという条件はUSER_UI_ATTESTEDであり、Git実測・内部独立証明とは区別。
- 既存サイト6ファイルのGit blobは全件不変。AERAN Target限定のPUBLIC B方式を維持し、完全なSource→Target対応はアクセス制限されたPRIVATE管理記録で保持。
- 全体指揮によるA-PROJECT-BOOTSTRAPは今回の実Project導入に限定してPASS。Phase 7 Closeout全体の完成ではない。
- ブラウザ表示・アプリ動作・Pages配信再検証は未実施。

## 2026年10月24日（JST）— #7-210状態文書3件の整合

**実施範囲**

`CURRENT-HANDOFF.md`、`STATUS.md`、`WORKLOG.md`のみを更新し、#7-209の完了実績と作成時点の記録を区別した。既存の日付付き履歴は保持した。

**編集前の確認**

固定task HEAD・親・local main・origin/main、clean・untrackedなし、lock・進行中Git操作・他worktree競合なしを確認。限定read-only remote照会でmainとtaskの2refが固定開始SHAに一致した。通常ファイル・metadata・Git副作用条件を確認し、既存6サイトファイルの基準blob一致を確認した。

**編集後の確認**

差分が指定3文書のみであること、UTF-8/LF・見出し・参照先、内容readback、PUBLIC安全、歴史的記録との時点区別、Git差分整合を確認した。AGENTS.md・DECISIONS.mdと既存6サイトファイルは不変。

**記録作成時点と次工程**

今回の追加commit・task push・main FF-only統合は本記録作成時点では未実施。編集後のPUBLIC安全・静的検証、指定3件のみのstageとstaged差分検証を通過した場合に、追加commit最大1回・既存task branchへの通常push最大1回を行う。完了したGit配送は最終的にGit履歴と作業完了報告で確認する。

第1段階配送後のGitHub独立readbackは別工程であり、この編集では未実施。第2段階はそのPASS結果、明示された続行指示、fresh資格確認を前提とする。main統合・サイト変更・配信設定変更は今回行わない。
