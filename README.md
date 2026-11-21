# Kasvuvalguse planeerija

Kasvuvalguse kalkulaator (V3.1, 03.11.2026).

Veebis: https://junnike.github.io/kasvuvalgus-planeerija/

## Jagatav link (V3.16)

Nupp **Kopeeri link** (üleval paremal) kopeerib aadressi, mis avab täpselt sama seadistuse: ruum, kõrgus, peegeldus, valgusti ja selle parameetrid, LED-plaadi koostis, taim/faas, käsitsi paigutatud valgustite asukohad ja aruande väljad. Aadressiriba uueneb iga muudatusega, nii et värskendamine (F5) hoiab seadistuse alles.

Vorming: `#s=<base64url(JSON)>`, JSON `{v:1, f:{välja_id: väärtus}, lay, lamps:[[x,y,rot]], pcb:[[kind,K,cri,n,model]], pl, ps, st, ies}`. `f` hoiab ainult vaikimisi väärtustest erinevaid välju. IES/LDT faili lingis ei ole. Agentidele (Grok, Cursor, Claude): ära nimeta väljade id-sid ümber, siis vanad lingid töötavad edasi; uued väljad lisa lihtsalt juurde.
