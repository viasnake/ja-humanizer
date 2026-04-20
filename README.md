# ja-writing-humanizer

日本語の下書きから AI 生成らしい癖を見つけ、意味・事実・文体を保ったまま自然な文章へ整える Agent Skill です。

記事、レポート、説明文、社内メモなどの公開前推敲に使えます。文章が「整いすぎている」「抽象的で薄い」「定型句が残っている」と感じるときに、局所修正を中心に読みやすさを戻します。

## Install

GitHub CLI v2.90.0 以降では、次のコマンドでインストールできます。

```bash
gh skill install viasnake/ja-humanizer ja-writing-humanizer --agent codex
```

`npx skills` を使う場合は、次のコマンドでインストールできます。

```bash
npx skills add viasnake/ja-humanizer --skill ja-writing-humanizer -a codex
```

ほかの Agent Skills 対応ホストでも、`skills/ja-writing-humanizer/SKILL.md` を skill として読み込めます。

## Use

```text
Use $ja-writing-humanizer to この日本語下書きを、意味を保ったまま自然な文章に整えてください。
```

## What It Checks

- 意義や重要性を過剰に強調していないか
- 接続語、抽象語、評価語が機械的に連続していないか
- チャットボットの対話表現が残っていないか
- 見出しや箇条書きが定型的に反復していないか
- 事実、数値、固有名詞、主張の強さが変わっていないか

この skill は、単一の兆候だけで AI 生成と断定しません。検出器のスコアにも依存せず、曖昧さ、冗長さ、不正確さを優先して直します。

## References

- [Agent Skills specification](https://agentskills.io)
- [Manage agent skills with GitHub CLI](https://github.blog/changelog/2026-04-16-manage-agent-skills-with-github-cli/)
- [anthropics/skills](https://github.com/anthropics/skills)
- [vercel-labs/skills](https://github.com/vercel-labs/skills)
- [Wikipedia: Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing)
- [Wikipedia: WikiProject AI Cleanup](https://en.wikipedia.org/wiki/Wikipedia:WikiProject_AI_Cleanup)

## License

MIT
