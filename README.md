<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Danny Baylen | Music</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: Arial, sans-serif;
  background: #0b0b0b;
  color: white;
  scroll-behavior: smooth;
}

/* HERO */
.hero {
  height: 100vh;
  background: url("https://images.unsplash.com/photo-1511379938547-c1f69419868d?auto=format&fit=crop&w=1400&q=80") center/cover no-repeat;
  display: flex;
  flex-direction: column;
  justify-content: center;
  text-align: center;
  padding: 20px;
  animation: fadeIn 2s ease;
}

.hero h1 {
  font-size: 3em;
  letter-spacing: 3px;
}

.hero p {
  margin-top: 15px;
  font-size: 1.2em;
  opacity: 0.9;
}

.button {
  margin-top: 25px;
  padding: 12px 30px;
  border: none;
  border-radius: 30px;
  background: white;
  color: black;
  text-decoration: none;
  font-weight: bold;
}

/* SECTIONS */
section {
  padding: 60px 20px;
  text-align: center;
}

.fade {
  opacity: 0;
  transform: translateY(30px);
  transition: all 1s ease;
}

.fade.show {
  opacity: 1;
  transform: translateY(0);
}

/* AUDIO PLAYER */
audio {
  width: 90%;
  max-width: 400px;
  margin-top: 20px;
}

/* GALLERY */
.gallery {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(150px,1fr));
  gap: 15px;
  padding: 20px;
}

.gallery img {
  width: 100%;
  border-radius: 10px;
  transition: transform 0.4s ease;
}

.gallery img:hover {
  transform: scale(1.05);
}

/* FOOTER */
footer {
  padding: 20px;
  background: #111;
  font-size: 14px;
}

/* ANIMATION */
@keyframes fadeIn {
  from {opacity:0;}
  to {opacity:1;}
}

/* MOBILE */
@media(max-width:600px){
  .hero h1 {
    font-size: 2.2em;
  }
}
</style>
</head>

<body>

<div class="hero">
  <h1>DANNY BAYLEN</h1>
  <p>Emotional indie pop from Langley, BC</p>
  <a href="#music" class="button">Listen</a>
</div>

<section class="fade">
  <h2>About</h2>
  <p>Danny Baylen is a Canadian artist creating raw, emotional music inspired by late nights, heartbreak, and hope.</p>
</section>

<section id="music" class="fade">
  <h2>My Music</h2>
  <p>New single out now:</p>
  <audio controls>
    <source src="your-song.mp3" type="audio/mpeg">
  </audio>
</section>

<section class="fade">
  <h2>Photo Gallery</h2>
  <div class="gallery">
    <img src="https://images.unsplash.com/photo-1529626455594-4ff0802cfb7e">
    <img src="https://images.unsplash.com/photo-1500530855697-b586d89ba3ee">
    <img src="https://images.unsplash.com/photo-1517841905240-472988babdf9">
    <img src="https://images.unsplash.com/photo-1503342217505-b0a15ec3261c">
  </div>
</section>

<section class="fade">
  <h2>Contact</h2>
  <p>Email: dannybaylenmusic@gmail.com</p>
  <p>
    <a href="https://instagram.com/yourinstagram" class="button">Instagram</a>
    <a href="https://tiktok.com/@yourtiktok" class="button">TikTok</a>
  </p>
</section>

<footer>
  <p>© 2026 Danny Baylen</p>
</footer>

<script>
const fades = document.querySelectorAll(".fade");

const observer = new IntersectionObserver(entries => {
  entries.forEach(entry => {
    if(entry.isIntersecting){
      entry.target.classList.add("show");
    }
  });
});

fades.forEach(fade => observer.observe(fade));
</script>

</body>
</html>


