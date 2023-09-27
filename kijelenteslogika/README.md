# Klasszikus kijelentéslogika

Minden formális nyelv kapcsán két szempontot vizsgálunk: 
- [**Szintaxis**](kijelenteslogika/szintaxis/): Mely formális kifejezések alkotják a nyelv elemeit? 
    Például a logika nyelvének nem része a hatványozás jele, de része a tagadás $\lnot$ jele.
- [**Szemantika**](kijelenteslogika/szemantika/): A formális kifejezések mit jelentenek? Például a logika szemantikájában a betűk igazságértékeket (igaz vagy hamis) jelölnek, míg a számok nyelvében a betűk számokat jelölnek. 

A logika központi feladata mindig az, hogy meghatározza a helyes következtetés fogalmát. Ezt a klasszikus kijelentéslogikában a szintaxis és a szemantika területén is meg lehet tenni. Mi ebben a jegyzetben most csak a szemantikai definíciót adjuk meg, lévén hogy csak középiskolásoknak szól a jegyzet. 

Viszont a logika feladata az is, hogy ha lehetséges, akkor egy következtetés helyességének eldöntését is leírja. Azaz adjon olyan eljárást/algoritmust, amellyel -- ha lehet -- véges időn belül ki lehessen deríteni, hogy egy következtetés helyes-e vagy sem.

Erre két módszert mutatunk meg: 
- [Igazságtáblázatok módszere](kijelenteslogika/igazsatablazatok/): Felírjük az összes lehetséges értékelést és ellenőrizzük a definíciókat.
- [Analitikus fák módszere:](kijelenteslogika/analitikus_fak/) Egy indirekt érvelésen keresztül az esetszétválasztást algoritmizáljuk.
