# braille-logic-converter
Sistema de lógica digital que converte ASCII em Braille utilizando lógica combinacional e Mapas de Karnaugh.


Funcionalidades
- Conversão ASCII → Braille
- Lógica combinacional
- Simplificação com Karnaugh
- Verificação de paridade

Tecnologias
- Logisim

Objetivo: Acessibilidade para pessoas com deficiência visual.


## Raciocínio
Cada caractere ASCII tem um número (de 0 a 127). Quando ele entra no sistema, é transformado em binário (8 bits), mas é utilizado somente os 6 últimos bits que são os mais importantes para montar o padrão Braille.

## Como funciona a conversão
Cada caractere ASCII é transformado em binário (8 bits), mas só usamos os 6 últimos bits, que são os mais importantes. Cada um desses bits corresponde a um dos 6 pontos do Braille:
   1 4
   2 5
   3 6

## Exemplo

| Caractere | ASCII     | 6 bits finais | Pontos ativos | Resultado em Braille |
|----------|----------|---------------|---------------|----------------------|
| "        | 00100010 | 100010        | 2 e 6         | ⠢                   |
| #        | 00100011 | 100011        | 1, 2 e 6      | ⠣                   |

## Tabela Verdade

| Símbolo | b1 | b2 | b3 | b4 | b5 | b6 | A | B | C | D | E | F |
|--------|----|----|----|----|----|----|---|---|---|---|---|---|
| !      | 0  | 0  | 0  | 0  | 0  | 1  | 1 | 0 | 0 | 0 | 0 | 1 |
| "      | 0  | 0  | 0  | 0  | 1  | 0  | 0 | 1 | 0 | 0 | 0 | 0 |
| #      | 0  | 0  | 0  | 0  | 1  | 1  | 1 | 1 | 0 | 0 | 0 | 0 |
| $      | 0  | 0  | 0  | 1  | 0  | 0  | 0 | 0 | 1 | 0 | 0 | 0 |
| %      | 0  | 0  | 0  | 1  | 0  | 1  | 0 | 1 | 1 | 0 | 0 | 1 |
| &      | 0  | 0  | 0  | 1  | 1  | 0  | 0 | 1 | 1 | 0 | 0 | 1 |
| '      | 0  | 0  | 0  | 1  | 1  | 1  | 1 | 1 | 0 | 0 | 0 | 1 |
| (      | 0  | 0  | 1  | 0  | 0  | 0  | 0 | 0 | 0 | 1 | 0 | 1 |
| )      | 0  | 0  | 1  | 0  | 0  | 1  | 1 | 0 | 0 | 1 | 0 | 1 |
| *      | 0  | 0  | 1  | 0  | 1  | 0  | 1 | 0 | 0 | 1 | 0 | 0 |
| +      | 0  | 0  | 1  | 0  | 1  | 1  | 1 | 0 | 0 | 1 | 0 | 0 |
| ,      | 0  | 0  | 1  | 1  | 0  | 0  | 0 | 0 | 1 | 1 | 0 | 1 |
| -      | 0  | 0  | 1  | 1  | 0  | 1  | 1 | 0 | 1 | 1 | 0 | 1 |
| .      | 0  | 0  | 1  | 1  | 1  | 0  | 0 | 1 | 1 | 1 | 0 | 1 |
| /      | 0  | 0  | 1  | 1  | 1  | 1  | 1 | 1 | 1 | 1 | 0 | 1 |
| @      | 0  | 0  | 0  | 0  | 0  | 0  | 0 | 0 | 0 | 0 | 0 | 0 |
| :      | 0  | 1  | 1  | 0  | 0  | 1  | 0 | 1 | 0 | 1 | 1 | 1 |
| ;      | 0  | 1  | 1  | 0  | 1  | 0  | 1 | 0 | 1 | 1 | 1 | 1 |
| <      | 0  | 1  | 1  | 1  | 0  | 0  | 0 | 1 | 1 | 1 | 1 | 1 |
| =      | 0  | 1  | 1  | 1  | 1  | 0  | 0 | 1 | 1 | 1 | 1 | 1 |
| >      | 0  | 1  | 1  | 1  | 1  | 1  | 0 | 1 | 1 | 1 | 1 | 1 |
| ?      | 0  | 1  | 1  | 1  | 1  | 1  | 1 | 1 | 1 | 1 | 1 | 1 |
| [      | 1  | 1  | 0  | 0  | 1  | 1  | 1 | 0 | 0 | 1 | 1 | 1 |
| \\     | 1  | 1  | 0  | 1  | 0  | 0  | 0 | 1 | 0 | 1 | 1 | 1 |
| ]      | 1  | 1  | 0  | 1  | 0  | 1  | 0 | 1 | 0 | 1 | 1 | 1 |
| ^      | 1  | 1  | 0  | 1  | 1  | 0  | 0 | 1 | 0 | 1 | 1 | 1 |
| _      | 1  | 1  | 0  | 1  | 1  | 1  | 1 | 1 | 1 | 1 | 1 | 1 |
| {      | 1  | 1  | 1  | 0  | 1  | 1  | 1 | 0 | 1 | 1 | 1 | 1 |

