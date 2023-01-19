# O seu código vai funcionar como o esperado?

TDD é um acrônimo para Test Driven Development ou Desenvolvimento Orientado por Testes. 

Essa prática tem como premissa o desenvolvimento de código a partir do teste, ou seja, antes de qualquer coisa devemos escrever um teste de acordo com o resultado esperado e posteriormente escrevemos o código da aplicação.

Em seu blog “The Clean Code Blog”, Robert Martin diz que após sentar-se com Kent Beck para aprender mais sobre o assunto, o processo de desenvolvimento foi:

inicialmente se escreve uma linha de código de teste que irá falhar e depois se escreve uma linha de código correspondente em produção para que o teste funcione e a proporção de código era realmente muito próximo de uma linha.

A idea é escrever somente o necessário de código no projeto para que o teste funcione. 

Isso nos leva para o ciclo dos testes unitários: Red,Green, Refactor.

1. Vermelho (red): Escrever um teste que não funcione obrigatoriamente antes de escrever o código de produção.
2. Verde (green): Escreva código de produção apenas o sufciente para fazer seu teste funcionar.
3. Refatorar (refactor): Arrume a bagunça.

![Captura de tela 2023-01-19 152047](https://user-images.githubusercontent.com/60930603/213528160-d97abb8f-3cd8-43c2-90a9-2995ffa2bf56.png#vitrinedev)

Nesse sentido, gostei bastante da descrição do ciclo de TDD feita por James Shore em seu site e irei colocar aqui minha interpretação:

1. Pense: Inicialmente pese em como fazer um teste assertivo que irá ajudar na produção de seu código.
2. Red: Escreva o teste da forma mais simples possível, não mais que cinco linhas. A barra de teste deve ficar vermelha.
3. Green: Escreva o código de produção que irá passar em seu teste e execute o teste. Neste momento não se preocupe com os detalhes ou a forma de seu código. A barra de teste deve ficar verde.
4. Refactor: O seu código passou no teste então respire fundo, dê uma olhada geral em seu código e pense em como melhorá-lo. É possível fazer melhorias no código sem se preocupar em quebrá-lo. Lembre-se de executar o teste a cada mudança. Neste passo use o tempo que precisar.
5. Repita: Faça o ciclo novamente por várias vezes em uma hora e passe algum tempo refatorando seu código.

Resumindo, a filosofia é que não damos conta de pensar em duas coisas simultaneamente: Comportamento correto e  Estrutura correta.

Dito isso, o JUnit é a principal biblioteca Java, open source, para escrever testes de unitários automatizados. Criado por Kent Beck e Erich Gamma, o JUnit permite saber rapidamente se o código funciona como esperado, ou se as modificações no código estão impactando a aplicação. Essa biblioteca acabou tornando-se um padrão no mercado tendo bibliotecas correspondentes em outras linguagens de programação, por exemplo: XUnit (C#) e PyUnit (Python).

As principais vantagens dos testes automatizados são: 

 - Diminuição de testes manuais e mitigação dos riscos atrelados
 - Automatização de ações repetitivas 
 - Obtenção de feedback mais ágil
 - Segurança para mudar o código e não se perder
 - Estimular melhorias no código uma vez que facilita que a mudança possa ser desfeita ou corrigida

Cabe ainda dizer que o desenvolvedor deve ser pragmático na elaboração dos testes, isso quer dizer que você deve fazer testes úteis de forma prática e não para todas as classes e métodos, por exemplo: não é necessário testar construtores, getters e setters ou interfaces de usuário.

Além disso, há discussões sobre a aplicação do TDD nas empresas. Alguns acreditam que a implementação pode elevar os custos na produção de software e ter uma baixa aderência da equipe.

O fato é que desenvolvendo aplicações com TDD, os testes serão feitos de forma antecipada, consequentemente a funcionalidade já será implementada com cobertura de testes.

### Referências
Rodrigo da Silva Ferreira Caneppele e Alura - https://www.alura.com.br/curso-online-tdd-java-testes-automatizados-junit
Robert Martin - https://blog.cleancoder.com/uncle-bob/2014/12/17/TheCyclesOfTDD.html
James Shore - http://www.jamesshore.com/v2/blog/2005/red-green-refactor
DevMedia - https://www.devmedia.com.br/test-driven-development-tdd-simples-e-pratico/18533

Feito por **Vitor Marcato** https://www.linkedin.com/in/vitormarcato/
