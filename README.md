Jak postawić prostą stronę HTML na GitHub Pages (z własną domeną i SSL)

1. Załóż konto i repozytorium

• Konto: wejdź na github.com i załóż konto (jeśli jeszcze nie masz).
• Nowe repozytorium:• kliknij New repository,
• Name: np. moja-strona,
• zaznacz Public,
• możesz zaznaczyć Add a README (opcjonalnie),
• kliknij Create repository.



---

2. Dodaj plik `index.html`

Najprostsza strona:
```html
<!DOCTYPE html>
<html lang="pl">
<head>
  <meta charset="UTF-8">
  <title>Moja strona</title>
</head>
<body>
  <h1>Cześć, to moja strona na GitHub Pages!</h1>
</body>
</html>
```

• W repozytorium kliknij Add file → Create new file.
• Nazwa pliku: index.html.
• Wklej kod HTML.
• Na dole kliknij Commit changes.


---

3. Włącz GitHub Pages

• Wejdź w Settings repozytorium.
• Po lewej znajdź sekcję Pages.
• W części Source wybierz:• Branch: main (lub master, jeśli taki masz),
• Folder: /root.

• Kliknij Save.


Po chwili pojawi się adres w stylu:

https://twoj-login.github.io/moja-strona/

Strona już działa i ma darmowy certyfikat SSL.

---

4. Podpięcie własnej domeny

Załóżmy, że masz domenę twojadomena.pl.

1. Dodaj plik CNAME w repozytorium:• Add file → Create new file.
• Nazwa pliku: CNAME (bez rozszerzenia).
• Zawartość pliku:twojadomena.pl

• Commit changes.

2. Ustaw DNS u operatora domeny:• Wejdź do panelu domeny (np. OVH, nazwa.pl, cyber_Folks).
• Dodaj rekord:• Typ: CNAME
• Nazwa/Host: twojadomena.pl (lub www, jeśli chcesz www.twojadomena.pl)
• Wartość: twoj-login.github.io

• Zapisz zmiany.



Po propagacji DNS (zwykle od kilku minut do kilku godzin) strona będzie dostępna pod Twoją domeną.

---

5. Certyfikat SSL (HTTPS)

• GitHub Pages automatycznie wystawia certyfikat SSL dla domeny, którą podasz w pliku CNAME.
• W Settings → Pages zobaczysz opcję Enforce HTTPS—po chwili powinna być dostępna, zaznacz ją.
• Gotowe: Twoja strona działa pod https://twojadomena.pl z darmowym certyfikatem.


---

Jeśli chcesz, możesz napisać, jaką dokładnie masz domenę i pokażę Ci konkretne rekordy DNS, które trzeba ustawić.
