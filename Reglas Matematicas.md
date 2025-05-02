### Reglas del Blackjack en Formato Lógico (Modus Ponens)

1. **Seguro contra A del dealer**
   - \( \text{DealerMuestra(A)} \Rightarrow \neg \text{PagarSeguro} \)

2. **Dividir A-A**
   - \( \text{JugadorTiene(A, A)} \Rightarrow \text{Dividir} \)

3. **Dividir 9-9 si dealer tiene 2–5 o 7–8; si no, plantarse**
   - \( \text{JugadorTiene(9, 9)} \land \text{DealerEntre(2, 5)} \lor \text{DealerEntre(7, 8)} \Rightarrow \text{Dividir} \)
   - \( \text{JugadorTiene(9, 9)} \land \neg(\text{DealerEntre(2, 5)} \lor \text{DealerEntre(7, 8)}) \Rightarrow \text{Plantarse} \)

4. **Dividir 8-8**
   - \( \text{JugadorTiene(8, 8)} \Rightarrow \text{Dividir} \)

5. **Dividir 7-7, 2-2, 3-3 si dealer tiene 2–7; si no, pedir**
   - \( \text{JugadorTiene(7, 7)} \land \text{DealerEntre(2, 7)} \Rightarrow \text{Dividir} \)
   - \( \text{JugadorTiene(7, 7)} \land \neg \text{DealerEntre(2, 7)} \Rightarrow \text{Pedir} \)
   - *(igual para 2-2 y 3-3)*

6. **Dividir 6-6 si dealer tiene 2–6; si no, pedir**
   - \( \text{JugadorTiene(6, 6)} \land \text{DealerEntre(2, 6)} \Rightarrow \text{Dividir} \)
   - \( \text{JugadorTiene(6, 6)} \land \neg \text{DealerEntre(2, 6)} \Rightarrow \text{Pedir} \)

7. **Suma 8 = Pedir**
   - \( \text{Suma(8)} \Rightarrow \text{Pedir} \)

8. **A-2 o A-3 → Doblar si 2 cartas y dealer = 5 o 6; si no, pedir**
   - \( \text{Mano(A, 2 o 3)} \land \text{DosCartas} \land (\text{DealerMuestra(5)} \lor \text{DealerMuestra(6)}) \Rightarrow \text{Doblar} \)
   - \( \text{Mano(A, 2 o 3)} \land (\neg \text{DosCartas} \lor \neg (\text{DealerMuestra(5)} \lor \text{DealerMuestra(6)})) \Rightarrow \text{Pedir} \)

9. **A-4 o A-5 → Doblar si dealer 4–6 y 2 cartas; si no, pedir**
   - \( \text{Mano(A, 4 o 5)} \land \text{DosCartas} \land \text{DealerEntre(4, 6)} \Rightarrow \text{Doblar} \)
   - Si no, \( \Rightarrow \text{Pedir} \)

10. **A-6 → Doblar si dealer 3–6 y 2 cartas; si no, pedir**
    - \( \text{Mano(A, 6)} \land \text{DosCartas} \land \text{DealerEntre(3, 6)} \Rightarrow \text{Doblar} \)
    - Si no, \( \Rightarrow \text{Pedir} \)

11. **A-7 → Doblar si dealer 3–6 y 2 cartas; pedir si dealer 9–A; si no, plantarse**
    - \( \text{Mano(A, 7)} \land \text{DosCartas} \land \text{DealerEntre(3, 6)} \Rightarrow \text{Doblar} \)
    - \( \text{Mano(A, 7)} \land \text{DealerEntre(9, A)} \Rightarrow \text{Pedir} \)
    - Resto de casos: \( \Rightarrow \text{Plantarse} \)

12. **Suma 9 → Doblar si dealer 3–6 y 2 cartas; si no, pedir**
    - \( \text{Suma(9)} \land \text{DosCartas} \land \text{DealerEntre(3, 6)} \Rightarrow \text{Doblar} \)
    - Si no, \( \Rightarrow \text{Pedir} \)

13. **Suma 10 o 11 → Doblar si dealer 2–9 y 2 cartas; si no, pedir**
    - \( \text{Suma(10 \lor 11)} \land \text{DosCartas} \land \text{DealerEntre(2, 9)} \Rightarrow \text{Doblar} \)
    - Si no, \( \Rightarrow \text{Pedir} \)

14. **Suma 12 → Plantarse si dealer 4–6; si no, pedir**
    - \( \text{Suma(12)} \land \text{DealerEntre(4, 6)} \Rightarrow \text{Plantarse} \)
    - Si no, \( \Rightarrow \text{Pedir} \)

15. **Suma 13–16 → Plantarse si dealer 2–6; si no, pedir**
    - \( \text{SumaEntre(13, 16)} \land \text{DealerEntre(2, 6)} \Rightarrow \text{Plantarse} \)
    - Si no, \( \Rightarrow \text{Pedir} \)

16. **Suma 17–21 → Siempre plantarse**
    - \( \text{SumaEntre(17, 21)} \Rightarrow \text{Plantarse} \)
