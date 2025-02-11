# Estudos-logica-js-projeto2
 Estudos - Lógica de Programação com JavaScript (Projeto 2)
 
 1- Primeira aula: Manipulação de textos.

**Objetivo:** Aprender a manipular textos no HTML utilizando JavaScript.

**Descrição:** Nesta aula, vamos aprender a modificar o conteúdo de elementos HTML usando JavaScript, ao invés de editar diretamente o código HTML. Como exemplo, vamos alterar o texto de um título (h1) e de um parágrafo (p) na página.

**Exemplo:** 
    Suponha que temos o seguinte código HTML, onde temos um título em um h1.

No JavaScript, vamos criar uma variável para selecionar o título e alterar seu conteúdo dinamicamente:

    let titulo = document.querySelector('h1');
    titulo.innerHTML = 'Jogo do Número Secreto';

**Explicação:**
**1- Selecionando o elemento:** 
    Usamos o document.querySelector('h1') para selecionar o primeiro h1 encontrado na página.

**2- Alterando o conteúdo:** 
    Com a propriedade innerHTML, alteramos o conteúdo do h1 para "Jogo do Número Secreto".
    Dessa forma, o título será alterado na página sem precisar modificar diretamente o HTML.

**Exemplo 2: Alterando o Parágrafo.**
    Agora, vamos supor que temos o seguinte código HTML com um parágrafo:

No JavaScript, vamos criar uma variável para selecionar o parágrafo e alternar o seu conteúdo:

    let paragrafo = document.querySelector('p');
    paragrafo.innerHTML = 'Escolha um número entre 1 a 100';

A explicação é a mesma do exemplo anterior, com o objetivo de modificar o conteúdo de um parágrafo, em vez de um título.

**Observações Finais:**

    querySelector é uma maneira eficiente de selecionar elementos no DOM, permitindo que você altere o conteúdo, adicione ou remova classes, e muito mais.
    A manipulação do conteúdo usando innerHTML altera o HTML do elemento selecionado. Contudo, em alguns casos, pode ser interessante usar outras propriedades como textContent para evitar problemas de segurança (como injeção de HTML indesejado).

2- Segunda aula: Criando uma função.

**Objetivo:** Aprender a criar uma função em JavaScript e vinculá-la a um evento de clique em um botão no HTML.

**Descrição:** Nesta aula, vamos aprender a criar uma função JavaScript que será chamada quando o botão "Chutar" for clicado. Para isso, no HTML, vamos usar a tag button e associar um evento onclick à função criada em JavaScript.

**Passos:**
1- No HTML: Criamos um botão com a tag button e adicionamos o atributo onclick para chamar a função quando o botão for clicado.   

**Exemplo de código HTML:** 

    <button onclick="verificarChute()">Chutar</button>

2- No JavaScript: Criamos a função verificarChute() que será chamada quando o botão for clicado. Dentro dessa função, podemos definir o que deve acontecer quando o evento ocorrer.

**Exemplo de código JavaScript:**

    function verificarChute() {
    console.log('O botão foi clicado!');
}

**Explicação:**  

    HTML: O atributo onclick="verificarChute()" vincula o evento de clique do botão à função verificarChute(). Ou seja, quando o botão for clicado, a função será executada.

2- JavaScript: 
            - A função verificarChute() é definida utilizando a palavra-chave function.

            - Dentro da função, o comando console.log('O botão foi clicado!') exibe uma mensagem no console sempque o botão é clicado.
            Dessa forma, ao clicar no botão, a função será executada e a mensagem será exibida no console.

**O que é uma função?** Uma função em JavaScript é um bloco de código que pode ser reutilizado em várias partes do seu programa. Ela pode ser chamada a partir de diferentes pontos no código para realizar uma tarefa específica.

**Sintaxe básica de uma função:** 
    function nomeDaFuncao() {
        // código a ser executado
    }
No caso do exemplo acima, verificarChute() é o nome da função, e dentro dela colocamos o código que será executado sempre que ela for chamada.

3- Terceira aula: Funções com parâmetros.

**Objetivo:** Evitar a repetição de código utilizando funções.

**Exemplo:** Vamos criar uma função chamada exibirTextoNaTela para simplificar a tarefa de alterar o conteúdo de diferentes elementos HTML.

    function exibirTextoNatela(){
    let campo = document.querySelector(tag, texto);
    campo.innerHTML = texto;
    }
**Como funciona:**

Com essa função, podemos passar a tag HTML e o texto como parâmetros, evitando a necessidade de criar várias variáveis e funções para cada tag que queremos alterar. Agora, podemos reutilizar a mesma função para exibir textos em diferentes partes da página.

**Exemplo de uso:**

    exibirTextoNaTela('h1', 'Jogo do Número Secreto');
    exibirTextoNaTela('p', 'Escolha um número entre 1 a 100');

Isso torna o código mais compacto, organizado e fácil de entender, já que não precisamos repetir a mesma lógica para cada novo elemento. O código fica mais limpo e fácil de manter.

4- Quarta aula: Funções com retorno.

**Objetivo:** Vamos criar uma função para gerar um número aleatorio para nosso jogo.

**Exemplo:** Primeiro, precisamos criar uma variável que vai armazenar o número aleatório gerado pela função. Vamos começar criando a variável numeroSecreto e atribuindo o valor retornado pela função gerarNumeroAleatorio:

    let numeroSecreto = gerarNumeroAleatorio();

Agora, vamos criar a função gerarNumeroAleatorio que retorna um número aleatório entre 1 e 100.
**O código da função será:**

    function gerarNumeroAleatorio() {
        return parseInt(Math.random() *100 +1);
    }

**Explicação:** 
    1- A função Math.random() gera um número aleatório entre 0 e 1.
    2- Multiplicamos esse número por 100 e somamos 1, assim obtemos um número aleatório entre 1 e 100.
    3- O parseInt é usado para garantir que o número gerado seja um inteiro.

O return dentro da função faz com que, quando chamarmos a variável numeroSecreto, ela nos retorne um valor aleatório dentro do intervalo desejado.

5- Quinta aula: Tipo booleano.

**Objetivo:** Comparar o número que o usuário chutou com o número secreto.

**Exemplo:** No nosso HTML, temos uma tag <input> para o usuário inserir um valor entre 1 e 100. Quando o usuário faz um chute, esse valor é capturado e comparado com o número secreto. No JavaScript, dentro da função verificarChute (que é onde está o botão para realizar o chute), criamos uma variável que recebe o valor inserido pelo usuário.

    let chute = document.querySelector('input').value;
    console.log(chute == numeroSecreto);

**Explicação:** 

    1- document.querySelector('input').value: Acessa o valor inserido pelo usuário no campo <input>.
    2- chute == numeroSecreto: Compara o valor do chute com o número secreto e retorna true (verdadeiro) se forem iguais, ou false (falso) se forem diferentes.

Esse código exibe no console se o chute do usuário é correto, ou seja, se o valor inserido é igual ao número secreto.