<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Pos Tugas Kelas XJ</title>
<style>
@import url('https://fonts.googleapis.com/css2?family=Special+Elite&family=IBM+Plex+Sans:wght@400;500;600;700&family=IBM+Plex+Mono:wght@400;500;600&display=swap');

:root{
  --paper:#EFEADD;
  --paper-card:#F7F3E8;
  --paper-dark:#E2DBC4;
  --ink:#22252B;
  --navy:#2B3A55;
  --navy-dark:#1D2840;
  --stamp:#B23A2F;
  --mustard:#C68A2E;
  --line:#B9AF93;
  --muted:#6B6555;
  --font-display:'Special Elite','Courier New',monospace;
  --font-body:'IBM Plex Sans',-apple-system,sans-serif;
  --font-mono:'IBM Plex Mono','Courier New',monospace;
}

*{box-sizing:border-box;}
html,body{margin:0;padding:0;background:var(--paper);color:var(--ink);font-family:var(--font-body);}
body{min-height:100vh;padding:28px 16px 60px;}

.wrap{max-width:600px;margin:0 auto;}

.masthead{text-align:center;margin-bottom:22px;}
.masthead .icon{font-size:30px;display:block;margin-bottom:6px;}
.masthead h1{font-family:var(--font-display);font-size:26px;letter-spacing:1px;margin:0 0 6px;color:var(--navy-dark);}
.masthead p{margin:0;color:var(--muted);font-size:14px;line-height:1.5;}

.tabs{display:flex;gap:4px;margin-top:20px;padding-left:8px;flex-wrap:wrap;}
.tab-btn{
  font-family:var(--font-mono);font-size:13px;font-weight:600;letter-spacing:.3px;
  padding:10px 14px 12px;border:none;border-radius:8px 8px 0 0;
  background:var(--paper-dark);color:var(--muted);cursor:pointer;position:relative;top:2px;
  transition:background .15s,color .15s;
}
.tab-btn.active{background:var(--paper-card);color:var(--navy-dark);box-shadow:0 -2px 0 var(--mustard) inset;}
.tab-btn:not(.active):hover{background:#DAD2B6;}

.card-stack{position:relative;}
.card-stack::before,.card-stack::after{
  content:"";position:absolute;left:8px;right:8px;height:100%;
  background:var(--paper-dark);border-radius:4px;z-index:0;
}
.card-stack::before{top:6px;transform:rotate(-1.1deg);}
.card-stack::after{top:3px;transform:rotate(0.8deg);}

.card{position:relative;z-index:1;background:var(--paper-card);border-radius:4px;padding:28px 24px 26px;box-shadow:0 6px 18px rgba(34,37,43,.12);}

.field{margin-bottom:22px;}
.field label{display:block;font-family:var(--font-mono);font-size:12px;text-transform:uppercase;letter-spacing:.8px;color:var(--muted);margin-bottom:6px;}
.field input[type=text],.field input[type=password]{
  width:100%;border:none;border-bottom:2px solid var(--line);background:transparent;
  font-family:var(--font-mono);font-size:16px;padding:6px 2px 8px;color:var(--ink);outline:none;
  transition:border-color .15s;
}
.field input:focus{border-color:var(--navy);}
.field input::placeholder{color:#A79F87;}

.row2{display:flex;gap:20px;}
.row2 .field{flex:1;}

.dropzone{
  border:2px dashed var(--line);border-radius:6px;padding:20px 14px;text-align:center;cursor:pointer;
  transition:border-color .15s,background .15s;font-family:var(--font-mono);font-size:13.5px;color:var(--muted);
}
.dropzone:hover{border-color:var(--navy);background:rgba(43,58,85,.04);}
.dropzone.has-file{border-style:solid;border-color:var(--navy);color:var(--navy-dark);}
.dropzone input{display:none;}
.dz-hint{display:block;margin-top:4px;font-size:11px;color:#A79F87;}

.err-msg{font-family:var(--font-mono);font-size:12.5px;color:var(--stamp);margin-top:-10px;margin-bottom:16px;min-height:16px;}

.submit-btn{
  width:100%;background:var(--navy-dark);color:#F5F1E4;border:none;border-radius:5px;padding:14px;
  font-family:var(--font-mono);font-size:14px;font-weight:600;letter-spacing:1px;text-transform:uppercase;cursor:pointer;
  transition:background .15s,transform .1s;
}
.submit-btn:hover{background:#233151;}
.submit-btn:active{transform:scale(.99);}
.submit-btn:disabled{background:#9A9384;cursor:not-allowed;}

.note{font-family:var(--font-mono);font-size:11.5px;color:var(--muted);text-align:center;margin-top:14px;}

.success-view{position:relative;z-index:1;background:var(--paper-card);border-radius:4px;padding:40px 24px;box-shadow:0 6px 18px rgba(34,37,43,.12);text-align:center;}
.stamp{display:inline-block;border:4px double var(--stamp);color:var(--stamp);font-family:var(--font-display);font-size:22px;letter-spacing:2px;padding:12px 22px;transform:rotate(-6deg) scale(.7);opacity:0;animation:stampIn .35s ease-out forwards;animation-delay:.05s;}
@keyframes stampIn{to{transform:rotate(-6deg) scale(1);opacity:1;}}
.receipt{font-family:var(--font-mono);font-size:13.5px;color:var(--muted);margin-top:22px;line-height:1.9;}
.receipt b{color:var(--ink);}
.again-btn{margin-top:24px;background:none;border:2px solid var(--navy-dark);color:var(--navy-dark);font-family:var(--font-mono);font-size:13px;font-weight:600;padding:10px 18px;border-radius:5px;cursor:pointer;}
.again-btn:hover{background:var(--navy-dark);color:#F5F1E4;}

.inbox-head{display:flex;align-items:center;justify-content:space-between;margin-bottom:14px;padding:0 2px;gap:8px;flex-wrap:wrap;}
.inbox-count{font-family:var(--font-mono);font-size:13px;color:var(--muted);}
.refresh-btn{background:none;border:1px solid var(--line);border-radius:5px;font-family:var(--font-mono);font-size:12px;color:var(--muted);padding:6px 10px;cursor:pointer;}
.refresh-btn:hover{border-color:var(--navy);color:var(--navy-dark);}

.search-field{margin-bottom:16px;}
.search-field input{width:100%;border:none;border-bottom:2px solid var(--line);background:transparent;font-family:var(--font-mono);font-size:14px;padding:8px 2px;outline:none;}
.search-field input:focus{border-color:var(--navy);}

.sub-list{display:flex;flex-direction:column;gap:10px;}
.sub-item{background:var(--paper-card);border-left:3px dashed var(--mustard);border-radius:0 4px 4px 0;padding:14px 16px;box-shadow:0 2px 6px rgba(34,37,43,.08);display:flex;justify-content:space-between;align-items:center;gap:12px;}
.sub-info .title{font-weight:600;font-size:14.5px;margin-bottom:3px;color:var(--ink);}
.sub-info .meta{font-family:var(--font-mono);font-size:12.5px;color:var(--muted);}
.sub-info .time{font-family:var(--font-mono);font-size:11px;color:#A79F87;margin-top:3px;}
.dup-badge{display:inline-block;font-family:var(--font-mono);font-size:10px;color:var(--stamp);border:1px solid var(--stamp);border-radius:3px;padding:1px 6px;margin-left:8px;vertical-align:middle;}
.btn-col{display:flex;flex-direction:column;gap:6px;flex-shrink:0;}
.dl-btn{background:none;border:1.5px solid var(--navy);color:var(--navy-dark);font-family:var(--font-mono);font-size:12px;font-weight:600;padding:8px 12px;border-radius:5px;cursor:pointer;white-space:nowrap;}
.dl-btn:hover{background:var(--navy);color:#F5F1E4;}
.pv-btn{background:none;border:1.5px solid var(--mustard);color:#7A5419;font-family:var(--font-mono);font-size:12px;font-weight:600;padding:8px 12px;border-radius:5px;cursor:pointer;white-space:nowrap;}
.pv-btn:hover{background:var(--mustard);color:#fff;}
.del-btn{background:none;border:1.5px solid var(--stamp);color:var(--stamp);font-family:var(--font-mono);font-size:12px;font-weight:600;padding:8px 12px;border-radius:5px;cursor:pointer;white-space:nowrap;}
.del-btn:hover{background:var(--stamp);color:#F5F1E4;}

.preview-overlay{position:fixed;inset:0;background:rgba(34,37,43,.55);display:none;align-items:center;justify-content:center;padding:20px;z-index:100;}
.preview-modal{background:var(--paper-card);border-radius:6px;max-width:640px;width:100%;max-height:85vh;display:flex;flex-direction:column;box-shadow:0 10px 30px rgba(0,0,0,.3);}
.preview-head{display:flex;justify-content:space-between;align-items:center;padding:14px 18px;border-bottom:1px dashed var(--line);gap:10px;}
.preview-head span{font-family:var(--font-mono);font-size:13px;font-weight:600;color:var(--ink);word-break:break-all;}
.preview-close{background:none;border:none;font-size:18px;color:var(--muted);cursor:pointer;line-height:1;padding:4px;flex-shrink:0;}
.preview-close:hover{color:var(--stamp);}
.preview-body{padding:18px;overflow:auto;flex:1;display:flex;align-items:center;justify-content:center;}
.preview-body img{max-width:100%;max-height:60vh;border-radius:4px;display:block;}
.pdf-frame{width:100%;height:65vh;border:1px solid var(--line);border-radius:4px;}
.text-preview{width:100%;white-space:pre-wrap;word-break:break-word;font-family:var(--font-mono);font-size:12.5px;color:var(--ink);text-align:left;margin:0;}
.preview-fallback{text-align:center;font-family:var(--font-mono);font-size:13px;color:var(--muted);line-height:1.7;}
.preview-actions{padding:14px 18px;border-top:1px dashed var(--line);text-align:right;}

.empty-state,.loading-state,.error-state{text-align:center;padding:40px 20px;color:var(--muted);font-family:var(--font-mono);font-size:13.5px;line-height:1.7;}
.error-state{color:var(--stamp);}

.privacy-note{font-family:var(--font-mono);font-size:11px;color:#A79F87;text-align:center;margin-top:18px;line-height:1.6;}

.lock-card{text-align:center;}
.lock-card .lock-icon{font-size:26px;display:block;margin-bottom:10px;}
.lock-card p{color:var(--muted);font-size:13.5px;line-height:1.6;margin-bottom:20px;}

.section-title{font-family:var(--font-mono);font-size:12px;text-transform:uppercase;letter-spacing:.8px;color:var(--muted);margin:24px 0 10px;}

.dup-group{background:#F3E9DC;border:1px dashed var(--stamp);border-radius:6px;padding:12px 14px;margin-bottom:14px;}
.dup-group-head{display:flex;justify-content:space-between;align-items:center;margin-bottom:8px;gap:8px;flex-wrap:wrap;}
.dup-group-head b{font-size:13.5px;}
.mini-btn{background:none;border:1px solid var(--navy);color:var(--navy-dark);font-family:var(--font-mono);font-size:11px;padding:5px 8px;border-radius:4px;cursor:pointer;}
.mini-btn:hover{background:var(--navy);color:#F5F1E4;}
.dup-entry{display:flex;justify-content:space-between;align-items:center;padding:6px 0;font-family:var(--font-mono);font-size:12px;color:var(--muted);border-top:1px dashed #D8CBA8;}
.dup-entry:first-child{border-top:none;}

.panel-head{display:flex;justify-content:space-between;align-items:center;margin-bottom:6px;}
.lock-again{background:none;border:none;color:var(--muted);font-family:var(--font-mono);font-size:11px;text-decoration:underline;cursor:pointer;padding:4px;}

@media (max-width:420px){
  .row2{flex-direction:column;gap:0;}
  .card,.success-view{padding:22px 16px 20px;}
  .sub-item{flex-direction:column;align-items:stretch;}
  .btn-col{flex-direction:row;}
}
</style>
</head>
<body>
<div class="wrap">

  <div class="masthead">
    <span class="icon">📮</span>
    <h1>POS TUGAS KELAS XJ</h1>
    <p>Kumpulkan tugas Kelas XJ dalam satu tempat.<br>Isi nama, kelas, nomor absen, lalu lampirkan file tugasmu.</p>
  </div>

  <div class="tabs">
    <button class="tab-btn active" id="tabSend">Kirim Tugas</button>
    <button class="tab-btn" id="tabInbox">Kotak Masuk <span id="inboxBadge"></span></button>
    <button class="tab-btn" id="tabManage">⚙ Kelola</button>
  </div>

  <!-- SEND VIEW -->
  <div id="sendView" class="card-stack">
    <div class="card" id="formCard">
      <div class="field">
        <label for="fNama">Nama</label>
        <input type="text" id="fNama" placeholder="nama lengkap">
      </div>
      <div class="row2">
        <div class="field">
          <label for="fKelas">Kelas</label>
          <input type="text" id="fKelas" placeholder="mis. 8B">
        </div>
        <div class="field">
          <label for="fAbsen">No. Absen</label>
          <input type="text" id="fAbsen" placeholder="mis. 07">
        </div>
      </div>
      <div class="field">
        <label for="fJudul">Nama Tugas / Mapel <span style="text-transform:none;letter-spacing:0;">(opsional)</span></label>
        <input type="text" id="fJudul" placeholder="mis. Matematika - Bab 3">
      </div>
      <div class="field">
        <label>File Tugas</label>
        <div class="dropzone" id="dropzone">
          <span id="dzText">📎 Ketuk untuk pilih file</span>
          <span class="dz-hint">Maks. 3MB per file</span>
          <input type="file" id="fFile">
        </div>
      </div>
      <div class="err-msg" id="errMsg"></div>
      <button class="submit-btn" id="submitBtn">Kirim Tugas →</button>
      <div class="note">File tersimpan otomatis begitu dikirim. Mengirim ulang tidak menimpa kiriman lama — keduanya tersimpan, dan bisa dirapikan lewat tab Kelola.</div>
    </div>
  </div>

  <!-- SUCCESS VIEW -->
  <div id="successView" class="success-view" style="display:none;">
    <div class="stamp">✓ DITERIMA</div>
    <div class="receipt" id="receiptText"></div>
    <button class="again-btn" id="againBtn">Kirim tugas lain →</button>
  </div>

  <!-- INBOX VIEW -->
  <div id="inboxView" style="display:none;">
    <div class="inbox-head">
      <span class="inbox-count" id="inboxCount">Memuat...</span>
      <button class="refresh-btn" id="refreshBtn">↻ Muat ulang</button>
    </div>
    <div class="search-field">
      <input type="text" id="searchInput" placeholder="Cari nama atau kelas...">
    </div>
    <div id="inboxList"></div>
    <div class="privacy-note">Siapa pun yang membuka link ini dapat melihat dan mengunduh semua tugas yang masuk. Hanya pengelola (tab Kelola) yang bisa menghapus kiriman.</div>
  </div>

  <!-- MANAGE VIEW -->
  <div id="manageView" style="display:none;">
    <div id="manageContent"></div>
  </div>

</div>

<!-- PREVIEW MODAL -->
<div class="preview-overlay" id="previewOverlay">
  <div class="preview-modal" id="previewModal">
    <div class="preview-head">
      <span id="previewTitle"></span>
      <button class="preview-close" id="previewClose">✕</button>
    </div>
    <div class="preview-body" id="previewBody"></div>
    <div class="preview-actions">
      <button class="dl-btn" id="previewDownloadBtn">Unduh</button>
    </div>
  </div>
</div>

<script>
const MAX_BYTES = 3 * 1024 * 1024;

const sendView = document.getElementById('sendView');
const successView = document.getElementById('successView');
const inboxView = document.getElementById('inboxView');
const manageView = document.getElementById('manageView');
const tabSend = document.getElementById('tabSend');
const tabInbox = document.getElementById('tabInbox');
const tabManage = document.getElementById('tabManage');
const dropzone = document.getElementById('dropzone');
const fileInput = document.getElementById('fFile');
const dzText = document.getElementById('dzText');
const errMsg = document.getElementById('errMsg');
const submitBtn = document.getElementById('submitBtn');
const inboxBadge = document.getElementById('inboxBadge');
const manageContent = document.getElementById('manageContent');

let selectedFile = null;
let submissionsCache = [];
let isAdmin = false;

function showView(name){
  sendView.style.display = name==='send' ? '' : 'none';
  successView.style.display = 'none';
  inboxView.style.display = name==='inbox' ? '' : 'none';
  manageView.style.display = name==='manage' ? '' : 'none';
  tabSend.classList.toggle('active', name==='send');
  tabInbox.classList.toggle('active', name==='inbox');
  tabManage.classList.toggle('active', name==='manage');
  if(name==='inbox') loadSubmissions();
  if(name==='manage') renderManageView();
}

tabSend.addEventListener('click', ()=>showView('send'));
tabInbox.addEventListener('click', ()=>showView('inbox'));
tabManage.addEventListener('click', ()=>showView('manage'));

dropzone.addEventListener('click', ()=>fileInput.click());
fileInput.addEventListener('change', ()=>{
  const f = fileInput.files[0];
  if(!f) return;
  if(f.size > MAX_BYTES){
    errMsg.textContent = 'File terlalu besar (maks 3MB). Pilih file lain.';
    fileInput.value = '';
    selectedFile = null;
    dropzone.classList.remove('has-file');
    dzText.textContent = '📎 Ketuk untuk pilih file';
    return;
  }
  errMsg.textContent = '';
  selectedFile = f;
  dropzone.classList.add('has-file');
  dzText.textContent = '✓ ' + f.name;
});

function fileToBase64(file){
  return new Promise((resolve, reject)=>{
    const reader = new FileReader();
    reader.onload = ()=> resolve(reader.result.split(',')[1]);
    reader.onerror = ()=> reject(new Error('Gagal membaca file'));
    reader.readAsDataURL(file);
  });
}

function randomId(){ return Date.now() + '_' + Math.random().toString(36).slice(2,8); }
function escapeHtml(s){ const d=document.createElement('div'); d.textContent=s; return d.innerHTML; }
function groupKey(s){ return (s.nama||'').trim().toLowerCase()+'|'+(s.kelas||'').trim().toLowerCase()+'|'+(s.absen||'').trim().toLowerCase(); }

function findDuplicateGroups(subs){
  const map = {};
  subs.forEach(s=>{ const k=groupKey(s); (map[k]=map[k]||[]).push(s); });
  return Object.values(map).filter(a=>a.length>1).map(a=>a.slice().sort((x,y)=>y.submittedAt-x.submittedAt));
}

submitBtn.addEventListener('click', async ()=>{
  const nama = document.getElementById('fNama').value.trim();
  const kelas = document.getElementById('fKelas').value.trim();
  const absen = document.getElementById('fAbsen').value.trim();
  const judul = document.getElementById('fJudul').value.trim();

  if(!nama || !kelas || !absen){ errMsg.textContent = 'Nama, kelas, dan nomor absen wajib diisi.'; return; }
  if(!selectedFile){ errMsg.textContent = 'Pilih file tugas terlebih dahulu.'; return; }

  errMsg.textContent = '';
  submitBtn.disabled = true;
  submitBtn.textContent = 'Mengirim...';

  try{
    const base64 = await fileToBase64(selectedFile);
    const id = randomId();
    const entry = {
      id, nama, kelas, absen, judul,
      fileName: selectedFile.name,
      fileType: selectedFile.type || 'application/octet-stream',
      fileSize: selectedFile.size,
      fileData: base64,
      submittedAt: Date.now()
    };
    const result = await window.storage.set('submission:' + id, JSON.stringify(entry), true);
    if(!result){ throw new Error('Penyimpanan gagal'); }

    const waktu = new Date(entry.submittedAt).toLocaleString('id-ID', {dateStyle:'medium', timeStyle:'short'});
    document.getElementById('receiptText').innerHTML =
      '<b>' + escapeHtml(nama) + '</b><br>' +
      'Kelas ' + escapeHtml(kelas) + ' &middot; No. Absen ' + escapeHtml(absen) + '<br>' +
      (judul ? escapeHtml(judul) + '<br>' : '') + waktu;

    sendView.style.display = 'none';
    successView.style.display = 'block';
    resetForm();
  }catch(e){
    errMsg.textContent = 'Gagal mengirim tugas. Periksa koneksi lalu coba lagi.';
  }finally{
    submitBtn.disabled = false;
    submitBtn.textContent = 'Kirim Tugas →';
  }
});

document.getElementById('againBtn').addEventListener('click', ()=>{
  successView.style.display = 'none';
  sendView.style.display = '';
});

function resetForm(){
  document.getElementById('fNama').value = '';
  document.getElementById('fKelas').value = '';
  document.getElementById('fAbsen').value = '';
  document.getElementById('fJudul').value = '';
  fileInput.value = '';
  selectedFile = null;
  dropzone.classList.remove('has-file');
  dzText.textContent = '📎 Ketuk untuk pilih file';
}

async function fetchAllSubmissions(){
  const listResult = await window.storage.list('submission:', true);
  const keys = (listResult && listResult.keys) ? listResult.keys : [];
  if(keys.length === 0) return [];
  const results = await Promise.all(keys.map(async k=>{
    try{ const r = await window.storage.get(k, true); return r ? JSON.parse(r.value) : null; }
    catch(e){ return null; }
  }));
  return results.filter(Boolean).sort((a,b)=> b.submittedAt - a.submittedAt);
}

async function loadSubmissions(){
  const listEl = document.getElementById('inboxList');
  const countEl = document.getElementById('inboxCount');
  listEl.innerHTML = '<div class="loading-state">Memuat kiriman...</div>';
  countEl.textContent = 'Memuat...';
  try{
    submissionsCache = await fetchAllSubmissions();
    renderList();
  }catch(e){
    listEl.innerHTML = '<div class="error-state">Gagal memuat data. Coba muat ulang.</div>';
    countEl.textContent = '';
  }
}

function renderList(){
  const listEl = document.getElementById('inboxList');
  const countEl = document.getElementById('inboxCount');
  const query = document.getElementById('searchInput').value.trim().toLowerCase();

  const dupKeys = new Set(findDuplicateGroups(submissionsCache).map(g=>groupKey(g[0])));

  const filtered = submissionsCache.filter(s=>{
    if(!query) return true;
    return (s.nama||'').toLowerCase().includes(query) || (s.kelas||'').toLowerCase().includes(query) || (s.judul||'').toLowerCase().includes(query);
  });

  countEl.textContent = submissionsCache.length + ' tugas telah masuk';
  inboxBadge.textContent = submissionsCache.length ? '(' + submissionsCache.length + ')' : '';

  if(submissionsCache.length === 0){
    listEl.innerHTML = '<div class="empty-state">Belum ada tugas yang masuk.<br>Bagikan link ini supaya teman-teman bisa mengirim tugas mereka.</div>';
    return;
  }
  if(filtered.length === 0){
    listEl.innerHTML = '<div class="empty-state">Tidak ada hasil untuk pencarian ini.</div>';
    return;
  }

  listEl.innerHTML = '';
  const container = document.createElement('div');
  container.className = 'sub-list';
  filtered.forEach(s=>{
    const item = document.createElement('div');
    item.className = 'sub-item';
    const waktu = new Date(s.submittedAt).toLocaleString('id-ID', {dateStyle:'medium', timeStyle:'short'});
    const badge = dupKeys.has(groupKey(s)) ? '<span class="dup-badge">duplikat</span>' : '';
    item.innerHTML =
      '<div class="sub-info">' +
        '<div class="title">' + escapeHtml(s.judul || s.fileName) + badge + '</div>' +
        '<div class="meta">' + escapeHtml(s.nama) + ' &middot; Kelas ' + escapeHtml(s.kelas) + ' &middot; No. ' + escapeHtml(s.absen) + '</div>' +
        '<div class="time">' + waktu + '</div>' +
      '</div>' +
      '<div class="btn-col">' +
        '<button class="pv-btn">Lihat</button>' +
        '<button class="dl-btn">Unduh</button>' +
      '</div>';
    item.querySelector('.pv-btn').addEventListener('click', ()=>previewSubmission(s));
    item.querySelector('.dl-btn').addEventListener('click', ()=>downloadSubmission(s));
    container.appendChild(item);
  });
  listEl.appendChild(container);
}

function base64ToBlob(s){
  const byteChars = atob(s.fileData);
  const byteNumbers = new Array(byteChars.length);
  for(let i=0;i<byteChars.length;i++){ byteNumbers[i] = byteChars.charCodeAt(i); }
  const byteArray = new Uint8Array(byteNumbers);
  return new Blob([byteArray], {type: s.fileType || 'application/octet-stream'});
}

function base64ToText(b64){
  const binary = atob(b64);
  const bytes = new Uint8Array(binary.length);
  for(let i=0;i<binary.length;i++){ bytes[i] = binary.charCodeAt(i); }
  return new TextDecoder('utf-8').decode(bytes);
}

function downloadSubmission(s){
  try{
    const blob = base64ToBlob(s);
    const url = URL.createObjectURL(blob);
    const a = document.createElement('a');
    a.href = url; a.download = s.fileName;
    document.body.appendChild(a); a.click(); document.body.removeChild(a);
    URL.revokeObjectURL(url);
  }catch(e){ alert('Gagal mengunduh file.'); }
}

/* ---------- PREVIEW ---------- */
const previewOverlay = document.getElementById('previewOverlay');
const previewModal = document.getElementById('previewModal');
const previewTitle = document.getElementById('previewTitle');
const previewBody = document.getElementById('previewBody');
const previewDownloadBtn = document.getElementById('previewDownloadBtn');
const TEXT_EXTS = ['txt','csv','md','json','js','css','html','xml','log','yaml','yml'];
let currentPreviewUrl = null;

function previewSubmission(s){
  if(currentPreviewUrl){ URL.revokeObjectURL(currentPreviewUrl); currentPreviewUrl = null; }
  const type = s.fileType || '';
  const ext = (s.fileName.split('.').pop() || '').toLowerCase();

  try{
    if(type.startsWith('image/')){
      const url = URL.createObjectURL(base64ToBlob(s));
      currentPreviewUrl = url;
      previewBody.innerHTML = '<img src="' + url + '" alt="' + escapeHtml(s.fileName) + '">';
    }else if(type === 'application/pdf' || ext === 'pdf'){
      const url = URL.createObjectURL(base64ToBlob(s));
      currentPreviewUrl = url;
      previewBody.innerHTML = '<iframe class="pdf-frame" src="' + url + '"></iframe>';
    }else if(type.startsWith('text/') || TEXT_EXTS.includes(ext)){
      let text = base64ToText(s.fileData);
      let truncated = false;
      if(text.length > 5000){ text = text.slice(0, 5000); truncated = true; }
      previewBody.innerHTML = '<pre class="text-preview">' + escapeHtml(text) + (truncated ? '\n\n… (dipotong, unduh untuk versi lengkap)' : '') + '</pre>';
    }else{
      previewBody.innerHTML = '<div class="preview-fallback">📄 Pratinjau belum tersedia untuk file <b>.' + escapeHtml(ext || 'ini') + '</b>.<br>Unduh file untuk membukanya di aplikasi yang sesuai (mis. Word, Excel, PowerPoint).</div>';
    }
  }catch(e){
    previewBody.innerHTML = '<div class="preview-fallback">Gagal menampilkan isi file. Silakan unduh untuk membukanya.</div>';
  }

  previewTitle.textContent = s.fileName;
  previewDownloadBtn.onclick = ()=>downloadSubmission(s);
  previewOverlay.style.display = 'flex';
}

function closePreview(){
  previewOverlay.style.display = 'none';
  previewBody.innerHTML = '';
  if(currentPreviewUrl){ URL.revokeObjectURL(currentPreviewUrl); currentPreviewUrl = null; }
}

document.getElementById('previewClose').addEventListener('click', closePreview);
previewOverlay.addEventListener('click', (e)=>{ if(e.target === previewOverlay) closePreview(); });

document.getElementById('refreshBtn').addEventListener('click', loadSubmissions);
document.getElementById('searchInput').addEventListener('input', renderList);

/* ---------- ADMIN / KELOLA ---------- */

async function sha256Hex(str){
  const enc = new TextEncoder().encode(str);
  const buf = await crypto.subtle.digest('SHA-256', enc);
  return Array.from(new Uint8Array(buf)).map(b=>b.toString(16).padStart(2,'0')).join('');
}

async function getAdminConfig(){
  try{
    const r = await window.storage.get('admin-config', true);
    return r ? JSON.parse(r.value) : null;
  }catch(e){ return null; }
}

async function renderManageView(){
  manageContent.innerHTML = '<div class="loading-state">Memuat...</div>';
  let config;
  try{ config = await getAdminConfig(); }
  catch(e){ manageContent.innerHTML = '<div class="error-state">Gagal memuat status pengelola.</div>'; return; }

  if(!config){
    renderSetupForm();
  }else if(!isAdmin){
    renderLoginForm();
  }else{
    await renderAdminPanel();
  }
}

function renderSetupForm(){
  manageContent.innerHTML =
    '<div class="card-stack"><div class="card lock-card">' +
      '<span class="lock-icon">🔑</span>' +
      '<p>Belum ada pengelola untuk link ini. Buat PIN sekarang supaya hanya kamu yang bisa menghapus atau merapikan kiriman. Siapa pun yang membuka link ini masih bisa mengirim tugas dan melihat/mengunduh Kotak Masuk seperti biasa.</p>' +
      '<div class="field"><label>Buat PIN (minimal 4 karakter)</label><input type="password" id="pinNew" placeholder="••••"></div>' +
      '<div class="field"><label>Ulangi PIN</label><input type="password" id="pinConfirm" placeholder="••••"></div>' +
      '<div class="err-msg" id="setupErr"></div>' +
      '<button class="submit-btn" id="setupBtn">Jadikan Saya Pengelola</button>' +
      '<div class="note">Simpan PIN ini baik-baik — tidak tersimpan sebagai teks biasa dan tidak bisa dipulihkan kalau lupa.</div>' +
    '</div></div>';

  document.getElementById('setupBtn').addEventListener('click', async ()=>{
    const pin = document.getElementById('pinNew').value;
    const confirmPin = document.getElementById('pinConfirm').value;
    const errEl = document.getElementById('setupErr');
    if(pin.length < 4){ errEl.textContent = 'PIN minimal 4 karakter.'; return; }
    if(pin !== confirmPin){ errEl.textContent = 'PIN tidak sama.'; return; }
    errEl.textContent = '';
    try{
      const pinHash = await sha256Hex(pin);
      const result = await window.storage.set('admin-config', JSON.stringify({pinHash, createdAt: Date.now()}), true);
      if(!result) throw new Error('gagal simpan');
      isAdmin = true;
      renderAdminPanel();
    }catch(e){
      errEl.textContent = 'Gagal menyimpan PIN. Coba lagi.';
    }
  });
}

function renderLoginForm(){
  manageContent.innerHTML =
    '<div class="card-stack"><div class="card lock-card">' +
      '<span class="lock-icon">🔒</span>' +
      '<p>Bagian ini terkunci. Masukkan PIN pengelola untuk menghapus atau merapikan kiriman ganda.</p>' +
      '<div class="field"><label>PIN</label><input type="password" id="pinLogin" placeholder="••••"></div>' +
      '<div class="err-msg" id="loginErr"></div>' +
      '<button class="submit-btn" id="loginBtn">Buka</button>' +
    '</div></div>';

  const tryLogin = async ()=>{
    const pin = document.getElementById('pinLogin').value;
    const errEl = document.getElementById('loginErr');
    try{
      const config = await getAdminConfig();
      const hash = await sha256Hex(pin);
      if(config && hash === config.pinHash){
        isAdmin = true;
        renderAdminPanel();
      }else{
        errEl.textContent = 'PIN salah.';
      }
    }catch(e){
      errEl.textContent = 'Gagal memeriksa PIN. Coba lagi.';
    }
  };
  document.getElementById('loginBtn').addEventListener('click', tryLogin);
  document.getElementById('pinLogin').addEventListener('keydown', e=>{ if(e.key==='Enter') tryLogin(); });
}

async function renderAdminPanel(){
  manageContent.innerHTML = '<div class="loading-state">Memuat kiriman...</div>';
  let subs;
  try{ subs = await fetchAllSubmissions(); submissionsCache = subs; }
  catch(e){ manageContent.innerHTML = '<div class="error-state">Gagal memuat kiriman.</div>'; return; }

  const dupGroups = findDuplicateGroups(subs);

  let html = '<div class="panel-head"><span class="inbox-count">' + subs.length + ' kiriman total</span>' +
    '<button class="lock-again" id="lockBtn">Kunci lagi</button></div>';

  html += '<div class="section-title">Kiriman Ganda (' + dupGroups.length + ')</div>';
  if(dupGroups.length === 0){
    html += '<div class="empty-state" style="padding:20px 10px;">Tidak ada kiriman ganda saat ini.</div>';
  }else{
    dupGroups.forEach((group, gi)=>{
      html += '<div class="dup-group" data-gi="' + gi + '">' +
        '<div class="dup-group-head"><b>' + escapeHtml(group[0].nama) + ' &middot; Kelas ' + escapeHtml(group[0].kelas) + ' &middot; No. ' + escapeHtml(group[0].absen) + '</b>' +
        '<button class="mini-btn keep-latest-btn" data-gi="' + gi + '">Simpan yang terbaru saja</button></div>';
      group.forEach(s=>{
        const waktu = new Date(s.submittedAt).toLocaleString('id-ID', {dateStyle:'medium', timeStyle:'short'});
        html += '<div class="dup-entry"><span>' + escapeHtml(s.judul || s.fileName) + ' &middot; ' + waktu + '</span>' +
          '<button class="del-btn del-one-btn" data-id="' + s.id + '">Hapus</button></div>';
      });
      html += '</div>';
    });
  }

  html += '<div class="section-title">Semua Kiriman</div>';
  if(subs.length === 0){
    html += '<div class="empty-state" style="padding:20px 10px;">Belum ada kiriman masuk.</div>';
  }else{
    html += '<div class="sub-list">';
    subs.forEach(s=>{
      const waktu = new Date(s.submittedAt).toLocaleString('id-ID', {dateStyle:'medium', timeStyle:'short'});
      html += '<div class="sub-item">' +
        '<div class="sub-info">' +
          '<div class="title">' + escapeHtml(s.judul || s.fileName) + '</div>' +
          '<div class="meta">' + escapeHtml(s.nama) + ' &middot; Kelas ' + escapeHtml(s.kelas) + ' &middot; No. ' + escapeHtml(s.absen) + '</div>' +
          '<div class="time">' + waktu + '</div>' +
        '</div>' +
        '<div class="btn-col">' +
          '<button class="pv-btn pv-admin-btn" data-id="' + s.id + '">Lihat</button>' +
          '<button class="dl-btn dl-admin-btn" data-id="' + s.id + '">Unduh</button>' +
          '<button class="del-btn del-one-btn" data-id="' + s.id + '">Hapus</button>' +
        '</div>' +
      '</div>';
    });
    html += '</div>';
  }

  manageContent.innerHTML = html;

  document.getElementById('lockBtn').addEventListener('click', ()=>{ isAdmin = false; renderManageView(); });

  manageContent.querySelectorAll('.keep-latest-btn').forEach(btn=>{
    btn.addEventListener('click', ()=> keepLatestOnly(dupGroups[parseInt(btn.dataset.gi,10)]));
  });
  manageContent.querySelectorAll('.del-one-btn').forEach(btn=>{
    btn.addEventListener('click', ()=> deleteSubmission(btn.dataset.id));
  });
  manageContent.querySelectorAll('.dl-admin-btn').forEach(btn=>{
    btn.addEventListener('click', ()=>{
      const s = submissionsCache.find(x=>x.id===btn.dataset.id);
      if(s) downloadSubmission(s);
    });
  });
  manageContent.querySelectorAll('.pv-admin-btn').forEach(btn=>{
    btn.addEventListener('click', ()=>{
      const s = submissionsCache.find(x=>x.id===btn.dataset.id);
      if(s) previewSubmission(s);
    });
  });
}

async function deleteSubmission(id){
  if(!confirm('Hapus kiriman ini? Tindakan ini tidak bisa dibatalkan.')) return;
  try{
    await window.storage.delete('submission:' + id, true);
    submissionsCache = submissionsCache.filter(s=>s.id!==id);
    await renderAdminPanel();
  }catch(e){
    alert('Gagal menghapus. Coba lagi.');
  }
}

async function keepLatestOnly(group){
  if(!group || group.length < 2) return;
  const toDelete = group.slice(1);
  if(!confirm('Hapus ' + toDelete.length + ' kiriman lama dari ' + group[0].nama + '? Hanya kiriman terbaru yang disimpan.')) return;
  for(const s of toDelete){
    try{ await window.storage.delete('submission:' + s.id, true); }catch(e){ /* skip */ }
  }
  await renderAdminPanel();
}

loadSubmissions();
</script>
</body>
</html>
