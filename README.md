### Bootstrap 5 Meteora

# 01/05 - Integrando Bootstrap ao projeto

no site no Bootstrap vamos copia o <link> no Incluir via CDN, e cole na <head>. depois vamos copia o <script> e coloca no fechamento da tag <Body> 


# 01/07 - Explorando a documentação do Bootstrap

no fragma o WIREFRAME é os esqueleto que recebomos no projeto, mostrando como vamos deixar os elementos na posição correta

site Bootstrap -> Document -> components -> navBar

NavBar é a parte de cima

para abrir no browser é só clicar em cima do arquivo com mouse esquerdo

no carousel vamos escoler o terceiro e clicar no raío e copiar toda a div
para colocar o carrosel para rodar vamos no (Autoplaying carousels) vamos copiar o data-bs-ride="carousel"
    <div id="carouselExampleCaptions" class="carousel slide" data-bs-ride="carousel">

# 02/02 - Inserindo mais componentes

vamos deixar o menu humburguer só para celulares, tablet vai ser normal, vamos resolver essse problema

bootstrap -> Docs -> Layouts -> Breakpoints

<nav class="navbar navbar-expand-md bg-body-tertiary"> vamos atualizar collcando md, que é o que mostrou na tabela no Available breakpoints
  

# 02/05 - Grid no Bootstrap

bootstrap -> Docs -> Layouts -> Grid

ele distribui a tela em 12 partes 

"Alt + Shift + F” para indentar o código

# 02/06 - Grid e Brealpoints

mx- : margem e x é da direita e esquerda.
g: é o gap "o espaço entre os elementos"

vamos unir as telas 
    <div class="col-6 col-md-4 col-xxl-2">

***
Exemplos sobre a grid 
Supondo que em um projeto, há uma div com 4 imagens no seu interior, sendo necessário organizar essas imagens da seguinte forma:
Para telas a partir de 768px de largura ficam 2 imagens por linha;
Para telas pequenas deve ficar 1 imagem por linha.
Utilizando das soluções do Bootstrap de Grid + Breakpoints, qual a opção permite chegar nesse resultado:
<div class="row">
  <img class="col-12 col-md-6" src="./assets/imagem-1" alt="Descrição imagem 1">
  <img class="col-12 col-md-6" src="./assets/imagem-2" alt="Descrição imagem 2">
  <img class="col-12 col-md-6" src="./assets/imagem-3" alt="Descrição imagem 3">
  <img class="col-12 col-md-6" src="./assets/imagem-4" alt="Descrição imagem 4">
</div>

 "pb-4" do Bootstrap representa o espaçamento inferior

# 03/02 - Bootstrap Icons

isso é uma atalho para criar 3 divs ( div*3>div*3 ).

vamos criar os Icones 

Bootstrap -> Icons -> Install -> CDN
copia o <Link> e cole no <Head>

agora podemos utilizar os Icones

# 03/04 - Ajustando fontes

vamos mudar o tamanho do icone, o mesmo que utilizamos para stylizar os textos vamos stylizar os icone
bootstrap -> Docs -> Utilities -> text -> Font size

 <div><i class="bi bi-arrow-repeat fs-1"></i></div>

# 03/05 -  sintaxe de espaçamento

Resumão de espaçamento no Bootstrap 5
O Bootstrap inclui uma ampla variedade de utilitários destinados ao espaçamento, que podem ser aplicados em todos os pontos de quebra (sm, md, lg, xl e xxl).

Para aplicar a classe de espaçamento é bem simples, basta seguir a regra do tipo + direção + valor. Mas calma, vamos olhar cada um em detalhes!

Tipo
O tipo do espaçamento indica se aquele valor que está sendo aplicado é referente ao margin ou ao padding, que são representados na classe pelas letras m e p, respectivamente.

Direção
Uma outra informação importante que compõe a classe é pra qual lado esse espaçamento será aplicado, temos algumas opções.

t - significa top ou topo e é aplicado superiormente
b - vem de bottom e é aplicado abaixo ou inferiormente
s - vem de start e se refere ao left ou lado esquerdo do elemento
e - vem de end e se refere ao right ou lado direito do elemento
x - do eixo x ou horizontal, é aplicado à esquerda e direita do elemento
y - do eixo y ou vertical, é aplicado acima e abaixo do elemento
blank - aplica em todos os 4 lados do elemento

Valor
Por último, só ficou faltando dizer qual o valor que será aplicado de espaçamento, o que varia de 0 até 5 e é utilizado o rem como unidade de medida padrão.

0 elimina o espaçamento já definido
1 ou 0.25rem
2 ou 0.5rem
3ou 1rem
4 ou 1.5rem
5 ou 3rem
auto calcula automaticamente um valor para a propriedade margin ou m.
Um ponto interessante, é que ocorre um cálculo em que a variável Sass $spacer é multiplicada ao valor em rem da classe. Por exemplo, o 1 corresponde ao valor $spacer * 0.25 e isso irá ocorrer para todos os outros. Com isso, é possível modificar o valor da variável para outro valor a ser multiplicado e caso não aconteça, irá seguir o valor padrão em rem.

Resultado final
Com esses três parâmetros a classe de espaçamento está pronta para ser utilizada, veja um exemplo abaixo.

Aplicação no HTML
<h1 class="ms-1">Olá Mundo!</h1>
No CSS por debaixo dos panos
.ms-1 {
  margin-left: ($spacer * .25) !important;
}

# 03/07 - Flexbox no Bootstrap

vamos definir uma largura para os icones 
bootstrap -> Docs -> utilities -> sizing no bootstrap ele tem valores fixo  25%, 50%, 75%, 100%, que não tem como alterar os valores do
vamos fazer isso no css

vamos criar uma <div> para inglobar todas as três divs para uzarmos flex boox
 <div class="d-flex">
 <div class="d-flex flex-column align-items-center gap-3">

 para colocar os icones ao lado e do texto vamos criar outra <div>
<div class="d-flex flex-column align-items-center gap-3">
<div class="divs-facilidades">
    <div><i class="bi bi-x-diamond fs-1"></i></div>
    <div> <!-- div criada-->
        <div class="ms-3 mb-1">PAGUE COM PIX</div>
        <div class="texto-menor">Ganhe 5% OFF em Pagementos via PIX.</div>
    </div>
</div>
 <div class="ms-3 mb-1">TROCA GRÁTIS</div>

 nas 3 div div class="divs-facilidades d-flex"> acrescentei ao d-flex e o icone ficou ao lado do texto

 agra vamos desgrudar o texto de baixo do icone
 <div class="texto-menor ms-3">Moda responsável, que respeita o meio ambiente.</div>
 add ms-3 para colocar uma margem ao lado esquerdo

 adicionamos uma padding bottom de valor 4 <section class="pb-4">

# 03/08 - Desafio: Flexbox e Breakpoints

vamos colocar os icones e os textos <divs facilidades> para ficar em row/linha 
 <div class="d-flex flex-column flex-lg-row align-items-center justify-content-center gap-3 px-3">
 <div class="divs-facilidades d-flex align-items-center">

# 03/06-  Para saber mais: classes do Flexbox no Bootstrap
Não é novidade que o uso de Flexbox é uma maneira poderosa de organizar o layout e dispor elementos na tela, inclusive temos até um curso sobre Flexbox aqui na Alura! E utilizá-lo em conjunto com o Bootstrap, é a união perfeita! Isso porque você irá gerenciar rapidamente o layout, por meio de um conjunto extremamente completo de utilitários.

Manual do Flex no Bootstrap 5
Flex Container
Use d-flex e d-inline-flex: para criar um container flexbox comum ou em linha e transformar os elementos filhos diretos em itens flexíveis.

Modificando a direção
O padrão de direção no flex é row ou linha, então ao utilizar o Bootstrap e aplicar a classe d-flex, por padrão a classe flex-row também é aplicada. Utilize flex-column para definir uma direção vertical.

Alinhamento dos itens e da caixa
Itens Flexíveis
Justificando no eixo principal (eixo x por padrão e eixo y no flex-column )
Use a classe justify-content- e em seguida aplique uma das direções que gostaria de alinhar, como por exemplo start, end, center, between, around ou evenly.

Alinhando no eixo cruzado (eixo y por padrão e eixo x no flex-column )
Use a classe align-items- e assim como anteriormente, aplique uma das direções que gostaria de alinhar, como start, end, center, baseline ou stretch. Essa propriedade alinha de uma vez só todos os itens.

Caso você queira alinhar apenas 1 item flexível, você pode aplicar a classe diretamente nesse elemento e ao invés de align-items- ficará align-self-

O container
Para alinhar a caixa do Flexbox em si, utilize a classe align-content-, somada a direção que gostaria de aplicar, ou seja, start, end, center, between, around ou stretch.

Capacidade de encolher e expandir
Para fazer com que um um item flexível tenha a capacidade de crescer para preencher o espaço disponível, utilize o utilitário flex-grow-, por exemplo, com flex-grow-1 o elemento usa todo o espaço disponível, enquanto permite que os outros itens flexíveis ocupem o espaço restante.

E quando há a necessidade de fazer com que um item flexível encolha para que outro item tenha espaço, utiliza-se a classe flex-shrink- e o valor.

Quebrando de linha
O padrão no flex é a ausência de quebra de linha, então ao utilizar o Bootstrap e aplicar a classe d-flex, por padrão a classe flex-nowrap também é aplicada. Caso queira que após os elementos filhos ocuparem a largura total do container, ocorra a quebra para linha de baixo, utilize o utilitário flex-wrap.

Ordenando itens
É possível alterar a ordem visual de itens flexíveis específicos com a propriedade order do CSS, no bootstrap o utilitário também leva o mesmo nome que a propriedade somado ao valor inteiro de 0 a 5, exemplo: order-3.

Uma observação importante é que para todos os utilitários citados acima, é possível adicionar uma abreviação de breakpoint para modificar a estilização de acordo com a *responsividade. Por exemplo: .align-self-lg-start.


# 04/03 - Conhecendo a documentação de estilos (Customize)

vamos colocar o icone na janela que fica na barra de pesquisa

uma atalho :  link:favicon e abertar enter cria a tag:  <link rel="shortcut icon" href="favicon.ico" type="image/x-icon">

<link rel="shortcut icon" href="./assets/favicon.png" type="image/x-icon">

vamos alterar a cor: bootstrap -> Docs -> Customize -> color
<nav class="navbar navbar-expand-md bg-black navbar-dark">

bg-black: colocou a background 
navbar-dark: clariou as palavras

vamos inserir um logo no navBar:
 <a class="navbar-brand" href="#">
    <h1 class="m-0"><img class="d-block" src="./assets/logo-meteora.png" alt="Logo da loja Meteora"/></h1>
</a>

agora vamos zera o valor da margem que veio com o ícone, insirindo esse display-block (class="d-block")
class="m-0 na tag h1
<input class="form-control me-2 rounded-0" type="search" placeholder="Digite o produto" aria-label="Search">
insirir rounded-0 para tirar o arredondamento

 <button class="btn btn-outline-light rounded-0" type="submit">Buscar</button>
 tiramos o redondamento e mudamos a cor de verde para branco com -light
 style.css
 .verde-limao{
    color: #DAFF01;
}
.botao-lilas{
    background-color: #9353FF;
}
e colocado assim: <a href="#" class="btn btn-primary botao-lilas rounded-0 border-0"> ver mais </a>
<div><i class="verde-limao bi bi-x-diamond fs-1"></i></div>


***
obs: <link rel="stylesheet" href="./style.css"> ele tem que se colocado abaixo do <link> Bootstrap, para funcionar as stylizações do arquivo style.css

# 04/06 - Imagens e Breakpoints

vamos adicionar uma imagem no carosel
<img class="img-fluid" src="./assets/Mobile/banner1-mobile.png" alt="Banner" />

e para ajustar a img vamos utiliza o img-fluid, 

<img class="img-fluid" src="./assets/Tablet/banner1-tablet.png" alt="Mulher vestindo blusa rosa, em fundo lilás." />

vamos utilizar breakpoint para esconder a img p/ tlabet, quando estiver em mobile tela menor, utilizando a classe none:

Bootstrap -> Doc -> Layouts -> Breakpoint
<img class="img-fluid d-none d-md-block d-xl-none" src="./assets/Tablet/banner1-tablet.png" alt="Mulher vestindo blusa rosa, em fundo lilás."/>
d-none (é uma display none)

d-md-block para aparecer quando a tela ficar maior

e vamos esconer para a tela de Moblie com a class=' d-md-none'

d-xl-none : para esconder quando a tela estiver maior ainda
d-xl-block: display, tamanho da tela Extra large xl, diplay block

as modificações dos slides do carosel ficou assim:
<div class="carousel-item position-relative">
        <img class="w-100 img-fluid d-md-none" src="./assets/Mobile/banner3-mobile.png" alt="Homem negro vestindo uma roupa cinza, no fundo laranja."/>
        <img class="w-100 img-fluid d-none d-md-block d-xl-none" src="./assets/Tablet/banner3-tablet.png" alt="Homem negro vestindo uma roupa cinza, no fundo laranja."/>
        <img class="w-100 img-fluid d-none d-xl-block" src="./assets/Desktop/banner3-desktop.png" alt="Homem negro vestindo uma roupa cinza, no fundo laranja."/>
        <div class="carousel-caption position-absolute posicao ">
            <h5 class="fs-1">COLEÇÃO ATEMPORAL</h5>
            <p>Alto impacto visual, baixo impacto ambiental.</p>
        </div>
    </div>
</div>
Por fim é necessário incluir no arquivo CSS um estilo para a classe posicao dentro de uma media query para alterar a posição dos textos em telas menores que 768px e fora do media query para telas de tablets e desktops. Ficaria assim:
.posicao{
    top: 40%;
}

@media(max-width: 767px){
    .posicao{
        top:60%;
    }
}
isso fara o texto ficar no meio 

# 05/02 - Finalizando imagens com Breakpoint

vamos dá os espaçamentos 
my : margem top e buttom
mx : left e right

para colocar o titulo centralizado no mobile colocar container na class
 <h2 class="container text-center my-3"> Produtos que estão bombando! </h2>

 para tirar o arendondamento : rounded-0 border-0

  <div class="col-6 col-md-4 col-xl-2 ">
            <div>
                <div class="card rounded-0 border-0">
                    <img class="d-md-none d-block" src="./assets/Mobile/categorias/categoria-camiseta.png"
                        alt="Camiseta verde de manga curta, com detalhe vermelho.">
                    <img class="d-none d-md-block d-xl-none" src="./assets/Tablet/categorias/categoria-camiseta.png"
                        alt="Camiseta verde de manga curta, com detalhe vermelho.">
                    <img class="d-none d-xl-block" src="./assets/Desktop/categorias/categoria-camiseta.png"
                        alt="Camiseta verde de manga curta, com detalhe vermelho.">
                    <div class="card-header bg-black text-bg-dark">
                        <p class="text-center navbar-dark">Camisetas</p>
                    </div>
                </div>
            </div>
        </div>

    d-md-none: vamos dá um display none quando a tela tiver 768px de whith "desaparecer"
    d-block para "Aparecer " quando a tela tiver menor
    d-none é para já ficar escondida
    d-md-block vai aparecer quando estiver 768 px telas de tablet
    d-xl-none esconde para telas maiores

# 05/03 - DEsafio inserindo imagem aos cards
<div class="col-12 col-md-6 col-xl-4 pb-4">
    <div class="card rounded-0">
        <img class="d-md-none d-block" src="./assets/Mobile/produtos/camiseta.png"
            alt="Homem branco vestindo uma camiseta amarela.">
        <img class="d-none d-xl-none d-md-block" src="./assets/Tablet/produtos/camiseta.png"
            alt="Homem branco vestindo uma camiseta amarela.">
        <img class="d-none d-xl-block" src="./assets/Desktop/produtos/camiseta.png"
            alt="Homem branco vestindo uma camiseta amarela.">

        <div class="card-body">
            <h5 class="card-title fw-bold">Camiseta conforto</h5>
            <p class="card-text">
                Multicores e tamanhos. Tecido de algodão 100%, fresquinho para o verão.
                Moldagem unissex.
            </p>
            <p class="fw-bold">R$70,00</p>
            <a href="#" class="btn btn-primary botao-lilas rounded-0 border-0"> ver mais </a>
        </div>
    </div>
</div>