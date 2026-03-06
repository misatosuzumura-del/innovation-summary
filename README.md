# イノベーション推進チーム 月次サマリー作成スキル

Claude Code 用のカスタムスキルです。Slack・Notion・Google からイノベーション推進チームの月次振り返りを自動作成します。

## セットアップ

1. `innovation-summary.md` を `~/.claude/commands/` にコピー

```bash
cp innovation-summary.md ~/.claude/commands/
```

2. Claude Code を再起動

## 使い方

Claude Code 内で以下のように実行:

```
/innovation-summary 3月
```

引数なしの場合は前月が対象になります。

## 必要な環境

- Claude Code（Notion MCP 接続済み）
- Google OAuth トークン（カレンダー・Gmail用）
  - `~/check_calendar.py` / `~/check_gmail.py` が動作すること

## スキルの内容

- Notion（経営企画部定例議事録、DIDIM関連ページ）から情報収集
- Slack（#innovation_general 等）から情報収集
- Google カレンダー・Gmail から関連情報を抽出
- テンプレートに沿って簡潔なサマリーを生成

## チーム構成

| メンバー | 主な担当領域 |
|---------|------------|
| 相馬さん | DIDIM事業・展示会・代理店・実証実験・メディア対応 |
| 外山さん | DIDIM契約・法務・海外・M&A |
| 鈴村 | プロダクト営業・インフラ整備・展示会準備 |

## カスタマイズ

チーム構成や担当領域が変わった場合は `innovation-summary.md` 内の「チーム構成」セクションを更新してください。
