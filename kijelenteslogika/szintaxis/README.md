# Szintaxis
## A kijelentések definíciója

A $p$, $q$, $r$, ... betűket használjuk az **atomi** vagy más néven **elemi kijelentések** jelölésére.

A következő műveleteket használjuk az összetett kijelentések létrehozására: 
- $\lnot$: "Nem igaz, hogy [...]", egyváltozós művelet, a neve **negáció**.
- $\land$: "[...] és [...]", kétváltozós művelet, a neve **konjunkció**.
- $\lor$: "[...] vagy [...]", kétváltozós művelet, a neve **diszjunkció**.
- $\to$: "ha [...], akkor [...]", kétváltozós művelet, a neve **kondicionális** vagy **implikáció**
- $\leftrightarrow$: "akkor és csak akkor [...], ha [...]", kétváltozós művelet, a neve **bikondicionális**. (Mások hívják ekvivalenciának is, de ezt a szót mi másra használjuk. Másoknál ez a kifejezés kétértelmű, és ezt akarjuk elkerülni.)

**Definíció (Kijelentés):** 
- Minden *atomi kijelentés* **kijelentés** is egyben. 
- Ha $A$ és $B$ **kijelentések**, akkor 
    - $\lnot A$ is **kijelentés**,
    - $(A\land B)$ is **kijelentés**,
    - $(A\lor B)$ is **kijelentés**,
    - $(A\to B)$ is **kijelentés**,
    - $(A\leftrightarrow B)$ is **kijelentés**,
- Mást nem tekintünk **kijelentésnek**.

A fentieket röviden így szokták összefoglalni: 
$$ A ::= \quad p \quad |\quad  \lnot A \quad |\quad A\land B \quad |\quad A\lor B \quad |\quad A\to B\quad |\quad A\leftrightarrow B $$

Ezt az utóbbi rövidítést egyébként Backus-Naur formának (BNF) nevezik.