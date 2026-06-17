# ja-writing-humanizer

日本語を主対象に、英語や日英混在文書の LLM 生成らしい癖を、意味・事実・文体を保ったまま自然な文章へ整える Agent Skill です。

記事、レポート、説明文、社内メモ、メール、お知らせ、商品説明、SNS 投稿などの推敲に使えます。文章が「整いすぎている」「抽象的で薄い」「同じ言い方を繰り返している」「宣伝調に寄っている」「翻訳調が残っている」と感じるときに、局所修正を中心に読みやすさを戻します。

この skill は技術文書に限りません。AI っぽさ、曖昧さ、冗長さ、表記ゆれ、温度感のずれを抑え、読み手に自然な日本語へ整えることに絞っています。

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
Use $ja-writing-humanizer to この下書きの意味と事実を保ったまま、LLM臭さと冗長さを抜いて、自然な日本語に整えてください。
```

## What It Checks

- 意義や重要性を過剰に強調していないか
- 接続語、抽象語、評価語が機械的に連続していないか
- 英語の `not just X but Y` や抽象名詞三連が残っていないか
- 日本語の表記ゆれ、重言、直訳調が残っていないか
- チャットボットの対話表現が残っていないか
- 見出しや箇条書きが定型的に反復していないか
- 事実、数値、固有名詞、主張の強さが変わっていないか

この skill は、単一の兆候だけで AI 生成と断定しません。検出器のスコアにも依存せず、曖昧さ、冗長さ、不正確さを優先して直します。

## Bundled References

- `references/patterns.md`: LLM 臭さ、反復、空句、宣伝調の検出パターン
- `references/japanese-style.md`: 自然な日本語へ整えるための語感、表記、敬語、句読点の観点
- `references/cases.md`: お知らせ、メール、記事、商品説明、SNS 投稿などの用途別ケース
- `references/language-foundations.md`: 文法、語彙、かな・漢字、読解の土台から確認する観点

## License

MIT
