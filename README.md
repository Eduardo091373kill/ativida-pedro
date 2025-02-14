# ativida-pedro
o codigo é bacamente codigo de HTML, CSS e javascript. com a função de trascrever nome e idade para o resultado
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Formulário</title>
    <link rel="stylesheet" href="style.css">
    <script src="script.js" defer></script>
</head>
<body>
    <div class="cabecalho">
        <h1>Meu Cabeçalho</h1>
    </div>
    <form id="meuForm">
        <label for="nome">Nome:</label>
        <input type="text" id="nome" required>
        
        <label for="dataNascimento">Data Nascimento:</label>
        <input type="date" id="dataNascimento" required>
        
        <button type="button" id="imprimir">Imprimir</button>
    </form>
    
    <div class="resultado">
        <h2>Resultado</h2>
        <p id="resultadoTexto"></p>
    </div>
    <footer>
        <h3></h3>
    </footer>
</body>
</html>
<!-- CSS -->
body {
    font-family: Arial, sans-serif;
}

.cabecalho {
    text-align: center;
}

form {
    margin: 30px;
    padding: 18px;
    border: 1px solid #0a0a0a;
    border-radius: 8px;
}

label {
    display: block;
    margin-top: 20px;
}

input {
    width: 100%;
    padding: 10px;
    margin-top: 8px;
    border: 2px solid #080808;
    border-radius: 10px;
}

button {
    margin-top: 20px;
    padding: 10px;
    background-color: #7428a7;
    color: rgb(255, 255, 255);
    border: none;
    border-radius: 5px;
    cursor: pointer;
}

button:hover {
    background-color: #053447;
}

.resultado {
    margin-top: 5px;
    border: 2px solid #020202;
    padding: 15px;
}

footer {
    text-align: center;
    margin-top: 20px;
}
javascript;
document.getElementById('imprimir').addEventListener('click', function() {
    const nome = document.getElementById('nome').value;
    const dataNascimento = document.getElementById('dataNascimento').value;
    document.getElementById('resultadoTexto').textContent = `Nome: ${nome}, Data de Nascimento: ${dataNascimento}`;
});

