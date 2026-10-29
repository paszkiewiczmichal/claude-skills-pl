# claude-skills-pl

Trzy skille dla Claude do pracy z polskim tekstem: codziennym, kancelaryjnym i prawniczym. Każdy działa samodzielnie i ma osobny zakres, więc nie dublują się ani sobie nie przeszkadzają.

Autor: [Michał Paszkiewicz](https://kancelariapaszkiewicz.pl), radca prawny.

## Skille

| Skill | Co robi | Do czego |
| --- | --- | --- |
| [`polszczyzna`](skills/polszczyzna) | Buduje poprawne polskie zdania i usuwa znamiona tekstu generowanego przez AI | posty, artykuły, oferty, opisy usług, notatki |
| [`komunikacja-kancelaryjna`](skills/komunikacja-kancelaryjna) | Dobiera ton i szkielet wiadomości do adresata, pilnuje tajemnicy zawodowej | maile do klienta, do zespołu, do sądu, urzędu i strony przeciwnej |
| [`legal-style-pl`](skills/legal-style-pl) | Narzuca rejestr prawniczy: precyzję, terminy zdefiniowane, technikę prawodawczą | umowy, klauzule, regulaminy, pisma procesowe, opinie, raporty |

Skille pilnują warstwy językowej. Nie weryfikują przepisów, nie analizują ryzyka i nie zastępują oceny prawnika.

## polszczyzna

Dobry polski tekst to nie tylko brak błędów. To także brak odruchów, po których czytelnik poznaje, że pisała maszyna: napuszonego podkreślania wagi, reguły trzech, doczepek w rodzaju „co podkreśla”, długich myślników żywcem z angielskiego i pożegnań typu „daj znać, jeśli”.

Skill ma dwie warstwy:

- **Warsztat** ([`WARSZTAT.md`](skills/polszczyzna/references/WARSZTAT.md)). Jak zbudować dobre polskie zdanie: spójniki przyczynowe, rejestr, rzeczowniki odczasownikowe, strona bierna, szyk, interpunkcja zdania złożonego, konsekwencja terminologiczna. Każda reguła jest oznaczona jako norma albo decyzja redakcyjna, żeby preferencji nie mylić z poprawnością.
- **Katalog wzorców AI** ([`WZORCE_AI.md`](skills/polszczyzna/references/WZORCE_AI.md)). 33 wzorce z przykładami przed i po, wskazówki, czego nie brać za fałszywy alarm, oraz lista oznak ludzkiego pisania, których nie wolno „naprawiać”.

Skill zna też własne granice. W tekstach prawniczych wyłącza reguły, które by je psuły (stronę bierną w opisie stanu prawnego, powtarzanie terminów zdefiniowanych, rozbudowane zdania warunkowe), i odsyła do `legal-style-pl`. Opcjonalnie kalibruje głos do próbki Twojego własnego pisania.

> **Źle:** Wprowadzenie obowiązku oznaczania treści nastąpi z dniem 2 sierpnia, a dokonanie weryfikacji materiałów leży po stronie przedsiębiorcy.
>
> **Dobrze:** Od 2 sierpnia trzeba oznaczać treści, a weryfikuje je przedsiębiorca.

## komunikacja-kancelaryjna

Korespondencja kancelaryjna to trzy różne rejestry: klient, współpracownik, sąd lub urząd. Skill rozpoznaje adresata, typ sprawy i pilność wiadomości, dobiera szkielet i ton, a gotowy draft przepuszcza przez listę kontrolną przed wysłaniem.

- **Klient.** Cztery typy: instytucjonalny, wierzyciel w upadłości lub restrukturyzacji, osoba fizyczna, konsument. Każdy dostaje inny język i inny stopień formalności.
- **Zgodność z Kodeksem Etyki Radcy Prawnego.** Wiadomość informuje o skutkach czynności, a nie tylko o samym fakcie (art. 44 ust. 1). Prośba o zgodę wyjaśnia skutki, zagrożenia i alternatywy (art. 5 pkt 9).
- **Pilność.** Skill wyłapuje sygnały niepokoju w wiadomości przychodzącej i każe odpowiedzieć na nie w pierwszym zdaniu.
- **Tajemnica zawodowa.** Przed wysłaniem sprawdza adresatów, kopie i historię cytowań przy przekazywaniu wątku.
- **Draft do akceptacji.** Skill nie jest autopilotem i niczego nie wysyła bez pokazania treści.

> „Proszę o sprawdzenie klauzuli kary umownej w załączonym projekcie. Potrzebuję tego do jutra rana, klient czeka na odpowiedź.”
>
> Wiadomość do współpracownika: priorytet i termin podane wprost, bez rozgrzewki.

Skill nie służy do pism procesowych jako dokumentów formalnych ani do merytorycznej treści opinii prawnej. Od tego jest `legal-style-pl`.

## legal-style-pl

W umowie język ma być jednoznaczny, a nie ładny. Skill włącza rejestr zawodowy radcy prawnego jako tryb pisania i pilnuje, żeby postanowienie tworzyło obowiązek, a nie tylko wyrażało intencję.

- Czas teraźniejszy, strona czynna, wyraźny podmiot.
- Jedna myśl w jednym przepisie.
- Terminy zdefiniowane używane konsekwentnie, bez synonimów.
- Liczby i daty zapisane zgodnie z konwencją dla danego typu dokumentu.
- Zakaz sformułowań nieokreślonych („niezwłocznie”, „odpowiedni”, „rozsądny termin”) wraz z gotowymi zamiennikami.
- Hierarchia redakcyjna według Zasad Techniki Prawodawczej: `§`, `ust.`, `pkt`, `lit.`.
- Wzorce dla umów, maili do klientów, raportów i opinii oraz pism procesowych.
- Lista archaizmów kancelaryjnych i słów typowych dla AI do wycięcia.

> **Źle:** Strony powinny dążyć do polubownego rozwiązania sporów, co pozwoli uniknąć niepotrzebnych kosztów.
>
> **Dobrze:** Strony zobowiązują się do podjęcia negocjacji w terminie 14 dni od dnia doręczenia pisemnego wezwania, przed skierowaniem sprawy na drogę sądową.

Pierwsza wersja wyraża intencję. Druga tworzy obowiązek.

## Który skill wybrać

| Piszesz | Skill |
| --- | --- |
| post, artykuł, ofertę, opis usługi, notatkę | `polszczyzna` |
| mail do klienta, współpracownika, sądu, urzędu | `komunikacja-kancelaryjna` |
| umowę, klauzulę, regulamin, pismo procesowe, opinię | `legal-style-pl` |

Gdy tekst przecina kategorie, skille się uzupełniają. `polszczyzna` sama odsyła do pozostałych dwóch, gdy rozpozna rejestr prawniczy albo korespondencję kancelaryjną.

## Instalacja

**Claude Code, jako plugin** (wszystkie trzy skille naraz):

```bash
claude plugin marketplace add paszkiewiczmichal/claude-skills-pl
claude plugin install claude-skills-pl@claude-skills-pl
```

To samo w sesji: `/plugin marketplace add paszkiewiczmichal/claude-skills-pl`, potem `/plugin install claude-skills-pl@claude-skills-pl`. Skille pojawiają się z prefiksem pluginu, na przykład `/claude-skills-pl:polszczyzna`.

**Claude Code, ręcznie** (jeden skill albo wybrane):

```bash
git clone https://github.com/paszkiewiczmichal/claude-skills-pl.git
mkdir -p ~/.claude/skills
cp -r claude-skills-pl/skills/polszczyzna ~/.claude/skills/
```

Kopiuj cały folder skilla, nie sam plik `SKILL.md`: `polszczyzna` ma jeszcze podfolder `references`.

**Claude.ai.** Skille wgrywa się jako plik `.zip` z folderem skilla, w ustawieniach, w sekcji Skills:

```bash
cd claude-skills-pl/skills
zip -r polszczyzna.zip polszczyzna
```

## Struktura repozytorium

```
claude-skills-pl/
├── .claude-plugin/
│   ├── plugin.json
│   └── marketplace.json
├── skills/
│   ├── polszczyzna/
│   │   ├── SKILL.md
│   │   └── references/
│   │       ├── WARSZTAT.md
│   │       └── WZORCE_AI.md
│   ├── komunikacja-kancelaryjna/
│   │   └── SKILL.md
│   └── legal-style-pl/
│       └── SKILL.md
├── LICENSE
├── NOTICE
└── README.md
```

## Historia zmian

**2.0.0.** Usunięto `humanizer-pl`. Wykrywanie i usuwanie znamion tekstu AI przejął `polszczyzna`, który łączy je z warstwą warsztatową. Dodano `komunikacja-kancelaryjna`. `legal-style-pl` nie zależy już od żadnego innego skilla. Wszystkie skille mają jednolity frontmatter, licencję MIT i oznaczenie autora.

**1.0.0.** Pierwsze wydanie: `humanizer-pl` i `legal-style-pl`.

## Źródła

- Poradnia Językowa PWN, Wielki słownik ortograficzny PWN, Nowy słownik poprawnej polszczyzny PWN, rozstrzygnięcia Rady Języka Polskiego.
- Kodeks Etyki Radcy Prawnego (tekst jednolity, uchwała nr 884/XI/2023 Prezydium KRRP) i ustawa z 6 lipca 1982 r. o radcach prawnych.
- Rozporządzenie Prezesa Rady Ministrów z 20 czerwca 2002 r. w sprawie Zasad Techniki Prawodawczej.
- Katalog wzorców AI w `polszczyzna` jest polską adaptacją listy wzorców ze skilla [humanizer](https://github.com/blader/humanizer) (Siqi Chen, MIT), opartej na stronie Wikipedii „Signs of AI writing” (WikiProject AI Cleanup). Pełna nota: [`NOTICE`](NOTICE).

## Licencja

[MIT](LICENSE), Copyright (c) 2026 Michał Paszkiewicz. Noty dla materiału pochodnego: [`NOTICE`](NOTICE).
