# Hello World em Ruby on Rails

### Links do Trabalho

VÍDEO: https://youtu.be/1nbLfQadTaA

ARTIGO E SLIDE: https://drive.google.com/drive/folders/1uc0Q_-pn4zf2iNWLzMYcd-sMCLypR8N6?usp=sharing

## Hello World

Antes de tudo, caso queira ver um vídeo autoexplicativo ao invés de ler o texto abaixo, clique aqui: https://youtu.be/lbaUQUEdIbY

Primeiramente, crie uma pasta a onde você colocará o projeto. Colocamos seu nome como: “Rails”. Navegue até ela com o comando “cd” na linha de comando. No nosso caso, será: 

```
cd Rails
```

Agora, criaremos nosso novo aplicativo com o nome: “helloWorld”:

```
rails new helloWorld
```

Ao executar o comando acima, irá criar uma pasta com o nome “helloWorld”. Dentro dela vai ter diversos arquivos e subpastas que contém um arquivo Rails.
Você já possuirá um servidor web instalado no seu sistema chamado WEBRick. 

Na linha de comando, vá para a pasta criada:

```
cd helloWorld
```

Inicie o servidor com o comando:

```
rails server
```

Por padrão, o servidor é executado na porta 3000.
Portanto, o servidor web foi implantado com sucesso. Abra seu navegador e acesse:
http://localhost:3000/

Ao abrir, verá que aparecerá uma mensagem: “Yay! You’re on Rails!”. Quer dizer que deu tudo certo!

Antes de continuarmos, tentaremos explicar como um aplicativo Rails funciona.

* Qualquer solicitação ao aplicativo será atendida por métodos chamados “actions”, que são definidos em arquivos especiais chamados “controllers”.

* Essas ações executam o necessário e definirão quais serão a respostas, por exemplo, uma página HTML. As respostas, por exemplo, uma página, serão definidas em arquivos especiais que chamamos de “views”.

* Os “routes” definem qual ação o “controller” atenderá cada solicitação no arquivo chamado “routes.rb”.

Vamos criar nosso primeiro controlador chamado “welcome”. Na linha de comando:

```
rails generate controller welcome index
```

Por agora, vamos abrir a View “welcome”. Para isso, abra a pasta “app”. Dentro dela abra uma pasta chamada “views”. Abra também a pasta que criamos chamada “welcome”. Por final, abra o arquivo chamado “index.html.erb”. 

Dentro dele, vamos alterar a informação “Welcome” para “Hello World”. Irá ficar assim:

```
<h1>Hello World#index</h1>
<p>Find me in app/views/welcome/index.html.erb</p>
```

Próximo! Agora teremos que rotear as solicitações raiz para o nosso Controller. Para isso, abra a pasta “config” e depois o arquivo “routes.rb”.

Adicione a seguinte linha que informa que o caminho raiz (root path) será atendido pela ação inicial do nosso Controller:

```
root 'welcome#index'
```

Se você atualizar o navegador, verá a página que acabamos de criar!
