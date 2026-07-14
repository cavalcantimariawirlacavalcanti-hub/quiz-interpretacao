<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Quiz de Compreensão e Interpretação de Texto</title>
<style>
body{
font-family:Arial,sans-serif;
background:#f2f2f2;
padding:20px;
max-width:700px;
margin:auto;
}
h1{text-align:center;}
.pergunta{
background:#fff;
padding:15px;
margin:15px 0;
border-radius:10px;
}
button{
padding:10px 20px;
font-size:18px;
display:block;
margin:20px auto;
}
#resultado{
font-size:22px;
text-align:center;
font-weight:bold;
}
</style>
</head>
<body>

<h1>Quiz de Compreensão e Interpretação</h1>

<p><strong>Texto:</strong> João acordou cedo para estudar. Mesmo cansado, revisou matemática e português antes da prova. No fim do dia, ficou feliz com seu desempenho.</p>

<form id="quiz">

<div class="pergunta">
1. João acordou cedo para:
<br><input type="radio" name="q1" value="c"> Passear
<br><input type="radio" name="q1" value="b"> Estudar
</div>

<div class="pergunta">
2. Ele revisou:
<br><input type="radio" name="q2" value="b"> Matemática e Português
<br><input type="radio" name="q2" value="c"> Ciências e História
</div>

<div class="pergunta">
3. João estava:
<br><input type="radio" name="q3" value="b"> Cansado
<br><input type="radio" name="q3" value="c"> Doente
</div>

<div class="pergunta">
4. Como terminou o dia?
<br><input type="radio" name="q4" value="b"> Feliz
<br><input type="radio" name="q4" value="c"> Triste
</div>

<div class="pergunta">
5. O texto mostra que estudar pode trazer:
<br><input type="radio" name="q5" value="b"> Bons resultados
<br><input type="radio" name="q5" value="c"> Problemas
</div>

<button type="button" onclick="corrigir()">Ver Resultado</button>

</form>

<p id="resultado"></p>

<script>
function corrigir(){
let pontos=0;
if(document.querySelector('input[name="q1"]:checked')?.value=="b")pontos++;
if(document.querySelector('input[name="q2"]:checked')?.value=="b")pontos++;
if(document.querySelector('input[name="q3"]:checked')?.value=="b")pontos++;
if(document.querySelector('input[name="q4"]:checked')?.value=="b")pontos++;
if(document.querySelector('input[name="q5"]:checked')?.value=="b")pontos++;
document.getElementById("resultado").innerHTML="Você acertou "+pontos+" de 5 questões!";
}
</script>

</body>
</html>
