# Introducció a Git - 01 Git Basics

Repositori d'exercicis de git. Segueix les instruccions i resold els exercicis
proposats. Llegeix atentament les instruccions i procura no entrar en cap
estat _estrany_ del git que requereixi de cap **_màgia arcana_** per
arreglar-ho.

> ### _Think twice before press Return_
>
> Pots usar el _pull request_ `Feedback` (ja està creat) per demanar ajut i
> fer alguna pregunta en els comentaris. **_No el tanquis ni facis cap merge
> amb ell_**. Si menciones a algú directament amb `@`, per exemple `@rocher`,
> llavors li arriba un email amb el missatge.
>
> Recorda que qualsevol comanda de git sempre té una petita ajuda disponible
> amb l'opció `-h`. Per exemple:
> ```bash
>     git commit -h
>     git push -h
> ```
> Si uses l'opció `--help` llavors accediràs a la pàgina de manual. Per
> exemple:
> ```bash
>     git add --help
> ```

## Exercici 1

  - Clona aquest repositori remot en un repositori local.
  - Copia el següent codi html i posa'l en un fitxer que es digui `exe1.html`.

```html
<html>
    <body>
        <h1>Exercici 1</h1>
    </body>
</html>
```

  - Un cop copiat, esborra el codi html d'aquest fitxer, `README.md`, de forma
    que aquest punt quedi junt al punt anterior (sense cap línia en blanc entre
    ambdós).
  - Fes un únic commit que inclogui els canvis dels fitxers `README.md` i
    `exe1.html`. El missatge ha del commit ha de dir 'Nou exe1'.
  - Fes el push del commit que acabes de fer.

## Exercici 2

  - Copia el fitxer `exe1.html` a `exe2.html`.
  - Edita `exe2.html` i canvia _Exercici 1_ per _Exercici 2_.
  - Fes un commit i un push del fitxer `exe2.html` amb el missatge 'Nou exe2'.

## Exercici 3

  - Ens agrada molt usar Bootstrap. Afegeix el següent codi html just abans del
    `<body>` en els fitxers `exe1.html` i `exe2.html`, adaptant el `?` a cada
    un d'ells amb el número corresponent (1 o 2, òbviament).

```html
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>Exercici ?</title>

    <!-- Include Bootstrap HTML, CSS and JS library -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.8/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-sRIl4kxILFvY47J16cr9ZwB07vP4J8+LH7qKQnuqkuIAvNWLzeN8tE5YBujZqJLB" crossorigin="anonymous">
  </head>
  ```

  - Esborra el codi html d'aquest fitxer, `README.md`, de forma que aquest
    punt quedi a continuació de l'anterior (sense línies en blanc entre mig
    d'ambdós).
  - Fes un commit amb tots els canvis (3 fitxers). El missatge ha de dir
    'Using Bootstrap'.
  - Fes un push del commit anterior.

## Exercici 4

  - Crea una branca que es digui `web`. Fes que la branca principal tingui
    només el fitxer `README.md` i la branca `web` tots els fitxers. Usa `git
    rm` per esborrar fitxers i `git commit` per confirmar que els esborres.
    Fes el push de les dues branques. `git rm -h` et donarà alguna pista més.

## Exercici 5

  - Crea un fitxer amb el log de totes les comandes `git` que has usat en el
    repositori local. Fes-ho amb la comanda `history | grep git > git.log`.
    Fes el commit i el push del fitxer `git.log` a la branca principal. El
    missatge del commit ha de ser 'New git log'

## Exercici 6

  - A la branca `web`, afegeix el fitxer d'estil `style.css` amb el contingut
    següent:

```css
pre {
    background-color: #333;
    color: #373;
}
```

  - Esborra els codi css d'aquest fitxer, `README.md`, de forma que aquest
    punt estigui a continuació de l'anterior. Fes el commit i el push del
    `README.md` a la branca principal. Missatge: 'README Only'.
  - Fes el commit i el push del fitxer d'estil a la branca `web`. El missatge
    de commit ha de ser 'Nou css'.

## Exercici 7

  - A la branca `web`, Aplica el fitxer d'estil css als fitxers `exe1.html` i
    `exe2.html`. Has de posar el següent html just abans de `</head>`:

```html
    <link href="style.css">
```

  - Esborra aquest codi html d'aquest fitxer, `README.md`, i fes el commit i
    el push a la branca principal. Missatge: 'HTML done'.
  - Fes el commit i el push dels fitxers `exe1.html` i `exe2.html` a la branca
    `web` amb el missatge 'More css'.

## Exercici 8

  - En el fitxer `exe1.html`, just a sota de `<h1>Exercici 1</h1>`, inserta el
    fitxer `git.log` entre `<pre>` i `</pre>` amb les següents comandes:

```bash
    echo '<pre>' >> exe1.html
    cat git.log >> exe1.html
    echo '</pre>' >> exe1.html
```

  - Edita el fitxer `exe1.html` i posa a lloc el bloc `<pre>..</pre>`, que ha
    d'anar just abans del tag `</body>`.
  - Fes el commit i el push del fitxer `exe1.html` a la branca `web`.
    Missatge: 'Git log to exe1'.
  - Esborra el codi `bash` anterior d'aquest fitxer, `README.md`, de forma que
    no hi hagi línies en blanc entre els punts. Fes el commit i el push
    d'aquests canvis a la branca principal. Missatge: 'No bash'.

## Exercici 9

  - Posa el tag `v0.1` a la branca `web`, en el darrer commit, amb el missatge
    `first web version`. Fes el push del tag.
  - Posa el tag `v0.1` a la branca principal, en el commit que té el missatge
    'Only README'. Fes el push del tag.
