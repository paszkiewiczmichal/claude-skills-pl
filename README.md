# claude-skills-pl

Dwa skille dla Claude, które pomagają pisać po polsku tak, żeby nie brzmiało jak LLM.

Autor: [Michał Paszkiewicz](https://kancelariapaszkiewicz.pl) — radca prawny.

---

## humanizer-pl

Tekst wygenerowany przez AI ma charakterystyczne wzorce. Napuszone podkreślanie wagi każdej banalnej rzeczy. Doczepki "co podkreśla / co odzwierciedla". Reguła trzech. Długie myślniki żywcem z angielskiego. Słownictwo w stylu "kluczowy / istotny / kompleksowy". Strona bierna z ukrytym sprawcą. I nieodmiennie frazesy na pożegnanie — "daj znać / mam nadzieję, że pomogłem".

Ten skill każe Claude to wszystko wyłapać i przepisać. Naturalnie, po polsku, bez sterylnej równości zdań.

Reguły oparte na normach PWN, nie na intuicji.

**Instalacja:**

```
/plugin install humanizer-pl@paszkiewiczmichal/claude-skills-pl
```

---

## legal-style-pl

Do tekstów prawnych humanizer nie pasuje. Umowy, pisma, opinie mają własne reguły: zdefiniowane pojęcia muszą się powtarzać, zdania z wieloma warunkami są normą, strona bierna w opisie stanu prawnego jest poprawna. Humanizer by to wszystko popsuł.

legal-style-pl pilnuje języka w dokumentach prawnych: precyzja terminologiczna, poprawna polska interpunkcja, zero sztucznej lekkości, zero sformułowań AI.

**Instalacja:**

```
/plugin install legal-style-pl@paszkiewiczmichal/claude-skills-pl
```

---

## Jak używać

Skille działają w Claude.ai, Claude Code i Cowork.

**W projekcie Claude.ai** — wgraj plik `.md` do zasobów projektu lub wklej treść do instrukcji systemowej.

**W Claude Code** — zainstaluj przez `/plugin install`.

**Ręcznie** — skopiuj zawartość pliku `.md` i wklej na początku rozmowy z poleceniem: "Załaduj ten skill i stosuj przez całą rozmowę."

---

## Struktura

```
claude-skills-pl/
├── humanizer-pl/
│   └── SKILL.md
├── legal-style-pl/
│   └── SKILL.md
└── README.md
```

---

MIT License
