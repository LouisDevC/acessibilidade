# acessibilidade
* ### Por que a acessibilidade é importante?  
>de acordo com o site [web.dev](https://web.dev/learn/accessibility/why?hl=pt-br), a acessibilidade é importante pois a dificuldade na inclusão pode se tornar um problema pra uma quantidade enorme de pessoas.  
A inclusão digital e acessibilidade da mesma afeta direta e indiretamente, o fator financeiro, quantidade de usuários, fatores legais, entre muitos outros fatores.
#### "Um mundo mais acessível para todos é a grande essência da tecnologia. Mostrar que as mais 1,3 bilhões de pessoas que se identificam como tendo uma deficiência podem, devem e terão, acesso à recursos digitais, sites, redes sociais, e muitos outros."

* ### Qual o impacto financeiro?
>A [ American Institutes for Research (AIR)](https://www.researchgate.net/profile/Dahlia-Shaewitz/publication/324603094_A_Hidden_Market_The_Purchasing_Power_of_Working-Age_Adults_With_Disabilities_A_Hidden_Market_The_Purchasing_Power_of_Working-Age_Adults_With_Disabilities/links/5ad89016458515c60f5918f3/A-Hidden-Market-The-Purchasing-Power-of-Working-Age-Adults-With-Disabilities-A-Hidden-Market-The-Purchasing-Power-of-Working-Age-Adults-With-Disabilities.pdf) diz
"a renda disponível total após a tributação para norte-americanos em idade ativa com deficiência é de cerca de US $490 bilhões por ano."  
As empresas que não se planejarem de maneira á criar produtos e serviços acessíveis, ficará para traz.

# Como a acessibilidade digital é medida?
>As leis políticas locais e ,etas de acessibilidade gerais normalmente são o que definem as diretrizes a serem seguidas.  
uma boa ideia é seguir o que está descrito na [WCAG 2 Overview](https://www.w3.org/WAI/standards-guidelines/wcag/).

- algumas praticas a seguir  
    - Realizar auditorias de acessibilidade no seu produto.
        >Uma auditoria de acessibilidade usa várias metodologias, técnicas e ferramentas, incluindo testes de design, automatizados, manuais e de **_tecnologia adaptativa (AT)_**.  

        >Execute essa auditoria várias vezes durante o ciclo de vida do produto de software para verificar se há alterações no nível de conformidade, em relação a um conjunto de pontos de verificação ou diretrizes de acessibilidade predeterminados.
    - POUR:   
    Perceptível:  
        >Esse princípio afirma que os usuários precisam perceber todas as informações essenciais na tela, e elas precisam ser transmitidas para vários sentidos.
        * #### há algum conteúdo ou função no seu produto digital que uma pessoa com uma deficiência específica não conseguiria perceber? Considere todos os diferentes tipos de deficiência: deficiências visuais, de mobilidade, audição, cognitivas e de fala, distúrbios vestibulares e convulsivos, entre outros.
        Operável:  
        >Para esse princípio, os usuários precisam conseguir operar a interface do produto digital. A interface não pode exigir interações que um usuário não possa realizar.
        * #### os usuários podem controlar os elementos interativos do seu produto digital? Há problemas de ordem de foco ou armadilhas de teclado? Como as interfaces touch são tratadas?  
        Compreensível:
        >Para esse princípio, os usuários precisam entender as informações e a operação da interface do usuário.
        * #### todo o conteúdo está escrito de forma clara?" Todas as interações são fáceis de entender? A ordem da página faz sentido para usuários com visão, usuários que usam apenas o teclado e usuários com leitores de tela?  
        Robusta:
        >Esse princípio se concentra no suporte a tecnologias adaptativas e garante que, à medida que os dispositivos e agentes do usuário evoluem, o produto digital permaneça acessível.
        * #### a quais tipos de tecnologia adaptativa você está apoiando? Seu produto digital só funciona nos navegadores ou sistemas operacionais mais recentes? Ele funciona em todos os pontos de interrupção e em diferentes orientações do dispositivo?
    ## estrutura do conteúdo:
    >A estrutura de uma pagina seja de um site ou um app, se depender apenas de estiliação, entrega um contexto crítico às pessoas que usam [AT's](#como-a-acessibilidade-digital-é-medida), como por exemplo leitores de tela.

    >Os elementos estruturais, são como um esboço do conteúdo na tela, mas também atuam como pontos de fixação para facilitar a navegação dentro do conteúdo.
    #### Os AT's leem as tags semânticas do html, dando assim mais significado ao conteúdo.
    * #### em algumas cituações adicionar atributos aria vai resolver alguns problemas mas no geral as mais de 100 tags do html costumam funcionar bem com os [AT's](#como-a-acessibilidade-digital-é-medida)
    ![Tags semanticas do html](./images/semantic%20html.png)
    #### o uso dos títulos de niveis diferentes e das listas ordenadas e não ordenadas também ajuda os AT's na hora de fazer identificação do item a ser lido, descrito ou mostrado.

# Aria & HTML:
### Ambos são usados para converter conteúdo em um formato alternativo, como Braille ou conversão de texto em voz (TTS).
#### introdução:
*  Accessible Rich Internet Applications (ARIA):
>São um conjunto de atributos que você pode adicionar ao html.  
esses atributos comuncam para as [AT's](#como-a-acessibilidade-digital-é-medida), função, estado, e propriedade por meio de API's.  
#### "ARIA modifica o código incorreto ou incompleto para criar uma experiência melhor para aqueles que usam TA, alterando, expondo e ampliando partes da acessibilidade árvore."
[(web.dev - 2022-09-30 UTC)](https://web.dev/learn/accessibility/aria-html?continue=https%3A%2F%2Fweb.dev%2Flearn%2Faccessibility&hl=pt-br#article-https://web.dev/learn/accessibility/aria-html&hl=pt-br)
>Em 2014, o W3C publicou oficialmente a recomendação HTML5. Com ele veio algumas grandes mudanças, incluindo a adição de elementos de ponto de referência, como main,header, footer, aside, nav e atributos como hidden e required. Com esses novos elementos e atributos HTML5, aliados maior suporte a navegadores, algumas partes de ARIA agora são menos críticas.

* #### ARIA é necessária quando um elemento HTML não tem compatibilidade com acessibilidade. Isso pode ser porque o design não permitir um elemento HTML específico ou o recurso/comportamento desejado não estiver disponíveis em HTML. No entanto, essas situações são raras.

## cuidado as arias tem que ser usadas ao maximo de forma correta.
# keyboard focus:
* >a ordem de foco é um aspecto importante da acessibilidade do teclado. Também é importante decidir como esse foco será estilizado. Porque, mesmo que a ordem de foco seja excelente, como um usuário saberia onde está na página sem o estilo adequado?  
O uso do tabindex indica a sequencia, o tabindex='0' segue o fluxo html da página dai pra frente é definido quem vem primeiro como tabindex = '1', ele segue exatamente desta maneira aqui:
```html
<div>
  <h1>Focus order</h1>
  <p tabindex="0">4th (primeiro do fluxo html)</p>
  <p tabindex="2">2nd</p>
  <p tabindex="1">1st</p>
  <p tabindex="-1">never</p>
  <p tabindex="3">3rd</p>
  <p tabindex="0">5th (segundo do fluxo html)</p>
</div>
```
<div>
  <h1>Focus order</h1>
  <p tabindex="0">4th</p>
  <p tabindex="2">2nd</p>
  <p tabindex="1">1st</p>
  <p tabindex="-1">never</p>
  <p tabindex="3">3rd</p>
  <p tabindex="0">5th</p>
</div>

# focus do css:
a:focus {  
  outline: auto 5px Highlight; /* para navegadores não-webkit */  
  outline: auto 5px -webkit-focus-ring-color; /* para navegadores webkit */  
}  
>Ao inves de usar outline none utilize o focus estilizado para definir o foco de um elemento.
#### (me pareceu uma ótima ideia pra fazer um texto por exemplo ser grifado enquanto é passado ou uma lista mesmo.)

# mais sobre Aria:
* role:

>Função: Define o papel do elemento na interface do usuário (UI), como button, navigation, dialog, etc.

Exemplo:

```html
<div role="navigation">...</div>
```
* aria-label:

>Função: Fornece um rótulo acessível para um elemento que pode não ter um rótulo visível.

Exemplo:

```html
<button aria-label="Fechar">X</button>
```
* aria-labelledby:

>Função: Associa o elemento a outro elemento que serve como seu rótulo.

Exemplo:

```html
<h2 id="titulo">Título</h2>
<div aria-labelledby="titulo">...</div>
```
* aria-describedby:

>Função: Associa o elemento a outro elemento que fornece uma descrição adicional.

Exemplo:

```html
<input type="text" aria-describedby="desc">
<p id="desc">Insira seu nome completo.</p>
```
* aria-hidden:

>Função: Indica se um elemento deve ser ignorado por tecnologias assistivas.

Exemplo:

```html
<div aria-hidden="true">...</div>
```
* aria-live:

>Função: Indica a relevância das mudanças dinâmicas no conteúdo para tecnologias assistivas.

Exemplo:

```html
<div aria-live="polite">...</div>
```
* aria-expanded:

>Função: Indica se um elemento, como um menu ou seção, está expandido ou colapsado.

Exemplo:

```html
<button aria-expanded="false">Menu</button>
```
* aria-checked:

>Função: Indica o estado de seleção de um elemento, como caixas de seleção ou botões de rádio.

Exemplo:

```html
<input type="checkbox" aria-checked="true">
```
* aria-required:

>Função: Indica que um campo de formulário é obrigatório.

Exemplo:

```html
<input type="text" aria-required="true">
```
* aria-invalid:

>Função: Indica que o valor de um campo de formulário não é válido.

Exemplo:

```html
<input type="text" aria-invalid="true">
```
**Exemplo de Uso:**
Aqui está um exemplo prático usando alguns desses atributos:

```html
<form>
  <label for="nome">Nome:</label>
  <input type="text" id="nome" aria-required="true" aria-describedby="nomeDesc">
  <p id="nomeDesc">Por favor, insira seu nome completo.</p>

  <button aria-label="Enviar formulário">Enviar</button>
</form>

Este formulário usa aria-required para indicar que o campo é obrigatório, aria-describedby para fornecer uma descrição adicional, e aria-label para fornecer um rótulo acessível para o botão.
```
# JavaScript acessível
* >__Se um elemento não semântico for usado para um evento acionador, um evento keydown/keyup precisa ser adicionado para detectar a tecla Enter ou Space pressionada. A adição de eventos de acionamento a elementos não semânticos é frequentemente esquecida. Infelizmente, quando isso acontece, o resultado é um componente que só pode ser acessado com um mouse. Os usuários que utilizam apenas o teclado ficam sem acesso às ações associadas.__
## sobre títulos:
* >Como aprendemos no módulo de documentos, o título da página é essencial para usuários de leitores de tela. Ele informa aos usuários em qual página eles estão e se eles navegaram para uma nova página.  

>Se você usa um framework JavaScript, é preciso considerar como processa os títulos de página. Isso é especialmente importante para apps de página única (SPAs, na sigla em inglês) que são carregados de um único arquivo index.html, já que as transições ou rotas (mudanças de página) não envolvem uma atualização da página. Sempre que um usuário carrega uma nova página em um SPA, o título não muda por padrão.

>Para SPAs, o valor document.title pode ser adicionado manualmente ou com um pacote auxiliar (dependendo do framework JavaScript). Anunciar os títulos de página atualizados para um usuário de leitor de tela pode exigir mais trabalho, mas a boa notícia é que você tem opções, como conteúdo dinâmico.

### com frequencia se é usado js na acessibilidade e fazemos isso inserindo html e css:

>Com grandes poderes, vêm grandes responsabilidades. Infelizmente, a injeção de JavaScript de HTML e CSS já foi usada indevidamente para criar conteúdo inacessível. Confira alguns usos indevidos comuns:

![uso correto da insersão de html ou css através do javascript](./images/html%20inject%20js.png)

>!__Para CSS, alterne as classes CSS em vez de adicionar estilos inline, já que isso permite reutilização e simplicidade. Use conteúdo oculto na página e alterne as classes para ocultar e mostrar conteúdo para HTML dinâmico. Se você precisar usar JavaScript para adicionar conteúdo à sua página dinamicamente, verifique se ele é simples, conciso e acessível__!

### Ao fazer a transição entre páginas (ou roteamento), a equipe de desenvolvimento precisa decidir para onde o foco vai quando a página é carregada.

*Há várias técnicas para fazer isso:*

* Coloque o foco no contêiner principal com um aviso aria-live.
* Coloque o foco novamente em um link para acessar o conteúdo principal.
* Mova o foco para o título de nível superior da nova página.

>No entanto, ao usar elementos svg inline, é preciso prestar atenção à acessibilidade.

>Primeiro, como os SVGs são codificados semanticamente, o AT os ignora por padrão. Se você tiver uma imagem decorativa, isso não será um problema. A AT vai ignorá-la conforme o esperado. No entanto, se você tiver uma imagem informativa, um ARIA role="img" precisa ser adicionado ao padrão para que a AA reconheça a imagem.

>Em segundo lugar, os elementos svg não usam o atributo alt. Portanto, métodos de codificação diferentes precisam ser usados para adicionar descrições alternativas às imagens informativas.

**Assim como as imagens informativas, as imagens funcionais precisam incluir uma descrição alternativa para informar todos os usuários sobre o propósito delas. Ao contrário de uma imagem informativa, cada imagem funcional precisa descrever a ação da imagem, não os aspectos visuais.**

# Cor e contraste:

>***Matiz:*** é uma maneira qualitativa de descrever uma cor, como vermelho, verde ou azul, em que cada matiz tem um ponto específico no espectro de cores, com valores que variam de 0 a 360, com vermelho em 0, verde em 120 e azul em 240.

[exemplo de matiz](./pages/exemplo.html)

>***saturação:*** é a intensidade de uma cor, medida em porcentagens que variam de 0% a 100%. Uma cor com saturação total (100%) seria muito vívida, enquanto uma cor sem saturação (0%) seria em escala de cinza ou preto e branco.

[exemplo de saturação](./pages/sat.html)

>***claridade:*** é o caractere claro ou escuro de uma cor, medido em porcentagens que variam de 0% (preto) a 100% (branco).

#### A claridade se refere a quantidade entre do preto ao branco em uma cor como azul por exemplo

[exemplo de claridade](./pages/clar.html)

>## Ferramentas como Adobe Color, Color Contrast Analyzer, Leonardo e o seletor de cores do Chrome DevTools podem informar rapidamente as proporções de contraste de cores e oferecer sugestões para ajudar a criar pares e paletas de cores mais inclusivos.

## consulta de midia com foco em cores:
>Além de verificar as taxas de contraste de cores e o uso de cores na tela, é recomendável aplicar as media queries cada vez mais populares e com suporte, que oferecem aos usuários mais controle sobre o que é exibido na tela.

>Por exemplo, usando a consulta de mídia ***@prefers-color-scheme***, é possível criar um tema escuro, que pode ser útil para pessoas com fotofobia ou sensibilidade à luz. Você também pode criar um tema de alto contraste com ***@prefers-contrast***, que oferece suporte a pessoas com deficiências de cor e sensibilidade ao contraste.

# Animação e movimento

>Aos 40 anos, mais de 35% dos adultos já terão experimentado algum tipo de disfunção vestibular. Isso pode levar a um período de tontura temporário, vertigem induzida por enxaqueca ou uma deficiência vestibular mais permanente.

>Além de causar vertigem, muitas pessoas acham que o conteúdo em movimento, piscando ou rolando uma tela é uma distração. Pessoas com TDAH e outros transtornos de déficit de atenção podem ficar tão distraídas pelos elementos animados que se esquecem de por que acessaram seu site ou app em primeiro lugar.

>Ao criar animação e movimento, verifique se o movimento do elemento é excessivo. Por exemplo, cores que piscam de escuro para claro ou movimentos rápidos na tela podem causar convulsões em pessoas com epilepsia fotossensível. Estima-se que 3% das pessoas com epilepsia sofrem de fotossensibilidade, que é mais comum em mulheres e pessoas mais jovens.

## As diretrizes de atualização das WCAG recomendam contra o seguinte:

> * Pisca mais de três vezes em um segundo
> * Pisca abaixo do limiar de [flash geral e flash vermelho.](./flash.md)

***Esses flashes podem, na melhor das hipóteses, causar uma incapacidade de usar uma página da Web ou, na pior das hipóteses, levar a uma doença.***

>Para qualquer movimento extremo, é fundamental testar usando a Ferramenta de análise fotosensível de epilepsia (PEAT, na sigla em inglês). A PEAT é uma ferramenta gratuita para identificar se o conteúdo, o vídeo ou as animações da tela podem causar convulsões. Nem todo conteúdo precisa ser avaliado pelo PEAT, mas o conteúdo que contém transições rápidas ou intermitentes entre cores de plano de fundo claras e escuras precisa ser avaliado, só por segurança.

> ***Outra pergunta que você deve fazer sobre animação e movimento é se o movimento do elemento é essencial para entender o conteúdo ou as ações na tela. Se não for essencial, considere remover todo o movimento, até mesmo micromovimentos, do elemento que você está criando ou projetando.***

### como manter as animações para a experiência do usuário?
>Suponha que você acredite que o movimento do elemento não é essencial, mas poderia melhorar a experiência geral do usuário, ou não é possível remover o movimento por outro motivo. Nesse caso, siga as diretrizes de movimento da WCAG. As diretrizes afirmam que você precisa criar uma opção para os usuários pausarem, pararem ou ocultarem o movimento para elementos não essenciais em movimento, piscando ou de rolagem que começam automaticamente, duram mais de cinco segundos e fazem parte de outros elementos da página.

#### @prefers-reduced-motion
>Assim como as consultas de mídia com foco em cores no módulo de cores, a consulta de mídia @prefers-reduced-motion verifica as configurações do SO do usuário relacionadas à animação.