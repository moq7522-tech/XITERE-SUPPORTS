<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#090d18">
<title>XITER supports</title>
<style>
:root{color-scheme:dark;--bg:#080c16;--panel:rgba(20,28,47,.78);--line:rgba(255,255,255,.11);--muted:#91a0bb;--text:#f3f6ff;--cyan:#70e1f5;--violet:#a78bfa;--red:#ff718b}
*{box-sizing:border-box}body{margin:0;min-height:100vh;font-family:Inter,ui-sans-serif,system-ui,-apple-system,Segoe UI,sans-serif;color:var(--text);background:radial-gradient(ellipse at 12% 0%,#24305a 0,transparent 38%),radial-gradient(ellipse at 95% 20%,#183d4b 0,transparent 32%),linear-gradient(145deg,#080c16,#0d1425 55%,#090d18);padding:28px 16px 50px}
.wrap{width:min(980px,100%);margin:auto}#connectPanel{margin-top:clamp(70px,14vh,150px)}.top{display:flex;align-items:center;justify-content:space-between;gap:16px;margin-bottom:24px}.brand{display:flex;align-items:center;gap:13px}.logo{width:46px;height:46px;border-radius:15px;display:grid;place-items:center;background:linear-gradient(145deg,#8cecff,#8d79ff);box-shadow:0 8px 30px #6d8dff55;color:#10172a;font-size:22px;font-weight:900}.brand h1{font-size:20px;margin:0;letter-spacing:.2px}.brand p{margin:4px 0 0;color:var(--muted);font-size:12px;letter-spacing:1.7px;text-transform:uppercase}.pill{border:1px solid var(--line);border-radius:999px;padding:8px 12px;color:#b9c7e2;font-size:12px;background:#ffffff08}
.panel{background:linear-gradient(145deg,#17223a,#101a2d);border:1px solid var(--line);border-radius:18px;box-shadow:0 8px 24px #0004;padding:20px;margin-bottom:15px}
h2{font-size:18px;margin:0 0 7px}.sub{color:var(--muted);font-size:13px;line-height:1.55;margin:0 0 20px}
.grid{display:grid;grid-template-columns:1fr 1fr;gap:14px}.field{display:flex;flex-direction:column;gap:8px}.field.full{grid-column:1/-1}label{font-size:12px;color:#c2cce0;font-weight:650;letter-spacing:.3px}input,textarea{width:100%;border:1px solid #ffffff19;background:#080e1dba;color:var(--text);border-radius:12px;padding:14px 15px;outline:none;font:inherit;font-size:14px;transition:border-color .15s}input:focus,textarea:focus{border-color:#77dff0;box-shadow:0 0 0 3px #70e1f51b}input::placeholder,textarea::placeholder{color:#64718b}.hint{font-size:11px;color:#8190aa;line-height:1.45}
.actions{display:flex;gap:10px;flex-wrap:wrap;margin-top:18px}.btn{border:1px solid #ffffff20;border-radius:12px;padding:12px 17px;color:#edf5ff;background:linear-gradient(145deg,#263552,#17233a);font-weight:700;font-size:13px;cursor:pointer;transition:background .15s,border-color .15s;box-shadow:0 3px 10px #0002}.btn:hover{filter:brightness(1.08)}.btn.primary{color:#071321;background:linear-gradient(110deg,#7de8f5,#9c8bff);border:0}.btn.danger{background:linear-gradient(120deg,#612c45,#351d36);color:#ffc0cd}.btn:disabled{opacity:.5;cursor:wait;transform:none}
.status{display:none;margin-top:14px;padding:12px 14px;border-radius:12px;font-size:13px;line-height:1.45}.status.show{display:block}.status.ok{background:#153a32;color:#a9f5d5;border:1px solid #3d9b7a55}.status.err{background:#451f31;color:#ffc0d0;border:1px solid #e76b8a55}.status.info{background:#182d48;color:#b8dcff;border:1px solid #5a9ad455}
.toolbar{display:flex;align-items:center;justify-content:space-between;gap:14px;margin-bottom:15px}.toolbar h2{margin:0}.toolbar .count{font-size:12px;color:var(--muted)}.search{max-width:280px;padding:11px 13px}.records{display:grid;gap:11px}.record{border:1px solid var(--line);border-radius:15px;padding:15px;background:linear-gradient(120deg,#ffffff08,#ffffff03);display:flex;justify-content:space-between;gap:14px;align-items:center;min-width:0}.record-main{min-width:0}.record-key{font-weight:750;font-size:14px;overflow-wrap:anywhere}.record-value{color:#9eacc5;font-size:12px;margin-top:6px;overflow-wrap:anywhere;white-space:pre-wrap;max-height:65px;overflow:hidden}.record-value.status-active{color:#55e69a;font-weight:800}.record-value.status-pending{color:#f4c76b;font-weight:750}.record-actions{display:flex;gap:7px;flex-shrink:0}.mini{padding:8px 11px;border-radius:9px;font-size:11px}.empty{text-align:center;padding:35px 12px;color:var(--muted);border:1px dashed #ffffff22;border-radius:15px;font-size:13px}.hidden{display:none!important}
.modal{position:fixed;inset:0;background:#030610c9;display:grid;place-items:center;padding:16px;z-index:5}.modal-card{width:min(520px,100%);background:#111b30;border:1px solid #ffffff22;border-radius:20px;padding:22px;box-shadow:0 25px 90px #000b}.modal-card h2{margin-bottom:16px}.modal-card textarea{min-height:145px;resize:vertical;font-family:ui-monospace,monospace;font-size:13px}.foot{text-align:center;color:#697894;font-size:11px;margin-top:20px;line-height:1.6}

.status-tabs{display:flex;gap:9px;flex-wrap:wrap;margin:0 0 17px}
.status-tab{border:1px solid #ffffff20;border-radius:12px;padding:11px 14px;background:#0b1427;color:#aebdd8;font-weight:750;font-size:12px;cursor:pointer;transition:.2s}
.status-tab span{display:inline-grid;place-items:center;min-width:22px;height:21px;margin-left:5px;padding:0 5px;border-radius:7px;background:#ffffff12;color:#e9f3ff}
.status-tab.active{border-color:#70e1f5aa;color:#8cefff;background:linear-gradient(110deg,#70e1f51c,#a78bfa1c);box-shadow:0 0 18px #70e1f51c}
.generator-card select{width:100%;border:1px solid #52678c66;background:#080f20;color:var(--text);border-radius:13px;padding:15px;font:inherit;font-size:14px;outline:none}
.generator-card select:focus{border-color:#78e6f4;box-shadow:0 0 0 3px #70e1f522}
.device-list{margin-top:8px;padding:9px 11px;border-radius:10px;background:#081426;border:1px solid #70e1f522;color:#9fe9f4;font-size:11px;line-height:1.6;overflow-wrap:anywhere}
.device-list b{color:#dceaff}
.generator-card{width:min(560px,100%);padding:25px;background:radial-gradient(circle at 100% 0%,#283a62 0,transparent 36%),linear-gradient(145deg,#14213a,#0d1629);border:1px solid #8b9cff44;box-shadow:0 25px 90px #000c,0 0 35px #7188ff18;max-height:92vh;overflow:auto}
.modal-head{display:flex;align-items:center;gap:14px;margin-bottom:23px}
.modal-icon{width:48px;height:48px;flex:0 0 48px;border-radius:15px;display:grid;place-items:center;font-size:23px;color:#091322;background:linear-gradient(135deg,#83edfa,#a58bff);box-shadow:0 7px 25px #8a9cff55}
.eyebrow{font-size:10px;letter-spacing:2px;color:#8fe8f5;font-weight:800;margin-bottom:5px}
.modal-head h2{font-size:21px;margin:0}
.modal-sub{font-size:12px;color:#91a0bb;margin:5px 0 0}
.generator-card .field{margin-bottom:17px}
.generator-card label{font-size:11px;letter-spacing:1px;color:#d4def3}
.generator-card input,.generator-card textarea{border-radius:13px;background:#080f20;border:1px solid #52678c66;padding:15px}
.generator-card input:focus,.generator-card textarea:focus{border-color:#78e6f4;box-shadow:0 0 0 3px #70e1f522,0 0 18px #70e1f414}
.generator-preview{display:flex;align-items:center;gap:11px;padding:14px;border:1px solid #8b9cff33;border-radius:14px;background:linear-gradient(100deg,#70e1f511,#a78bfa11);margin-top:5px}
.preview-dot{width:10px;height:10px;border-radius:50%;background:#72e9f5;box-shadow:0 0 12px #72e9f5;flex:0 0 10px}
.generator-preview strong,.generator-preview small{display:block}
.generator-preview strong{font-size:11px;letter-spacing:1px;color:#dceaff}
.generator-preview small{font-size:10px;color:#8f9fbb;margin-top:4px}
.modal-actions{margin-top:21px}
.modal-actions .btn{padding:13px 18px}
@media(max-width:620px){body{padding:18px 12px 35px}.panel{padding:18px;border-radius:19px}.grid{grid-template-columns:1fr}.field.full{grid-column:auto}.top{align-items:flex-start}.pill{font-size:10px}.toolbar{align-items:flex-start;flex-direction:column}.search{max-width:none}.record{align-items:flex-start;flex-direction:column}.record-actions{width:100%}.record-actions .btn{flex:1}}

.menu-trigger{width:44px;height:44px;border:1px solid #ffffff24;border-radius:13px;background:#111d32;color:#eaf5ff;font-size:23px;cursor:pointer;display:grid;place-items:center;flex:0 0 44px}
.top{justify-content:flex-start}.top .pill{margin-left:auto}
.drawer-shade{position:fixed;inset:0;background:#020610b8;z-index:20;opacity:0;pointer-events:none;transition:.22s}
.drawer-shade.open{opacity:1;pointer-events:auto}.drawer{position:fixed;z-index:21;inset:0 auto 0 0;width:min(330px,86vw);padding:22px 16px;background:linear-gradient(160deg,#1b2b49,#0b1222 70%);border-right:1px solid #91a9ff44;box-shadow:20px 0 70px #0009;transform:translateX(-105%);transition:transform .24s;overflow:auto}.drawer.open{transform:translateX(0)}
.drawer-head{display:flex;align-items:center;justify-content:space-between;margin-bottom:22px}.drawer-head strong{font-size:17px}.drawer-close{border:0;background:#ffffff12;color:#fff;border-radius:10px;padding:8px 12px;font-size:20px}
.nav-item{display:flex;align-items:center;gap:13px;width:100%;padding:15px 13px;margin:8px 0;border:1px solid #ffffff12;border-radius:13px;background:#ffffff08;color:#eaf1ff;text-align:left;font:700 13px inherit;cursor:pointer}.nav-item.active{border-color:#73e2f5aa;background:linear-gradient(100deg,#70e1f522,#a78bfa22);color:#9aeeff}.nav-icon{width:27px;text-align:center;font-size:19px}
.nav-caption{font-size:10px;letter-spacing:1.8px;color:#7185a7;margin:20px 10px 8px}.view-panel{display:none}.view-panel.current{display:block}.login-key{margin:12px 0;padding:15px;border:1px solid #ffffff1b;border-radius:14px;background:#ffffff08}.login-key h3{margin:0 0 9px;font-size:14px}.hwid-chip{display:block;margin:6px 0;padding:9px 10px;border-radius:9px;background:#071326;color:#a4eefa;font:12px ui-monospace,monospace;overflow-wrap:anywhere}
.ui-fields{display:grid;grid-template-columns:1fr 1fr;gap:12px}.ui-fields .field{min-width:0}.ui-fields textarea{min-height:82px}.ui-fields input[type=checkbox]{width:20px;height:20px}.ui-fields .field.full{grid-column:1/-1}.section-note{font-size:12px;color:#91a0bb;line-height:1.5;margin-bottom:15px}
@media(max-width:620px){.ui-fields{grid-template-columns:1fr}.ui-fields .field.full{grid-column:auto}}
</style>
</head>
<body>
<div class="wrap">
  <header class="top">
    <button class="menu-trigger" id="menuTrigger" aria-label="Open menu">☰</button>
    <div class="brand"><div class="logo">X</div><div><h1>XITER supports</h1><p>Firebase Control Studio</p></div></div>
    <div class="pill">REALTIME DATABASE</div>
  </header>

  <section class="panel" id="connectPanel">
    <h2>Connect your Firebase</h2>
    <p class="sub">Connect your Realtime Database and manage keys, values and optional HWIDs inside <b>/keys</b>.</p>
    <div class="grid">
      <div class="field full"><label for="dbUrl">FIREBASE DATABASE URL</label><input id="dbUrl" type="url" placeholder="https://your-project-default-rtdb.firebaseio.com" autocomplete="url"></div>
      <div class="field full"><label for="token">AUTH TOKEN <span style="color:#8b9ab4;font-weight:400">(OPTIONAL)</span></label><input id="token" type="password" placeholder="Paste ID token if your database requires authentication" autocomplete="off"><div class="hint">Leave blank if your Firebase Security Rules allow access without authentication. Token is kept only in this page's memory.</div></div>
    </div>
    <div class="actions"><button class="btn primary" id="connectBtn">Connect to Firebase ↗</button></div>
    <div class="status" id="connectStatus" role="status"></div>
  </section>

  <section class="panel view-panel" id="activeKeysPanel">
    <div class="toolbar">
      <div><h2>Active Keys</h2><div class="count" id="activeKeysSummary">Keys become Active after a successful app login.</div></div>
    </div>
    <div class="actions" style="margin:0 0 18px">
      <button class="btn primary" id="activeAddBtn" style="width:100%;padding:19px 22px;font-size:17px;border-radius:15px">＋ ADD KEY</button>
    </div>
    <div class="records" id="activeKeyRecords">
      <div class="empty">Connect Firebase to view keys.</div>
    </div>
  </section>

  <section class="panel hidden" id="homePanel">
    <div class="toolbar"><div><h2>Home • Key Management</h2><div class="count" id="dbLabel">/keys</div></div><input class="search" id="search" placeholder="Search keys / HWID..." aria-label="Search keys"></div>
    <div class="status-tabs" role="tablist" aria-label="Key status">
      <button class="status-tab active" data-filter="active">● Active <span id="activeCount">0</span></button>
      <button class="status-tab" data-filter="expired">◷ Expired <span id="expiredCount">0</span></button>
      <button class="status-tab" data-filter="banned">⛔ Device Banned <span id="bannedCount">0</span></button>
    </div>
    <div class="actions" style="margin:0 0 16px"><button class="btn primary" id="addBtn">＋ Add new key</button><button class="btn" id="bulkBtn">＋ Bulk add keys</button><button class="btn" id="banBtn">⛔ Ban HWID</button><button class="btn danger" id="expiredBtn">Delete expired</button><button class="btn" id="refreshBtn">↻ Refresh</button><button class="btn" id="disconnectBtn">Disconnect</button></div>
    <div class="status" id="dataStatus" role="status"></div>
    <div class="records" id="records"><div class="empty">Connect to load your Firebase records.</div></div>
  </section>

  <section class="panel view-panel" id="loginPanel">
    <div class="toolbar"><div><h2>Keys Login Info</h2><div class="count">Device HWIDs recorded under /keys/{key}/devices</div></div><button class="btn" id="loginRefresh">↻ Refresh</button></div>
    <p class="section-note">Yahan wahi HWID dikhenge jo tumhara app/backend successful login par Firebase mein record karega. HTML khud phone ka HWID discover nahi kar sakta.</p>
    <div id="loginRecords"><div class="empty">Connect Firebase to load login info.</div></div>
  </section>
  <section class="panel view-panel" id="banPanel">
    <div class="toolbar"><div><h2>Device Ban Manager</h2><div class="count">Firebase path: /ban_list</div></div><button class="btn" id="banRefresh">↻ Refresh</button></div>
    <div class="grid">
      <div class="field"><label for="banHwidInput">DEVICE HWID</label><input id="banHwidInput" placeholder="Paste exact HWID"></div>
      <div class="field"><label for="banReasonInput">BAN REASON</label><input id="banReasonInput" value="Violation of Terms" placeholder="Reason"></div>
    </div>
    <div class="actions"><button class="btn primary" id="saveBanBtn">⛔ Ban / Upload HWID</button><button class="btn" id="uploadBanJsonBtn">Upload ban-list JSON</button></div>
    <div class="status" id="banStatus"></div><div class="records" id="banRecords"></div>
  </section>
  <section class="panel view-panel" id="firebasePanel">
    <h2>Firebase Connection</h2><p class="section-note">Database URL aur optional auth token yahan manage karo. Connect/disconnect se current session control hoga.</p>
    <div class="grid">
      <div class="field full"><label for="dbUrlMirror">FIREBASE DATABASE URL</label><input id="dbUrlMirror" placeholder="https://project-default-rtdb.firebaseio.com"></div>
      <div class="field full"><label for="tokenMirror">AUTH TOKEN (OPTIONAL)</label><input id="tokenMirror" type="password" placeholder="Optional Firebase ID token"></div>
    </div>
    <div class="actions"><button class="btn primary" id="firebaseConnectBtn">Connect / Update</button><button class="btn danger" id="firebaseDisconnectBtn">Disconnect</button></div><div class="status" id="firebaseStatus"></div>
  </section>
  <section class="panel view-panel" id="uiPanel">
    <div class="toolbar"><div><h2>App UI Settings</h2><div class="count">Firebase path: /free_card</div></div><button class="btn" id="uiRefreshBtn">↻ Load</button></div>
    <p class="section-note">Screenshot wale app ke /free_card fields yahan se edit honge. Existing fields aur unki value type preserve rahegi.</p>
    <div id="uiFields" class="ui-fields"><div class="empty">Connect Firebase to load UI settings.</div></div>
    <div class="actions"><button class="btn primary" id="saveUiBtn">Save UI Settings</button></div><div class="status" id="uiStatus"></div>
  </section>
  <div class="foot">XITER SUPPORTS • Your database remains yours<br>Device bans are stored separately in /ban_list. Login HWIDs require your app/backend to record them under /keys/{key}/devices/{hwid}.</div>
</div>

<div class="drawer-shade" id="drawerShade"></div>
<aside class="drawer" id="sideDrawer" aria-label="Main menu">
  <div class="drawer-head"><strong>✦ XITER SUPPORTS MENU</strong><button class="drawer-close" id="drawerClose" aria-label="Close">×</button></div>
  <div class="nav-caption">MANAGEMENT</div>
  <button class="nav-item active" data-view="home"><span class="nav-icon">🏠</span>Home — All Management</button>
  <button class="nav-item" data-view="active"><span class="nav-icon">🔑</span>Active Keys — Add / Edit</button>
  <button class="nav-item" data-view="ban"><span class="nav-icon">⛔</span>Ban Device — Edit / Upload</button>
  <button class="nav-item" data-view="login"><span class="nav-icon">📱</span>Keys Login Info — HWIDs</button>
  <div class="nav-caption">CONFIGURATION</div>
  <button class="nav-item" data-view="firebase"><span class="nav-icon">🔥</span>Firebase Info — Connect</button>
  <button class="nav-item" data-view="ui"><span class="nav-icon">🎨</span>UI Settings — Edit App UI</button>
</aside>

<div class="modal hidden" id="editor" role="dialog" aria-modal="true" aria-labelledby="editorTitle">
  <div class="modal-card generator-card">
    <div class="modal-head">
      <div class="modal-icon">✦</div>
      <div>
        <div class="eyebrow">KEY GENERATOR • CONTROL PANEL</div>
        <h2 id="editorTitle">Generate New Keys</h2>
        <p class="modal-sub">Configure quantity, expiry and device binding</p>
      </div>
    </div>

    <div id="generateFields">
      <div class="field">
        <label for="entryCount">HOW MANY KEYS TO GENERATE?</label>
        <input id="entryCount" type="number" min="1" max="100" value="1" inputmode="numeric" placeholder="Enter key quantity">
        <div class="hint">Choose between 1 and 100 unique keys.</div>
      </div>

      <div class="field">
        <label for="entryExpiry">SELECT EXPIRY DATE</label>
        <input id="entryExpiry" type="date">
        <div class="hint">Select the expiry date only. No time is saved.</div>
      </div>

      <div class="field">
        <label for="entryHwid">DEVICE ID / HWID (OPTIONAL FIXED DEVICE)</label>
        <input id="entryHwid" placeholder="Enter a specific device HWID">
        <div class="hint">Use this only when the key should be pre-bound to one device.</div>
      </div>
      <div class="field">
        <label for="entryMaxDevices">HOW MANY DEVICES CAN LOGIN WITH EACH KEY?</label>
        <select id="entryMaxDevices">
          <option value="1">1 Device</option><option value="2">2 Devices</option><option value="3">3 Devices</option><option value="5">5 Devices</option><option value="10">10 Devices</option><option value="0">Unlimited</option>
        </select>
        <div class="hint">The app/backend must enforce this limit when a device logs in.</div>
      </div>

      <div class="generator-preview">
        <span class="preview-dot"></span>
        <div><strong>DP-VIP KEY BATCH</strong><small>Unique keys • Firebase sync • Device binding</small></div>
      </div>
    </div>

    <div id="editFields" class="hidden">
      <div class="field">
        <label for="entryKey">KEY / RECORD ID</label>
        <input id="entryKey" placeholder="Key name">
      </div>
      <div class="field">
        <label for="editHwid">DEVICE ID / HWID</label>
        <input id="editHwid" placeholder="Enter or update HWID">
      </div>
      <div class="field">
        <label for="editExpiry">EXPIRY DATE</label>
        <input id="editExpiry" type="date">
      </div>
      <div class="field">
        <label for="editMaxDevices">MAXIMUM LOGIN DEVICES</label>
        <select id="editMaxDevices">
          <option value="1">1 Device</option><option value="2">2 Devices</option><option value="3">3 Devices</option><option value="5">5 Devices</option><option value="10">10 Devices</option><option value="0">Unlimited</option>
        </select>
      </div>
      <div class="field">
        <label for="entryValue">VALUE (JSON OR PLAIN TEXT)</label>
        <textarea id="entryValue" spellcheck="false" placeholder='Example: {"status":"active","code":"ABC123"}'></textarea>
      </div>
    </div>

    <div class="actions modal-actions">
      <button class="btn primary" id="saveBtn">✦ Generate Keys</button>
      <button class="btn" id="cancelBtn">Cancel</button>
    </div>
    <div class="status" id="editorStatus"></div>
  </div>
</div>
<script>
(() => {
  const $ = id => document.getElementById(id);
  let baseUrl = '', authToken = '', records = {}, bannedDevices = {}, uiConfig = {}, editingKey = null, busy = false, activeFilter = 'active';
  const connectStatus = $('connectStatus'), dataStatus = $('dataStatus'), editorStatus = $('editorStatus');
  function status(el, message, type='info') { el.textContent = message; el.className = 'status show ' + type; }
  function clearStatus(el) { el.textContent=''; el.className='status'; }
  function cleanBase(value) {
    let s = value.trim().replace(/\/+$/, '');
    if (!/^https:\/\/[a-z0-9-]+(?:\.[a-z0-9-]+)+$/i.test(s)) throw new Error('Enter a valid HTTPS Firebase database URL.');
    return s;
  }
  function bannedEndpoint() { const u=new URL(baseUrl + '/ban_list.json'); if(authToken)u.searchParams.set('auth',authToken); return u.toString(); }
  function pathEndpoint(path){const safe=path.replace(/^\/+|\/+$/g,'').split('/').map(encodeURIComponent).join('/');const u=new URL(baseUrl+'/'+safe+'.json');if(authToken)u.searchParams.set('auth',authToken);return u.toString();}
  function endpoint(key) {
    const suffix = key === undefined ? 'keys' : 'keys/' + encodeURIComponent(String(key));
    const u = new URL(baseUrl + '/' + suffix + '.json');
    if (authToken) u.searchParams.set('auth', authToken);
    return u.toString();
  }
  async function request(url, options={}) {
    const response = await fetch(url, { ...options, headers:{'Content-Type':'application/json', ...(options.headers||{})} });
    const body = await response.text();
    let data = null;
    try { data = body ? JSON.parse(body) : null; } catch { data = body; }
    if (!response.ok) {
      const message = data && typeof data === 'object' && data.error ? data.error : `HTTP ${response.status}`;
      throw new Error(String(message) + '. Check the URL, token and Firebase Security Rules.');
    }
    return data;
  }
  function setBusy(value) {
    busy = value;
    ['connectBtn','addBtn','activeAddBtn','refreshBtn','saveBtn'].forEach(id => $(id).disabled = value);
  }
  async function loadRecords() {
    setBusy(true); clearStatus(dataStatus);
    try {
      const data = await request(endpoint());
      records = data && typeof data === 'object' ? data : {};
      try { const banned=await request(bannedEndpoint()); bannedDevices=banned&&typeof banned==='object'?banned:{}; } catch { bannedDevices={}; }
      try { const ui=await request(pathEndpoint('free_card')); uiConfig=ui&&typeof ui==='object'?ui:{}; } catch { uiConfig={}; }
      $('homePanel').classList.remove('hidden'); $('connectPanel').classList.add('hidden');
      $('dbLabel').textContent = baseUrl.replace(/^https:\/\//,'') + '  •  /keys';
      render();
      status(dataStatus, 'Database synced successfully.', 'ok');
      return true;
    } catch(e) {
      status(dataStatus, e.message, 'err');
      status(connectStatus, 'Connection failed: ' + e.message, 'err');
      return false;
    } finally { setBusy(false); }
  }
  function formatExpiryDate(input) {
    if (!input) return '';
    const parts=String(input).split('-');
    if (parts.length===3 && parts[0].length===4) return `${parts[2]}/${parts[1]}/${parts[0]}`;
    return String(input);
  }
  function expiryDateOf(record) {
    if (!record || typeof record!=='object') return '';
    const value=record.value && typeof record.value==='object' ? record.value : {};
    return value.expires_date || record.expires_date || (record.expiresAt ? new Date(record.expiresAt).toLocaleDateString('en-GB') : '');
  }
  function dateIsExpired(record) {
    const raw=expiryDateOf(record);
    if (!raw) return false;
    const m=String(raw).match(/^(\d{2})\/(\d{2})\/(\d{4})$/);
    const d=m ? new Date(Number(m[3]),Number(m[2])-1,Number(m[1]),23,59,59,999) : new Date(raw);
    return !Number.isNaN(d.getTime()) && d.getTime()<Date.now();
  }
  function render() {
    const host=$('records'); host.replaceChildren();
    const query=$('search').value.trim().toLowerCase(), now=Date.now();
    const all=Object.entries(records);
    const isExpired=v=>dateIsExpired(v) || !!(v&&typeof v==='object'&&v.expiresAt&&new Date(v.expiresAt).getTime()<=now);
    const active=all.filter(([,v])=>!isExpired(v)), expired=all.filter(([,v])=>isExpired(v));
    const bannedEntries=Object.entries(bannedDevices);
    $('activeCount').textContent=active.length; $('expiredCount').textContent=expired.length; $('bannedCount').textContent=bannedEntries.length;
    $('dbLabel').textContent=`${baseUrl.replace(/^https:\/\//,'')} • /keys • ${all.length} keys`;
    if(activeFilter==='banned'){
      const filtered=bannedEntries.filter(([hwid,v])=>(hwid+' '+formatValue(v)).toLowerCase().includes(query));
      if(!filtered.length){host.innerHTML='<div class="empty">No banned devices found.</div>';return;}
      filtered.forEach(([hwid,info])=>{
        const card=document.createElement('div');card.className='record';const main=document.createElement('div');main.className='record-main';
        const name=document.createElement('div');name.className='record-key';name.textContent='⛔ '+hwid;
        const val=document.createElement('div');val.className='record-value';val.textContent='Device banned • '+(typeof info==='string'?info:(info&&info.reason?info.reason:'Banned device')); 
        main.append(name,val);const actions=document.createElement('div');actions.className='record-actions';
        const unban=document.createElement('button');unban.className='btn mini';unban.textContent='Unban';unban.addEventListener('click',()=>unbanHwid(hwid));actions.append(unban);card.append(main,actions);host.append(card);
      });return;
    }
    let entries=(activeFilter==='active'?active:expired).filter(([k,v])=>(k+' '+formatValue(v)+' '+(v&&typeof v==='object'?(v.hwid||'')+' '+formatValue(v.devices||{}):'')).toLowerCase().includes(query));
    if(!entries.length){const empty=document.createElement('div');empty.className='empty';empty.textContent=activeFilter==='expired'?'No expired keys.':'No active keys found.';host.append(empty);return;}
    entries.forEach(([key,value])=>{
      const item=value&&typeof value==='object'&&!Array.isArray(value)?value:{}, valObj=item.value&&typeof item.value==='object'?item.value:{}, devices=item.devices&&typeof item.devices==='object'?Object.entries(item.devices):[], max=Number(valObj.max_devices??item.max_devices??item.maxDevices??1);
      const card=document.createElement('div');card.className='record';const main=document.createElement('div');main.className='record-main';
      const name=document.createElement('div');name.className='record-key';name.textContent=key;
      const val=document.createElement('div');val.className='record-value '+(isExpired(value)?'':(devices.length>0?'status-active':'status-pending'));val.textContent=`${isExpired(value)?'EXPIRED':(devices.length>0?'ACTIVE':'PENDING')} • ${devices.length}/${max===0?'∞':max} device logins${item.hwid?' • Fixed HWID: '+item.hwid:''}${expiryDateOf(item)?' • Expires: '+expiryDateOf(item):''}`;
      main.append(name,val);
      if(devices.length){const list=document.createElement('div');list.className='device-list';list.innerHTML='<b>LOGGED-IN DEVICE HWIDs</b><br>'+devices.map(([hwid])=>escapeHtml(hwid)).join('<br>');main.append(list);}
      const actions=document.createElement('div');actions.className='record-actions';
      const copy=document.createElement('button');copy.className='btn mini';copy.textContent='Copy';copy.addEventListener('click',()=>copyText(key,copy));
      const edit=document.createElement('button');edit.className='btn mini';edit.textContent='Edit';edit.addEventListener('click',()=>openEditor(key));
      const del=document.createElement('button');del.className='btn mini danger';del.textContent='Delete';del.addEventListener('click',()=>deleteRecord(key));
      actions.append(copy,edit,del);card.append(main,actions);host.append(card);
    });
  }
  function escapeHtml(value){return String(value).replace(/[&<>"']/g,c=>({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c]));}
  async function unbanHwid(hwid){
    if(!confirm('Remove this HWID from the banned list?'))return;
    try{const u=new URL(baseUrl+'/ban_list/'+encodeURIComponent(hwid)+'.json');if(authToken)u.searchParams.set('auth',authToken);await request(u.toString(),{method:'DELETE'});delete bannedDevices[hwid];render();status(dataStatus,'Device removed from /ban_list.','ok');}
    catch(e){status(dataStatus,e.message,'err');}
  }

  function formatValue(v) {
    if (typeof v === 'string') return v;
    try { return JSON.stringify(v, null, 2); } catch { return String(v); }
  }
  function parseValue(raw) {
    const text = raw.trim();
    if (!text) return '';
    try { return JSON.parse(text); } catch { return raw; }
  }
  function openEditor(key=null) {
    editingKey=key;
    const isEdit=key!==null;
    $('editorTitle').textContent=isEdit?'Edit Key Details':'Generate New Keys';
    $('generateFields').classList.toggle('hidden',isEdit);
    $('editFields').classList.toggle('hidden',!isEdit);
    $('saveBtn').textContent=isEdit?'Save Changes':'✦ Generate Keys';
    if(isEdit){
      const item=records[key] && typeof records[key]==='object' && !Array.isArray(records[key]) ? records[key] : {};
      $('entryKey').value=key;
      $('entryKey').disabled=true;
      $('editHwid').value=item.hwid||'';
      const expiry=expiryDateOf(item), match=String(expiry).match(/^(\d{2})\/(\d{2})\/(\d{4})$/);
      $('editExpiry').value=match?`${match[3]}-${match[2]}-${match[1]}`:'';
      const valObj=item.value&&typeof item.value==='object'?item.value:{};
      $('editMaxDevices').value=String(item.max_devices??valObj.max_devices??item.maxDevices??1);
      const directRecord={...valObj,...item}; delete directRecord.value; delete directRecord.plan; delete directRecord.maxDevices; delete directRecord.expiresAt;
      $('entryValue').value=formatValue(directRecord);
    }else{
      $('entryCount').value='1';
      $('entryExpiry').value='';
      $('entryHwid').value='';
      $('entryMaxDevices').value='1';
    }
    clearStatus(editorStatus);
    $('editor').classList.remove('hidden');
    (isEdit?$('editHwid'):$('entryCount')).focus();
  }
  function closeEditor() { $('editor').classList.add('hidden'); editingKey=null; }
  async function saveRecord() {
    if(editingKey===null){
      const count=Number($('entryCount').value);
      const hwid=$('entryHwid').value.trim();
      const maxDevices=Number($('entryMaxDevices').value);
      const expiry=$('entryExpiry').value;
      if(!Number.isInteger(count)||count<1||count>100){status(editorStatus,'Enter a whole number between 1 and 100.','err');return;}
      let expiresDate='';
      if(expiry){
        const date=new Date(expiry+'T23:59:59');
        if(Number.isNaN(date.getTime())||date.getTime()<Date.now()){status(editorStatus,'Please select a valid future expiry date.','err');return;}
        expiresDate=formatExpiryDate(expiry);
      }
      setBusy(true);
      try{
        const updated={...records}, created=[];
        for(let i=0;i<count;i++){
          const key=makeUniqueKey(updated);
          const item={max_devices:maxDevices};
          if(expiresDate)item.expires_date=expiresDate;
          if(hwid)item.hwid=hwid;
          updated[key]=item;created.push(key);
        }
        await request(endpoint(),{method:'PUT',body:JSON.stringify(updated)});
        records=updated;closeEditor();render();renderActiveKeys();
        status(dataStatus,`${created.length} unique DP-VIP key${created.length===1?'':'s'} generated and saved successfully.`, 'ok');
      }catch(e){status(editorStatus,e.message,'err');}
      finally{setBusy(false);}
      return;
    }

    const key=editingKey, raw=$('entryValue').value, hwid=$('editHwid').value.trim(), expiry=$('editExpiry').value, maxDevices=Number($('editMaxDevices').value);
    if(expiry && Number.isNaN(new Date(expiry+'T23:59:59').getTime())){status(editorStatus,'Invalid expiry date.','err');return;}
    setBusy(true);
    try{
      const old=records[key]&&typeof records[key]==='object'?records[key]:{};
      let parsed=raw.trim()?parseValue(raw):{};
      if(!parsed || typeof parsed!=='object' || Array.isArray(parsed)) parsed={};
      const legacyValue=old.value&&typeof old.value==='object'?old.value:{};
      const record={...legacyValue,...old,...parsed};
      delete record.value; delete record.plan; delete record.maxDevices; delete record.expiresAt;
      record.max_devices=maxDevices;
      if(expiry)record.expires_date=formatExpiryDate(expiry); else delete record.expires_date;
      if(hwid)record.hwid=hwid; else delete record.hwid;
      await request(endpoint(key),{method:'PUT',body:JSON.stringify(record)});
      closeEditor();await loadRecords();renderActiveKeys();status(dataStatus,'Key updated successfully.','ok');
    }catch(e){status(editorStatus,e.message,'err');}
    finally{setBusy(false);}
  }
  async function unbindKeyHwid(key){
    const item=records[key]&&typeof records[key]==='object'?records[key]:{};
    const hasBinding=!!item.hwid || !!(item.devices&&typeof item.devices==='object'&&Object.keys(item.devices).length);
    if(!hasBinding){status(dataStatus,'No HWID binding found for this key.','info');return;}
    if(!confirm(`Unbind all HWIDs from ${key}? This clears the fixed HWID and recorded device bindings for this key.`))return;
    setBusy(true);
    try{
      const updated={...item};
      delete updated.hwid;
      delete updated.devices;
      await request(endpoint(key),{method:'PUT',body:JSON.stringify(updated)});
      records[key]=updated;
      render();renderActiveKeys();renderLoginInfo();
      status(dataStatus,`All HWID bindings cleared for ${key}.`,'ok');
    }catch(e){status(dataStatus,e.message,'err');}
    finally{setBusy(false);}
  }

  async function deleteRecord(key) {
    if (!confirm(`Delete "${key}" from /keys? This cannot be undone.`)) return;
    setBusy(true);
    try {
      await request(endpoint(key),{method:'DELETE'});
      await loadRecords(); renderActiveKeys(); status(dataStatus,`"${key}" deleted.`, 'ok');
    } catch(e) { status(dataStatus,e.message,'err'); }
    finally { setBusy(false); }
  }

  function makeUniqueKey(existing) {
    const chars='ABCDEFGHJKLMNPQRSTUVWXYZ23456789';
    let candidate='';
    do {
      let part='';
      for(let i=0;i<12;i++) part+=chars[Math.floor(Math.random()*chars.length)];
      candidate='DP-VIP-'+part;
    } while (Object.prototype.hasOwnProperty.call(existing,candidate));
    return candidate;
  }
  async function bulkAdd() {
    const raw=prompt('How many unique DP-VIP keys should be created? (1–100)');
    if(raw===null) return;
    const count=Number(raw);
    if(!Number.isInteger(count)||count<1||count>100){status(dataStatus,'Enter a whole number from 1 to 100.','err');return;}
    const expiryRaw=prompt('Expiry date only (optional, format DD/MM/YYYY). Leave blank for no expiry:','');
    if(expiryRaw===null) return;
    let expiresDate='';
    if(expiryRaw.trim()){
      if(!/^\d{2}\/\d{2}\/\d{4}$/.test(expiryRaw.trim())){status(dataStatus,'Expiry format is invalid. Use DD/MM/YYYY.','err');return;}
      expiresDate=expiryRaw.trim();
    }
    setBusy(true);
    try {
      const updated={...records};
      const created=[];
      for(let i=0;i<count;i++){
        const key=makeUniqueKey(updated);
        const item={max_devices:1};
        if(expiresDate)item.expires_date=expiresDate;
        updated[key]=item; created.push(key);
      }
      await request(endpoint(),{method:'PUT',body:JSON.stringify(updated)});
      records=updated; render();
      status(dataStatus,`${created.length} unique DP-VIP keys created successfully.`, 'ok');
    } catch(e){status(dataStatus,e.message,'err');}
    finally{setBusy(false);}
  }
  async function banHwid() {
    const hwid=prompt('Enter the exact HWID to add to the ban list:');
    if(hwid===null) return;
    if(!hwid.trim()){status(dataStatus,'HWID cannot be blank.','err');return;}
    setBusy(true);
    try {
      const u=new URL(baseUrl+'/ban_list/'+encodeURIComponent(hwid.trim())+'.json');
      if(authToken) u.searchParams.set('auth',authToken);
      const banReason='Violation of Terms';
      await request(u.toString(),{method:'PUT',body:JSON.stringify(banReason)});
      bannedDevices[hwid.trim()]=banReason;render();status(dataStatus,'HWID saved to /ban_list (separate from /keys). Your app/backend must check /ban_list to enforce the ban.','ok');
    } catch(e){status(dataStatus,e.message,'err');}
    finally{setBusy(false);}
  }
  async function deleteExpired() {
    const now=Date.now();
    const expired=Object.entries(records).filter(([,v])=>v && typeof v==='object' && v.expiresAt && new Date(v.expiresAt).getTime()<=now).map(([k])=>k);
    if(!expired.length){status(dataStatus,'No expired keys found.','info');return;}
    if(!confirm(`Delete all ${expired.length} expired keys from /keys? This cannot be undone.`)) return;
    setBusy(true);
    try {
      for(const key of expired) await request(endpoint(key),{method:'DELETE'});
      await loadRecords();
      status(dataStatus,`${expired.length} expired keys deleted.`, 'ok');
    } catch(e){status(dataStatus,e.message,'err');}
    finally{setBusy(false);}
  }

  function openDrawer(){ $('sideDrawer').classList.add('open'); $('drawerShade').classList.add('open'); }
  function closeDrawer(){ $('sideDrawer').classList.remove('open'); $('drawerShade').classList.remove('open'); }
  function showView(view){
    closeDrawer();
    $('connectPanel').classList.toggle('hidden',view!=='firebase' && !!baseUrl);
    $('homePanel').classList.toggle('hidden',view!=='home');
    ['activeKeysPanel','loginPanel','banPanel','firebasePanel','uiPanel'].forEach(id=>$(id).classList.remove('current'));
    if(view==='home'){render();}
    if(view==='active'){ $('activeKeysPanel').classList.add('current'); renderActiveKeys(); }
    if(view==='ban'){$('banPanel').classList.add('current');renderBanList();}
    if(view==='login'){$('loginPanel').classList.add('current');renderLoginInfo();}
    if(view==='firebase'){$('firebasePanel').classList.add('current');$('dbUrlMirror').value=baseUrl;$('tokenMirror').value=authToken;}
    if(view==='ui'){$('uiPanel').classList.add('current');renderUiFields();}
    document.querySelectorAll('.nav-item').forEach(b=>b.classList.toggle('active',b.dataset.view===view));
    if(!baseUrl && view!=='firebase') status(connectStatus,'Connect Firebase first in Firebase Info.','info');
  }
  async function copyText(value, button){
    const original=button.textContent;
    const text=String(value);
    try{
      if(navigator.clipboard && typeof navigator.clipboard.writeText==='function'){
        await navigator.clipboard.writeText(text);
      }else{
        const area=document.createElement('textarea');
        area.value=text;
        area.setAttribute('readonly','');
        area.style.position='fixed';
        area.style.left='0';
        area.style.top='0';
        area.style.width='2px';
        area.style.height='2px';
        area.style.opacity='0.01';
        document.body.appendChild(area);
        area.focus();
        area.select();
        area.setSelectionRange(0, area.value.length);
        const ok=document.execCommand('copy');
        area.remove();
        if(!ok) throw new Error('Clipboard API unavailable');
      }
      button.textContent='COPIED ✓';
      setTimeout(()=>button.textContent=original,1400);
      clearStatus(dataStatus);
    }catch(e){
      // Android browsers that open local content:// files may block clipboard APIs.
      // Show the exact selected key so the user can use the native Copy action.
      const copied=window.prompt('Automatic copy is blocked by this browser. Long-press the key below and choose Copy:',text);
      if(copied!==null){
        button.textContent='KEY SHOWN';
        setTimeout(()=>button.textContent=original,1400);
      }
    }
  }

  function renderActiveKeys(){
    const host=$('activeKeyRecords');host.replaceChildren();
    const entries=Object.entries(records).filter(([,v])=>!dateIsExpired(v));
    $('activeKeysSummary').textContent=`${entries.length} key(s) • Pending until first successful app login`;
    if(!entries.length){host.innerHTML='<div class="empty">No keys found. Tap ADD KEY to create one.</div>';return;}
    entries.forEach(([key,value])=>{
      const item=value&&typeof value==='object'&&!Array.isArray(value)?value:{};
      const devices=item.devices&&typeof item.devices==='object'?Object.keys(item.devices):[];
      const card=document.createElement('div');card.className='record';
      const main=document.createElement('div');main.className='record-main';
      const name=document.createElement('div');name.className='record-key';name.textContent=key;
      const state=document.createElement('div');state.className='record-value '+(devices.length>0?'status-active':'status-pending');
      state.textContent=devices.length>0?'● ACTIVE • Successful app login recorded':'○ PENDING • Not logged in yet';
      main.append(name,state);
      // Put this key's own Copy button directly underneath its key/status.
      const copy=document.createElement('button');copy.className='btn mini';copy.textContent='COPY THIS KEY';copy.setAttribute('type','button');
      copy.addEventListener('click',()=>copyText(key,copy));
      main.append(copy);
      const actions=document.createElement('div');actions.className='record-actions';
      const unbind=document.createElement('button');unbind.className='btn mini';unbind.textContent='Unbind HWID';unbind.addEventListener('click',()=>unbindKeyHwid(key));
      const edit=document.createElement('button');edit.className='btn mini';edit.textContent='Edit';edit.addEventListener('click',()=>openEditor(key));
      const del=document.createElement('button');del.className='btn mini danger';del.textContent='Delete';del.addEventListener('click',()=>deleteRecord(key));
      actions.append(unbind,edit,del);card.append(main,actions);host.append(card);
    });
  }
  function renderLoginInfo(){
    const host=$('loginRecords');host.replaceChildren();let count=0;
    Object.entries(records).forEach(([key,record])=>{const devices=record&&typeof record==='object'&&record.devices&&typeof record.devices==='object'?Object.entries(record.devices):[];if(!devices.length)return;count+=devices.length;const card=document.createElement('div');card.className='login-key';const h=document.createElement('h3');h.textContent=key+' • '+devices.length+' device(s)';card.append(h);devices.forEach(([hwid,info])=>{const chip=document.createElement('div');chip.className='hwid-chip';chip.textContent=hwid+(info&&typeof info==='object'&&info.last_login?' • Last login: '+info.last_login:'');const cp=document.createElement('button');cp.className='btn mini';cp.textContent='Copy HWID';cp.addEventListener('click',()=>copyText(hwid,cp));chip.append(' ',cp);card.append(chip);});host.append(card);});
    if(!count)host.innerHTML='<div class="empty">No login HWIDs recorded yet. Your app/backend must write /keys/{key}/devices/{hwid}.</div>';
  }
  function renderBanList(){
    const host=$('banRecords');host.replaceChildren();const entries=Object.entries(bannedDevices);
    if(!entries.length){host.innerHTML='<div class="empty">No devices in /ban_list.</div>';return;}
    entries.forEach(([hwid,reason])=>{const card=document.createElement('div');card.className='record';const main=document.createElement('div');main.className='record-main';const title=document.createElement('div');title.className='record-key';title.textContent=hwid;const val=document.createElement('div');val.className='record-value';val.textContent=typeof reason==='string'?reason:formatValue(reason);main.append(title,val);const actions=document.createElement('div');actions.className='record-actions';const edit=document.createElement('button');edit.className='btn mini';edit.textContent='Edit';edit.onclick=()=>{$('banHwidInput').value=hwid;$('banReasonInput').value=typeof reason==='string'?reason:(reason?.reason||'Violation of Terms');};const unban=document.createElement('button');unban.className='btn mini danger';unban.textContent='Unban';unban.onclick=()=>unbanHwid(hwid);actions.append(edit,unban);card.append(main,actions);host.append(card);});
  }
  async function saveBanRecord(){const hwid=$('banHwidInput').value.trim(),reason=$('banReasonInput').value.trim()||'Violation of Terms';if(!hwid){status($('banStatus'),'Enter a device HWID.','err');return;}try{await request(pathEndpoint('ban_list/'+hwid),{method:'PUT',body:JSON.stringify(reason)});bannedDevices[hwid]=reason;$('banHwidInput').value='';renderBanList();render();status($('banStatus'),'HWID uploaded to /ban_list.','ok');}catch(e){status($('banStatus'),e.message,'err');}}
  async function uploadBanJson(){const raw=prompt('Paste JSON object for /ban_list. Example: {"HWID_123":"Violation of Terms"}');if(raw===null)return;let obj;try{obj=JSON.parse(raw);if(!obj||typeof obj!=='object'||Array.isArray(obj))throw new Error();}catch{status($('banStatus'),'Invalid JSON object.','err');return;}try{await request(bannedEndpoint(),{method:'PATCH',body:JSON.stringify(obj)});bannedDevices={...bannedDevices,...obj};renderBanList();render();status($('banStatus'),'Ban-list JSON uploaded.','ok');}catch(e){status($('banStatus'),e.message,'err');}}
  function renderUiFields(){const host=$('uiFields');host.replaceChildren();const entries=Object.entries(uiConfig||{});if(!entries.length){host.innerHTML='<div class="empty">No /free_card data found or permission denied.</div>';return;}entries.forEach(([key,value])=>{const wrap=document.createElement('div');wrap.className='field'+(String(value).length>90?' full':'');const label=document.createElement('label');label.textContent=key;label.htmlFor='ui_'+key;let input;if(typeof value==='boolean'){input=document.createElement('input');input.type='checkbox';input.checked=value;}else if(value&&typeof value==='object'){input=document.createElement('textarea');input.value=JSON.stringify(value,null,2);}else if(String(value).length>90){input=document.createElement('textarea');input.value=String(value);}else{input=document.createElement('input');input.type=typeof value==='number'?'number':'text';input.value=value??'';}input.id='ui_'+key;input.dataset.key=key;input.dataset.kind=typeof value;wrap.append(label,input);host.append(wrap);});}
  async function saveUiSettings(){try{const next={...uiConfig};$('uiFields').querySelectorAll('[data-key]').forEach(el=>{const key=el.dataset.key,kind=el.dataset.kind;let val;if(kind==='boolean')val=el.checked;else if(kind==='number')val=el.value===''?0:Number(el.value);else if(kind==='object'){try{val=JSON.parse(el.value);}catch{throw new Error('Invalid JSON in '+key);}}else val=el.value;next[key]=val;});await request(pathEndpoint('free_card'),{method:'PUT',body:JSON.stringify(next)});uiConfig=next;status($('uiStatus'),'UI settings saved to /free_card.','ok');}catch(e){status($('uiStatus'),e.message,'err');}}
  async function refreshEverything(){await loadRecords();renderLoginInfo();renderBanList();renderUiFields();}

  // Keep the dashboard synced with the newest Firebase values while connected.
  let liveSyncRunning = false;
  async function syncLatestFromFirebase(){
    if(!baseUrl || liveSyncRunning || busy) return;
    liveSyncRunning = true;
    try {
      // /keys is required; optional sections must not break key syncing
      // if their Firebase rules do not grant read access.
      const keyData = await request(endpoint());
      records = keyData && typeof keyData === 'object' ? keyData : {};
      try {
        const banData = await request(bannedEndpoint());
        bannedDevices = banData && typeof banData === 'object' ? banData : {};
      } catch(e) { /* Keep last known ban-list data if access is denied. */ }
      try {
        const uiData = await request(pathEndpoint('free_card'));
        uiConfig = uiData && typeof uiData === 'object' ? uiData : {};
      } catch(e) { /* Keep last known UI settings if access is denied. */ }
      render();
      if($('activeKeysPanel').classList.contains('current')) renderActiveKeys();
      if($('loginPanel').classList.contains('current')) renderLoginInfo();
      if($('banPanel').classList.contains('current')) renderBanList();
      // Do not rebuild UI inputs during polling; that could erase text being edited.
      $('dbLabel').textContent = baseUrl.replace(/^https:\/\//,'') + '  •  Live Firebase sync';
    } catch(e) {
      if(baseUrl) status(dataStatus, 'Live sync paused: ' + e.message, 'err');
    } finally { liveSyncRunning = false; }
  }
  setInterval(syncLatestFromFirebase, 3000);

  $('connectBtn').addEventListener('click', async()=>{
    clearStatus(connectStatus);
    try {
      baseUrl=cleanBase($('dbUrl').value);
      try{localStorage.setItem('xiter_firebase_url',baseUrl);}catch{}
      authToken=$('token').value.trim();
      const connected=await loadRecords();
      if(connected) status(connectStatus,'Connected. You can manage your /keys records below.','ok');
    } catch(e) { status(connectStatus,e.message,'err'); }
  });
  $('addBtn').addEventListener('click',()=>openEditor());
  $('activeAddBtn').addEventListener('click',()=>openEditor());
  $('bulkBtn').addEventListener('click',()=>openEditor());
  $('banBtn').addEventListener('click',banHwid);
  $('expiredBtn').addEventListener('click',deleteExpired);
  $('saveBtn').addEventListener('click',saveRecord);
  $('cancelBtn').addEventListener('click',closeEditor);
  $('refreshBtn').addEventListener('click',loadRecords);
  $('disconnectBtn').addEventListener('click',()=>{baseUrl='';authToken='';try{localStorage.removeItem('xiter_firebase_url');}catch{}records={};$('token').value='';$('homePanel').classList.add('hidden');$('activeKeysPanel').classList.remove('current');['loginPanel','banPanel','firebasePanel','uiPanel'].forEach(id=>$(id).classList.remove('current'));$('connectPanel').classList.remove('hidden');clearStatus(connectStatus);status(connectStatus,'Disconnected.','info');});
  $('search').addEventListener('input',render);
  document.querySelectorAll('.status-tab').forEach(tab=>tab.addEventListener('click',()=>{
    activeFilter=tab.dataset.filter;
    document.querySelectorAll('.status-tab').forEach(t=>t.classList.toggle('active',t===tab));
    render();
  }));
  $('menuTrigger').addEventListener('click',openDrawer);$('drawerClose').addEventListener('click',closeDrawer);$('drawerShade').addEventListener('click',closeDrawer);
  document.querySelectorAll('.nav-item').forEach(b=>b.addEventListener('click',()=>showView(b.dataset.view)));
  $('saveBanBtn').addEventListener('click',saveBanRecord);$('uploadBanJsonBtn').addEventListener('click',uploadBanJson);$('banRefresh').addEventListener('click',async()=>{try{bannedDevices=await request(bannedEndpoint())||{};renderBanList();status($('banStatus'),'Ban list refreshed.','ok');}catch(e){status($('banStatus'),e.message,'err');}});
  $('loginRefresh').addEventListener('click',async()=>{await loadRecords();renderLoginInfo();});
  $('uiRefreshBtn').addEventListener('click',async()=>{try{uiConfig=await request(pathEndpoint('free_card'))||{};renderUiFields();status($('uiStatus'),'UI settings loaded.','ok');}catch(e){status($('uiStatus'),e.message,'err');}});$('saveUiBtn').addEventListener('click',saveUiSettings);
  $('firebaseConnectBtn').addEventListener('click',async()=>{try{baseUrl=cleanBase($('dbUrlMirror').value||$('dbUrl').value);try{localStorage.setItem('xiter_firebase_url',baseUrl);}catch{}authToken=$('tokenMirror').value.trim();$('dbUrl').value=baseUrl;$('token').value=authToken;const connected=await loadRecords();if(connected)status($('firebaseStatus'),'Firebase connected / updated.','ok');else status($('firebaseStatus'),'Connection failed. See the error in Firebase Info / connection panel.','err');}catch(e){status($('firebaseStatus'),e.message,'err');}});
  $('firebaseDisconnectBtn').addEventListener('click',()=>{$('disconnectBtn').click();status($('firebaseStatus'),'Disconnected.','info');});
  $('editor').addEventListener('click',e=>{if(e.target===$('editor'))closeEditor();});
  document.addEventListener('keydown',e=>{if(e.key==='Escape')closeEditor();});

  // Remember the database URL locally and reconnect automatically on the next launch.
  (async()=>{
    let savedUrl='';
    try{savedUrl=localStorage.getItem('xiter_firebase_url')||'';}catch{}
    if(!savedUrl)return;
    $('dbUrl').value=savedUrl;
    status(connectStatus,'Connecting to Firebase…','info');
    try{
      baseUrl=cleanBase(savedUrl);
      authToken=''; // Auth tokens are intentionally not persisted in browser storage.
      const connected=await loadRecords();
      if(connected)status(connectStatus,'Connected to Firebase automatically.','ok');
      else status(connectStatus,'Auto-connect failed. Check Firebase rules or enter the required auth token.','err');
    }catch(e){status(connectStatus,'Auto-connect failed: '+e.message,'err');}
  })();
})();
</script>
</body>
</html>
