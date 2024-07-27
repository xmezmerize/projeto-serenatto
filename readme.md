# Projeto Serenatto

# Link do WireFrame do projeto no Figma: https://www.figma.com/file/1jsN5KMprfMLOrYc8QrJZh/Serenatto-%7C-2985---Bootstrap-5--Curso-2?type=design&node-id=116-73325&t=BCoSSv0DsoMSdU1D-0

**html**
*data-bs-theme* data attribute utilizado para configurar ou modificar o tema de um componente específico, como um modal, um dropdown, ou outros elementos.(no caso theme, ele altera a cor do tema da página)

*fixed-top* Fixa o cabeçalho da página mesmo rolando a página pra baixo.

*container-fluid* é usada para criar um container que ocupa toda a largura disponível do viewport. Além desse existem outros dois containers. O *container*, usado para medidas fixas de páginas e o *container-md* usado para medidas com breakpoints.

*navbar-expand* define que a navbar será expandida (exibida em toda a largura) apenas em telas de tamanho igual ou superior a largura definida pelo breakpoint.

*efeito Parallax* O efeito parallax é uma técnica de design utilizada em websites para criar uma sensação de profundidade e movimento ao rolar a página.
CSS background-attachment: fixed; Este é o ponto chave para aplicar o efeito parallax usando CSS.
.banners {
    width: 100%;
    height: 100vh;
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
    background-attachment: fixed;
}
background-attachment: fixed; faz com que a imagem de fundo (ou o fundo de cor) do elemento .banners permaneça fixo em relação à janela do navegador, independentemente de rolar a página. Isso cria a ilusão de que o conteúdo da frente está se movendo sobre um plano de fundo estático, o que é essencial para o efeito parallax.

Outros atributos:
background-repeat: no-repeat;: Evita que a imagem de fundo seja repetida.
background-size: cover;: Garante que a imagem de fundo cubra todo o elemento .banners sem distorcer a proporção.
background-position: center;: Centraliza a imagem de fundo dentro do elemento .banners.

*modal* Os modais são componentes muito úteis no Bootstrap para exibir conteúdo em uma sobreposição que mantém o contexto da página.

Conteúdo dentro do main:
<div class="col-12 col-md-6 col-lg-4">
  <div class="card border-0 mx-auto btn" data-bs-toggle="modal" data-bs-target="#modal-1" style="width: 18rem;">
    <img src="./assets/produtos-cafe-tradicional.png" class="card-img-top" alt="Café preto.">
    <div class="card-body">
      <h3 class="card-text text-center fw-bold">Cafés Tradicionais</h3>
    </div>
  </div>
</div>
data-bs-toggle="modal" e data-bs-target="#modal-1" são atributos do Bootstrap que controlam o comportamento do modal. Quando o elemento .card é clicado, ele ativa o modal identificado por #modal-1.
A classe col-12 col-md-6 col-lg-4 é usada para definir a largura e o comportamento responsivo da coluna que contém o cartão.

Fora do main:
<div class="modal fade" id="modal-1" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
  <div class="modal-dialog">
    <div class="modal-content">
      <div class="modal-header">
        <h2 class="modal-title fs-5 fw-bold" id="exampleModalLabel">Cafés tradicionais</h2>
        <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
      </div>
      <div class="modal-body">
        <img src="./assets/produtos-cafe-tradicional.png" class="w-100" alt="Xícara de café preto">
        <p>O café Serenatto é conhecido por seus blends tradicionais e saborosos, que agradam aos amantes da bebida. Nossos grãos são cuidadosamente selecionados e torrados para produzir um aroma rico e sabor equilibrado.</p>
        <p>Entre os cafés mais tradicionais da casa, destaca-se o "Café Serenatto", um blend exclusivo de grãos com notas de chocolate e caramelo. Outra opção popular é o "Café Italiano", um café expresso encorpado e intenso. Já o "Café Cappuccino" é uma escolha clássica para quem prefere uma bebida cremosa e suave.</p>
      </div>
    </div>
  </div>
</div>
div class="modal fade" id="modal-1" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true" define o modal com a classe modal, indicando que é um modal do Bootstrap. O id="modal-1" é usado para vincular o modal ao botão que o abre.
div class="modal-dialog" é o contêiner do modal que controla o seu tamanho e alinhamento dentro da janela do navegador.
div class="modal-content" contém todo o conteúdo do modal, incluindo o cabeçalho, corpo e rodapé.
div class="modal-header" contém o cabeçalho do modal com o título e o botão de fechar (btn-close).
div class="modal-body" contém o corpo do modal com o conteúdo a ser exibido quando o modal é aberto, como a imagem e os parágrafos sobre os cafés tradicionais.

>Funcionamento geral:
Quando o usuário clica no cartão dentro do <main> (que tem data-bs-toggle="modal" e data-bs-target="#modal-1"), o modal identificado por #modal-1 é exibido. Ele cobre o conteúdo da página principal, mantendo o foco no modal até que seja fechado pelo usuário clicando no botão de fechar ou clicando fora do modal.

*formulário*

<section class="py-4 container">:

<section> é uma tag semântica para agrupar conteúdo relacionado, e py-4 adiciona padding vertical de 4 unidades (normalmente 1 unidade é 16 pixels) para espaçamento interno.
container é uma classe do Bootstrap que define um container fixo com largura máxima e centraliza o conteúdo na página.
<div class="row">, <div class="col-10 col-xl-8 mx-auto">:

<div class="row"> cria uma linha para conter colunas no sistema de grid do Bootstrap.
<div class="col-10 col-xl-8 mx-auto"> cria uma coluna que ocupa 10 colunas em telas pequenas (col-10) e 8 colunas em telas extra grandes (col-xl-8), com margem automática horizontal (mx-auto) para centralizar na página.
Formulário (<form id="contato">):

<form> é usado para encapsular elementos de entrada de dados.
id="contato" é um identificador único para o formulário, que pode ser usado em scripts para referenciar o formulário.
Campos de entrada (<div class="form-floating mb-3">, <input>, <label>):

form-floating é uma classe do Bootstrap que aplica um estilo especial para campos de entrada flutuantes, onde o <label> se move para cima quando o usuário começa a digitar no <input>.
mb-3 adiciona margem na parte inferior para separar os campos.
<input> define os campos de entrada, como texto (type="text"), email (type="email"), número (type="number"), etc.
<label> fornece uma descrição do campo de entrada.
Dropdown (<select class="form-select mb-3" aria-label="Default select example">, <option>):

form-select estiliza um dropdown (select) do Bootstrap.
mb-3 adiciona margem na parte inferior para separar do próximo elemento.
<option> define as opções dentro do dropdown, com uma opção inicial selecionada (selected).
Slider (<input type="range" class="form-range input-range" id="nivel-satisfacao">):

form-range estiliza um slider do Bootstrap para seleção de valores contínuos.
input-range pode ser uma classe personalizada para estilos adicionais.
<input type="range"> cria um controle deslizante para selecionar um valor dentro de um intervalo.
Checkbox (<input class="form-check-input" type="checkbox" value="" id="flexCheckDefault">, <label class="form-check-label" for="flexCheckDefault">):

form-check-input estiliza uma checkbox do Bootstrap.
<label class="form-check-label"> fornece a descrição ou texto associado à checkbox.
Botão (<button type="button" class="btn botao-padrao w-100 fw-bold mt-3 py-3">Enviar</button>):

btn é uma classe do Bootstrap para estilizar botões.
botao-padrao pode ser uma classe personalizada para estilos adicionais.
w-100 define a largura do botão como 100% da largura do elemento pai.
fw-bold aplica negrito ao texto do botão.
mt-3 adiciona margem superior para separar do elemento anterior.
py-3 adiciona padding vertical (py) de 3 unidades ao redor do botão.
**fim-html**

**css**
*variáveis-globais*
body {
  --bege: #E6E0D6;
  --marrom-escuro: #816D4F;
  --marrom-claro: #B29463;
  font-family: 'Barlow', sans-serif;
}
Variáveis CSS (--bege, --marrom-escuro, --marrom-claro): Define variáveis de cor para facilitar a reutilização e manutenção das cores ao longo do estilo. Por exemplo, --marrom-claro é usado para a cor de fundo dos checkboxes e botões.

font-family: Define a fonte padrão para todo o documento como 'Barlow' e fallback para sans-serif caso 'Barlow' não esteja disponível.

*estilização-checkbox*
input[type=checkbox] {
  border: 2px solid var(--marrom-claro);
  box-shadow: none;
}

input[type=checkbox]:checked,
input[type="checkbox"]:focus {
  background-color: var(--marrom-claro);
  border-color: var(--marrom-claro);
  box-shadow: none;
  outline: none;
}
>Define o estilo dos checkboxes:
border e border-color definem a largura e a cor da borda.
box-shadow remove a sombra padrão.
background-color e border-color são modificados quando o checkbox está checked (marcado) ou focus (focado), utilizando a cor --marrom-claro.

*estilo slider* 
O termo "slider" no contexto web geralmente se refere a um controle deslizante ou uma barra de rolagem horizontal que permite aos usuários selecionar um valor dentro de um intervalo específico.

.input-range::-webkit-slider-thumb {
  background-color: var(--marrom-claro);
}
>Define o estilo do polegar do slider (input[type="range"]) em navegadores WebKit (como Chrome e Safari):
background-color define a cor de fundo do polegar como --marrom-claro.

*Dark-theme*
[data-bs-theme="dark"] {
  color: white;
}

[data-bs-theme="dark"] .nav-link,
[data-bs-theme="dark"] .card-body,
[data-bs-theme="dark"] .offcanvas,
[data-bs-theme="dark"] .accordion,
[data-bs-theme="dark"] .btn {
  --bs-nav-link-color: white;
  --bs-card-color: white;
  --bs-offcanvas-color: white;
  --bs-body-color: white;
  --bs-body-color: white;
}
>Define um tema escuro para elementos que tenham o atributo data-bs-theme="dark".
color: white; define a cor do texto como branco para todos os elementos dentro deste tema escuro.
--bs-nav-link-color, --bs-card-color, --bs-offcanvas-color, --bs-body-color são variáveis do Bootstrap que são alteradas para branco (white) para garantir que os elementos específicos (links de navegação, corpos de cartão, offcanvas, acordeões, botões) tenham o texto e fundo adequados ao tema escuro.
**fim-css**

**javascript**
    1. Seleção de Elementos HTML:

*const inputCheck = document.querySelector('#modo-noturno');*
inputCheck é uma variável que armazena o elemento HTML encontrado usando document.querySelector().
#modo-noturno é o seletor CSS usado para selecionar o elemento cujo id é modo-noturno.
Este elemento provavelmente é um <input type="checkbox"> em seu HTML que os usuários podem clicar para ativar ou desativar o modo noturno.

*const elemento = document.querySelector('body');*
elemento é uma variável que armazena o elemento HTML <body>, que é o elemento raiz do seu documento HTML.
Estamos selecionando <body> para poder adicionar um atributo data-bs-theme que controla o tema do site (dark ou light).

    2. Adicionando um Evento de Escuta:

*inputCheck.addEventListener('click', () => { ... });*
addEventListener() é um método que escuta por eventos em elementos HTML específicos.
Neste caso, estamos escutando o evento de clique (click) no elemento inputCheck (o checkbox #modo-noturno).

    3. Alternando entre Modo Escuro e Modo Claro:

*const modo = inputCheck.checked ? 'dark' : 'light';*
inputCheck.checked é uma propriedade que indica se o checkbox está marcado (true) ou desmarcado (false).
modo é uma variável que armazena 'dark' se o checkbox estiver marcado (indicando que o usuário quer o modo noturno) ou 'light' se o checkbox estiver desmarcado.

    4. Atualizando o Atributo data-bs-theme do <body>:

*elemento.setAttribute("data-bs-theme", modo);*
setAttribute() é um método que define ou atualiza o valor de um atributo em um elemento HTML.
Estamos usando isso para definir o atributo data-bs-theme do <body> para o valor de modo determinado anteriormente ('dark' ou 'light').

>Funcionamento:
Quando o usuário clica no checkbox #modo-noturno, o evento de clique é acionado.
O script verifica se o checkbox está marcado ou não (inputCheck.checked).
Com base nisso, decide se deve aplicar o tema escuro ('dark') ou o tema claro ('light') ao site.
O atributo data-bs-theme no <body> é atualizado dinamicamente com o valor do modo selecionado.
Isso permite que o CSS e possivelmente o JavaScript do seu site ajustem automaticamente o estilo do conteúdo com base no modo selecionado.
**fim-javascript**