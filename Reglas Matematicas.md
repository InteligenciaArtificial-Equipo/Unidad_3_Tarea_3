### Reglas del Blackjack en Formato Lógico (Modus Ponens)

1. **Seguro contra A del dealer**
   - `DealerMuestra(A) ⇒ ¬PagarSeguro`

2. **Dividir A-A**
   - `JugadorTiene(A, A) ⇒ Dividir`

3. **Dividir 9-9 si dealer tiene 2–5 o 7–8; si no, plantarse**
   - `JugadorTiene(9, 9) ∧ (DealerEntre(2, 5) ∨ DealerEntre(7, 8)) ⇒ Dividir`
   - `JugadorTiene(9, 9) ∧ ¬(DealerEntre(2, 5) ∨ DealerEntre(7, 8)) ⇒ Plantarse`

4. **Dividir 8-8**
   - `JugadorTiene(8, 8) ⇒ Dividir`

5. **Dividir 7-7, 2-2, 3-3 si dealer tiene 2–7; si no, pedir**
   - `(JugadorTiene(2, 2), JugadorTiene(3, 3), JugadorTiene(7, 7)) ∧ DealerEntre(2, 7) ⇒ Dividir`
   - `(JugadorTiene(2, 2), JugadorTiene(3, 3), JugadorTiene(7, 7)) ∧ ¬DealerEntre(2, 7) ⇒ Pedir`

6. **Dividir 6-6 si dealer tiene 2–6; si no, pedir**
   - `JugadorTiene(6, 6) ∧ DealerEntre(2, 6) ⇒ Dividir`
   - `JugadorTiene(6, 6) ∧ ¬DealerEntre(2, 6) ⇒ Pedir`

7. **Suma 8 = Pedir**
   - `Suma(8) ⇒ Pedir`

8. **A-2 o A-3 → Doblar si 2 cartas y dealer = 5 o 6; si no, pedir**
   - `As ∧ DosCartas ∧ (Suma(2) ∨ Suma(3)) ∧ DealerEntre(5, 6) ⇒ Doblar`
   - `As ∧ (Suma(2) ∨ Suma(3)) ∧ (¬DosCartas ∨ ¬DealerEntre(5, 6)) ⇒ Pedir`

9. **A-4 o A-5 → Doblar si dealer 4–6 y 2 cartas; si no, pedir**
   - `As ∧ DosCartas ∧ (Suma(4) ∨ Suma(5)) ∧ DealerEntre(4, 6) ⇒ Doblar`
   - `As ∧ (Suma(4) ∨ Suma(5)) ∧ (¬DosCartas ∨ ¬DealerEntre(4, 6)) ⇒ Pedir`

11. **A-6 → Doblar si dealer 3–6 y 2 cartas; si no, pedir**
    - `As ∧ DosCartas ∧ Suma(6) ∧ DealerEntre(3, 6) ⇒ Doblar`
    - `As ∧ ¬DosCartas ∧ Suma(6) ∧ ¬DealerEntre(3, 6) ⇒ Pedir`

13. **A-7 → Doblar si dealer 3–6 y 2 cartas; pedir si dealer 9–A; si no, plantarse**
    - `As ∧ DosCartas ∧ Suma(7) ∧ DealerEntre(3, 6) ⇒ Doblar`
    - `As ∧ Suma(7) ∧ DealerEntre(9, A) ⇒ Pedir`
    - `As ∧ Suma(7) ∧ DealerEntre(2, 8) ⇒ Plantarse`

15. **Suma 9 → Doblar si dealer 3–6 y 2 cartas; si no, pedir**
    - `Suma(9) ∧ DosCartas ∧ DealerEntre(3, 6) ⇒ Doblar`
    - `Suma(9) ∧ ¬DosCartas ∧ DealerEntre(3, 6) ⇒ Pedir`

16. **Suma 10 o 11 → Doblar si dealer 2–9 y 2 cartas; si no, pedir**
    - `(Suma(10) ∨ Suma(11)) ∧ DosCartas ∧ DealerEntre(2, 9) ⇒ Doblar`
    - `(Suma(10) ∨ Suma(11)) ∧ ¬(DosCartas ∨ DealerEntre(2, 9)) ⇒ Pedir`

17. **Suma 12 → Plantarse si dealer 4–6; si no, pedir**
    - `Suma(12) ∧ DealerEntre(4, 6) ⇒ Plantarse`
    - `Suma(12) ∧ ¬DealerEntre(4, 6) ⇒ Pedir`

18. **Suma 13–16 → Plantarse si dealer 2–6; si no, pedir**
    - `SumaEntre(13, 16) ∧ DealerEntre(2, 6) ⇒ Plantarse`
    - `SumaEntre(13, 16) ∧ ¬DealerEntre(2, 6) ⇒ Pedir`

19. **Suma 17–21 → Siempre plantarse**
    - `SumaEntre(17, 21) ⇒ Plantarse`
