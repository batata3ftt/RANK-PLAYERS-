
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>ETERNALS • Rank Players</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&family=Poppins:wght@500;600;700;800&display=swap" rel="stylesheet">
<style>
:root{
  --bg:#04070d;
  --line:rgba(255,255,255,0.08);
  --text:#ffffff;
  --muted:#9fb0cf;
  --blue:#1e4fff;
  --blue2:#0f2ea3;
  --gold:#ffd666;
  --gold2:#fff0b8;
  --shadow:0 20px 60px rgba(0,0,0,0.45);
}
*{margin:0;padding:0;box-sizing:border-box;}
body{
  font-family:Inter,sans-serif;color:var(--text);
  background:
    radial-gradient(circle at top left,rgba(30,79,255,0.20),transparent 25%),
    radial-gradient(circle at bottom right,rgba(255,214,102,0.07),transparent 20%),
    linear-gradient(180deg,#02040e 0%,#050a18 40%,#02040e 100%);
  overflow-x:hidden;
}
.bg{position:fixed;inset:0;overflow:hidden;pointer-events:none;z-index:-1;}
.blur1,.blur2{position:absolute;border-radius:999px;filter:blur(100px);opacity:.5;}
.blur1{width:340px;height:340px;background:rgba(30,79,255,0.28);top:-70px;left:-70px;}
.blur2{width:280px;height:280px;background:rgba(255,224,138,0.10);right:-80px;bottom:-80px;}
.container{width:min(1100px,calc(100% - 24px));margin:auto;padding:28px 0 40px;}
.hero{
  position:relative;padding:34px;border-radius:36px;
  background:linear-gradient(145deg,rgba(8,13,28,0.97),rgba(10,18,40,0.93));
  border:1px solid var(--line);overflow:hidden;box-shadow:var(--shadow);
}
.hero::before{
  content:"";position:absolute;inset:0;
  background:linear-gradient(135deg,rgba(30,79,255,0.13),transparent 30%,transparent 70%,rgba(255,224,138,0.04));
}
.top{display:flex;justify-content:space-between;align-items:center;gap:20px;flex-wrap:wrap;position:relative;z-index:1;}
.brand{display:flex;align-items:center;gap:18px;}
.logo{width:88px;height:88px;border-radius:24px;object-fit:cover;border:1px solid rgba(255,255,255,0.1);box-shadow:0 0 30px rgba(30,79,255,0.30);}
.badge{
  display:inline-flex;align-items:center;gap:8px;padding:8px 14px;border-radius:999px;
  background:rgba(255,214,102,0.14);border:1px solid rgba(255,214,102,0.30);
  font-size:13px;font-weight:700;color:var(--gold2);margin-bottom:12px;
}
h1,h2,h3,.btn{font-family:Poppins,sans-serif;}
h1{font-size:clamp(2rem,5vw,4rem);font-weight:800;letter-spacing:-0.05em;}
.description{margin-top:18px;max-width:800px;line-height:1.8;color:var(--muted);position:relative;z-index:1;}
.buttons{display:flex;gap:14px;flex-wrap:wrap;margin-top:24px;position:relative;z-index:1;}
.btn{text-decoration:none;padding:15px 20px;border-radius:18px;font-weight:700;transition:.25s ease;border:1px solid transparent;}
.btn-primary{background:linear-gradient(135deg,var(--blue),var(--blue2));color:white;box-shadow:0 12px 30px rgba(30,79,255,0.28);}
.btn-primary:hover{transform:translateY(-2px);}
.rank-section{
  margin-top:28px;padding:28px;border-radius:36px;
  background:rgba(7,11,20,0.92);border:1px solid var(--line);
  box-shadow:var(--shadow);position:relative;overflow:hidden;
}
.rank-section::before{
  content:"";position:absolute;inset:0;
  background:linear-gradient(135deg,rgba(30,79,255,0.08),transparent 30%,transparent 70%,rgba(255,224,138,0.04));
}
.section-top{
  display:flex;justify-content:space-between;align-items:center;
  flex-wrap:wrap;gap:12px;margin-bottom:24px;position:relative;z-index:1;
}
.section-top p{color:var(--muted);}
.rank-list{display:flex;flex-direction:column;gap:18px;position:relative;z-index:1;}
.rank-card{
  display:flex;align-items:center;gap:18px;padding:18px;border-radius:26px;
  background:linear-gradient(180deg,rgba(255,255,255,0.05),rgba(255,255,255,0.02));
  border:1px solid rgba(255,255,255,0.06);transition:.25s ease;
}
.rank-card:hover{transform:translateY(-4px);border-color:rgba(30,79,255,0.35);box-shadow:0 20px 40px rgba(0,0,0,0.35);}
.rank-number{
  min-width:80px;height:80px;display:flex;align-items:center;justify-content:center;
  border-radius:22px;font-size:1.8rem;font-weight:800;font-family:Poppins,sans-serif;
  background:linear-gradient(135deg,rgba(30,79,255,0.25),rgba(255,255,255,0.04));
  border:1px solid rgba(30,79,255,0.22);
}
.rank-card:nth-child(1) .rank-number{
  background:linear-gradient(135deg,rgba(255,214,102,0.38),rgba(255,255,255,0.05));
  border-color:rgba(255,214,102,0.40);color:#fff0b7;
}
.rank-card:nth-child(2) .rank-number{
  background:linear-gradient(135deg,rgba(200,200,200,0.25),rgba(255,255,255,0.05));
}
.rank-card:nth-child(3) .rank-number{
  background:linear-gradient(135deg,rgba(205,127,50,0.28),rgba(255,255,255,0.05));
}
.rank-info{flex:1;}
.rank-info h3{font-size:1.2rem;margin-bottom:8px;}
.rank-info p{color:var(--muted);line-height:1.6;}
.empty{opacity:.6;font-style:italic;}
.footer{margin-top:22px;text-align:center;color:var(--muted);}
@media(max-width:700px){
  .rank-card{flex-direction:column;align-items:flex-start;}
  .rank-number{width:100%;}
}
</style>
</head>
<body>
<div class="bg">
  <div class="blur1"></div>
  <div class="blur2"></div>
</div>
<main class="container">

  <section class="hero">
    <div class="top">
      <div class="brand">
        <img class="logo" src="https://i.imgur.com/2JUG8yz.png" alt="Logo Impact Zero">
        <div>
          <div class="badge">🏆 ETERNALS • RANK PLAYERS</div>
          <h1>Rank dos Jogadores</h1>
        </div>
      </div>
    </div>
    <p class="description">
      Aqui ficará o ranking oficial dos jogadores do ETERNALS. Conforme os jogos forem acontecendo, os melhores jogadores irão subir no ranking.
    </p>
    <div class="buttons">
      <a class="btn btn-primary" href="index.html">Voltar ao Time</a>
    </div>
  </section>

  <section class="rank-section">
    <div class="section-top">
      <h2>🏅 Ranking Atual</h2>
      <p>Top jogadores do time</p>
    </div>
    <div class="rank-list">

      <div class="rank-card">
        <div class="rank-number">#1</div>
        <div class="rank-info">
          <h3 class="empty">Sem jogador definido</h3>
          <p>O primeiro lugar ainda não foi escolhido.</p>
        </div>
      </div>

      <div class="rank-card">
        <div class="rank-number">#2</div>
        <div class="rank-info">
          <h3 class="empty">Sem jogador definido</h3>
          <p>O segundo lugar ainda não foi escolhido.</p>
        </div>
      </div>

      <div class="rank-card">
        <div class="rank-number">#3</div>
        <div class="rank-info">
          <h3 class="empty">Sem jogador definido</h3>
          <p>O terceiro lugar ainda não foi escolhido.</p>
        </div>
      </div>

      <div class="rank-card">
        <div class="rank-number">#4</div>
        <div class="rank-info">
          <h3 class="empty">Sem jogador definido</h3>
          <p>Posição livre para futuros jogadores.</p>
        </div>
      </div>

      <div class="rank-card">
        <div class="rank-number">#5</div>
        <div class="rank-info">
          <h3 class="empty">Sem jogador definido</h3>
          <p>Posição livre para futuros jogadores.</p>
        </div>
      </div>

    </div>
  </section>

  <div class="footer">✦ ETERNALS • Rank Oficial • Evolução • Vitória ✦</div>
</main>
</body>
</html>

```
