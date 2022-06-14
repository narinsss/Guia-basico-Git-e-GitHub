### Guia básico de Git e Github para auxiliar nos estudos

Resumo com base na aula Git e GitHub da plataforma Alura cursos, com tutor Vinícius Dias

##### Mudar de master para main ↴

`git add remote origin url.repositorio.remoto` - associar o repositório do github main com o master do local;

`git pull origin main` - puxar atualização do github

`git checkout -b main` - mudar de branch ou criar um branch main caso não exista;

**Ou rodar esses dois comandos no git bash ou terminal ↴** 

`git branch -m master main`
`git push -u origin main`



#### Criando um repositório e fazendo o primeiro commit: 

- Para saber se o git está instalado: `git --version`
- Listar pastas e arquivos: `ls` ou `dir`
- Localizar projeto a ser versionado: `cd nomeDaPasta/file`
- Subir/voltar pastas: `cd ..`
- Inicializar um repositório: `git init`
- Para saber o estado de seu repositório, se algo foi alterado, ou não: `git status`
- Para mover um arquivo para área de teste, para commitar: git add (para arquivo específico), `git add *` ou `git add` . (add all, todos os arquivos do repositório);
- Para commitar: `git commit -m "Criei um arquivo com tais informações"`



#### Configurando o seu git:

- Para editar configuração para o respositório específico: `git config --local`
- Para editar configuração em todos os projetos: `git config --global`
- Editar username: `git config --global user.name "nomeNoGitHub"`
- Editar email: `git config --global user.email "seuEmail@"`

*Para visualizar o email ou username já configurado, utilizar o mesmo código  git config --global user.email*



#### Do repositório local para o remoto(GitHub):

- Para criar um diretório: `mkdir nomeDoDiretorio`

- Tornar um repositório puro para conter apenas informações dos arquivos: `git init --bare`
- Listar repositórios remotos: `git remote`
- Para adicionar um repositório remoto: `git remote add dêUmNome C:/CaminhoDoRepositorio` ou `git remote add dêUmNome URL`
- Verificar caminho do repositório: `git remote -v`
- Clonar um repositório remoto: `git clone URL ou CAMINHO`
- Clonar e modificar o nome: `git clone URL ou CAMINHO novoNomeParaClone`
- Para mandar enviar alterações do repositório local para o remoto: `git push nomeDoRepositorioLocal main`
- Para mudar o nome do repositório remoto: `git remote rename nomeInicial nomeNovo`
- Para trazer alterações do repositório remoto para o local: `git pull nomeNovo main` 



#### Trabalhar com mais de um branch:

- Para visualizar os branch's: `git branch`
- Para criar um novo branch: `git branch outraBranch`
- Para selecionar outro branch: `git checkout branch`
- Para criar um branch e ir para ele: `git checkout -b outraBranch`
- Para excluir um branch: `git branch -d nome`
- Unir branch's com merge, gerando um commit a mais: `git merge outraBranch`, salvar e confirmar `:x`
- Para trazer os commit's de um branch para outro branch (melhor forma): `git rebase outraBranch`



#### Desfazer ações no Git:

- Para transformar arquivos staged para unstaged: `git reset HEAD nomeArquivo`
- Para desfazer alteração de determinado arquivo unstaged: `git checkout -- nomeArquivo`
- Encontrar um hash de um commit específico: `git log`
- Para descommitar: `git revert hashEspecífico`



#### Outros comandos:

- **Para criar uma pasta** para armazenar informações: `mkdir nomeDaPasta`, depois `git init --bare` dentro da pasta;

- **Para modificar o status** de um arquivo ou repositório para "unstage": `git rm --cached file/`

- **Para ver o histórico de modificações:** `git log`, `git log --oneline` (apenas os commits), `git log -p` (com todas as informações);

- **Para fazer o git ignorar um arquivo:** no repositório terá um arquivo de nome .gitignore, lá você põe o nome do arquivo que deseja ignorar;

- `Gerar um ponto imutável` na aplicação: `git tag -a v0.1.0 -m "Cmd que determina um marco ou lançamento de versão, onde novas alterações ocasionarão uma nova versão, ex. v0.1.1"`

- **Para ver todas as tag's**: `git tag`, para ver no github é só ir para a sessão "releases";

- **Para enviar ao repositório remoto a tag:** `git push origin v.0.1.0`

  

##### GIT DIFF ⏬

- **Para ver alterações** que ainda não foram commitadas: `git diff`
- **Para ver diferenças entre dois commits:** `git diff hashUm..hashDois`, os dois pontos significam até;



##### Voltar em commit's anteriores ⏬

- Verificar hash do commit usando o cmd: `git log --oneline`
- Para ir até o commit: `git checkoud hashEspecífico`
- Para incluir outro commit, é necessário criar um branch novo: `git checkout -b novo-branch`



##### Git Stash ⏬

- Para salvar temporariamente uma alteração não funcional: `git stash`
- Para ver arquivos temporários: `git stash list`
- Para aplicar modificação: `git stash apply numeroDaStash`
- Remover a Stash já aplicada: `git stash drop`
- Para aplicar e já removê-la: `git stash pop`



#### Termos importantes ↴

⚠ **Commit:** Mudanças a serem enviadas e salvas;

⚠**Branch:** Linhas de desenvolvimento;

⚠**Main:** nome do branch principal;

⚠**HashCode:** código de identificação dos commits



#### Estados   ↴

⚠ **Modified:** modificado;

⚠ **Staged:** preparado;

⚠ **Committed:** Dados armazenados de forma segura;

⚠**Untracked:** Arquivos existentes que não fazem parte do repo
