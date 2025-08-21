<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>ESBA shoppinps</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700&family=Great+Vibes&family=Poppins:wght@300;500;700&display=swap" rel="stylesheet">
<style>
*{margin:0;padding:0;box-sizing:border-box;}
body{font-family:'Poppins',sans-serif;background:#0b0b0b;color:#fff;overflow-x:hidden;}
nav{position:fixed;top:0;left:0;right:0;display:flex;justify-content:space-between;align-items:center;padding:1rem 2rem;z-index:1000;background:rgba(0,0,0,0.5);backdrop-filter:blur(10px);}
nav h1{font-family:'Playfair Display',serif;color:#ff4d6d;letter-spacing:2px;font-size:1.8rem;}
nav ul{list-style:none;display:flex;gap:2rem;}
nav ul li{cursor:pointer;font-family:'Playfair Display',serif;font-weight:500;transition:.3s;}
nav ul li:hover{color:#ff4d6d;}
.page{min-height:100vh;width:100%;display:none;padding-top:100px;text-align:center;opacity:0;transition:opacity .8s;}
.active{display:block;opacity:1;}
#intro{position:fixed;top:0;left:0;width:100%;height:100%;background:#111;display:flex;flex-direction:column;justify-content:center;align-items:center;z-index:9999;}
#intro img{width:250px;margin-bottom:2rem;transform:translateY(50px);opacity:0;transition:all 1s;}
#intro button{padding:1rem 2.5rem;border:none;border-radius:40px;background:linear-gradient(45deg,#ff4d6d,#ff1a4d);font-family:'Great Vibes',cursive;font-size:1.5rem;color:#fff;cursor:pointer;transform:translateY(50px);opacity:0;transition:all 1s;}
.showcase{padding:3rem;display:grid;grid-template-columns:repeat(auto-fit,minmax(250px,1fr));gap:2.5rem;}
.card{background:linear-gradient(145deg,#1a1a1a,#0d0d0d);border-radius:25px;padding:1rem;text-align:center;box-shadow:0 10px 25px rgba(0,0,0,0.5);transform:translateY(50px);opacity:0;transition:all .6s;}
.card img{width:100%;border-radius:15px;margin-bottom:.5rem;transition:all .4s;}
.card h3{font-family:'Playfair Display',serif;font-size:1.3rem;margin-bottom:.3rem;}
.card p{font-family:'Great Vibes',cursive;font-size:1.1rem;margin-bottom:.5rem;}
.card button{font-family:'Great Vibes',cursive;border:none;padding:.6rem 1.5rem;border-radius:30px;background:linear-gradient(45deg,#ff4d6d,#ff1a4d);color:#fff;cursor:pointer;}
.card:hover{transform:translateY(-10px) scale(1.05);box-shadow:0 15px 35px rgba(255,77,109,0.4);}
.card img:hover{transform:scale(1.05);}
.detail-page{position:fixed;top:0;left:0;width:100%;height:100%;background:#111;display:none;flex-direction:column;align-items:center;justify-content:center;padding:2rem;z-index:9999;overflow:auto;text-align:center;opacity:0;transition:opacity .6s;}
.detail-page img{max-width:350px;border-radius:20px;margin-bottom:1rem;}
.detail-page h2{font-family:'Playfair Display',serif;font-size:2rem;margin-bottom:.5rem;}
.detail-page p{font-family:'Great Vibes',cursive;font-size:1.3rem;margin-bottom:1rem;}
.detail-page button{font-family:'Great Vibes',cursive;padding:.8rem 2rem;border:none;border-radius:40px;background:linear-gradient(45deg,#ff4d6d,#ff1a4d);color:#fff;cursor:pointer;margin:5px;transition:.3s;}
.detail-page button:hover{transform:scale(1.05);}
.surprise{display:none;position:fixed;top:0;left:0;width:100%;height:100%;background:#000;flex-direction:column;justify-content:center;align-items:center;text-align:center;z-index:9999;opacity:0;transition:opacity .8s;}
.surprise img{max-width:400px;border-radius:20px;margin-bottom:1rem;}
.surprise h1{font-family:'Great Vibes',cursive;font-size:2.5rem;color:#ff4d6d;}
.checkout{position:fixed;bottom:1rem;left:50%;transform:translateX(-50%);background:rgba(255,255,255,0.08);backdrop-filter:blur(15px);border-radius:40px;padding:1rem 2rem;display:none;justify-content:space-between;align-items:center;width:90%;max-width:400px;box-shadow:0 8px 25px rgba(0,0,0,0.6);}
.heart{position:absolute;color:#ff4d6d;font-size:1.5rem;opacity:0;pointer-events:none;transition:all 1s;}
</style>
</head>
<body>

<!-- Intro -->
<section id="intro">
  <img src="https://upload.wikimedia.org/wikipedia/commons/3/36/Hand_Holding.svg" alt="Hand Holding">
  <button onclick="enterShop()">Enter Boutique</button>
</section>

<nav>
  <h1>ESBA shoppinps</h1>
  <ul>
    <li onclick="goPage('home')">Home</li>
    <li onclick="goPage('products')">Products</li>
    <li onclick="showCheckout()">Checkout</li>
  </ul>
</nav>

<!-- Home -->
<section id="home" class="page active" style="opacity:1;">
  <h1>Welcome to ESBA shoppinps</h1>
  <p>Luxury shopping with kisses 💋 instead of money</p>
</section>

<!-- Products -->
<section id="products" class="page">
  <div class="showcase">
    <div class="card">
      <img src="https://images.unsplash.com/photo-1606813908136-1b1f4f9d3b3d?auto=format&fit=crop&w=400&q=80" alt="Kinderjoy">
      <h3>Kinderjoy</h3>
      <p>2 Kisses 💋</p>
      <button onclick="viewProduct('Kinderjoy','2','https://images.unsplash.com/photo-1606813908136-1b1f4f9d3b3d?auto=format&fit=crop&w=400&q=80')">View</button>
    </div>
    <div class="card">
      <img src="https://images.unsplash.com/photo-1617196034743-52d69f96455c?auto=format&fit=crop&w=400&q=80" alt="Jumkas">
      <h3>Jumkas</h3>
      <p>5 Kisses 💋</p>
      <button onclick="viewProduct('Jumkas','5','https://images.unsplash.com/photo-1617196034743-52d69f96455c?auto=format&fit=crop&w=400&q=80')">View</button>
    </div>
    <div class="card">
      <img src="https://images.unsplash.com/photo-1606813908136-9abcde123456?auto=format&fit=crop&w=400&q=80" alt="Kurtas">
      <h3>Kurtas</h3>
      <p>10 Kisses 💋</p>
      <button onclick="viewProduct('Kurtas','10','https://images.unsplash.com/photo-1606813908136-9abcde123456?auto=format&fit=crop&w=400&q=80')">View</button>
    </div>
  </div>
</section>

<!-- Detail Page -->
<section id="detail" class="detail-page">
  <img id="detail-img" src="" alt="">
  <h2 id="detail-title"></h2>
  <p id="detail-price"></p>
  <button onclick="addToCart()">Add to Cart</button>
  <button onclick="closeDetail()">Back</button>
</section>

<!-- Surprise -->
<section class="surprise" id="surprise">
  <img src="https://images.unsplash.com/photo-1606813908136-surprise123?auto=format&fit=crop&w=400&q=80" alt="Surprise">
  <h1>Thank you for your love 💋</h1>
</section>

<!-- Checkout -->
<div class="checkout">
  <span id="cart-count">0 Kisses 💋</span>
  <button onclick="showCheckout()">Checkout</button>
</div>

<script>
let kisses=0;

// Animate intro image and button
window.onload = () => {
  const introImg=document.querySelector('#intro img');
  const introBtn=document.querySelector('#intro button');
  setTimeout(()=>{introImg.style.opacity=1; introImg.style.transform='translateY(0)';},200);
  setTimeout(()=>{introBtn.style.opacity=1; introBtn.style.transform='translateY(0)';},800);
};

// Floating hearts
function createHeart(){
  const heart=document.createElement('div');
  heart.className='heart';
  heart.innerText='💖';
  document.body.appendChild(heart);
  heart.style.left=Math.random()*window.innerWidth+'px';
  heart.style.fontSize=(Math.random()*20+15)+'px';
  heart.style.opacity=1;
  setTimeout(()=>{heart.style.transform='translateY(-400px) scale(1.5)'; heart.style.opacity=0;},50);
  setTimeout(()=>{heart.remove();},2000);
}
setInterval(createHeart,800);

// Navigation functions
function enterShop(){
  document.getElementById('intro').style.display='none';
  const home=document.getElementById('home');
  home.classList.add('active');
  home.style.opacity=1;
}
function goPage(id){
  document.querySelectorAll('.page').forEach(p=>{p.classList.remove('active');p.style.opacity=0;});
  const page=document.getElementById(id);
  page.classList.add('active');
  setTimeout(()=>{page.style.opacity=1;},50);
  document.getElementById('detail').style.display='none';
  document.getElementById('surprise').style.display='none';
}
function viewProduct(title,price,img){
  document.getElementById('detail-title').innerText=title;
  document.getElementById('detail-price').innerText=price+' Kisses 💋';
  document.getElementById('detail-img').src=img;
  const detail=document.getElementById('detail');
  detail.style.display='flex';
  setTimeout(()=>{detail.style.opacity=1;},50);
}
function closeDetail(){document.getElementById('detail').style.opacity=0;setTimeout(()=>{document.getElementById('detail').style.display='none';},400);}
function addToCart(){
  let price=parseInt(document.getElementById('detail-price').innerText);
  kisses+=price;
  document.getElementById('cart-count').innerText=kisses+' Kisses 💋';
  document.querySelector('.checkout').style.display='flex';
  closeDetail();
}
function showCheckout(){
  document.querySelectorAll('.page').forEach(p=>{p.classList.remove('active');p.style.opacity=0;});
  document.getElementById('detail').style.display='none';
  const surprise=document.getElementById('surprise');
  surprise.style.display='flex';
  setTimeout(()=>{surprise.style.opacity=1;},50);
}
</script>
</body>
</html>

