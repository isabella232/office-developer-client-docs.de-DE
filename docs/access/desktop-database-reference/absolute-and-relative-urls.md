---
<<<<<<< HEAD-Titel: Absolute und Relative URLs TOCTitle: Absolute und Relative URLs Ms:assetid: 79a1f793-7154-1c13-7dfe-a1b8cd64e1ea Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249501(v=office.15) Ms:contentKeyID: 48545774 ms.date: 09/18/2015 Mtps_version: V = Office.15
---

# <a name="absolute-and-relative-urls"></a>Absolute und relative URLs

**Betrifft**: Access 2013 | Office 2013 

Eine URL gibt den Speicherort eines auf einem lokalen oder vernetzten Computer gespeicherten Ziels an, z. B. eine Datei, ein Verzeichnis, eine HTML-Seite, ein Bild, ein Programm usw.** In dieser Diskussion hat eine *absolute URL* dieses Format:
=======
Titel: Absolute und relative URLs TOCTitle: Absolute und relative URLs Ms:assetid: 79a1f793-7154-1c13-7dfe-a1b8cd64e1ea Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249501(v=office.15) Ms:contentKeyID: 48545774 ms.date: 10/17/2018 Mtps_version: Office. 15
---

# <a name="absolute-and-relative-urls"></a>Absolute und relative URLs

**Betrifft**: Access 2013 | Office 2013 

Eine URL gibt den Speicherort eines Ziels auf einem lokalen Computer oder Netzwerkcomputer, wie ein Datei-, Verzeichnis-, HTML-Seite, Bild, Programm, und So weiter gespeichert. In dieser Erläuterung hat eine *absolute URL* Folgendes Format:
>>>>>>> master

*Schema://Server/Pfad/Ressource*

Dabei gilt Folgendes:

<<<<<<< Kopf
  - *Schema*

  - Gibt an, wie die *Ressource* zugegriffen werden.

  - *Server*

  - Gibt den Namen des Computers, auf dem die *Ressource* befindet.

  - *Pfad*

  - Die Sequenz der zum Ziel führenden Verzeichnisse wird angegeben. Wenn *Ressource* weggelassen wird, ist das Ziel das letzte Verzeichnis im *Pfad*.

  - *Ressource*

  - Wenn enthalten, *Ressource* ist das Ziel und ist in der Regel der Name einer Datei. Es kann eine *einfache Datei* , die einen einzelnen binären Stream von Bytes oder ein *strukturiertes Dokument* , enthält einen Speicher und binären enthält sein.
=======
|Name |Beschreibung|
|:----|:----------|
|*Schema*|Gibt an, wie die *Ressource* zugegriffen werden.|
|*Server*|Gibt den Namen des Computers, auf dem die *Ressource* befindet.|
|*Pfad*|Die Sequenz der zum Ziel führenden Verzeichnisse wird angegeben. Wenn *Ressource* weggelassen wird, ist das Ziel das letzte Verzeichnis im *Pfad*.|
|*Ressource*|Wenn enthalten, *Ressource* ist das Ziel und ist in der Regel der Name einer Datei. Es kann eine *einfache Datei*, mit einer einzigen binären Stream von Bytes oder ein *strukturiertes Dokument*mit einer speichern und binären sein.|
>>>>>>> master

Eine *absolute URL* enthält alle Informationen zum Suchen einer Ressource.

Durch eine *relative URL* wird eine Ressource mithilfe einer absoluten URL als Ausgangspunkt gesucht. Tatsächlich wird die "vollständige URL" des Ziels durch Verketten der absoluten und relativen URLs angegeben. Eine relative URL besteht normalerweise nur aus dem *Pfad* und optional aus der *Ressource*, enthält jedoch kein *Schema* und keinen *Server*.

<<<<<<< Kopf
## <a name="url-scheme-registration"></a>URL-Schemaregistrierung

Wenn von einem Anbieter URLs unterstützt werden, wird mindestens ein URL-Schema für den Anbieter registriert. Das heißt, dass durch alle URLs, in denen dieses Schema verwendet wird, automatisch der registrierte Anbieter aufgerufen wird. Beispielsweise ist das *http-* Schema für den [Microsoft OLE DB-Anbieter für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)registriert. In ADO wird davon ausgegangen, dass alle URLs mit dem Präfix "http" Webordner oder mit dem Internet Publishing-Anbieter zu verwendende Dateien darstellen. Weitere Informationen zu den für den Anbieter registrierten Schemas finden Sie in der Anbieterdokumentation.

## <a name="defining-context-with-a-url"></a>Definieren von Kontext mit einer URL
=======
## <a name="url-scheme-registration"></a>URL-schemaregistrierung

Wenn von einem Anbieter URLs unterstützt werden, wird mindestens ein URL-Schema für den Anbieter registriert. Das heißt, dass durch alle URLs, in denen dieses Schema verwendet wird, automatisch der registrierte Anbieter aufgerufen wird. Beispielsweise ist das *http-* Schema für den [Microsoft OLE DB-Anbieter für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)registriert. ADO wird davon ausgegangen, dass alle URLs mit dem Präfix "http" Webordner oder Dateien mit dem Internet Publishing-Anbieter darstellen. Weitere Informationen zu den für den Anbieter registrierten Schemas finden Sie in der Anbieterdokumentation.

## <a name="defining-context-with-a-url"></a>Definieren von Kontext mit einer URL
>>>>>>> master

Eine Funktion einer geöffneten Verbindung, die durch ein [Connection](connection-object-ado.md)-Objekt dargestellt wird, ist die Einschränkung nachfolgender Operationen auf die durch diese Verbindung dargestellte Datenquelle. Das heißt, der Kontext für nachfolgende Operationen wird durch die Verbindung definiert.

Mit ADO 2.5 kann ein Kontext auch durch eine absolute URL definiert werden. Wenn z. B. ein [Record](record-object-ado.md)-Objekt mit einer absoluten URL geöffnet wird, wird implizit ein **Connection** -Objekt erstellt, das die durch die URL angegebene Ressource darstellt.

<<<<<<< Eine absolute URL, die ein Kontext definiert werden, in der *ActiveConnection* -Parameter des **Datensatzes angegeben kann** HEAD-Objekts [Open](open-method-ado-record.md) -Methode. Eine absolute URL kann auch angegeben werden, als der Wert der neuen "URL**=**"-Schlüsselwort in der **Connection** -Objekt-Parameter *ConnectionString* [Open](open-method-ado-connection.md) -Methode und der [Open](open-method-ado-recordset.md) -Methode *ActiveConnection für das [Recordset](recordset-object-ado.md) -Objekt *Parameter.

Der Kontext kann auch durch ein geöffnetes **Record** - oder **Recordset** -Objekt, das ein Verzeichnis darstellt, definiert werden, da diese Objekte bereits über ein implizit oder explizit deklariertes **Connection** -Objekt verfügen, durch das der Kontext angegeben wird.

## <a name="scoped-operations"></a>Bereichsvorgänge

Der Kontext definiert einen *Bereich* gleichzeitig – d. h., des Verzeichnisses und seiner Unterverzeichnisse, die in den folgenden Vorgängen beteiligt sein können. Das **Record** -Objekt verfügt über mehrere bereichsbezogenen Methoden, einschließlich [CopyRecord](copyrecord-method-ado.md), [DeleteRecord](https://msdn.microsoft.com/library/jj249832\(v=office.15\)), und [MoveRecord](moverecord-method-ado.md), die auf ein Verzeichnis und alle Unterverzeichnisse ausgeführt werden.

## <a name="relative-urls-as-command-text"></a>Relative URLs als Befehlstext
=== Eine absolute URL, die definiert einen Kontext kann in der *ActiveConnection* -Parameter der [Open](open-method-ado-record.md) -Methode des **Record** -Objekts angegeben werden. Eine absolute URL kann auch angegeben werden, als der Wert des neuen `URL=` Schlüsselwort in der **Connection** -Objekt-Parameter *ConnectionString* [Open](open-method-ado-connection.md) -Methode und der [Open](open-method-ado-recordset.md) -Methode *ActiveConnection* für das [Recordset](recordset-object-ado.md) -Objekt der Parameter.

Der Kontext kann auch durch ein geöffnetes **Record** - oder **Recordset** -Objekt, das ein Verzeichnis darstellt, definiert werden, da diese Objekte bereits über ein implizit oder explizit deklariertes **Connection** -Objekt verfügen, durch das der Kontext angegeben wird.

## <a name="scoped-operations"></a>Bereichsvorgänge

Der Kontext definiert einen *Bereich*gleichzeitig – d. h., des Verzeichnisses und seiner Unterverzeichnisse, die in den folgenden Vorgängen beteiligt sein können. Das **Record** -Objekt verfügt über mehrere bereichsbezogenen Methoden, einschließlich [CopyRecord](copyrecord-method-ado.md), [DeleteRecord](deleterecord-method-ado.md), und [MoveRecord](moverecord-method-ado.md), die auf ein Verzeichnis und alle Unterverzeichnisse ausgeführt werden.

## <a name="relative-urls-as-command-text"></a>Relative URLs als Befehlstext
>>>>>>> master

In der **Connection** -Objekt **Execute** -Methode *CommandText* -Parameter und der **Recordset** -Objekt **Open** -Methode *Source* -Parameter kann eine Zeichenfolge zur Angabe eines für die Datenquelle auszuführender Befehls angegeben werden.

Eine relative URL kann im *CommandText* oder *Source* -Parameter angegeben werden. Die relative URL gibt keine tatsächlich einen Befehl (beispielsweise einen SQL-Befehl); Es wird lediglich in diesen Parametern angegeben. Darüber hinaus muss im Kontext der aktiven Verbindung eine absolute URL sein, und der *Option* -Parameter muss auf **AdCmdTableDirect**festgelegt sein.

Beispielsweise kann ein Recordset-Objekt wie folgt für die Datei Readme25.txt im Verzeichnis Winnt/system32 geöffnet werden:

```vb
recordset.Open "system32/Readme25.txt", "URL=https://YourServer/Winnt/",,,adCmdTableDirect 
```

<<<<<<< HEAD die absolute URL in der Verbindungszeichenfolge gibt den Server (YourServer) und der Pfad () und den Pfad (Winnt). Durch diese URL wird auch der Kontext definiert.

Die relative URL im Befehlstext wird die absolute URL als Ausgangspunkt und der restliche Pfad (system32) und die Datei zu öffnen () und die Datei (Readme25.txt) geöffnet.

<a name="the-options-field--indicates-that-the-command-type-is-a-relative-url"></a>Das Feld (Optionen) gibt an, dass der Befehlstyp eine relative URL ist.
=======
Die absolute URL in der Verbindungszeichenfolge gibt den Server (YourServer) und den Pfad (Winnt). Durch diese URL wird auch der Kontext definiert.

Die relative URL im Befehlstext wird die absolute URL als Ausgangspunkt und der restliche Pfad (system32) und die Datei (Readme25.txt) geöffnet.

Das Feld "Optionen" gibt an, dass der Befehlstyp eine relative URL ist.
>>>>>>> master

Als weiteres Beispiel wird mit dem folgende Code ein **Recordset-Objekt** auf den Inhalt des Verzeichnisses geöffnet:

```vb
recordset.Open "", "URL=https://YourServer/Winnt/",,,adCmdTableDirect 
```

<<<<<<< Kopf
## <a name="ole-db-provider-supplied-url-schemes"></a>Vom OLE DB-Anbieter bereitgestellte URL-Schemas

Vorderer Teil der eine voll qualifizierte URL wird das *Schema* verwendet, um die durch den Rest der URL angegebene Ressource zugreifen. Beispiele sind HTTP (HyperText Transfer Protocol) und FTP (File Transfer Protocol).

In ADO werden OLE DB-Anbieter unterstützt, von denen die eigenen URL-Schemas erkannt werden. Beispielsweise wird vom [Microsoft OLE DB-Anbieter für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)*,* durch den auf "veröffentlichte" Windows 2000-Dateien zugegriffen wird, das vorhandene HTTP-Schema erkannt.
=======
## <a name="ole-db-provider-supplied-url-schemes"></a>OLE DB-Anbieter bereitgestellte URL-Schemas

Vorderer Teil der eine voll qualifizierte URL wird das *Schema* verwendet, um die durch den Rest der URL angegebene Ressource zugreifen. Beispiele sind HTTP (HyperText Transfer Protocol) und FTP (File Transfer Protocol).

In ADO werden OLE DB-Anbieter unterstützt, von denen die eigenen URL-Schemas erkannt werden. Beispielsweise werden von der [Microsoft OLE DB-Anbieter für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md), welche Zugriffe "Windows 2000-Dateien veröffentlicht", das vorhandene HTTP-Schema erkannt.
>>>>>>> master

