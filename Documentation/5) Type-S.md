# Type-S Instructions

## Intro
* As instruções do tipo-S são aquelas instruções que executam stores.
* Store nada mais é do que uma operação de transferência de dados de um registrador para a memória. Mais especificamente, para um endereço de memória específico.
* Modo de Endereçamento para instruções de store: Para conseguir obter um endereço de memória para guardar um dado presente em um registrador na memória, a gente que tem que pegar o valor que está em um registrador de nossa escolha e adicionar a esse valor, um imediato de 12 bits (que tenha sofrido sign-extend). Feito isso, o valor resultante será um endereço de memória, que poderá ser utilizado para guardamos nosso dado do registrador.

## Instruções 
### 1) sb
* __Significado: Store Byte (sb).__
* __Síntaxe: sb rs2, imm, rs1__
* imm = valor imediato/constante (com sinal) de 12 bits.
* rs1 = registrador auxiliar usado para calcular o endereço de memória.
* rs2 = registrador-fonte que contém o dado a ser armazenado na memória.
* __Operação Realizada: rd = pc + signalextend(immediate[31:12] << 12).__
* Essa instrução pega o valor imediato (com sinal) de 20 bits. Depois disso, aplica extensao de sinal nele e dá um shift left nele de 12 bits. Por fim, adiciona esse valor de 32 bits ao valor do registrador pc (Program Counter) e o guarda no registrador-destino (rd).

### 2) sh

### 3) sw