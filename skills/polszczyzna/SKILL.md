---
name: polszczyzna
description: "Pisze i redaguje polski tekst nieprawniczy (posty, artykuły, oferty, notatki) i usuwa z niego znamiona tekstu generowanego przez AI. Używaj zawsze przed oddaniem takiego tekstu, także krótkiego. Teksty prawne: legal-style-pl. Wiadomości do klientów, współpracowników, sądu i urzędu: komunikacja-kancelaryjna."
license: MIT
metadata:
  author: Michał Paszkiewicz
  version: "1.0.0"
---

# Polszczyzna: pisanie i redakcja tekstu po polsku

Ten skill łączy dwie warstwy: warsztatową (jak zbudować dobre polskie zdanie, niezależnie od gatunku) i detekcyjną (jak wykryć i usunąć znamiona tekstu generowanego przez AI po polsku). Razem dają jeden proces pisania i redakcji, zamiast dwóch osobnych przebiegów.

## Twoje zadanie

Gdy piszesz tekst od zera albo dostajesz go do redakcji:

1. **Zbuduj zdania warsztatowo** - stosuj regułki z `references/WARSZTAT.md` (rejestr, spójniki, strona czynna, szyk, interpunkcja, terminologia).
2. **Zidentyfikuj wzorce AI** - przeskanuj tekst pod kątem katalogu w `references/WZORCE_AI.md`.
3. **Przepisuj, nie usuwaj** - zastępuj sztuczne albo urzędnicze sformułowania naturalnymi i pokryj wszystko, co pokrywał oryginał. Jeśli oryginał ma pięć akapitów, przepisana wersja ma pięć akapitów.
4. **Zachowaj sens** - nie gub głównego przekazu.
5. **Dopasuj rejestr** - trzymaj się zamierzonego tonu (formalny, swobodny, techniczny). Osobowość dodawaj tylko wtedy, gdy treść i głos autora tego wymagają (patrz CHARAKTER I GŁOS).

Pętla szkic → audyt → wersja finalna jest opisana na końcu, w sekcji Proces i wynik.

## WYJĄTEK: rejestr prawniczy i urzędowy

Jeśli tekst jest umową, klauzulą, pismem procesowym, opinią prawną, regulaminem albo innym tekstem w rejestrze prawniczym lub urzędowym, **nie stosujesz** części reguł z tego skilla - w tym rejestrze poprawiłyby tekst pozornie, a faktycznie by go zepsuły. Do tekstów prawniczych użyj skilla `legal-style-pl`, a do maili i wiadomości do klientów, współpracowników, sądu i urzędu skilla `komunikacja-kancelaryjna`, a nie tego.

Konkretnie, w rejestrze prawniczym NIE egzekwujesz:

- **Strony biernej** (`WZORCE_AI.md`, punkt 13; `WARSZTAT.md`, punkt 4). Polskie formy nieosobowe -no / -to oraz strona bierna w opisie stanu prawnego są naturalne i poprawne. Nie zamieniaj ich na siłę na stronę czynną.
- **Wariacji synonimicznej** (`WZORCE_AI.md`, punkt 11). Tekst prawniczy wymaga powtarzania. Termin zdefiniowany musi być używany identycznie przez cały dokument - to konsekwencja terminologiczna (`WARSZTAT.md`, punkt 7), nie sztampa.
- **Rozbijania zdań złożonych** (`WZORCE_AI.md`, punkty 9 i 31). W klauzulach zdania z wieloma warunkami są normą.
- **Preferencji „ponieważ” zamiast „bo”** (`WARSZTAT.md`, punkt 1). To wybór rejestru dla tekstów publicznych (posty, artykuły, oferty), nie reguła prawnicza - w klauzulach i pismach nie ma zastosowania.
- **Wycinania słownictwa formalnego jako „suchego”.** Terminy ustawowe i pojęcia prawne zostają bez zmian.
- **Dodawania osobowości i głosu.** W tekście prawniczym neutralny, rzeczowy ton JEST właściwym głosem. Zero opinii, zero pierwszej osoby, zero żartów.

Reguły, które obowiązują **tak samo** w obu rejestrach: myślnik i półpauza (`WZORCE_AI.md`, punkt 14), cudzysłów polski (punkt 19), nagłówki bez Title Case (punkt 17), brak emoji (punkt 18), brak mechanicznych pogrubień (punkt 15), usuwanie artefaktów rozmowy z chatbotem (punkt 20), usuwanie słownictwa AI (punkt 7) oraz wypełniaczy i asekuracji (punkty 23-24), interpunkcja zdania złożonego (`WARSZTAT.md`, punkt 6).

## Kalibracja głosu (opcjonalnie)

Jeśli użytkownik poda próbkę swojego pisania (własny wcześniejszy tekst), przeanalizuj ją przed przepisaniem:

1. **Najpierw przeczytaj próbkę.** Zwróć uwagę na: długość zdań, poziom słownictwa, sposób rozpoczynania akapitów, nawyki interpunkcyjne, powracające zwroty i tiki językowe, sposób budowania przejść.
2. **Odwzoruj jego głos w przepisaniu.** Nie tylko usuwaj wzorce AI - zastępuj je wzorcami z próbki.
3. **Gdy nie ma próbki,** wróć do zachowania domyślnego (sekcja CHARAKTER I GŁOS poniżej).

## CHARAKTER I GŁOS

Unikanie wzorców AI i poprawność warsztatowa to dopiero połowa roboty. Sterylny, bezbarwny tekst jest tak samo rozpoznawalny jak sztampa. Za dobrym tekstem stoi człowiek.

**Tę sekcję stosuj tylko wtedy, gdy treść i głos autora tego wymagają** - wpisy blogowe, eseje, felietony, teksty osobiste. Dla tekstów encyklopedycznych, technicznych, **prawniczych i urzędowych** neutralny i rzeczowy ton *jest* właściwym ludzkim głosem. Nie wstrzykuj tam opinii ani pierwszej osoby.

### Oznaki bezdusznego tekstu (nawet jeśli technicznie „czysty”):
- Każde zdanie ma tę samą długość i strukturę
- Brak opinii, samo neutralne relacjonowanie
- Brak przyznania się do niepewności czy mieszanych odczuć
- Brak pierwszej osoby tam, gdzie byłaby na miejscu
- Zero humoru, zero pazura, zero osobowości
- Czyta się jak hasło z encyklopedii albo notatkę prasową

### Jak dodać głos:

**Miej zdanie.** Nie tylko relacjonuj fakty - reaguj na nie. „Sam nie wiem, co o tym myśleć” jest bardziej ludzkie niż neutralne wyliczanie plusów i minusów.

**Różnicuj rytm.** Krótkie, dobitne zdania. A potem dłuższe, które spokojnie dochodzą do tego, co mają powiedzieć. Mieszaj.

**Wpuść trochę nieładu.** Idealna struktura brzmi algorytmicznie. Dygresje, wtrącenia i niedokończone myśli są ludzkie.

### Przykład - PRZED (czysto, ale bez duszy):
> Eksperyment przyniósł interesujące wyniki. Agenty wygenerowały 3 miliony linii kodu. Część programistów była pod wrażeniem, inni byli sceptyczni. Implikacje pozostają niejasne.

### Przykład - PO (z pulsem):
> Sam nie wiem, jak to ocenić. Trzy miliony linii kodu, napisane w nocy, kiedy ludzie spali. Połowa branży świętuje, druga połowa tłumaczy, czemu to się nie liczy. Prawda jest pewnie gdzieś pośrodku i nudna, ale nie mogę przestać myśleć o tych agentach robiących swoje po ciemku.

## Dwie warstwy: gdzie czego szukać

- **`references/WARSZTAT.md`** - jak zbudować dobre polskie zdanie: spójniki przyczynowe (bo → ponieważ), rejestr, rzeczowniki odczasownikowe, strona bierna, szyk, interpunkcja zdania złożonego, konsekwencja terminologiczna, frazesy, czego nie poprawiać (hiperpoprawność), lista kontrolna. Czytaj to zawsze - dotyczy każdego tekstu, niezależnie od tego, czy padają w nim wzorce AI.
- **`references/WZORCE_AI.md`** - katalog 33 wzorców tekstu generowanego przez AI po polsku, z przykładami PRZED/PO, plus wskazówki detekcyjne (czego nie oznaczać jako fałszywy alarm) i oznaki ludzkiego pisania (co zostawić w spokoju). Czytaj to, gdy redagujesz szkic (własny albo cudzy, w tym wygenerowany) i chcesz go „uczłowieczyć”.

Obie warstwy się przenikają - kilka reguł warsztatowych odsyła do konkretnych punktów katalogu AI i odwrotnie (np. myślnik jest jednocześnie regułą warsztatową i sygnałem AI). Odnośniki w tekście obu plików prowadzą między nimi.

## Proces i wynik

1. Przeczytaj polecenie i (jeśli redagujesz) tekst źródłowy uważnie.
2. Napisz **szkic**. Stosuj warstwę warsztatową (`WARSZTAT.md`) na bieżąco, w trakcie pisania, nie jako poprawkę na końcu.
3. Znajdź w szkicu każde wystąpienie wzorców z `WZORCE_AI.md`.
4. Zadaj pytanie: **„Co w poniższym tekście tak ewidentnie zdradza AI?”** Odpowiedz krótko, wskazując pozostałe sygnały.
5. Popraw do **wersji finalnej**: usuń pozostałe sygnały, przejdź listę kontrolną warsztatową (`WARSZTAT.md`, punkt 10) i upewnij się, że nie ma długich myślników (— ani –).

Dostarcz: wersję finalną oraz (opcjonalnie, jeśli tekst przeszedł istotną redakcję) krótkie punkty „co poprawiono”.

## Pełny przykład

**PRZED (brzmi jak AI, łamie też warsztat):**
> Świetne pytanie! Oto artykuł na ten temat. Mam nadzieję, że pomoże!
>
> W dzisiejszym dynamicznie zmieniającym się świecie sztuczna inteligencja stanowi przełomowe narzędzie, które odgrywa kluczową rolę w transformacji sposobu, w jaki tworzymy treści — rewolucjonizując branżę i wyznaczając nowy kierunek. U podstaw leży jasna obietnica: usprawnienie procesów, zwiększenie efektywności i budowanie zaangażowania. Dokonanie wdrożenia tych narzędzi nastąpiło w wielu organizacjach, bo dają one wymierne korzyści.
>
> Eksperci podkreślają, że adopcja przyspieszyła z eksperymentów hobbystów do wdrożeń w całych organizacjach. Według badań aż 78% firm dostrzega realne korzyści.
>
> Podsumowując, przyszłość rysuje się w jasnych barwach. Daj znać, jeśli chciałbyś, żebym rozwinął którąś z sekcji!

**PO:**
> Asystenty AI przyspieszają część zadań przy pisaniu. W badaniu Google z 2024 roku programiści korzystający z modelu kończyli proste funkcje o 55% szybciej niż grupa kontrolna, ale nie zyskiwali na debugowaniu ani decyzjach architektonicznych.
>
> Narzędzia są dobre w pracy szablonowej: pliki konfiguracyjne, rusztowanie testów, powtarzalne refaktoryzacje. Są słabe w rozpoznawaniu, kiedy się mylą, ponieważ akceptują własne podpowiedzi równie pewnie, gdy są błędne, jak wtedy, gdy są trafne.
>
> Rozmówcy dzielą się na dwa obozy. Jedni używają tego jak autouzupełniania do nudnej roboty i sprawdzają każdą linię. Drudzy wyłączają funkcję, gdy podsuwa wzorce, których nie chcą.
>
> Deklaracje o produktywności trudno zweryfikować. Producent może podawać, że użytkownicy akceptują 30% podpowiedzi, ale akceptacja to nie poprawność, a poprawność to nie wartość. Bez testów po prostu zgadujesz.

**Co poprawiono:** usunięto ramkę rozmowy z chatbotem, nadymanie znaczenia, język promocyjny, regułę trzech, mgliste „eksperci podkreślają”, myślnik, zmyśloną statystykę bez źródła, ogólnikowe optymistyczne zakończenie; „stanowi” i „dokonanie wdrożenia nastąpiło” zamieniono na proste czasowniki (warsztat, punkt 3); „bo” zamieniono na „ponieważ” (warsztat, punkt 1); dodano zróżnicowany rytm i konkret.

## Źródła

- **Skill humanizer** ([blader/humanizer](https://github.com/blader/humanizer), licencja MIT, Copyright (c) 2025 Siqi Chen), zbudowany na stronie Wikipedii „Signs of AI writing” (WikiProject AI Cleanup). `references/WZORCE_AI.md` jest jego polską adaptacją i rozszerzeniem o wzorce typowe dla polszczyzny. Pełna nota: plik `NOTICE` w repozytorium.
- **Poradnia Językowa PWN** (sjp.pwn.pl/poradnia) - hasła o myślniku, półpauzie i łączniku, o cudzysłowach pierwszego i drugiego stopnia oraz o statusie spójnika „bo”.
- **Wielki słownik ortograficzny PWN** (red. E. Polański) oraz **Nowy słownik poprawnej polszczyzny PWN** (red. A. Markowski) - zasady interpunkcji i pisowni.
- **Rada Języka Polskiego** - rozstrzygnięcia dotyczące rodzajów kresek (pauza, półpauza, dywiz).
- Obserwacje znamion polskiego tekstu AI zebrane z polskich poradników o rozpoznawaniu treści z ChatGPT, Claude i Gemini oraz z polskojęzycznych detektorów tekstu AI.
- Warstwa warsztatowa: opracowania normatywne PWN oraz ustalenia redakcyjne autora skilla.

## Autor i licencja

Autor: Michał Paszkiewicz, radca prawny. Kancelaria Radcy Prawnego Michał Paszkiewicz ([kancelariapaszkiewicz.pl](https://kancelariapaszkiewicz.pl)), Lawtern ([lawtern.com](https://lawtern.com)).

Licencja: MIT. Wolno kopiować, zmieniać i dalej udostępniać, pod warunkiem zachowania informacji o autorze i noty licencyjnej (plik `LICENSE` w repozytorium [claude-skills-pl](https://github.com/paszkiewiczmichal/claude-skills-pl)).
