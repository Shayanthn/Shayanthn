<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Shayan Taherkhani - GitHub Profile</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    :root {
      --primary-bg: #0a0a14;
      --secondary-bg: #121220;
      --accent: #8a2be2;
      --accent-light: #a45deb;
      --text-primary: #f0f0ff;
      --text-secondary: #c0c0e0;
      --glass-bg: rgba(25, 25, 45, 0.6);
      --glass-border: rgba(255, 255, 255, 0.1);
      --card-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
      --transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
    }

    body {
      background: linear-gradient(135deg, var(--primary-bg), var(--secondary-bg));
      color: var(--text-primary);
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      min-height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      padding: 20px;
      line-height: 1.6;
      overflow-x: hidden;
      position: relative;
    }

    /* Background elements */
    .bg-elements {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      z-index: -1;
      overflow: hidden;
    }

    .bg-circle {
      position: absolute;
      border-radius: 50%;
      filter: blur(60px);
      opacity: 0.3;
    }

    .circle-1 {
      width: 400px;
      height: 400px;
      background: linear-gradient(120deg, #ff00cc, #333399);
      top: 10%;
      left: 10%;
      animation: float 15s infinite alternate ease-in-out;
    }

    .circle-2 {
      width: 350px;
      height: 350px;
      background: linear-gradient(120deg, #00ccff, #6600ff);
      bottom: 15%;
      right: 10%;
      animation: float 18s infinite alternate-reverse ease-in-out;
    }

    .circle-3 {
      width: 250px;
      height: 250px;
      background: linear-gradient(120deg, #ff9900, #ff0066);
      top: 40%;
      right: 20%;
      animation: float 12s infinite alternate ease-in-out;
    }

    @keyframes float {
      0% {
        transform: translate(0, 0) rotate(0deg);
      }
      100% {
        transform: translate(20px, 20px) rotate(5deg);
      }
    }

    /* Main container */
    .container {
      width: 100%;
      max-width: 900px;
      perspective: 1200px;
    }

    /* Profile card */
    .profile-card {
      background: var(--glass-bg);
      backdrop-filter: blur(12px);
      -webkit-backdrop-filter: blur(12px);
      border: 1px solid var(--glass-border);
      border-radius: 25px;
      padding: 40px;
      box-shadow: var(--card-shadow);
      position: relative;
      overflow: hidden;
      transform-style: preserve-3d;
      transition: var(--transition);
    }

    .profile-card::before {
      content: '';
      position: absolute;
      top: -50%;
      left: -50%;
      width: 200%;
      height: 200%;
      background: radial-gradient(circle, rgba(138,43,226,0.1) 0%, transparent 70%);
      z-index: -1;
      opacity: 0.6;
    }

    /* Header section */
    .header {
      display: flex;
      flex-direction: column;
      align-items: center;
      text-align: center;
      margin-bottom: 40px;
      position: relative;
    }

    .avatar-container {
      position: relative;
      width: 160px;
      height: 160px;
      margin-bottom: 25px;
      transform-style: preserve-3d;
      perspective: 1000px;
    }

    .avatar {
      width: 100%;
      height: 100%;
      border-radius: 50%;
      border: 4px solid var(--accent);
      object-fit: cover;
      transform: translateZ(30px);
      transition: var(--transition);
      box-shadow: 0 10px 30px rgba(138, 43, 226, 0.3);
    }

    .avatar-border {
      position: absolute;
      top: -10px;
      left: -10px;
      right: -10px;
      bottom: -10px;
      border-radius: 50%;
      border: 2px solid var(--accent-light);
      animation: rotate 20s linear infinite;
      z-index: -1;
    }

    @keyframes rotate {
      from { transform: rotate(0deg); }
      to { transform: rotate(360deg); }
    }

    h1 {
      font-size: 3.2rem;
      margin-bottom: 10px;
      text-transform: uppercase;
      letter-spacing: 2px;
      background: linear-gradient(to right, #ff00cc, #6600ff);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      font-weight: 800;
      text-shadow: 0 4px 10px rgba(102, 0, 255, 0.2);
      position: relative;
      transform: translateZ(40px);
    }

    .title {
      font-size: 1.3rem;
      color: var(--text-secondary);
      margin-bottom: 20px;
      font-weight: 300;
      letter-spacing: 1px;
    }

    .bio {
      font-size: 1.1rem;
      max-width: 600px;
      margin: 0 auto;
      color: var(--text-primary);
      line-height: 1.8;
      background: rgba(0, 0, 0, 0.2);
      padding: 20px;
      border-radius: 15px;
      border-left: 3px solid var(--accent);
      transform: translateZ(20px);
    }

    .highlight {
      color: var(--accent-light);
      font-weight: bold;
    }

    /* Content sections */
    .content-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 30px;
      margin: 40px 0;
    }

    .section {
      background: rgba(15, 15, 30, 0.7);
      border-radius: 20px;
      padding: 25px;
      border: 1px solid var(--glass-border);
      box-shadow: 0 8px 20px rgba(0, 0, 0, 0.2);
      transform-style: preserve-3d;
      transform: translateZ(20px);
      transition: var(--transition);
    }

    .section:hover {
      transform: translateZ(30px) translateY(-10px);
      box-shadow: 0 15px 30px rgba(0, 0, 0, 0.3);
    }

    .section-title {
      font-size: 1.6rem;
      margin-bottom: 20px;
      color: var(--accent-light);
      display: flex;
      align-items: center;
      gap: 10px;
    }

    .section-title i {
      background: rgba(138, 43, 226, 0.2);
      width: 40px;
      height: 40px;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    /* Links section */
    .links-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 15px;
    }

    .link-card {
      background: rgba(20, 20, 40, 0.7);
      border-radius: 15px;
      padding: 20px;
      text-align: center;
      display: flex;
      flex-direction: column;
      align-items: center;
      transition: var(--transition);
      border: 1px solid transparent;
      transform: translateZ(10px);
    }

    .link-card:hover {
      transform: translateZ(20px) scale(1.05);
      background: rgba(30, 30, 60, 0.8);
      border-color: var(--accent);
    }

    .link-icon {
      font-size: 2.5rem;
      margin-bottom: 15px;
      color: var(--accent-light);
    }

    .link-title {
      font-size: 1.1rem;
      margin-bottom: 5px;
    }

    .link-text {
      font-size: 0.9rem;
      color: var(--text-secondary);
      word-break: break-word;
    }

    /* Websites section */
    .websites-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 15px;
    }

    .website-card {
      background: rgba(20, 20, 40, 0.7);
      border-radius: 15px;
      padding: 20px;
      transition: var(--transition);
      border: 1px solid transparent;
      transform: translateZ(10px);
    }

    .website-card:hover {
      transform: translateZ(20px) translateY(-5px);
      border-color: var(--accent);
      background: rgba(30, 30, 60, 0.8);
    }

    .website-title {
      font-size: 1.2rem;
      margin-bottom: 10px;
      color: var(--accent-light);
      display: flex;
      align-items: center;
      gap: 10px;
    }

    /* Footer */
    .footer {
      text-align: center;
      margin-top: 40px;
      padding-top: 30px;
      border-top: 1px solid var(--glass-border);
      color: var(--text-secondary);
      font-size: 0.9rem;
      transform: translateZ(10px);
    }

    .company {
      color: var(--accent-light);
      font-weight: bold;
      margin-top: 5px;
      font-size: 1.1rem;
    }

    /* 3D effect */
    .container {
      transform-style: preserve-3d;
    }

    /* Responsive design */
    @media (max-width: 768px) {
      .profile-card {
        padding: 25px;
      }
      
      h1 {
        font-size: 2.5rem;
      }
      
      .avatar-container {
        width: 130px;
        height: 130px;
      }
      
      .content-grid {
        grid-template-columns: 1fr;
      }
    }

    @media (max-width: 480px) {
      .profile-card {
        padding: 20px;
      }
      
      h1 {
        font-size: 2rem;
      }
      
      .title {
        font-size: 1.1rem;
      }
      
      .bio {
        font-size: 1rem;
        padding: 15px;
      }
      
      .section {
        padding: 20px;
      }
      
      .section-title {
        font-size: 1.4rem;
      }
    }
  </style>
</head>
<body>
  <div class="bg-elements">
    <div class="bg-circle circle-1"></div>
    <div class="bg-circle circle-2"></div>
    <div class="bg-circle circle-3"></div>
  </div>

  <div class="container">
    <div class="profile-card">
      <div class="header">
        <div class="avatar-container">
          <img src="https://raw.githubusercontent.com/Shayanthn/shayantaherkhani.github.io/main/file_000000003c7061f698c731eb9caef603.png" alt="Shayan Taherkhani" class="avatar">
          <div class="avatar-border"></div>
        </div>
        
        <h1>Shayan Taherkhani</h1>
        <div class="title">PROFESSIONAL GITHUB PROFILE</div>
        
        <div class="bio">
          <i class="fas fa-quote-left" style="margin-right: 10px; color: #a45deb;"></i>
          I'm someone who can't stop exploring. Passionate about innovation and technology, constantly pushing boundaries in AI and web development.
          <i class="fas fa-quote-right" style="margin-left: 10px; color: #a45deb;"></i>
        </div>
      </div>

      <div class="content-grid">
        <div class="section">
          <h2 class="section-title"><i class="fas fa-link"></i> Professional Links</h2>
          <div class="links-grid">
            <a href="https://scholar.google.com/citations?user=S0jy4-IAAAAJ&hl=en" target="_blank" class="link-card">
              <div class="link-icon"><i class="fab fa-google"></i></div>
              <div class="link-title">Google Scholar</div>
              <div class="link-text">Research Publications</div>
            </a>
            
            <a href="https://github.com/shayanthn" target="_blank" class="link-card">
              <div class="link-icon"><i class="fab fa-github"></i></div>
              <div class="link-title">GitHub</div>
              <div class="link-text">PRO Account</div>
            </a>
            
            <a href="https://www.researchgate.net/profile/Shayan-Taherkhani" target="_blank" class="link-card">
              <div class="link-icon"><i class="fas fa-flask"></i></div>
              <div class="link-title">ResearchGate</div>
              <div class="link-text">Academic Profile</div>
            </a>
            
            <a href="https://www.linkedin.com/in/shayantaherkhani78" target="_blank" class="link-card">
              <div class="link-icon"><i class="fab fa-linkedin"></i></div>
              <div class="link-title">LinkedIn</div>
              <div class="link-text">Professional Network</div>
            </a>
          </div>
        </div>
        
        <div class="section">
          <h2 class="section-title"><i class="fas fa-globe"></i> My Websites</h2>
          <div class="websites-grid">
            <a href="https://shayantaherkhani.ir" target="_blank" class="website-card">
              <h3 class="website-title"><i class="fas fa-star"></i> shayantaherkhani.ir</h3>
              <p>Personal portfolio and professional hub</p>
            </a>
            
            <a href="https://aetherai.ir" target="_blank" class="website-card">
              <h3 class="website-title"><i class="fas fa-brain"></i> aetherai.ir</h3>
              <p>AI research and development platform</p>
            </a>
            
            <a href="https://stickerino.ir" target="_blank" class="website-card">
              <h3 class="website-title"><i class="fas fa-sticky-note"></i> stickerino.ir</h3>
              <p>Creative sticker marketplace</p>
            </a>
          </div>
        </div>
        
        <div class="section">
          <h2 class="section-title"><i class="fas fa-envelope"></i> Contact Information</h2>
          <div class="links-grid">
            <div class="link-card">
              <div class="link-icon"><i class="fas fa-envelope-open-text"></i></div>
              <div class="link-title">University Email</div>
              <div class="link-text">shayan.taherkhani.studio.unibo.it</div>
            </div>
            
            <div class="link-card">
              <div class="link-icon"><i class="fas fa-envelope"></i></div>
              <div class="link-title">Direct Contact</div>
              <div class="link-text">admin@shayantaherkhani.ir</div>
            </div>
          </div>
        </div>
      </div>

      <div class="footer">
        <p>© 2025 Shayan Taherkhani. All Rights Reserved.</p>
        <p class="company">AetherosTech</p>
      </div>
    </div>
  </div>

  <script>
    document.addEventListener('DOMContentLoaded', function() {
      const container = document.querySelector('.container');
      const card = document.querySelector('.profile-card');
      
      // Mouse move effect for 3D perspective
      document.addEventListener('mousemove', (e) => {
        const xAxis = (window.innerWidth / 2 - e.pageX) / 25;
        const yAxis = (window.innerHeight / 2 - e.pageY) / 25;
        
        card.style.transform = `rotateY(${xAxis}deg) rotateX(${yAxis}deg)`;
      });
      
      // Mouse enter effect
      container.addEventListener('mouseenter', () => {
        card.style.transition = 'none';
      });
      
      // Mouse leave effect
      container.addEventListener('mouseleave', () => {
        card.style.transition = 'all 0.5s ease';
        card.style.transform = 'rotateY(0deg) rotateX(0deg)';
      });
      
      // Background circles animation
      const circles = document.querySelectorAll('.bg-circle');
      circles.forEach((circle, index) => {
        circle.style.animationDelay = `${index * 2}s`;
      });
    });
  </script>
</body>
</html>
