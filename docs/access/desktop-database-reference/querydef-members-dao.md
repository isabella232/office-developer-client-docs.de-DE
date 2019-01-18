---
title: QueryDef-Member (DAO)
TOCTitle: QueryDef Members
ms:assetid: 3f914d23-aa63-3ebd-1d86-4f53da71131b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192855(v=office.15)
ms:contentKeyID: 48544403
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5b3afc134636d5621f38ece4530be5312e42bc74
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716145"
---
# <a name="querydef-members-dao"></a><span data-ttu-id="23ea6-102">QueryDef-Member (DAO)</span><span class="sxs-lookup"><span data-stu-id="23ea6-102">QueryDef members (DAO)</span></span>


<span data-ttu-id="23ea6-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="23ea6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="23ea6-104">Ein QueryDef -Objekt ist eine gespeicherte Definition einer Abfrage in einer Datenbank des Microsoft Access-Datenbankmoduls.</span><span class="sxs-lookup"><span data-stu-id="23ea6-104">A QueryDef object is a stored definition of a query in a Microsoft Access database engine database.</span></span>

## <a name="methods"></a><span data-ttu-id="23ea6-105">Methoden</span><span class="sxs-lookup"><span data-stu-id="23ea6-105">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="23ea6-106">Name</span><span class="sxs-lookup"><span data-stu-id="23ea6-106">Name</span></span></p></th>
<th><p><span data-ttu-id="23ea6-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="23ea6-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="23ea6-108"><strong><a href="querydef-cancel-method-dao.md">Abbrechen</a></strong></span><span class="sxs-lookup"><span data-stu-id="23ea6-108"><strong><a href="querydef-cancel-method-dao.md">Cancel</a></strong></span></span></p></td>
<td><p><span data-ttu-id="23ea6-109"><strong>Hinweis</strong>: für ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="23ea6-109"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="23ea6-110">Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="23ea6-110">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="23ea6-111">Die Ausführung eines ausstehenden asynchronen Methodenaufrufs wird abgebrochen (gilt nur für ODBCDirect-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="23ea6-111">Cancels execution of a pending asynchronous method call (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23ea6-112"><strong><a href="querydef-close-method-dao.md">Schließen Sie</a></strong></span><span class="sxs-lookup"><span data-stu-id="23ea6-112"><strong><a href="querydef-close-method-dao.md">Close</a></strong></span></span></p></td>
<td><p><span data-ttu-id="23ea6-113">Schließt ein geöffnetes <strong>QueryDef</strong>-Objekt.</span><span class="sxs-lookup"><span data-stu-id="23ea6-113">Closes an open <strong>QueryDef</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23ea6-114"><strong><a href="querydef-createproperty-method-dao.md">CreateProperty</a></strong></span><span class="sxs-lookup"><span data-stu-id="23ea6-114"><strong><a href="querydef-createproperty-method-dao.md">CreateProperty</a></strong></span></span></p></td>
<td><p><span data-ttu-id="23ea6-115">Erstellt ein neues, benutzerdefiniertes <strong><a href="property-object-dao.md">Property</a></strong> -Objekt (gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="23ea6-115">Creates a new user-defined <strong><a href="property-object-dao.md">Property</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23ea6-116"><strong><a href="querydef-execute-method-dao.md">Ausführen</a></strong></span><span class="sxs-lookup"><span data-stu-id="23ea6-116"><strong><a href="querydef-execute-method-dao.md">Execute</a></strong></span></span></p></td>
<td><p><span data-ttu-id="23ea6-117">Führt eine SQL-Anweisung für das angegebene Objekt aus.</span><span class="sxs-lookup"><span data-stu-id="23ea6-117">Executes an SQL statement on the specified object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23ea6-118"><strong><a href="querydef-openrecordset-method-dao.md">OpenRecordset</a></strong></span><span class="sxs-lookup"><span data-stu-id="23ea6-118"><strong><a href="querydef-openrecordset-method-dao.md">OpenRecordset</a></strong></span></span></p></td>
<td><p><span data-ttu-id="23ea6-119">Erstellt ein neues <strong><a href="recordset-object-dao.md">Recordset</a></strong> -Objekt und fügt es an die <strong>Recordsets</strong>-Auflistung an.</span><span class="sxs-lookup"><span data-stu-id="23ea6-119">Creates a new <strong><a href="recordset-object-dao.md">Recordset</a></strong> object and appends it to the <strong>Recordsets</strong> collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="23ea6-120">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="23ea6-120">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="23ea6-121">Name</span><span class="sxs-lookup"><span data-stu-id="23ea6-121">Name</span></span></p></th>
<th><p><span data-ttu-id="23ea6-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="23ea6-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="23ea6-123"><strong><a href="querydef-cachesize-property-dao.md">CacheSize</a></strong></span><span class="sxs-lookup"><span data-stu-id="23ea6-123"><strong><a href="querydef-cachesize-property-dao.md">CacheSize</a></strong></span></span></p></td>
<td><p><span data-ttu-id="23ea6-p102">Legt die Anzahl der von einer ODBC-Datenquelle abgefragten Datensätze fest, die lokal zwischengespeichert werden, oder gibt den betreffenden Wert zurück. <strong>Long</strong>-Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="23ea6-p102">Sets or returns the number of records retrieved from an ODBC data source that will be cached locally. Read/write <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23ea6-126"><strong><a href="querydef-connect-property-dao.md">Connect</a></strong></span><span class="sxs-lookup"><span data-stu-id="23ea6-126"><strong><a href="querydef-connect-property-dao.md">Connect</a></strong></span></span></p></td>
<td><p><span data-ttu-id="23ea6-p103">Legt einen Wert fest, der Informationen über die Quelle der in einer Pass-Through-Abfrage verwendeten Datenbank bereitstellt, oder gibt den betreffenden Wert zurück. Schreibgeschützter <strong>String</strong>-Wert.</span><span class="sxs-lookup"><span data-stu-id="23ea6-p103">Sets or returns a value that provides information about the source of database used in a pass-through query. Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23ea6-129"><strong><a href="querydef-datecreated-property-dao.md">DateCreated</a></strong></span><span class="sxs-lookup"><span data-stu-id="23ea6-129"><strong><a href="querydef-datecreated-property-dao.md">DateCreated</a></strong></span></span></p></td>
<td><p><span data-ttu-id="23ea6-p104">Gibt das Datum und die Uhrzeit der Objekterstellung zurück (nur Microsoft Access-Arbeitsbereiche). Schreibgeschützter <strong>Variant</strong>-Wert.</span><span class="sxs-lookup"><span data-stu-id="23ea6-p104">Returns the date and time that an object was created (Microsoft Access workspaces only). Read-only <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23ea6-132"><strong><a href="querydef-fields-property-dao.md">Felder</a></strong></span><span class="sxs-lookup"><span data-stu-id="23ea6-132"><strong><a href="querydef-fields-property-dao.md">Fields</a></strong></span></span></p></td>
<td><p><span data-ttu-id="23ea6-p105">Gibt eine <strong><a href="fields-collection-dao.md">Fields</a></strong> -Auflistung zurück, die alle gespeicherten <strong><a href="field-object-dao.md">Field</a></strong> -Objekte für das angegebene Objekt enthält. Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="23ea6-p105">Returns a <strong><a href="fields-collection-dao.md">Fields</a></strong> collection that represents all stored <strong><a href="field-object-dao.md">Field</a></strong> objects for the specified object. Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23ea6-135"><strong><a href="querydef-lastupdated-property-dao.md">LastUpdated</a></strong></span><span class="sxs-lookup"><span data-stu-id="23ea6-135"><strong><a href="querydef-lastupdated-property-dao.md">LastUpdated</a></strong></span></span></p></td>
<td><p><span data-ttu-id="23ea6-p106">Gibt das Datum und die Uhrzeit der letzten Änderung eines Objekts zurück. Schreibgeschützter <strong>Variant</strong>-Wert.</span><span class="sxs-lookup"><span data-stu-id="23ea6-p106">Returns the date and time of the most recent change made to an object. Read-only <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23ea6-138"><strong><a href="querydef-maxrecords-property-dao.md">MaxRecords</a></strong></span><span class="sxs-lookup"><span data-stu-id="23ea6-138"><strong><a href="querydef-maxrecords-property-dao.md">MaxRecords</a></strong></span></span></p></td>
<td><p><span data-ttu-id="23ea6-139">Legt die maximale Anzahl von Datensätzen fest, die von einer Abfrage an eine ODBC-Datenquelle zurückgegeben werden sollen, oder gibt den betreffenden Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="23ea6-139">Sets or returns the maximum number of records to return from a query against an ODBC data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23ea6-140"><strong><a href="querydef-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="23ea6-140"><strong><a href="querydef-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="23ea6-p107">Gibt den Namen des angegebenen Objekts zurück oder legt diesen fest. <strong>String</strong>-Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="23ea6-p107">Returns or sets the name of the specified object. Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23ea6-143"><strong><a href="querydef-odbctimeout-property-dao.md">ODBCTimeout</a></strong></span><span class="sxs-lookup"><span data-stu-id="23ea6-143"><strong><a href="querydef-odbctimeout-property-dao.md">ODBCTimeout</a></strong></span></span></p></td>
<td><p><span data-ttu-id="23ea6-144">Gibt an, wie viele Sekunden gewartet werden soll, bevor ein Timeoutfehler auftritt, wenn ein <strong><a href="querydef-object-dao.md">QueryDef</a></strong> -Objekt in einer ODBC-Datenbank ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="23ea6-144">Indicates the number of seconds to wait before a timeout error occurs when a <strong><a href="querydef-object-dao.md">QueryDef</a></strong> is executed on an ODBC database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23ea6-145"><strong><a href="querydef-parameters-property-dao.md">Parameter</a></strong></span><span class="sxs-lookup"><span data-stu-id="23ea6-145"><strong><a href="querydef-parameters-property-dao.md">Parameters</a></strong></span></span></p></td>
<td><p><span data-ttu-id="23ea6-p108">Gibt eine <strong><a href="parameters-collection-dao.md">Parameters</a></strong> -Auflistung zurück, die alle <strong><a href="parameter-object-dao.md">Parameter</a></strong> -Objekte des angegebenen <strong>QueryDef</strong>-Objekts enthält. Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="23ea6-p108">Returns a <strong><a href="parameters-collection-dao.md">Parameters</a></strong> collection that contains all of the <strong><a href="parameter-object-dao.md">Parameter</a></strong> objects of the specified <strong>QueryDef</strong>. Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23ea6-148"><strong><a href="querydef-prepare-property-dao.md">Prepare</a></strong></span><span class="sxs-lookup"><span data-stu-id="23ea6-148"><strong><a href="querydef-prepare-property-dao.md">Prepare</a></strong></span></span></p></td>
<td><p><span data-ttu-id="23ea6-149"><strong>Hinweis</strong>: für ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="23ea6-149"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="23ea6-150">Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="23ea6-150">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="23ea6-p110">Legt einen Wert fest, der angibt, ob die Abfrage auf dem Server als temporäre gespeicherte Prozedur mithilfe der ODBC-API-Funktion <strong>SQLPrepare</strong> vor der Ausführung vorbereitet werden soll oder nur mithilfe der ODBC-API-Funktion <strong>SQLExecDirect</strong> ausgeführt werden soll, oder gibt den betreffenden Wert zurück (nur ODBCDirect-Arbeitsbereiche). <strong><a href="querydefstateenum-enumeration-dao.md">QueryDefStateEnum</a></strong> -Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="23ea6-p110">Sets or returns a value that indicates whether the query should be prepared on the server as a temporary stored procedure, using the ODBC <strong>SQLPrepare</strong> API function, prior to execution, or just executed using the ODBC <strong>SQLExecDirect</strong> API function (ODBCDirect workspaces only). Read/Write <strong><a href="querydefstateenum-enumeration-dao.md">QueryDefStateEnum</a></strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23ea6-153"><strong><a href="querydef-properties-property-dao.md">Eigenschaften</a></strong></span><span class="sxs-lookup"><span data-stu-id="23ea6-153"><strong><a href="querydef-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="23ea6-p111">Gibt die <strong><a href="properties-collection-dao.md">Properties</a></strong> -Auflistung des angegebenen Objekts zurück. Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="23ea6-p111">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object. Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23ea6-156"><strong><a href="querydef-recordsaffected-property-dao.md">RecordsAffected</a></strong></span><span class="sxs-lookup"><span data-stu-id="23ea6-156"><strong><a href="querydef-recordsaffected-property-dao.md">RecordsAffected</a></strong></span></span></p></td>
<td><p><span data-ttu-id="23ea6-157">Gibt die Anzahl der Datensätze zurück, die von der zuletzt aufgerufenen <strong><a href="querydef-execute-method-dao.md">Execute</a></strong> -Methode betroffen waren.</span><span class="sxs-lookup"><span data-stu-id="23ea6-157">Returns the number of records affected by the most recently invoked <strong><a href="querydef-execute-method-dao.md">Execute</a></strong> method.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23ea6-158"><strong><a href="querydef-returnsrecords-property-dao.md">ReturnsRecords</a></strong></span><span class="sxs-lookup"><span data-stu-id="23ea6-158"><strong><a href="querydef-returnsrecords-property-dao.md">ReturnsRecords</a></strong></span></span></p></td>
<td><p><span data-ttu-id="23ea6-159">Gibt einen Wert zurück, der angibt, ob eine SQL Pass-Through-Abfrage an eine externe Datenbank Datensätze zurückgibt (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="23ea6-159">Sets or returns a value that indicates whether an SQL pass-through query to an external database returns records (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23ea6-160"><strong><a href="querydef-sql-property-dao.md">SQL</a></strong></span><span class="sxs-lookup"><span data-stu-id="23ea6-160"><strong><a href="querydef-sql-property-dao.md">SQL</a></strong></span></span></p></td>
<td><p><span data-ttu-id="23ea6-161">Legt die SQL-Anweisung fest, die die Abfrage definiert, die von einem <strong><a href="querydef-object-dao.md">QueryDef</a></strong> -Objekt ausgeführt wird, oder gibt sie zurück.</span><span class="sxs-lookup"><span data-stu-id="23ea6-161">Sets or returns the SQL statement that defines the query executed by a <strong><a href="querydef-object-dao.md">QueryDef</a></strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23ea6-162"><strong><a href="querydef-stillexecuting-property-dao.md">StillExecuting</a></strong></span><span class="sxs-lookup"><span data-stu-id="23ea6-162"><strong><a href="querydef-stillexecuting-property-dao.md">StillExecuting</a></strong></span></span></p></td>
<td><p><span data-ttu-id="23ea6-163"><strong>Hinweis</strong>: für ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="23ea6-163"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="23ea6-164">Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="23ea6-164">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="23ea6-165">Gibt an, ob ein asynchroner Vorgang (d. h. eine Methode, die mit der <a href="recordsetoptionenum-enumeration-dao.md">dbRunAsync</a>-Option aufgerufen wurde) abgeschlossen wurde (nur ODBCDirect-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="23ea6-165">Indicates whether or not an asynchronous operation (that is, a method called with the <a href="recordsetoptionenum-enumeration-dao.md">dbRunAsync</a> option) has finished executing (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23ea6-166"><strong><a href="querydef-type-property-dao.md">Typ</a></strong></span><span class="sxs-lookup"><span data-stu-id="23ea6-166"><strong><a href="querydef-type-property-dao.md">Type</a></strong></span></span></p></td>
<td><p><span data-ttu-id="23ea6-167">Legt einen Wert fest, der den Funktions- oder Datentyp eines Objekts angibt, oder gibt diesen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="23ea6-167">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="23ea6-168">Read-only<strong>ganze Zahl</strong>.</span><span class="sxs-lookup"><span data-stu-id="23ea6-168">Read-only<strong>Integer</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23ea6-169"><strong><a href="querydef-updatable-property-dao.md">Updatable</a></strong></span><span class="sxs-lookup"><span data-stu-id="23ea6-169"><strong><a href="querydef-updatable-property-dao.md">Updatable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="23ea6-p114">Gibt einen Wert zurück, der anzeigt, ob ein DAO-Objekt geändert werden kann. Schreibgeschützter <strong>Boolean</strong>-Wert.</span><span class="sxs-lookup"><span data-stu-id="23ea6-p114">Returns a value that indicates whether you can change a DAO object. Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

