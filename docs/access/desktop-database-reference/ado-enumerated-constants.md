---
title: ADO-Aufzählungskonstanten
TOCTitle: ADO enumerated constants
ms:assetid: 7c983acd-8b38-dc3c-6704-46e649ebb7d6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249522(v=office.15)
ms:contentKeyID: 48545841
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 05e5d3a77dc7db5ef5a0d81a3f13d5fc5987f5de
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707940"
---
# <a name="ado-enumerated-constants"></a><span data-ttu-id="d3eed-102">ADO-Aufzählungskonstanten</span><span class="sxs-lookup"><span data-stu-id="d3eed-102">ADO enumerated constants</span></span>

<span data-ttu-id="d3eed-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d3eed-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d3eed-p101">Zur Unterstützung beim Debuggen wird in den ADO-Aufzählungen für jede Konstante ein Wert aufgelistet. Dieser Wert ist jedoch lediglich ein Hinweis und kann zwischen ADO-Versionen geändert werden. Der Code sollte nur vom Namen, nicht vom tatsächlichen Wert, der einzelnen aufgezählten Konstanten abhängen.</span><span class="sxs-lookup"><span data-stu-id="d3eed-p101">To assist in debugging, the ADO enumerations list a value for each constant. However, this value is purely advisory, and may change from one release of ADO to another. Your code should only depend on the name, not the actual value, of each enumerated constant.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th><span data-ttu-id="d3eed-107">Enumerierte Konstante</span><span class="sxs-lookup"><span data-stu-id="d3eed-107">Enumerated constant</span></span></th>
<th><span data-ttu-id="d3eed-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d3eed-108">Description</span></span></th>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3eed-109"><a href="adcprop-asyncthreadpriority-enum.md">ADCPROP_ASYNCTHREADPRIORITY_ENUM</a></span><span class="sxs-lookup"><span data-stu-id="d3eed-109"><a href="adcprop-asyncthreadpriority-enum.md">ADCPROP_ASYNCTHREADPRIORITY_ENUM</a></span></span></p></td>
<td><p><span data-ttu-id="d3eed-110">Gibt für ein RDS-<strong>Recordset</strong>-Objekt die Ausführungspriorität des asynchronen Threads an, der Daten abruft.</span><span class="sxs-lookup"><span data-stu-id="d3eed-110">For an RDS <strong>Recordset</strong> object, specifies the execution priority of the asynchronous thread that retrieves data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3eed-111"><a href="adcprop-autorecalc-enum.md">ADCPROP_AUTORECALC_ENUM</a></span><span class="sxs-lookup"><span data-stu-id="d3eed-111"><a href="adcprop-autorecalc-enum.md">ADCPROP_AUTORECALC_ENUM</a></span></span></p></td>
<td><p><span data-ttu-id="d3eed-112">Gibt an, wann der <strong>MSDataShape</strong> -Anbieter aggregierte und berechnete Spalten in einem hierarchischen <strong>Recordset</strong>erneut berechnet.</span><span class="sxs-lookup"><span data-stu-id="d3eed-112">Specifies when the <strong>MSDataShape</strong> provider re-calculates aggregate and calculated columns in a hierarchical <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3eed-113"><a href="adcprop-updatecriteria-enum.md">ADCPROP_UPDATECRITERIA_ENUM</a></span><span class="sxs-lookup"><span data-stu-id="d3eed-113"><a href="adcprop-updatecriteria-enum.md">ADCPROP_UPDATECRITERIA_ENUM</a></span></span></p></td>
<td><p><span data-ttu-id="d3eed-114">Gibt an, welche Felder zum Erkennen von Konflikten während einer optimistischen Aktualisierung einer Zeile der Datenquelle mit einem <strong>Recordset</strong>-Objekt verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="d3eed-114">Specifies which fields can be used to detect conflicts during an optimistic update of a row of the data source with a <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3eed-115"><a href="adcprop-updateresync-enum.md">ADCPROP_UPDATERESYNC_ENUM</a></span><span class="sxs-lookup"><span data-stu-id="d3eed-115"><a href="adcprop-updateresync-enum.md">ADCPROP_UPDATERESYNC_ENUM</a></span></span></p></td>
<td><p><span data-ttu-id="d3eed-116">Gibt an, ob die <strong>UpdateBatch</strong>-Methode von einer impliziten <strong>Resync</strong>-Methodenoperation gefolgt wird. Ist dies der Fall, wird dadurch der Umfang einer solchen Operation festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d3eed-116">Specifies whether the <strong>UpdateBatch</strong> method is followed by an implicit <strong>Resync</strong> method operation and if so, the scope of that operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3eed-117"><a href="affectenum.md">AffectEnum</a></span><span class="sxs-lookup"><span data-stu-id="d3eed-117"><a href="affectenum.md">AffectEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d3eed-118">Gibt an, welche Datensätze von einer Operation betroffen sind.</span><span class="sxs-lookup"><span data-stu-id="d3eed-118">Specifies which records are affected by an operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3eed-119"><a href="bookmarkenum.md">BookmarkEnum</a></span><span class="sxs-lookup"><span data-stu-id="d3eed-119"><a href="bookmarkenum.md">BookmarkEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d3eed-120">Gibt eine Textmarke an, die darauf hinweist, wo die Operation beginnen soll.</span><span class="sxs-lookup"><span data-stu-id="d3eed-120">Specifies a bookmark indicating where the operation should begin.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3eed-121"><a href="commandtypeenum.md">CommandTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="d3eed-121"><a href="commandtypeenum.md">CommandTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d3eed-122">Gibt an, wie ein Befehlsargument interpretiert werden sollte.</span><span class="sxs-lookup"><span data-stu-id="d3eed-122">Specifies how a command argument should be interpreted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3eed-123"><a href="compareenum.md">CompareEnum</a></span><span class="sxs-lookup"><span data-stu-id="d3eed-123"><a href="compareenum.md">CompareEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d3eed-124">Gibt die relative Position von zwei Datensätzen an, die durch ihre Textmarken dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="d3eed-124">Specifies the relative position of two records represented by their bookmarks.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3eed-125"><a href="connectmodeenum.md">ConnectModeEnum</a></span><span class="sxs-lookup"><span data-stu-id="d3eed-125"><a href="connectmodeenum.md">ConnectModeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d3eed-126">Gibt die verfügbaren Berechtigungen zum Ändern von Daten in einer <strong>Verbindung</strong> an, wobei ein <strong>Datensatz</strong> geöffnet wird oder Werte für die <strong>Mode</strong>-Eigenschaft der <strong>Record</strong> - und <strong>Stream</strong>-Objekte angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d3eed-126">Specifies the available permissions for modifying data in a <strong>Connection</strong>, opening a <strong>Record</strong>, or specifying values for the <strong>Mode</strong> property of the <strong>Record</strong> and <strong>Stream</strong> objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3eed-127"><a href="connectoptionenum.md">ConnectOptionEnum</a></span><span class="sxs-lookup"><span data-stu-id="d3eed-127"><a href="connectoptionenum.md">ConnectOptionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d3eed-128">Gibt an, ob die <strong>Open</strong>-Methode eines <strong>Connection</strong>-Objekts zurückgegeben werden soll, nachdem (synchron) oder bevor (asynchron) die Verbindung hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="d3eed-128">Specifies whether the <strong>Open</strong> method of a <strong>Connection</strong> object should return after (synchronously) or before (asynchronously) the connection is established.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3eed-129"><a href="connectpromptenum.md">ConnectPromptEnum</a></span><span class="sxs-lookup"><span data-stu-id="d3eed-129"><a href="connectpromptenum.md">ConnectPromptEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d3eed-130">Es wird angegeben, ob ein Dialog angezeigt werden soll, der zur Eingabe fehlender Parameter auffordert, wenn eine Verbindung mit einer ODBC-Datenquelle geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="d3eed-130">Specifies whether a dialog box should be displayed to prompt for missing parameters when opening a connection to an ODBC data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3eed-131"><a href="copyrecordoptionsenum.md">CopyRecordOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="d3eed-131"><a href="copyrecordoptionsenum.md">CopyRecordOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d3eed-132">Gibt das Verhalten der <strong>CopyRecord</strong>-Methode an.</span><span class="sxs-lookup"><span data-stu-id="d3eed-132">Specifies the behavior of the <strong>CopyRecord</strong> method.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3eed-133"><a href="cursorlocationenum.md">CursorLocationEnum</a></span><span class="sxs-lookup"><span data-stu-id="d3eed-133"><a href="cursorlocationenum.md">CursorLocationEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d3eed-134">Der Speicherort des Cursormoduls wird angegeben.</span><span class="sxs-lookup"><span data-stu-id="d3eed-134">Specifies the location of the cursor engine.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3eed-135"><a href="cursoroptionenum.md">CursorOptionEnum</a></span><span class="sxs-lookup"><span data-stu-id="d3eed-135"><a href="cursoroptionenum.md">CursorOptionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d3eed-136">Gibt an, welche Funktionalität die <strong>Supports</strong>-Methode testen soll.</span><span class="sxs-lookup"><span data-stu-id="d3eed-136">Specifies what functionality the <strong>Supports</strong> method should test for.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3eed-137"><a href="cursortypeenum.md">CursorTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="d3eed-137"><a href="cursortypeenum.md">CursorTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d3eed-138">Gibt den in einem <strong>Recordset</strong>-Objekt verwendeten Cursortyp an.</span><span class="sxs-lookup"><span data-stu-id="d3eed-138">Specifies the type of cursor used in a <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3eed-139"><a href="datatypeenum.md">DataTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="d3eed-139"><a href="datatypeenum.md">DataTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d3eed-140">Gibt den Datentyp eines <strong>Felds</strong>, eines <strong>Parameters</strong> oder einer <strong>Eigenschaft</strong> an.</span><span class="sxs-lookup"><span data-stu-id="d3eed-140">Specifies the data type of a <strong>Field</strong>, <strong>Parameter</strong>, or <strong>Property</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3eed-141"><a href="editmodeenum.md">EditModeEnum</a></span><span class="sxs-lookup"><span data-stu-id="d3eed-141"><a href="editmodeenum.md">EditModeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d3eed-142">Gibt den Bearbeitungsstatus eines Datensatzes an.</span><span class="sxs-lookup"><span data-stu-id="d3eed-142">Specifies the editing status of a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3eed-143"><a href="errorvalueenum.md">ErrorValueEnum</a></span><span class="sxs-lookup"><span data-stu-id="d3eed-143"><a href="errorvalueenum.md">ErrorValueEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d3eed-144">Gibt den Typ des ADO-Laufzeitfehlers an.</span><span class="sxs-lookup"><span data-stu-id="d3eed-144">Specifies the type of ADO run-time error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3eed-145"><a href="eventreasonenum.md">EventReasonEnum</a></span><span class="sxs-lookup"><span data-stu-id="d3eed-145"><a href="eventreasonenum.md">EventReasonEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d3eed-146">Gibt den Grund an, der zu einem Ereignis führte.</span><span class="sxs-lookup"><span data-stu-id="d3eed-146">Specifies the reason that caused an event to occur.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3eed-147"><a href="eventstatusenum.md">EventStatusEnum</a></span><span class="sxs-lookup"><span data-stu-id="d3eed-147"><a href="eventstatusenum.md">EventStatusEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d3eed-148">Gibt den aktuellen Status der Ausführung eines Ereignisses an.</span><span class="sxs-lookup"><span data-stu-id="d3eed-148">Specifies the current status of the execution of an event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3eed-149"><a href="executeoptionenum.md">ExecuteOptionEnum</a></span><span class="sxs-lookup"><span data-stu-id="d3eed-149"><a href="executeoptionenum.md">ExecuteOptionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d3eed-150">Gibt an, wie ein Anbieter einen Befehl ausführen sollte.</span><span class="sxs-lookup"><span data-stu-id="d3eed-150">Specifies how a provider should execute a command.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3eed-151"><a href="fieldenum.md">FieldEnum</a></span><span class="sxs-lookup"><span data-stu-id="d3eed-151"><a href="fieldenum.md">FieldEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d3eed-152">Gibt die speziellen Felder an, auf die in der <strong>Fields</strong>-Auflistung eines <strong>Record</strong>-Objekts verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="d3eed-152">Specifies the special fields referenced in a <strong>Record</strong> object's <strong>Fields</strong> collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3eed-153"><a href="fieldattributeenum.md">FieldAttributeEnum</a></span><span class="sxs-lookup"><span data-stu-id="d3eed-153"><a href="fieldattributeenum.md">FieldAttributeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d3eed-154">Gibt mindestens ein Attribut eines <strong>Field</strong>-Objekts an.</span><span class="sxs-lookup"><span data-stu-id="d3eed-154">Specifies one or more attributes of a <strong>Field</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3eed-155"><a href="fieldstatusenum.md">FieldStatusEnum</a></span><span class="sxs-lookup"><span data-stu-id="d3eed-155"><a href="fieldstatusenum.md">FieldStatusEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d3eed-156">Gibt den Status eines <strong>Field</strong> -Objekts an.</span><span class="sxs-lookup"><span data-stu-id="d3eed-156">Specifies the status of a <strong>Field</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3eed-157"><a href="filtergroupenum.md">FilterGroupEnum</a></span><span class="sxs-lookup"><span data-stu-id="d3eed-157"><a href="filtergroupenum.md">FilterGroupEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d3eed-158">Gibt die Gruppe der Datensätze an, die aus einem <strong>Recordset</strong> gefiltert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d3eed-158">Specifies the group of records to be filtered from a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3eed-159"><a href="getrowsoptionenum.md">GetRowsOptionEnum</a></span><span class="sxs-lookup"><span data-stu-id="d3eed-159"><a href="getrowsoptionenum.md">GetRowsOptionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d3eed-160">Gibt an, wie viele Datensätze aus einem <strong>Recordset</strong> abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d3eed-160">Specifies how many records to retrieve from a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3eed-161"><a href="isolationlevelenum.md">IsolationLevelEnum</a></span><span class="sxs-lookup"><span data-stu-id="d3eed-161"><a href="isolationlevelenum.md">IsolationLevelEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d3eed-162">Gibt die Transaktionsisolation für ein <strong>Connection</strong>-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="d3eed-162">Specifies the level of transaction isolation for a <strong>Connection</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3eed-163"><a href="lineseparatorsenum.md">LineSeparatorsEnum</a></span><span class="sxs-lookup"><span data-stu-id="d3eed-163"><a href="lineseparatorsenum.md">LineSeparatorsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d3eed-164">Gibt das Zeichen an, das als Zeilentrennzeichen in <strong>Stream</strong>-Textobjekten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d3eed-164">Specifies the character used as a line separator in text <strong>Stream</strong> objects.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3eed-165"><a href="locktypeenum.md">LockTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="d3eed-165"><a href="locktypeenum.md">LockTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d3eed-166">Gibt den Sperrentyp für Datensätze während der Bearbeitung an.</span><span class="sxs-lookup"><span data-stu-id="d3eed-166">Specifies the type of lock placed on records during editing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3eed-167"><a href="marshaloptionsenum.md">MarshalOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="d3eed-167"><a href="marshaloptionsenum.md">MarshalOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d3eed-168">Gibt an, welche Datensätze an den Server zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d3eed-168">Specifies which records should be returned to the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3eed-169"><a href="moverecordoptionsenum.md">MoveRecordOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="d3eed-169"><a href="moverecordoptionsenum.md">MoveRecordOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d3eed-170">Gibt das Verhalten der <strong>MoveRecord</strong>-Methode des <strong>Record</strong>-Objekts an.</span><span class="sxs-lookup"><span data-stu-id="d3eed-170">Specifies the behavior of the <strong>Record</strong> object <strong>MoveRecord</strong> method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3eed-171"><a href="objectstateenum.md">ObjectStateEnum</a></span><span class="sxs-lookup"><span data-stu-id="d3eed-171"><a href="objectstateenum.md">ObjectStateEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d3eed-172">Es wird angegeben, ob ein Objekt geöffnet oder geschlossen ist, eine Verbindung mit einer Datenquelle herstellt, einen Befehl ausführt oder Daten abruft.</span><span class="sxs-lookup"><span data-stu-id="d3eed-172">Specifies whether an object is open or closed, connecting to a data source, executing a command, or fetching data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3eed-173"><a href="parameterattributesenum.md">ParameterAttributesEnum</a></span><span class="sxs-lookup"><span data-stu-id="d3eed-173"><a href="parameterattributesenum.md">ParameterAttributesEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d3eed-174">Gibt die Attribute eines <strong>Parameter</strong>-Objekts an.</span><span class="sxs-lookup"><span data-stu-id="d3eed-174">Specifies the attributes of a <strong>Parameter</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3eed-175"><a href="parameterdirectionenum.md">ParameterDirectionEnum</a></span><span class="sxs-lookup"><span data-stu-id="d3eed-175"><a href="parameterdirectionenum.md">ParameterDirectionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d3eed-176">Es wird angegeben, ob das <strong>Parameter</strong>-Objekt einen Eingabeparameter und/oder einen Ausgabeparameter darstellt oder ob der Parameter der Rückgabewert aus einer gespeicherten Prozedur ist.</span><span class="sxs-lookup"><span data-stu-id="d3eed-176">Specifies whether the <strong>Parameter</strong> represents an input parameter, an output parameter, or both, or if the parameter is the return value from a stored procedure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3eed-177"><a href="persistformatenum.md">PersistFormatEnum</a></span><span class="sxs-lookup"><span data-stu-id="d3eed-177"><a href="persistformatenum.md">PersistFormatEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d3eed-178">Gibt das Format an, in dem ein <strong>Recordset</strong> gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d3eed-178">Specifies the format in which to save a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3eed-179"><a href="positionenum.md">PositionEnum</a></span><span class="sxs-lookup"><span data-stu-id="d3eed-179"><a href="positionenum.md">PositionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d3eed-180">Gibt die aktuelle Position des Datensatzzeigers innerhalb eines <strong>Recordsets</strong> an.</span><span class="sxs-lookup"><span data-stu-id="d3eed-180">Specifies the current position of the record pointer within a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3eed-181"><a href="propertyattributesenum.md">PropertyAttributesEnum</a></span><span class="sxs-lookup"><span data-stu-id="d3eed-181"><a href="propertyattributesenum.md">PropertyAttributesEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d3eed-182">Gibt die Attribute eines <strong>Property</strong>-Objekts an.</span><span class="sxs-lookup"><span data-stu-id="d3eed-182">Specifies the attributes of a <strong>Property</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3eed-183"><a href="recordcreateoptionsenum.md">RecordCreateOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="d3eed-183"><a href="recordcreateoptionsenum.md">RecordCreateOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d3eed-184">Die <strong>Open</strong>-Methode des <strong>Record</strong>-Objekts wird angegeben, sowie ob ein vorhandenes <strong>Record</strong>-Objekt geöffnet werden soll oder ob ein neues <strong>Record</strong>-Objekt erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d3eed-184">Specifies for the <strong>Record</strong> object <strong>Open</strong> method whether an existing <strong>Record</strong> should be opened, or a new <strong>Record</strong> should be created.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3eed-185"><a href="recordopenoptionsenum.md">RecordOpenOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="d3eed-185"><a href="recordopenoptionsenum.md">RecordOpenOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d3eed-p102">Optionen für das Öffnen eines <strong>Record</strong>-Objekts werden angegeben. Diese Werte können mithilfe eines OR-Operators kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="d3eed-p102">Specifies options for opening a <strong>Record</strong>. These values may be combined by using an OR operator.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3eed-188"><a href="recordstatusenum.md">RecordStatusEnum</a></span><span class="sxs-lookup"><span data-stu-id="d3eed-188"><a href="recordstatusenum.md">RecordStatusEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d3eed-189">Gibt den Status eines Datensatzes in Bezug auf Batchaktualisierungen und andere Mengenoperationen an.</span><span class="sxs-lookup"><span data-stu-id="d3eed-189">Specifies the status of a record with regard to batch updates and other bulk operations.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3eed-190"><a href="recordtypeenum.md">RecordTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="d3eed-190"><a href="recordtypeenum.md">RecordTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d3eed-191">Gibt den Typ des <strong>Record</strong>-Objekts an.</span><span class="sxs-lookup"><span data-stu-id="d3eed-191">Specifies the type of <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3eed-192"><a href="resyncenum.md">ResyncEnum</a></span><span class="sxs-lookup"><span data-stu-id="d3eed-192"><a href="resyncenum.md">ResyncEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d3eed-193">Gibt an, ob die zugrunde liegenden Werte durch einen Aufruf von <strong>Resync</strong> überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="d3eed-193">Specifies whether underlying values are overwritten by a call to <strong>Resync</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3eed-194"><a href="saveoptionsenum.md">SaveOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="d3eed-194"><a href="saveoptionsenum.md">SaveOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d3eed-p103">Gibt an, ob eine Datei erstellt oder gespeichert werden sollte, wenn die Speicherung in einem <strong>Stream</strong>-Objekt erfolgt. Die Werte können mit einem AND-Operator kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="d3eed-p103">Specifies whether a file should be created or overwritten when saving from a <strong>Stream</strong> object. The values can be combined with an AND operator.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3eed-197"><a href="schemaenum.md">SchemaEnum</a></span><span class="sxs-lookup"><span data-stu-id="d3eed-197"><a href="schemaenum.md">SchemaEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d3eed-p104">Der Typ des <strong>Recordset</strong>-Schemaobjekts wird angegeben, das von der <strong>OpenSchema</strong>-Methode abgerufen wird. Die Richtung einer Datensatzsuche innerhalb eines <strong>Recordset</strong>-Objekts wird angegeben.</span><span class="sxs-lookup"><span data-stu-id="d3eed-p104">Specifies the type of schema <strong>Recordset</strong> that the <strong>OpenSchema</strong> method retrieves. Specifies the direction of a record search within a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3eed-200"><a href="searchdirectionenum.md">SearchDirectionEnum</a></span><span class="sxs-lookup"><span data-stu-id="d3eed-200"><a href="searchdirectionenum.md">SearchDirectionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d3eed-201">Die Richtung einer Datensatzsuche innerhalb eines <strong>Recordset</strong>-Objekts wird angegeben. Der Typ des auszuführenden <strong>Seek</strong>-Vorgangs wird angegeben.</span><span class="sxs-lookup"><span data-stu-id="d3eed-201">Specifies the direction of a record search within a <strong>Recordset</strong>.Specifies the type of <strong>Seek</strong> to execute.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3eed-202"><a href="seekenum.md">SeekEnum</a></span><span class="sxs-lookup"><span data-stu-id="d3eed-202"><a href="seekenum.md">SeekEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d3eed-p105">Der Typ des auszuführenden <strong>Seek</strong>-Vorgangs wird angegeben. Optionen für das Öffnen eines <strong>Stream</strong>-Objekts werden angegeben. Die Werte können mit einem AND-Operator kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="d3eed-p105">Specifies the type of <strong>Seek</strong> to execute.Specifies options for opening a <strong>Stream</strong> object. The values can be combined with an AND operator.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3eed-205"><a href="streamopenoptionsenum.md">StreamOpenOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="d3eed-205"><a href="streamopenoptionsenum.md">StreamOpenOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d3eed-p106">Optionen für das Öffnen eines <strong>Stream</strong>-Objekts werden angegeben. Die Werte können mit einem AND-Operator kombiniert werden. Es wird angegeben, ob der gesamte Datenstrom oder die nächste Zeile aus einem <strong>Stream</strong>-Objekt gelesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="d3eed-p106">Specifies options for opening a <strong>Stream</strong> object. The values can be combined with an AND operator.Specifies whether the whole stream or the next line should be read from a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3eed-208"><a href="streamreadenum.md">StreamReadEnum</a></span><span class="sxs-lookup"><span data-stu-id="d3eed-208"><a href="streamreadenum.md">StreamReadEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d3eed-209">Es wird angegeben, ob der gesamte Datenstrom oder die nächste Zeile aus einem <strong>Stream</strong>-Objekt gelesen werden soll. Der Typ der in einem <strong>Stream</strong>-Objekt gespeicherten Daten wird angegeben.</span><span class="sxs-lookup"><span data-stu-id="d3eed-209">Specifies whether the whole stream or the next line should be read from a <strong>Stream</strong> object.Specifies the type of data stored in a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3eed-210"><a href="streamtypeenum.md">StreamTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="d3eed-210"><a href="streamtypeenum.md">StreamTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d3eed-211">Der Typ der in einem <strong>Stream</strong>-Objekt gespeicherten Daten wird angegeben. Es wird angegeben, ob ein Zeilentrennzeichen an die Zeichenfolge angefügt wird, die in ein <strong>Stream</strong>-Objekt geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="d3eed-211">Specifies the type of data stored in a <strong>Stream</strong> object.Specifies whether a line separator is appended to the string written to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3eed-212"><a href="streamwriteenum.md">StreamWriteEnum</a></span><span class="sxs-lookup"><span data-stu-id="d3eed-212"><a href="streamwriteenum.md">StreamWriteEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d3eed-213">Es wird angegeben, ob ein Zeilentrennzeichen an die Zeichenfolge angefügt wird, die in ein <strong>Stream</strong>-Objekt geschrieben wird. Das Format beim Abrufen eines <strong>Recordset</strong>-Objekts wird als Zeichenfolge angegeben.</span><span class="sxs-lookup"><span data-stu-id="d3eed-213">Specifies whether a line separator is appended to the string written to a <strong>Stream</strong> object.Specifies the format when retrieving a <strong>Recordset</strong> as a string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3eed-214"><a href="stringformatenum.md">StringFormatEnum</a></span><span class="sxs-lookup"><span data-stu-id="d3eed-214"><a href="stringformatenum.md">StringFormatEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d3eed-215">Das Format beim Abrufen eines <strong>Recordset</strong>-Objekts wird als Zeichenfolge angegeben. Die Transaktionsattribute eines <strong>Connection</strong>-Objekts werden angegeben.</span><span class="sxs-lookup"><span data-stu-id="d3eed-215">Specifies the format when retrieving a <strong>Recordset</strong> as a string.Specifies the transaction attributes of a <strong>Connection</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3eed-216"><a href="xactattributeenum.md">XactAttributeEnum</a></span><span class="sxs-lookup"><span data-stu-id="d3eed-216"><a href="xactattributeenum.md">XactAttributeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d3eed-217">Gibt die Transaktionsattribute eines <strong>Connection</strong>-Objekts an.</span><span class="sxs-lookup"><span data-stu-id="d3eed-217">Specifies the transaction attributes of a <strong>Connection</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>

