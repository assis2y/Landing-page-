<!DOCTYPE html>
<html lang="pt-br">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>VKMR — VinckMonero</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=IBM+Plex+Mono:wght@400;500;600&family=Fraunces:opsz,wght@9..144,400;9..144,500;9..144,600&display=swap" rel="stylesheet">
<style>
  :root{
    --ink:#0B0D10;
    --panel:#12151A;
    --panel-line:#22262E;
    --paper:#E7E3D8;
    --paper-dim:#9C9A90;
    --amber:#D4A73D;
    --amber-dim:#8A712C;
    --redact:#1C2026;
  }
  *{box-sizing:border-box; margin:0; padding:0;}
  html{scroll-behavior:smooth;}
  body{
    background:var(--ink);
    color:var(--paper);
    font-family:'IBM Plex Mono', monospace;
    line-height:1.6;
    -webkit-font-smoothing:antialiased;
  }
  @media (prefers-reduced-motion: reduce){
    *{animation-duration:0.01ms !important; animation-iteration-count:1 !important; transition-duration:0.01ms !important;}
  }
  a{color:var(--amber); text-decoration:none;}
  a:hover{text-decoration:underline;}
  a:focus-visible, button:focus-visible{outline:2px solid var(--amber); outline-offset:3px;}

  .wrap{max-width:920px; margin:0 auto; padding:0 24px;}
  .eyebrow{
    font-size:12px; letter-spacing:.18em; text-transform:uppercase;
    color:var(--amber-dim); display:flex; align-items:center; gap:10px;
  }
  .eyebrow::before{content:""; width:6px; height:6px; background:var(--amber); border-radius:50%; display:inline-block; animation:pulse 2.4s ease-in-out infinite;}
  @keyframes pulse{0%,100%{opacity:1;} 50%{opacity:.25;}}

  header.hero{
    min-height:92vh; display:flex; flex-direction:column; justify-content:center;
    border-bottom:1px solid var(--panel-line);
    position:relative; overflow:hidden;
  }
  header.hero .wrap{padding-top:80px; padding-bottom:80px;}
  .hero-top{margin-bottom:48px;}

  .redact-line{display:flex; flex-wrap:wrap; gap:.5ch;}
  h1.title{
    font-family:'Fraunces', serif;
    font-weight:600;
    font-size:clamp(56px, 12vw, 132px);
    letter-spacing:-0.02em;
    color:var(--paper);
    line-height:0.95;
    display:flex;
  }
  .glyph{
    position:relative;
    display:inline-block;
    background:var(--redact);
    color:transparent;
    border-radius:3px;
    animation:reveal 0.05s steps(1) forwards;
    animation-fill-mode:forwards;
  }
  .glyph.on{background:transparent; color:var(--paper);}

  .tagline{
    max-width:52ch; margin-top:28px; font-size:17px; color:var(--paper-dim);
    font-family:'IBM Plex Mono', monospace;
  }
  .tagline b{color:var(--paper); font-weight:500;}

  .hero-meta{
    display:flex; gap:32px; margin-top:56px; flex-wrap:wrap;
    font-size:13px; color:var(--paper-dim);
  }
  .hero-meta div{border-left:2px solid var(--panel-line); padding-left:12px;}
  .hero-meta strong{display:block; color:var(--amber); font-weight:500; font-size:14px; margin-bottom:2px;}

  section{padding:96px 0; border-bottom:1px solid var(--panel-line);}
  .label{
    font-size:12px; letter-spacing:.16em; text-transform:uppercase; color:var(--amber-dim);
    margin-bottom:20px; display:block;
  }
  h2{
    font-family:'Fraunces', serif; font-weight:500; font-size:clamp(28px,4vw,40px);
    color:var(--paper); max-width:22ch; margin-bottom:24px; letter-spacing:-.01em;
  }
  p.lead{max-width:60ch; color:var(--paper-dim); font-size:16px;}
  p.lead b{color:var(--paper); font-weight:500;}

  .notice{
    margin-top:32px; padding:16px 18px; background:var(--panel);
    border:1px solid var(--panel-line); border-left:3px solid var(--amber-dim);
    font-size:13px; color:var(--paper-dim); max-width:60ch;
  }

  /* ring diagram */
  .ring-wrap{display:flex; justify-content:center; align-items:center; margin:56px 0;}
  svg.ring{width:min(360px, 80vw); height:auto;}
  .ring-node{fill:var(--redact); stroke:var(--panel-line); stroke-width:1;}
  .ring-node.active{fill:var(--amber); }
  .ring-edge{stroke:var(--panel-line); stroke-width:1; fill:none;}
  .ring-edge.live{stroke:var(--amber-dim);}

  .grid2{display:grid; grid-template-columns:1fr 1fr; gap:40px; margin-top:40px;}
  @media(max-width:640px){.grid2{grid-template-columns:1fr;}}
  .card{background:var(--panel); border:1px solid var(--panel-line); padding:28px;}
  .card h3{font-family:'Fraunces',serif; font-weight:500; font-size:20px; margin-bottom:10px; color:var(--paper);}
  .card p{font-size:14px; color:var(--paper-dim);}

  .timeline{margin-top:40px; display:flex; flex-direction:column;}
  .tl-row{display:grid; grid-template-columns:120px 1fr; gap:24px; padding:20px 0; border-top:1px solid var(--panel-line);}
  .tl-row:last-child{border-bottom:1px solid var(--panel-line);}
  .tl-stage{font-size:13px; color:var(--amber); letter-spacing:.08em; text-transform:uppercase;}
  .tl-desc h4{font-family:'Fraunces',serif; font-weight:500; font-size:18px; color:var(--paper); margin-bottom:6px;}
  .tl-desc p{font-size:14px; color:var(--paper-dim);}

  .cta-row{display:flex; gap:16px; flex-wrap:wrap; margin-top:36px;}
  .btn{
    font-family:'IBM Plex Mono', monospace; font-size:14px; padding:13px 22px;
    border:1px solid var(--panel-line); background:transparent; color:var(--paper);
    cursor:pointer; display:inline-flex; align-items:center; gap:8px; transition:border-color .2s, color .2s;
  }
  .btn.primary{background:var(--amber); color:var(--ink); border-color:var(--amber); font-weight:600;}
  .btn.primary:hover{background:transparent; color:var(--amber); text-decoration:none;}
  .btn:not(.primary):hover{border-color:var(--amber-dim); color:var(--amber); text-decoration:none;}

  footer{padding:56px 0 80px;}
  footer .wrap{display:flex; justify-content:space-between; flex-wrap:wrap; gap:20px; font-size:13px; color:var(--paper-dim);}
  footer .disclaimer{max-width:56ch; margin-top:24px; font-size:12px; color:var(--panel-line); line-height:1.7;}
  footer .disclaimer{color:#5b5f66;}
</style>
</head>
<body>

<header class="hero">
  <div class="wrap">
    <div class="hero-top">
      <span class="eyebrow">projeto de estudo &middot; solidity &middot; em construção</span>
    </div>
    <h1 class="title" id="title" aria-label="VKMR"></h1>
    <p class="tagline">
      <b>VinckMonero (VKMR)</b> é um token experimental escrito em Solidity, construído para aprender —
      publicamente, um commit de cada vez — como funcionam privacidade e propriedade em cadeia.
    </p>
    <div class="hero-meta">
      <div><strong>VKMR</strong>ticker</div>
      <div><strong>Solidity</strong>linguagem</div>
      <div><strong>GitHub</strong>código aberto</div>
      <div><strong>Estudo</strong>não é produto</div>
    </div>
    <div class="cta-row">
      <a class="btn primary" href="https://github.com/assis2y/Vinckmonero-" target="_blank" rel="noopener">Ver o repositório</a>
      <a class="btn" href="https://x.com/assis2y" target="_blank" rel="noopener">Acompanhar no X</a>
    </div>
  </div>
</header>

<section id="what">
  <div class="wrap">
    <span class="label">O que é</span>
    <h2>Um contrato, aberto, sendo construído em público</h2>
    <p class="lead">
      VKMR nasceu como <b>exercício de engenharia</b>: entender, na prática, como um contrato de token
      é estruturado, testado e evoluído — usando conceitos de privacidade explorados por projetos como
      o Monero como referência de estudo, não como promessa de produto pronto.
    </p>
    <div class="notice">
      Este é um projeto educacional em desenvolvimento ativo. Não é uma oferta de investimento,
      não tem garantias de valor ou liquidez, e o código pode mudar a qualquer momento.
    </div>
  </div>
</section>

<section id="privacy">
  <div class="wrap">
    <span class="label">Por que privacidade</span>
    <h2>Cada nó da rede confirma sem revelar quem confirmou</h2>
    <p class="lead">
      A referência de estudo por trás do VKMR é o conceito de <b>assinaturas em anel</b>: um grupo de
      participantes valida uma transação em conjunto, sem expor qual deles a originou. O diagrama
      abaixo é uma representação simplificada dessa ideia — o ponto em destaque muda, mas a origem
      real permanece indistinguível dentro do anel.
    </p>
    <div class="ring-wrap">
      <svg class="ring" viewBox="0 0 300 300" role="img" aria-label="Diagrama de anel representando assinatura em grupo">
        <g id="ringGroup"></g>
      </svg>
    </div>
  </div>
</section>

<section id="build">
  <div class="wrap">
    <span class="label">Construído em público</span>
    <h2>O repositório é o registro de verdade</h2>
    <p class="lead">Todo progresso — testes, refatorações, decisões de arquitetura — fica versionado e visível.</p>
    <div class="grid2">
      <div class="card">
        <h3>Código</h3>
        <p>O contrato evolui a partir do que já existe no repositório, sem reescritas do zero. Cada mudança parte do histórico anterior.</p>
      </div>
      <div class="card">
        <h3>Contribuição</h3>
        <p>Issues marcadas como ponto de entrada para quem quiser explorar o código e sugerir melhorias.</p>
      </div>
    </div>
  </div>
</section>

<section id="roadmap">
  <div class="wrap">
    <span class="label">Andamento</span>
    <h2>Onde o projeto está agora</h2>
    <div class="timeline">
      <div class="tl-row">
        <div class="tl-stage">Atual</div>
        <div class="tl-desc">
          <h4>Base do contrato</h4>
          <p>Estrutura em Solidity herdada do repositório original, em revisão e documentação.</p>
        </div>
      </div>
      <div class="tl-row">
        <div class="tl-stage">Em seguida</div>
        <div class="tl-desc">
          <h4>Testes e cobertura</h4>
          <p>Suíte de testes para validar comportamento do token antes de qualquer nova funcionalidade.</p>
        </div>
      </div>
      <div class="tl-row">
        <div class="tl-stage">Depois</div>
        <div class="tl-desc">
          <h4>Documentação pública</h4>
          <p>README e whitepaper curto explicando decisões técnicas, para quem quiser acompanhar ou contribuir.</p>
        </div>
      </div>
    </div>
  </div>
</section>

<footer>
  <div class="wrap">
    <div>VKMR — VinckMonero</div>
    <div><a href="https://github.com/assis2y/Vinckmonero-" target="_blank" rel="noopener">github.com/assis2y/Vinckmonero-</a> &middot; <a href="https://x.com/assis2y" target="_blank" rel="noopener">@assis2y</a></div>
  </div>
  <div class="wrap">
    <p class="disclaimer">
      Projeto pessoal de estudo em Solidity. Nada nesta página constitui aconselhamento financeiro
      ou oferta de compra/venda de qualquer ativo.
    </p>
  </div>
</footer>

<script>
  // Redaction-reveal title animation
  const word = "VKMR";
  const titleEl = document.getElementById('title');
  word.split('').forEach((ch, i) => {
    const span = document.createElement('span');
    span.className = 'glyph';
    span.textContent = ch;
    span.style.animationDelay = (0.4 + i * 0.18) + 's';
    titleEl.appendChild(span);
  });
  const glyphs = titleEl.querySelectorAll('.glyph');
  glyphs.forEach((g, i) => {
    setTimeout(() => g.classList.add('on'), 400 + i * 180 + 260);
  });

  // Ring diagram: nodes around a circle, one highlighted node cycles
  const svgNS = "http://www.w3.org/2000/svg";
  const group = document.getElementById('ringGroup');
  const cx = 150, cy = 150, r = 100;
  const n = 8;
  const nodes = [];
  for (let i = 0; i < n; i++) {
    const angle = (i / n) * Math.PI * 2 - Math.PI / 2;
    const x = cx + r * Math.cos(angle);
    const y = cy + r * Math.sin(angle);
    nodes.push({x, y});
  }
  // edges (ring)
  for (let i = 0; i < n; i++) {
    const a = nodes[i], b = nodes[(i + 1) % n];
    const line = document.createElementNS(svgNS, 'line');
    line.setAttribute('x1', a.x); line.setAttribute('y1', a.y);
    line.setAttribute('x2', b.x); line.setAttribute('y2', b.y);
    line.setAttribute('class', 'ring-edge');
    group.appendChild(line);
  }
  const circles = nodes.map((p) => {
    const c = document.createElementNS(svgNS, 'circle');
    c.setAttribute('cx', p.x); c.setAttribute('cy', p.y); c.setAttribute('r', 9);
    c.setAttribute('class', 'ring-node');
    group.appendChild(c);
    return c;
  });
  let activeIdx = 0;
  circles[activeIdx].classList.add('active');
  const reduced = window.matchMedia('(prefers-reduced-motion: reduce)').matches;
  if (!reduced) {
    setInterval(() => {
      circles[activeIdx].classList.remove('active');
      activeIdx = (activeIdx + 1) % n;
      circles[activeIdx].classList.add('active');
    }, 1400);
  }
</script>

</body>
</html>
