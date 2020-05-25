Escrito por [**Jason McCreary**](https://jasonmccreary.me/) - [versão original](https://jasonmccreary.me/articles/practices-write-readable-code-less-complex/)

Traduzido e adaptado por [**Bruno Bandeira**](https://brunobandeira.me/)

# 10 práticas para se ter um código legível

Escrevo código há 20 anos. Durante esse período, trabalhei com 17 equipes codificando em diferentes linguagens para criar centenas de projetos. Incluindo, desde um simples blog, até [**APIs**](https://jasonmccreary.me/articles/why-i-leave-a-job/) que suportam 3.000 solicitações por segundo [**para os aplicativos mais vendidos**](https://jasonmccreary.me/articles/successful-app-fail/).

A partir dessas experiências, combinadas com [**os livros que li**](https://jasonmccreary.me/articles/the-reading-list/), ficou claro para mim o que mais importa no código: **legibilidade**.

Superficialmente, a legibilidade pode parecer subjetiva. Algo que pode variar entre linguagens, bases de código e equipes. Mas quando você olha com atenção, existem elementos em todo o código que o tornam legível.

Muitos programadores estão muito perto do computador. Se o código for executado, nada mais importa. Embora seja uma defesa comum, remove todo o elemento humano do que fazemos.

Nos últimos meses, trabalhei para extrair esses elementos em 10 práticas para escrever código, com foco em melhorar a legibilidade e diminuir a complexidade. Eu escrevi sobre isso em detalhes e os apliquei a trechos de código do mundo real no [**BaseCode**](https://basecodefieldguide.com/).

Infelizmente, muitos descartam isso como trivial demais. Fundamental demais. Mas garanto que todo código incorreto que encontrei falhou ao aplicar essas práticas. E todo pedaço de código bom, você pode encontrar pelo o menos uma dessas práticas, se não mais.

# Formatação

Muita energia é desperdiçada formatando. Tabs versus espaços. Allman versus K&R. Chegará um ponto em que você perceberá que a formatação **não é o que importa** na programação. Adote um formato padrão, aplique-o à base de código e automatize-o. Então você pode focar novamente essa energia na escrita do código.

# Código morto

Todos os blocos comentados, variáveis ​​não utilizadas e código inacessível são como *código estragado*. Eles efetivamente dizem ao leitor: "Eu não ligo para esse código". Então começa um ciclo de decadência. Com o tempo, esse código morto matará sua base de código. É a clássica  [**Teoria da Janela Quebrada**](https://en.wikipedia.org/wiki/Broken_windows_theory). Você deve procurar e destruir o código morto. Embora ele não precise ser seu foco principal, sempre seja um [**escoteiro**](https://jasonmccreary.me/articles/are-you-a-boy-scout/).

# Código aninhado / agrupado

A base de quase todo o código é lógica. Escrevemos código para tomar decisões, iterações e cálculos. Isso geralmente resulta em ramificações ou *loops* que criam blocos de código profundamente aninhados. Embora isso possa ser fácil de ser interpretado e lido por um computador, pode haver muita dificuldade para ser lido por um ser humano. Portanto, o código parece complexo e ilegível. Desvendar o código aninhado usando cláusulas de guarda, retornos antecipados ou aspectos da programação funcional.

# Usando objetos

Apesar da era atual da Programação Orientada a Objetos, ainda temos [Obsessão Primitiva](https://blog.codinghorror.com/code-smells/). Encontramos isso em longas listas de parâmetros, agrupamentos de dados e estruturas personalizadas de *array* (matriz) / dicionário. Estes podem ser refatorados em objetos. Fazer isso não apenas formaliza a estrutura dos dados, mas fornece uma base para toda a lógica repetida que acompanha os dados primitivos.

# Grandes blocos

Apesar de não possuir números concretos, os blocos de código podem atingir um comprimento crítico. Quando você determina que possui um grande bloco de código, há uma oportunidade de reconhecer, reagrupar e refatorar o código. Esse processo simples permite determinar o contexto e o nível de abstração do bloco de código, para que você possa identificar adequadamente as responsabilidades e refatorar o código em um bloco mais legível e menos complexo.

# Nomeação

Claro, nomear as coisas é difícil. Mas apenas porque tornamos difícil. Há um pequeno truque que funciona bem com muitas coisas na programação, incluindo nomeação - *adiamento*. Nunca fique preso nomeando algo. Apenas continue codificando. Nomeie uma variável como sentença, se necessário. Apenas continue codificando. Garanto que, quando você concluir o recurso, um nome melhor aparecerá.

# Removendo comentários

Esta prática foi um divisor de águas para mim. É o que me coloca no caminho de focar na legibilidade. Apesar dos [meus esforços para explicar](https://jasonmccreary.me/articles/removing-comments/), sempre há pelo menos uma pessoa que me odeia por isso. Eles têm aquele exemplo em que um comentário era absolutamente necessário. Claro, quando o sistema de telemetria do telescópio Hubble precisa fazer interface com um adaptador herdado, retornando `687` para leituras desconhecidas, então isso pode precisar ser comunicado com um comentário. Mas para praticamente todo o resto, você deve desafiar a reescrever o código para que ele não precise de um comentário.

# Retornos / devoluções razoáveis

Retornamos os valores mais estranhos para as coisas. Especialmente para casos de limites. Valores como `-1` ou `687` ou `null`. Por sua vez, muito código é escrito para lidar com esses valores. De fato, o criador do `null` o chama de [**O erro de bilhões de dólares**](https://www.infoq.com/presentations/Null-References-The-Billion-Dollar-Mistake-Tony-Hoare). Você deve retornar um valor mais razoável. Idealmente, algo que permita que o código de chamada continue mesmo no caso de um caminho negativo. Se houver casos verdadeiramente excepcionais, há maneiras melhores de comunicá-los do que `null`.

# Regra de Três

Pense em uma série matemática de números. Eu forneço o número `2` e pergunto: "O que vem a seguir?" Talvez seja `3` ou `4`, mas talvez seja `1` ou `2,1`. Na realidade, você não tem ideia. Então, forneço outro número das séries `2, 4` e pergunto: "O que vem a seguir?" Talvez seja `6` ou `8` ou `16`. Novamente, apesar de nossa confiança aumentada, não sabemos realmente. Agora forneço outro número das séries `2, 4, 16` e pergunto: "O que vem a seguir?" Agora, com três pontos de dados, nossos cérebros programadores veem a série ao quadrado e determinam o próximo número como `256`. Essa é a regra dos três.

O exemplo demonstra, sem nos distrair com o código, que não devemos predeterminar uma abstração ou design imediatamente. A Regra dos Três neutraliza nossa necessidade de combater a duplicação, adiando até que tenhamos mais dados para tomar uma decisão informada. Nas [**palavras de Sandi Metz**](https://www.sandimetz.com/blog/2016/1/20/the-wrong-abstraction), "a duplicação é muito mais barata que a abstração errada".

# Simetria

Agora, para a prática final e que dê a qualquer pedaço de código esse toque duradouro de legibilidade quase poética - *simetria*. Isso é extraído diretamente dos [**Padrões de Implementação**](https://www.amazon.com/Implementation-Patterns-Kent-Beck/dp/0321413091) de Kent Beck, que simplesmente afirmam:

> Simetria no código é onde a mesma idéia é expressa da mesma maneira em todos os lugares em que aparece.

Isto é mais fácil dizer do que fazer. A simetria incorpora o lado criativo da escrita. Está subjacente a muitas das outras práticas: nomeação, estrutura, objetos, padrões. Pode variar de linguagem para linguagem, de base de código para base de código e de equipe para equipe. Como tal, você poderia passar o resto de sua vida buscando-o. No entanto, quando você começa a aplicar simetria ao seu código, [**aparece uma forma mais pura**](https://twitter.com/gonedark/status/1041716025862119425) e o código toma forma rapidamente.

*Para mais detalhes sobre essas 10 práticas para escrever código menos complexo e mais legível, leia o [BaseCode Field Guide](https://basecodefieldguide.com/) ou ouça o [The BaseCode Podcast](https://basecodefieldguide.com/podcast/).*

Thank you **JMac** for allowing me to do this.
