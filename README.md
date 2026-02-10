<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Danny Baylen</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600&display=swap" rel="stylesheet">

<style>
body {
  margin:0;
  font-family: 'Inter', sans-serif;
  background:black;
  color:white;
  text-align:center;
}

header {
  padding:60px 20px;
  border-bottom:1px solid #222;
}

h1 {
  letter-spacing:6px;
  font-weight:400;
}

nav a {
  color:white;
  margin:0 12px;
  text-decoration:none;
  font-size:14px;
  opacity:0.8;
}

nav a:hover {
  opacity:1;
}

section {
  padding:60px 20px;
}

.fade {
  opacity:0;
  transform:translateY(30px);
  transition:1s ease;
}

.fade.show {
  opacity:1;
  transform:translateY(0);
}

/* MUSIC */
audio {
  width:90%;
  max-width:400px;
  margin-top:15px;
}

/* GALLERY */
.gallery {
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(200px,1fr));
  gap:15px;
  padding:20px;
}

.gallery img {
  width:100%;
  border-radius:6px;
}

/* VIDEOS */
.video-grid {
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(300px,1fr));
  gap:20px;
}

/* FOOTER */
footer {
  border-top:1px solid #222;
  padding:30px;
  font-size:14px;
}

.socials a {
  margin:0 10px;
  color:white;
  text-decoration:none;
  font-size:14px;
}

/* MOBILE */
@media(max-width:600px){
  h1 {font-size:28px;}
}
</style>
</head>

<body>

<header>
  <h1>DANNY BAYLEN</h1>
  <nav>
    <a href="#music">MUSIC</a>
    <a href="#videos">VIDEOS</a>
    <a href="#gallery">PHOTOS</a>
  </nav>
</header>

<section id="music" class="fade">
  <h2>MUSIC</h2>
  <p>Latest song preview</p>

  <audio controls>
    <source src="your-song.mp3" type="audio/mpeg">
  </audio>

  <p style="margin-top:20px;">
    <a href="https://open.spotify.com/artist/1sEDsEf0zV8EWIl5ZwirGS">Spotify</a> |
    <a href="https://music.apple.com/ca/artist/danny-baylen/1745303435">Apple Music</a>
  </p>
</section>

<section id="videos" class="fade">
  <h2>VIDEOS</h2>
  <div class="video-grid">
    <iframe width="100%" height="315" src="https://www.youtube.com/embed/4GQ9soRIelU" frameborder="0" allowfullscreen></iframe>
    <iframe width="100%" height="315" src="https://www.youtube.com/embed/VV155sd5uA8" frameborder="0" allowfullscreen></iframe>
  </div>
</section>

<section id="gallery" class="fade">
  <h2>PHOTOS</h2>
  <div class="gallery">
    <img src="photo1.jpg">
    <img src="photo2.jpg">
    <img src="photo3.jpg">
    <img src="photo4.jpg">
  </div>
</section>

<footer>
  <div class="socials">
    <a href="https://www.tiktok.com/@yesdanny">TikTok</a>
    <a href="https://www.youtube.com/c/DannyBaylen">YouTube</a>
    <a href="https://www.instagram.com/dannybaylen/?hl=en">Instagram</a>
    <a href="https://open.spotify.com/artist/1sEDsEf0zV8EWIl5ZwirGS">Spotify</a>
    <a href="https://music.apple.com/ca/artist/danny-baylen/1745303435">Apple Music</a>
  </div>
  <p>© 2026 Danny Baylen</p>
</footer>

<script>
const fades = document.querySelectorAll(".fade");

const observer = new IntersectionObserver(entries=>{
  entries.forEach(entry=>{
    if(entry.isIntersecting){
      entry.target.classList.add("show");
    }
  });
});

fades.forEach(f=>observer.observe(f));
</script>

</body>
</html>
