---
title: Arbeitsbereichsmitglieder (DAO)
TOCTitle: Workspace Members
ms:assetid: 13ac7d41-1b25-20d2-5c85-0f21bfd38328
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845437(v=office.15)
ms:contentKeyID: 48543374
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f3deb259e5058fe595099e5fa556ff5fca8e4baf
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923889"
---
# <a name="workspace-members-dao"></a><span data-ttu-id="ee1b9-102">Arbeitsbereichsmitglieder (DAO)</span><span class="sxs-lookup"><span data-stu-id="ee1b9-102">Workspace members (DAO)</span></span>


<span data-ttu-id="ee1b9-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ee1b9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ee1b9-p101">Ein Arbeitsbereichs objekt definiert eine benannte Sitzung für einen Benutzer. Es enthält geöffnete Datenbanken und stellt Mechanismen für gleichzeitige Transaktionen und in Microsoft Access Arbeitsbereiche für den sicheren Arbeitsgruppen-Support bereit.</span><span class="sxs-lookup"><span data-stu-id="ee1b9-p101">A Workspace object defines a named session for a user. It contains open databases and provides mechanisms for simultaneous transactions and, in Microsoft Access workspaces, secure workgroup support.</span></span>

## <a name="methods"></a><span data-ttu-id="ee1b9-106">Methoden</span><span class="sxs-lookup"><span data-stu-id="ee1b9-106">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ee1b9-107">Name</span><span class="sxs-lookup"><span data-stu-id="ee1b9-107">Name</span></span></p></th>
<th><p><span data-ttu-id="ee1b9-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ee1b9-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee1b9-109"><strong><a href="workspace-begintrans-method-dao.md">BeginTrans</a></strong></span><span class="sxs-lookup"><span data-stu-id="ee1b9-109"><strong><a href="workspace-begintrans-method-dao.md">BeginTrans</a></strong></span></span></p></td>
<td><p><span data-ttu-id="ee1b9-p102">Startet eine neue Transaktion. <strong>Database</strong> -Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="ee1b9-p102">Begins a new transaction. Read/write <strong>Database</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee1b9-112"><strong><a href="workspace-close-method-dao.md">Schließen Sie</a></strong></span><span class="sxs-lookup"><span data-stu-id="ee1b9-112"><strong><a href="workspace-close-method-dao.md">Close</a></strong></span></span></p></td>
<td><p><span data-ttu-id="ee1b9-113">Schließt ein geöffnetes <strong>Workspace</strong>-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ee1b9-113">Closes an open <strong>Workspace</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee1b9-114"><strong><a href="workspace-committrans-method-dao.md">CommitTrans</a></strong></span><span class="sxs-lookup"><span data-stu-id="ee1b9-114"><strong><a href="workspace-committrans-method-dao.md">CommitTrans</a></strong></span></span></p></td>
<td><p><span data-ttu-id="ee1b9-115">Beendet die aktuelle Transaktion und speichert die Änderungen.</span><span class="sxs-lookup"><span data-stu-id="ee1b9-115">Ends the current transaction and saves the changes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee1b9-116"><strong><a href="workspace-createdatabase-method-dao.md">CreateDatabase</a></strong></span><span class="sxs-lookup"><span data-stu-id="ee1b9-116"><strong><a href="workspace-createdatabase-method-dao.md">CreateDatabase</a></strong></span></span></p></td>
<td><p><span data-ttu-id="ee1b9-117">Erstellt ein neues <strong><a href="database-object-dao.md">Database</a></strong> -Objekt, speichert die Datenbank auf einem Datenträger und gibt ein geöffnetes <strong>Database</strong>-Objekt zurück (gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="ee1b9-117">Creates a new <strong><a href="database-object-dao.md">Database</a></strong> object, saves the database to disk, and returns an opened <strong>Database</strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee1b9-118"><strong><a href="workspace-openconnection-method-dao.md">OpenConnection</a></strong></span><span class="sxs-lookup"><span data-stu-id="ee1b9-118"><strong><a href="workspace-openconnection-method-dao.md">OpenConnection</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <P><span data-ttu-id="ee1b9-p103">[!HINWEIS] ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ee1b9-p103">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


<p><span data-ttu-id="ee1b9-121">Öffnet ein <strong><a href="connection-object-dao.md">Connection</a></strong> -Objekt in einer ODBC-Datenquelle (gilt nur für ODBCDirect-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="ee1b9-121">Opens a <strong><a href="connection-object-dao.md">Connection</a></strong> object on an ODBC data source (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee1b9-122"><strong><a href="workspace-opendatabase-method-dao.md">OpenDatabase</a></strong></span><span class="sxs-lookup"><span data-stu-id="ee1b9-122"><strong><a href="workspace-opendatabase-method-dao.md">OpenDatabase</a></strong></span></span></p></td>
<td><p><span data-ttu-id="ee1b9-123">Öffnet eine bestimmte Datenbank in einem <strong><a href="workspace-object-dao.md">Workspace</a></strong> -Objekt und gibt einen Verweis auf das <strong><a href="database-object-dao.md">Database</a></strong> -Objekt zurück, das es darstellt.</span><span class="sxs-lookup"><span data-stu-id="ee1b9-123">Opens a specified database in a <strong><a href="workspace-object-dao.md">Workspace</a></strong> object and returns a reference to the <strong><a href="database-object-dao.md">Database</a></strong> object that represents it.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee1b9-124"><strong><a href="workspace-rollback-method-dao.md">Rollback</a></strong></span><span class="sxs-lookup"><span data-stu-id="ee1b9-124"><strong><a href="workspace-rollback-method-dao.md">Rollback</a></strong></span></span></p></td>
<td><p><span data-ttu-id="ee1b9-125">Beendet die aktuelle Transaktion und setzt die Datenbanken im <strong>Workspace</strong>-Objekt in den Zustand zurück, in dem sie sich befanden, als die aktuelle Transaktion gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="ee1b9-125">Ends the current transaction and restores the databases in the <strong>Workspace</strong> object to the state they were in when the current transaction began.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="ee1b9-126">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ee1b9-126">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ee1b9-127">Name</span><span class="sxs-lookup"><span data-stu-id="ee1b9-127">Name</span></span></p></th>
<th><p><span data-ttu-id="ee1b9-128">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ee1b9-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee1b9-129"><strong><a href="workspace-connections-property-dao.md">Connections</a></strong></span><span class="sxs-lookup"><span data-stu-id="ee1b9-129"><strong><a href="workspace-connections-property-dao.md">Connections</a></strong></span></span></p></td>
<td><p><span data-ttu-id="ee1b9-p104">Gibt eine <strong>Connections</strong>-Auflistung zurück, die die aktuellen Verbindungen im angegebenen <strong>Workspace</strong>-Objekt darstellt. Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ee1b9-p104">Returns a <strong>Connections</strong> collection that represents the current connections in the specified <strong>Workspace</strong>. Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee1b9-132"><strong><a href="workspace-databases-property-dao.md">Databases</a></strong></span><span class="sxs-lookup"><span data-stu-id="ee1b9-132"><strong><a href="workspace-databases-property-dao.md">Databases</a></strong></span></span></p></td>
<td><p><span data-ttu-id="ee1b9-p105">Gibt eine <strong>Databases</strong>-Auflistung zurück, die die geöffneten Datenbanken im angegebenen <strong>Workspace</strong>-Objekt darstellt. Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ee1b9-p105">Returns a <strong>Databases</strong> collection that represents the open databases in the specified <strong>Workspace</strong>. Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee1b9-135"><strong><a href="workspace-defaultcursordriver-property-dao.md">DefaultCursorDriver</a></strong></span><span class="sxs-lookup"><span data-stu-id="ee1b9-135"><strong><a href="workspace-defaultcursordriver-property-dao.md">DefaultCursorDriver</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <P><span data-ttu-id="ee1b9-p106">[!HINWEIS] ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ee1b9-p106">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


<p><span data-ttu-id="ee1b9-138">Mit dieser Eigenschaft wird der Typ des Cursortreibers festgelegt oder zurückgegeben, der für die mit der <strong><a href="dbengine-openconnection-method-dao.md">OpenConnection</a></strong> - oder <strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong> -Methode erstellte Verbindung verwendet wird (gilt nur für ODBCDirect-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="ee1b9-138">Sets or returns the type of cursor driver used on the connection created by the <strong><a href="dbengine-openconnection-method-dao.md">OpenConnection</a></strong> or <strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong> methods (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee1b9-139"><strong><a href="workspace-isolateodbctrans-property-dao.md">IsolateODBCTrans</a></strong></span><span class="sxs-lookup"><span data-stu-id="ee1b9-139"><strong><a href="workspace-isolateodbctrans-property-dao.md">IsolateODBCTrans</a></strong></span></span></p></td>
<td><p><span data-ttu-id="ee1b9-140">Legt einen Wert fest, der angibt, ob mehrere Transaktionen, die dieselbe mit der Microsoft Access-Datenbank-Engine verbundene ODBC-Datenquelle verwenden, isoliert sind, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="ee1b9-140">Sets or returns a value that indicates whether multiple transactiond that involve the same Microsoft Access database engine-connected ODBC data source are isolated (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee1b9-141"><strong><a href="workspace-logintimeout-property-dao.md">LoginTimeout</a></strong></span><span class="sxs-lookup"><span data-stu-id="ee1b9-141"><strong><a href="workspace-logintimeout-property-dao.md">LoginTimeout</a></strong></span></span></p></td>
<td><p><span data-ttu-id="ee1b9-142">Legt fest, wie viele Sekunden gewartet wird, bis ein Fehler auftritt, wenn versucht wird, sich bei einer ODBC-Datenbank anzumelden, oder gibt die betreffende Anzahl von Sekunden zurück.</span><span class="sxs-lookup"><span data-stu-id="ee1b9-142">Sets or returns the number of seconds before an error occurs when you attempt to log on to an ODBC database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee1b9-143"><strong><a href="workspace-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="ee1b9-143"><strong><a href="workspace-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="ee1b9-p107">Gibt den Namen des angegebenen Objekts zurück oder legt diesen fest. <strong>String</strong>-Wert mit Lese-/Schreibzugriff, wenn das Objekt noch keiner Auflistung angefügt wurde. Schreibgeschützter <strong>String</strong>-Wert, wenn das Objekt einer Auflistung angefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="ee1b9-p107">Returns or sets the name of the specified object. Read/write <strong>String</strong> if the object has not been appended to a collection. Read-only <strong>String</strong> if the object has been appended to a collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee1b9-147"><strong><a href="workspace-properties-property-dao.md">Eigenschaften</a></strong></span><span class="sxs-lookup"><span data-stu-id="ee1b9-147"><strong><a href="workspace-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="ee1b9-p108">Gibt die <strong><a href="properties-collection-dao.md">Properties</a></strong> -Auflistung des angegebenen Objekts zurück. Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="ee1b9-p108">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object. Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee1b9-150"><strong><a href="workspace-type-property-dao.md">Typ</a></strong></span><span class="sxs-lookup"><span data-stu-id="ee1b9-150"><strong><a href="workspace-type-property-dao.md">Type</a></strong></span></span></p></td>
<td><p><span data-ttu-id="ee1b9-p109">Legt einen Wert fest, der den Funktions- oder Datentyp eines Objekts angibt, oder gibt diesen Wert zurück. Schreibgeschützter <strong>Integer</strong>-Wert.</span><span class="sxs-lookup"><span data-stu-id="ee1b9-p109">Sets or returns a value that indicates the operational type or data type of an object. Read-only <strong>Integer</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

