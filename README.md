<h1 align="left">INTRODUÇÃO A CIÊNCIA DA COMPUTAÇÃO COM LINGUGAME C</h1>

###

<p align="left">BY: Comunidade UNITEC</p>

###

<p align="left">INSTRUTOR: Josimar Tito             @Guilfoyle-Dev</p>

###

<h2 align="left">MÓDULO 01</h2>

###

<p align="left">Sobre</p>

###

<h2 align="left">Temas</h2>

###

<p align="left"># C<br>-<br># Compilação<br>-<br># Funções e argumentos<br>-<br># Função principal(main) e arquivos de cabeçalho<br>-<br># Ferramentas<br>-<br># Comandos<br>-<br># Tipos e Códigos de Formato<br>-<br>Operadores, limitações, truncamento<br>-<br># Variáveis e Açúcar Sintático(boas # práticas)<br>-<br>#  Condicionais<br>-<br># Expressões booleanas, loops<br>-<br>#  Abstração<br>-<br># Mario<br>-<br># Memória, imprecisão e overflow</p>

###

<h2 align="left">Tecnologias a estudar</h2>

###

<div align="left">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/c/c-original.svg" height="40" alt="c logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg" height="40" alt="git logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/github/github-original.svg" height="40" alt="github logo"  />
</div>

###

<h2 align="left">C</h2>

###

<h4 align="left">Hoje vamos aprender uma nova linguagem, C : uma linguagem de programação que tem todos os recursos do Scratch e muito mais, porém talvez um pouco menos amigável, por ser puramente em texto:<br><br>#include <stdio.h><br>int main(void) <br>{<br>    printf("olá, mundo"); <br>}<br><br>Embora a princípio tentar absorver todos esses novos conceitos possa parecer como beber de uma mangueira de incêndio - pegando emprestado uma frase do MIT - , tenha certeza de que, no final do semestre, estaremos capacitados e experientes em aprender e aplicar esses conceitos.<br><br>Podemos comparar muitos dos recursos de programação em C aos blocos que já vimos e usamos no Scratch. Os detalhes da sintaxe são muito menos importantes do que as ideias, às quais já fomos apresentados.</h4>

###

<h2 align="left">Compilação</h2>

###

<h4 align="left">No terminal no painel inferior de nosso IDE, iremos compilar nosso código antes de podermos executá-lo. Os computadores só entendem binário, que também é usado para representar instruções como imprimir algo na tela. Nosso código-fonte foi escrito em caracteres que podemos ler, mas precisa ser compilado: convertido em código de máquina, padrões de zeros e uns que nosso computador possa entender diretamente.<br><br>Um programa chamado compilador pegará o código-fonte como entrada e produzirá o código de máquina como saída. No IDE CS50, já temos acesso a um compilador, por meio de um comando chamado make . Em nosso terminal, digitaremos make hello, que encontrará automaticamente nosso arquivo hello.c com nosso código-fonte e o compilará em um programa chamado hello. Haverá alguma saída, mas nenhuma mensagem de erro em amarelo ou vermelho, então nosso programa foi compilado com sucesso.<br><br>Para executar nosso programa, digitaremos outro comando, ./hello, que procura na pasta atual , . , para um programa chamado hello e o executa.</h4>

###

<h2 align="left">Funções e argumentos</h2>

###

<h4 align="left">Usaremos as mesmas ideias que exploramos no Scratch.<br><br>Funções são pequenas ações ou verbos que podemos usar em nosso programa para fazer algo, e as entradas para funções são chamadas de argumentos.<br><br>Por exemplo, o bloco “say” (“dizer”) no Scratch pode ter considerado algo como “olá, mundo” como um argumento. Em C, a função de imprimir algo na tela é chamada de printf(com f significando texto “formatado”, que veremos em breve). E em C, passamos os argumentos entre parênteses, como em printf ("hello, world"); . As aspas duplas indicam que queremos imprimir as letras hello, world literalmente, e o ponto-e-vírgula no final indica o fim de nossa linha de código.<br>As funções também podem ter dois tipos de saídas:<br><br>efeitos colaterais, como algo impresso na tela,<br>e valores de retorno, um valor que é passado de volta ao nosso programa que podemos usar ou armazenar para mais tarde.<br>O bloco “ask” (“perguntar”) no Scratch, por exemplo, criou um bloco “answer” (“responder”).<br>Para obter a mesma funcionalidade do bloco “ask”, usaremos uma biblioteca ou um conjunto de código já escrito. A Biblioteca CS50 incluirá algumas funções básicas e simples que podemos usar imediatamente. Por exemplo, get_string pedirá ao usuário uma string, ou alguma sequência de texto, e a retornará ao nosso programa. get_string recebe algum input e o usa como prompt para o usuário, como “Qual é o seu nome?”, e nós teremos que salvá-lo em uma variável com:<br><br>string answer = get_string("Qual é o seu nome?");<br>Em C, o “=” indica atribuição ou configuração do valor à direita para a variável à esquerda. E o programa chamará a função get_string primeiro para então obter seu output.<br>E também precisamos indicar que nossa variável chamada answer é do tipo string, então nosso programa saberá interpretar os zeros e uns como texto.<br>Finalmente, precisamos nos lembrar de adicionar um ponto-e-vírgula para encerrar nossa linha de código.<br>No Scratch, também usamos o bloco “answer” dentro de nossos blocos “join” (“juntar”) e “say”. Em C, faremos isso:<br><br>printf("olá,% s", resposta);<br>O %s é chamado de código de formatação, o que significa apenas que queremos que a função printf substitua uma variável onde está o marcador %s. E a variável que queremos usar é answer, que passamos para printf como outro argumento, separado do primeiro por uma vírgula. (printf ("hello, answer")) iria literalmente imprimir hello, answer sempre.)<br>De volta ao IDE CS50, nós implementaremos o que descobrimos:<br><br>#include <cs50.h><br>#include <stdio.h><br>int main(void)<br>{<br>     string answer = get_string("Qual é o seu nome?");<br>     printf("olá, %s", resposta);<br>}<br>Precisamos dizer ao compilador para incluir a Biblioteca CS50, com #include <cs50.h>, para que possamos usar a função get_string.<br>Também temos a oportunidade de escrever o código usando um “estilo” que favoreca intuitividade, já que poderíamos nomear nossa variável de resposta com qualquer coisa, mas um nome mais descritivo nos ajudará a entender sua finalidade melhor do que um nome mais curto como a ou x.<br>Depois de salvar o arquivo, precisaremos recompilar nosso programa com make hello, já que alteramos apenas o código-fonte, mas não o código de máquina compilado. Outras linguagens ou IDEs podem não exigir que recompilemos manualmente nosso código depois de alterá-lo, mas aqui temos a oportunidade de ter mais controle e compreensão do que está acontecendo nos bastidores.<br><br>Agora, ./hello executará nosso programa e solicitará nosso nome conforme pretendido. Podemos notar que o próximo prompt é impresso imediatamente após a saída de nosso programa, como em hello, Brian ~ / $ . Podemos adicionar uma nova linha após a saída de nosso programa, de modo que o próximo prompt esteja em sua própria linha, com \n:<br><br>printf("olá, %s\n" ,resposta);<br>\n é um exemplo de sequência de escape ou algum texto que na verdade representa algum outro texto.</h4>

###
