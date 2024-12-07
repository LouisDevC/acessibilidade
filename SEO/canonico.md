# Como especificar um URL canônico com rel="canonical" e outros métodos:
> Para especificar um URL canônico ***de páginas duplicadas ou muito semelhantes à Pesquisa Google***, você pode indicar sua preferência usando vários métodos.
- ***Redirecionamentos:*** é um forte indicador de que o destino do redirecionamento precisa ser canônico.
- ***Anotações rel="canonical"*** link: são um forte indicador de que o URL especificado precisa ser canônico.
- ***Inclusão de sitemaps:*** é um indicador fraco que ajuda os URLs incluídos em um sitemap a se tornarem canônicos.  

### _Embora seja recomendado usar esses métodos, nenhum deles é necessário. Seu site provavelmente vai funcionar bem sem especificar uma preferência canônica. Isso ocorre porque, se você não especificar um URL canônico, o Google vai identificar qual versão do URL é a melhor para mostrar aos usuários na Pesquisa._
## Motivos para especificar um URL canônico:  
> **Embora geralmente não seja essencial especificar uma preferência canônica para seus URLs, há vários motivos para informar ao Google explicitamente sobre uma página canônica em um conjunto de páginas duplicadas ou semelhantes:**
- Para especificar o URL que será visto pelas pessoas nos resultados da pesquisa.

- Para consolidar indicadores em páginas semelhantes ou duplicadas.

- Para simplificar as métricas de rastreamento de um conteúdo.

- Para poupar tempo de rastreamento em páginas duplicadas.

## Práticas recomendadas:  
 -Não use o arquivo robots.txt para fins de canonização.

- Não use a Ferramenta de remoção de URL para canonização, porque ela oculta todas as versões de um URL da Pesquisa.

- Não especifique URLs diferentes como versões canônicas da mesma página usando uma ou mais técnicas de canonização. Por exemplo, não especifique um URL no sitemap e indique outro URL para essa mesma página usando rel="canonical".

- Não especifique um fragmento de URL como canônico, já que o Google geralmente não oferece suporte a fragmentos de URL.

- Não recomendamos usar noindex para impedir a seleção de uma página canônica em um único site, porque isso vai bloquear completamente a página da Pesquisa

- Anotações rel="canonical" link são a solução preferida.

- Se você usar elementos hreflang, especifique uma página canônica no mesmo idioma ou no melhor substituto possível caso não haja uma página canônica no mesmo idioma.

- Ao criar links no seu site, use o URL canônico em vez de um URL duplicado. Vincular o site consistentemente ao URL que você considera canônico ajuda o Google a entender sua preferência.  
````html
<html>
<head>
<title>Explore the world of dresses</title>
<link rel="alternate" media="only screen and (max-width: 640px)"  href="https://m.example.com/dresses/green-dresses">
<link rel="canonical" href="https://example.com/dresses/green-dresses" />
<!-- other elements -->
</head>
<!-- rest of the HTML -->
````
# O que é canonização?  
> A canonização é o processo de selecionar o URL representativo (canônico) de um conteúdo. Consequentemente, um URL canônico é o URL de uma página que o Google escolheu como o mais representativo de um conjunto de páginas duplicadas. Muitas vezes chamado de eliminação de duplicação, esse processo ajuda o Google a mostrar apenas uma versão do conteúdo duplicado nos resultados da pesquisa.  
### Razões para duplicatas:
 - ***Variantes da região:*** por exemplo, uma parte do conteúdo para os EUA e o Reino Unido, que pode ser acessada em diferentes URLs, mas basicamente o mesmo conteúdo no mesmo idioma.

- ***Variantes do dispositivo:*** por exemplo, uma página com uma versão para dispositivos móveis e para computadores.

- ***Variantes de protocolo:*** por exemplo, as versões HTTP e HTTPS de um site

- ***Funções do site:*** por exemplo, os resultados da classificação e filtragem de funções de uma página de categoria

- ***Variantes acidentais:*** por exemplo, a versão de demonstração do site é aberta acidentalmente para rastreadores