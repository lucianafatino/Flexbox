# Introdução ao Flex Box

### O que é?

- Modelo de layout unidimensional e método que pode ser usado para oferecer distribuição de espaço entre elementos em uma interface e recursos de alinhamento.

### Flex Container

- É a tag que envolve os elementos e será nela que aplicaremos a propriedade "display: flex".

- Esta tag transforma todos os seus itens filhos em flex items.

- Pode ser inicializado em qualquer tipo de tag, como div, h1, span, a, etc.

- Suas propriedades relacionadas são

  - display
       - inicializador do container

  - flex-direction
      - faz o direcionamento dos itens, seja em linha ou em coluna

  - flex-wrap
       - se aplica para quebra de linha, ou não

  - flex-flow
       - junção do flex-direction e do flex-wrap

  - justify-content
       - alinha os items do container de acordo com a sua direção

  - align-items
       - alinha os items de acordo com o seu eixo do container

  - align-content
       - alinha as linhas do container

### Flex Item

- São elementos filhos diretos do container

- Eles também podem se tornar Flex Container

- Suas propriedades relacionadas são:

  - flex-grow
    - define o fator de crescimento

  - flex-basis
    - define o tamanho inicial do item antes da distribuição do espaço restante dentro do container

  - flex-shrink
    - define a capacidade de redução

  - flex
    - abreviação das propriedades anteriores

  - order
       - relacionado a ordem de distribuição e listagem dos itens

  - align-self
    - define o alinhamento de um item específico dentro do container



# Aula 02 - Fundamentos 

### Flex Container

#### Display Flex

- display: flex;
  - Torna uma tag em um elemento do tipo flex container, e assim automaticamente, todos os seus filhos diretos dessa tag tornam-se flex-items.
  - Pode ser aplicado a várias tags como divs, spans, h1, links, etc.

#### Flex Direction

- Propriedade que estabelece o eixo principal do container, definindo assim a direção que os flex items são colocados no flex container.

- Os eixos são dois: 
  - linha (horizontal)
    - row (padrão): à direção do texto, da esquerda para direita 
    - row-reverse: sentido oposto à direção do texto
  - coluna (vertical)
    - column: ordenação de cima para baixo, em coluna única
    - column-reverse: ordenação inversa, de baixo para cima

#### Flex Wrap

- Define se os itens devem ou não quebrar linha

#### nowrap

- Padrão
- Não permite quebra de linha

#### wrap

- permite a quebra de linha assim que um dos flex itens não possam ser mais compactados

#### wrap-reverse

- permite a quebra de linha assim que um dos flex itens não possam ser mais compactados, porém, na direção contrária da linha, e acima.

#### Flex Flow

- É um atalho para as propriedades **flex-direction** e **flex-wrap**



### Justify Content

- Se encarrega de alinhas os itens dentro do container, de acordo com a direção pretendida e trata da distribuição de espaçamento entre eles.

#### Variações

- flex-start: início do container
- flex-end: final do container
- center: centraliza 
- space-between: cria um espaçamento igual entre os elementos
- space-around: os espaçamentos do meio são duas vezes maiores que o inicial e final



### Align Items

- Trata do alinhamento dos flex items de acordo com o eixo do container
- O alinhamento é diferente quand os itens estão em linhas ou colunas
- Permite o alinhamento central no eixo vertical

#### Tipos de Alinhamentos

- center
  - alinhamento dos itens ao centro
- stretch
  - padrão
  - os flex items crescem igualmente
- flex-start
  - alinhamento ao início
- flex-end
  - alinhamento ao final
- baseline
  - alinhamento de acordo com a linha base da tipografia dos itens



### Align Content

- Responsável por tratar o alinhamento das linhas do container em relação ao eixo vertical do container
- Precisamos que:
  - O container utilize quebra de linhas
  - A altura seja maior que a soma das linhas dos itens

#### Tipos de Alinhamento

- Os mesmos do item Align Items e Justify Content



# Aula 03 - Fundamentos (Parte 2)

### Flex Grow

- Define a proporcionalidade de crescimento dos itens, respeitando o tamanho de seus conteúdos internos
- Não funciona se colocarmos justify-content no nosso flex-container

### Flex Basis

- Estabelece o tamanho inicial do item antes das distribuições de espaço restante dentro deles, usando como base o conteúdo interno disposto

  #### Valores Possíveis

  - Auto: caso o item não tenha tamanho, este será proporcional ao conteúdo
  - px, %, em: são valores exatos e previamente definidos
  - 0: terá relação com a definição do flex-grow
