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
