---
title: DbEngine-Member (DAO)
TOCTitle: DBEngine Members
ms:assetid: 740b6a85-585f-0e1d-710b-84ba24825325
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195868(v=office.15)
ms:contentKeyID: 48545652
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1128b27385ef9f8c898fb79d05ae28d596c4af6a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294281"
---
# <a name="dbengine-members-dao"></a>DbEngine-Member (DAO)


**Gilt für**: Access 2013, Office 2013

Das DBEngine-Objekt ist im DAO-Objektmodell das Objekt der obersten Ebene.

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
<td><p><strong><a href="dbengine-begintrans-method-dao.md">BeginTrans</a></strong></p></td>
<td><p>Startet eine neue Transaktion. <strong>Database</strong> -Wert mit Lese-/Schreibzugriff.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-committrans-method-dao.md">CommitTrans</a></strong></p></td>
<td><p>Beendet die aktuelle Transaktion und speichert die Änderungen.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-compactdatabase-method-dao.md">CompactDatabase</a></strong></p></td>
<td><p>Kopiert eine geschlossene Datenbank und gibt Ihnen die Möglichkeit, Ihre Version, Sortierreihenfolge und Verschlüsselung zu ändern. (Gilt nur für Microsoft Access-Arbeitsbereiche). .</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-createdatabase-method-dao.md">CreateDatabase</a></strong></p></td>
<td><p>Erstellt ein neues <strong><a href="database-object-dao.md">Database</a></strong> -Objekt, speichert die Datenbank auf einem Datenträger und gibt ein geöffnetes <strong>Database</strong>-Objekt zurück (gilt nur für Microsoft Access-Arbeitsbereiche). .</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-createworkspace-method-dao.md">CreateWorkspace</a></strong></p></td>
<td><p>Erstellt ein neues <strong><a href="workspace-object-dao.md">Workspace</a></strong> -Objekt.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-idle-method-dao.md">Leerlauf</a></strong></p></td>
<td><p>Unterbricht die Datenverarbeitung und ermöglicht es dem Microsoft Access-Datenbankmodul, anstehende Aufgaben auszuführen, z. B. Speicheroptimierung oder Timeouts von Seiten (gilt nur für Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-openconnection-method-dao.md">OpenConnection</a></strong></p></td>
<td><p>Einer der <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> -Werte.</p>
<td><p><strong>Hinweis</strong>: ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</p>
<p>Öffnet ein <strong><a href="connection-object-dao.md">Connection</a></strong> -Objekt in einer ODBC-Datenquelle (gilt nur für ODBCDirect-Arbeitsbereiche).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong></p></td>
<td><p>Öffnet eine angegebene Datenbank und gibt einen Verweis auf das <strong><a href="database-object-dao.md">Database</a></strong> -Objekt zurück, das sie darstellt.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-registerdatabase-method-dao.md">RegisterDatabase</a></strong></p></td>
<td><p>Gibt Verbindungsinformationen für eine ODBC-Datenquelle in die Windows-Registrierung ein. Der ODBC-Treiber benötigt Verbindungsinformationen, wenn die ODBC-Datenquelle während einer Sitzung geöffnet wird.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-rollback-method-dao.md">Rollback</a></strong></p></td>
<td><p>Beendet die aktuelle Transaktion und setzt die Datenbanken im <strong>Workspace</strong>-Objekt in den Zustand zurück, in dem sie sich befanden, als die aktuelle Transaktion gestartet wurde.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-setoption-method-dao.md">SetOption</a></strong></p></td>
<td><p>Werte für die Schlüssel des Microsoft Access-Datenbankmoduls werden in der Windows-Registrierung temporär überschrieben (gilt nur für Microsoft Access-Arbeitsbereiche).</p></td>
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
<td><p><strong><a href="dbengine-defaultpassword-property-dao.md">DefaultPassword</a></strong></p></td>
<td><p>Legt das Kennwort fest, mit dem der Standard <strong>Arbeitsbereich</strong> erstellt wird, wenn es initialisiert wird. <strong>Zeichenfolge</strong> mit Lese-/Schreibzugriff.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-defaulttype-property-dao.md">DefaultType</a></strong></p></td>
<td><p>Mit dieser Eigenschaft wird ein Wert festgelegt oder zurückgegeben, der den beim Erstellen des nächsten <strong><a href="workspace-object-dao.md">Workspace</a></strong> -Objekts verwendeten Typ des Arbeitsbereichs angibt.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-defaultuser-property-dao.md">DefaultUser</a></strong></p></td>
<td><p>Legt den Benutzernamen fest, mit dem das Standardobjekt <strong>Workspace</strong> bei seiner Initialisierung erstellt wird. <strong>String</strong>-Wert mit Lese-/Schreibzugriff.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-errors-property-dao.md">Fehler</a></strong></p></td>
<td><p>Gibt eine <strong>Errors</strong>-Auflistung zurück, die alle gespeicherten <strong>Error</strong>-Objekte für die angegebene Datenbank enthält. Schreibgeschützt.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-inipath-property-dao.md">IniPath</a></strong></p></td>
<td><p>Legt Informationen über den Windows-Registrierungsschlüssel fest, der Werte für die Microsoft Access-Datenbank-Engine enthält, oder gibt die Informationen zurück (nur Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-logintimeout-property-dao.md">LoginTimeout</a></strong></p></td>
<td><p>Legt fest, wie viele Sekunden gewartet wird, bis ein Fehler auftritt, wenn versucht wird, sich bei einer ODBC-Datenbank anzumelden, oder gibt die betreffende Anzahl von Sekunden zurück.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-properties-property-dao.md">Eigenschaften</a></strong></p></td>
<td><p>Gibt die <strong><a href="properties-collection-dao.md">Properties</a></strong> -Auflistung des angegebenen Objekts zurück. Schreibgeschützt.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-version-property-dao.md">Version</a></strong></p></td>
<td><p>Gibt die aktuell verwendete DAO-Version zurück. Schreibgeschützter <strong>String</strong>-Wert.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-workspaces-property-dao.md">Arbeitsbereiche</a></strong></p></td>
<td><p>Gibt eine <strong>Workspaces</strong>-Auflistung zurück, die alle aktiven, nicht ausgeblendeten <strong>Workspace</strong>-Objekte enthält. Schreibgeschützt.</p></td>
</tr>
</tbody>
</table>

