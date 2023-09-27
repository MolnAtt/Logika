# Igazságtáblázatok módszere

A módszer a következő: A vizsgálandó formulában véges sok atomi formula szerepelhet. Legyen a formulában szereplő különböző atomi formulák száma $n$.

1. Létrehozunk egy $n$ oszlopból és $2^n$ sorból álló táblázatot.
2. Az oszlopokba felírjuk a formulában található atomi formulákat
3. Az összes lehetséges értékelést felírjuk a táblázat első sora fölé, ami különbözhet a felírt formulák tekintetében. 

    Mivel mindegyik formula igaz vagy hamis lehet, mindegyik formula kapcsán 2 választási lehetőségünk van. Így $\underbrace{2\cdot2\cdot\dots}_{n\textup{ db}}$ lehetőségünk van, ami $2^n$. Ezért van ennyi sora az igazságtáblázatnak.

4. Ezt követően újabb és újabb oszlopokat illesztünk a táblázathoz, amikben sorra vesszük a részformulákat és a logikai műveletek szabályai szerint kitöltjük az igazságértékeiket mindegyik sorban.
5. A legnagyobb részformula maga a formula/formulák lesznek, amelyeket vizsgálunk. Az eljárás végén a kérdéstől levonhatjuk a következtetéseket:

    - **Logikai igazság-e?** A vizsgált formula pontosan akkor logikai igazság vagy tautológia, ha az oszlopában csak igaz igazságértékek szerepelnek. 
    - **Ellentmondás-e?** a vizsgált formula pontosan akkor ellentmondás, ha az oszlopában csak és kizárólag hamis igazságértékek szerepelnek.
    - **Helyes következtetés-e?** Egy következtetés pontosan akkor helyes, ha az igazságtáblázat minden olyan sorában, ahol a premisszák igazak, a konklúzió is igaz. 

        Vagy más szóval: Ha nem találni olyan sort az igazságtáblázatban, ahol a premisszák igazak, de a konklúzió hamis.
    - **Ekvivalensek-e?** Két kijelentés pontosan akkor ekvivalens, ha az igazságtáblázatban mindkét formula alatt sorról sorra megegyeznek az igazságértékek.

## Példák