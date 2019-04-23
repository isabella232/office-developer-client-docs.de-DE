---
title: ActiveX Data Objects (ADO)-Glossar
TOCTitle: ADO Glossary
ms:assetid: 40f00876-7525-4117-8f57-f3d87c54be99
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249184(v=office.15)
ms:contentKeyID: 48544438
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7ecb6208a8c970f037cb0ac699c947544eb8f547
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284834"
---
# <a name="ado-glossary"></a>ADO-Glossar

**Gilt für**: Access 2013, Office 2013

## <a name="a"></a>A

**Absolute URL**

Eine vollqualifizierte URL, die den Speicherort einer Ressource angibt, die sich im Internet oder in einem Intranet befindet. Siehe auch **URL** und **relative URL**.

**ActiveX-Steuerelement**

Self-Registration, in-Process-COM-Komponente, die oft ein visuelles Element entweder zur Entwurfszeit oder zur Laufzeit hat. ActiveX-Steuerelemente können auch mit einem aktiven Dokument Container wie Microsoft Internet Explorer kommunizieren.

**OnISAPI (Advanced Data Internet Server Application Programming Interface)**

Eine ISAPI-DLL, die Analyse-, Automatisierungs-und **Recordset** -Marshalling sowie MIME-Verpackungen bereitstellt. Die webDienste-Komponente funktioniert über die von Internet Information Services (IIS) bereitgestellte API. Siehe auch **ISAPI**.

**Aggregatfunktion**

In einer Abfrage eine Funktion wie COUNT, AVG oder STDEV, die einen Wert mit allen Zeilen in einer Spalte einer Tabelle berechnet. Beim Schreiben von Ausdrücken und in der Programmierung können Sie SQL-Aggregatfunktionen (einschließlich der drei oben aufgeführten) und Domänen-Aggregatfunktionen verwenden, um verschiedene Statistiken zu bestimmen.

**alias**

Ein alternativer Name, den Sie einer Spalte oder einem Ausdruck in einer SQL SELECT-Anweisung geben, oft kürzer oder aussagekräftiger. Beispielsweise ist BobSales der Alias in der folgenden SELECT-Anweisung: "wählen Sie WR-Sales als BobSales aus SalesDB" aus. Ein Alias kann zum dynamischen Zuweisen von Spalten zum Steuern von Bindungen für das **DataControl** -Objekt verwendet werden.

**Apartmentthreading**

Ein COM-Threadingmodell, bei dem alle Aufrufe eines Objekts in einem Thread stattfinden. Bei Apartment-Threading werden Anrufe von COM synchronisiert und gemarshallt. Siehe auch **com**.

**asynchroner Vorgang**

Ein Vorgang, der die Steuerung an das aufrufende Programm zurückgibt, ohne darauf zu warten, dass der Vorgang abgeschlossen ist. Bevor der Vorgang abgeschlossen ist, wird die Codeausführung fortgesetzt. Siehe auch **synchroner Vorgang**.

Zurück zum Seitenanfang

## <a name="b"></a>B

**Bindungseintrag**

Eine Zuordnung zwischen einem Feld in einer Tabelle und einer Variablen. In den ADO-Visual C++-Erweiterungen werden **Recordset** -Felder C/C++-Variablen zugeordnet.

**Bitmaske**

Ein numerischer Wert, der für einen Bit-für-Bit-Wertvergleich mit anderen numerischen Werten vorgesehen ist und in der Regeloptionen in Parameter-oder Rückgabewerten kennzeichnet. Dieser Vergleich erfolgt NormalerWeise mit bitweisen logischen Operatoren wie **und** und **oder** in Visual Basic **&** und **|** in C++.

Beispielsweise können die ADO- **FieldAttributeEnum** -Werte als Bitmasken verwendet werden, um die Attribute eines Felds zu bestimmen. Angenommen, Sie möchten feststellen, ob ein Feld aktualisiert werden konnte. Sie können dies mit dem folgenden Ausdruck in Visual Basic testen:  
  

Wenn das Ergebnis TRUE ist, ist das Feld aktualisierbar.

**bookmark**

Ein Marker, der eine Zeile innerhalb einer Reihe von Zeilen eindeutig identifiziert, sodass ein Benutzer schnell zu diesem navigieren kann.

**Geschäftsobjekt**

Ein Objekt, das eine definierte Gruppe von Vorgängen wie Datenüberprüfung oder Geschäftsregellogik ausführt. Geschäftsobjekte befinden sich normalerweise auf der mittleren Ebene.

**Geschäftsregel**

Die Kombination aus Validierungs Bearbeitungen, Anmelde Überprüfungen, Daten Bank Lookups, Richtlinien und algorithmischen Transformationen, die die Geschäftsweise eines Unternehmens darstellen. Auch als *Geschäftslogik*bezeichnet.

Zurück zum Seitenanfang

## <a name="c"></a>C

**Berechneter Ausdruck**

Ein Ausdruck, der nicht konstant ist, dessen Wert jedoch von anderen Werten abhängt. Um ausgewertet werden zu können, muss ein berechneter Ausdruck Werte aus anderen Quellen abrufen und berechnen, normalerweise in anderen Feldern oder Zeilen.

**Kapitel**

Ein Verweis auf einen Zeilenbereich aus einer Datenquelle. In ADO ist ein Kapitel in der Regel ein Verweis auf ein anderes **Recordset**-Objekt.

Kapitelspalten ermöglichen des Definieren einer *Übergeordnet-Untergeordnet*-Beziehung, in der das *übergeordnete* Element das **Recordset**-Objekt ist, das die Kapitelspalte enthält, und das *untergeordnete* Element das durch das Kapitel dargestellte **Recordset**-Objekt ist.

**chapter-alias**

Ein Alias, der auf die dem übergeordneten Element hinzugefügte Spalte verweist.

**Zeichensatz**

Eine Zuordnung einer Gruppe von Zeichen zu ihren numerischen Werten. Unicode ist beispielsweise ein 16-Bit-Zeichensatz, der alle bekannten Zeichen codieren und als weltweite Zeichen Codierungs Norm verwendet werden kann.

**untergeordneten**

Die abhängige Seite einer hierarchischen Beziehung. Ein untergeordnetes Element ist ein Knoten in einer hierarchischen Struktur mit einem anderen Knoten (näher am Stamm). Siehe auch **Child-Alias**, **Parent-Child Beziehung**, **Parent**.

**child-alias**

Ein Alias, der auf das untergeordnete Element verweist. Siehe auch **Alias**, **Child**.

**CLSID (Klassenbezeichner)**

Ein universell eindeutiger Bezeichner (UUID), der eine COM-Komponente identifiziert. Jede COM-Komponente hat Ihre CLSID in der Windows-Registrierung, sodass Sie von anderen Anwendungen geladen werden kann. Siehe auch **ProgID** **com**.

**Clientebene**

Eine logische Schicht eines verteilten Systems, die Daten in der Regel an und verarbeitet Eingaben des Benutzers, manchmal auch als *Front-End*bezeichnet. Die Clientebene fordert in der Regel Daten von einem Server basierend auf der Eingabe an und formatiert und zeigt dann das Ergebnis an. Siehe auch **mittlere Ebene**, **Datenquellenebene**, **verteilte Anwendung**.

**COM (Component-Objektmodell)**

Ein binärer Standard, der es ermöglicht, Objekte in einer Netzwerkumgebung zu verwenden, unabhängig von der Sprache, in der Sie entwickelt wurden, oder auf welchen Computern Sie sich befinden. Zu den COM-basierten Technologien gehört ActiveX-Steuerelemente, Automatisierung und Object Linking and Embedding (OLE). COM ermöglicht es einem Objekt, seine Funktionalität für andere Komponenten verfügbar zu machen und Anwendungen zu hosten. Es definiert, wie das Objekt sich selbst verfügbar macht und wie diese Belichtung über Prozesse und Netzwerke hinweg funktioniert. COM definiert auch den Lebenszyklus des Objekts.

**COM-Komponente**

Binäre Datei, wie dll, ocx und einige exe-Dateien, die den COM-Standard für die Bereitstellung von Objekten unterstützt. Eine solche Datei enthält Code für eine oder mehrere Klassenfactorys, COM-Klassen, Registrierungs Eingabe Mechanismen, ladenden Code usw.

**Vergleichsoperator**

Ein Operator, der zwei Ausdrücke vergleicht und einen booleschen Wert zurückgibt.

Ein Criteria-\>Parameter, der als "" (größer als), "\<" (kleiner als), "=" (gleich), "\>=" (größer als oder gleich), "\<=" (kleiner als oder gleich)\<\>, "" (ungleich) oder "like" (Mustervergleich) ausgedrückt werden kann.

**component**

Ein Objekt, das sowohl Daten als auch Code kapselt und eine Reihe von öffentlich verfügbaren Diensten bereitstellt.

**Verbunddatei**

Eine Implementierung des COM-strukturierten Speichers für Dateien. Eine Verbunddatei speichert separate Objekte in einer einzelnen strukturierten Datei, die aus zwei Hauptelementen besteht: Storage-Objekten und Stream-Objekten. Zusammen funktionieren Sie wie ein Dateisystem innerhalb einer Datei. Weitere Informationen finden Sie unter Verbunddateien im Microsoft Platform SDK.

Eine Reihe von einzelnen Dateien, die in einer physischen Datei gebunden sind. Jeder einzelnen Datei in einer Verbunddatei kann zugegriffen werden, als wäre es eine einzelne physische Datei.

**Konstante**

Ein numerischer oder Zeichenfolgenwert, der nicht geändert wird. Benannte ADO-Enumerationen (Aufzählungskonstanten) können in Ihrem Code anstelle von tatsächlichen Werten verwendet werden, beispielsweise ist **adUseClient** eine Konstante, deren Wert 3 ist. (Const adUseClient = 3). Siehe auch **-Enumeration**.

**Cursor**

Ein Database-Element, mit dem die Datensatznavigation, die Aktualisierbarkeit und die Transparenz der an der Datenbank von anderen Benutzern vorgenommenen Änderungen gesteuert werden.

Zurück zum Seitenanfang

## <a name="d"></a>D

**Datenbindung**

Der Vorgang des Zuordnens der Objekte oder Steuerelemente einer Anwendung zu einer Datenquelle. Ein Steuerelement, das einer Datenquelle zugeordnet ist, wird als *datengebundenes Steuerelement*bezeichnet.

Die Inhalte eines datengebundenen Steuerelements sind Werten aus einer Datenbank zugeordnet. Ein Grid-Steuerelement, das an ein **Recordset** -Objekt gebunden ist, kann beispielsweise aktualisiert werden, wenn die Zeilen im **Recordset** aktualisiert werden. Wenn neue Werte vom **Recordset**abgerufen werden, werden neue Werte im Raster angezeigt.

**Datenanbieter**

Software, die Daten für eine ADO-Anwendung entweder direkt oder über einen Dienstanbieter bereitstellt. Siehe auch **Dienstanbieter**.

**Datenstrukturierung**

Eine Technik, die eine formalisierte Syntax (die sogenannte **Shape-Sprache**) verwendet, um ein spezielles **Recordset** -Objekt (als **geformtes Recordset**bezeichnet) zu definieren, das nicht nur Daten, sondern auch Verweise auf andere **Recordset** -Objekte enthält und /oder berechnete Werte basierend auf diesen anderen **Recordset** -Objekten.

**Datenquellenebene**

Eine logische Schicht eines verteilten Systems, die einen Computer mit einem DBMS darstellt, beispielsweise eine SQL Server-Datenbank. Siehe auch **Clientebene**, **mittlere Ebene**, **verteilte Anwendung**.

**DCOM**

Ein Draht Protokoll, mit dem COM-Komponenten über ein Netzwerk direkt miteinander kommunizieren können. Siehe auch **com**, **Component**.

**DDL (DatendefinitionsSprache)**

Diese Anweisungen in SQL, die definieren, im Gegensatz zu manipulieren, Daten. Das Schema einer Datenbank wird mit DDL erstellt oder geändert. Beispiel: **CREATE TABLE**, **Create Index**, **Grant**und **REVOKE** sind SQL DDL-Anweisungen.

**Standarddatenstrom**

Ein Text-oder Binärdatenstrom (dargestellt durch ein **Stream** -Objekt), der mit **Record** -oder **Recordset** -Objekten verknüpft ist, wenn bestimmte OLE DB-Anbieter wie der Microsoft OLE DB-Anbieter für Internet Publishing verwendet werden. Der Standarddatenstrom enthält in der Regel den Inhalt einer Datei wie den HTML-Code für den Stamm einer Website.

**verteilte Anwendung**

Ein Programm, das so geschrieben wurde, dass die Verarbeitung über mehrere Computer über ein Netzwerk verteilt werden kann. In der Regel wird eine verteilte Anwendung in Präsentations-, Geschäftslogik-und Datenspeicher Ebenen oder *Ebenen*unterteilt. Siehe auch **Clientebene**, **mittlere Ebene**, **Datenquellenebene**.

**getrenntes Recordset**

Ein **Recordset** -Objekt in einem Clientcache, das nicht mehr über eine Live-Verbindung mit dem Server verfügt. Wenn aus irgendeinem Grund wieder auf die ursprüngliche Datenquelle zugegriffen werden muss, wie beispielsweise das Aktualisieren von Daten, muss die Verbindung wiederhergestellt werden. Auf die Auflistungen, Eigenschaften und Methoden eines getrennten **Recordset-Objekts** kann jedoch weiterhin zugegriffen werden.

**DLL (Dynamic Link Library)**

Eine Datei, die eine oder mehrere Funktionen enthält, die unabhängig von den Prozessen kompiliert, verknüpft und gespeichert werden, die Sie verwenden. Das Betriebssystem ordnet die DLLs dem Adressraum des aufrufenden Prozesses zu, wenn der Prozess gestartet wird oder während er ausgeführt wird.

**DML (Datenbearbeitungssprache)**

Diese Anweisungen in SQL, die bearbeiten, im Gegensatz zu define, Data. Die Werte in einer Datenbank werden mit DML ausgewählt und geändert. Beispielsweise sind **Insert**, **Update**, **Delete**und **Select** SQL DML-Anweisungen.

**Dokumentquellenanbieter**

Eine spezielle Klasse von Anbietern, die Ordner und Dokumente verwalten. Wenn ein Dokument durch ein **Record** -Objekt dargestellt wird oder ein Ordner mit Dokumenten durch ein **Recordset** -Objekt dargestellt wird, füllt der Dokumentquellenanbieter diese Objekte mit einer eindeutigen Gruppe von Feldern auf, die die Eigenschaften des Dokuments beschreiben. anstelle des eigentlichen Dokuments. Siehe auch **Ressourceneintrag**.

**DSN (Datenquellenname)**

Die Sammlung von Informationen, die verwendet werden, um Ihre Anwendung mit einer bestimmten ODBC-Datenbank zu verbinden. Der ODBC-Treiber-Manager verwendet diese Informationen, um eine Verbindung mit der Datenbank herzustellen. Ein DSN kann in einer Datei (einem Datei-DSN) oder in der Windows-Registrierung (eine Computer-DSN) gespeichert werden.

**Dynamic-Eigenschaft**

Eine Eigenschaft, die für einen Datenanbieter oder den Cursordienst spezifisch ist. Die **Properties** -Auflistung eines Objekts wird automatisch mit diesen ("dynamisch") aufgefüllt. Ein Objekt hat keine dynamischen Eigenschaften, bis es mit einer Datenquelle über einen bestimmten Datenanbieter verbunden ist. Siehe auch **Data Provider**, **Cursor**.

Zurück zum Seitenanfang

## <a name="e-i"></a>E-I

**Enumeration**

Eine Liste mit benannten Konstanten. AufZählungswerte müssen nicht eindeutig sein. Der Name der einzelnen Werte muss jedoch innerhalb des Bereichs, in dem die Enumeration definiert ist, eindeutig sein. In ADO werden Enumerationen für numerische Parameter und Rückgabewerte verwendet, um ADO-Code eine Bedeutung hinzuzufügen und den Entwickler von den numerischen Werten abzuschirmen (was sich von Version zu Version ändern kann). Um beispielsweise ein statisches **Recordset**-Objekt zu öffnen, verwenden Sie den **adOpenStatic** -Aufzählungswert:  
  

Wird auch als aufgezählte *Konstante*bezeichnet. Siehe auch **Constant**.

**event**

Eine Aktion, die von einem Objekt erkannt wird, für das Sie Code zur Reaktion schreiben können. Ereignisse können unter anderem durch Befehlsausführung, Transaktionsabschluss, Recordset-Navigation und Datenaktualisierungen generiert werden. Siehe auch **Ereignishandler**.

**Ereignishandler**

Ein Ereignishandler ist der Code, der ausgeführt wird, wenn ein Ereignis auftritt. Siehe auch- **Ereignis**.

**handler**

Eine Routine, die eine allgemeine und relativ einfache Bedingung oder einen Vorgang wie die Fehlerwiederherstellung oder die Datenverwaltung verwaltet.

**Hierarchisches Recordset**

Ein **Recordset** -Objekt, das ein anderes **Recordset**-Objekt enthält. Siehe auch **Datenstrukturierung**, **Kapitel**.

Weitere Informationen finden Sie unter [zugreifen auf Zeilen in einem hierarchischEn Recordset](accessing-rows-in-a-hierarchical-recordset.md)

**Hierarchie**

Im Allgemeinen ist eine Hierarchie eine geordnete Struktur mit einer obersten Ebene und untergeordneten Ebenen. In ADO werden hierarchische **Recordsets** verwendet, um die über-und untergeordnete Beziehung zwischen einem Datensatz und einem Kapitel darzustellen. Auch in ADO können **Record** -und **Stream** -Objekte für den Zugriff auf hierarchische Struktur Strukturen wie Ordner und Dokumente verwendet werden. ADO MD enthält auch **Hierarchie** Objekte, um eine Beziehung zwischen den Ebenen einer Dimension in einem OLAP-Cube darzustellen. Siehe auch **hierarchische Recordsets**, **Parent-Child-Beziehung**, **Chapter**, **Tree**.

**ISAPI (Internet Server Application Programming Interface)**

Eine Reihe von Funktionen für Internet Server, beispielsweise einen Windows NT Server/Windows 2000-Server mit Microsoft Internet Information Services (IIS).

Zurück zum Seitenanfang

## <a name="k-m"></a>Km

**key**

Eine Spalte oder Spalten in einer Tabelle, die eine Zeile eindeutig identifiziert; wird häufig zum Indizieren einer Tabelle verwendet.

**Marshalling**

Der Vorgang des Packens, Sendens und entpacken von Schnittstellenmethoden Parametern über Thread-oder Prozessgrenzen hinweg.

**mittlere Ebene**

Die logische Ebene in einem verteilten System zwischen einer Benutzeroberfläche oder einem Webclient und der Datenbank. In der Regel werden Geschäftsobjekte instanziiert. Bei der mittleren Ebene handelt es sich um eine Sammlung von Geschäftsregeln und-Funktionen, die Informationen generieren und verwenden. Dies erreichen Sie durch Geschäftsregeln, die sich häufig ändern und daher in Komponenten gekapselt werden, die physisch von der Anwendungslogik selbst getrennt sind. Wird auch als *Anwendungsserverebene*bezeichnet. Siehe auch **verteilte Anwendung**, **Clientebene**, **Datenquellenebene**.

**MIME (mehr Zweck Internet-e-Mail-Erweiterung)**

Ein Internet Protokoll, das ursprünglich für den Austausch von e-Mail-Nachrichten mit umfangreichen Inhalten in heterogenen Netzwerk-, Computer-und e-Mail-Umgebungen entwickelt wurde. In der Praxis wurde MIME auch von nicht-e-Mail-Anwendungen übernommen und erweitert.

MIME ist ein Standard, mit dem binäre Daten im Internet veröffentlicht und gelesen werden können. Die Kopfzeile einer Datei mit Binärdaten enthält den MIME-Typ der Daten; Dadurch werden Clientprogramme (beispielsweise Webbrowser und e-Mail-Pakete) darüber informiert, dass Sie die Daten anders behandeln müssen als gerade Text. Beispielsweise enthält die Kopfzeile eines Webdokuments mit einer JPEG-Grafik den MIME-Typ, der für das JPEG-Dateiformat spezifisch ist. Dadurch kann ein Browser die Datei mit dem JPEG-Viewer anzeigen, sofern vorhanden.

Zurück zum Seitenanfang

## <a name="n-o"></a>N-O

**Knoten**

Ein Element in einer hierarchischen Struktur. Ein Knoten kann der Stamm oder das untergeordnete Element eines anderen Knotens sein. Ein Knoten kann auch das übergeordnete Element mehrerer untergeordneter Elemente sein. Siehe auch **Hierarchie**, **Baum**, **Stamm**, **Kind**, **übergeordnetes Element**.

**Objektvariable**

Eine Variable, die einen Verweis auf ein Objekt enthält. Beispielsweise ist objCustomObject eine Variable, die auf ein Objekt vom Typ Customobject zeigt:  
  
ist eine Variable, die auf ein Objekt vom Typ Customobject zeigt:  
  
Legen Sie objCustomObject = CreateObject (ADODB. Recordset

**ODBC (Open Database Connectivity)**

Eine Standardschnittstelle für Programmiersprachen, die zum Herstellen einer Verbindung mit einer Vielzahl von Datenquellen verwendet wird. Auf diesen Zugriff wird normalerweise über die Systemsteuerung zugegriffen, wobei Datenquellennamen (DSNs) für die Verwendung bestimmter ODBC-Treiber zugewiesen werden können.

**OLE DB**

Eine Gruppe von Schnittstellen, die Daten aus einer Vielzahl von Quellen mithilfe von COM verfügbar machen. OLE DB-Schnittstellen bieten Anwendungen einen einheitlichen Zugriff auf Daten, die in unterschiedlichen Informationsquellen gespeichert sind. Diese Schnittstellen unterstützen die für die Datenquelle geeignete DBMS-Funktionalität, sodass Sie Ihre Daten freigeben kann. Siehe auch **com**.

**optimistische Sperrung**

Ein Sperrtyp, bei dem die Datenseite, die einen oder mehrere Datensätze enthält, einschließlich des bearbeiteten Datensatzes, für andere Benutzer nur verfügbar ist, während der Datensatz von der **Update** -Methode aktualisiert wird, aber vor und nach dem Aufruf von **Update** verfügbar ist. .

Optimistische Sperren werden verwendet, wenn das **Recordset** -Objekt mit **** dem LockType-Parameter oder der Eigenschaft auf **adLockOptimistic** oder **adLockBatchOptimistic**. Siehe auch **pessimistische Sperrung**.

**Ordnungswert**

Die numerische Position eines Elements innerhalb eines Auftrags. In einer ADO-Auflistung ist der Ordnungswert des ersten Elements NULL (0). Das nächste Element ist eins (1) usw.

Zurück zum Seitenanfang

## <a name="p"></a>P

**parametrisierter Befehl**

Eine Abfrage oder ein Befehl, mit dem Sie Parameterwerte festlegen können, bevor der Befehl ausgeführt wird. Eine SQL-Zeichenfolge kann beispielsweisedurch das Einbetten von Parametermarkierungen in die SQL-Zeichenfolge (durch das Zeichen "?" gekennzeichnet) parametrisiert werden. Die Anwendung gibt dann die Werte für jeden Parameter an und führt den Befehl aus.

**Eltern**

Die Steuerung einer hierarchischen Beziehung. In einer hierarchischen Struktur weist ein übergeordnetes Element einen oder mehrere untergeordnete Knoten direkt darunter in der Hierarchie auf. Siehe auch **Parent-Alias**, **Parent-Child Relationship**, **Child**.

**parent-alias**

Ein Alias, der auf das übergeordnete Element verweist. Siehe auch **Alias**, **übergeordnetes Element**.

**Beziehung zwischen über-und untergeordneten Elementen**

Eine Beziehung in einer hierarchischen Struktur, in der das übergeordnete Element eine Ebene höher und direkt einem oder mehreren untergeordneten Elementen zugeordnet ist. Ein untergeordnetes Element ist eine Ebene niedriger und muss ein übergeordnetes Element aufweisen. Siehe auch **Parent**, **Child**.

**beibehalten**

Zum Speichern von Daten in einem permanenten Status, beispielsweise zum Speichern eines **Recordset-Objekts** in einer Datei.

**pessimistische Sperrung**

Ein Sperrtyp, bei dem die Seite, die einen oder mehrere Datensätze enthält, einschließlich des bearbeiteten Datensatzes, für andere Benutzer nicht verfügbar ist, um sicherzustellen, dass ein Update vorgenommen wird. Das pessimistische Sperrverhalten wird vom OLE DB-Anbieter definiert. In der Regel werden Datensätze bei der Bearbeitung gesperrt und bleiben erst verfügbar, wenn die **Update** -Methode abgeschlossen ist.

Die pessimistische Sperre wird aktiviert, wenn das **Recordset** -Objekt mit **** dem LockType-Parameter oder der Eigenschaft auf **AdLockPessimistic**geöffnet wird. Siehe auch **optimistische Sperrung**.

**Pooling**

Eine Leistungsoptimierung, die auf der Verwendung von Auflistungen von vorab zugewiesenen Ressourcen wie Objekten oder Datenbankverbindungen basiert. Es ist effizienter, eine vorhandene Ressource aus dem Pool zu zeichnen, als eine neue Ressource zu erstellen.

**ProgID (Programmed Identifier)**

Ein eindeutiger Name, der der Windows-Registrierung von einer COM-Anwendung zugeordnet ist. Die ProgID für eine ADO-Verbindung lautet "ADODB. Connection ". Siehe auch **CLSID** **com**.

**Proxy**

Ein Schnittstellen spezifisches Objekt, das das Marshallen und die Kommunikation bereitstellt, die ein Client zum Aufrufen eines Application-Objekts benötigt, das in einer anderen Ausführungsumgebung ausgeführt wird, beispielsweise in einem anderen Thread oder in einem anderen Prozess. Der Proxy befindet sich beim Client und kommuniziert mit einem entsprechenden Stub, der sich mit dem aufgerufenen Application-Objekt befindet. Siehe auch **Stub**.

Zurück zum Seitenanfang

## <a name="r"></a>R

**relative URL**

Eine teilweise qualifizierte URL, die eine Ressource im Internet oder in einem Intranet angibt, deren Speicherort relativ zu einem Anfangspunkt ist, der durch eine absolute URL oder ein entsprechendes ADO-Connection-Objekt angegeben ist. Die verketteten absoluten und relativen URLs consitute eine vollständige URL. Siehe auch **URL** und **absolute URL**.

**Remotedatenquelle**

Eine Datenquelle, die auf einem anderen Computer vorhanden ist, statt auf dem lokalen System (in dem die Clientanwendung ausgeführt wird).

**Ressourceneintrag**

Ein Datensatz aus einem Dokumentquellenanbieter, der Felder für die Definition und Beschreibung eines Ordners oder Dokuments enthält. Das Dokument selbst ist nicht im Ressourceneintrag enthalten, aber in der Regel kann der Standarddatenstrom oder ein Feld im Ressourceneintrag mit einer URL zugegriffen werden. Siehe auch **Dokumentquellenanbieter**, **Standarddatenstrom**, **URL**.

**root**

Die oberste Ebene in einer hierarchischen Struktur. Der Stammknoten hat keine übergeordneten Elemente, er kann jedoch untergeordnet sein. Siehe auch **Hierarchie**, **Baum**, **übergeordnet**, **untergeordnet**.

**Rowset**

Eine Reihe von Zeilen aus einer Datenquelle, die alle dasselbe Feld Schema aufweisen. Ein Rowset kann alle oder einige Felder aus einer Tabelle darstellen. Ein Rowset kann auch eine virtuelle Tabelle darstellen, die durch eine Abfrage oder eine Verknüpfung von zwei oder mehr Tabellen erstellt wird. In ADO werden Rowsets durch **Recordset** -Objekte dargestellt.

Zurück zum Seitenanfang

## <a name="s"></a>S

**Schema**

Eine Beschreibung einer Datenbank für das Datenbankverwaltungssystem (DBMS), die in der Regel mithilfe der vom DBMS bereitgestellten Datendefinitionssprache generiert wird. Ein Schema definiert Attribute der Datenbank, wie Tabellen, Spalten und Eigenschaften.

**scope**

Der Referenzwert für ein Objekt oder eine Variable oder einen Datensatztyp in einer Ansicht oder Tabelle. Lokale Variablen können beispielsweise nur innerhalb der Prozedur referenziert werden, in der Sie definiert wurden. Auf öffentliche Variablen kann von einer beliebigen Stelle in der Anwendung aus zugegriffen werden. Objekte, wie die aktuelle Datenbank, befinden sich im Bereich, wenn Sie sich im definierten Suchpfad befinden. Datensatzbereiche können mit einer Scope-Klausel in zahlreichen Befehlen angegeben werden.

**Dienstanbieter**

Software, die einen Dienst kapselt, indem Daten erstellt und genutzt werden, wodurch Features in Ihren ADO-Anwendungen erweitert werden. Es handelt sich dabei um einen Anbieter, der Daten nicht direkt verfügbar macht, sondern einen Dienst wie die Abfrageverarbeitung bereitstellt. Der Dienstanbieter verarbeitet Daten, die von einem Datenanbieter bereitgestellt werden. Siehe auch **Data Provider**.

**geformtes Recordset**

Ein **Recordset** -Objekt, dessen Spalten speziell definiert wurden, um nicht nur Daten, sondern auch Verweise (als Chapter bezeichnet) auf andere **Recordset** -Objekte und/oder berechnete Werte basierend auf anderen **Recordset** -Objekten zu enthalten.

**gleichgeordneten Knoten**

Zwei oder mehr Knoten in einer hierarchischen Struktur, die sich auf derselben Ebene in der Hierarchie befinden. Der Stammknoten in einer Hierarchie hat keine gleichgeordneten Elemente.

**Gespeicherte Prozedur**

Eine vorkompilierte Auflistung von Code wie SQL-Anweisungen und optionalen Ablaufsteuerungsanweisungen, die unter einem Namen gespeichert und als Einheit verarbeitet werden. Gespeicherte Prozeduren werden in einer Datenbank gespeichert; Sie können mit einem Aufruf von einer Anwendung ausgeführt werden und Benutzer deklarierte Variablen, bedingte Ausführung und andere leistungsstarke Programmierfeatures zulassen.

**Stub**

Ein Interface-spezifisches Objekt, das das Marshallen und die Kommunikation bereitstellt, die für ein Application-Objekt erforderlich ist, um Aufrufe von einem Client zu empfangen, der in einer anderen Ausführungsumgebung ausgeführt wird, beispielsweise in einem anderen Thread oder in einem anderen Prozess. Der Stub befindet sich mit dem Application-Objekt und kommuniziert mit einem entsprechenden Proxy, der sich mit dem Client befindet, von dem es aufgerufen wird. Siehe auch **Proxy**.

**Unterknoten**

Siehe **Child**.

**synchroner Vorgang**

Ein von Code initiierter Vorgang, der vor dem nächsten Vorgang abgeschlossen werden kann. Siehe auch **asynchroner Vorgang**.

Zurück zum Seitenanfang

## <a name="t-w"></a>T-W

**Struktur**

Eine Struktur, die eine hierarchische Beziehung zwischen Elementen (Knoten) darstellt. Es gibt einen Knoten auf der obersten Ebene einer Struktur (der Stamm). Unter dem Stamm können mehrere untergeordnete Elemente vorhanden sein. Jedes Kind kann wiederum das übergeordnete Element anderer Kinder sein und verzweigt sich wie eine Struktur. Ein Ordner mit Dokumenten und anderen Ordnern ist ein typisches Beispiel für eine Baumstruktur. Siehe auch **Hierarchie**, **Knoten**, **Stamm**, **Kind**, **übergeordnetes Element**.

**URL (Uniform Resource Locator)**

Gibt den Speicherort einer Ressource an, die sich im Internet oder in einem Intranet befindet. Eine vollständige URL besteht aus einem Schema (wie FTP, HTTP, mailto, File usw.), gefolgt von einem Doppelpunkt, einem Servernamen und dem vollständigen Pfad einer Ressource (beispielsweise einem Dokument, einer Grafik oder einer anderen Datei). Einige Beispiele für URLs sind:  
  
- https://www.domain.com/default.html  
- FTP://FTP.Server.somewhere/ftp.file  
  
- FTP://FTP.Server.somewhere/ftp.file  
- file://Server/Share/File.doc

Siehe auch **absolute URL** und **relative URL**.

**Webserver**

Ein Computer, der Intranet-und Internet Benutzern Webdienste und Seiten bereitstellt.



