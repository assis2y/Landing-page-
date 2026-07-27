<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>$vinckmonero Token — Solana Meme Coin</title>
<style>
*{margin:0;padding:0;box-sizing:border-box}
body{font-family:-apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,"Helvetica Neue",Arial,sans-serif;background:#0a0a0a;color:#fff;min-height:100vh}
.w{width:100%;max-width:720px;margin:0 auto;padding:24px 16px}
.th{text-align:center;margin-bottom:24px}
.tl{width:80px;height:80px;border-radius:50%;background:#1a1a1a;border:1px solid #2a2a2a;display:flex;align-items:center;justify-content:center;margin:0 auto 16px;font-size:32px}
.tn{font-size:28px;font-weight:600;margin-bottom:4px}
.ts{font-size:16px;color:#888}
.cb{background:#1a1a1a;border:1px solid #2a2a2a;border-radius:12px;padding:12px 16px;margin-bottom:20px;display:flex;align-items:center;gap:12px}
.cl{font-size:12px;color:#666;text-transform:uppercase;letter-spacing:.5px;white-space:nowrap}
.ca{font-family:"SF Mono",Monaco,monospace;font-size:13px;color:#aaa;flex:1;overflow:hidden;text-overflow:ellipsis;white-space:nowrap}
.ca2{display:flex;gap:8px}
.ib{width:32px;height:32px;border-radius:8px;border:1px solid #2a2a2a;background:transparent;color:#888;cursor:pointer;display:flex;align-items:center;justify-content:center;transition:all .15s ease}
.ib:hover{background:#2a2a2a;color:#fff}
.ib svg{width:16px;height:16px}
.ag{display:grid;grid-template-columns:repeat(2,1fr);gap:12px;margin-bottom:20px}
.ab{display:flex;align-items:center;justify-content:center;gap:8px;padding:14px 16px;border-radius:12px;border:1px solid #2a2a2a;background:#1a1a1a;color:#fff;font-size:15px;font-weight:500;cursor:pointer;text-decoration:none;transition:all .15s ease}
.ab:hover{background:#2a2a2a;border-color:#fff}
.ab.p{background:#fff;color:#0a0a0a;border-color:#fff}
.ab.p:hover{opacity:.9}
.ab svg{width:18px;height:18px}
.sg{display:grid;grid-template-columns:repeat(3,1fr);gap:12px;margin-bottom:20px}
.sb{display:flex;align-items:center;justify-content:center;gap:8px;padding:12px;border-radius:12px;border:1px solid #2a2a2a;background:#1a1a1a;color:#888;font-size:14px;cursor:pointer;text-decoration:none;transition:all .15s ease}
.sb:hover{background:#2a2a2a;color:#fff;border-color:#fff}
.sb svg{width:18px;height:18px}
.stg{display:grid;grid-template-columns:repeat(3,1fr);gap:12px;margin-bottom:20px}
.sc{background:#1a1a1a;border:1px solid #2a2a2a;border-radius:12px;padding:16px;text-align:center}
.sv{font-size:20px;font-weight:600;margin-bottom:4px}
.sl{font-size:12px;color:#666}
.se{background:#1a1a1a;border:1px solid #2a2a2a;border-radius:12px;padding:16px;margin-bottom:20px}
.st{font-size:15px;font-weight:600;margin-bottom:16px;display:flex;align-items:center;gap:8px}
.st svg{width:18px;height:18px;color:#888}
.tb{display:flex;flex-direction:column;gap:12px}
.tr{display:flex;align-items:center;gap:12px}
.tl2{width:100px;font-size:13px;color:#888;flex-shrink:0}
.tt{flex:1;height:24px;background:#0a0a0a;border-radius:6px;overflow:hidden}
.tf{height:100%;border-radius:6px}
.tv{width:50px;font-size:13px;font-weight:500;text-align:right;flex-shrink:0}
.rm{position:relative;padding-left:24px}
.rm::before{content:'';position:absolute;left:7px;top:4px;bottom:4px;width:2px;background:#2a2a2a}
.ri{position:relative;margin-bottom:20px}
.ri:last-child{margin-bottom:0}
.rd{position:absolute;left:-20px;top:2px;width:12px;height:12px;border-radius:50%;border:2px solid #2a2a2a;background:#1a1a1a}
.ri.d .rd{background:#22c55e;border-color:#22c55e}
.ri.a .rd{background:#3b82f6;border-color:#3b82f6}
.rp{font-size:12px;color:#666;margin-bottom:2px}
.rt{font-size:14px;font-weight:600;margin-bottom:4px}
.rde{font-size:13px;color:#888;line-height:1.5}
.sp{display:flex;flex-direction:column;gap:12px}
.stp{display:flex;gap:12px;align-items:flex-start}
.sn{width:28px;height:28px;border-radius:50%;background:#fff;color:#0a0a0a;display:flex;align-items:center;justify-content:center;font-size:13px;font-weight:600;flex-shrink:0}
.sct{flex:1}
.stt{font-size:14px;font-weight:600;margin-bottom:2px}
.sd{font-size:13px;color:#888;line-height:1.5}
.fi{border-bottom:1px solid #2a2a2a}
.fi:last-child{border-bottom:none}
.fq{display:flex;align-items:center;justify-content:space-between;padding:14px 0;cursor:pointer;font-size:14px;font-weight:600}
.fq svg{width:16px;height:16px;color:#666;transition:transform .2s ease;flex-shrink:0}
.fi.o .fq svg{transform:rotate(180deg)}
.fa{max-height:0;overflow:hidden;transition:max-height .3s ease,padding .3s ease}
.fi.o .fa{max-height:200px;padding-bottom:14px}
.fa p{font-size:13px;color:#888;line-height:1.6}
.wb{background:rgba(234,179,8,.1);border:1px solid rgba(234,179,8,.25);border-radius:12px;padding:12px 16px;display:flex;align-items:flex-start;gap:10px}
.wb svg{width:18px;height:18px;color:#eab308;flex-shrink:0;margin-top:2px}
.wt{font-size:13px;color:#888;line-height:1.5}
.toast{position:fixed;bottom:24px;left:50%;transform:translateX(-50%) translateY(100px);background:#fff;color:#0a0a0a;padding:10px 20px;border-radius:10px;font-size:14px;font-weight:600;opacity:0;transition:all .3s ease;pointer-events:none;z-index:100}
.toast.show{transform:translateX(-50%) translateY(0);opacity:1}
@media(max-width:480px){.ag{grid-template-columns:1fr}.stg{grid-template-columns:repeat(2,1fr)}.sg{grid-template-columns:1fr}.tn{font-size:22px}.tl2{width:80px;font-size:12px}}
</style>
</head>
<body>
<div class="w">
<div class="th"><div class="tl">🪙</div><div class="tn">$PUMP Token</div><div class="ts">Solana Meme Coin</div></div>

<div class="cb"><span class="cl">Contrato</span><span class="ca" id="cA">CLY71nCdMvJF4oFYfqqdRSjngCjtq6hPgfM8R569pump</span><div class="ca2"><button class="ib" onclick="navigator.clipboard.writeText(document.getElementById('cA').innerText);var t=document.getElementById('toast');t.classList.add('show');setTimeout(function(){t.classList.remove('show')},2000)" aria-label="Copiar"><svg width="16" height="16" viewBox="0 0 24 24" fill="none"><path fill-rule="evenodd" clip-rule="evenodd" d="M17 7.1c2.154 0 3.9 1.746 3.9 3.9v6c0 2.154-1.746 3.9-3.9 3.9h-6a3.9 3.9 0 01-3.9-3.9v-6c0-2.154 1.746-3.9 3.9-3.9h6zm-6 1.8a2.1 2.1 0 00-2.1 2.1v6c0 1.16.94 2.1 2.1 2.1h6a2.1 2.1 0 002.1-2.1v-6a2.1 2.1 0 00-2.1-2.1h-6zM5.1 3a.9.9 0 01.9-.9h8a.9.9 0 010 1.8h-8a.9.9 0 01-.9-.9zm-.2 2a.9.9 0 01.9-.9h8a.9.9 0 01.9.9v8a.9.9 0 01-1.8 0V5.9h-7.1a.9.9 0 01-.9-.9z" fill="currentColor"/></svg></button><a class="ib" href="https://solscan.io/token/CLY71nCdMvJF4oFYfqqdRSjngCjtq6hPgfM8R569pump" target="_blank" aria-label="Solscan"><svg width="16" height="16" viewBox="0 0 24 24" fill="none"><path fill-rule="evenodd" clip-rule="evenodd" d="M19.886 4.913a.9.9 0 00-.9-.897h-7.833a.9.9 0 000 1.8h5.663L4.293 18.364a.9.9 0 001.274 1.272L18.094 7.084v5.663a.9.9 0 001.8 0V5.085a.9.9 0 00-.008-.172z" fill="currentColor"/></svg></a></div></div>

<div class="ag"><a class="ab p" href="https://jup.ag/swap/SOL-CLY71nCdMvJF4oFYfqqdRSjngCjtq6hPgfM8R569pump" target="_blank"><svg width="18" height="18" viewBox="0 0 24 24" fill="none"><path d="M9.052 5.809V16.29a.9.9 0 001.8 0V7.824a.9.9 0 011.8 0v10.557a.9.9 0 001.374.77l6.069-4.43a.9.9 0 00.127-1.378l-7.136-6.194c-1.813-1.573-4.635-.285-4.635 2.115v-1.986a.9.9 0 00-1.8 0v1.986c-.91.055-1.64.179-2.273.366C3.893 9.052 1.7 11.793 1.7 15.016v1.968a.9.9 0 001.123.668.9.9 0 00.968-.414c.86-.885 1.594-1.332 2.312-1.588.559-.198 1.175-.306 1.949-.359V18.38a2.1 2.1 0 003.635 1.418l7.136-6.379a2.1 2.1 0 00-.127-3.378l-7.136-6.194a2.1 2.1 0 00-3.374 1.68v1.016z" fill="currentColor"/></svg>Comprar agora</a><a class="ab" href="https://dexscreener.com/solana/CLY71nCdMvJF4oFYfqqdRSjngCjtq6hPgfM8R569pump" target="_blank"><svg width="18" height="18" viewBox="0 0 24 24" fill="none"><path d="M4 3.085a1 1 0 011 1v13.951h14.994l.103.005a1 1 0 01-.103 1.995H5a2 2 0 01-2-2V4.085a1 1 0 011-1z" fill="currentColor"/><path d="M18.263 6.517a1 1 0 011.411 1.414l-4.95 4.95a1 1 0 01-1.414 0l-2.121-2.121a1 1 0 00-1.415 0l-3.536 3.536a1 1 0 11-1.414-1.414l3.536-3.536a3 3 0 014.243 0l1.414 1.414 4.243-4.243z" fill="currentColor"/></svg>Ver gráfico</a></div>

<div class="sg"><a class="sb" href="https://x.com/assis2y" target="_blank"><svg width="18" height="18" viewBox="0 0 24 24" fill="currentColor"><path d="M18.244 2.25h3.308l-7.227 8.26 8.502 11.24H16.17l-5.214-6.817L4.99 21.75H1.68l7.73-8.835L1.254 2.25H8.08l4.713 6.231zm-1.161 17.52h1.833L7.084 4.126H5.117z"/></svg>Twitter / X</a><a class="sb" href="https://t.me/" target="_blank"><svg width="18" height="18" viewBox="0 0 24 24" fill="currentColor"><path d="M11.944 0A12 12 0 0 0 0 12a12 12 0 0 0 12 12 12 12 0 0 0 12-12A12 12 0 0 0 12 0a12 12 0 0 0-.056 0zm4.962 7.224c.1-.002.321.023.465.14a.506.506 0 0 1 .171.325c.016.093.036.306.02.472-.18 1.898-.962 6.502-1.36 8.627-.168.9-.499 1.201-.82 1.23-.696.065-1.225-.46-1.9-.902-1.056-.693-1.653-1.124-2.678-1.8-1.185-.78-.417-1.21.258-1.91.177-.184 3.247-2.977 3.307-3.23.007-.032.014-.15-.056-.212s-.174-.041-.249-.024c-.106.024-1.793 1.14-5.061 3.345-.48.33-.913.49-1.302.48-.428-.008-1.252-.241-1.865-.44-.752-.245-1.349-.374-1.297-.789.027-.216.325-.437.893-.663 3.498-1.524 5.83-2.529 6.998-3.014 3.332-1.386 4.025-1.627 4.476-1.635z"/></svg>Telegram</a><a class="sb" href="#" target="_blank"><svg width="18" height="18" viewBox="0 0 24 24" fill="none"><path d="M12.4 12.486c-.003-1.607 1.867-2.492 3.108-1.47l5.882 4.844c1.236 1.019.726 2.993-.798 3.322l-.151.026-2.745.382a.5.5 0 00-.03.009l-.024.016-2.036 1.882-.116.1c-1.18.937-2.95.164-3.066-1.34l-.007-.152-.017-7.619zm1.857-1.094a.5.5 0 00-.047.037l-5.882 4.844a.5.5 0 00.266.884l2.745-.382a.5.5 0 01.53.53l-.382 2.745a.5.5 0 00.884.266l5.882-4.844a.5.5 0 00-.266-.884l-2.745.382a.5.5 0 01-.53-.53l.382-2.745a.5.5 0 00-.266-.884.5.5 0 00-.266.037z" fill="currentColor"/></svg>Website</a></div>

<div class="stg"><div class="sc"><div class="sv">$1.2M</div><div class="sl">Market cap</div></div><div class="sc"><div class="sv">2.4K</div><div class="sl">Holders</div></div><div class="sc"><div class="sv">1B</div><div class="sl">Supply total</div></div></div>

<div class="se"><div class="st"><svg width="18" height="18" viewBox="0 0 24 24" fill="none"><path d="M4 3.333a1 1 0 011 1v13.758h15.067a1 1 0 010 2H5a2 2 0 01-2-2V4.333a1 1 0 011-1z" fill="currentColor"/><path d="M18.263 6.517a1 1 0 011.411 1.414l-4.95 4.95a1 1 0 01-1.414 0l-2.121-2.121a1 1 0 00-1.415 0l-3.536 3.536a1 1 0 11-1.414-1.414l3.536-3.536a3 3 0 014.243 0l1.414 1.414 4.243-4.243z" fill="currentColor"/></svg>Tokenomics</div><div class="tb"><div class="tr"><span class="tl2">Liquidez</span><div class="tt"><div class="tf" style="width:80%;background:#3b82f6"></div></div><span class="tv">80%</span></div><div class="tr"><span class="tl2">Marketing</span><div class="tt"><div class="tf" style="width:10%;background:#ef4444"></div></div><span class="tv">10%</span></div><div class="tr"><span class="tl2">Desenvolvimento</span><div class="tt"><div class="tf" style="width:7%;background:#22c55e"></div></div><span class="tv">7%</span></div><div class="tr"><span class="tl2">Equipe</span><div class="tt"><div class="tf" style="width:3%;background:#a855f7"></div></div><span class="tv">3%</span></div></div></div>

<div class="se"><div class="st"><svg width="18" height="18" viewBox="0 0 24 24" fill="none"><path d="M10 5.188A8.003 8.003 0 004.9 12c0 4.418 3.582 8 8 8a8.003 8.003 0 007.812-6h1.86A9.96 9.96 0 0112 21.9c-5.467 0-9.9-4.433-9.9-9.9S6.533 2.1 12 2.1c.186 0 .37.005.552.015" fill="currentColor"/><path d="M17.657 8.343l-4.95 4.95a1 1 0 01-1.414 0l-2.121-2.121a1 1 0 00-1.415 0l-3.536 3.536a1 1 0 11-1.414-1.414l3.536-3.536a3 3 0 014.243 0l1.414 1.414 4.243-4.243a1 1 0 011.414 1.414z" fill="currentColor"/></svg>Roadmap</div><div class="rm"><div class="ri d"><div class="rd"></div><div class="rp">Fase 1 — Concluída</div><div class="rt">Lançamento no Pump.fun</div><div class="rde">Token criado e listado na curva de ligação. Liquidez inicial estabelecida.</div></div><div class="ri d"><div class="rd"></div><div class="rp">Fase 2 — Concluída</div><div class="rt">Listagem em DEX</div><div class="rde">Migrado para Raydium. Par de trading ativo com liquidez bloqueada.</div></div><div class="ri a"><div class="rd"></div><div class="rp">Fase 3 — Em andamento</div><div class="rt">Marketing & comunidade</div><div class="rde">Campanhas no Twitter/X, parcerias com influencers e crescimento orgânico.</div></div><div class="ri"><div class="rd"></div><div class="rp">Fase 4 — Futuro</div><div class="rt">Utilidade & expansão</div><div class="rde">Integrações DeFi, staking e possíveis listagens em CEXs.</div></div></div></div>

<div class="se"><div class="st"><svg width="18" height="18" viewBox="0 0 24 24" fill="none"><path d="M12.068 2.034a.9.9 0 01.9.9v8.166h8.097a.9.9 0 01.9.9.9.9 0 01-.9.9h-8.097v8.165a.9.9 0 01-.9.9.9.9 0 01-.9-.9V12.9H2.966a.9.9 0 01-.9-.9.9.9 0 01.9-.9h8.202V2.934a.9.9 0 01.9-.9z" fill="currentColor"/></svg>Como comprar</div><div class="sp"><div class="stp"><div class="sn">1</div><div class="sct"><div class="stt">Crie uma wallet Solana</div><div class="sd">Baixe Phantom, Solflare ou Backpack. Guarde sua seed phrase com segurança.</div></div></div><div class="stp"><div class="sn">2</div><div class="sct"><div class="stt">Deposite SOL</div><div class="sd">Transfira SOL da sua exchange (Binance, Coinbase, etc.) para o endereço da sua wallet.</div></div></div><div class="stp"><div class="sn">3</div><div class="sct"><div class="stt">Conecte no Jupiter</div><div class="sd">Acesse jup.ag, conecte sua wallet e cole o endereço do contrato do token.</div></div></div><div class="stp"><div class="sn">4</div><div class="sct"><div class="stt">Confirme a swap</div><div class="sd">Escolha o valor, revise a taxa de slippage e confirme a transação na sua wallet.</div></div></div></div></div>

<div class="se"><div class="st"><svg width="18" height="18" viewBox="0 0 24 24" fill="none"><path d="M12 2.1a9.9 9.9 0 110 19.8 9.9 9.9 0 010-19.8zm0 1.8a8.1 8.1 0 100 16.2 8.1 8.1 0 000-16.2zM12 16.5a.9.9 0 110 1.8.9.9 0 010-1.8zm0-11.7a.9.9 0 01.9.9v7.2a.9.9 0 01-1.8 0V5.7a.9.9 0 01.9-.9z" fill="currentColor"/></svg>FAQ</div><div class="fi"><div class="fq" onclick="this.parentElement.classList.toggle('o')">O que é esse token?<svg viewBox="0 0 24 24" fill="none"><path d="M11.386 21.639a.9.9 0 001.27 0l5.539-5.539a.9.9 0 10-1.272-1.272L12 19.753l-4.923-4.925a.9.9 0 00-1.272 1.272l5.539 5.539z" fill="currentColor"/></svg></div><div class="fa"><p>Um token meme criado na Solana via Pump.fun. Não tem utilidade intrínseca — seu valor vem da comunidade e da demanda do mercado.</p></div></div><div class="fi"><div class="fq" onclick="this.parentElement.classList.toggle('o')">O contrato é renunciado?<svg viewBox="0 0 24 24" fill="none"><path d="M11.386 21.639a.9.9 0 001.27 0l5.539-5.539a.9.9 0 10-1.272-1.272L12 19.753l-4.923-4.925a.9.9 0 00-1.272 1.272l5.539 5.539z" fill="currentColor"/></svg></div><div class="fa"><p>Verifique no Solscan se a autoridade de mint foi renunciada e se a liquidez está bloqueada. Sempre DYOR antes de investir.</p></div></div><div class="fi"><div class="fq" onclick="this.parentElement.classList.toggle('o')">Qual a taxa de slippage recomendada?<svg viewBox="0 0 24 24" fill="none"><path d="M11.386 21.639a.9.9 0 001.27 0l5.539-5.539a.9.9 0 10-1.272-1.272L12 19.753l-4.923-4.925a.9.9 0 00-1.272 1.272l5.539 5.539z" fill="currentColor"/></svg></div><div class="fa"><p>Para tokens com baixa liquidez, use 5-10% de slippage. No Jupiter, vá em Settings e ajuste conforme necessário.</p></div></div><div class="fi"><div class="fq" onclick="this.parentElement.classList.toggle('o')">Como acompanhar o preço?<svg viewBox="0 0 24 24" fill="none"><path d="M11.386 21.639a.9.9 0 001.27 0l5.539-5.539a.9.9 0 10-1.272-1.272L12 19.753l-4.923-4.925a.9.9 0 00-1.272 1.272l5.539 5.539z" fill="currentColor"/></svg></div><div class="fa"><p>Use DexScreener, Birdeye ou o próprio Jupiter. Cole o endereço do contrato para ver o gráfico em tempo real.</p></div></div></div>

<div class="wb"><svg width="18" height="18" viewBox="0 0 24 24" fill="none"><path d="M12 7a.9.9 0 00-.9.826v6.348a.9.9 0 001.8 0V7.826A.9.9 0 0012 7zM12.9 17.1a.9.9 0 11-1.8 0 .9.9 0 011.8 0z" fill="currentColor"/><path d="M12 2.1a9.9 9.9 0 100 19.8 9.9 9.9 0 000-19.8zm0 1.8a8.1 8.1 0 110 16.2 8.1 8.1 0 010-16.2z" fill="currentColor"/></svg><div class="wt">Tokens meme são altamente especulativos e arriscados. Não invista mais do que pode perder. Este não é um conselho financeiro. Sempre faça sua própria pesquisa (DYOR).</div></div>
</div>

<div class="toast" id="toast">Endereço copiado!</div>
</body>
</html>
