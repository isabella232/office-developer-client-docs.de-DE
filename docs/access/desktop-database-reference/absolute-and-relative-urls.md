---
title: Absolute und relative URLs
TOCTitle: Absolute and relative URLs
ms:assetid: 79a1f793-7154-1c13-7dfe-a1b8cd64e1ea
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249501(v=office.15)
ms:contentKeyID: 48545774
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a488617dc7ba0d7d1f7e38391f8382fa1e7ed247
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282101"
---
# <a name="absolute-and-relative-urls"></a>Absolute und relative URLs

**Gilt für**: Access 2013, Office 2013    

Eine URL gibt den Speicherort eines auf einem lokalen oder vernetzten Computer gespeicherten Ziels an, z. B. eine Datei, ein Verzeichnis, eine HTML-Seite, ein Bild, ein Programm usw. In dieser Diskussion hat eine *absolute URL* folgende Form:

*Schema://Server/Pfad/Ressource*

Dabei gilt Folgendes:

|Name |Beschreibung|
|:----|:----------|
|*Schema*|Es wird angegeben, wie auf die *Ressource* zugegriffen werden soll.|
|*server*|Der Name des Computers, auf dem sich die *Ressource* befindet, wird angegeben.|
|*Pfad*|Die Sequenz der zum Ziel führenden Verzeichnisse wird angegeben. Wenn *Ressource* weggelassen wird, ist das Ziel das letzte Verzeichnis im *Pfad*.|
|*resource*|Wenn die *Ressource* enthalten ist, ist sie das Ziel (normalerweise der Name einer Datei). Es kann sich um eine *einfache Datei*handeln, die einen einzelnen binären Byte-Datenstrom enthält, oder ein *strukturiertes Dokument*, das mindestens einen Speicher und binäre Byte-Streams enthält.|

Eine *absolute URL* enthält alle Informationen, die zum Suchen einer Ressource notwendig sind.

Durch eine *relative URL* wird eine Ressource mithilfe einer absoluten URL als Ausgangspunkt gesucht. Tatsächlich wird die "vollständige URL" des Ziels durch Verketten der absoluten und relativen URLs angegeben. Eine relative URL besteht normalerweise nur aus dem *Pfad* und optional aus der *Ressource*, enthält jedoch kein *Schema* und keinen *Server*.

## <a name="url-scheme-registration"></a>URL-Schemaregistrierung

Wenn von einem Anbieter URLs unterstützt werden, wird mindestens ein URL-Schema für den Anbieter registriert. Das heißt, dass durch alle URLs, in denen dieses Schema verwendet wird, automatisch der registrierte Anbieter aufgerufen wird. Beispielsweise ist das Schema *http* für den [Microsoft OLE DB-Anbieter für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) registriert. ADO geht davon aus, dass alle URLs mit dem Präfix "http" Webordner oder Dateien darstellen, die mit dem Internet Publishing-Anbieter verwendet werden sollen. Weitere Informationen zu den für den Anbieter registrierten Schemas finden Sie in der Anbieterdokumentation.

## <a name="defining-context-with-a-url"></a>Definieren des Kontexts mit einer URL

Eine Funktion einer geöffneten Verbindung, die durch ein [Connection](connection-object-ado.md)-Objekt dargestellt wird, ist die Einschränkung nachfolgender Operationen auf die durch diese Verbindung dargestellte Datenquelle. Das heißt, der Kontext für nachfolgende Operationen wird durch die Verbindung definiert.

Mit ADO 2.5 kann ein Kontext auch durch eine absolute URL definiert werden. Wenn z. B. ein [Record](record-object-ado.md)-Objekt mit einer absoluten URL geöffnet wird, wird implizit ein **Connection** -Objekt erstellt, das die durch die URL angegebene Ressource darstellt.

Eine absolute URL, durch die ein Kontext definiert wird, kann im *ActiveConnection*-Parameter der [Open](open-method-ado-record.md)-Methode des **Record**-Objekts angegeben werden. Eine absolute `URL=` URL kann auch als Wert des Schlüsselwortes New im **Connection** -Objekt [Open](open-method-ado-connection.md) -Methode *ConnectionString* -Parameter und die [Open](open-method-ado-recordset.md) -Methode des [Recordset](recordset-object-ado.md) -Objekts *ActiveConnection* Parameter.

Der Kontext kann auch durch ein geöffnetes **Record** - oder **Recordset** -Objekt, das ein Verzeichnis darstellt, definiert werden, da diese Objekte bereits über ein implizit oder explizit deklariertes **Connection** -Objekt verfügen, durch das der Kontext angegeben wird.

## <a name="scoped-operations"></a>Bereichsbezogene Vorgänge

Der Kontext definiert gleichzeitig einen *Bereich*, also das Verzeichnis und dessen Unterverzeichnisse, die an nachfolgenden Vorgängen teilnehmen können. Das **Record** -Objekt verfügt über mehrere bereichsbezogene Methoden, einschließlich [CopyRecord](copyrecord-method-ado.md), [MoveRecord](moverecord-method-ado.md)und [DeleteRecord](deleterecord-method-ado.md), die für ein Verzeichnis und alle zugehörigen Unterverzeichnisse ausgeführt werden.

## <a name="relative-urls-as-command-text"></a>Relative URLs als Befehlstext

Eine Zeichenfolge, durch die ein für die Datenquelle auszuführender Befehl angegeben wird, kann im *CommandText*-Parameter der **Execute**-Methode des **Connection**-Objekts und im *Source*-Parameter der **Open**-Methode des **Recordset**-Objekts angegeben werden.

Eine relative URL kann im Parameter *CommandText* oder *Source* angegeben werden. Durch die relative URL wird nicht wirklich ein Befehl (z. B. ein SQL-Befehl) angegeben; der Befehl wird lediglich in diesen Parametern angegeben. Außerdem muss der Kontext der aktiven Verbindung eine absolute URL sein, und der *Option*-Parameter muss auf **adCmdTableDirect** festgelegt sein.

For example, a **Recordset** could be opened on the Readme25.txt file of the Winnt/system32 directory like this:

```vb
recordset.Open "system32/Readme25.txt", "URL=https://YourServer/Winnt/",,,adCmdTableDirect 
```

Die absolute URL in der Verbindungszeichenfolge gibt den Server (YourServer) und den Pfad (WinNT) an. Durch diese URL wird auch der Kontext definiert.

Die relative URL im Befehlstext verwendet die absolute URL als Ausgangspunkt und gibt den Rest des Pfads (system32) und die zu öffnende Datei an (Readme25. txt).

Das Optionsfeld gibt an, dass der Befehlstyp eine relative URL ist.

Als weiteres Beispiel wird im folgenden Code ein **Recordset** -Objekt für den Inhalt des Verzeichnisses geöffnet:

```vb
recordset.Open "", "URL=https://YourServer/Winnt/",,,adCmdTableDirect 
```

## <a name="ole-db-provider-supplied-url-schemes"></a>Vom OLE DB-Anbieter bereitgestellte URL-Schemas

Der führende Teil einer vollständig qualifizierten URL ist das *Schema*, das für den Zugriff auf die Ressource verwendet wird, die durch den Rest der URL identifiziert wird. Beispiele sind HTTP (HyperText Transfer Protocol) und FTP (File Transfer Protocol).

In ADO werden OLE DB-Anbieter unterstützt, von denen die eigenen URL-Schemas erkannt werden. Beispielsweise wird vom [Microsoft OLE DB-Anbieter für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md), durch den auf "veröffentlichte" Windows 2000-Dateien zugegriffen wird, das vorhandene HTTP-Schema erkannt.

