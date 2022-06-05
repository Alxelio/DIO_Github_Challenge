# DIO_Github_Challenge
It's from Santander Bootcamp 2022 - First Challenge



/*			SCRIPT GIT 101 e 102
Para baixar o Git acesse o link:
https://git-scm.com/downloads
É sempre bom verificar a arquitetura, se é 32bits ou 64bits apesar dos computadores mais atuais serem de 64bits.
No caso do Sistema Operacional Windows, através do link https://gitforwindows.org/ podemos baixar o git versionado com o terminal bash para Windows.
Nesse caso o Sistema é Linux Ubuntu e o download fora feito para o respectivo Sistema Operacional.
Comando para verificar se há e qual a versão do git instalada em seu computador:
git --version
Para realizar a assinatura/configuração de seu nome, e-mail, editor de texto, entre outros aspectos:
git config --global user.name "Alxelio Esteves"
git config --global user.email "auxelio_esteves@usp.br"
git config --global core.editor subl
Para consultar os dados configurados usam-se os comandos abaixo:
git config user.name
git config user.email
git config core.editor
git config --list
Branches: São versões diferentes do meu sistema. A versão principal do meu repositório é a Master.
OBS: CASO QUEIRA BUSCAR ALGUM ARQUIVO NO SISTEMA TEMOS OS COMANDOS:
find / -iname (nome do arquivo)
ou
locate -i (nome do arquivo)
Precisa-se criar um Novo Projeto no GitLab. Adicionar o nome do projeto, status público para estar aberto à comunidade, caso queira e, sempre é bom inicializar com um arquivo README.md.
Após isso (arquivo README(GIT).md), copia-se a URL no servidor GITLAB com o botão CLONE e no diretório/local do seu computador dê o comando de clonar como segue abaixo:

				git clone https://gitlab.com/Auccelio/git-101-102.git


Deve-se colocar ou por cópia, ou por cola o respectivo arquivo que se queira "commitar", neste caso, READMEGIT.md .
O próximo passo é realizar os seguintes comandos abaixo para commitar:

				git add READMEGIT.md
				git commit -s -m "Add READMEGIT base file"
				git push origin master ou git push -u origin master 

				ls ~/.ssh/id_rsa.pub (comando para verificar se há SSH visto que o GitLab mudou sua política quanto ao HTTP)
				ssh-keygen (comando para fazer uma senha SSH)
				cat ~/.ssh/id_rsa.pub (comando para verificar se realmente foi feito uma senha SSH)


Pode-se fazer uso dos comandos:

				git status 
				git diff
				git log 
				git branch


a qualquer momento para verificar os arquivos, sem nenhum prejuízo no repositório.
Para voltar o commit ou até mesmo excluir algum, pode-se utilizar os comandos:

				git reset --soft (volta um commit anterior deixando o último preparado - em vermelho a coloração)
				git reset --mixed (volta um comit anterior contudo não deixa o último preparado, necessitando de um git add - git commit - git push origin master novamente)
				git reset --hard (Ignora tudo o que fora feito no último commit e volta ao commit anterior. Todas as alterações serão perdidas no último commit. Não é recomendado quando se trabalha em equipe)


Para se criar um novo ramo no GIT, utiliza-se o comando:
git branch teste					(por exemplo)
git checkout teste					(movimenta-se o 'ponteiro' para o ramo teste)
Quando se anda pelos ramos, cada ramo tem o poder de ver o que consta nele especificamente, não podendo detalhar os commits que estão em outros ramos. Para isso devemos colocar o 'ponteiro' no respectivo ramo que queremos detalhar.
Assim que for alterado qualquer caractere ou linha no arquivo.git, podemos verificar as alterações antes de commitar utilizando o comando:
git diff
Também podemos nos valer do comando:
git diff --name-only
Caso queiramos voltar o commit de um arquivo.git que ainda não fora commitado, podemos utilizar o comando:
git checkout HEAD --(file_name_here)
Daí voltamos um estado anterior a essa última alteração.
Com os comandos:
git remote
git remote -v
Conseguimos ver se há um arquivo.git no repositório remoto, em outras palavras, no servidor de hospedagem GitLab neste caso.
Caso tenhamos alguns arquivos que não sejam para aquela determinada pasta/diretório git ou não queiramos que elas aparecem, tanto no repositório local ou remoto, podemos utilizar o comando juntamente com um arquivo por exemplo, .gitignore:
touch .gitignore
(file_name_here)					arquivo que queremos ignorar, escrito com a respectiva extensão
(file_name_here_2)					arquivo que queremos ignorar, escrito com a respectiva extensão
git status							não aparecerá(ão) o(s) arquivo(s) dentro do arquivo .gitignore

				git add -A
				git commit -s -m "Comitando Arquivos com o .gitignore evitando que os arquivos dentro dele sejam commitados"


Há também o comando que reverte as suas alterações (no repositório local), contudo conseguimos ainda ter acesso aqueles commites de alterações. O comando é:
git revert --no-edit (código_commit)
Para adicionar um branch/ramo para o repositório remoto(servidor) devemos usar o seguinte comando:
git push origin teste				origin(remoto/servidor) e teste(ramo novo que queremos incluir)
Caso queiramos deletar qualquer branch/ramo para o repositório remoto(servidor) devemos usar o seguinte comando:
git push origin :teste				: na frente do ramo em questão faz com que o ramo seja deletado
Para deletar um branch/ramo no repositório local devemos sair dele primeiramente, e após isso, utilizar o seguinte comando:
git branch -D (file_name_here)
git Branch 							somente para consultar se realmente fora deletado
Quando estamos trabalhando em equipe, sempre há colaboração de commits no projeto (repositório remoto/servidor) e, nós devemos atualizar o nosso repositório local para estarmos alinhados com o projeto fidedignamente. Daí há a necessidade de se utilizar o comando:
git pull origin master
Esse comando não traz apenas arquivos mas o histórico também é carregado juntamente. É só nos atentarmos ao Author do commit e veremos que o processo foi o inverso do que estava sendo feito - (máquina-servidor) agora é (servidor-máquina).
Se porventura eu quiser contribuir com algum projeto no repositório remoto(servidor) eu posso utilizar o comando para clonar:
git clone https://github.com/suporteb7web/modulogit 					por exemplo
Depois de suas contribuições, o responsável pelo projeto avaliará as suas alterações para validá-las. Esse processo é feito com o botão da página do servidor chamado: New Pull Request -> Create Pull Request  (deve-se observar a base fork e o head fork se estão coerentes com o responsável e o contribuinte respectivamente)
Se for válida a contribuição, o responsável irá realizar o merge para juntar os respectivos projetos.
Referência: https://www.youtube.com/watch?v=OuOb1_qADBQ 					(Bonieky Lacerda)
*/
