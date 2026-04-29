<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
<meta name="apple-mobile-web-app-title" content="Gastos 🏠">
<title>Gastos en pareja</title>
<link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@300;400;500;600&family=DM+Serif+Display&display=swap" rel="stylesheet">

<!-- Firebase -->
<script src="https://www.gstatic.com/firebasejs/9.22.2/firebase-app-compat.js"></script>
<script src="https://www.gstatic.com/firebasejs/9.22.2/firebase-firestore-compat.js"></script>

<style>
  :root {
    --bg: #0f0f13;
    --surface: #1a1a22;
    --surface2: #22222e;
    --border: #2e2e3e;
    --text: #f0efe8;
    --muted: #7a7a8e;
    --accent1: #e8a87c;
    --accent2: #7c9fe8;
    --green: #7ce8a0;
    --red: #e87c7c;
    --fijo-color: #e8a87c;
    --var-color: #7c9fe8;
    --radius: 16px;
    --font: 'DM Sans', sans-serif;
    --serif: 'DM Serif Display', serif;
  }

  * { box-sizing: border-box; margin: 0; padding: 0; }

  body {
    font-family: var(--font);
    background: var(--bg);
    color: var(--text);
    min-height: 100vh;
    padding: env(safe-area-inset-top) 0 env(safe-area-inset-bottom);
  }

  /* Header */
  .header {
    padding: 28px 20px 16px;
    text-align: center;
    border-bottom: 1px solid var(--border);
    position: sticky;
    top: 0;
    background: var(--bg);
    z-index: 10;
  }

  .header h1 {
    font-family: var(--serif);
    font-size: 26px;
    letter-spacing: -0.5px;
    color: var(--text);
    margin-bottom: 4px;
  }

  .header p {
    font-size: 13px;
    color: var(--muted);
  }

  /* Porcentaje config */
  .pct-bar {
    display: flex;
    align-items: center;
    gap: 10px;
    padding: 12px 20px;
    background: var(--surface);
    border-bottom: 1px solid var(--border);
  }

  .pct-bar label { font-size: 12px; color: var(--muted); white-space: nowrap; }

  .pct-bar input[type=range] {
    flex: 1;
    accent-color: var(--accent1);
    height: 4px;
  }

  .pct-badge {
    font-size: 12px;
    font-weight: 600;
    padding: 3px 8px;
    border-radius: 20px;
    white-space: nowrap;
  }

  .pct-vos { background: rgba(232,168,124,0.15); color: var(--accent1); }
  .pct-ella { background: rgba(124,159,232,0.15); color: var(--accent2); }

  /* Tabs */
  .tabs {
    display: flex;
    gap: 0;
    padding: 16px 20px 0;
  }

  .tab {
    flex: 1;
    padding: 10px 0;
    font-size: 14px;
    font-weight: 500;
    text-align: center;
    border: none;
    background: transparent;
    color: var(--muted);
    cursor: pointer;
    border-bottom: 2px solid transparent;
    transition: all 0.2s;
  }

  .tab.active-fijo { color: var(--fijo-color); border-color: var(--fijo-color); }
  .tab.active-var  { color: var(--var-color);  border-color: var(--var-color); }

  /* Secciones */
  .section { padding: 16px 20px; display: none; }
  .section.active { display: block; }

  /* Formulario agregar */
  .form-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: var(--radius);
    padding: 16px;
    margin-bottom: 16px;
  }

  .form-title {
    font-size: 13px;
    font-weight: 600;
    color: var(--muted);
    text-transform: uppercase;
    letter-spacing: 0.8px;
    margin-bottom: 12px;
  }

  .form-row {
    display: flex;
    gap: 8px;
    margin-bottom: 8px;
  }

  input[type=text], input[type=number], select {
    background: var(--surface2);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 10px 12px;
    font-family: var(--font);
    font-size: 14px;
    color: var(--text);
    outline: none;
    transition: border-color 0.2s;
    width: 100%;
  }

  input:focus, select:focus { border-color: var(--accent1); }

  select option { background: var(--surface2); }

  .btn-add {
    width: 100%;
    padding: 12px;
    border: none;
    border-radius: 10px;
    font-family: var(--font);
    font-size: 14px;
    font-weight: 600;
    cursor: pointer;
    margin-top: 4px;
    transition: opacity 0.2s;
  }

  .btn-add:active { opacity: 0.75; }
  .btn-fijo { background: var(--fijo-color); color: #1a1009; }
  .btn-var  { background: var(--var-color);  color: #0e1526; }

  /* Balance card */
  .balance-card {
    border-radius: var(--radius);
    padding: 16px;
    margin-bottom: 16px;
    border: 1px solid var(--border);
  }

  .balance-fijo { background: rgba(232,168,124,0.07); border-color: rgba(232,168,124,0.25); }
  .balance-var  { background: rgba(124,159,232,0.07); border-color: rgba(124,159,232,0.25); }

  .balance-title {
    font-size: 12px;
    font-weight: 600;
    text-transform: uppercase;
    letter-spacing: 0.8px;
    margin-bottom: 12px;
    color: var(--muted);
  }

  .balance-row {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 8px 0;
    border-bottom: 1px solid var(--border);
  }

  .balance-row:last-child { border: none; }

  .balance-name { font-size: 14px; font-weight: 500; }
  .balance-amount { font-family: var(--serif); font-size: 20px; }

  .balance-name.vos { color: var(--accent1); }
  .balance-name.ella { color: var(--accent2); }
  .balance-amount.vos { color: var(--accent1); }
  .balance-amount.ella { color: var(--accent2); }

  .deuda-box {
    margin-top: 10px;
    padding: 10px 12px;
    border-radius: 10px;
    font-size: 13px;
    font-weight: 500;
    text-align: center;
  }

  .deuda-ok  { background: rgba(124,232,160,0.12); color: var(--green); }
  .deuda-vos { background: rgba(232,124,124,0.12); color: var(--red); }
  .deuda-ella{ background: rgba(124,232,160,0.12); color: var(--green); }

  /* Lista items */
  .list-title {
    font-size: 13px;
    font-weight: 600;
    color: var(--muted);
    text-transform: uppercase;
    letter-spacing: 0.8px;
    margin-bottom: 10px;
  }

  .item-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 12px 14px;
    margin-bottom: 8px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    animation: fadeIn 0.3s ease;
  }

  @keyframes fadeIn { from { opacity:0; transform:translateY(6px); } to { opacity:1; transform:none; } }

  .item-left { flex: 1; }
  .item-nombre { font-size: 14px; font-weight: 500; margin-bottom: 2px; }
  .item-meta { font-size: 12px; color: var(--muted); }

  .item-right { display: flex; align-items: center; gap: 10px; }
  .item-monto { font-family: var(--serif); font-size: 18px; }
  .item-monto.vos  { color: var(--accent1); }
  .item-monto.ella { color: var(--accent2); }

  .btn-del {
    background: none;
    border: none;
    color: var(--muted);
    cursor: pointer;
    font-size: 16px;
    padding: 2px 4px;
    border-radius: 6px;
    line-height: 1;
    transition: color 0.2s;
  }
  .btn-del:hover { color: var(--red); }

  /* Fijo específico: split visual */
  .split-row {
    display: flex;
    gap: 6px;
    margin-top: 4px;
  }

  .split-pill {
    font-size: 11px;
    padding: 2px 8px;
    border-radius: 20px;
    font-weight: 500;
  }

  .split-pill.vos  { background: rgba(232,168,124,0.15); color: var(--accent1); }
  .split-pill.ella { background: rgba(124,159,232,0.15); color: var(--accent2); }

  /* Estado de conexión */
  .status-dot {
    display: inline-block;
    width: 7px; height: 7px;
    border-radius: 50%;
    margin-right: 5px;
    background: var(--green);
  }

  .empty-state {
    text-align: center;
    padding: 32px 0;
    color: var(--muted);
    font-size: 14px;
  }

  .empty-state span { display: block; font-size: 28px; margin-bottom: 8px; }

  /* Mes selector */
  .mes-row {
    display: flex;
    align-items: center;
    gap: 8px;
    margin-bottom: 14px;
  }

  .mes-row select { flex: 1; }
  .mes-row label { font-size: 13px; color: var(--muted); white-space: nowrap; }

  /* Config overlay */
  .config-overlay {
    display: none;
    position: fixed;
    inset: 0;
    background: rgba(0,0,0,0.7);
    z-index: 100;
    align-items: flex-end;
  }

  .config-overlay.open { display: flex; }

  .config-sheet {
    background: var(--surface);
    border-radius: 24px 24px 0 0;
    padding: 24px 20px 40px;
    width: 100%;
    border-top: 1px solid var(--border);
  }

  .config-sheet h3 { font-family: var(--serif); font-size: 22px; margin-bottom: 16px; }

  .config-sheet label { font-size: 13px; color: var(--muted); display: block; margin-bottom: 6px; margin-top: 14px; }

  .btn-config {
    position: fixed;
    bottom: calc(24px + env(safe-area-inset-bottom));
    right: 20px;
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 50%;
    width: 44px; height: 44px;
    font-size: 20px;
    cursor: pointer;
    display: flex;
    align-items: center;
    justify-content: center;
    z-index: 50;
    box-shadow: 0 4px 20px rgba(0,0,0,0.4);
  }

  .btn-guardar-config {
    width: 100%;
    padding: 13px;
    border: none;
    border-radius: 12px;
    background: var(--accent1);
    color: #1a1009;
    font-family: var(--font);
    font-size: 15px;
    font-weight: 600;
    cursor: pointer;
    margin-top: 20px;
  }

  .no-firebase {
    background: rgba(232,124,124,0.1);
    border: 1px solid rgba(232,124,124,0.3);
    border-radius: 12px;
    padding: 14px;
    font-size: 13px;
    color: var(--red);
    margin: 16px 20px;
    line-height: 1.6;
  }
</style>
</head>
<body>

<!-- Header -->
<div class="header">
  <h1>🏠 Gastos en pareja</h1>
  <p><span class="status-dot" id="statusDot"></span><span id="statusText">Conectando...</span></p>
</div>

<!-- Aviso si no hay Firebase -->
<div class="no-firebase" id="noFirebaseMsg" style="display:none">
  ⚠️ Todavía no está configurado Firebase. Los datos no se guardarán entre sesiones. Seguí las instrucciones que te dio Claude para configurarlo.
</div>

<!-- Porcentaje -->
<div class="pct-bar">
  <label>División:</label>
  <input type="range" id="pctSlider" min="10" max="90" value="60" oninput="actualizarPct(this.value)">
  <span class="pct-badge pct-vos" id="badgeVos">Vos 60%</span>
  <span class="pct-badge pct-ella" id="badgeElla">Ella 40%</span>
</div>

<!-- Tabs -->
<div class="tabs">
  <button class="tab active-fijo" onclick="cambiarTab('fijos')" id="tabFijos">🏠 Gastos fijos</button>
  <button class="tab" onclick="cambiarTab('variables')" id="tabVars">🛒 Variables</button>
</div>

<!-- ===== SECCIÓN FIJOS ===== -->
<div class="section active" id="secFijos">

  <div class="form-card">
    <div class="form-title">Agregar gasto fijo</div>
    <div class="form-row">
      <input type="text" id="fijoNombre" placeholder="Nombre (ej: Alquiler)">
    </div>
    <div class="form-row">
      <input type="number" id="fijoMonto" placeholder="Monto total $" inputmode="decimal">
    </div>
    <button class="btn-add btn-fijo" onclick="agregarFijo()">+ Agregar gasto fijo</button>
  </div>

  <!-- Balance fijos -->
  <div class="balance-card balance-fijo" id="balanceFijos">
    <div class="balance-title">Balance — Gastos fijos</div>
    <div class="balance-row">
      <span class="balance-name vos">Vos</span>
      <span class="balance-amount vos" id="totalFijoVos">$0</span>
    </div>
    <div class="balance-row">
      <span class="balance-name ella">Ella</span>
      <span class="balance-amount ella" id="totalFijoElla">$0</span>
    </div>
    <div class="deuda-box deuda-ok" id="deudaFijos">Sin gastos aún</div>
  </div>

  <div class="list-title">Gastos del mes</div>
  <div id="listaFijos"><div class="empty-state"><span>🏠</span>Todavía no hay gastos fijos</div></div>
</div>

<!-- ===== SECCIÓN VARIABLES ===== -->
<div class="section" id="secVars">

  <div class="form-card">
    <div class="form-title">Agregar gasto variable</div>
    <div class="form-row">
      <input type="text" id="varNombre" placeholder="¿Qué compraron? (ej: Super)">
    </div>
    <div class="form-row">
      <input type="number" id="varMonto" placeholder="Monto $" inputmode="decimal" style="flex:1">
      <select id="varQuien" style="flex:0.8">
        <option value="vos">Vos</option>
        <option value="ella">Ella</option>
      </select>
    </div>
    <button class="btn-add btn-var" onclick="agregarVariable()">+ Agregar gasto variable</button>
  </div>

  <!-- Balance variables -->
  <div class="balance-card balance-var" id="balanceVars">
    <div class="balance-title">Balance — Gastos variables</div>
    <div class="balance-row">
      <span class="balance-name vos">Vos</span>
      <span class="balance-amount vos" id="totalVarVos">$0</span>
    </div>
    <div class="balance-row">
      <span class="balance-name ella">Ella</span>
      <span class="balance-amount ella" id="totalVarElla">$0</span>
    </div>
    <div class="deuda-box deuda-ok" id="deudaVars">Sin gastos aún</div>
  </div>

  <div class="list-title">Historial del mes</div>
  <div id="listaVars"><div class="empty-state"><span>🛒</span>Todavía no hay gastos variables</div></div>
</div>

<!-- Botón config -->
<button class="btn-config" onclick="abrirConfig()">⚙️</button>

<!-- Config sheet -->
<div class="config-overlay" id="configOverlay" onclick="cerrarConfig(event)">
  <div class="config-sheet">
    <h3>Configuración</h3>
    <label>Tu nombre</label>
    <input type="text" id="cfgNombreVos" placeholder="Tu nombre">
    <label>Nombre de ella</label>
    <input type="text" id="cfgNombreElla" placeholder="Nombre de tu novia">
    <button class="btn-guardar-config" onclick="guardarConfig()">Guardar</button>
    <p style="font-size:12px;color:var(--muted);margin-top:14px;text-align:center">Los datos se sincronizan automáticamente 🔄</p>
  </div>
</div>

<script>
// ============================================================
// FIREBASE CONFIG — REEMPLAZÁ ESTOS VALORES CON LOS TUYOS
// ============================================================
const firebaseConfig = {
  apiKey: "AIzaSyAkl86S-gfcmCR0-jaLBhZg4McNeC0RAss",
  authDomain: "gastos-pareja-5c18c.firebaseapp.com",
  projectId: "gastos-pareja-5c18c",
  storageBucket: "gastos-pareja-5c18c.firebasestorage.app",
  messagingSenderId: "600607581181",
  appId: "1:600607581181:web:11e884f974dae56cd3ef94"
};
// ============================================================

let db = null;
let firebaseOk = false;

// Inicializar Firebase
try {
  firebase.initializeApp(firebaseConfig);
  db = firebase.firestore();
  firebaseOk = true;
} catch(e) {
  console.warn("Firebase no configurado:", e);
}

// Estado local
let fijos = [];
let variables = [];
let pctVos = 60;
let nombreVos = "Vos";
let nombreElla = "Ella";

// Mes actual como ID de documento
const mesId = () => {
  const d = new Date();
  return `${d.getFullYear()}-${String(d.getMonth()+1).padStart(2,'0')}`;
};

// Formatear $
const fmt = n => '$' + Number(n).toLocaleString('es-AR');

// ======== FIREBASE ========
async function cargarDatos() {
  if (!firebaseOk || firebaseConfig.apiKey === "TU_API_KEY") {
    document.getElementById('noFirebaseMsg').style.display = 'block';
    document.getElementById('statusDot').style.background = '#e87c7c';
    document.getElementById('statusText').textContent = 'Sin conexión';
    return;
  }

  document.getElementById('statusDot').style.background = '#e8c87c';
  document.getElementById('statusText').textContent = 'Conectando...';

  try {
    // Config
    const cfgDoc = await db.collection('config').doc('general').get();
    if (cfgDoc.exists) {
      const cfg = cfgDoc.data();
      pctVos = cfg.pctVos || 60;
      nombreVos = cfg.nombreVos || 'Vos';
      nombreElla = cfg.nombreElla || 'Ella';
      document.getElementById('pctSlider').value = pctVos;
      actualizarPct(pctVos, false);
    }

    // Escuchar fijos en tiempo real
    db.collection('gastos').doc(mesId()).collection('fijos')
      .orderBy('fecha', 'desc')
      .onSnapshot(snap => {
        fijos = snap.docs.map(d => ({ id: d.id, ...d.data() }));
        renderFijos();
      });

    // Escuchar variables en tiempo real
    db.collection('gastos').doc(mesId()).collection('variables')
      .orderBy('fecha', 'desc')
      .onSnapshot(snap => {
        variables = snap.docs.map(d => ({ id: d.id, ...d.data() }));
        renderVars();
      });

    document.getElementById('statusDot').style.background = '#7ce8a0';
    document.getElementById('statusText').textContent = 'Sincronizado';
  } catch(e) {
    document.getElementById('statusDot').style.background = '#e87c7c';
    document.getElementById('statusText').textContent = 'Error de conexión';
    console.error(e);
  }
}

async function guardarFijo(item) {
  if (!firebaseOk || firebaseConfig.apiKey === "TU_API_KEY") return;
  await db.collection('gastos').doc(mesId()).collection('fijos').add(item);
}

async function guardarVariable(item) {
  if (!firebaseOk || firebaseConfig.apiKey === "TU_API_KEY") return;
  await db.collection('gastos').doc(mesId()).collection('variables').add(item);
}

async function borrarFijo(id) {
  if (!firebaseOk || firebaseConfig.apiKey === "TU_API_KEY") {
    fijos = fijos.filter(f => f.id !== id);
    renderFijos();
    return;
  }
  await db.collection('gastos').doc(mesId()).collection('fijos').doc(id).delete();
}

async function borrarVariable(id) {
  if (!firebaseOk || firebaseConfig.apiKey === "TU_API_KEY") {
    variables = variables.filter(v => v.id !== id);
    renderVars();
    return;
  }
  await db.collection('gastos').doc(mesId()).collection('variables').doc(id).delete();
}

async function guardarConfigFirebase() {
  if (!firebaseOk || firebaseConfig.apiKey === "TU_API_KEY") return;
  await db.collection('config').doc('general').set({ pctVos, nombreVos, nombreElla });
}

// ======== UI ========
function actualizarPct(val, guardar = true) {
  pctVos = parseInt(val);
  const pctElla = 100 - pctVos;
  document.getElementById('badgeVos').textContent = `${nombreVos} ${pctVos}%`;
  document.getElementById('badgeElla').textContent = `${nombreElla} ${pctElla}%`;
  renderFijos();
  if (guardar) guardarConfigFirebase();
}

function cambiarTab(tab) {
  document.getElementById('secFijos').classList.remove('active');
  document.getElementById('secVars').classList.remove('active');
  document.getElementById('tabFijos').className = 'tab';
  document.getElementById('tabVars').className = 'tab';

  if (tab === 'fijos') {
    document.getElementById('secFijos').classList.add('active');
    document.getElementById('tabFijos').className = 'tab active-fijo';
  } else {
    document.getElementById('secVars').classList.add('active');
    document.getElementById('tabVars').className = 'tab active-var';
  }
}

function agregarFijo() {
  const nombre = document.getElementById('fijoNombre').value.trim();
  const monto = parseFloat(document.getElementById('fijoMonto').value);
  if (!nombre || !monto || monto <= 0) { alert('Completá nombre y monto'); return; }

  const item = { nombre, monto, fecha: new Date().toISOString() };

  if (!firebaseOk || firebaseConfig.apiKey === "TU_API_KEY") {
    item.id = Date.now().toString();
    fijos.unshift(item);
    renderFijos();
  } else {
    guardarFijo(item);
  }

  document.getElementById('fijoNombre').value = '';
  document.getElementById('fijoMonto').value = '';
}

function agregarVariable() {
  const nombre = document.getElementById('varNombre').value.trim();
  const monto = parseFloat(document.getElementById('varMonto').value);
  const quien = document.getElementById('varQuien').value;
  if (!nombre || !monto || monto <= 0) { alert('Completá nombre y monto'); return; }

  const item = { nombre, monto, quien, fecha: new Date().toISOString() };

  if (!firebaseOk || firebaseConfig.apiKey === "TU_API_KEY") {
    item.id = Date.now().toString();
    variables.unshift(item);
    renderVars();
  } else {
    guardarVariable(item);
  }

  document.getElementById('varNombre').value = '';
  document.getElementById('varMonto').value = '';
}

function renderFijos() {
  const pctElla = 100 - pctVos;
  let totalVos = 0, totalElla = 0;

  const lista = document.getElementById('listaFijos');
  if (fijos.length === 0) {
    lista.innerHTML = '<div class="empty-state"><span>🏠</span>Todavía no hay gastos fijos</div>';
    document.getElementById('totalFijoVos').textContent = '$0';
    document.getElementById('totalFijoElla').textContent = '$0';
    document.getElementById('deudaFijos').textContent = 'Sin gastos aún';
    document.getElementById('deudaFijos').className = 'deuda-box deuda-ok';
    return;
  }

  lista.innerHTML = fijos.map(f => {
    const pV = (f.monto * pctVos / 100);
    const pE = (f.monto * pctElla / 100);
    totalVos += pV;
    totalElla += pE;
    const fecha = new Date(f.fecha).toLocaleDateString('es-AR', { day:'numeric', month:'short' });
    return `
      <div class="item-card">
        <div class="item-left">
          <div class="item-nombre">${f.nombre}</div>
          <div class="item-meta">${fecha} · Total: ${fmt(f.monto)}</div>
          <div class="split-row">
            <span class="split-pill vos">${nombreVos}: ${fmt(pV)}</span>
            <span class="split-pill ella">${nombreElla}: ${fmt(pE)}</span>
          </div>
        </div>
        <div class="item-right">
          <button class="btn-del" onclick="borrarFijo('${f.id}')">✕</button>
        </div>
      </div>`;
  }).join('');

  document.getElementById('totalFijoVos').textContent = fmt(totalVos);
  document.getElementById('totalFijoElla').textContent = fmt(totalElla);
  renderDeuda('deudaFijos', totalVos, totalElla);
}

function renderVars() {
  let totalVos = 0, totalElla = 0;

  const lista = document.getElementById('listaVars');
  if (variables.length === 0) {
    lista.innerHTML = '<div class="empty-state"><span>🛒</span>Todavía no hay gastos variables</div>';
    document.getElementById('totalVarVos').textContent = '$0';
    document.getElementById('totalVarElla').textContent = '$0';
    document.getElementById('deudaVars').textContent = 'Sin gastos aún';
    document.getElementById('deudaVars').className = 'deuda-box deuda-ok';
    return;
  }

  lista.innerHTML = variables.map(v => {
    if (v.quien === 'vos') totalVos += v.monto;
    else totalElla += v.monto;
    const fecha = new Date(v.fecha).toLocaleDateString('es-AR', { day:'numeric', month:'short' });
    const cls = v.quien === 'vos' ? 'vos' : 'ella';
    const nomQ = v.quien === 'vos' ? nombreVos : nombreElla;
    return `
      <div class="item-card">
        <div class="item-left">
          <div class="item-nombre">${v.nombre}</div>
          <div class="item-meta">${fecha} · Pagó: ${nomQ}</div>
        </div>
        <div class="item-right">
          <span class="item-monto ${cls}">${fmt(v.monto)}</span>
          <button class="btn-del" onclick="borrarVariable('${v.id}')">✕</button>
        </div>
      </div>`;
  }).join('');

  document.getElementById('totalVarVos').textContent = fmt(totalVos);
  document.getElementById('totalVarElla').textContent = fmt(totalElla);
  renderDeuda('deudaVars', totalVos, totalElla);
}

function renderDeuda(elId, totalVos, totalElla) {
  const el = document.getElementById(elId);
  const diff = totalVos - totalElla;
  if (Math.abs(diff) < 1) {
    el.textContent = '✓ Están iguales';
    el.className = 'deuda-box deuda-ok';
  } else if (diff > 0) {
    el.textContent = `${nombreElla} le debe ${fmt(diff)} a ${nombreVos}`;
    el.className = 'deuda-box deuda-ella';
  } else {
    el.textContent = `${nombreVos} le debe ${fmt(Math.abs(diff))} a ${nombreElla}`;
    el.className = 'deuda-box deuda-vos';
  }
}

function abrirConfig() {
  document.getElementById('cfgNombreVos').value = nombreVos !== 'Vos' ? nombreVos : '';
  document.getElementById('cfgNombreElla').value = nombreElla !== 'Ella' ? nombreElla : '';
  document.getElementById('configOverlay').classList.add('open');
}

function cerrarConfig(e) {
  if (e.target === document.getElementById('configOverlay'))
    document.getElementById('configOverlay').classList.remove('open');
}

function guardarConfig() {
  const nv = document.getElementById('cfgNombreVos').value.trim();
  const ne = document.getElementById('cfgNombreElla').value.trim();
  if (nv) nombreVos = nv;
  if (ne) nombreElla = ne;
  actualizarPct(pctVos);
  renderFijos();
  renderVars();
  guardarConfigFirebase();
  document.getElementById('configOverlay').classList.remove('open');
}

// Arrancar
cargarDatos();
</script>
</body>
</html>
