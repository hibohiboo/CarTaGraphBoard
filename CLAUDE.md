# CarTaGraphBoard プロジェクトルール

進め方・ディレクトリ・最重要ルールは、ツールに依存しない入口ファイル `AGENTS.md` にまとめている（ここに重複して書かない）。ここには Claude Code だけの話を書く。

@AGENTS.md

## Claude Code 固有の補足

- `.claude/skills/` は `docs/process/` に書いた手順の**呼び出し口**である。手順の本文を変えるときは `docs/process/` を直す。
- 作業の記録（プランに当たるもの）は `docs/cycles/` に置く（`settings.json` の `plansDirectory`）。
- 自動メモリ（`.claude/memory/`）は他のエージェントから見えない。プロジェクトとして残す知識は `docs/` に書き、メモリには個人的な作業上の学びだけを残す。
- サブエージェントを足すときは `model: inherit` にし、特定のモデルに固定しない。
- 独立した調べもの（複数ファイルの Read・Grep）は1回の応答でまとめて呼ぶ。
