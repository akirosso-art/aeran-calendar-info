# AERAN Calendar 公開情報サイトの作業ルール

## 対象と目的

このrepository `akirosso-art/aeran-calendar-info` は、個人利用向けiPhoneアプリ「AERAN Calendar」の公開案内サイトを管理する。

対象は、アプリの説明、プライバシーポリシー、利用案内およびサイトの表示用ファイルである。iPhoneアプリ本体の実装コード、Google認証の内部実装、個人の予定情報は管理対象に含まない。

GitHubの正式repositoryを共有正本とし、過去のチャット内容ではなく、現在のGit状態とrepository内の文書を根拠に作業する。

## 作業開始時の確認

1. 正式Git root、origin、branch、HEAD、upstream、index、working tree、untracked、進行中Git操作を確認する。
2. `CURRENT-HANDOFF.md`、本書、`STATUS.md`、必要な`WORKLOG.md`と`DECISIONS.md`を確認する。
3. 変更対象の既存ファイルと関連リンクを確認する。
4. 作業範囲、必要な検証、承認済み操作、禁止操作を明確にする。

意図不明な変更やGitの分岐があれば停止する。無断のreset、stash、rebase、force push、既存ファイルの上書きで解消しない。

## 管理対象ファイル

- `index.html`：アプリの紹介と機能案内
- `privacy.html`：データの取扱いとプライバシーポリシー
- `terms.html`：利用に関する案内
- `style.css`：ページの共通デザインとレスポンシブ表示
- `.nojekyll`：GitHub Pages向けの既存設定ファイル
- `googlefea83941af27001f.html`：既存のサイト所有確認用ファイル
- `AGENTS.md`、`CURRENT-HANDOFF.md`、`STATUS.md`、`WORKLOG.md`、`DECISIONS.md`：開発・保守の判断と引き継ぎ

変更依頼に直接関係しないファイルは変更しない。特に所有確認用ファイル、公開ポリシー、Pages設定は、必要性と影響範囲が確認されるまで維持する。

## 公開情報の安全条件

このrepositoryはPUBLICであり、作業branchのcommitも第三者から閲覧され得る。

認証情報、token、秘密鍵、個人の予定内容、メールアドレス、端末固有パス、非公開repositoryの識別情報、内部運用記録、非公開の設計・セキュリティ情報を保存しない。

公開文書とサイト本文の内容は、ユーザーの明示承認を受けてから公開branchへ配送する。認証状態の確認、外部通信、権限変更、サイトの公開設定変更は、個別に許可された範囲でのみ実施する。

## 静的検証

変更対象に応じて、原則として次を確認する。

- HTMLの構造、文字コード、文書タイトル、見出し、ページ内リンク
- `index.html`、`privacy.html`、`terms.html`間のナビゲーションと相対リンク
- `style.css`への参照とCSS構文
- 画面幅に応じた表示規則への影響
- 説明文とプライバシーポリシー・利用案内の不整合
- 意図しない秘密情報、外部script、フォーム、トラッキング機能の追加
- `git diff --check`など、許可された範囲の差分整合

静的検査、ブラウザでの表示確認、実機アプリの動作確認は別の検証である。実行していない検査をPASSと記録しない。検査ツールがファイルやキャッシュを作る場合は、その副作用を事前確認する。

## 変更・配送

作業は承認されたファイルとGit操作だけに限定する。必要に応じて独立したtask branchを使い、commit・pushの前に差分と公開内容を確認する。

PUBLIC task branchへのpushと、`main`への統合は別の判断である。main統合、サイトの配信設定変更、プライバシーポリシーの実質変更は明示承認なしに実施しない。

## 状態文書と引き継ぎ

- `CURRENT-HANDOFF.md`：次の会話で再開する地点
- `STATUS.md`：Projectの現在地、未検証事項、管理文書の状態
- `WORKLOG.md`：実際に行った作業と検証の時系列記録
- `DECISIONS.md`：重要判断、その理由、見直し条件

Sourceとなった標準テンプレートと、このrepositoryに導入したTarget文書は別の成果物である。公開版には非公開Sourceの識別情報を無断掲載しない。完全な由来情報の管理方法は、承認されたprovenance方針に従う。

新しいCodex会話では、まずGit状態とこれらの文書を読み、目的、現在地、安全境界、判断理由、検証方法、未解決事項、次の一手を復元する。過去チャットへの依存を前提にしない。
