echo "# elderbot" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/ps1700068-crypto/elderbot.git
git push -u origin main
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>ElderBot • Sant Atulanand Convent School Innovation</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@500;700&family=Roboto:wght@300;400;500&display=swap" rel="stylesheet">
  
  <style>
    :root {
      --bg: #0a0015;
      --neon1: #ff00aa;
      --neon2: #00f0ff;
      --neon3: #9d00ff;
      --glass: rgba(40, 40, 80, 0.28);
      --glow1: 0 0 25px rgba(255,0,170,0.7);
      --glow2: 0 0 35px rgba(0,240,255,0.6);
    }

    * { margin:0; padding:0; box-sizing:border-box; }
    body {
      background: linear-gradient(135deg, var(--bg), #120025);
      color: #f0f0ff;
      font-family: 'Roboto', sans-serif;
      min-height: 100vh;
      overflow-x: hidden;
    }

    h1,h2,h3 { font-family: 'Orbitron', sans-serif; letter-spacing: 2px; }

    header {
      position: relative;
      height: 100vh;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      text-align: center;
      padding: 2rem 5%;
      overflow: hidden;
    }

    .logo-container {
      position: absolute;
      top: 2rem;
      left: 50%;
      transform: translateX(-50%);
      z-index: 10;
    }

    .school-logo {
      width: 160px;
      height: auto;
      filter: drop-shadow(0 0 18px rgba(255,215,0,0.7)) brightness(1.2);
    }

    .orb {
      position: absolute;
      width: 420px;
      height: 420px;
      background: radial-gradient(circle at 30% 30%, #ff99ff, #00ffff, #9933ff, transparent 68%);
      border-radius: 50%;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      filter: blur(70px) brightness(1.5);
      opacity: 0.42;
      animation: float 20s ease-in-out infinite alternate, hueRotate 35s linear infinite;
    }

    @keyframes float { 0% { transform: translate(-50%, -53%) scale(1); } 100% { transform: translate(-50%, -47%) scale(1.1); } }
    @keyframes hueRotate { 0% { filter: hue-rotate(0deg) blur(70px) brightness(1.5); } 100% { filter: hue-rotate(360deg) blur(70px) brightness(1.5); } }

    .content { position: relative; z-index: 2; max-width: 1100px; }
    h1 {
      font-size: clamp(4rem, 13vw, 10rem);
      background: linear-gradient(90deg, var(--neon1), var(--neon2), var(--neon3));
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      text-shadow: var(--glow1), var(--glow2);
      margin: 1rem 0;
    }

    .subtitle { font-size: 1.7rem; max-width: 820px; margin: 0 auto 2.5rem; color: #d0d0ff; line-height: 1.5; }

    .cta {
      padding: 1.3rem 3.5rem;
      font-size: 1.5rem;
      background: linear-gradient(45deg, #ff00cc, #00ccff);
      color: white;
      text-decoration: none;
      border-radius: 50px;
      box-shadow: 0 0 35px rgba(0,204,255,0.7);
      transition: all 0.4s;
    }

    .cta:hover { transform: translateY(-10px) scale(1.1); box-shadow: 0 0 70px rgba(0,204,255,1); }

    section { padding: 8rem 5%; }

    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(360px, 1fr));
      gap: 2.8rem;
      max-width: 1400px;
      margin: 4rem auto 0;
    }

    .card {
      background: var(--glass);
      backdrop-filter: blur(14px);
      border: 1px solid rgba(255,255,255,0.1);
      border-radius: 28px;
      padding: 2.8rem;
      transition: all 0.5s cubic-bezier(0.23,1,0.32,1);
      transform: perspective(1200px) rotateX(5deg) rotateY(7deg) scale(0.97);
      box-shadow: 0 25px 60px rgba(0,0,0,0.5);
      position: relative;
      overflow: hidden;
    }

    .card:hover {
      transform: perspective(1200px) rotateX(0) rotateY(0) scale(1.05) translateY(-20px);
      box-shadow: var(--glow1), var(--glow2), 0 40px 100px rgba(0,0,0,0.7);
      border-color: rgba(0,240,255,0.5);
    }

    .card h3 {
      font-size: 2.1rem;
      margin-bottom: 1.3rem;
      background: linear-gradient(90deg, #ff99ff, #66ffff);
      -webkit-background-clip: text;
      color: transparent;
    }

    .card p { color: #d0d0ff; line-height: 1.7; font-size: 1.15rem; }

    /* Reviews section styles remain the same as previous version */
    #reviews { background: linear-gradient(to bottom, rgba(20,0,40,0.9), rgba(40,0,60,0.7)); }

    .review-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(340px, 1fr)); gap: 2rem; margin-top: 3rem; }

    .review-card {
      background: rgba(60,40,100,0.3);
      border: 1px solid rgba(0,240,255,0.2);
      border-radius: 20px;
      padding: 2rem;
      backdrop-filter: blur(10px);
    }

    .stars { color: #ffd700; font-size: 1.4rem; margin-bottom: 0.8rem; }

    .review-form {
      max-width: 700px;
      margin: 5rem auto 0;
      background: var(--glass);
      padding: 3rem;
      border-radius: 24px;
      border: 1px solid rgba(255,255,255,0.1);
    }

    .review-form input, .review-form textarea, .review-form select {
      width: 100%;
      padding: 1rem;
      margin: 0.8rem 0;
      background: rgba(255,255,255,0.05);
      border: 1px solid rgba(0,240,255,0.3);
      color: white;
      border-radius: 12px;
      font-size: 1.1rem;
    }

    .review-form button {
      padding: 1rem 2.5rem;
      background: linear-gradient(45deg, var(--neon1), var(--neon2));
      border: none;
      color: white;
      font-size: 1.2rem;
      border-radius: 50px;
      cursor: pointer;
      margin-top: 1rem;
    }

    footer {
      text-align: center;
      padding: 4rem 1rem 2rem;
      color: #8888aa;
      border-top: 1px solid rgba(255,255,255,0.05);
    }

    .footer-logo { width: 110px; height: auto; margin-bottom: 1rem; filter: brightness(1.3) drop-shadow(0 0 10px gold); }

    @media (max-width: 768px) {
      h1 { font-size: 5.5rem; }
      .subtitle { font-size: 1.4rem; }
      .school-logo { width: 130px; }
    }
  </style>
</head>
<body>

  <header>
    <div class="logo-container">
      <img src="https://ezyschooling.com/_next/image?url=https%3A%2F%2Fstorage.googleapis.com%2Fezyschooling.appspot.com%2Fschool_logo%2Fsant-atulanand-convent-school-koirajpur-varanasi-logo.png&w=384&q=75" 
           alt="Sant Atulanand Convent School Official Logo" class="school-logo">
    </div>

    <div class="orb"></div>

    <div class="content">
      <h1>ElderBot</h1>
      <p class="subtitle">
        Powered by Sant Atulanand Convent School Innovation<br>
        The futuristic, loving companion that moves, entertains, cares & connects generations
      </p>
      <a href="#features" class="cta">Explore ElderBot →</a>
    </div>
  </header>

  <!-- Features section remains the same as in the previous version -->
  <section id="features">
    <h2 style="text-align:center; font-size:3.8rem; margin-bottom:1rem; background:linear-gradient(90deg,var(--neon1),var(--neon2)); -webkit-background-clip:text; color:transparent;">
      Advanced Features of ElderBot
    </h2>

    <div class="grid">
      <div class="card">
        <h3>Mobility & Entertainment</h3>
        <p>Can smoothly move around home (wheels/tracks), plays old classic songs & movies, tells jokes/stories, plays interactive games, dances gently to cheer up elders.</p>
      </div>

      <div class="card">
        <h3>24/7 Caring System</h3>
        <p>Constant health monitoring, detects falls/emergencies, reminds about hydration/exercise, gentle wake-up calls, mood detection with comforting words.</p>
      </div>

      <div class="card">
        <h3>Natural Conversation</h3>
        <p>Talks like a wise friend in local language, answers any question (health, news, recipes, religion, memories), remembers past conversations.</p>
      </div>

      <div class="card">
        <h3>Smart Medicine Compartment</h3>
        <p>Built-in secure medicine box — dispenses exact pills at right time with voice confirmation, alerts if missed, auto-refill reminders to family.</p>
      </div>

      <div class="card">
        <h3>Family Video & Voice Bridge</h3>
        <p>One-command video calls to children/grandchildren, relays messages, shows photos/videos sent by family, lets grandkids talk directly to ElderBot.</p>
      </div>

      <div class="card">
        <h3>Extra Smart Features</h3>
        <p>Voice mode always-on, daily health summary report, prayer/meditation guide, weather/news in simple words, emergency SOS to multiple contacts.</p>
      </div>
    </div>
  </section>

  <!-- Reviews section remains the same -->
  <section id="reviews">
    <h2 style="text-align:center; font-size:3.8rem; margin-bottom:1rem; background:linear-gradient(90deg,var(--neon2),var(--neon3)); -webkit-background-clip:text; color:transparent;">
      What Families Are Saying
    </h2>

    <div class="review-grid">
      <div class="review-card">
        <div class="stars">★★★★★</div>
        <p>"ElderBot has become my mother's best friend. She talks to it daily, takes medicines on time, and even dances sometimes!"</p>
        <p style="text-align:right; margin-top:1rem; color:#00f0ff;">— Ramesh, Son from Kanpur</p>
      </div>

      <div class="review-card">
        <div class="stars">★★★★☆</div>
        <p>"The medicine compartment is a lifesaver. No more confusion about doses. Grandkids love video chatting through the bot too!"</p>
        <p style="text-align:right; margin-top:1rem; color:#00f0ff;">— Priya, Daughter</p>
      </div>

      <div class="review-card">
        <div class="stars">★★★★★</div>
        <p>"Feels like having a caring family member at home. Very safe & trustworthy. Proud it's from our school vision!"</p>
        <p style="text-align:right; margin-top:1rem; color:#00f0ff;">— Dr. Sharma, Retired Teacher</p>
      </div>
    </div>

    <div class="review-form">
      <h3>Share Your ElderBot Experience</h3>
      <input type="text" placeholder="Your Name">
      <input type="text" placeholder="Relationship (Son/Daughter/Grandchild/etc)">
      <select>
        <option>Rating</option>
        <option>★★★★★</option>
        <option>★★★★☆</option>
        <option>★★★☆☆</option>
        <option>★★☆☆☆</option>
        <option>★☆☆☆☆</option>
      </select>
      <textarea rows="5" placeholder="Your review... How did ElderBot help?"></textarea>
      <button>Submit Review</button>
    </div>
  </section>

  <footer>
    <img src="https://ezyschooling.com/_next/image?url=https%3A%2F%2Fstorage.googleapis.com%2Fezyschooling.appspot.com%2Fschool_logo%2Fsant-atulanand-convent-school-koirajpur-varanasi-logo.png&w=384&q=75" 
         alt="SACS Logo" class="footer-logo">
    <p>© 2026 ElderBot Project • Sant Atulanand Convent School • To Serve Humanity</p>
    <p style="margin-top:0.8rem;">Made with love & futuristic vision for our elders</p>
  </footer>

</body>
</html>
