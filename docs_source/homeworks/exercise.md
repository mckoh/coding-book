# Übungsblatt

Ziel dieses Übungsblatts ist es, 60 Punkte zu erreichen. Ihr könnt aus folgenden Aufgaben frei wählen. Erstellt für jede ausgewählte Aufgabe eine eigene Datei. Ihr könnt in Teams von zwei Personen arbeiten.

## Einfache Aufgaben

### Darts (<span style="color:#33FF7D ">Einfach</span>, 15 Punkte)

Ziel dieses Projekts ist es, eine Funktion (`calculate_score()`) zu entwickeln, die die Punkte eines Dartwurfs berechnet. Bei dieser vereinfachten Variante des Darts wird die Punktezahl basierend auf dem Kreis ermittelt, in dem der Dartpfeil landet. Das Spielfeld besteht aus mehreren konzentrischen Kreisen, wobei jeder Kreis eine unterschiedliche Punktezahl hat.

- Der Pfeil landet außerhalb der Dartscheibe: `0 Punkte`
- Der Pfeil landet im äußersten Kreis: `1 Punkt`
- Der Pfeil landet im mittleren Kreis: `5 Punkte`
- Der Pfeil landet im innersten Kreis: `10 Punkte`

Der innerste Kreis hat einen Radius von `1`. Der mittlere Kreis hat einen Radius von `5`. Der äußerste Kreis und damit auch die Dartscheibe haben einen Radius von `10`.

Ein Wurf wird mit seinen `x` und `y` Koordinaten angegeben. Der Mittelpunkt der Dartscheibe ist mit den Koordinaten `(0, 0)` definiert.

```python
# Testfälle
calculate_score(-3.5, 3.5) # 5 Punkte
calculate_score(7.1, -7.1) # 0 Punkte
calculate_score(0, 10) # 1 Punkte
calculate_score(-0.1, -0.1) # 10 Punkte
```

### Palindrom prüfen (<span style="color:#33FF7D ">Einfach</span>, 15 Punkte)

Entwickle eine Funktion namens ``palindrom()``, die überprüft, ob ein gegebener String ein Palindrom ist. Ein Palindrom ist ein Wort, das von vorne und hinten gelesen identisch ist.

```python
# Testfälle
palindrom(`Otto`) # True
palindrom(`Anna`) # True
palindrom(`Reliefpfeiler`) # True
palindrom(`Racecar`) # True
palindrom(`Palindrom`) # False
palindrom(`Haus`) # False
palindrom(`Auto`) # False
```

### Fizz-Buzz (<span style="color:#33FF7D ">Einfach</span>, 15 Punkte)

Bei dem Spiel Fizz-Buzz zählen die Spieler abwechselnd von eins an aufwärts. Wenn eine Spielerin an der Reihe ist und die Zahl durch 3 teilbar ist, sagt sie "fizz" anstelle der Zahl, und wenn sie an der Reihe ist und die Zahl durch 5 teilbar ist, sagt sie "buzz" anstelle der Zahl. Wenn die Zahl sowohl ein Vielfaches von 3 als auch von 5 ist, sollte sie anstelle der Zahl "fizzbuzz" sagen.

Schreibe ein Programm ``fizz_buzz()``, das den Benutzer nach einer ganzen Zahl fragt. Das Programm soll bis zu dieser Zahl zählen und dabei die Spielregeln von Fizz-Buzz einhalten. Wenn es fertig ist, soll das Programm ausgeben, wie viele Zahlen auf dem Weg gezischt (fizz), gesummt (buzz) oder gebrummt (fizzbuff) wurden.

```python
fizz_buzz(8) # 1, 2, fizz, 4, buzz, fizz, 7, 8

# Num fizzed: 2
# Num buzzed: 1
# Num fizzbuzzed: 0
```

### Diamond (<span style="color:#FFB533 ">Mittel</span>, 30 Punkte)

Entwickle eine Function `diamond()` die auf der Konsole symmetrische Diamanten bestehend aus Buchstaben und Leerzeichen ausgibt. Die Funktion soll einen beliebigen Buchstaben des Alphabets (`"A"` bis `"Z"`) als Argument entgegennehmen und diesen anschließend zur Konstruktion der Diamantform verwenden. Beachte dabei folgende Regeln:

- Die erste Zeile enthält zentriert den Buchstaben `A`.
- Die letzte Zeile enthält zentriert den Buchstaben `A`.
- Alle Zeilen, bis auf die erste und die letzte, enthalten immer 2 identische Buchstaben.
- Alle Zeilen haben immer gleichviele Leerräume am Anfang und am Ende der Zeile (das können auch `0` Leerräume sein).
- Der Diamant ist horizontal und vertical symmetrisch.
- Der Diamant hat eine quadratische Struktur (Anzahl der Zeilen und Spalten ist identischt).
- Die Buchstaben formen die Diamant Struktur.
- Die obere Hälfte hat die Buchstaben aufsteigend sortiert (`A-Z`), die untere Hälfte hat die Buchstaben absteigend sortiert (`Z-A`).
- Die vier Ecken formen Dreiecke über die Leerräume

```python
# Testfälle

diamant("A")
A

diamant("B")
·A·
B·B
·A·

diamant("C")
··A··
·B·B·
C···C
·B·B·
··A··

diamant("E")
····A····
···B·B···
··C···C··
·D·····D·
E·······E
·D·····D·
··C···C··
···B·B···
····A····
```

### Längster String (<span style="color:#33FF7D ">Einfach</span>, 15 Punkte)

Erstelle eine Funktion `string_filter()`, der du eine beliebige Anzahl an Strings übergeben kannst. Die Funktion gibt dann den längsten der übergebenen Strings zurück. Sollte die maximale Länge auf mehrere Strings zutreffen, wird der zuerst übergebene String zurückgegeben.

```python
# Testfälle
string_filter("sometimes", "you", "eat", "the", "bear") # sometimes
string_filter("python", "is", "superb") # python
```

### Primzahlen prüfen (<span style="color:#33FF7D ">Einfach</span>, 15 Punkte)

Entwickle eine Funktion `is_prime()`, die überprüft, ob eine gegebene Zahl eine Primzahl ist. Eine Primzahl ist eine natürliche Zahl größer als 1, die nur durch 1 und sich selbst teilbar ist.

```python
# Testfälle
is_prime(8) # False
is_prime(9) # False
is_prime(10) # False
is_prime(240) # False
is_prime(1024) # False
is_prime(19) # True
is_prime(23) # True
is_prime(47) # True
is_prime(67) # True
is_prime(89) # True
```

## Mittelschwere Aufgaben

### Snake Case zu Camel Case (<span style="color:#FFB533 ">Mittel</span>, 30 Punkte)

Entwickle eine Funktion ``to_camel_case()``, die einen Variablennamen von der Snake Case Notation in die Camel Case Notation umwandelt. Nutze hierzu die String-Funktionen  [`split`](<https://docs.python.org/3/library/stdtypes.html#str.split)>), [`upper`](https://docs.python.org/3/library/stdtypes.html#str.upper), und/oder [`join`](https://docs.python.org/3/library/stdtypes.html#str.join).

```python
# Testfälle
to_camel_case("this_is_snake_case") # thisIsSnakeCase
to_camel_case("name") # name
to_camel_case("hallo_welt") # halloWelt
```

### Personen (<span style="color:#FFB533 ">Mittel</span>, 30 Punkte)

Erstellt eine Klasse `Person`. Die Klasse hat folgende Eigenschaften:

- Vorname
- Nachname
- E-Mail Adresse

Es soll möglich sein, bei der Erstellung eines Objekts entweder Vorname und Nachname zu übergeben werden, oder Vorname, Nachname und E-Mail-Adresse zu übergeben. Es soll auch die Funktion `get_full_name` implementiert werden. Diese Funktion gibt den Vornamen und Nachnamen mit einem Leerzeichen verbunden als String zurück.

Die Klasse `Person` soll zählen, wie viele Objekte erzeugt wurden.

### Gültige Passwörter (<span style="color:#FFB533 ">Mittel</span>, 30 Punkte)

Schreibt eine Funktion `correct_password()`, der eine String Liste übergeben wird. Jeder String hat folgendes Format: `low-high character: password`.

`low` gibt an, wie oft `character` mindestens in `password` vorkommen muss; `high` gibt an wie oft `character` maximal in `password` vorkommen darf. Zählt, wie viele der übergebenen Passwörter den Vorgaben entsprechen. Gebt die Anzahl der gültigen Passwörter auf der Konsole aus.

```python
# Testfälle
correct_password("1-3 a: abcde") # True
correct_password("1-3 b: cdefg") # False
correct_password("2-9 c: ccccccccc") # True
```

### Sekunden umrechnen (<span style="color:#FFB533 ">Mittel</span>, 30 Punkte)

Entwickle eine Funktion `covert_time()`, der man einen beliebigen Sekundenwert übergeben kann. Die Funktion rechnet dann die übergebenen Sekunden in Wochen, Tage, Stunden, Minuten und Sekunden um und gibt das Ergebnis als `str` zurück.

```python
# Testfälle
covert_time(66) # 1 Minute, 6 Sekunden
covert_time(148) # 2 Minuten, 28 Sekunden
covert_time(86400) # 1 Tag
covert_time(789891) # 1 Woche, 2 Tag, 3 Stunden, 24 Minuten, 51 Sekunden
```

### Primfaktorenzerlegung (<span style="color:#FFB533 ">Mittel</span>, 30 Punkte)

Entwickle eine Funktion `decompose()`, die für eine gegebene Zahl das Produkt der Primfaktoren berechnet. Jede natürliche Zahl kann als Produkt von Primzahlen dargestellt werden. Deine Funktion sollte wie folgt vorgehen:

* Eingabeüberprüfung: Stelle sicher, dass die übergebene Zahl eine natürliche Zahl größer als 1 ist.

* Primfaktorzerlegung: Zerlege die Zahl in ihre Primfaktoren. Beginne mit dem kleinsten Primfaktor (2) und arbeite dich zu größeren Primzahlen vor.

* Berechnung des Produkts: Multipliziere alle gefundenen Primfaktoren, um das Produkt zu berechnen.

```python
# Testfälle
decompose(12) # 2 * 2 * 3
decompose(123) # 3 * 41
decompose(360) # 2 * 2 * 2 * 3 * 3 * 5
decompose(754) # 2 * 13 * 29
```

### Cäsarverschlüsselung (<span style="color:#FFB533 ">Mittel</span>, 30 Punkte)

Erstelle ein Programm, mit dem du Text mit der Cäsar-Verschlüsselung ver- und entschlüsseln kannst. Bei der Cäsar-Verschlüsselung wird jeder Buchstabe um eine bestimmte Anzahl von Stellen im Alphabet verschoben. Die Verschiebung erfolgt nach vorne beim Verschlüsseln und nach hinten beim Entschlüsseln. Um es einfach zu halten, werden nur Großbuchstaben berücksichtigt und Leerzeichen bleiben unverändert. Implementiere das Programm als `CaesarCipher`-Klasse mit zumindest zwei Methoden:

- `encrypt()`: Verschiebt einen übergebenen String um die übergebenen Stellen im Alphabet nach vorne
- `decrypt()`: Verschiebt einen übergebenen String um die übergebenen Stellen im Alphabet nach hinten

```python
# Testfälle
cc = CaesarCipher(shift=3)
cc.encrypt("HALLO WELT") # KDOOR ZHOW

cc = CaesarCipher(shift=5)
cc.decrypt("KM PZKXYJNS") #FH KUFSTEIN
```

## Herausfordernde Aufgaben

### Memory (<span style="color:#C70039">Herausfordernd</span>, 40 Punkte)

Programmiere das Spiel [Memory](<https://de.wikipedia.org/wiki/Memory_(Spiel)>) Das Spiel soll 2 Spieler:innen unterstützen und aus einem 6x6-Spielfeld, somit 36 Karten bzw. 13 Paaren, bestehen. Die Karten sind die Buchstaben A bis M. Spieler:innen geben pro Durchgang für zwei Karten Zeile und Spalten für ein Feld, die umgedreht werden sollen, ein. Sollten die beiden Karten nicht zusammenpassen, werden die Karten wieder umgedreht.

### Tic Tac Toe (<span style="color:#C70039">Herausfordernd</span>, 40 Punkte)

Erstellt ein Programm, mit dem man Tic Tac Toe und 2 Spieler:innen spielen kann. Die Spieler:innen geben abwechselnd über die Konsole die Zeile und die Spalte ein, wo ein X bzw. O gesetzt werden wollen. Nach jeder Eingabe wird überprüft, ob das Feld bereits belegt ist. Ist das der Fall, wird der:die Spieler:in so lange aufgefordert, bis er:sie ein freies Feld wählt. Nach jeder korrekten Eingabe wird überprüft, ob jemand gewonnen hat.

### Bestellung (<span style="color:#C70039">Herausfordernd</span>, 40 Punkte)

Erstelle eine Klasse `order` die Bestellungen verwalten kann. Jede Bestellung erhält eine Bestellnummer, die aus dem Buchstaben B und einer fortlaufenden Nummer besteht (z.B. B1 für die erste Bestellung, B2 für die zweite usw.). Diese Bestellnummer wird automatisch beim Erstellen einer Bestellung vergeben.

Zusätzlich hat jede Bestellung ein Bestelldatum und einen Kommentar. Du kannst jeder Bestellung bis zu 5 Produkte hinzufügen. Überprüfe beim Hinzufügen von Produkten, ob die maximale Anzahl von 5 Produkten erreicht ist. Falls ja, soll die Funktion False zurückgeben und das Produkt nicht hinzufügen. In allen anderen Fällen gibt die Funktion True zurück und speichert das Produkt.

Produkte haben einen Namen, eine Beschreibung und einen Verkaufspreis. Für jede Bestellung muss es möglich sein, den Gesamtpreis zu berechnen. Der Gesamtpreis ergibt sich aus der Summe der Verkaufspreise der hinzugefügten Produkte.

### Summe der umliegenden Felder (<span style="color:#C70039">Herausfordernd</span>, 40 Punkte)

Erstelle eine Funktion ``transform_matrix()``, der du eine zweidimensionale int-Liste übergeben kannst. Diese Funktion soll für jede Position in der zweidimensionalen int-Liste die Summe der umliegenden Elemente (unten, oben, rechts, links und diagonal) berechnen.

```python
# Testfall
input_list = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

transform_matrix(input_list)

# Output
# [
#    [11, 19, 13],
#    [23, 40, 27],
#    [17, 31, 19]
# ]
```

### Schere, Stein, Papier, Echse, Spock (<span style="color:#C70039">Herausfordernd</span>, 40 Punkte)

Implementiere das Spiel [Schere, Stein, Papier, Echse, Spock](https://www.youtube.com/watch?v=03QhVJcuVoY). Nimm dazu die Spielzüge von zwei Spieler:innen nacheinander entgegen. Wenn beide Spieler:innen dieselbe Wahl getroffen haben, wird das Spiel so lange wiederholt, bis ein:e Spieler:in gewonnen hat. Es gelten folgende Regeln:

- Schere schneidet Papier
- Papier bedeckt Stein
- Stein zerquetscht Echse
- Echse vergiftet Spock
- Spock zertrümmert Schere
- Schere köpft Echse
- Echse frisst Papier
- Papier widerlegt Spock
- Spock verdampft Stein
- Stein zerstört Schere

Konzipiere eine effiziente Speicherung der Regeln, um zu vermeiden, 10 `if`-Statements benutzen zu müssen.

### Conways Spiel des Lebens (<span style="color:#C70039">Herausfordernd</span>, 40 Punkte)

Setzte [Conways Spiel des Lebens](https://de.wikipedia.org/wiki/Conways_Spiel_des_Lebens) mit hilfe von Python um. Bei diesem Spiel geht es darum, die Evolution von Zellen über mehrere Generationen zu berechnen. Es gibt ein rechteckiges Spielfeld von Zellen. Jede Zelle kann entweder tot oder lebendig sein (`status = 0` oder `status = 1`). Die nächste Generation eine Zelle ergibt sich aus dem Zustand der Nachbarn einer Zelle. Dabei gelten folgende Regeln:

- Eine tote Zelle mit genau drei lebenden Nachbarn wird in der nächsten Generation lebendig
- Eine lebende Zelle mit weniger als zwei lebenden Nachbarn stirbt in der nächsten Generation
- Eine lebende Zelle mit zwei oder drei lebenden Nachbarn ist auch in der nächsten Generation lebendig
- Eine lebende Zelle mit mehr als drei lebenden Nachbarn stirbt in der nächsten Generation

Die Zustände der nächsten Generationen werden gleichzeitig berechnet und ersetzen Zustände der aktuellen Generation.

Das Spiel soll in der Lage sein, am Anfang eine komplette Spielfeldbelegung mit lebendigen/toten Zellen zu übernehmen, die dann in der Evolution weiterentwickelt werden. Ein Beispiel, wie sich Generationen verhalten, findest du [hier](https://en.wikipedia.org/wiki/Conway%27s_Game_of_Life#Examples_of_patterns).
