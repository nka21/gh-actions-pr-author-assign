## PRのコミット作者を自動でAssignするGitHub Actions

このリポジトリは、GitHub Actionsで **PRをコミット作者全員（bot除外）に自動でAssign** するワークフローを提供する。

English version: `README.md`

## 何が嬉しいの？

- **「このPRの担当誰？」問題が消える**: 作者が自動でassigneeになる
- **複数人でコミットしたPRに強い**: 複数authorをまとめてAssignできる
- **コミット追加にも追従**: PRに新しいコミットが追加されたら、新しい作者も自動で追加される

## 挙動

- コミット作者のうち、**まだassigneeに居ない人だけ** 追加（既存assigneeは維持）
- botと、GitHubユーザーに紐づかないコミットはスキップ
- `opened` と `synchronize`（PRに新しいコミットが追加）で動かす想定
