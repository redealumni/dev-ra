title: "[Dev-Tips] Rspec - Executando um único exemplo"
date: 2014-12-04 02:20:18
tags: [rails, rspec, tips]
---


O projeto ficou grande, você trabalhou em uma nova feature, commitou e esperou a sua ferramenta de entrega contínua te dizer que você quebrou um teste. Tsk, tsk, que coisa feia!

```
$ rspec spec
...
Finished in 4 minutes 5.6 seconds (files took 12.73 seconds to load)
341 examples, 1 failures, 1 pending
```

Dá preguiça mesmo de esperar toda a suite de testes rodar, as vezes você fica até preso a isso, demora tanto que eu até esqueço o que eu estava fazendo. Mas ok, um teste falhou, vou rodar somente aquele arquivo:

```
$ rspec spec/models/your_model_spec.rb
...
Finished in 1.36 seconds (files took 10.13 seconds to load)
30 examples, 1 failures
```

Um pouco melhor, mas ainda pode ser mais rápido. Tem 30 exemplos nesse arquivo e só um teste está falhando. O rspec me diz qual é esse teste, eu conserto e vou rodar novamente. Existe uma forma mais rápida de testar um grupo de teste ou um único de exemplo no RSpec: o truque é informar, além do arquivo, qual a linha do exemplo que você quer testar.

```
$ rspec spec/models/your_model_spec.rb:51
...
Finished in 0.65885 seconds (files took 9.36 seconds to load)
1 example, 0 failures
```

Depois no nome do arquivo, dois pontos (:) e o número da linha. Simples, han!
