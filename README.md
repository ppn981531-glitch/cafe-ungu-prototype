# cafe-ungu-prototype
<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Cafe Ungu Amikom Purwokerto – Menu & Rekomendasi</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;800&display=swap" rel="stylesheet">
<style>
:root{--bg:#f6f1ff;--surface:#fff;--text:#1d1030;--muted:#6f6385;--brand:#5b21b6;--brand-d:#3b1478;--gold:#ffc72c;--line:#e4d8f7;--chip:#ece3fb;
box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}
@media (prefers-color-scheme:dark){:root:not([data-theme="light"]){--bg:#120a20;--surface:#1d1230;--text:#f5eeff;--muted:#b5a8cc;--brand:#a78bfa;--line:#352650;--chip:#2a1c42}}
:root[data-theme="dark"]{--bg:#120a20;--surface:#1d1230;--text:#f5eeff;--muted:#b5a8cc;--brand:#a78bfa;--line:#352650;--chip:#2a1c42}
html{scroll-behavior:smooth;scroll-padding-top:80px}
*{box-sizing:border-box}
body{margin:0;background:var(--bg);color:var(--text);font-family:Poppins,system-ui,-apple-system,"Segoe UI",sans-serif}
a{text-decoration:none;color:inherit}
nav{position:sticky;top:0;z-index:4;background:var(--brand-d);color:#fff;display:flex;align-items:center;justify-content:space-between;gap:10px;padding:12px 18px}
nav .logo{font-weight:800;font-size:1.15rem}
nav .logo span{color:var(--gold)}
.links{display:flex;gap:18px;align-items:center;font-weight:600;font-size:.92rem}
.links a.t{opacity:.85}
.links a.t:hover{opacity:1;color:var(--gold)}
.ig{background:linear-gradient(45deg,#f09433,#e6683c 30%,#dc2743 55%,#cc2366 75%,#bc1888);color:#fff;padding:8px 16px;border-radius:999px;font-weight:700;font-size:.88rem;display:inline-flex;gap:6px;align-items:center;white-space:nowrap}
@media(max-width:560px){.links a.t{display:none}}
.hero{background:radial-gradient(circle at 80% 20%,#7c3aed 0,transparent 45%),var(--brand-d);color:#fff;padding:44px 20px 80px;text-align:center}
.hero .eyebrow{display:inline-block;background:var(--gold);color:#2b1d00;font-weight:800;font-size:.75rem;padding:5px 14px;border-radius:999px;letter-spacing:1px}
.hero h1{font-size:clamp(2rem,6vw,3.4rem);margin:14px 0 8px;line-height:1.1;font-weight:800}
.hero h1 em{font-style:normal;color:var(--gold)}
.hero p{margin:0 auto 22px;max-width:480px;opacity:.85}
.btn{display:inline-block;background:var(--gold);color:#2b1d00;font-weight:800;padding:12px 26px;border-radius:999px}
.wrap{max-width:1040px;margin:-44px auto 0;padding:0 16px 40px}
.panel{background:var(--surface);border-radius:20px;padding:14px;box-shadow:0 10px 30px rgba(60,20,120,.15);display:flex;flex-direction:column;gap:10px}
.panel input{width:100%;padding:12px 16px;border-radius:12px;border:2px solid var(--line);background:var(--bg);color:var(--text);font:inherit}
.tabs{display:flex;gap:8px;overflow-x:auto}
.tab{flex:none;border:0;background:var(--chip);color:var(--text);padding:9px 18px;border-radius:999px;font:600 .9rem Poppins,sans-serif;cursor:pointer}
.tab.on{background:var(--brand);color:#fff}
h2.sec{margin:28px 0 4px;font-size:1.4rem}
.grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(230px,1fr));gap:18px;margin-top:14px}
.card{background:var(--surface);border-radius:22px;border:0;padding:0;text-align:center;cursor:pointer;color:inherit;font:inherit;overflow:hidden;box-shadow:0 4px 14px rgba(60,20,120,.1);transition:transform .2s,box-shadow .2s}
.card:hover{transform:translateY(-5px);box-shadow:0 12px 26px rgba(60,20,120,.2)}
.pic{height:170px;display:grid;place-items:center;position:relative}
.plate{width:116px;height:116px;border-radius:50%;background:rgba(255,255,255,.65);display:grid;place-items:center;font-size:3.8rem}
.badge{position:absolute;top:12px;left:12px;background:var(--gold);color:#2b1d00;font-size:.7rem;font-weight:800;padding:4px 10px;border-radius:999px}
.info{padding:14px 16px 18px}
.info h3{margin:0;font-size:1.05rem}
.info small{color:var(--muted)}
.price{display:inline-block;margin-top:10px;background:var(--brand);color:#fff;font-weight:800;padding:6px 16px;border-radius:999px}
.empty{text-align:center;color:var(--muted);padding:40px 0}
.cta{background:linear-gradient(135deg,var(--brand-d),#7c3aed);color:#fff;border-radius:24px;padding:28px 22px;text-align:center;margin-top:36px}
.cta h3{margin:0 0 6px;font-size:1.3rem}
.cta .row{display:flex;gap:10px;justify-content:center;flex-wrap:wrap;margin-top:16px}
.cta .ghost{border:2px solid rgba(255,255,255,.6);padding:10px 18px;border-radius:999px;font-weight:600;font-size:.9rem}
footer{text-align:center;color:var(--muted);font-size:.85rem;padding:10px 16px 30px}
#detail{position:fixed;inset:0;background:var(--bg);overflow-y:auto;display:none;z-index:9;padding-top:env(safe-area-inset-top,0px)}
#detail.open{display:block}
.dhero{min-height:280px;display:grid;place-items:center;position:relative}
.dhero .plate{width:190px;height:190px;font-size:6.5rem}
.back{position:absolute;top:14px;left:14px;border:0;background:#fff;color:#1d1030;padding:9px 16px;border-radius:999px;font:700 .9rem Poppins,sans-serif;cursor:pointer;box-shadow:0 2px 8px rgba(0,0,0,.2)}
.dbody{max-width:680px;margin:-26px auto 0;background:var(--surface);border-radius:26px 26px 0 0;padding:26px 22px 60px;position:relative;min-height:60vh}
.dbody h2{font-size:1.9rem;margin:0 0 4px}
.big{font-size:1.6rem;font-weight:800;color:var(--brand)}
.tags{display:flex;gap:8px;flex-wrap:wrap;margin:14px 0}
.tag{background:var(--chip);padding:5px 13px;border-radius:999px;font-size:.82rem;font-weight:600}
.why{background:var(--chip);border-radius:16px;padding:14px 16px;margin:18px 0}
.dbody .ig{display:flex;justify-content:center;padding:13px;margin-top:20px;font-size:1rem}
</style>
</head>
<body>
<nav>
  <a class="logo" href="#top">Cafe<span>Ungu</span></a>
  <div class="links">
    <a class="t" href="#menu">Menu</a>
    <a class="t" href="#rekomendasi">Rekomendasi</a>
    <a class="ig" href="https://www.instagram.com/cafeungu.pwt" target="_blank" rel="noopener">📸 Instagram</a>
  </div>
</nav>

<section class="hero" id="top">
  <span class="eyebrow">AMIKOM PURWOKERTO</span>
  <h1>Nongkrong enak,<br>makan <em>puas</em>.</h1>
  <p>Intip menu andalan Cafe Ungu dan pilih yang paling cocok buat lo.</p>
  <a class="btn" href="#menu">Lihat Menu</a>
</section>

<div class="wrap">
  <div class="panel">
    <input id="q" type="search" placeholder="Cari menu favorit…">
    <div class="tabs" id="tabs"></div>
  </div>

  <h2 class="sec" id="rekomendasi">⭐ Rekomendasi Kami</h2>
  <div class="grid" id="recgrid"></div>

  <h2 class="sec" id="menu">Semua Menu</h2>
  <div class="grid" id="grid"></div>
  <div class="empty" id="empty" hidden>Menu tidak ditemukan.</div>

  <div class="cta">
    <h3>Mau lihat menu terbaru & promo?</h3>
    <div>Update lengkap ada di Instagram resmi Cafe Ungu.</div>
    <div class="row">
      <a class="ig" href="https://www.instagram.com/cafeungu.pwt" target="_blank" rel="noopener">📸 @cafeungu.pwt</a>
      <a class="ghost" href="https://www.instagram.com/reels/DQETaXAEv0P/" target="_blank" rel="noopener">▶ Tonton Reels</a>
      <a class="ghost" href="https://www.instagram.com/p/C0S8JWYJkId/" target="_blank" rel="noopener">🖼 Lihat Postingan</a>
    </div>
  </div>
</div>
<footer>© Cafe Ungu Amikom Purwokerto</footer>
<div id="detail"></div>

<script>
/* ====== EDIT MENU DI SINI ======
   Data CONTOH. Ganti dengan menu & harga asli dari Instagram @cafeungu.pwt.
   rec:true = tampil di Rekomendasi. color = warna latar kartu. */
const IG = "https://www.instagram.com/cafeungu.pwt";
const MENU = [
  {id:"nasi-goreng",cat:"Makanan",name:"Nasi Goreng Ungu",emoji:"🍳",price:16000,rec:true,color:"#fcd9a8",desc:"Nasi goreng bumbu spesial dengan telur mata sapi, kerupuk, dan acar segar.",tags:["Gurih","Kenyang"],why:"Menu klasik yang selalu aman buat makan siang atau malam."},
  {id:"nasi-ayam-geprek",cat:"Makanan",name:"Nasi Ayam Geprek",emoji:"🍗",price:18000,rec:true,color:"#fde68a",desc:"Ayam crispy digeprek dengan sambal bawang pedas, disajikan dengan nasi hangat dan lalapan.",tags:["Pedas","Kenyang"],why:"Favorit mahasiswa buat makan siang di sela kuliah."},
  {id:"mie-goreng-ungu",cat:"Makanan",name:"Mie Goreng Ungu",emoji:"🍜",price:15000,rec:false,color:"#ddd6fe",desc:"Mie goreng bumbu spesial dengan telur dan sayuran segar.",tags:["Gurih"],why:"Porsi pas dan harga bersahabat."},
  {id:"chicken-katsu",cat:"Makanan",name:"Chicken Katsu Rice",emoji:"🍛",price:20000,rec:false,color:"#fed7aa",desc:"Chicken katsu renyah dengan saus pilihan di atas nasi.",tags:["Crispy"],why:"Cocok buat yang suka tekstur renyah."},
  {id:"kentang-goreng",cat:"Snack",name:"Kentang Goreng",emoji:"🍟",price:12000,rec:true,color:"#fef08a",desc:"Kentang goreng garing dengan bumbu tabur pilihan.",tags:["Sharing"],why:"Teman nongkrong paling aman."},
  {id:"kopi-susu",cat:"Minuman",name:"Es Kopi Susu",emoji:"☕",price:15000,rec:true,color:"#d6bcfa",desc:"Espresso, susu segar, dan gula aren.",tags:["Kopi","Dingin"],why:"Teman begadang ngerjain tugas."},
  {id:"es-teh-lemon",cat:"Minuman",name:"Es Teh Lemon",emoji:"🍋",price:8000,rec:false,color:"#fef9c3",desc:"Teh segar dengan perasan lemon.",tags:["Segar","Hemat"],why:"Paling hemat dan menyegarkan."}
];
const CATS = ["Semua",...new Set(MENU.map(m=>m.cat))];
const rp = n => "Rp " + n.toLocaleString("id-ID");
let cat="Semua", term="";
const $ = s => document.querySelector(s);
const cardHTML = m => `
  <button class="card" data-id="${m.id}">
    <div class="pic" style="background:${m.color}">${m.rec?'<span class="badge">⭐ Rekomendasi</span>':""}<div class="plate">${m.emoji}</div></div>
    <div class="info"><h3>${m.name}</h3><small>${m.cat}</small><br><span class="price">${rp(m.price)}</span></div>
  </button>`;
function bind(root){root.querySelectorAll(".card").forEach(c=>c.onclick=()=>openItem(c.dataset.id));}
function renderTabs(){
  $("#tabs").innerHTML = CATS.map(c=>`<button class="tab ${c===cat?"on":""}" data-c="${c}">${c}</button>`).join("");
  $("#tabs").querySelectorAll(".tab").forEach(b=>b.onclick=()=>{cat=b.dataset.c;renderTabs();renderGrid();});
}
function renderGrid(){
  const list = MENU.filter(m=>(cat==="Semua"||m.cat===cat)&&m.name.toLowerCase().includes(term));
  $("#empty").hidden = list.length>0;
  $("#grid").innerHTML = list.map(cardHTML).join(""); bind($("#grid"));
}
function renderRec(){ $("#recgrid").innerHTML = MENU.filter(m=>m.rec).map(cardHTML).join(""); bind($("#recgrid")); }
function openItem(id,fromHash){
  const m = MENU.find(x=>x.id===id); if(!m) return;
  $("#detail").innerHTML = `
    <div class="dhero" style="background:${m.color}"><button class="back" id="back">← Kembali</button><div class="plate">${m.emoji}</div></div>
    <div class="dbody">
      <h2>${m.name}</h2><div class="big">${rp(m.price)}</div>
      <div class="tags"><span class="tag">${m.cat}</span>${m.rec?'<span class="tag">⭐ Rekomendasi</span>':""}${m.tags.map(t=>`<span class="tag">${t}</span>`).join("")}</div>
      <p>${m.desc}</p>
      <div class="why"><strong>Kenapa direkomendasikan?</strong><br>${m.why}</div>
      <a class="ig" href="${IG}" target="_blank" rel="noopener">📸 Lihat di Instagram Cafe Ungu</a>
    </div>`;
  $("#detail").classList.add("open"); $("#detail").scrollTop=0;
  $("#back").onclick=closeItem;
  if(!fromHash){try{location.hash=id;}catch(e){}}
}
function closeItem(){$("#detail").classList.remove("open");try{history.replaceState(null,"",location.pathname+location.search);}catch(e){}}
$("#q").oninput=e=>{term=e.target.value.toLowerCase().trim();renderGrid();};
window.addEventListener("hashchange",()=>{const h=location.hash.slice(1);if(MENU.some(m=>m.id===h))openItem(h,true);else $("#detail").classList.remove("open");});
renderTabs();renderRec();renderGrid();
if(MENU.some(m=>m.id===location.hash.slice(1)))openItem(location.hash.slice(1),true);
</script>
</body>
</html>
