---
title: Connection-Elemente (DAO)
TOCTitle: Connection Members
ms:assetid: 94fc60ee-b6f2-cf08-b008-ed51bf7e7f8c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197681(v=office.15)
ms:contentKeyID: 48546422
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: df81fc1fe146832799d8af3b02c13ce8df65d5a7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597585"
---
# <a name="connection-members-dao"></a>Connection-Elemente (DAO)

**Gilt für**: Access 2013, Office 2013

> [!NOTE]
> [!HINWEIS] ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden. Bei einem Connection-Objekt handelt es sich um eine Verbindung mit einer ODBC-Datenbank (gilt nur für ODBCDirect-Arbeitsbereiche).
 
## <a name="methods"></a>Methoden

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong><a href="connection-cancel-method-dao.md">Cancel</a></strong></p></td>
<td><p>Die Ausführung eines ausstehenden asynchronen Methodenaufrufs wird abgebrochen (gilt nur für ODBCDirect-Arbeitsbereiche).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="connection-close-method-dao.md">Close</a></strong></p></td>
<td><p>Schließt ein geöffnetes <strong>Connection</strong>-Objekt.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="connection-createquerydef-method-dao.md">CreateQueryDef</a></strong></p></td>
<td><p>Erstellt ein neues <strong><a href="querydef-object-dao.md">QueryDef</a></strong>-Objekt.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="connection-execute-method-dao.md">Execute</a></strong></p></td>
<td><p>Führt eine Aktionsabfrage oder eine SQL-Anweisung für das angegebene Objekt aus.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="connection-openrecordset-method-dao.md">OpenRecordset</a></strong></p></td>
<td><p>Erstellt ein neues <strong><a href="recordset-object-dao.md">Recordset</a></strong>-Objekt und fügt es an die <strong>Recordsets</strong>-Auflistung an.</p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a>Eigenschaften

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong><a href="connection-connect-property-dao.md">Verbinden</a></strong></p></td>
<td><p>Legt einen Wert fest, der Informationen zur Quelle einer geöffneten Verbindung bereitstellt, oder gibt den Wert zurück. <strong>String</strong>-Wert mit Lese-/Schreibzugriff.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="connection-database-property-dao.md">Datenbank</a></strong></p></td>
<td><p>Gibt das <strong><a href="database-object-dao.md">Database-Objekt</a></strong> zurück, das dieser Verbindung entspricht (gilt nur für ODBCDirect-Arbeitsbereiche).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="connection-name-property-dao.md">Name</a></strong></p></td>
<td><p>Gibt den Namen eines <strong><a href="connection-object-dao.md">Connection</a></strong> -Objekts zurück.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="connection-querydefs-property-dao.md">QueryDefs</a></strong></p></td>
<td><p>Gibt eine <strong>QueryDefs</strong>-Auflistung zurück, die alle <strong>QueryDef</strong>-Objekte der angegebenen Verbindung enthält. Schreibgeschützt.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="connection-querytimeout-property-dao.md">Querytimeout</a></strong></p></td>
<td><p>Mit dieser Eigenschaft wird ein Wert festgelegt oder zurückgegeben, der angibt, wie viele Sekunden beim Ausführen einer Abfrage zu einer ODBC-Datenquelle gewartet wird, bevor ein Timeoutfehler auftritt.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="connection-recordsaffected-property-dao.md">RecordsAffected</a></strong></p></td>
<td><p>Gibt die Anzahl der Datensätze zurück, die von der zuletzt aufgerufenen <strong><a href="connection-execute-method-dao.md">Execute</a></strong> -Methode betroffen waren.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="connection-recordsets-property-dao.md">Recordsets</a></strong></p></td>
<td><p>Gibt eine <strong>Recordsets</strong>-Auflistung zurück, die alle geöffneten Recordsets für die angegebene Verbindung enthält. Schreibgeschützt.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="connection-stillexecuting-property-dao.md">StillExecuting</a></strong></p></td>
<td><p>Gibt an, ob ein asynchroner Vorgang (d. h. eine Methode, die mit der <strong>dbRunAsync</strong>-Option aufgerufen wurde) abgeschlossen wurde (nur ODBCDirect-Arbeitsbereiche).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="connection-transactions-property-dao.md">Transactions</a></strong></p></td>
<td><p>Gibt einen Wert zurück, der angibt, ob ein Objekt Transaktionen unterstützt. Schreibgeschützter <strong>Boolean</strong>-Wert.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="connection-updatable-property-dao.md">Updatable</a></strong></p></td>
<td><p>Gibt einen Wert zurück, der anzeigt, ob ein DAO-Objekt geändert werden kann. Schreibgeschützter <strong>Boolean</strong>-Wert.</p></td>
</tr>
</tbody>
</table>

