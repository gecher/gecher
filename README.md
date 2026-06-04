@import url('https://fonts.googleapis.com/css2?family=Space+Mono:wght@400;700&family=Outfit:wght@300;400;500;600;700&display=swap'); \*{margin:0;padding:0;box-sizing:border-box;} :root{ --navy:#0a0f1e;--navy2:#0e1628;--navy3:#111d35; --blue:#1e88e5;--blue2:#42a5f5;--blue3:#90caf9; --cyan:#00bcd4;--cyan2:#26c6da; --orange:#ff7043;--orange2:#ff8a65; --green:#00e676;--green2:#69f0ae; --purple:#7c4dff;--text:#e8eaf6;--muted:#8892b0; } body{ font-family:'Outfit',sans-serif; background:var(--navy); color:var(--text); overflow-x:hidden; min-height:100vh; } .profile-wrap{ max-width:820px; margin:0 auto; padding:2rem 1.5rem; } /\* ── HERO ── \*/ .hero{ position:relative; text-align:center; padding:3rem 1rem 2.5rem; overflow:hidden; } .hero-bg{ position:absolute;inset:0; background:radial-gradient(ellipse 80% 60% at 50% 0%, rgba(30,136,229,.18) 0%, transparent 70%), radial-gradient(ellipse 50% 40% at 80% 80%, rgba(0,188,212,.10) 0%, transparent 60%); animation:pulseBg 6s ease-in-out infinite alternate; } @keyframes pulseBg{from{opacity:.7}to{opacity:1}} .avatar-ring{ position:relative; width:110px;height:110px; margin:0 auto 1.5rem; display:flex;align-items:center;justify-content:center; } .avatar-ring::before{ content:'';position:absolute;inset:-5px; border-radius:50%; background:conic-gradient(var(--blue),var(--cyan),var(--purple),var(--orange),var(--blue)); animation:spinRing 4s linear infinite; } @keyframes spinRing{to{transform:rotate(360deg)}} .avatar-inner{ position:relative; width:100%;height:100%;border-radius:50%; background:linear-gradient(135deg,var(--blue),var(--purple)); display:flex;align-items:center;justify-content:center; font-family:'Space Mono',monospace; font-size:2rem;font-weight:700; color:#fff; z-index:1; box-shadow:0 0 30px rgba(30,136,229,.4); border:3px solid var(--navy); } .hero-name{ font-family:'Outfit',sans-serif; font-size:2.2rem;font-weight:700; background:linear-gradient(90deg,var(--blue2),var(--cyan),var(--blue3)); -webkit-background-clip:text;-webkit-text-fill-color:transparent; background-clip:text; animation:shimmer 3s ease infinite; background-size:200% auto; } @keyframes shimmer{ 0%{background-position:0%}100%{background-position:200%} } .hero-title{ font-size:1rem;color:var(--muted);margin:.6rem 0 1.2rem; font-weight:400;letter-spacing:.02em; } .hero-title span{color:var(--cyan2);font-weight:500;} .badges{ display:flex;flex-wrap:wrap;gap:.5rem; justify-content:center;margin-bottom:1.5rem; } .badge{ font-size:.72rem;font-weight:600;letter-spacing:.05em; padding:.32rem .8rem;border-radius:20px; text-transform:uppercase; border:1px solid; animation:fadeSlideIn .6s ease both; } .badge-blue{background:rgba(30,136,229,.12);color:var(--blue2);border-color:rgba(30,136,229,.3);} .badge-cyan{background:rgba(0,188,212,.12);color:var(--cyan2);border-color:rgba(0,188,212,.3);} .badge-orange{background:rgba(255,112,67,.12);color:var(--orange2);border-color:rgba(255,112,67,.3);} .badge-purple{background:rgba(124,77,255,.12);color:#b39ddb;border-color:rgba(124,77,255,.3);} .badge-green{background:rgba(0,230,118,.1);color:var(--green2);border-color:rgba(0,230,118,.25);} .badge:nth-child(1){animation-delay:.1s} .badge:nth-child(2){animation-delay:.2s} .badge:nth-child(3){animation-delay:.3s} .badge:nth-child(4){animation-delay:.4s} .badge:nth-child(5){animation-delay:.5s} @keyframes fadeSlideIn{from{opacity:0;transform:translateY(10px)}to{opacity:1;transform:none}} .terminal-tagline{ font-family:'Space Mono',monospace; font-size:.82rem;color:var(--green2); background:rgba(0,230,118,.06); border:1px solid rgba(0,230,118,.2); border-radius:8px; padding:.6rem 1.2rem; display:inline-block; margin-top:.5rem; } .terminal-tagline::before{content:'> ';color:var(--muted);} .cursor{display:inline-block;width:2px;height:.9em;background:var(--green2);margin-left:2px;animation:blink 1s step-end infinite;vertical-align:text-bottom;} @keyframes blink{50%{opacity:0}} /\* ── SECTION ── \*/ .section{margin:1.8rem 0;} .section-title{ font-family:'Space Mono',monospace; font-size:.75rem;font-weight:700;letter-spacing:.12em; color:var(--blue2);text-transform:uppercase; display:flex;align-items:center;gap:.7rem; margin-bottom:1.1rem; } .section-title::after{content:'';flex:1;height:1px;background:linear-gradient(to right,rgba(30,136,229,.4),transparent);} /\* ── ABOUT GRID ── \*/ .about-grid{ display:grid;grid-template-columns:1fr 1fr;gap:.7rem; } .about-item{ background:rgba(255,255,255,.04); border:1px solid rgba(255,255,255,.07); border-radius:10px; padding:.75rem 1rem; font-size:.88rem;color:var(--muted); display:flex;align-items:flex-start;gap:.6rem; transition:all .25s; animation:fadeSlideIn .5s ease both; } .about-item:hover{ background:rgba(30,136,229,.1); border-color:rgba(30,136,229,.3); color:var(--text);transform:translateY(-2px); } .about-item .dot{ width:6px;height:6px;border-radius:50%; margin-top:5px;flex-shrink:0; } /\* ── SKILLS ── \*/ .skills-grid{ display:grid;grid-template-columns:repeat(auto-fill,minmax(175px,1fr));gap:.7rem; } .skill-card{ background:rgba(255,255,255,.04); border:1px solid rgba(255,255,255,.07); border-radius:10px;padding:.8rem 1rem; animation:fadeSlideIn .5s ease both; transition:all .25s; } .skill-card:hover{transform:translateY(-3px);border-color:rgba(30,136,229,.35);background:rgba(30,136,229,.08);} .skill-cat{font-size:.68rem;font-weight:600;letter-spacing:.1em;text-transform:uppercase;color:var(--muted);margin-bottom:.5rem;} .skill-tags{display:flex;flex-wrap:wrap;gap:.35rem;} .skill-tag{ font-size:.7rem;font-weight:500; padding:.2rem .5rem;border-radius:5px; background:rgba(255,255,255,.07);color:var(--text); border:1px solid rgba(255,255,255,.1); } /\* ── PROJECTS ── \*/ .projects-list{display:flex;flex-direction:column;gap:.75rem;} .project-card{ background:rgba(255,255,255,.04); border:1px solid rgba(255,255,255,.07); border-left:3px solid; border-radius:0 10px 10px 0; padding:.9rem 1.1rem; animation:fadeSlideIn .5s ease both; transition:all .25s; } .project-card:hover{transform:translateX(4px);background:rgba(255,255,255,.07);} .project-head{display:flex;align-items:center;justify-content:space-between;margin-bottom:.4rem;flex-wrap:wrap;gap:.4rem;} .project-name{font-size:.95rem;font-weight:600;color:var(--text);} .project-icon{font-size:1.1rem;} .project-desc{font-size:.82rem;color:var(--muted);line-height:1.55;} .project-stack{display:flex;flex-wrap:wrap;gap:.3rem;margin-top:.55rem;} .stack-tag{ font-size:.65rem;font-weight:600;padding:.18rem .5rem;border-radius:4px; background:rgba(255,255,255,.06);color:var(--muted); border:1px solid rgba(255,255,255,.1);letter-spacing:.03em; } /\* ── STATS ── \*/ .stats-row{ display:grid;grid-template-columns:repeat(3,1fr);gap:.7rem; } .stat-box{ background:rgba(255,255,255,.04); border:1px solid rgba(255,255,255,.07); border-radius:10px;padding:1rem;text-align:center; animation:fadeSlideIn .5s ease both; transition:all .25s; } .stat-box:hover{transform:scale(1.03);border-color:rgba(0,188,212,.35);background:rgba(0,188,212,.07);} .stat-num{font-family:'Space Mono',monospace;font-size:1.5rem;font-weight:700;color:var(--cyan2);display:block;} .stat-label{font-size:.72rem;color:var(--muted);margin-top:.2rem;letter-spacing:.05em;} /\* ── DIVIDER ── \*/ .divider{height:1px;background:linear-gradient(to right,transparent,rgba(255,255,255,.1),transparent);margin:1.5rem 0;} /\* ── FOOTER ── \*/ .footer{text-align:center;padding:1.5rem 0 .5rem;} .footer-text{font-size:.78rem;color:var(--muted);font-style:italic;} .footer-quote{ font-family:'Space Mono',monospace; font-size:.78rem;color:var(--blue3); margin-top:.5rem; } /\* ── FLOATING PARTICLES ── \*/ .particles{position:fixed;inset:0;pointer-events:none;overflow:hidden;z-index:0;} .particle{ position:absolute; width:2px;height:2px;border-radius:50%; background:var(--blue2); animation:float linear infinite; opacity:0; } @keyframes float{ 0%{transform:translateY(100vh) scale(0);opacity:0} 10%{opacity:.6} 90%{opacity:.3} 100%{transform:translateY(-20px) scale(1.5);opacity:0} } .profile-wrap{position:relative;z-index:1;} .delay1{animation-delay:.15s} .delay2{animation-delay:.3s} .delay3{animation-delay:.45s} .delay4{animation-delay:.6s} .delay5{animation-delay:.75s} .delay6{animation-delay:.9s}

Getacher Ashebir – GitHub Profile
---------------------------------

GA

Getacher Ashebir
================

Backend Engineer · AI & Agentic Systems · Enterprise Architect

ASP.NET Core AI / LLMs Multi-Agent Aviation Systems Clean Architecture

Building intelligent systems for enterprise

About Me

Building AI-driven systems with multi-agent architectures

Designing enterprise e-service & workflow platforms

Large-scale backend systems in aviation industry

Passionate about LLMs, automation & intelligent flows

Creator of low-code dynamic form & workflow systems

Currently at Ethiopian Airlines on mission-critical systems

Technical Skills

Languages

C# Python TypeScript SQL

Backend

ASP.NET Core EF Core CQRS MediatR

AI & Agents

OpenAI API LangGraph RAG Vector DBs

Frontend

React Next.js

Databases

MSSQL PostgreSQL MongoDB

Cloud & DevOps

Azure DevOps CI/CD GitHub Actions

Featured Projects

🤖 Automaton Auditor Multi-Agent

AI multi-agent system for automated repository auditing. Uses LangGraph + OpenAI tool-calling for structured, explainable code quality evaluation.

LangGraphOpenAIPythonTool Calling

✈️ ECAA E-Service Platform Aviation

Pilot licensing & crew application systems with a low-code dynamic form builder. Integrated Power Automate + SharePoint approval workflows.

ASP.NET CorePower AutomateSharePointLow-Code

📦 e-Procurement System Ethiopian Airlines

Purchase request & supplier management system with RabbitMQ async workflows, connecting finance and inventory systems across departments.

ASP.NET CoreRabbitMQMSSQLMicroservices

🏥 Medical Management System 17,000+ Employees

Manages medical records & employee health for 17,000+ Ethiopian Airlines employees. Built on CQRS + MediatR architecture for high scalability.

CQRSMediatRClean ArchPostgreSQL

🏨 AlphaPlus Booking System 2000+ Daily Users

Transit hotel booking backend serving 2000+ daily users. Automated booking & notification workflows, reducing booking errors by 40%.

ASP.NET CoreNotificationsAutomation

Impact Numbers

0

Employees Served

0

Daily Users

0%

Error Reduction

"Building intelligent systems that simplify complex enterprise operations."

Ethiopian Airlines · Addis Ababa, Ethiopia

const P=document.getElementById('particles'); for(let i=0;i<28;i++){ const p=document.createElement('div'); p.className='particle'; const colors=\['#42a5f5','#26c6da','#7c4dff','#ff7043','#00e676'\]; p.style.cssText=\`left:${Math.random()\*100}%;animation-duration:${6+Math.random()\*12}s;animation-delay:${Math.random()\*10}s;background:${colors\[Math.floor(Math.random()\*colors.length)\]};width:${1+Math.random()\*3}px;height:${1+Math.random()\*3}px;\`; P.appendChild(p); } const texts=\[ "Building intelligent systems for enterprise", "Designing multi-agent AI workflows", "Scaling aviation backend systems", "Turning complex processes into digital solutions" \]; let ti=0,ci=0,del=false; const el=document.getElementById('tagline'); function typeLoop(){ const cur=texts\[ti\]; if(!del){ ci++; el.innerHTML=cur.slice(0,ci)+'<span class="cursor"></span>'; if(ci===cur.length){del=true;setTimeout(typeLoop,2200);return;} setTimeout(typeLoop,42); } else { ci--; el.innerHTML=cur.slice(0,ci)+'<span class="cursor"></span>'; if(ci===0){del=false;ti=(ti+1)%texts.length;setTimeout(typeLoop,400);return;} setTimeout(typeLoop,20); } } typeLoop(); function animNum(id,target,suffix='',dur=1400){ const el=document.getElementById(id); let start=null; function step(ts){ if(!start)start=ts; const p=Math.min((ts-start)/dur,1); const v=Math.round(p\*p\*target); el.textContent=v.toLocaleString()+suffix; if(p<1)requestAnimationFrame(step); else el.textContent=target.toLocaleString()+suffix; } requestAnimationFrame(step); } const obs=new IntersectionObserver(entries=>{ entries.forEach(e=>{ if(e.isIntersecting){ animNum('stat1',17000,''); animNum('stat2',2000,''); animNum('stat3',40,'%'); obs.disconnect(); } }); },{threshold:.4}); obs.observe(document.getElementById('stat1'));
