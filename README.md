# LaTeX-Unterlagen
In diesem Repository befinden sich die LaTeX-Unterlagen zum Modul.

## Aufgabe 1
In dieser Aufgabe beschäftigen wir uns mit Objektorientierung in Python. Der Fokus liegt auf der Implementierung einer Klasse, dabei nutzen wir insbesondere auch Magic Methods.

Ein Datensatz besteht aus mehreren Daten, ein einzelnes Datum wird durch ein
Objekt der Klasse **DataSetItem** repräsentiert. Jedes Datum hat einen Namen (Zeichenkette), eine ID (Zahl) und bel. Inhalt.

Nun sollen mehrere Daten, Objekte vom Typ **DataSetItem*, in einem Datensatz zusammengefasst werden. Sie haben sich schon auf eine Schnittstelle und die
beötigen Operationen, die ein Datensatz unterstützen muss, geeinigt. Es gibt eine Klasse **DataSetInterface**, die die Schnittstelle definiert und Operationen jedes
Datensatzes angibt. Bisher fehlt aber noch die Implementierung eines Datensatzes mit allen Operationen.

Implementieren Sie eine Klasse **DataSet** als eine Unterklasse von **DataSetInterface**.

Es gibt drei Dateien **dataset.py**, **main.py** und **implementation.py1**. In der **dataset.py** befinden sich die Klassen **DataSetInterface** und **DataSetItem**, in
der Datei **implementation.py** muss die Klasse **DataSet** implementiert werden. Die Datei **main.py** nutzt die Klassen **DataSet** und **DataSetItem** aus den jeweiligen
Dateien und testet die Schnittstelle und Operationen von **DataSetInterface**.

>Bei der Klasse **DataSet** sind insbesondere folgenden Methoden zu implementieren, die
genaue Spezifikation finden Sie in der **dataset.py**:
>1. \_\_setitem\_\_(self, name, id content) Hinzufügen eines Datums, mit Name, ID und Inhalt
>2. \_\_iadd\_\_(self, item) Hinzufügen eines DataSetItem
>3. \_\_delitem\_\_(self, name) Löschen eines Datums auf Basis des Namens. Das heißt auch, dass der Name eines Datums ein eindeutiger Schlüssel ist und jeder Name nur einmal pro Datensatz vorkommen kann.
>4. \_\_contains\_\_(self, name) Prüfung, ob ein Datum mit diesem Namen im Datensatz vorhanden ist.
>5. \_\_getitem\_\_(self, name) Abrufen des Datums über seinen Namen.
>6. \_\_and\_\_(self, dataset) Schnittmenge zweier Datensätze bestimmen und als einen neuen Datensatz zurückgeben.
>7. \_\_or\_\_(self, dataset) Vereinigungen zweier Datensätze bestimmen und als einen neuen Datensatz zurückgeben.
>8. \_\_iter\_\_(self) Iteration über alle Daten den Datensatzes (es ist möglich eine
Sortierung für die Reihenfolge der Iteration anzugeben).
>9. \_\_filtered\_iterate\_\_ (self, filter) Gefilterte Iteration über einen Datensatz, dabei dient eine Lambda-Funktion mit den Parametern Name und ID für
jedes Datum als Filter.
>10. \_\_len\_\_(self) Anzahl der Daten in einem Datensatz abrufen.

## Hinweise
Beachten Sie insbesondere die vorgestellten Funktionalitäten von Python im ersten Teil (erste drei Vorlesungen) des Moduls. Gucken Sie sich den im
Moodle zur Verfügung gestellten Code an, dort sind die gesamten Klassen **DataSetInterface** und **DataSetItem** mit ausführlichen Kommentaren hochgeladen.

Gucken Sie sich auch die **main.py** an, welche eine Auswahl an Testfälle beinhaltet. Sofern Sie die **main.py** zusammen mit der **dataset.py** und ihrer Implementierung der Klasse **DataSet** in der **implementation.py** ausf¨ uhren, werden die Testfälle durchgeführt. Alle Testfälle sind erfüllt, wenn **CodeIsValid** ausgegeben wird. Im Fehlerfall wird **CodeIsNotValid** ausgegeben und ein Hinweis zur Zeile mit dem Fehler wird angezeigt.

Sie dürfen alle im VPL verfügbaren Python-Funktionen nutzen, mit Ausnahme von Netzwerkkommunikation sowie Ausführungen anderer Programme (os.system()). Weiterhin sind einige wenige Funktionen und Module deaktiviert, um Manipulationen
an der **main.py** und **dataset.py** im Moodle zu verhindern. Sie bekommen eine Fehlermeldung angezeigt, sollten Sie eine der deaktivierten Funktionen nutzen.

Sie müssen die Oberklasse **DataSetInterface** nutzen.

## Abgabe
Programmieren Sie die Klasse **DataSet** in der Datei **implementation.py** zur Lösung der oben beschrieben Aufgabe im VPL. Sie können auch direkt auf Ihrem Computer
programmieren, dazu finden Sie alle drei benötigten Dateien zum Download im Moodle.

Das VPL nutzt den gleichen Code, wobei die **main.py** um weitere Testfälle und Überprüfungen erweitert wurde. Die
ÜberprÜfungen dienen dazu sicherzustellen, dass Sie die richtigen Klassen nutzen.

