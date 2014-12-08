title: "[Dev-Tips] where.not"
date: 2014-12-08 03:14:12
tags: [rails, activerecord, tips]
author: Claudia Farias
bio: 'Meu escritório é na praia.'
github: http://github.com/krawdyah
twitter: http://twitter.com/krawdyah
---

Geralmente, trabalhando com Rails, quando precisamos fazer uma consulta que retorne os registros com valores diferentes de um dado específico, fazemos a seguinte query:

```
 Article.where('status <> draft')
```


Outra forma de fazer a mesma consulta é utilizando o `where.not` do ActiveRecord.

```
 Article.where.not(status: 'draft')
```


[api](http://api.rubyonrails.org/classes/ActiveRecord/QueryMethods/WhereChain.html#method-i-not)
