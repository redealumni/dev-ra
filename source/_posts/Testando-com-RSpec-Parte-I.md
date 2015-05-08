title: "[TechTalk] Testando com RSpec 3.2 - Parte I"
date: 2015-05-08 16:39:18
tags: [teste, rspec]
author: Thiago Brandão
github: http://github.com/thiagobrandam
---

Pessoal, mais uma talk com o assunto de testes! Na verdade, essa foi uma de uma série de talks que eu quero fazer para que nosso time ganhe o hábito de sempre codar com specs de maneira consistente, e que sejam legíveis e fáceis de gerenciar.

Obviamente, o objetivo maior é deixar nossa suíte de testes tinindo, o que está longe da realidade. Se alcançarmos um nível decente de cobertura de testes (e como decente quero dizer cobrindo no mínimo as entidades _core_ do negócio), não só estaremos documentando nosso projeto mas também passaremos a ter mais confiança em adicionar / modificar _features_.

Nessa talk eu me concentrei em explicar o básico do RSpec e sugeri alguns guidelines que considero constituir passos fundamentais para se escrever bons specs em RSpec.

Baixem [aqui](https://s3.amazonaws.com/redealumnidevs/testing-with-rspec-parte-i.pdf) a versão em PDF dos meus slides.

Na próxima talk pretendo ir mais a fundo em testes de models e cobrir um pouco o mocks, stubs e spies. Até lá, familiarizem-se com o framework e escrevam suas specs seguindo os guidelines sugeridos na apresentação.

_For the lazy_:

* Use a API do model como proxy p/ escrever os specs.
* Use context quando puder.
* Evite should.
* Um expectation por exemplo (com exceção de specs de integração)
* Mesmo que use o DB, model specs ainda podem ser considerados unit specs.

Links:

* [RSpec-Core](http://www.relishapp.com/rspec/rspec-core/v/3-2)
* [RSpec-Mocks](http://www.relishapp.com/rspec/rspec-mocks/v/3-2/docs/)
* [RSpec-Expectations](http://www.relishapp.com/rspec/rspec-expectations/v/3-2/docs/)
* [RSpec-Rails](http://www.relishapp.com/rspec/rspec-rails/v/3-2/docs/)
* [BetterSpecs](http://betterspecs.org/)


P.S.: _Props_ pro [@pufe](http://github.com/pufe) que chamou atenção para o comportamento dos helpers _let_. Para quem não estava presente, os helpers _let_ só garantem a memoização do bloco [se chamados dentro de um mesmo exemplo](https://gist.github.com/thiagobrandam/9444093be25b08920c2b).

Happy spec'ing!
