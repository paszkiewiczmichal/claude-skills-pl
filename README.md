# claude-skills-pl

Claude pisze po polsku poprawnie, ale po kilku zdaniach widać, że to tekst z modelu: „odgrywa kluczową rolę”, trzy przymiotniki z rzędu, długi myślnik przeniesiony z angielskiego, „daj znać, jeśli…” na końcu maila. Klient to zauważa. Sędzia też.

Napisałem te trzy skille do własnej pracy w kancelarii. Uczą Claude pisać tak, jak pisze uważny polski autor, a przy umowach, pismach i korespondencji z klientem tak, jak pisze radca prawny.

Michał Paszkiewicz, radca prawny, [kancelariapaszkiewicz.pl](https://kancelariapaszkiewicz.pl)

| Skill | Co robi | Do jakich tekstów |
| --- | --- | --- |
| [`polszczyzna`](skills/polszczyzna) | Buduje naturalne polskie zdania i usuwa znamiona tekstu generowanego przez AI | posty, artykuły, oferty, opisy usług, notatki |
| [`komunikacja-kancelaryjna`](skills/komunikacja-kancelaryjna) | Dobiera ton i układ wiadomości do adresata, pilnuje tajemnicy zawodowej | maile do klienta, zespołu, sądu, urzędu i strony przeciwnej |
| [`legal-style-pl`](skills/legal-style-pl) | Pisze rejestrem prawniczym: precyzyjnie, z terminami zdefiniowanymi, według techniki prawodawczej | umowy, klauzule, regulaminy, pisma procesowe, opinie |

Skille pilnują języka. Nie sprawdzają przepisów, nie oceniają ryzyka i nie zastępują prawnika.

## Jak skill polszczyzna poprawia tekst?

Poprawność to za mało. Tekst ma też nie zdradzać, że pisała go maszyna. Skill pracuje na dwóch poziomach.

**Warsztat** ([`WARSZTAT.md`](skills/polszczyzna/references/WARSZTAT.md)) to zasady budowania dobrego polskiego zdania: spójniki, rejestr, rzeczowniki odczasownikowe, strona bierna, szyk, interpunkcja, konsekwencja w terminologii. Przy każdej regule zaznaczam, czy to norma językowa, czy decyzja redakcyjna, żeby nie mylić preferencji z błędem.

**Katalog wzorców AI** ([`WZORCE_AI.md`](skills/polszczyzna/references/WZORCE_AI.md)) opisuje 33 nawyki tekstu z modelu, każdy z przykładem przed i po. Jest też lista cech ludzkiego pisania, których skill nie ma prawa „poprawiać”.

> **Przed:** W dzisiejszym dynamicznie zmieniającym się świecie sztuczna inteligencja stanowi przełomowe narzędzie, które odgrywa kluczową rolę w transformacji sposobu, w jaki tworzymy treści.
>
> **Po:** Asystenty AI przyspieszają pisanie tekstów szablonowych. Gorzej radzą sobie z oceną, kiedy się mylą.

Skill zna swoje granice. Przy tekście prawniczym wyłącza reguły, które by go zepsuły, na przykład zakaz powtórzeń, bo w umowie termin zdefiniowany powtarza się celowo. Może też dopasować styl do próbki twojego własnego pisania.

## Jak komunikacja-kancelaryjna pisze do klienta, sądu i zespołu?

Mail do klienta, notatka dla współpracownika i pismo do urzędu wymagają trzech różnych rejestrów. Skill rozpoznaje adresata, rodzaj sprawy i pilność, dobiera układ i ton, a przed oddaniem szkicu przechodzi listę kontrolną.

- **Cztery typy klienta:** instytucjonalny, wierzyciel w upadłości lub restrukturyzacji, osoba fizyczna i konsument. Każdy dostaje inny poziom formalności.
- **Kodeks Etyki Radcy Prawnego:** wiadomość mówi o skutkach czynności, a nie tylko o tym, że ją wykonano (art. 44 ust. 1). Prośba o zgodę wyjaśnia skutki, zagrożenia i inne możliwości (art. 5 pkt 9).
- **Pilność:** skill wychwytuje niepokój w wiadomości od klienta i odpowiada na niego w pierwszym zdaniu.
- **Tajemnica zawodowa:** przed wysłaniem sprawdza adresatów, kopie i cytowaną historię wątku.
- **Tylko szkic:** skill niczego nie wysyła sam. Najpierw pokazuje treść do akceptacji.

> **Przed:** Szanowny Panie, w nawiązaniu do naszej rozmowy uprzejmie informuję, że pozew został złożony. Daj znać, jeśli masz pytania!
>
> **Po:** Szanowny Panie, wczoraj złożyłem pozew. Sąd doręczy go pozwanemu i wyznaczy mu termin na odpowiedź. O terminie rozprawy napiszę, gdy tylko sąd go wyznaczy.

Pisma procesowe i treść merytoryczną opinii zostawia skillowi `legal-style-pl`.

## Jak legal-style-pl redaguje umowy i pisma procesowe?

W umowie język ma być jednoznaczny, a nie ładny. Skill włącza rejestr radcy prawnego i pilnuje, żeby postanowienie tworzyło obowiązek, zamiast wyrażać dobre chęci.

- czas teraźniejszy, strona czynna, wskazany podmiot obowiązku,
- jedna myśl w jednym przepisie,
- terminy zdefiniowane używane konsekwentnie, bez synonimów,
- liczby i daty zapisane według konwencji danego dokumentu,
- zakaz sformułowań nieostrych („niezwłocznie”, „odpowiedni”, „rozsądny termin”) wraz z gotowymi zamiennikami,
- jednostki redakcyjne według Zasad Techniki Prawodawczej: `§`, `ust.`, `pkt`, `lit.`,
- wzorce dla umów, maili do klientów, raportów, opinii i pism procesowych,
- lista archaizmów kancelaryjnych i słów typowych dla AI do usunięcia.

> **Przed:** Strony powinny dążyć do polubownego rozwiązania sporów, co pozwoli uniknąć niepotrzebnych kosztów.
>
> **Po:** Strony zobowiązują się do podjęcia negocjacji w terminie 14 dni od dnia doręczenia pisemnego wezwania, przed skierowaniem sprawy na drogę sądową.

Pierwsza wersja wyraża intencję. Druga tworzy obowiązek, którego wykonanie da się sprawdzić.

## Który skill wybrać do danego tekstu?

| Tekst | Skill |
| --- | --- |
| post, artykuł, oferta, opis usługi, notatka | `polszczyzna` |
| mail do klienta, współpracownika, sądu, urzędu | `komunikacja-kancelaryjna` |
| umowa, klauzula, regulamin, pismo procesowe, opinia | `legal-style-pl` |

Skille się uzupełniają. Gdy `polszczyzna` rozpozna tekst prawniczy albo korespondencję kancelaryjną, sama odsyła do właściwego skilla.

## Jak zainstalować skille w Claude Code i Claude.ai?

**Claude Code, jako plugin** (wszystkie trzy skille naraz):

```bash
claude plugin marketplace add paszkiewiczmichal/claude-skills-pl
claude plugin install claude-skills-pl@claude-skills-pl
```

W sesji Claude Code to samo robią `/plugin marketplace add paszkiewiczmichal/claude-skills-pl` i `/plugin install claude-skills-pl@claude-skills-pl`. Skille mają wtedy prefiks pluginu, na przykład `/claude-skills-pl:polszczyzna`.

**Claude Code, ręcznie** (wybrany skill):

```bash
git clone https://github.com/paszkiewiczmichal/claude-skills-pl.git
mkdir -p ~/.claude/skills
cp -r claude-skills-pl/skills/polszczyzna ~/.claude/skills/
```

Kopiuj cały folder skilla, a nie sam `SKILL.md`, bo `polszczyzna` ma jeszcze podfolder `references`.

**Claude.ai:** spakuj folder skilla do `.zip` i wgraj go w ustawieniach, w sekcji Skills.

```bash
cd claude-skills-pl/skills
zip -r polszczyzna.zip polszczyzna
```

## Co się zmieniło w wersji 2.0.0?

**2.0.0.** Usunąłem `humanizer-pl`. Jego zadanie przejął `polszczyzna`, który łączy wykrywanie wzorców AI z warsztatem pisania. Doszedł `komunikacja-kancelaryjna`. `legal-style-pl` nie zależy już od innych skilli. Wszystkie skille mają jednolity frontmatter, licencję MIT i oznaczenie autora.

**1.0.0.** Pierwsze wydanie: `humanizer-pl` i `legal-style-pl`.

## Wdrożenie Claude w kancelarii i dziale prawnym

Te skille powstały przy mojej pracy radcy prawnego i używam ich codziennie. Jeśli chcesz dopasować je do stylu swojej kancelarii albo wdrożyć Claude w pracy z dokumentami, napisz do mnie przez [kancelariapaszkiewicz.pl/kontakt](https://kancelariapaszkiewicz.pl/kontakt).

Przepisy, orzecznictwo i dane z rejestrów, na których tekst prawniczy ma się opierać, daje [Lawtern](https://lawtern.com).

Błąd w skillu albo pomysł na zmianę zgłoś w [Issues](https://github.com/paszkiewiczmichal/claude-skills-pl/issues).

## Źródła

- Poradnia Językowa PWN, Wielki słownik ortograficzny PWN, Nowy słownik poprawnej polszczyzny PWN, rozstrzygnięcia Rady Języka Polskiego.
- Kodeks Etyki Radcy Prawnego (tekst jednolity, uchwała nr 884/XI/2023 Prezydium KRRP) i ustawa z dnia 6 lipca 1982 r. o radcach prawnych.
- Rozporządzenie Prezesa Rady Ministrów z dnia 20 czerwca 2002 r. w sprawie „Zasad techniki prawodawczej”.

## Licencja

[MIT](LICENSE), Copyright (c) 2026 Michał Paszkiewicz.
