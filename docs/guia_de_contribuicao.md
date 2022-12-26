# Guia de Contribuição

## 1. Histórico de versão

| Versão | Data       | Descrição | Autor |
| ------ | ---------- | --------- | ------ |
| 0.1    | 10/12/2022 | Criação do documento | Lucas Rodrigues |
| 1.0   | 11/12/2022 | Revisão do documento | Kleidson Alves, Lucas Rodrigues|
| 2.0   | 14/12/2022 | Adição de exemplos e informações | Lucas Rodrigues|

## Motivação

Buscando uma padronização das contribuições para o projeto devem ser seguidas as normas apresentadas nesse documento, sejam as contibuições feitas por meio de issues, commits ou pull requests. Assim, pretende-se manter uma boa organização geral do repositório.

## Issues

As issues podem ser criadas para descrever novas funcionalidades, para informar problemas no código existente ou outras tarefas a serem realizadas no repositório.

1 - Antes de criar a issue verifique se já não há uma que trata do mesmo problema.

2 - Para uma melhor padronização do formato das issues utilize os templates disponibilizados no repositório. Após clicar em New issue, as opções de template e suas situações de uso serão apresentadas:
![](https://i.imgur.com/kWUvjnV.png)

3 - Descreva de forma objetiva o problema no título e na descrição, seguindo os itens definidos no template. Caso haja uma história de usuário relacionada, cite-a no título da issue, como no seguinte exemplo: **[US13] - CRUD de chamado**.

4 - Após criar a issue, classifique-a de acordo com as suas características utilizando labels. Para listar as labels disponíveis, clique na opção Labels na página da issue.

## Branches

Crie branches antes de iniciar o desenvolvimento de novas funcionalidades ou correções para que, quando finalizada, seja feito o merge dessa branch para a branch de desenvolvimento (develop), e posteriormente adicionadas a branch principal do repositório (main).

1 - Antes de alterar o código localmente, certifique-se sempre de que a branch esteja na versão mais recente do código com o seguinte comando:

```
git pull
```

2 - Novas branches devem ser criadas com base na develop. Para isso, execute os seguintes comandos:

```
git checkout develop
git checkout -b nome_da_nova_branch
```

3 - Caso haja uma história de usuário relacionada, utilize o seu identificador e o nome da funcionalidade como nome da branch. Por exemplo, para a US13, tratando de Crud de chamado, utilize o seguinte nome: **US13-CrudChamado**.

4 - Sempre que adicionar novos commits, faça o push para disponibilizar o código alterado para os outros desenvolvedores, evitando conflitos.
```
git push origin nome_da_branch
```

## Commits

1 - A mensagem do commit deve descrever objetivamente o que está sendo alterado ou implementado. Sendo assim, deve-se buscar fazer commits atômicos, ou seja, que implementem pequenas e significativas alterações.

2 - Caso mais de uma pessoa tenha trabalhado no commit, utilize o co-author para identificar cada um dos demais responsáveis.

Para isso, ao invés de executar:
```
git commit -m "Mensagem do commit"
```

Execute o seguinte comando, adicionando uma linha Co-authored-by para cada usuário participante e incluindo o nome e email do usuário no GitHub:
```
git commit -m "Mensagem do commit

Co-authored-by: name <name@example.com>"
```

## Pull Requests

Pull Requests podem ser criados para adicionar novas funcionalidades, correções ou documentações para outras branches.

1 - Para uma melhor padronização do formato dos pull requests utilize os templates disponibilizados no repositório.

2 - O título e a descrição do pull request devem descrever objetivamente o que está sendo alterado, seguindo os itens definidos no template.

3 - Na descrição do pull request adicione um comentário com o número da issue, no formato "#numero_da_issue" para criar um link e manter a rastreabilidade.

4 - As funcionalidades implementadas no pull request devem atender os critérios de aceitação definidos na issue relacionada.

5 - Aguarde a revisão e aprovação do pull request antes de realizar o merge.
