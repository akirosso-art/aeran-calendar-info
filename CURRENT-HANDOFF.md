# 現在の引き継ぎ

## 基準情報

更新日：2026年10月24日（JST）

正式repository：`akirosso-art/aeran-calendar-info`

確認済みの公開GitHub `main` 基準commit：`5db247a7be18acc349b64921d2daad92e7afee50`

このcommitは標準管理文書の導入前の基準である。作業開始時のローカルHEAD、branch、working tree、remote-tracking refは、その都度改めて確認する。

## Projectの目的

AERAN Calendarの公開案内サイトを、安全かつ継続的に保守する。

サイトでは、アプリの概要、Google Calendarとの連携に関する利用者向け説明、プライバシーポリシー、利用に関する注意事項を掲載している。

iPhoneアプリ本体の開発や個人のGoogle Calendarデータ管理は、このrepositoryの作業範囲に含まない。

## 確認済みの現在地

2026年10月24日時点の公開GitHub mainでは、サイトを構成する6ファイルを確認済み。標準管理Markdown 5文書は存在していなかった。

公開内容とAERAN限定のprovenance B方式は承認済み。2026年10月24日、`task/7-209-aeran-public-bootstrap`で標準管理文書5件を非破壊追加した。既存サイト6ファイルは変更していない。

本記録のファイル作成時点ではcommit・pushは未実施。最終的なcommit・配送結果はGit履歴と作業完了報告で確認する。

GitHub上の確認結果と、個々のPCの現在のローカル状態は区別する。

## 次に行う作業

5文書のreadback・静的検証・PUBLIC安全確認と既存6ファイルのblob不変確認は実施済み。指定5文書のstage後に差分検証し、承認されたtask branchへのcommit・通常pushを行う。配送後はGitHub側で独立readbackを行い、その後に本人が正式Project内で新しい空チャットを作成して復元を確認する。

main統合、サイト配信設定の変更は承認範囲に含めない。

## 未解決事項

- staged差分検証、commit・pushの最終結果の確認
- GitHub側の独立readback
- 過去チャットを渡さない新規Codex会話からの引き継ぎ復元

独立readbackと新会話復元は未実施。配送の独立PASS、Bootstrap総合PASSは宣言しない。

## 再開時の確認順序

`git status`・branch・HEAD・origin → `CURRENT-HANDOFF.md` → `AGENTS.md` → `STATUS.md` → `WORKLOG.md` → 必要な`DECISIONS.md` → 対象サイトファイル。

最終的な配送commitと検証結果は、実施後にGit履歴および状態文書で確認する。
