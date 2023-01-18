# Centralizado

servidor contém todo o histórico
    qualquer problema no servidor impact no projeto
padrão por muitos anos


# Distribuído

toda máquina possui uma cópia do repositório
mudanças são realizadas localmente
não depende de uma única máquina


# Características do Git

ações locais
    navegação de histórico
    criação de branch
integridade
    uma vez que um arquivo é adicionado, todo seu histórico é guardado
    mesmo a remoção de arquivo é feito através de uma adção de versão onde diz que o arquivo foi removido
desenvolvimento não linear
    várias versões a partir de um único ponto
    facilidade para diversas pessoas realizarem alterações sem dependência de arquivos
independência da complexidade do projeto
    eficiência para pequenos e grandes projetos
    complexidade de uso permanece a mesma


# Quatro Estados dos Arquivos no Git

Untraked
Unmodified
Modified
Staged


# Comandos Básicos do Git

git rm --cached -r . > remove todos os arquivos do stage

git diff > modificado vs commitado
git diff --cached / git diff --staged > da área de stage vs commitados

git log --p / git log --stat / git log --shortstat > visualizar commits e seus arquivos editados

git commit --amend -m "mensagem" / git commit --amend --no-edit / git commit --amend > alteração de commits

git config --global core.editor "editor --wait" > altera o editor do git

git checkout nomedoarquivo.ext > reverte o arquivo para sua última versão

git clean -f / git checkout > remove arquivos untracked

git restore --staged nomedoarquivo.ext / git rm --cached nomedoarquivo.ext / git reset --hard > remove arquivos trakeds/staged

git update-index --skip-worktree nomedoarquivo.ext > para de rastrear o arquivo

git remote set-url origin novaurl > atualiza a url do repositório

git switch nomedabranch / git swich - > muda de branch

git push -u origin nomedabranch > envia a branch para o repositório remoto

git push --delete origin nomedabranch > deleta uma branch do repositório remoto

git branch -m novonome / git branch -m nomedabranch novonome > altera o nome da branch

git log nomedabranch --online > consulta os commits de outras branchs

git branch --no-merged > lista de branchs que não foram unidas a master

git tag nomedatag / git tag -a -m "mensagem" nomedatag > cria uma tag para o último commit

git tag nomedatag iddocommit > cria uma tag para um commit específico

git push origin nomedatag > envia a tag para o repositório remoto

git tag -d nomedatag / git push --delete origin nomedatag > deleta uma tag do repositório local e remoto

git stash > envia as mudanças para uma lista na memória

git stash list > lista as mudanças salvas na memória

git stash aply > aplica a última mudança salva na memória

git stash aply stash@{posição} > aplica uma mudança específica passando sua posição na lista

git stash pop > aplica e deleta a última mudança salva na memória

git stash pop stash@{posição} > aplica e deleta uma mudança específica passando sua posição na lista

git stash drop > remove a mudança de posição 0 na lista

git stash drop stash@{posição} > deleta uma mudança específica passando sua posição na lista

git stash branch nomedabranchnova > cria uma nova branch aplicando as mudanças salvas


# Comandos Intermediários e Avançados do Git

git reset --hard iddocommit / git reset --hard iddocommit~1 / git reset --mixed iddocommit~1 / git reset --soft iddocommit~1 > comandos para apagar branchs

git push --force / git push --force-with-lease > força o envio das informações para o repositório remoto e sobreescreve tudo


# GitHub

Issues
    mudanção que poderão ser feita e que podemos apontar nos repositórios que o dono ou outras pessoas verão

Labels
    tags que caracterizará uma issue

Milestones
    um marco a atingir, com descrição e data de conclusão

Chave SSH
    comandos para acessar o repositório
        git clone linksshdorepositorio nomedapasta > exemplo
        eval $(ssh-agent) > inicia um agente
        ssh-add caminhododiretoriodachave
