# Desafio de programação 1
A idéia deste desafio é nos permitir avaliar melhor as habilidades de candidatos à vagas de programador, de vários níveis.

Este desafio deve ser feito por você em sua casa. Gaste o tempo que você quiser, porém normalmente você não deve precisar de mais do que algumas horas.


## Descrição do projeto
Você recebeu um arquivo de texto com os dados de vendas da empresa. Precisamos criar uma maneira para que estes dados sejam importados para um banco de dados.

Sua tarefa é criar uma interface web que aceite upload de arquivos, normalize os dados e armazene-os em um banco de dados relacional.

Sua aplicação web DEVE:

1. Aceitar (via um formulário) o upload de arquivos separados por TAB com as seguintes colunas: purchaser name, item description, item price, purchase count, merchant address, merchant name. Você pode assumir que as colunas estarão sempre nesta ordem, que sempre haverá dados em cada coluna, e que sempre haverá uma linha de cabeçalho. Um arquivo de exemplo chamado example_input.tab está incluído neste repositório.
1. Interpretar ("parsear") o arquivo recebido, normalizar os dados, e salvar corretamente a informação em um banco de dados relacional.
1. Exibir a receita bruta total representada pelo arquivo enviado após o upload + parser.
1. Ser escrita obrigatoriamente em Ruby 2.0+ ou Python 2.7+ (caso esteja entrevistando para uma vaga específica, utilize a linguagem solicitada pela vaga).
1. Ser simples de configurar e rodar, funcionando em ambiente compatível com Unix (Linux ou Mac OS X). Ela deve utilizar apenas linguagens e bibliotecas livres ou gratuitas.


# Configuração da aplicação.

Observação¹: Esta branch foi desenvolvida utilizando-se o SGBD Postgresql. 
Observação²: Já estamos considerando que sua maquina já possue a versão 5.1.4 do Ruby On Rails ou superior.


1. Em seu terminal, acesse o diretório "importfile" ( cd importfile ) e abra seu editor de texto preferido ( preferencialmente Atom Text ou Sublime Text ).

1. Agora vamos começar a configurar a aplicação.

1. Primeiramente, vamos configurar o arquivo "database" - Abrir o arquivo "database.yml", localizado em: 'config\database.yml'.

   Altere as chaves: username e password, conforme abaixo: 

     Alterar a chave 'username: Usuario_do_seu_Banco', trocando a expressão "Usuario_do_seu_Banco" para o seu usuario do banco de dados
     postgres.

     Alterar a chave 'password: Senha_do_seu_Banco', trocando a expressão "Senha_do_seu_Banco" para sua senha do banco de dados
     postgres.

1. Após configurar o passo anterior, dentro do diretório da aplicação 'importfile' dê o seguinte comando:

     "rails db:create" - sem as aspas 

     Com este comando conseguiremos criar o nosso banco de dados

     Logo em seguida, dê comando:

     "rails db:migrate" - sem as aspas.

     Com este comando iremos criar as tabelas necesárias (e solicitadas pelo desafio).

1. Agora vamos subir o servidor local.
  
   Em seu terminal, dentro do diretório 'importfile', dê o seguinte comando:

     "bin/rails s" - sem as aspas.

 
   Após o comando acima, basta abrir seu navegador (preferencialmente o firefox) e digitar o seguinte endereço:

    "localhost:3000" - sem as aspas.

   Pronto !


  Agora basta selecionar um arquivo do formato CSV ( Somente CSV ) mencionado na descrição do desafio !



   


