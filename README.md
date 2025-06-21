# Formato de instrucciones

## Aclaraciones

Nuestro instruccion set solo necesita 5 bits, pero igual se seguirá el sistema normal de RISC-V por simplicidad, solamente alterando la cantidad de bits usados para opCode

![alt text](image.png)

![alt text](inst2.png)

## R-Type

Instrucciones usan solo registros

    0-6     OP Code
    7-11    Registro destino
    12-14   func3
    15-19   Registro 1
    20-24   Registro 2
    25-31   func7

## I-Type

Instrucciones que reciben un immediato

    0-6     OP Code
    7-11    Registro destino
    12-14   func3
    15-19   Registro 1
    20-31   Immediato

## U-Type

Cuando se usan immediatos muy grandes

    0-6     OP Code
    7-11    Registro destino
    12-31   Inmediato

## S-Type

Se usa para stores

    0-6     OP Code
    7-11    Inmediato (bits 4-0)
    12-14   func3
    15-19   Registro 1
    20-24   Registro 2
    25-31   Inmediato (11-5)

## B-Type

No entiendo como funciona el immediato de esta, supongo que e bit 0 esta en 7 pero la verdad no estoy seguro

    0-6     OP Code
    7-7     [11] (ni idea)
    8-11    Inmediato (bits 4-1)
    12-14   func3
    15-19   Registro 1
    20-24   Registro 2
    25-30   Inmediato (bits 10-5)
    31-31   [20] (ni idea)

## J-Type

    0-6     OP Code
    7-11    Registro destino
    12-19   Inmediato (bits 19-12)
    20-20   [11] (ni idea)
    21-30   Inmediato  (bits 10-1)
    31-31   [20] (ni idea)


# Instrucciones

Instruccion| Tipo |
|-|-|
ADD | R
SUB | R
ADDi | I 
AND | R
OR | R
XOR | R
ANDi | I
ORi | I
XORi | I

