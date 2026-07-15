---
marp: true
theme: default
size: 16:9
paginate: false
style: |
  :root { --navy:#1f3864; --navy2:#244b84; --gold:#c99312; --pale:#fff7df; --text:#22324a; --muted:#64748b; --line:#c9d2de; --soft:#f3f6fa; }
  section { font-family:"BIZ UDPGothic","Hiragino Sans","Yu Gothic","YuGothic","Noto Sans JP",sans-serif; position:relative; overflow:hidden; box-sizing:border-box; padding:58px 64px 76px; border-top:24px solid var(--navy); color:var(--text); background:#fff; font-size:20px; line-height:1.55; }
  section::before { display:none !important; } h1 { margin:0; color:var(--navy); font-size:39px; line-height:1.2; font-weight:700; letter-spacing:-.01em; } h2 { margin:0 0 9px; color:var(--navy); font-size:23px; line-height:1.3; } p { margin:0; } ul { margin:0; padding-left:1.1em; } li { margin-bottom:6px; }
  .top-label { position:absolute; top:-19px; right:64px; color:#fff; font-size:13px; z-index:3; }.subtitle { margin-top:13px; color:var(--muted); font-size:20px; line-height:1.5; }.usage { display:inline-block; margin-top:14px; padding:5px 10px; border-radius:3px; background:#fff2c7; color:#76540a; font-size:14px; font-weight:700; }.footer { position:absolute; bottom:0; left:0; right:0; min-height:47px; padding:11px 64px 9px; box-sizing:border-box; background:var(--navy); color:#fff; font-size:19px; line-height:1.25; text-align:center; }.accent { color:#f1c54c; }.source { margin-top:10px; color:#64748b; font-size:12px; line-height:1.4; }
  .cover { margin-top:60px; }.cover h1 { font-size:50px; letter-spacing:-.02em; }.cover .subtitle { font-size:23px; }.cover-rule { width:74px; height:5px; margin-top:29px; background:var(--gold); }.cover-message { max-width:900px; margin-top:23px; color:var(--navy); font-size:29px; line-height:1.45; font-weight:700; }.cover-note { margin-top:26px; color:var(--muted); font-size:16px; }
  .center-stage { display:flex; min-height:365px; flex-direction:column; align-items:center; justify-content:center; text-align:center; }.center-stage h1 { max-width:1020px; font-size:44px; }.center-stage p { max-width:850px; margin-top:18px; color:var(--muted); font-size:21px; }.center-rule { width:72px; height:5px; margin:26px 0 0; background:var(--gold); }
  .cards3 { display:grid; grid-template-columns:repeat(3,1fr); gap:26px; margin-top:25px; }.card { min-height:205px; padding:18px; border:0; border-top:4px solid var(--line); border-radius:0; background:#fff; }.card.recommended { border-color:var(--gold); background:var(--pale); }.tag { display:inline-block; padding:5px 10px; border-radius:999px; background:var(--navy); color:#fff; font-size:13px; font-weight:700; }.tag.gold { background:var(--gold); }.card h2 { margin-top:13px; }.card p { color:#3d4d64; font-size:16.5px; line-height:1.52; }
  .matrix { display:grid; grid-template-columns:180px repeat(3,1fr); margin-top:22px; border-top:1px solid var(--line); font-size:15.5px; }.matrix > div { min-height:58px; padding:13px 15px; border-bottom:1px solid var(--line); }.matrix .head { background:var(--navy); color:#fff; font-weight:700; }.matrix .row { background:var(--soft); color:var(--navy); font-weight:700; }.matrix .focus { background:var(--pale); }.matrix strong { color:var(--navy); }.matrix .head strong { color:#fff; }
  .price-grid { display:grid; grid-template-columns:1.2fr .8fr .8fr 1.45fr; margin-top:23px; border-top:1px solid var(--line); font-size:14px; line-height:1.32; }.price-grid > div { min-height:35px; padding:8px 12px; border-bottom:1px solid var(--line); }.price-grid .head { background:var(--navy); color:#fff; font-weight:700; }.price-grid .hot { background:var(--pale); }.price-grid .muted { color:var(--muted); font-size:14px; }.price-grid strong { color:var(--navy); }.price-grid .head strong { color:#fff; }
  .two-col { display:grid; grid-template-columns:1fr 1fr; gap:30px; margin-top:24px; }.soft { padding:18px; border:0; border-top:3px solid var(--line); border-radius:0; background:var(--soft); }.soft h2 { font-size:22px; }.soft p,.soft li { font-size:16px; }.callout { margin-top:19px; padding:15px 18px; border:0; border-left:5px solid var(--gold); border-radius:0; background:var(--pale); font-size:17px; }.icon { width:30px; height:30px; object-fit:contain; vertical-align:middle; margin-right:8px; }.icon-lg { width:54px; height:54px; object-fit:contain; margin-bottom:10px; }
  .performance { display:grid; grid-template-columns:1fr 1fr; gap:20px 30px; margin-top:22px; }.performance > div { min-height:112px; padding:16px 0 16px 18px; border-left:5px solid var(--gold); background:var(--soft); }.performance h2 { font-size:21px; }.performance p { font-size:15.5px; line-height:1.5; }.performance .caution { border-left-color:var(--navy); background:#edf2f8; }
  .usecase { display:grid; grid-template-columns:178px 1fr 1fr; margin-top:25px; border-top:1px solid var(--line); font-size:16px; }.usecase > div { min-height:72px; padding:15px; border-bottom:1px solid var(--line); }.usecase .head { background:var(--navy); color:#fff; font-weight:700; }.usecase .row { background:var(--soft); color:var(--navy); font-weight:700; }.usecase .focus { background:var(--pale); }
  .flow { display:grid; grid-template-columns:1fr 70px 1fr 70px 1fr; gap:0; align-items:center; margin-top:48px; }.flow .node { min-height:132px; padding:18px; border:1.5px solid var(--line); border-radius:8px; background:var(--soft); text-align:center; }.flow .node.focus { border-color:var(--gold); background:var(--pale); }.flow .arrow { color:var(--gold); font-size:42px; text-align:center; }.flow h2 { font-size:22px; }.flow p { color:#3d4d64; font-size:15px; }
  .eval-steps { display:grid; grid-template-columns:repeat(3,1fr); gap:18px; margin-top:28px; }.eval-steps > div { min-height:178px; padding:17px; border-top:4px solid var(--navy); background:var(--soft); }.eval-no { color:var(--gold); font-size:16px; font-weight:700; }.eval-steps h2 { margin-top:8px; font-size:22px; }.eval-steps p { font-size:16px; }
---

<div class="top-label">モデル比較ガイド | 表紙</div>
<div class="cover">

# GPT-5.6 と Claude の<br>選び方

<p class="subtitle">GPT-5.6 Sol / Terra / Luna、GPT-5.5、Claude Sonnet 5、Claude Opus 4.8</p>
<div class="cover-rule"></div>
<div class="cover-message">最高スコアを探すより、<br>仕事の失敗コスト・自律性・運用単価で選ぶ。</div>
<div class="cover-note">公開情報ベース｜APIの価格と機能を中心に比較｜2026年7月時点</div>

</div>
<div class="footer">比較の目的は<span class="accent">「どれが最強か」</span>ではなく、仕事に合う標準を決めること</div>

---

<div class="top-label">モデル比較ガイド | 結論</div>
<div class="center-stage">
  <h1>日常のエージェント・開発は<br>Terra または Sonnet 5。<br>高難度・長期自律は Sol または Opus 4.8。</h1>
  <div class="center-rule"></div>
  <p>GPT-5.5 は、既存の OpenAI 運用を変えずに比較する基準点として扱う。</p>
</div>
<div class="footer">標準モデルを決め、<span class="accent">例外条件だけ上位モデルへ</span>切り替える</div>

---

<div class="top-label">モデル比較ガイド | 前提</div>

# 公開ベンチマークだけで、4モデルを順位付けしない

<p class="subtitle">評価セット、ツールの有無、推論量、実行環境が異なるため、ベンダー横断の数字はそのまま比較できない</p>
<div class="usage">この資料の読み方：①公開された位置づけ ②価格・機能 ③実業務での評価、の順に判断する</div>

<div class="two-col"><div class="soft"><h2>比較できるもの</h2><ul><li>API価格・コンテキスト・利用可能なツール</li><li>各社が明示するモデルの役割</li><li>同じ自社タスクで測った成功率・時間・費用</li></ul></div><div class="soft"><h2>比較に注意が必要なもの</h2><ul><li>別々の公開ベンチマークの点数</li><li>ツールあり／なしが混在する評価</li><li>推論量やエージェント設定が異なる結果</li></ul></div></div>
<div class="callout"><strong>重要：</strong>この資料の性能比較は「公開情報から分かる傾向」。採用判断は必ず、自社の代表タスクで再評価する。</div>
<div class="footer">ベンチマークは<span class="accent">候補を絞る材料</span>、最終判断は実務評価</div>

---

<div class="top-label">モデル比較ガイド | GPT-5.6</div>

# GPT-5.6 は、能力・費用・規模を3階層から選ぶ

<p class="subtitle">OpenAIは Sol を最上位、Terra を性能と費用の均衡、Luna を大量・低コスト処理向けに位置づける</p>

<div class="cards3"><div class="card"><span class="tag gold">FLAGSHIP</span><h2>Sol</h2><p>複雑な専門業務、難しい設計、品質優先のエージェント。`gpt-5.6` のエイリアスは Sol に接続。</p></div><div class="card recommended"><span class="tag">BALANCED</span><h2>Terra</h2><p>日常の開発、調査、文書化、ツール利用。能力と費用を最もバランス良く取りたい標準候補。</p></div><div class="card"><span class="tag">VOLUME</span><h2>Luna</h2><p>整形、分類、抽出、短い要約など。高頻度の定型処理を低単価で回す。</p></div></div>
<div class="source">出典：OpenAI「Model guidance」「Models」</div>
<div class="footer">GPT-5.6 は<span class="accent">一つのモデルではなく、使い分けるファミリー</span></div>

---

<div class="top-label">モデル比較ガイド | API価格</div>

# API単価は、Sonnet 5 と Terra が日常業務の中心帯

<p class="subtitle">価格は 100万トークンあたり（入力 / 出力、USD）。サブスクリプションの月額とは別に考える</p>

<div class="price-grid"><div class="head">モデル</div><div class="head">入力</div><div class="head">出力</div><div class="head">読み方</div><div><strong>GPT-5.6 Sol</strong></div><div>$5</div><div>$30</div><div>GPT-5.5 と同水準の最上位帯</div><div class="hot"><strong>GPT-5.6 Terra</strong></div><div class="hot">$2.5</div><div class="hot">$15</div><div class="hot">Sol の半額。標準運用の候補</div><div><strong>GPT-5.6 Luna</strong></div><div>$1</div><div>$6</div><div>大量・定型処理の低価格帯</div><div><strong>GPT-5.5</strong></div><div>$5</div><div>$30</div><div>既存OpenAI運用の比較基準</div><div class="hot"><strong>Claude Sonnet 5</strong></div><div class="hot">$2*</div><div class="hot">$10*</div><div class="hot">*2026/8/31までの導入価格。通常は $3 / $15</div><div><strong>Claude Opus 4.8</strong></div><div>$5</div><div>$25</div><div>最上位。出力はSol / GPT-5.5より低い</div></div>
<div class="source">出典：OpenAI各モデルページ、Anthropic「Introducing Claude Sonnet 5 / Opus 4.8」。ツール利用料・長文入力時の料金は別途発生し得る。</div>
<div class="footer">単価差よりも、<span class="accent">成功率・手戻り・トークン量</span>まで含めて総費用を比べる</div>

---

<div class="top-label">モデル比較ガイド | 性能の読み方</div>

# 公開情報から読める性能傾向

<p class="subtitle">同一条件の総合順位ではなく、各社が強調する仕事の種類と、確認すべき限界を整理する</p>

<div class="performance"><div><h2>GPT-5.6</h2><p>複雑な本番ワークフローの品質・効率、ツール利用、フロントエンドのレイアウト／視覚階層／デザイン判断を強化。推論量を `none`〜`max` で調整できる。</p></div><div><h2>GPT-5.5</h2><p>複雑なコーディング・専門業務向けの既存フロンティア基準。5.6への移行では、同等または一段低い推論量から実測するよう案内されている。</p></div><div><h2>Claude Sonnet 5</h2><p>推論・ツール利用・コーディング・ナレッジワークで Sonnet 4.6 を上回り、高い推論量では一部のエージェント評価で Opus 4.8 に届くとAnthropicは説明。</p></div><div><h2>Claude Opus 4.8</h2><p>長時間の自律的な作業、ツール利用、複雑な判断を主眼にした最上位モデル。Anthropicは Online-Mind2Web で 84% と報告している。</p></div><div class="caution"><h2>比較時の注意</h2><p>OpenAIとAnthropicの公表値は、評価セット・ハーネス・推論量・ツール有無が一致しない。異なる表の数字を横並びにして優劣を断定しない。</p></div><div class="caution"><h2>実務上の読み替え</h2><p>「難問で強い」より、テスト通過・根拠の完全性・ツール誤操作・総時間で比較する。特にエージェントは、最後まで完遂する確率を見る。</p></div></div>
<div class="footer">性能とは、<span class="accent">正答率だけでなく完遂率と確認コスト</span>で決まる</div>

---

<div class="top-label">モデル比較ガイド | 機能・自律性</div>

# 自律的な開発・調査では、モデルだけでなく「実行基盤」も選ぶ

<p class="subtitle">APIで使えるツール、推論量、並列化やワークフローの仕組みが、実行できる仕事の範囲を決める</p>

<div class="matrix"><div class="head">観点</div><div class="head">GPT-5.6 ファミリー</div><div class="head">Claude Sonnet 5</div><div class="head">Claude Opus 4.8</div><div class="row">推論量</div><div class="focus">`none`〜`max`、Pro mode。難問だけ強くする設計</div><div>effort を調整。中程度で費用効率、高めで一部Opus級</div><div>effort と高速モード。品質優先の長期作業向け</div><div class="row">ツール・エージェント</div><div class="focus">Responses API、Web/File検索、コード実行、Computer Use、MCP、PTC、マルチエージェント（β）</div><div>ブラウザ・ターミナル等のツール利用を想定したエージェント性を強調</div><div>Claude Codeの dynamic workflows で大規模・長時間タスクを主眼</div><div class="row">向く運用</div><div>OpenAI基盤上で、ツールの接続・統制を細かく設計したい</div><div class="focus">日常の自律化を、低い単価で広げたい</div><div>少数でも高難度・長期の完遂率を重視したい</div></div>
<div class="source">出典：OpenAI「Model guidance」、Anthropic「Introducing Claude Sonnet 5 / Opus 4.8」。機能の提供範囲は契約・リージョン・プレビュー状況で変動。</div>
<div class="footer">モデル比較は、<span class="accent">能力 × 実行環境 × ガードレール</span>で見る</div>

---

<div class="top-label">モデル比較ガイド | ユースケース</div>

# ユースケース別の、最初の選択肢

<p class="subtitle">標準モデルを一つ決め、仕事の性質が変わる条件だけを上位・下位モデルへ分岐させる</p>

<div class="usecase"><div class="head">仕事の条件</div><div class="head">最初に試すモデル</div><div class="head">上げる／下げる条件</div><div class="row">通常の実装・調査・資料作成</div><div class="focus"><strong>GPT-5.6 Terra / Sonnet 5</strong><br>品質・費用・自律性のバランス</div><div>複数の難所、重要設計、長時間の完遂が必要なら Sol / Opus 4.8</div><div class="row">複雑な設計・大規模改修・重要レビュー</div><div><strong>GPT-5.6 Sol / Opus 4.8</strong><br>探索・検証・判断に価値がある</div><div>作業が定型化したら Terra / Sonnet 5 に落とし、運用単価を抑える</div><div class="row">大量の分類・抽出・整形</div><div><strong>GPT-5.6 Luna</strong><br>低単価・高頻度処理</div><div>例外処理だけ Terra / Sonnet 5 にエスカレーション</div></div>
<div class="footer">おすすめは固定ではない。<span class="accent">仕事の失敗コスト</span>で切り替える</div>

---

<div class="top-label">モデル比較ガイド | 選び方</div>

# 迷ったときの、実務的な選び方

<p class="subtitle">「どのモデルが一番賢いか」ではなく、必要な完遂品質と許容できる運用単価を順に問う</p>

<div class="flow"><div class="node"><h2>1. 標準を決める</h2><p>OpenAI中心なら Terra、Claude中心なら Sonnet 5 を代表タスクで試す。</p></div><div class="arrow">→</div><div class="node focus"><h2>2. 失敗コストを判定</h2><p>重要設計・長期自律・厳密なレビューなら、Sol または Opus 4.8 を候補にする。</p></div><div class="arrow">→</div><div class="node"><h2>3. 大量処理を分ける</h2><p>定型・反復作業は Luna へ寄せ、例外のみ標準モデルへ戻す。</p></div></div>
<div class="callout"><strong>補足：</strong>GPT-5.6 は選ばれたパートナー向けプレビューで、広い提供は今後予定と案内されている。実際の利用可否は契約・モデルピッカー・API環境を確認する。</div>
<div class="footer">選択ルールは、<span class="accent">一つの標準＋少数の例外</span>にする</div>

---

<div class="top-label">モデル比較ガイド | 評価計画</div>

# 採用前に、同じ仕事で小さく比較する

<p class="subtitle">公開ベンチマークを読む時間より、代表タスクを10〜20件ずつ測る方が、導入後の失敗を減らせる</p>

<div class="eval-steps"><div><div class="eval-no">STEP 01</div><h2>代表タスクを選ぶ</h2><p>通常実装、難しい障害、調査、定型処理など、実際の業務から10〜20件を抽出する。</p></div><div><div class="eval-no">STEP 02</div><h2>同じ条件で実行する</h2><p>プロンプト、ツール、テスト、許可範囲を揃える。推論量は標準と高めの2段階で試す。</p></div><div><div class="eval-no">STEP 03</div><h2>総費用で選ぶ</h2><p>成功率、テスト通過、根拠、手戻り、所要時間、入力・出力トークン、運用上の事故を記録する。</p></div></div>
<div class="callout"><strong>最終提案：</strong>まず Terra と Sonnet 5 を標準候補として比較し、Sol / Opus 4.8 は「品質差が明確に利益を生む仕事」に限定して検証する。</div>
<div class="footer">最終的に選ぶのは<span class="accent">ベンチマーク上の勝者ではなく、実務で最も再現性のある組み合わせ</span></div>

---

<div class="top-label">モデル比較ガイド | 参考資料</div>

# 参考資料・前提

<div class="two-col"><div class="soft"><h2>OpenAI</h2><ul><li><a href="https://developers.openai.com/api/docs/guides/latest-model">Model guidance / Using GPT-5.6</a></li><li><a href="https://developers.openai.com/api/docs/models">Models</a></li><li><a href="https://developers.openai.com/api/docs/models/gpt-5.6-sol">GPT-5.6 Sol</a></li><li><a href="https://developers.openai.com/api/docs/models/gpt-5.6-terra">GPT-5.6 Terra</a></li><li><a href="https://developers.openai.com/api/docs/models/gpt-5.5">GPT-5.5</a></li></ul></div><div class="soft"><h2>Anthropic</h2><ul><li><a href="https://www.anthropic.com/news/claude-sonnet-5">Introducing Claude Sonnet 5</a></li><li><a href="https://www.anthropic.com/news/claude-opus-4-8">Introducing Claude Opus 4.8</a></li><li>各モデルのSystem Card（評価条件・安全性の詳細）</li></ul></div></div>
<div class="callout"><strong>注意：</strong>価格・提供範囲・プレビュー・利用制限は更新される。意思決定時には、必ず公式ページと自分の契約環境を再確認する。</div>
<div class="footer">情報は更新される。<span class="accent">評価ルールは自社に残す</span></div>
