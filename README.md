# Estudos-logica-js-projeto2
 Estudos - Lógica de Programação com JavaScript (Projeto 2)
 
 1- Primeira aula: Manipulação de textos.
**Objetivo:** Aprender a manipular textos no HTML utilizando JavaScript.
**Descrição:** Nesta aula, vamos aprender a modificar o conteúdo de elementos HTML usando JavaScript, ao invés de editar diretamente o código HTML. Como exemplo, vamos alterar o texto de um título (h1) e de um parágrafo (p) na página.

**Exemplo:** Suponha que temos o seguinte código HTML, onde temos um título em um h1.
<h1>Titulo original</h1>
No JavaScript, vamos criar uma variável para selecionar o título e alterar seu conteúdo dinamicamente:

let titulo = document.querySelector('h1');
titulo.innerHTML = 'Jogo do Número Secreto';

**Explicação:**
**1- Selecionando o elemento:** Usamos o document.querySelector('h1') para selecionar o primeiro h1 encontrado na página.
**2- Alterando o conteúdo:** Com a propriedade innerHTML, alteramos o conteúdo do h1 para "Jogo do Número Secreto".
Dessa forma, o título será alterado na página sem precisar modificar diretamente o HTML.

**Exemplo 2: Alterando o Parágrafo.** Agora, vamos supor que temos o seguinte código HTML com um parágrafo:
<p>Aqui está o paragrafo</p>
No JavaScript, vamos criar uma variável para selecionar o parágrafo e alternar o seu conteúdo:

let paragrafo = document.querySelector('p');
paragrafo.innerHTML = 'Escolha um número entre 1 a 100';

A explicação é a mesma do exemplo anterior, com o objetivo de modificar o conteúdo de um parágrafo, em vez de um título.

**Observações Finais:**

querySelector é uma maneira eficiente de selecionar elementos no DOM, permitindo que você altere o conteúdo, adicione ou remova classes, e muito mais.
A manipulação do conteúdo usando innerHTML altera o HTML do elemento selecionado. Contudo, em alguns casos, pode ser interessante usar outras propriedades como textContent para evitar problemas de segurança (como injeção de HTML indesejado).

2- Segunda aula: Criando uma função.
**Objetivo:** Aprender a criar uma função em JavaScript e vinculá-la a um evento de clique em um botão no HTML.
**Descrição:** Nesta aula, vamos aprender a criar uma função JavaScript que será chamada quando o botão "Chutar" for clicado. Para isso, no HTML, vamos usar a tag <button> e associar um evento onclick à função criada em JavaScript.

**Passos:**
1- No HTML: Criamos um botão com a tag <button> e adicionamos o atributo onclick para chamar a função quando o botão for clicado.   

**Exemplo de código HTML:** <button onclick="verificarChute()">Chutar</button>

2- No JavaScript: Criamos a função verificarChute() que será chamada quando o botão for clicado. Dentro dessa função, podemos definir o que deve acontecer quando o evento ocorrer.

**Exemplo de código JavaScript:** function verificarChute() {
    console.log('O botão foi clicado!');
}

**Explicação:** 1- HTML: O atributo onclick="verificarChute()" vincula o evento de clique do botão à função verificarChute(). Ou seja, quando o botão for clicado, a função será executada.

2- JavaScript: 1- A função verificarChute() é definida utilizando a palavra-chave function.

            2- Dentro da função, o comando console.log('O botão foi clicado!') exibe uma mensagem no console sempre que o botão é clicado.
Dessa forma, ao clicar no botão, a função será executada e a mensagem será exibida no console.

**O que é uma função?** Uma função em JavaScript é um bloco de código que pode ser reutilizado em várias partes do seu programa. Ela pode ser chamada a partir de diferentes pontos no código para realizar uma tarefa específica.

**Sintaxe básica de uma função:** function nomeDaFuncao() {
    // código a ser executado
}
No caso do exemplo acima, verificarChute() é o nome da função, e dentro dela colocamos o código que será executado sempre que ela for chamada.