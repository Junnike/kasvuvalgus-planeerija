# Kasvuvalguse planeerija

Kasvuvalguse kalkulaator (V3.1, 03.11.2026).

Veebis: https://junnike.github.io/kasvuvalgus-planeerija/

## Jagatav link (V3.16)

Nupp **Kopeeri link** (üleval paremal) kopeerib aadressi, mis avab täpselt sama seadistuse: ruum, kõrgus, peegeldus, valgusti ja selle parameetrid, LED-plaadi koostis, taim/faas, käsitsi paigutatud valgustite asukohad ja aruande väljad. Aadressiriba uueneb iga muudatusega, nii et värskendamine (F5) hoiab seadistuse alles.

Vorming: `#s=<base64url(JSON)>`, JSON `{v:1, f:{välja_id: väärtus}, lay, lamps:[[x,y,rot]], pcb:[[kind,K,cri,n,model]], pl, ps, st, ies}`. `f` hoiab ainult vaikimisi väärtustest erinevaid välju. IES/LDT faili lingis ei ole. Agentidele (Grok, Cursor, Claude): ära nimeta väljade id-sid ümber, siis vanad lingid töötavad edasi; uued väljad lisa lihtsalt juurde.

## V3.17: moodulid ja eri valgustid koos

- Arvuväljad võtavad nii koma kui punkti (1,44 = 1.44). Valgusti mõõdud võivad olla alates 0,1 cm; mm näit kuvatakse kohe.
- Valgustite loendis **Lisa ruudustikuna**: veerud × read, esimese x/y ja vahed. Sobib ka tuhandetele LED-moodulitele.
- **Valgusti tüübid**: salvesta sammu 2 valgusti tüübiks (T1, T2...) ja sega neid ühes arvutuses (nt külgedel T8 korpused, keskel moodulid). Väli = tüüpide väljade summa.
- Hoiatus, kui lm/W > 250 või µmol/J > 4,5.
- Link: `ty` = tüübid, `lamps` võib sisaldada `{g:[x0,y0,dx,dy,C,R,rot,t]}` ruudustikke (lühike link). V3.16 lingid töötavad edasi.
