---
name: komunikacja-kancelaryjna
description: "Wspiera pisanie i redagowanie wiadomości kancelaryjnych - do klienta, wewnątrz zespołu współpracowników oraz do sądu/urzędu/strony przeciwnej - dobierając ton, szkielet i rejestr językowy do adresata, typu sprawy i pilności, z pilnowaniem tajemnicy zawodowej. Działa samodzielnie, bez potrzeby dodatkowych skilli językowych."
license: MIT
metadata:
  author: Michał Paszkiewicz
  version: "1.0.0"
---

# Komunikacja kancelaryjna

Uniwersalny, samodzielny skill do pisania wiadomości związanych z pracą kancelarii prawnej - nie tylko do klienta. Spora część korespondencji związanej ze sprawą to nie kontakt z klientem, tylko komunikacja wewnętrzna (między prawnikami/współpracownikami kancelarii) albo z sądem/urzędem/pełnomocnikiem strony przeciwnej - i każda z tych trzech grup wymaga innego rejestru językowego. Oparty na Kodeksie Etyki Radcy Prawnego (KERP, tekst jednolity - uchwała nr 884/XI/2023 Prezydium KRRP), który normuje obowiązki informacyjne wobec klienta i tajemnicę zawodową dotyczącą każdej korespondencji związanej ze sprawą, oraz na zasadach poprawnej polszczyzny i polskiego rejestru prawniczego. Wszystkie potrzebne reguły językowe są wbudowane poniżej - skill nie wymaga ładowania żadnego innego skilla.

Nie generuj całych wiadomości od zera bez kontekstu sprawy - ten skill to checklista i dobór tonu, nie autopilot. Zawsze pokaż draft do akceptacji przed wysłaniem, zgodnie z zasadą „nie wysyłamy niczego bez pokazania treści do zaakceptowania”.

## Kiedy używać

- Redagowanie maila do klienta.
- Redagowanie maila do współpracownika w kancelarii (przekazanie zadania, prośba o sprawdzenie, aktualizacja statusu sprawy).
- Redagowanie maila do sądu, urzędu, syndyka/nadzorcy, pełnomocnika strony przeciwnej.
- Przegląd gotowego draftu przed wysłaniem (checklista w sekcji 7).

Nie używaj do pism procesowych jako dokumentu formalnego (to inna forma niż mail, z własną strukturą z KPC) ani do treści merytorycznej opinii prawnej.

## 1. Rozpoznaj adresata - trzy różne rejestry

| Adresat | Charakter | Rejestr językowy |
|---|---|---|
| **Klient** | Zależy od typu sprawy - patrz sekcja 2 | Dopasowany do typu klienta |
| **Współpracownik w kancelarii** | Zna kontekst sprawy, priorytet to szybkość i jasność | Bezpośredni, bez zbędnego formalizmu (powitanie/podpis można skrócić), ale **priorytet i termin zawsze jawne wprost** - dobry wzorzec to „Proszę o sprawdzenie X - potrzebuję tego do jutra rana”, zły to prośba bez wskazania, na kiedy i dlaczego |
| **Sąd / urząd / syndyk / nadzorca / pełnomocnik strony przeciwnej** | Komunikacja formalna, często quasi-procesowa | Formalny, precyzyjny, z powołaniem sygnatury akt i podstawy umocowania (pełnomocnictwa) przy pierwszym kontakcie w sprawie, bez żadnego elementu emocjonalnego czy potocznego |

## 2. Klient - rozpoznaj typ sprawy

Ton i oczekiwania klienta różnią się mocno w zależności od typu sprawy:

| Typ sprawy | Charakter klienta | Rejestr językowy |
|---|---|---|
| Klient instytucjonalny/korporacyjny (spółka, urząd, fundacja - obsługa bieżąca, zamówienia, KIO) | Osoba kontaktowa działa w imieniu organizacji, oczekuje konkretu biznesowego | Rzeczowy, ryzyko nazwane wprost w kategoriach biznesowych (kara umowna, korekta finansowa), bez owijania w bawełnę, ale i bez czystego żargonu |
| Wierzyciel instytucjonalny w upadłości/restrukturyzacji (np. instytucja finansowa) | Zna procedurę, oczekuje precyzji proceduralnej | Formalny, dokładne sygnatury i terminy, mniej przestrzeni na empatię |
| Osoba fizyczna - sprawa indywidualna (rodzinna, majątkowa, spadkowa) | Często emocjonalnie zaangażowana | Empatyczny, z wyraźnym potwierdzeniem odbioru wrażliwych materiałów i jasną informacją co się z nimi dalej dzieje |
| Konsument w sporze bankowym/frankowym | Zwykle mniej biegły prawniczo, czeka długo na rozstrzygnięcie | Prosty język, tłumaczyć żargon, jasno komunikować co oznacza dany etap |

## 3. Rozpoznaj nastrój i pilność w wiadomości przychodzącej

Dotyczy głównie klientów, ale sygnały pilności warto rozpoznawać też wewnętrznie:

- słowa: „pilne”, „pilnie”, „ASAP”, „natychmiast”, „od tygodni bez odpowiedzi”, „nie rozumiem, dlaczego”
- wielokrotne wykrzykniki, WIELKIE LITERY
- opis sytuacji jako błędu/awarii blokującej termin
- ton spadający z rosnącą frustracją w kolejnych mailach tego samego wątku

Gdy wykryjesz taki sygnał od klienta: odpowiedź MUSI zaadresować niepokój w pierwszym zdaniu, zanim przejdzie do szczegółów proceduralnych. Przy współpracowniku - potwierdź priorytet i realny czas realizacji od razu, nie dopiero na końcu odpowiedzi.

## 4. Szkielet wiadomości

### Do klienta (zgodny z KERP)

Warto zadbać o pełny szkielet, zwłaszcza w pierwszej wiadomości nowego wątku:

1. Powitanie dopasowane do relacji.
2. Uspokojenie, jeśli trzeba (sekcja 3) - jedno zdanie.
3. Kontekst i cel maila - jednym zdaniem, bez rozgrzewki.
4. Sedno sprawy - meritum od razu, bez wstępu.
5. **Skutki czynności, nie tylko fakt** - art. 44 ust. 1 KERP wymaga informowania nie tylko „co zrobiono”, ale też jakie to ma konsekwencje. Sam fakt bez wyjaśnienia skutku nie wystarcza.
6. **Przy prośbie o zgodę** - zgodnie z art. 5 pkt 9 KERP wyjaśnij: na czym polega działanie/zaniechanie, jego skutki, zagrożenia, dostępne alternatywy (i które zostaną wykluczone). Nie proś o „OK?” bez tego kontekstu.
7. Następny krok z konkretnym terminem - kto co robi i do kiedy.
8. Zakończenie z podpisem - bez deklaracji typu „mam nadzieję, że pomogłem” czy „daj znać, jeśli”; kończ konkretem.

### Do współpracownika w kancelarii

1. Krótkie powitanie/zwrot (może być nieformalny, jeśli tak jest przyjęte w zespole).
2. Sygnatura sprawy/nazwa klienta, jeśli wątek nie jest oczywisty z kontekstu.
3. Konkretna prośba lub informacja - jedno zadanie na wiadomość, jeśli to możliwe.
4. **Priorytet i termin wprost** („potrzebuję do jutra rana”, „nie pali się, można w tym tygodniu”).
5. Jeśli przekazujesz zadanie dalej - upewnij się, że odbiorca ma dostęp do akt/kontekstu, którego potrzebuje.

### Do sądu / urzędu / syndyka / strony przeciwnej

1. Powołanie podstawy umocowania („działając w imieniu [klient] na podstawie pełnomocnictwa...”) przy pierwszym kontakcie w sprawie.
2. Sygnatura akt / numer postępowania wprost w pierwszym zdaniu lub temacie.
3. Rzeczowa treść, bez elementu emocjonalnego, bez zbytniej nieformalności.
4. Jasne wskazanie, o co wnosisz / czego dotyczy pismo, i ewentualny termin.
5. Podpis z pełnymi danymi kancelarii.

## 5. Rejestr językowy - zasady obowiązujące w każdej wiadomości

Te zasady stosuj niezależnie od adresata. Poprawiają precyzję i naturalność języka, nie tylko „styl”.

**Archaizmy kancelaryjne - zastępuj naturalnym słowem:**

| Unikaj | Użyj zamiast |
|---|---|
| albowiem | bo / ponieważ |
| aczkolwiek | chociaż / mimo że |
| atoli, wszelako | jednak / ale |
| ergo | zatem |
| iż | że |
| li tylko | tylko |
| niemniej jednak | jednak |
| niniejszym | (usuń - zacznij od treści) |
| przedmiotowy | (usuń lub nazwij konkretnie) |
| tegoż | tego |
| tudzież | i / oraz |
| uprzejmie informuję, iż | (usuń - przejdź do treści) |
| zaś | a / natomiast |

**Zwroty grzecznościowe do usunięcia z końcówek maili:** „Niniejszym pozwalam sobie”, „W załączeniu przekazuję uprzejmie”, „Licząc na przychylne rozpatrzenie”, „Mam nadzieję, że to pomoże”, „Daj znać, jeśli”. Zakończenie maila to konkret (co dalej, kto, do kiedy), nie deklaracja gotowości.

**Słownictwo „AI-generyczne” - unikaj:** „kluczowy” (użyj: istotny / zasadniczy), „fundamentalny” (podstawowy), „holistyczny” (opisz konkretnie), „warto zauważyć” / „należy podkreślić” (wytnij, przejdź do treści), „w świetle powyższego” (zatem / w konsekwencji), „dedykowany” (przeznaczony), „w oparciu o” (na podstawie), „procesować” (przetwarzać / rozpatrywać), oraz ogólnie: „niezwykle”, „wszechstronny”, „dynamiczny”, „innowacyjny”, „odgrywa kluczową rolę”.

**Interpunkcja i zapis:**
- Nie używaj myślnika (—) ani półpauzy (–) w funkcji interpunkcyjnej w zdaniu - zastępuj kropką (nowe zdanie), przecinkiem, dwukropkiem albo nawiasem. Dywiz (-) zamiast myślnika, zawsze.
- Cudzysłów polski „...” (dolny-górny), nie angielski "..." ani “...” - ważne zwłaszcza przy powoływaniu się na tytuł dokumentu lub cytat z przepisu.
- Nagłówki i tematy maili bez Title Case - wielką literą tylko pierwsze słowo i nazwy własne.
- Bez emoji. Pogrubienia tylko funkcjonalnie (np. termin, kwota), nie do „podkreślenia ważności” zdania.
- Liczby: w mailach do klienta/współpracownika - cyfrą („kara wynosi 500 zł”); w pismach formalnych do sądu/urzędu, przy kwotach spornych - słownie i cyfrą („pięciuset złotych (500 zł)”).
- Daty: w mailach np. „30.06.2026”; w pismach formalnych „do dnia 30 czerwca 2026 roku”.

**Wyjątek - cytaty z przepisów i terminy zdefiniowane:** jeśli fragment jest dosłownym cytatem przepisu albo terminem zdefiniowanym w umowie/regulaminie, zostaw go w oryginalnym brzmieniu, nawet jeśli zawiera archaizm - nie parafrazuj treści normatywnej.

## 6. Tajemnica zawodowa - dotyczy każdej wiadomości, nie tylko do klienta

Zgodnie z art. 15 i 23 KERP oraz art. 3 ustawy o radcach prawnych, tajemnica zawodowa obejmuje całą korespondencję związaną ze sprawą i jest bezwzględna, nieograniczona w czasie - również przy przekazywaniu spraw wewnątrz kancelarii. Przed wysłaniem sprawdź:

- Czy każdy adresat i każde CC (klient, współpracownik, sąd) ma faktyczne prawo widzieć tę treść?
- Przy przekazywaniu (Fwd) wątku wewnątrz zespołu - czy nie ciągniesz historii cytowań zawierającej dane, których odbiorca (np. asystent, aplikant) nie powinien widzieć bez potrzeby?
- Czy wybrany kanał jest adekwatny do wrażliwości sprawy?

## 7. Checklista przed wysłaniem

- [ ] Rozpoznany typ adresata (klient / współpracownik / sąd-urząd-strona przeciwna) i dobrany rejestr
- [ ] Powitanie i podpis na miejscu tam, gdzie potrzebne (zwłaszcza pierwszy mail w wątku do klienta lub sądu)
- [ ] Jeśli klient/współpracownik był zaniepokojony lub pytał o priorytet - odpowiedź adresuje to w pierwszym zdaniu
- [ ] Skutki czynności wyjaśnione klientowi, nie tylko sam fakt
- [ ] Przy prośbie o zgodę klienta - skutki, zagrożenia, alternatywy wyjaśnione (art. 5 pkt 9 KERP)
- [ ] Następny krok/zadanie ma konkretny termin
- [ ] Krąg odbiorców/CC właściwy, historia cytowań nie ciągnie zbędnych treści
- [ ] Przy piśmie do sądu/urzędu - sygnatura i podstawa umocowania są wskazane
- [ ] Brak archaizmów kancelaryjnych i słownictwa AI-generycznego z sekcji 5
- [ ] Brak myślnika/półpauzy w funkcji interpunkcyjnej, cudzysłów polski, bez Title Case, bez emoji
- [ ] Liczby i daty zapisane zgodnie z konwencją dla danego typu pisma (mail vs pismo formalne)

## 8. Przykłady ilustracyjne

**Do klienta, dobrze - ryzyko nazwane wprost, w języku biznesowym:**
> „W naszej ocenie takie ujęcie zapisu może zostać zakwestionowane jako niezgodne z przepisami. Rekomendujemy zmianę treści przed podpisaniem.”

**Do klienta, do poprawy - szablon bez kontekstu i z kancelaryjnym wtrętem:**
> „Dzień dobry, w załączniku przesyłam uprzejmie fakturę nr [NR]. Pozdrawiam.” - brakuje kontekstu i informacji, co dalej, a „uprzejmie” nic nie wnosi.

**Wewnętrznie, dobrze - priorytet i termin wprost:**
> „Proszę o sprawdzenie klauzuli kary umownej w załączonym projekcie. Potrzebuję tego do jutra rana, klient czeka na odpowiedź.”

**Do sądu/urzędu, dobrze - rzeczowe pismo z terminem:**
> „Działając w imieniu [klient] na podstawie załączonego pełnomocnictwa, wnoszę o [...] w terminie 7 (siedmiu) dni od doręczenia niniejszego pisma.”

## Źródła

- Kodeks Etyki Radcy Prawnego, tekst jednolity - uchwała nr 884/XI/2023 Prezydium KRRP z 7.02.2023 (art. 5 pkt 9, art. 6, art. 8, art. 12, art. 15, art. 23, art. 36, art. 43, art. 44)
- Ustawa z 6 lipca 1982 r. o radcach prawnych, art. 3 (tajemnica zawodowa)
- Zasady poprawnej polszczyzny (Poradnia Językowa PWN, Nowy słownik poprawnej polszczyzny PWN) i polskiego rejestru prawniczego (Rozporządzenie Prezesa RM z 20.06.2002 r. w sprawie Zasad Techniki Prawodawczej) - jako podstawa wbudowanych reguł językowych w sekcji 5

## Autor i licencja

Autor: Michał Paszkiewicz, radca prawny. Kancelaria Radcy Prawnego Michał Paszkiewicz ([kancelariapaszkiewicz.pl](https://kancelariapaszkiewicz.pl)), Lawtern ([lawtern.com](https://lawtern.com)).

Licencja: MIT. Wolno kopiować, zmieniać i dalej udostępniać, pod warunkiem zachowania informacji o autorze i noty licencyjnej (plik `LICENSE` w repozytorium [claude-skills-pl](https://github.com/paszkiewiczmichal/claude-skills-pl)).
