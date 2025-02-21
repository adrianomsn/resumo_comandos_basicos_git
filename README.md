# Resumo de comandos básicos Git para iniciantes
Aprendendo sobre Git e Github


FLUXO BÁSICO DE TRABALHO COM GIT


Fluxo inicial básico:

Cria diretório;
Inicia o git dentro do diretório que foi criado anteriormente → git init .
Edita ou cria os arquivos que serão utilizados
Valida se o status da alterações → git status
Adiciona os arquivos a fila de commit → git add “nome_do_arquivo”
Valida novamente se efetuou a adição anterior → git status
Efetua o commit da fila de commit organizada → git commit -m “nome_do_commit”;
Valida novamente se o commit foi corretamente → git status
Cria um repositório no GitHub por exemplo, e conecta o seu repositório local com o remoto através do -> git remote add origin “link_do_repositorio_git.git”
Efetue um push do seu repositório local para o remoto utilizando → git push origin main 
Pronto está feito. Daqui em diante considere criar outra branch secundaria no repositório local utilizando → git checkout -b “nome_branch”
Repita o processo a partir do passo 3 e na hora do git push altere apenas o nome da branch de main para alt.
Abre seu repositório GitHub, crie um PR e avalia alterações e efetue o Merge. Você pode fazer esse processo via CLI (comandos no terminal, porém como o foco do documento são resumo básico de aprendizado recomendo executa essa parte via GUI (Interface gráfica) do GitHub por ser mais intuitivo).


Dicas:

Utilize uma branch secundária e trabalhe com ela, para depois mergear as alterações da branch alt com a branch main.
RESUMO GERAL DE COMANDOS GIT


O que é Commit?
Fazendo uma analogia é como se fosse um save progress ou checkpoint. Nos quais você pode retornar a cada um desses checkpoints quando achar necessário. Comitou? Criou um checkpoint e assim por diante. Dessa forma, criando versões do código ou seja, o versionamento.
Comandos básicos:
cd → Muda de diretório, exemplo:  cd Desktop/    ← muda o diretório para o caminho da pasta Desktop;
ls → Lista os itens contidos dentro do diretório que foi determinado, como por exemplo o desktop;
pwd → Retorna o caminho completo de onde você está (print work director);
ls -a → Mostra todos os itens contidos incluindo os ocultos;
cd .. → Desloca para a pasta anterior de onde você está atualmente;
cd . → É a própria pasta onde você está;
mkdir → Cria um nova pasta chamada ‘nome_pasta’, exemplo: mkdir nome_pasta
cat  → Exibe o que tem contido dentro de qualquer arquivo editável, exemplo: cat nome_arquivo.txt 
git init . → cria um repositório git vazio dentro do caminho
rm -rf . git/ → apaga a pasta/repositório vazio caso haja alguma erro, etc.
-rf é um acrescimo de comando que força apagar sem nenhum tipo de interrupção, ou seja, rf = recursão force. Ou seja, cuidado isso pode apagar qualquer coisa sem ter o que fazer. * CUIDADO AO UTILIZAR* 
git status → Dá um resumo geral da branch utilizada
untracked files → são arquivos que ainda não foram comitados ou seja não há versionamento.
git add → Adiciona o arquivo que eu quero versionar com o commit. Exemplo: git add  nome_arquivo.txt , aqui você  adiciona esse arquivo no commit.
git commit -m → Fazer um commit e nomea-lo  por exemplo: git commit -m “comandos bash”
git config —global user.email “email@.com.br” - > assim você seta qual email/user sera definido para todos os repositórios.
git config —global user.email  ou git config —global user.name → verifica qual email ou nome está setado atualmente.
git log → Verifica os logs de todos os commits já feitos
. → diretório atual
.. → diretório anterior ao atual
 * → se refere a tudo. Por exemplo: ‘git add comandos_*’ , esse comando adicionaria para fila de commit todo os arquivos dentro ta pasta atual q tenham nome q contenham ‘comandos_’.
git diff → mostra a diferença ou alterações entre commits, por exemplo: ‘git diff comandos_git.txt’
git reset → Altera o status de um arquivo de staged para unstaged, ou seja, remove ele da fila de add para o proximo commit. Exemplo: git reset ‘nome_arquivo.txt’
git checkout -b →  Cria uma branch ou ramificação da branch main ou principal, exemplo: git checkout -b ‘nome_branch_secundaria’. 
p.s: Utiliza-se o termo -b é só quando a branch não existe ainda.
git branch → Exibe quais as branchs existentes e qual branch você está no momento.
git merge → Unifica as duas branchs, exemplo: git merge secundaria.
Vale notar que, se fizemos merge de uma branch secundaria_1 com a main e depois um merge de outra branch secundaria_2 também com a main, tanto a branch secundaria_1 como a branch secundaria_2 estarão inalteradas, pois só fizemos as alterações presentes em cada branch para main e não unindo as duas branchs secundarias antes de mergear com a main.
a ideia tb é sempre sua branch pessoal fazer merge com a main pra levar as alteracoes da SUA BRANCH, entao caso outra pessoa faça um merge entre a branch dela com a nova main branch (alterada pelo seu avanço) pode assim ocorrer um conflito.
git branch -d <nome_branch> → Apaga a branch selecionada.
git remote  add origin →  Conecta o repositório local com o repositório remoto no GitHub, Gitlab, etc.
git remote remove origin → remove o link com repo pra vc trocar de projeto por exemplo
git push - u  origin <branch que quer enviar a alteração> → Esse comando envia  todas as alterações da branch local da main para branch remota <origin>. Ou seja, envia as coisas alteradas no ultim commit para a repo remota.
GIT PUSH ENVIA ALTERACOES DE X PARA, EXEMPLO: origin main, quer dizer que está enviando da main (local) para remota (origin).
touch <nome do arquivo> → criar uma arquivo vazio
git pull - u origin <branch que quer puxar a alteração> → então você quer RECEBER alterações da origin.
git clone <link do repositório> → clona todo o repositório para sua máquina local.