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

導入前の公開main基準では既存サイト6ファイルが存在し、標準管理Markdown 5文書は存在していなかった。

2026年10月24日、#7-209で`task/7-209-aeran-public-bootstrap`へ標準管理文書5件を非破壊追加し、commit `1d89ea1f6f3dbca5119e15652dee3764f1b8fb20`として通常pushを完了した。GitHub側の独立readbackはPASS（承認済み引き継ぎ結果）。既存サイト6ファイルは全件Git blob不変。

独立した新規空チャットからのProject復元はPASS。正式Project内の新規空チャットであることはUSER_UI_ATTESTEDであり、Git実測や内部独立証明とは区別する。

AERAN PUBLIC Target限定のprovenance B方式を維持し、完全なSource→Target対応はアクセス制限されたPRIVATE管理記録で保持する。全体指揮によるA-PROJECT-BOOTSTRAPの今回の実Project導入は限定PASS。Phase 7 Closeout全体の完成は宣言しない。

ブラウザ表示・アプリ動作・Pages配信再検証は未実施。

## 次に行う作業

#7-210では`CURRENT-HANDOFF.md`、`STATUS.md`、`WORKLOG.md`のみを整合する。本文編集時点では#7-210の追加commit・task push・main統合は未実施。実際の配送結果はGit履歴と作業完了報告で確認する。

第1段階は静的検証後の追加commit最大1回と既存task branchへの通常push最大1回まで。続くGitHub側の独立readbackを待つ工程境界で終了する。

第2段階のmain FF-only統合は一括承認範囲に含まれるが、独立readback PASS、明示された続行指示、fresh Git・security資格確認を必要とする。再開時には現在のGit refs・履歴・承認scopeを再確認し、本文内のSHAを将来の現在値と決め打ちしない。サイト配信設定変更は対象外。

## 未解決事項

- #7-210の追加commit・task pushの最終結果とGitHub側の独立readback
- 第2段階のfresh確認、main FF-only統合・通常push、正式mainの独立readback
- ブラウザ表示・アプリ動作・Pages配信の再検証（今回の対象外）

## 再開時の確認順序

`git status`・branch・HEAD・origin → `CURRENT-HANDOFF.md` → `AGENTS.md` → `STATUS.md` → `WORKLOG.md` → 必要な`DECISIONS.md` → 対象サイトファイル。

最終的な配送commitと検証結果は、実施後にGit履歴および状態文書で確認する。
