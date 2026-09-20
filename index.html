<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Stocks Boutique (version autonome)</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@500;600;700&family=IBM+Plex+Sans:wght@400;500;600&family=IBM+Plex+Mono:wght@500;600&display=swap" rel="stylesheet">
<style>
  :root{
    box-sizing:border-box;
    --bg:#171310; --surface:#211b16; --surface-2:#2b241c; --border:#3a3025;
    --text:#f5efe5; --muted:#b3a596; --muted-2:#7d6f61;
    --accent:#ff6a2b; --accent-2:#ffb648; --accent-ink:#2b0f02;
    --ok:#4ecb8a; --warn:#ffb648; --crit:#ef4a4a; --crit-bg:#301613;
    --shadow: 0 8px 24px -12px rgba(0,0,0,0.55);
    --font-head:'Space Grotesk', system-ui, sans-serif;
    --font-body:'IBM Plex Sans', system-ui, sans-serif;
    --font-mono:'IBM Plex Mono', ui-monospace, monospace;
    padding-top:env(safe-area-inset-top,0px);
    padding-bottom:env(safe-area-inset-bottom,0px);
  }
  *,*::before,*::after{box-sizing:inherit}
  html{scroll-padding-top:env(safe-area-inset-top,0px); height:100%;}
  body{
    height:100%; margin:0; background:var(--bg); color:var(--text);
    font-family:var(--font-body); -webkit-font-smoothing:antialiased;
    display:flex; flex-direction:column;
    background-image: radial-gradient(circle at 15% 0%, rgba(255,106,43,0.10), transparent 45%);
  }
  ::selection{background:var(--accent); color:var(--accent-ink)}

  header{
    position:sticky; top:0; z-index:20;
    background:linear-gradient(180deg, #1c1712 0%, var(--bg) 100%);
    border-bottom:1px solid var(--border);
    padding:14px 16px calc(10px + env(safe-area-inset-top,0px)) 16px;
    padding-top:calc(14px + env(safe-area-inset-top,0px));
  }
  .brand{display:flex; align-items:center; justify-content:space-between; gap:8px}
  .brand-left{display:flex; align-items:center; gap:9px}
  .brand-mark{
    width:30px; height:30px; border-radius:8px; flex:0 0 auto;
    background:linear-gradient(135deg, var(--accent), var(--accent-2));
    display:flex; align-items:center; justify-content:center; font-size:16px;
    box-shadow:0 4px 10px -3px rgba(255,106,43,0.55);
  }
  .brand h1{
    font-family:var(--font-head); font-size:18px; font-weight:700; margin:0;
    letter-spacing:0.2px; line-height:1.1;
  }
  .brand .sub{font-size:10.5px; color:var(--muted-2); font-weight:500; letter-spacing:0.3px}
  .brand .tag{font-family:var(--font-mono); font-size:10.5px; color:var(--muted-2); display:flex; align-items:center}
  .sector-scroll{
    display:flex; gap:7px; overflow-x:auto; margin-top:13px; padding-bottom:2px;
    scrollbar-width:none;
  }
  .sector-scroll::-webkit-scrollbar{display:none}
  .chip{
    flex:0 0 auto; font-size:12.5px; font-weight:500; padding:7px 13px;
    border-radius:100px; border:1px solid var(--border); background:var(--surface);
    color:var(--muted); white-space:nowrap; cursor:pointer;
    display:flex; align-items:center; gap:5px; transition:background .15s, color .15s, border-color .15s;
  }
  .chip.active{background:var(--accent); color:var(--accent-ink); border-color:var(--accent); font-weight:600}

  main{flex:1; overflow-y:auto; padding:16px; padding-bottom:100px; max-width:640px; width:100%; margin:0 auto;}
  .view{display:none} .view.active{display:block; animation:fadeIn .18s ease}
  @keyframes fadeIn{ from{opacity:0; transform:translateY(4px)} to{opacity:1; transform:none} }

  .card{
    background:var(--surface); border:1px solid var(--border); border-radius:16px;
    padding:16px; margin-bottom:14px; box-shadow:var(--shadow);
  }
  h2.section-title{
    font-family:var(--font-head); font-size:14px; font-weight:600; margin:0 0 10px 0;
    color:var(--muted); text-transform:none;
  }

  /* Scanner view */
  .scan-cta{
    width:100%; padding:17px; border-radius:16px; border:1px solid var(--border);
    background:linear-gradient(135deg, var(--surface-2), var(--surface)); color:var(--text); font-family:var(--font-head);
    font-size:15.5px; font-weight:600; display:flex; align-items:center; justify-content:center;
    gap:10px; cursor:pointer; box-shadow:var(--shadow); transition:transform .1s;
  }
  .scan-cta:active{transform:scale(0.98)}
  #reader{
    width:100%; border-radius:14px; overflow:hidden; margin-top:12px; background:#000;
    display:none; border:1px solid var(--border);
  }
  #reader.active{display:block}
  .manual-row{display:flex; gap:8px; margin-top:12px}
  input[type=text], input[type=number], input[type=password], select, textarea{
    background:var(--bg); border:1px solid var(--border); color:var(--text);
    border-radius:11px; padding:11px 12px; font-size:15px; font-family:var(--font-body);
    width:100%;
  }
  input[type=text]:focus, input[type=number]:focus, input[type=password]:focus, select:focus, textarea:focus{
    outline:none; border-color:var(--accent); box-shadow:0 0 0 3px rgba(255,106,43,0.15);
  }
  .manual-row input{flex:1}
  .btn{
    border:none; border-radius:11px; padding:12px 16px; font-size:14.5px; font-weight:600;
    cursor:pointer; font-family:var(--font-body); transition:transform .08s, filter .15s;
  }
  .btn:active{transform:scale(0.97)}
  .btn-accent{background:linear-gradient(135deg, var(--accent), var(--accent-2)); color:var(--accent-ink); box-shadow:0 6px 16px -6px rgba(255,106,43,0.5)}
  .btn-ghost{background:var(--surface-2); color:var(--text); border:1px solid var(--border)}
  .btn-danger{background:transparent; color:var(--crit); border:1px solid rgba(239,74,74,0.5)}
  .btn:disabled{opacity:0.45; cursor:default}

  .product-hit{margin-top:16px}
  .product-hit .name{font-family:var(--font-head); font-size:19px; font-weight:700; margin:0}
  .product-hit .meta{font-family:var(--font-mono); font-size:11.5px; color:var(--muted); margin-top:4px}
  .stock-row{
    display:flex; align-items:center; justify-content:space-between; margin-top:14px;
    background:var(--surface-2); border:1px solid var(--border); border-radius:14px; padding:14px 16px;
  }
  .stock-num{font-family:var(--font-head); font-size:30px; font-weight:700; line-height:1}
  .stock-sub{font-size:11.5px; color:var(--muted); margin-top:2px}
  .stepper{display:flex; align-items:center; gap:10px}
  .step-btn{
    width:44px; height:44px; border-radius:11px; border:1px solid var(--border);
    background:var(--bg); color:var(--text); font-size:19px; font-weight:700; cursor:pointer;
  }
  .step-btn:active{background:var(--surface)}
  .actions-row{display:flex; gap:8px; margin-top:12px}
  .actions-row .btn{flex:1}
  .preview-line{text-align:center; font-size:11.5px; color:var(--muted); margin-top:5px; font-family:var(--font-mono)}
  .empty-hint{color:var(--muted); font-size:13.5px; line-height:1.5}
  .not-found{
    margin-top:16px; padding:16px; border-radius:14px; border:1px dashed var(--border);
    color:var(--muted); font-size:13.5px; background:var(--surface);
  }
  .log-item{
    display:flex; align-items:center; gap:10px; padding:9px 0;
    border-bottom:1px solid var(--border); font-size:13px;
  }
  .log-item:last-child{border-bottom:none}
  .l-icon{
    flex:0 0 auto; width:26px; height:26px; border-radius:8px; display:flex; align-items:center;
    justify-content:center; font-size:13px; font-weight:700;
  }
  .l-icon-out{background:rgba(239,74,74,0.14); color:var(--crit)}
  .l-icon-in{background:rgba(78,203,138,0.14); color:var(--ok)}
  .l-info{flex:1; min-width:0}
  .l-info .l-name{font-size:13px; font-weight:500; white-space:nowrap; overflow:hidden; text-overflow:ellipsis}
  .l-info .l-meta{color:var(--muted-2); font-family:var(--font-mono); font-size:10.5px; margin-top:1px}
  .l-pill{
    flex:0 0 auto; font-family:var(--font-mono); font-size:12px; font-weight:700;
    padding:4px 9px; border-radius:8px; min-width:34px; text-align:center;
  }
  .l-pill-out{background:rgba(239,74,74,0.12); color:var(--crit)}
  .l-pill-in{background:rgba(78,203,138,0.12); color:var(--ok)}
  .day-counter{
    flex:1; border-radius:12px; padding:10px 12px; border:1px solid var(--border); background:var(--surface-2);
  }
  .day-counter .dc-num{font-family:var(--font-head); font-size:22px; font-weight:700; line-height:1}
  .day-counter .dc-label{font-size:10.5px; color:var(--muted); margin-top:3px}

  /* Dashboard */
  .order-banner{
    border:1px solid rgba(239,74,74,0.4); background:var(--crit-bg); border-radius:16px;
    padding:15px 16px; margin-bottom:16px; box-shadow:var(--shadow);
  }
  .order-banner h3{
    font-family:var(--font-head); color:#ff8a7a; font-size:15px; margin:0 0 9px 0;
    display:flex; align-items:center; gap:7px;
  }
  .order-line{
    display:flex; justify-content:space-between; font-size:13.5px; padding:6px 0;
    border-bottom:1px solid rgba(239,74,74,0.2);
  }
  .order-line:last-of-type{border-bottom:none}
  .order-line .sku{font-family:var(--font-mono); font-size:11.5px; color:var(--muted)}
  .copy-btn{margin-top:10px; width:100%}
  .resp-row{display:flex; gap:8px; margin-top:12px}
  .resp-row select{flex:1}
  .btn-whatsapp{background:#25D366; color:#06210f; white-space:nowrap; box-shadow:0 6px 16px -6px rgba(37,211,102,0.5)}
  .sector-group{margin-bottom:20px}
  .sector-group h3{
    font-family:var(--font-head); font-size:13.5px; font-weight:600; color:var(--muted);
    margin:0 0 9px 2px; display:flex; justify-content:space-between; align-items:center;
    padding-bottom:6px; border-bottom:1px solid var(--border);
  }
  .prod-row{
    display:flex; align-items:center; justify-content:space-between; gap:10px;
    background:var(--surface); border:1px solid var(--border); border-radius:13px;
    padding:12px 14px; margin-bottom:7px; transition:border-color .15s;
  }
  .prod-row .p-left{min-width:0}
  .prod-row .p-name{font-size:14px; font-weight:500; white-space:nowrap; overflow:hidden; text-overflow:ellipsis}
  .prod-row .p-sku{font-family:var(--font-mono); font-size:10.5px; color:var(--muted-2); margin-top:2px}
  .badge{
    flex:0 0 auto; font-family:var(--font-mono); font-size:12px; font-weight:700;
    padding:6px 10px; border-radius:9px; min-width:36px; text-align:center;
  }
  .badge-ok{background:rgba(78,203,138,0.14); color:var(--ok)}
  .badge-warn{background:rgba(255,182,72,0.16); color:var(--warn)}
  .badge-crit{background:rgba(239,74,74,0.16); color:var(--crit)}

  /* Produits (management) */
  .form-grid{display:grid; grid-template-columns:1fr 1fr; gap:10px}
  .form-grid .full{grid-column:1/-1}
  label{font-size:12px; color:var(--muted); display:block; margin-bottom:5px; font-weight:500}
  .plist-row{
    display:flex; align-items:center; gap:10px; padding:12px 0; border-bottom:1px solid var(--border);
  }
  .plist-row:last-child{border-bottom:none}
  .plist-row .p-info{flex:1; min-width:0}
  .plist-row .p-name{font-size:14px; font-weight:500}
  .plist-row .p-meta{font-size:11.5px; color:var(--muted); font-family:var(--font-mono); margin-top:2px}
  .icon-btn{
    width:36px; height:36px; border-radius:10px; border:1px solid var(--border);
    background:var(--surface-2); color:var(--muted); font-size:15px; cursor:pointer;
  }

  nav.tabbar{
    position:fixed; left:0; right:0; bottom:0; z-index:30;
    background:rgba(33,27,22,0.92); backdrop-filter:blur(10px); border-top:1px solid var(--border);
    padding-bottom:env(safe-area-inset-bottom,0px);
    display:flex; max-width:640px; margin:0 auto; width:100%;
  }
  nav.tabbar .tab{
    flex:1; background:none; border:none; color:var(--muted); font-family:var(--font-body);
    font-size:11.5px; padding:11px 4px 12px; display:flex; flex-direction:column; align-items:center;
    gap:4px; cursor:pointer; position:relative;
  }
  nav.tabbar .tab .ic{font-size:20px}
  nav.tabbar .tab.active{color:var(--accent); font-weight:600}
  nav.tabbar .tab.active::before{
    content:''; position:absolute; top:0; left:50%; transform:translateX(-50%);
    width:26px; height:3px; border-radius:0 0 4px 4px; background:var(--accent);
  }
  @media (max-width:380px){ nav.tabbar{max-width:100%} }
  .status-dot{width:7px; height:7px; border-radius:50%; display:inline-block; margin-right:5px}
  .toast{
    position:fixed; left:50%; transform:translateX(-50%); bottom:calc(80px + env(safe-area-inset-bottom,0px));
    background:var(--surface-2); border:1px solid var(--border); color:var(--text);
    padding:11px 18px; border-radius:12px; font-size:13px; z-index:50; opacity:0; pointer-events:none;
    transition:opacity .2s, transform .2s; box-shadow:var(--shadow);
  }
  .toast.show{opacity:1}
  ::-webkit-scrollbar{width:8px} ::-webkit-scrollbar-thumb{background:var(--border); border-radius:8px}

  /* Profil collègue */
  .profile-bubble{
    width:32px; height:32px; border-radius:50%; background:var(--surface-2); border:1px solid var(--border);
    color:var(--accent-2); font-family:var(--font-head); font-weight:700; font-size:13px;
    display:flex; align-items:center; justify-content:center; cursor:pointer; flex:0 0 auto;
  }
  .header-right{display:flex; align-items:center; gap:10px}
  .id-overlay{
    position:fixed; inset:0; z-index:60; background:rgba(10,8,6,0.75); backdrop-filter:blur(4px);
    display:flex; align-items:center; justify-content:center; padding:24px;
  }
  .id-card{
    background:var(--surface); border:1px solid var(--border); border-radius:18px; padding:24px;
    max-width:340px; width:100%; box-shadow:var(--shadow); text-align:center;
  }
  .id-card .id-emoji{font-size:34px; margin-bottom:6px}
  .id-card h2{font-family:var(--font-head); font-size:18px; margin:0 0 4px 0}
  .id-card p{color:var(--muted); font-size:13px; margin:0 0 16px 0; line-height:1.5}
  .id-card input{margin-bottom:12px; text-align:center; font-size:16px}
</style>
</head>
<body>

<div class="id-overlay" id="pinOverlay" style="display:none">
  <div class="id-card">
    <div class="id-emoji">🔒</div>
    <h2>Accès protégé</h2>
    <p>Entre le code de l'équipe pour ouvrir l'appli de gestion des stocks.</p>
    <input type="password" id="pinInput" placeholder="Code d'accès" inputmode="numeric" autocomplete="off">
    <button class="btn btn-accent" id="pinConfirmBtn" style="width:100%">Déverrouiller</button>
  </div>
</div>

<div class="id-overlay" id="idOverlay" style="display:none">
  <div class="id-card">
    <div class="id-emoji">👋</div>
    <h2>C'est qui ?</h2>
    <p>Ton prénom s'affichera à côté de chaque sortie ou entrée que tu enregistres — pratique pour s'y retrouver à plusieurs.</p>
    <input type="text" id="idNameInput" placeholder="Ton prénom" autocomplete="off">
    <button class="btn btn-accent" id="idConfirmBtn" style="width:100%">C'est parti</button>
  </div>
</div>

<header>
  <div class="brand">
    <div class="brand-left">
      <div class="brand-mark">📦</div>
      <div>
        <h1>Stocks Boutique</h1>
        <div class="sub">Suivi des stocks en temps réel · v3</div>
      </div>
    </div>
    <span class="header-right">
      <span class="tag" id="conn-tag" title="Taper pour voir l'adresse configurée">…</span>
      <span class="profile-bubble" id="profileBubble" title="Changer de profil">?</span>
    </span>
  </div>
  <div class="sector-scroll" id="sectorScroll"></div>
</header>

<main>

  <!-- SCANNER VIEW -->
  <section class="view active" id="view-scan">
    <button class="scan-cta" id="btnCamera">📷 Scanner un code-barre</button>
    <div id="reader"></div>
    <div class="manual-row">
      <input type="text" id="manualCode" placeholder="Ou saisir la référence / SKU" inputmode="text">
      <button class="btn btn-accent" id="btnLookup">OK</button>
    </div>

    <div id="hitZone"></div>

    <div class="card" style="margin-top:18px">
      <h2 class="section-title" id="logTitle">Dernières sorties / entrées</h2>
      <div id="dayCounters" style="display:flex; gap:10px; margin-bottom:14px"></div>
      <div id="logList"><p class="empty-hint">Aucun mouvement pour l'instant.</p></div>
    </div>
  </section>

  <!-- DASHBOARD VIEW -->
  <section class="view" id="view-dash">
    <div id="orderBanner"></div>
    <div id="dashList"></div>
  </section>

  <!-- PRODUITS VIEW -->
  <section class="view" id="view-prod">
    <div class="card">
      <h2 class="section-title" id="formTitle">Ajouter un produit</h2>
      <div class="form-grid">
        <div class="full">
          <label>Nom de l'article</label>
          <input type="text" id="f-nom" placeholder="Ex. Coque MagSafe iPhone 16">
        </div>
        <div class="full">
          <label>Référence / code-barre (SKU)</label>
          <input type="text" id="f-sku" placeholder="Ex. 3700123456789">
        </div>
        <div class="full">
          <label>Secteur</label>
          <select id="f-secteur"></select>
        </div>
        <div class="full">
          <label>Famille</label>
          <select id="f-famille"></select>
        </div>
        <div>
          <label>Stock initial</label>
          <input type="number" id="f-stock" value="0" min="0">
        </div>
        <div>
          <label>Seuil de commande</label>
          <input type="number" id="f-seuil" value="3" min="0">
        </div>
      </div>
      <div class="actions-row">
        <button class="btn btn-accent" id="btnSaveProd" style="flex:2">Enregistrer</button>
        <button class="btn btn-ghost" id="btnCancelEdit" style="display:none">Annuler</button>
      </div>
    </div>

    <div class="card">
      <h2 class="section-title">Catalogue (<span id="prodCount">0</span>)</h2>
      <div id="prodList"><p class="empty-hint">Aucun produit enregistré. Ajoute ton premier article ci-dessus.</p></div>
    </div>
  </section>

</main>

<div class="toast" id="toast"></div>

<nav class="tabbar">
  <button class="tab active" data-view="scan"><span class="ic">🔍</span>Scanner</button>
  <button class="tab" data-view="dash"><span class="ic">📊</span>Tableau de bord</button>
  <button class="tab" data-view="prod"><span class="ic">🗂️</span>Produits</button>
</nav>

<script src="https://cdn.jsdelivr.net/npm/html5-qrcode@2.3.8/html5-qrcode.min.js"></script>
<script>
(function(){
  "use strict";

  const FAMILLES = [
    { code:"1001", nom:"Appareils photo", secteur:"Photo" },
    { code:"1002", nom:"Objectif photo", secteur:"Photo" },
    { code:"1004", nom:"Divers périph. photo", secteur:"Photo" },
    { code:"1013", nom:"Périphérique vidéo", secteur:"TV / Vidéo" },
    { code:"1006", nom:"TV écrans plats", secteur:"TV / Vidéo" },
    { code:"1024", nom:"Lecteur/Enreg/DVD", secteur:"TV / Vidéo" },
    { code:"1014", nom:"Hifi & Micro Chaîne", secteur:"Son" },
    { code:"1015", nom:"Enceinte & Accès.", secteur:"Son" },
    { code:"1021", nom:"Audio traditionnel", secteur:"Son" },
    { code:"1064", nom:"Casques & Accessoires", secteur:"Son" },
    { code:"1025", nom:"Ordinateur", secteur:"Micro / Laptop" },
    { code:"1026", nom:"Périphérique micro & imprimante", secteur:"Micro / Laptop" },
    { code:"1027", nom:"Moniteur", secteur:"Micro / Laptop" },
    { code:"1028", nom:"Gaming son imagerie", secteur:"Micro / Laptop" },
    { code:"1029", nom:"Stockage lecteur", secteur:"Micro / Laptop" },
    { code:"1030", nom:"Bureautique réseau & Mémoire", secteur:"Micro / Laptop" },
    { code:"1034", nom:"Liseuse", secteur:"Micro / Laptop" },
    { code:"1035", nom:"Objets connectés", secteur:"Objets connectés" },
    { code:"1037", nom:"Téléphonie", secteur:"Téléphonie" },
    { code:"1043", nom:"Téléphonie", secteur:"Téléphonie" },
    { code:"1076", nom:"Accessoires Mobiles (GSM)", secteur:"Accessoires Mobiles (GSM)" },
    { code:"1067", nom:"Papiers et encreur", secteur:"Papiers et encreur" },
    { code:"1069", nom:"Accessoires Micro", secteur:"Accessoires Micro" }
  ];
  const SECTEURS = [...new Set(FAMILLES.map(f=>f.secteur))];
  function famillesDe(secteur){ return FAMILLES.filter(f=>f.secteur===secteur); }
  const RESPONSABLES = [
    { nom: "Ha
