# my-dream-house
My Dream House - AI Home Redesign Website
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>My Dream House - AI Home Redesign</title>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: Arial, sans-serif;
  background: #f7f8fa;
  color: #222;
}

header {
  background: #111827;
  color: white;
  padding: 18px 7%;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo {
  font-size: 24px;
  font-weight: bold;
}

nav a {
  color: white;
  text-decoration: none;
  margin-left: 20px;
}

.hero {
  text-align: center;
  padding: 70px 20px;
  background: linear-gradient(135deg,#eef2ff,#ffffff);
}

.hero h1 {
  font-size: 46px;
  margin-bottom: 15px;
}

.hero h1 span {
  color: #6366f1;
}

.hero p {
  font-size: 18px;
  color: #555;
  margin-bottom: 30px;
}

.btn {
  background: #6366f1;
  color: white;
  border: none;
  padding: 15px 28px;
  border-radius: 10px;
  font-size: 16px;
  cursor: pointer;
}

.container {
  max-width: 1000px;
  margin: 40px auto;
  padding: 20px;
}

.card {
  background: white;
  padding: 30px;
  border-radius: 18px;
  box-shadow: 0 8px 30px rgba(0,0,0,.08);
  margin-bottom: 30px;
}

.upload {
  border: 2px dashed #aaa;
  padding: 45px 20px;
  text-align: center;
  border-radius: 15px;
  cursor: pointer;
}

.upload input {
  display: none;
}

#preview {
  max-width: 100%;
  max-height: 400px;
  margin-top: 20px;
  border-radius: 12px;
  display: none;
}

.styles {
  display: grid;
  grid-template-columns: repeat(auto-fit,minmax(130px,1fr));
  gap: 12px;
  margin: 20px 0;
}

.style {
  padding: 15px;
  border: 2px solid #ddd;
  border-radius: 10px;
  text-align: center;
  cursor: pointer;
}

.style.active {
  border-color: #6366f1;
  background: #eef2ff;
}

.pricing {
  display: grid;
  grid-template-columns: repeat(auto-fit,minmax(220px,1fr));
  gap: 20px;
}

.price {
  padding: 30px;
  background: white;
  border-radius: 15px;
  text-align: center;
  box-shadow: 0 5px 20px rgba(0,0,0,.08);
}

.price h3 {
  margin-bottom: 15px;
}

.price strong {
  font-size: 30px;
  display: block;
  margin: 15px;
}

footer {
  text-align: center;
  padding: 30px;
  background: #111827;
  color: white;
  margin-top: 50px;
}
</style>
</head>

<body>

<header>
  <div class="logo">🏠 My Dream House</div>
  <nav>
    <a href="#design">Design</a>
    <a href="#pricing">Pricing</a>
  </nav>
</header>

<section class="hero">
  <h1>Design Your <span>Dream House</span> With AI</h1>
  <p>Upload your house photo and transform it into your dream home.</p>
  <a href="#design">
    <button class="btn">✨ Start Designing</button>
  </a>
</section>

<div class="container">

<section id="design" class="card">

<h2>1. Upload Your House</h2>
<br>

<label class="upload">
  📸 Click to Upload House Photo
  <input type="file" id="photo" accept="image/*">
</label>

<img id="preview">

<br><br>

<h2>2. Choose Your Style</h2>

<div class="styles">

<div class="style active" onclick="selectStyle(this)">
🏡 Modern
</div>

<div class="style" onclick="selectStyle(this)">
✨ Luxury
</div>

<div class="style" onclick="selectStyle(this)">
🏰 Villa
</div>

<div class="style" onclick="selectStyle(this)">
🌿 Minimalist
</div>

<div class="style" onclick="selectStyle(this)">
🌎 Scandinavian
</div>

</div>

<button class="btn" onclick="redesign()">
✨ Redesign My House
</button>

<p id="message" style="margin-top:20px;"></p>

</section>

<section id="pricing">

<h2 style="text-align:center;margin-bottom:25px;">
Simple Pricing
</h2>

<div class="pricing">

<div class="price">
<h3>Free</h3>
<strong>$0</strong>
<p>1 AI design</p>
<p>Standard quality</p>
<br>
<button class="btn">Start Free</button>
</div>

<div class="price">
<h3>Premium</h3>
<strong>$4.99</strong>
<p>10 AI designs</p>
<p>HD images</p>
<br>
<button class="btn">Get Premium</button>
</div>

<div class="price">
<h3>Pro</h3>
<strong>$9.99</strong>
<p>Unlimited designs</p>
<p>High-resolution images</p>
<br>
<button class="btn">Go Pro</button>
</div>

</div>

</section>

</div>

<footer>
© 2026 My Dream House — AI Home Redesign
</footer>

<script>

const photo = document.getElementById("photo");
const preview = document.getElementById("preview");

photo.addEventListener("change", function() {

  const file = this.files[0];

  if(file) {
    preview.src = URL.createObjectURL(file);
    preview.style.display = "block";
  }

});

function selectStyle(element) {

  document.querySelectorAll(".style")
    .forEach(x => x.classList.remove("active"));

  element.classList.add("active");
}

function redesign() {

  if(!photo.files.length) {
    alert("Please upload your house photo first.");
    return;
  }

  document.getElementById("message").innerHTML =
  "✨ Your AI redesign request is ready! AI generation API will be connected in the next version.";
}

</script>

</body>
</html>
