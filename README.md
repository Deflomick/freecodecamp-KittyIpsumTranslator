# Kitty Ipsum Translator

Script Bash che "traduce" testi sui gatti in testi sui cani, sostituendo
le parole con `sed`. Progetto del workshop freeCodeCamp *Learn Advanced
Bash by Building a Kitty Ipsum Translator*.

## Cosa fa

- `translate.sh` legge un testo e sostituisce `catnip` → `dogchow`,
  `cat` → `dog`, `meow`/`meowzer` → `woof`
- `kitty_info` raccoglie statistiche sui due testi: righe, parole,
  caratteri, occorrenze di "meow" e "cat" e righe in cui compaiono

## Requisiti

- Bash
- Strumenti standard: `grep`, `sed`, `wc`, `cat`, `diff`

## Utilizzo

```bash
chmod +x translate.sh

# Da file come argomento
./translate.sh kitty_ipsum_1.txt

# Da standard input
./translate.sh < kitty_ipsum_1.txt
cat kitty_ipsum_1.txt | ./translate.sh

# Salvare la traduzione e confrontarla con l'originale
./translate.sh kitty_ipsum_1.txt > doggy_1
diff --color kitty_ipsum_1.txt doggy_1
```

## Cosa ho imparato

- Redirect di stdout e stderr (`>`, `>>`, `2>`, `1>`)
- Input da file e pipe (`<`, `|`, `read`, `cat`)
- Script eseguibili: shebang, `chmod +x`, argomenti (`$1`)
- `wc`, `grep` (`-n`, `-o`, `-c`) e `sed` con regex estese (`-E`)
- Confronto di file con `diff`
