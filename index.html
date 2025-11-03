<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>عشارك — شبكة المتاجر</title>
<link rel="stylesheet" href="styles.css" />
</head>
<body>
  <div class="header">عشارك — شبكة المتاجر</div>
  <div class="container">

    <div class="controls">
      <div class="left">
        <input id="search" class="search" placeholder="ابحث باسم المتجر أو المدينة..." />
        <select id="typeFilter" class="filter">
          <option value="all">كل المتاجر</option>
          <option value="flowers">متاجر الورد</option>
          <option value="cherries">متاجر الكرزات</option>
        </select>
      </div>
      <div>
        <button class="btn ghost" onclick="openAdmin()">لوحة الأدمن</button>
        <button class="btn" onclick="seedDemo()">جرب بيانات توضيحية</button>
      </div>
    </div>

    <div id="storesGrid" class="grid"></div>

  </div>

<script>
/* helpers */
function uid(pref='id'){ return pref + '_' + Date.now() + '_' + Math.floor(Math.random()*900+100) }
function save(key,val){ localStorage.setItem(key, JSON.stringify(val)) }
function load(key, fallback){ try{ return JSON.parse(localStorage.getItem(key)) || fallback }catch(e){ return fallback } }

/* data keys */
let stores = load('stores', []);
let orders = load('orders', []);
let settings = load('settings', { currency: 'د.ع' });

/* render stores */
const grid = document.getElementById('storesGrid');
function renderStores(){
  grid.innerHTML = '';
  const q = (document.getElementById('search').value || '').trim().toLowerCase();
  const type = document.getElementById('typeFilter').value;
  const filtered = stores.filter(s=>{
    if(type !== 'all' && s.type !== type) return false;
    if(!q) return true;
    return (s.name || '').toLowerCase().includes(q) || (s.address||'').toLowerCase().includes(q);
  });
  if(!filtered.length){
    grid.innerHTML = '<div class="small">لم يتم العثور على متاجر. اضغط "جرب بيانات توضيحية" لإضافة أمثلة.</div>';
    return;
  }
  filtered.forEach(s=>{
    const card = document.createElement('div');
    card.className = 'store-card';
    card.innerHTML = `
      <div class="store-cover"><img src="${s.coverImage || 'data:image/svg+xml;charset=utf-8,<svg xmlns=%22http://www.w3.org/2000/svg%22 width=%22240%22 height=%22160%22></svg>'}" alt=""></div>
      <div class="store-body">
        <div>
          <div class="store-title">${s.name}</div>
          <div class="store-meta">${s.type === 'flowers' ? 'متجر ورد' : (s.type === 'cherries' ? 'متجر كرزات' : s.type)} • ${s.address || ''}</div>
          <div class="small">${(s.description||'').slice(0,90)}</div>
        </div>
        <div class="store-actions">
          <div class="small">مالك: ${s.owner || '-'}</div>
          <div>
            <button class="btn" onclick="openStore('${s.id}', event)">عرض المتجر</button>
          </div>
        </div>
      </div>`;
    grid.appendChild(card);
  });
}

/* open store page */
function openStore(id, e){
  e.stopPropagation();
  window.location.href = `store.html?id=${encodeURIComponent(id)}`;
}

/* search & filter events */
document.getElementById('search').addEventListener('input', renderStores);
document.getElementById('typeFilter').addEventListener('change', renderStores);

/* admin open */
function openAdmin(){ window.location.href = 'admin.html' }

/* demo seed (مؤقت) */
function seedDemo(){
  if(stores && stores.length) if(!confirm('ستتم إضافة متاجر تجريبية بالإضافة للمتاجر الحالية. متابعة؟')) return;
  const demo = [
    {
      id: uid('store'), type:'flowers', name:'ورود بغداد',
      owner:'مهدي الحلاق', phone:'07701234567', address:'منطقة الكرادة', description:'متجر ورد فاخر مع تغليف هدايا راقي',
      coverImage:'images/demo1.jpg',
      gallery:['images/demo1.jpg','images/demo2.jpg'],
      products:[
        {id:uid('p'), name:'باقة أحمر كلاسيك', price:5000, description:'12 وردة حمراء', image:'images/p1.jpg', availableQty:50, colors:['أحمر','وردي']},
        {id:uid('p'), name:'باقة ناعمة', price:4200, description:'باقة ناعمة مميزة', image:'images/p2.jpg', availableQty:30, colors:['أبيض','وردي']}
      ],
      createdAt: Date.now()
    },
    {
      id: uid('store'), type:'cherries', name:'كرزات حلوة',
      owner:'سارة المعروف', phone:'07809998877', address:'منطقة المنصور', description:'حلويات وكعكات صغيرة للفعاليات',
      coverImage:'images/demo3.jpg',
      gallery:['images/demo3.jpg'],
      products:[
        {id:uid('p'), name:'صندوق كرزات صغير', price:3000, description:'12 حبة', image:'images/c1.jpg', availableQty:80, colors:[]}
      ],
      createdAt: Date.now()
    }
  ];
  stores = stores.concat(demo);
  save('stores', stores);
  alert('أضيفت بيانات توضيحية. الآن تعرض في الصفحة.');
  renderStores();
}

/* initial render */
renderStores();

</script>
</body>
</html>
