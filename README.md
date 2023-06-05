### Plugins e atalhos do VSCODE

#### Baixe o vscode para seu Sistema operacional:
* [Visual Studio Code](https://code.visualstudio.com/download) - IDE Editor de códigos

#### Abra o terminal linux com o comando:
```
CTRL + ALT + T
```
Após isso digite:
* sudo apt update
* sudo apt upgrade

#### Instalando no `Debian` e `Ubuntu` family:
```
sudo dpkg -i code*.deb
```

#### Instalando no `RHEL` e `Cent OS`:
```
sudo rpm -ivh code*.rpm
```
-------------------------------
#### Instalando o vscode via repositório

#### Baixe a chave gpg do repositório:
```
curl https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > vscode-microsoft.gpg
```

#### Instale a chave gpg:
```
sudo install -D -o root -g root -m 644 vscode-microsoft.gpg /etc/apt/trusted.gpg.d/
```

#### Adicione o repositório do vscode:
```
sudo sh -c 'echo "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main" > /etc/apt/sources.list.d/vscode.list'
```

#### Agora digite os comandos abaixo:
* sudo apt install apt-transport-https
* sudo apt update
* sudo apt install code

ou

* sudo apt install code-insiders

-------------------------------
#### Instalando o navegador google-chrome

#### Baixe a chave pública que será adicionada ao SO:
```
wget -q -O - https://dl.google.com/linux/linux_signing_key.pub | sudo apt-key add -
```

#### Adicione o repositório do navegador:
```
sudo sh -c 'echo "deb [arch=amd64] http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google-chrome.list'
```

#### Agora digite os comandos abaixo:

* sudo apt update
* sudo apt install google-chrome-stable

-------------------------------
#### Sem nenhum plugin html5 instalado usaremos os recursos `Emmet Abbreviation` então basta digitar em sua página `index.html`:
```
html
```

#### Então aparecerá:
```
html:5
html:xml
```

#### Ao escolher `html:5` ele criará a estrutura básica do html5.

#### Também podemos digitar:
```
! -> Cria a estrutura básica do html5
!! -> cria o cabeçalho do documento HTML5
!!! -> cria o cabeçalho do documento HTML5
```
-------------------------------
#### Criando a pasta e o arquivo `css/style.css`

#### No cabeçalho do arquivo html dentro da tag `head` digite a linha abaixo: 
```
<link rel="stylesheet" href="css/style.css">
```
##### Depois pressione as teclas  `CTRL+CLICK` no link `css/style.css` criando a pasta e o arquivo no projeto se não existir.

-------------------------------
#### Criando um button com `id="idButton"`
```
button#idButton + ENTER 

<button id="idButton"></button>
```

#### Criando um button do `type="submit"` com `id="idCadastrar"`
```
button:submit#idCadastrar + ENTER

<button type="submit" id="idCadastrar"></button>
```

#### Criando um button com as classes `btn`, `btn-success` do bootstrap4 e com `id="idLogar"`
```
button.btn.btn-success#idLogar + ENTER

<button class="btn btn-success" id="idLogar"></button>
```
-------------------------------
#### Criando a tag `body` com uma `div` contendo o `id="container"`:
```
body>div#container + ENTER

<body>
  <div id="container"></div>
</body>
```
-------------------------------
#### Criando `5 div's`:
```
div*5 + ENTER

<div></div>
<div></div>
<div></div>
<div></div>
<div></div>
```
Note o `*5` ele é quem multiplica as `div's` 5 vezes.

#### Agora iremos usar seleção multilinha para adicionarmos a classe `className` nas `div's`, pressione:
SHIFT + ALT + SETA (&#8657;) ou (&#8659;) até selecionar todas as `div's`, depois pressione a tecla `BARRA_ESPAÇO` e digite `class="className"` será colocada em todas as `div's` simultâneamente.

```
<div class="className"></div>
<div class="className"></div>
<div class="className"></div>
<div class="className"></div>
<div class="className"></div>
```
-------------------------------
#### Criando `5 div's` com a mesma classe:
```
 div.className*5 + ENTER
 ou
 div*5.className + ENTER

 <div class="className"></div>
 <div class="className"></div>
 <div class="className"></div>
 <div class="className"></div>
 <div class="className"></div>
```
#### Note o asterisco `*5` após a `div` e no final de `div.className` ele multiplíca as `div's` com a mesma classe 5 vezes.

-------------------------------
#### Criando `5 li's` na `ul` "Lista não ordenada" todas com a mesma classe:
```
ul>li.className*5 + ENTER
ou
ul>li*5.className + ENTER

<ul>
   <li class="className"></li>
   <li class="className"></li>
   <li class="className"></li>
   <li class="className"></li>
   <li class="className"></li>
</ul>
```
#### Note o asterisco `*5` após a `ul>li` e no final de `ul>li.className` ele multiplíca as `li's` com a mesma classe 5 vezes.

-------------------------------
#### Criando `5 li's` na `ul` "Lista não ordenada" com `id's` enumerados de 1 a 5:

##### Note o cifrão `$` antes de `*5` após o `ul>li#idFotos` ele é quem enumera todos os `id's` de 1 à 5 nas `li's` que estão sendo multiplicadas 5 vezes.
```
ul>li#idFotos$*5 + ENTER
ou
ul>li*5#idFotos$ + ENTER
```

#### Após executar algums dos dois `Emmet Abbreviation` acima para a `ul` teremos a estrutura básica abaixo:
```
<ul>
   <li id="idFotos1"></li>
   <li id="idFotos2"></li>
   <li id="idFotos3"></li>
   <li id="idFotos4"></li>
   <li id="idFotos5"></li>
</ul>
```
-------------------------------
#### Criando `5 li's` na `ul` todos com a classe `nav-item` e colocando `link's` nas `li's` com a classe `nav-link` do bootstrap4:
```
ul>li*5.nav-item>a.nav-link*1 + ENTER
ou
ul>li.nav-item*5>a.nav-link*1 + ENTER
```
Note que após o `li.nav-item*5` utilizamos `>a.nav-link*1` por que?

#### Por que será apenas um link em cada `li` se utilizarmos `>a.nav-link*5` ele criará `5 link's` em cada `li`.

##### Após executar algums dos dois `Emmet Abbreviation` acima para a `ul` teremos a estrutura básica abaixo:
```
<ul>
   <li class="nav-item">
   <a href="" class="nav-link"></a>
   </li>

   <li class="nav-item">
   <a href="" class="nav-link"></a>
   </li>
   
   <li class="nav-item">
   <a href="" class="nav-link"></a>
   </li>
   
   <li class="nav-item">
   <a href="" class="nav-link"></a>
   </li>
   
   <li class="nav-item">
   <a href="" class="nav-link"></a>
   </li>
</ul>
```
-------------------------------
#### Criando dentro da tag `header` a tag `nav` com as classes do bootstrap4:
```
header>nav.navbar.navbar-expand-md.navbar-dark.bg-dark + ENTER

<header>
<nav class="navbar navbar-expand-md navbar-dark bg-dark"></nav>
</header>
```
-------------------------------
#### Criando dentro da tag `header` e `nav` uma `ul` com as classes `navbar-nav` e `ml-auto` do bootstrap4 e `5 li's` com a classe `className`:
```
ul.navbar-nav.ml-auto>li*5.className + ENTER
ou
ul.navbar-nav.ml-auto>li.className*5 + ENTER
```

##### Após executar algums dos dois `Emmet Abbreviation` acima para a `ul` teremos a estrutura básica abaixo:
```
<header>
   
   <nav class="navbar navbar-expand-md navbar-dark bg-dark">

    <ul class="navbar-nav ml-auto">
     
     <li class="className"></li>
     <li class="className"></li>
     <li class="className"></li>
     <li class="className"></li>
     <li class="className"></li>

    </ul>

  </nav>

</header>
```
-------------------------------
#### Criando dentro da tag `header` e `nav` uma `ul` com as classes `navbar-nav` e `ml-auto` do bootstrap4 e `5 li's` com classes iguais e `idLista` enumerados de 1 a 5:
``` 
ul.navbar-nav.ml-auto>li.className#idLista$*5 + ENTER
ou
ul.navbar-nav.ml-auto>li.className*5#idLista$ + ENTER
```

##### Após executar algums dos dois `Emmet Abbreviation` acima para a `ul` teremos a estrutura básica abaixo:
```
<header>
  
  <nav class="navbar navbar-expand-md navbar-dark bg-dark">
    
    <ul class="navbar-nav ml-auto">
      
      <li class="className" id="idLista1"></li>
      <li class="className" id="idLista2"></li>
      <li class="className" id="idLista3"></li>
      <li class="className" id="idLista4"></li>
      <li class="className" id="idLista5"></li>

    </ul>
  
  </nav>

</header>
```
-------------------------------

#### Criando dentro da tag `header` e `nav` uma `ul` com as classes `navbar-nav` e `ml-auto` do bootstrap4 contendo `5 li's` com a classe `nav-item` e id `idLista` enumerados de 1 a 5, juntamente com a classe `nav-link` nos `link's`:
```
ul.navbar-nav.ml-auto>li.nav-item#idLista$*5>a.nav-link*1 + ENTER
ou
ul.navbar-nav.ml-auto>li.nav-item*5#idLista$>a.nav-link*1 + ENTER
```

#### Após executar algums dos dois `Emmet Abbreviation` acima para a `ul` teremos a estrutura básica abaixo:
```
<header>
  
  <nav class="navbar navbar-expand-md navbar-dark bg-dark">
    
    <ul class="navbar-nav ml-auto">

      <li class="nav-item" id="idLista1">
      <a href="" class="nav-link"></a>
      </li>
      
      <li class="nav-item" id="idLista2">
      <a href="" class="nav-link"></a>
      </li>
      
      <li class="nav-item" id="idLista3">
      <a href="" class="nav-link"></a>
      </li>
      
      <li class="nav-item" id="idLista4">
      <a href="" class="nav-link"></a>
      </li>
      
      <li class="nav-item" id="idLista5">
      <a href="" class="nav-link"></a>
      </li>
    </ul>
  
  </nav>

</header>
```
-------------------------------
#### Movendo uma linha de código, clique na linha e pressione:

ALT + SETA para (&#8657;) ou (&#8659;) para mover a linha de código.

#### Selecão multilinhas, clique na linha e pressione:

SHIFT + ALT + SETA para (&#8657;) ou (&#8659;)
```
Até selecionar todas as linhas iguais que deseja alterar simultâneamente, 
ainda com as teclas SHIFT + ALT pressionadas pressione a tecla, 
SETA (<= Esquerda) ou (Direita =>) para selecionar a ocorrência que deseja substituir.
```
-------------------------------
#### Renomeando várias ocorrências:

#### Clique na ocorrência e pressione `CTRL+D` e a cada toque em `D` ele seleciona as outras `ocorrências` iguais depois é só renomear.

#### ou

#### Clique na ocorrência que você quer alterar e pressione `CTRL+F2`, este comando selecionará todas as ocorrências iguais simultâneamente, digite uma nova classe ou nome da tag, assim todas as linhas com a mesma ocorrência serão alteradas para a nova ocorrência digitada.

-------------------------------
### Melhorando a visibilidade do código.

#### No VSCODE no arquivo do código para aumentar o zoon pressione:
```
CTRL + 
```

#### Para diminuir o zoon pressione:
```
CTRL -
```

#### Se preferir edite o arquivo `settings.json`:

##### Abra a Paleta de Comandos `CTRL+SHIFT+P` execute:
```
Preferences: Open User Settings(JSON)
```

#### Adicione as linhas abaixo dentro das chaves `{}` acima das configurações existentes:
```
"editor.fontSize": 16, // Aumenta o tamanho da fonte no editor, default é 14.
"editor.fontWeight": "bold", // Deixa a letra em formato bold, default é normal.
"editor.lineHeight": 30, // Altura da linha dos códigos no editor, default é 20.

//////////////////////
```
---------------------------------
#### Buscando por linhas específicas no código, pressione:
```
CTRL + SHIFT + O
```
##### Navegue na lista de simbolos que aparecer, até você encontrar exatamente a linha de código que deseja.

#### Abrir terminal nativo do SO pelo VSCODE, pressione:
```
CTRL + SHIFT + C
```
Este comando acima abre o terminal nativo na pasta do projeto aberto no VSCODE.

#### Selecionando linha do Início/Fim:

Clique no Início da linha e pressione:
```
SHIFT + End
```

#### Selecionando linha do Fim/Inicio:

Clique no Fim da linha e pressione:
```
SHIFT + Home
```
-------------------------------
#### Utilizando a tag `pre` e `code` para mostrar código fonte na página.

```
<pre><!---->
<code><!---->
  #inlude &lt;iostream&gt;
  
  using namespace std;

  int main(){

    cout << "Hello World!\n";
      
    return 0;

  }
</code>
</pre>
```

A tag `pre` ajusta as tabulações e enter do código adicionado exatamanete como está na página
A tag `code` serve para colocarmos um exemplo de código no site podemos usar a tag code

-------------------------------
#### Carrega a página no próprio frame.
```
<a href="www.site.com.br" target="_self">Link 1</a>
```
#### Geralmente `target="_self"` é usado nos links internos da prória página.

#### Carrega a página em uma nova janela do navegador.
```
<a href="www.site.com.br" target="_blank">Link 1</a>
```
##### Geralmente `target="_blank` é usado para link's externos de outros sites.

-------------------------------
#### Crie um projeto chamado `comandos_emmet`:

#### Crie uma página `index.html`

#### Abra o VSCODE e va até `Arquivo >> Abrir Pasta` procure o projeto no local onde foi criado.

#### Na página `index.html` digite:
```
html
```

#### Então aparecerá:
```
html:5
html:xml
```

#### Escolha `html:5` ele criará a estrutura básica abaixo:
```
<!DOCTYPE html>

<html lang="en">

<head>
    <meta charset="UTF-8">

    <meta http-equiv="X-UA-Compatible" content="IE=edge">

    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Document</title>
</head>

<body>

</body>

</html>
```
-------------------------------
#### Altere `lang="en"` para `lang="pt-br"`

#### Altere a tag `title` colocando `Emmet Abreviation VSCODE`

#### Adicione os scripts abaixo no fim da página dentro da tag `body` para não termos problemas com precedência de execução.
```
<!-- jQuery first, then Popper.js, then Bootstrap JS -->
<script src="https://code.jquery.com/jquery-3.3.1.slim.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.3/umd/popper.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/bootstrap@4.1.3/dist/js/bootstrap.min.js"></script>
```

#### Adicione dentro da tag `head` a seguinte linha abaixo:
```
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@4.1.3/dist/css/bootstrap.min.css">
```

#### Ainda dentro da tag `head` adicone após o link do `bootstrap4` o link abaixo referente ao nosso arquivo `css/style.css` para podermos sobrescrever as classes do bootstrap4:
```
<link rel="stylesheet" href="css/style.css">
```
#### Presssione `CTRL+CLICK` no link `css/style.css` para criar a pasta e o arquivo no projeto se não existir. 

#### Ficando desta forma abaixo:
```
<!DOCTYPE html>

<html lang="pt-br">

<head>
    <meta charset="UTF-8">

    <meta http-equiv="X-UA-Compatible" content="IE=edge">

    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@4.1.3/dist/css/bootstrap.min.css">

    <link rel="stylesheet" href="css/style.css">

    <title>Emmet Abreviation VSCODE</title>
</head>

<body>


    <!-- jQuery first, then Popper.js, then Bootstrap JS then JavaScript page -->
    <script src="https://code.jquery.com/jquery-3.3.1.slim.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.3/umd/popper.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@4.1.3/dist/js/bootstrap.min.js"></script>
    <!--script src="js/script_page.js"></script-->

</body>

</html>
```
-------------------------------
#### Criando a tag `header` e tag `nav` adicionando as classes do bootstrap4 nas tag's:

#### Dentro da tag `body` digite a `Emmet Abbreviation` abaixo:
```
header>nav.navbar.navbar-expand-md.navbar-dark.bg-dark + ENTER

<header>
  <nav class="navbar navbar-expand-md navbar-dark bg-dark"></nav>
</header>
```

#### Agora dentro da tag `nav` iremos criar uma `div` com as classes `collapse` e `navbar-collapse` do bootstrap4, juntamente com o id `navegacao` para ocultar os link's e criar o `menu hamburguer` então digite `div.collapse.navbar-collapse#navegacao + ENTER`:
```
<header>
  
  <nav class="navbar navbar-expand-md navbar-dark bg-dark">
  
   div.collapse.navbar-collapse#navegacao + ENTER

  </nav>

</header>
```
#### Note que ao usarmos o `Emmet Abbreviation` do VSCODE para criar a `div` definimos um `id="navegacao"`, este id será fundamental para a criação do `menu-hamburguer` menu responsivo.

#### Após executar o `Emmet Abbreviation` acima dentro da tag `nav` teremos a estrutura da `div` abaixo:
```
<header>
  
  <nav class="navbar navbar-expand-md navbar-dark bg-dark">
  
   <div class="collapse navbar-collapse" id="navegacao"></div>

  </nav>

</header>
```

#### Agora na tag `div` que está dentro da tag  `nav` no `header`, criaremos uma `ul` lista não ordenada com `5 li's` com `1 link` em cada li então digite `ul.navbar-nav.ml-auto>li.nav-item*5>a.nav-link*1 + ENTER`:
```
<header>
  
  <nav class="navbar navbar-expand-md navbar-dark bg-dark">
  
   <div class="collapse navbar-collapse" id="navegacao">
  
    ul.navbar-nav.ml-auto>li.nav-item*5>a.nav-link*1 + ENTER

   </div>

  </nav>

</header>
```

#### Após executar o `Emmet Abbreviation` acima teremos a estrutura da `ul` dentro da tag `div`:

#### Em cada um dos `link's` coloque `#1`, `#2`, `#3`, `#4`, `#5` para que quando clicar no primeiro link os outros não fiquem visitados também.
```
<!DOCTYPE html>
<html lang="pt-br">

<head>
    <meta charset="utf-8">

    <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">

    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@4.1.3/dist/css/bootstrap.min.css">

    <link rel="stylesheet" href="css/style.css">

    <title>Emmet Abbreviation VSCODE</title>
</head>

<body>

    <header>

        <nav class="navbar navbar-expand-md navbar-dark bg-dark">

            <div class="collapse navbar-collapse" id="navegacao">

                <ul class="navbar-nav ml-auto">
                    <li class="nav-item">
                      <a href="#1" class="nav-link"></a>
                    </li>

                    <li class="nav-item">
                      <a href="#2" class="nav-link"></a>
                    </li>
                    
                    <li class="nav-item">
                      <a href="#3" class="nav-link"></a>
                    </li>
                    
                    <li class="nav-item">
                      <a href="#4" class="nav-link"></a>
                    </li>

                    <li class="nav-item">
                      <a href="#5" class="nav-link"></a>
                    </li>
                </ul>

            </div>

        </nav>

    </header>

    <!-- jQuery first, then Popper.js, then Bootstrap JS then JavaScript page -->
    <script src="https://code.jquery.com/jquery-3.3.1.slim.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.3/umd/popper.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@4.1.3/dist/js/bootstrap.min.js"></script>
    <!--script src="js/script_page.js"></script-->

</body>

</html>
```

#### Agora dentro da tag `body` após a tag `header` vamos criar uma `div` com `id="container"` e um parágrafo `p` com a classe `class="paragrafo"` e um link dentro do parágrafo com a classe `class="direita"` então digite o `Emmet Abreviation` abaixo:
```
div#container>p.paragrafo>a.direita + ENTER

 <div id="container">
   <p class="paragrafo">
    <a href="" class="direita"></a>
   </p>
 </div>
```
Adicione um texto lorem ipsum no parágrafo.

#### Ficando desta forma abaixo:
```
<!DOCTYPE html>
<html lang="pt-br">

<head>
    <meta charset="utf-8">

    <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">

    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@4.1.3/dist/css/bootstrap.min.css">

    <link rel="stylesheet" href="css/style.css">

    <title>Emmet Abreviation VSCODE</title>
</head>

<body>

    <header>

        <nav class="navbar navbar-expand-md navbar-dark bg-dark">

            <div class="collapse navbar-collapse" id="navegacao"></div>

        </nav>

    </header>

    <div id="container">
        <p class="paragrafo">

         <a href="#6" class="direita">Leia Mais</a>
        </p>
    </div>

    <!-- jQuery first, then Popper.js, then Bootstrap JS then JavaScript page -->
    <script src="https://code.jquery.com/jquery-3.3.1.slim.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.3/umd/popper.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@4.1.3/dist/js/bootstrap.min.js"></script>
    <!--script src="js/script_page.js"></script-->

</body>

</html>
```

#### Barra de navegação com o `menu-hamburguer` menu responsivo:

#### Agora digite esta estrutura abaixo dentro da tag `nav` antes da tag `div`:
```
 <button class="navbar-toggler" data-toggle="collapse" data-target="#navegacao">
  
  <span class="navbar-toggler-icon"></span>

 </button>
```

#### Ficando como abaixo:
```
<!DOCTYPE html>
<html lang="pt-br">

<head>
    <meta charset="utf-8">

    <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">

    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@4.1.3/dist/css/bootstrap.min.css">

    <link rel="stylesheet" href="css/style.css">

    <title>Emmet Abbreviation VSCODE</title>
</head>

<body>

    <header>

        <nav class="navbar navbar-expand-md navbar-dark bg-dark">

            <button class="navbar-toggler" data-toggle="collapse" data-target="#navegacao">

                <span class="navbar-toggler-icon"></span>

            </button>

            <div class="collapse navbar-collapse" id="navegacao">

                <ul class="navbar-nav ml-auto">
                    <li class="nav-item">
                      <a href="#1" class="nav-link">Home</a>
                    </li>

                    <li class="nav-item">
                      <a href="#2" class="nav-link">Sobre</a>
                    </li>

                    <li class="nav-item">
                      <a href="#3" class="nav-link">Serviços</a>
                    </li>

                    <li class="nav-item">
                      <a href="#4" class="nav-link">Quem Somos</a>
                    </li>

                    <li class="nav-item">
                      <a href="#5" class="nav-link">Contato</a>
                    </li>
                </ul>

            </div>

        </nav>

    </header>

    <div id="container">

        <p class="paragrafo">
            Lorem ipsum dolor, sit amet consectetur adipisicing elit.
            Magnam illum accusantium voluptas velit.
            Voluptate molestiae maxime, hic obcaecati adipisci consequuntur ducimus.
            Blanditiis unde quae voluptate distinctio quibusdam. Explicabo, amet autem!
            <a class="direita" href="#" target="_blank">Leia Mais</a>
        </p>

    </div>

    <!-- jQuery first, then Popper.js, then Bootstrap JS then JavaScript page -->
    <script src="https://code.jquery.com/jquery-3.3.1.slim.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.3/umd/popper.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@4.1.3/dist/js/bootstrap.min.js"></script>
    <!--script src="js/script_page.js"></script-->

</body>

</html>
```

#### PS: para que a página responsiva funcione, temos que adicionar os scripts js abaixo no fim página dentro da tag `body` para não termos problemas com precedência de execução:
```
<!-- jQuery first, then Popper.js, then Bootstrap JS then JavaScript page -->
<script src="https://code.jquery.com/jquery-3.3.1.slim.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.3/umd/popper.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/bootstrap@4.1.3/dist/js/bootstrap.min.js"></script>
<!--script src="js/script_page.js"></script-->
```

#### Caso tenha preferência por adicionar os scripts JS no cabeçalho `head` use o atributo `defer` no link do script. O atributo defer diz ao navegador para executar o script apenas quando a análise do HTML estiver finalizada.
```
<head>

<script defer src="js/script.js">

</head>
```

#### O arquivo `css/style.css` deste exemplo tem as seguintes configurações:
```
/*
* Prefixed by https://autoprefixer.github.io
*/

/*
**Style Emmet Abreviation page
*******************************
*/

/*
Zera todas as bordas, margens, padding, 
e retira o estilo de todas as listas "ul, ol -> list-style=none" 
na página em que o arquivo style.css for utilizado.
*/

* {
    border: 0;
    margin: 0;
    padding: 0;
    list-style: none;
    box-sizing: border-box;
}

/*Definindo as configurações padão da tag body*/
body {
    font-style: normal;
    background: #DEDEDE;
    font-family: Arial, Helvetica, sans-serif;
}

/*Definindo o tamanho da página usando o id container.*/
#container {
    width: 920px;
    margin: auto;
    padding: 20px;
    background: white;
    border: 1px solid black;
    box-shadow: 5px 5px 10px rgba(0, 0, 0, 0.5);
}

/*Definindo as configurações do parágrafo na classe "paragrafo".*/
.paragrafo {
    color: black;
    font-size: 15pt;
    text-indent: 50px;
    line-height: 25px;
    margin-bottom: 0;
    text-align: justify;
}

/*Definindo a posição do link com a classe ".direita"*/
.direita{
    text-align: right;
    margin-left: 247px;
}

.direita a{
    display: block;
    text-decoration: none;
}

/*Cor do link ao passar o mouse*/
.direita, a:hover {
    color: #f645c4;
    text-decoration: none;
}

/*Cor do link visitado*/
.direita, a:visited {
    color: red;
}

/*Estado hover dos link's visitados*/
.direita, a:visited:hover {
    color: green;
}

/*Alterando a cor dos link's na barra de navegação.*/
.navbar-dark .navbar-nav .nav-link {
    color: blue;
    display: block;
    font-size: 12pt;
    font-weight: bold;
    text-decoration: none;
}

/*Cor dos links visitados na barra de navegação*/
.navbar-dark .navbar-nav .nav-link:visited {
    color: red;
}

/*Cor dos link's visitados na barra de navegação ao passar o mouse*/
.navbar-dark .navbar-nav .nav-link:visited:hover {
    color: green;
}

/*Utilizando as classes do bootstrap através da especificidade, 
definiremos o estado hover; efeito ao passar o mouse nos link's.*/
.navbar-dark .navbar-nav .nav-link:hover {
    color: aqua;
    font-size: 12pt;
    font-weight: bold;
    padding: 3px;
    background: white;
    border-radius: 10px;
}

/*Deixando responsivo*/
@media screen and (max-width: 920px) {

    /*Pega a largura do dispositivo em 100% até 920px*/
    #container {
        width: 100%;
    }
}
```
-------------------------------
#### Utilizando a `pseudo-classe` CSS `:root` e variáveis no css:

#### Sem utilizar a variável:
```
body {
  background-color: #DEDEDE;
}
```

#### Usando a variável fica assim:
```
:root {
  --bg-light: #f8f9fa;
  --red: red;
  --black: black;
  --white: #fff;
  --bg-cinza: #DEDEDE;
  --font-family-sans-serif: "Arial", "Helvetica", "sans-serif";
}
```

#### Feito isso podemos usar esse valor usando a função `var()`, dessa forma:
```
body {
  background-color: var(--bg-cinza);
  font-family: var(--font-family-sans-serif);
}
```

#### Utilizando a função `var()` para configurar outras tag's.
```
nav ul li a{
    padding: 3px;
    display: block;
    color: var(--black);
    text-decoration: none;
    background: var(--bg-light);
}
```

#### Utilizando a função `var()` para configurar a cor do estado hover.
```
nav ul li a:hover{
    padding: 5px;
    display: block;
    color: var(--red);
    transition: all .3s;
    text-decoration: none;
    background-color: var(--white);
}
```

#### Podemos utilizar também da seguinte forma abaixo:
```
color: var(--blue)

border: 1px solid var(--black)

background: var(--light)

backgroud-color: var(--cor-secundaria)
```

#### No seu projeto html5 na pasta `css` crie um arquivo chamado `colors.css`;
#### Para utilizar estas configurações basta formatar neste arquivo as tag's que deseja, e importar este arquivo `css/colors.css` para a página em que deseja:
```
<link rel="stylesheet" href="css/colors.css">
```

#### Copie e coloque esta `pseudo-classe` abaixo no arquivo `css/colors.css` do seu projeto.
```
:root {
    --cor-principal: #2e3e4d;
    --cor-secundaria: #dee4eb;
    --blue: #007bff;
    --indigo: #6610f2;
    --purple: #6f42c1;
    --pink: #e83e8c;
    --red: #dc3545;
    --orange: #fd7e14;
    --yellow: #ffc107;
    --green: #28a745;
    --teal: #20c997;
    --cyan: #17a2b8;
    --white: #fff;
    --gray: #6c757d;
    --gray-blue: #53687a;
    --gray-dark: #343a40;
    --primary: #007bff;
    --secondary: #6c757d;
    --success: #28a745;
    --info: #17a2b8;
    --warning: #ffc107;
    --danger: #dc3545;
    --light: #f8f9fa;
    --dark: #343a40;
    --breakpoint-xs: 0;
    --breakpoint-sm: 576px;
    --breakpoint-md: 768px;
    --breakpoint-lg: 992px;
    --breakpoint-xl: 1200px;
    --font-family-sans-serif: "Arial", "Helvetica", "sans-serif";
}

/*
**Tags configuradas com a função var():
*/

body{
    background-color: var(--light);
    font-family: var(--font-family-sans-serif);
}

nav ul li a{
    padding: 3px;
    display: block;
    color: var(--purple);
    text-decoration: none;
    background: var(--teal);
}

nav ul li a:hover{
    padding: 5px;
    display: block;
    color: var(--white);
    transition: all .3s;
    text-decoration: none;
    background-color: var(--gray-blue);
}
```
[Utilize variáveis no seu css com a função var](https://medium.com/trainingcenter/utilize-vari%C3%A1veis-no-seu-css-com-a-fun%C3%A7%C3%A3o-var-4645cebbb770)

-------------------------------
### Melhorando a performace do vscode:

#### Após abrir o seu vscode pela primeira vez, será criado em seu usuário a pasta `~/.vscode`, que conterá todas as configurações e extensões do Editor.

#### Abra a Paleta de Comandos pressionando `CTRL+SHIFT+P` execute o comando:
```
Preferences: Configure Runtime Arguments
```

##### ou edite o arquivo:
```
nano ~/.vscode/argv.json
```

#### Descomente a seguinte linha:
```
// "disable-hardware-acceleration": true,
```

#### Deixando como abaixo:
```
"disable-hardware-acceleration": true,
```

#### Abra a Paleta de Comandos novamente pressionando `CTRL+SHIFT+P` execute:
```
Preferences: Open User Settings(JSON)
```

##### ou edite o arquivo
```
nano ~/.config/Code/User/settings.json
```

##### O arquivo `settings.json` tem a seguinte estrutura:
```
{
    "workbench.startupEditor": "none",
}
```

#### Adicione esta linha abaixo dentro das chave `{}` acima das configurações existentes:
```
"terminal.integrated.gpuAcceleration": "off",  // Disable hardware aceleration.

////////////////////////////////////////

```

* Adicionando outras melhorias significativas no vscode:

#### Adicione as linhas abaixo dentro das chaves `{}` acima das configurações existentes:
```
"breadcrumbs.enabled": false, //Desabilita a visualização do caminho dos arquivos
"editor.tabSize": 4, // Tabulação com 4 espaços
"editor.insertSpaces": true, //Configura interseção de espaços para a tabulação
"editor.cursorStyle": "block",  //Faz o cursor se comportar como um bloco
"editor.cursorBlinking": "smooth",  //Efeito fadein/fadeout do cursor
"editor.fontSize": 16, // Aumenta o tamanho da fonte no editor, default é 14.
"editor.fontWeight": "bold", // Deixa a letra em formato bold, default é normal.
"editor.lineHeight": 30, // Altura da linha dos códigos no editor, default é 20.
////////////////////////////////////////
```

#### Após adicionar as configurações nosso arquivo ficará com a seguinte estrutura abaixo:
```
{

"breadcrumbs.enabled": false, //Desabilita visualização do caminho dos arquivos, default é true 
"editor.tabSize": 4, // Tabulação com 4 espaços
"editor.insertSpaces": true, //Configura interseção de espaços para a tabulação
//"editor.cursorStyle": "block",  //Faz o cursor se comportar como um bloco
"editor.cursorBlinking": "smooth",  //Efeito fadein/fadeout do cursor
"editor.fontSize": 16, // Aumenta o tamanho da fonte no editor, default é 14.
"editor.fontWeight": "bold", // Deixa a letra em formato bold, default é normal.
"editor.lineHeight": 30, // Altura da linha dos códigos no editor, default é 20.
////////////////////////////////////////

"terminal.integrated.gpuAcceleration": "off",  // Disable hardware aceleration.

////////////////////////////////////////

    "workbench.startupEditor": "none"
}
```

Pressione `CTRL+X e S` para sair e salvar.

#### Agora edite o arquivo `/usr/share/applications/code.desktop`
```
sudo nano /usr/share/applications/code.desktop
```

##### Comente a linha:
```
#Exec=/usr/share/code/code --unity-launch %F
```
Adicione a linha:
```
Exec=/usr/share/code/code --disable-gpu
```

Feche o vscode e abra novamente.

-------------------------------
#### Fazendo o google-chrome abrir mais rapido.

##### Edite o lançador do navegador:
```
sudo nano /usr/share/applications/google-chrome.desktop
```

##### Comente a linha:
```
#Exec=/usr/bin/google-chrome-stable %U
```

##### Adicione a linha:
```
Exec=/usr/bin/google-chrome-stable %U --disable-gpu
```

#### O mesmo pode ser feito para o firefox, não é nescessário fazer em todas as linhas que contém `Exec` somente na primeira que aparecer.

-------------------------------

#### Caso deseje remover as configurações, abra a Paleta de Comandos novamente pressionando `CTRL+SHIFT+P` navegue até:
```
Preferences: Open User Settings(JSON)
```
E remova todas as configurações acima da linha de comentário `/////////////////////`

#### Resetando configurações e extensões completamente caso deseje:

##### Remove a pasta com as configurações do vscode e extensões.
```
rm -rf ~/.vscode
```

##### Remove por completo todas as condifigurações e extensões.
```
rm -rf ~/.config/Code
```
##### Após rodar estes dois comandos acima é so abrir o vscode novamente.


[How can I disable GPU Visual Studio Code](https://stackoverflow.com/questions/29966747/how-can-i-disable-gpu-rendering-in-visual-studio-code)

[Melhorias significativas para o seu VSCode](https://medium.com/contexto-delimitado/agrad%C3%A1vel-visual-studio-code-542fec41dee3)

-------------------------------
## Plugins úteis vscode

### Live Preview -> Microsoft microsoft.com

##### Ao abrir a página usando o `Live Preview`, ele mostrará as alterações feitas no documento em tempo real no prório editor lado a lado. Esta estensão também mostra alterações feitas em arquivos `README (Markdown)` no próprio editor.

##### Clique com o botão direito do mouse na página html => (Show Preview)
ou
##### Clique no icone `Show Preview` que será habilitado no editor.

-------------------------------
### Live Server (Five Server)

#### Pesquise por `five server` e instale a extensão.

#### Ao abrir a página usando o servidor `five server` ele mostrará as alterações feitas na página em tempo real no navegador.

##### Clique com o botão direito do mouse na página html => (Open with Five Server)

-------------------------------
### Pesquise por `Tabnine AI Autocomplete`:
* Tabnine AI Autocomplete for JavaScript, Python, Java, Typescript & all other languages

-------------------------------
#### Pesquise por `AutoFileName`
* Auto file name -> completa nome de arquivos

### Pesquise por `Auto Complete Tag`
#### Esta extensão é um pack com as extensões abaixo:

* Auto Close Tag -> fecha a tag automáticamente
* Auto Rename Tag -> renomeia abertura e fechamento das tag's

-------------------------------
### Pesquise por `Class autocomplete for HTML`:
#### Aparecerá as extensões abaixo:

* Class autocomplete for HTML - README -> completa nome de classes css

* IntelliSense for CSS class names in HTML -> completa nome de classes css

Instale a versão mais recente.

-------------------------------
* Auto Import - ES6 & TS -> Add JavaScript Support (ES6)

* StandardJS - JavaScript Standard Style -> Visual Studio Code extension for JavaScript Standard Style.

* shell-format -> A formatter for shell scripts, Dockerfile, gitignore and others..

-------------------------------
### Copiando texto de imagens.
* BlackBox extension firefox
[BlackBox Extension](https://addons.mozilla.org/pt-BR/firefox/addon/blackbox/)

* BlackBox extension google-chrome
[BlackBox Extension](https://chrome.google.com/webstore/detail/blackbox-code-search-auto/mcgbeeipkmelnpldkobichboakdfaeon)

-------------------------------
### HTML Boilerplate
Cria uma estrutura simples do HTML5

* html:5
* html5-boilertemplate
* html5-start
* html5-start-optimized
* html5-bootstrap
* html-table
* html-form

-------------------------------
### HTML SNIPPETS SKA:

* CTRL + SHIFT + H -> Cria toda estrutura de codigos html5
* CTRL + SHIFT + T -> Cria toda estrutura de uma tabela
* CTRL + SHIFT + F -> Cria toda estrutura de um formulario
* CTRL + SHIFT + O -> Optimiza o codigo html5
* CTRL + ALT + R -> cria todas as classes e id no css

-------------------------------
* Java IDE -> "vscode-java-saber" "Java IDE"

* Java IDE Pack -> All awesome VS Code extensions for Java development.

### Pesquise por `Community Server Connectors`:

#### Aparecerá:
* Community Server Connectors -> Red Hat redhat.com

Com os seguintes servidores abaixo:
```
Apache Tomcat
Apache Karaf
Apache Felix
Jetty
Glassfish
Websphere Liberty
```
-------------------------------
[Running VScode linux all](https://code.visualstudio.com/docs/setup/linux)

[KeyBoard Short Cut Linux](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-linux.pdf) - Comandos VSCODE linux

[Fundação Bradesco](http://www.fundacaobradesco.org.br/vv-apostilas/cursoHTML/Arquivo_do_menu_opcoes.html)

[VS Code Configuration](https://gist.github.com/AlanD20/c7ca5e96a929d87f0a1e349982ccfde9)

[Disable gpu vscode](https://stackoverflow.com/questions/29966747/how-can-i-disable-gpu-rendering-in-visual-studio-code)

[Deixando o vscode mais agradavel](https://medium.com/contexto-delimitado/agrad%C3%A1vel-visual-studio-code-542fec41dee3)

[VSCODE Proditividade infinita](https://github.com/bylearn/VS-Code-Produtividade-Infinita)

[Criando um README para seu perfil](https://natansl.medium.com/criando-um-readme-para-seu-perfil-no-github-6eb119218c4)

[Como fazer um bom README](https://blog.rocketseat.com.br/como-fazer-um-bom-readme/)

[DevMedia - Entidades HTML](http://arquivo.devmedia.com.br/artigos/devmedia/html-entities.html)

[SimboloCC](https://symbl.cc/pt/html-entities/)

[Emojis - README](https://gist.github.com/rxaviers/7360908)
### :+1: *Repositório VSCODE_Plugins_E_Comandos criado com o script gitpratico* :shipit:
