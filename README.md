# Formato de instrucciones

## Aclaraciones

Nuestro instruccion set solo necesita 5 bits, pero igual se seguirá el sistema normal de RISC-V por simplicidad, solamente alterando la cantidad de bits usados para opCode

![alt text](image.png)

## R-Type

Instrucciones usan solo registros

    0-4     OP Code
    5-6     Nada
    7-11    Registro destino
    12-14   NAN
    15-19   Registro 1
    20-24   Registro 2
    25-31   NAN

## I-Type

Instrucciones que reciben un immediato

    0-4     OP Code
    5-6     Nada
    7-11    Registro destino
    12-14   NAN
    15-19   Registro 1
    20-31   Immediato

## S-Type

Se usa para stores (Esta la voy a alterar mas para guardar todo el immediate seguido)

    0-4     OP Code
    5-6     Nada
    7-11    Registro destino
    12-14   NAN
    15-19   Registro 1
    20-31   Immediato

## U-Type

Cuando se usan immediatos muy grandes

    0-4     OP Code
    5-6     Nada
    7-11    Registro destino
    12-31   Inmediato

# Instrucciones

Instruccion| Tipo |
|-|-|
ADD | R
SUB | R
ADDi | U 
AND | R
OR | R
XOR | R
ANDi | U
ORi | U
XORi | U

