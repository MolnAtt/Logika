# Szemantika
## Alapelvek és érdekességek
A kijelentéslogika a legegyszerűbb logika, itt mindössze két igazságérték van, és minden kijelentés pontosan az egyikkel rendelkezik. Ezt nevezik a **kétértékűség elvének**. 

Ez két alapvetőbb elv együttes alkalmazása igazából: 
- **Ellentmondástalanság elve**: Egyetlen kijelentés sem lehet egyszerre igaz és hamis.
- **Kizárt harmadik elve**: Minden kijelentés igaz vagy hamis, harmadik lehetőség nincs.

Megjegyezzük, hogy léteznek olyan logikai rendszerek, amelyekben a fenti két elv nem teljesül. Ezek természetesen nem klasszikus logikák: 
- Parakonzisztens logikának nevezik azon rendszereket, amelyekben az ellentmondás elve nem teljesül. Ilyen rendszerekre ott lehet például szükség, amikor egymásnak ellentmondó információk között kell következtetéseket hozni.
- Programozás során is előfordulhatnak olyan helyzetek, amikor kényelmes háromértékű logikához nyúlni: Pl. amikor egy kijelentés sem nem igaz, sem nem hamis, hanem épp nincs meghatározva az igazságértéke, és ezt a meghatározatlanságot egy új igazságértékként kezelni. Ezek az értékréses logikák. 

## Formális szemantika

Az **igaz** és a **hamis** kijelentések alapfogalmak, ezeket nem definiáljuk. Ezeket az egyszerűség kedvéért 1-gyel és 0-val fogjuk jelölni. 

Nagyon fontos, hogy a kijelentések jelentése során nem a valósággal foglalkozunk. Ebben a fejezetben tulajdonképpen lehetséges valóságokkal foglalkozunk. Ezek a lehetséges valóságok/világok döntik el, hogy mely kijelentés igaz vagy hamis. 

**Definíció (értékelés):** Értékelésnek nevezzük azon függvényeket, amelyek az atomi kijelentésekhez igaz illetve hamis értékeket rendelnek. 

Atomi kijelentés igazsága tehát mindig attól függ, hogy milyen értékelés szerint nézzük. 

Ezáltal még nem határoztuk meg, hogy mit jelent egy kijelentés igazságértéke. Egy értékelés mindössze az atomi kijelentések igazságértékét határozza meg. 

**Definíció (Jelentés/igazságérték):** Egy $A$ kijelentés $v$ értékelésén alapuló $|A|_v$-vel jelölt igazságértéke a következő:
- amennyiben $A$ atomi formula, akkor az igazságértéke $v(A)$.
- amennyiben $A$ egy $\lnot B$ alakú formula, akkor $|A|_v$ pontosan akkor igaz, ha $|B|_v$ hamis. 
- amennyiben $A$ egy $(B\land C)$ alakú formula, akkor $|A|_v$ pontosan akkor igaz, ha $|B|_v$ és $|C|_v$ is igaz.  
- amennyiben $A$ egy $(B\lor C)$ alakú formula, akkor $|A|_v$ pontosan akkor hamis, ha $|B|_v$ és $|C|_v$ is hamis.
- amennyiben $A$ egy $(B\to C)$ alakú formula, akkor $|A|_v$ pontosan akkor hamis, ha $|B|_v$ igaz de $|C|_v$ is hamis.
- amennyiben $A$ egy $(B\leftrightarrow C)$ alakú formula, akkor $|A|_v$ pontosan akkor igaz, ha $|B|_v$ és $|C|_v$ igazságértékei megegyeznek.

**Definíció (Következtetés):** **Következtetés** alatt egy formulasorozatot értünk. Az utolsó tagját (amire következtetünk), **konklúziónak** nevezzük, a többi tagját pedig (amiből következtetünk) **premisszáknak** nevezzük.

### Legfontosabb szemantikai fogalmak
- **Definíció (Logikai igazság / tautológia):** Egy formulát **logikai igazságnak** vagy **tautológiának** nevezünk, ha minden lehetséges értékelés mellett igaz.
- **Definíció (Ellentmondás / Kielégíthetetlenség):** Egy formulát **ellentmondásnak** vagy **kielégíthetetlennek** nevezünk, ha minden lehetséges értékelés mellett hamis.
- **Definíció (Helyes következtetés):** Egy következtetést **helyesnek** mondunk, ha bármely értékelés mellett, amely szerint a premisszái igazak, a konklúziója is igaz. 

    Más megfogalmazásban: Helyes egy következtetés, ha nincs olyan értékelés, amely a premisszáit igazzá, a konklúzióját viszont hamissá tenné. 

    Két $A$ és $B$ formula esetén ezt a következőképpen jelöljük:
    
    $$ A\Longrightarrow B$$

    De használatos a következő jelölés is:
    
    $$\begin{array}{r}A\\ \hline \therefore B\end{array}$$

    Ebben az esetben tehát $A$ a premissza és $B$ a konklúzió.

    Több formula esetén, azaz ha pl. az $A$, $B$ és $C$ premisszákból a $D$ következtetéséről beszélünk:
    
    $$ \{A,B,C\}\Longrightarrow D$$
    
    Azaz a premisszák formula**halmazából** következik a $D$. 
    De hosszú és összetett formulák esetén könnyebb írni és áttekinteni a következő jelölést:
    
    $$\begin{array}{r}A\\ B\\ C\\ \hline \therefore D\end{array}$$

- **Definíció (Ekvivalencia):** Két formulát pontosan akkor mondunk ekvivalensnek, ha igazságértékük minden értékelés szerint megegyezik.

    Az ekvivalencia jelölése:

    $$ A\iff B$$
    és 
    $$\begin{array}{r}A\\ \hline\hline B\end{array}$$

