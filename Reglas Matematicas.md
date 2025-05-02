### Reglas del Blackjack en Formato Lógico (Modus Ponens)

1. **Seguro contra A del dealer**
   - `DealerMuestra(A) ⇒ ¬PagarSeguro`

2. **Dividir A-A**
   - `JugadorTiene(A, A) ⇒ Dividir`

3. **Dividir 9-9 si dealer tiene 2–5 o 7–8; si no, plantarse**
   - `JugadorTiene(9, 9) ∧ DealerEntre(2, 5) ∨ DealerEntre(7, 8) ⇒ Dividir`
   - `JugadorTiene(9, 9) ∧ ¬(DealerEntre(2, 5) ∨ DealerEntre(7, 8)) ⇒ Plantarse`

4. **Dividir 8-8**
   - `JugadorTiene(8, 8) ⇒ Dividir`

5. **Dividir 7-7, 2-2, 3-3 si dealer tiene 2–7; si no, pedir**
   - `JugadorTiene(7, 7) ∧ DealerEntre(2, 7) ⇒ Dividir`
   - `JugadorTiene(7, 7) ∧ ¬DealerEntre(2, 7) ⇒ Pedir`
   - *(igual para 2-2 y 3-3)*

6. **Dividir 6-6 si dealer tiene 2–6; si no, pedir**
   - `JugadorTiene(6, 6) ∧ DealerEntre(2, 6) ⇒ Dividir`
   - `JugadorTiene(6, 6) ∧ ¬DealerEntre(2, 6) ⇒ Pedir`

7. **Suma 8 = Pedir**
   - `Suma(8) ⇒ Pedir`

8. **A-2 o A-3 → Doblar si 2 cartas y dealer = 5 o 6; si no, pedir**
   - `Mano(A, 2 o 3) ∧ DosCartas ∧ (DealerMuestra(5) ∨ DealerMuestra(6)) ⇒ Doblar`
   - `Mano(A, 2 o 3) ∧ (¬DosCartas ∨ ¬(DealerMuestra(5) ∨ DealerMuestra(6))) ⇒ Pedir`

9. **A-4 o A-5 → Doblar si dealer 4–6 y 2 cartas; si no, pedir**
   - `Mano(A, 4 o 5) ∧ DosCartas ∧ DealerEntre(4, 6) ⇒ Doblar`
   - Si no, ⇒ `Pedir`

10. **A-6 → Doblar si dealer 3–6 y 2 cartas; si no, pedir**
    - `Mano(A, 6) ∧ DosCartas ∧ DealerEntre(3, 6) ⇒ Doblar`
    - Si no, ⇒ `Pedir`

11. **A-7 → Doblar si dealer 3–6 y 2 cartas; pedir si dealer 9–A; si no, plantarse**
    - `Mano(A, 7) ∧ DosCartas ∧ DealerEntre(3, 6) ⇒ Doblar`
    - `Mano(A, 7) ∧ DealerEntre(9, A) ⇒ Pedir`
    - Resto de casos: ⇒ `Plantarse`

12. **Suma 9 → Doblar si dealer 3–6 y 2 cartas; si no, pedir**
    - `Suma(9) ∧ DosCartas ∧ DealerEntre(3, 6) ⇒ Doblar`
    - Si no, ⇒ `Pedir`

13. **Suma 10 o 11 → Doblar si dealer 2–9 y 2 cartas; si no, pedir**
    - `Suma(10 ∨ 11) ∧ DosCartas ∧ DealerEntre(2, 9) ⇒ Doblar`
    - Si no, ⇒ `Pedir`

14. **Suma 12 → Plantarse si dealer 4–6; si no, pedir**
    - `Suma(12) ∧ DealerEntre(4, 6) ⇒ Plantarse`
    - Si no, ⇒ `Pedir`

15. **Suma 13–16 → Plantarse si dealer 2–6; si no, pedir**
    - `SumaEntre(13, 16) ∧ DealerEntre(2, 6) ⇒ Plantarse`
    - Si no, ⇒ `Pedir`

16. **Suma 17–21 → Siempre plantarse**
    - `SumaEntre(17, 21) ⇒ Plantarse`
