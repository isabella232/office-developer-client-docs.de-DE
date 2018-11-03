---
title: QueryDef-Member (DAO)
TOCTitle: QueryDef Members
ms:assetid: 3f914d23-aa63-3ebd-1d86-4f53da71131b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192855(v=office.15)
ms:contentKeyID: 48544403
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 84f8be8360996eb209462347dc18b118cf460442
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937617"
---
# <a name="querydef-members-dao"></a>QueryDef-Member (DAO)


**Betrifft**: Access 2013, Office 2013

Ein QueryDef -Objekt ist eine gespeicherte Definition einer Abfrage in einer Datenbank des Microsoft Access-Datenbankmoduls.

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
<td><p><strong><a href="querydef-cancel-method-dao.md">Abbrechen</a></strong></p></td>
<td><p></p>

> [!NOTE]
> [!HINWEIS] ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.


<p>Die Ausführung eines ausstehenden asynchronen Methodenaufrufs wird abgebrochen (gilt nur für ODBCDirect-Arbeitsbereiche).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="querydef-close-method-dao.md">Schließen Sie</a></strong></p></td>
<td><p>Schließt ein geöffnetes <strong>QueryDef</strong>-Objekt.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="querydef-createproperty-method-dao.md">CreateProperty</a></strong></p></td>
<td><p>Erstellt ein neues, benutzerdefiniertes <strong><a href="property-object-dao.md">Property</a></strong> -Objekt (gilt nur für Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="querydef-execute-method-dao.md">Ausführen</a></strong></p></td>
<td><p>Führt eine SQL-Anweisung für das angegebene Objekt aus.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="querydef-openrecordset-method-dao.md">OpenRecordset</a></strong></p></td>
<td><p>Erstellt ein neues <strong><a href="recordset-object-dao.md">Recordset</a></strong> -Objekt und fügt es an die <strong>Recordsets</strong>-Auflistung an.</p></td>
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
<td><p><strong><a href="querydef-cachesize-property-dao.md">CacheSize</a></strong></p></td>
<td><p>Legt die Anzahl der von einer ODBC-Datenquelle abgefragten Datensätze fest, die lokal zwischengespeichert werden, oder gibt den betreffenden Wert zurück. <strong>Long</strong>-Wert mit Lese-/Schreibzugriff.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="querydef-connect-property-dao.md">Connect</a></strong></p></td>
<td><p>Legt einen Wert fest, der Informationen über die Quelle der in einer Pass-Through-Abfrage verwendeten Datenbank bereitstellt, oder gibt den betreffenden Wert zurück. Schreibgeschützter <strong>String</strong>-Wert.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="querydef-datecreated-property-dao.md">DateCreated</a></strong></p></td>
<td><p>Gibt das Datum und die Uhrzeit der Objekterstellung zurück (nur Microsoft Access-Arbeitsbereiche). Schreibgeschützter <strong>Variant</strong>-Wert.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="querydef-fields-property-dao.md">Felder</a></strong></p></td>
<td><p>Gibt eine <strong><a href="fields-collection-dao.md">Fields</a></strong> -Auflistung zurück, die alle gespeicherten <strong><a href="field-object-dao.md">Field</a></strong> -Objekte für das angegebene Objekt enthält. Schreibgeschützt.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="querydef-lastupdated-property-dao.md">LastUpdated</a></strong></p></td>
<td><p>Gibt das Datum und die Uhrzeit der letzten Änderung eines Objekts zurück. Schreibgeschützter <strong>Variant</strong>-Wert.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="querydef-maxrecords-property-dao.md">MaxRecords</a></strong></p></td>
<td><p>Legt die maximale Anzahl von Datensätzen fest, die von einer Abfrage an eine ODBC-Datenquelle zurückgegeben werden sollen, oder gibt den betreffenden Wert zurück.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="querydef-name-property-dao.md">Name</a></strong></p></td>
<td><p>Gibt den Namen des angegebenen Objekts zurück oder legt diesen fest. <strong>String</strong>-Wert mit Lese-/Schreibzugriff.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="querydef-odbctimeout-property-dao.md">ODBCTimeout</a></strong></p></td>
<td><p>Gibt an, wie viele Sekunden gewartet werden soll, bevor ein Timeoutfehler auftritt, wenn ein <strong><a href="querydef-object-dao.md">QueryDef</a></strong> -Objekt in einer ODBC-Datenbank ausgeführt wird.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="querydef-parameters-property-dao.md">Parameter</a></strong></p></td>
<td><p>Gibt eine <strong><a href="parameters-collection-dao.md">Parameters</a></strong> -Auflistung zurück, die alle <strong><a href="parameter-object-dao.md">Parameter</a></strong> -Objekte des angegebenen <strong>QueryDef</strong>-Objekts enthält. Schreibgeschützt.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="querydef-prepare-property-dao.md">Prepare</a></strong></p></td>
<td><p></p>

> [!NOTE]
> [!HINWEIS] ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.


<p>Legt einen Wert fest, der angibt, ob die Abfrage auf dem Server als temporäre gespeicherte Prozedur mithilfe der ODBC-API-Funktion <strong>SQLPrepare</strong> vor der Ausführung vorbereitet werden soll oder nur mithilfe der ODBC-API-Funktion <strong>SQLExecDirect</strong> ausgeführt werden soll, oder gibt den betreffenden Wert zurück (nur ODBCDirect-Arbeitsbereiche). <strong><a href="querydefstateenum-enumeration-dao.md">QueryDefStateEnum</a></strong> -Wert mit Lese-/Schreibzugriff.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="querydef-properties-property-dao.md">Eigenschaften</a></strong></p></td>
<td><p>Gibt die <strong><a href="properties-collection-dao.md">Properties</a></strong> -Auflistung des angegebenen Objekts zurück. Schreibgeschützt.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="querydef-recordsaffected-property-dao.md">RecordsAffected</a></strong></p></td>
<td><p>Gibt die Anzahl der Datensätze zurück, die von der zuletzt aufgerufenen <strong><a href="querydef-execute-method-dao.md">Execute</a></strong> -Methode betroffen waren.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="querydef-returnsrecords-property-dao.md">ReturnsRecords</a></strong></p></td>
<td><p>Gibt einen Wert zurück, der angibt, ob eine SQL Pass-Through-Abfrage an eine externe Datenbank Datensätze zurückgibt (nur Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="querydef-sql-property-dao.md">SQL</a></strong></p></td>
<td><p>Legt die SQL-Anweisung fest, die die Abfrage definiert, die von einem <strong><a href="querydef-object-dao.md">QueryDef</a></strong> -Objekt ausgeführt wird, oder gibt sie zurück.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="querydef-stillexecuting-property-dao.md">StillExecuting</a></strong></p></td>
<td><p></p>

> [!NOTE]
> [!HINWEIS] ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.


<p>Gibt an, ob ein asynchroner Vorgang (d. h. eine Methode, die mit der <a href="recordsetoptionenum-enumeration-dao.md">dbRunAsync</a>-Option aufgerufen wurde) abgeschlossen wurde (nur ODBCDirect-Arbeitsbereiche).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="querydef-type-property-dao.md">Typ</a></strong></p></td>
<td><p>Legt einen Wert fest, der den Funktions- oder Datentyp eines Objekts angibt, oder gibt diesen Wert zurück. Read-only<strong>ganze Zahl</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="querydef-updatable-property-dao.md">Updatable</a></strong></p></td>
<td><p>Gibt einen Wert zurück, der anzeigt, ob ein DAO-Objekt geändert werden kann. Schreibgeschützter <strong>Boolean</strong>-Wert.</p></td>
</tr>
</tbody>
</table>

