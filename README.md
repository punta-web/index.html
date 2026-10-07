<!doctype html>
<html lang="it">
<head>
<meta charset="utf-8"><meta name="viewport" content="width=device-width,initial-scale=1,viewport-fit=cover">
<meta name="theme-color" content="#071725"><meta name="description" content="TOMGITECH — contatto rapido NFC">
<title>TOMGITECH | Contatto rapido</title>
<style>
:root{--bg:#071725;--panel:#0c263b;--cyan:#37d9ef;--text:#edfaff;--muted:#b4cbd8;--green:#25D366}*{box-sizing:border-box}body{margin:0;min-height:100vh;background:radial-gradient(circle at 50% 0,#124269 0,#071725 45%,#030a10 100%);color:var(--text);font-family:system-ui,-apple-system,Segoe UI,Arial,sans-serif;display:grid;place-items:center;padding:22px}.card{width:min(430px,100%);text-align:center;padding:30px 20px 24px;border:1px solid #1e526e;border-radius:26px;background:linear-gradient(145deg,#0d2d45dd,#071725ee);box-shadow:0 24px 70px #0008}.brand{font-size:2.15rem;font-weight:900;letter-spacing:.045em}.brand span{color:var(--cyan)}.sub{font-size:.73rem;letter-spacing:.28em;color:#c9e7f2;margin-top:-2px}.tagline{color:var(--muted);margin:16px 0 25px;font-style:italic}.actions{display:grid;gap:12px}.btn{display:flex;align-items:center;gap:13px;min-height:59px;padding:12px 17px;border-radius:16px;text-decoration:none;color:#061823;background:linear-gradient(110deg,#12b3e5,#42e1e9);font-weight:800;text-align:left;box-shadow:0 8px 26px #00bfff20}.btn .ico{font-size:1.5rem;width:32px;text-align:center}.btn.wa{background:linear-gradient(110deg,#20bb5c,#38df76)}.btn.alt{background:#0b2031;color:var(--text);border:1px solid #39758e;box-shadow:none}.btn:hover{filter:brightness(1.1)}.foot{margin:23px 0 0;color:#7898a8;font-size:.78rem}.lang{display:flex;justify-content:flex-end;gap:6px;margin:-8px 0 8px}.lang button{border:1px solid #39758e;background:#081c2b;color:#dff7ff;border-radius:999px;padding:6px 9px;font-weight:800;cursor:pointer}.lang button.active{background:#174761;border-color:#46d9ec}.paypal{background:linear-gradient(110deg,#0878d1,#35a7ff)!important;color:#fff!important}.pulse{width:74px;height:4px;border-radius:99px;background:linear-gradient(90deg,transparent,var(--cyan),transparent);margin:18px auto 2px}
</style></head>
<body><main class="card">
<div class="lang"><button type="button" data-lang="it" class="active">🇮🇹 IT</button><button type="button" data-lang="en">🇬🇧 EN</button></div><div class="brand">TOMGI<span>TECH</span></div><div class="sub">ASSISTENZA DIGITALE</div><div class="pulse"></div>
<p class="tagline">La strada semplice verso la soluzione.</p>
<div class="actions">
<a class="btn" href="https://www.tomgitech.it/"><span class="ico">🌐</span><span>Visita il sito</span></a>
<a class="btn wa" href="https://wa.me/393759750870"><span class="ico">💬</span><span>Scrivimi su WhatsApp</span></a>
<a class="btn alt" href="tel:+393759750870"><span class="ico">☎</span><span>Chiama TOMGITECH</span></a>
<a class="btn alt" href="tomgitech.vcf" download><span class="ico">👤</span><span>Salva nei contatti</span></a>
<a class="btn alt" href="mailto:info@tomgitech.it"><span class="ico">✉</span><span>info@tomgitech.it</span></a>
<a class="btn paypal" href="https://paypal.me/trillytrippa" target="_blank" rel="noopener"><span class="ico">💳</span><span data-t="paypal">Paga con PayPal</span></a>
</div><p class="foot">TOMGITECH · Firenze e provincia</p>
</main><script>
const nfcText={en:{tagline:'The simple way to a solution.',site:'Visit the website',wa:'Message me on WhatsApp',call:'Call TOMGITECH',save:'Save contact',paypal:'Pay with PayPal',foot:'TOMGITECH · Florence and surrounding area'},it:{tagline:'La strada semplice verso la soluzione.',site:'Visita il sito',wa:'Scrivimi su WhatsApp',call:'Chiama TOMGITECH',save:'Salva nei contatti',paypal:'Paga con PayPal',foot:'TOMGITECH · Firenze e provincia'}};
const keys=['site','wa','call','save'];document.querySelectorAll('.actions .btn span:last-child').forEach((el,i)=>{if(i<4)el.dataset.t=keys[i]});document.querySelector('.tagline').dataset.t='tagline';document.querySelector('.foot').dataset.t='foot';
function nfcLang(l){document.documentElement.lang=l;document.querySelectorAll('[data-t]').forEach(e=>e.textContent=nfcText[l][e.dataset.t]);document.querySelectorAll('[data-lang]').forEach(b=>b.classList.toggle('active',b.dataset.lang===l));localStorage.setItem('tomgitech-lang',l);document.title=l==='en'?'TOMGITECH | Quick contact':'TOMGITECH | Contatto rapido'}
document.querySelectorAll('[data-lang]').forEach(b=>b.onclick=()=>nfcLang(b.dataset.lang));nfcLang(localStorage.getItem('tomgitech-lang')||'it');
</script></body></html>
