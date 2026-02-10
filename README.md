<html lang="en">
<head>
<meta charset="UTF-8">
<title>Danny Baylen</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<!-- Fonts -->
<link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@600;700&family=Inter:wght@400;600;800&display=swap" rel="stylesheet">

<!-- Icons -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">

<style>
* { box-sizing:border-box; }

body {
  margin:0;
  font-family:'Inter', sans-serif;
  background: linear-gradient(to bottom, #000000, #1a1a1a, #2e2e2e);
  color:white;
  text-align:center;
  font-weight:600;
}

/* LOADING SCREEN */
#loader {
  position:fixed;
  inset:0;
  background:black;
  display:flex;
  align-items:center;
  justify-content:center;
  z-index:9999;
}

#loader h1 {
  font-family:'Cinzel', serif;
  font-size:40px;
  color:red;
  animation: glow 2s infinite alternate;
}

@keyframes glow {
  from { text-shadow:0 0 5px red; }
  to { text-shadow:0 0 25px red; }
}

/* HEADER */
header {
  background:url("images/header.jpg") center/cover no-repeat;
  padding:30px 20px;
  position:relative;
}

header::after {
  content:"";
  position:absolute;
  inset:0;
  background:rgba(0,0,0,0.75);
  z-index:0;
}

header * {
  position:relative;
  z-index:1;
}

.logo {
  font-family:'Cinzel', serif;
  letter-spacing:6px;
  font-size:36px;
  animation: glow 3s infinite alternate;
}

/* SOCIAL ICONS */
.social-top a {
  color:red;
  margin:0 12px;
  font-size:30px;
  transition:0.3s;
}

.social-top a:hover {
  text-shadow:0 0 12px red,0 0 25px red;
  transform:scale(1.2);
}

/* NAV */
nav {
  margin-top:15px;
}

nav a {
  color:white;
  margin:0 12px;
  text-decoration:none;
  font-size:15px;
  font-weight:800;
}

/* HAMBURGER */
.hamburger {
  display:none;
  font-size:28px;
  cursor:pointer;
}

/* CONTACT BUTTON */
.contact-btn {
  display:inline-block;
  margin-top:15px;
  padding:12px 28px;
  border:2px solid white;
  border-radius:25px;
  color:white;
  text-decoration:none;
  font-weight:800;
}

.contact-btn:hover {
  box-shadow:0 0 15px white;
}

/* SECTIONS */
section {
  padding:70px 20px;
}

.fade {
  opacity:0;
  transform:translateY(40px);
  transition:1s ease;
}
.fade.show {
  opacity:1;
  transform:translateY(0);
}

h2 {
  font-family:'Cinzel', serif;
  letter-spacing:3px;
  font-size:28px;
}

/* RELEASES */
.releases {
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(300px,1fr));
  gap:20px;
}

/* VIDEOS */
.video-grid {
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(300px,1fr));
  gap:20px;
}

/* GALLERY */
.gallery {
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(200px,1fr));
  gap:15px;
}

.gallery img {
  width:100%;
  border-radius:10px;
  transition:0.3s;
}

.gallery img:hover {
  transform:scale(1.05);
  box-shadow:0 0 15px white;
}

/* CONTACT FORM */
form {
  max-width:400px;
  margin:auto;
}

input, textarea {
  width:100%;
  padding:12px;
  margin:10px 0;
  background:#111;
  border:1px solid #444;
  color:white;
}

button {
  padding:12px 25px;
  background:red;
  border:none;
  color:white;
  font-weight:800;
  cursor:pointer;
}

button:hover {
  box-shadow:0 0 15px red;
}

/* FOOTER */
footer {
  border-top:1px solid #333;
  padding:30px;
}

/* MOBILE */
@media(max-width:700px){
  nav { display:none; }
  nav.active { display:block; }
  nav a { display:block; margin:10px 0; }
  .hamburger { display:block; }
}
</style>
</head>

<body>

<!-- LOADER -->
<div id="loader">
  <h1>DANNY BAYLEN</h1>
</div>

<header>
  <div class="social-top">
    <a href="https://www.tiktok.com/@yesdanny"><i class="fab fa-tiktok"></i></a>
    <a href="https://www.youtube.com/c/DannyBaylen"><i class="fab fa-youtube"></i></a>
    <a href="https://www.instagram.com/dannybaylen/?hl=en"><i class="fab fa-instagram"></i></a>
    <a href="https://open.spotify.com/artist/1sEDsEf0zV8EWIl5ZwirGS"><i class="fab fa-spotify"></i></a>
    <a href="https://music.apple.com/ca/artist/danny-baylen/1745303435"><i class="fab fa-apple"></i></a>
  </div>

  <div class="hamburger" onclick="toggleMenu()">☰</div>

  <div class="logo">DANNY BAYLEN</div>

  <nav id="menu">
    <a href="#releases">RELEASES</a>
    <a href="#videos">VIDEOS</a>
    <a href="#gallery">PHOTOS</a>
    <a href="#contact">CONTACT</a>
  </nav>
</header>

<section id="releases" class="fade">
<h2>RECENT RELEASES</h2>
<div class="releases">
  <iframe src="<iframe data-testid="embed-iframe" style="border-radius:12px" src="https://open.spotify.com/embed/album/6aAF3r7pp1AUCxfkaabZrY?utm_source=generator" width="100%" height="152" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>"
  <iframe src="<iframe data-testid="embed-iframe" style="border-radius:12px" src="https://open.spotify.com/embed/album/4vYp0KvPQHBsz7OBSjI1qw?utm_source=generator" width="100%" height="152" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>"
</div>
</section>

<section class="fade">
<h2>ALL MUSIC</h2>
<iframe src="https://open.spotify.com/embed/artist/1sEDsEf0zV8EWIl5ZwirGS?theme=0"
width="90%" height="380" allow="encrypted-media"></iframe>
</section>

<section id="videos" class="fade">
<h2>VIDEOS</h2>
<div class="video-grid">
  <iframe src="https://www.youtube.com/embed/4GQ9soRIelU" width="100%" height="315"></iframe>
  <iframe src="https://www.youtube.com/embed/VV155sd5uA8" width="100%" height="315"></iframe>
</div>
</section>

<section id="gallery" class="fade">
<h2>PHOTOS</h2>
<div class="gallery">
  <img src="images/photo1.jpg">
  <img src="images/photo2.jpg">
  <img src="images/photo3.jpg">
  <img src="images/photo4.jpg">
</div>
</section>

<section id="contact" class="fade">
<h2>CONTACT</h2>

<form action="https://formspree.io/f/xbjvgrqe" method="POST">
  <input type="text" name="name" placeholder="Your Name" required>
  <input type="email" name="email" placeholder="Your Email" required>
  <textarea name="message" placeholder="Your Message" required></textarea>
  <button type="submit">SEND MESSAGE</button>
</form>

</section>

<footer>
<p>© 2026 Danny Baylen</p>
</footer>

<script>
// loader
window.onload = function(){
  document.getElementById("loader").style.display="none";
}

// fade animation
const fades = document.querySelectorAll(".fade");
const observer = new IntersectionObserver(entries=>{
  entries.forEach(entry=>{
    if(entry.isIntersecting){
      entry.target.classList.add("show");
    }
  });
});
fades.forEach(f=>observer.observe(f));

// mobile menu
function toggleMenu(){
  document.getElementById("menu").classList.toggle("active");
}
</script>

</body>
</html>
