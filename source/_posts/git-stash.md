title: "[Dev-Tips] git stash"
date: 2014-12-05 00:01:04
tags: git
author: Claudia Farias
bio: 'Meu escritório é na praia.'
github: http://github.com/krawdyah
twitter: http://twitter.com/krawdyah
---

Você está codando de boa em uma nova super feature e surge um bugs que precisa de um hotfix pra já. Ou você simplemente precisa trocar de branch por qualquer motivo. Não rola commitar tudo que você já alterou, é um canteiro de obras, vai quebrar.

A boa é de rola salvar suas alterações como rascunho temporariamente e recuperar essas alterações a qualquer momento. Sério!

Segue o fluxo:

`git status` conferiu quais alterações você fez.

`git stash` guarda todas as suas alterações em uma pilha.

`git stash list` lista todas as alterações salvas na branch.

`git stash show` te diz quais foram as alterações estão no stash, tipo um `git diff`.

`git stash apply` ou `git stash pop` recupera as alterações.

Se houver mais de um stash e precisar aplicar um mais antigo, basta referênciá-lo, por exemplo, `git stash apply stash@{2}`.


Dá pra fazer muitas coisas, inclusive criar uma nova branch a partir de um stash. Boa leitura: [git book](http://git-scm.com/book/pt-br/v1/Ferramentas-do-Git-Fazendo-Stash).
