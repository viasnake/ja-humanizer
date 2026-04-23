# 日本語・英語アンチ AI パターン集

推敲時は、単一項目ではなく複数項目の同時出現で判断する。英語で典型的な癖が、日本語では直訳調や表記ゆれとして現れることも多い。

## 0. 判定ルール

1. 単一兆候だけで AI 生成と断定しない
2. 文体上の癖と、事実性・根拠妥当性の問題を分けて扱う
3. まず不正確・曖昧・冗長を修正し、その後に文体を整える
4. 日本語では、表記体系と誤用の知識が品質改善に直結する

## 1. 内容パターン

### 1. 意義の過剰な強調

兆候:
- 「画期的」「重要性を浮き彫りにする」「新時代を切り開く」
- `revolutionary`, `groundbreaking`, `highlights the profound significance of`

悪い例:
- JA: この取り組みは業界に新時代を切り開く画期的な施策であり、その重要性を浮き彫りにした。
- EN: This initiative is a groundbreaking effort that highlights the profound significance of operational excellence.

改善例:
- JA: この取り組みで、作業時間は平均 18% 短縮した。
- EN: This initiative reduced average processing time by 18%.

修正方針:
- 評価語を削り、確認可能な事実・範囲・条件だけを残す

### 2. 注目度や権威の盛りすぎ

兆候:
- 媒体名や権威者名を並べて価値を補強する
- `widely recognized by experts and major media outlets`

悪い例:
- JA: 複数の有力メディアや専門家が注目しており、非常に高い評価を受けている。
- EN: It has been widely recognized by experts, thought leaders, and major media outlets.

改善例:
- JA: 日経クロステックと ITmedia が 2026 年 3 月にこの機能を紹介した。
- EN: Nikkei xTECH and ITmedia covered the feature in March 2026.

修正方針:
- 誰がいつ何を述べたかに分解する。必要のない権威づけは削る

### 3. 表面的な付け足し分析

兆候:
- データの後に「示唆する」「浮き彫りにする」を機械的に連結する
- `This suggests that...` を根拠なく足す

悪い例:
- JA: 利用率は 62% だった。これは、ユーザーの高い満足度を示唆している。
- EN: Adoption reached 62%, which suggests strong user satisfaction and long-term loyalty.

改善例:
- JA: 利用率は 62% だった。満足度との関係は、このデータだけでは判断できない。
- EN: Adoption reached 62%. This dataset alone does not show user satisfaction.

修正方針:
- 解釈に根拠がないなら削る。必要なら条件付きで短く書く

### 4. 宣伝調・広告調

兆候:
- 「魅力的」「卓越した」「革新的」など評価語の多用
- `robust`, `seamless`, `cutting-edge`, `best-in-class`

悪い例:
- JA: 革新的でシームレスな体験を提供する卓越したプラットフォームです。
- EN: It delivers a seamless, cutting-edge, best-in-class experience for modern teams.

改善例:
- JA: モバイルとデスクトップで同じ手順で操作できる。
- EN: The same workflow works on both mobile and desktop.

修正方針:
- 観察できる挙動、制約、比較条件を書く

### 5. 曖昧な権威づけと過度な一般化

兆候:
- 「専門家によると」「多くの人が」「一般的に」など主語不明
- `many people believe`, `it is widely considered`

悪い例:
- JA: 一般的に、この方法は非常に効果的だと考えられている。
- EN: It is widely considered to be one of the most effective methods available.

改善例:
- JA: 社内の 3 チームで試した結果、2 チームで作業時間が短縮した。
- EN: In trials with three internal teams, two reported shorter processing time.

修正方針:
- 主体・範囲・母数を具体化する。できないなら控えめにする

### 6. 課題と展望の定型段落

兆候:
- 「課題はあるが今後の展開に注目」「さらなる発展が期待される」
- `Challenges remain, but the future looks promising`

悪い例:
- JA: いくつかの課題は残るものの、今後のさらなる発展が期待される。
- EN: While some challenges remain, the future looks promising and continued growth is expected.

改善例:
- JA: 課題は API 制限と運用コストの 2 点で、次の判断は 5 月の検証後に行う。
- EN: The main issues are API limits and operating cost. We will revisit the decision after the May trial.

修正方針:
- 課題、条件、次の行動を具体化する

## 2. 言語パターン

### 7. AI 頻出語の連打

兆候:
- 「さらに」「加えて」「一方で」「包括的に」の過密
- `moreover`, `furthermore`, `additionally`, `in today’s rapidly evolving`

悪い例:
- JA: さらに、加えて、一方で、包括的に見れば、この施策は多面的な価値を持つ。
- EN: Furthermore, additionally, in today’s rapidly evolving landscape, this initiative provides multifaceted value.

改善例:
- JA: この施策には、コスト削減と待ち時間短縮の効果がある。
- EN: This initiative cuts cost and shortens wait time.

修正方針:
- 接続語を間引き、主文から書く

### 8. 回りくどい繋辞回避

兆候:
- 「〜として位置づけられる」「〜の役割を果たす」の乱用
- `serves as`, `is positioned as`, `can be seen as`

悪い例:
- JA: この手順は品質向上の基盤として位置づけられる。
- EN: This process serves as a foundational pillar for improving quality.

改善例:
- JA: この手順でレビュー漏れを減らせる。
- EN: This process reduces missed reviews.

修正方針:
- `is/are`, 「です」「ある」「担う」で十分なら短くする

### 9. 否定対比のテンプレ

兆候:
- 「XだけでなくY」「単なるAではない」の反復
- `not just X but also Y`, `not merely A`

悪い例:
- JA: この機能は単なる通知機能ではなく、業務変革を支える基盤でもある。
- EN: This is not just a notification feature, but also a strategic enabler of transformation.

改善例:
- JA: この機能は通知に加えて承認依頼も送れる。
- EN: The feature sends both notifications and approval requests.

修正方針:
- 肯定文で直接書く。対比は本当に必要なときだけ使う

### 10. 三点セットの強制

兆候:
- 何でも 3 項目に並べる
- `speed, efficiency, and innovation` のような空疎な三連

悪い例:
- JA: 本施策は、効率性、柔軟性、拡張性を実現する。
- EN: The solution improves speed, efficiency, and innovation.

改善例:
- JA: 本施策で、月次集計にかかる時間が 2 時間減る。
- EN: The solution cuts monthly reporting time by two hours.

修正方針:
- 実際に言うべき数だけ列挙する。抽象名詞の三連を避ける

### 11. 同義語の無意味な循環

兆候:
- 同じ対象を毎回別名で呼ぶ
- `tool`, `solution`, `platform`, `framework` が対象不明のまま入れ替わる

悪い例:
- JA: このシステムは、このソリューションにより、当プラットフォーム上で機能する。
- EN: The tool enables the platform to make the solution more impactful.

改善例:
- JA: このシステムは、管理画面から申請を処理する。
- EN: The system processes requests from the admin console.

修正方針:
- 最も明確な呼び名を決め、文書内で維持する

### 12. 過剰ヘッジの積層

兆候:
- 「〜かもしれない可能性がある」
- `may potentially`, `could possibly`, `appears to seem`

悪い例:
- JA: 利用率が改善する可能性があるかもしれない。
- EN: Adoption may potentially improve over time.

改善例:
- JA: 利用率は改善する可能性がある。
- EN: Adoption may improve.

修正方針:
- ヘッジは 1 つだけ残す

### 13. 回りくどい冗語

兆候:
- 「〜することが可能です」「〜という点において」
- `in terms of`, `with regard to`, `has the ability to`

悪い例:
- JA: 本機能は、設定を変更することが可能です。
- EN: The feature has the ability to modify settings in terms of user preferences.

改善例:
- JA: 本機能で設定を変更できる。
- EN: The feature lets users change settings.

修正方針:
- 動詞中心に戻す。名詞化をほどく

## 3. 日本語で特に見るパターン

### 14. 直訳調の不自然さ

兆候:
- 英語の構文をそのまま写したような語順や抽象語

悪い例:
- JA: この変更は、チームがより良い意思決定を行うことを可能にする。

改善例:
- JA: この変更で、チームは判断しやすくなる。

修正方針:
- `enable`, `ensure`, `drive` の直訳臭を疑い、日本語の自然な動詞へ置き換える

### 15. 表記ゆれ

兆候:
- 「ユーザー」と「ユーザ」、「出来る」と「できる」、「Web」と「ウェブ」が混在

悪い例:
- JA: ユーザーはWeb画面から申請できる。別の画面ではユーザが申込みを出来る。

改善例:
- JA: ユーザーはウェブ画面から申請できる。

修正方針:
- 文書ごとに表記方針を決め、全体で揃える

### 16. 重言と無駄な言い換え

兆候:
- 「頭痛が痛い」「電車に乗車する」「まだ未定」

悪い例:
- JA: 現時点ではまだ未定です。

改善例:
- JA: 現時点では未定です。

修正方針:
- 語義が重複していないか確認する。ただし慣用化した表現は文脈で判断する

### 17. テンプレ導入・テンプレ結論

兆候:
- 「ここでは〜を解説します」「以上のことから〜が重要だと言える」

悪い例:
- JA: ここでは、本機能の重要性と意義について詳しく解説します。
- EN: In conclusion, it is important to recognize the significance of this feature.

改善例:
- JA: 本機能は 3 月の更新で追加された。
- EN: The feature was added in the March release.

修正方針:
- 最初の文で要件や事実を述べる。結論も空疎に広げない

## 4. スタイルパターン

### 18. ダッシュ類の多用

兆候:
- `—` や `——` で挿入句を多用する

悪い例:
- JA: この機能は — 特に管理者にとって — 非常に有用です。
- EN: This feature is useful — especially for administrators — in many scenarios.

改善例:
- JA: この機能は、特に管理者に役立つ。
- EN: This feature is especially useful for administrators.

修正方針:
- 読点、括弧、文分割で置き換える

### 19. 太字の機械的多用

兆候:
- 重要でない語まで強調する

悪い例:
- JA: **この機能** は **非常に重要** で **多くの価値** をもたらします。
- EN: **This feature** provides **significant value** across **many workflows**.

改善例:
- JA: 太字は本当に区別したい語だけに使う。
- EN: Use bold only for terms that need emphasis.

### 20. インライン見出し箇条書きの機械的反復

兆候:
- `- 速度: ...` `- 柔軟性: ...` を延々と続ける

悪い例:
- JA: - 速度: 高い。- 柔軟性: 高い。- 拡張性: 高い。
- EN: - Speed: strong. - Flexibility: strong. - Scalability: strong.

改善例:
- JA: 処理は速く、設定変更にも対応しやすい。
- EN: The process is fast and adapts easily to configuration changes.

## 5. 対話残留パターン

### 21. チャットボット残留表現

兆候:
- 「ご質問ありがとうございます」「お役に立てれば幸いです」
- `Thanks for your question`, `I hope this helps`

修正方針:
- 本文用途なら完全に削除する

### 22. お世辞・追従トーン

兆候:
- 根拠のない称賛、過度な同意

悪い例:
- JA: とても素晴らしい視点です。この施策は間違いなく大成功です。
- EN: That is an excellent point, and this initiative will undoubtedly be a huge success.

改善例:
- JA: 指摘の論点は、運用コストの見積りに関わる。
- EN: That point affects the cost estimate.

### 23. 知識制約の定型断り

兆候:
- 「最新情報ではない可能性があります」
- `my knowledge cutoff`, `I may not have access to the latest information`

修正方針:
- 本文用途に不要なら削除する。必要なら別の注記欄へ分離する

## 6. 仕上げ監査

1. 冒頭がテンプレ導入になっていないか
2. 結論が「今後の展開が注目されます」で逃げていないか
3. `—` と `——` がゼロか
4. 日本語の表記が揃っているか
5. 英語の語が抽象名詞の連打になっていないか
6. 事実・数値・固有名詞が改変されていないか
7. 日英の温度感とレジスターがずれていないか

## 7. 補助参照

- 日本語の表記・誤用・語感を確認したいときは `japanese-basics.md` を読む
- 英語の兆候分類の原型は Wikipedia の Signs of AI writing を参照する
