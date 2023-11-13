# git-flow

Repositório para demonstração do fluxo de trabalho do git, com foco na utilização de branches e pull requests para colaboração e rastreio de alterações de códigos.

## Referências

- [Github Docs: GitHub flow](https://docs.github.com/en/get-started/quickstart/github-flow)
- [Github Docs: Creating a pull request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request)
- [Github Docs:  Merging a pull request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/incorporating-changes-from-a-pull-request/merging-a-pull-request)
- [Github Docs: Linking a pull request to an issue link](https://docs.github.com/en/issues/tracking-your-work-with-issues/linking-a-pull-request-to-an-issue)

## Fluxo de Trabalho

### Descrição

O fluxo de trabalho aqui demonstrado compreende a utilização de um repositório com diversas pessoas colaborando simultaneamente em seu desenvolvimento. Dessa forma, é necessário garantir que não haja conflitos entre os códigos que foram alterados ou desenvolvidos por diferentes pessoas, isto é, é necessário que haja um desenvolvimento consistente e não divergente.

Para atingir este objetivo, é mantida uma branch principal do repositório, e as pessoas passam a desenvolver e alterar esta branch principal através de ramificações (branches) secundárias. Após finalização do trabalho na branch secundária, esta deve ser mesclada com a branch principal e, por isso, é importante que não haja conflitos nos códigos desenvolvidos/alterados.

A etapa de 'mesclagem' de volta da branch secundária para a principal deve ocorrer através de um pull request, onde o usuário solicita que sua branch seja mesclada à principal e nesta etapa podem ser realizadas revisões do código e outras verificações antes que as alterações sejam aceitas. Essa revisão de código por outros desenvolvedores podem garantir uma maior confiabilidade do código e menor taxa de erro.

Por fim, se houverem conflitos, estes devem ser resolvidos antes de finalizar o processo.

### Etapas

1. Criação de branch  
Essa etapa garante que as alterações não sejam realizadas diretamente na branch principal, facilitando a correção de erros e não propagação deste para a branch principal e, consequentemente, para os códigos que estão sendo utilizados por outros desenvolvedores. O nome da branch pode ser curto e descritivo da tarefa que será realizada nesta branch (exemplo: correcao-modelo-tg).  
A criação da branch pode ser realizada através da própria interface web do Github.
2. Realização das alterações e desenvolvimento de código  
Geralmente ocorre em tarefas como upgrade no código (criação de features, funções, correções, etc), e é interessante que não sejam realizadas grandes blocos de desenvolvimento antes de realizar o merge de volta para a principal, uma vez que isso pode facilitar a revisão do código e afins.  
Essa etapa deve ocorrer no ambiente de desenvolvimento de quem for realizar as alterações. Portanto, pode-se realizar um `git clone <repo>` ou algo do tipo para cópia do repositório para o ambiente de desenvolvimento. Ao fim, deve-se realizar o 'upload' das alterações para o repositório remoto (no github). Isso ocorre através dos comandos `git commit` e `git push`.  As mensagens dos commits podem ser de acordo com as alterações que foram realizadas e cada commit, idealmente, contem uma alteração isolada completa, para facilitar o trabalho caso seja necessário verificar ou reverter alguma alteração. Por fim, realizam-se diversos commits e pushes até que seja finalizada a tarefa em questão e possa ser realizado o review daquelas alterações para inclusão na branch principal.  
Comandos: `git clone`, `git commit` e `git push`.
3. [Criação de pull request](https://docs.github.com/en/get-started/quickstart/github-flow#create-a-pull-request)  
A criação do pull request ocorre a fim de obter os code reviews pelos colaboradores que não trabalharam naquela tarefa e consequente merge no branch principal. Na criação do pull request é interessante a inclusão de descrição sobre o que foi realizado, podendo incluir imagens, links, etc, o que for necessário para uma boa descrição.  
Pode ser que haja algum *issue* relacionado ao que foi executado de alteração nessa branch. Dessa forma, é interessante que esse pull request seja linkado ao issue em questão, sendo assim possível o rastreio das alterações que vieram a resolver aquele issue em questão. - [Linking a pull request to an issue link](https://docs.github.com/en/issues/tracking-your-work-with-issues/linking-a-pull-request-to-an-issue)
4. Merge do pull request à branch principal  
Após finalização de todas as etapas necessárias, desde a criação da branch até a criação do pull request, é realizada a mesclagem dessas alterações ao branch principal.
5. Exclusão da branch 'secundária'  
Por fim, é sugerida a exclusão da branch criada no início desse processo, com o objetivo de evitar a utilização de uma versão 'desatualizada' do repositório. Isso não irá excluir os commits ou pull requests, não perdendo informações sobre o histórico de desenvolvimento. Além disso, se necessário, é possível recuperar uma branch excluída ou reverter um pull request.

### Pull Request

https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests