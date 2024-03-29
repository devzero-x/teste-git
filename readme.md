Testando git...

* Atalhos teclado terminal vscode

CTRL+L limpa tela
CTRL+Insert copia
SHIFT+Insert cola
TAB completa entradas
seta para cima :arrowup navega pelas ultimos comandos inseridos no terminal

* Comandos Git 

git init

git remote add apelido url

git remote remove origin

git remote -v

git add

git push

git config --global user.email "seu emailaqui@servidor.com"

git config --global user.name "Seu Nome"

git commit -m "mensagemdocommit"

ls lista todos itens do diretório

cd.

echo > readme.txt cria um arquivo de texto com nome readme

git status

git push -u origin main

* Git remote add origin

Usado para conectar seu projeto local do Git com o repositório remoto no GitHub:

    git remote add origin git@github.com:githubuser/repositorio.git

* Git clone url 

Clona um diretório do github na maquina 

    git clone urlaqui

Pra isso, é preciso:

1. Abrir o terminal na pasta desejada
2. Inserir o comando para clonar

* Git log

Mostra os ultimos comandos usados no terminal git

    git log

# Sinalização de arquivo no vsCode

* Modified (M)

Significa que o arquivo já existia no repositório, mas que recebeu alguma modificação que ainda não foi registrada no Git.

* Untracked (U): 

Significa que o arquivo ainda não existia no repositório e que ainda não teve seu registro (commit) feito no Git.

---------------------

__Aula 02_08__

* Clonando um repositório:

Clona o repositório remoto

    git clone https://github.com/devzero-x/teste-git.git

* Git remote

Lista os repositórios remotos.

    git remote

* Origin

É a origem desse repositório (apelido do repositório remoto)

* Main

É a branch principal

* Git push

Envia os commits do repositório local para o repositório remoto.
Pode ser configurado (caso não esteja configurado ainda)

    git push 
	git push origin main

-------

Obs.: 

Para que atualizações sejam enviadas a um repositório clonado, é necessário que o dono do repositório que foi copiado permita que você contribua no repositório dele.

O procedimento é feito manualmente:

1. No git hub (dentro do repositório)
2. Abrir SETTINGS
3. No menu esquerdo > COLLABORATORS > ADD PEOPLE
4. Inserir o gitHub do usuário que você quer que colabore.
5. Esse usuário vai ter que aceitar o convite que foi enviado por e-mail

----------------------------

Fazer alterações no projeto clonado na minha máquina,

git add .
git commit
git push

Obs: Para indicar uma co-autoria usar:

    git commit -m "Adicionar nova funcionalidade.
    >
    >
    Co-authored-by: NOME <nome@email.com>
    Co-authored-by: OUTRO-NOME <outro@email.com>"

### PRONTO! AS ALTERAÇÕES FORAM COMMITADAS E PUSHADAS PARA O DIR REMOTO DE OUTRA PESSOA

Agora essa pessoa precisa "baixar" as alterações para o diretório local dela.

* git pull

Puxa os commits do remoto para o local

    git pull origin main

Com o pull podemos baixar as alterações que outro colaborador fez

Execute o comando:

    git remote -v 

para listar as entradas remotas configuradas e suas URLs.

-----------------------------

__Aula git 02 01__

# Como abrir o git de uma forma visual? O vsCode faz isso:

Abrir o source no vs code (git ) -- abrir o simbolo abaixo da lupa no menu esquerdo

As alterações ficam em "changes"
Ao passar o mouse:
O sinal de + adiciona as mudanças no git. (git add)

Agora as alterações estão em stage.

Colocar a mensagem e dar commit (git commit)

----------------

O que fazer quando outros colaboradores alteram a mesma linha de código que você?

Para baixar os arquivos de outra pessoa, clicar nos 3 pontinhos e ir em pull.

Caso tenham alterado a mesma linha de código vai dar conflito: (merge conflict)
Ele indica no arquivo modificado os conflitos
Temos que escolher qual vai ser a alteração escolhida.

Excluir a marcação indesejada e deixar a versão desejada.
git add .
git commit
git push

# SIMULANDO UM CONFLITO

O conflito acontece uma mesma linha foi alterada em 2 repositorios diferentes

# Também dá pra fazer o ajuste com o merge editor:

clicar no bortão "resolve in merge editor"

* Incoming (remoto): modificações que chegam do repositório remoto.

-- Accept Incoming: aceita modificações oriundas do remoto

-- Accept Combination Incoming First: realiza a combinação com as linhas do código do repositório remoto no topo.

-- Ignore: ignora as modificações.

* Current (local): modificações locais.

-- Accept Current: Aceita a modificação local no resultado do documento

-- Accept combination Current First: Aceita a combinação local + remoto.

-- Ignore: ignora as modificações no resultado no final.

* Result (resultado): resultado do merge, ou seja, a resolução dos conflitos de mesclagem. É o estado atual do arquivo.


-------------

Após selecionarmos a opção com o resultado desejado, devemos:

Salvar o arquivo
Clicar no botão “complete Merge”
Realizar o commit das modificações
Sincronizar as modificações para realizar o push.

Para ver as diferenças usar:

	git diff

# 04 01 DESFAZENDO UM COMMIT

No github conseguimos ver os commits feitos.

No git vcscode não conseguimos ver os logs (não tem essa opção)
Mas podemos ver aqui pelo terminal do vscode mesmo.

    git log

Pra sair do log é só apertar q
Cada commit possui um ID único

Caso queira excluir um commit é só:
dar git log e copiar o ID do commit que quer excluir e inserir o comando:

    git revert ID

O revert não deleta o commit, ele desfaz a mudança que foi feita.

# resetando um commit

Quando queremos APAGAR um commit do histórico de commits.

Exemplo:

Realizar uma mudança no rep local;
git add . ;
git commit -m ;

Quero deletar essa mudança. Seguir os seguintes passos: (ainda não dei o push pro rep remoto)

No terminal, rodar o git log;
Copiar o ID do commit ANTERIOR ao que se quer excluir;

dar o comando:

    git reset --hard id

O reset tem algumas configurações. O --hard é uma delas.
O hard apaga o commit E o código (a alteração) que foi feita junto ao commit.

Obs: NÃO é recomendado apagar commits que já estão disponíveis remotamente.

# ALTERANDO O ÚLTIMO COMMIT

Quero alterar a mensagem do último commit que foi escrito errado, por exemplo.

    git commit --amend -m "texto da mensagem do commit corrigido"

OBSERVAÇÃO:
Alterações de commit é utilizado sempre com cautela. Evitar sempre alterar commits que já estão disponíveis remotamente.

# README

O leia-me usa formato html e mark down.
Dicas sobre o que colocar no readme

- Descrição do seu projeto;
- Funcionalidades;
- Como os usuários podem utilizá-lo;
- Onde os usuários podem encontrar ajuda sobre seu projeto;
- Autores do projeto.

são legais de se ter no seu README, como:

Título e Imagem de capa;
Badges;
Índice;
Descrição do Projeto;
Status do Projeto;
Funcionalidades e Demonstração da Aplicação;
Acesso ao Projeto;
Tecnologias utilizadas;
Pessoas Contribuidoras;
Pessoas Desenvolvedoras do Projeto;
Licença.

Para colocar um título centralizado:

    <h1 align="center"> Seu título aqui </h1>

o Shields.io, ele fornece na página principal diversos exemplos de Badges (distintivos, insígnias, etc)

Exemplo de índice:

    # Índice 

    * [Título e Imagem de capa](#Título-e-Imagem-de-capa)
    * [Badges](#badges)
    * [Índice](#índice)
    * [Descrição do Projeto](#descrição-do-projeto)
    * [Status do Projeto](#status-do-Projeto)
    * [Funcionalidades e Demonstração da Aplicação](#funcionalidades-e-demonstração-da-aplicação)
    * [Acesso ao Projeto](#acesso-ao-projeto)
    * [Tecnologias utilizadas](#tecnologias-utilizadas)
    * [Pessoas Contribuidoras](#pessoas-contribuidoras)
    * [Pessoas Desenvolvedoras do Projeto](#pessoas-desenvolvedoras)
    * [Licença](#licença)
    * [Conclusão](#conclusão)

# IGNORANDO ARQUIVOS NO GITHUB

Ou fazer o git add de cada arquivo que quer adicionar ao commit ( sem o .)
Ou continuar usando o git add . mas indicar qual arquivo o git deve ignorar:
Criar um arquivo oculto chamado .gitignore e listar lá todos os tipos de arquivo que devem ser ignorados pelo commit

Exemplos:

    temp/
    senhas.txt
    *.css

O *.css ignora todos os arquivos css

Existe alguns sites geradores de gitinore: gitignore.io
Ele pede a linguagem e gera todos os nomes pra colocar no arquivo gitignore.

# COMPARTILHANDO TRECHOS DE CÓDIGO
 
 Sem precisar criar um repositório novo só pra isso.

 ícone de + no canto superior direito > NEW GIST

 Criar descrição, tipo de arquivo e copiar o código que vc quer mostrar

Então: CREATE PUBLIC GIST
Copiar o endereço que foi criado na barra de navegador
Compartilhar