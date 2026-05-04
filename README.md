<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>For Bahriya ❤️</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;600&display=swap" rel="stylesheet">

<style>
* {margin:0;padding:0;box-sizing:border-box;}

body {
  font-family: 'Poppins', sans-serif;
  background: #020617;
  color: white;
  overflow-x: hidden;
}

/* HERO */
.hero {
  height: 100vh;
  background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)),
              url('me.jpg') center/cover;
  display:flex;
  flex-direction:column;
  justify-content:center;
  align-items:center;
  text-align:center;
}

.hero h1 {
  font-size: 55px;
  color:#ff4d6d;
}

.hero p {
  margin-top:10px;
  font-size:20px;
}

.btn {
  margin-top:25px;
  padding:12px 30px;
  background:#ff4d6d;
  border:none;
  border-radius:8px;
  color:white;
  font-size:18px;
  cursor:pointer;
  transition:0.3s;
}

.btn:hover {
  background:#ff1f4b;
}

/* SECTION */
.section {
  padding:80px 20px;
  text-align:center;
}

/* TEXT CARD */
.card {
  max-width:700px;
  margin:auto;
  background:#0f172a;
  padding:30px;
  border-radius:15px;
  line-height:1.8;
  font-size:18px;
}

/* GALLERY */
.gallery {
  display:flex;
  justify-content:center;
  gap:20px;
  flex-wrap:wrap;
  margin-top:30px;
}

.gallery img {
  width:260px;
  border-radius:15px;
  transition:0.4s;
}

.gallery img:hover {
  transform:scale(1.05);
}

/* COUNTDOWN */
.countdown {
  display:flex;
  justify-content:center;
  gap:20px;
  margin-top:30px;
}

.box {
  background:#0f172a;
  padding:20px;
  border-radius:10px;
  min-width:80px;
}

/* HEART ANIMATION */
.heart {
  position:fixed;
  top:-10px;
  color:red;
  animation:fall 5s linear infinite;
}

@keyframes fall {
  to { transform:translateY(100vh);}
}

/* FOOTER */
.footer {
  padding:30px;
  background:#020617;
  text-align:center;
}
</style>
</head>

<body>

<!-- HERO -->
<div class="hero">
  <h1>Happy Birthday Bahriya ❤️</h1>
  <p>You are my today and all of my tomorrows</p>
  <button class="btn" onclick="playMusic()">Play Our Song 🎵</button>
</div>

<!-- MESSAGE -->
<div class="section">
  <div class="card">
    <h2>💌 For You</h2><br>
    Lovem ❤️<br><br>

    Your birthday is not just a date, it’s a reminder to the world that someone truly special was born.<br><br>

    With you, even the simplest moments turn into the most beautiful memories.<br><br>

    You’re not just my partner, you’re my best friend, my peace, and the reason behind so many of my smiles.<br><br>

    I hope this year brings you success, happiness, and lots of crazy beautiful moments…<br><br>

    And of course, I hope you always stay by my side so we can create amazing memories together 😄<br><br>

    <b>Happy Birthday, my love 🎂✨</b>
  </div>
</div>

<!-- PHOTOS -->
<div class="section">
  <h2>📸 Our Moments</h2>
  <div class="gallery">
    <img src="girlfriend.jpg">
    <img src="me.jpg">
  </div>
</div>

<!-- COUNTDOWN -->
<div class="section">
  <h2>⏳ Until We Meet Again</h2>
  <div class="countdown">
    <div class="box"><h3 id="days">0</h3><p>Days</p></div>
    <div class="box"><h3 id="hours">0</h3><p>Hours</p></div>
    <div class="box"><h3 id="minutes">0</h3><p>Minutes</p></div>
    <div class="box"><h3 id="seconds">0</h3><p>Seconds</p></div>
  </div>
</div>

<!-- FOOTER -->
<div class="footer">
  <p>Made with ❤️ for Bahriya</p>
</div>

<!-- MUSIC -->
<audio id="music" src="song.mp3"></audio>

<script>
// MUSIC
function playMusic() {
  document.getElementById("music").play();
}

// COUNTDOWN (change date)
let target = new Date("Dec 31, 2026 00:00:00").getTime();

setInterval(() => {
  let now = new Date().getTime();
  let diff = target - now;

  document.getElementById("days").innerHTML = Math.floor(diff/(1000*60*60*24));
  document.getElementById("hours").innerHTML = Math.floor((diff%(1000*60*60*24))/(1000*60*60));
  document.getElementById("minutes").innerHTML = Math.floor((diff%(1000*60*60))/(1000*60));
  document.getElementById("seconds").innerHTML = Math.floor((diff%(1000*60))/1000);
},1000);

// HEARTS
setInterval(() => {
  let heart = document.createElement("div");
  heart.className="heart";
  heart.innerHTML="❤️";
  heart.style.left=Math.random()*100+"vw";
  heart.style.fontSize=(Math.random()*20+10)+"px";
  document.body.appendChild(heart);

  setTimeout(()=>heart.remove(),5000);
},300);
</script>

</body>
</html>
