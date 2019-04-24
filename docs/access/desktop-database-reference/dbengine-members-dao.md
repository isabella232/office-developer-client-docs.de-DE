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
# <a name="dbengine-members-dao"></a><span data-ttu-id="f5ef1-102">DbEngine-Member (DAO)</span><span class="sxs-lookup"><span data-stu-id="f5ef1-102">DBEngine members (DAO)</span></span>


<span data-ttu-id="f5ef1-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f5ef1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f5ef1-104">Das DBEngine-Objekt ist im DAO-Objektmodell das Objekt der obersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="f5ef1-104">The DBEngine object is the top level object in the DAO object model.</span></span>

## <a name="methods"></a><span data-ttu-id="f5ef1-105">Methoden</span><span class="sxs-lookup"><span data-stu-id="f5ef1-105">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f5ef1-106">Name</span><span class="sxs-lookup"><span data-stu-id="f5ef1-106">Name</span></span></p></th>
<th><p><span data-ttu-id="f5ef1-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f5ef1-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f5ef1-108"><strong><a href="dbengine-begintrans-method-dao.md">BeginTrans</a></strong></span><span class="sxs-lookup"><span data-stu-id="f5ef1-108"><strong><a href="dbengine-begintrans-method-dao.md">BeginTrans</a></strong></span></span></p></td>
<td><p><span data-ttu-id="f5ef1-109">Startet eine neue Transaktion.</span><span class="sxs-lookup"><span data-stu-id="f5ef1-109">Begins a new transaction.</span></span> <span data-ttu-id="f5ef1-110"><strong>Database</strong> -Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="f5ef1-110">Read/write <strong>Database</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5ef1-111"><strong><a href="dbengine-committrans-method-dao.md">CommitTrans</a></strong></span><span class="sxs-lookup"><span data-stu-id="f5ef1-111"><strong><a href="dbengine-committrans-method-dao.md">CommitTrans</a></strong></span></span></p></td>
<td><p><span data-ttu-id="f5ef1-112">Beendet die aktuelle Transaktion und speichert die Änderungen.</span><span class="sxs-lookup"><span data-stu-id="f5ef1-112">Ends the current transaction and saves the changes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5ef1-113"><strong><a href="dbengine-compactdatabase-method-dao.md">CompactDatabase</a></strong></span><span class="sxs-lookup"><span data-stu-id="f5ef1-113"><strong><a href="dbengine-compactdatabase-method-dao.md">CompactDatabase</a></strong></span></span></p></td>
<td><p><span data-ttu-id="f5ef1-114">Kopiert eine geschlossene Datenbank und gibt Ihnen die Möglichkeit, Ihre Version, Sortierreihenfolge und Verschlüsselung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="f5ef1-114">Copies and compacts a closed database, and gives you the option of changing its version, collating order, and encryption.</span></span> <span data-ttu-id="f5ef1-115">(Gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="f5ef1-115">(Microsoft Access workspaces only).</span></span> <span data-ttu-id="f5ef1-116">.</span><span class="sxs-lookup"><span data-stu-id="f5ef1-116"></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5ef1-117"><strong><a href="dbengine-createdatabase-method-dao.md">CreateDatabase</a></strong></span><span class="sxs-lookup"><span data-stu-id="f5ef1-117"><strong><a href="dbengine-createdatabase-method-dao.md">CreateDatabase</a></strong></span></span></p></td>
<td><p><span data-ttu-id="f5ef1-118">Erstellt ein neues <strong><a href="database-object-dao.md">Database</a></strong> -Objekt, speichert die Datenbank auf einem Datenträger und gibt ein geöffnetes <strong>Database</strong>-Objekt zurück (gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="f5ef1-118">Creates a new <strong><a href="database-object-dao.md">Database</a></strong> object, saves the database to disk, and returns an opened <strong>Database</strong> object (Microsoft Access workspaces only).</span></span> <span data-ttu-id="f5ef1-119">.</span><span class="sxs-lookup"><span data-stu-id="f5ef1-119"></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5ef1-120"><strong><a href="dbengine-createworkspace-method-dao.md">CreateWorkspace</a></strong></span><span class="sxs-lookup"><span data-stu-id="f5ef1-120"><strong><a href="dbengine-createworkspace-method-dao.md">CreateWorkspace</a></strong></span></span></p></td>
<td><p><span data-ttu-id="f5ef1-121">Erstellt ein neues <strong><a href="workspace-object-dao.md">Workspace</a></strong> -Objekt.</span><span class="sxs-lookup"><span data-stu-id="f5ef1-121">Creates a new <strong><a href="workspace-object-dao.md">Workspace</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5ef1-122"><strong><a href="dbengine-idle-method-dao.md">Leerlauf</a></strong></span><span class="sxs-lookup"><span data-stu-id="f5ef1-122"><strong><a href="dbengine-idle-method-dao.md">Idle</a></strong></span></span></p></td>
<td><p><span data-ttu-id="f5ef1-123">Unterbricht die Datenverarbeitung und ermöglicht es dem Microsoft Access-Datenbankmodul, anstehende Aufgaben auszuführen, z. B. Speicheroptimierung oder Timeouts von Seiten (gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="f5ef1-123">Suspends data processing, enabling the Microsoft Access database engine to complete any pending tasks, such as memory optimization or page timeouts (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5ef1-124"><strong><a href="dbengine-openconnection-method-dao.md">OpenConnection</a></strong></span><span class="sxs-lookup"><span data-stu-id="f5ef1-124"><strong><a href="dbengine-openconnection-method-dao.md">OpenConnection</a></strong></span></span></p></td>
<td><p><span data-ttu-id="f5ef1-125">Einer der <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> -Werte.</span><span class="sxs-lookup"><span data-stu-id="f5ef1-125">One of the <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> values.</span></span></p>
<td><p><span data-ttu-id="f5ef1-126"><strong>Hinweis</strong>: ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f5ef1-126"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="f5ef1-127">Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="f5ef1-127">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="f5ef1-128">Öffnet ein <strong><a href="connection-object-dao.md">Connection</a></strong> -Objekt in einer ODBC-Datenquelle (gilt nur für ODBCDirect-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="f5ef1-128">Opens a <strong><a href="connection-object-dao.md">Connection</a></strong> object on an ODBC data source (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5ef1-129"><strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong></span><span class="sxs-lookup"><span data-stu-id="f5ef1-129"><strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong></span></span></p></td>
<td><p><span data-ttu-id="f5ef1-130">Öffnet eine angegebene Datenbank und gibt einen Verweis auf das <strong><a href="database-object-dao.md">Database</a></strong> -Objekt zurück, das sie darstellt.</span><span class="sxs-lookup"><span data-stu-id="f5ef1-130">Opens a specified database and returns a reference to the <strong><a href="database-object-dao.md">Database</a></strong> object that represents it.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5ef1-131"><strong><a href="dbengine-registerdatabase-method-dao.md">RegisterDatabase</a></strong></span><span class="sxs-lookup"><span data-stu-id="f5ef1-131"><strong><a href="dbengine-registerdatabase-method-dao.md">RegisterDatabase</a></strong></span></span></p></td>
<td><p><span data-ttu-id="f5ef1-p105">Gibt Verbindungsinformationen für eine ODBC-Datenquelle in die Windows-Registrierung ein. Der ODBC-Treiber benötigt Verbindungsinformationen, wenn die ODBC-Datenquelle während einer Sitzung geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="f5ef1-p105">Enters connection information for an ODBC data source in the Windows Registry. The ODBC driver needs connection information when the ODBC data source is opened during a session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5ef1-134"><strong><a href="dbengine-rollback-method-dao.md">Rollback</a></strong></span><span class="sxs-lookup"><span data-stu-id="f5ef1-134"><strong><a href="dbengine-rollback-method-dao.md">Rollback</a></strong></span></span></p></td>
<td><p><span data-ttu-id="f5ef1-135">Beendet die aktuelle Transaktion und setzt die Datenbanken im <strong>Workspace</strong>-Objekt in den Zustand zurück, in dem sie sich befanden, als die aktuelle Transaktion gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="f5ef1-135">Ends the current transaction and restores the databases in the <strong>Workspace</strong> object to the state they were in when the current transaction began.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5ef1-136"><strong><a href="dbengine-setoption-method-dao.md">SetOption</a></strong></span><span class="sxs-lookup"><span data-stu-id="f5ef1-136"><strong><a href="dbengine-setoption-method-dao.md">SetOption</a></strong></span></span></p></td>
<td><p><span data-ttu-id="f5ef1-137">Werte für die Schlüssel des Microsoft Access-Datenbankmoduls werden in der Windows-Registrierung temporär überschrieben (gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="f5ef1-137">Temporarily overrides values for the Microsoft Access database engine keys in the Windows Registry (Microsoft Access workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="f5ef1-138">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f5ef1-138">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f5ef1-139">Name</span><span class="sxs-lookup"><span data-stu-id="f5ef1-139">Name</span></span></p></th>
<th><p><span data-ttu-id="f5ef1-140">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f5ef1-140">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f5ef1-141"><strong><a href="dbengine-defaultpassword-property-dao.md">DefaultPassword</a></strong></span><span class="sxs-lookup"><span data-stu-id="f5ef1-141"><strong><a href="dbengine-defaultpassword-property-dao.md">DefaultPassword</a></strong></span></span></p></td>
<td><p><span data-ttu-id="f5ef1-142">Legt das Kennwort fest, mit dem der Standard <strong>Arbeitsbereich</strong> erstellt wird, wenn es initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="f5ef1-142">Sets the password used to create the default <strong>Workspace</strong> when it is initialized.</span></span> <span data-ttu-id="f5ef1-143"><strong>Zeichenfolge</strong> mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="f5ef1-143">Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5ef1-144"><strong><a href="dbengine-defaulttype-property-dao.md">DefaultType</a></strong></span><span class="sxs-lookup"><span data-stu-id="f5ef1-144"><strong><a href="dbengine-defaulttype-property-dao.md">DefaultType</a></strong></span></span></p></td>
<td><p><span data-ttu-id="f5ef1-145">Mit dieser Eigenschaft wird ein Wert festgelegt oder zurückgegeben, der den beim Erstellen des nächsten <strong><a href="workspace-object-dao.md">Workspace</a></strong> -Objekts verwendeten Typ des Arbeitsbereichs angibt.</span><span class="sxs-lookup"><span data-stu-id="f5ef1-145">Sets or returns a value that indicates what type of workspace will be used by the next <strong><a href="workspace-object-dao.md">Workspace</a></strong> object created.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5ef1-146"><strong><a href="dbengine-defaultuser-property-dao.md">DefaultUser</a></strong></span><span class="sxs-lookup"><span data-stu-id="f5ef1-146"><strong><a href="dbengine-defaultuser-property-dao.md">DefaultUser</a></strong></span></span></p></td>
<td><p><span data-ttu-id="f5ef1-147">Legt den Benutzernamen fest, mit dem das Standardobjekt <strong>Workspace</strong> bei seiner Initialisierung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="f5ef1-147">Sets the user name used to create the default <strong>Workspace</strong> when it is initialized.</span></span> <span data-ttu-id="f5ef1-148"><strong>String</strong>-Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="f5ef1-148">Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5ef1-149"><strong><a href="dbengine-errors-property-dao.md">Fehler</a></strong></span><span class="sxs-lookup"><span data-stu-id="f5ef1-149"><strong><a href="dbengine-errors-property-dao.md">Errors</a></strong></span></span></p></td>
<td><p><span data-ttu-id="f5ef1-150">Gibt eine <strong>Errors</strong>-Auflistung zurück, die alle gespeicherten <strong>Error</strong>-Objekte für die angegebene Datenbank enthält.</span><span class="sxs-lookup"><span data-stu-id="f5ef1-150">Returns an <strong>Errors</strong> collection that contains all of the stored <strong>Error</strong> objects for the specified object.</span></span> <span data-ttu-id="f5ef1-151">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="f5ef1-151">Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5ef1-152"><strong><a href="dbengine-inipath-property-dao.md">IniPath</a></strong></span><span class="sxs-lookup"><span data-stu-id="f5ef1-152"><strong><a href="dbengine-inipath-property-dao.md">IniPath</a></strong></span></span></p></td>
<td><p><span data-ttu-id="f5ef1-153">Legt Informationen über den Windows-Registrierungsschlüssel fest, der Werte für die Microsoft Access-Datenbank-Engine enthält, oder gibt die Informationen zurück (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="f5ef1-153">Sets or returns information about the Windows Registry key that contains values for the Microsoft Access database engine (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5ef1-154"><strong><a href="dbengine-logintimeout-property-dao.md">LoginTimeout</a></strong></span><span class="sxs-lookup"><span data-stu-id="f5ef1-154"><strong><a href="dbengine-logintimeout-property-dao.md">LoginTimeout</a></strong></span></span></p></td>
<td><p><span data-ttu-id="f5ef1-155">Legt fest, wie viele Sekunden gewartet wird, bis ein Fehler auftritt, wenn versucht wird, sich bei einer ODBC-Datenbank anzumelden, oder gibt die betreffende Anzahl von Sekunden zurück.</span><span class="sxs-lookup"><span data-stu-id="f5ef1-155">Sets or returns the number of seconds before an error occurs when you attempt to log on to an ODBC database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5ef1-156"><strong><a href="dbengine-properties-property-dao.md">Eigenschaften</a></strong></span><span class="sxs-lookup"><span data-stu-id="f5ef1-156"><strong><a href="dbengine-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="f5ef1-157">Gibt die <strong><a href="properties-collection-dao.md">Properties</a></strong> -Auflistung des angegebenen Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="f5ef1-157">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object.</span></span> <span data-ttu-id="f5ef1-158">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="f5ef1-158">Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5ef1-159"><strong><a href="dbengine-version-property-dao.md">Version</a></strong></span><span class="sxs-lookup"><span data-stu-id="f5ef1-159"><strong><a href="dbengine-version-property-dao.md">Version</a></strong></span></span></p></td>
<td><p><span data-ttu-id="f5ef1-160">Gibt die aktuell verwendete DAO-Version zurück.</span><span class="sxs-lookup"><span data-stu-id="f5ef1-160">Rreturns the version of DAO currently in use.</span></span> <span data-ttu-id="f5ef1-161">Schreibgeschützter <strong>String</strong>-Wert.</span><span class="sxs-lookup"><span data-stu-id="f5ef1-161">Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5ef1-162"><strong><a href="dbengine-workspaces-property-dao.md">Arbeitsbereiche</a></strong></span><span class="sxs-lookup"><span data-stu-id="f5ef1-162"><strong><a href="dbengine-workspaces-property-dao.md">Workspaces</a></strong></span></span></p></td>
<td><p><span data-ttu-id="f5ef1-163">Gibt eine <strong>Workspaces</strong>-Auflistung zurück, die alle aktiven, nicht ausgeblendeten <strong>Workspace</strong>-Objekte enthält.</span><span class="sxs-lookup"><span data-stu-id="f5ef1-163">Returns a <strong>Workspaces</strong> collection that contains all of the active, unhidden <strong>Workspace</strong> objects.</span></span> <span data-ttu-id="f5ef1-164">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="f5ef1-164">Read-only.</span></span></p></td>
</tr>
</tbody>
</table>

