<p align="center"><img src="/images/logo.png" alt=""></p>
<h1 align="center">What the f*ck Python! 😱</h1>
<p align="center">Entdecke und verstehe Python durch überraschende Code-Schnipsel.</p>

Übersetzungen: [English](https://github.com/satwikkansal/wtfpython) |

Andere Modi: [Interaktiv](https://colab.research.google.com/github/satwikkansal/wtfpython/blob/master/irrelevant/wtf.ipynb) | [CLI](https://pypi.python.org/pypi/wtfpython)

Python, bekannt als gut designte High-Level und Interpreter-basierte Programmiersprache, stellt viele Features zur Verfügung, um dem Programmierer das Leben zu erleichtern. Allerdings kann es vorkommen, dass ein Python-Schnipsel ein unerwartetes Verhalten zeigt.

Hier ist ein schönes Projekt, das versucht die Dinge aufzuzeigen, die bei einigen Code-Schnipseln unter der Haube passieren und darüber hinaus einige weniger bekannte Features von Python zu erklären.

Während manche Beispiele nicht unbedingt beeindruckend erscheinen, zeigen sie dennoch interessante Details von Python, die dir womöglich noch nicht aufgefallen sind. Ich finde, dass es eine schöne Möglichkeit ist, die Interna einer Programmiersprache zu lernen und ich glaube das findest du auch !

Wenn du ein erfahrener Python-Programmierer bist, kannst du dies als Herausforderung ansehen, um möglichst viel beim ersten Anlauf
richtig zu machen. Du hast vielleicht manches schon erlebt, sodass ich möglicherweise alte Erinnerungen wecken kann! :sweat_smile:

PS: Wenn du bereits mehrfach hier warst, kannst du dich [hier](https://github.com/satwikkansal/wtfpython/releases/) über neue Modifikationen informieren (die Beispiele, die mit einem Stern markiert sind, sind Teil des letzten Releases).

Also, los gehts...

# Inhaltsverzeichnis

<!-- Generated using "markdown-toc -i README.md --maxdepth 3"-->

<!-- toc -->

- [Inhaltsverzeichnis](#inhaltsverzeichnis)
- [Sruktur der Beispiele](#sruktur-der-beispiele)
- [Benutzung](#benutzung)
- [👀 Beispiele](#-beispiele)
  - [Kapitel: Fordere dein Gehirn heraus!](#kapitel-fordere-dein-gehirn-heraus)
    - [▶ Das Wichtigste zuerst! \*](#-das-wichtigste-zuerst-)
      - [💡 Erklärung](#-erklärung)
    - [▶ Strings können manchmal schwierig sein](#-strings-können-manchmal-schwierig-sein)
      - [💡 Erklärung:](#-erklärung-1)
    - [▶ Vorsicht bei verketteten Operationen](#-vorsicht-bei-verketteten-operationen)
      - [💡 Erklärung:](#-erklärung-2)
    - [▶ Wie man den `is` Operator nicht nutzt](#-wie-man-den-is-operator-nicht-nutzt)
      - [💡 Erklärung:](#-erklärung-3)
    - [▶ Hash brownies](#-hash-brownies)
      - [💡 Erklärung](#-erklärung-4)
    - [▶ Tief im Inneren sind wir alle gleich](#-tief-im-inneren-sind-wir-alle-gleich)
      - [💡 Erklärung:](#-erklärung-5)
    - [▶ Unordnung in der Ordnung \*](#-unordnung-in-der-ordnung-)
      - [💡 Erklärung:](#-erklärung-6)
    - [▶ Versuche es weiter... \*](#-versuche-es-weiter-)
      - [💡 Erklärung:](#-erklärung-7)
    - [▶ Wofür?](#-wofür)
      - [💡 Erklärung:](#-erklärung-8)
    - [▶ Diskrepanz in der Auswertungszeit](#-diskrepanz-in-der-auswertungszeit)
      - [💡 Erklärung](#-erklärung-9)
    - [▶ `is not ...` ist nicht `is (not ...)`](#-is-not--ist-nicht-is-not-)
      - [💡 Erklärung](#-erklärung-10)
    - [▶ Ein tic-tac-toe wo X im ersten Versuch gewinnt!](#-ein-tic-tac-toe-wo-x-im-ersten-versuch-gewinnt)
      - [💡 Erklärung:](#-erklärung-11)
    - [▶ Schrödingers Variable \*](#-schrödingers-variable-)
      - [💡 Erklärung:](#-erklärung-12)
    - [▶ Das Henne-Ei-Problem \*](#-das-henne-ei-problem-)
      - [💡 Erklärung](#-erklärung-13)
    - [▶ Beziehungen in Unterklassen](#-beziehungen-in-unterklassen)
      - [💡 Erklärung:](#-erklärung-14)
    - [▶ Methodengleichheit und -identität](#-methodengleichheit-und--identität)
      - [💡 Erklärung](#-erklärung-15)
    - [▶ All-true-ation \*](#-all-true-ation-)
      - [💡 Erklärung:](#-erklärung-16)
      - [💡 Erklärung:](#-erklärung-17)
    - [▶ Strings und die Backslashes](#-strings-und-die-backslashes)
      - [💡 Erklärung](#-erklärung-18)
    - [▶ not knot!](#-not-knot)
      - [💡 Erklärung:](#-erklärung-19)
    - [▶ Halbe Zeichenketten in dreifachen Anführungszeichen](#-halbe-zeichenketten-in-dreifachen-anführungszeichen)
      - [💡 Erklärung:](#-erklärung-20)
    - [▶ Was ist falsch an booleans?](#-was-ist-falsch-an-booleans)
      - [💡 Erklärung:](#-erklärung-21)
    - [▶ Klassen- und Instanzattribute](#-klassen--und-instanzattribute)
      - [💡 Erklärung:](#-erklärung-22)
    - [▶ yielding None](#-yielding-none)
      - [💡 Erklärung:](#-erklärung-23)
    - [▶ Yielding from... return! \*](#-yielding-from-return-)
      - [💡 Erklärung:](#-erklärung-24)
    - [▶ Nan-Reflexivität \*](#-nan-reflexivität-)
      - [💡 Erklärung:](#-erklärung-25)
    - [▶ Verändern des Unveränderlichen!](#-verändern-des-unveränderlichen)
      - [💡 Erklärung:](#-erklärung-26)
    - [▶ Die verschwindende Variable aus dem äußeren Gültigkeitsbereich](#-die-verschwindende-variable-aus-dem-äußeren-gültigkeitsbereich)
      - [💡 Erklärung:](#-erklärung-27)
    - [▶ Die mysteriöse key type Umwandlung](#-die-mysteriöse-key-type-umwandlung)
      - [💡 Erklärung:](#-erklärung-28)
    - [▶ Lass uns sehen, ob du dies errätst?](#-lass-uns-sehen-ob-du-dies-errätst)
      - [💡 Erklärung:](#-erklärung-29)
    - [▶ Überschreitet den Grenzwert für die Umwandlung von Integer-Strings](#-überschreitet-den-grenzwert-für-die-umwandlung-von-integer-strings)
      - [💡 Erklärung:](#-erklärung-30)
  - [Kapitel: Slippery Slopes](#kapitel-slippery-slopes)
    - [▶ Modifizieren eines Dictionarys während einer Iteration](#-modifizieren-eines-dictionarys-während-einer-iteration)
      - [💡 Erklärung:](#-erklärung-31)
    - [▶ Hartnäckige `del` Operation](#-hartnäckige-del-operation)
      - [💡 Erklärung:](#-erklärung-32)
    - [▶ Die Variable aus dem äußeren Geltungsbereich](#-die-variable-aus-dem-äußeren-geltungsbereich)
      - [💡 Erklärung:](#-erklärung-33)
    - [▶ Löschen eines Listenelements während einer Iteration](#-löschen-eines-listenelements-während-einer-iteration)
      - [💡 Erklärung:](#-erklärung-34)
    - [▶ Lossy Zips von Iteratoren \*](#-lossy-zips-von-iteratoren-)
      - [💡 Erklärung:](#-erklärung-35)
    - [▶ Schleifenvariablen, die auslaufen!](#-schleifenvariablen-die-auslaufen)
      - [💡 Erklärung:](#-erklärung-36)
    - [▶ Vorsicht vor standardmäßig veränderbaren Argumenten!](#-vorsicht-vor-standardmäßig-veränderbaren-argumenten)
      - [💡 Erklärung:](#-erklärung-37)
    - [▶ Fangen der Exceptions](#-fangen-der-exceptions)
      - [💡 Erklärung](#-erklärung-38)
    - [▶ Gleiche Operanden, unterschiedliche Story!](#-gleiche-operanden-unterschiedliche-story)
      - [💡 Erklärung:](#-erklärung-39)
    - [▶ Namensauflösung ohne Berücksichtigung des Geltungsbereichs der Klasse](#-namensauflösung-ohne-berücksichtigung-des-geltungsbereichs-der-klasse)
      - [💡 Erklärung](#-erklärung-40)
    - [▶ Runden wie ein Bankier \*](#-runden-wie-ein-bankier-)
      - [💡 Erklärung:](#-erklärung-41)
    - [▶ Nadeln im Heuhaufen \*](#-nadeln-im-heuhaufen-)
      - [💡 Erklärung:](#-erklärung-42)
    - [▶ Splitsies \*](#-splitsies-)
      - [💡 Erklärung:](#-erklärung-43)
    - [▶ Wilde Imports \*](#-wilde-imports-)
      - [💡 Erklärung:](#-erklärung-44)
    - [▶  Alles sortieren ? \*](#--alles-sortieren--)
      - [💡 Erklärung:](#-erklärung-45)
    - [▶ Mitternachtszeit gibt es nicht ?](#-mitternachtszeit-gibt-es-nicht-)
      - [💡 Erklärung:](#-erklärung-46)
  - [Kapitel: Die verborgenen Schätze!](#kapitel-die-verborgenen-schätze)
    - [▶ Okay Python, kannst du mich fliegen lassen?](#-okay-python-kannst-du-mich-fliegen-lassen)
      - [💡 Erklärung:](#-erklärung-47)
    - [▶ `goto`, aber wieso?](#-goto-aber-wieso)
      - [💡 Erklärung:](#-erklärung-48)
    - [▶ Halte dich fest!](#-halte-dich-fest)
      - [💡 Erklärung:](#-erklärung-49)
    - [▶ Let's meet Friendly Language Uncle For Life](#-lets-meet-friendly-language-uncle-for-life)
      - [💡 Erklärung:](#-erklärung-50)
    - [▶ Selbst Python versteht, dass Liebe kompliziert ist](#-selbst-python-versteht-dass-liebe-kompliziert-ist)
      - [💡 Erklärung:](#-erklärung-51)
    - [▶ Ja, es existiert!](#-ja-es-existiert)
      - [💡 Erklärung:](#-erklärung-52)
    - [▶ Ellipsen \*](#-ellipsen-)
      - [💡 Erklärung](#-erklärung-53)
    - [▶ Einbindung](#-einbindung)
      - [💡 Erklärung:](#-erklärung-54)
    - [▶ Lass uns demolieren](#-lass-uns-demolieren)
      - [💡 Erklärung:](#-erklärung-55)
  - [Kapitel: Der Schein trügt!](#kapitel-der-schein-trügt)
    - [▶ Zeilen überspringen?](#-zeilen-überspringen)
      - [💡 Erklärung](#-erklärung-56)
    - [▶ Teleportation](#-teleportation)
      - [💡 Erklärung:](#-erklärung-57)
    - [▶ Da ist wohl irgendwas faul...](#-da-ist-wohl-irgendwas-faul)
      - [💡 Erklärung](#-erklärung-58)
  - [Kapitel: Sonstiges](#kapitel-sonstiges)
    - [▶ `+=` ist schneller](#--ist-schneller)
      - [💡 Erklärung:](#-erklärung-59)
    - [▶ Lass uns einen gigantischen String machen!](#-lass-uns-einen-gigantischen-string-machen)
      - [💡 Erklärung](#-erklärung-60)
    - [▶ Verlangsamen von `dict` Lookups \*](#-verlangsamen-von-dict-lookups-)
      - [💡 Erklärung:](#-erklärung-61)
    - [▶ Blähende Instanz `dict`s \*](#-blähende-instanz-dicts-)
      - [💡 Erklärung:](#-erklärung-62)
    - [▶ Kleinigkeiten \*](#-kleinigkeiten-)
  - [Das Verhalten ist darauf zurückzuführen, dass leere Teilstrings (`''`) mit Slices der Länge 0 in der ursprünglichen Zeichenkette übereinstimmen](#das-verhalten-ist-darauf-zurückzuführen-dass-leere-teilstrings--mit-slices-der-länge-0-in-der-ursprünglichen-zeichenkette-übereinstimmen)
- [Contributing](#contributing)
- [Anerkennung](#anerkennung)
      - [Ein paar nützliche Links!](#ein-paar-nützliche-links)
- [🎓 License](#-license)
  - [Überrasche auch deine Freunde!](#überrasche-auch-deine-freunde)
  - [Brauchst du eine pdf version?](#brauchst-du-eine-pdf-version)

<!-- tocstop -->

# Sruktur der Beispiele

Alle Beispiele sind nach folgendem Muster aufgebaut:

> ### ▶ Ein schicker Titel
>
> ```py
> # Vorbereitung des Codes.
> # Vorbereitung für etwas Magisches...
> ```
>
> **Ausgabe (Python version(en)):**
>
> ```py
> >>> triggering_statement
> Irgendeine unerwartete Ausgabe
> ```
> (Optional): Eine Zeile, die die unerwartete Ausgabe beschreibt.
>
>
> #### 💡 Erklärung:
>
> * Kurze Erklärung was und warum es passiert.
> ```py
> # Aufsetzen des Codes
> # Mehr Beispiele für ein besseres Verständnis (wenn erforderlich)
> ```
> **Ausgabe (Python version(en)):**
>
> ```py
> >>> trigger # Ein Beispiel, das es einfach macht, die Magie zu verstehen
> # Eine begründete Ausgabe
> ```

**Note:** Alle Beispiele sind mit Pythons 3.5.2 interaktiven Interpreter getestet, und sie sollten für alle Python Versionen funktionieren. Ausnahmen werden vor dem Ausgabe kenntlich gemacht.

# Benutzung

Ein guter Weg, um die Beispiele bestmöglich zu nutzen, ist es, sie von anfang an durchzugehen und bei jedem Beispiel folgendes zu tun:
- Lese vorsichtig den initialen Code des Beispiels. Wenn du ein erfahrener Python-Programmierer bist, wirst du wahrscheinlich wissen, was
als nächstes kommt.
- Lies die Schnippsel durch und
  + Überprüfe, dass die Ausgabe die ist, die du erwartet hast
  + Weißt du, warum sich die Ausgabe so gestaltet, wie sie es tut ?
    - Wenn die Antwort Nein ist (was vollkommen in Ordnung ist), nimm einen tiefen Atemzug, und lies dir die Erklärung durch. Wenn du es dann immernoch nicht verstanden hast, frage nach Hilfe, indem du [hier](https://github.com/satwikkansal/wtfpython/issues/new) ein Issue erstellst.
    - Wenn Ja, kannst du dir auf die Schulter klopfen und zum nächsten Beispiel springen. 

PS: Du kannst dir auch WTFPython im Terminal ansehen, indem du das [pypi package](https://pypi.python.org/pypi/wtfpython) nutzt:
```sh
$ pip install wtfpython -U
$ wtfpython
```
---

# 👀 Beispiele

## Kapitel: Fordere dein Gehirn heraus!

### ▶ Das Wichtigste zuerst! *

<!-- Example ID: d3d73936-3cf1-4632-b5ab-817981338863 -->
<!-- read-only -->

Aus irgendwelchen Gründen ist der "Walrus" Operator (`:=`) in Python 3.8 ziemlich beliebt. Lass uns starten,

1\.

```py
# Python version 3.8+

>>> a = "wtf_walrus"
>>> a
'wtf_walrus'

>>> a := "wtf_walrus"
File "<stdin>", line 1
    a := "wtf_walrus"
      ^
SyntaxError: invalid syntax

>>> (a := "wtf_walrus") # Das funktioniert merkwürdigerweise
'wtf_walrus'
>>> a
'wtf_walrus'
```

2 \.

```py
# Python version 3.8+

>>> a = 6, 9
>>> a
(6, 9)

>>> (a := 6, 9)
(6, 9)
>>> a
6

>>> a, b = 6, 9 # Typisches Auspacken
>>> a, b
(6, 9)
>>> (a, b = 16, 19) # Oops
  File "<stdin>", line 1
    (a, b = 16, 19)
          ^
SyntaxError: invalid syntax

>>> (a, b := 16, 19) # Dies gibt ein eigenartiges 3-Tupel aus
(6, 16, 19)

>>> a # Ist a immernoch unverändert ?
6

>>> b
16
```



#### 💡 Erklärung

**Schneller Rückblick zum Walrus Operator**

Der Walrus Operator (`:=`) wurde in Python 3.8 eingeführt. Er kann in Situationen sinvoll sein, in 
denen du ein Wert einer Variablen in einem Ausdruck zuweisen möchtest.

```py
def irgendeine_funktion():
        # Irgendeine Berechnung, die teuer ist (=> sehr viel Zeit und Ressourcen in Aspruch nimmt)
        # time.sleep(1000)
        return 5

# Anstatt:
if irgendeine_funktion():
        print(irgendeine_funktion()) # Schlechter Stil, da die Funktion zweimal aufgerufen wird

# Oder:
a = irgendeine_funktion()
if a:
    print(a)

# Nun kannst du folgendes schreiben:
if a := irgendeine_funktion():
        print(a)
```

**Ausgabe (> 3.8):**

```py
5
5
5
```

Das hat uns eine Zeile Code erspart. Zudem spart es einen zusätzlichen Aufruf der Funktion `irgendeine_funktion`.

- Nichtgeklammerte "Zuweisung Ausdruck" (Verwendung des Walrus-Operator), ist auf der obersten Ebene beschränkt, daher der `Syntaxfehler` in der Anweisung `a := "wtf_walrus"` des erstes Schnipsels.  Einklammeren hat funktioniert und wies `a` zu.

- Wie immer, Einklammerung eines Ausdrucks, welcher `=`- Operator enthält, ist nicht erlaubt. Daher der Syntaxfehler in `(a, b = 6, 9)`.

- Die Syntax des Walrus Operators lautet wie folgt: `NAME:= ausdruck`, wobei `NAME` ist ein gültiger Identifier, und `ausdruck` ist ein gültiger Ausdruck. Zudem werden iterierbares Verpacken und Entpacken nicht unterstützt, d.h.: 

  - `(a := 6, 9)` ist äquivalent zu `((a := 6), 9)` und zu `(a, 9) ` (where `a`'s value is 6')

    ```py
    >>> (a := 6, 9) == ((a := 6), 9)
    True
    >>> x = (a := 696, 9)
    >>> x
    (696, 9)
    >>> x[0] is a # Both reference same memory location
    True
    ```

  - Ähnlich: `(a, b := 16, 19)` ist äquivalent zu `(a, (b := 16), 19)`, was einfach ein 3-Tupel ist. 

---

### ▶ Strings können manchmal schwierig sein

<!-- Example ID: 30f1d3fc-e267-4b30-84ef-4d9e7091ac1a --->
1\.

```py
>>> a = "irgendein_string"
>>> id(a)
140420665652016
>>> id("irgendein" + "_" + "string") # Beachte, dass beide ids dieselben sind.
140420665652016
```

2\.
```py
>>> a = "wtf"
>>> b = "wtf"
>>> a is b
True

>>> a = "wtf!"
>>> b = "wtf!"
>>> a is b
False

```

3\.

```py
>>> a, b = "wtf!", "wtf!"
>>> a is b # Alle Versionen außer 3.7.x
True

>>> a = "wtf!"; b = "wtf!"
>>> a is b # Das wird True oder False ausgeben, je nach dem wo du es aufrufst (Python Shell / iPython / in einem Skript)
False
```

```py
# Dieses mal in einer Datei: some_file.py
a = "wtf!"
b = "wtf!"
print(a is b)

# Gibt True aus, wenn das Modul aufgerufen wird!
```

4\.

**Ausgabe (< Python3.7 )**

```py
>>> 'a' * 20 is 'aaaaaaaaaaaaaaaaaaaa'
True
>>> 'a' * 21 is 'aaaaaaaaaaaaaaaaaaaaa'
False
```

Ergibt Sinn, Oder?

#### 💡 Erklärung:
+ Das Verhalten im ersten und zweiten Schnipsel erklärt sich durch eine CPython Optimierung (auch string interning genannt), die versucht, existierende
immutable Objekte zu nutzen anstatt jedes mal ein neues Objekt zu erstellen.
+ Nachdem "interned" (festgehalten) wurde, kann es sein, dass viele Variablen dasselbe String-Objekt im Speicher referenzieren (man spart also Speicher). 

+ In den Schnipseln oben werden Strings implizit festgehalten. Die Entscheidung, wann ein String implizit festgehalten wird, ist von der Implementierung
abhängig. Es gibt einige Regeln, die benutzt werden können, um zu erahnen, ob ein String festgehalten wird oder nicht:
  * Alle String der Länge 0 und 1 werden festgehalten.
  * Strings werden während der Compilezeit festgehalten (`'wtf'` wird festgehalten, aber `''.join(['w', 't', 'f'])` nicht)
  * Strings, die nicht aus ASCII-Buchstaben, Ziffern oder Unterstrichen zusammengesetzt sind, werden nicht festgehalten. Das erklärt warum `'wtf!'` nicht festgehalten wurde (wegen `!`). 
  Die CPython-Implementierung dieser Regel kann [hier](https://github.com/python/cpython/blob/3.6/Objects/codeobject.c#L19) gefunden werden
  ![image](/images/string-intern/string_intern.png)
+ Wenn `a` und `b` in derselben Zeile auf `"wtf!"` gesetzt werden, erzeugt der Python Interpreter ein neues Objekt, welches von der zweiten Variable zur selben Zeit referenziert wird. Wenn du es in zwei verschiedenen Zeilen deklarierst, dann "weiß" der Interpreter nicht, dass `"wtf!"` als Objekt schon existiert (weil `"wtf!"` nicht implizit festgehalten wird, siehe obige Auflistung). Es ist eine Compilezeit-Optimierung. Diese Optimierung gilt nicht für 3.7.x Versionen von CPython (siehe dieses [Issue](https://github.com/satwikkansal/wtfpython/issues/100)).
+ Eine Compile-Unit ist eine interaktive Umgebung, wie z.B. IPython besteht aus einen einzigen Statement, während es aus einem ganzen Modul im Falle von Modulen besteht. `a, b = "wtf!", "wtf!"` ist ein einziges Statement, während `a = "wtf!"; b = "wtf!"` zwei Statements in einer Zeile sind. Das erklärt, warum die Identitäten `a = "wtf!"; b = "wtf!"` verschieden sind. Es erklärt auch, warum sie dieselben sind, wenn sie in `some_file.py` aufgerufen werden.
+ Die abrupte Veränderung in der Ausgabe des 4.Schnipsel ist der [peephole Optimierung](https://en.wikipedia.org/wiki/Peephole_optimization) Technik
geschuldet, auch als Constant Folding bekannt. Das bedeutet, der Ausdruck `'a'*20` wird durch `'aaaaaaaaaaaaaaaaaaaa'` während der Kompilierung ersetzt, um ein paar Taktzyklen während der Laufzeit zu sparen. Constant Folding wird nur für String mit einer kleineren Länge als 21 angewendet. (Wieso ? Stelle dir die Größe einer `.pyc` Datei vor, die durch den Ausdruck `'a'*10**10` generiert wurde). [Hier](https://github.com/python/cpython/blob/3.6/Python/peephole.c#L288) ist die Quelle der Implementierung dafür.
+ Notiz: In Python 3.7, konstantes Folding wurde vom peephole-Optimierer zum neuen AST-Optimierer verschoben (mit ein paar Veränderungen in der Logik), d.h. das 4.Schnipsel funktioniert in Python 3.7 nicht. Du kannst [hier](https://bugs.python.org/issue11549) mehr darüber erfahren.

---


### ▶ Vorsicht bei verketteten Operationen
<!-- Example ID: 07974979-9c86-4720-80bd-467aa19470d9 --->
```py
>>> (False == False) in [False] # makes sense
False
>>> False == (False in [False]) # makes sense
False
>>> False == False in [False] # now what?
True

>>> True is False == False
False
>>> False is False is False
True

>>> 1 > 0 < 1
True
>>> (1 > 0) < 1
False
>>> 1 > (0 < 1)
False
```

#### 💡 Erklärung:

Zitat von https://docs.python.org/3/reference/expressions.html#comparisons

> Formally, if a, b, c, ..., y, z are expressions and op1, op2, ..., opN are comparison operators, then a op1 b op2 c ... y opN z is equivalent to a op1 b and b op2 c and ... y opN z, except that each expression is evaluated at most once.

Übersetzt:

> Formal ausgedrückt: wenn a, b, c, ..., y, z Ausdrücke und op1, op2, ..., opN Vergleichsoperatoren sind, dann sind a op1 b op2 c ... y opN z äquivalent zu a op1 b and b op2 c and ... y opN z, mit der Ausnahme, dass jeder Ausdruck höchstens einmal ausgewertet wird.


Während dieses Verhalten in den Beispielen vielleicht unsinnig erscheint, kann es super verwendet werden, z.B. `a == b == c` und `0 <= x <= 100`.

* `False is False is False` ist äquivalent zu `(False is False) and (False is False)`
* `True is False == False` ist äquivalent zu `(True is False) and (False == False)` und während der erste Teil des Statements (`True is False`) zu `False` ausgewertet wird, wird der gesamt Ausdruck zu `False` ausgewertet.
* `1 > 0 < 1` ist äquivalent zu `(1 > 0) and (0 < 1)` which evaluates to `True`.
* Der Ausdruck `(1 > 0) < 1` ist äquivalent zu `True < 1` und
  ```py
  >>> int(True)
  1
  >>> True + 1 # Nicht relevant für dieses Beispiel, aber trotzdem nur zum Spaß
  2
  ```
  So wird `1 < 1` zu `False` ausgewertet

---

### ▶ Wie man den `is` Operator nicht nutzt
<!-- Example ID: 230fa2ac-ab36-4ad1-b675-5f5a1c1a6217 --->
Das folgende Beispiel ist im Internet überall bekannt.

1\.

```py
>>> a = 256
>>> b = 256
>>> a is b
True

>>> a = 257
>>> b = 257
>>> a is b
False
```

2\.

```py
>>> a = []
>>> b = []
>>> a is b
False

>>> a = tuple()
>>> b = tuple()
>>> a is b
True
```

3\.
**Ausgabe**

```py
>>> a, b = 257, 257
>>> a is b
True
```

**Ausgabe (Python 3.7.x spezifisch)**

```py
>>> a, b = 257, 257
>>> a is b
False
```

#### 💡 Erklärung:

**Der Unterschied zwischen `is` und `==`**

* `is` Operator checkt, ob sich beide Operanden auf dasselbe Objekt beziehen (i.e., it checks if the identity of the operands matches or not).
* `==` Operator vergleicht die Werte der beiden Operanden und überprüft, ob diese gleich sind.
* Also `is` wird für Beziehungsgleichheit und `==` für Wertgleichheit benutzt. Ein Beispiel, um das Gesagte zu vertiefen:
  ```py
  >>> class A: pass
  >>> A() is A() # Das sind zwei leere Objekte an zwei verschiedenen Orten im Speicher.
  False
  ```

**`256` ist ein existierendes Objekt, aber `257` nicht**

Wenn du Python startest, werden die Nummern von `-5` bis `256` bereitgestellt. Diese Nummern werden sehr oft benutzt, also ergibt es Sinn,
sie schnell bereit zu haben.

Zitat von https://docs.python.org/3/c-api/long.html
> The current implementation keeps an array of integer objects for all integers between -5 and 256, when you create an int in that range you just get back a reference to the existing object. So it should be possible to change the value of 1. I suspect the behavior of Python, in this case, is undefined. :-)

Übersetzung:
> Die momentane Implementation stellt ein Array aus Integer-Objekten für alle Integer zwischen -5 und 256 bereit. Wenn du einen int in diesem Bereich erstellst, bekommst du nur eine Referenz auf das existierende Objekt zurück. Also sollte es möglich sein, den Wert von 1 zu ändern. Ich vermute das Verhalten von Python ist in diesem Fall undefiniert. :-)


```py
>>> id(256)
10922528
>>> a = 256
>>> b = 256
>>> id(a)
10922528
>>> id(b)
10922528
>>> id(257)
140084850247312
>>> x = 257
>>> y = 257
>>> id(x)
140084850247440
>>> id(y)
140084850247344
```

Hier ist der Interpreter nicht schlau genug während des Ausführens von `y = 257` zu erkennen, dass wir bereits ein Integer mit dem Wert `257` erstellt haben und daher wird ein neues Objekt im Speicher angelegt.

Ähnliche Optimierungen treffen auf andere **immutable** Objekte zu, z.B. leere Tuples. Da Listen mutable sind, wird `[] is []` zu `False` ausgewertet und `() is ()` wird zu `True` ausgewertet. Das erklärt unser zweiter Schnipsel. Lass uns mit dem dritten Beispiell weiter machen: 

**Sowohl `a` und `b` beziehen sich auf dasselbe Objekt wenn sie in derselben Zeile mit demselben Wert initialisiert werden.**

**Ausgabe**

```py
>>> a, b = 257, 257
>>> id(a)
140640774013296
>>> id(b)
140640774013296
>>> a = 257
>>> b = 257
>>> id(a)
140640774013392
>>> id(b)
140640774013488
```

* Wenn a und b in derselben Zeile auf `257` gesetzt werden, erstellt der Python Interpreter ein neues Objekt, und referenziert die zweite Variable
zur selben Zeit. Wenn man es in verschiedenen Zeilen macht, dann weiß Python nicht, dass eine `257` als Objekt schon existiert.

* Es ist eine Compiler Optimierung, die speziell für die interaktive Umgebung gilt. Wenn man zwei Zeilen in einem Live Interpreter eingibt, dann
werden sie getrennt kompiliert und auch getrennt optimiert. Wenn du dieses Beispiel in einer `.py` Datei ausprobierst, würdest du nicht dasselbe
Verhalten beobachten, denn die Datei wird auf einmal kompiliert. Diese Optimierung ist nicht auf Integer beschränkt, sie funktioniert auch für
andere immutable Datentypen, wie z.B. Strings (siehe auch das Beispiel "Strings können manchmal schwierig sein") oder floats:

  ```py
  >>> a, b = 257.0, 257.0
  >>> a is b
  True
  ```

* Warum funktioniert das nicht in Python 3.7 ? Die abstrakte Antwort ist: Die Compiler Optimierungen sind von der Implementierung abhängig (es verändert sich mit der Version, dem Betriebssystem, etc.). Ich versuche noch herauszufinden, welche Implementierungsänderung dieses Problem
verursacht. Für Updates, schaue dieses [Issue](https://github.com/satwikkansal/wtfpython/issues/100) an.

---


### ▶ Hash brownies
<!-- Example ID: eb17db53-49fd-4b61-85d6-345c5ca213ff --->
1\.
```py
some_dict = {}
some_dict[5.5] = "JavaScript"
some_dict[5.0] = "Ruby"
some_dict[5] = "Python"
```

**Ausgabe:**

```py
>>> some_dict[5.5]
"JavaScript"
>>> some_dict[5.0] # "Python" hat die Existenz von "Ruby" ausgelöscht ?
"Python"
>>> some_dict[5] 
"Python"

>>> complex_five = 5 + 0j
>>> type(complex_five)
complex
>>> some_dict[complex_five]
"Python"
```

Warum also ist Python überall zu finden ?


#### 💡 Erklärung

* Uniqueness of keys in a Python dictionary is by *equivalence*, not identity. So even though `5`, `5.0`, and `5 + 0j` are distinct objects of different types, since they're equal, they can't both be in the same `dict` (or `set`). As soon as you insert any one of them, attempting to look up any distinct but equivalent key will succeed with the original mapped value (rather than failing with a `KeyError`):
  ```py
  >>> 5 == 5.0 == 5 + 0j
  True
  >>> 5 is not 5.0 is not 5 + 0j
  True
  >>> some_dict = {}
  >>> some_dict[5.0] = "Ruby"
  >>> 5.0 in some_dict
  True
  >>> (5 in some_dict) and (5 + 0j in some_dict)
  True
  ```
* This applies when setting an item as well. So when you do `some_dict[5] = "Python"`, Python finds the existing item with equivalent key `5.0 -> "Ruby"`, overwrites its value in place, and leaves the original key alone.
  ```py
  >>> some_dict
  {5.0: 'Ruby'}
  >>> some_dict[5] = "Python"
  >>> some_dict
  {5.0: 'Python'}
  ```
* So how can we update the key to `5` (instead of `5.0`)? We can't actually do this update in place, but what we can do is first delete the key (`del some_dict[5.0]`), and then set it (`some_dict[5]`) to get the integer `5` as the key instead of floating `5.0`, though this should be needed in rare cases.

* How did Python find `5` in a dictionary containing `5.0`? Python does this in constant time without having to scan through every item by using hash functions. When Python looks up a key `foo` in a dict, it first computes `hash(foo)` (which runs in constant-time). Since in Python it is required that objects that compare equal also have the same hash value ([docs](https://docs.python.org/3/reference/datamodel.html#object.__hash__) here), `5`, `5.0`, and `5 + 0j` have the same hash value.
  ```py
  >>> 5 == 5.0 == 5 + 0j
  True
  >>> hash(5) == hash(5.0) == hash(5 + 0j)
  True
  ```
  **Note:** Das Inverse ist nicht unbedingt wahr: Objekte mit gleichem Hashwert können evtl. ungleich sein. (Das versursacht was auch als [hash collision](https://de.wikipedia.org/wiki/Kollisionsresistenz) bekannt ist), und und verschlechtert die zeitlich konstante Leistung, die Hashing normalerweise bietet.

---

### ▶ Tief im Inneren sind wir alle gleich
<!-- Example ID: 8f99a35f-1736-43e2-920d-3b78ec35da9b --->
```py
class WTF:
  pass
```

**Ausgabe:**
```py
>>> WTF() == WTF() # two different instances can't be equal
False
>>> WTF() is WTF() # identities are also different
False
>>> hash(WTF()) == hash(WTF()) # hashes _should_ be different as well
True
>>> id(WTF()) == id(WTF())
True
```

#### 💡 Erklärung:

* When `id` was called, Python created a `WTF` class object and passed it to the `id` function. The `id` function takes its `id` (its memory location), and throws away the object. The object is destroyed.
* When we do this twice in succession, Python allocates the same memory location to this second object as well. Since (in CPython) `id` uses the memory location as the object id, the id of the two objects is the same.
* So, the object's id is unique only for the lifetime of the object. After the object is destroyed, or before it is created, something else can have the same id.
* But why did the `is` operator evaluate to `False`? Let's see with this snippet.
  ```py
  class WTF(object):
    def __init__(self): print("I")
    def __del__(self): print("D")
  ```

  **Ausgabe:**
  ```py
  >>> WTF() is WTF()
  I
  I
  D
  D
  False
  >>> id(WTF()) == id(WTF())
  I
  D
  I
  D
  True
  ```
  As you may observe, the order in which the objects are destroyed is what made all the difference here.

---

### ▶ Unordnung in der Ordnung *
<!-- Example ID: 91bff1f8-541d-455a-9de4-6cd8ff00ea66 --->
```py
from collections import OrderedDict

dictionary = dict()
dictionary[1] = 'a'; dictionary[2] = 'b';

ordered_dict = OrderedDict()
ordered_dict[1] = 'a'; ordered_dict[2] = 'b';

another_ordered_dict = OrderedDict()
another_ordered_dict[2] = 'b'; another_ordered_dict[1] = 'a';

class DictWithHash(dict):
    """
    A dict that also implements __hash__ magic.
    """
    __hash__ = lambda self: 0

class OrderedDictWithHash(OrderedDict):
    """
    An OrderedDict that also implements __hash__ magic.
    """
    __hash__ = lambda self: 0
```

**Ausgabe**
```py
>>> dictionary == ordered_dict # If a == b
True
>>> dictionary == another_ordered_dict # and b == c
True
>>> ordered_dict == another_ordered_dict # then why isn't c == a ??
False

# We all know that a set consists of only unique elements,
# let's try making a set of these dictionaries and see what happens...

>>> len({dictionary, ordered_dict, another_ordered_dict})
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: unhashable type: 'dict'

# Makes sense since dict don't have __hash__ implemented, let's use
# our wrapper classes.
>>> dictionary = DictWithHash()
>>> dictionary[1] = 'a'; dictionary[2] = 'b';
>>> ordered_dict = OrderedDictWithHash()
>>> ordered_dict[1] = 'a'; ordered_dict[2] = 'b';
>>> another_ordered_dict = OrderedDictWithHash()
>>> another_ordered_dict[2] = 'b'; another_ordered_dict[1] = 'a';
>>> len({dictionary, ordered_dict, another_ordered_dict})
1
>>> len({ordered_dict, another_ordered_dict, dictionary}) # changing the order
2
```

Was geht hier vor ?

#### 💡 Erklärung:

- The reason why intransitive equality didn't hold among `dictionary`, `ordered_dict` and `another_ordered_dict` is because of the way `__eq__` method is implemented in `OrderedDict` class. From the [docs](https://docs.python.org/3/library/collections.html#ordereddict-objects)
  
    > Equality tests between OrderedDict objects are order-sensitive and are implemented as `list(od1.items())==list(od2.items())`. Equality tests between `OrderedDict` objects and other Mapping objects are order-insensitive like regular dictionaries.
- The reason for this equality in behavior is that it allows `OrderedDict` objects to be directly substituted anywhere a regular dictionary is used.
- Okay, so why did changing the order affect the length of the generated `set` object? The answer is the lack of intransitive equality only. Since sets are "unordered" collections of unique elements, the order in which elements are inserted shouldn't matter. But in this case, it does matter. Let's break it down a bit,
    ```py
    >>> some_set = set()
    >>> some_set.add(dictionary) # these are the mapping objects from the snippets above
    >>> ordered_dict in some_set
    True
    >>> some_set.add(ordered_dict)
    >>> len(some_set)
    1
    >>> another_ordered_dict in some_set
    True
    >>> some_set.add(another_ordered_dict)
    >>> len(some_set)
    1

    >>> another_set = set()
    >>> another_set.add(ordered_dict)
    >>> another_ordered_dict in another_set
    False
    >>> another_set.add(another_ordered_dict)
    >>> len(another_set)
    2
    >>> dictionary in another_set
    True
    >>> another_set.add(another_ordered_dict)
    >>> len(another_set)
    2
    ```
    So the inconsistency is due to `another_ordered_dict in another_set` being `False` because `ordered_dict` was already present in `another_set` and as observed before, `ordered_dict == another_ordered_dict` is `False`.

---

### ▶ Versuche es weiter... *
<!-- Example ID: b4349443-e89f-4d25-a109-82616be9d41a --->
```py
def some_func():
    try:
        return 'from_try'
    finally:
        return 'from_finally'

def another_func(): 
    for _ in range(3):
        try:
            continue
        finally:
            print("Finally!")

def one_more_func(): # A gotcha!
    try:
        for i in range(3):
            try:
                1 / i
            except ZeroDivisionError:
                # Let's throw it here and handle it outside for loop
                raise ZeroDivisionError("A trivial divide by zero error")
            finally:
                print("Iteration", i)
                break
    except ZeroDivisionError as e:
        print("Zero division error occurred", e)
```

**Ausgabe:**

```py
>>> some_func()
'from_finally'

>>> another_func()
Finally!
Finally!
Finally!

>>> 1 / 0
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ZeroDivisionError: division by zero

>>> one_more_func()
Iteration 0

```

#### 💡 Erklärung:

- When a `return`, `break` or `continue` statement is executed in the `try` suite of a "try…finally" statement, the `finally` clause is also executed on the way out.
- The return value of a function is determined by the last `return` statement executed. Since the `finally` clause always executes, a `return` statement executed in the `finally` clause will always be the last one executed.
- The caveat here is, if the finally clause executes a `return` or `break` statement, the temporarily saved exception is discarded.

---


### ▶ Wofür?
<!-- Example ID: 64a9dccf-5083-4bc9-98aa-8aeecde4f210 --->
```py
some_string = "wtf"
some_dict = {}
for i, some_dict[i] in enumerate(some_string):
    i = 10
```

**Ausgabe:**
```py
>>> some_dict # An indexed dict appears.
{0: 'w', 1: 't', 2: 'f'}
```

####  💡 Erklärung:

* A `for` statement is defined in the [Python grammar](https://docs.python.org/3/reference/grammar.html) as:
  ```
  for_stmt: 'for' exprlist 'in' testlist ':' suite ['else' ':' suite]
  ```
  Where `exprlist` is the assignment target. This means that the equivalent of `{exprlist} = {next_value}` is **executed for each item** in the iterable.
  An interesting example that illustrates this:
  ```py
  for i in range(4):
      print(i)
      i = 10
  ```

  **Ausgabe:**
  ```
  0
  1
  2
  3
  ```

  Hast du erwartet, dass die Schleife nur einmal läuft ?

  **💡 Erklärung:**

  - The assignment statement `i = 10` never affects the iterations of the loop because of the way for loops work in Python. Before the beginning of every iteration, the next item provided by the iterator (`range(4)` in this case) is unpacked and assigned the target list variables (`i` in this case).

* The `enumerate(some_string)` function yields a new value `i` (a counter going up) and a character from the `some_string` in each iteration. It then sets the (just assigned) `i` key of the dictionary `some_dict` to that character. The unrolling of the loop can be simplified as:
  ```py
  >>> i, some_dict[i] = (0, 'w')
  >>> i, some_dict[i] = (1, 't')
  >>> i, some_dict[i] = (2, 'f')
  >>> some_dict
  ```

---

### ▶ Diskrepanz in der Auswertungszeit
<!-- Example ID: 6aa11a4b-4cf1-467a-b43a-810731517e98 --->
1\.
```py
array = [1, 8, 15]
# A typical generator expression
gen = (x for x in array if array.count(x) > 0)
array = [2, 8, 22]
```

**Ausgabe:**

```py
>>> print(list(gen)) # Where did the other values go?
[8]
```

2\.

```py
array_1 = [1,2,3,4]
gen_1 = (x for x in array_1)
array_1 = [1,2,3,4,5]

array_2 = [1,2,3,4]
gen_2 = (x for x in array_2)
array_2[:] = [1,2,3,4,5]
```

**Ausgabe:**
```py
>>> print(list(gen_1))
[1, 2, 3, 4]

>>> print(list(gen_2))
[1, 2, 3, 4, 5]
```

3\.

```py
array_3 = [1, 2, 3]
array_4 = [10, 20, 30]
gen = (i + j for i in array_3 for j in array_4)

array_3 = [4, 5, 6]
array_4 = [400, 500, 600]
```

**Ausgabe:**
```py
>>> print(list(gen))
[401, 501, 601, 402, 502, 602, 403, 503, 603]
```

#### 💡 Erklärung

- In a [generator](https://wiki.python.org/moin/Generators) expression, the `in` clause is evaluated at declaration time, but the conditional clause is evaluated at runtime.
- So before runtime, `array` is re-assigned to the list `[2, 8, 22]`, and since out of `1`, `8` and `15`, only the count of `8` is greater than `0`, the generator only yields `8`.
- The differences in the Ausgabe of `g1` and `g2` in the second part is due the way variables `array_1` and `array_2` are re-assigned values.
- In the first case, `array_1` is bound to the new object `[1,2,3,4,5]` and since the `in` clause is evaluated at the declaration time it still refers to the old object `[1,2,3,4]` (which is not destroyed).
- In the second case, the slice assignment to `array_2` updates the same old object `[1,2,3,4]` to `[1,2,3,4,5]`. Hence both the `g2` and `array_2` still have reference to the same object (which has now been updated to `[1,2,3,4,5]`).
- Okay, going by the logic discussed so far, shouldn't be the value of `list(gen)` in the third snippet be `[11, 21, 31, 12, 22, 32, 13, 23, 33]`? (because `array_3` and `array_4` are going to behave just like `array_1`). The reason why (only) `array_4` values got updated is explained in [PEP-289](https://www.python.org/dev/peps/pep-0289/#the-details)
  
    > Only the outermost for-expression is evaluated immediately, the other expressions are deferred until the generator is run.

---


### ▶ `is not ...` ist nicht `is (not ...)`
<!-- Example ID: b26fb1ed-0c7d-4b9c-8c6d-94a58a055c0d --->
```py
>>> 'something' is not None
True
>>> 'something' is (not None)
False
```

#### 💡 Erklärung

- `is not` is a single binary operator, and has behavior different than using `is` and `not` separated.
- `is not` evaluates to `False` if the variables on either side of the operator point to the same object and `True` otherwise. 
- In the example, `(not None)` evaluates to `True` since the value `None` is `False` in a boolean context, so the expression becomes `'something' is True`.

---

### ▶ Ein tic-tac-toe wo X im ersten Versuch gewinnt!
<!-- Example ID: 69329249-bdcb-424f-bd09-cca2e6705a7a --->

```py
# Let's initialize a row
row = [""] * 3 #row i['', '', '']
# Let's make a board
board = [row] * 3
```

**Ausgabe:**

```py
>>> board
[['', '', ''], ['', '', ''], ['', '', '']]
>>> board[0]
['', '', '']
>>> board[0][0]
''
>>> board[0][0] = "X"
>>> board
[['X', '', ''], ['X', '', ''], ['X', '', '']]
```

We didn't assign three `"X"`s, did we?

#### 💡 Erklärung:

When we initialize `row` variable, this visualization explains what happens in the memory

![image](/images/tic-tac-toe/after_row_initialized.png)

And when the `board` is initialized by multiplying the `row`, this is what happens inside the memory (each of the elements `board[0]`, `board[1]` and `board[2]` is a reference to the same list referred by `row`)

![image](/images/tic-tac-toe/after_board_initialized.png)

We can avoid this scenario here by not using `row` variable to generate `board`. (Asked in [this](https://github.com/satwikkansal/wtfpython/issues/68) issue).

```py
>>> board = [['']*3 for _ in range(3)]
>>> board[0][0] = "X"
>>> board
[['X', '', ''], ['', '', ''], ['', '', '']]
```

---

### ▶ Schrödingers Variable *
<!-- Example ID: 4dc42f77-94cb-4eb5-a120-8203d3ed7604 --->


```py
funcs = []
results = []
for x in range(7):
    def some_func():
        return x
    funcs.append(some_func)
    results.append(some_func())  # note the function call here

funcs_results = [func() for func in funcs]
```

**Ausgabe (Python version):**
```py
>>> results
[0, 1, 2, 3, 4, 5, 6]
>>> funcs_results
[6, 6, 6, 6, 6, 6, 6]
```

The values of `x` were different in every iteration prior to appending `some_func` to `funcs`, but all the functions return 6 when they're evaluated after the loop completes.

2.

```py
>>> powers_of_x = [lambda x: x**i for i in range(10)]
>>> [f(2) for f in powers_of_x]
[512, 512, 512, 512, 512, 512, 512, 512, 512, 512]
```

#### 💡 Erklärung:
* When defining a function inside a loop that uses the loop variable in its body, the loop function's closure is bound to the *variable*, not its *value*. The function looks up `x` in the surrounding context, rather than using the value of `x` at the time the function is created. So all of the functions use the latest value assigned to the variable for computation. We can see that it's using the `x` from the surrounding context (i.e. *not* a local variable) with:
```py
>>> import inspect
>>> inspect.getclosurevars(funcs[0])
ClosureVars(nonlocals={}, globals={'x': 6}, builtins={}, unbound=set())
```
Since `x` is a global value, we can change the value that the `funcs` will lookup and return by updating `x`:

```py
>>> x = 42
>>> [func() for func in funcs]
[42, 42, 42, 42, 42, 42, 42]
```

* To get the desired behavior you can pass in the loop variable as a named variable to the function. **Why does this work?** Because this will define the variable *inside* the function's scope. It will no longer go to the surrounding (global) scope to look up the variables value but will create a local variable that stores the value of `x` at that point in time.

```py
funcs = []
for x in range(7):
    def some_func(x=x):
        return x
    funcs.append(some_func)
```

**Ausgabe:**

```py
>>> funcs_results = [func() for func in funcs]
>>> funcs_results
[0, 1, 2, 3, 4, 5, 6]
```

It is not longer using the `x` in the global scope:

```py
>>> inspect.getclosurevars(funcs[0])
ClosureVars(nonlocals={}, globals={}, builtins={}, unbound=set())
```

---

### ▶ Das Henne-Ei-Problem *
<!-- Example ID: 60730dc2-0d79-4416-8568-2a63323b3ce8 --->
1\.
```py
>>> isinstance(3, int)
True
>>> isinstance(type, object)
True
>>> isinstance(object, type)
True
```

So which is the "ultimate" base class? There's more to the confusion by the way,

2\. 

```py
>>> class A: pass
>>> isinstance(A, A)
False
>>> isinstance(type, type)
True
>>> isinstance(object, object)
True
```

3\.

```py
>>> issubclass(int, object)
True
>>> issubclass(type, object)
True
>>> issubclass(object, type)
False
```


#### 💡 Erklärung

- `type` is a [metaclass](https://realpython.com/python-metaclasses/) in Python.
- **Everything** is an `object` in Python, which includes classes as well as their objects (instances).
- class `type` is the metaclass of class `object`, and every class (including `type`) has inherited directly or indirectly from `object`.
- There is no real base class among `object` and `type`. The confusion in the above snippets is arising because we're thinking about these relationships (`issubclass` and `isinstance`) in terms of Python classes. The relationship between `object` and `type` can't be reproduced in pure python. To be more precise the following relationships can't be reproduced in pure Python,
    + class A is an instance of class B, and class B is an instance of class A.
    + class A is an instance of itself.
- These relationships between `object` and `type` (both being instances of each other as well as themselves) exist in Python because of "cheating" at the implementation level.

---

### ▶ Beziehungen in Unterklassen
<!-- Example ID: 9f6d8cf0-e1b5-42d0-84a0-4cfab25a0bc0 --->
**Ausgabe:**
```py
>>> from collections import Hashable
>>> issubclass(list, object)
True
>>> issubclass(object, Hashable)
True
>>> issubclass(list, Hashable)
False
```

The Subclass relationships were expected to be transitive, right? (i.e., if `A` is a subclass of `B`, and `B` is a subclass of `C`, the `A` _should_ a subclass of `C`)

#### 💡 Erklärung:

* Subclass relationships are not necessarily transitive in Python. Anyone is allowed to define their own, arbitrary `__subclasscheck__` in a metaclass.
* When `issubclass(cls, Hashable)` is called, it simply looks for non-Falsey "`__hash__`" method in `cls` or anything it inherits from.
* Since `object` is hashable, but `list` is non-hashable, it breaks the transitivity relation.
* More detailed Erklärung can be found [here](https://www.naftaliharris.com/blog/python-subclass-intransitivity/).

---

### ▶ Methodengleichheit und -identität
<!-- Example ID: 94802911-48fe-4242-defa-728ae893fa32 --->

1.
```py
class SomeClass:
    def method(self):
        pass

    @classmethod
    def classm(cls):
        pass

    @staticmethod
    def staticm():
        pass
```

**Ausgabe:**
```py
>>> print(SomeClass.method is SomeClass.method)
True
>>> print(SomeClass.classm is SomeClass.classm)
False
>>> print(SomeClass.classm == SomeClass.classm)
True
>>> print(SomeClass.staticm is SomeClass.staticm)
True
```

Accessing `classm` twice, we get an equal object, but not the *same* one? Let's see what happens
with instances of `SomeClass`:

2.
```py
o1 = SomeClass()
o2 = SomeClass()
```

**Ausgabe:**
```py
>>> print(o1.method == o2.method)
False
>>> print(o1.method == o1.method)
True
>>> print(o1.method is o1.method)
False
>>> print(o1.classm is o1.classm)
False
>>> print(o1.classm == o1.classm == o2.classm == SomeClass.classm)
True
>>> print(o1.staticm is o1.staticm is o2.staticm is SomeClass.staticm)
True
```

Accessing` classm` or `method` twice, creates equal but not *same* objects for the same instance of `SomeClass`.

#### 💡 Erklärung
* Functions are [descriptors](https://docs.python.org/3/howto/descriptor.html). Whenever a function is accessed as an
attribute, the descriptor is invoked, creating a method object which "binds" the function with the object owning the
attribute. If called, the method calls the function, implicitly passing the bound object as the first argument
(this is how we get `self` as the first argument, despite not passing it explicitly).
```py
>>> o1.method
<bound method SomeClass.method of <__main__.SomeClass object at ...>>
```
* Accessing the attribute multiple times creates a method object every time! Therefore `o1.method is o1.method` is
never truthy. Accessing functions as class attributes (as opposed to instance) does not create methods, however; so
`SomeClass.method is SomeClass.method` is truthy.
```py
>>> SomeClass.method
<function SomeClass.method at ...>
```
* `classmethod` transforms functions into class methods. Class methods are descriptors that, when accessed, create
a method object which binds the *class* (type) of the object, instead of the object itself.
```py
>>> o1.classm
<bound method SomeClass.classm of <class '__main__.SomeClass'>>
```
* Unlike functions, `classmethod`s will create a method also when accessed as class attributes (in which case they
bind the class, not to the type of it). So `SomeClass.classm is SomeClass.classm` is falsy.
```py
>>> SomeClass.classm
<bound method SomeClass.classm of <class '__main__.SomeClass'>>
```
* A method object compares equal when both the functions are equal, and the bound objects are the same. So
`o1.method == o1.method` is truthy, although not the same object in memory.
* `staticmethod` transforms functions into a "no-op" descriptor, which returns the function as-is. No method
objects are ever created, so comparison with `is` is truthy.
```py
>>> o1.staticm
<function SomeClass.staticm at ...>
>>> SomeClass.staticm
<function SomeClass.staticm at ...>
```
* Having to create new "method" objects every time Python calls instance methods and having to modify the arguments
every time in order to insert `self` affected performance badly.
CPython 3.7 [solved it](https://bugs.python.org/issue26110) by introducing new opcodes that deal with calling methods
without creating the temporary method objects. This is used only when the accessed function is actually called, so the
snippets here are not affected, and still generate methods :)

### ▶ All-true-ation *

<!-- Example ID: dfe6d845-e452-48fe-a2da-0ed3869a8042 -->

```py
>>> all([True, True, True])
True
>>> all([True, True, False])
False

>>> all([])
True
>>> all([[]])
False
>>> all([[[]]])
True
```

Why's this True-False alteration?

#### 💡 Erklärung:

- The implementation of `all` function is equivalent to

- ```py
  def all(iterable):
      for element in iterable:
          if not element:
              return False
      return True
  ```

- `all([])` returns `True` since the iterable is empty. 
- `all([[]])` returns `False` because the passed array has one element, `[]`, and in python, an empty list is falsy.
- `all([[[]]])` and higher recursive variants are always `True`. This is because the passed array's single element (`[[...]]`) is no longer empty, and lists with values are truthy.

---

### ▶ Das überraschende Komma
<!-- Example ID: 31a819c8-ed73-4dcc-84eb-91bedbb51e58 --->
**Ausgabe (< 3.6):**

```py
>>> def f(x, y,):
...     print(x, y)
...
>>> def g(x=4, y=5,):
...     print(x, y)
...
>>> def h(x, **kwargs,):
  File "<stdin>", line 1
    def h(x, **kwargs,):
                     ^
SyntaxError: invalid syntax

>>> def h(*args,):
  File "<stdin>", line 1
    def h(*args,):
                ^
SyntaxError: invalid syntax
```

#### 💡 Erklärung:

- Trailing comma is not always legal in formal parameters list of a Python function.
-  In Python, the argument list is defined partially with leading commas and partially with trailing commas. This conflict causes situations where a comma is trapped in the middle, and no rule accepts it.
-  **Note:** The trailing comma problem is [fixed in Python 3.6](https://bugs.python.org/issue9232). The remarks in [this](https://bugs.python.org/issue9232#msg248399) post discuss in brief different usages of trailing commas in Python.

---

### ▶ Strings und die Backslashes
<!-- Example ID: 6ae622c3-6d99-4041-9b33-507bd1a4407b --->
**Ausgabe:**
```py
>>> print("\"")
"

>>> print(r"\"")
\"

>>> print(r"\")
File "<stdin>", line 1
    print(r"\")
              ^
SyntaxError: EOL while scanning string literal

>>> r'\'' == "\\'"
True
```

#### 💡 Erklärung

- In a usual python string, the backslash is used to escape characters that may have a special meaning (like single-quote, double-quote, and the backslash itself).
    ```py
    >>> "wt\"f"
    'wt"f'
    ```
- In a raw string literal (as indicated by the prefix `r`),  the backslashes pass themselves as is along with the behavior of escaping the following character.
    ```py
    >>> r'wt\"f' == 'wt\\"f'
    True
    >>> print(repr(r'wt\"f')
    'wt\\"f'

    >>> print("\n")

    >>> print(r"\\n")
    '\\n'
    ```
- This means when a parser encounters a backslash in a raw string, it expects another character following it. And in our case (`print(r"\")`), the backslash escaped the trailing quote, leaving the parser without a terminating quote (hence the `SyntaxError`). That's why backslashes don't work at the end of a raw string.

---

### ▶ not knot!
<!-- Example ID: 7034deb1-7443-417d-94ee-29a800524de8 --->
```py
x = True
y = False
```

**Ausgabe:**
```py
>>> not x == y
True
>>> x == not y
  File "<input>", line 1
    x == not y
           ^
SyntaxError: invalid syntax
```

#### 💡 Erklärung:

* Operator precedence affects how an expression is evaluated, and `==` operator has higher precedence than `not` operator in Python.
* So `not x == y` is equivalent to `not (x == y)` which is equivalent to `not (True == False)` finally evaluating to `True`.
* But `x == not y` raises a `SyntaxError` because it can be thought of being equivalent to `(x == not) y` and not `x == (not y)` which you might have expected at first sight.
* The parser expected the `not` token to be a part of the `not in` operator (because both `==` and `not in` operators have the same precedence), but after not being able to find an `in` token following the `not` token, it raises a `SyntaxError`.

---

### ▶ Halbe Zeichenketten in dreifachen Anführungszeichen
<!-- Example ID: c55da3e2-1034-43b9-abeb-a7a970a2ad9e --->
**Ausgabe:**
```py
>>> print('wtfpython''')
wtfpython
>>> print("wtfpython""")
wtfpython
>>> # The following statements raise `SyntaxError`
>>> # print('''wtfpython')
>>> # print("""wtfpython")
  File "<input>", line 3
    print("""wtfpython")
                        ^
SyntaxError: EOF while scanning triple-quoted string literal
```

#### 💡 Erklärung:
+ Python supports implicit [string literal concatenation](https://docs.python.org/3/reference/lexical_analysis.html#string-literal-concatenation), Example,
  ```
  >>> print("wtf" "python")
  wtfpython
  >>> print("wtf" "") # or "wtf"""
  wtf
  ```
+ `'''` and `"""` are also string delimiters in Python which causes a SyntaxError because the Python interpreter was expecting a terminating triple quote as delimiter while scanning the currently encountered triple quoted string literal.

---

### ▶ Was ist falsch an booleans?
<!-- Example ID: 0bba5fa7-9e6d-4cd2-8b94-952d061af5dd --->
1\.

```py
# A simple example to count the number of booleans and
# integers in an iterable of mixed data types.
mixed_list = [False, 1.0, "some_string", 3, True, [], False]
integers_found_so_far = 0
booleans_found_so_far = 0

for item in mixed_list:
    if isinstance(item, int):
        integers_found_so_far += 1
    elif isinstance(item, bool):
        booleans_found_so_far += 1
```

**Ausgabe:**
```py
>>> integers_found_so_far
4
>>> booleans_found_so_far
0
```


2\.
```py
>>> some_bool = True
>>> "wtf" * some_bool
'wtf'
>>> some_bool = False
>>> "wtf" * some_bool
''
```

3\.

```py
def tell_truth():
    True = False
    if True == False:
        print("I have lost faith in truth!")
```

**Ausgabe (< 3.x):**

```py
>>> tell_truth()
I have lost faith in truth!
```



#### 💡 Erklärung:

* `bool` is a subclass of `int` in Python
    
    ```py
    >>> issubclass(bool, int)
    True
    >>> issubclass(int, bool)
    False
    ```
    
* And thus, `True` and `False` are instances of `int`
  ```py
  >>> isinstance(True, int)
  True
  >>> isinstance(False, int)
  True
  ```

* The integer value of `True` is `1` and that of `False` is `0`.
  ```py
  >>> int(True)
  1
  >>> int(False)
  0
  ```

* See this StackOverflow [answer](https://stackoverflow.com/a/8169049/4354153) for the rationale behind it.

* Initially, Python used to have no `bool` type (people used 0 for false and non-zero value like 1 for true).  `True`, `False`, and a `bool` type was added in 2.x versions, but, for backward compatibility, `True` and `False` couldn't be made constants. They just were built-in variables, and it was possible to reassign them

* Python 3 was backward-incompatible, the issue was finally fixed, and thus the last snippet won't work with Python 3.x!

---

### ▶ Klassen- und Instanzattribute
<!-- Example ID: 6f332208-33bd-482d-8106-42863b739ed9 --->
1\.
```py
class A:
    x = 1

class B(A):
    pass

class C(A):
    pass
```

**Ausgabe:**
```py
>>> A.x, B.x, C.x
(1, 1, 1)
>>> B.x = 2
>>> A.x, B.x, C.x
(1, 2, 1)
>>> A.x = 3
>>> A.x, B.x, C.x # C.x changed, but B.x didn't
(3, 2, 3)
>>> a = A()
>>> a.x, A.x
(3, 3)
>>> a.x += 1
>>> a.x, A.x
(4, 3)
```

2\.
```py
class SomeClass:
    some_var = 15
    some_list = [5]
    another_list = [5]
    def __init__(self, x):
        self.some_var = x + 1
        self.some_list = self.some_list + [x]
        self.another_list += [x]
```

**Ausgabe:**

```py
>>> some_obj = SomeClass(420)
>>> some_obj.some_list
[5, 420]
>>> some_obj.another_list
[5, 420]
>>> another_obj = SomeClass(111)
>>> another_obj.some_list
[5, 111]
>>> another_obj.another_list
[5, 420, 111]
>>> another_obj.another_list is SomeClass.another_list
True
>>> another_obj.another_list is some_obj.another_list
True
```

#### 💡 Erklärung:

* Class variables and variables in class instances are internally handled as dictionaries of a class object. If a variable name is not found in the dictionary of the current class, the parent classes are searched for it.
* The `+=` operator modifies the mutable object in-place without creating a new object. So changing the attribute of one instance affects the other instances and the class attribute as well.

---

### ▶ yielding None
<!-- Example ID: 5a40c241-2c30-40d0-8ba9-cf7e097b3b53 --->
```py
some_iterable = ('a', 'b')

def some_func(val):
    return "something"
```

**Ausgabe (<= 3.7.x):**

```py
>>> [x for x in some_iterable]
['a', 'b']
>>> [(yield x) for x in some_iterable]
<generator object <listcomp> at 0x7f70b0a4ad58>
>>> list([(yield x) for x in some_iterable])
['a', 'b']
>>> list((yield x) for x in some_iterable)
['a', None, 'b', None]
>>> list(some_func((yield x)) for x in some_iterable)
['a', 'something', 'b', 'something']
```

#### 💡 Erklärung:
- This is a bug in CPython's handling of `yield` in generators and comprehensions.
- Quelle and Erklärung can be found here: https://stackoverflow.com/questions/32139885/yield-in-list-comprehensions-and-generator-expressions
- Related bug report: https://bugs.python.org/issue10544
- Python 3.8+ no longer allows `yield` inside list comprehension and will throw a `SyntaxError`.

---


### ▶ Yielding from... return! *
<!-- Example ID: 5626d8ef-8802-49c2-adbc-7cda5c550816 --->
1\.

```py
def some_func(x):
    if x == 3:
        return ["wtf"]
    else:
        yield from range(x)
```

**Ausgabe (> 3.3):**

```py
>>> list(some_func(3))
[]
```

Where did the `"wtf"` go? Is it due to some special effect of `yield from`? Let's validate that,

2\.

```py
def some_func(x):
    if x == 3:
        return ["wtf"]
    else:
        for i in range(x):
          yield i
```

**Ausgabe:**

```py
>>> list(some_func(3))
[]
```

The same result, this didn't work either.

#### 💡 Erklärung:

+ From Python 3.3 onwards, it became possible to use `return` statement with values inside generators (See [PEP380](https://www.python.org/dev/peps/pep-0380/)). The [official docs](https://www.python.org/dev/peps/pep-0380/#enhancements-to-stopiteration) say that,

> "... `return expr` in a generator causes `StopIteration(expr)` to be raised upon exit from the generator."

+ In the case of `some_func(3)`, `StopIteration` is raised at the beginning because of `return` statement. The `StopIteration` exception is automatically caught inside the `list(...)` wrapper and the `for` loop. Therefore, the above two snippets result in an empty list.

+ To get `["wtf"]` from the generator `some_func` we need to catch the `StopIteration` exception,

  ```py
  try:
      next(some_func(3))
  except StopIteration as e:
      some_string = e.value
  ```

  ```py
  >>> some_string
  ["wtf"]
  ```

---

### ▶ Nan-Reflexivität *

<!-- Example ID: 59bee91a-36e0-47a4-8c7d-aa89bf1d3976 --->

1\.

```py
a = float('inf')
b = float('nan')
c = float('-iNf')  # These strings are case-insensitive
d = float('nan')
```

**Ausgabe:**

```py
>>> a
inf
>>> b
nan
>>> c
-inf
>>> float('some_other_string')
ValueError: could not convert string to float: some_other_string
>>> a == -c # inf==inf
True
>>> None == None # None == None
True
>>> b == d # but nan!=nan
False
>>> 50 / a
0.0
>>> a / a
nan
>>> 23 + b
nan
```

2\.

```py
>>> x = float('nan')
>>> y = x / x
>>> y is y # identity holds
True
>>> y == y # equality fails of y
False
>>> [y] == [y] # but the equality succeeds for the list containing y
True
```



#### 💡 Erklärung:

- `'inf'` and `'nan'` are special strings (case-insensitive), which, when explicitly typecast-ed to `float` type, are used to represent mathematical "infinity" and "not a number" respectively.

- Since according to IEEE standards ` NaN != NaN`, obeying this rule breaks the reflexivity assumption of a collection element in Python i.e. if `x` is a part of a collection like `list`, the implementations like comparison are based on the assumption that `x == x`.  Because of this assumption, the identity is compared first (since it's faster) while comparing two elements, and the values are compared only when the identities mismatch. The following snippet will make things clearer,

  ```py
  >>> x = float('nan')
  >>> x == x, [x] == [x]
  (False, True)
  >>> y = float('nan')
  >>> y == y, [y] == [y]
  (False, True)
  >>> x == y, [x] == [y]
  (False, False)
  ```

  Since the identities of `x` and `y` are different, the values are considered, which are also different; hence the comparison returns `False` this time.

- Interesting read: [Reflexivity, and other pillars of civilization](https://bertrandmeyer.com/2010/02/06/reflexivity-and-other-pillars-of-civilization/)

---

### ▶ Verändern des Unveränderlichen!

<!-- Example ID: 15a9e782-1695-43ea-817a-a9208f6bb33d --->

This might seem trivial if you know how references work in Python.

```py
some_tuple = ("A", "tuple", "with", "values")
another_tuple = ([1, 2], [3, 4], [5, 6])
```

**Ausgabe:**
```py
>>> some_tuple[2] = "change this"
TypeError: 'tuple' object does not support item assignment
>>> another_tuple[2].append(1000) #This throws no error
>>> another_tuple
([1, 2], [3, 4], [5, 6, 1000])
>>> another_tuple[2] += [99, 999]
TypeError: 'tuple' object does not support item assignment
>>> another_tuple
([1, 2], [3, 4], [5, 6, 1000, 99, 999])
```

But I thought tuples were immutable...

#### 💡 Erklärung:

* Zitat von https://docs.python.org/3/reference/datamodel.html

    > Immutable sequences
        An object of an immutable sequence type cannot change once it is created. (If the object contains references to other objects, these other objects may be mutable and may be modified; however, the collection of objects directly referenced by an immutable object cannot change.)

* `+=` operator changes the list in-place. The item assignment doesn't work, but when the exception occurs, the item has already been changed in place.
* There's also an Erklärung in [official Python FAQ](https://docs.python.org/3/faq/programming.html#why-does-a-tuple-i-item-raise-an-exception-when-the-addition-works).

---

### ▶ Die verschwindende Variable aus dem äußeren Gültigkeitsbereich
<!-- Example ID: 7f1e71b6-cb3e-44fb-aa47-87ef1b7decc8 --->

```py
e = 7
try:
    raise Exception()
except Exception as e:
    pass
```

**Ausgabe (Python 2.x):**
```py
>>> print(e)
# prints nothing
```

**Ausgabe (Python 3.x):**
```py
>>> print(e)
NameError: name 'e' is not defined
```

#### 💡 Erklärung:

* Quelle: https://docs.python.org/3/reference/compound_stmts.html#except

  When an exception has been assigned using `as` target, it is cleared at the end of the `except` clause. This is as if

  ```py
  except E as N:
      foo
  ```

  was translated into

  ```py
  except E as N:
      try:
          foo
      finally:
          del N
  ```

  This means the exception must be assigned to a different name to be able to refer to it after the except clause. Exceptions are cleared because, with the traceback attached to them, they form a reference cycle with the stack frame, keeping all locals in that frame alive until the next garbage collection occurs.

* The clauses are not scoped in Python. Everything in the example is present in the same scope, and the variable `e` got removed due to the execution of the `except` clause. The same is not the case with functions that have their separate inner-scopes. The example below illustrates this:

     ```py
     def f(x):
         del(x)
         print(x)

     x = 5
     y = [5, 4, 3]
     ```

     **Ausgabe:**
     ```py
     >>> f(x)
     UnboundLocalError: local variable 'x' referenced before assignment
     >>> f(y)
     UnboundLocalError: local variable 'x' referenced before assignment
     >>> x
     5
     >>> y
     [5, 4, 3]
     ```

* In Python 2.x, the variable name `e` gets assigned to `Exception()` instance, so when you try to print, it prints nothing.

    **Ausgabe (Python 2.x):**
    ```py
    >>> e
    Exception()
    >>> print e
    # Nothing is printed!
    ```

---


### ▶ Die mysteriöse key type Umwandlung
<!-- Example ID: 00f42dd0-b9ef-408d-9e39-1bc209ce3f36 --->
```py
class SomeClass(str):
    pass

some_dict = {'s': 42}
```

**Ausgabe:**
```py
>>> type(list(some_dict.keys())[0])
str
>>> s = SomeClass('s')
>>> some_dict[s] = 40
>>> some_dict # expected: Two different keys-value pairs
{'s': 40}
>>> type(list(some_dict.keys())[0])
str
```

#### 💡 Erklärung:

* Both the object `s` and the string `"s"` hash to the same value because `SomeClass` inherits the `__hash__` method of `str` class.
* `SomeClass("s") == "s"` evaluates to `True` because `SomeClass` also inherits `__eq__` method from `str` class.
* Since both the objects hash to the same value and are equal, they are represented by the same key in the dictionary.
* For the desired behavior, we can redefine the `__eq__` method in `SomeClass`
  ```py
  class SomeClass(str):
    def __eq__(self, other):
        return (
            type(self) is SomeClass
            and type(other) is SomeClass
            and super().__eq__(other)
        )

    # When we define a custom __eq__, Python stops automatically inheriting the
    # __hash__ method, so we need to define it as well
    __hash__ = str.__hash__

  some_dict = {'s':42}
  ```

  **Ausgabe:**
  ```py
  >>> s = SomeClass('s')
  >>> some_dict[s] = 40
  >>> some_dict
  {'s': 40, 's': 42}
  >>> keys = list(some_dict.keys())
  >>> type(keys[0]), type(keys[1])
  (__main__.SomeClass, str)
  ```

---

### ▶ Lass uns sehen, ob du dies errätst?
<!-- Example ID: 81aa9fbe-bd63-4283-b56d-6fdd14c9105e --->
```py
a, b = a[b] = {}, 5
```

**Ausgabe:**
```py
>>> a
{5: ({...}, 5)}
```

#### 💡 Erklärung:

* According to [Python language reference](https://docs.python.org/3/reference/simple_stmts.html#assignment-statements), assignment statements have the form
  ```
  (target_list "=")+ (expression_list | yield_expression)
  ```
  and
  
> An assignment statement evaluates the expression list (remember that this can be a single expression or a comma-separated list, the latter yielding a tuple) and assigns the single resulting object to each of the target lists, from left to right.

* The `+` in `(target_list "=")+` means there can be **one or more** target lists. In this case, target lists are `a, b` and `a[b]` (note the expression list is exactly one, which in our case is `{}, 5`).

* After the expression list is evaluated, its value is unpacked to the target lists from **left to right**. So, in our case, first the `{}, 5` tuple is unpacked to `a, b` and we now have `a = {}` and `b = 5`.

* `a` is now assigned to `{}`, which is a mutable object.

* The second target list is `a[b]` (you may expect this to throw an error because both `a` and `b` have not been defined in the statements before. But remember, we just assigned `a` to `{}` and `b` to `5`).

* Now, we are setting the key `5` in the dictionary to the tuple `({}, 5)` creating a circular reference (the `{...}` in the Ausgabe refers to the same object that `a` is already referencing). Another simpler example of circular reference could be
  ```py
  >>> some_list = some_list[0] = [0]
  >>> some_list
  [[...]]
  >>> some_list[0]
  [[...]]
  >>> some_list is some_list[0]
  True
  >>> some_list[0][0][0][0][0][0] == some_list
  True
  ```
  Similar is the case in our example (`a[b][0]` is the same object as `a`)

* So to sum it up, you can break the example down to
  ```py
  a, b = {}, 5
  a[b] = a, b
  ```
  And the circular reference can be justified by the fact that `a[b][0]` is the same object as `a`
  ```py
  >>> a[b][0] is a
  True
  ```


---

### ▶ Überschreitet den Grenzwert für die Umwandlung von Integer-Strings
```py
>>> # Python 3.10.6
>>> int("2" * 5432)

>>> # Python 3.10.8
>>> int("2" * 5432)
```

**Ausgabe:**
```py
>>> # Python 3.10.6
222222222222222222222222222222222222222222222222222222222222222...

>>> # Python 3.10.8
Traceback (most recent call last):
   ...
ValueError: Exceeds the limit (4300) for integer string conversion:
   value has 5432 digits; use sys.set_int_max_str_digits()
   to increase the limit.
```

#### 💡 Erklärung:
This call to `int()` works fine in Python 3.10.6 and raises a ValueError in Python 3.10.8. Note that Python can still work with large integers. The error is only raised when converting between integers and strings.

Fortunately, you can increase the limit for the allowed number of digits when you expect an operation to exceed it. To do this, you can use one of the following:
- The -X int_max_str_digits command-line flag
- The set_int_max_str_digits() function from the sys module
- The PYTHONINTMAXSTRDIGITS environment variable

[Check the documentation](https://docs.python.org/3/library/stdtypes.html#int-max-str-digits) for more details on changing the default limit if you expect your code to exceed this value.


---


## Kapitel: Slippery Slopes

### ▶ Modifizieren eines Dictionarys während einer Iteration
<!-- Example ID: b4e5cdfb-c3a8-4112-bd38-e2356d801c41 --->
```py
x = {0: None}

for i in x:
    del x[i]
    x[i+1] = None
    print(i)
```

**Ausgabe (Python 2.7- Python 3.5):**

```
0
1
2
3
4
5
6
7
```

Yes, it runs for exactly **eight** times and stops.

#### 💡 Erklärung:

* Iteration over a dictionary that you edit at the same time is not supported.
* It runs eight times because that's the point at which the dictionary resizes to hold more keys (we have eight deletion entries, so a resize is needed). This is actually an implementation detail.
* How deleted keys are handled and when the resize occurs might be different for different Python implementations.
* So for Python versions other than Python 2.7 - Python 3.5, the count might be different from 8 (but whatever the count is, it's going to be the same every time you run it). You can find some discussion around this [here](https://github.com/satwikkansal/wtfpython/issues/53) or in [this](https://stackoverflow.com/questions/44763802/bug-in-python-dict) StackOverflow thread.
* Python 3.7.6 onwards, you'll see `RuntimeError: dictionary keys changed during iteration` exception if you try to do this.

---

### ▶ Hartnäckige `del` Operation
<!-- Example ID: 777ed4fd-3a2d-466f-95e7-c4058e61d78e --->
<!-- read-only -->

```py
class SomeClass:
    def __del__(self):
        print("Deleted!")
```

**Ausgabe:**
1\.
```py
>>> x = SomeClass()
>>> y = x
>>> del x # this should print "Deleted!"
>>> del y
Deleted!
```

Phew, deleted at last. You might have guessed what saved `__del__` from being called in our first attempt to delete `x`. Let's add more twists to the example.

2\.
```py
>>> x = SomeClass()
>>> y = x
>>> del x
>>> y # check if y exists
<__main__.SomeClass instance at 0x7f98a1a67fc8>
>>> del y # Like previously, this should print "Deleted!"
>>> globals() # oh, it didn't. Let's check all our global variables and confirm
Deleted!
{'__builtins__': <module '__builtin__' (built-in)>, 'SomeClass': <class __main__.SomeClass at 0x7f98a1a5f668>, '__package__': None, '__name__': '__main__', '__doc__': None}
```

Okay, now it's deleted :confused:

#### 💡 Erklärung:
+ `del x` doesn’t directly call `x.__del__()`.
+ When `del x` is encountered, Python deletes the name `x` from current scope and decrements by 1 the reference count of the object `x` referenced. `__del__()` is called only when the object's reference count reaches zero.
+ In the second Ausgabe snippet, `__del__()` was not called because the previous statement (`>>> y`) in the interactive interpreter created another reference to the same object (specifically, the `_` magic variable which references the result value of the last non `None` expression on the REPL), thus preventing the reference count from reaching zero when `del y` was encountered.
+ Calling `globals` (or really, executing anything that will have a non `None` result) caused `_` to reference the new result, dropping the existing reference. Now the reference count reached 0 and we can see "Deleted!" being printed (finally!).

---

### ▶ Die Variable aus dem äußeren Geltungsbereich
<!-- Example ID: 75c03015-7be9-4289-9e22-4f5fdda056f7 --->

1\.
```py
a = 1
def some_func():
    return a

def another_func():
    a += 1
    return a
```

2\.
```py
def some_closure_func():
    a = 1
    def some_inner_func():
        return a
    return some_inner_func()

def another_closure_func():
    a = 1
    def another_inner_func():
        a += 1
        return a
    return another_inner_func()
```

**Ausgabe:**
```py
>>> some_func()
1
>>> another_func()
UnboundLocalError: local variable 'a' referenced before assignment

>>> some_closure_func()
1
>>> another_closure_func()
UnboundLocalError: local variable 'a' referenced before assignment
```

#### 💡 Erklärung:
* When you make an assignment to a variable in scope, it becomes local to that scope. So `a` becomes local to the scope of `another_func`, but it has not been initialized previously in the same scope, which throws an error.
* To modify the outer scope variable `a` in `another_func`, we have to use the `global` keyword.
  ```py
  def another_func()
      global a
      a += 1
      return a
  ```

  **Ausgabe:**
  ```py
  >>> another_func()
  2
  ```
* In `another_closure_func`, `a` becomes local to the scope of `another_inner_func`, but it has not been initialized previously in the same scope, which is why it throws an error. 
* To modify the outer scope variable `a` in `another_inner_func`, use the `nonlocal` keyword. The nonlocal statement is used to refer to variables defined in the nearest outer (excluding the global) scope.
  ```py
  def another_func():
      a = 1
      def another_inner_func():
          nonlocal a
          a += 1
          return a
      return another_inner_func()
  ```

  **Ausgabe:**
  ```py
  >>> another_func()
  2
  ```
* The keywords `global` and `nonlocal` tell the python interpreter to not declare new variables and look them up in the corresponding outer scopes.
* Read [this](https://sebastianraschka.com/Articles/2014_python_scope_and_namespaces.html) short but an awesome guide to learn more about how namespaces and scope resolution works in Python.

---

### ▶ Löschen eines Listenelements während einer Iteration
<!-- Example ID: 4cc52d4e-d42b-4e09-b25f-fbf5699b7d4e --->
```py
list_1 = [1, 2, 3, 4]
list_2 = [1, 2, 3, 4]
list_3 = [1, 2, 3, 4]
list_4 = [1, 2, 3, 4]

for idx, item in enumerate(list_1):
    del item

for idx, item in enumerate(list_2):
    list_2.remove(item)

for idx, item in enumerate(list_3[:]):
    list_3.remove(item)

for idx, item in enumerate(list_4):
    list_4.pop(idx)
```

**Ausgabe:**
```py
>>> list_1
[1, 2, 3, 4]
>>> list_2
[2, 4]
>>> list_3
[]
>>> list_4
[2, 4]
```

Can you guess why the Ausgabe is `[2, 4]`?

#### 💡 Erklärung:

* It's never a good idea to change the object you're iterating over. The correct way to do so is to iterate over a copy of the object instead, and `list_3[:]` does just that.

     ```py
     >>> some_list = [1, 2, 3, 4]
     >>> id(some_list)
     139798789457608
     >>> id(some_list[:]) # Notice that python creates new object for sliced list.
     139798779601192
     ```

**Difference between `del`, `remove`, and `pop`:**
* `del var_name` just removes the binding of the `var_name` from the local or global namespace (That's why the `list_1` is unaffected).
* `remove` removes the first matching value, not a specific index, raises `ValueError` if the value is not found.
* `pop` removes the element at a specific index and returns it, raises `IndexError` if an invalid index is specified.

**Why the Ausgabe is `[2, 4]`?**
- The list iteration is done index by index, and when we remove `1` from `list_2` or `list_4`, the contents of the lists are now `[2, 3, 4]`. The remaining elements are shifted down, i.e., `2` is at index 0, and `3` is at index 1. Since the next iteration is going to look at index 1 (which is the `3`), the `2` gets skipped entirely. A similar thing will happen with every alternate element in the list sequence.

* Refer to this StackOverflow [thread](https://stackoverflow.com/questions/45946228/what-happens-when-you-try-to-delete-a-list-element-while-iterating-over-it) explaining the example
* See also this nice StackOverflow [thread](https://stackoverflow.com/questions/45877614/how-to-change-all-the-dictionary-keys-in-a-for-loop-with-d-items) for a similar example related to dictionaries in Python.

---


### ▶ Lossy Zips von Iteratoren *
<!-- Example ID: c28ed154-e59f-4070-8eb6-8967a4acac6d --->

```py
>>> numbers = list(range(7))
>>> numbers
[0, 1, 2, 3, 4, 5, 6]
>>> first_three, remaining = numbers[:3], numbers[3:]
>>> first_three, remaining
([0, 1, 2], [3, 4, 5, 6])
>>> numbers_iter = iter(numbers)
>>> list(zip(numbers_iter, first_three)) 
[(0, 0), (1, 1), (2, 2)]
# so far so good, let's zip the remaining
>>> list(zip(numbers_iter, remaining))
[(4, 3), (5, 4), (6, 5)]
```
Where did element `3` go from the `numbers` list?

#### 💡 Erklärung:

- From Python [docs](https://docs.python.org/3.3/library/functions.html#zip), here's an approximate implementation of zip function,
    ```py
    def zip(*iterables):
        sentinel = object()
        iterators = [iter(it) for it in iterables]
        while iterators:
            result = []
            for it in iterators:
                elem = next(it, sentinel)
                if elem is sentinel: return
                result.append(elem)
            yield tuple(result)
    ```
- So the function takes in arbitrary number of iterable objects, adds each of their items to the `result` list by calling the `next` function on them, and stops whenever any of the iterable is exhausted. 
- The caveat here is when any iterable is exhausted, the existing elements in the `result` list are discarded. That's what happened with `3` in the `numbers_iter`.
- The correct way to do the above using `zip` would be,
    ```py
    >>> numbers = list(range(7))
    >>> numbers_iter = iter(numbers)
    >>> list(zip(first_three, numbers_iter))
    [(0, 0), (1, 1), (2, 2)]
    >>> list(zip(remaining, numbers_iter))
    [(3, 3), (4, 4), (5, 5), (6, 6)]
    ```
    The first argument of zip should be the one with fewest elements.

---

### ▶ Schleifenvariablen, die auslaufen!
<!-- Example ID: ccec7bf6-7679-4963-907a-1cd8587be9ea --->
1\.
```py
for x in range(7):
    if x == 6:
        print(x, ': for x inside loop')
print(x, ': x in global')
```

**Ausgabe:**
```py
6 : for x inside loop
6 : x in global
```

But `x` was never defined outside the scope of for loop...

2\.
```py
# This time let's initialize x first
x = -1
for x in range(7):
    if x == 6:
        print(x, ': for x inside loop')
print(x, ': x in global')
```

**Ausgabe:**
```py
6 : for x inside loop
6 : x in global
```

3\.

**Ausgabe (Python 2.x):**
```py
>>> x = 1
>>> print([x for x in range(5)])
[0, 1, 2, 3, 4]
>>> print(x)
4
```

**Ausgabe (Python 3.x):**
```py
>>> x = 1
>>> print([x for x in range(5)])
[0, 1, 2, 3, 4]
>>> print(x)
1
```

#### 💡 Erklärung:

- In Python, for-loops use the scope they exist in and leave their defined loop-variable behind. This also applies if we explicitly defined the for-loop variable in the global namespace before. In this case, it will rebind the existing variable.

- The differences in the Ausgabe of Python 2.x and Python 3.x interpreters for list comprehension example can be explained by following change documented in [What’s New In Python 3.0](https://docs.python.org/3/whatsnew/3.0.html) changelog:

    > "List comprehensions no longer support the syntactic form `[... for var in item1, item2, ...]`. Use `[... for var in (item1, item2, ...)]` instead. Also, note that list comprehensions have different semantics: they are closer to syntactic sugar for a generator expression inside a `list()` constructor, and in particular, the loop control variables are no longer leaked into the surrounding scope."

---

### ▶ Vorsicht vor standardmäßig veränderbaren Argumenten!
<!-- Example ID: 7d42dade-e20d-4a7b-9ed7-16fb58505fe9 --->

```py
def some_func(default_arg=[]):
    default_arg.append("some_string")
    return default_arg
```

**Ausgabe:**
```py
>>> some_func()
['some_string']
>>> some_func()
['some_string', 'some_string']
>>> some_func([])
['some_string']
>>> some_func()
['some_string', 'some_string', 'some_string']
```

#### 💡 Erklärung:

- The default mutable arguments of functions in Python aren't really initialized every time you call the function. Instead, the recently assigned value to them is used as the default value. When we explicitly passed `[]` to `some_func` as the argument, the default value of the `default_arg` variable was not used, so the function returned as expected.

    ```py
    def some_func(default_arg=[]):
        default_arg.append("some_string")
        return default_arg
    ```

    **Ausgabe:**
    ```py
    >>> some_func.__defaults__ #This will show the default argument values for the function
    ([],)
    >>> some_func()
    >>> some_func.__defaults__
    (['some_string'],)
    >>> some_func()
    >>> some_func.__defaults__
    (['some_string', 'some_string'],)
    >>> some_func([])
    >>> some_func.__defaults__
    (['some_string', 'some_string'],)
    ```

- A common practice to avoid bugs due to mutable arguments is to assign `None` as the default value and later check if any value is passed to the function corresponding to that argument. Example:

    ```py
    def some_func(default_arg=None):
        if default_arg is None:
            default_arg = []
        default_arg.append("some_string")
        return default_arg
    ```

---

### ▶ Fangen der Exceptions
<!-- Example ID: b5ca5e6a-47b9-4f69-9375-cda0f8c6755d --->
```py
some_list = [1, 2, 3]
try:
    # This should raise an ``IndexError``
    print(some_list[4])
except IndexError, ValueError:
    print("Caught!")

try:
    # This should raise a ``ValueError``
    some_list.remove(4)
except IndexError, ValueError:
    print("Caught again!")
```

**Ausgabe (Python 2.x):**
```py
Caught!

ValueError: list.remove(x): x not in list
```

**Ausgabe (Python 3.x):**
```py
  File "<input>", line 3
    except IndexError, ValueError:
                     ^
SyntaxError: invalid syntax
```

#### 💡 Erklärung

* To add multiple Exceptions to the except clause, you need to pass them as parenthesized tuple as the first argument. The second argument is an optional name, which when supplied will bind the Exception instance that has been raised. Example,
  ```py
  some_list = [1, 2, 3]
  try:
     # This should raise a ``ValueError``
     some_list.remove(4)
  except (IndexError, ValueError), e:
     print("Caught again!")
     print(e)
  ```
  **Ausgabe (Python 2.x):**
  ```
  Caught again!
  list.remove(x): x not in list
  ```
  **Ausgabe (Python 3.x):**
  ```py
    File "<input>", line 4
      except (IndexError, ValueError), e:
                                       ^
  IndentationError: unindent does not match any outer indentation level
  ```

* Separating the exception from the variable with a comma is deprecated and does not work in Python 3; the correct way is to use `as`. Example,
  ```py
  some_list = [1, 2, 3]
  try:
      some_list.remove(4)

  except (IndexError, ValueError) as e:
      print("Caught again!")
      print(e)
  ```
  **Ausgabe:**
  ```
  Caught again!
  list.remove(x): x not in list
  ```

---

### ▶ Gleiche Operanden, unterschiedliche Story!
<!-- Example ID: ca052cdf-dd2d-4105-b936-65c28adc18a0 --->
1\.
```py
a = [1, 2, 3, 4]
b = a
a = a + [5, 6, 7, 8]
```

**Ausgabe:**
```py
>>> a
[1, 2, 3, 4, 5, 6, 7, 8]
>>> b
[1, 2, 3, 4]
```

2\.
```py
a = [1, 2, 3, 4]
b = a
a += [5, 6, 7, 8]
```

**Ausgabe:**
```py
>>> a
[1, 2, 3, 4, 5, 6, 7, 8]
>>> b
[1, 2, 3, 4, 5, 6, 7, 8]
```

#### 💡 Erklärung:

*  `a += b` doesn't always behave the same way as `a = a + b`.  Classes *may* implement the *`op=`* operators differently, and lists do this.

* The expression `a = a + [5,6,7,8]` generates a new list and sets `a`'s reference to that new list, leaving `b` unchanged.

* The expression `a += [5,6,7,8]` is actually mapped to an "extend" function that operates on the list such that `a` and `b` still point to the same list that has been modified in-place.

---

### ▶ Namensauflösung ohne Berücksichtigung des Geltungsbereichs der Klasse
<!-- Example ID: 03f73d96-151c-4929-b0a8-f74430788324 --->
1\.
```py
x = 5
class SomeClass:
    x = 17
    y = (x for i in range(10))
```

**Ausgabe:**
```py
>>> list(SomeClass.y)[0]
5
```

2\.
```py
x = 5
class SomeClass:
    x = 17
    y = [x for i in range(10)]
```

**Ausgabe (Python 2.x):**
```py
>>> SomeClass.y[0]
17
```

**Ausgabe (Python 3.x):**
```py
>>> SomeClass.y[0]
5
```

#### 💡 Erklärung
- Scopes nested inside class definition ignore names bound at the class level.
- A generator expression has its own scope.
- Starting from Python 3.X, list comprehensions also have their own scope.

---

### ▶ Runden wie ein Bankier *

Let's implement a naive function to get the middle element of a list:
```py
def get_middle(some_list):
    mid_index = round(len(some_list) / 2)
    return some_list[mid_index - 1]
```

**Python 3.x:**
```py
>>> get_middle([1])  # looks good
1
>>> get_middle([1,2,3])  # looks good
2
>>> get_middle([1,2,3,4,5])  # huh?
2
>>> len([1,2,3,4,5]) / 2  # good
2.5
>>> round(len([1,2,3,4,5]) / 2)  # why?
2
```
It seems as though Python rounded 2.5 to 2.

#### 💡 Erklärung:

- This is not a float precision error, in fact, this behavior is intentional. Since Python 3.0, `round()` uses [banker's rounding](https://en.wikipedia.org/wiki/Rounding#Round_half_to_even) where .5 fractions are rounded to the nearest **even** number:

```py
>>> round(0.5)
0
>>> round(1.5)
2
>>> round(2.5)
2
>>> import numpy  # numpy does the same
>>> numpy.round(0.5)
0.0
>>> numpy.round(1.5)
2.0
>>> numpy.round(2.5)
2.0
```

- This is the recommended way to round .5 fractions as described in [IEEE 754](https://en.wikipedia.org/wiki/IEEE_754#Rounding_rules). However, the other way (round away from zero) is taught in school most of the time, so banker's rounding is likely not that well known. Furthermore, some of the most popular programming languages (for example: JavaScript, Java, C/C++, Ruby, Rust) do not use banker's rounding either. Therefore, this is still quite special to Python and may result in confusion when rounding fractions. 
- See the [round() docs](https://docs.python.org/3/library/functions.html#round) or [this stackoverflow thread](https://stackoverflow.com/questions/10825926/python-3-x-rounding-behavior) for more information.
- Note that `get_middle([1])` only returned 1 because the index was `round(0.5) - 1 = 0 - 1 = -1`, returning the last element in the list.

---

### ▶ Nadeln im Heuhaufen *

<!-- Example ID: 52a199b1-989a-4b28-8910-dff562cebba9 --->

I haven't met even a single experience Pythonist till date who has not come across one or more of the following scenarios,

1\.

```py
x, y = (0, 1) if True else None, None
```

**Ausgabe:**

```py
>>> x, y  # expected (0, 1)
((0, 1), None)
```

2\.

```py
t = ('one', 'two')
for i in t:
    print(i)

t = ('one')
for i in t:
    print(i)

t = ()
print(t)
```

**Ausgabe:**

```py
one
two
o
n
e
tuple()
```

3\.

```
ten_words_list = [
    "some",
    "very",
    "big",
    "list",
    "that"
    "consists",
    "of",
    "exactly",
    "ten",
    "words"
]
```

**Ausgabe**

```py
>>> len(ten_words_list)
9
```

4\. Not asserting strongly enough

```py
a = "python"
b = "javascript"
```

**Ausgabe:**

```py
# An assert statement with an assertion failure message.
>>> assert(a == b, "Both languages are different")
# No AssertionError is raised
```

5\.

```py
some_list = [1, 2, 3]
some_dict = {
  "key_1": 1,
  "key_2": 2,
  "key_3": 3
}

some_list = some_list.append(4) 
some_dict = some_dict.update({"key_4": 4})
```

**Ausgabe:**

```py
>>> print(some_list)
None
>>> print(some_dict)
None
```

6\.

```py
def some_recursive_func(a):
    if a[0] == 0:
        return
    a[0] -= 1
    some_recursive_func(a)
    return a

def similar_recursive_func(a):
    if a == 0:
        return a
    a -= 1
    similar_recursive_func(a)
    return a
```

**Ausgabe:**

```py
>>> some_recursive_func([5, 0])
[0, 0]
>>> similar_recursive_func(5)
4
```

#### 💡 Erklärung:

* For 1, the correct statement for expected behavior is `x, y = (0, 1) if True else (None, None)`.

* For 2, the correct statement for expected behavior is `t = ('one',)` or `t = 'one',` (missing comma) otherwise the interpreter considers `t` to be a `str` and iterates over it character by character.

* `()` is a special token and denotes empty `tuple`.

* In 3, as you might have already figured out, there's a missing comma after 5th element (`"that"`) in the list. So by implicit string literal concatenation,

  ```py
  >>> ten_words_list
  ['some', 'very', 'big', 'list', 'thatconsists', 'of', 'exactly', 'ten', 'words']
  ```

* No `AssertionError` was raised in 4th snippet because instead of asserting the individual expression `a == b`, we're asserting entire tuple. The following snippet will clear things up,

  ```py
  >>> a = "python"
  >>> b = "javascript"
  >>> assert a == b
  Traceback (most recent call last):
      File "<stdin>", line 1, in <module>
  AssertionError
  
  >>> assert (a == b, "Values are not equal")
  <stdin>:1: SyntaxWarning: assertion is always true, perhaps remove parentheses?
  
  >>> assert a == b, "Values are not equal"
  Traceback (most recent call last):
      File "<stdin>", line 1, in <module>
  AssertionError: Values are not equal
  ```

* As for the fifth snippet, most methods that modify the items of sequence/mapping objects like `list.append`, `dict.update`, `list.sort`, etc. modify the objects in-place and return `None`. The rationale behind this is to improve performance by avoiding making a copy of the object if the operation can be done in-place (Referred from [here](https://docs.python.org/3/faq/design.html#why-doesn-t-list-sort-return-the-sorted-list)).

* Last one should be fairly obvious, mutable object (like `list`) can be altered in the function, and the reassignment of an immutable (`a -= 1`) is not an alteration of the value.

* Being aware of these nitpicks can save you hours of debugging effort in the long run. 

---


### ▶ Splitsies *
<!-- Example ID: ec3168ba-a81a-4482-afb0-691f1cc8d65a --->
```py
>>> 'a'.split()
['a']

# is same as
>>> 'a'.split(' ')
['a']

# but
>>> len(''.split())
0

# isn't the same as
>>> len(''.split(' '))
1
```

#### 💡 Erklärung:

- It might appear at first that the default separator for split is a single space `' '`, but as per the [docs](https://docs.python.org/3/library/stdtypes.html#str.split)
    >  If sep is not specified or is `None`, a different splitting algorithm is applied: runs of consecutive whitespace are regarded as a single separator, and the result will contain no empty strings at the start or end if the string has leading or trailing whitespace. Consequently, splitting an empty string or a string consisting of just whitespace with a None separator returns `[]`.
    > If sep is given, consecutive delimiters are not grouped together and are deemed to delimit empty strings (for example, `'1,,2'.split(',')` returns `['1', '', '2']`). Splitting an empty string with a specified separator returns `['']`.
- Noticing how the leading and trailing whitespaces are handled in the following snippet will make things clear,
    ```py
    >>> ' a '.split(' ')
    ['', 'a', '']
    >>> ' a '.split()
    ['a']
    >>> ''.split(' ')
    ['']
    ```

---

### ▶ Wilde Imports *
<!-- Example ID: 83deb561-bd55-4461-bb5e-77dd7f411e1c --->
<!-- read-only -->

```py
# File: module.py

def some_weird_name_func_():
    print("works!")

def _another_weird_name_func():
    print("works!")

```

**Ausgabe**

```py
>>> from module import *
>>> some_weird_name_func_()
"works!"
>>> _another_weird_name_func()
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name '_another_weird_name_func' is not defined
```

#### 💡 Erklärung:

- It is often advisable to not use wildcard imports. The first obvious reason for this is, in wildcard imports, the names with a leading underscore don't get imported. This may lead to errors during runtime.
- Had we used `from ... import a, b, c` syntax, the above `NameError` wouldn't have occurred.
    ```py
    >>> from module import some_weird_name_func_, _another_weird_name_func
    >>> _another_weird_name_func()
    works!
    ```
- If you really want to use wildcard imports, then you'd have to define the list `__all__` in your module that will contain a list of public objects that'll be available when we do wildcard imports.
    ```py
    __all__ = ['_another_weird_name_func']

    def some_weird_name_func_():
        print("works!")

    def _another_weird_name_func():
        print("works!")
    ```
    **Ausgabe**

    ```py
    >>> _another_weird_name_func()
    "works!"
    >>> some_weird_name_func_()
    Traceback (most recent call last):
      File "<stdin>", line 1, in <module>
    NameError: name 'some_weird_name_func_' is not defined
    ```

---

### ▶  Alles sortieren ? *

<!-- Example ID: e5ff1eaf-8823-4738-b4ce-b73f7c9d5511 -->

```py
>>> x = 7, 8, 9
>>> sorted(x) == x
False
>>> sorted(x) == sorted(x)
True

>>> y = reversed(x)
>>> sorted(y) == sorted(y)
False
```

#### 💡 Erklärung:

- The `sorted` method always returns a list, and comparing lists and tuples always returns `False` in Python. 

- ```py
  >>> [] == tuple()
  False
  >>> x = 7, 8, 9
  >>> type(x), type(sorted(x))
  (tuple, list)
  ```

- Unlike `sorted`, the `reversed` method returns an iterator. Why? Because sorting requires the iterator to be either modified in-place or use an extra container (a list), whereas reversing can simply work by iterating from the last index to the first.

- So during comparison `sorted(y) == sorted(y)`, the first call to `sorted()` will consume the iterator `y`, and the next call will just return an empty list.

  ```py
  >>> x = 7, 8, 9
  >>> y = reversed(x)
  >>> sorted(y), sorted(y)
  ([7, 8, 9], [])
  ```

---

### ▶ Mitternachtszeit gibt es nicht ?
<!-- Example ID: 1bce8294-5619-4d70-8ce3-fe0bade690d1 --->
```py
from datetime import datetime

midnight = datetime(2018, 1, 1, 0, 0)
midnight_time = midnight.time()

noon = datetime(2018, 1, 1, 12, 0)
noon_time = noon.time()

if midnight_time:
    print("Time at midnight is", midnight_time)

if noon_time:
    print("Time at noon is", noon_time)
```

**Ausgabe (< 3.5):**

```py
('Time at noon is', datetime.time(12, 0))
```
The midnight time is not printed.

#### 💡 Erklärung:

Before Python 3.5, the boolean value for `datetime.time` object was considered to be `False` if it represented midnight in UTC. It is error-prone when using the `if obj:` syntax to check if the `obj` is null or some equivalent of "empty."

---
---



## Kapitel: Die verborgenen Schätze!

Dieser Abschnitt enthält ein paar weniger bekannte und interessante Dinge über Python, die den meisten Anfängern wie mir nicht bekannt sind (nun aber schon).

### ▶ Okay Python, kannst du mich fliegen lassen?
<!-- Example ID: a92f3645-1899-4d50-9721-0031be4aec3f --->
Nun hier wären wir:

```py
import antigravity
```

**Ausgabe:**
Sshh... Es ist supergeheim.

#### 💡 Erklärung:
+ Das `antigravity` Modul ist eines der wenigen easter eggs, die von Python Entwicklern veröffentlicht werden.
+ `import antigravity` öffnet deinen Webbrowser und zeigt zum [klassischen XKCD Comic](https://xkcd.com/353/).
+ Nun, es gibt noch mehr. Es gibt noch ein **easter egg im easter egg**. Wenn du dir den [code](https://github.com/python/cpython/blob/master/Lib/antigravity.py#L7-L17) anschaust, dann findest du eine Funktion, die die Ausführung des [XKCDs Geohashing Algorithmus](https://xkcd.com/426/) beabsichtigt.

---

### ▶ `goto`, aber wieso?
<!-- Example ID: 2aff961e-7fa5-4986-a18a-9e5894bd89fe --->

```py
from goto import goto, label
for i in range(9):
    for j in range(9):
        for k in range(9):
            print("I am trapped, please rescue!")
            if k == 2:
                goto .breakout # breaking out from a deeply nested loop
label .breakout
print("Freedom!")
```

**Ausgabe (Python 2.3):**
```py
I am trapped, please rescue!
I am trapped, please rescue!
Freedom!
```

#### 💡 Erklärung:
- Eine funktionierende Version von `goto` in Python wurde als Aprilscherz am 1. April 2004 [angekündigt](https://mail.python.org/pipermail/python-announce-list/2004-April/002982.html).
- Aktuelle Versionen von Python haben dieses Modul nicht.
- Auch wenn es funktioniert, benutze es bitte nicht. Hier ist die [Antwort](https://docs.python.org/3/faq/design.html#why-is-there-no-goto), warum `goto` in Python nicht verwendet wird.

---

### ▶ Halte dich fest!
<!-- Example ID: 5c0c75f2-ddd9-4da3-ba49-c4be7ec39acf --->
Wenn du zu den Leuten gehörst, die keine Leerzeichen in Python verwenden wollen, um Bereiche zu kennzeichnen, kannst du den C-Stil {} verwenden, indem du folgendes importierst:

```py
from __future__ import braces
```

**Ausgabe:**
```py
  File "some_file.py", line 1
    from __future__ import braces
SyntaxError: not a chance
```

Klammern? Niemals! Wenn du enttäuscht bist, nutze Java. Okay, eine weitere überraschende Sache, kannst du herausfinden, wo `SyntaxError` im `__future__` Mmodul geworfen wird [code](https://github.com/python/cpython/blob/master/Lib/__future__.py)?

#### 💡 Erklärung:
+ Das `__future__` Modul wird normalerweise benutzt, um Features von zukünftigen Python Versionen bereitzustellen. Das "future" is in diesem spezifischen Kontext ironisch gemeint.
+ Das ist ein easter egg die die Gefühle der Community in dieser Frage wiederspiegeln.
+ Der Code ist tatsächlich [hier](https://github.com/python/cpython/blob/025eb98dc0c1dc27404df6c544fc2944e0fa9f3a/Python/future.c#L49) in der Datei `future.c` verfügbar.
+ Wenn der CPython Compiler auf ein  [future Statement](https://docs.python.org/3.3/reference/simple_stmts.html#future-statements) trifft, wird zunächst der entsprechende Code in `future.c` ausgeführt, bevor es als normale Importanweisung behandelt wird.

---

### ▶ Let's meet Friendly Language Uncle For Life
<!-- Example ID: 6427fae6-e959-462d-85da-ce4c94ce41be --->
**Ausgabe (Python 3.x)**
```py
>>> from __future__ import barry_as_FLUFL
>>> "Ruby" != "Python" # Hier bestehen keine Zweifel
  File "some_file.py", line 1
    "Ruby" != "Python"
              ^
SyntaxError: invalid syntax

>>> "Ruby" <> "Python"
True
```

Das wars schon.

#### 💡 Erklärung:
-Das ist relevant für [PEP-401](https://www.python.org/dev/peps/pep-0401/), was am 1. April 2009 veröffentlicht wurde (nun weißt du, was das heißt).
- Zitat vom PEP-401
  
  > Recognized that the != inequality operator in Python 3.0 was a horrible, finger-pain inducing mistake, the FLUFL reinstates the <> diamond operator as the sole spelling.
- There were more things that Uncle Barry had to share in the PEP; you can read them [here](https://www.python.org/dev/peps/pep-0401/).
- It works well in an interactive environment, but it will raise a `SyntaxError` when you run via python file (see this [issue](https://github.com/satwikkansal/wtfpython/issues/94)). However, you can wrap the statement inside an `eval` or `compile` to get it working,
    ```py
    from __future__ import barry_as_FLUFL
    print(eval('"Ruby" <> "Python"'))
    ```

---

### ▶ Selbst Python versteht, dass Liebe kompliziert ist
<!-- Example ID: b93cad9e-d341-45d1-999c-fcdce65bed25 --->
```py
import this
```

Warte, was ist **this**? `this` ist love :heart:

**Ausgabe:**
```
Der Zen von Python, von Tim Peters

Beautiful is better than ugly.
Explicit is better than implicit.
Simple is better than complex.
Complex is better than complicated.
Flat is better than nested.
Sparse is better than dense.
Readability counts.
Special cases aren't special enough to break the rules.
Although practicality beats purity.
Errors should never pass silently.
Unless explicitly silenced.
In the face of ambiguity, refuse the temptation to guess.
There should be one-- and preferably only one --obvious way to do it.
Although that way may not be obvious at first unless you're Dutch.
Now is better than never.
Although never is often better than *right* now.
If the implementation is hard to explain, it's a bad idea.
If the implementation is easy to explain, it may be a good idea.
Namespaces are one honking great idea -- let's do more of those!
```

Das ist der Zen von Python!

```py
>>> love = this
>>> this is love
True
>>> love is True
False
>>> love is False
False
>>> love is not True or False
True
>>> love is not True or False; love is love  # Love is complicated
True
```

#### 💡 Erklärung:

* `this` module in Python is an easter egg for The Zen Of Python ([PEP 20](https://www.python.org/dev/peps/pep-0020)).
* And if you think that's already interesting enough, check out the implementation of [this.py](https://hg.python.org/cpython/file/c3896275c0f6/Lib/this.py). Interestingly, **the code for the Zen violates itself** (and that's probably the only place where this happens).
* Regarding the statement `love is not True or False; love is love`, ironic but it's self-explanatory (if not, please see the examples related to `is` and `is not` operators).

---

### ▶ Ja, es existiert!
<!-- Example ID: 4286db3d-1ea7-47c9-8fb6-a9a04cac6e49 --->
**The `else` clause for loops.** Ein typisches Beispiel wäre:

```py
  def does_exists_num(l, to_find):
      for num in l:
          if num == to_find:
              print("Exists!")
              break
      else:
          print("Does not exist")
```

**Ausgabe:**
```py
>>> some_list = [1, 2, 3, 4, 5]
>>> does_exists_num(some_list, 4)
Exists!
>>> does_exists_num(some_list, -1)
Does not exist
```

**The `else` clause in exception handling.** Ein Beispiel:

```py
try:
    pass
except:
    print("Exception occurred!!!")
else:
    print("Try block executed successfully...")
```

**Ausgabe:**
```py
Try block executed successfully...
```

#### 💡 Erklärung:
- The `else` clause after a loop is executed only when there's no explicit `break` after all the iterations. You can think of it as a "nobreak" clause.
- `else` clause after a try block is also called "completion clause" as reaching the `else` clause in a `try` statement means that the try block actually completed successfully.

---
### ▶ Ellipsen *
<!-- Example ID: 969b7100-ab3d-4a7d-ad7d-a6be16181b2b --->
```py
def some_func():
    Ellipsis
```

**Ausgabe**
```py
>>> some_func()
# Keine Ausgabe, Kein Fehler

>>> SomeRandomString
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'SomeRandomString' is not defined

>>> Ellipsis
Ellipsis
```

#### 💡 Erklärung
- In Python, `Ellipsis` ist ein global verfügbares built-in Objekt, was äquivalent ist zu `...`.
    ```py
    >>> ...
    Ellipsis
    ```
- Ellipsis can be used for several purposes,
    + As a placeholder for code that hasn't been written yet (just like `pass` statement)
    + In slicing syntax to represent the full slices in remaining direction
    ```py
    >>> import numpy as np
    >>> three_dimensional_array = np.arange(8).reshape(2, 2, 2)
    array([
        [
            [0, 1],
            [2, 3]
        ],

        [
            [4, 5],
            [6, 7]
        ]
    ])
    ```
    So our `three_dimensional_array` is an array of array of arrays. Let's say we want to print the second element (index `1`) of all the innermost arrays, we can use Ellipsis to bypass all the preceding dimensions
    ```py
    >>> three_dimensional_array[:,:,1]
    array([[1, 3],
       [5, 7]])
    >>> three_dimensional_array[..., 1] # using Ellipsis.
    array([[1, 3],
       [5, 7]])
    ```
    Note: this will work for any number of dimensions. You can even select slice in first and last dimension and ignore the middle ones this way (`n_dimensional_array[firs_dim_slice, ..., last_dim_slice]`)
    + In [type hinting](https://docs.python.org/3/library/typing.html) to indicate only a part of the type (like `(Callable[..., int]` or `Tuple[str, ...]`))
    + You may also use Ellipsis as a default function argument (in the cases when you want to differentiate between the "no argument passed" and "None value passed" scenarios).

---

### ▶ Einbindung
<!-- Example ID: ff473ea8-a3b1-4876-a6f0-4378aff790c1 --->
Die Schreibweise ist beabsichtigt. Bitte schicke keinen Patch hierfür ab.

**Ausgabe (Python 3.x):**
```py
>>> infinity = float('infinity')
>>> hash(infinity)
314159
>>> hash(float('-inf'))
-314159
```

#### 💡 Erklärung:
- Hash of infinity is 10⁵ x π.
- Interestingly, the hash of `float('-inf')` is "-10⁵ x π" in Python 3, whereas "-10⁵ x e" in Python 2.

---

### ▶ Lass uns demolieren
<!-- Example ID: 37146d2d-9e67-43a9-8729-3c17934b910c --->
1\.
```py
class Yo(object):
    def __init__(self):
        self.__honey = True
        self.bro = True
```

**Ausgabe:**
```py
>>> Yo().bro
True
>>> Yo().__honey
AttributeError: 'Yo' object has no attribute '__honey'
>>> Yo()._Yo__honey
True
```

2\.
```py
class Yo(object):
    def __init__(self):
        # Versuchen wir es dieses Mal mit etwas Symmetrischem
        self.__honey__ = True
        self.bro = True
```

**Ausgabe:**
```py
>>> Yo().bro
True

>>> Yo()._Yo__honey__
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
AttributeError: 'Yo' object has no attribute '_Yo__honey__'
```

Warum hat `Yo()._Yo__honey` funktioniert?

3\.

```py
_A__variable = "Some value"

class A(object):
    def some_func(self):
        return __variable # noch nirgends initialisiert
```

**Ausgabe:**
```py
>>> A().__variable
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
AttributeError: 'A' object has no attribute '__variable'

>>> A().some_func()
'Some value'
```


#### 💡 Erklärung:

* [Name Mangling](https://en.wikipedia.org/wiki/Name_mangling) wird verwendet, um Namenskollisionen zwischen verschiedenen namespaces zu vermeiden.
* In Python, the interpreter modifies (mangles) the class member names starting with `__` (double underscore a.k.a "dunder") and not ending with more than one trailing underscore by adding `_NameOfTheClass` in front.
* So, to access `__honey` attribute in the first snippet, we had to append `_Yo` to the front, which would prevent conflicts with the same name attribute defined in any other class.
* But then why didn't it work in the second snippet? Because name mangling excludes the names ending with double underscores.
* The third snippet was also a consequence of name mangling. The name `__variable` in the statement `return __variable` was mangled to `_A__variable`, which also happens to be the name of the variable we declared in the outer scope.
* Also, if the mangled name is longer than 255 characters, truncation will happen.

---
---

## Kapitel: Der Schein trügt!

### ▶ Zeilen überspringen?
<!-- Example ID: d50bbde1-fb9d-4735-9633-3444b9d2f417 --->
**Ausgabe:**
```py
>>> value = 11
>>> valuе = 32
>>> value
11
```

Was?

**Note:** Um dies zu reproduzieren, kopiere einfach die Anweisungen aus dem obigen Ausschnitt und füge sie in deine Datei/Shell ein.

#### 💡 Erklärung

Some non-Western characters look identical to letters in the English alphabet but are considered distinct by the interpreter.

```py
>>> ord('е') # cyrillic 'e' (Ye)
1077
>>> ord('e') # latin 'e', as used in English and typed using standard keyboard
101
>>> 'е' == 'e'
False

>>> value = 42 # latin e
>>> valuе = 23 # cyrillic 'e', Python 2.x interpreter would raise a `SyntaxError` here
>>> value
42
```

The built-in `ord()` function returns a character's Unicode [code point](https://en.wikipedia.org/wiki/Code_point), and different code positions of Cyrillic 'e' and Latin 'e' justify the behavior of the above example.

---

### ▶ Teleportation

<!-- Example ID: edafe923-0c20-4315-b6e1-0c31abfc38f5 --->

```py
# `pip install numpy` vorher.
import numpy as np

def energy_send(x):
    # Initialisiere ein numpy array
    np.array([float(x)])

def energy_receive():
    # Gib ein leeres numpy array zurück
    return np.empty((), dtype=np.float).tolist()
```

**Ausgabe:**
```py
>>> energy_send(123.456)
>>> energy_receive()
123.456
```

Wo ist der Nobelpreis?

#### 💡 Erklärung:

* Notice that the numpy array created in the `energy_send` function is not returned, so that memory space is free to reallocate.
* `numpy.empty()` returns the next free memory slot without reinitializing it. This memory spot just happens to be the same one that was just freed (usually, but not always).

---

### ▶ Da ist wohl irgendwas faul...
<!-- Example ID: cb6a37c5-74f7-44ca-b58c-3b902419b362 --->
```py
def square(x):
    """
    Eine einfahce FUnktion, um das Quadrat einer Zahl durch Addition zu bestimmen
    """
    sum_so_far = 0
    for counter in range(x):
        sum_so_far = sum_so_far + x
  return sum_so_far
```

**Ausgabe (Python 2.x):**

```py
>>> square(10)
10
```

Sollte das nicht 100 sein?

**Note:** Wenn du das Ergebnis nicht reproduzieren kannst, versuch die Datei [mixed_tabs_and_spaces.py](/mixed_tabs_and_spaces.py) via shell auszuführen.

#### 💡 Erklärung

* **Don't mix tabs and spaces!** The character just preceding return is a "tab",  and the code is indented by multiple of "4 spaces" elsewhere in the example.
* This is how Python handles tabs:
  
  > First, tabs are replaced (from left to right) by one to eight spaces such that the total number of characters up to and including the replacement is a multiple of eight <...>
* So the "tab" at the last line of `square` function is replaced with eight spaces, and it gets into the loop.
* Python 3 is kind enough to throw an error for such cases automatically.

    **Ausgabe (Python 3.x):**
    ```py
    TabError: inconsistent use of tabs and spaces in indentation
    ```

---
---

## Kapitel: Sonstiges


### ▶ `+=` ist schneller
<!-- Example ID: bfd19c60-a807-4a26-9598-4912b86ddb36 --->

```py
# using "+", three strings:
>>> timeit.timeit("s1 = s1 + s2 + s3", setup="s1 = ' ' * 100000; s2 = ' ' * 100000; s3 = ' ' * 100000", number=100)
0.25748300552368164
# using "+=", three strings:
>>> timeit.timeit("s1 += s2 + s3", setup="s1 = ' ' * 100000; s2 = ' ' * 100000; s3 = ' ' * 100000", number=100)
0.012188911437988281
```

#### 💡 Erklärung:
+ `+=` ist schneller als `+`, um mehr als zwei String zu konkatenieren, weil der erste String (Beispiel: `s1` für `s1 += s2 + s3`), während der Kalkulation des gesamten Strings, nicht zerstört wird.

---

### ▶ Lass uns einen gigantischen String machen!
<!-- Example ID: c7a07424-63fe-4504-9842-8f3d334f28fc --->
```py
def add_string_with_plus(iters):
    s = ""
    for i in range(iters):
        s += "xyz"
    assert len(s) == 3*iters

def add_bytes_with_plus(iters):
    s = b""
    for i in range(iters):
        s += b"xyz"
    assert len(s) == 3*iters

def add_string_with_format(iters):
    fs = "{}"*iters
    s = fs.format(*(["xyz"]*iters))
    assert len(s) == 3*iters

def add_string_with_join(iters):
    l = []
    for i in range(iters):
        l.append("xyz")
    s = "".join(l)
    assert len(s) == 3*iters

def convert_list_to_string(l, iters):
    s = "".join(l)
    assert len(s) == 3*iters
```

**Ausgabe:**

```py
# Executed in ipython shell using %timeit for better readability of results.
# You can also use the timeit module in normal python shell/scriptm=, example usage below
# timeit.timeit('add_string_with_plus(10000)', number=1000, globals=globals())

>>> NUM_ITERS = 1000
>>> %timeit -n1000 add_string_with_plus(NUM_ITERS)
124 µs ± 4.73 µs per loop (mean ± std. dev. of 7 runs, 100 loops each)
>>> %timeit -n1000 add_bytes_with_plus(NUM_ITERS)
211 µs ± 10.5 µs per loop (mean ± std. dev. of 7 runs, 1000 loops each)
>>> %timeit -n1000 add_string_with_format(NUM_ITERS)
61 µs ± 2.18 µs per loop (mean ± std. dev. of 7 runs, 1000 loops each)
>>> %timeit -n1000 add_string_with_join(NUM_ITERS)
117 µs ± 3.21 µs per loop (mean ± std. dev. of 7 runs, 1000 loops each)
>>> l = ["xyz"]*NUM_ITERS
>>> %timeit -n1000 convert_list_to_string(l, NUM_ITERS)
10.1 µs ± 1.06 µs per loop (mean ± std. dev. of 7 runs, 1000 loops each)
```

Let's increase the number of iterations by a factor of 10.

```py
>>> NUM_ITERS = 10000
>>> %timeit -n1000 add_string_with_plus(NUM_ITERS) # Linear increase in execution time
1.26 ms ± 76.8 µs per loop (mean ± std. dev. of 7 runs, 1000 loops each)
>>> %timeit -n1000 add_bytes_with_plus(NUM_ITERS) # Quadratic increase
6.82 ms ± 134 µs per loop (mean ± std. dev. of 7 runs, 1000 loops each)
>>> %timeit -n1000 add_string_with_format(NUM_ITERS) # Linear increase
645 µs ± 24.5 µs per loop (mean ± std. dev. of 7 runs, 1000 loops each)
>>> %timeit -n1000 add_string_with_join(NUM_ITERS) # Linear increase
1.17 ms ± 7.25 µs per loop (mean ± std. dev. of 7 runs, 1000 loops each)
>>> l = ["xyz"]*NUM_ITERS
>>> %timeit -n1000 convert_list_to_string(l, NUM_ITERS) # Linear increase
86.3 µs ± 2 µs per loop (mean ± std. dev. of 7 runs, 1000 loops each)
```

#### 💡 Erklärung
- You can read more about [timeit](https://docs.python.org/3/library/timeit.html) or [%timeit](https://ipython.org/ipython-doc/dev/interactive/magics.html#magic-timeit) on these links. They are used to measure the execution time of code pieces.
- Don't use `+` for generating long strings — In Python, `str` is immutable, so the left and right strings have to be copied into the new string for every pair of concatenations. If you concatenate four strings of length 10, you'll be copying (10+10) + ((10+10)+10) + (((10+10)+10)+10) = 90 characters instead of just 40 characters. Things get quadratically worse as the number and size of the string increases (justified with the execution times of `add_bytes_with_plus` function)
- Therefore, it's advised to use `.format.` or `%` syntax (however, they are slightly slower than `+` for very short strings).
- Or better, if already you've contents available in the form of an iterable object, then use `''.join(iterable_object)` which is much faster.
- Unlike `add_bytes_with_plus` because of the `+=` optimizations discussed in the previous example, `add_string_with_plus` didn't show a quadratic increase in execution time. Had the statement been `s = s + "x" + "y" + "z"` instead of `s += "xyz"`, the increase would have been quadratic.
  ```py
  def add_string_with_plus(iters):
      s = ""
      for i in range(iters):
          s = s + "x" + "y" + "z"
      assert len(s) == 3*iters

  >>> %timeit -n100 add_string_with_plus(1000)
  388 µs ± 22.4 µs per loop (mean ± std. dev. of 7 runs, 1000 loops each)
  >>> %timeit -n100 add_string_with_plus(10000) # Quadratic increase in execution time
  9 ms ± 298 µs per loop (mean ± std. dev. of 7 runs, 100 loops each)
  ```
- So viele Möglichkeiten einen gigantischen String zu erzeugen und zu formatieren stehen irgendwie in Kontrast zum [Zen von Python](https://www.python.org/dev/peps/pep-0020/), nachdem gilt:
  
    > Es sollte einen - und vorzugsweise nur einen - offensichtlichen Weg geben, dies zu tun.

---

### ▶ Verlangsamen von `dict` Lookups *
<!-- Example ID: c9c26ce6-df0c-47f7-af0b-966b9386d4c3 --->
```py
some_dict = {str(i): 1 for i in range(1_000_000)}
another_dict = {str(i): 1 for i in range(1_000_000)}
```

**Ausgabe:**
```py
>>> %timeit some_dict['5']
28.6 ns ± 0.115 ns per loop (mean ± std. dev. of 7 runs, 10000000 loops each)
>>> some_dict[1] = 1
>>> %timeit some_dict['5']
37.2 ns ± 0.265 ns per loop (mean ± std. dev. of 7 runs, 10000000 loops each)

>>> %timeit another_dict['5']
28.5 ns ± 0.142 ns per loop (mean ± std. dev. of 7 runs, 10000000 loops each)
>>> another_dict[1]  # Trying to access a key that doesn't exist
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
KeyError: 1
>>> %timeit another_dict['5']
38.5 ns ± 0.0913 ns per loop (mean ± std. dev. of 7 runs, 10000000 loops each)
```
Wieso werden dieselben lookups immer langsamer?

#### 💡 Erklärung:
+ CPython has a generic dictionary lookup function that handles all types of keys (`str`, `int`, any object ...), and a specialized one for the common case of dictionaries composed of `str`-only keys.
+ The specialized function (werden `lookdict_unicode` in CPythons [code](https://github.com/python/cpython/blob/522691c46e2ae51faaad5bbbce7d959dd61770df/Objects/dictobject.c#L841) genannt) knows all existing keys (including the looked-up key) are strings, and uses the faster & simpler string comparison to compare keys, instead of calling the `__eq__` method.
+ The first time a `dict` instance is accessed with a non-`str` key, it's modified so future lookups use the generic function.
+ This process is not reversible for the particular `dict` instance, and the key doesn't even have to exist in the dictionary. That's why attempting a failed lookup has the same effect.


### ▶ Blähende Instanz `dict`s *
<!-- Example ID: fe706ab4-1615-c0ba-a078-76c98cbe3f48 --->
```py
import sys

class SomeClass:
    def __init__(self):
        self.some_attr1 = 1
        self.some_attr2 = 2
        self.some_attr3 = 3
        self.some_attr4 = 4


def dict_size(o):
    return sys.getsizeof(o.__dict__)

```

**Ausgabe:** (Python 3.8, oder Python 3 Versionen können ein bisschen variieren)
```py
>>> o1 = SomeClass()
>>> o2 = SomeClass()
>>> dict_size(o1)
104
>>> dict_size(o2)
104
>>> del o1.some_attr1
>>> o3 = SomeClass()
>>> dict_size(o3)
232
>>> dict_size(o1)
232
```

Versuchen wir es noch einmal... In einem neuen Interpreter:

```py
>>> o1 = SomeClass()
>>> o2 = SomeClass()
>>> dict_size(o1)
104  # as expected
>>> o1.some_attr5 = 5
>>> o1.some_attr6 = 6
>>> dict_size(o1)
360
>>> dict_size(o2)
272
>>> o3 = SomeClass()
>>> dict_size(o3)
232
```

What makes those dictionaries become bloated? And why are newly created objects bloated as well?

#### 💡 Erklärung:
+ CPython is able to reuse the same "keys" object in multiple dictionaries. This was added in [PEP 412](https://www.python.org/dev/peps/pep-0412/) with the motivation to reduce memory usage, specifically in dictionaries of instances - where keys (instance attributes) tend to be common to all instances.
+ This optimization is entirely seamless for instance dictionaries, but it is disabled if certain assumptions are broken.
+ Key-sharing dictionaries do not support deletion; if an instance attribute is deleted, the dictionary is "unshared", and key-sharing is disabled for all future instances of the same class.
+ Additionaly, if the dictionary keys have been resized (because new keys are inserted), they are kept shared *only* if they are used by a exactly single dictionary (this allows adding many attributes in the `__init__` of the very first created instance, without causing an "unshare"). If multiple instances exist when a resize happens, key-sharing is disabled for all future instances of the same class: CPython can't tell if your instances are using the same set of attributes anymore, and decides to bail out on attempting to share their keys.
+ A small tip, if you aim to lower your program's memory footprint: don't delete instance attributes, and make sure to initialize all attributes in your `__init__`!


### ▶ Kleinigkeiten *
<!-- Example ID: f885cb82-f1e4-4daa-9ff3-972b14cb1324 --->
* `join()` ist eine String-Operation anstatt einer List-Operation. (auf den ersten Blick nicht einfach zu verstehen)

  **💡 Erklärung:** Wenn `join()` eine Methode auf einem String ist, dann kann es auf irgendeinem Iterable operieren (Liste, Tuple, Iteratoren). Wäre es eine Methode auf einer Liste, müsste sie von jedem Typ separat implementiert werden. Außerdem macht es nicht viel Sinn, eine String-spezifische Methode auf eine generische API eines `listen`-Objektes anzuwenden
  
* Ein paar komisch aussehende aber semantisch korrekte Statements:
  + `[] = ()` ist ein semantisch korrektes Statement (entpacken eines leeren `Tuples` in eine leere `Liste`)
  + `'a'[0][0][0][0][0]` ist auch semantisch korrect, weil Python keinen Char-Datentyp wie viele andere Sprachen, die auf C basieren, hat. Also ergibt das Auswählen eines einzelnen Characters aus einem String einen Single-character String.
  + `3 --0-- 5 == 8` und `--5 == 5` sind beides semantisch korrekte Statements und wird zu `True` ausgewertet.

* Sei `a` eine Zahl, `++a` und `--a` sind beides valide Python Statements aber sie verhaten sich nicht so wie vergleichbare Statements in Sprachen wie C, C++, oder Java.
  ```py
  >>> a = 5
  >>> a
  5
  >>> ++a
  5
  >>> --a
  5
  ```

  **💡 Erklärung:**
  + Es gibt keinen `++` Operator in der Python Grammatik. Es handelt sich eigentlich um zwei `+` Operatoren.
  + `++a` parst eigentlich `+(+a)` was übersetzt wird zu `a`. In ähnlicher Weise kann die Ausgabe des Statement `--a` begründet werden.
  + Dieser StackOverflow [Thread](https://stackoverflow.com/questions/3654830/why-are-there-no-and-operators-in-python) erörtert die Gründe für das Fehlen von Inkrement- und Dekrementoperatoren in Python.

* Der Walrus Operator in Python sollte dir bekannt sein. Aber hast du schon mal von dem *space-invader Operator* gehört?
  ```py
  >>> a = 42
  >>> a -=- 1
  >>> a
  43
  ```
  Er wird als alternativer Inkrementierungsoperator verwendet, zusammen mit einem anderen Operator
  ```py
  >>> a +=+ 1
  >>> a
  >>> 44
  ```
  **💡 Erklärung:** Dieser Streich kommt von [Raymond Hettingers Tweet](https://twitter.com/raymondh/status/1131103570856632321?lang=en). Der Space Invader Operator ist tatsächlich nur ein schlecht formatiertes `a -= (-1)`, was äquivalent zu `a = a - (- 1)` ist. Ähnliches gilt für `a += (+ 1)`.
  
* Python hat einen undokumentierten [umgekehrten Implikations](https://en.wikipedia.org/wiki/Converse_implication) Operator. 
     
     ```py
     >>> False ** False == True
     True
     >>> False ** True == False
     True
     >>> True ** False == True
     True
     >>> True ** True == True
     True
     ```

     **💡 Erklärung:** If you replace `False` and `True` by 0 and 1 and do the maths, the truth table is equivalent to a converse implication operator. ([Quelle](https://github.com/cosmologicon/pywat/blob/master/Erklärung.md#the-undocumented-converse-implication-operator))
     
* Weil wir über Operatoren sprechen, erwähnen wir auch den `@` Ooperator, der für Matrixmultiplikation benutzt wird (Keine Sorge, diese mal ist es ernst).

     ```py
     >>> import numpy as np
     >>> np.array([2, 2, 2]) @ np.array([7, 8, 8])
     46
     ```

     **💡 Erklärung:** Der `@` Operator wurde, mit der wissenschaftlichen Community im Hinterkopf, in Python 3.5 eingeführt. Jedes Objekt kann die magische `__matmul__`  Method überladen, um ein bestimmtes Verhalten für diesen Operator zu definieren.

* Ab Python 3.8 kannst du eine typische f-String-Syntax wie `f'{some_var=}` für schnelles Debugging verwenden. Zum Beispiel:
    ```py
    >>> some_string = "wtfpython"
    >>> f'{some_string=}'
    "some_string='wtfpython'"
    ``` 

* Python nutzt 2 Bytes die Speicherung lokaler Variablen in Funktionen. Theoretisch heißt das, dass nur 65536 Variablen in einer Funktion gespeichert werden können. Allerdings hat Python eine praktische, eingebaute Lösung, die benutzt werden kann, um mehr als 2^16 Variablennamen zu speichern. Der folgende Code demonstriert, was im Stack passiert, wenn mehr als 65536 lokale Variablen definiert werden (Warnung: Dieser Code gibt ungefähr 2^18 Zeilen Text aus, also sei darauf vorbereitet!):
     
     ```py
     import dis
    exec("""
    def f():
        """ + """
        """.join(["X" + str(x) + "=" + str(x) for x in range(65539)]))

    f()

    print(dis.dis(f))
    ```
     
* Mehrere Python Threads werden deinen *Python code* nicht gleichzeitig laufen lassen (Ja, du hast richtig gehört!).
Es mag intuitiv erscheinen, mehrere Threads zu erzeugen, die dann deinen Python code gleichzeitig ausführen, aber wegen dem [Global Interpreter Lock](https://wiki.python.org/moin/GlobalInterpreterLock) in Python, sorgst du nur dafür, dass die Threads abwechselnd auf demselben Kern ausgeführt werden. 
Python Threads sind gut für IO-gebundene Aufgaben, aber um tatsächliche Parallelisierung für CPU-gebundene Aufgaben in Python zu erreichen, solltest du lieber das Python [multiprocessing](https://docs.python.org/3/library/multiprocessing.html) Modul benutzen.

* Manchmal gibt die `print` Methode die Werte nicht sofort aus. Zum Beispiel:

     ```py
     # File some_file.py
     import time
     
     print("wtfpython", end="_")
     time.sleep(3)
     ```

    Das wird `wtfpython` nach 3 Sekunden, aufgrund des `end` Argumentes ausgeben, wei der Ausgabe-Puffer, entweder nach `\n` oder wenn das Programm die Ausführung beendet, geflusht wird. Mit dem Argument `flush=True` können wir den Puffer zum Flushen zwingen.

* List slicing mit Indices, die nicht innerhalb der Grenzen liegen, wirft keinen Fehler
  ```py
  >>> some_list = [1, 2, 3, 4, 5]
  >>> some_list[111:]
  []
  ```

* Slicing eines Iterables erzeugt nicht immer ein neues Objekt. Zum Beispiel:
    ```py
    >>> some_str = "wtfpython"
    >>> some_list = ['w', 't', 'f', 'p', 'y', 't', 'h', 'o', 'n']
    >>> some_list is some_list[:] # False erwartet, weil ein neues Objekt erzeugt wird.
    False
    >>> some_str is some_str[:] # True, weil Strings immutable sind, daher ist die Erstellung eines neuen Objektes sinnlos.
    True
    ```

* `int('١٢٣٤٥٦٧٨٩')` gibt `123456789` in Python 3 zurück. In Python umfassen Dezimalzeichen auch Ziffernzeichen, und alle Zeichen, die zum Erstellen von Dezimal-Radix-Nummern benutzt werden können, z.B. U+0660, ARABIC-INDIC DIGIT ZERO. Hier  ist eine [interessante Geschichte](https://chris.improbable.org/2014/8/25/adventures-in-unicode-digits/) im Zusammenhang mit diesem Verhalten in Python.

* Du kannst numerische Literale mit Unterstrichen trennen, um die Lesbarkeit zu erhöhen (Python 3 spezifisch).

     ```py
     >>> sechs_millionen = 6_000_000
     >>> sechs_millionen
     6000000
     >>> sechs_millionen = 0xF00D_CAFE
     >>> sechs_millionen
     4027435774
     ```

* `'abc'.count('') == 4`. Here's an approximate implementation of `count` method, which would make the things more clear
  ```py
  def count(s, sub):
      result = 0
      for i in range(len(s) + 1 - len(sub)):
          result += (s[i:i + len(sub)] == sub)
      return result
  ```
  Das Verhalten ist darauf zurückzuführen, dass leere Teilstrings (`''`) mit Slices der Länge 0 in der ursprünglichen Zeichenkette übereinstimmen 
---
---

# Contributing

Ein paar Wege, wie du zu wtfpython beitragen kannst:

- neue Beispiele vorschlagen
- bei der Übersetzung helfen (Siehe [issues sind mit 'translation' markiert](https://github.com/satwikkansal/wtfpython/issues?q=is%3Aissue+is%3Aopen+label%3Atranslation))
- Verbesserungen vorschlagen, z.B. Aufzeigen von veralteten Schnipseln, Typen, Formatfehlern, etc.
- Lücken identifizieren (z.B. unzureichende Erklärungen, überflüssige Beispiele, etc.)
- Irgendwelche kreativen Vorschläge unterbreiten, um dieses Projekt spaßiger und nützlicher zu machen

Für mehr Details, wirf bitte einen Blick auf [CONTRIBUTING.md](/CONTRIBUTING.md). Erstelle ruhig ein neues [Issue](https://github.com/satwikkansal/wtfpython/issues/new), um zu diskutieren.

PS: Bitte keine Anfragen mit Links erstellen. Es werden keine Links hinzugefügt, es sein denn sie sind für das Projekt relevant.

# Anerkennung

Die Idee und das Design für diese Sammlung wurden durch Denys Dovhans tolles Projekt inspiriert [wtfjs](https://github.com/denysdovhan/wtfjs). Der überragende Support von Pythonisten hat es zu dem gemacht, was es heute ist.

#### Ein paar nützliche Links!
* https://www.youtube.com/watch?v=sH4XF6pKKmk
* https://www.reddit.com/r/Python/comments/3cu6ej/what_are_some_wtf_things_about_python
* https://sopython.com/wiki/Common_Gotchas_In_Python
* https://stackoverflow.com/questions/530530/python-2-x-gotchas-and-landmines
* https://stackoverflow.com/questions/1011431/common-pitfalls-in-python
* https://www.python.org/doc/humor/
* https://github.com/cosmologicon/pywat#the-undocumented-converse-implication-operator
* https://www.codementor.io/satwikkansal/python-practices-for-efficient-code-performance-memory-and-usability-aze6oiq65
* https://github.com/wemake-services/wemake-python-styleguide/search?q=wtfpython&type=Issues
* WFTPython discussion threads on [Hacker News](https://news.ycombinator.com/item?id=21862073) and [Reddit](https://www.reddit.com/r/programming/comments/edsh3q/what_the_fck_python_30_exploring_and/).

# 🎓 License

[![WTFPL 2.0][license-image]][license-url]

&copy; [Satwik Kansal](https://satwikkansal.xyz)

[license-url]: http://www.wtfpl.net
[license-image]: https://img.shields.io/badge/License-WTFPL%202.0-lightgrey.svg?style=flat-square

## Überrasche auch deine Freunde!

Wenn du wtfpython cool findest, kannst du diese Quick-Links nutzen, um es mit deinen Freunden zu teilen:

[Twitter](https://twitter.com/intent/tweet?url=https://github.com/satwikkansal/wtfpython&text=If%20you%20really%20think%20you%20know%20Python,%20think%20once%20more!%20Check%20out%20wtfpython&hashtags=python,wtfpython) | [Linkedin](https://www.linkedin.com/shareArticle?url=https://github.com/satwikkansal&title=What%20the%20f*ck%20Python!&summary=If%20you%20really%20thing%20you%20know%20Python,%20think%20once%20more!) | [Facebook](https://www.facebook.com/dialog/share?app_id=536779657179021&display=page&href=https%3A%2F%2Fgithub.com%2Fsatwikkansal%2Fwtfpython&quote=If%20you%20really%20think%20you%20know%20Python%2C%20think%20once%20more!)  

## Brauchst du eine pdf version?

Ich habe ein paar Anfragen für eine pdf (und epub) Version von wtfpython erhalten. Du kannst [hier](https://form.jotform.com/221593245656057) deine Daten angeben, um sie schnellstmöglich zu bekommen.

**Das ist alles, Freunde!** Um neue Updates zu erhalten, kannst du deine email [hier](https://form.jotform.com/221593598380062) hinzufügen.
