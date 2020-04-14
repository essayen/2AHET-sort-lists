# 2AHET-sort-lists

In diesem Beispiel werden verschiedene Konzepte des vorangegangenen Stoffes, vor allem Structs und Listen, angewendet.

## Gesamtkonzept

Es soll ein Programm entworfen werden, um die Planung von Sportereignissen wie z.B. Volleyballturnieren zu unterstützen. Das Programm soll die Aufteilung der Mannschaften auf die Spiele der Gruppenphase durchführen, so dass ein Spielplan nach bestimmten Kriterien erstellt wird.

### Anforderungen

Verwende Exceptions (siehe Class Notebook) in diesem Beispiel um Fehleingaben des Benutzers abzufangen. 

An vielen Stellen wird die Möglichkeit bestehen, dass der Benutzer ungültige Werte eingibt (unmögliche Indizes, Werte, die keinen Sinn machen). Verwende den Mechanismus  *try-catch* um solche Falscheingaben abzufangen und passende Fehlermeldungen auszugeben.

## Datenstrukturen

### Sportteam (Basic)

Erstelle ein *struct* für die Sportteams, welches folgende Attribute enthält:

* den Namen (einen String)
* das Spielerlevel (eine nicht vorzeichenbehaftete Ganzzahl)
* der Heimatort (als String)

### Paarung (Basic)

Erstelle ein *struct* für eine Paarung zweier Mannschaften, welches folgende Attribute enthält:

* Team A (ein Sportteam)
* Team B (ein Sportteam)
* Punkte A (eine nicht vorzeichenbehaftete Ganzzahl)
* Punkte B (eine nicht vorzeichenbehaftete Ganzzahl)
* abgeschlossen (eine bool'sche Variable, welche *true* ist, wenn das Spiel abgeschlossen wurde und bis dahin *false* gesetzt wird)

### Teamliste (Basic)

Erstelle eine *List* für Teams.

### Paarungen (Advanced)

Erstelle jeweils eine Liste für die Paarungen der 1., 2. und jeder weiteren Runde des Turniers bis zum Halbinale. Die Anzahl der Listen hängt hierbei von der Anzahl (n) der Mannschaften in der Teamliste ab. In der 1. Runde finden sich n/2 Paarungen, in der 2. Runde n/4 usw. Im Halbfinale finden sich genau 2 Paarungen.

## Funktionen

### Eingabe der Mannschaften (Basic)

Schreibe eine Funktion, um eine neue Mannschaft in die Liste der Mannschaften einzugeben. Die Funktion erhält genau eine Parameter (die Liste) und hat keinen Rückgabewert.

Die Funktion fragt den Benutzer nach den Attributen für einen neue Mannschaft und fügt diese in die Liste der Mannschaften ein.

### Erstellen einer Paarung (Advanced)

Schreibe eine Funktion, um eine neue Paarung zu erstellen. Die Funktion erhält genau einen Parameter (die Liste der Mannschaften) und liefert eine neue Paarung als Rückgabewert.

Die Funktion gibt zuerst die Liste der möglichen Mannschaften aus und fragt den Benutzer in Anschluss um zwei Indizes aus dieser Liste. Es wird eine neue Paarung mit den beiden Mannschaften an diesen Indizes erstellt. Die beiden Mannschaften werden im Anschluss aus der Mannschaftsliste gelöscht und die Paarung zurückgegeben.

### Automatisches Erstellen von Paarungen (Expert)

Diese Funktion erstetzt das manuelle Erstellen einer Paarung.

Schreibe eine Funktion, um eine neue Paarung zu erstellen. Die Funktion erhält genau einen Parameter (die Liste der Mannschaften) und liefert eine neue Paarung als Rückgabewert.

Die Funktion wählt aus der Liste der möglichen Mannschaften zwei aus, welche folgende Kriterien erfüllen:

* möglichst ähnliches Spielerlevel
* möglichst nicht aus dem selben Heimatort

### Erstellen der Paarungen für die 1. Runde (Advanced)

Schreibe eine Funktion, welche die Paarungen für die erste Runde eines Turniers erstellt. Die Funktion erhält zwei Parameter (die Liste der Mannschaften und die (leere) Liste der 1. Runde) und hat keinen Rückgabewert. 

Die Funktion erstellt mit Hilfe der oben beschriebenen Funktion Paarungen und fügt diese zur Spielliste für die erste Runde zusammen.

### Erstellen der Paarungen für die 2. und darauf folgende Runden (Expert)

Schreibe eine Funktion, welche die Paarungen für eine weitere Runde des Turniers erstellt. Die Funktion erhält zwei Parameter (die Liste aktuellen Runde und die (leere) Liste der nächsten Runde) und hat keinen Rückgabewert. 

Die Funktion erstellt aufgrund der Ergebnisse (nur wenn die Paarung abgeschlossen wurde; die Mannschaft mit den höheren Punkten gewinnt) neue Paarungen für die nächste Runde und fügt diese zur Spielliste für die nächste Runde hinzu.
