<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>EduCompass - Ultimate Professional UX</title>
<link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700&family=Montserrat:wght@600;700;800&display=swap" rel="stylesheet">
<style>
  /* --- 🎨 ULTIMATE UX & SPACING OVERHAUL --- */
  /* --- 🎨 ULTIMATE UX & SPACING OVERHAUL --- */
:root{
  --primary-blue: #1A5276; /* Dark Blue/Navy for Authority */
  --accent-teal: #00CCB3; /* Bright Teal for Interactivity */
  --bg-main: #f8f9fa; /* Very Light Background */
  --card-bg: #ffffff;
  --text-dark: #212529;
  --text-muted: #6c757d;
  --success: #00CCB3;
  --border-color: #e3e6e8;
  --shadow-pro: 0 10px 30px rgba(0, 0, 0, 0.08);
}
*{box-sizing:border-box;margin:0;padding:0}
body{
  font-family: Arial, Helvetica, sans-serif;
  background-color: var(--bg-main);
  color: var(--text-dark);
  line-height: 1.6;
}

/* Layout Structure - Significantly Wider and More Spaced */
.container{width:90%;max-width:1400px;margin:80px auto 120px;display:block;} 

/* Desktop / default */
header {
  background: var(--card-bg);
  border-bottom: 1px solid var(--border-color);
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.05);
  height: 70px;
  display: flex;
  align-items: center;
  padding: 0 20px;
}

.nav-wrap {
  width: 90%;
  max-width: 1400px;
  margin: 0 auto;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

/* Mobile / phones only */
@media (max-width: 600px) {
  header {
    padding: 0 12px;
    width: 100%;
    box-sizing: border-box;
  }

  .nav-wrap {
    width: 100%;
    max-width: none;
    margin: 0;
    justify-content: space-between;
    display: flex;
  }

  .nav-wrap > * {
    flex-shrink: 0;    /* prevents 'Result' from shrinking */
  }

  body, html {
    overflow-x: hidden;
  }
}


@media (max-width: 520px){
  .progress-bar-outer-top {
    width: 100%; /* full width on phones */
  }
}

.brand .logo {
  background: var(--accent-teal);
  color: white;
  width: 45px;
  height: 45px;
  font-size: 1.1rem;
  border-radius: 8px;
  display: flex;
  align-items: center;
  justify-content: center;
}
/* MOBILE: Add space between brand and nav */
@media (max-width: 520px) {
  header .nav-wrap {
    flex-direction: column; /* stack brand and nav vertically */
    align-items: flex-start; /* left-align brand */
    gap: 15px; /* vertical space between brand and nav */
  }

  nav {
    justify-content: flex-start; /* left-align nav links */
    gap: 20px; /* increase spacing between links */
  }
}
@media (max-width: 520px) {
  .nav-wrap {
    justify-content: space-between; /* keep row layout */
  }

  .brand {
    margin-right: 20px; /* push nav links farther right */
  }
}




.brand h1{font-family: 'Montserrat', sans-serif; font-size:1.5rem;color:var(--primary-blue);font-weight:700;}

/* --- FIX APPLIED HERE --- */
nav {
  display: flex; /* Make links in a row */
  align-items: center; /* Center vertically */
  padding: 0;
  gap: 25px; /* Use gap for consistent spacing between links */
}
/* --- END FIX --- */
nav a{
  position: relative;
  text-decoration: none;
  font-weight: 600;
  font-size: 1rem;
  color: var(--primary-blue);
  /* Removed margin-left: 35px for better centering and used gap above */
  padding: 5px 0;
  transition: color 0.3s ease;
  opacity: 0.8; /* Re-added opacity from original code */
}
nav a:hover{opacity:1; color:var(--accent-teal);}

nav a::after {
  content: '';
  position: absolute;
  left: 0;
  bottom: -3px;
  width: 0;
  height: 3px;
  background: var(--accent-teal);
  border-radius: 2px;
  transition: width 0.3s ease;
}

nav a:hover::after {
  width: 100%;
}

/* Active link highlight */
nav a.active {
  color: var(--accent-teal);
}

nav a.active::after {
  width: 100%;
}
 
/* Hero Section - Highly Structured */
.hero {
  padding: 80px 60px; /* MAXIMUM PADDING */
  border-radius: 24px;
  display: grid;
  grid-template-columns: 2fr 1.2fr; 
  color: white;
  background: linear-gradient(135deg, var(--primary-blue) 0%, #3498db 100%); 
  box-shadow: 0 20px 50px rgba(26, 82, 118, 0.5); 
}
.hero h2{font-family: 'Montserrat', sans-serif; font-size:3rem;margin-bottom:25px;font-weight:800; line-height: 1.2;}
.hero p{font-size: 1.25rem; opacity:0.9; margin-bottom:40px}
.cta-row {
  display: flex;
  gap: 12px; /* space between buttons */
}

@media (max-width: 520px) {
  .cta-row {
    flex-direction: column; /* stack buttons vertically on phones */
    gap: 10px;
  }
}

.btn-primary{
  background: var(--accent-teal); 
  color: var(--primary-blue); 
  padding:18px 36px;
  border-radius:12px;
  font-size: 1.1rem;
  font-weight: 700;
  box-shadow:0 8px 30px rgba(0, 204, 179, 0.4);
}
.btn-primary:hover{transform:translateY(-5px);box-shadow:0 15px 40px rgba(0, 204, 179, 0.6);}
.small-cta{
  background: transparent; 
  border: 2px solid rgba(255,255,255,0.7); 
  color: white; 
  padding: 16px 30px; 
  border-radius: 12px; 
  font-weight: 700;
  font-size: 1.1rem; /* <-- increase font size to match Start Quiz */
}
.small-cta:hover{background:rgba(255,255,255,0.1); transform:translateY(-3px);}

.hero-card{background: var(--card-bg); padding:35px; border-radius:18px; color: var(--text-dark);}
.hero-card h3{color:var(--primary-blue); font-family: 'Montserrat', sans-serif; margin-bottom: 15px;}
.hero-card .features div {padding: 18px; border-radius: 10px; background: var(--bg-main);}
.hero-card .features{gap:25px; margin-top:25px;}
.hero-overlay {
  display: grid;
  grid-template-columns: 1fr 420px;
  gap: 24px;
}

@media (max-width: 520px) {
  .hero-overlay {
    grid-template-columns: 1fr; /* stack content vertically */
  }

  .hero-card {
    margin-top: 20px; /* space above the card */
  }
}
.hidden {
  display: none;
}
/* --- QUIZ SECTION --- */

/* Progress Segment */
.progress-wrap-fixed{padding: 30px 0; background: var(--bg-main); border-bottom: 1px solid var(--border-color);}
.progress-bar-outer-top{width: 90%; max-width: 1400px;}
.progress-bar-inner-top{background: var(--accent-teal); transition: width 0.4s ease-in-out;}

.progress-step-indicator {
  width: 90%; max-width: 1200px; margin: 0 auto 25px;
  padding: 0 15px; /* Add space around the steps */
}
.progress-step {
  width: 35px; height: 35px; 
}
.progress-step.active {background: var(--primary-blue); box-shadow: 0 0 0 6px rgba(26, 82, 118, 0.2);}
.progress-step.complete {background: var(--success);}

/* Question Card - The Centerpiece */
.card{
  margin-top:50px;
  padding:50px; /* MAXIMUM CARD SPACE */
  border-radius:24px;
  background: var(--card-bg);
  box-shadow: var(--shadow-pro); 
}
.quiz-header {margin-bottom: 30px; border-bottom: 1px solid var(--border-color); padding-bottom: 20px;}
.question-text{
  font-family: 'Montserrat', sans-serif; 
  font-size:1.8rem;
  font-weight:700;
  margin-bottom:40px; /* HUGE SPACE BELOW QUESTION */
  color:var(--primary-blue);
}

/* Options - Spacious and Interactive */
.options{
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(350px, 1fr)); /* Adaptive Grid Layout */
  gap:30px; /* MAXIMUM SPACE BETWEEN OPTIONS */
}
label.option{
  padding:30px; /* MAXIMUM OPTION INTERNAL SPACE */
  border-radius:16px;
  border:3px solid var(--border-color);
  font-size: 1.15rem;
  font-weight: 500;
  transition: all 0.3s ease;
  cursor: pointer;
  display: flex;
  align-items: center;
  position: relative;
  user-select: none;
}
label.option:hover{
  transform:translateY(-8px); /* More dramatic lift */
  box-shadow:0 15px 40px rgba(0, 204, 179, 0.2);
  border-color:var(--accent-teal);
}
label.option.selected{
  background: #e6f7f5; /* Light accent background */
  border-color:var(--primary-blue);
  box-shadow:0 8px 30px rgba(26, 82, 118, 0.15);
}
label.option input{
  position: absolute; /* Hide radio visually */
  opacity: 0;
  cursor: pointer;
}

.quiz-actions{margin-top:40px; display: flex; justify-content: space-between; align-items: center;}
.btn-ghost{color: var(--text-muted); border: none;}
.btn-ghost:hover{color: var(--primary-blue); background: var(--bg-main);}
.btn-next{
  padding:16px 32px;
  border-radius:12px;
  background: var(--primary-blue);
  color: white;
  font-size: 1.1rem;
  font-weight: 600;
}
.btn-next:hover{background: #144060; transform:translateY(-3px);}

/* Results Section */
.results-wrap{margin-top:60px;}
.results-grid {
display: grid;
grid-template-columns: 1fr;
gap: 30px;
}

.result-item{
  padding:35px; /* MAXIMUM RESULT SPACE */
  border-radius:20px;
  border-left:12px solid var(--accent-teal); /* Thicker accent line */
  background:var(--card-bg); 
  box-shadow: var(--shadow-pro);
}
.result-item.top-match{
  border-left-color:var(--success); 
  background: #effffb; 
  border: 1px solid var(--success);
}
.result-item h3{font-size:1.8rem; color:var(--primary-blue); margin-bottom:15px; font-family: 'Montserrat', sans-serif;}
.result-item p{margin:10px 0; font-size:1.1rem;}
.major-detail-btn{background:var(--primary-blue); color:white; padding:12px 22px; border-radius:10px; margin-top:25px; font-weight:600;}
.major-detail-btn:hover{background:var(--accent-teal); color: var(--primary-blue);}
.restart-btn{margin-top:40px; padding: 18px 35px; font-size: 1.1rem;}

/* Modal */
.modal-content{padding:60px;border-radius:24px;max-width:800px; box-shadow: 0 10px 50px rgba(0,0,0,0.3);}
.modal-content h4{color:var(--primary-blue);font-size:2.2rem;}

/* Major Info Section */
#major-info{margin-top:80px;padding:50px;background:#eaf0f4; border-radius: 20px;}
.major-grid{
  display: grid;
  
  gap: 50px; /* Bigger spacing between cards */
}
.major-card{padding:30px;border-radius:18px;border-left:8px solid var(--primary-blue); background:var(--card-bg); box-shadow:var(--shadow-pro);}
.major-icon{width:60px;height:60px;background:#eaf0f4; border-radius: 12px; font-size: 1.8rem;}
/* Hide Results header and Restart Quiz button */

#previousResults h3 {
  display: none;
}
/* --- MOBILE FIXES --- */
@media (max-width: 520px){
  .container {
    width: 100%;
    margin: 50px auto 80px;
  }

  /* Hero section */
  .hero {
    grid-template-columns: 1fr;
    padding: 40px 20px;
  }
  .hero h2 { font-size: 2rem; }
  .hero p { font-size: 1rem; }
  .cta-row { flex-direction: column; gap: 10px; }

  /* Quiz card */
  .card { padding: 20px; }
  .question-text { font-size: 1.4rem; }
  .options { grid-template-columns: 1fr; gap: 15px; }

  /* Buttons */
  .btn-next, .btn-ghost { padding: 12px 20px; font-size: 1rem; }

  /* Result / Major cards */
  .result-item, .result-item.top-match { padding: 20px; font-size: 0.95rem; }
  .major-card { padding: 15px; font-size: 0.95rem; }
}
@media (max-width: 520px) {
  .quiz-actions {
    flex-direction: column; /* Stack buttons vertically */
    gap: 15px; /* Space between Previous and Next */
  }

  .quiz-actions div {
    width: 100%; /* Make Next button full width if you want */
  }

  #backBtn, #nextBtn {
    width: 100%; /* Optional: make buttons fill the container */
  }
}
#major-info {
  display: none;
}
.logo-box {
  width: 60px;    /* smaller box */
  height: 70px;      /* smaller box */
  overflow: hidden;
  border-radius: 18px;
  margin: 0;         /* remove default margins */
}

.fit-image {
  width: 120%;        /* fit the box */
  height: 110%;
  object-fit: cover;
  display: block;
}
@media (max-width: 400px) {
  nav a {
    font-size: 14px;
    padding: 6px 8px;
  }
}
.brand {
  display: flex;
  align-items: center; /* vertical center logo and name */
  gap: 10px;           /* space between EC and EduCompass */
}
.site-name{
  font-weight: bold;
}
.features div {
  padding: 15px;        /* your existing padding */
  border-radius: 10px;
  background: var(--bg-main);
  margin-bottom: 20px;  /* ← add this for vertical space */
}

.features div:last-child {
  margin-bottom: 0;     /* remove extra space after the last item */
}



</style>
</head>
<body>

<header>
  <div class="nav-wrap">
    <div class="brand">
      <div class="logo">EC</div>
  <div class="site-name">EduCompass</div>
</div>

    </div>
    <nav>
  <a href="#home" class="active">Home</a>
  <a href="#career">Career</a>
  <a href="#quiz">Quiz</a>
  <a href="#results">Results</a>
</nav>
  </div>
</header>

<main class="container" id="home">
  <section class="hero-overlay hero" aria-labelledby="hero-title">
    <div style="padding:20px">
      <h2 id="hero-title">Discover Your Path <br> With EduCompass</h2>
      <p>Answer 20 quick, scientifically-backed questions about your skills, interests, and personality. Receive personalized, detailed recommendations.</p>
      <div class="cta-row">
        <button class="btn-primary" id="startBtn">Start Quiz Now</button>
        <button class="small-cta" id="exploreAnchor">Explore Full Catalog</button>
      </div>
    </div>

    <aside class="hero-card">
      <h3>Assessment Snapshot</h3>
      <p style="color:var(--text-muted);">This professional tool helps match your profile to university majors and future career skills.</p>
      <div class="features">
        <div><strong>Algorithm:</strong> Advanced Logic (3-point matching)</div>
        <div><strong>Duration:</strong> ~ 5 Minutes</div>
      </div>
    </aside>
  </section>

  <div class="progress-wrap-fixed" id="progressFixedWrap" style="display:none">
    <div class="progress-step-indicator" id="stepIndicator">
      </div>
    <div class="progress-bar-outer-top">
      <div class="progress-bar-inner-top" id="topProgressFixed" style="width:0%"></div>
    </div>
  </div>

  <section class="card" id="quizCard" style="display:none">
    <div class="quiz-header">
      <div class="quiz-title" style="font-size: 1.4rem; font-weight: 700; color: var(--accent-teal);">Major Assessment</div>
      <div style="font-size:1.2rem;font-weight:600;color:var(--primary-blue)" id="progressText">0 / 15 Questions Answered</div>
    </div>
    <div class="question-area">
      <div class="question-text" id="questionText"></div>
      <form id="optionsForm" class="options" onsubmit="return false"></form>
    </div>
    <div class="quiz-actions">
      <button class="btn-ghost" id="backBtn" style="padding: 16px 25px;">← Previous Question</button>
      <div style="display:flex; gap:20px;">
        <button class="btn-next" id="nextBtn">Next Question →</button>
      </div>
    </div>
    
    <div class="results-wrap" id="resultsWrap" style="display:none">
      <h3 style="color:var(--primary-blue);margin-bottom:40px; font-size: 2.2rem;">Your Top Recommended Majors 🏆</h3>
      <div class="results-grid" id="resultsGrid"></div>
      <button class="restart-btn btn-primary" id="restartBtn" style="background: #dc3545; box-shadow: 0 8px 20px rgba(220, 53, 69, 0.3);">Start Over</button>
    </div>
    <div id="previousResults" style="margin-top:30px;">
  <h3>Previous Results</h3>
  <div id="historyGrid" style="display:flex; flex-direction:column; gap:15px;"></div>
</div>

  </section>

  <section id="major-info" aria-hidden="true">
    <h3 style="text-align:center;color:var(--primary-blue);margin-bottom:40px;font-size:2.4rem; font-family: 'Montserrat', sans-serif;">Full Major Catalog & Details</h3>
    <div class="major-grid" id="majorGrid"></div>
  </section>

  <section id="major-info" style="display:none;" aria-hidden="true">
  <h3 style="text-align:center;color:var(--primary-blue);margin-bottom:40px;font-size:2.4rem; font-family: 'Montserrat', sans-serif;">Full Major Catalog & Details</h3>
  <div class="major-grid" id="majorGrid"></div>
</section>

  
</main>

<footer style="text-align:center;padding: 40px 0;color:white;background:var(--primary-blue);font-weight:500; font-size: 0.9rem;">© 2025 EduCompass — Major Recommendation System. All Rights Reserved.</footer>



<script>
  // --- DATA (Unchanged) ---
   const questions = [
    { q:"1) Which activity appeals to you most?", o:["Writing code","Starting a business","Helping people","Creating visuals","Running experiments","Exploring new technologies"]},
    { q:"2) Which skill fits you best?", o:["Logical thinking","Leadership & organizing","Empathy & listening","Creative design","Analytical reasoning","Adaptability & problem-solving"]},
    { q:"3) Preferred daily task?", o:["Debugging a program","Managing a team","Counseling someone","Sketching concepts","Collecting data","Learning something new"]},
    { q:"4) Which classroom subject do you like most?", o:["Math","Economics","Psychology","Art","Biology","Computer Science"]},
    { q:"5) How do you prefer to solve problems?", o:["Write code or tools","Plan & coordinate","Talk & support","Try visual ideas","Research & test","Experiment & iterate"]},
    { q:"6) Which tool do you enjoy using?", o:["Computer/IDE","Spreadsheets/Slides","Notebooks & reports","Design software","Lab equipment","Online resources / simulations"]},
    { q:"7) What environment fits you?", o:["Office/Tech team","Startup/Business","Community center","Studio/Workshop","Laboratory","Remote / flexible work"]},
    { q:"8) Which future job sounds exciting?", o:["AI Engineer","Founder/Manager","Social worker","Graphic Designer","Research Scientist","Entrepreneur / Innovator"]},
    { q:"9) How do you make decisions?", o:["Data-driven","Vision & risk","Heart & care","Aesthetic sense","Evidence-based","Balanced / flexible approach"]},
    { q:"10) Your work style?", o:["Independent coding","Leading groups","Empathetic helping","Collaborative design","Methodical research","Adaptive & versatile"]},
    { q:"11) What motivates you?", o:["Building systems","Business growth","Making people's lives better","Creating beauty","Discovering new knowledge","Learning new skills"]},
    { q:"12) Which elective would you choose?", o:["Algorithms","Entrepreneurship","Counseling","Digital Illustration","Molecular Biology","Psychology or Human Behavior"]},
    { q:"13) How do you measure success?", o:["Working systems","Revenue/impact","Lives improved","Portfolio & exhibitions","Published findings","Personal growth & learning"]},
    { q:"14) Team role you prefer?", o:["Backend/Engineer","Project Lead","Care Coordinator","Creative Lead","Research Analyst","Support / versatile role"]},
    { q:"15) Which short internship appeals to you?", o:["Software dev intern","Business analyst intern","NGO outreach intern","Design studio intern","Lab assistant intern","Startup / innovation intern"]},
    { q:"16) Which problem would you like to solve?", o:["Optimize a program","Scale a business","Improve community health","Design a new product","Research scientific question","Develop sustainable tech"]},
    { q:"17) Which learning style suits you?", o:["Hands-on coding","Workshops & case studies","Mentorship & counseling","Studio practice","Lab experiments","Project-based learning"]},
    { q:"18) Preferred communication style?", o:["Technical reports","Business presentations","Empathetic conversation","Visual storytelling","Data presentations","Innovative pitches"]},
    { q:"19) Favorite extracurricular?", o:["Coding club","Entrepreneur club","Volunteer/NGO work","Art/Music club","Science club","Innovation & hackathons"]},
    { q:"20) Which future skill excites you most?", o:["AI & Machine Learning","Business Strategy","Social Impact & Policy","Design Thinking","Research & Data Analysis","Entrepreneurship & Innovation"]}
  ];

  const majors = [
    { id:"cs", name:"Computer Science", careers:"Software Developer, Data Scientist, AI Engineer", answers:["Writing code","Logical thinking","Debugging a program","Math","Write code or tools","Computer/IDE","Office/Tech team","AI Engineer","Data-driven","Independent coding","Building systems","Algorithms","Working systems","Backend/Engineer","Software dev intern","Optimize a program","Hands-on coding","Technical reports","Coding club","AI & Machine Learning"], color:"#007bff", icon:"💻" },
    { id:"is", name:"Information Systems", careers:"Systems Analyst, IT Consultant, Business Analyst", answers:["Writing code","Analytical reasoning","Collecting data","Math","Research & test","Computer/IDE","Office/Tech team","Research Scientist","Data-driven","Methodical research","Building systems","Algorithms","Working systems","Research Analyst","Software dev intern","Develop sustainable tech","Project-based learning","Data presentations","Science club","Research & Data Analysis"], color:"#00bcd4", icon:"🖥️" },
    { id:"bus", name:"Business Administration", careers:"Manager, Entrepreneur, Business Analyst", answers:["Starting a business","Leadership & organizing","Managing a team","Economics","Plan & coordinate","Spreadsheets/Slides","Startup/Business","Founder/Manager","Vision & risk","Leading groups","Business growth","Entrepreneurship","Revenue/impact","Project Lead","Business analyst intern","Scale a business","Workshops & case studies","Business presentations","Entrepreneur club","Business Strategy"], color:"#ff9f1c", icon:"💼" },
    { id:"sw", name:"Social Work / Public Health", careers:"Social Worker, Counselor, Public Health Officer", answers:["Helping people","Empathy & listening","Counseling someone","Psychology","Talk & support","Notebooks & reports","Community center","Social worker","Heart & care","Empathetic helping","Making people's lives better","Counseling","Lives improved","Care Coordinator","NGO outreach intern","Improve community health","Mentorship & counseling","Empathetic conversation","Volunteer/NGO work","Social Impact & Policy"], color:"#28a745", icon:"🤝" },
    { id:"gd", name:"Graphic Design / Arts", careers:"Graphic Designer, UI/UX Designer, Illustrator", answers:["Creating visuals","Creative design","Sketching concepts","Art","Try visual ideas","Design software","Studio/Workshop","Graphic Designer","Aesthetic sense","Collaborative design","Creating beauty","Digital Illustration","Portfolio & exhibitions","Creative Lead","Design studio intern","Design a new product","Studio practice","Visual storytelling","Art/Music club","Design Thinking"], color:"#fd7e14", icon:"🎨" },
    { id:"bio", name:"Biology / Life Sciences", careers:"Research Scientist, Lab Technician, Environmental Biologist", answers:["Running experiments","Analytical reasoning","Collecting data","Biology","Research & test","Lab equipment","Laboratory","Research Scientist","Evidence-based","Methodical research","Discovering new knowledge","Molecular Biology","Published findings","Research Analyst","Lab assistant intern","Research scientific question","Lab experiments","Data presentations","Science club","Research & Data Analysis"], color:"#17a2b8", icon:"🔬" },
    { id:"eng", name:"Engineering", careers:"Civil Engineer, Project Engineer, Mechanical Designer", answers:["Running experiments","Analytical reasoning","Collecting data","Math","Research & test","Lab equipment","Laboratory","Research Scientist","Evidence-based","Methodical research","Discovering new knowledge","Molecular Biology","Published findings","Research Analyst","Lab assistant intern","Develop sustainable tech","Project-based learning","Data presentations","Innovation & hackathons","Entrepreneurship & Innovation"], color:"#6f42c1", icon:"🛠️" },
    { id:"law", name:"Law", careers:"Lawyer, Legal Advisor, Policy Analyst", answers:["Helping people","Analytical reasoning","Researching cases","History/Politics","Talk & support","Notebooks & reports","Office","Policy Advisor","Evidence-based","Methodical research","Social impact","Legal Studies","Lives improved","Care Coordinator","NGO outreach intern","Policy problem-solving","Workshops & case studies","Analytical reports","Volunteer/NGO work","Social Impact & Policy"], color:"#ff0066", icon:"⚖️" },
    { id:"edu", name:"Education / Teaching", careers:"Teacher, Curriculum Designer, Education Consultant", answers:["Helping people","Leadership & organizing","Teaching others","Psychology/Education","Plan & coordinate","Notebooks & reports","Classroom/Online","Teacher","Heart & care","Empathetic helping","Impact student learning","Pedagogy","Lives improved","Project Lead","NGO outreach intern","Mentorship & counseling","Workshops & case studies","Empathetic conversation","Volunteer/NGO work","Personal growth & learning"], color:"#6c757d", icon:"📚" },
    { id:"env", name:"Natural Resource Management", careers:"Environmental Analyst, Conservationist, Sustainability Officer", answers:["Running experiments","Analytical reasoning","Collecting data","Biology/Earth Science","Research & test","Lab equipment","Fieldwork","Environmental Scientist","Evidence-based","Methodical research","Discovering new knowledge","Ecology","Published findings","Research Analyst","Lab assistant intern","Develop sustainable tech","Project-based learning","Data presentations","Innovation & hackathons","Entrepreneurship & Innovation"], color:"#28a745", icon:"🌱" },
    { id:"music", name:"Art and Literature", careers:"Musician, Performer, Composer", answers:["Creating visuals","Creative design","Performing","Art/Music","Try visual ideas","Studio/Workshop","Stage/Studio","Performer","Aesthetic sense","Collaborative design","Creating beauty","Music Theory","Portfolio & exhibitions","Creative Lead","Design studio intern","Compose & perform","Studio practice","Visual storytelling","Art/Music club","Design Thinking"], color:"#ff33cc", icon:"🎵" }
  ];

  // --- majorsInfo can also be expanded similarly ---
  const majorsInfo = majors.map(m => ({
    id: m.id,
    title: m.name,
    about: `Explore ${m.name}, careers include: ${m.careers}.`,
    careers: m.careers,
    skills: "Relevant skills for this major",
    icon: m.icon,
    topics: "Core topics for this major"
  }));
  // --- DOM Elements & State (unchanged) ---
  const startBtn = document.getElementById('startBtn');
  const exploreAnchor = document.getElementById('exploreAnchor');
  const quizCard = document.getElementById('quizCard');
  const questionText = document.getElementById('questionText');
  const optionsForm = document.getElementById('optionsForm');
  const nextBtn = document.getElementById('nextBtn');
  const backBtn = document.getElementById('backBtn');
  const restartBtn = document.getElementById('restartBtn');
  const resultsWrap = document.getElementById('resultsWrap');
  const resultsGrid = document.getElementById('resultsGrid');
  const topProgressFixed = document.getElementById('topProgressFixed');
  const progressText = document.getElementById('progressText');
  const majorInfoSection = document.getElementById('major-info');
  const majorGrid = document.getElementById('majorGrid');
  const majorModal = document.getElementById('majorModal');
  const modalClose = document.querySelector('.modal-close');
  const closeModalBtn = document.getElementById('closeModalBtn');
  const stepIndicator = document.getElementById('stepIndicator');

  let currentIndex = 0;
  let selectedAnswers = Array(questions.length).fill(null);
  let scores = Array(majors.length).fill(0);
  const maxPossibleScore = questions.length * 3;

  // --- Functions ---

  function renderStepIndicator() {
    stepIndicator.innerHTML = '';
    const totalSteps = questions.length;
    const indicatorInner = document.createElement('div');
    indicatorInner.style.display = 'flex';
    indicatorInner.style.justifyContent = 'space-between';
    indicatorInner.style.alignItems = 'center';
    indicatorInner.style.width = '100%';
    
    for (let i = 0; i < totalSteps; i++) {
      const dot = document.createElement('div');
      dot.style.width = '15px';
      dot.style.height = '15px';
      dot.style.borderRadius = '50%';
      dot.style.transition = 'all 0.3s ease';
      dot.style.flexShrink = 0;
      dot.style.zIndex = 2;
      
      if (i < currentIndex) {
        dot.style.background = 'var(--success)';
      } else if (i === currentIndex) {
        dot.style.background = 'var(--primary-blue)';
        dot.style.transform = 'scale(1.4)';
        dot.style.boxShadow = '0 0 0 4px rgba(26, 82, 118, 0.1)';
      } else {
        dot.style.background = 'var(--border-color)';
      }
      
      indicatorInner.appendChild(dot);

      if (i < totalSteps - 1) {
          const line = document.createElement('div');
          line.style.height = '2px';
          line.style.flexGrow = 1;
          line.style.background = i < currentIndex ? 'var(--success)' : 'var(--border-color)';
          line.style.margin = '0 5px';
          line.style.transition = 'background 0.3s ease';
          indicatorInner.appendChild(line);
      }
    }
    stepIndicator.appendChild(indicatorInner);
  }

  function updateProgress(){
    const percent = (currentIndex / questions.length) * 100;
    progressText.innerText = `${currentIndex} / ${questions.length} Questions Answered`;
    topProgressFixed.style.width = percent + '%';
    
    backBtn.disabled = currentIndex === 0;
    backBtn.style.opacity = currentIndex === 0 ? 0.4 : 1;
    
    nextBtn.textContent = (currentIndex === questions.length - 1) ? "View Results" : "Next Question →";
    
    renderStepIndicator();
  }

  function handleOptionSelection(label, input, opt, idx) {
    document.querySelectorAll('.option').forEach(el => el.classList.remove('selected'));
    label.classList.add('selected');
    input.checked = true;
    selectedAnswers[idx] = opt;
    // Optional: Auto-advance after selection for faster UX
    // setTimeout(() => nextBtn.click(), 300); 
  }

  function renderQuestion(idx){
    const q = questions[idx];
    questionText.textContent = q.q;
    optionsForm.innerHTML = '';
    
    q.o.forEach((opt)=>{
      const id = `q${idx}_opt${opt.replace(/\W/g, '')}`;
      const label = document.createElement('label');
      label.className = 'option';
      label.setAttribute('for', id); // Crucial for accessibility and large click target
      
      const input = document.createElement('input');
      input.type = 'radio';
      input.name = 'q';
      input.value = opt;
      input.id = id;
      
      if(selectedAnswers[idx] === opt){
        input.checked = true;
        label.classList.add('selected');
      }

      // **THE FIX**: Attach the selection handler directly to the label click
      label.addEventListener('click', (e) => {
        // Prevent default behavior if the input itself is the target to avoid double handling
        if (e.target.tagName !== 'INPUT') {
            handleOptionSelection(label, input, opt, idx);
        }
      });
      // Also attach to input change for robustness
      input.addEventListener('change', () => {
          handleOptionSelection(label, input, opt, idx);
      });

      label.appendChild(input);
      // Create a visible span for the text
      const textSpan = document.createElement('span');
      textSpan.textContent = opt;
      textSpan.style.marginLeft = '10px';
      label.appendChild(textSpan);
      
      optionsForm.appendChild(label);
    });
    
    updateProgress();
    quizCard.scrollIntoView({behavior:'smooth', block:'start'}); 
  }

  function computeScores(){
    scores = scores.map(()=>0);
    majors.forEach((major, mIdx)=>{
      major.answers.forEach((expected, qIdx)=>{
        if(!selectedAnswers[qIdx]) return;
        
        const sel = selectedAnswers[qIdx].toLowerCase();
        const exp = expected.toLowerCase();
        
        if(sel === exp){ 
          scores[mIdx] += 3; 
        } else {
          const selTokens = sel.split(/[\s\/&]+/).filter(Boolean);
          const expTokens = exp.split(/[\s\/&]+/).filter(Boolean);
          
          if(selTokens.some(token => expTokens.includes(token))) {
             scores[mIdx] += 1; 
          }
        }
      });
    });
  }

  function showResults(){
    document.getElementById('optionsForm').innerHTML = '';
    nextBtn.style.display = 'none';
    backBtn.style.display = 'none';
    document.getElementById('quizCard').querySelector('.quiz-actions').style.display = 'none';
    resultsWrap.style.display = 'block';
    resultsGrid.innerHTML = '';
    
    const ranking = majors.map((m, i)=>({major:m, score:scores[i]})).sort((a,b)=>b.score-a.score);
    
    ranking.slice(0,3).forEach((item, index)=>{
      const matchPercent = ((item.score / maxPossibleScore) * 100).toFixed(0);
      const div = document.createElement('div');
      div.className = 'result-item';
      if(index === 0) div.classList.add('top-match'); 
      
      div.innerHTML = `<h3>${item.major.icon} ${item.major.name}</h3>
      <p><strong>Top Careers:</strong> ${item.major.careers}</p>
      <p><strong>Match Score:</strong> ${matchPercent}% (${item.score.toFixed(1)} / ${maxPossibleScore}.0 points)</p>
      <button class="major-detail-btn" data-major-id="${item.major.id}">View Full Details</button>`;
      
      resultsGrid.appendChild(div);
    });

    updateProgress(); 
    restartBtn.style.display = 'inline-block';
    resultsWrap.scrollIntoView({behavior:'smooth'});
  }

  function renderMajorsInfo(){
    majorGrid.innerHTML = '';
    majorsInfo.forEach(m=>{
      const card = document.createElement('div');
      card.className = 'major-card';
      card.innerHTML = `
        <div style="display:flex;align-items:center;gap:15px;margin-bottom:15px">
          <div class="major-icon" style="display:flex; justify-content:center; align-items:center;">${m.icon}</div>
          <div style="font-weight:700; font-size:1.3rem; color:var(--primary-blue); font-family: 'Montserrat', sans-serif;">${m.title}</div>
        </div>
        <p style="color:var(--text-muted); margin-bottom:18px;">${m.about}</p>
        <div class="major-meta" style="font-size: 0.95rem;"><strong>Top Careers:</strong> ${m.careers}</div>
        <div class="major-meta" style="font-size: 0.95rem;"><strong>Key Skills:</strong> ${m.skills}</div>
      `;
      majorGrid.appendChild(card);
    });
  }
  renderMajorsInfo();


  // --- Event Listeners ---
  
  startBtn.addEventListener('click', ()=>{
    document.getElementById('home').scrollIntoView({behavior:'smooth'});
    quizCard.style.display = 'block';
    document.getElementById('progressFixedWrap').style.display = 'block';
    majorInfoSection.style.display = 'none';
    resultsWrap.style.display = 'none';
    nextBtn.style.display = 'inline-block';
    backBtn.style.display = 'inline-block';
    document.getElementById('quizCard').querySelector('.quiz-actions').style.display = 'flex';
    currentIndex = 0; 
    renderQuestion(currentIndex);
  });

  exploreAnchor.addEventListener('click', (e)=> {
    e.preventDefault();
    majorInfoSection.style.display = majorInfoSection.style.display === 'block' ? 'none' : 'block';
    majorInfoSection.scrollIntoView({behavior:'smooth'});
  });

  nextBtn.addEventListener('click', ()=>{
    const checked = document.querySelector('input[name="q"]:checked');
    if(!checked){ alert('Please select an option before continuing.'); return; }
    
    // The selection is already saved by the new handler, but we ensure it here
    selectedAnswers[currentIndex] = checked.value;
    currentIndex++;
    
    if(currentIndex >= questions.length){ 
      computeScores(); 
      showResults(); 
      return; 
    }
    
    renderQuestion(currentIndex);
  });

  backBtn.addEventListener('click', ()=>{
    if(currentIndex > 0){
      // Save current selection before moving back
      const currentSelection = document.querySelector('input[name="q"]:checked');
      if(currentSelection) {
        selectedAnswers[currentIndex] = currentSelection.value;
      }
      
      currentIndex--;
      renderQuestion(currentIndex);
    }
  });

  restartBtn.addEventListener('click', ()=>{
    currentIndex = 0; selectedAnswers = Array(questions.length).fill(null); scores = Array(majors.length).fill(0);
    resultsWrap.style.display = 'none';
    nextBtn.style.display = 'inline-block';
    backBtn.style.display = 'inline-block';
    document.getElementById('quizCard').querySelector('.quiz-actions').style.display = 'flex';
    renderQuestion(currentIndex);
    window.scrollTo({top:0, behavior:'smooth'});
  });

  modalClose.addEventListener('click', () => { majorModal.style.display = 'none'; });
  closeModalBtn.addEventListener('click', () => { majorModal.style.display = 'none'; });
  window.addEventListener('click', (e) => {
    if (e.target === majorModal) {
      majorModal.style.display = 'none';
    }
  });
  
  renderStepIndicator();
  function handleOptionSelection(label, input, opt, idx) {
    document.querySelectorAll('.option').forEach(el => el.classList.remove('selected'));
    label.classList.add('selected');
    input.checked = true;
    selectedAnswers[idx] = opt;

    // Only scroll on small screens (e.g., phones)
    if (window.innerWidth <= 520) { 
        document.querySelector('#quizCard .quiz-actions').scrollIntoView({ behavior: 'smooth', block: 'start' });
    }
}

  
</script>

</body>
</html>
