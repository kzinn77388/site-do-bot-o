<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Você me ama? ❤️</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:Arial, Helvetica, sans-serif;
}

body{
    width:100vw;
    height:100vh;
    overflow:hidden;
    display:flex;
    justify-content:center;
    align-items:center;
    background:linear-gradient(135deg,#ff758c,#ff7eb3);
}

.container{
    text-align:center;
}

h1{
    color:#fff;
    font-size:42px;
    margin-bottom:50px;
    text-shadow:2px 2px 10px rgba(0,0,0,.3);
}

#sim,#nao{
    border:none;
    padding:15px 35px;
    font-size:22px;
    border-radius:10px;
    cursor:pointer;
    transition:.2s;
}

#sim{
    background:#28a745;
    color:#fff;
    margin-right:30px;
}

#sim:hover{
    transform:scale(1.08);
}

#nao{
    position:absolute;
    background:#dc3545;
    color:#fff;
    left:55%;
    top:55%;
}
</style>

</head>
<body>

<div class="container">
    <h1>Você me ama? ❤️</h1>

    <button id="sim">✅ Sim</button>
    <button id="nao">❌ Não</button>
</div>

<script>
const nao = document.getElementById("nao");
const sim = document.getElementById("sim");

function fugir(){

    const largura = window.innerWidth - nao.offsetWidth - 20;
    const altura = window.innerHeight - nao.offsetHeight - 20;

    const x = Math.floor(Math.random()*largura);
    const y = Math.floor(Math.random()*altura);

    nao.style.left = x + "px";
    nao.style.top = y + "px";
}

nao.addEventListener("mouseover", fugir);
nao.addEventListener("touchstart", fugir);

sim.addEventListener("click", function(){
    alert("❤️ Já sabia!\n\nMas eu te amo muito mais gatinha <3");
});
</script>

</body>
</html>
