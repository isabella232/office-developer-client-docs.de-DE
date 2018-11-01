---
title: ActiveX Data Objects (ADO)-Glossar
TOCTitle: ADO Glossary
ms:assetid: 40f00876-7525-4117-8f57-f3d87c54be99
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249184(v=office.15)
ms:contentKeyID: 48544438
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 809431c51b7fab9e56d492b44610d607e4da3b06
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869967"
---
# <a name="ado-glossary"></a>ADO-Glossar

**Betrifft**: Access 2013, Office 2013

## <a name="a"></a>A

**absolute URL**

Eine vollqualifizierte URL, der den Speicherort einer Ressource, die befindet sich im Internet oder Intranet angibt. Siehe auch **URL** und **relative URL**.

**ActiveX-Steuerelement**

Selbst registrieren in-Process-COM-Komponente, die häufig ein visuelles Element entweder zur Entwurfszeit oder zur Laufzeit verfügt. ActiveX-Steuerelemente haben auch die Möglichkeit zur Kommunikation mit einem aktiven Dokument-Container, wie beispielsweise Microsoft Internet Explorer.

**ADISAPI (Advanced Data Internet Server Application Programming Interface)**

Ein ISAPI DLL für die Analyse, Automation-Steuerelement, **Recordset** Marshalling und MIME-packen. Die ADISAPI-Komponente wird über die API von Internetinformationsdienste (Internet Information Services, IIS) bereitgestellt. Siehe auch **ISAPI**.

**Aggregatfunktion**

In einer Abfrage, die eine Funktion wie COUNT, AVG oder STDEV, die alle Zeilen in einer Spalte einer Tabelle mit einen Wert berechnet. Schreiben von Ausdrücken und beim Programmieren können Sie die SQL-Aggregatfunktionen (einschließlich der drei oben aufgeführten) und Domänen-Aggregatfunktionen verwenden, um verschiedene Statistiken zu bestimmen.

**alias**

Ein alternativer Name, den Sie einer Spalte oder einem Ausdruck in einer SQL-SELECT-Anweisung, häufig kürzer oder aussagekräftiger gewähren. Beispielsweise ist ///BobSales der Alias in der folgenden SELECT-Anweisung: "Select ///WR-Sales as ///BobSales from ///SalesDB". Ein Alias kann verwendet werden, dynamisch Spalten zum Steuern von Bindungen im **DataControl** -Objekt zugewiesen.

**Apartmentthreading**

Ein COM Threadingmodell, in denen alle Anrufe auf ein Objekt in einem Thread auftreten. Apartmentthreading COM synchronisiert und gemarshallt Anrufe. Siehe auch **COM**.

**asynchrone operation**

Ein Vorgang, der Steuerung an das aufrufende Programm zurückgibt, ohne warten, bis des Vorgangs abgeschlossen ist. Bevor der Vorgang abgeschlossen ist, wird die codeausführung fortgesetzt. Siehe auch **synchronen Vorgang**.

Nach oben

## <a name="b"></a>B

**Bindungseintrag**

Eine Zuordnung zwischen einem Feld in einer Tabelle und einer Variablen. **Recordset** -Felder werden in ADO Visual C++-Erweiterungen C/C++-Variablen zugeordnet.

**Bitmaske**

Ein numerischer Wert für die direkte Verwendung einen Wert von bitweiser Vergleich mit andere numerische Werte, in der Regel Optionen im Parameter oder Rückgabewerte zu kennzeichnen. In der Regel erfolgt dieser Vergleich mit bitweisen logischen Operatoren wie **und** und **oder** in Visual Basic, **&** und **|** in C++.

Beispielsweise können die ADO **FieldAttributeEnum** Werte als Bitmasken verwendet werden, um die Attribute eines Felds zu bestimmen. Angenommen Sie, Sie möchten ermitteln, ob ein Feld aktualisiert wurde. Sie können für diese mit den folgenden Ausdruck in Visual Basic testen:  
  

Wenn das Ergebnis auf true festgelegt ist, ist das Feld aktualisierbar.

**bookmark**

Eine Markierung, die eine Zeile innerhalb einer Gruppe von Zeilen, damit ein Benutzer schnell darauf navigieren eindeutig identifiziert.

**Geschäftsobjekt**

Ein Objekt, das eine definierte Reihe von Vorgängen, wie Daten Überprüfung oder Regel die Geschäftslogik ausgeführt wird. Geschäftsobjekte befinden sich in der Regel in der mittleren Ebene.

**Geschäftsregeln**

Die Kombination von Validierung bearbeitet, Anmeldung-Überprüfungen, Datenbankabfragen, Richtlinien und algorithmische Transformationen, die Art der Geschäftsführung eines Unternehmens bilden. Auch bekannt als *Geschäftslogik*.

Nach oben

## <a name="c"></a>C

**berechneter Ausdruck**

Ein Ausdruck, der nicht Konstante, aber, dessen Wert von anderen Werten abhängig. Um ausgewertet werden, muss ein berechnetes Ausdrucks zu erhalten und Berechnen von Werten aus anderen Quellen, in der Regel in anderen Feldern oder Zeilen.

**Kapitel**

Ein Verweis auf einen Bereich von Zeilen aus einer Datenquelle. In ADO ist ein Kapitel in der Regel einen Verweis auf ein anderes **Recordset-Objekt**.

Kapitelspalten ermöglichen es, eine *hierarchische* Beziehung zu definieren, in dem das *übergeordnete* ist, enthält die Kapitelspalte und das *untergeordnete* **Recordset-Objekt** das **Recordset-Objekt** durch das Kapitel dargestellt ist.

**chapter-alias**

Ein Alias, der dem übergeordneten Element angefügte Spalte verweist.

**Zeichensatz**

Eine Zuordnung von einer Reihe von Zeichen zu ihren numerischen Werten. Unicode ist beispielsweise ein 16-Bit-Zeichensatz alle bekannten Zeichen codiert werden können und als weltweiter Standard Character-Codierung verwendet.

**untergeordnetes Element**

Die abhängige Seite einer hierarchischen Beziehung. Ein untergeordnetes Element ist ein Knoten in einer hierarchischen Struktur, die einen anderen Knoten befindlichen Anwendung verfügt (näher am Stamm). Siehe auch **untergeordnete-Alias**, **hierarchische Beziehung**, **übergeordneten**.

**child-alias**

Ein Alias, der auf das untergeordnete Element verweist. Siehe auch **Alias**, **untergeordnete**.

**CLSID (Class Identifier)**

Ein eindeutiger Bezeichner (UUID), der eine COM-Komponente identifiziert. Jede COM-Komponente hat seine CLSID in der Windows-Registrierung, sodass sie von einer anderen Anwendung geladen werden kann. Siehe auch **ProgID**, **COM**.

**Clientebene**

Eine logische Ebene eines verteilten Systems, die in der Regel zeigt Daten an und verarbeitet Eingaben des Benutzers, der manchmal auch als *Front-End*-bezeichnet. In der Regel die Clientebene fordert Daten von einem Server basierend auf Benutzereingaben, dann so formatiert, und das Ergebnis angezeigt. Siehe auch **mittlere Ebene**, **Datenquelle Tier**, **verteilte Anwendung**.

**COM (Component Object Model)**

Einen binären Standard, mit der Objekte für die Zusammenarbeit in einer vernetzten Umgebung unabhängig von der Sprache, in der diese entwickelt wurden, oder auf welchen Computern sie sich befinden kann. COM-basierte Technologien gehören ActiveX-Steuerelemente, Automatisierung und Objekte verknüpfen und einbetten (OLE). COM ermöglicht es einem Objekt seine Funktionalität für andere Komponenten und hostanwendungen verfügbar machen. Es definiert sowohl wie das Objekt offen gelegt wird und wie dieses Offenlegen über Prozesse und Netzwerke hinweg funktioniert. COM definiert auch Lebenszyklus des Objekts.

**COM-Komponente**

Binärdatei – wie .dll, .ocx und einige .exe-Dateien –, die zum Bereitstellen von Objekten im COM-Standard unterstützt. Eine solche Datei enthält Code für eine oder mehrere Klasse Diensttypen, COM-Klassen, Mechanismen für Registrierungseinträge, Code zum Laden und usw..

**Vergleichsoperator**

Ein Operator, der vergleicht zwei Ausdrücke und gibt einen booleschen Wert zurück.

Einen Kriterienparameter, der als ausgedrückt werden möglicherweise "\>"(größer als),"\<"(kleiner als), "=" (gleich),"\>=" (größer als oder gleich), "\<=" (kleiner als oder gleich), "\<\>" (nicht gleich) oder "like" (Mustervergleich).

**component**

Ein Objekt, das Daten und Code kapselt und bietet eine gut spezifizierte Reihe von öffentlich verfügbaren Diensten.

**Verbunddatei**

Eine Implementierung von COM strukturiert Speicher für Dateien. Eine Verbunddatei speichert separate Objekte in einer einzelnen, strukturierten Datei bestehend aus zwei Hauptelemente: Speicherobjekte und Stream-Objekten. Zusammen können sie wie in einem Dateisystem in einer Datei. Weitere Informationen finden Sie unter zusammengesetzte Dateien im Microsoft Platform SDK.

Eine Anzahl von einzelnen Dateien in einer physischen Datei zusammen gebunden. Jede einzelne Datei in einer Verbunddatei kann zugegriffen werden, als wäre es einer einzelnen physischen Datei.

**Konstante**

Eine numerische oder String-Wert, der nicht geändert wird. Benannte ADO-Enumerationen (aufgezählte Konstanten) können in Ihrem Code anstelle der tatsächlichen Werte verwendet werden, beispielsweise **AdUseClient** ist eine Konstante, deren Wert 3 ist. (Const AdUseClient = 3). Siehe auch **Enumeration**.

**Cursor**

Eine Datenbank-Element, das Datensatznavigation aktualisierbar von Daten und der Sichtbarkeit von Änderungen an der Datenbank von anderen Benutzern steuert.

Nach oben

## <a name="d"></a>D

**Binden von Daten**

Der Prozess der Verknüpfen von Objekten oder Steuerelementen einer Anwendung mit einer Datenquelle. Ein Steuerelement mit einer Datenquelle verknüpft ist, wird ein *datengebundenes Steuerelement*aufgerufen.

Der Inhalt des Steuerelements datengebundenen sind Werten aus einer Datenbank zugeordnet. Beispielsweise kann ein Grid-Steuerelement, das an ein **Recordset** -Objekt gebunden ist aktualisiert werden, wenn die Zeilen im **Recordset** aktualisiert werden. Wenn neue Werte durch das **Recordset**abgerufen werden, werden die neuen Werte im Raster angezeigt.

**Datenanbieter**

Software, die Daten zu einer ADO-Anwendung verfügbar macht entweder direkt oder über einen Dienstanbieter. Siehe auch **-Dienstanbieter**.

**datenstrukturierung**

Eine Methode, welche eine formalisierte Syntax (als **Form Sprache**bezeichnet nutzt) so definieren Sie ein spezialisierte **Recordset** -Objekt ( **geformten Recordset-Objekts**als bezeichnet), die nicht nur die Daten enthält, aber auch verweist auf andere **Recordset** -Objekte, und und/oder berechnete Werte, die basierend auf diesen **Recordset** -Objekte.

**Quelle der Datenebene**

Eine logische Ebene eines verteilten Systems, die einen Computer mit einem DBMS, wie eine SQL Server-Datenbank darstellt. Siehe auch **Clientebene**, **mittlere Ebene**und **verteilte Anwendung**.

**DCOM**

Ein Protokoll, mit dem COM-Komponenten, die über ein Netzwerk direkt miteinander kommunizieren kann. Siehe auch **COM**, **Komponente**.

**DDL (Data Definition Language)**

Diese Anweisungen in SQL Server, die im Gegensatz zum Bearbeiten von Daten definieren. Das Schema einer Datenbank wird erstellt oder mit DDL geändert. Beispielsweise sind **CREATE TABLE**, **CREATE INDEX**, **erteilen**und **ENTZIEHEN** SQL DDL-Anweisungen.

**Standarddatenstrom**

Ein Text oder binären Stream (dargestellt durch ein **Stream** -Objekt), der bei Verwendung von bestimmten OLE DB-Anbietern wie etwa der Microsoft OLE DB-Anbieter für Internet Publishing **oder ein **Recordset** ** -Objekten zugeordnet ist. Der Standarddatenstrom enthält normalerweise den Inhalt einer Datei wie den HTML-Code für den Stamm einer Website.

**verteilte Anwendung**

Ein Programm geschrieben, damit die Verarbeitung auf mehreren Computern über ein Netzwerk unterteilt werden kann. In der Regel ist eine verteilte Anwendung in die Präsentation, Geschäftslogik und Data Store Ebenen oder *Ebenen*unterteilt. Siehe auch **Clientebene**, **mittlere Ebene**und **Datenquellen-Tier**.

**getrenntes Recordset**

Ein **Recordset** -Objekt in einem Clientcache, die über eine aktive Verbindung mit dem Server nicht mehr verfügt. Wenn die ursprüngliche Datenquelle muss erneut für aus irgendeinem Grund, wie das Aktualisieren von Daten zugegriffen werden muss die Verbindung erneut hergestellt werden. Die Auflistungen, Eigenschaften und Methoden des ein getrenntes **Recordset-Objekt** können jedoch weiterhin zugegriffen werden.

**DLL (Dynamic Link Library)**

Eine Datei, die eine oder mehrere Funktionen enthält, die kompiliert werden, verknüpft und getrennt von den Prozessen, die sie verwenden gespeichert werden. Das Betriebssystem ordnet die DLLs in den Adressraum des aufrufenden Prozesses beim Starten des Prozesses oder während der Ausführung.

**DML (Data Manipulation Language)**

Diese Anweisungen in SQL Server, die im Gegensatz um zu definieren, Daten zu bearbeiten. Die Werte in einer Datenbank sind ausgewählt und mit DML geändert. Beispielsweise sind **Einfügen**, **Aktualisieren**, **Löschen**und **Wählen Sie** SQL DML-Anweisungen.

**Dokumentquellenanbieter**

Eine spezielle Klasse von Anbietern, die Ordner und Dokumente zu verwalten. Wenn ein Dokument durch ein **Record** -Objekt dargestellt wird, oder ein Ordner mit Dokumenten durch ein **Recordset** -Objekt dargestellt wird, füllt der Dokumentquellenanbieter diese Objekte mit einem eindeutigen Satz von Feldern, die Merkmale des Dokuments beschreiben, Dokumentieren Sie anstelle der tatsächlichen selbst aus. Siehe auch **Ressourceneintrag**.

**DSN (Data Source Name)**

Die Auflistung von Informationen zum Verbinden Ihrer Anwendung mit einer bestimmten ODBC-Datenbank. Der ODBC-Treiber-Manager verwendet diese Informationen zum Erstellen einer Verbindung mit der Datenbank. Ein DSN kann in einer Datei (Datei-DSN) oder in der Windows-Registrierung (Computer-DSN) gespeichert werden.

**dynamische Eigenschaft**

Eine Eigenschaft, die speziell für einen Datenprovider oder der Microsoft Cursor Service. Die **Properties** -Auflistung eines Objekts wird automatisch gefüllt ("dynamisch"). Ein Objekt hat keine dynamischen Eigenschaften, bis er mit einer Datenquelle über einen bestimmten Datenprovider verbunden ist. Siehe auch **Datenanbieter**, **Cursor**.

Nach oben

## <a name="e-i"></a>E-ICH

**(Aufzählung)**

Eine Liste der benannten-Konstanten sein. Enumerationswerte müssen nicht eindeutig sein. Jedoch muss der Name der einzelnen Wert innerhalb des Bereichs eindeutig sein, auf dem die Enumeration definiert ist. In ADO Enumerationen dienen für numerische Parameter und Rückgabewerte, ADO Code Bedeutung hinzugefügt und den Entwickler von numerischen Werten zu bewahren (die von Version zu Version ändern können). Verwenden Sie beispielsweise zum Öffnen einer statischen **Datensatzgruppe**den Wert **AdOpenStatic** aufgelistet:  
  

Auch bezeichnet als *Aufzählungskonstante*. Siehe auch **Konstante**.

**Ereignis**

Eine Aktion, die von einem Objekt, für die Sie Code zum reagieren schreiben können erkannte. Ereignisse können durch Ausführung des Befehls, Transaktion abgeschlossen, Recordsetnavigation und Aktualisierung von Daten zwischen anderen Aktionen generiert werden. Siehe auch **Ereignishandler**.

**Ereignishandler**

Ein Ereignishandler ist der Code, der ausgeführt wird, wenn ein Ereignis auftritt. Siehe auch **-Ereignis**.

**handler**

Eine Routine, die eine allgemeine und relativ einfach Bedingung oder Vorgang, beispielsweise Fehler Recovery oder Daten Management verwaltet.

**hierarchische Recordset-Objekt**

Ein **Recordset-Objekt** , das ein anderes **Recordset**enthält. Siehe auch **Data shaping**, **Kapitel**.

Weitere Informationen finden Sie unter [Zugreifen auf Zeilen in einem hierarchischen Recordset](accessing-rows-in-a-hierarchical-recordset.md)

**Hierarchie**

Im Allgemeinen eine Hierarchie ist eine Rangfolge Struktur mit einer Top Ebene und untergeordneten Ebenen. In ADO werden hierarchische **Recordsets** zur Darstellung der über-und untergeordnete elementbeziehungen zwischen einem Datensatz und einem Kapitel verwendet. Außerdem können in ADO Objekte **Record** und **Stream** verwendet werden auf der hierarchischen Struktur wie beispielsweise einen Ordner und Dokumente zugreifen. ADO MD umfasst auch **Hierarchy** -Objekte, um eine Beziehung zwischen den Ebenen einer Dimension in einem OLAP-Cube darstellen. Siehe auch **hierarchische Recordsets**, **hierarchische Beziehung**, **Kapitel**, **Struktur**.

**ISAPI (Internet Server Application Programming Interface)**

Eine Reihe von Funktionen für Internetserver, wie ein Windows NT Server/Windows 2000 Server mit Microsoft-Internetinformationsdienste (Internet Information Services, IIS).

Nach oben

## <a name="k-m"></a>K-M

**Schlüssel**

Eine Spalte oder Spalten in einer Tabelle, die eine Zeile eindeutig identifizieren; häufig verwendet, um eine Tabelle zu indizieren.

**Marshalling**

Der Prozess der Verpackung, senden und Entpackens-Methodenparameter für die Benutzeroberfläche über Prozess oder Thread hinweg.

**mittlere Ebene**

Die logische Ebene in einem verteilten System zwischen einer Schnittstelle oder Web-Client des Benutzers und der Datenbank. Dies ist üblicherweise, in dem Geschäftsobjekte instanziiert werden. Die mittlere Ebene ist eine Auflistung von Geschäftsregeln und Funktionen, die beim Abrufen von Daten ausgeführt werden. Das erreichen sie mithilfe von Geschäftsregeln, die häufig ändern können, und sind somit in Komponenten, die von der Anwendungslogik selbst physisch getrennt sind eingeschlossen. Auch bekannt als *Anwendungsserverebene*. Siehe auch **verteilte Anwendung**, **Clientebene**, **Datenquelle Tier**.

**MIME (Multi-Purpose Internet Mail Extension)**

Ein Internetprotokoll entwickelt ursprünglich zum Austausch von e-Mail-Nachrichten mit umfangreichen Inhalt über heterogene Netzwerk, Computer und e-Mail-Umgebungen zu ermöglichen. In der Praxis wurde MIME auch eine Form und durch nicht e-Mail Programmen, die erweitert.

MIME ist ein Standard, der binäre Daten veröffentlicht und im Internet gelesen werden kann. Die Kopfzeile einer Datei mit Binärdaten enthält den MIME-Typ der Daten. Dieser informiert Clientprogramme (web-beispielsweise Browser und e-Mail-Pakete), mit die Daten auf andere Weise behandelt, als einfachen Text benötigt wird. Beispielsweise enthält die Kopfzeile der einem Webdokument, die eine JPEG-Grafik enthält den MIME-Typ, der speziell für das JPEG-Dateiformat. Dadurch wird einen Browser zum Anzeigen der Datei mit seinem JPEG-Viewer, sofern vorhanden.

Nach oben

## <a name="n-o"></a>N-O

**Knoten**

Ein Element in einer hierarchischen Struktur. Ein Knoten kann der Stamm oder das untergeordnete Element eines anderen Knotens sein. Ein Knoten kann auch das übergeordnete Objekt des mehrere untergeordnete Elemente sein. Siehe auch **Hierarchie**, **Struktur**, **Stamm**, **untergeordnete**und **übergeordnete**.

**Objektvariable**

Eine Variable, die einen Verweis auf ein Objekt enthält. ObjCustomObject wird beispielsweise eine Variable, die auf ein Objekt vom Typ Benutzerobjekt verweist:  
  
ist eine Variable, die auf ein Objekt vom Typ Benutzerobjekt verweist:  
  
Legen Sie ObjCustomObject = CreateObject (Adodb. Recordset-Objekt)

**ODBC (Open Database Connectivity)**

Ein standard Language-Programmierschnittstelle zum Verbinden mit einer Vielzahl von Datenquellen. Dies erfolgt normalerweise über die Systemsteuerung, in dem Datenquellennamen (DSNs) zugewiesen werden können, um bestimmte ODBC-Treiber verwenden.

**OLE DB**

Eine Reihe von Schnittstellen, die Daten aus einer Vielzahl von Quellen mithilfe von COM offen OLE DB-Schnittstellen bieten Clientanwendungen mit einheitlichen Zugriff auf Daten in unterschiedlichen Quellen gespeichert. Diese Schnittstellen unterstützen die an die Datenquelle, aktivieren sie Datenfreigabe geeignete DBMS-Funktionalität. Siehe auch **COM**.

**Parallelität**

Ein Typ der Sperre, in dem die Datenseite mit einem oder mehreren Datensätzen, einschließlich des Datensatzes, der gerade bearbeitet wird, ist für andere Benutzer als nicht verfügbar nur während der Aktualisierung des Datensatzes durch die **Update** -Methode ist aber steht vor und nach dem Aufruf von **Update** .

Parallelität wird verwendet, wenn das **Recordset** -Objekt, bei dem Parameter der **LockType** -Eigenschaft auf **AdLockOptimistic** oder **AdLockBatchOptimistic**festgelegt geöffnet wird. Siehe auch **vollständige Sperren**.

**Ordinalwert**

Die numerische Position eines Elements in einem Auftrag. In einer ADO-Auflistung ist der Wert des ersten Elements Null (0). Das nächste Element ist ein (1) und So weiter.

Nach oben

## <a name="p"></a>P

**parametrisierten Befehl**

Eine Abfrage oder einen Befehl, mit dem Sie Parameterwerte festzulegen, bevor der Befehl ausgeführt wird. Durch das Einbetten von Markierungen Parameter in der SQL-Zeichenfolge kann beispielsweise eine SQL-Zeichenfolge parametrisiert werden (genehmigtes der '?' Zeichen). Die Anwendung dann gibt Werte für jeden Parameter und führt den Befehl.

**das übergeordnete**

Die steuernde Seite einer hierarchischen Beziehung. In einer hierarchischen Struktur hat ein übergeordnetes Element eine oder mehrere untergeordnete Knoten direkt darunter in der Hierarchie. Siehe auch **übergeordnete-Alias**, **hierarchische Beziehung**, **untergeordnete**.

**parent-alias**

Ein Alias, der dem übergeordneten Element verwiesen wird. Siehe auch **Alias**, **das übergeordnete**.

**über-und untergeordnete elementbeziehungen**

Eine Beziehung in einer hierarchischen Struktur in der das übergeordnete Element eine Ebene höher und direkt einen oder mehrere untergeordnete Elemente zugeordnet ist. Ein untergeordnetes Element ist eine Ebene niedriger und muss ein übergeordnetes Element aufweisen. Siehe auch **übergeordnete**und **untergeordnete**.

**beibehalten**

Zum Speichern von Daten in einem permanenten Zustand, wie ein **Recordset-Objekt** in einer Datei gespeichert.

**Vollständiges Sperren**

Ein Typ von Sperren in der die Seite mit einem oder mehreren Datensätzen, einschließlich des Datensatzes, der gerade bearbeitet wird, ist nicht verfügbar für andere Benutzer, um sicherzustellen, dass eine Aktualisierung vorgenommen wird. Eingeschränkte Sperren Verhalten wird durch den OLE DB-Anbieter definiert. In der Regel Datensätze nach dem Bearbeiten gesperrt sind und nicht verfügbar bleiben, bis die **Update** -Methode ausgeführt wurde.

Vollständiges Sperren ist aktiviert, wenn das **Recordset** -Objekt, bei dem Parameter der **LockType** -Eigenschaft auf **AdLockPessimistic**festgelegt geöffnet wird. Siehe auch **optimistischen Sperren**.

**Pooling**

Eine Optimierung basierend auf Sammlungen von reservierte Ressourcen, wie Objekte oder Datenbankverbindungen verwenden. Es ist eine effizientere eine vorhandene Ressource aus dem Pool als zum Erstellen einer neuen Ressource gezeichnet wird.

**ProgID (Programmatische ID)**

Ein eindeutiger Name, der Windows-Registrierung, die von einem COM-Anwendung zugeordnet sind. Die ProgID für eine ADO-Verbindung lautet "ADODB. Verbindung". Siehe auch **CLSID**, **COM**.

**Proxy**

Eine Schnittstelle-Objekt, das die Parametermarshaling bereitstellt und Kommunikation erforderlich, damit ein Client ein Application-Objekt aufgerufen wird, die in einer Umgebung mit verschiedenen Ausführung wie auf einem anderen Thread oder in einem anderen Prozess ausgeführt wird. Der Proxy befindet sich mit dem Client und kommuniziert mit einem entsprechenden Stub, der mit dem Application-Objekt gespeichert ist, die aufgerufen wird. Siehe auch **Stub**.

Nach oben

## <a name="r"></a>R

**relative URL**

Eine teilweise qualifizierte URL, die gibt eine Ressource im Internet oder Intranet, dessen Position relativ zum Ausgangspunkt durch eine absolute URL oder die entsprechende ADO-Connection-Objekt angegeben ist. Aktiviert die verketteten absoluten und relativen URLs bilden eine vollständige URL. Siehe auch **URL** und **absolute URL**.

**Remote-Datenquelle**

Eine Datenquelle, die auf einem anderen Computer, statt die Daten auf dem lokalen System vorhanden (, wo die Client-Anwendung ausgeführt wird).

**-Ressourceneintrag**

Ein Datensatz aus einem Dokumentquellenanbieter, der Felder für die Definition und die Beschreibung eines Ordners oder eines Dokuments enthält. Das Dokument selbst nicht in der Ressourceneintrag enthalten ist, aber in der Regel durch den Standarddatenstrom oder ein Feld in der mit einer URL-Ressourceneintrag zugegriffen werden kann. Siehe auch **Dokumentquellenanbieter** **Standarddatenstrom**, **URL**.

**root**

Auf der obersten Ebene in einer hierarchischen Struktur. Der Stammknoten weist keine übergeordneten Elemente, aber möglicherweise untergeordnete Elemente. Siehe auch **Hierarchie**, **Struktur**, **übergeordneten**und **untergeordneten**.

**Rowset**

Eine Reihe von Zeilen aus einer Datenquelle, mit dem Schema dar. Ein Rowset kann alle oder einige Felder aus einer Tabelle darstellen. Ein Rowset kann auch eine virtuelle Tabelle, die von einer Abfrage oder einer Verknüpfung von zwei oder mehr Tabellen erstellt darstellen. In ADO werden Rowsets durch **Recordset** -Objekte dargestellt.

Nach oben

## <a name="s"></a>S

**Schema**

Eine Beschreibung einer Datenbank für die Datenbank-Managementsystem (DBMS), mit der vom DBMS bereitgestellten Datendefinitionssprache in der Regel generiert. Ein Schema definiert Attribute der Datenbank, wie Tabellen, Spalten und Eigenschaften.

**scope**

Der Bereich der Referenz für ein Objekt oder eine Variable oder einen Bereich von Datensätzen in einer Ansicht oder einer Tabelle. Beispielsweise können lokale Variablen nur innerhalb der Prozedur verwiesen werden in denen sie definiert wurden. Public-Variablen werden aus an einer beliebigen Stelle in der Anwendung zugegriffen. Objekte, wie der aktuellen Datenbank befinden sich im Bereich werden im definierten Suchpfad. Erfassen von Bereichen können mit einer Bereichsklausel in vielen Befehlen angegeben werden.

**Dienstanbieter**

Software, die einen Dienst kapselt, Herstellung und Verarbeiten von Daten, und Erweitern von Funktionen in der ADO-Anwendung. Ein Anbieter, der direkt keine Daten offen gelegt werden, es stellt einen Dienst wie der abfrageverarbeitung. Der Dienstanbieter kann Daten von einem Datenprovider verarbeiten bereitgestellt. Siehe auch **Datenanbieter**.

**geformten Recordset-Objekts**

Ein **Recordset-Objekt** , dessen Spalten insbesondere definiert wurden, nicht nur Daten, sondern auch Verweise (als Kapitel bezeichnet) in andere **Recordset** -Objekte und/oder berechnete Werte basierend auf andere **Recordset** -Objekte enthalten.

**gleichgeordneten Knoten**

Alle zwei oder mehr Knoten in einer hierarchischen Struktur, die sich auf derselben Ebene in der Hierarchie. Der Stammknoten in einer Hierarchie hat keine gleichgeordnete Elemente.

**gespeicherte Prozedur**

Eine vorkompilierte Auflistung von Code wie SQL-Anweisungen und optional der Fluss Steuerelements Anweisungen unter einem Namen gespeichert und als Einheit verarbeitet. Gespeicherte Prozeduren werden in einer Datenbank gespeichert. Sie können mit einem einzigen Aufruf aus einer Anwendung ausgeführt werden und ermöglichen benutzerdefinierte Variablen, bedingte Ausführung und andere leistungsstarke Features für die Programmierung.

**Stub**

Eine Schnittstelle-Objekt, das die Parametermarshaling bereitstellt und die Kommunikation für ein Application-Objekt von einem Client Anrufe, die in einer Umgebung mit verschiedenen Ausführung wie auf einem anderen Thread oder in einem anderen Prozess ausgeführt wird. Stub befindet sich mit dem Anwendungsobjekt und kommuniziert mit einem entsprechenden Proxy, die sich mit dem Client, die es aufruft. Siehe auch **Proxy**.

**Unterknoten**

Finden Sie unter **untergeordneten**.

**synchrone operation**

Ein Vorgang von Code, der abgeschlossen ist, bevor die nächste Operation beginnen kann initiiert wurde. Siehe auch **asynchrone Operation**.

Nach oben

## <a name="t-w"></a>T-W

**Struktur**

Eine Struktur, die eine hierarchische Beziehung zwischen Elementen (Knoten) darstellt. Ein Knoten ist auf der obersten Ebene einer Struktur (Stamm) vorhanden. Unter dem Stamm können mehrere untergeordnete Elemente vorhanden sein. Jede untergeordnete möglicherweise wiederum das übergeordnete Objekt des anderen untergeordneten, Verzweigen wie einer Struktur. Ein Ordner, Dokumente und andere Ordner enthält ist ein Beispiel einer Struktur. Siehe auch **Hierarchie**, **Knoten**, **Stamm**, **untergeordnete**und **übergeordnete**.

**URL (Uniform Resource Locator)**

Gibt den Speicherort einer Ressource im Internet oder Intranet. Eine vollständige URL besteht aus einem Schema (z. B. FTP, HTTP, Mailto, Datei usw.), gefolgt von einem Doppelpunkt, einen Servernamen und den vollständigen Pfad einer Ressource (beispielsweise ein Dokument, eine Grafik oder andere Datei). Einige Beispiele für URLs sind:  
  
https://www.domain.com/default.html  
FTP://FTP.Server.somewhere/ftp.File  
  
FTP://FTP.Server.somewhere/ftp.File  
file://Server/Share/File.doc

Siehe auch **absolute URL** und **relative URL**.

**Webserver**

Ein Computer, der Webdienste und Seiten für Intranet- und Internetbenutzer bereitstellt.

Nach oben

