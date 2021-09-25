---
title: Microsoft OLE DB-Anbieter für Microsoft Active Directory-Dienst
TOCTitle: Microsoft OLE DB Provider for Microsoft Active Directory Service
ms:assetid: 92d1c967-aa61-f3b5-1c0a-301ef236894c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249647(v=office.15)
ms:contentKeyID: 48546385
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 7ea95d40d10823de22b7496615a4fddb3e2860c5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593964"
---
# <a name="microsoft-ole-db-provider-for-microsoft-active-directory-service"></a>Microsoft OLE DB Provider for Microsoft Active Directory Service

**Gilt für**: Access 2013, Office 2013

Mithilfe des Microsoft ADSI-Anbieters (Active Directory Service Interfaces) kann ADO über ADSI eine Verbindung mit heterogenen Verzeichnisdiensten herstellen. Dadurch erlangen ADO-Anwendungen schreibgeschützten Zugriff auf die Verzeichnisdienste von Microsoft Windows NT 4.0 und Microsoft Windows 2000 sowie auf sämtliche LDAP-kompatible Verzeichnisdienste und Novell Directory Services. ADSI selbst basiert auf einem Anbietermodell. Wenn also ein neuer Anbieter Zugriff auf ein anderes Verzeichnis gewährt, kann die ADO-Anwendung problemlos auf dieses Verzeichnis zugreifen. Der ADSI-Anbieter ist ein Freethreadanbieter, der Unicode verwendet.

## <a name="connection-string-parameters"></a>Verbindungszeichenfolgen-Parameter

Um eine Verbindung mit diesem Anbieter herzustellen, legen Sie das **Provider**-Argument der [ConnectionString](connectionstring-property-ado.md)-Eigenschaft fest auf:

```vb 
 
ADSDSOObject 
```

Beim Lesen der [Provider](provider-property-ado.md)-Eigenschaft wird diese Zeichenfolge ebenfalls zurückgegeben.

## <a name="typical-connection-string"></a>Typische Verbindungszeichenfolge

Eine typische Verbindungszeichenfolge für diesen Anbieter lautet:

```vb 
 
"Provider=ADSDSOObject;User ID=userName;Password=userPassword;" 
```

Die Zeichenfolge besteht aus den folgenden Schlüsselwörtern:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Schlüsselwort</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Provider</strong></p></td>
<td><p>Gibt den OLE DB-Anbieter für Microsoft Active Directory-Dienst an.</p></td>
</tr>
<tr class="even">
<td><p><strong>User ID</strong></p></td>
<td><p>Gibt den Benutzernamen an. Wenn dieses Schlüsselwort nicht angegeben ist, werden die aktuellen Anmeldeinformationen verwendet.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Password</strong></p></td>
<td><p>Gibt das Benutzerkennwort an. Wenn dieses Schlüsselwort nicht angegeben ist, werden die aktuellen Anmeldeinformationen verwendet.</p></td>
</tr>
</tbody>
</table>


**Befehlstext**

Eine vierteilige Befehlstextzeichenfolge wird durch den Anbieter in der folgenden Syntax erkannt:

`"Root; Filter; Attributes[; Scope]"`

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Wert</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Root</em></p></td>
<td><p>Gibt das <strong>ADsPath</strong>-Objekt an, von dem aus die Suche gestartet werden soll (d. h. den Stamm der Suche).</p></td>
</tr>
<tr class="even">
<td><p><em>Filter</em></p></td>
<td><p>Gibt den Suchfilter im Format RFC 1960 an.</p></td>
</tr>
<tr class="odd">
<td><p><em>Attributes</em></p></td>
<td><p>Gibt eine Liste mit durch Komma getrennten Attributen an, die zurückgegeben werden sollen.</p></td>
</tr>
<tr class="even">
<td><p><em>Scope</em></p></td>
<td><p>Optional. Eine <strong>Zeichenfolge</strong>, dien den Bereich der Suche angibt. Dies kann eine der folgenden Sein: Base - Nur das Basisobjekt (Stamm der Suche) durchsuchen.<br />
OneLevel – Nur eine Ebene durchsuchen.<br />
Unterstruktur – Durchsuchen Sie die gesamte Unterstruktur.</p></td>
</tr>
</tbody>
</table>


Beispiel:

```vb 
 
"<LDAP://DC=ArcadiaBay,DC=COM>;(objectClass=*);sn, givenName; subtree" 
```

Der Anbieter unterstützt auch SQL SELECT als Befehlstext. Beispiel:

```vb 
 
"SELECT title, telephoneNumber From 'LDAP://DC=Microsoft, DC=COM' WHERE 
objectClass='user' AND objectCategory='Person'" 
```

Der Anbieter akzeptiert weder Aufrufe gespeicherter Prozeduren noch einfache Tabellennamen (die [CommandType](commandtype-property-ado.md)-Eigenschaft lautet beispielsweise immer **adCmdText**). Eine ausführlichere Beschreibung der Befehlstextelemente finden Sie in der Dokumentation zu ADSI (Active Directory Service Interfaces).

## <a name="recordset-behavior"></a>Recordset-Verhalten

In den folgenden Tabellen sind die für ein [Recordset](recordset-object-ado.md)-Objekt verfügbaren Features aufgeführt, das mit diesem Anbieter geöffnet wird. Nur der statische Cursortyp (**adOpenStatic**) ist verfügbar.

Ausführlichere Informationen zum **Recordset** -Verhalten Ihrer Anbieterkonfiguration erhalten Sie, wenn Sie die [Supports](supports-method-ado.md)-Methode ausführen und die [Properties](properties-collection-ado.md) -Auflistung des **Recordset** -Objekts aufzählen, um zu ermitteln, ob anbieterspezifische dynamische Eigenschaften vorhanden sind.

Verfügbarkeit von ADO-Standardeigenschaften des **Recordset**-Objekts:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Eigenschaft</p></th>
<th><p>Verfügbarkeit</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="absolutepage-property-ado.md">AbsolutePage</a></p></td>
<td><p>Lese-/Schreibzugriff</p></td>
</tr>
<tr class="even">
<td><p><a href="absoluteposition-property-ado.md">AbsolutePosition</a></p></td>
<td><p>Lese-/Schreibzugriff</p></td>
</tr>
<tr class="odd">
<td><p><a href="activeconnection-property-ado.md">Activeconnection</a></p></td>
<td><p>Schreibgeschützt</p></td>
</tr>
<tr class="even">
<td><p><a href="bof-eof-properties-ado.md">BOF</a></p></td>
<td><p>Schreibgeschützt</p></td>
</tr>
<tr class="odd">
<td><p><a href="bookmark-property-ado.md">Bookmark</a></p></td>
<td><p>Lese-/Schreibzugriff</p></td>
</tr>
<tr class="even">
<td><p><a href="cachesize-property-ado.md">CacheSize</a></p></td>
<td><p>Lese-/Schreibzugriff</p></td>
</tr>
<tr class="odd">
<td><p><a href="cursorlocation-property-ado.md">CursorLocation</a></p></td>
<td><p>immer <strong>adUseServer</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="cursortype-property-ado.md">Cursortype</a></p></td>
<td><p>immer <strong>adOpenStatic</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="editmode-property-ado.md">EditMode</a></p></td>
<td><p>immer <strong>adEditNone</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="bof-eof-properties-ado.md">EOF</a></p></td>
<td><p>Schreibgeschützt</p></td>
</tr>
<tr class="odd">
<td><p><a href="filter-property-ado.md">Filter</a></p></td>
<td><p>Lese-/Schreibzugriff</p></td>
</tr>
<tr class="even">
<td><p><a href="locktype-property-ado.md">LockType</a></p></td>
<td><p>Lese-/Schreibzugriff</p></td>
</tr>
<tr class="odd">
<td><p><a href="marshaloptions-property-ado.md">MarshalOptions</a></p></td>
<td><p>nicht verfügbar</p></td>
</tr>
<tr class="even">
<td><p><a href="maxrecords-property-ado.md">MaxRecords</a></p></td>
<td><p>Lese-/Schreibzugriff</p></td>
</tr>
<tr class="odd">
<td><p><a href="pagecount-property-ado.md">PageCount</a></p></td>
<td><p>Schreibgeschützt</p></td>
</tr>
<tr class="even">
<td><p><a href="pagesize-property-ado.md">PageSize</a></p></td>
<td><p>Lese-/Schreibzugriff</p></td>
</tr>
<tr class="odd">
<td><p><a href="recordcount-property-ado.md">RecordCount</a></p></td>
<td><p>Schreibgeschützt</p></td>
</tr>
<tr class="even">
<td><p><a href="source-property-ado-recordset.md">Source</a></p></td>
<td><p>Lese-/Schreibzugriff</p></td>
</tr>
<tr class="odd">
<td><p><a href="state-property-ado.md">State</a></p></td>
<td><p>Schreibgeschützt</p></td>
</tr>
<tr class="even">
<td><p><a href="status-property-ado-recordset.md">Status</a></p></td>
<td><p>Schreibgeschützt</p></td>
</tr>
</tbody>
</table>


Verfügbarkeit von ADO-Standardmethoden des **Recordset**-Objekts:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Methode</p></th>
<th><p>Verfügbar?</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="addnew-method-ado.md">AddNew</a></p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p><a href="cancel-method-ado.md">Cancel</a></p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p><a href="cancelbatch-method-ado.md">CancelBatch</a></p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p><a href="cancelupdate-method-ado.md">CancelUpdate</a></p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p><a href="clone-method-ado.md">Clone</a></p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p><a href="close-method-ado.md">Schließen</a></p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p><a href="delete-method-ado-recordset.md">Löschen</a></p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p><a href="getrows-method-ado.md">GetRows</a></p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p><a href="move-method-ado.md">Move</a></p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p><a href="nextrecordset-method-ado.md">NextRecordset</a></p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p><a href="open-method-ado-recordset.md">Öffnen</a></p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p><a href="requery-method-ado.md">Requery</a></p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p><a href="resync-method-ado.md">Resync</a></p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p><a href="supports-method-ado.md">Unterstützt</a></p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p><a href="update-method-ado.md">Update</a></p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p><a href="updatebatch-method-ado.md">UpdateBatch</a></p></td>
<td><p>Nein</p></td>
</tr>
</tbody>
</table>

