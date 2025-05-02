# ♠️ Reglas del sistema experto de Blackjack en forma de Modus Ponens

## Regla 1

Si el dealer muestra un A, entonces nunca pagar seguro.

P: Dealer muestra un A
Q: No pagar seguro

## Regla 2

Si el jugador tiene A - A, entonces dividir.

P: Jugador tiene A - A
Q: Dividir

## Regla 3

Si el jugador tiene 9 - 9 Y el dealer muestra una carta entre 2 - 5 O 7 - 8, entonces dividir; si no, plantarse.

P: Jugador tiene 9 - 9 y Dealer muestra carta entre 2 - 5 o 7 - 8
Q: Dividir
P': Si no, plantarse

## Regla 4

Si el jugador tiene 8 - 8, entonces dividir.

P: Jugador tiene 8 - 8
Q: Dividir

## Regla 5

Si el jugador tiene 7 - 7 O 2 - 2 O 3 - 3 Y el dealer muestra una carta entre 2 - 7, entonces dividir; si no, pedir.

P: Jugador tiene 7 - 7 o 2 - 2 o 3 - 3 y Dealer muestra carta entre 2 - 7
Q: Dividir
P': Si no, pedir

## Regla 6

Si el jugador tiene 6 - 6 Y el dealer muestra una carta entre 2 - 6, entonces dividir; si no, pedir.

P: Jugador tiene 6 - 6 y Dealer muestra carta entre 2 - 6
Q: Dividir
P': Si no, pedir

## Regla 7

Si la suma del jugador es 8, entonces pedir.

P: Jugador tiene suma = 8
Q: Pedir

## Regla 8

Si el jugador tiene A y suma 2 O A y suma 3 Y tiene solo 2 cartas Y el dealer muestra un 5 o 6, entonces doblar; si no, pedir.

P: Jugador tiene A y suma 2 o A y suma 3, solo 2 cartas, Dealer muestra 5 o 6
Q: Doblar
P': Si no, pedir

## Regla 9

Si el jugador tiene A y suma 4 O A y suma 5 Y tiene solo 2 cartas Y el dealer muestra una carta entre 4 y 6, entonces doblar; si no, pedir.

P: Jugador tiene A y suma 4 o A y suma 5, solo 2 cartas, Dealer muestra carta entre 4 y 6
Q: Doblar
P': Si no, pedir

## Regla 10

Si el jugador tiene A y suma 6 Y tiene solo 2 cartas Y el dealer muestra una carta entre 3 y 6, entonces doblar; si no, pedir.

P: Jugador tiene A y suma 6, solo 2 cartas, Dealer muestra carta entre 3 y 6
Q: Doblar
P': Si no, pedir

## Regla 11

Si el jugador tiene A y suma 7 Y tiene solo 2 cartas Y el dealer muestra una carta entre 3 y 6, entonces doblar; SI el dealer muestra 9 o A, entonces pedir; SI NO, plantarse.

P: Jugador tiene A y suma 7, solo 2 cartas, Dealer muestra carta entre 3 y 6
Q: Doblar
P': Si Dealer muestra 9 o A, pedir
P'': Si no, plantarse

## Regla 12

Si el jugador suma 9 Y tiene solo 2 cartas Y el dealer muestra una carta entre 3 y 6, entonces doblar; si no, pedir.

P: Jugador tiene suma 9, solo 2 cartas, Dealer muestra carta entre 3 y 6
Q: Doblar
P': Si no, pedir

## Regla 13

Si el jugador suma 10 O 11 Y tiene solo 2 cartas Y el dealer muestra una carta entre 2 y 9, entonces doblar; si no, pedir.

P: Jugador tiene suma 10 o 11, solo 2 cartas, Dealer muestra carta entre 2 y 9
Q: Doblar
P': Si no, pedir

## Regla 14

Si el jugador suma 12 Y el dealer muestra una carta entre 4 y 6, entonces plantarse; si no, pedir.

P: Jugador tiene suma 12 y Dealer muestra carta entre 4 y 6
Q: Plantarse
P': Si no, pedir

## Regla 15

Si el jugador suma entre 13 y 16 Y el dealer muestra una carta entre 2 y 6, entonces plantarse; si no, pedir.

P: Jugador tiene suma entre 13 y 16, Dealer muestra carta entre 2 y 6
Q: Plantarse
P': Si no, pedir

## Regla 16

Si el jugador suma entre 17 y 21, entonces plantarse.

P: Jugador tiene suma entre 17 y 21
Q: Plantarse
