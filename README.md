
<style>
  * { box-sizing: border-box; margin: 0; padding: 0; }
  body { font-family: var(--font-sans); color: var(--color-text-primary); }

  .hero {
    padding: 2.5rem 0 2rem;
    border-bottom: 0.5px solid var(--color-border-tertiary);
    margin-bottom: 2rem;
  }
  .hero-name {
    font-size: 28px;
    font-weight: 500;
    letter-spacing: -0.5px;
    margin-bottom: 4px;
  }
  .hero-title {
    font-size: 14px;
    color: var(--color-text-secondary);
    margin-bottom: 1.25rem;
    letter-spacing: 0.4px;
  }
  .hero-bio {
    font-size: 15px;
    line-height: 1.7;
    color: var(--color-text-primary);
    max-width: 560px;
    margin-bottom: 1.5rem;
  }
  .hero-bio strong { font-weight: 500; }
  .badge-row { display: flex; flex-wrap: wrap; gap: 8px; margin-bottom: 1.5rem; }
  .badge {
    font-size: 12px;
    padding: 4px 10px;
    border-radius: 20px;
    font-weight: 500;
    border: 0.5px solid;
  }
  .badge-purple { background: #EEEDFE; color: #3C3489; border-color: #AFA9EC; }
  .badge-teal { background: #E1F5EE; color: #085041; border-color: #5DCAA5; }
  .badge-coral { background: #FAECE7; color: #712B13; border-color: #F0997B; }
  .badge-gray { background: #F1EFE8; color: #444441; border-color: #B4B2A9; }

  .link-row { display: flex; gap: 16px; flex-wrap: wrap; }
  .link-item {
    display: flex; align-items: center; gap: 6px;
    font-size: 13px; color: var(--color-text-secondary);
    text-decoration: none;
    border-bottom: 1px solid transparent;
    transition: color 0.15s, border-color 0.15s;
  }
  .link-item:hover { color: #534AB7; border-color: #534AB7; }
  .link-item i { font-size: 15px; }

  .section-label {
    font-size: 11px;
    font-weight: 500;
    letter-spacing: 1.2px;
    color: var(--color-text-tertiary);
    text-transform: uppercase;
    margin-bottom: 1rem;
  }

  .stat-row {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
    gap: 10px;
    margin-bottom: 2.5rem;
  }
  .stat-card {
    background: var(--color-background-secondary);
    border-radius: var(--border-radius-md);
    padding: 14px 16px;
    text-align: center;
  }
  .stat-num { font-size: 22px; font-weight: 500; }
  .stat-num.purple { color: #534AB7; }
  .stat-num.teal { color: #0F6E56; }
  .stat-num.coral { color: #993C1D; }
  .stat-label { font-size: 11px; color: var(--color-text-secondary); margin-top: 3px; }

  .projects { margin-bottom: 2.5rem; }
  .project-card {
    background: var(--color-background-primary);
    border: 0.5px solid var(--color-border-tertiary);
    border-radius: var(--border-radius-lg);
    padding: 1.1rem 1.25rem;
    margin-bottom: 10px;
    transition: border-color 0.15s;
  }
  .project-card:hover { border-color: var(--color-border-secondary); }
  .project-card.featured { border-left: 3px solid #7F77DD; border-radius: 0 var(--border-radius-lg) var(--border-radius-lg) 0; }
  .project-header { display: flex; align-items: flex-start; justify-content: space-between; margin-bottom: 6px; }
  .project-name { font-size: 14px; font-weight: 500; display: flex; align-items: center; gap: 8px; }
  .project-name i { font-size: 16px; color: #7F77DD; }
  .project-name.teal-icon i { color: #1D9E75; }
  .project-name.coral-icon i { color: #D85A30; }
  .project-name.gray-icon i { color: #888780; }
  .project-desc { font-size: 13px; color: var(--color-text-secondary); line-height: 1.55; margin-bottom: 10px; }
  .tag-row { display: flex; gap: 6px; flex-wrap: wrap; }
  .tag { font-size: 11px; padding: 3px 8px; border-radius: 4px; background: var(--color-background-secondary); color: var(--color-text-secondary); font-family: var(--font-mono); }
  .project-link { font-size: 12px; color: #534AB7; display: flex; align-items: center; gap: 4px; white-space: nowrap; }
  .project-link i { font-size: 13px; }

  .exp-section { margin-bottom: 2.5rem; }
  .exp-item { display: flex; gap: 14px; padding: 12px 0; border-bottom: 0.5px solid var(--color-border-tertiary); }
  .exp-item:last-child { border-bottom: none; }
  .exp-dot { width: 8px; height: 8px; border-radius: 50%; margin-top: 6px; flex-shrink: 0; }
  .exp-dot.purple { background: #7F77DD; }
  .exp-dot.teal { background: #1D9E75; }
  .exp-dot.coral { background: #D85A30; }
  .exp-dot.gray { background: #888780; }
  .exp-role { font-size: 13px; font-weight: 500; margin-bottom: 2px; }
  .exp-org { font-size: 12px; color: var(--color-text-secondary); margin-bottom: 2px; }
  .exp-detail { font-size: 12px; color: var(--color-text-tertiary); }

  .skills-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(140px, 1fr)); gap: 10px; margin-bottom: 2.5rem; }
  .skill-group { background: var(--color-background-secondary); border-radius: var(--border-radius-md); padding: 12px 14px; }
  .skill-group-title { font-size: 11px; font-weight: 500; color: var(--color-text-secondary); letter-spacing: 0.5px; margin-bottom: 8px; text-transform: uppercase; }
  .skill-list { display: flex; flex-direction: column; gap: 4px; }
  .skill-item { font-size: 12px; color: var(--color-text-primary); display: flex; align-items: center; gap: 6px; }
  .skill-item i { font-size: 13px; color: var(--color-text-tertiary); }

  .footer {
    border-top: 0.5px solid var(--color-border-tertiary);
    padding-top: 1.5rem;
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-wrap: gap;
  }
  .footer-tag { font-size: 12px; color: var(--color-text-tertiary); }
  .avail-badge { display: flex; align-items: center; gap: 6px; font-size: 12px; font-weight: 500; color: #0F6E56; }
  .avail-dot { width: 7px; height: 7px; border-radius: 50%; background: #1D9E75; }
</style>

<h2 class="sr-only">Naga Pranathi Majji — AI Engineer GitHub profile preview</h2>

<div class="hero">
  <div class="hero-name">Naga Pranathi Majji</div>
  <div class="hero-title">AI ENGINEER · AGENTIC SYSTEMS · RAG · FULL-STACK AI PRODUCTS</div>
  <p class="hero-bio">
    I build AI systems that actually <strong>reason and act</strong> — not just respond. LangGraph agents running Mistral 7B locally, production RAG pipelines, and full-stack mobile apps. Currently founding engineer at Tummy Tales + IIT Ropar lab contributor. <strong>9.38 GPA, immediate joiner.</strong>
  </p>
  <div class="badge-row">
    <span class="badge badge-purple"><i class="ti ti-brain" aria-hidden="true"></i> LangGraph + Local LLMs</span>
    <span class="badge badge-teal"><i class="ti ti-database" aria-hidden="true"></i> RAG Pipelines</span>
    <span class="badge badge-coral"><i class="ti ti-device-mobile" aria-hidden="true"></i> React Native</span>
    <span class="badge badge-gray"><i class="ti ti-map-pin" aria-hidden="true"></i> Andhra Pradesh, India</span>
  </div>
  <div class="link-row">
    <a href="https://linkedin.com/in/nagapranathimajji" class="link-item"><i class="ti ti-brand-linkedin" aria-hidden="true"></i> LinkedIn</a>
    <a href="mailto:nagapranathimajji@gmail.com" class="link-item"><i class="ti ti-mail" aria-hidden="true"></i> Email</a>
    <a href="https://github.com/nagapranathimajji" class="link-item"><i class="ti ti-brand-github" aria-hidden="true"></i> GitHub</a>
  </div>
</div>

<div class="stat-row">
  <div class="stat-card">
    <div class="stat-num purple">9.38</div>
    <div class="stat-label">GPA / 10</div>
  </div>
  <div class="stat-card">
    <div class="stat-num teal">5</div>
    <div class="stat-label">internships</div>
  </div>
  <div class="stat-card">
    <div class="stat-num coral">IIT</div>
    <div class="stat-label">Ropar lab</div>
  </div>
  <div class="stat-card">
    <div class="stat-num purple">Top 5%</div>
    <div class="stat-label">NPTEL</div>
  </div>
</div>

<div class="projects">
  <div class="section-label">featured projects</div>

  <div class="project-card featured">
    <div class="project-header">
      <div class="project-name"><i class="ti ti-robot" aria-hidden="true"></i> LangGraph Mistral Agent</div>
      <a href="https://github.com/nagapranathimajji/langgraph-mistral-agent" class="project-link"><i class="ti ti-external-link" aria-hidden="true"></i> repo</a>
    </div>
    <div class="project-desc">Fully local agentic workflow — multi-step reasoning, tool use, conditional branching. No OpenAI dependency. Mistral 7B runs via Ollama on-device.</div>
    <div class="tag-row">
      <span class="tag">LangGraph</span><span class="tag">Mistral 7B</span><span class="tag">Ollama</span><span class="tag">Python</span><span class="tag">agentic AI</span>
    </div>
  </div>

  <div class="project-card featured">
    <div class="project-header">
      <div class="project-name teal-icon"><i class="ti ti-device-mobile" aria-hidden="true"></i> Tummy Tales — full-stack mobile app</div>
      <a href="https://github.com/nagapranathimajji/Tummy-Tales" class="project-link"><i class="ti ti-external-link" aria-hidden="true"></i> repo</a>
    </div>
    <div class="project-desc">Solo-built production app for school meal delivery startup. Multi-role dashboards (parent / chef / admin), JWT auth, subscription management, Flask backend, Google Agentspace integration.</div>
    <div class="tag-row">
      <span class="tag">React Native</span><span class="tag">Flask</span><span class="tag">Google Agentspace</span><span class="tag">JWT</span><span class="tag">MongoDB</span>
    </div>
  </div>

  <div class="project-card">
    <div class="project-header">
      <div class="project-name"><i class="ti ti-database" aria-hidden="true"></i> Internal IT Assistant — RAG Demo</div>
      <a href="https://github.com/nagapranathimajji/Internal-IT-Assistant-RAG-Demo-" class="project-link"><i class="ti ti-external-link" aria-hidden="true"></i> repo</a>
    </div>
    <div class="project-desc">Organisational knowledge retrieval system. Contextual document search using vector DB + LLM. Deployed live on Hugging Face Spaces.</div>
    <div class="tag-row">
      <span class="tag">RAG</span><span class="tag">vector DB</span><span class="tag">LLM</span><span class="tag">Hugging Face</span>
    </div>
  </div>

  <div class="project-card">
    <div class="project-header">
      <div class="project-name coral-icon"><i class="ti ti-eye" aria-hidden="true"></i> AR eye tracking for ASD — major project</div>
    </div>
    <div class="project-desc">Multimodal deep learning architecture (CNN + Bi-LSTM + contrastive learning) for Autism Spectrum Disorder analysis in natural environments. ~80% accuracy. Published at ICRAIQIIT 2026.</div>
    <div class="tag-row">
      <span class="tag">CNN</span><span class="tag">Bi-LSTM</span><span class="tag">contrastive learning</span><span class="tag">healthcare AI</span>
    </div>
  </div>
</div>

<div class="exp-section">
  <div class="section-label">experience</div>
  <div class="exp-item">
    <div class="exp-dot purple"></div>
    <div>
      <div class="exp-role">Founding engineer & product designer</div>
      <div class="exp-org">Tummy Tales · Jun 2025 – present</div>
      <div class="exp-detail">Solo-built React Native + Flask production stack, multi-role auth, Google Agentspace</div>
    </div>
  </div>
  <div class="exp-item">
    <div class="exp-dot teal"></div>
    <div>
      <div class="exp-role">MERN stack intern — Vicharanashala Lab</div>
      <div class="exp-org">IIT Ropar, under Prof. Sudarshan Iyengar · Jan 2026 – present</div>
      <div class="exp-detail">Industry-impactful applications for research lab</div>
    </div>
  </div>
  <div class="exp-item">
    <div class="exp-dot coral"></div>
    <div>
      <div class="exp-role">AI intern</div>
      <div class="exp-org">Ravi Aadhya Infotech · May–Jun 2025</div>
      <div class="exp-detail">Agentic workflows: LangGraph + Mistral 7B via Ollama</div>
    </div>
  </div>
  <div class="exp-item">
    <div class="exp-dot gray"></div>
    <div>
      <div class="exp-role">AI intern — TechSaksham (Microsoft & SAP)</div>
      <div class="exp-org">AICTE / Edunet Foundation · Jan–Feb 2025</div>
      <div class="exp-detail">Stable Diffusion image generation pipeline</div>
    </div>
  </div>
  <div class="exp-item">
    <div class="exp-dot gray"></div>
    <div>
      <div class="exp-role">Generative AI intern</div>
      <div class="exp-org">Codegnan · May–Jul 2024</div>
      <div class="exp-detail">Word Sphere — Flask-based GenAI word game</div>
    </div>
  </div>
</div>

<div class="section-label">skills</div>
<div class="skills-grid">
  <div class="skill-group">
    <div class="skill-group-title">Agentic AI</div>
    <div class="skill-list">
      <div class="skill-item"><i class="ti ti-arrow-right" aria-hidden="true"></i> LangGraph</div>
      <div class="skill-item"><i class="ti ti-arrow-right" aria-hidden="true"></i> Ollama</div>
      <div class="skill-item"><i class="ti ti-arrow-right" aria-hidden="true"></i> Mistral 7B</div>
      <div class="skill-item"><i class="ti ti-arrow-right" aria-hidden="true"></i> RAG pipelines</div>
    </div>
  </div>
  <div class="skill-group">
    <div class="skill-group-title">Deep learning</div>
    <div class="skill-list">
      <div class="skill-item"><i class="ti ti-arrow-right" aria-hidden="true"></i> CNN / Bi-LSTM</div>
      <div class="skill-item"><i class="ti ti-arrow-right" aria-hidden="true"></i> Stable Diffusion</div>
      <div class="skill-item"><i class="ti ti-arrow-right" aria-hidden="true"></i> Contrastive learning</div>
      <div class="skill-item"><i class="ti ti-arrow-right" aria-hidden="true"></i> Streamlit</div>
    </div>
  </div>
  <div class="skill-group">
    <div class="skill-group-title">Mobile / web</div>
    <div class="skill-list">
      <div class="skill-item"><i class="ti ti-arrow-right" aria-hidden="true"></i> React Native</div>
      <div class="skill-item"><i class="ti ti-arrow-right" aria-hidden="true"></i> Flask</div>
      <div class="skill-item"><i class="ti ti-arrow-right" aria-hidden="true"></i> React.js</div>
      <div class="skill-item"><i class="ti ti-arrow-right" aria-hidden="true"></i> Node.js / MongoDB</div>
    </div>
  </div>
  <div class="skill-group">
    <div class="skill-group-title">Languages</div>
    <div class="skill-list">
      <div class="skill-item"><i class="ti ti-arrow-right" aria-hidden="true"></i> Python</div>
      <div class="skill-item"><i class="ti ti-arrow-right" aria-hidden="true"></i> JavaScript</div>
      <div class="skill-item"><i class="ti ti-arrow-right" aria-hidden="true"></i> C</div>
      <div class="skill-item"><i class="ti ti-arrow-right" aria-hidden="true"></i> R</div>
    </div>
  </div>
</div>

<div class="footer">
  <div class="footer-tag">NRI Institute of Technology · B.Tech CSE · May 2026</div>
  <div class="avail-badge"><div class="avail-dot"></div> Immediate joiner</div>
</div>
