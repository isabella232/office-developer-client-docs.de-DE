---
title: ActiveX Data Objects (ADO)-Glossar
TOCTitle: ADO Glossary
ms:assetid: 40f00876-7525-4117-8f57-f3d87c54be99
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249184(v=office.15)
ms:contentKeyID: 48544438
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: d9b80155bcd88ac486b01a6b6a272b265463b142
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59553368"
---
# <a name="ado-glossary"></a>ADO-Glossar

**Gilt für**: Access 2013, Office 2013

## <a name="a"></a>A

**Absolute URL**

Eine vollqualifizierte URL, die den Speicherort einer Ressource angibt, die sich im Internet oder in einem Intranet befindet. Siehe auch **URL** und **relative URL.**

**ActiveX-Steuerelement**

Selbst registrierende, prozessinterne COM-Komponente, die häufig ein visuelles Element zur Entwurfs- oder Laufzeit aufweist. ActiveX Steuerelemente können auch mit einem Container für aktive Dokumente kommunizieren, z. B. Microsoft Internet Explorer.

**ADISAPI (Advanced Data Internet Server Application Programming Interface)**

Eine ISAPI-DLL, die Analyse,  Automatisierungssteuerelement, Recordset-Marshaling und MIME-Verpackung bereitstellt. Die ADISAPI-Komponente funktioniert über die von Internetinformationsdienste (IIS) bereitgestellte API. Siehe auch **ISAPI**.

**Aggregatfunktion**

In einer Abfrage eine Funktion wie COUNT, AVG oder STDEV, die einen Wert mit allen Zeilen in einer Spalte einer Tabelle berechnet. Beim Schreiben von Ausdrücken und beim Programmieren können Sie SQL Aggregatfunktionen (einschließlich der drei oben aufgeführten) und Domänenaggregatfunktionen verwenden, um verschiedene Statistiken zu bestimmen.

**alias**

Ein alternativer Name, den Sie einer Spalte oder einem Ausdruck in einer SQL SELECT-Anweisung geben, häufig kürzer oder aussagekräftiger. Beispielsweise ist BobSales der Alias in der folgenden SELECT-Anweisung: "Select wr-Sales as BobSales from SalesDB". Ein Alias kann zum dynamischen Zuweisen von Spalten zum Steuern von Bindungen für das **DataControl-Objekt** verwendet werden.

**Apartmentthreading**

Ein COM-Threadingmodell, bei dem alle Aufrufe eines Objekts in einem Thread erfolgen. Beim Apartmentthreading werden AUFRUFE von COM synchronisiert und gemarshallt. Siehe auch **COM**.

**asynchroner Vorgang**

Ein Vorgang, der die Steuerung an das aufrufende Programm zurückgibt, ohne auf den Abschluss des Vorgangs zu warten. Bevor der Vorgang abgeschlossen ist, wird die Codeausführung fortgesetzt. Siehe auch **synchrone Operation.**

Zurück zum Seitenanfang

## <a name="b"></a>B

**Bindungseintrag**

Eine Zuordnung zwischen einem Feld in einer Tabelle und einer Variablen. In den ADO Visual C++-Erweiterungen werden **Recordset-Felder** C/C++-Variablen zugeordnet.

**Bitmaske**

Ein numerischer Wert, der für einen Bit-für-Bit-Wertvergleich mit anderen numerischen Werten vorgesehen ist, in der Regel zum Kennzeichnen von Optionen in Parametern oder Rückgabewerten. Dieser Vergleich erfolgt in der Regel mit bitweisen logischen Operatoren wie **"And"** und **"Or"** in Visual Basic **&** und in **|** C++.

Beispielsweise können die ADO **FieldAttributeEnum-Werte** als Bitmasken verwendet werden, um die Attribute eines Felds zu bestimmen. Angenommen, Sie möchten ermitteln, ob ein Feld aktualisiert werden kann. Sie können dies mit dem folgenden Ausdruck in Visual Basic testen:  
  

Wenn das Ergebnis TRUE ist, kann das Feld aktualisiert werden.

**bookmark**

Eine Markierung, die eine Zeile innerhalb einer Reihe von Zeilen eindeutig identifiziert, sodass ein Benutzer schnell zu dieser Zeile navigieren kann.

**Geschäftsobjekt**

Ein Objekt, das einen definierten Satz von Vorgängen ausführt, z. B. Datenüberprüfung oder Geschäftsregellogik. Geschäftsobjekte befinden sich in der Regel auf der mittleren Ebene.

**Geschäftsregel**

Die Kombination aus Überprüfungsbearbeitungen, Anmeldeüberprüfungen, Datenbanksuche, Richtlinien und algorithmischen Transformationen, die die Geschäftstätigkeit eines Unternehmens darstellen. Wird auch als *Geschäftslogik* bezeichnet.

Zurück zum Seitenanfang

## <a name="c"></a>C

**Berechneter Ausdruck**

Ein Ausdruck, der nicht konstant ist, dessen Wert jedoch von anderen Werten abhängt. Um ausgewertet zu werden, muss ein berechneter Ausdruck Werte aus anderen Quellen abrufen und berechnen, in der Regel in anderen Feldern oder Zeilen.

**Kapitel**

Ein Verweis auf einen Zeilenbereich aus einer Datenquelle. In ADO ist ein Kapitel in der Regel ein Verweis auf ein anderes **Recordset -Objekt.**

Kapitelspalten ermöglichen des Definieren einer *Übergeordnet-Untergeordnet*-Beziehung, in der das *übergeordnete* Element das **Recordset**-Objekt ist, das die Kapitelspalte enthält, und das *untergeordnete* Element das durch das Kapitel dargestellte **Recordset**-Objekt ist.

**chapter-alias**

Ein Alias, der sich auf die Spalte bezieht, die an das übergeordnete Element angefügt ist.

**Zeichensatz**

Eine Zuordnung einer Gruppe von Zeichen zu ihren numerischen Werten. Unicode ist beispielsweise ein 16-Bit-Zeichensatz, der alle bekannten Zeichen codieren kann und als weltweiter Zeichencodierungsstandard verwendet wird.

**Kind**

Die abhängige Seite einer hierarchischen Beziehung. Ein untergeordnetes Element ist ein Knoten in einer hierarchischen Struktur, der einen anderen Knoten darüber hat (näher am Stamm). Siehe auch **untergeordneter Alias,** **Beziehung zwischen übergeordneten und untergeordneten** Elementen, **übergeordneten** Elementen.

**child-alias**

Ein Alias, der auf das untergeordnete Element verweist. Siehe auch **Alias**, **untergeordnetes** Element.

**CLSID (Klassenbezeichner)**

Ein universally unique identifier (UUID), der eine COM-Komponente identifiziert. Jede COM-Komponente verfügt über ihre CLSID in der Windows-Registrierung, sodass sie von anderen Anwendungen geladen werden kann. Siehe auch **ProgID**, **COM**.

**Clientebene**

Eine logische Ebene eines verteilten Systems, das in der Regel Daten zum Benutzer darstellt und Eingaben verarbeitet, die manchmal als *Front-End* bezeichnet werden. In der Regel fordert die Clientebene Daten von einem Server basierend auf der Eingabe an und formatiert dann das Ergebnis und zeigt es an. Siehe auch **mittlere Ebene,** **Datenquellenebene,** **verteilte Anwendung.**

**COM (Component Object Model)**

Ein binärer Standard, der es Objekten ermöglicht, in einer netzwerkgebundenen Umgebung unabhängig von der Sprache, in der sie entwickelt wurden, oder auf den Computern, auf denen sie sich befinden, zu zusammenarbeiten. COM-basierte Technologien umfassen ActiveX Steuerelemente, Automatisierung und Objektverknüpfung und Einbettung (OLE). COM ermöglicht es einem Objekt, seine Funktionalität für andere Komponenten und Hostanwendungen verfügbar zu machen. Es definiert sowohl, wie sich das Objekt selbst verfügbar macht, als auch wie diese Belichtung prozess- und netzwerkübergreifend funktioniert. COM definiert auch den Lebenszyklus des Objekts.

**COM-Komponente**

Binärdatei , z. B. .dll, OCX und einige .exe Dateien, die den COM-Standard für die Bereitstellung von Objekten unterstützt. Eine solche Datei enthält Code für eine oder mehrere Klassenfactorys, COM-Klassen, Registrierungseintragsmechanismen, Ladecode usw.

**Vergleichsoperator**

Ein Operator, der zwei Ausdrücke vergleicht und einen booleschen Wert zurückgibt.

Ein Kriterienparameter, der als " \> " (größer als), " \<" (less than), "=" (equal), "\> =" (größer als oder gleich), " \<=" (less than or equal), "\<\> " (ungleich) oder "like" (Mustervergleich) ausgedrückt werden kann.

**component**

Ein Objekt, das Sowohl Daten als auch Code kapselt und eine reihe von öffentlich verfügbaren Diensten bereitstellt.

**Verbunddatei**

Eine Implementierung des strukturierten COM-Speichers für Dateien. Eine zusammengesetzte Datei speichert separate Objekte in einer einzelnen strukturierten Datei, die aus zwei Hauptelementen besteht: Speicherobjekten und Streamobjekten. Zusammen funktionieren sie wie ein Dateisystem innerhalb einer Datei. Weitere Informationen finden Sie unter "Verbunddateien" im Microsoft Platform SDK.

Eine Anzahl einzelner Dateien, die in einer physischen Datei miteinander verbunden sind. Auf jede einzelne Datei in einer Verbunddatei kann wie auf eine einzelne physische Datei zugegriffen werden.

**Konstante**

Ein numerischer oder Zeichenfolgenwert, der sich nicht ändert. Benannte ADO-Enumerationen (aufgezählte Konstanten) können im Code anstelle der tatsächlichen Werte verwendet werden, **z. B. ist adUseClient** eine Konstante, deren Wert 3 ist. (Const adUseClient = 3). Siehe auch **Enumeration**.

**Cursor**

Ein Datenbankelement, das die Datensatznavigation, die Aktualisierung von Daten und die Sichtbarkeit von Änderungen steuert, die von anderen Benutzern an der Datenbank vorgenommen wurden.

Zurück zum Seitenanfang

## <a name="d"></a>D

**Datenbindung**

Der Vorgang zum Zuordnen der Objekte oder Steuerelemente einer Anwendung zu einer Datenquelle. Ein Steuerelement, das einer Datenquelle zugeordnet ist, wird als *datengebundenes Steuerelement* bezeichnet.

Der Inhalt eines datengebundenen Steuerelements ist Werten aus einer Datenbank zugeordnet. Beispielsweise kann ein Rastersteuerelement, das an ein **Recordset** -Objekt gebunden ist, aktualisiert werden, wenn die Zeilen im **Recordset** aktualisiert werden. Wenn neue Werte vom **Recordset** abgerufen werden, werden neue Werte im Raster angezeigt.

**Datenanbieter**

Software, die Daten für eine ADO-Anwendung direkt oder über einen Dienstanbieter verfügbar macht. Siehe auch **Dienstanbieter**.

**Datenstrukturierung**

Eine Technik, bei der eine formalisierte Syntax **(shape** language) verwendet wird, um ein spezielles **Recordset-Objekt** (auch als **formiertes Recordset** bezeichnet) zu definieren, das nicht nur Daten, sondern auch Verweise auf andere **Recordset-Objekte** und/oder berechnete Werte basierend auf diesen anderen **Recordset-Objekten** enthält.

**Datenquellenebene**

Eine logische Ebene eines verteilten Systems, die einen Computer darstellt, auf dem ein DBMS ausgeführt wird, z. B. eine SQL Server Datenbank. Siehe auch **Clientebene,** **mittlere Ebene,** **verteilte Anwendung.**

**DCOM**

Ein Drahtprotokoll, das es COM-Komponenten ermöglicht, direkt über ein Netzwerk miteinander zu kommunizieren. Siehe auch **COM**, **Komponente**.

**DDL (Data Definition Language)**

Diese Anweisungen in SQL, die Daten definieren, anstatt sie zu bearbeiten. Das Schema einer Datenbank wird mit DDL erstellt oder geändert. CREATE **TABLE,** **CREATE INDEX,** **GRANT** und **REVOKE** sind beispielsweise SQL DDL-Anweisungen.

**Standarddatenstrom**

Ein Text- oder binärer  Datenstrom (dargestellt durch ein Stream-Objekt), der **mit Record-** oder **Recordset-Objekten** verknüpft ist, wenn bestimmte OLE DB-Anbieter verwendet werden, z. B. der Microsoft OLE DB-Anbieter für Internet Publishing. Der Standarddatenstrom enthält in der Regel den Inhalt einer Datei, z. B. den HTML-Code für den Stamm einer Website.

**Verteilte Anwendung**

Ein Programm, das so geschrieben wurde, dass die Verarbeitung über ein Netzwerk auf mehrere Computer aufgeteilt werden kann. In der Regel wird eine verteilte Anwendung in Darstellungs-, Geschäftslogik- und Datenspeicherebenen oder *Ebenen* unterteilt. Siehe auch **Clientebene,** **mittlere Ebene,** **Datenquellenebene.**

**getrenntes Recordset**

Ein **Recordset-Objekt** in einem Clientcache, das keine Liveverbindung mehr mit dem Server hat. Wenn aus irgendeinem Grund erneut auf die ursprüngliche Datenquelle zugegriffen werden muss, z. B. beim Aktualisieren von Daten, muss die Verbindung wiederhergestellt werden. Auf die Auflistungen, Eigenschaften und Methoden eines getrennten **Recordset-Objekts** kann jedoch weiterhin zugegriffen werden.

**DLL (Dynamic Link Library)**

Eine Datei, die eine oder mehrere Funktionen enthält, die separat von den Prozessen, die sie verwenden, kompiliert, verknüpft und gespeichert werden. Das Betriebssystem ordnet die DLLs dem Adressraum des aufrufenden Prozesses zu, wenn der Prozess gestartet wird oder während der Ausführung.

**DML (Data Manipulation Language)**

Diese Anweisungen in SQL, die Daten ändern, anstatt sie zu definieren. Die Werte in einer Datenbank werden mit DML ausgewählt und geändert. Insert,  **UPDATE,** **DELETE** und **SELECT** sind beispielsweise SQL DML-Anweisungen.

**Dokumentquellanbieter**

Eine spezielle Klasse von Anbietern, die Ordner und Dokumente verwalten. Wenn ein Dokument durch ein **Record -Objekt** dargestellt wird oder ein Ordner von Dokumenten durch ein **Recordset** -Objekt dargestellt wird, füllt der Dokumentquellenanbieter diese Objekte mit einem eindeutigen Satz von Feldern, die Merkmale des Dokuments beschreiben, anstelle des eigentlichen Dokuments selbst. Siehe auch **Ressourceneintrag.**

**DSN (Datenquellenname)**

Die Sammlung von Informationen, die zum Verbinden der Anwendung mit einer bestimmten ODBC-Datenbank verwendet werden. Der ODBC-Treiber-Manager verwendet diese Informationen, um eine Verbindung mit der Datenbank herzustellen. Ein DSN kann in einer Datei (einem Datei-DSN) oder in der Windows Registrierung (einem Computer-DSN) gespeichert werden.

**Dynamische Eigenschaft**

Eine für einen Datenanbieter oder cursordienst spezifische Eigenschaft. Die **Properties-Auflistung** eines Objekts wird automatisch ("dynamisch") mit diesen aufgefüllt. Ein Objekt hat keine dynamischen Eigenschaften, bis es über einen bestimmten Datenanbieter mit einer Datenquelle verbunden ist. Siehe auch **Datenanbieter**, **Cursor**.

Zurück zum Seitenanfang

## <a name="e-i"></a>E-I

**Enumeration**

Eine Liste benannter Konstanten. Aufgezählte Werte müssen nicht eindeutig sein. Der Name jedes Werts muss jedoch innerhalb des Bereichs eindeutig sein, in dem die Enumeration definiert ist. In ADO werden Enumerationen für numerische Parameter und Rückgabewerte verwendet, um ADO-Code Bedeutung hinzuzufügen und den Entwickler von den numerischen Werten zu schützen (die von Version zu Version geändert werden können). Um beispielsweise ein statisches **Recordset** zu öffnen, verwenden Sie den **adOpenStatic-Aufzählungswert:**  
  

Wird auch als *Aufzählungskonstante* bezeichnet. Siehe auch **Konstante**.

**event**

Eine von einem Objekt erkannte Aktion, für die Sie Code schreiben können, um zu antworten. Ereignisse können unter anderem durch Befehlsausführung, Transaktionsabschluss, Datensatznavigation und Datenaktualisierungen generiert werden. Siehe auch **Ereignishandler.**

**Ereignishandler**

Ein Ereignishandler ist der Code, der ausgeführt wird, wenn ein Ereignis auftritt. Siehe auch **Ereignis**.

**handler**

Eine Routine, die einen allgemeinen und relativ einfachen Zustand oder Vorgang verwaltet, z. B. fehlerwiederherstellung oder Datenverwaltung.

**hierarchisches Recordset**

Ein **Recordset-Objekt,** das ein anderes **Recordset -Objekt** enthält. Siehe auch **Datenstrukturierung**, **Kapitel**.

Weitere Informationen finden Sie unter ["Zugreifen auf Zeilen in einem hierarchischen Recordset"](accessing-rows-in-a-hierarchical-recordset.md)

**Hierarchie**

Im Allgemeinen ist eine Hierarchie eine Rangfolgestruktur mit einer obersten Ebene und untergeordneten Ebenen. In ADO werden hierarchische **Recordsets** verwendet, um die beziehung zwischen einem Datensatz und einem Kapitel über- und untergeordnete Elemente darzustellen. Auch in ADO können **Record-** und **Stream-Objekte** verwendet werden, um auf hierarchische Strukturstrukturen wie z. B. einen Ordner und Dokumente zuzugreifen. ADO MD enthält auch **Hierarchy-Objekte,** die eine Beziehung zwischen den Ebenen einer Dimension in einem OLAP-Cube darstellen. Siehe auch **hierarchische Recordsets**, **Parent-Child-Beziehung**, **Kapitel**, **Struktur**.

**ISAPI (Internet Server Application Programming Interface)**

Eine Reihe von Funktionen für Internetserver, z. B. ein Windows NT-Server/Windows 2000-Server, auf dem Microsoft-Internetinformationsdienste (IIS) ausgeführt wird.

Zurück zum Seitenanfang

## <a name="k-m"></a>K-M

**key**

Eine Spalte oder Spalten in einer Tabelle, die eine Zeile eindeutig identifizieren; wird häufig zum Indizierung einer Tabelle verwendet.

**Marshalling**

Der Prozess des Verpackens, Sendens und Entpackens von Schnittstellenmethodenparametern über Thread- oder Prozessgrenzen hinweg.

**mittlere Ebene**

Die logische Ebene in einem verteilten System zwischen einer Benutzeroberfläche oder einem Webclient und der Datenbank. Hier werden in der Regel Geschäftsobjekte instanziiert. Die mittlere Ebene ist eine Sammlung von Geschäftsregeln und -funktionen, die Informationen generieren und beim Empfang von Informationen ausführen. Sie erreichen dies über Geschäftsregeln, die sich häufig ändern können, und werden daher in Komponenten gekapselt, die physisch von der Anwendungslogik selbst getrennt sind. Wird auch als *Anwendungsserverebene* bezeichnet. Siehe auch **verteilte Anwendung,** **Clientebene,** **Datenquellenebene.**

**MIME (Multi-purpose Internet Mail Extension)**

Ein Internetprotokoll wurde ursprünglich entwickelt, um den Austausch von E-Mail-Nachrichten mit umfangreichen Inhalten in heterogenen Netzwerk-, Computer- und E-Mail-Umgebungen zu ermöglichen. In der Praxis wurde MIME auch von Nicht-Mail-Anwendungen übernommen und erweitert.

MIME ist ein Standard, mit dem binäre Daten im Internet veröffentlicht und gelesen werden können. Der Header einer Datei mit Binärdaten enthält den MIME-Typ der Daten. Dadurch werden Clientprogramme (z. B. Webbrowser und E-Mail-Pakete) darüber informiert, dass sie die Daten anders verarbeiten müssen als mit geradem Text. Beispielsweise enthält die Kopfzeile eines Webdokuments, das eine JPEG-Grafik enthält, den FÜR das JPEG-Dateiformat spezifischen MIME-Typ. Auf diese Weise kann ein Browser die Datei mit dem JPEG-Viewer anzeigen, sofern vorhanden.

Zurück zum Seitenanfang

## <a name="n-o"></a>N-O

**Knoten**

Ein Element in einer hierarchischen Struktur. Ein Knoten kann der Stamm oder das untergeordnete Element eines anderen Knotens sein. Ein Knoten kann auch das übergeordnete Element mehrerer untergeordneter Elemente sein. Siehe auch **Hierarchie**, **Struktur**, **Stamm**, **untergeordnete**, **übergeordnete**.

**Objektvariable**

Eine Variable, die einen Verweis auf ein Objekt enthält. Beispielsweise ist objCustomObject eine Variable, die auf ein Objekt vom Typ CustomObject zeigt:  
  
ist eine Variable, die auf ein Objekt vom Typ CustomObject zeigt:  
  
Set objCustomObject = CreateObject(adodb. Recordset)

**ODBC (Open Database Connectivity)**

Eine Standardmäßige Programmiersprachenschnittstelle, die zum Herstellen einer Verbindung mit einer Vielzahl von Datenquellen verwendet wird. Dieser Zugriff erfolgt in der Regel über die Systemsteuerung, in der Datenquellennamen (Data Source Names, DSNs) zugewiesen werden können, um bestimmte ODBC-Treiber zu verwenden.

**OLE DB**

Eine Reihe von Schnittstellen, die Daten aus einer Vielzahl von Quellen mithilfe von COM verfügbar machen. OLE DB-Schnittstellen bieten Anwendungen einen einheitlichen Zugriff auf Daten, die in verschiedenen Informationsquellen gespeichert sind. Diese Schnittstellen unterstützen die Menge der dbms-Funktionalität, die für die Datenquelle geeignet ist, sodass sie ihre Daten freigeben kann. Siehe auch **COM**.

**Optimistische Sperre**

Ein Sperrtyp, bei dem die Datenseite mit einem oder mehreren Datensätzen, einschließlich des zu bearbeitenden Datensatzes, für andere Benutzer nur während der Aktualisierung des Datensatzes durch die **Update-Methode** nicht verfügbar ist, aber vor und nach dem Aufruf von **Update** verfügbar ist.

Die optimistische Sperrung wird verwendet, wenn das **Recordset** -Objekt geöffnet wird, wobei der **LockType-Parameter** oder die Eigenschaft auf **"adLockOptimistic"** oder **"adLockBatchOptimistic"** festgelegt ist. Siehe auch **pessimistisches Sperren.**

**Ordinalwert**

Die numerische Position eines Elements innerhalb einer Bestellung. In einer ADO-Auflistung ist der Ordnungswert des ersten Elements null (0). Das nächste Element ist eins (1) usw.

Zurück zum Seitenanfang

## <a name="p"></a>P

**parametrisierten Befehl**

Eine Abfrage oder ein Befehl, mit dem Sie Parameterwerte festlegen können, bevor der Befehl ausgeführt wird. Beispielsweise kann eine SQL Zeichenfolge parametrisiert werden, indem Parametermarkierungen in die SQL Zeichenfolge eingebettet werden (durch das Zeichen '?' festgelegt). Die Anwendung gibt dann Werte für jeden Parameter an und führt den Befehl aus.

**übergeordnetes Element**

Die steuerungsseitige Seite einer hierarchischen Beziehung. In einer hierarchischen Struktur weist ein übergeordnetes Element einen oder mehrere untergeordnete Knoten direkt darunter in der Hierarchie auf. Siehe auch **parent-alias**, **parent-child relationship**, **child**.

**parent-alias**

Ein Alias, der auf das übergeordnete Element verweist. Siehe auch **Alias**, **übergeordnetes** Element.

**Beziehung zwischen übergeordneten und untergeordneten Elementen**

Eine Beziehung in einer hierarchischen Struktur, in der das übergeordnete Element eine Ebene höher ist und direkt einem oder mehreren untergeordneten Elementen zugeordnet ist. Ein untergeordnetes Element ist eine Ebene niedriger und muss über ein übergeordnetes Element verfügen. Siehe auch **übergeordnetes**, **untergeordnetes**.

**Beibehalten**

So speichern Sie Daten in einem permanenten Zustand, z. B. beim Speichern eines **Recordset-Objekts** in einer Datei.

**pessimistisches Sperren**

Ein Sperrtyp, bei dem die Seite mit einem oder mehreren Datensätzen, einschließlich des zu bearbeitenden Datensatzes, für andere Benutzer nicht verfügbar ist, um sicherzustellen, dass eine Aktualisierung vorgenommen wird. Das pessimistische Sperrverhalten wird vom OLE DB-Anbieter definiert. In der Regel werden Datensätze beim Bearbeiten gesperrt und bleiben nicht verfügbar, bis die **Update-Methode** abgeschlossen ist.

Die pessimistische Sperrung ist aktiviert, wenn das **Recordset** -Objekt geöffnet wird, wobei der **LockType-Parameter** oder die Eigenschaft auf **adLockPessimistic** festgelegt ist. Siehe auch **optimistische Sperre.**

**Pooling**

Eine Leistungsoptimierung basierend auf der Verwendung von Sammlungen vorab zugewiesener Ressourcen, z. B. Objekte oder Datenbankverbindungen. Es ist effizienter, eine vorhandene Ressource aus dem Pool zu zeichnen, als eine neue Ressource zu erstellen.

**ProgID (programmgesteuerte ID)**

Ein eindeutiger Name, der der Windows Registrierung durch eine COM-Anwendung zugeordnet ist. Die ProgID für eine ADO-Verbindung lautet "ADODB. Connection". Siehe auch **CLSID**, **COM**.

**Proxy**

Ein schnittstellenspezifisches Objekt, das das Marshalling von Parametern und die Kommunikation bereitstellt, die ein Client benötigt, um ein Anwendungsobjekt aufzurufen, das in einer anderen Ausführungsumgebung ausgeführt wird, z. B. in einem anderen Thread oder in einem anderen Prozess. Der Proxy befindet sich beim Client und kommuniziert mit einem entsprechenden Stub, der sich mit dem aufgerufenen Anwendungsobjekt befindet. Siehe auch **Stub**.

Zurück zum Seitenanfang

## <a name="r"></a>R

**Relative URL**

Eine teilweise qualifizierte URL, die eine Ressource im Internet oder in einem Intranet angibt, deren Speicherort relativ zu einem Anfangspunkt ist, der durch eine absolute URL oder ein entsprechendes ADO Connection-Objekt angegeben wird. Tatsächlich enthalten die verketteten absoluten und relativen URLs eine vollständige URL. Siehe auch **URL** und **absolute URL.**

**Remotedatenquelle**

Eine Datenquelle, die auf einem anderen Computer und nicht auf dem lokalen System (auf dem die Clientanwendung ausgeführt wird) vorhanden ist.

**Ressourcendatensatz**

Ein Datensatz von einem Dokumentquellanbieter, der Felder für die Definition und Beschreibung eines Ordners oder Dokuments enthält. Das Dokument selbst ist nicht im Ressourcendatensatz enthalten, kann aber in der Regel über den Standarddatenstrom oder ein Feld im Ressourcendatensatz, der eine URL enthält, aufgerufen werden. Siehe auch **Dokumentquellanbieter**, **Standarddatenstrom**, **URL**.

**root**

Die oberste Ebene in einer hierarchischen Struktur. Der Stammknoten hat keine untergeordneten Elemente, aber möglicherweise untergeordnete Elemente. Siehe auch **Hierarchie**, **Struktur**, **übergeordnete**, **untergeordnete**.

**Rowset**

Eine Gruppe von Zeilen aus einer Datenquelle, die alle das gleiche Feldschema aufweisen. Ein Rowset kann alle oder einige Felder aus einer Tabelle darstellen. Ein Rowset kann auch eine virtuelle Tabelle darstellen, die durch eine Abfrage oder eine Verknüpfung von mindestens zwei Tabellen erstellt wird. In ADO werden Rowsets durch **Recordset-Objekte** dargestellt.

Zurück zum Seitenanfang

## <a name="s"></a>S

**schema**

Eine Beschreibung einer Datenbank für das Datenbankverwaltungssystem (DBMS), die in der Regel mithilfe der vom DBMS bereitgestellten Datendefinitionssprache generiert wird. Ein Schema definiert Attribute der Datenbank, z. B. Tabellen, Spalten und Eigenschaften.

**scope**

Der Bezugsbereich für ein Objekt oder eine Variable oder einen Datensatzbereich in einer Ansicht oder Tabelle. Auf lokale Variablen kann beispielsweise nur innerhalb der Prozedur verwiesen werden, in der sie definiert wurden. Auf öffentliche Variablen kann von überall in der Anwendung aus zugegriffen werden. Objekte, z. B. die aktuelle Datenbank, befinden sich im Bereich, wenn sie sich im definierten Suchpfad befinden. Datensatzbereiche können mit einer Scope-Klausel in vielen Befehlen angegeben werden.

**Dienstleister**

Software, die einen Dienst kapselt, indem Daten erzeugt und verbraucht werden, wodurch Features in Ihren ADO-Anwendungen erweitert werden. Es handelt sich um einen Anbieter, der daten nicht direkt verfügbar macht, sondern einen Dienst bereitstellt, z. B. die Abfrageverarbeitung. Der Dienstanbieter kann Daten verarbeiten, die von einem Datenanbieter bereitgestellt werden. Siehe auch **Datenanbieter**.

**Formiertes Recordset**

Ein **Recordset-Objekt,** dessen Spalten speziell so definiert wurden, dass sie nicht nur Daten enthalten, sondern auch Verweise (kapitelweise bezeichnet) auf andere **Recordset-Objekte** und/oder berechnete Werte, die auf anderen **Recordset-Objekten** basieren.

**Geschwister**

Alle zwei oder mehr Knoten in einer hierarchischen Struktur, die sich auf derselben Ebene in der Hierarchie befinden. Der Stammknoten in einer Hierarchie hat keine gleichgeordneten Knoten.

**Gespeicherte Prozedur**

Eine vorkompilierte Sammlung von Code, z. B. SQL Anweisungen und optionalen Steuerelement-of-Flow-Anweisungen, die unter einem Namen gespeichert und als Einheit verarbeitet werden. Gespeicherte Prozeduren werden in einer Datenbank gespeichert. Sie können mit einem Aufruf von einer Anwendung ausgeführt werden und vom Benutzer deklarierte Variablen, bedingte Ausführung und andere leistungsstarke Programmierfeatures zulassen.

**Stub**

Ein schnittstellenspezifisches Objekt, das das Marshalling und die Kommunikation von Parametern bereitstellt, die erforderlich sind, damit ein Anwendungsobjekt Aufrufe von einem Client empfängt, der in einer anderen Ausführungsumgebung ausgeführt wird, z. B. in einem anderen Thread oder in einem anderen Prozess. Der Stub befindet sich mit dem Anwendungsobjekt und kommuniziert mit einem entsprechenden Proxy, der sich mit dem Client befindet, der ihn aufruft. Siehe auch **Proxy**.

**Unterknoten**

Siehe **untergeordnetes** Element.

**synchroner Vorgang**

Ein durch Code initiierter Vorgang, der vor dem nächsten Vorgang abgeschlossen wird. Siehe auch **asynchrone Operation.**

Zurück zum Seitenanfang

## <a name="t-w"></a>T-W

**Baum**

Eine Struktur, die eine hierarchische Beziehung zwischen Elementen (Knoten) darstellt. Es gibt einen Knoten auf der obersten Ebene einer Struktur (dem Stamm). Unterhalb des Stamms können mehrere untergeordnete Elemente vorhanden sein. Jedes untergeordnete Element kann wiederum das übergeordnete Element anderer untergeordneter Elemente sein und somit wie eine Struktur verzweigt werden. Ein Ordner mit Dokumenten und anderen Ordnern ist ein typisches Beispiel für eine Strukturstruktur. Siehe auch **Hierarchie**, **Knoten**, **Stamm**, **untergeordnete**, **übergeordnete**.

**URL (Uniform Resource Locator)**

Gibt den Speicherort einer Ressource an, die sich im Internet oder in einem Intranet befindet. Eine vollständige URL besteht aus einem Schema (z. B. FTP, HTTP, Mailto, Datei usw.), gefolgt von einem Doppelpunkt, einem Servernamen und dem vollständigen Pfad einer Ressource (z. B. einem Dokument, einer Grafik oder einer anderen Datei). Beispiele für URLs sind:  
  
- https://www.domain.com/default.html  
- ftp://ftp.server.somewhere/ftp.file  
  
- ftp://ftp.server.somewhere/ftp.file  
- file://Server/Share/File.doc

Siehe auch **absolute URL** und **relative URL.**

**Webserver**

Ein Computer, der Webdienste und Seiten für Intranet- und Internetbenutzer bereitstellt.



