---
title: Datenbankmember (DAO)
TOCTitle: Database Members
ms:assetid: 68b0c069-8ed9-64dc-ea68-0d323e24c79c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195257(v=office.15)
ms:contentKeyID: 48545392
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 0f6688f09a542ade2b47c4e9909dc67977b7b163
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59589806"
---
# <a name="database-members-dao"></a>Datenbankmember (DAO)


**Gilt für**: Access 2013, Office 2013

Ein Database -Objekt stellt eine geöffnete Datenbank dar.

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
<td><p><strong><a href="database-close-method-dao.md">Close</a></strong></p></td>
<td><p>Schließt ein geöffnetes <strong>Database</strong>-Objekt.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-createproperty-method-dao.md">Createproperty</a></strong></p></td>
<td><p>Erstellt ein neues, benutzerdefiniertes <strong><a href="property-object-dao.md">Property</a></strong> -Objekt (gilt nur für Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-createquerydef-method-dao.md">CreateQueryDef</a></strong></p></td>
<td><p>Erstellt ein neues <strong><a href="querydef-object-dao.md">QueryDef</a></strong>-Objekt.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-createrelation-method-dao.md">CreateRelation</a></strong></p></td>
<td><p>Erstellt ein neues <strong><a href="relation-object-dao.md">Relation</a></strong> -Objekt (gilt nur für Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-createtabledef-method-dao.md">CreateTableDef</a></strong></p></td>
<td><p>Erstellt ein neues <strong><a href="tabledef-object-dao.md">TableDef</a></strong> -Objekt (nur Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-execute-method-dao.md">Execute</a></strong></p></td>
<td><p>Führt eine Aktionsabfrage oder eine SQL-Anweisung für das angegebene Objekt aus.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-makereplica-method-dao.md">MakeReplica</a></strong></p></td>
<td><p>Macht aus einem Datenbankreplikat ein neues Replikat (gilt nur für Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-newpassword-method-dao.md">Newpassword</a></strong></p></td>
<td><p>Ändert das Kennwort einer vorhandenen Microsoft Access-Datenbank (gilt nur für Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-openrecordset-method-dao.md">OpenRecordset</a></strong></p></td>
<td><p>Erstellt ein neues <strong><a href="recordset-object-dao.md">Recordset</a></strong>-Objekt und fügt es an die <strong>Recordsets</strong>-Auflistung an.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-populatepartial-method-dao.md">PopulatePartial</a></strong></p></td>
<td><p>Synchronisiert alle Änderungen in einem Teilreplikat mit dem vollständigen Repliktat, löscht alle Datensätze im Teilreplikat, und füllt dann das Teilreplikat auf Basis der aktuellen Replikatfilter erneut auf (gilt nur für Microsoft Access-Datenbanken).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-synchronize-method-dao.md">Synchronize</a></strong></p></td>
<td><p>Synchronisiert zwei Replikate (gilt nur für Microsoft Access-Arbeitsbereiche).</p></td>
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
<td><p><strong><a href="database-collatingorder-property-dao.md">CollatingOrder</a></strong></p></td>
<td><p>Gibt einen Wert zurück, der die Sequenz der Sortierreihenfolge im Text für den Zeichenfolgenvergleich oder die Sortierung angibt (gilt nur für Microsoft Access-Arbeitsbereiche). Schreibgeschützter <strong>Long</strong>-Wert.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-connect-property-dao.md">Verbinden</a></strong></p></td>
<td><p>Legt einen Wert fest, der Informationen zur Quelle einer geöffneten Datenbank bereitstellt, oder gibt den Wert zurück. <strong>String</strong>-Wert mit Lese-/Schreibzugriff.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-connection-property-dao.md">Connection</a></strong></p></td>
<td><p><strong>HINWEIS</strong>: ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</p>
<p>Gibt das <strong><a href="connection-object-dao.md">Connection</a></strong> -Objekt zurück, das der Datenbank entspricht (gilt nur für ODBCDirect-Arbeitsbereiche).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-containers-property-dao.md">Container</a></strong></p></td>
<td><p>Gibt eine <strong>Containers</strong>-Auflistung zurück, die alle <strong>Container</strong>-Objekte in der angegebenen Datenbank darstellt. Schreibgeschützt.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-designmasterid-property-dao.md">DesignMasterID</a></strong></p></td>
<td><p>Mit dieser Eigenschaft wird ein 16-Byte-Wert festgelegt oder zurückgegeben, der den Designmaster in einer Replikatgruppe eindeutig identifiziert (gilt nur für Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-name-property-dao.md">Name</a></strong></p></td>
<td><p>Gibt den Namen des angegebenen Objekts zurück. Read-only <strong>Zeichenfolge</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-properties-property-dao.md">Properties</a></strong></p></td>
<td><p>Gibt die <strong><a href="properties-collection-dao.md">Properties</a></strong> -Auflistung des angegebenen Objekts zurück. Schreibgeschützt.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-querydefs-property-dao.md">QueryDefs</a></strong></p></td>
<td><p>Gibt eine <strong>QueryDefs</strong>-Auflistung zurück, die alle <strong>QueryDef</strong>-Objekte der angegebenen Datenbank enthält. Schreibgeschützt.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-querytimeout-property-dao.md">Querytimeout</a></strong></p></td>
<td><p>Mit dieser Eigenschaft wird ein Wert festgelegt oder zurückgegeben, der angibt, wie viele Sekunden beim Ausführen einer Abfrage zu einer ODBC-Datenquelle gewartet wird, bevor ein Timeoutfehler auftritt.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-recordsaffected-property-dao.md">RecordsAffected</a></strong></p></td>
<td><p>Gibt die Anzahl der Datensätze zurück, die von der zuletzt aufgerufenen <strong><a href="connection-execute-method-dao.md">Execute</a></strong> -Methode betroffen waren.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-recordsets-property-dao.md">Recordsets</a></strong></p></td>
<td><p>Gibt eine <strong>Recordsets</strong>-Auflistung zurück, die alle geöffneten Recordsets für die angegebene Datenbank enthält. Schreibgeschützt.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-relations-property-dao.md">Relations</a></strong></p></td>
<td><p>Gibt eine <strong>Relations</strong>-Auflistung zurück, die alle gespeicherten <strong>Relation</strong>-Objekte für die angegebene Datenbank enthält. Schreibgeschützt.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-replicaid-property-dao.md">Replicaid</a></strong></p></td>
<td><p>Gibt einen 16-Byte-Wert zurück, der ein Replikat einer Datenbank eindeutig kennzeichnet (nur Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-tabledefs-property-dao.md">TableDefs</a></strong></p></td>
<td><p>Gibt eine <strong>TableDefs</strong>-Auflistung zurück, die alle gespeicherten <strong>TableDef</strong>-Objekte für die angegebene Datenbank enthält. Schreibgeschützt.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-transactions-property-dao.md">Transactions</a></strong></p></td>
<td><p>Gibt einen Wert zurück, der angibt, ob ein Objekt Transaktionen unterstützt. Schreibgeschützter <strong>Boolean</strong>-Wert.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-updatable-property-dao.md">Updatable</a></strong></p></td>
<td><p>Gibt einen Wert zurück, der anzeigt, ob ein DAO-Objekt geändert werden kann. Schreibgeschützter <strong>Boolean</strong>-Wert.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-version-property-dao.md">Version</a></strong></p></td>
<td><p>In einem Microsoft Access-Arbeitsbereich gibt diese Eigenschaft die Version der Microsoft Jet- oder Microsoft Access-Datenbank-Engine zurück, mit der die Datenbank erstellt wurde. Schreibgeschützter <strong>String</strong>-Wert.</p></td>
</tr>
</tbody>
</table>

