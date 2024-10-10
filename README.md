## 📐 Projeto: Calculadora de Expressão Infixa para Pós-fixa

Este projeto é uma calculadora que converte expressões matemáticas infixas (com operadores como +, -, *, /) para notação pós-fixa (também conhecida como notação polonesa reversa). Após a conversão, a expressão pós-fixa é avaliada para produzir o resultado final. O código também lida com números decimais.

## 📋 Funcionalidades

Conversão de Expressão Infixa para Pós-fixa:
O algoritmo converte uma expressão matemática em notação infixa (por exemplo, 3 + 5 * (2 - 4)) para notação pós-fixa (3 5 2 4 - * +).
Avaliação de Expressão Pós-fixa:
Após a conversão, a expressão pós-fixa é avaliada para retornar o resultado matemático.
Suporte para Operações:
Soma (+)
Subtração (-)
Multiplicação (*)
Divisão (/)
Correção de Erros de Arredondamento:
Implementação ajustada para corrigir possíveis erros de arredondamento, especialmente em operações com números decimais.

## 🛠️ Como Compilar e Executar

### Compilação

Para compilar o código, use o GCC (ou qualquer outro compilador de C). Execute o seguinte comando no terminal:

```bash
gcc calculadora.c -o calculadora -lm
```

O argumento `-lm` é necessário para linkar a biblioteca matemática.

Execução
Após compilar, execute o programa com o seguinte comando:

```bash
./calculadora
```
O programa aceitará uma expressão infixa como entrada.

#### Exemplo de Entrada e Saída

Entrada:
```bash
3 + 5 * (2 - 4)
```

Saída:
```bash
Infixa: 3 + 5 * (2 - 4)
Posfixa: 3 5 2 4 - * +
Resultado: -7.00
```

## 🔧 Estrutura do Código

#### Pilha:
Utilizada para armazenar operadores e operandos durante a conversão e avaliação da expressão.
A estrutura da pilha é definida por um array e um ponteiro topo que indica a posição mais alta.

#### Funções:
inicializarPilha: Inicializa a pilha.
empilhar e desempilhar: Manipulam a pilha para adicionar e remover elementos.
infixaParaPosfixa: Converte a expressão infixa para pós-fixa.
expressaoPosfixa: Avalia a expressão pós-fixa e retorna o resultado.
imprimirPosfixa: Imprime a expressão na notação pós-fixa.

## 📌 Observações Importantes

O programa suporta números decimais e utiliza um ajuste para corrigir possíveis erros de arredondamento nas operações.
A entrada da expressão deve ser feita sem erros de sintaxe (parênteses bem balanceados, operadores válidos, etc.).
As operações seguem a precedência correta (multiplicação e divisão têm maior precedência que adição e subtração).
