Written by **Daan** - [original version](https://medium.com/better-programming/9-excuses-why-programmers-dont-test-their-code-8860a616b1b5)

Translated and adapted by [**Bruno Bandeira**](https://github.com/brunobandev/translated-code)

# 9 desculpas por que os programadores não testam seu código.

Uma lista de desculpas com as quais todos podemos nos relacionar.

![alt text](004-files/000.jpg "Code Testing")

Programadores e testes - definitivamente não são uma combinação feita no céu. Embora a maioria dos programadores entenda a importância dos testes e por que é útil, às vezes simplesmente não sentimos vontade.

Existem muitas desculpas que são usadas o tempo todo apenas para evitar uma coisa: escrever testes.

Você já usou alguma das desculpas desta lista?

## 1. “Meu código funciona bem - por que eu deveria me incomodar em testá-lo?”

Esse tipo de declaração geralmente é feito por desenvolvedores arrogantes. Pensar que alguém poderia escrever um código perfeito é ingênuo, na melhor das hipóteses. Até os melhores programadores cometem erros. E eles os fazem o tempo todo.

Ninguém é perfeito - os erros acontecem com muito mais frequência do que deveriam, e isso é realmente bom desde que aprendemos com esses erros.

Não há problema em confiar no seu código. Mas mesmo se outro desenvolvedor revisou seu código e o aprovou, você não deveria estar satisfeito ... ainda. Mesmo se você testou manualmente alguns casos de uso, ainda existe um perigo em todas essas coisas.

Todas essas coisas dependem do fator humano. E é exatamente isso que você não deve querer, pois o fator humano falha de tempos em tempos. Quando isso acontece, você deseja ter os testes adequados que você cobriu.

> "Na verdade, ninguém cria código perfeito da primeira vez, exceto eu. Mas só existe um de mim." ***Linus Torvalds***

## 2. “Este trecho de código não pode ser testado”

O que você quer dizer é que realmente não sabe como testar esse pedaço de código. Provavelmente, seu código está estruturado de maneira ruim, o que o torna não testável. Se for apenas esse pedaço de código, refatore-o em pedaços pequenos e testáveis.

Quando você lida com um código que não pode ser testado, uma vez que é mal projetado e o código é abaixo do ideal, você tem alguns problemas maiores. O código não testável é caro para manter e modificar. Além disso, o código não testável será difícil para os novos membros da equipe aprenderem.

Se você não estiver testando seu código, acabará enfrentando o problema em que os desenvolvedores não têm confiança para implantar o código. A falta de testes os deixa ansiosos, pois não têm a confirmação de que suas alterações não quebraram nada.

## 3. "Não sei o que testar"

Você está em dúvida sobre o que testar? Teste tudo!

Um ótimo começo seria testar o caso mais comum de tudo que você puder. Isso informará quando essa parte do código será quebrada, com maior impacto.

Mas há muito mais a testar do que apenas clicar no cenário do caminho feliz. Você deve testar alguns casos extremos de partes do seu código que são as mais complexas ou de partes com maior probabilidade de erros.

Sempre que você encontrar um bug, é uma boa prática escrever um novo teste que cubra esse caso de teste.

Torne os testes de escrita parte da sua rotina - não a torne opcional.

## 4. "O teste aumenta o tempo de desenvolvimento e o tempo está acabando"

Este é um dos maiores equívocos quando se trata de teste. Sempre que você começa a escrever testes pela primeira vez, isso definitivamente aumenta o tempo de desenvolvimento. Primeiro, você precisa aprender a escrever código testável e como fazer testes adequados. Este é um investimento que você faz a longo prazo.

Quando o teste se tornar um hábito, você economizará bastante tempo. E dores de cabeça. Fazer testes poupará o problema de desenvolvedores que não têm confiança para implantar seu código - apesar do fato de que você tem a capacidade de executar todo o seu conjunto de testes com a facilidade de clicar em um botão, é claro.

## 5. “Os requisitos não são bons”

Requisitos ruins não são uma desculpa para pular testes de escrita. Você tem muitas opções para descobrir os requisitos. Às vezes fica ainda pior. Infelizmente, requisitos não documentados são uma realidade que a maioria de nós enfrenta com mais frequência do que gostaria.

Nos dois casos, você precisa trabalhar com qualquer pequeno pedaço de documentação que possa colocar em suas mãos. Tente pesquisar e-mails antigos ou algumas anotações que você fez para tentar encontrar algumas pistas.

Você também deseja dar uma olhada nas versões atuais ou mais antigas do aplicativo - se possível, é claro. Você provavelmente encontrará muitas pistas ocultas aqui. Não se esqueça de dar uma olhada nos testes. Eles podem estar cheios de jóias escondidas que podem ajudá-lo.

Por último, mas não menos importante, tente conversar com alguns membros da equipe. Eles podem saber muito mais sobre os requisitos não documentados que você está procurando. Pense na única coisa que foi discutida, mas não documentada, naquela reunião em que você não pôde participar.

## 6. "Este pedaço de código não muda"

"Não faz sentido testar o código que não muda. Isso é uma completa perda de tempo. "

Bem, a única certeza que temos no desenvolvimento de software é que os requisitos mudarão. Às vezes, eles parecem estar sempre mudando.

As pessoas mudam de idéia por muitas razões e o fazem regularmente. A mudança de requisitos pode ser causada por muitas coisas. Algumas pessoas solicitam um recurso, mas na verdade não sabem o que querem. Infelizmente, isso acontece muito. Outra razão pela qual os requisitos podem mudar é por causa da política dentro de uma organização.

Sempre que você estiver lidando com alterações de requisitos, priorize o teste dos fluxos mais comuns.

## 7. “Posso testar dessa maneira mais rapidamente se fizer manualmente”

O problema com os testes manuais é que você deve executá-los repetidamente. E de novo.

Sim, você pode testar um determinado recurso mais rapidamente ao fazê-lo manualmente uma vez. Porém, os testes manuais consomem muito tempo quando você precisa executá-los repetidamente. O teste manual é interminável e muito caro.

A gravação de testes leva algum tempo, mas depois de fazer o teste, você pode executá-lo inúmeras vezes e custa apenas uma fração do tempo em comparação com o teste manual. A execução de um teste automatizado leva menos tempo do que abrir o navegador e digitar o endereço da página.

## 8. “O cliente quer pagar apenas pelos produtos a serem entregues”

Todo cliente deseja ver o máximo de entregas possível, pois isso dá a sensação de que a equipe de desenvolvimento está realizando algum trabalho. Quando possível, eles querem manter os custos o mais baixo possível.

É exatamente isso que os desenvolvedores dizem a seus gerentes sempre que não desejam testar.

Os testes são uma parte essencial do desenvolvimento de software, e essa parte do código é tão importante quanto qualquer outra parte  - portanto, você deve tratá-lo dessa maneira. Inclua tempo para escrever testes nas estimativas que você faz.

Escrever testes reduz os custos de manutenção e os custos de desenvolvimento a longo prazo.

## 9. "Este pedaço de código é tão pequeno ... não vai quebrar nada"

Todo desenvolvedor escreveu trechos de código tão pequenos que não poderiam quebrar nada importante. E, no entanto, ele ainda conseguiu quebrar alguma coisa. Essas duas linhas de código que você adicionou conseguiram quebrar algo que você não previa.

Como você sabe que seu código funciona perfeitamente?

Por favor, deixe suas palavras serem apoiadas por alguns testes reais. O teste completo filtra os bugs críticos, garantindo que o código funcione da maneira pretendida.

## Para finaizar

Você poderia se identificar com alguma das desculpas desta lista?

Acho que todos nós já usamos um desses antes. Da próxima vez, provavelmente devemos considerar escrever os testes, já que todos sabemos que não testar nosso código voltará a nos morder em algum momento posterior.

Obrigado por ler!
