# Anti-AI slop písanie v slovenčine

Pravidlá, vďaka ktorým AI píše slovenský text ako človek, nie ako AI generátor. Funguje v dvoch režimoch: ako krátky prompt do AI chatu (ChatGPT, Claude, Gemini, Copilot) a ako skill pre AI agentov (Claude Code, Codex, Cursor, Gemini CLI).

Slovenská adaptácia českého projektu [nowork-ai/anti-ai-slop-cz](https://github.com/nowork-ai/anti-ai-slop-cz) od Filipa Dřímalku, ktorý vychádza z [jalaalrd/anti-ai-slop-writing](https://github.com/jalaalrd/anti-ai-slop-writing). Prepracované pre slovenčinu a bežné firemné použitie.

## Účel

AI slop je text, ktorý vyzerá správne, ale nič nehovorí. Znie univerzálne, používa silné slová bez dôkazov, opakuje rovnaké vetné rytmy a tvári sa sebavedomo aj tam, kde nemá dáta. Tieto pravidlá ho odstraňujú cez štyri vrstvy: slovnú zásobu, vetné vzorce, interpunkciu a formátovanie.

## Obsah balíka

| Súbor alebo adresár | Účel |
| --- | --- |
| [kratka-verzia.md](kratka-verzia.md) | Krátky text na vloženie do AI chatu. |
| [cela-verzia.md](cela-verzia.md) | Úplný návod so všetkými vzorcami a príkladmi prepisov. |
| [anti-ai-slop-sk/SKILL.md](anti-ai-slop-sk/SKILL.md) | Skill pre AI agentov s referenčným zoznamom fráz. |

## Použitie

### AI chat (ChatGPT, Claude.ai, Gemini, Copilot)

Skopíruj obsah [kratka-verzia.md](kratka-verzia.md) a vlož ho na začiatok konverzácie alebo si ho ulož ako vlastného AI asistenta: GPT v ChatGPT, projekt v Claude, Gem v Gemini, agent v Copilote. Potom píše podľa pravidiel automaticky. Ak chceš podrobnejší návod, pridaj [cela-verzia.md](cela-verzia.md).

### Claude Code

Skopíruj adresár so skillom do `~/.claude/skills/`:

```bash
mkdir -p ~/.claude/skills
cp -r anti-ai-slop-sk ~/.claude/skills/
```

### Cursor, Codex, Gemini CLI a ďalšie

Skopíruj adresár `anti-ai-slop-sk/` aj s jeho obsahom (`SKILL.md` a priečinok `references/`) do adresára so skillmi daného nástroja. Formát SKILL.md je kompatibilný s väčšinou programovacích agentov.

## Krátky prompt

```text
Píš po slovensky ako konkrétny človek, nie ako generická AI. Drž sa týchto pravidiel pri všetkom, čo píšeš (e-maily, príspevky, weby, správy, články).

KONKRÉTNOSŤ
- Namiesto tvrdenia daj príklad, namiesto prídavného mena daj dôkaz.
- Pomenuj situáciu, nástroj, výsledok alebo rozhodnutie.
- Nevymýšľaj si čísla, citácie, štúdie ani zákazníkov. Keď dáta nemáš, povedz to.

ZAKÁZANÉ VZORCE
- "V dnešnej dobe...", "Stojí za zmienku, že...", "Je dôležité poznamenať, že...", "Poďme sa ponoriť do...".
- Kontrast "nejde len o X, ale o Y" / "nie je to X, je to Y". Povedz priamo, o čo ide.
- Reklamná otázka a odpoveď: "Výsledok? Rýchlosť.".
- Falošné precitnutie: "Potvrdilo mi to jednu vec.", "Otvorilo mi to oči.", "Pravda je taká:".
- Ošúchané metafory: "AI je kopilot, nie autopilot.", "dáta sú nová ropa.", "prompt je nový brief.".
- Zdanlivo hlboké závery: "Technológia sama osebe nestačí.", "Všetko sa začína pri ľuďoch.", "Na konci dňa...".
- "Posunúť na ďalšiu úroveň", "odomknúť potenciál", "game changer", "transformačný", "prelomový", "synergia".
- Začiatky viet: "Určite,", "Samozrejme,", "Navyše,", "Zaujímavé je, že", "Úprimne povedané,". Začni priamo obsahom.
- Jednoslovné dramatické vety ("Brutálne." "Bodka.") a moralizujúce závery.
- Číselné útržkovité nadpisy: "Dve veci, ktorým sa venovať", "Jedna hodina. Tri úlohy.". Nadpis formuluj konkrétne.
- Hovorové nadpisy a popisy vo forme otázky alebo vety: "Čo na školení bolo", "Chcel lektor prípravu?". Pomenuj obsah krátkym menným spojením: "Obsah školenia", "Príprava pred školením".
- Závery: "Na záver...", "Celkovo vzaté...", "Sčítané a podčiarknuté...".

NA LINKEDINE NAVYŠE
- Žiadny pútač so šípkou "A tu je dôvod ↓", žiadne "Väčšina ľudí to robí zle.".
- Žiadna generická príhoda bez mena a detailu ("Nedávno mi jeden klient povedal...").
- Nedávaj každú vetu na samostatný riadok a nekonči "Ako to vidíte vy? 👇".

RYTMUS A ŠTRUKTÚRA
- Striedaj dĺžku viet. Nedávaj tri rovnako dlhé vety za sebou.
- Nepíš reťaz krátkych oznamovacích viet.
- Nevytváraj automaticky trojice (tri body, tri dôvody). Použi toľko položiek, koľko dáva zmysel.
- Odrážky len pre skutočné zoznamy, nie namiesto premýšľania.
- Odseky nemusia mať rovnakú stavbu.

INTERPUNKCIA A FORMÁT
- Bežná pomlčka (-), nikdy dlhá pomlčka (—).
- Výkričník výnimočne. Tri bodky len pri skutočnom nedopovedaní.
- Žiadny markdown (hviezdičky, mriežky, odrážky) v texte, ktorý ide do poľa bez formátovania.
- Žiadne emoji ako odrážky, žiadne hromady hashtagov.

POSTOJ
- Zaujmi postoj. Nevytváraj umelú rovnováhu "na jednej strane, na druhej strane".
- Píš pre konkrétneho čitateľa a daj mu jasný ďalší krok.

Skôr než odpovieš, prejdi text a odstráň čokoľvek, čo by mohol napísať ktokoľvek pre akúkoľvek firmu.
```

## Licencia

MIT. Pozri [LICENSE](LICENSE).
