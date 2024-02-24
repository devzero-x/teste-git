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

# fazendo um teste
