# Estudos-logica-js-projeto2
 Estudos - Lógica de Programação com JavaScript (Projeto 2)
 
 1. Primeira aula: Manipulação de textos.

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

2. Segunda aula: Criando uma função.

**Objetivo:** Aprender a criar uma função em JavaScript e vinculá-la a um evento de clique em um botão no HTML.

**Descrição:** Nesta aula, vamos aprender a criar uma função JavaScript que será chamada quando o botão "Chutar" for clicado. Para isso, no HTML, vamos usar a tag button e associar um evento onclick à função criada em JavaScript.

**Passos:**
1. No HTML: Criamos um botão com a tag button e adicionamos o atributo onclick para chamar a função quando o botão for clicado.   

**Exemplo de código HTML:** 

    <button onclick="verificarChute()">Chutar</button>

2. No JavaScript: Criamos a função verificarChute() que será chamada quando o botão for clicado. Dentro dessa função, podemos definir o que deve acontecer quando o evento ocorrer.

**Exemplo de código JavaScript:**

    function verificarChute() {
    console.log('O botão foi clicado!');
}

**Explicação:**  

    HTML: O atributo onclick="verificarChute()" vincula o evento de clique do botão à função verificarChute(). Ou seja, quando o botão for clicado, a função será executada.

2. JavaScript: 
            - A função verificarChute() é definida utilizando a palavra-chave function.

            - Dentro da função, o comando console.log('O botão foi clicado!') exibe uma mensagem no console sempque o botão é clicado.
            Dessa forma, ao clicar no botão, a função será executada e a mensagem será exibida no console.

**O que é uma função?** Uma função em JavaScript é um bloco de código que pode ser reutilizado em várias partes do seu programa. Ela pode ser chamada a partir de diferentes pontos no código para realizar uma tarefa específica.

**Sintaxe básica de uma função:** 
    function nomeDaFuncao() {
        // código a ser executado
    }
No caso do exemplo acima, verificarChute() é o nome da função, e dentro dela colocamos o código que será executado sempre que ela for chamada.

3. Terceira aula: Funções com parâmetros.

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

4. Quarta aula: Funções com retorno.

**Objetivo:** Vamos criar uma função para gerar um número aleatorio para nosso jogo.

**Exemplo:** Primeiro, precisamos criar uma variável que vai armazenar o número aleatório gerado pela função. Vamos começar criando a variável numeroSecreto e atribuindo o valor retornado pela função gerarNumeroAleatorio:

    let numeroSecreto = gerarNumeroAleatorio();

Agora, vamos criar a função gerarNumeroAleatorio que retorna um número aleatório entre 1 e 100.
**O código da função será:**

    function gerarNumeroAleatorio() {
        return parseInt(Math.random() *100 +1);
    }

**Explicação:** 
1. A função Math.random() gera um número aleatório entre 0 e 1.
2. Multiplicamos esse número por 100 e somamos 1, assim obtemos um número aleatório entre 1 e 100.
3. O parseInt é usado para garantir que o número gerado seja um inteiro.

O return dentro da função faz com que, quando chamarmos a variável numeroSecreto, ela nos retorne um valor aleatório dentro do intervalo desejado.

5. Quinta aula: Tipo booleano.

**Objetivo:** Comparar o número que o usuário chutou com o número secreto.

**Exemplo:** No nosso HTML, temos uma tag <input> para o usuário inserir um valor entre 1 e 100. Quando o usuário faz um chute, esse valor é capturado e comparado com o número secreto. No JavaScript, dentro da função verificarChute (que é onde está o botão para realizar o chute), criamos uma variável que recebe o valor inserido pelo usuário.

    let chute = document.querySelector('input').value;
    console.log(chute == numeroSecreto);

**Explicação:** 

1. document.querySelector('input').value: Acessa o valor inserido pelo usuário no campo <input>.
2. chute == numeroSecreto: Compara o valor do chute com o número secreto e retorna true (verdadeiro) se forem iguais, ou false (falso) se forem diferentes.

Esse código exibe no console se o chute do usuário é correto, ou seja, se o valor inserido é igual ao número secreto.

6. Sexta aula: Verificando o chute.
**Objetivo:** O objetivo dessa aula é permitir que a máquina verifique o chute do usuário e forneça uma resposta adequada, informando se o usuário acertou ou não o número secreto.

**Descrição:** A função verificarChute realiza a verificação do número fornecido pelo usuário. Se o usuário acertar o número secreto, uma mensagem de "Parabéns" será exibida. Caso contrário, o sistema informa se o número secreto é maior ou menor que o chute do usuário, ajudando-o a tentar novamente.

**Comportamento esperado:** Se o usuário acertar o número secreto:
Uma mensagem de sucesso é exibida:

"Acertou!"
"Parabéns, você descobriu o número secreto!"

Se o usuário errar o número secreto:
O sistema informa se o número secreto é:

Menor ou maior que o número escolhido pelo usuário.

**Exemplo:** se o usuario acertar o número secreto, irá aparecer a mensagem Acertou e embaixo, Parabéns você descobriu o número secreto.
se o usuario errar, ira aparecer a mensagem o numero secreto é menor ou maior dependendo da escolha do usuario.

    function verificarChute() {
        let chute = document.querySelector('input').value;

            // verifica se o chute está correto
            if (chute == numeroSecreto){
                exibirTextoNaTela('h1', 'Acertou!');
                exibirTextoNaTela('p', 'Parabéns você descobriu o número secreto!');
            } else {
                // caso o chute seja maior ou menor
                if (chute > numeroSecreto){
                exibirTextoNaTela('p', 'O número secreto é menor');
            } else {
                exibirTextoNaTela('p', 'O número secreto é maior');
            }
        }
    }

**Explicação do Código:**

1. Captura do Chute: A função começa capturando o valor inserido pelo usuário no campo de input.
2. Verificação de Acerto: Se o chute for igual ao número secreto, a mensagem de acerto é exibida.
3. Verificação de Erro: Caso contrário, o código verifica se o chute é maior ou menor que o número secreto e exibe a mensagem correspondente.

7. Sétima aula: Contando tentativas.
**Objetivo:** O objetivo dessa aula é contar quantas tentativas o usuário teve até descobrir o número secreto. Após o usuário acertar, será exibido o número total de tentativas feitas.

**Descrição:**

Nesta aula, adicionaremos uma variável para controlar o número de tentativas. A cada vez que o usuário errar o número secreto, a variável será incrementada. Quando o usuário acertar, o sistema mostrará quantas tentativas foram necessárias para chegar à resposta correta.

**Comportamento esperado:** 

1. Quando o usuário acertar o número secreto: O sistema exibirá uma mensagem parabenizando o usuário, incluindo o número total de tentativas feitas.
Exemplo de mensagem: "Parabéns, você descobriu o número secreto com X tentativas!"

2. Quando o usuário errar: O sistema informará se o número secreto é maior ou menor que o chute e continuará contando as tentativas.

**Exemplo de implementação:**

    function verificarChute() {
        let chute = document.querySelector('input').value;
        
        // Verifica se o chute está correto
        if (chute == numeroSecreto) {
            exibirTextoNaTela('h1', 'Acertou!');
            
            // Mensagem com a quantidade de tentativas
            let palavraTentativa = tentativas > 1 ? 'Tentativas' : 'tentativa';
            let mensagemTentativas = `Parabéns, você descobriu o número secreto com ${tentativas} ${palavraTentativa}!`;
            exibirTextoNaTela('p', mensagemTentativas);
        } else {
            // Caso o chute seja maior ou menor
            if (chute > numeroSecreto) {
                exibirTextoNaTela('p', 'O número secreto é menor');
            } else {
                exibirTextoNaTela('p', 'O número secreto é maior');
            }
            
            // Incrementa a contagem de tentativas
            tentativas = tentativas + 1;
        }
    }

8. Oitava aula: Implementação do Botão de reiniciar.

**Objetivo:** O objetivo desta funcionalidade é permitir que o número secreto seja reiniciado a cada tentativa de chute, seja no caso de erro ou quando o jogador acerta o número. Isso garantirá que, ao errar, o campo de entrada para o chute seja limpo automaticamente, e, ao acertar, o botão de "Novo Jogo" se torne habilitado para o usuário começar uma nova partida com um número aleatório.

**Como funciona:** 
1. Limpeza do Campo de Entrada: Toda vez que o jogador errar, o campo de entrada (input) será limpo, preparando-o para um novo chute.

2. Habilitação do Botão de "Novo Jogo": Quando o jogador acertar o número secreto, o botão de "Novo Jogo" será ativado, permitindo que o jogador comece uma nova partida.

**Passos para implementação:**

1. Crie uma função limparCampo() que limpa o valor no campo de entrada toda vez que o jogador errar o número:

    function limparCampo() {
        let chute = document.querySelector('input');
        chute.value = ''; // Limpa o valor do campo de entrada
    }


Atualização na Função verificarChute:
Em seguida, adicione a chamada para a função limparCampo() ao final da função verificarChute(), logo após incrementar o número de tentativas.

**Exemplo do incremento:**

    function verificarChute() {
        let chute = document.querySelector('input').value;
        
        if (chute == numeroSecreto) {
            exibirTextoNaTela('h1', 'Acertou!');
            let palavraTentativa = tentativas > 1 ? 'Tentativas' : 'tentativa';
            let mensagemTentativas = `Parabéns, você descobriu o número secreto com ${tentativas} ${palavraTentativa}!`;
            exibirTextoNaTela('p', mensagemTentativas);

            // Ativar o botão de "Novo Jogo"
            document.getElementById('reiniciar').removeAttribute('disabled');
        } else {
            if (chute > numeroSecreto) {
                exibirTextoNaTela('p', 'O número secreto é menor');
            } else {
                exibirTextoNaTela('p', 'O número secreto é maior');
            }

            tentativas += 1; // Incrementa o número de tentativas
            limparCampo(); // Limpa o campo de entrada
        }
    }


**Habilitar o Botão de "Novo Jogo":**

Logo após o jogador acertar o número, habilite o botão "Novo Jogo" removendo o atributo disabled:

**Exemplo de incremento:**

    document.getElementById('reiniciar').removeAttribute('disabled');

Essa linha de código garante que o botão de reinício ficará disponível para o usuário começar um novo jogo após acertar o número secreto.

**Resumo do Fluxo:**

1. O jogador faz um chute.
2. Se o chute estiver correto, ele verá uma mensagem de sucesso e o botão de "Novo Jogo" será ativado.
3. Se o chute estiver incorreto, o sistema irá informar se o número secreto é maior ou menor, incrementar as tentativas e limpar o campo de entrada para um novo chute.

Com essas modificações, o jogo fica mais dinâmico e interativo, permitindo uma experiência mais fluida para o jogador.

9. Nona aula: Reiniciando o jogo.

**Objetivo:** Fazer com que o botão "Novo Jogo" reinicie o jogo, sorteando um novo número secreto e permitindo que o jogo comece novamente.

**Como funciona:** 
1. No HTML, adicionaremos a função que será chamada quando o botão "Novo Jogo" for clicado.
2. Em seguida, criaremos a função reiniciarJogo() no JavaScript para gerar um novo número secreto, limpar o campo de entrada e reiniciar o contador de tentativas.
3. Também vamos garantir que o botão "Novo Jogo" só fique habilitado quando o jogador acertar o número secreto.

**Passos para Implementação:**
1. HTML: Adicionando o Evento onclick:

No HTML, criamos um botão com o atributo onclick para chamar a função reiniciarJogo() sempre que o jogador clicar no botão. Inicialmente, o botão estará desabilitado

    <button onclick="reiniciarJogo()" id="reiniciar" class="container__botao" disabled>Novo jogo</button>

2. JavaScript: Criando a Função reiniciarJogo():

Agora, no JavaScript, criaremos a função reiniciarJogo() que irá gerar um novo número secreto, limpar o campo de entrada e reiniciar o contador de tentativas.

    function reiniciarJogo() {
        numeroSecreto = gerarNumeroAleatorio(); // Gera um novo número secreto
        limparCampo(); // Limpa o campo de entrada
        tentativas = 1; // Reinicia o contador de tentativas
    }

3. Exibindo a Mensagem Inicial:

Para evitar que a mensagem inicial fique repetitiva, vamos criar uma função separada chamada exibirMensagemInicial(), que será responsável por exibir as mensagens de introdução do jogo.

    function exibirMensagemInicial() {
        exibirTextoNaTela('h1', 'Jogo do Número Secreto'); // Exibe o título
        exibirTextoNaTela('p', 'Escolha um número entre 1 e 100'); // Exibe a instrução inicial
    }

    // Chama a função para exibir a mensagem inicial
    exibirMensagemInicial();

4. Atualizando a Função reiniciarJogo():

Agora, vamos adicionar a função exibirMensagemInicial() dentro da função reiniciarJogo() para que as mensagens de introdução apareçam toda vez que o jogador começar um novo jogo.

    function reiniciarJogo() {
        numeroSecreto = gerarNumeroAleatorio(); // Gera um novo número secreto
        limparCampo(); // Limpa o campo de entrada
        tentativas = 1; // Reinicia o contador de tentativas
        exibirMensagemInicial(); // Exibe a mensagem inicial
    }

5. Desabilitando o Botão de "Novo Jogo" até o Acerto:

Por fim, vamos garantir que o botão de "Novo Jogo" permaneça desabilitado até que o jogador acerte o número secreto. Para isso, vamos desabilitar o botão de "Novo Jogo" sempre que ele for clicado para reiniciar o jogo.

No final da função reiniciarJogo(), adicionamos o seguinte código:

    document.getElementById('reiniciar').setAttribute('disabled', true); // Desabilita o botão de novo jogo

**Resumo do fluxo:**

1. O jogador clica no botão "Novo Jogo".
2. A função reiniciarJogo() é chamada, gerando um novo número secreto, limpando o campo de entrada e reiniciando o contador de tentativas.
3. A função exibirMensagemInicial() é chamada para exibir as mensagens de introdução.
4. O botão de "Novo Jogo" é desabilitado até que o jogador acerte o número secreto.