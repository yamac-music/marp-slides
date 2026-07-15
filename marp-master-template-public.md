---
marp: true
theme: default
size: 16:9
paginate: false
style: |
  :root {
    --navy: #1f3864;
    --navy-2: #244b84;
    --blue: #2e5fa3;
    --gold: #e8c15a;
    --gold-2: #b98b16;
    --text: #22324a;
    --muted: #667085;
    --line: #c9d2de;
    --soft: #f4f6f9;
  }
  section { font-family: "BIZ UDPGothic", "Hiragino Sans", "Yu Gothic", "YuGothic", "Noto Sans JP", sans-serif; position: relative; overflow: hidden; box-sizing: border-box; color: var(--text); background: #fff; border-top: 24px solid #1f3864; padding: 58px 64px 76px; font-size: 20px; line-height: 1.55; }
  section::before { display: none !important; }
  h1 { margin: 0; color: var(--navy); font-size: 39px; line-height: 1.2; font-weight: 700; letter-spacing: -0.01em; }
  h2 { margin: 0 0 10px; color: var(--navy); font-size: 24px; line-height: 1.25; font-weight: 700; }
  h3 { margin: 0 0 9px; color: var(--navy); font-size: 20px; line-height: 1.3; font-weight: 700; }
  p { margin: 0; } ul { margin: 0; padding-left: 1.1em; } li { margin: 0 0 5px; }
  .top-label { position: absolute; top: -19px; right: 64px; z-index: 2; color: #fff; font-size: 13px; line-height: 1.2; }
  .subtitle { margin-top: 14px; color: var(--muted); font-size: 21px; line-height: 1.5; }
  .usage-note { display: inline-block; margin-top: 15px; padding: 5px 10px; border-radius: 3px; background: #fff4cf; color: #72520c; font-size: 14px; font-weight: 700; }
  .cover h1 { margin-top: 56px; font-size: 48px; letter-spacing: -0.02em; }
  .cover .subtitle { max-width: 760px; font-size: 23px; }
  .cover-rule { width: 76px; height: 5px; margin-top: 30px; background: var(--gold-2); }
  .cover-message { max-width: 780px; margin-top: 22px; color: var(--navy); font-size: 28px; line-height: 1.45; font-weight: 700; }
  .cover-meta { position: absolute; left: 54px; bottom: 86px; color: var(--muted); font-size: 15px; }
  .section-divider { margin-top: 105px; max-width: 790px; }
  .section-divider .eyebrow { color: var(--gold-2); font-size: 18px; font-weight: 700; letter-spacing: 0.08em; }
  .section-divider h1 { margin-top: 16px; font-size: 46px; }
  .section-divider p { margin-top: 20px; color: var(--muted); font-size: 23px; }
  .blue-line { margin-top: 12px; color: var(--blue); font-size: 21px; font-weight: 700; }
  .section-label { margin: 24px 0 12px; color: var(--navy); font-size: 22px; font-weight: 700; }
  .position-box, .evidence-box, .proposal { margin-top: 20px; padding: 15px 18px; border: 0; border-left: 5px solid var(--line); border-radius: 0; background: var(--soft); font-size: 17px; }
  .evidence-box, .proposal { border-left-color: var(--gold-2); background: #fff9ea; }
  .cards-3, .cards-2, .numbered-summary { display: grid; gap: 18px; }
  .cards-3, .numbered-summary { grid-template-columns: repeat(3, 1fr); }
  .cards-2 { grid-template-columns: repeat(2, 1fr); }
  .split { display: grid; grid-template-columns: 1fr 1fr; gap: 22px; margin-top: 22px; }
  .insight-layout { display: grid; grid-template-columns: 0.8fr 1.2fr; gap: 34px; align-items: center; margin-top: 34px; }
  .metric { padding: 22px 18px; border-left: 6px solid var(--gold-2); background: var(--soft); }
  .metric-number { color: var(--navy); font-size: 66px; line-height: 1; font-weight: 700; }
  .metric-label { margin-top: 10px; color: var(--muted); font-size: 17px; }
  .insight-copy { font-size: 21px; line-height: 1.55; }
  .insight-copy strong { color: var(--navy); }
  .timeline { display: grid; grid-template-columns: repeat(3, 1fr); gap: 0; margin-top: 34px; }
  .timeline-step { min-height: 165px; padding: 0 22px; border-left: 2px solid var(--line); }
  .timeline-step:first-child { border-left: 0; padding-left: 0; }
  .timeline-no { color: var(--gold-2); font-size: 17px; font-weight: 700; }
  .timeline-title { margin-top: 12px; color: var(--navy); font-size: 23px; font-weight: 700; }
  .timeline-body { margin-top: 9px; font-size: 16px; line-height: 1.45; }
  .closing { margin-top: 104px; max-width: 930px; color: var(--navy); font-size: 42px; line-height: 1.35; font-weight: 700; }
  .closing-note { margin-top: 24px; color: var(--muted); font-size: 20px; }
  .media-layout { display: grid; grid-template-columns: 1fr 1fr; gap: 34px; align-items: center; margin-top: 24px; }
  .media-frame { display: flex; min-height: 285px; align-items: center; justify-content: center; border: 2px dashed #aeb9c8; border-radius: 8px; background: var(--soft); color: var(--muted); font-size: 17px; text-align: center; }
  .media-copy { font-size: 20px; line-height: 1.55; }
  .media-copy strong { color: var(--navy); }
  .quote { margin-top: 60px; max-width: 940px; padding-left: 30px; border-left: 6px solid var(--gold-2); color: var(--navy); font-size: 34px; line-height: 1.45; font-weight: 700; }
  .quote-byline { margin: 20px 0 0 36px; color: var(--muted); font-size: 17px; }
  .matrix { display: grid; grid-template-columns: 145px repeat(3, 1fr); margin-top: 24px; border-top: 1px solid var(--line); border-left: 1px solid var(--line); font-size: 16px; }
  .matrix > div { min-height: 58px; padding: 12px; border-right: 1px solid var(--line); border-bottom: 1px solid var(--line); }
  .matrix .head { background: var(--navy); color: #fff; font-weight: 700; }
  .matrix .rowhead { background: var(--soft); color: var(--navy); font-weight: 700; }
  .matrix .recommended { background: #fff8e4; }
  .reference-list { margin-top: 28px; font-size: 18px; line-height: 1.8; }
  .figure-only { display: flex; min-height: 365px; align-items: center; justify-content: center; margin-top: 20px; border: 2px dashed #aeb9c8; border-radius: 8px; background: var(--soft); color: var(--muted); font-size: 18px; text-align: center; }
  .figure-row { display: grid; grid-template-columns: 1fr 1fr; gap: 22px; margin-top: 25px; }
  .figure-row .media-frame { min-height: 230px; }
  .columns-3 { display: grid; grid-template-columns: repeat(3, 1fr); gap: 22px; margin-top: 24px; }
  .columns-3 > div { min-height: 178px; padding: 16px; border-left: 2px solid var(--line); }
  .columns-3 > div:first-child { border-left: 0; }
  .columns-3 h2 { font-size: 22px; }
  .center-stage { display: flex; min-height: 365px; flex-direction: column; align-items: center; justify-content: center; text-align: center; }
  .center-stage h1 { max-width: 940px; font-size: 46px; }
  .center-stage p { max-width: 800px; margin-top: 18px; color: var(--muted); font-size: 22px; }
  .code-sample { margin-top: 20px; padding: 16px 20px; border-radius: 8px; background: #172033; color: #e9eef8; font-family: "SFMono-Regular", Consolas, monospace; font-size: 16px; line-height: 1.5; white-space: pre-wrap; }
  .small-text { font-size: 16px; line-height: 1.38; }
  section.no-header { border-top: 0; padding-top: 54px; }
  section.no-header .top-label { display: none; }
  .text-center { text-align: center; }
  .h1-text-center { text-align: center; }
  .content-image-right .media-layout { grid-template-columns: 0.9fr 1.1fr; }
  .content-image-left .media-layout { grid-template-columns: 1.1fr 0.9fr; }
  section.layout-section { background: #f4f6f9; }
  section.layout-quote { background: #fffdf8; }
  .card, .soft-card { border: 0; border-top: 3px solid var(--line); border-radius: 0; background: #fff; padding: 17px 18px; }
  .soft-card { background: var(--soft); }
  .card strong, .soft-card strong { color: var(--navy); }
  .card-number { display: inline-block; margin-right: 8px; color: var(--blue); font-weight: 700; }
  .card-title { color: var(--navy); font-weight: 700; font-size: 20px; line-height: 1.25; }
  .card-body { margin-top: 12px; color: #3a3f47; font-size: 16.5px; }
  .compact { font-size: 15.5px; line-height: 1.42; }
  .pill { display: inline-block; padding: 7px 16px; border-radius: 999px; background: var(--navy); color: #fff; font-size: 15px; font-weight: 700; }
  .pill.gold { background: var(--gold-2); } .pill.gray { background: #aeb4bd; }
  .mini-table { width: 100% !important; table-layout: fixed; border-collapse: collapse; font-size: 14px; line-height: 1.45; margin-top: 16px; }
  .mini-table th { background: var(--navy); color: #fff; font-weight: 700; text-align: left; }
  .mini-table th, .mini-table td { border: 0; border-bottom: 1px solid var(--line); padding: 10px 11px; vertical-align: top; }
  .mini-table .target { background: #fff8e4; }
  .source-line { margin-top: 10px; color: #6b7280; font-size: 12px; }
  .icon { width: 30px; height: 30px; object-fit: contain; vertical-align: middle; margin-right: 8px; }
  .icon-lg { width: 58px; height: 58px; object-fit: contain; margin-bottom: 10px; }
  .icon-grid { display: grid; grid-template-columns: repeat(5, 1fr); gap: 13px; margin-top: 17px; }
  .icon-sample { min-height: 86px; padding: 10px; border: 1.5px solid var(--line); border-radius: 8px; background: var(--soft); text-align: center; font-size: 13px; }
  .icon-sample img { display: block; width: 42px; height: 42px; object-fit: contain; margin: 0 auto 6px; }
  .transition-line { margin-top: 12px; color: #344054; font-size: 15px; text-align: center; }
  .footer-message { position: absolute; left: 0; right: 0; bottom: 0; min-height: 48px; padding: 11px 58px 10px; background: var(--navy); color: #fff; font-size: 20px; line-height: 1.25; text-align: center; z-index: 3; }
  .footer-message .accent, .accent { color: var(--gold); }
  .summary-no { width: 36px; height: 36px; border-radius: 50%; background: #f0f4fa; color: var(--blue); display: flex; align-items: center; justify-content: center; font-size: 20px; font-weight: 700; margin-bottom: 10px; }
  .agenda-list { display:grid; grid-template-columns:repeat(2,1fr); gap:0 46px; margin-top:30px; counter-reset:agenda; }
  .agenda-list div { display:flex; align-items:baseline; min-height:60px; border-bottom:1px solid var(--line); color:var(--navy); font-size:22px; font-weight:700; }
  .agenda-list div::before { content:counter(agenda, decimal-leading-zero); counter-increment:agenda; width:66px; color:var(--gold-2); font-size:16px; }
  .takeaway { margin-top:58px; max-width:960px; padding:28px 34px; border-top:4px solid var(--gold-2); background:var(--soft); color:var(--navy); font-size:34px; line-height:1.42; font-weight:700; }
  .takeaway-note { margin-top:22px; color:var(--muted); font-size:19px; }
  .flow { display:flex; align-items:stretch; gap:0; margin-top:34px; }
  .flow-step { position:relative; flex:1; min-height:156px; padding:18px 28px 18px 18px; border:1px solid var(--line); background:#fff; }
  .flow-step + .flow-step { border-left:0; }
  .flow-step + .flow-step::before { content:""; position:absolute; left:-1px; top:50%; width:0; height:0; border-top:13px solid transparent; border-bottom:13px solid transparent; border-left:16px solid var(--gold-2); transform:translateY(-50%); }
  .flow-step h2 { font-size:21px; } .flow-step p { color:#3a3f47; font-size:16px; }
  .before-after { display:grid; grid-template-columns:1fr 92px 1fr; gap:20px; align-items:center; margin-top:34px; }
  .before-after .state { min-height:224px; padding:24px; border:1.5px solid var(--line); border-radius:8px; background:var(--soft); }
  .before-after .state.after { border-color:var(--gold-2); background:#fff9ea; }
  .before-after .arrow { color:var(--gold-2); font-size:54px; text-align:center; }
  .architecture { display:grid; grid-template-columns:1fr 70px 1fr 70px 1fr; align-items:center; margin-top:36px; }
  .architecture .node { min-height:154px; padding:20px; border:1.5px solid var(--line); border-radius:8px; background:var(--soft); text-align:center; }
  .architecture .node.primary { border-color:var(--gold-2); background:#fff9ea; }
  .architecture .arrow { color:var(--gold-2); font-size:44px; text-align:center; }
  .case-layout { display:grid; grid-template-columns:0.9fr 1.1fr; gap:36px; align-items:stretch; margin-top:30px; }
  .case-label { color:var(--gold-2); font-size:16px; font-weight:700; letter-spacing:.06em; }
  .case-claim { margin-top:16px; color:var(--navy); font-size:29px; line-height:1.38; font-weight:700; }
  .case-fact { padding:22px; border-left:5px solid var(--gold-2); background:var(--soft); font-size:18px; line-height:1.55; }
  .faq { display:grid; grid-template-columns:1fr 1fr; gap:16px 22px; margin-top:24px; }
  .faq-item { padding:14px 16px; border-bottom:1px solid var(--line); }
  .faq-q { color:var(--navy); font-size:19px; font-weight:700; }.faq-a { margin-top:8px; color:#3a3f47; font-size:16px; }
  .decision-tree { display:grid; grid-template-columns:1fr 64px 1fr 64px 1fr; gap:0; align-items:center; margin-top:56px; }
  .decision-tree .question,.decision-tree .answer { min-height:102px; padding:18px; border:1.5px solid var(--line); border-radius:8px; background:var(--soft); text-align:center; color:var(--navy); font-size:20px; font-weight:700; }
  .decision-tree .answer { border-color:var(--gold-2); background:#fff9ea; }.decision-tree .branch { color:var(--gold-2); font-size:38px; text-align:center; }
  .data-points { display:grid; grid-template-columns:repeat(4,1fr); gap:18px; margin-top:35px; }.data-points > div { padding:18px 14px; border-top:3px solid var(--navy); background:var(--soft); }.data-points strong { display:block; color:var(--navy); font-size:31px; }.data-points span { display:block; margin-top:8px; color:var(--muted); font-size:15px; }
  .design-rules { display:grid; grid-template-columns:repeat(2,1fr); gap:20px 36px; margin-top:26px; }.design-rules > div { min-height:98px; padding:14px 0 0 18px; border-left:4px solid var(--gold-2); }.design-rules h2 { font-size:22px; }.design-rules p { color:#3a3f47; font-size:16px; line-height:1.48; }
---

<!--
使い方：このファイルを複製し、各スライドの top-label / 見出し / 本文を置き換える。
推奨構成：表紙 → 結論 → 根拠 → 比較 → 実行方針 → まとめ。
-->

<!-- _class: layout-cover -->
<div class="top-label">資料名 | 表紙</div>

<div class="cover">

# 資料タイトル

<p class="subtitle">結論をひと目で理解できる、副題を一文で置く</p>
<div class="usage-note">使う場面：初回説明、提案書、意思決定資料の表紙</div>
<div class="cover-rule"></div>
<div class="cover-message">この資料で相手に理解・判断・行動してほしいことを、端的に伝える。</div>
<div class="cover-meta">対象者 / 作成日 / 必要なら部署名</div>

</div>

<div class="footer-message">表紙は<span class="accent">「何のための資料か」だけ</span>を伝える</div>

---

<!-- _class: layout-section -->
<div class="top-label">資料名 | セクション</div>

<div class="section-divider">
  <div class="eyebrow">SECTION 01</div>
  <div class="usage-note">使う場面：話題を切り替え、次の論点を予告したいとき</div>
  <h1>見出しは、<br>次に考えるべき問いを置く</h1>
  <p>詳細や図表の前に、ここでの論点と結論の方向性を一文で示す。</p>
</div>

<div class="footer-message">章の切り替えでは、<span class="accent">情報より論点</span>を先に置く</div>

---

<!-- _class: layout-metric -->
<div class="top-label">資料名 | 根拠</div>

# 数字は「何を意味するか」まで見せる

<p class="subtitle">大きな数値は一つに絞り、読み手に必要な解釈を隣に置く</p>
<div class="usage-note">使う場面：KPI、調査結果、コスト削減や改善幅を強調したいとき</div>

<div class="insight-layout">
  <div class="metric"><div class="metric-number">+38%</div><div class="metric-label">前期比の改善率（例）</div></div>
  <div class="insight-copy"><strong>改善は、実行量ではなく意思決定の速さで生まれた。</strong><br><br>数字だけを置かず、背景・比較対象・この数字が示す判断を短く説明する。</div>
</div>

<div class="source-line">出典：データの出所、集計条件、対象期間を簡潔に記載</div>
<div class="footer-message">数字は<span class="accent">事実 → 解釈 → 判断</span>の順で見せる</div>

---

<!-- _class: layout-compare -->
<div class="top-label">資料名 | 比較</div>

# 比較は、選ぶ基準を先に決める

<p class="subtitle">全項目を並べるより、意思決定に効く比較軸を3〜4個へ絞る</p>
<div class="usage-note">使う場面：製品・施策・モデルなど、選択肢から一つを選ぶとき</div>

<table class="mini-table">
  <thead><tr><th>選択肢</th><th>品質</th><th>コスト</th><th>向く場面</th></tr></thead>
  <tbody>
    <tr class="target"><td><strong>推奨案</strong></td><td>十分に高い</td><td>バランスがよい</td><td><strong>日常的な利用</strong></td></tr>
    <tr><td>上位案</td><td>最高</td><td>高い</td><td>難しい判断</td></tr>
    <tr><td>軽量案</td><td>必要十分</td><td>低い</td><td>大量・定型処理</td></tr>
  </tbody>
</table>

<div class="proposal"><strong>推奨：</strong>標準の選択肢を明確にし、上位案へ切り替える条件を一文で決める。</div>
<div class="footer-message">比較表の目的は、<span class="accent">情報収集ではなく選択</span></div>

---

<!-- _class: layout-timeline -->
<div class="top-label">資料名 | 進め方</div>

# 実行計画は「次の3手」に分ける

<p class="subtitle">行動・担当・確認点が読み取れる粒度にして、細かいタスク表は別紙へ回す</p>
<div class="usage-note">使う場面：導入計画、ロードマップ、合意後の最初のアクションを示すとき</div>

<div class="timeline">
  <div class="timeline-step"><div class="timeline-no">STEP 01</div><div class="timeline-title">始める</div><div class="timeline-body">対象を一つ決め、現状値と成功条件を共有する。</div></div>
  <div class="timeline-step"><div class="timeline-no">STEP 02</div><div class="timeline-title">試す</div><div class="timeline-body">小さく実行し、品質・時間・費用の変化を確認する。</div></div>
  <div class="timeline-step"><div class="timeline-no">STEP 03</div><div class="timeline-title">広げる</div><div class="timeline-body">結果を基準に、対象範囲と運用ルールを段階的に広げる。</div></div>
</div>

<div class="footer-message">行動の説明は、<span class="accent">3段階まで</span>に抑える</div>

---

<!-- _class: layout-closing -->
<div class="top-label">資料名 | 結論</div>

<div class="usage-note">使う場面：提案・報告・説明の最後に、意思決定や次の一手を残すとき</div>
<div class="closing">結論は、<br>次に取る行動まで含めて言い切る。</div>
<div class="closing-note">例：まず通常業務で標準案を試し、効果が測れた領域から段階的に広げる。</div>

<div class="footer-message">最後に残すのは、<span class="accent">「なので、何をするか」</span></div>

---

<!-- _class: layout-media-right -->
<div class="top-label">資料名 | 図解 右</div>

# 文章と図を、同じ重さで見せる

<p class="subtitle">図や写真を右に置き、左側で「何が重要か」を解説する</p>
<div class="usage-note">使う場面：サービス概要、プロダクト画面、構成図、事例の説明</div>

<div class="media-layout">
  <div class="media-copy"><strong>図を見せる前に、結論を一文で置く。</strong><br><br>本文は3点まで。画像の中に書いてあることを、もう一度文章で繰り返さない。</div>
  <div class="media-frame">ここにスクリーンショット、<br>写真、構成図を配置</div>
</div>

<div class="footer-message">図は<span class="accent">「見る理由」</span>を添えて初めて伝わる</div>

---

<!-- _class: layout-media-left -->
<div class="top-label">資料名 | 図解 左</div>

# 図を先に、意味は右で補う

<p class="subtitle">視覚的な証拠を先に見せたいときは、図を左側へ置く</p>
<div class="usage-note">使う場面：ビフォー・アフター、利用シーン、画面比較、デモの要点</div>

<div class="media-layout">
  <div class="media-frame">ここにビフォー・アフター、<br>画面、写真を配置</div>
  <div class="media-copy"><strong>見せるものは一つ、伝えることも一つ。</strong><br><br>矢印や枠線は、視線を誘導するために必要な箇所だけへ使う。</div>
</div>

<div class="footer-message">画面比較では、<span class="accent">違いを一つに絞る</span></div>

---

<!-- _class: layout-two-column -->
<div class="top-label">資料名 | 二つの観点</div>

# 二つの観点を対比させる

<p class="subtitle">片方を主役にせず、両方を同じ粒度で説明したい場合のレイアウト</p>
<div class="usage-note">使う場面：現状と理想、メリットと注意点、利用者と運用者の視点</div>

<div class="split">
  <div class="soft-card"><h2>観点A</h2><ul class="compact"><li>主張を一行で置く</li><li>根拠を2〜3点に絞る</li><li>必要なら小さなアイコンを添える</li></ul></div>
  <div class="soft-card"><h2>観点B</h2><ul class="compact"><li>同じ粒度で対になる主張</li><li>重複する説明は避ける</li><li>最後に両方を統合して結論へつなぐ</li></ul></div>
</div>

<div class="footer-message">対比は、<span class="accent">同じ比較軸</span>でそろえる</div>

---

<!-- _class: layout-three-options -->
<div class="top-label">資料名 | 三択</div>

# 選択肢は三つまでに整理する

<p class="subtitle">三案の役割を分け、中央に推奨案を置くと選ぶ理由が伝わりやすい</p>
<div class="usage-note">使う場面：導入案、優先順位、モデル選定、投資レベルの比較</div>

<div class="cards-3" style="margin-top:25px">
  <div class="card"><div class="card-title">選択肢A</div><div class="card-body">低コスト・軽量。<br>大量の定型処理に向く。</div></div>
  <div class="card" style="border-color:#b98b16;background:#fff9ea"><div class="card-title">推奨案</div><div class="card-body">品質・時間・費用のバランス。<br><strong>標準として使う。</strong></div></div>
  <div class="card"><div class="card-title">選択肢C</div><div class="card-body">最高品質。<br>失敗コストが高い場面に絞る。</div></div>
</div>

<div class="footer-message">選択肢は、<span class="accent">役割で区別</span>すると選びやすい</div>

---

<!-- _class: layout-matrix -->
<div class="top-label">資料名 | 判断マトリクス</div>

# 複数条件の判断は、マトリクスで整理する

<p class="subtitle">「どの条件なら、どの対応か」を一枚で共有する</p>
<div class="usage-note">使う場面：判断基準、権限分担、リスク対応、優先度の整理</div>

<div class="matrix">
  <div class="head"></div><div class="head">低い</div><div class="head">中程度</div><div class="head">高い</div>
  <div class="rowhead">影響度</div><div>記録する</div><div class="recommended">担当者が確認</div><div>責任者へ共有</div>
  <div class="rowhead">緊急度</div><div>次回対応</div><div>当日中に確認</div><div class="recommended">即時に対応</div>
</div>

<div class="footer-message">判断基準は、<span class="accent">文章より表</span>で共有する</div>

---

<!-- _class: layout-quote -->
<div class="top-label">資料名 | 引用・メッセージ</div>

# 一つの言葉を印象に残す

<div class="usage-note">使う場面：顧客の声、調査の要旨、方針の宣言、会議での合意事項</div>

<div class="quote">「利用者が迷わず選べることが、最も価値のある改善だった。」</div>
<div class="quote-byline">発言者・調査名・日付などを記載</div>

<div class="footer-message">引用は、<span class="accent">メッセージを一つに絞る</span>と効く</div>

---

<!-- _class: layout-risk -->
<div class="top-label">資料名 | 注意点</div>

# 注意点は、対策とセットで示す

<p class="subtitle">不安を並べるだけでなく、どこまでなら進められるかを明らかにする</p>
<div class="usage-note">使う場面：リスク説明、導入時の留意点、レビュー結果、運用ガードレール</div>

<div class="split">
  <div class="soft-card"><h2>想定する注意点</h2><ul class="compact"><li>品質のばらつき</li><li>権限・データの扱い</li><li>利用条件やコストの変動</li></ul></div>
  <div class="evidence-box"><h2>取るべき対策</h2><ul class="compact"><li>確認が必要な範囲を決める</li><li>外部操作は承認を必須にする</li><li>小規模に試し、指標で判断する</li></ul></div>
</div>

<div class="footer-message">注意点は、<span class="accent">対策まで示して初めて前進できる</span></div>

---

<!-- _class: layout-references -->
<div class="top-label">資料名 | 参考</div>

# 参考資料・注記

<p class="subtitle">根拠の確認先を残しつつ、本文の流れは止めない</p>
<div class="usage-note">使う場面：資料末尾、補足、調査レポート、データの出典一覧</div>

<div class="reference-list">
  <div>1. 発行元「資料名」｜公開日・URL</div>
  <div>2. 発行元「調査名」｜対象・集計期間・URL</div>
  <div>3. 発行元「ガイドライン」｜参照日・URL</div>
</div>

<div class="position-box"><strong>注記：</strong>ページ内の数値・画像・アイコンの出典や利用条件を、ここへまとめて記載する。</div>
<div class="footer-message">根拠は<span class="accent">追跡できる形</span>で残す</div>

---

<!-- _class: no-header -->
# タイトル・図のみ

<p class="subtitle">図がメインのスライドは、説明を最小限にする</p>
<div class="usage-note">使う場面：構成図、画面キャプチャ、写真、デモ画面を大きく見せたいとき</div>

<div class="figure-only">ここに大きな図・画面・写真を配置<br>（推奨：横幅 800px 程度）</div>

<div class="footer-message">図が主役なら、<span class="accent">文字は脇役</span>にする</div>

---

<!-- _class: no-header -->
# 複数の図を並べて比較する

<p class="subtitle">比較対象が二つなら、同じ大きさ・同じ高さで並べる</p>
<div class="usage-note">使う場面：ビフォー・アフター、二案比較、画面差分、二つの事例</div>

<div class="figure-row">
  <div class="media-frame">図・画面 A</div>
  <div class="media-frame">図・画面 B</div>
</div>

<div class="footer-message">並べる図は、<span class="accent">比較してほしい軸</span>をそろえる</div>

---

<!-- _class: content-image-right -->
<div class="top-label">資料名 | 図と説明</div>

# 図を右に、説明を左に置く

<p class="subtitle">`content-image-right` を付けると、右側を少し広く取る</p>
<div class="usage-note">使う場面：図の余白が多い、画面の読み取りに幅が必要、説明を先に読ませたいとき</div>

<div class="media-layout">
  <div class="media-copy"><strong>ここに結論と説明を置く。</strong><br><br>図の中の文字をそのまま転記せず、見るべき箇所と意味だけを補う。</div>
  <div class="media-frame">図・画面・写真</div>
</div>

<div class="footer-message">右図レイアウトは、<span class="accent">説明から視線を導く</span></div>

---

<!-- _class: content-image-left -->
<div class="top-label">資料名 | 図と説明</div>

# 左図、右で意味を補う

<p class="subtitle">`content-image-left` を付けると、左側を少し広く取る</p>
<div class="usage-note">使う場面：画面やビフォー・アフターを最初に見せ、解釈を後から添えたいとき</div>

<div class="media-layout">
  <div class="media-frame">図・画面・写真</div>
  <div class="media-copy"><strong>右側では、図が意味することを短く説明する。</strong><br><br>結論、理由、次のアクションの順に置くと読みやすい。</div>
</div>

<div class="footer-message">左図レイアウトは、<span class="accent">視覚的な証拠から入る</span></div>

---

<!-- _class: column-layout -->
<div class="top-label">資料名 | 3カラム</div>

# 三つの要素を同じ粒度で整理する

<p class="subtitle">`column-layout` は、順序よりも三つの観点を並列に見せたいときに使う</p>
<div class="usage-note">使う場面：3つの特徴、役割分担、評価軸、選択肢、成功条件</div>

<div class="columns-3">
  <div><h2>観点 1</h2><p class="compact">短い結論と、補足を2〜3点に絞る。</p></div>
  <div><h2>観点 2</h2><p class="compact">3カラムでは、各列の情報量をそろえる。</p></div>
  <div><h2>観点 3</h2><p class="compact">上下関係を付けたい場合は、別のレイアウトを使う。</p></div>
</div>

<div class="footer-message">3カラムは、<span class="accent">並列の関係</span>を見せるときに使う</div>

---

<!-- _class: align-center -->
<div class="top-label">資料名 | メッセージ</div>

<div class="center-stage">
  <div class="usage-note">使う場面：重要な転換点、メッセージ、ワークショップの問い、休憩前後</div>
  <h1>読み手に残したい<br>一文だけを、中央に置く。</h1>
  <p>背景・根拠・詳細は前後のスライドに任せる。</p>
</div>

<div class="footer-message">中央配置は、<span class="accent">一文を印象づける</span>ために使う</div>

---

<!-- _class: layout-code -->
<div class="top-label">資料名 | コード</div>

# コードは、読む範囲を絞って示す

<p class="subtitle">見せたい行だけを抜粋し、スライドではコード全体を読ませない</p>
<div class="usage-note">使う場面：実装方針、API利用例、設定例、レビューで議論したい差分</div>

<div class="code-sample">const response = await client.responses.create({
  model: "gpt-5.6-terra",
  input: "要件を3点に整理してください"
});</div>

<div class="proposal"><strong>説明の要点：</strong>このコードが何を実現するか、注意点は何かを一文で補う。</div>
<div class="footer-message">コードは、<span class="accent">議論したい箇所だけ</span>を見せる</div>

---

<!-- _class: small-text -->
<div class="top-label">資料名 | 補足</div>

# 情報量が多い補足スライド

<p class="subtitle">`small-text` は例外的に使い、原則は内容を分割する</p>
<div class="usage-note">使う場面：用語集、仕様一覧、出典の詳細、会議の配布資料として読ませる補足</div>

<div class="split">
  <div class="soft-card"><h2>使ってよい場合</h2><ul><li>投影より配布・後読みが主目的</li><li>一覧性が価値になる</li><li>短時間で説明する本編ではない</li></ul></div>
  <div class="soft-card"><h2>避けるべき場合</h2><ul><li>結論や意思決定を伝える本編</li><li>会場投影で読み上げるページ</li><li>図表を見ながら議論するページ</li></ul></div>
</div>

<div class="footer-message">小さい文字は、<span class="accent">情報を減らせない最後の手段</span></div>

---

<!-- _class: layout-icons -->
<div class="top-label">資料名 | 視覚的な強調 1/2</div>

# アイコンなしで、役割を見分けやすくする

<p class="subtitle">形ではなく、言葉・位置・色で意味を補助する。公開資料でも扱いやすい表現。</p>
<div class="usage-note">使う場面：ライセンスの確認が必要な素材を使わず、分類や優先度を示したいとき</div>

<div class="icon-grid">
  <div class="icon-sample"><strong>開発</strong><br>PC・実装</div>
  <div class="icon-sample"><strong>推論</strong><br>分析・判断</div>
  <div class="icon-sample"><strong>設定</strong><br>改善・最適化</div>
  <div class="icon-sample"><strong>比較</strong><br>評価・成長</div>
  <div class="icon-sample"><strong>重要</strong><br>安全・確認</div>
  <div class="icon-sample"><strong>完了</strong><br>チェック・合意</div>
  <div class="icon-sample"><strong>連携</strong><br>接続・共有</div>
  <div class="icon-sample"><strong>出力</strong><br>表示・報告</div>
</div>

<div class="proposal"><strong>使い方：</strong>一つの資料ではラベルの種類を 3〜5 個に絞り、同じ意味には同じ色・同じ位置を使う。</div>
<div class="footer-message">素材がなくても、<span class="accent">情報の階層</span>は作れる</div>

---

<!-- _class: layout-icons -->
<div class="top-label">資料名 | 視覚的な強調 2/2</div>

# 記号と余白で、情報の優先度を付ける

<p class="subtitle">記号は装飾ではなく、読んでほしい順番を補助するために使う</p>
<div class="usage-note">使う場面：注意点、結論、比較結果、次のアクションを短く強調したいとき</div>

<div class="icon-grid" style="grid-template-columns:repeat(4,1fr)">
  <div class="icon-sample"><strong>01</strong> 順序・手順</div>
  <div class="icon-sample"><strong>→</strong> 流れ・変化</div>
  <div class="icon-sample"><strong>＋</strong> 追加・統合</div>
  <div class="icon-sample"><strong>×</strong> 除外・停止</div>
  <div class="icon-sample"><strong>!</strong> 注意・要確認</div>
  <div class="icon-sample"><strong>?</strong> 問い・未確定</div>
  <div class="icon-sample"><strong>✓</strong> 完了・承認</div>
  <div class="icon-sample"><strong>★</strong> 推奨・要点</div>
</div>

<div class="proposal"><strong>注意：</strong>色だけ、または記号だけに意味を預けない。短いラベルや見出しと組み合わせて伝える。</div>
<div class="footer-message">強調は、<span class="accent">読ませる順番</span>を作るために使う</div>

---

<!-- _class: layout-agenda -->
<div class="top-label">資料名 | 全体像</div>

# 話す順番を、最初に共有する

<p class="subtitle">議論の道筋が重要な資料では、章立てを先に見せて聞き手の負荷を下げる</p>
<div class="usage-note">使う場面：経営報告、提案、ワークショップ、複数論点を扱う説明</div>

<div class="agenda-list"><div>背景と課題</div><div>選択肢の比較</div><div>根拠と検証結果</div><div>推奨する方針</div><div>実行計画</div><div>決めてほしいこと</div></div>

<div class="footer-message">アジェンダは、<span class="accent">資料の地図</span>として使う</div>

---

<!-- _class: layout-takeaway -->
<div class="top-label">資料名 | 要点</div>

# このページで伝えること

<p class="subtitle">詳細に入る前に、聞き手に残す結論を一文で提示する</p>
<div class="usage-note">使う場面：要約、章の冒頭、重要な分析結果、役員向けの結論</div>

<div class="takeaway">標準案を採用し、例外だけを上位の判断プロセスに回すことで、品質と運用負荷を両立できる。</div>
<div class="takeaway-note">この後に「なぜそう言えるのか」を、データ・比較・実例で裏付ける。</div>

<div class="footer-message">結論先出しでは、<span class="accent">一文を太くする</span></div>

---

<!-- _class: layout-flow -->
<div class="top-label">資料名 | プロセス</div>

# 仕組みは、流れで見せる

<p class="subtitle">時系列または処理順に意味があるものは、箇条書きよりフローにする</p>
<div class="usage-note">使う場面：業務フロー、利用手順、承認プロセス、データ処理の説明</div>

<div class="flow"><div class="flow-step"><h2>入力</h2><p>依頼・データ・前提条件を受け取る。</p></div><div class="flow-step"><h2>判断</h2><p>基準に沿って、必要な確認を行う。</p></div><div class="flow-step"><h2>実行</h2><p>決定内容を、担当者または仕組みが実施する。</p></div><div class="flow-step"><h2>記録</h2><p>結果を残し、次回の改善につなげる。</p></div></div>

<div class="footer-message">フローでは、<span class="accent">1ステップ1動詞</span>にする</div>

---

<!-- _class: layout-before-after -->
<div class="top-label">資料名 | 変化</div>

# 変化は、前後を並べて見せる

<p class="subtitle">改善の価値は、導入前後の違いを同じ物差しで比べると伝わりやすい</p>
<div class="usage-note">使う場面：業務改善、UI改善、導入効果、運用ルール変更の説明</div>

<div class="before-after"><div class="state"><h2>導入前</h2><ul class="compact"><li>担当者ごとに手順が違う</li><li>確認が後工程に集中する</li><li>判断の理由が残らない</li></ul></div><div class="arrow">→</div><div class="state after"><h2>導入後</h2><ul class="compact"><li>判断基準を共通化する</li><li>確認すべき点を前倒しする</li><li>記録から継続的に改善する</li></ul></div></div>

<div class="footer-message">前後比較は、<span class="accent">同じ項目</span>で変化を示す</div>

---

<!-- _class: layout-architecture -->
<div class="top-label">資料名 | 構成</div>

# 構成は、要素と流れを最小限に描く

<p class="subtitle">システム全体を描く前に、今回理解してほしい3要素だけに絞る</p>
<div class="usage-note">使う場面：システム構成、データ連携、役割分担、サービス概要</div>

<div class="architecture"><div class="node"><h2>利用者</h2><p class="compact">依頼・操作・確認</p></div><div class="arrow">→</div><div class="node primary"><h2>中核の仕組み</h2><p class="compact">判断・処理・記録</p></div><div class="arrow">→</div><div class="node"><h2>業務システム</h2><p class="compact">参照・更新・通知</p></div></div>

<div class="proposal"><strong>補足：</strong>矢印には「何が流れるか」を必要な場合だけ書く。全接続を描かない。</div>
<div class="footer-message">構成図は、<span class="accent">理解に必要な範囲</span>だけ描く</div>

---

<!-- _class: layout-case -->
<div class="top-label">資料名 | 事例</div>

# 事例は、変化と再現条件を示す

<p class="subtitle">成功談だけで終わらせず、どんな条件で再現できるかを添える</p>
<div class="usage-note">使う場面：導入事例、PoC結果、プロジェクト報告、改善の横展開</div>

<div class="case-layout"><div><div class="case-label">CASE STUDY</div><div class="case-claim">確認作業を前倒ししたことで、後工程の手戻りを減らせた。</div></div><div class="case-fact"><strong>背景</strong><br>複数の担当者が、同じ確認を別々のタイミングで実施していた。<br><br><strong>打ち手</strong><br>入力時点のチェックと、例外時だけのレビューを導入した。<br><br><strong>再現条件</strong><br>判断基準と責任者を事前に決めておく。</div></div>

<div class="footer-message">事例は、<span class="accent">成果より再現条件</span>まで伝える</div>

---

<!-- _class: layout-faq -->
<div class="top-label">資料名 | よくある質問</div>

# よくある疑問を、先回りして解消する

<p class="subtitle">説明の最後に残りやすい不安を、短い答えとともに並べる</p>
<div class="usage-note">使う場面：導入説明、社内展開、提案の補足、説明会の末尾</div>

<div class="faq"><div class="faq-item"><div class="faq-q">Q. 最初から全社へ展開すべき？</div><div class="faq-a">A. まず対象業務を一つに絞り、効果と運用を確認する。</div></div><div class="faq-item"><div class="faq-q">Q. 誰が最終確認する？</div><div class="faq-a">A. 例外条件を定め、責任者が確認する範囲を明確にする。</div></div><div class="faq-item"><div class="faq-q">Q. 効果はどう測る？</div><div class="faq-a">A. 時間・品質・手戻りのうち、目的に合う指標を一つ選ぶ。</div></div><div class="faq-item"><div class="faq-q">Q. 途中で見直せる？</div><div class="faq-a">A. 定期的なレビュー日を決め、基準・対象・運用を更新する。</div></div></div>

<div class="footer-message">FAQは、<span class="accent">質問を短く、答えを具体的に</span></div>

---

<!-- _class: layout-decision-tree -->
<div class="top-label">資料名 | 判断フロー</div>

# 迷いがちな選択は、分岐で示す

<p class="subtitle">条件によって対応が変わる場合は、判断順を固定して説明する</p>
<div class="usage-note">使う場面：利用ガイド、承認基準、問い合わせ振り分け、モデル選定</div>

<div class="decision-tree"><div class="question">成果物の重要度は高い？</div><div class="branch">→</div><div class="question">複雑な判断・検証が必要？</div><div class="branch">→</div><div class="answer">はい：上位の確認プロセスへ<br><br>いいえ：標準の手順で進める</div></div>

<div class="transition-line">実際には、分岐は2〜3回までに抑えると、投影時にも判断しやすい。</div>
<div class="footer-message">分岐図は、<span class="accent">判断の順番</span>を決めるために使う</div>

---

<!-- _class: layout-data-points -->
<div class="top-label">資料名 | データ要約</div>

# 数字が複数あるときは、意味ごとに分ける

<p class="subtitle">ダッシュボードにせず、比較・推移・成果など役割の異なる数字を分離する</p>
<div class="usage-note">使う場面：実績報告、調査サマリー、KPIレビュー、導入効果の概況</div>

<div class="data-points"><div><strong>42%</strong><span>改善率<br>前年同月比</span></div><div><strong>3.2日</strong><span>対応時間<br>従来との差</span></div><div><strong>18件</strong><span>例外件数<br>要レビュー</span></div><div><strong>96%</strong><span>完了率<br>対象期間内</span></div></div>

<div class="source-line">出典：対象期間・集計条件・比較の基準を記載する</div>
<div class="footer-message">数字は、<span class="accent">何を測ったか</span>を必ず添える</div>

---

<!-- _class: layout-operating-model -->
<div class="top-label">資料名 | 運用設計</div>

# 役割分担は、担当と責任を分けて示す

<p class="subtitle">誰が動くかだけでなく、誰が決め、誰に共有するかまで揃える</p>
<div class="usage-note">使う場面：新しい運用、プロジェクト体制、ガバナンス、定常業務の設計</div>

<div class="matrix" style="grid-template-columns:150px 1.1fr 1.1fr .8fr"><div class="head">役割</div><div class="head">主な仕事</div><div class="head">決めること</div><div class="head">共有先</div><div class="rowhead">実行担当</div><div>日常の処理・一次確認</div><div>定められた基準内の対応</div><div>責任者</div><div class="rowhead">責任者</div><div class="recommended">例外の確認・品質管理</div><div class="recommended">基準外の判断</div><div>関係部署</div><div class="rowhead">意思決定者</div><div>方針・優先順位の決定</div><div>運用変更・投資判断</div><div>全体</div></div>

<div class="footer-message">体制図では、<span class="accent">仕事・決定・共有</span>を分ける</div>

---

<!-- _class: layout-appendix -->
<div class="top-label">資料名 | 付録</div>

# 補足情報は、結論を邪魔しない場所へ置く

<p class="subtitle">本編で使わない詳細は、後から確認できる付録として整理する</p>
<div class="usage-note">使う場面：前提条件、用語、データ定義、詳細スケジュール、追加の根拠</div>

<div class="split"><div class="soft-card"><h2>付録に入れるもの</h2><ul class="compact"><li>指標の定義と集計方法</li><li>比較表の全項目</li><li>検討の経緯や前提条件</li></ul></div><div class="soft-card"><h2>本編に残すもの</h2><ul class="compact"><li>聞き手が決めるための要点</li><li>結論を支える最小限の根拠</li><li>次に取るアクション</li></ul></div></div>

<div class="footer-message">付録は、<span class="accent">必要な人が深掘りできる場所</span>にする</div>

---

<!-- _class: layout-priority -->
<div class="top-label">資料名 | 優先順位</div>

# やることが多いときは、優先順位を明示する

<p class="subtitle">重要度と緊急度を混ぜず、着手順が分かる粒度に整理する</p>
<div class="usage-note">使う場面：施策の整理、バックログ、改善候補、投資検討、会議の意思決定</div>

<div class="matrix"><div class="head">優先度</div><div class="head">今期</div><div class="head">次期</div><div class="head">保留</div><div class="rowhead">高い価値</div><div class="recommended"><strong>最優先</strong><br>責任者と期限を決める</div><div>準備を始める</div><div>前提条件を確認</div><div class="rowhead">通常の価値</div><div>余力があれば着手</div><div class="recommended"><strong>計画に入れる</strong><br>効果を測る</div><div>定期的に見直す</div></div>

<div class="footer-message">優先順位では、<span class="accent">やらないこと</span>も見えるようにする</div>

---

<!-- _class: layout-design-rules -->
<div class="top-label">資料名 | デザインチェック</div>

# 伝わるための、4つの基本ルール

<p class="subtitle">迷ったら、装飾を足す前に「揃える・まとめる・余白・コントラスト」を確認する</p>
<div class="usage-note">使う場面：資料作成の開始前、レビュー時、テンプレートを別の題材へ転用するとき</div>

<div class="design-rules"><div><h2>揃える</h2><p>左端・上端・図と本文の幅を合わせる。原則は左揃え。中央揃えは一文だけを見せる場面に限定する。</p></div><div><h2>まとめる</h2><p>関係が強い情報は近づけ、関係が弱い情報は離す。色だけではなく、位置・見出し・線でも関係を示す。</p></div><div><h2>余白を取る</h2><p>文字と枠、図と文章、スライド端の間を詰めない。収まらない場合は、文字を小さくする前に内容を減らす。</p></div><div><h2>コントラストを付ける</h2><p>重要な一つだけを太さ・濃さ・背景で目立たせる。高彩度の色や、赤と緑だけで意味を区別することは避ける。</p></div></div>

<div class="footer-message">デザインは、<span class="accent">読み手の負担を減らすためのルール</span>である</div>
