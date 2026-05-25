<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>PreJoin — HR Engagement Platform</title>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
:root{
  --bg:#ffffff;--bg2:#f4f8ff;--bg3:#e8f0ff;--bg4:#dbe7ff;
  --sur:#ffffff;--sur2:#f4f8ff;--sur3:#e8f0ff;
  --bdr:rgba(37,99,235,.12);--bdr2:rgba(37,99,235,.2);
  --tx:#0b2545;--tx2:#345080;--tx3:#6b7fa8;
  --ac:#2563eb;--acl:rgba(37,99,235,.12);--ach:#1d4ed8;
  --teal:#0ea5e9;--teall:rgba(14,165,233,.12);
  --grn:#0284c7;--grnl:rgba(2,132,199,.12);
  --amb:#3b82f6;--ambl:rgba(59,130,246,.12);
  --red:#1e40af;--redl:rgba(30,64,175,.12);
  --pur:#1e3a8a;--purl:rgba(30,58,138,.12);
  --pnk:#60a5fa;--pnkl:rgba(96,165,250,.15);
  --r:12px;--rs:8px;--rxs:6px;
  --sh:0 4px 24px rgba(37,99,235,.08);--sh2:0 8px 40px rgba(37,99,235,.12);
}
*{box-sizing:border-box;margin:0;padding:0}
body{font-family:'Inter',sans-serif;background:var(--bg);color:var(--tx);font-size:14px;min-height:100vh}
::-webkit-scrollbar{width:4px;height:4px}
::-webkit-scrollbar-track{background:transparent}
::-webkit-scrollbar-thumb{background:var(--bg4);border-radius:4px}

/* ── SHELL ── */
.shell{display:flex;height:100vh;overflow:hidden}

/* ── SIDEBAR ── */
.side{width:240px;background:var(--bg2);display:flex;flex-direction:column;flex-shrink:0;border-right:1px solid var(--bdr)}
.logo{padding:22px 18px 18px;display:flex;align-items:center;gap:10px;border-bottom:1px solid var(--bdr)}
.logo-icon{width:34px;height:34px;border-radius:10px;background:linear-gradient(135deg,var(--ac),var(--teal));display:flex;align-items:center;justify-content:center;font-size:15px;font-weight:700;color:#fff;flex-shrink:0}
.logo-text .logo-m{font-size:14px;font-weight:700;color:var(--tx);letter-spacing:-.02em}
.logo-text .logo-s{font-size:11px;color:var(--tx3);margin-top:1px}
.side-sec{padding:20px 14px 6px;font-size:10px;font-weight:600;letter-spacing:.1em;text-transform:uppercase;color:var(--tx3)}
.side-nav{flex:1;padding:0 8px;overflow-y:auto}
.ni{display:flex;align-items:center;gap:10px;padding:9px 10px;border-radius:var(--rs);cursor:pointer;font-size:13px;color:var(--tx2);margin-bottom:2px;transition:all .15s;user-select:none;font-weight:500}
.ni:hover{background:var(--sur2);color:var(--tx)}
.ni.on{background:var(--acl);color:var(--ach)}
.ni-ic{width:18px;height:18px;display:flex;align-items:center;justify-content:center;font-size:14px;flex-shrink:0;border-radius:5px}
.ni.on .ni-ic{background:var(--ac);color:#fff;font-size:11px;font-weight:700}
.side-ft{padding:12px 8px;border-top:1px solid var(--bdr)}
.rl-lbl{font-size:10px;text-transform:uppercase;letter-spacing:.1em;color:var(--tx3);padding:4px 6px 8px}
.rsw{display:grid;grid-template-columns:1fr 1fr;gap:4px}
.rb{padding:7px 8px;font-size:11px;color:var(--tx3);cursor:pointer;border:1px solid var(--bdr);background:var(--bg3);font-family:inherit;transition:all .15s;border-radius:var(--rxs);text-align:center;font-weight:500}
.rb:hover{border-color:var(--bdr2);color:var(--tx2);background:var(--sur2)}
.rb.on{background:var(--acl);color:var(--ach);border-color:rgba(99,102,241,.3);font-weight:600}

/* ── MAIN ── */
.main{flex:1;display:flex;flex-direction:column;overflow:hidden}
.tbar{background:var(--bg2);border-bottom:1px solid var(--bdr);padding:0 24px;height:58px;display:flex;align-items:center;justify-content:space-between;flex-shrink:0}
.tbar-t{font-size:16px;font-weight:700;letter-spacing:-.02em;color:var(--tx)}
.tbar-r{display:flex;align-items:center;gap:12px}
.av{width:32px;height:32px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:11px;font-weight:700;flex-shrink:0}
.av-s{width:28px;height:28px;font-size:10px}
.av-lg{width:50px;height:50px;font-size:16px;font-weight:700;border-radius:14px}
.content{flex:1;overflow-y:auto;padding:24px}

/* ── CARDS ── */
.card{background:var(--sur);border:1px solid var(--bdr);border-radius:var(--r);padding:20px;margin-bottom:16px}
.card:last-child{margin-bottom:0}
.card-glow{box-shadow:0 0 0 1px rgba(99,102,241,.2),0 4px 24px rgba(99,102,241,.1)}
.ctit{font-size:14px;font-weight:700;margin-bottom:16px;display:flex;align-items:center;justify-content:space-between;flex-wrap:wrap;gap:8px;color:var(--tx)}
.g2{display:grid;grid-template-columns:1fr 1fr;gap:16px;margin-bottom:16px}
.g3{display:grid;grid-template-columns:1fr 1fr 1fr;gap:16px;margin-bottom:16px}
.g4{display:grid;grid-template-columns:repeat(4,1fr);gap:16px;margin-bottom:16px}
.g5{display:grid;grid-template-columns:repeat(5,1fr);gap:16px;margin-bottom:16px}

/* ── STAT CARDS ── */
.sc{background:var(--sur);border:1px solid var(--bdr);border-radius:var(--r);padding:18px;position:relative;overflow:hidden;transition:all .2s}
.sc:hover{border-color:var(--bdr2);transform:translateY(-1px);box-shadow:var(--sh)}
.sc::before{content:'';position:absolute;top:0;right:0;width:60px;height:60px;border-radius:50%;opacity:.06}
.sc-ac::before{background:var(--ac)}
.sc-teal::before{background:var(--teal)}
.sc-red::before{background:var(--red)}
.sc-amb::before{background:var(--amb)}
.sc-grn::before{background:var(--grn)}
.sc-pur::before{background:var(--pur)}
.sl{font-size:11px;color:var(--tx3);text-transform:uppercase;letter-spacing:.08em;margin-bottom:8px;font-weight:600;display:flex;align-items:center;gap:6px}
.sl-icon{width:18px;height:18px;border-radius:5px;display:flex;align-items:center;justify-content:center;font-size:10px}
.sv{font-size:30px;font-weight:700;font-family:'JetBrains Mono',monospace;line-height:1;color:var(--tx)}
.ss{font-size:11px;color:var(--tx3);margin-top:6px}

/* ── BADGES ── */
.bdg{display:inline-flex;align-items:center;gap:4px;font-size:11px;font-weight:600;padding:3px 9px;border-radius:20px;white-space:nowrap;letter-spacing:.01em}
.b-r{background:var(--redl);color:var(--red)}
.b-a{background:var(--ambl);color:var(--amb)}
.b-g{background:var(--grnl);color:var(--grn)}
.b-b{background:var(--acl);color:var(--ach)}
.b-t{background:var(--teall);color:var(--teal)}
.b-p{background:var(--purl);color:var(--pur)}
.b-pk{background:var(--pnkl);color:var(--pnk)}
.b-n{background:var(--bg4);color:var(--tx2)}
.dot{width:6px;height:6px;border-radius:50%;display:inline-block}
.dr{background:var(--red)}.da{background:var(--amb)}.dg{background:var(--grn)}

/* offer status badges */
.os-acc{background:rgba(16,185,129,.15);color:#34d399;border:1px solid rgba(16,185,129,.2)}
.os-dec{background:rgba(239,68,68,.15);color:#f87171;border:1px solid rgba(239,68,68,.2)}
.os-rev{background:rgba(245,158,11,.15);color:#fbbf24;border:1px solid rgba(245,158,11,.2)}
.os-wait{background:rgba(99,102,241,.15);color:#a5b4fc;border:1px solid rgba(99,102,241,.2)}

/* ── TABLE ── */
.tbl{width:100%;border-collapse:collapse;font-size:13px}
.tbl th{text-align:left;padding:10px 14px;font-size:11px;font-weight:600;color:var(--tx3);text-transform:uppercase;letter-spacing:.08em;border-bottom:1px solid var(--bdr);white-space:nowrap}
.tbl td{padding:12px 14px;border-bottom:1px solid var(--bdr);vertical-align:middle}
.tbl tr:last-child td{border-bottom:none}
.tbl tr:hover td{background:var(--sur2)}
.tbl tbody tr{transition:background .1s}

/* ── BUTTONS ── */
.btn{display:inline-flex;align-items:center;gap:6px;padding:8px 16px;border-radius:var(--rs);font-size:13px;font-weight:600;cursor:pointer;border:none;font-family:inherit;transition:all .15s;white-space:nowrap}
.bp{background:linear-gradient(135deg,var(--ac),#4f46e5);color:#fff;box-shadow:0 2px 12px rgba(99,102,241,.3)}
.bp:hover{box-shadow:0 4px 20px rgba(99,102,241,.5);transform:translateY(-1px)}
.bsm{padding:6px 12px;font-size:12px}
.bxs{padding:3px 8px;font-size:11px}
.bo{background:transparent;border:1px solid var(--bdr2);color:var(--tx2)}
.bo:hover{border-color:var(--ach);color:var(--ach);background:var(--acl)}
.bg2{background:transparent;color:var(--tx2);padding:5px 8px;border:none;border-radius:var(--rxs)}
.bg2:hover{background:var(--sur2);color:var(--tx)}
.bteal{background:linear-gradient(135deg,var(--teal),#0891b2);color:#fff;box-shadow:0 2px 12px rgba(6,182,212,.25)}
.bteal:hover{box-shadow:0 4px 20px rgba(6,182,212,.4)}
.bgrn{background:linear-gradient(135deg,var(--grn),#059669);color:#fff}
.bred{background:transparent;border:1px solid rgba(239,68,68,.3);color:var(--red)}
.bred:hover{background:var(--redl)}

/* ── PROGRESS ── */
.pb{height:5px;background:var(--bg4);border-radius:4px;overflow:hidden}
.pb-lg{height:8px}
.pf{height:100%;border-radius:4px;transition:width .6s ease}
.pg{background:linear-gradient(90deg,var(--grn),#34d399)}
.pa{background:linear-gradient(90deg,var(--amb),#fbbf24)}
.pr{background:linear-gradient(90deg,var(--red),#f87171)}
.pt{background:linear-gradient(90deg,var(--teal),#22d3ee)}
.pac{background:linear-gradient(90deg,var(--ac),var(--ach))}

/* ── FORMS ── */
.fg{margin-bottom:14px}
.fg:last-child{margin-bottom:0}
.fl{font-size:12px;font-weight:600;color:var(--tx2);margin-bottom:6px;display:block;letter-spacing:.01em}
.fi{width:100%;padding:9px 12px;border:1px solid var(--bdr2);border-radius:var(--rs);font-size:13px;font-family:inherit;background:var(--bg3);color:var(--tx);outline:none;transition:all .15s}
.fi:focus{border-color:var(--ac);background:var(--bg4);box-shadow:0 0 0 3px rgba(99,102,241,.1)}
.fi::placeholder{color:var(--tx3)}
textarea.fi{resize:vertical;min-height:80px}
select.fi option{background:var(--bg3)}

/* ── CHECKLIST ── */
.ci{display:flex;align-items:center;gap:10px;padding:10px 0;border-bottom:1px solid var(--bdr);cursor:pointer;transition:all .1s}
.ci:last-child{border-bottom:none}
.ci:hover{padding-left:4px}
.cb{width:18px;height:18px;border-radius:5px;border:2px solid var(--bdr2);display:flex;align-items:center;justify-content:center;flex-shrink:0;font-size:9px;transition:all .15s}
.cb.ck{background:var(--grn);border-color:var(--grn);color:#fff}
.ct{font-size:13px;flex:1;color:var(--tx2)}
.ct.dn{text-decoration:line-through;color:var(--tx3)}

/* ── POSTS ── */
.post{background:var(--sur);border:1px solid var(--bdr);border-radius:var(--r);padding:18px;margin-bottom:12px;transition:all .2s}
.post:hover{border-color:var(--bdr2);box-shadow:var(--sh)}
.ph{display:flex;align-items:center;gap:10px;margin-bottom:12px}
.pm{flex:1}
.pa2{font-size:13px;font-weight:600;color:var(--tx)}
.pdt{font-size:11px;color:var(--tx3);margin-top:2px}
.ptit{font-size:15px;font-weight:700;margin-bottom:8px;color:var(--tx)}
.pbod{font-size:13px;color:var(--tx2);line-height:1.7}
.post-footer{margin-top:12px;padding-top:12px;border-top:1px solid var(--bdr);display:flex;gap:8px}

/* ── MODALS ── */
.ov{display:none;position:fixed;inset:0;background:rgba(0,0,0,.7);backdrop-filter:blur(4px);z-index:100;align-items:center;justify-content:center}
.ov.op{display:flex}
.mod{background:var(--sur);border:1px solid var(--bdr2);border-radius:16px;padding:26px;width:540px;max-width:96vw;max-height:90vh;overflow-y:auto;box-shadow:var(--sh2);animation:modalIn .2s ease}
.mod-lg{width:720px}
.mod-xl{width:860px}
@keyframes modalIn{from{opacity:0;transform:scale(.96) translateY(8px)}to{opacity:1;transform:scale(1) translateY(0)}}
.mt{font-size:16px;font-weight:700;margin-bottom:20px;display:flex;align-items:center;justify-content:space-between;color:var(--tx)}
.mc{cursor:pointer;color:var(--tx3);background:var(--bg4);border:none;width:28px;height:28px;border-radius:8px;display:flex;align-items:center;justify-content:center;font-size:14px;transition:all .15s}
.mc:hover{background:var(--sur3);color:var(--tx)}
.mf{display:flex;gap:10px;justify-content:flex-end;margin-top:22px;padding-top:18px;border-top:1px solid var(--bdr)}
.msec{font-size:11px;font-weight:700;letter-spacing:.1em;text-transform:uppercase;color:var(--tx3);margin:18px 0 10px;padding-bottom:6px;border-bottom:1px solid var(--bdr)}

/* ── TABS ── */
.tabs{display:flex;gap:2px;background:var(--bg3);border-radius:10px;padding:3px;margin-bottom:20px}
.tab{padding:7px 14px;font-size:13px;font-weight:600;cursor:pointer;color:var(--tx3);border-radius:8px;transition:all .15s}
.tab:hover{color:var(--tx2)}
.tab.on{background:var(--ac);color:#fff;box-shadow:0 2px 8px rgba(99,102,241,.3)}
.tab-pane{display:none}
.tab-pane.on{display:block}

/* ── TOAST ── */
.toast{position:fixed;bottom:24px;right:24px;background:var(--sur3);border:1px solid var(--bdr2);color:var(--tx);padding:12px 18px;border-radius:var(--rs);font-size:13px;z-index:300;transform:translateY(60px);opacity:0;transition:all .3s;pointer-events:none;max-width:340px;font-weight:500;box-shadow:var(--sh2)}
.toast.sh{transform:translateY(0);opacity:1}

/* ── WELCOME BANNER ── */
.wb{background:linear-gradient(135deg,#1e1b4b 0%,#312e81 50%,#1e3a5f 100%);border:1px solid rgba(99,102,241,.3);border-radius:var(--r);padding:24px 28px;margin-bottom:16px;position:relative;overflow:hidden}
.wb::before{content:'';position:absolute;right:-40px;top:-40px;width:160px;height:160px;border-radius:50%;background:radial-gradient(circle,rgba(99,102,241,.2),transparent)}
.wb::after{content:'';position:absolute;left:-20px;bottom:-20px;width:100px;height:100px;border-radius:50%;background:radial-gradient(circle,rgba(6,182,212,.15),transparent)}
.wh{font-size:20px;font-weight:800;color:#fff;margin-bottom:6px;letter-spacing:-.02em}
.ws{font-size:13px;color:rgba(255,255,255,.6);line-height:1.5}
.dp{display:inline-flex;align-items:center;gap:6px;background:rgba(99,102,241,.25);color:#a5b4fc;padding:6px 14px;border-radius:20px;font-size:12px;font-weight:600;margin-top:14px;border:1px solid rgba(99,102,241,.3)}

/* ── BUDDY CARD ── */
.bc{display:flex;align-items:center;gap:14px;padding:14px;background:var(--bg3);border-radius:var(--rs);border:1px solid var(--bdr)}
.bn{font-weight:700;font-size:14px;color:var(--tx)}
.br2{font-size:12px;color:var(--tx3);margin-top:2px}
.be{font-size:12px;color:var(--teal);margin-top:6px;font-weight:500}

/* ── KV ROWS ── */
.kv-row{display:flex;justify-content:space-between;align-items:center;padding:9px 0;border-bottom:1px solid var(--bdr)}
.kv-row:last-child{border-bottom:none}
.kv-key{font-size:12px;color:var(--tx3);font-weight:500;min-width:130px}
.kv-val{font-size:13px;font-weight:600;text-align:right;color:var(--tx)}

/* ── ENGAGEMENT PLAN ── */
.ep-card{border:1px solid var(--bdr);border-radius:var(--r);overflow:hidden;margin-bottom:8px;transition:all .15s}
.ep-card:hover{border-color:var(--bdr2)}
.ep-head{padding:12px 16px;display:flex;align-items:center;justify-content:space-between;cursor:pointer;user-select:none;background:var(--sur)}
.ep-head:hover{background:var(--sur2)}
.ep-body{padding:14px 16px;border-top:1px solid var(--bdr);background:var(--bg3);display:none}
.ep-body.open{display:block}
.ep-task{display:flex;align-items:flex-start;gap:10px;padding:8px 0;border-bottom:1px solid var(--bdr);font-size:13px}
.ep-task:last-child{border-bottom:none}
.ep-check{width:17px;height:17px;border-radius:4px;border:2px solid var(--bdr2);flex-shrink:0;display:flex;align-items:center;justify-content:center;font-size:9px;margin-top:1px;cursor:pointer;transition:all .15s}
.ep-check.done{background:var(--grn);border-color:var(--grn);color:#fff}
.ep-task-txt{flex:1;line-height:1.5;color:var(--tx2)}
.ep-task-txt.done{text-decoration:line-through;color:var(--tx3)}

/* email compose area */
.ep-send-btn{display:inline-flex;align-items:center;gap:5px;padding:4px 10px;border-radius:6px;font-size:11px;font-weight:600;cursor:pointer;border:none;font-family:inherit;transition:all .15s;margin-top:8px}
.es-email{background:var(--acl);color:var(--ach);border:1px solid rgba(99,102,241,.3)}
.es-email:hover{background:rgba(99,102,241,.25)}
.es-video{background:var(--teall);color:var(--teal);border:1px solid rgba(6,182,212,.3)}
.es-video:hover{background:rgba(6,182,212,.2)}
.compose-box{background:var(--bg4);border:1px solid var(--bdr2);border-radius:var(--rs);padding:12px;margin-top:10px;display:none}
.compose-box.open{display:block}
.compose-label{font-size:11px;font-weight:700;letter-spacing:.08em;text-transform:uppercase;color:var(--tx3);margin-bottom:8px;display:flex;align-items:center;gap:6px}
.compose-fi{width:100%;padding:7px 10px;border:1px solid var(--bdr2);border-radius:var(--rxs);font-size:12px;font-family:inherit;background:var(--bg3);color:var(--tx);outline:none;margin-bottom:8px;transition:border-color .15s}
.compose-fi:focus{border-color:var(--ac)}
.video-preview{background:var(--sur);border:2px dashed var(--bdr2);border-radius:var(--rs);padding:16px;text-align:center;margin-bottom:8px;cursor:pointer;transition:all .15s}
.video-preview:hover{border-color:var(--teal);background:var(--teall)}
.video-file-input{display:none}

/* ── ALERT ── */
.alr{background:var(--redl);border:1px solid rgba(239,68,68,.2);border-radius:var(--r);padding:14px 18px;margin-bottom:16px;display:flex;align-items:center;gap:12px}
.alr-icon{font-size:20px;flex-shrink:0}
.alr-text .alr-title{font-weight:700;color:var(--red);font-size:13px}
.alr-text .alr-sub{font-size:12px;color:rgba(239,68,68,.7);margin-top:3px}

/* ── DETAIL HEADER ── */
.det-header{display:flex;align-items:center;gap:18px;margin-bottom:22px;padding:18px;background:var(--bg3);border-radius:var(--r);border:1px solid var(--bdr)}
.det-info{flex:1}
.det-name{font-size:20px;font-weight:800;color:var(--tx);letter-spacing:-.02em;margin-bottom:4px}
.det-sub{font-size:13px;color:var(--tx3)}
.det-tags{display:flex;gap:6px;flex-wrap:wrap;margin-top:8px}

/* ── TIMELINE ── */
.etl{position:relative;padding-left:28px}
.etl::before{content:'';position:absolute;left:9px;top:0;bottom:0;width:2px;background:var(--bdr2)}
.etl-item{position:relative;padding-bottom:20px}
.etl-item:last-child{padding-bottom:0}
.etl-dot{position:absolute;left:-28px;top:2px;width:20px;height:20px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:9px;font-weight:700;border:2px solid var(--bg3)}
.ed-done{background:var(--grn);color:#fff}
.ed-next{background:var(--ac);color:#fff}
.ed-pending{background:var(--amb);color:#fff}
.ed-missed{background:var(--red);color:#fff}
.ed-future{background:var(--bg4);color:var(--tx3)}
.etl-title{font-size:13px;font-weight:600;color:var(--tx);margin-bottom:2px}
.etl-sub{font-size:12px;color:var(--tx3)}
.etl-note{font-size:12px;color:var(--grn);margin-top:4px;font-style:italic}

/* ── MISC ── */
.fb{display:flex;justify-content:space-between;align-items:center;flex-wrap:wrap;gap:8px}
.fc{display:flex;align-items:center}
.t2{color:var(--tx2)}.t3{color:var(--tx3)}.tsm{font-size:12px}.fw5{font-weight:500}.fw6{font-weight:600}.fw7{font-weight:700}
.row-sep{display:flex;align-items:center;gap:10px;padding:11px 0;border-bottom:1px solid var(--bdr)}
.row-sep:last-child{border-bottom:none}
.divl{height:1px;background:var(--bdr);margin:16px 0}
.chip{display:inline-flex;align-items:center;gap:4px;font-size:11px;font-weight:600;padding:3px 8px;border-radius:6px;background:var(--bg4);color:var(--tx2)}
.src-chip{background:var(--purl);color:var(--pur);border:1px solid rgba(168,85,247,.2)}
</style>
</head>
<body>
<div class="shell">
  <aside class="side">
    <div class="logo">
      <div class="logo-icon">PJ</div>
      <div class="logo-text"><div class="logo-m">PreJoin</div><div class="logo-s">HR Engagement</div></div>
    </div>
    <div class="side-nav" id="sideNav"></div>
    <div class="side-ft">
      <div class="rl-lbl">Switch Role (Demo)</div>
      <div class="rsw" id="rsw">
        <button class="rb" data-role="hr">HR Admin</button>
        <button class="rb" data-role="recruiter">Recruiter</button>
        <button class="rb" data-role="manager">Manager</button>
        <button class="rb" data-role="joiner">New Joiner</button>
      </div>
    </div>
  </aside>
  <div class="main">
    <div class="tbar">
      <div class="tbar-t" id="tbarT"></div>
      <div class="tbar-r">
        <button class="btn bp bsm" id="addBtn" style="display:none">✦ Add Prospective Employee</button>
        <div class="fc" style="gap:10px">
          <div class="av" id="tbarAv"></div>
          <div><div style="font-size:13px;font-weight:600" id="tbarN"></div><div class="tsm t3" id="tbarR"></div></div>
        </div>
      </div>
    </div>
    <div class="content" id="content"></div>
  </div>
</div>

<!-- ADD/EDIT MODAL -->
<div class="ov" id="mAdd">
  <div class="mod mod-xl">
    <div class="mt"><span id="mAddTitle">Add Prospective Employee</span><button class="mc" data-close="mAdd">✕</button></div>
    <div class="msec">Personal Details</div>
    <div class="g3" style="margin-bottom:0">
      <div class="fg"><label class="fl">Full Name *</label><input class="fi" id="fName" placeholder="e.g. Rahul Verma"></div>
      <div class="fg"><label class="fl">Email *</label><input class="fi" id="fEmail" placeholder="rahul@company.com"></div>
      <div class="fg"><label class="fl">Mobile Number *</label><input class="fi" id="fMobile" placeholder="+91 98765 43210"></div>
    </div>
    <div class="msec">Role & Joining</div>
    <div class="g3" style="margin-bottom:0">
      <div class="fg"><label class="fl">Joining Date *</label><input class="fi" type="date" id="fDate" oninput="calcNoticePeriod()"></div>
      <div class="fg"><label class="fl">Offered Date</label><input class="fi" type="date" id="fOfferedDate" oninput="calcNoticePeriod()"></div>
      <div class="fg"><label class="fl">Offer Acceptance Date</label><input class="fi" type="date" id="fOfferAcceptDate"></div>
    </div>
    <div class="g3" style="margin-bottom:0">
      <div class="fg"><label class="fl">Offer Status</label>
        <select class="fi" id="fOfferStatus" onchange="autoFillAcceptDate()">
          <option value="awaiting">Awaiting Offer Acceptance</option>
          <option value="accepted">Offer Accepted</option>
          <option value="joined">Joined</option>
          <option value="declined">Offer Declined</option>
          <option value="revoked">Offer Revoked</option>
        </select>
      </div>
      <div class="fg"><label class="fl">Notice Period <span style="color:var(--tx3);font-weight:400">(auto-calculated)</span></label><input class="fi" id="fNoticeDisplay" readonly placeholder="Set Offered & Joining dates" style="background:var(--bg3);color:var(--tx2);cursor:default"></div>
      <div class="fg" style="display:flex;flex-direction:column;justify-content:flex-end"><div style="font-size:11px;color:var(--tx3);padding:8px 10px;background:var(--bg3);border:1px solid var(--bdr);border-radius:var(--rs);line-height:1.5">💡 Notice period = difference between Offered Date and Joining Date</div></div>
    </div>
    <div class="g3" style="margin-bottom:0">
      <div class="fg"><label class="fl">Department</label>
        <select class="fi" id="fDept"><option>Engineering</option><option>Product</option><option>Design</option><option>Sales</option><option>HR</option><option>Finance</option><option>Operations</option></select>
      </div>
      <div class="fg"><label class="fl">Designation</label><input class="fi" id="fDesig" placeholder="e.g. Senior Engineer"></div>
      <div class="fg"><label class="fl">Business Unit</label>
        <select class="fi" id="fBU">
          <option value="">— Select Business Unit —</option>
          <option value="Technology">Technology</option>
          <option value="Product & Design">Product &amp; Design</option>
          <option value="Sales & Marketing">Sales &amp; Marketing</option>
          <option value="Corporate">Corporate</option>
          <option value="Operations">Operations</option>
          <option value="Finance & Legal">Finance &amp; Legal</option>
          <option value="Human Resources">Human Resources</option>
        </select>
      </div>
    </div>
    <div class="g3" style="margin-bottom:0">
      <div class="fg"><label class="fl">Work Location</label>
        <select class="fi" id="fWorkLoc">
          <option value="">— Select Location —</option>
          <option value="Hyderabad">Hyderabad</option>
          <option value="Bangalore">Bangalore</option>
          <option value="Mumbai">Mumbai</option>
          <option value="Delhi NCR">Delhi NCR</option>
          <option value="Chennai">Chennai</option>
          <option value="Pune">Pune</option>
          <option value="Remote">Remote</option>
          <option value="Hybrid">Hybrid</option>
        </select>
      </div>
      <div class="fg"><label class="fl">Source</label>
        <select class="fi" id="fSource">
          <option value="LinkedIn">LinkedIn</option>
          <option value="Naukri">Naukri</option>
          <option value="Referral">Referral</option>
          <option value="Campus">Campus Placement</option>
          <option value="Agency">Recruitment Agency</option>
          <option value="Direct">Direct Application</option>
          <option value="Indeed">Indeed</option>
          <option value="Other">Other</option>
        </select>
      </div>
      <div class="fg"></div>
    </div>
    <div class="msec">Assignment</div>
    <div class="g3" style="margin-bottom:0">
      <div class="fg"><label class="fl">Recruiter</label><select class="fi" id="fRec"><option>Priya Mehta</option><option>Karan Shah</option><option>Anita Nair</option></select></div>
      <div class="fg"><label class="fl">Hiring Manager</label><select class="fi" id="fMgr"><option>Raj Kumar</option><option>Sunita Rao</option><option>Dev Patel</option></select></div>
      <div class="fg"><label class="fl">Buddy</label><input class="fi" id="fBuddy" placeholder="Buddy name"></div>
    </div>
    <div class="fg"><label class="fl">Notes / Special Requirements</label><textarea class="fi" id="fNotes" rows="2" placeholder="Any notes, requirements, or relocation details..."></textarea></div>
    <div class="mf">
      <button class="btn bo" data-close="mAdd">Cancel</button>
      <button class="btn bp" id="btnAddSubmit">Save Prospective Employee</button>
    </div>
  </div>
</div>

<!-- VIEW MODAL -->
<div class="ov" id="mView">
  <div class="mod mod-xl">
    <div class="mt"><span id="mViewTitle">Profile</span><button class="mc" data-close="mView">✕</button></div>
    <div id="mViewBody"></div>
    <div class="mf">
      <button class="btn bo" data-close="mView">Close</button>
      <button class="btn bp" id="btnEditFromView">✎ Edit Profile</button>
    </div>
  </div>
</div>


<!-- CANDIDATES LIST MODAL -->
<div class="ov" id="mCands">
  <div class="mod mod-lg">
    <div class="mt"><span id="mCandsTitle">Candidates</span><button class="mc" data-close="mCands">✕</button></div>
    <div id="mCandsBody"></div>
    <div class="mf"><button class="btn bo" data-close="mCands">Close</button></div>
  </div>
</div>

<!-- FOLLOW-UP MODAL -->
<div class="ov" id="mFU">
  <div class="mod">
    <div class="mt">Update Follow-up <button class="mc" data-close="mFU">✕</button></div>
    <div id="fuInfo"></div>
    <div class="fg"><label class="fl">Status</label>
      <select class="fi" id="fuSt"><option value="done">✅ Done</option><option value="pending">⏳ Pending</option><option value="missed">❌ Missed</option></select>
    </div>
    <div class="fg"><label class="fl">Remarks</label><input class="fi" id="fuRem" placeholder="Notes about this follow-up..."></div>
    <div class="mf">
      <button class="btn bo" data-close="mFU">Cancel</button>
      <button class="btn bp" id="btnFUSubmit">Save &amp; Recalculate Risk</button>
    </div>
  </div>
</div>

<!-- POST MODAL -->
<div class="ov" id="mPost">
  <div class="mod">
    <div class="mt">New Engagement Post <button class="mc" data-close="mPost">✕</button></div>
    <div class="fg"><label class="fl">Title</label><input class="fi" id="pTit" placeholder="e.g. Welcome to the Team!"></div>
    <div class="fg"><label class="fl">Audience</label>
      <select class="fi" id="pAud"><option value="all">All Prospective Employees</option><option value="engineering">Engineering only</option><option value="product">Product only</option><option value="sales">Sales only</option></select>
    </div>
    <div class="fg"><label class="fl">Content</label><textarea class="fi" id="pBod" rows="4" placeholder="Write your message..."></textarea></div>
    <div class="mf">
      <button class="btn bo" data-close="mPost">Cancel</button>
      <button class="btn bp" id="btnPostSubmit">📢 Publish Post</button>
    </div>
  </div>
</div>

<!-- EMAIL COMPOSE MODAL -->
<div class="ov" id="mEmail">
  <div class="mod mod-lg">
    <div class="mt"><span id="mEmailTitle">📧 Compose Email</span><button class="mc" data-close="mEmail">✕</button></div>
    <div class="fg"><label class="fl">To</label><input class="fi" id="eTo" readonly style="background:var(--bg4)"></div>
    <div class="fg"><label class="fl">Subject</label><input class="fi" id="eSub" placeholder="e.g. Welcome! Your Joining Details Inside 🎉"></div>
    <div class="fg"><label class="fl">Message</label><textarea class="fi" id="eBody" rows="6" placeholder="Dear [Name],&#10;&#10;We are excited to have you join our team..."></textarea></div>
    <div id="eVideoArea" style="display:none">
      <div class="msec" style="margin-top:0">📎 Attach Video / File</div>
      <div class="video-preview" id="videoDrop">
        <div style="font-size:28px;margin-bottom:8px">🎬</div>
        <div style="font-size:13px;font-weight:600;color:var(--tx2)">Drag &amp; drop video or click to browse</div>
        <div class="tsm t3" style="margin-top:4px">MP4, MOV, AVI up to 50MB · Or paste a YouTube / Loom URL</div>
        <input type="file" class="video-file-input" id="videoFile" accept="video/*">
      </div>
      <div class="fg"><label class="fl">Or paste Video URL (YouTube / Loom)</label><input class="fi" id="eVideoUrl" placeholder="https://loom.com/share/..."></div>
      <div id="videoPreviewBlock" style="display:none;margin-bottom:12px">
        <div style="background:var(--bg4);border-radius:var(--rs);padding:10px 14px;display:flex;align-items:center;gap:10px;border:1px solid var(--bdr2)">
          <span style="font-size:20px">🎬</span>
          <div style="flex:1"><div class="fw6 tsm" id="videoPreviewName">video.mp4</div><div class="tsm t3">Attached</div></div>
          <button class="btn bg2 bxs" data-a="clearVideo">✕ Remove</button>
        </div>
      </div>
    </div>
    <div class="fg">
      <label class="fl">Email Template</label>
      <select class="fi" id="eTpl">
        <option value="">— Choose a template —</option>
        <option value="welcome">Welcome &amp; Offer Congratulations</option>
        <option value="day1">Day 1 Joining Instructions</option>
        <option value="buddy">Meet Your Buddy</option>
        <option value="checklist">Pre-Joining Checklist Reminder</option>
        <option value="culture">Company Culture &amp; Values</option>
        <option value="video">Company Introduction Video</option>
      </select>
    </div>
    <div class="mf">
      <button class="btn bo" data-close="mEmail">Cancel</button>
      <button class="btn bteal bsm" id="btnSendEmail">🚀 Send Email</button>
    </div>
  </div>
</div>

<div class="toast" id="toast"></div>

<script>
!function(){
'use strict';

/* ═══ DATA ═══════════════════════════════════════════════ */
var D = {
  role:'hr', page:'hr-ov', editFU:null, viewingJid:null, editingJid:null,
  emailJid:null, emailHasVideo:false,
  joiners:[],
  fus:[],
  posts:[],
  checklist:[],
  engagementPlans:{},
  sentEmails:[]
};

var EP_TEMPLATE = [
  {key:'offer',phase:'Offer Stage',icon:'📄',desc:'Right after offer acceptance',cls:'b-b',tasks:['Send personalised congratulations email','Share company welcome video / culture deck','Connect on LinkedIn with a warm message','Share pre-joining FAQ document']},
  {key:'d1',phase:'Joining Day',icon:'🎉',desc:'Welcome onboard',cls:'b-pk',tasks:['Send email welcoming the new joiner onboard']},

];

var ROLES = {
  hr:       {title:'HR Admin Dashboard',  user:'Sneha Arora', role:'HR Admin',          av:'SA',bg:'linear-gradient(135deg,#6366f1,#8b5cf6)',tc:'#fff',addBtn:true, nav:[{ic:'⊞',lbl:'Overview',pg:'hr-ov'},{ic:'👥',lbl:'Prospective Employees',pg:'hr-jn'},{ic:'📢',lbl:'Engagement Posts',pg:'hr-po'},{ic:'📊',lbl:'Reports',pg:'hr-rp'}]},
  recruiter:{title:'Recruiter Dashboard', user:'Priya Mehta',  role:'Recruiter',         av:'PM',bg:'linear-gradient(135deg,#2563eb,#0ea5e9)',tc:'#fff',addBtn:true,nav:[{ic:'⊞',lbl:'My Dashboard',pg:'rec-ov'},{ic:'👤',lbl:'My Candidates',pg:'rec-jn'},{ic:'✓',lbl:"Follow-ups",pg:'rec-fu'}]},
  manager:  {title:'Hiring Manager',      user:'Raj Kumar',    role:'Hiring Manager',    av:'RK',bg:'linear-gradient(135deg,#10b981,#06b6d4)',tc:'#fff',addBtn:false,nav:[{ic:'⊞',lbl:'Overview',pg:'mgr-ov'},{ic:'👥',lbl:'Team Pipeline',pg:'mgr-jn'}]},
  joiner:   {title:'My Joining Journey',  user:'Arjun Patel',  role:'New Joiner — Eng',  av:'AP',bg:'linear-gradient(135deg,#8b5cf6,#ec4899)',tc:'#fff',addBtn:false,nav:[{ic:'🏠',lbl:'My Dashboard',pg:'j-ov'},{ic:'✅',lbl:'Checklist',pg:'j-cl'},{ic:'📅',lbl:'Joining Plan',pg:'j-ep'},{ic:'📰',lbl:'Feed',pg:'j-fd'}]},
};

/* ═══ UTILS ══════════════════════════════════════════════ */
function $(id){return document.getElementById(id)}
function offerBdg(s){
  var m={accepted:['os-acc','✅ Offer Accepted'],joined:['os-acc','🎉 Joined'],declined:['os-dec','❌ Offer Declined'],revoked:['os-rev','⚠ Offer Revoked'],awaiting:['os-wait','⏳ Awaiting Acceptance']};
  var d=m[s]||m['awaiting'];
  return '<span class="bdg '+d[0]+'">'+d[1]+'</span>';
}
function rbdg(s){var m={RED:['b-r','dr'],AMBER:['b-a','da'],GREEN:['b-g','dg']};return '<span class="bdg '+m[s][0]+'"><span class="dot '+m[s][1]+'"></span>'+s+'</span>';}
function avEl(av,bg,tc,cls){return '<div class="av '+(cls||'')+'" style="background:'+bg+';color:'+tc+'">'+av+'</div>';}
function scol(s){return s==='done'?'var(--grn)':s==='missed'?'var(--red)':'var(--amb)';}
function toast(msg,type){
  var t=$('toast');
  t.textContent=msg;
  t.style.borderLeftColor=(type==='error')?'var(--red)':(type==='success')?'var(--grn)':'var(--ac)';
  t.style.borderLeft='3px solid '+(type==='error'?'var(--red)':type==='success'?'var(--grn)':'var(--ac)');
  t.classList.add('sh');
  setTimeout(function(){t.classList.remove('sh');},3200);
}
function openM(id){$(id).classList.add('op');}
function closeM(id){$(id).classList.remove('op');}
function recalc(jid){
  var mis=D.fus.filter(function(f){return f.jid===jid&&f.st==='missed';}).length;
  var j=D.joiners.find(function(x){return x.id===jid;});
  if(mis>=2){j.risk='RED';}else if(mis===1){j.risk='AMBER';}else{j.risk='GREEN';}
}
function epProgress(jid){
  var j=D.joiners.find(function(x){return x.id===jid;});
  if(!j)return 0;
  var jd=new Date(j.joiningDate);
  var today=new Date();
  var daysLeft=Math.round((jd-today)/864e5);
  var WINDOW=60;
  if(daysLeft>=WINDOW)return 0;
  if(daysLeft<=0)return 100;
  return Math.round((WINDOW-daysLeft)/WINDOW*100);
}
function epTaskProgress(jid){
  initEP(jid);var plan=D.engagementPlans[jid];
  var tot=0,dn=0;
  getEPTemplate(jid).forEach(function(ph){if(!plan[ph.key])return;plan[ph.key].forEach(function(t){tot++;if(t.done)dn++;});});
  return tot?Math.round((dn/tot)*100):0;
}
/* Build notice-period-aware EP phases for a candidate */
function buildEPTemplate(noticeDays){
  noticeDays = noticeDays || 0;
  var phases = [
    {key:'offer',phase:'Offer Stage',icon:'📄',desc:'Right after offer acceptance',cls:'b-b',
     tasks:['Send personalised congratulations email','Share company welcome video / culture deck','Connect on LinkedIn with a warm message','Share pre-joining FAQ document']}
  ];
  // Dynamically add mid-phases based on notice period
  if(noticeDays >= 90){
    phases.push({key:'t75',phase:'T−75 Days',icon:'🤝',desc:'75 days before joining',cls:'b-p',
      tasks:['Schedule introductory call with recruiter','Share organisational chart and team structure','Send company welcome kit / swag','Introduce buddy via email']});
    phases.push({key:'t45',phase:'T−45 Days',icon:'📞',desc:'45 days before joining',cls:'b-p',
      tasks:['T-45 check-in call — confirm excitement and address concerns','Share first-week schedule and Day-1 plan','Confirm equipment preferences (laptop, desk setup)','Send parking and office access guide']});
    phases.push({key:'t20',phase:'T−20 Days',icon:'📅',desc:'20 days before joining',cls:'b-a',
      tasks:['T-20 check-in call — final questions','Send IT setup instructions and email login details','Confirm health insurance and payroll forms','Share team Slack/WhatsApp group invite']});
  } else if(noticeDays >= 60){
    phases.push({key:'t45',phase:'T−45 Days',icon:'📞',desc:'45 days before joining',cls:'b-p',
      tasks:['Introductory call with recruiter','Share organisational chart and team structure','Send company welcome kit / swag','Introduce buddy via email']});
    phases.push({key:'t20',phase:'T−20 Days',icon:'📅',desc:'20 days before joining',cls:'b-a',
      tasks:['T-20 check-in call — confirm joining and address concerns','Share first-week schedule','Confirm laptop / equipment preferences','Send parking and office access guide']});
  } else if(noticeDays >= 45){
    phases.push({key:'t30',phase:'T−30 Days',icon:'📅',desc:'30 days before joining',cls:'b-a',
      tasks:['Introductory call with recruiter','Share first-week schedule','Confirm laptop / equipment preferences','Introduce buddy via email']});
    phases.push({key:'t15',phase:'T−15 Days',icon:'💬',desc:'15 days before joining',cls:'b-t',
      tasks:['T-15 check-in call — excitement building','Send IT setup instructions and email login details','Confirm health insurance and payroll forms sent','Send Day-1 agenda']});
  } else if(noticeDays >= 30){
    phases.push({key:'t20',phase:'T−20 Days',icon:'📅',desc:'20 days before joining',cls:'b-a',
      tasks:['Introductory call with recruiter','Share first-week schedule and team structure','Introduce buddy via email','Send company culture deck']});
    phases.push({key:'t7',phase:'T−7 Days',icon:'🎯',desc:'7 days before joining',cls:'b-g',
      tasks:['T-7 final call — last-minute questions','Send Day-1 joining instructions (time, floor, dress code)','Confirm buddy availability on Day 1','Share team communication channels']});
  } else if(noticeDays >= 15){
    phases.push({key:'t10',phase:'T−10 Days',icon:'📞',desc:'10 days before joining',cls:'b-a',
      tasks:['Welcome call with recruiter','Share first-week schedule and buddy details','Send IT setup instructions','Confirm Day-1 logistics']});
  } else {
    // Immediate / 0 days — just a prep phase
    phases.push({key:'prep',phase:'Pre-Joining Preparation',icon:'⚡',desc:'Before your start date',cls:'b-a',
      tasks:['Send all onboarding documents immediately','Schedule Day-1 orientation briefing','Confirm workstation and equipment readiness','Share emergency contacts and IT helpdesk details']});
  }
  phases.push({key:'d1',phase:'Joining Day',icon:'🎉',desc:'Welcome onboard',cls:'b-pk',
    tasks:['Send email welcoming the new joiner onboard']});
  return phases;
}

function autoCreateEP(jid){
  var j = D.joiners.find(function(x){return x.id===jid;});
  if(!j) return;
  var tpl = buildEPTemplate(j.noticePeriod||0);
  var plan = {};
  tpl.forEach(function(ph){ plan[ph.key] = ph.tasks.map(function(t){return{txt:t,done:false};}); });
  D.engagementPlans[jid] = plan;
  // Store custom template on the plan object so renderEPCards can use it
  D.engagementPlans[jid].__tpl = tpl;
}

function getEPTemplate(jid){
  var plan = D.engagementPlans[jid];
  if(plan && plan.__tpl) return plan.__tpl;
  return EP_TEMPLATE;
}

function initEP(jid){
  if(D.engagementPlans[jid])return;
  var j=D.joiners.find(function(x){return x.id===jid;});
  if(j && j.offerStatus==='accepted'){
    autoCreateEP(jid);
  } else {
    var plan={};
    EP_TEMPLATE.forEach(function(ph){plan[ph.key]=ph.tasks.map(function(t){return{txt:t,done:false};});});
    D.engagementPlans[jid]=plan;
  }
  // No seed progress — clean slate
}
D.joiners.forEach(function(j){initEP(j.id);});

function daysFromToday(dateStr){
  var d=new Date(dateStr); var t=new Date(); t.setHours(0,0,0,0); d.setHours(0,0,0,0);
  return Math.round((d-t)/864e5);
}
function fmtDate(d){return d.toISOString().slice(0,10);}
function phaseTargetDate(jid,key){
  var j=D.joiners.find(function(x){return x.id===jid;}); if(!j)return null;
  if(key==='offer')return j.offeredDate||null;
  var offsets={t60:60,t30:30,t15:15,t7:7,d1:0};
  if(!(key in offsets))return null;
  var d=new Date(j.joiningDate); d.setDate(d.getDate()-offsets[key]);
  return fmtDate(d);
}
function phaseStatus(jid,key){
  var t=phaseTargetDate(jid,key); if(!t)return 'upcoming';
  var days=daysFromToday(t);
  if(days<-2)return 'past';
  if(days>=-2 && days<=2)return 'current';
  return 'upcoming';
}
/* Recompute follow-up due dates and statuses from joiningDate */
function normalizeFus(){
  D.fus.forEach(function(f){
    var j=D.joiners.find(function(x){return x.id===f.jid;}); if(!j)return;
    var m=f.lbl.match(/T-?(\d+)/i); if(!m)return;
    var n=parseInt(m[1],10);
    var d=new Date(j.joiningDate); d.setDate(d.getDate()-n);
    f.due=fmtDate(d);
    if(f.st!=='done'){
      f.st = daysFromToday(f.due)<0 ? 'missed' : 'pending';
    }
  });
  D.joiners.forEach(function(j){recalc(j.id);});
}
normalizeFus();

var EMAIL_TEMPLATES={
  welcome:{sub:'Welcome to the Team! Your Offer & Joining Details 🎉',body:'Dear {name},\n\nCongratulations on accepting the offer! We are absolutely thrilled to have you joining our {dept} team as {desig}.\n\nYour official joining date is {date}. We will be in touch with more details about your first day.\n\nWarm regards,\nPreJoin HR Team'},
  day1:{sub:'Day 1 Joining Instructions — {date} 📍',body:'Dear {name},\n\nWe are excited for your first day!\n\n📍 Location: HITEC City, Tower B, 5th Floor, Hyderabad\n⏰ Reporting Time: 9:00 AM\n👔 Dress Code: Smart Casual\n\nPlease carry your original ID proof and offer letter.\n\nSee you soon!\nHR Team'},
  buddy:{sub:'Meet Your Buddy at {company}! 👋',body:'Dear {name},\n\nWe are pleased to introduce your buddy who will guide you through your first few weeks.\n\nBuddy: {buddy}\n\nYour buddy will reach out to you soon. Feel free to ask them anything!\n\nBest,\nHR Team'},
  checklist:{sub:'Pre-Joining Checklist — Action Required 📋',body:'Dear {name},\n\nAs your joining date {date} approaches, please complete the following:\n\n✅ Background verification form\n✅ Educational documents\n✅ Equipment preferences\n✅ Health insurance form\n\nPlease complete these at the earliest.\n\nHR Team'},
  culture:{sub:'Discover Our Culture & Values 🌟',body:'Dear {name},\n\nWe want you to feel at home from Day 1. Here is a glimpse of what makes us unique — our values, work culture, and the amazing team you are joining.\n\nWe believe in: Innovation, Collaboration, and People First.\n\nLooking forward to having you onboard!\n\nHR Team'},
  video:{sub:'Must-Watch: Your Company Introduction Video 🎬',body:'Dear {name},\n\nWe have put together a special video just for you! It covers our culture, team, and what to expect in your first week.\n\n🎬 Watch here: [Video Link]\n\nExcited to have you join us!\n\nHR Team'},
};

/* ═══ ENGAGEMENT PLAN CARD RENDERER ═══════════════════════ */
function renderEPCards(jid){
  initEP(jid);
  var plan=D.engagementPlans[jid];
  return getEPTemplate(jid).map(function(ph){
    var tasks=plan[ph.key];
    var dn=tasks.filter(function(t){return t.done;}).length;
    var pct=Math.round((dn/tasks.length)*100);
    var pcls=pct===100?'pg':pct>50?'pa':'pr';
    var chevron='<svg width="14" height="14" viewBox="0 0 14 14" fill="currentColor" style="color:var(--tx3);transition:transform .2s" id="chev-'+jid+'-'+ph.key+'"><path d="M4 5l3 3 3-3"/></svg>';
    var taskRows=tasks.map(function(t,ti){
      var jbase=D.viewingJid||jid;
      return '<div class="ep-task"><div class="ep-check'+(t.done?' done':'')+'" data-a="epck" data-jid="'+jid+'" data-ph="'+ph.key+'" data-ti="'+ti+'">'+(t.done?'✓':'')+'</div><div style="flex:1"><span class="ep-task-txt'+(t.done?' done':'')+'">'+t.txt+'</span><div style="margin-top:4px"><button class="ep-send-btn es-email" data-a="openEmail" data-jid="'+jid+'" data-task="'+t.txt+'">📧 Send Email</button> <button class="ep-send-btn es-video" data-a="openEmailVideo" data-jid="'+jid+'" data-task="'+t.txt+'">🎬 Send with Video</button></div></div></div>';
    }).join('');
    var pTarget=phaseTargetDate(jid,ph.key);
    var pStat=phaseStatus(jid,ph.key);
    var statBdg=pStat==='current'?'<span class="bdg b-a bxs" style="margin-left:6px">● Current</span>':pStat==='past'?'<span class="bdg b-g bxs" style="margin-left:6px">Past</span>':'<span class="bdg b-b bxs" style="margin-left:6px">Upcoming</span>';
    var dateLbl=pTarget?'<div style="font-size:11px;color:var(--ac);font-weight:600;margin-top:2px">📅 '+pTarget+(pStat==='upcoming'?' · in '+daysFromToday(pTarget)+'d':pStat==='past'?' · '+Math.abs(daysFromToday(pTarget))+'d ago':' · today')+'</div>':'';
    var headBorder=pStat==='current'?'border-left:3px solid var(--amb);':'';
    return '<div class="ep-card" style="'+headBorder+'"><div class="ep-head" data-a="epToggle" data-jid="'+jid+'" data-ph="'+ph.key+'"><div style="display:flex;align-items:center;gap:10px"><span style="font-size:18px">'+ph.icon+'</span><div><div style="font-size:13px;font-weight:700;color:var(--tx)">'+ph.phase+statBdg+'</div><div style="font-size:11px;color:var(--tx3)">'+ph.desc+'</div>'+dateLbl+'</div><span class="bdg '+ph.cls+' bxs">'+dn+'/'+tasks.length+'</span></div><div style="display:flex;align-items:center;gap:8px"><div class="pb" style="width:70px"><div class="pf '+pcls+'" style="width:'+pct+'%"></div></div>'+chevron+'</div></div><div class="ep-body" id="epb-'+jid+'-'+ph.key+'">'+taskRows+'</div></div>';
  }).join('');
}

/* ═══ VIEW PANEL ═══════════════════════════════════════════ */
function viewJoinerHtml(jid){
  var j=D.joiners.find(function(x){return x.id===jid;});
  var fus=D.fus.filter(function(f){return f.jid===jid;});
  var ep=epProgress(jid);
  var _np=(j.offeredDate&&j.joiningDate&&new Date(j.joiningDate)>new Date(j.offeredDate))?Math.round((new Date(j.joiningDate)-new Date(j.offeredDate))/864e5):null;
  var kvs=[
    ['Email',j.email],['Mobile',j.mobile],
    ['Department',j.dept],['Designation',j.desig||'—'],
    ['Business Unit',j.businessUnit||'—'],['Work Location',j.workLocation||'—'],
    ['Joining Date',j.joiningDate],['Offered Date',j.offeredDate||'—'],
    ['Offer Acceptance Date',j.offerAcceptDate||'—'],
    ['Notice Period',_np!==null?_np+' Days':'—'],
    ['Source','<span class="chip src-chip">'+j.source+'</span>'],
    ['Recruiter',j.rec],['Hiring Manager',j.mgr],
    ['Buddy',j.buddy+(j.bmail?' · <span style="color:var(--teal)">'+j.bmail+'</span>':'')],
    ['Notes',j.notes||'—'],
  ];
  var kvH=kvs.map(function(kv){return '<div class="kv-row"><span class="kv-key">'+kv[0]+'</span><span class="kv-val">'+kv[1]+'</span></div>';}).join('');
  var fuH=fus.map(function(f){var dc=f.st==='done'?'ed-done':f.st==='missed'?'ed-missed':f.st==='pending'?'ed-pending':'ed-future';return '<div class="etl-item"><div class="etl-dot '+dc+'">'+(f.st==='done'?'✓':f.st==='missed'?'✗':'→')+'</div><div class="etl-title">'+f.lbl+'</div><div class="etl-sub">Due: '+f.due+' · <span style="color:'+scol(f.st)+';font-weight:600">'+f.st.toUpperCase()+'</span></div>'+(f.rem?'<div class="etl-note">"'+f.rem+'"</div>':'')+'</div>';}).join('');
  return '<div class="det-header">'+avEl(j.av,j.bg,j.tc,'av-lg')+'<div class="det-info"><div class="det-name">'+j.name+'</div><div class="det-sub">'+j.desig+' · '+j.dept+'</div><div class="det-tags">'+rbdg(j.risk)+offerBdg(j.offerStatus)+'<span class="chip src-chip">'+j.source+'</span><span class="bdg b-b">'+j.days+'d to join</span></div></div></div>'
    +'<div class="tabs" id="viewTabs"><div class="tab on" data-tab="vt-info">👤 Profile</div><div class="tab" data-tab="vt-fu">📞 Follow-ups</div><div class="tab" data-tab="vt-ep">📅 Engagement Plan</div></div>'
    +'<div class="tab-pane on" id="vt-info">'+kvH+'</div>'
    +'<div class="tab-pane" id="vt-fu"><div class="etl">'+fuH+'</div></div>'
    +'<div class="tab-pane" id="vt-ep"><div class="fb" style="margin-bottom:14px"><span class="tsm t3">Overall onboarding progress</span><span class="fw7" style="color:var(--ach)">'+ep+'%</span></div><div class="pb pb-lg" style="margin-bottom:18px"><div class="pf pac" style="width:'+ep+'%"></div></div>'+renderEPCards(jid)+'</div>';
}

/* ═══ POST CARD ═══════════════════════════════════════════ */
function postCard(p){
  var videoBlock=p.hasVideo&&p.videoUrl?'<div style="margin-top:12px;border-radius:var(--rs);overflow:hidden;aspect-ratio:16/9"><iframe width="100%" height="100%" src="'+p.videoUrl+'" frameborder="0" allowfullscreen style="display:block"></iframe></div>':'';
  return '<div class="post"><div class="ph">'+avEl(p.av,'linear-gradient(135deg,#6366f1,#8b5cf6)','#fff','av-s')+'<div class="pm"><div class="pa2">'+p.author+'</div><div class="pdt">'+p.date+'</div></div><div style="display:flex;gap:6px"><span class="bdg b-b">'+p.tag+'</span>'+(p.hasVideo?'<span class="bdg b-t">🎬 Video</span>':'')+'</div></div><div class="ptit">'+p.title+'</div><div class="pbod">'+p.body+'</div>'+videoBlock+'</div>';
}

/* ═══ PAGES ═══════════════════════════════════════════════ */
function renderPage(pg){
  D.page=pg;
  var map={
    'hr-ov':hrOv,'hr-jn':hrJn,'hr-po':hrPo,'hr-rp':hrRp,
    'rec-ov':recOv,'rec-jn':recJn,'rec-fu':recFu,
    'mgr-ov':mgrOv,'mgr-jn':mgrOv,
    'j-ov':jOv,'j-cl':jCl,'j-ep':jEp,'j-fd':jFd
  };
  $('content').innerHTML=(map[pg]||function(){return '<div class="card">Coming soon.</div>';})();
}

function buildMonthDashboard(){
  var MONTHS=['January','February','March','April','May','June','July','August','September','October','November','December'];
  var curYear=new Date().getFullYear();
  // Build stats per month index (0-11) based on joiningDate year = current year
  var stats=MONTHS.map(function(){return {released:0,accepted:0,notAccepted:0,joined:0,declined:0};});
  D.joiners.forEach(function(j){
    var d=new Date(j.joiningDate);
    if(d.getFullYear()!==curYear)return;
    var mi=d.getMonth();
    stats[mi].released++;
    if(j.offerStatus==='accepted'||j.offerStatus==='joined'){stats[mi].accepted++;}
    else if(j.offerStatus==='awaiting'||j.offerStatus==='revoked'){stats[mi].notAccepted++;}
    else if(j.offerStatus==='declined'){stats[mi].notAccepted++;stats[mi].declined++;}
    if(j.offerStatus==='joined'){stats[mi].joined++;}
  });

  // Table
  var thStyle='padding:10px 14px;text-align:center;color:var(--tx2);font-weight:600;font-size:12px;border-bottom:2px solid var(--bdr);white-space:nowrap;';
  var thStyleL='padding:10px 14px;text-align:left;color:var(--tx2);font-weight:600;font-size:12px;border-bottom:2px solid var(--bdr);';
  var tableRows=MONTHS.map(function(mn,i){
    var s=stats[i];
    var isEmpty=s.released===0&&s.accepted===0&&s.notAccepted===0&&s.joined===0&&s.declined===0;
    var rowBg=isEmpty?'':'background:var(--bg2);';
    var cell=function(v,color){return '<td style="padding:9px 14px;text-align:center;border-bottom:1px solid var(--bdr);font-weight:'+(v?'700':'400')+';color:'+(v?color:'var(--tx3)')+';font-size:13px">'+(v||'—')+'</td>';};
    return '<tr style="'+rowBg+'">'
      +'<td style="padding:9px 14px;font-weight:600;color:var(--tx);border-bottom:1px solid var(--bdr);font-size:13px">'+mn+'</td>'
      +cell(s.released,'var(--ac)')
      +cell(s.accepted,'var(--grn)')
      +cell(s.notAccepted,'var(--amb)')
      +cell(s.joined,'var(--teal)')
      +cell(s.declined,'var(--red)')
      +'</tr>';
  }).join('');

  // SVG grouped bar chart
  var chartW=680,chartH=200,padL=36,padB=28,padT=16,padR=16;
  var plotW=chartW-padL-padR, plotH=chartH-padB-padT;
  var barGroupW=plotW/12;
  var numCols=5, gap=1, barW=(barGroupW-gap*(numCols+1))/numCols;
  barW=Math.max(barW,3);
  var allVals=stats.map(function(s){return Math.max(s.released,s.accepted,s.notAccepted,s.joined,s.declined);});
  var maxVal=Math.max.apply(null,allVals)||1;
  var colors=['#2563eb','#22c55e','#f59e0b','#0ea5e9','#ef4444'];
  var keys=['released','accepted','notAccepted','joined','declined'];
  var bars='';
  stats.forEach(function(s,i){
    var gx=padL+i*barGroupW+gap;
    keys.forEach(function(k,ki){
      var val=s[k];
      var bh=val?(val/maxVal)*plotH:0;
      var bx=gx+ki*(barW+gap);
      var by=padT+plotH-bh;
      if(val>0){
        bars+='<rect x="'+bx.toFixed(1)+'" y="'+by.toFixed(1)+'" width="'+barW.toFixed(1)+'" height="'+bh.toFixed(1)+'" fill="'+colors[ki]+'" rx="2" opacity="0.85"><title>'+MONTHS[i]+' — '+['Offers Released','Offers Accepted','Not Accepted','Joined','Declined'][ki]+': '+val+'</title></rect>';
        if(bh>12)bars+='<text x="'+(bx+barW/2).toFixed(1)+'" y="'+(by-3).toFixed(1)+'" font-size="8" text-anchor="middle" fill="'+colors[ki]+'" font-weight="700">'+val+'</text>';
      }
    });
  });
  // X axis month labels
  var xlabels=MONTHS.map(function(mn,i){
    var cx=(padL+i*barGroupW+barGroupW/2).toFixed(1);
    return '<text x="'+cx+'" y="'+(chartH-6)+'" font-size="9" text-anchor="middle" fill="var(--tx3)">'+mn.slice(0,3)+'</text>';
  }).join('');
  // Y axis gridlines
  var gridlines='';
  for(var gi=0;gi<=4;gi++){
    var gv=Math.round((maxVal/4)*gi);
    var gy=(padT+plotH-(gv/maxVal)*plotH).toFixed(1);
    gridlines+='<line x1="'+padL+'" y1="'+gy+'" x2="'+(chartW-padR)+'" y2="'+gy+'" stroke="var(--bdr)" stroke-width="1"/>';
    gridlines+='<text x="'+(padL-4)+'" y="'+(parseFloat(gy)+3)+'" font-size="9" text-anchor="end" fill="var(--tx3)">'+gv+'</text>';
  }
  var legendLabels=['Offers Released','Offers Accepted','Not Accepted','Joined','Declined'];
  var legend=colors.map(function(c,i){
    var lx=padL+(i*130);
    return '<rect x="'+lx+'" y="4" width="10" height="10" fill="'+c+'" rx="2"/><text x="'+(lx+14)+'" y="13" font-size="10" fill="var(--tx2)" font-weight="500">'+legendLabels[i]+'</text>';
  }).join('');
  var svg='<svg viewBox="0 0 680 '+(chartH+28)+'" xmlns="http://www.w3.org/2000/svg" style="width:100%;max-width:680px;display:block;margin:0 auto">'
    +'<g>'+legend+'</g>'
    +'<g transform="translate(0,20)">'+gridlines+bars+xlabels+'</g>'
    +'</svg>';

  // Donut chart for offer status breakdown
  var total=D.joiners.length;
  var slices=[
    {label:'Accepted',val:D.joiners.filter(function(j){return j.offerStatus==='accepted'||j.offerStatus==='joined';}).length,color:'#22c55e'},
    {label:'Awaiting',val:D.joiners.filter(function(j){return j.offerStatus==='awaiting';}).length,color:'#f59e0b'},
    {label:'Declined',val:D.joiners.filter(function(j){return j.offerStatus==='declined';}).length,color:'#ef4444'},
    {label:'Revoked',val:D.joiners.filter(function(j){return j.offerStatus==='revoked';}).length,color:'#6b7280'},
  ].filter(function(s){return s.val>0;});
  var donutSvg='<svg viewBox="0 0 200 160" xmlns="http://www.w3.org/2000/svg" style="width:100%;max-width:200px;display:block;margin:0 auto">';
  if(total>0){
    var cx=100,cy=82,r=58,ir=36;
    var startAngle=-Math.PI/2;
    slices.forEach(function(s){
      var angle=(s.val/total)*2*Math.PI;
      var endAngle=startAngle+angle;
      var x1=cx+r*Math.cos(startAngle),y1=cy+r*Math.sin(startAngle);
      var x2=cx+r*Math.cos(endAngle),y2=cy+r*Math.sin(endAngle);
      var ix1=cx+ir*Math.cos(startAngle),iy1=cy+ir*Math.sin(startAngle);
      var ix2=cx+ir*Math.cos(endAngle),iy2=cy+ir*Math.sin(endAngle);
      var large=angle>Math.PI?1:0;
      donutSvg+='<path d="M '+ix1.toFixed(2)+' '+iy1.toFixed(2)+' L '+x1.toFixed(2)+' '+y1.toFixed(2)+' A '+r+' '+r+' 0 '+large+' 1 '+x2.toFixed(2)+' '+y2.toFixed(2)+' L '+ix2.toFixed(2)+' '+iy2.toFixed(2)+' A '+ir+' '+ir+' 0 '+large+' 0 '+ix1.toFixed(2)+' '+iy1.toFixed(2)+' Z" fill="'+s.color+'" opacity="0.9"><title>'+s.label+': '+s.val+'</title></path>';
      startAngle=endAngle;
    });
    donutSvg+='<text x="'+cx+'" y="'+(cy-6)+'" font-size="22" font-weight="700" text-anchor="middle" fill="var(--tx)">'+total+'</text>';
    donutSvg+='<text x="'+cx+'" y="'+(cy+12)+'" font-size="10" text-anchor="middle" fill="var(--tx3)">Total</text>';
  } else {
    donutSvg+='<text x="100" y="82" font-size="13" text-anchor="middle" fill="var(--tx3)">No data</text>';
  }
  // Donut legend
  var dl=slices.map(function(s,i){var lx=10+(i%2)*95,ly=140+(i>1?14:0);return '<rect x="'+lx+'" y="'+(ly-8)+'" width="8" height="8" fill="'+s.color+'" rx="1"/><text x="'+(lx+11)+'" y="'+ly+'" font-size="9" fill="var(--tx2)">'+s.label+' ('+s.val+')</text>';}).join('');
  donutSvg+=dl+'</svg>';

  return '<div class="card" style="margin-top:16px">'
    +'<div class="ctit">📅 Month-wise Status Dashboard <span class="tsm t3" style="font-weight:400">('+curYear+')</span></div>'
    +'<div style="overflow-x:auto"><table style="width:100%;border-collapse:collapse;font-size:13px">'
    +'<thead><tr style="background:var(--bg4)">'
    +'<th style="'+thStyleL+'">Month ↓ / Status →</th>'
    +'<th style="'+thStyle+'">Offers Released</th>'
    +'<th style="'+thStyle+'">Offers Accepted</th>'
    +'<th style="'+thStyle+'">Offers Not Accepted</th>'
    +'<th style="'+thStyle+'">Joined</th>'
    +'<th style="'+thStyle+'">Declined</th>'
    +'</tr></thead><tbody>'+tableRows+'</tbody></table></div>'
    +'<div style="margin-top:24px"><div style="font-size:13px;font-weight:700;margin-bottom:12px;color:var(--tx)">📊 Monthly Trends — Bar Chart</div>'+svg+'</div>'
    +'<div style="display:grid;grid-template-columns:200px 1fr;gap:20px;margin-top:20px;align-items:start">'
    +'<div><div style="font-size:13px;font-weight:700;margin-bottom:12px;color:var(--tx)">🍩 Offer Status Mix</div>'+donutSvg+'</div>'
    +'<div><div style="font-size:13px;font-weight:700;margin-bottom:12px;color:var(--tx)">📈 Year Summary</div>'
    +'<div style="display:grid;grid-template-columns:1fr 1fr;gap:10px">'
    +(function(){
      var rel=D.joiners.length;
      var acc=D.joiners.filter(function(j){return j.offerStatus==='accepted'||j.offerStatus==='joined';}).length;
      var joi=D.joiners.filter(function(j){return j.offerStatus==='joined';}).length;
      var dec=D.joiners.filter(function(j){return j.offerStatus==='declined';}).length;
      var awt=D.joiners.filter(function(j){return j.offerStatus==='awaiting';}).length;
      var accR=rel?Math.round((acc/rel)*100):0;
      var cards=[
        ['Offers Released',rel,'var(--ac)','📋'],
        ['Acceptance Rate',accR+'%','var(--grn)','✅'],
        ['Successfully Joined',joi,'var(--teal)','🎉'],
        ['Awaiting Response',awt,'var(--amb)','⏳'],
      ];
      return cards.map(function(c){
        return '<div style="background:var(--bg2);border:1px solid var(--bdr);border-radius:var(--rs);padding:12px 14px">'
          +'<div style="font-size:18px;margin-bottom:4px">'+c[3]+'</div>'
          +'<div style="font-size:11px;color:var(--tx3);text-transform:uppercase;letter-spacing:.06em;font-weight:600;margin-bottom:4px">'+c[0]+'</div>'
          +'<div style="font-size:22px;font-weight:700;font-family:monospace;color:'+c[2]+'">'+c[1]+'</div>'
          +'</div>';
      }).join('');
    })()
    +'</div></div></div>'
    +'</div>';
}

function hrOv(){
  var stats={RED:0,AMBER:0,GREEN:0,accepted:0,awaiting:0,declined:0,revoked:0,joined:0};
  D.joiners.forEach(function(j){stats[j.risk]++;stats[j.offerStatus]=(stats[j.offerStatus]||0)+1;});
  var today=new Date();
  var onboarded=D.joiners.filter(function(j){return j.offerStatus==='joined' || (j.offerStatus==='accepted' && new Date(j.joiningDate)<=today);}).length;

  return '<div class="g5">'
    +'<div class="sc sc-ac" data-a="showCands" data-filter="total" style="cursor:pointer"><div class="sl"><div class="sl-icon" style="background:var(--acl)">👥</div>Total</div><div class="sv">'+D.joiners.length+'</div><div class="ss">Prospective employees</div></div>'
    +'<div class="sc sc-grn" data-a="showCands" data-filter="accepted" style="cursor:pointer"><div class="sl"><div class="sl-icon" style="background:var(--grnl)">✅</div>Accepted</div><div class="sv" style="color:var(--grn)">'+stats.accepted+'</div><div class="ss">Offer accepted</div></div>'
    +'<div class="sc sc-amb" data-a="showCands" data-filter="awaiting" style="cursor:pointer"><div class="sl"><div class="sl-icon" style="background:var(--ambl)">⏳</div>Awaiting Acceptance</div><div class="sv" style="color:var(--amb)">'+stats.awaiting+'</div><div class="ss">Pending response</div></div>'
    +'<div class="sc sc-red" data-a="showCands" data-filter="declined" style="cursor:pointer"><div class="sl"><div class="sl-icon" style="background:var(--redl)">❌</div>Declined</div><div class="sv" style="color:var(--red)">'+(stats.declined||0)+'</div><div class="ss">Offer declined</div></div>'
    +'<div class="sc sc-grn" data-a="showCands" data-filter="onboarded" style="cursor:pointer"><div class="sl"><div class="sl-icon" style="background:var(--grnl)">🎉</div>On-Boarded</div><div class="sv" style="color:var(--grn)">'+onboarded+'</div><div class="ss">Successfully joined</div></div>'
    +'</div>'
    +buildMonthDashboard();
}

function hrJn(){
  if(!D.joiners.length)return '<div class="card"><div class="ctit">Prospective Employees <button class="btn bp bsm" data-a="openAdd">✦ Add New</button></div><div style="padding:40px;text-align:center;color:var(--tx3)">No prospective employees yet. Click <strong>Add New</strong> to get started.</div></div>';
  var rows=D.joiners.map(function(j){
    var fus=D.fus.filter(function(f){return f.jid===j.id;});
    var dn=fus.filter(function(f){return f.st==='done';}).length;
    var pct=Math.round((dn/3)*100);
    var ep=epProgress(j.id);
    return '<tr><td><div style="display:flex;align-items:center;gap:10px">'+avEl(j.av,j.bg,j.tc,'av-s')+'<div><div class="fw6">'+j.name+'</div><div class="tsm t3">'+j.email+'</div><div class="tsm t3">'+j.mobile+'</div></div></div></td>'
      +'<td>'+j.dept+'<div class="tsm t3">'+j.desig+'</div></td>'
      +'<td><div class="fw6 tsm">'+j.joiningDate+'</div><div class="tsm t3">Offered: '+(j.offeredDate||'—')+'</div></td>'
      +'<td><span class="chip src-chip tsm">'+j.source+'</span></td>'
      +'<td>'+offerBdg(j.offerStatus)+'</td>'
      +'<td><div style="display:flex;align-items:center;gap:5px"><div class="pb" style="width:50px"><div class="pf '+(dn===3?'pg':dn>0?'pa':'pr')+'" style="width:'+pct+'%"></div></div><span class="tsm t3">'+dn+'/3</span></div></td>'
      +'<td><div style="display:flex;align-items:center;gap:5px"><div class="pb" style="width:50px"><div class="pf '+(ep>66?'pg':ep>33?'pa':'pr')+'" style="width:'+ep+'%"></div></div><span class="tsm t3">'+ep+'%</span></div></td>'
      +'<td>'+rbdg(j.risk)+'</td>'
      +'<td><div style="display:flex;gap:4px"><button class="btn bg2 bsm" data-a="vj" data-id="'+j.id+'">👁 View</button><button class="btn bo bsm" data-a="editJ" data-id="'+j.id+'">✎ Edit</button><button class="btn bteal bsm" data-a="openEmail" data-jid="'+j.id+'" data-task="">📧</button></div></td>'
      +'</tr>';
  }).join('');
  return '<div class="card"><div class="ctit">Prospective Employees <button class="btn bp bsm" data-a="openAdd">✦ Add New</button></div><div style="overflow-x:auto"><table class="tbl"><thead><tr><th>Name &amp; Contact</th><th>Role</th><th>Dates</th><th>Source</th><th>Offer Status</th><th>Follow-ups</th><th>Eng Plan</th><th>Risk</th><th>Actions</th></tr></thead><tbody>'+rows+'</tbody></table></div></div>';
}

function hrPo(){
  return '<div class="fb" style="margin-bottom:18px"><div style="font-size:16px;font-weight:700">Engagement Posts</div><button class="btn bp" data-a="openPost">📢 New Post</button></div>'+D.posts.map(postCard).join('');
}

function hrRp(){
  var tot=D.fus.length,dn2=D.fus.filter(function(f){return f.st==='done';}).length,pct2=tot?Math.round((dn2/tot)*100):0;
  var src={};D.joiners.forEach(function(j){src[j.source]=(src[j.source]||0)+1;});
  var srcRows=Object.keys(src).map(function(s){return '<div style="display:flex;align-items:center;gap:8px;padding:6px 0;border-bottom:1px solid var(--bdr)"><span class="chip src-chip">'+s+'</span><div class="pb" style="flex:1"><div class="pf pac" style="width:'+Math.round((src[s]/D.joiners.length)*100)+'%"></div></div><span class="fw6 tsm">'+src[s]+'</span></div>';}).join('');
  var statusRows=['accepted','awaiting','declined','revoked'].map(function(s){var c=D.joiners.filter(function(j){return j.offerStatus===s;}).length;return c>0?'<div style="display:flex;align-items:center;gap:10px;padding:8px 0;border-bottom:1px solid var(--bdr)">'+offerBdg(s)+'<div class="pb" style="flex:1"><div class="pf '+(s==='accepted'?'pg':s==='awaiting'?'pa':'pr')+'" style="width:'+Math.round((c/D.joiners.length)*100)+'%"></div></div><span class="fw6 tsm">'+c+'</span></div>':'';}).join('');
  return '<div class="g3">'
    +'<div class="sc sc-grn"><div class="sl">Follow-up Rate</div><div class="sv">'+pct2+'%</div><div class="pb" style="margin-top:10px"><div class="pf pg" style="width:'+pct2+'%"></div></div><div class="ss">'+dn2+' of '+tot+' done</div></div>'
    +'<div class="sc sc-ac"><div class="sl">Avg Engagement</div><div class="sv">'+(function(){if(!D.joiners.length)return 0;var s=0;D.joiners.forEach(function(j){s+=epProgress(j.id);});return Math.round(s/D.joiners.length);})()+'%</div><div class="ss">Plan completion avg</div></div>'
    +'<div class="sc sc-teal"><div class="sl">Emails Sent</div><div class="sv" style="color:var(--teal)">'+D.sentEmails.length+'</div><div class="ss">Total communications</div></div>'
    +'</div><div class="g2">'
    +'<div class="card" style="margin:0"><div class="ctit">Offer Status Breakdown</div>'+statusRows+'</div>'
    +'<div class="card" style="margin:0"><div class="ctit">Source Breakdown</div>'+srcRows+'</div>'
    +'</div><div class="card"><div class="ctit">Per-Candidate Summary</div>'
    +D.joiners.map(function(j){var fus=D.fus.filter(function(f){return f.jid===j.id;});var ep=epProgress(j.id);var cols=fus.map(function(f){return '<div style="flex:1;padding:5px 8px;border-radius:6px;background:'+(f.st==='done'?'var(--grnl)':f.st==='missed'?'var(--redl)':'var(--bg4)')+';border:1px solid '+(f.st==='done'?'rgba(16,185,129,.2)':f.st==='missed'?'rgba(239,68,68,.2)':'var(--bdr)')+';text-align:center"><div style="font-size:10px;font-weight:600;color:'+(f.st==='done'?'var(--grn)':f.st==='missed'?'var(--red)':'var(--tx3)')+'">'+f.lbl+'</div><div style="font-size:9px;color:var(--tx3)">'+f.st.toUpperCase()+'</div></div>';}).join('');
    return '<div style="margin-bottom:14px"><div class="fb" style="margin-bottom:8px"><div style="display:flex;align-items:center;gap:8px">'+avEl(j.av,j.bg,j.tc,'av-s')+'<span class="fw6">'+j.name+'</span>'+offerBdg(j.offerStatus)+rbdg(j.risk)+'</div><span class="tsm t3">Eng: '+ep+'%</span></div><div style="display:flex;gap:6px">'+cols+'</div></div>';}).join('')
    +'</div>';
}

function recOv(){
  var mine=D.joiners.filter(function(j){return j.rec==='Priya Mehta';});
  var myFU=D.fus.filter(function(f){return f.own==='Priya Mehta';});
  var pen=myFU.filter(function(f){return f.st==='pending';}).length;
  var dn2=myFU.filter(function(f){return f.st==='done';}).length;
  var fuPct=myFU.length?Math.round((dn2/myFU.length)*100):0;
  var rows=mine.map(function(j){var fus=D.fus.filter(function(f){return f.jid===j.id;});var mis=fus.filter(function(f){return f.st==='missed';}).length;var np=fus.find(function(f){return f.st==='pending';});var btn=np?'<button class="btn bo bsm" data-a="openFU" data-id="'+np.id+'">Update</button>':'<span class="bdg b-g">✓ Done</span>';return '<div class="row-sep">'+avEl(j.av,j.bg,j.tc,'av-s')+'<div style="flex:1;padding:0 10px"><div class="fw6">'+j.name+' <span class="t3 tsm">'+j.dept+'</span></div><div class="tsm t3">'+j.mobile+' · Joins '+j.joiningDate+'</div>'+(mis>0?'<div class="tsm" style="color:var(--red);margin-top:2px">⚠ '+mis+' missed</div>':'')+'</div>'+offerBdg(j.offerStatus)+rbdg(j.risk)+'<button class="btn bg2 bsm" data-a="vj" data-id="'+j.id+'">View</button>'+btn+'</div>';}).join('');
  return '<div class="g3"><div class="sc sc-ac"><div class="sl">My Candidates</div><div class="sv">'+mine.length+'</div></div><div class="sc sc-amb"><div class="sl">Pending Follow-ups</div><div class="sv" style="color:var(--amb)">'+pen+'</div></div><div class="sc sc-grn"><div class="sl">Completion Rate</div><div class="sv" style="color:var(--grn)">'+fuPct+'%</div></div></div><div class="card"><div class="ctit">My Candidates</div>'+rows+'</div>';
}

function recJn(){
  var mine=D.joiners.filter(function(j){return j.rec==='Priya Mehta';});
  var cards=mine.map(function(j){var fus=D.fus.filter(function(f){return f.jid===j.id;});var cols=fus.map(function(f){return '<div style="flex:1"><div class="tsm fw6" style="color:var(--tx2);margin-bottom:5px">'+f.lbl+'</div><div style="padding:7px 8px;border-radius:var(--rxs);background:'+(f.st==='done'?'var(--grnl)':f.st==='missed'?'var(--redl)':'var(--bg4)')+';border:1px solid '+(f.st==='done'?'rgba(16,185,129,.2)':f.st==='missed'?'rgba(239,68,68,.2)':'var(--bdr)')+'""><div style="font-size:11px;font-weight:700;color:'+scol(f.st)+'">'+f.st.toUpperCase()+'</div><div class="tsm t3">'+f.due+'</div></div><button class="btn bg2 bsm" data-a="openFU" data-id="'+f.id+'" style="margin-top:4px;width:100%;justify-content:center">Edit</button></div>';}).join('');return '<div style="border:1px solid var(--bdr);border-radius:var(--r);padding:16px;margin-bottom:12px;background:var(--sur)"><div style="display:flex;align-items:center;gap:12px;margin-bottom:14px">'+avEl(j.av,j.bg,j.tc,'')+'<div style="flex:1"><div class="fw7" style="font-size:15px">'+j.name+'</div><div class="tsm t3">'+j.email+' · '+j.mobile+'</div></div>'+offerBdg(j.offerStatus)+rbdg(j.risk)+'<button class="btn bg2 bsm" data-a="vj" data-id="'+j.id+'">View</button></div><div style="display:flex;gap:8px">'+cols+'</div></div>';}).join('');
  return '<div class="card"><div class="ctit">My Assigned Candidates</div>'+cards+'</div>';
}

function fuRowH(f){
  var j=D.joiners.find(function(x){return x.id===f.jid;});
  return '<div class="row-sep">'+avEl(j.av,j.bg,j.tc,'av-s')+'<div style="flex:1;padding:0 10px"><div class="fw6 tsm">'+j.name+' — '+f.lbl+'</div><div class="tsm t3">'+j.mobile+' · Due: '+f.due+'</div>'+(f.rem?'<div class="tsm" style="color:var(--grn);margin-top:2px">"'+f.rem+'"</div>':'')+'</div>'+(f.st==='missed'?'<span class="bdg b-r">Missed</span>':'<span class="bdg b-a">Pending</span>')+'<button class="btn bo bsm" data-a="openFU" data-id="'+f.id+'">Update</button></div>';
}

function recFu(){
  var mis=D.fus.filter(function(f){return f.own==='Priya Mehta'&&f.st==='missed';});
  var pen=D.fus.filter(function(f){return f.own==='Priya Mehta'&&f.st==='pending';});
  return (mis.length?'<div class="alr"><div class="alr-icon">⚠️</div><div class="alr-text"><div class="alr-title">'+mis.length+' Missed Follow-up'+(mis.length>1?'s':'')+' Need Immediate Attention</div><div class="alr-sub">Please update status and remarks immediately to prevent drop-offs.</div></div></div>':'')
    +'<div class="card" style="margin-bottom:16px"><div class="ctit" style="color:var(--red)">❌ Missed ('+mis.length+')</div>'+(mis.length?mis.map(fuRowH).join(''):'<p class="tsm t3">No missed follow-ups! 🎉</p>')+'</div>'
    +'<div class="card"><div class="ctit" style="color:var(--amb)">⏳ Pending ('+pen.length+')</div>'+(pen.length?pen.map(fuRowH).join(''):'<p class="tsm t3">All caught up! ✓</p>')+'</div>';
}

function mgrOv(){
  var mine=D.joiners.filter(function(j){return j.mgr==='Raj Kumar';});
  var rows=mine.map(function(j){var ep=epProgress(j.id);return '<div class="row-sep">'+avEl(j.av,j.bg,j.tc,'')+'<div style="flex:1;padding:0 12px"><div class="fw6">'+j.name+'</div><div class="tsm t3">'+j.desig+' · Buddy: '+j.buddy+'</div></div><div style="text-align:right;min-width:90px"><div class="tsm t3">'+j.joiningDate+'</div><div style="font-size:12px;font-weight:600;color:var(--ach);margin-top:2px">'+j.days+' days</div></div><div style="min-width:80px"><div class="pb" style="margin-bottom:3px"><div class="pf '+(ep>66?'pg':ep>33?'pa':'pr')+'" style="width:'+ep+'%"></div></div><div class="tsm t3" style="text-align:center">'+ep+'%</div></div>'+rbdg(j.risk)+'<button class="btn bg2 bsm" data-a="vj" data-id="'+j.id+'">View</button></div>';}).join('');
  return '<div class="g3"><div class="sc sc-ac"><div class="sl">Team Joiners</div><div class="sv">'+mine.length+'</div></div><div class="sc sc-red"><div class="sl">At Risk</div><div class="sv" style="color:var(--red)">'+mine.filter(function(j){return j.risk==='RED';}).length+'</div></div><div class="sc sc-grn"><div class="sl">On Track</div><div class="sv" style="color:var(--grn)">'+mine.filter(function(j){return j.risk==='GREEN';}).length+'</div></div></div><div class="card"><div class="ctit">Team Joining Pipeline</div>'+rows+'</div>';
}

function jOv(){
  var j=D.joiners[0];
  if(!j)return '<div class="card" style="text-align:center;padding:40px;color:var(--tx3)">No candidate data yet.</div>';
  var dn2=D.checklist.filter(function(c){return c.done;}).length;
  var pct2=Math.round((dn2/D.checklist.length)*100);
  var ep=epProgress(j.id);
  var ki=[['Email',j.email],['Mobile',j.mobile],['Recruiter',j.rec],['Manager',j.mgr],['Designation',j.desig],['Department',j.dept],['Buddy',j.buddy+' ('+j.bmail+')'],['Source','<span class="chip src-chip">'+j.source+'</span>']].map(function(kv){return '<div class="kv-row"><span class="kv-key">'+kv[0]+'</span><span class="kv-val">'+kv[1]+'</span></div>';}).join('');
  var up=D.posts.slice(0,3).map(function(p){return '<div style="padding:9px 0;border-bottom:1px solid var(--bdr)"><div class="fw6 tsm">'+p.title+'</div><div class="tsm t3">'+p.date+(p.hasVideo?' · 🎬 Video':'')+'</div></div>';}).join('');
  return '<div class="wb"><div class="wh">Welcome, '+j.name+'! 👋</div><div class="ws">You are joining the '+j.dept+' team as <strong style="color:#a5b4fc">'+j.desig+'</strong>. We are so excited to have you!</div><div class="dp">⏱ '+j.days+' days until your first day — '+j.joiningDate+'</div></div>'
    +'<div class="g3"><div class="sc sc-grn"><div class="sl">Checklist</div><div class="sv">'+pct2+'%</div><div class="pb" style="margin-top:10px"><div class="pf pg" style="width:'+pct2+'%"></div></div><div class="ss">'+dn2+'/'+D.checklist.length+' tasks done</div></div><div class="sc sc-ac"><div class="sl">Joining Plan</div><div class="sv">'+ep+'%</div><div class="pb" style="margin-top:10px"><div class="pf pac" style="width:'+ep+'%"></div></div><div class="ss">Overall onboarding progress</div></div><div class="sc sc-teal"><div class="sl">Days to Join</div><div class="sv" style="color:var(--teal)">'+j.days+'</div><div class="ss">'+j.joiningDate+'</div></div></div>'
    +'<div class="g2"><div class="card" style="margin:0"><div class="ctit">Your Buddy 👯</div><div class="bc"><div class="av" style="background:linear-gradient(135deg,#8b5cf6,#ec4899);color:#fff;width:44px;height:44px;font-size:15px;border-radius:12px">AS</div><div><div class="bn">'+j.buddy+'</div><div class="br2">Senior Engineer · '+j.dept+'</div><div class="be">'+j.bmail+'</div></div></div></div><div class="card" style="margin:0"><div class="ctit">Key Info</div>'+ki+'</div></div>'
    +'<div class="card" style="margin-top:16px"><div class="ctit">Recent Updates 📰</div>'+up+'</div>';
}

function jCl(){
  if(!D.checklist.length)return '<div class="card" style="text-align:center;padding:40px;color:var(--tx3)">No checklist items yet.</div>';
  var dn2=D.checklist.filter(function(c){return c.done;}).length;
  return '<div class="card"><div class="ctit">First-day Checklist <span class="bdg b-g">'+dn2+'/'+D.checklist.length+' done</span></div>'+D.checklist.map(function(c){return '<div class="ci" data-a="ck" data-id="'+c.id+'"><div class="cb'+(c.done?' ck':'')+'">'+( c.done?'✓':'')+'</div><span class="ct'+(c.done?' dn':'')+'">'+c.text+'</span>'+(c.done?'<span class="bdg b-g">Done ✓</span>':'<span class="bdg b-n">Pending</span>')+'</div>';}).join('')+'</div>';
}

function jEp(){
  var j=D.joiners[0];
  if(!j)return '<div class="card" style="text-align:center;padding:40px;color:var(--tx3)">No candidate data yet.</div>';
  var ep=epProgress(j.id);
  return '<div class="card"><div class="ctit">My Pre-Joining Engagement Plan <span class="bdg b-b">'+ep+'% complete</span></div><p class="tsm t3" style="margin-bottom:16px;line-height:1.6">Every milestone below covers your full journey — from offer acceptance all the way to Day 90. Expand each phase and tick off tasks as you go!</p><div class="pb pb-lg" style="margin-bottom:20px"><div class="pf pac" style="width:'+ep+'%"></div></div>'+renderEPCards(j.id)+'</div>';
}

function jFd(){
  return '<div class="fb" style="margin-bottom:18px"><div style="font-size:16px;font-weight:700">Engagement Feed 📰</div><span class="bdg b-b">'+D.posts.length+' updates</span></div>'+D.posts.map(postCard).join('');
}

/* ═══ ROLE SWITCH ════════════════════════════════════════ */
function switchRole(role){
  D.role=role;
  var cfg=ROLES[role];
  $('tbarT').textContent=cfg.title;
  $('tbarN').textContent=cfg.user;
  $('tbarR').textContent=cfg.role;
  var av=$('tbarAv'); av.textContent=cfg.av; av.style.background=cfg.bg; av.style.color=cfg.tc;
  $('addBtn').style.display=cfg.addBtn?'inline-flex':'none';
  document.querySelectorAll('.rb').forEach(function(b){b.classList.toggle('on',b.dataset.role===role);});
  $('sideNav').innerHTML='<div class="side-sec">Navigation</div>'+cfg.nav.map(function(n,i){return '<div class="ni'+(i===0?' on':'')+'" data-pg="'+n.pg+'"><div class="ni-ic">'+n.ic+'</div>'+n.lbl+'</div>';}).join('');
  renderPage(cfg.nav[0].pg);
}

window.autoFillAcceptDate=function(){
  var sel=$('fOfferStatus');
  var acd=$('fOfferAcceptDate');
  if(!sel||!acd)return;
  if(sel.value==='accepted'){
    // Only set today if field is currently empty
    if(!acd.value){
      var t=new Date();
      acd.value=t.getFullYear()+'-'+String(t.getMonth()+1).padStart(2,'0')+'-'+String(t.getDate()).padStart(2,'0');
    }
  } else {
    // Clear the date when status moves away from accepted
    acd.value='';
  }
};

window.calcNoticePeriod=function calcNoticePeriod(){
  var od=$('fOfferedDate')?$('fOfferedDate').value:'';
  var jd=$('fDate')?$('fDate').value:'';
  var el=$('fNoticeDisplay');
  if(!el)return;
  if(od && jd){
    var diff=Math.round((new Date(jd)-new Date(od))/864e5);
    if(diff>0){
      el.value=diff+' Days';
    } else if(diff===0){
      el.value='Same Day';
    } else {
      el.value='⚠ Joining before Offered Date';
      el.style.color='var(--red)';
      return;
    }
    el.style.color='var(--tx2)';
  } else {
    el.value='';
    el.placeholder='Set Offered & Joining dates';
  }
}

function fillAddForm(j){
  $('fName').value=j?j.name:''; $('fEmail').value=j?j.email:''; $('fMobile').value=j?j.mobile:'';
  $('fDate').value=j?j.joiningDate:''; $('fOfferedDate').value=j?j.offeredDate:'';
  $('fOfferAcceptDate').value=j?j.offerAcceptDate||'':'';
  $('fDesig').value=j?j.desig:''; $('fBuddy').value=j?j.buddy:''; $('fNotes').value=j?j.notes:'';
  if($('fWorkLoc'))$('fWorkLoc').value=j&&j.workLocation?j.workLocation:'';
  if($('fBU'))$('fBU').value=j&&j.businessUnit?j.businessUnit:'';
  calcNoticePeriod();
  if(j){
    var depts=['Engineering','Product','Design','Sales','HR','Finance','Operations'];
    $('fDept').selectedIndex=Math.max(0,depts.indexOf(j.dept));
    var sts=['awaiting','accepted','joined','declined','revoked'];
    $('fOfferStatus').selectedIndex=Math.max(0,sts.indexOf(j.offerStatus));
    var srcs=['LinkedIn','Naukri','Referral','Campus','Agency','Direct','Indeed','Other'];
    $('fSource').selectedIndex=Math.max(0,srcs.indexOf(j.source));
    var recs=['Priya Mehta','Karan Shah','Anita Nair'];
    $('fRec').selectedIndex=Math.max(0,recs.indexOf(j.rec));
    var mgrs=['Raj Kumar','Sunita Rao','Dev Patel'];
    $('fMgr').selectedIndex=Math.max(0,mgrs.indexOf(j.mgr));
  }
  calcNoticePeriod();
}

function openEmailModal(jid, task, withVideo){
  var j=D.joiners.find(function(x){return x.id===jid;});
  D.emailJid=jid; D.emailHasVideo=!!withVideo;
  $('mEmailTitle').textContent=withVideo?'🎬 Send Email with Video':'📧 Compose Email';
  $('eTo').value=j.name+' <'+j.email+'>';
  $('eSub').value=task?'Regarding: '+task:'';
  $('eBody').value=task?'Dear '+j.name+',\n\nWe wanted to reach out regarding: '+j.desig+' joining on '+j.joiningDate+'.\n\n[Your message here]\n\nWarm regards,\nHR Team':'';
  $('eVideoArea').style.display=withVideo?'block':'none';
  $('videoPreviewBlock').style.display='none';
  $('eVideoUrl').value='';
  $('eTpl').value='';
  openM('mEmail');
}

function showCandidates(filter){
  var today=new Date();
  var list=D.joiners.filter(function(j){
    if(filter==='total')return true;
    if(filter==='accepted')return j.offerStatus==='accepted';
    if(filter==='awaiting')return j.offerStatus==='awaiting';
    if(filter==='declined')return j.offerStatus==='declined';
    if(filter==='onboarded')return j.offerStatus==='joined' || (j.offerStatus==='accepted' && new Date(j.joiningDate)<=today);
    return false;
  });
  var titles={total:'All Prospective Employees',accepted:'Candidates — Offer Accepted',awaiting:'Candidates — Awaiting Acceptance',declined:'Candidates — Offer Declined',onboarded:'Candidates — On-Boarded'};
  $('mCandsTitle').textContent=titles[filter]+' ('+list.length+')';
  var body=list.length?'<div style="overflow-x:auto"><table class="tbl"><thead><tr><th>Name</th><th>Role</th><th>Joining</th><th>Status</th><th>Contact</th></tr></thead><tbody>'
    +list.map(function(j){return '<tr><td><div style="display:flex;align-items:center;gap:10px">'+avEl(j.av,j.bg,j.tc,'av-s')+'<div><div class="fw6">'+j.name+'</div><div class="tsm t3">'+j.dept+'</div></div></div></td><td>'+j.desig+'</td><td><div class="fw6 tsm">'+j.joiningDate+'</div><div class="tsm t3">'+j.days+'d</div></td><td>'+offerBdg(j.offerStatus)+'</td><td><div class="tsm">'+j.email+'</div><div class="tsm t3">'+j.mobile+'</div></td></tr>';}).join('')
    +'</tbody></table></div>'
    :'<div style="padding:24px;text-align:center;color:var(--tx3)">No candidates found.</div>';
  $('mCandsBody').innerHTML=body;
  openM('mCands');
}

/* ═══ EVENT DELEGATION ════════════════════════════════════ */
document.addEventListener('click',function(e){
  var el=e.target;
  for(var i=0;i<8;i++){
    if(!el||el===document.body)break;
    if(el.dataset){
      if(el.dataset.close){closeM(el.dataset.close);return;}
      if(el.dataset.role){switchRole(el.dataset.role);return;}
      if(el.dataset.pg){
        document.querySelectorAll('.ni').forEach(function(n){n.classList.remove('on');});
        el.classList.add('on');
        renderPage(el.dataset.pg);
        return;
      }
      if(el.dataset.tab){
        var tabId=el.dataset.tab;
        el.closest('.tabs').querySelectorAll('.tab').forEach(function(t){t.classList.remove('on');});
        el.classList.add('on');
        ['vt-info','vt-fu','vt-ep'].forEach(function(tid){var p=$(tid);if(p)p.classList.toggle('on',tid===tabId);});
        return;
      }
      if(el.dataset.a){
        var a=el.dataset.a;
        if(a==='openAdd'){D.editingJid=null;$('mAddTitle').textContent='Add Prospective Employee';$('btnAddSubmit').textContent='Save Prospective Employee';fillAddForm(null);var d=new Date();d.setDate(d.getDate()+30);$('fDate').valueAsDate=d;openM('mAdd');return;}
        if(a==='editJ'){var je=D.joiners.find(function(x){return x.id===el.dataset.id;});D.editingJid=je.id;$('mAddTitle').textContent='Edit — '+je.name;$('btnAddSubmit').textContent='Save Changes';fillAddForm(je);closeM('mView');openM('mAdd');return;}
        if(a==='vj'){
          D.viewingJid=el.dataset.id;
          var jv=D.joiners.find(function(x){return x.id===D.viewingJid;});
          $('mViewTitle').textContent=jv.name+' — Profile';
          $('btnEditFromView').dataset.jid=D.viewingJid;
          $('mViewBody').innerHTML=viewJoinerHtml(D.viewingJid);
          openM('mView');return;
        }
        if(a==='openFU'){var fu=D.fus.find(function(f){return f.id===el.dataset.id;});if(!fu){toast('Not found.','error');return;}var jfu=D.joiners.find(function(x){return x.id===fu.jid;});D.editFU=fu.id;$('fuInfo').innerHTML='<div style="background:var(--bg4);border-radius:var(--rs);padding:10px 14px;margin-bottom:14px;border:1px solid var(--bdr2)"><div class="fw6">'+jfu.name+' — '+fu.lbl+'</div><div class="tsm t3">Due: '+fu.due+'</div></div>';$('fuSt').value=fu.st;$('fuRem').value=fu.rem;openM('mFU');return;}
        if(a==='openPost'){openM('mPost');return;}
        if(a==='ck'){var c=D.checklist.find(function(x){return x.id===el.dataset.id;});c.done=!c.done;renderPage('j-cl');toast(c.done?'✅ Task marked done!':'Task marked pending.');return;}
        if(a==='epToggle'){
          var phk=el.dataset.ph, jidEpT=el.dataset.jid;
          var b=document.getElementById('epb-'+jidEpT+'-'+phk);
          if(b)b.classList.toggle('open');
          return;
        }
        if(a==='epck'){
          var jidEp=el.dataset.jid,phEp=el.dataset.ph,tiEp=parseInt(el.dataset.ti);
          var plan=D.engagementPlans[jidEp];
          if(plan&&plan[phEp])plan[phEp][tiEp].done=!plan[phEp][tiEp].done;
          if($('mView').classList.contains('op')&&D.viewingJid===jidEp){
            $('mViewBody').innerHTML=viewJoinerHtml(jidEp);
            setTimeout(function(){var tb=document.querySelector('[data-tab="vt-ep"]');if(tb)tb.click();var b2=document.getElementById('epb-'+jidEp+'-'+phEp);if(b2)b2.classList.add('open');},10);
          } else renderPage(D.page);
          toast('Task updated! ✓','success');return;
        }
        if(a==='showCands'){showCandidates(el.dataset.filter);return;}
        if(a==='openEmail'){openEmailModal(el.dataset.jid,el.dataset.task,false);return;}
        if(a==='openEmailVideo'){openEmailModal(el.dataset.jid,el.dataset.task,true);return;}
        if(a==='clearVideo'){$('videoPreviewBlock').style.display='none';$('eVideoUrl').value='';$('videoFile').value='';return;}
        return;
      }
    }
    el=el.parentElement;
  }
});

/* ═══ FORM SUBMISSIONS ════════════════════════════════════ */
$('btnAddSubmit').addEventListener('click',function(){
  var name=$('fName').value.trim(),email=$('fEmail').value.trim(),mobile=$('fMobile').value.trim(),date=$('fDate').value;
  if(!name||!email||!mobile||!date){toast('Please fill Name, Email, Mobile and Joining Date.','error');return;}
  if(D.editingJid){
    var j=D.joiners.find(function(x){return x.id===D.editingJid;});
    var prevStatus=j.offerStatus;
    j.name=name;j.email=email;j.mobile=mobile;j.joiningDate=date;j.offeredDate=$('fOfferedDate').value;
    j.offerAcceptDate=$('fOfferAcceptDate').value;
    j.offerStatus=$('fOfferStatus').value;j.dept=$('fDept').value;j.desig=$('fDesig').value;
    j.source=$('fSource').value;j.rec=$('fRec').value;j.mgr=$('fMgr').value;
    j.buddy=$('fBuddy').value||j.buddy;j.notes=$('fNotes').value;
    j.workLocation=$('fWorkLoc').value;j.businessUnit=$('fBU').value;
    var _od=j.offeredDate,_jd=j.joiningDate;
    j.noticePeriod=(_od&&_jd&&new Date(_jd)>new Date(_od))?Math.round((new Date(_jd)-new Date(_od))/864e5):0;
    j.days=Math.max(0,Math.round((new Date(date)-new Date())/864e5));
    j.av=name.split(' ').map(function(w){return w[0];}).join('').toUpperCase().slice(0,2);
    if(j.offerStatus==='accepted' && prevStatus!=='accepted'){
      autoCreateEP(j.id);
      toast(name+' updated! Engagement plan auto-created based on '+j.noticePeriod+'-day notice period ✓','success');
    } else {
      toast(name+' updated successfully! ✓','success');
    }
    closeM('mAdd');D.editingJid=null;renderPage(D.page);
  } else {
    var av=name.split(' ').map(function(w){return w[0];}).join('').toUpperCase().slice(0,2);
    var id='j'+Date.now();
    var jd=new Date(date);
    var gradients=['linear-gradient(135deg,#6366f1,#8b5cf6)','linear-gradient(135deg,#10b981,#06b6d4)','linear-gradient(135deg,#f59e0b,#ef4444)','linear-gradient(135deg,#8b5cf6,#ec4899)'];
    var bg=gradients[D.joiners.length%gradients.length];
    var offeredDateVal=$('fOfferedDate').value;
    var offerAcceptDateVal=$('fOfferAcceptDate').value;
    var noticePeriod=(offeredDateVal&&date&&new Date(date)>new Date(offeredDateVal))?Math.round((new Date(date)-new Date(offeredDateVal))/864e5):0;
    var newOfferStatus=$('fOfferStatus').value;
    D.joiners.push({id:id,name:name,email:email,mobile:mobile,dept:$('fDept').value,desig:$('fDesig').value||'—',joiningDate:date,offeredDate:offeredDateVal,offerAcceptDate:offerAcceptDateVal,noticePeriod:noticePeriod,offerStatus:newOfferStatus,source:$('fSource').value,rec:$('fRec').value,mgr:$('fMgr').value,buddy:$('fBuddy').value||'TBD',bmail:'',notes:$('fNotes').value,workLocation:$('fWorkLoc').value,businessUnit:$('fBU').value,risk:'GREEN',av:av,bg:bg,tc:'#fff',days:Math.max(0,Math.round((jd-new Date())/864e5))});
    [30,15,7].forEach(function(n,i){var d=new Date(jd);d.setDate(d.getDate()-n);D.fus.push({id:'fx'+Date.now()+i,jid:id,own:$('fRec').value,lbl:'T-'+n+' Call',due:d.toISOString().slice(0,10),st:'pending',rem:''});});
    if(newOfferStatus==='accepted'){
      autoCreateEP(id);
      toast(name+' added! Engagement plan auto-created for '+noticePeriod+'-day notice period ✓','success');
    } else {
      initEP(id);
      toast(name+' added! Follow-ups created. Engagement plan will auto-generate when offer is accepted ✓','success');
    }
    closeM('mAdd');
    renderPage('hr-jn');
  }
});

$('btnFUSubmit').addEventListener('click',function(){
  if(!D.editFU)return;
  var fu=D.fus.find(function(f){return f.id===D.editFU;});
  fu.st=$('fuSt').value;fu.rem=$('fuRem').value;
  recalc(fu.jid);closeM('mFU');
  toast('Follow-up updated. Risk recalculated ✓','success');
  renderPage(D.page);
});

$('btnPostSubmit').addEventListener('click',function(){
  var t=$('pTit').value.trim(),b=$('pBod').value.trim();
  if(!t||!b){toast('Please fill all fields.','error');return;}
  var cfg=ROLES[D.role];
  D.posts.unshift({id:'p'+Date.now(),title:t,body:b,author:cfg.user,av:cfg.av,date:new Date().toLocaleDateString('en-IN',{day:'numeric',month:'short',year:'numeric'}),tag:'Update',hasVideo:false});
  closeM('mPost');$('pTit').value='';$('pBod').value='';
  toast('Post published to all candidates! 📢','success');renderPage(D.page.startsWith('hr-po')?'hr-po':D.page);
});

$('btnSendEmail').addEventListener('click',function(){
  var sub=$('eSub').value.trim(),body=$('eBody').value.trim();
  if(!sub||!body){toast('Please fill Subject and Message.','error');return;}
  var j=D.joiners.find(function(x){return x.id===D.emailJid;});
  var hasV=D.emailHasVideo&&($('eVideoUrl').value.trim()||$('videoFile').files.length>0);
  D.sentEmails.push({to:j.email,toName:j.name,sub:sub,date:'Today',hasVideo:hasV});
  closeM('mEmail');
  toast('Email sent to '+j.name+' '+(hasV?'with video 🎬':'📧'),'success');
});

// email template picker
$('eTpl').addEventListener('change',function(){
  var tpl=EMAIL_TEMPLATES[this.value];
  if(!tpl)return;
  var j=D.joiners.find(function(x){return x.id===D.emailJid;})||{};
  function fill(s){return s.replace(/{name}/g,j.name||'').replace(/{dept}/g,j.dept||'').replace(/{desig}/g,j.desig||'').replace(/{date}/g,j.joiningDate||'').replace(/{buddy}/g,j.buddy||'');}
  $('eSub').value=fill(tpl.sub);$('eBody').value=fill(tpl.body);
  if(this.value==='video'){$('eVideoArea').style.display='block';D.emailHasVideo=true;}
});

// video drop zone
$('videoDrop').addEventListener('click',function(){$('videoFile').click();});
$('videoFile').addEventListener('change',function(){
  if(this.files.length>0){
    $('videoPreviewBlock').style.display='block';
    document.getElementById('videoPreviewName').textContent=this.files[0].name;
  }
});
$('eVideoUrl').addEventListener('input',function(){
  if(this.value.trim()){$('videoPreviewBlock').style.display='block';document.getElementById('videoPreviewName').textContent=this.value.trim();}
  else{$('videoPreviewBlock').style.display='none';}
});

$('btnEditFromView').addEventListener('click',function(){
  var jid=this.dataset.jid||D.viewingJid;
  var je=D.joiners.find(function(x){return x.id===jid;});
  if(!je)return;
  D.editingJid=je.id;$('mAddTitle').textContent='Edit — '+je.name;$('btnAddSubmit').textContent='Save Changes';
  fillAddForm(je);closeM('mView');openM('mAdd');
});

$('addBtn').addEventListener('click',function(){
  D.editingJid=null;$('mAddTitle').textContent='Add Prospective Employee';$('btnAddSubmit').textContent='Save Prospective Employee';
  fillAddForm(null);var d=new Date();d.setDate(d.getDate()+30);$('fDate').valueAsDate=d;openM('mAdd');
});

document.querySelectorAll('.ov').forEach(function(o){o.addEventListener('click',function(e){if(e.target===o)o.classList.remove('op');});});

switchRole('hr');
}();
</script>
</body>
</html>
