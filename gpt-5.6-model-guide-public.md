---
marp: true
theme: default
size: 16:9
paginate: false
style: |
  :root { --navy:#1f3864; --blue:#2e5fa3; --gold:#e8c15a; --gold-2:#b98b16; --text:#22324a; --muted:#667085; --line:#c9d2de; --soft:#f4f6f9; }
  section { font-family:"Yu Gothic","YuGothic","Hiragino Kaku Gothic ProN","Noto Sans JP",sans-serif; position:relative; overflow:hidden; box-sizing:border-box; color:var(--text); background:#fff; border-top:28px solid #1f3864; padding:54px 54px 74px; font-size:20px; line-height:1.45; }
  section::before { display:none !important; }
  h1 { margin:0; color:var(--navy); font-size:39px; line-height:1.15; font-weight:700; } h2 { margin:0 0 10px; color:var(--navy); font-size:24px; line-height:1.25; font-weight:700; } h3 { margin:0 0 9px; color:var(--navy); font-size:20px; line-height:1.3; font-weight:700; } p { margin:0; } ul { margin:0; padding-left:1.1em; } li { margin:0 0 5px; }
  .top-label { position:absolute; top:-22px; right:54px; z-index:2; color:#fff; font-size:13px; line-height:1.2; }.subtitle { margin-top:14px; color:var(--muted); font-size:21px; }.blue-line { margin-top:12px; color:var(--blue); font-size:21px; font-weight:700; }.section-label { margin:24px 0 12px; color:var(--navy); font-size:22px; line-height:1.2; font-weight:700; }
  .cover { margin-top:58px; }.cover h1 { font-size:48px; }.cover .subtitle { font-size:23px; }.cover-rule { width:76px; height:5px; margin-top:28px; background:var(--gold-2); }.cover-message { max-width:800px; margin-top:22px; color:var(--navy); font-size:29px; line-height:1.45; font-weight:700; }.cover-note { margin-top:26px; color:var(--muted); font-size:17px; }.position-box,.evidence-box,.proposal { margin-top:20px; padding:13px 18px; border:1.5px solid var(--line); border-radius:8px; background:var(--soft); font-size:17px; }.evidence-box,.proposal { border-color:var(--gold-2); background:#fff9ea; }.cards-3,.cards-2,.numbered-summary { display:grid; gap:18px; }.cards-3,.numbered-summary { grid-template-columns:repeat(3,1fr); }.cards-2 { grid-template-columns:repeat(2,1fr); }.split { display:grid; grid-template-columns:1fr 1fr; gap:22px; margin-top:22px; }
  .card,.soft-card { border:1.5px solid var(--line); border-radius:8px; background:#fff; padding:15px 17px; }.soft-card { background:var(--soft); }.card strong,.soft-card strong { color:var(--navy); }.card-number { display:inline-block; margin-right:8px; color:var(--blue); font-weight:700; }.card-title { color:var(--navy); font-weight:700; font-size:20px; line-height:1.25; }.card-body { margin-top:12px; color:#3a3f47; font-size:16.5px; }.compact { font-size:15.5px; line-height:1.42; }
  .pill { display:inline-block; padding:7px 16px; border-radius:999px; background:var(--navy); color:#fff; font-size:15px; font-weight:700; }.pill.gold { background:var(--gold-2); }.pill.gray { background:#aeb4bd; }.mini-table { width:100%; border-collapse:collapse; font-size:14px; line-height:1.35; margin-top:16px; }.mini-table th { background:var(--navy); color:#fff; font-weight:700; }.mini-table th,.mini-table td { border:1px solid var(--line); padding:8px 9px; vertical-align:top; }.mini-table .target { background:#fff8e4; border-color:var(--gold-2); }.decision-grid { display:grid; grid-template-columns:185px repeat(3,1fr); margin-top:23px; border-top:1px solid var(--line); border-left:1px solid var(--line); font-size:16px; }.decision-grid > div { min-height:64px; padding:13px; border-right:1px solid var(--line); border-bottom:1px solid var(--line); }.decision-grid .head { background:var(--navy); color:#fff; font-weight:700; }.decision-grid .rowhead { background:var(--soft); color:var(--navy); font-weight:700; }.decision-grid .recommended { background:#fff8e4; }.source-line { margin-top:10px; color:#6b7280; font-size:12px; }.icon { width:30px; height:30px; object-fit:contain; vertical-align:middle; margin-right:8px; }.icon-lg { width:58px; height:58px; object-fit:contain; margin-bottom:10px; }.transition-line { margin-top:12px; color:#344054; font-size:15px; text-align:center; }.footer-message { position:absolute; left:0; right:0; bottom:0; min-height:48px; padding:11px 58px 10px; background:var(--navy); color:#fff; font-size:20px; line-height:1.25; text-align:center; z-index:3; }.footer-message .accent,.accent { color:var(--gold); }.summary-no { width:36px; height:36px; border-radius:50%; background:#f0f4fa; color:var(--blue); display:flex; align-items:center; justify-content:center; font-size:20px; font-weight:700; margin-bottom:10px; }
---

<div class="top-label">GPT-5.6 モデル選び | はじめに</div>

<div class="cover">

# GPT-5.6 のモデル選び

<p class="subtitle">Sol / Terra / Luna の違いと、Plus × Codex での実践的な使い分け</p>
<div class="cover-rule"></div>
<div class="cover-message">普段は Terra。<br>品質差が成果を左右する難問だけ Sol。</div>
<div class="cover-note">この資料では、3モデルの役割・公開根拠・Plus × Codex での選び方を整理する。</div>


</div>

<div class="footer-message">普段は<span class="accent">Terra</span>、難問だけ<span class="accent">Sol</span>。用途で使い分ける</div>

---

<div class="top-label">GPT-5.6 モデル選び | 1/7</div>

# GPT-5.6 は、知能・速度・費用を選べる3つの階層

<p class="subtitle">世代番号は共通。Sol / Terra / Luna は、用途に応じた能力階層を表す名称</p>
<p class="blue-line">「一番賢いモデルを常に使う」ではなく、タスクに必要な能力を選ぶ</p>

<div class="cards-3" style="margin-top:22px">
  <div class="card"><span class="pill gold">FLAGSHIP</span><div class="card-title" style="margin-top:14px">Sol</div><div class="card-body">最高能力<br>複雑なコーディング、深い分析、難しい設計判断</div></div>
  <div class="card" style="border-color:#b98b16;background:#fff9ea"><span class="pill">BALANCED</span><div class="card-title" style="margin-top:14px">Terra</div><div class="card-body">性能・速度・費用の均衡<br>日常の開発、調査、資料作成、業務自動化</div></div>
  <div class="card"><span class="pill gray">FAST / SCALE</span><div class="card-title" style="margin-top:14px">Luna</div><div class="card-body">最速・最安<br>整形、分類、抽出、短い要約などの大量定型処理</div></div>
</div>

<div class="evidence-box"><strong>補足：</strong>`gpt-5.6` のエイリアスは Sol にルーティングされる。明示的にモデルを選ぶときは `gpt-5.6-sol` / `-terra` / `-luna` を指定する。</div>
<div class="footer-message">モデル名は性能の上下ではなく、<span class="accent">役割分担</span>を表す</div>

---

<div class="top-label">GPT-5.6 モデル選び | 2/7</div>

# API料金では Terra は Sol の半額

<p class="subtitle">サブスクリプション利用と API 従量課金は別だが、モデル階層のコスト差は明確</p>

<table class="mini-table">
  <thead><tr><th>モデル</th><th>入力 / 100万 token</th><th>出力 / 100万 token</th><th>Sol 比</th><th>位置づけ</th></tr></thead>
  <tbody>
    <tr><td><strong>Sol</strong></td><td>$5.00</td><td>$30.00</td><td>100%</td><td>品質最優先</td></tr>
    <tr class="target"><td><strong>Terra</strong></td><td>$2.50</td><td>$15.00</td><td><strong>50%</strong></td><td><strong>日常作業の標準候補</strong></td></tr>
    <tr><td><strong>Luna</strong></td><td>$1.00</td><td>$6.00</td><td>20%</td><td>大量・高速処理</td></tr>
  </tbody>
</table>

<div class="split">
  <div class="soft-card"><h2>Terra がよい場面</h2><ul class="compact"><li>十分な品質を、繰り返し安定して得たい</li><li>速さと能力を両立したい</li><li>通常タスクで Sol を常用する必然性が薄い</li></ul></div>
  <div class="soft-card"><h2>Sol に切り替える場面</h2><ul class="compact"><li>1回の失敗・見落としが大きなコストになる</li><li>複数段階の推論や検証が要る</li><li>高い品質差が成果に直結する</li></ul></div>
</div>

<div class="footer-message">Terra は<span class="accent">費用を下げるためだけ</span>のモデルではない</div>

---

<div class="top-label">GPT-5.6 モデル選び | 3/7</div>

# Terra / Luna も GPT-5.5 を上回る公開スコア

<p class="subtitle">HealthBench Professional：臨床利用における回答品質・安全性を測る評価（0–100、回答長補正済み）</p>

<table class="mini-table">
  <thead><tr><th>モデル</th><th>スコア</th><th>GPT-5.5との差</th><th>読み方</th></tr></thead>
  <tbody>
    <tr><td>GPT-5.5</td><td>51.8</td><td>基準</td><td>比較の基準線</td></tr>
    <tr><td>GPT-5.6 Luna</td><td>55.7</td><td>+3.9</td><td>最安層でも上回る</td></tr>
    <tr class="target"><td><strong>GPT-5.6 Terra</strong></td><td><strong>57.7</strong></td><td><strong>+5.9</strong></td><td><strong>価格と性能のバランス</strong></td></tr>
    <tr><td>GPT-5.6 Sol</td><td>60.5</td><td>+8.7</td><td>最上位の品質</td></tr>
  </tbody>
</table>

<div class="evidence-box"><strong>読み取り：</strong>Sol − Terra は 2.8 点。Terra は Sol より低価格でも、GPT-5.5 を 5.9 点上回る。したがって、通常業務の標準に Terra を置く合理性がある。</div>
<div class="source-line">出典：OpenAI「GPT-5.6 Preview System Card」p.14。スコアは用途別の評価であり、万能な総合順位ではない。</div>
<div class="footer-message">Terra は<span class="accent">性能を保ちながら</span>日常利用へ寄せられる</div>

---

<div class="top-label">GPT-5.6 モデル選び | 4/7</div>

# Plus では、Codex で3モデルを選べる

<p class="subtitle">通常のChatGPT会話と Codex では、選べるモデルの範囲が異なる</p>

<table class="mini-table">
  <thead><tr><th>利用場所</th><th>Plus での GPT-5.6 利用</th><th>実務上の意味</th></tr></thead>
  <tbody>
    <tr><td>通常の ChatGPT 会話</td><td>Sol の Medium / High</td><td>Terra / Luna は直接選択できない</td></tr>
    <tr class="target"><td><strong>Codex</strong></td><td><strong>Sol / Terra / Luna</strong></td><td><strong>作業の難しさでモデルを使い分けられる</strong></td></tr>
    <tr><td>OpenAI API</td><td>Sol / Terra / Luna（従量課金）</td><td>アプリ側でモデルを指定する</td></tr>
  </tbody>
</table>

<div class="position-box"><strong>注意：</strong>GPT-5.6 の利用上限やロールアウトはプラン・アカウント・ワークスペース設定により変動する。Terra を選んだから Sol の利用枠が必ず温存される、とまでは公式に保証されていない。</div>
<div class="source-line">出典：OpenAI Help Center「GPT-5.6 in ChatGPT」（2026-07-10 確認）</div>
<div class="footer-message">Plus の Codex では、<span class="accent">モデルを選ぶ余地</span>がある</div>

---

<div class="top-label">GPT-5.6 モデル選び | 5/7</div>

# 迷ったら「重要度 × 複雑さ」で決める

<p class="subtitle">性能の序列ではなく、成果物の失敗コストと問題の難しさで使い分ける</p>

<div class="decision-grid">
  <div class="rowhead">成果物の重要度<br><span>× タスクの複雑さ</span></div>
  <div class="head">定型・単純</div>
  <div class="head">判断が必要</div>
  <div class="head">難問・曖昧</div>
  <div class="rowhead">低い<br><span>下書き・社内処理</span></div>
  <div>Luna<br><span>大量・反復</span></div>
  <div class="recommended"><strong>Terra</strong><br><span>日常の標準</span></div>
  <div class="recommended"><strong>Terra</strong><br><span>必要十分</span></div>
  <div class="rowhead">高い<br><span>顧客・設計判断</span></div>
  <div class="recommended"><strong>Terra</strong><br><span>確認を添える</span></div>
  <div class="recommended"><strong>Terra</strong><br><span>深く考えさせる</span></div>
  <div style="background:#1f3864;color:#fff"><strong>Sol</strong><br><span>初手の品質を取る</span></div>
</div>

<div class="transition-line">迷ったら Terra で開始し、成果物の重要度・複雑さが上がる場面だけ Sol に切り替える</div>
<div class="footer-message">標準は<span class="accent">Terra</span>、品質が決定的な場面だけ<span class="accent">Sol</span></div>

---

<div class="top-label">GPT-5.6 モデル選び | 6/7</div>

# 推論量も「常に最大」ではなく、タスクに合わせる

<p class="subtitle">GPT-5.6 は reasoning effort を調整可能。モデルの階層と合わせて、品質・速度を設計する</p>

<div class="split">
  <div class="soft-card"><h2>標準設定の考え方</h2><ul class="compact"><li>短時間で答えが出る作業：低い推論量</li><li>通常の開発・調査：中程度から開始</li><li>設計・検証が必要：高い推論量を試す</li></ul></div>
  <div class="soft-card"><h2>評価すべきもの</h2><ul class="compact"><li>正しさ・完成度</li><li>必要な証拠やテストの有無</li><li>応答時間と利用上限</li><li>モデルを上げたときの実測の改善</li></ul></div>
</div>

<div class="proposal"><strong>運用の原則：</strong>「最大のモデル × 最大の推論量」をデフォルトにせず、目的に対して十分な設定を測定して選ぶ。</div>
<div class="footer-message">最適化すべきは思考量ではなく、<span class="accent">成果に対する品質</span></div>

---

<div class="top-label">GPT-5.6 モデル選び | 7/7</div>

# 推奨する使い分け

<p class="subtitle">Plus × Codex では、まずこの運用から始める</p>

<div class="numbered-summary">
  <div class="card"><div class="summary-no">1</div><div class="card-title">標準を Terra にする</div><div class="card-body">普段のコード作業、調査、資料作成を Terra で開始する。</div></div>
  <div class="card"><div class="summary-no">2</div><div class="card-title">難問だけ Sol にする</div><div class="card-body">設計、高難度実装、重要レビューなど、品質差に価値があるときだけ切り替える。</div></div>
  <div class="card"><div class="summary-no">3</div><div class="card-title">Luna を定型処理に使う</div><div class="card-body">大量の整形・抽出・分類など、速度・回数が重要な作業に使う。</div></div>
</div>

<div class="proposal"><strong>最初の一歩：</strong>次の通常タスクを Terra で実施し、Sol が必要だったケースだけをメモする。1〜2週間で、自分の作業に合う切り替え条件が見えてくる。</div>
<div class="footer-message">GPT-5.6 を使いこなす鍵は、<span class="accent">モデル選択を習慣にすること</span></div>

---

<div class="top-label">GPT-5.6 モデル選び | 参考</div>

# 参考資料

<div class="soft-card">
  <ul class="compact">
    <li>OpenAI, <a href="https://help.openai.com/en/articles/20001354">GPT-5.6 in ChatGPT</a></li>
    <li>OpenAI, <a href="https://developers.openai.com/api/docs/guides/latest-model">Model guidance / Using GPT-5.6</a></li>
    <li>OpenAI, <a href="https://openai.com/index/previewing-gpt-5-6-sol/">Previewing GPT-5.6 Sol</a></li>
    <li>OpenAI, <a href="https://deploymentsafety.openai.com/gpt-5-6-preview/gpt-5-6-preview.pdf">GPT-5.6 Preview System Card</a></li>
  </ul>
</div>

<div class="position-box"><strong>更新性に関する注記：</strong>モデルの提供範囲、利用上限、プラン別の選択肢は段階的ロールアウトや設定により変動する。利用時はモデルピッカーの表示と公式ヘルプを確認する。</div>
<div class="footer-message">根拠は公式資料、判断は<span class="accent">自分の実務タスク</span>で検証する</div>
