[index.html.html](https://github.com/user-attachments/files/33751305/index.html.html)
<!doctype html>
<html lang="ja">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<meta name="theme-color" content="#fffaf7">
<title>リアクト！｜コミュニケーション診断</title>
<style>
:root{--ink:#414047;--muted:#77727b;--paper:#fffaf7;--card:#fff;--pink:#d78e9d;--pink-light:#f8e8ec;--blue:#8eaed4;--green:#7eae9a;--orange:#e6ad7a;--line:#eee4e2}
*{box-sizing:border-box}
body{margin:0;background:var(--paper);color:var(--ink);font-family:system-ui,-apple-system,"Noto Sans JP","Yu Gothic",Meiryo,sans-serif;line-height:1.65}
.wrap{max-width:760px;margin:auto;padding:20px 14px 44px}
header{text-align:center;padding:20px 8px 18px}
.kicker{font-size:.8rem;letter-spacing:.12em;color:#b77991;font-weight:700}
h1{font-size:2rem;margin:4px 0 2px;letter-spacing:.04em}
.subtitle{color:var(--muted);font-size:.92rem;margin:0}
.panel{background:var(--card);border:1px solid var(--line);border-radius:20px;padding:18px;margin:14px 0;box-shadow:0 4px 18px #5b414008}
h2{font-size:1.15rem;margin:0 0 8px}
.intro{font-size:.92rem;color:var(--muted);margin:0 0 14px}
.reaction-grid{display:grid;grid-template-columns:repeat(2,minmax(0,1fr));gap:10px}
.reaction{border:1px solid var(--line);border-radius:14px;padding:12px;background:#fffdfc}
.reaction label{display:block;font-weight:700;margin-bottom:7px}
.reaction small{display:block;color:var(--muted);font-weight:400;font-size:.76rem;min-height:2.4em}
.stepper{display:flex;align-items:center;justify-content:space-between;gap:8px;margin-top:9px}
.stepper button{width:40px;height:40px;border:1px solid #e6d9d8;background:#fff7f7;color:var(--ink);border-radius:12px;font-size:1.35rem;cursor:pointer}
.stepper input{width:58px;text-align:center;font-size:1.1rem;font-weight:700;border:1px solid var(--line);border-radius:10px;padding:8px 3px;color:var(--ink);background:white}
.actions{display:flex;gap:10px;margin-top:15px;flex-wrap:wrap}
button.primary{flex:1;min-height:48px;border:0;border-radius:14px;background:var(--pink);color:white;font-size:1rem;font-weight:700;cursor:pointer;padding:12px}
button.secondary{min-height:44px;border:1px solid var(--line);border-radius:14px;background:white;color:var(--ink);padding:10px 14px;cursor:pointer}
button:focus-visible,input:focus-visible{outline:3px solid #eac0cd;outline-offset:2px}
.notice{font-size:.82rem;color:var(--muted);background:#fff8f5;border-radius:12px;padding:11px 12px;margin-top:13px}
.result{display:none}
.result.show{display:block}
.result-head{text-align:center;padding:10px 2px 18px}
.pill{display:inline-block;background:var(--pink-light);color:#9e6074;border-radius:999px;padding:5px 12px;font-size:.8rem;font-weight:700}
.result-head h2{font-size:1.65rem;margin:10px 0 5px}
.result-head p{margin:0;color:var(--muted);font-size:.9rem}
.type-row{margin:15px 0}
.type-meta{display:flex;justify-content:space-between;gap:12px;font-weight:650;font-size:.95rem;margin-bottom:6px}
.percent{font-variant-numeric:tabular-nums}
.track{height:11px;background:#f0eceb;border-radius:999px;overflow:hidden}
.fill{height:100%;border-radius:999px;transition:width .35s ease}
.c-driving{background:var(--pink)}.c-expressive{background:var(--orange)}.c-amiable{background:var(--green)}.c-analytical{background:var(--blue)}
.dual{display:grid;grid-template-columns:1fr 1fr;gap:10px}
.stat{background:#fffaf8;border:1px solid var(--line);border-radius:14px;padding:13px}
.stat span{display:block;color:var(--muted);font-size:.82rem}
.stat strong{font-size:1.35rem}
h3{font-size:1rem;margin:18px 0 7px}
.body-copy{margin:0;font-size:.94rem}
ul{padding-left:1.25rem;margin:7px 0 0}
li{margin:5px 0;font-size:.93rem}
.reflection{border-left:4px solid var(--blue);padding:10px 13px;background:#f5f8fc;border-radius:0 12px 12px 0;margin-top:10px}
.reflection p{margin:0 0 6px;font-size:.92rem}.reflection p:last-child{margin-bottom:0}
table{width:100%;border-collapse:collapse;font-size:.9rem}
th,td{text-align:left;padding:9px 5px;border-bottom:1px solid var(--line)}
th{color:var(--muted);font-weight:600}
td:last-child,th:last-child{text-align:right;font-variant-numeric:tabular-nums}
.note{font-size:.8rem;color:var(--muted)}
footer{text-align:center;color:var(--muted);font-size:.78rem;padding:14px 8px}
@media(min-width:560px){.reaction-grid{grid-template-columns:repeat(3,minmax(0,1fr))}.wrap{padding-top:28px}.panel{padding:22px}}
@media print{body{background:white}.wrap{max-width:none}.panel{box-shadow:none;break-inside:avoid}.actions,.input-panel,header .subtitle{display:none!important}.result{display:block!important}}
</style>
</head>
<body>
<div class="wrap">
<header>
  <div class="kicker">COMMUNICATION CARD GAME</div>
  <h1>リアクト！</h1>
  <p class="subtitle">ゲーム中の反応から、コミュニケーションの傾向を振り返ろう</p>
</header>

<section class="panel input-panel">
  <h2>🎴 反応を入力しよう</h2>
  <p class="intro">ゲーム中に自分が選んだ反応を、それぞれ何回使ったか入力してください。使っていない反応は「0」のままでOKです。</p>
  <div class="reaction-grid" id="reactionGrid">
    <div class="reaction"><label for="count-assert">主張</label><small>自分の意見や考えを伝える</small><div class="stepper"><button type="button" data-change="-1" data-target="count-assert" aria-label="主張を1減らす">−</button><input id="count-assert" type="number" min="0" max="999" value="0" inputmode="numeric"><button type="button" data-change="1" data-target="count-assert" aria-label="主張を1増やす">＋</button></div></div>
    <div class="reaction"><label for="count-question">質問</label><small>相手の考えや理由をたずねる</small><div class="stepper"><button type="button" data-change="-1" data-target="count-question" aria-label="質問を1減らす">−</button><input id="count-question" type="number" min="0" max="999" value="0" inputmode="numeric"><button type="button" data-change="1" data-target="count-question" aria-label="質問を1増やす">＋</button></div></div>
    <div class="reaction"><label for="count-empathy">共感</label><small>気持ちを受け止めたり、理解を示したりする</small><div class="stepper"><button type="button" data-change="-1" data-target="count-empathy" aria-label="共感を1減らす">−</button><input id="count-empathy" type="number" min="0" max="999" value="0" inputmode="numeric"><button type="button" data-change="1" data-target="count-empathy" aria-label="共感を1増やす">＋</button></div></div>
    <div class="reaction"><label for="count-suggest">提案</label><small>解決策や別の方法を提案する</small><div class="stepper"><button type="button" data-change="-1" data-target="count-suggest" aria-label="提案を1減らす">−</button><input id="count-suggest" type="number" min="0" max="999" value="0" inputmode="numeric"><button type="button" data-change="1" data-target="count-suggest" aria-label="提案を1増やす">＋</button></div></div>
    <div class="reaction"><label for="count-disagree">反対</label><small>違う意見や別の見方を伝える</small><div class="stepper"><button type="button" data-change="-1" data-target="count-disagree" aria-label="反対を1減らす">−</button><input id="count-disagree" type="number" min="0" max="999" value="0" inputmode="numeric"><button type="button" data-change="1" data-target="count-disagree" aria-label="反対を1増やす">＋</button></div></div>
    <div class="reaction"><label for="count-hold">保留</label><small>すぐに決めず、いったん考える</small><div class="stepper"><button type="button" data-change="-1" data-target="count-hold" aria-label="保留を1減らす">−</button><input id="count-hold" type="number" min="0" max="999" value="0" inputmode="numeric"><button type="button" data-change="1" data-target="count-hold" aria-label="保留を1増やす">＋</button></div></div>
  </div>
  <div class="actions"><button class="primary" id="diagnose">診断結果を見る</button><button class="secondary" id="reset">リセット</button></div>
  <div class="notice">入力した回数はこのページ内で計算されます。サーバーへの送信や保存は行いません。</div>
  <p id="error" role="alert" style="display:none;color:#a33;font-size:.9rem"></p>
</section>

<section class="result" id="result" aria-live="polite">
  <div class="panel">
    <div class="result-head">
      <span class="pill">YOUR REACTION PROFILE</span>
      <h2 id="mainTitle">あなたの反応スタイル</h2>
      <p id="subTitle"></p>
    </div>
    <h2>① 4タイプの割合</h2>
    <p class="intro">ゲーム中の反応をもとに計算した、傾向を振り返るための目安です。</p>
    <div id="typeBars"></div>
    <div class="dual" style="margin-top:17px">
      <div class="stat"><span>入力した反応の合計</span><strong id="totalCount">0回</strong></div>
      <div class="stat"><span>最も多かった反応</span><strong id="topReaction">—</strong></div>
    </div>
  </div>
  <div class="panel">
    <h2>② あなたのコミュニケーションの特徴</h2>
    <p class="body-copy" id="feature"></p>
    <h3>③ 強みとして活かせそうなこと</h3>
    <p class="body-copy" id="strength"></p>
    <h3>④ 次の会話で試せる工夫</h3>
    <p class="body-copy" id="growth"></p>
  </div>
  <div class="panel">
    <h2>⑤ 反応の内訳</h2>
    <p class="intro">どんな反応を選んだかを、回数と割合で確認できます。</p>
    <table><thead><tr><th>反応</th><th>回数</th><th>割合</th></tr></thead><tbody id="reactionRows"></tbody></table>
    <p class="note">割合は、入力した反応の合計を100%として計算しています。</p>
  </div>
  <div class="panel">
    <h2>⑥ 自分の会話を振り返ろう</h2>
    <div class="reflection" id="reflection"></div>
    <p class="note" style="margin-top:13px">結果は性格を決めつけるものではありません。話題や相手、そのときの気持ちによって反応は変わります。</p>
    <div class="actions"><button class="primary" id="print">結果を印刷・PDF保存</button><button class="secondary" id="edit">回数を修正する</button></div>
  </div>
</section>
<footer>リアクト！｜自分と相手の反応の違いを楽しみながら、コミュニケーションを考えよう</footer>
</div>
<script>
const reactions = [
 {id:"assert",name:"主張",x:2,y:0,desc:"自分の意見や考えを伝える",hint:"自分の考えを言葉にして伝えた場面を振り返ろう。"},
 {id:"question",name:"質問",x:-1,y:0,desc:"相手の考えや理由をたずねる",hint:"相手をもっと知るために、どんな質問ができそう？"},
 {id:"empathy",name:"共感",x:-1,y:2,desc:"気持ちを受け止めたり、理解を示したりする",hint:"共感したとき、相手のどんな言葉や気持ちに注目した？"},
 {id:"suggest",name:"提案",x:1,y:1,desc:"解決策や別の方法を提案する",hint:"提案する前に、相手が何を求めているか確認できそう？"},
 {id:"disagree",name:"反対",x:2,y:-1,desc:"違う意見や別の見方を伝える",hint:"違う意見を伝えるとき、相手への配慮も一緒に表せるかな？"},
 {id:"hold",name:"保留",x:-2,y:-2,desc:"すぐに決めず、いったん考える",hint:"考える時間が必要なとき、相手にどう伝えるとよさそう？"}
];
const types=[
 {key:"driving",name:"ドライビング",color:"c-driving",short:"主張・行動を重視",desc:"目標や結論を意識し、自分の考えをはっきり示す反応が出やすい傾向です。",strength:"話を前に進めたり、決断が必要な場面で自分の考えを示したりすること。",growth:"相手の考えを聞く質問を加えたり、結論を急がず相手のペースも確かめたりしてみましょう。"},
 {key:"expressive",name:"エクスプレッシブ",color:"c-expressive",short:"感情・表現を重視",desc:"気持ちや考えを表現し、会話を活発にする反応が出やすい傾向です。",strength:"自分の思いを伝えたり、会話に勢いやアイデアを生み出したりすること。",growth:"相手の話を最後まで聞いたり、相手がどう感じているか質問したりすることも意識してみましょう。"},
 {key:"amiable",name:"エミアブル",color:"c-amiable",short:"共感・協調を重視",desc:"相手の気持ちや考えを受け止め、協力しながら会話を進める反応が出やすい傾向です。",strength:"相手が話しやすい雰囲気をつくったり、異なる気持ちにも耳を傾けたりすること。",growth:"相手を尊重しながら、「私はこう思う」と自分の意見も伝えてみましょう。"},
 {key:"analytical",name:"アナリティカル",color:"c-analytical",short:"慎重・分析を重視",desc:"すぐに結論を出さず、考えたり、情報を確かめたりする反応が出やすい傾向です。",strength:"状況を落ち着いて考え、理由や別の可能性を整理すること。",growth:"考えがまとまってから話すだけでなく、「今はこう考えている」と途中の考えを伝えてみましょう。"}
];
function countOf(id){return Math.max(0,Math.min(999,Number(document.getElementById("count-"+id).value)||0))}
document.querySelectorAll("[data-change]").forEach(b=>b.addEventListener("click",()=>{const el=document.getElementById(b.dataset.target);el.value=Math.max(0,Math.min(999,(Number(el.value)||0)+Number(b.dataset.change)));}));
document.getElementById("reset").addEventListener("click",()=>{reactions.forEach(r=>document.getElementById("count-"+r.id).value=0);document.getElementById("result").classList.remove("show");document.getElementById("error").style.display="none";window.scrollTo({top:0,behavior:"smooth"});});
document.getElementById("edit").addEventListener("click",()=>{document.querySelector(".input-panel").scrollIntoView({behavior:"smooth"});});
document.getElementById("print").addEventListener("click",()=>window.print());
document.getElementById("diagnose").addEventListener("click",()=>{
 const counts=reactions.map(r=>({...r,count:countOf(r.id)}));
 const total=counts.reduce((s,r)=>s+r.count,0);
 const err=document.getElementById("error");
 if(!total){err.textContent="反応の回数を1回以上入力してください。";err.style.display="block";return;}
 err.style.display="none";
 const X=counts.reduce((s,r)=>s+r.x*r.count,0)/total;
 const Y=counts.reduce((s,r)=>s+r.y*r.count,0)/total;
 const u=Math.max(-1,Math.min(1,X/2)),v=Math.max(-1,Math.min(1,Y/2));
 let values=[
  {key:"driving",pct:(1+u)*(1-v)/4*100},
  {key:"expressive",pct:(1+u)*(1+v)/4*100},
  {key:"amiable",pct:(1-u)*(1+v)/4*100},
  {key:"analytical",pct:(1-u)*(1-v)/4*100}
 ];
 // Round to whole numbers while keeping total at 100.
 const floors=values.map(t=>Math.floor(t.pct));let remain=100-floors.reduce((a,b)=>a+b,0);
 values.map((t,i)=>({i,frac:t.pct-floors[i]})).sort((a,b)=>b.frac-a.frac).slice(0,remain).forEach(o=>floors[o.i]++);
 values=values.map((t,i)=>({...t,pct:floors[i]})).sort((a,b)=>b.pct-a.pct);
 const primary=types.find(t=>t.key===values[0].key),secondary=types.find(t=>t.key===values[1].key);
 document.getElementById("mainTitle").textContent="「"+primary.name+"」傾向";
 document.getElementById("subTitle").textContent="サブ傾向："+secondary.name+"｜"+primary.short;
 document.getElementById("typeBars").innerHTML=values.map(t=>{const info=types.find(q=>q.key===t.key);return `<div class="type-row"><div class="type-meta"><span>${info.name}</span><span class="percent">${t.pct}%</span></div><div class="track"><div class="fill ${info.color}" style="width:${t.pct}%"></div></div><div class="note">${info.short}</div></div>`}).join("");
 document.getElementById("totalCount").textContent=total+"回";
 const max=Math.max(...counts.map(r=>r.count));const tops=counts.filter(r=>r.count===max).map(r=>r.name);
 document.getElementById("topReaction").textContent=tops.join("・");
 const sortedCounts=[...counts].sort((a,b)=>b.count-a.count);
 const lead=sortedCounts[0],least=sortedCounts.filter(r=>r.count===Math.min(...counts.map(c=>c.count))).map(r=>r.name);
 document.getElementById("feature").textContent=`今回のゲームでは「${lead.name}」の反応が最も多く、${primary.desc} 4タイプの割合では${primary.name}が最も高く、${secondary.name}も次に表れています。これは今回のゲームでの反応の傾向であり、普段のあなた全体を決めるものではありません。`;
 document.getElementById("strength").textContent=primary.strength;
 document.getElementById("growth").textContent=primary.growth;
 document.getElementById("reactionRows").innerHTML=counts.map(r=>`<tr><td>${r.name}</td><td>${r.count}回</td><td>${(r.count/total*100).toFixed(1)}%</td></tr>`).join("");
 const questions=[lead.hint,primary.growth,`今回あまり選ばなかった反応（${least.join("・")}）を、次の会話で試すならどんな場面がよさそう？`];
 document.getElementById("reflection").innerHTML=questions.map(q=>`<p>• ${q}</p>`).join("");
 const res=document.getElementById("result");res.classList.add("show");res.scrollIntoView({behavior:"smooth",block:"start"});
});
</script>
</body>
</html>
