
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Em busca da cidade perdida</title>
<!-- Fonte Google -->
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link
href="https://fonts.googleapis.com/css2?family=Bai+Jamjuree:wght@400;600&display=swa
p" rel="stylesheet">
<!-- CSS embutido -->
<style>
body {
font-family: 'Bai Jamjuree', sans-serif;
background: linear-gradient(135deg, #f0ead6, #d4c295);
margin: 0;
padding: 0;
display: flex;
justify-content: center;
align-items: center;
min-height: 100vh;
}
main {
width: 90%;
max-width: 750px;
background: #fffdf5;
padding: 30px;
border-radius: 18px;
box-shadow: 0 8px 25px rgba(0, 0, 0, 0.2);
text-align: center;
border: 2px solid #b08968;
}
.passo {
display: none;
animation: fadeIn 0.6s ease-in-out;
}
.passo.ativo {
display: block;
}
p {

font-size: 1.2rem;
line-height: 1.6;
color: #3c2f2f;
margin: 15px 0 25px;
}
img {
max-width: 100%;
border-radius: 14px;
margin-bottom: 20px;
border: 3px solid #b08968;
}
button {
background: #8b5e34;
color: #fff;
border: none;
padding: 12px 22px;
margin: 8px;
border-radius: 10px;
font-size: 1rem;
cursor: pointer;
transition: transform 0.2s, background 0.3s;
font-weight: 600;
}
button:hover {
background: #6f4518;
transform: scale(1.05);
}
button:active {
transform: scale(0.95);
}
@keyframes fadeIn {
from { opacity: 0; transform: translateY(10px); }
to { opacity: 1; transform: translateY(0); }
}
</style>
</head>
<body>
<main>
<!-- Passo 0 -->
<div class="passo ativo" id="passo-0">
<img src="cenario-passo0.png" alt="Mapa antigo">

<p>Um dia desses, dentro de um livro da biblioteca da escola, eu descobri uma carta
antiga sobre uma cidade perdida, escondida por riquezas e belezas naturais. Nessa carta, a
autora deixa algumas pistas para encontrar essa cidade e eu decidi segui-las!</p>
<button class="btn-proximo" data-proximo="1">parana</button>
<button class="btn-proximo" data-proximo="2">Pernambuco</button>
</div>
<!-- Passo 1 -->
<div class="passo" id="passo-1">
<img src="cenario-rio.png" alt="Montanhas do parana">
<p>Você começa sua jornada no parana, subindo a ladeira do morunbi ao
amanhecer para encontrar a primeira pista.</p>
<button class="btn-proximo" data-proximo="3">Procurar a pista no topo do
pico</button>
<button class="btn-proximo" data-proximo="4">Desistir e voltar para casa</button>
</div>
<!-- Passo 2 -->
<div class="passo" id="passo-2">
<img src="cenario-pernambuco.png" alt="Praias de Pernambuco">
<p>Você decide começar sua aventura por Pernambuco. Nas praias de Recife, encontra
símbolos misteriosos desenhados na areia.</p>
<button class="btn-proximo" data-proximo="5">Seguir os símbolos</button>
<button class="btn-proximo" data-proximo="4">Ignorar e voltar para casa</button>
</div>
<!-- Passo 3 -->
<div class="passo" id="passo-3">
<p>No topo do pico, você encontra uma inscrição enigmática que aponta para a
Amazônia.</p>
<button class="btn-proximo" data-proximo="6">Viajar para a Amazônia</button>
</div>
<!-- Passo 4 (final ruim) -->
<div class="passo" id="passo-4">
<p>Você desiste da aventura e volta para casa. A cidade perdida continuará sendo
apenas uma lenda...</p>
</div>
<!-- Passo 5 -->
<div class="passo" id="passo-5">
<p>Os símbolos levam até uma caverna secreta, onde há um mapa antigo indicando a
floresta amazônica.</p>
<button class="btn-proximo" data-proximo="6">Partir para a Amazônia</button>
</div>
<!-- Passo 6 -->
<div class="passo" id="passo-6">

<img src="cenario-amazonia.png" alt="Floresta Amazônica">
<p>Na Amazônia, você encontra um rio que bifurca em duas direções.</p>
<button class="btn-proximo" data-proximo="7">Seguir pelo rio da esquerda</button>
<button class="btn-proximo" data-proximo="8">Seguir pelo rio da direita</button>
</div>
<!-- Passo 7 (final ruim) -->
<div class="passo" id="passo-7">
<p>O rio da esquerda leva a uma cachoeira perigosa! Você quase não sobrevive e
decide encerrar sua aventura.</p>
</div>
<!-- Passo 8 (final bom) -->
<div class="passo" id="passo-8">
<p>O rio da direita leva a uma clareira secreta, onde finalmente encontra a cidade
perdida, cheia de belezas naturais e tesouros escondidos!</p>
</div>
</main>
<!-- JavaScript embutido -->
<script>
const botoes = document.querySelectorAll(".btn-proximo");
botoes.forEach(botao => {
botao.addEventListener("click", () => {
const passoAtual = botao.closest(".passo");
const proximoId = botao.getAttribute("data-proximo");
const proximoPasso = document.getElementById("passo-" + proximoId);
passoAtual.classList.remove("ativo");
proximoPasso.classList.add("ativo");
});
});
</script>
</body>
</html>