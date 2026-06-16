
<style>
  * { box-sizing: border-box; margin: 0; padding: 0; }
  body { font-family: var(--font-mono, monospace); }
  .readme { padding: 2rem 0; max-width: 860px; }
  .hero { text-align: center; padding: 2.5rem 1rem 2rem; border-bottom: 0.5px solid var(--color-border-tertiary); margin-bottom: 2rem; }
  .hero-name { font-size: 28px; font-weight: 500; color: var(--color-text-primary); font-family: var(--font-sans); letter-spacing: -0.5px; }
  .hero-role { font-size: 14px; color: var(--color-text-secondary); margin-top: 6px; font-family: var(--font-sans); }
  .hero-tagline { font-size: 13px; color: var(--color-text-tertiary); margin-top: 8px; font-family: var(--font-sans); max-width: 480px; margin-left: auto; margin-right: auto; line-height: 1.6; }
  .badges { display: flex; flex-wrap: wrap; gap: 8px; justify-content: center; margin-top: 1.25rem; }
  .badge { display: inline-flex; align-items: center; gap: 5px; padding: 4px 10px; border-radius: 20px; font-size: 12px; font-family: var(--font-sans); font-weight: 500; border: 0.5px solid var(--color-border-tertiary); color: var(--color-text-secondary); background: var(--color-background-secondary); }
  .badge i { font-size: 13px; }
  .badge.blue { background: #E6F1FB; color: #0C447C; border-color: #85B7EB; }
  .badge.teal { background: #E1F5EE; color: #085041; border-color: #5DCAA5; }
  .badge.purple { background: #EEEDFE; color: #3C3489; border-color: #AFA9EC; }
  .badge.amber { background: #FAEEDA; color: #633806; border-color: #EF9F27; }
  .badge.coral { background: #FAECE7; color: #4A1B0C; border-color: #F0997B; }
  .section { margin-bottom: 2rem; }
  .section-header { display: flex; align-items: center; gap: 8px; margin-bottom: 1rem; padding-bottom: 6px; border-bottom: 0.5px solid var(--color-border-tertiary); }
  .section-header i { font-size: 16px; color: var(--color-text-secondary); }
  .section-header span { font-size: 13px; font-weight: 500; color: var(--color-text-secondary); text-transform: uppercase; letter-spacing: 0.8px; font-family: var(--font-sans); }
  .about-text { font-size: 14px; color: var(--color-text-secondary); font-family: var(--font-sans); line-height: 1.7; }
  .two-col { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; }
  .card { background: var(--color-background-primary); border: 0.5px solid var(--color-border-tertiary); border-radius: var(--border-radius-lg); padding: 1rem 1.25rem; }
  .card-label { font-size: 11px; font-weight: 500; color: var(--color-text-tertiary); text-transform: uppercase; letter-spacing: 0.7px; font-family: var(--font-sans); margin-bottom: 10px; }
  .pursuit-item { display: flex; align-items: flex-start; gap: 8px; margin-bottom: 10px; font-family: var(--font-sans); }
  .pursuit-item:last-child { margin-bottom: 0; }
  .pursuit-icon { font-size: 15px; color: var(--color-text-secondary); margin-top: 1px; flex-shrink: 0; }
  .pursuit-title { font-size: 13px; font-weight: 500; color: var(--color-text-primary); }
  .pursuit-sub { font-size: 12px; color: var(--color-text-tertiary); margin-top: 2px; }
  .stack-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(140px, 1fr)); gap: 8px; }
  .stack-cat { background: var(--color-background-secondary); border: 0.5px solid var(--color-border-tertiary); border-radius: var(--border-radius-md); padding: 12px; }
  .stack-cat-label { font-size: 11px; color: var(--color-text-tertiary); text-transform: uppercase; letter-spacing: 0.7px; font-family: var(--font-sans); margin-bottom: 8px; font-weight: 500; }
  .tech-pills { display: flex; flex-wrap: wrap; gap: 5px; }
  .tech-pill { display: inline-flex; align-items: center; gap: 4px; padding: 3px 8px; border-radius: 12px; font-size: 11px; font-family: var(--font-sans); font-weight: 500; background: var(--color-background-primary); border: 0.5px solid var(--color-border-tertiary); color: var(--color-text-secondary); }
  .tech-pill i { font-size: 12px; }
  .orch-tags { display: flex; flex-wrap: wrap; gap: 6px; }
  .orch-tag { display: inline-flex; align-items: center; gap: 5px; padding: 5px 12px; border-radius: var(--border-radius-md); font-size: 12px; font-family: var(--font-sans); border: 0.5px solid var(--color-border-tertiary); color: var(--color-text-secondary); background: var(--color-background-secondary); }
  .orch-tag i { font-size: 14px; }
  .env-row { display: flex; align-items: center; gap: 8px; padding: 8px 0; border-bottom: 0.5px solid var(--color-border-tertiary); font-family: var(--font-sans); }
  .env-row:last-child { border-bottom: none; }
  .env-icon { font-size: 16px; width: 28px; text-align: center; color: var(--color-text-secondary); }
  .env-name { font-size: 13px; font-weight: 500; color: var(--color-text-primary); flex: 1; }
  .env-desc { font-size: 12px; color: var(--color-text-tertiary); }
  .stat-row { display: grid; grid-template-columns: repeat(4, 1fr); gap: 8px; }
  .stat-card { background: var(--color-background-secondary); border-radius: var(--border-radius-md); padding: 12px; text-align: center; }
  .stat-num { font-size: 22px; font-weight: 500; color: var(--color-text-primary); font-family: var(--font-sans); }
  .stat-label { font-size: 11px; color: var(--color-text-tertiary); font-family: var(--font-sans); margin-top: 3px; text-transform: uppercase; letter-spacing: 0.6px; }
  @media (max-width: 560px) {
    .two-col { grid-template-columns: 1fr; }
    .stat-row { grid-template-columns: repeat(2, 1fr); }
  }
</style>

<div class="readme">

  <div class="hero">
    <div class="hero-name">Vishwa Dhanujaya Gallage</div>
    <div class="hero-role">Computer Science Student &amp; Software Developer</div>
    <div class="hero-tagline">Building clean architecture, exploring data landscapes, and orchestrating intelligent systems.</div>
    <div class="badges">
      <span class="badge blue"><i class="ti ti-brand-python" aria-hidden="true"></i> Python</span>
      <span class="badge teal"><i class="ti ti-brand-cpp" aria-hidden="true"></i> C++</span>
      <span class="badge purple"><i class="ti ti-brand-php" aria-hidden="true"></i> PHP / Laravel</span>
      <span class="badge coral"><i class="ti ti-brand-react" aria-hidden="true"></i> React</span>
      <span class="badge amber"><i class="ti ti-robot" aria-hidden="true"></i> AI Orchestration</span>
    </div>
  </div>

  <div class="section">
    <div class="section-header">
      <i class="ti ti-user" aria-hidden="true"></i>
      <span>About</span>
    </div>
    <p class="about-text">
      I write readable, maintainable code and break complex technical challenges into elegant solutions. I treat version control as a narrative, data as a story, and optimization as a necessity. Currently exploring AI orchestration pipelines and scalable full-stack systems.
    </p>
  </div>

  <div class="section">
    <div class="section-header">
      <i class="ti ti-compass" aria-hidden="true"></i>
      <span>Focus areas</span>
    </div>
    <div class="two-col">
      <div class="card">
        <div class="card-label">Current pursuits</div>
        <div class="pursuit-item">
          <i class="ti ti-topology-star-3 pursuit-icon" aria-hidden="true"></i>
          <div>
            <div class="pursuit-title">Scalable architecture</div>
            <div class="pursuit-sub">Software design patterns &amp; clean systems</div>
          </div>
        </div>
        <div class="pursuit-item">
          <i class="ti ti-robot pursuit-icon" aria-hidden="true"></i>
          <div>
            <div class="pursuit-title">AI orchestration</div>
            <div class="pursuit-sub">Multi-agent pipelines &amp; LLM workflows</div>
          </div>
        </div>
        <div class="pursuit-item">
          <i class="ti ti-brand-git pursuit-icon" aria-hidden="true"></i>
          <div>
            <div class="pursuit-title">DevOps &amp; CI/CD</div>
            <div class="pursuit-sub">Git automation &amp; containerized workflows</div>
          </div>
        </div>
      </div>
      <div class="card">
        <div class="card-label">Technical interests</div>
        <div class="pursuit-item">
          <i class="ti ti-chart-dots pursuit-icon" aria-hidden="true"></i>
          <div>
            <div class="pursuit-title">Data computing</div>
            <div class="pursuit-sub">Analysis &amp; reproducible research</div>
          </div>
        </div>
        <div class="pursuit-item">
          <i class="ti ti-binary-tree pursuit-icon" aria-hidden="true"></i>
          <div>
            <div class="pursuit-title">Algorithms</div>
            <div class="pursuit-sub">Resource-efficient data structures</div>
          </div>
        </div>
        <div class="pursuit-item">
          <i class="ti ti-layers-intersect pursuit-icon" aria-hidden="true"></i>
          <div>
            <div class="pursuit-title">Full-stack systems</div>
            <div class="pursuit-sub">React frontends, Laravel APIs</div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <div class="section">
    <div class="section-header">
      <i class="ti ti-terminal-2" aria-hidden="true"></i>
      <span>Stack</span>
    </div>
    <div class="stack-grid">
      <div class="stack-cat">
        <div class="stack-cat-label"><i class="ti ti-code" aria-hidden="true"></i> Languages</div>
        <div class="tech-pills">
          <span class="tech-pill"><i class="ti ti-brand-python"></i>Python</span>
          <span class="tech-pill">R</span>
          <span class="tech-pill">SQL</span>
          <span class="tech-pill"><i class="ti ti-brand-cpp"></i>C++</span>
          <span class="tech-pill"><i class="ti ti-coffee"></i>Java</span>
          <span class="tech-pill"><i class="ti ti-brand-php"></i>PHP</span>
        </div>
      </div>
      <div class="stack-cat">
        <div class="stack-cat-label"><i class="ti ti-layout-grid" aria-hidden="true"></i> Frameworks</div>
        <div class="tech-pills">
          <span class="tech-pill"><i class="ti ti-brand-react"></i>React</span>
          <span class="tech-pill">Laravel</span>
          <span class="tech-pill">Pandas</span>
          <span class="tech-pill">NumPy</span>
          <span class="tech-pill">ggplot2</span>
          <span class="tech-pill">Scikit-Learn</span>
        </div>
      </div>
      <div class="stack-cat">
        <div class="stack-cat-label"><i class="ti ti-tool" aria-hidden="true"></i> Tools</div>
        <div class="tech-pills">
          <span class="tech-pill"><i class="ti ti-brand-git"></i>Git</span>
          <span class="tech-pill"><i class="ti ti-brand-docker"></i>Docker</span>
          <span class="tech-pill"><i class="ti ti-brand-ubuntu"></i>Linux</span>
          <span class="tech-pill">Bash</span>
        </div>
      </div>
      <div class="stack-cat">
        <div class="stack-cat-label"><i class="ti ti-device-desktop" aria-hidden="true"></i> Environments</div>
        <div class="tech-pills">
          <span class="tech-pill"><i class="ti ti-brand-vscode"></i>VS Code</span>
          <span class="tech-pill">RStudio</span>
          <span class="tech-pill">IntelliJ</span>
          <span class="tech-pill"><i class="ti ti-sparkles"></i>Project IDX</span>
        </div>
      </div>
    </div>
  </div>

  <div class="section">
    <div class="section-header">
      <i class="ti ti-robot" aria-hidden="true"></i>
      <span>AI Orchestration</span>
    </div>
    <div class="card">
      <div class="card-label" style="margin-bottom: 12px;">Multi-agent systems &amp; LLM tooling</div>
      <div class="orch-tags">
        <span class="orch-tag"><i class="ti ti-link-plus"></i> LangChain / LangGraph</span>
        <span class="orch-tag"><i class="ti ti-users-group"></i> Multi-agent pipelines</span>
        <span class="orch-tag"><i class="ti ti-message-dots"></i> Prompt engineering</span>
        <span class="orch-tag"><i class="ti ti-database"></i> RAG systems</span>
        <span class="orch-tag"><i class="ti ti-sparkles"></i> Project IDX (Google)</span>
        <span class="orch-tag"><i class="ti ti-arrows-exchange"></i> LLM API integration</span>
      </div>
    </div>
  </div>

  <div class="section">
    <div class="section-header">
      <i class="ti ti-device-laptop" aria-hidden="true"></i>
      <span>Dev environment</span>
    </div>
    <div class="card">
      <div class="env-row">
        <i class="ti ti-sparkles env-icon" aria-hidden="true"></i>
        <span class="env-name">Project IDX</span>
        <span class="env-desc">Google's AI-powered cloud IDE</span>
      </div>
      <div class="env-row">
        <i class="ti ti-brand-vscode env-icon" aria-hidden="true"></i>
        <span class="env-name">VS Code</span>
        <span class="env-desc">Primary local editor</span>
      </div>
      <div class="env-row">
        <i class="ti ti-chart-scatter env-icon" aria-hidden="true"></i>
        <span class="env-name">RStudio</span>
        <span class="env-desc">Statistical computing &amp; visualisation</span>
      </div>
      <div class="env-row">
        <i class="ti ti-brand-intellij env-icon" aria-hidden="true"></i>
        <span class="env-name">IntelliJ IDEA</span>
        <span class="env-desc">JVM ecosystem &amp; Java development</span>
      </div>
      <div class="env-row">
        <i class="ti ti-brand-ubuntu env-icon" aria-hidden="true"></i>
        <span class="env-name">Linux / Bash</span>
        <span class="env-desc">Shell scripting &amp; system tooling</span>
      </div>
    </div>
  </div>

</div>
