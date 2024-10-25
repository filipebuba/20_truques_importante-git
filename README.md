# [20 Truques importante de git](https://blog.stackademic.com/20-git-command-line-tricks-every-developer-should-know-bf817e83d6b9)



# Relatório

## Introdução
- Este documento apresenta uma visão geral dos 20 truques de linha de comando do Git que todo desenvolvedor deve conhecer, com o objetivo de aumentar a eficiência e a produtividade no uso do controle de versão.
- As principais descobertas incluem comandos que permitem um controle mais granular sobre os commits, a capacidade de reverter alterações e manter um ambiente de trabalho organizado.

## Secção 1: Comandos Essenciais do Git
- **Adicionar Interativo**: `git add -p`
- Permite organizar partes de um arquivo em vez do arquivo inteiro.
- **Desfazer o Último Commit**: `git reset --soft HEAD~1`
- Desfaz o último commit, mantendo as alterações no diretório de trabalho.
- **Verificar o Status Upstream**: `git fetch --all --prune`
- Busca atualizações do remoto e remove referências a branches excluídas.

## Secção 2: Gerenciamento de Branches
- **Limpar Branches Locais**: `git branch -d <branch-name>`
- Remove branches antigas que não são mais necessárias.
- **Cherry-Pick**: `git cherry-pick <commit-hash>`
- Aplica um commit específico de outro branch ao branch atual.
- **Estocar Trabalho**: `git stash`
- Salva alterações atuais sem fazer commit, permitindo troca de branch.

## Secção 3: Histórico e Depuração
- **Exibir Histórico de Arquivos**: `git log -- <file>`
- Mostra todos os commits que afetaram um arquivo específico.
- **Culpar uma Linha de Código**: `git blame <file-name>`
- Fornece um histórico linha por linha de quem alterou o quê em um arquivo.
- **Encontrar a Fonte de um Bug**: 
```bash
git bisect start
git bisect bad
git bisect good <older-commit-hash>
```
- Realiza uma busca binária no histórico para identificar a confirmação que introduziu um bug.

## Secção 4: Melhores Práticas
- **Reverter um Commit**: `git revert <commit-hash>`
- Cria um novo commit que desfaz as alterações do commit especificado.
- **Squash Commits**: `git rebase -i HEAD~<number-of-commits>`
- Combina vários commits em um único para um histórico mais organizado.
- **Ver Todas as Operações do Git**: `git reflog`
- Mostra um log de todas as operações no repositório, permitindo recuperar alterações perdidas.

## Conclusão
- O domínio desses truques de linha de comando pode melhorar drasticamente a eficiência e a organização no uso do Git, ajudando tanto desenvolvedores solo quanto equipes a manterem um fluxo de trabalho produtivo.
- A adoção desses comandos não apenas simplifica o gerenciamento de versões, mas também oferece um controle mais preciso sobre as alterações feitas no código.
