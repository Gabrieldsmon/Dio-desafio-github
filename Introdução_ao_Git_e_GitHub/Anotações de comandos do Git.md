# Comandos do CMD/Git

## WINDOWS 

- cd = Usado para mudar o diretório atual no sistema de arquivos

- cd .. = volta para o diretório

- dir = Lista arquivos e diretórios no diretório atual ou em um especificado

- dir -a: Mostra todos os arquivos, incluindo os ocultos (iniciados por .)

- mkdir = usado para criar diretórios

- del / rmdir = del - excluir que tem dentro de uma pasta / rmdir - excluir uma pasta



## UNIX

- cd = Usado para mudar o diretório atual no sistema de arquivos

- cd .. = volta para o diretório

- ls = Lista arquivos e diretórios no diretório atual ou em um especificado

- ls -a: Mostra todos os arquivos, incluindo os ocultos (iniciados por .)

- mkdir = usado para criar diretórios

- rm -rf = Comando poderoso para remover arquivos e diretórios de forma recursiva e forçada.
Significado das Opções:
-r: Recursivo, usado para apagar diretórios e seu conteúdo.
-f: Força a remoção, ignorando avisos.



## GIT

- git init = É usado no Git para inicializar um novo repositório.
- git add = É usado no Git para adicionar alterações no conteúdo de arquivos ao staging area (área de preparação).
  - Essa é a primeira etapa no processo de criar um commit.

- git add . = Adiciona todos os arquivos modificados, novos ou deletados no diretório atual.

- git status = Use git status para verificar quais arquivos estão no staging area.

- git commit = É usado no Git para salvar permanentemente as alterações no histórico do repositório. 

  - Ele pega as alterações que estão no staging area (preparadas com git add) e cria um snapshot (instantâneo) delas, adicionando ao histórico do projeto

  - #### Sintaxe Básica 

    #### Git Bash - (git commit -m "Mensagem do commit")