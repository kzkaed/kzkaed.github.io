<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>topology.work — style guide v1</title>
<style>
  /* ── tokens (exact match to main.min.css) ── */
  :root {
    --bg: #f9f9f7;
    --text: #1a1a1a;
    --secondary: #707070; /* was #888 — lifted to pass WCAG AA 4.5:1 (4.70:1 on --bg) */
    --border: #e2e2e0;
    --max-width: 680px;
    --font: -apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif;
    --mono: 'SF Mono', 'Fira Code', 'Fira Mono', monospace;
  }

  [data-theme="dark"] {
    --bg: #111110;
    --text: #e8e8e6;
    --secondary: #8a8a8a; /* was #5a5a58 — lifted to pass WCAG AA 4.5:1 (5.47:1 on --bg) */
    --border: #242422;
  }

  /* ── reset ── */
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  html { font-size: 17px; -webkit-font-smoothing: antialiased; }

  body {
    font-family: var(--font);
    background: var(--bg);
    color: var(--text);
    line-height: 1.65;
    min-height: 100dvh;
    display: flex;
    flex-direction: column;
  }

  /* ── site chrome (matches live site) ── */
  header { border-bottom: 1px solid var(--border); }

  nav {
    max-width: var(--max-width);
    margin: 0 auto;
    padding: 1.25rem 1.5rem;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  .wordmark {
    font-family: var(--mono);
    font-size: .9rem;
    font-weight: 500;
    color: var(--text);
    text-decoration: none;
    letter-spacing: -.01em;
  }
  .wordmark:hover { color: var(--secondary); }

  #theme-toggle {
    background: 0 0;
    border: 1px solid var(--border);
    border-radius: 4px;
    width: 32px;
    height: 32px;
    cursor: pointer;
    color: var(--secondary);
    font-size: .8rem;
    display: flex;
    align-items: center;
    justify-content: center;
    transition: border-color .15s, color .15s;
  }
  #theme-toggle::after { content: '◐'; }
  #theme-toggle:hover { border-color: var(--text); color: var(--text); }

  main {
    max-width: var(--max-width);
    margin: 0 auto;
    padding: 3rem 1.5rem;
    flex: 1;
    width: 100%;
  }

  footer {
    border-top: 1px solid var(--border);
    padding: 1.25rem 1.5rem;
    text-align: center;
  }
  footer span {
    font-family: var(--mono);
    font-size: .75rem;
    color: var(--secondary);
  }

  /* ── style guide layout ── */
  .sg-header {
    margin-bottom: 3rem;
    padding-bottom: 1.5rem;
    border-bottom: 1px solid var(--border);
  }
  .sg-header h1 {
    font-size: 1rem;
    font-weight: 600;
    letter-spacing: -.02em;
    line-height: 1.25;
    margin-bottom: .4rem;
  }
  .sg-header p {
    font-size: .85rem;
    color: var(--secondary);
  }

  .sg-section {
    margin-bottom: 3rem;
  }

  .sg-label {
    font-family: var(--mono);
    font-size: .7rem;
    letter-spacing: .1em;
    text-transform: uppercase;
    color: var(--secondary);
    margin-bottom: 1.25rem;
    display: block;
  }

  .sg-rule {
    border: none;
    border-top: 1px solid var(--border);
    margin: 2.5rem 0;
  }

  /* ── specimen blocks ── */
  .specimen {
    margin-bottom: 1.5rem;
  }

  .specimen-label {
    font-family: var(--mono);
    font-size: .72rem;
    color: var(--secondary);
    margin-top: .6rem;
  }

  /* ── token table ── */
  .token-table {
    width: 100%;
    border-collapse: collapse;
    font-size: .85rem;
  }
  .token-table tr {
    border-bottom: 1px solid var(--border);
  }
  .token-table tr:last-child { border-bottom: none; }
  .token-table td {
    padding: .65rem 0;
    vertical-align: middle;
  }
  .token-table td:first-child {
    font-family: var(--mono);
    font-size: .78rem;
    color: var(--secondary);
    width: 38%;
  }
  .swatch {
    display: inline-block;
    width: 20px;
    height: 20px;
    border-radius: 3px;
    border: 1px solid var(--border);
    vertical-align: middle;
    margin-right: 8px;
    flex-shrink: 0;
  }

  /* ── code blocks ── */
  pre, code {
    font-family: var(--mono);
    font-size: .82rem;
  }
  pre {
    background: var(--border);
    padding: 1rem 1.1rem;
    border-radius: 4px;
    overflow-x: auto;
    line-height: 1.65;
    color: var(--text);
    margin-bottom: 1rem;
  }
  code {
    background: var(--border);
    padding: .1em .35em;
    border-radius: 3px;
    font-size: .85em;
  }
  pre code { background: none; padding: 0; font-size: inherit; }

  /* ── typography specimens ── */
  .type-post-title {
    font-size: 1rem;
    font-weight: 400;
    color: var(--text);
    transition: opacity .15s;
  }
  .type-post-title:hover { opacity: .6; cursor: pointer; }

  .type-h1 {
    font-size: 1rem;
    font-weight: 600;
    letter-spacing: -.02em;
    line-height: 1.25;
    color: var(--text);
  }

  .type-h2 {
    font-size: 1.2rem;
    font-weight: 600;
    letter-spacing: -.01em;
    color: var(--text);
  }

  .type-h3 {
    font-size: 1rem;
    font-weight: 600;
    color: var(--text);
  }

  .type-body {
    font-size: 1rem;
    line-height: 1.75;
    color: var(--text);
  }
  .type-body p + p { margin-top: 1.4rem; }

  .type-meta {
    font-size: .8rem;
    color: var(--secondary);
    font-variant-numeric: tabular-nums;
  }

  .type-wordmark {
    font-family: var(--mono);
    font-size: .9rem;
    font-weight: 500;
    letter-spacing: -.01em;
    color: var(--text);
  }

  .type-footer {
    font-family: var(--mono);
    font-size: .75rem;
    color: var(--secondary);
  }

  blockquote.demo {
    border-left: 2px solid var(--border);
    padding-left: 1rem;
    color: var(--secondary);
    margin: 0;
  }

  /* ── post list demo ── */
  .post-list-demo { display: flex; flex-direction: column; gap: 0; }
  .post-entry-demo {
    display: flex;
    justify-content: space-between;
    align-items: baseline;
    gap: 1rem;
    padding: .85rem 0;
    border-bottom: 1px solid var(--border);
    text-decoration: none;
    color: var(--text);
    cursor: pointer;
  }
  .post-entry-demo:first-child { border-top: 1px solid var(--border); }
  .post-entry-demo:hover .post-entry-title { opacity: .6; }
  .post-entry-title {
    font-size: 1rem;
    transition: opacity .15s;
  }
  .post-entry-date {
    font-size: .8rem;
    color: var(--secondary);
    white-space: nowrap;
    font-variant-numeric: tabular-nums;
  }

  /* ── link demo ── */
  a.demo-link {
    color: var(--text);
    text-decoration: underline;
    text-underline-offset: 3px;
  }
  a.demo-link:hover { color: var(--secondary); }

  /* ── color grid ── */
  .color-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 0;
  }
  .color-cell {
    padding: .75rem 0;
    border-bottom: 1px solid var(--border);
    display: flex;
    align-items: center;
    gap: 10px;
    font-size: .82rem;
  }
  .color-cell:nth-last-child(-n+2) { border-bottom: none; }

  /* ── spacing bar ── */
  .spacing-row {
    display: flex;
    align-items: center;
    gap: 14px;
    padding: .5rem 0;
    border-bottom: 1px solid var(--border);
    font-size: .82rem;
  }
  .spacing-row:last-child { border-bottom: none; }
  .spacing-bar {
    background: var(--secondary);
    height: 8px;
    border-radius: 2px;
    opacity: .4;
    flex-shrink: 0;
  }
  .spacing-name {
    font-family: var(--mono);
    font-size: .75rem;
    color: var(--secondary);
    min-width: 72px;
  }
  .spacing-use {
    color: var(--text);
  }

  /* ── dark mode notice ── */
  .dark-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 1rem;
  }
  .dark-swatch-box {
    padding: 1.25rem;
    border-radius: 4px;
    border: 1px solid var(--border);
  }

  @media (max-width: 600px) {
    html { font-size: 16px; }
    main { padding: 2rem 1.25rem; }
    .color-grid { grid-template-columns: 1fr; }
    .dark-grid { grid-template-columns: 1fr; }
  }
</style>
</head>
<body>

<header>
  <nav>
    <a class="wordmark" href="#">topology.work</a>
    <button id="theme-toggle" aria-label="toggle theme" onclick="toggleTheme()"></button>
  </nav>
</header>

<main>

  <div class="sg-header">
    <h1>style guide — v1</h1>
    <p>Source of truth for topology.work visual language. Derived from <code>main.min.css</code>, April 2026.</p>
  </div>

  <!-- TOKENS -->
  <section class="sg-section">
    <span class="sg-label">01 — design tokens</span>

    <div class="specimen">
      <table class="token-table">
        <tr>
          <td><code>--bg</code></td>
          <td><span class="swatch" style="background:#f9f9f7"></span>#f9f9f7 — warm off-white · page background</td>
        </tr>
        <tr>
          <td><code>--text</code></td>
          <td><span class="swatch" style="background:#1a1a1a"></span>#1a1a1a — near-black · primary text</td>
        </tr>
        <tr>
          <td><code>--secondary</code></td>
          <td><span class="swatch" style="background:#707070"></span>#707070 — mid-gray · dates, meta, muted (was #888, lifted for WCAG AA)</td>
        </tr>
        <tr>
          <td><code>--border</code></td>
          <td><span class="swatch" style="background:#e2e2e0"></span>#e2e2e0 — warm gray · all rules and dividers</td>
        </tr>
        <tr>
          <td><code>--max-width</code></td>
          <td>680px — single centered content column</td>
        </tr>
        <tr>
          <td><code>--font</code></td>
          <td>-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui — no web fonts</td>
        </tr>
        <tr>
          <td><code>--mono</code></td>
          <td>'SF Mono', 'Fira Code', 'Fira Mono' — wordmark, footer, code</td>
        </tr>
      </table>
    </div>

    <div class="specimen">
      <p style="font-size:.85rem;color:var(--secondary);line-height:1.7">
        No accent color is defined. Links use <code>--text</code> with underline; hover shifts to <code>--secondary</code>. Color is not used as signal — only structure and weight.
      </p>
    </div>
  </section>

  <hr class="sg-rule">

  <!-- TYPOGRAPHY -->
  <section class="sg-section">
    <span class="sg-label">02 — typography</span>

    <div class="specimen">
      <div class="type-wordmark">topology.work</div>
      <p class="specimen-label">.wordmark — mono, 0.9rem, weight 500, ls −0.01em</p>
    </div>

    <div class="specimen">
      <div class="type-h1">The conditions beneath the work</div>
      <p class="specimen-label">.post-header h1 — 1rem, weight 600, ls −0.02em, lh 1.25</p>
    </div>

    <div class="specimen">
      <div class="type-h2">Section heading</div>
      <p class="specimen-label">post-content h2 — 1.2rem, weight 600, ls −0.01em</p>
    </div>

    <div class="specimen">
      <div class="type-h3">Sub-heading</div>
      <p class="specimen-label">post-content h3 — 1rem, weight 600</p>
    </div>

    <div class="specimen">
      <div class="type-post-title">New Space</div>
      <p class="specimen-label">.post-title — 1rem, weight 400 · hover → opacity 0.6</p>
    </div>

    <div class="specimen">
      <div class="type-body">
        <p>Software doesn't fail at the feature level. It fails at the substrate — the decisions made before the code was written, the constraints no one named, the assumptions baked into every pull request.</p>
        <p>The question isn't which framework you chose. It's what the framework made invisible.</p>
      </div>
      <p class="specimen-label">.post-content — 1rem, lh 1.75 · p + p margin-top 1.4rem</p>
    </div>

    <div class="specimen">
      <blockquote class="demo">
        The map is not the territory. The methodology is not the work.
      </blockquote>
      <p class="specimen-label">blockquote — border-left 2px --border, padding-left 1rem, color --secondary</p>
    </div>

    <div class="specimen">
      <p class="type-body">
        Run <code>hugo serve --buildDrafts</code> to preview. See the
        <a class="demo-link" href="#">deployment guide</a> for CI setup.
      </p>
      <p class="specimen-label">inline code — mono, 0.85em, bg --border, radius 3px · link — --text + underline, hover --secondary</p>
    </div>

    <div class="specimen">
      <div class="type-meta">Apr 2026</div>
      <p class="specimen-label">time — 0.8rem, --secondary, font-variant-numeric: tabular-nums</p>
    </div>

    <div class="specimen">
      <div class="type-footer">topology.work</div>
      <p class="specimen-label">footer span — mono, 0.75rem, --secondary</p>
    </div>
  </section>

  <hr class="sg-rule">

  <!-- COMPONENTS -->
  <section class="sg-section">
    <span class="sg-label">03 — components</span>

    <div class="specimen">
      <div class="post-list-demo">
        <div class="post-entry-demo">
          <span class="post-entry-title">New Space</span>
          <time class="post-entry-date">Apr 2026</time>
        </div>
        <div class="post-entry-demo">
          <span class="post-entry-title">On the intent loop</span>
          <time class="post-entry-date">Mar 2026</time>
        </div>
        <div class="post-entry-demo">
          <span class="post-entry-title">What Wardley mapping reveals</span>
          <time class="post-entry-date">Feb 2026</time>
        </div>
      </div>
      <p class="specimen-label">.post-list — flex col, gap 0 · .post-entry — space-between, baseline, padding .85rem 0, border-bottom 1px --border · first-child gets border-top</p>
    </div>

    <div class="specimen">
      <pre>hugo serve --buildDrafts --port 1313</pre>
      <p class="specimen-label">pre — bg --border, radius 4px, overflow-x auto, mono 0.85rem · nested code: bg none, padding 0</p>
    </div>

    <div class="specimen" style="display:flex;align-items:center;gap:12px">
      <button id="theme-toggle-demo" style="background:0 0;border:1px solid var(--border);border-radius:4px;width:32px;height:32px;cursor:pointer;color:var(--secondary);font-size:.8rem;display:flex;align-items:center;justify-content:center">◐</button>
      <span style="font-size:.85rem;color:var(--secondary)">theme toggle — 32×32px, border-radius 4px, mono ◐ glyph</span>
    </div>
    <p class="specimen-label" style="margin-top:.5rem">#theme-toggle — hover: border --text, color --text · toggles [data-theme="dark"] on &lt;html&gt;</p>
  </section>

  <hr class="sg-rule">

  <!-- SPACING -->
  <section class="sg-section">
    <span class="sg-label">04 — spacing</span>

    <div class="spacing-row">
      <span class="spacing-name">.85rem 0</span>
      <div class="spacing-bar" style="width:calc(.85 * 17px)"></div>
      <span class="spacing-use">post-entry vertical padding</span>
    </div>
    <div class="spacing-row">
      <span class="spacing-name">1rem</span>
      <div class="spacing-bar" style="width:17px"></div>
      <span class="spacing-use">blockquote padding-left</span>
    </div>
    <div class="spacing-row">
      <span class="spacing-name">1.25rem</span>
      <div class="spacing-bar" style="width:calc(1.25 * 17px)"></div>
      <span class="spacing-use">nav/footer vertical · post-header padding-bottom</span>
    </div>
    <div class="spacing-row">
      <span class="spacing-name">1.4rem</span>
      <div class="spacing-bar" style="width:calc(1.4 * 17px)"></div>
      <span class="spacing-use">paragraph gap (p + p)</span>
    </div>
    <div class="spacing-row">
      <span class="spacing-name">1.5rem</span>
      <div class="spacing-bar" style="width:calc(1.5 * 17px)"></div>
      <span class="spacing-use">post-header border margin · code block margin</span>
    </div>
    <div class="spacing-row">
      <span class="spacing-name">2rem</span>
      <div class="spacing-bar" style="width:34px"></div>
      <span class="spacing-use">h2 top margin · mobile main padding</span>
    </div>
    <div class="spacing-row">
      <span class="spacing-name">2.5rem</span>
      <div class="spacing-bar" style="width:calc(2.5 * 17px)"></div>
      <span class="spacing-use">post-header bottom margin</span>
    </div>
    <div class="spacing-row">
      <span class="spacing-name">3rem</span>
      <div class="spacing-bar" style="width:51px"></div>
      <span class="spacing-use">main top/bottom padding</span>
    </div>
  </section>

  <hr class="sg-rule">

  <!-- DARK MODE -->
  <section class="sg-section">
    <span class="sg-label">05 — dark mode</span>

    <div class="specimen">
      <table class="token-table">
        <tr>
          <td><code>--bg</code></td>
          <td><span class="swatch" style="background:#111110;border-color:#444"></span>#111110</td>
        </tr>
        <tr>
          <td><code>--text</code></td>
          <td><span class="swatch" style="background:#e8e8e6;border-color:#444"></span>#e8e8e6</td>
        </tr>
        <tr>
          <td><code>--secondary</code></td>
          <td><span class="swatch" style="background:#8a8a8a;border-color:#444"></span>#8a8a8a — was #5a5a58, lifted for WCAG AA</td>
        </tr>
        <tr>
          <td><code>--border</code></td>
          <td><span class="swatch" style="background:#242422;border-color:#555"></span>#242422</td>
        </tr>
      </table>
      <p class="specimen-label">only four tokens change · structure and layout are identical · toggle via [data-theme="dark"] on html</p>
    </div>

    <div class="specimen">
      <div style="background:#111110;border:1px solid #242422;border-radius:4px;padding:1.25rem 1.5rem">
        <div style="display:flex;justify-content:space-between;align-items:center;margin-bottom:1.25rem">
          <span style="font-family:var(--mono);font-size:.9rem;font-weight:500;letter-spacing:-.01em;color:#e8e8e6">topology.work</span>
          <span style="border:1px solid #242422;border-radius:4px;width:32px;height:32px;display:flex;align-items:center;justify-content:center;color:#8a8a8a;font-size:.8rem">◐</span>
        </div>
        <div style="border-top:1px solid #242422;border-bottom:1px solid #242422;display:flex;justify-content:space-between;align-items:baseline;padding:.85rem 0;gap:1rem">
          <span style="font-size:17px;color:#e8e8e6">New Space</span>
          <time style="font-size:.8rem;color:#8a8a8a;font-variant-numeric:tabular-nums">Apr 2026</time>
        </div>
        <div style="margin-top:1.25rem;text-align:center">
          <span style="font-family:var(--mono);font-size:.75rem;color:#8a8a8a">topology.work</span>
        </div>
      </div>
      <p class="specimen-label">dark mode preview — hardcoded to show dark regardless of system preference</p>
    </div>
  </section>

  <hr class="sg-rule">

  <!-- CSS SOURCE -->
  <section class="sg-section">
    <span class="sg-label">06 — css source (minified)</span>
    <pre style="font-size:.72rem;word-break:break-all;white-space:pre-wrap">:root{--bg:#f9f9f7;--text:#1a1a1a;--secondary:#707070;--border:#e2e2e0;--max-width:680px;--font:-apple-system,BlinkMacSystemFont,'Segoe UI',system-ui,sans-serif;--mono:'SF Mono','Fira Code','Fira Mono',monospace}
[data-theme=dark]{--bg:#111110;--text:#e8e8e6;--secondary:#8a8a8a;--border:#242422}</pre>
    <p class="specimen-label" style="margin-top:.5rem">complete token block from kzkaed.github.io/css/main.min.css · retrieved Apr 2026</p>
  </section>

</main>

<footer>
  <span>topology.work — style guide v1 · Apr 2026</span>
</footer>

<script>
  function toggleTheme() {
    const html = document.documentElement;
    html.dataset.theme = html.dataset.theme === 'dark' ? '' : 'dark';
  }
</script>

</body>
</html>
