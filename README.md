<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>CNC Tech Hindi | Learn • Practice • Perfect</title>
<style>
:root{
  --bg:#080808;--bg2:#0d0d0d;--card:#151515;--card2:#1b1b1b;
  --text:#fff;--muted:#9b9b9b;--red:#e50914;--red2:#ff2934;
  --border:rgba(255,255,255,.09);--max:1250px
}
*{margin:0;padding:0;box-sizing:border-box;scroll-behavior:smooth}
body{font-family:Arial,Helvetica,sans-serif;background:var(--bg);color:var(--text);line-height:1.6}
a{text-decoration:none;color:inherit}.container{width:min(92%,var(--max));margin:auto}
header{position:fixed;top:0;left:0;width:100%;z-index:1000;background:rgba(8,8,8,.9);backdrop-filter:blur(14px);border-bottom:1px solid var(--border)}
.nav{height:76px;display:flex;align-items:center;justify-content:space-between}
.logo{display:flex;align-items:center;gap:12px;font-weight:800}
.logo-mark{width:42px;height:42px;border:2px solid var(--red);border-radius:50%;display:grid;place-items:center;color:var(--red);font-weight:900}
.logo-text span{color:var(--red)}.logo-text small{display:block;color:#888;font-size:9px;letter-spacing:2px}
.nav-links{display:flex;gap:24px;align-items:center}.nav-links a{color:#ddd;font-size:14px}.nav-links a:hover{color:var(--red)}
.menu-btn{display:none;border:0;background:none;color:#fff;font-size:27px;cursor:pointer}
.hero{min-height:100vh;padding-top:76px;display:flex;align-items:center;overflow:hidden;background:radial-gradient(circle at 75% 40%,rgba(229,9,20,.16),transparent 32%),linear-gradient(135deg,#080808,#111)}
.hero-grid{display:grid;grid-template-columns:1.05fr .95fr;gap:50px;align-items:center}
.badge,.tag{color:#ff5961;text-transform:uppercase;font-size:12px;font-weight:800;letter-spacing:2px}
.badge{display:inline-flex;padding:7px 13px;border:1px solid rgba(229,9,20,.4);border-radius:30px;background:rgba(229,9,20,.06);margin-bottom:20px}
.hero h1{font-size:clamp(42px,6vw,78px);line-height:1.02;margin-bottom:22px}.hero h1 span{color:var(--red)}
.hero p{color:var(--muted);max-width:650px;font-size:18px;margin-bottom:30px}
.buttons{display:flex;gap:14px;flex-wrap:wrap}.btn{padding:13px 22px;border-radius:7px;font-weight:700;font-size:14px;transition:.25s;border:1px solid transparent;cursor:pointer}
.btn-primary{background:var(--red);color:#fff}.btn-primary:hover{background:var(--red2);transform:translateY(-2px)}
.btn-outline{border-color:#444;color:#fff}.btn-outline:hover{border-color:var(--red);color:var(--red)}
.machine-hero{min-height:430px;border:1px solid var(--border);border-radius:22px;background:linear-gradient(145deg,rgba(255,255,255,.04),rgba(255,255,255,.01));display:flex;align-items:center;justify-content:center}
.machine-graphic{width:82%;height:250px;border:3px solid #555;border-radius:15px;position:relative;background:linear-gradient(145deg,#242424,#101010);box-shadow:0 30px 70px rgba(0,0,0,.7)}
.machine-graphic:before{content:"CNC";position:absolute;left:25px;top:20px;font-size:42px;font-weight:900;color:#333}
.machine-screen{position:absolute;right:25px;top:25px;width:100px;height:65px;border:3px solid #555;background:#080808}
.machine-spindle{position:absolute;left:50%;top:75px;width:55px;height:110px;transform:translateX(-50%);background:#555;border-radius:8px}
.machine-spindle:after{content:"";position:absolute;bottom:-45px;left:20px;width:15px;height:55px;background:var(--red)}
.machine-base{position:absolute;left:20px;right:20px;bottom:20px;height:35px;background:#333}
section{padding:95px 0}.section-head{text-align:center;max-width:780px;margin:0 auto 50px}
.section-head h2{font-size:clamp(30px,4vw,48px);margin:10px 0}.section-head p{color:var(--muted)}
.categories,.machine-library,.code-section,.calculator{background:var(--bg2)}
.grid{display:grid;grid-template-columns:repeat(4,1fr);gap:18px}
.card{background:var(--card);border:1px solid var(--border);border-radius:14px;padding:25px;transition:.3s;position:relative;overflow:hidden;cursor:pointer}
.card:before{content:"";position:absolute;top:0;left:0;width:100%;height:2px;background:var(--red);transform:scaleX(0);transform-origin:left;transition:.3s}
.card:hover{transform:translateY(-6px);border-color:rgba(229,9,20,.4)}.card:hover:before{transform:scaleX(1)}
.icon{width:48px;height:48px;border-radius:10px;display:grid;place-items:center;background:rgba(229,9,20,.1);color:#ff5961;font-size:22px;margin-bottom:18px}
.card h3{margin-bottom:8px}.card p{color:#929292;font-size:14px}.card-link{display:inline-block;margin-top:18px;color:var(--red);font-size:13px;font-weight:700}
.topic-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:18px}.topic{background:linear-gradient(145deg,#171717,#101010);border:1px solid var(--border);border-radius:15px;padding:24px}
.topic h3{margin:8px 0}.topic ul{list-style:none;margin-top:14px}.topic li{padding:6px 0;color:#aaa;font-size:14px;border-bottom:1px solid rgba(255,255,255,.05)}
.code-box{max-width:950px;margin:auto;border:1px solid var(--border);border-radius:16px;overflow:hidden;background:#0b0b0b}
.code-top{display:flex;justify-content:space-between;padding:15px 20px;border-bottom:1px solid var(--border)}
.dots{display:flex;gap:6px}.dots i{width:9px;height:9px;border-radius:50%;background:#444}
pre{padding:25px;overflow:auto;color:#ddd;font-size:14px;line-height:1.8}.code-key{color:#ff5961}
.about{background:#080808}.about-grid{display:grid;grid-template-columns:.75fr 1.25fr;gap:60px;align-items:center}
.profile{min-height:390px;border-radius:20px;border:1px solid var(--border);background:radial-gradient(circle at center,rgba(229,9,20,.15),transparent 50%),#121212;display:grid;place-items:center}
.profile-circle{width:210px;height:210px;border-radius:50%;border:2px solid var(--red);display:grid;place-items:center;font-size:55px;font-weight:900;color:var(--red)}
.about h2{font-size:42px;margin:10px 0 20px}.about h2 span{color:var(--red)}.about p{color:#aaa;margin-bottom:17px}
.skills{display:flex;flex-wrap:wrap;gap:8px;margin:20px 0}.skill{padding:7px 11px;border:1px solid #333;border-radius:5px;font-size:12px;color:#ccc}
.calc{max-width:700px;margin:auto;background:#151515;padding:30px;border:1px solid var(--border);border-radius:16px}.calc-grid{display:grid;grid-template-columns:1fr 1fr;gap:15px}
.calc label{display:block;color:#999;font-size:13px;margin-bottom:5px}.calc input{width:100%;padding:12px;background:#0b0b0b;color:#fff;border:1px solid #333;border-radius:6px;outline:none}
.calc input:focus{border-color:var(--red)}.result{margin-top:20px;padding:20px;border-radius:10px;background:#0b0b0b;border-left:3px solid var(--red)}.result strong{color:var(--red);font-size:25px}
.social{text-align:center;background:radial-gradient(circle at center,rgba(229,9,20,.12),transparent 50%),#080808}.social h2{font-size:42px}.social p{color:#999;max-width:600px;margin:10px auto 25px}
footer{background:#050505;border-top:1px solid var(--border);padding:55px 0 20px}.footer-grid{display:grid;grid-template-columns:1.4fr 1fr 1fr 1fr;gap:35px}
footer h4{margin-bottom:15px}footer p,footer a{color:#858585;font-size:14px}footer a{display:block;margin:7px 0}footer a:hover{color:var(--red)}
.copyright{text-align:center;color:#555;font-size:12px;border-top:1px solid #181818;margin-top:35px;padding-top:20px}

/* machine library */
.machine-filter{display:flex;justify-content:center;gap:10px;flex-wrap:wrap;margin-bottom:35px}
.filter-btn{background:#151515;color:#aaa;border:1px solid #333;padding:9px 17px;border-radius:6px;cursor:pointer}
.filter-btn:hover,.filter-btn.active{background:var(--red);color:#fff;border-color:var(--red)}
.machine-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:18px}
.machine-card-item{background:linear-gradient(145deg,#181818,#101010);border:1px solid #292929;border-radius:15px;padding:25px;cursor:pointer;transition:.3s;position:relative;overflow:hidden}
.machine-card-item:before{content:"";position:absolute;left:0;top:0;width:100%;height:2px;background:var(--red);transform:scaleX(0);transform-origin:left;transition:.3s}
.machine-card-item:hover{transform:translateY(-6px);border-color:var(--red)}.machine-card-item:hover:before{transform:scaleX(1)}
.machine-icon{width:52px;height:52px;display:grid;place-items:center;border-radius:11px;background:rgba(229,9,20,.1);font-size:24px;margin-bottom:18px}
.machine-card-item h3{font-size:20px;margin-bottom:8px}.machine-card-item p{color:#999;font-size:14px;min-height:65px}
.axis-badge{display:inline-block;margin-top:15px;padding:6px 9px;border-radius:5px;background:#101010;border:1px solid #333;color:#ddd;font-size:11px}
.machine-more{display:block;margin-top:18px;color:var(--red);font-size:13px;font-weight:700}

/* modal */
.machine-modal{position:fixed;inset:0;z-index:3000;background:rgba(0,0,0,.88);backdrop-filter:blur(10px);display:none;overflow-y:auto;padding:35px 15px}
.machine-modal.show{display:block}.machine-detail{width:min(100%,1000px);margin:auto;background:#111;border:1px solid #333;border-radius:20px;padding:35px;position:relative}
.close-machine{position:absolute;top:15px;right:18px;width:42px;height:42px;border-radius:50%;border:1px solid #444;background:#181818;color:#fff;font-size:28px;cursor:pointer}
.detail-header{display:flex;align-items:center;gap:20px;padding-right:50px;margin-bottom:30px}.detail-icon{width:75px;height:75px;display:grid;place-items:center;border-radius:16px;background:rgba(229,9,20,.12);font-size:34px}
.detail-header h2{font-size:clamp(30px,5vw,48px);margin:3px 0}.detail-header p{color:#999;max-width:650px}
.detail-highlight{display:grid;grid-template-columns:1fr 1fr;gap:15px;margin-bottom:25px}.detail-highlight>div{background:#181818;border:1px solid #292929;padding:20px;border-radius:12px}
.detail-highlight small{display:block;color:var(--red);font-size:10px;letter-spacing:1px;margin-bottom:5px}.detail-section{margin-top:25px;padding-top:25px;border-top:1px solid #242424}
.detail-section h3{margin-bottom:15px;font-size:20px}.detail-section p{color:#999}.detail-list{display:flex;flex-wrap:wrap;gap:9px}.detail-list span{padding:8px 11px;background:#181818;border:1px solid #303030;border-radius:6px;color:#bbb;font-size:13px}

/* detailed learning page inside modal */
.subtopic-grid{display:grid;grid-template-columns:repeat(2,1fr);gap:12px;margin-top:15px}
.subtopic{background:#161616;border:1px solid #292929;border-radius:10px;padding:15px}.subtopic b{display:block;margin-bottom:5px}.subtopic span{color:#999;font-size:13px}
.axis-diagram{margin-top:18px;background:#090909;border:1px solid #292929;border-radius:12px;padding:20px;text-align:center}
.axis-line{height:2px;background:#555;margin:18px auto;max-width:500px;position:relative}.axis-line:after{content:"X →";position:absolute;right:-10px;top:-13px;color:var(--red);font-weight:700}
.axis-z:after{content:"Z →"}.axis-note{color:#999;font-size:13px}


.library-search{display:flex;justify-content:flex-end;margin:0 0 18px}
.library-search input{width:min(100%,360px);padding:12px 15px;border:1px solid #333;border-radius:8px;background:#151515;color:#fff;outline:none}
.library-search input:focus{border-color:var(--red)}
.topic-modal{position:fixed;inset:0;z-index:3200;background:rgba(0,0,0,.9);backdrop-filter:blur(10px);display:none;overflow-y:auto;padding:35px 15px}
.topic-modal.show{display:block}
.topic-detail{width:min(100%,1050px);margin:auto;background:#111;border:1px solid #333;border-radius:20px;padding:34px;position:relative}
.topic-detail h2{font-size:clamp(30px,5vw,48px);margin:8px 0}
.topic-detail .lead{color:#999;max-width:800px}
.topic-close{position:absolute;right:18px;top:15px;width:42px;height:42px;border-radius:50%;background:#181818;border:1px solid #444;color:#fff;font-size:28px;cursor:pointer}
.learning-columns{display:grid;grid-template-columns:repeat(2,1fr);gap:14px;margin-top:22px}
.learning-box{background:#161616;border:1px solid #292929;border-radius:12px;padding:18px}
.learning-box h3{margin-bottom:9px}
.learning-box ul{list-style:none}
.learning-box li{padding:6px 0;color:#aaa;border-bottom:1px solid #242424;font-size:14px}
.learning-box li:last-child{border-bottom:0}

.gdt-item{display:flex;justify-content:space-between;align-items:center;cursor:pointer;transition:.2s}
.gdt-item:hover{color:#fff;padding-left:5px}
.gdt-item span{color:var(--red);font-weight:800}
.gdt-detail-hero{display:grid;grid-template-columns:120px 1fr;gap:22px;align-items:center;background:linear-gradient(145deg,#181818,#101010);border:1px solid #292929;border-radius:14px;padding:22px;margin-top:22px}
.gdt-symbol-box{width:110px;height:110px;border:1px solid #3a3a3a;border-radius:12px;display:grid;place-items:center;background:#0b0b0b}
.gdt-symbol-mark{font-size:52px;color:#fff;font-weight:800}
.gdt-table{width:100%;border-collapse:collapse;margin-top:15px}
.gdt-table td{padding:11px 10px;border-bottom:1px solid #292929;vertical-align:top}
.gdt-table td:first-child{width:35%;color:#e50914;font-weight:700}
.gdt-example{background:#090909;border:1px solid #292929;border-radius:12px;padding:18px;margin-top:18px}
.fcf{display:inline-flex;align-items:center;background:#fff;color:#111;border:2px solid #111;margin:12px 0;padding:0;font-weight:800}
.fcf span{padding:8px 14px;border-right:2px solid #111}
.measure-steps{counter-reset:step;list-style:none;padding:0;margin-top:12px}
.measure-steps li{counter-increment:step;display:flex;gap:10px;padding:9px 0;color:#aaa}
.measure-steps li:before{content:counter(step);min-width:26px;height:26px;border-radius:50%;display:grid;place-items:center;background:rgba(229,9,20,.15);color:#ff5961;font-weight:800}
.gdt-symbol{font-size:44px;color:var(--red);font-weight:800}
.search-empty{grid-column:1/-1;text-align:center;color:#888;padding:35px}

/* responsive */
@media(max-width:950px){
 .nav-links{position:absolute;top:76px;left:0;width:100%;background:#0b0b0b;flex-direction:column;padding:25px;display:none;border-bottom:1px solid var(--border)}
 .nav-links.active{display:flex}.menu-btn{display:block}.hero-grid,.about-grid{grid-template-columns:1fr}
 .grid{grid-template-columns:repeat(2,1fr)}.topic-grid{grid-template-columns:1fr 1fr}.footer-grid{grid-template-columns:1fr 1fr}
 .machine-grid{grid-template-columns:1fr 1fr}
}
@media(max-width:600px){
 section{padding:70px 0}.hero{min-height:auto;padding-top:130px;padding-bottom:70px}.hero h1{font-size:43px}.hero p{font-size:15px}
 .machine-hero{min-height:300px}.grid,.topic-grid,.calc-grid,.footer-grid,.machine-grid,.detail-highlight,.subtopic-grid{grid-template-columns:1fr}
 .about h2,.social h2{font-size:32px}.machine-detail{padding:25px 18px}.detail-header{align-items:flex-start}
}
</style>
</head>

<body>

<header>
<div class="container nav">
<a href="#home" class="logo">
  <div class="logo-mark">CNC</div>
  <div class="logo-text">CNC <span>TECH HINDI</span><small>LEARN • PRACTICE • PERFECT</small></div>
</a>
<nav class="nav-links" id="navLinks">
  <a href="#home">Home</a><a href="#topics">Topics</a><a href="#cncMachines">CNC Machines</a>
  <a href="#learning">Learning</a><a href="#about">Er. Shadab</a><a href="#calculator">Calculator</a>
</nav>
<button class="menu-btn" onclick="toggleMenu()">☰</button>
</div>
</header>

<section class="hero" id="home">
<div class="container hero-grid">
<div>
  <div class="badge">ENGINEERING LEARNING PLATFORM</div>
  <h1>Master <span>CNC</span>.<br>Understand <span>Engineering.</span></h1>
  <p>Learn CNC Machines, CNC Programming, GD&T, Metrology, Cutting Tools, Engineering Drawing, AutoCAD, Mastercam and Manufacturing — from fundamentals to practical industry knowledge.</p>
  <div class="buttons">
    <a href="#topics" class="btn btn-primary">Explore Topics →</a>
    <a href="#about" class="btn btn-outline">Meet Er. Shadab</a>
  </div>
</div>
<div class="machine-hero">
  <div class="machine-graphic"><div class="machine-screen"></div><div class="machine-spindle"></div><div class="machine-base"></div></div>
</div>
</div>
</section>

<section class="categories" id="topics">
<div class="container">
<div class="section-head"><div class="tag">Explore</div><h2>Engineering Knowledge</h2><p>Everything organized into structured learning modules.</p></div>
<div class="grid">
  <div class="card" onclick="openCNCMachines()"><div class="icon">⚙</div><h3>CNC Machines</h3><p>Turning, Milling, Drilling, Grinding, EDM, Laser, Plasma, Router and more.</p><span class="card-link">Explore Machines →</span></div>
  <div class="card" onclick="openTopic('programming')"><div class="icon">⌨</div><h3>CNC Programming</h3><p>G-Codes, M-Codes, tool paths, offsets, cycles and programming concepts.</p><span class="card-link">Explore Programming →</span></div>
  <div class="card" onclick="openTopic('gdt')"><div class="icon">📐</div><h3>GD&T</h3><p>Form, Orientation, Location, Profile, Runout and Datum systems.</p><span class="card-link">Explore GD&T →</span></div>
  <div class="card" onclick="openTopic('metrology')"><div class="icon">🔍</div><h3>Metrology</h3><p>Measuring instruments, gauges, CMM, surface measurement and inspection.</p><span class="card-link">Explore Metrology →</span></div>
  <div class="card" onclick="openTopic('tools')"><div class="icon">🛠</div><h3>Cutting Tools</h3><p>Insert geometry, tool angles, grades, chip breakers, wear and selection.</p><span class="card-link">Explore Tools →</span></div>
  <div class="card" onclick="openTopic('manufacturing')"><div class="icon">📊</div><h3>Manufacturing</h3><p>5S, Kaizen, Lean, TPM, OEE, Poka-Yoke and quality systems.</p><span class="card-link">Explore Manufacturing →</span></div>
  <div class="card" onclick="openTopic('autocad')"><div class="icon">▣</div><h3>AutoCAD</h3><p>Mechanical drawing, commands, dimensions, layers, tolerances and drafting.</p><span class="card-link">Explore AutoCAD →</span></div>
  <div class="card" onclick="openTopic('mastercam')"><div class="icon">◈</div><h3>Mastercam</h3><p>CAD/CAM, toolpaths, simulation, verification and post processing.</p><span class="card-link">Explore Mastercam →</span></div>
</div>
</div>
</section>

<section class="machine-library" id="cncMachines">
<div class="container">
<div class="section-head"><div class="tag">CNC MACHINE LIBRARY</div><h2>Explore CNC Machines</h2><p>Select a machine to learn its working principle, axes, operations, tools, applications and programming.</p></div>
<div class="library-search">
  <input id="machineSearch" type="search" placeholder="Search machines, tools, topics..." oninput="searchMachines(this.value)">
</div>
<div class="machine-filter">
<button class="filter-btn active" onclick="filterMachines('all',this)">All</button>
<button class="filter-btn" onclick="filterMachines('turning',this)">Turning</button>
<button class="filter-btn" onclick="filterMachines('milling',this)">Milling</button>
<button class="filter-btn" onclick="filterMachines('cutting',this)">Cutting</button>
<button class="filter-btn" onclick="filterMachines('special',this)">Special</button>
</div>
<div class="machine-grid" id="machineGrid"></div>
</div>
</section>

<section class="learning" id="learning">
<div class="container">
<div class="section-head"><div class="tag">Deep Learning</div><h2>Learn Every Topic in Detail</h2><p>Each topic will contain definitions, practical examples, parameters, diagrams, inspection methods and industry applications.</p></div>
<div class="topic-grid">
<div class="topic"><small style="color:#e50914">ENGINEERING DRAWING</small><h3>Drawing Reading</h3><ul><li>Line Types & Symbols</li><li>Dimensions & Tolerances</li><li>Fits</li><li>Section Views</li><li>Surface Finish</li><li>Hole Callouts</li></ul></div>
<div class="topic"><small style="color:#e50914">CNC TURNING</small><h3>Complete Turning Guide</h3><ul><li>Axis & Machine Components</li><li>Turning Operations</li><li>Tool & Insert Selection</li><li>Tool Geometry</li><li>Cutting Parameters</li><li>G-Code Programming</li></ul></div>
<div class="topic"><small style="color:#e50914">GD&T</small><h3>Geometric Dimensioning
