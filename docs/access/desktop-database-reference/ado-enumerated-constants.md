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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283408"
---
# <a name="ado-enumerated-constants"></a><span data-ttu-id="c424e-102">ADO-Aufzählungskonstanten</span><span class="sxs-lookup"><span data-stu-id="c424e-102">ADO enumerated constants</span></span>

<span data-ttu-id="c424e-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c424e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c424e-p101">Zur Unterstützung beim Debuggen wird in den ADO-Aufzählungen für jede Konstante ein Wert aufgelistet. Dieser Wert ist jedoch lediglich ein Hinweis und kann zwischen ADO-Versionen geändert werden. Der Code sollte nur vom Namen, nicht vom tatsächlichen Wert, der einzelnen aufgezählten Konstanten abhängen.</span><span class="sxs-lookup"><span data-stu-id="c424e-p101">To assist in debugging, the ADO enumerations list a value for each constant. However, this value is purely advisory, and may change from one release of ADO to another. Your code should only depend on the name, not the actual value, of each enumerated constant.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th><span data-ttu-id="c424e-107">AufgeZählte Konstante</span><span class="sxs-lookup"><span data-stu-id="c424e-107">Enumerated constant</span></span></th>
<th><span data-ttu-id="c424e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c424e-108">Description</span></span></th>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c424e-109"><a href="adcprop-asyncthreadpriority-enum.md">ADCPROP_ASYNCTHREADPRIORITY_ENUM</a></span><span class="sxs-lookup"><span data-stu-id="c424e-109"><a href="adcprop-asyncthreadpriority-enum.md">ADCPROP_ASYNCTHREADPRIORITY_ENUM</a></span></span></p></td>
<td><p><span data-ttu-id="c424e-110">Für ein <strong>Recordset</strong>-RDS-Objekt wird die Ausführungspriorität des asynchronen Threads angegeben, durch den Daten abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c424e-110">For an RDS <strong>Recordset</strong> object, specifies the execution priority of the asynchronous thread that retrieves data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c424e-111"><a href="adcprop-autorecalc-enum.md">ADCPROP_AUTORECALC_ENUM</a></span><span class="sxs-lookup"><span data-stu-id="c424e-111"><a href="adcprop-autorecalc-enum.md">ADCPROP_AUTORECALC_ENUM</a></span></span></p></td>
<td><p><span data-ttu-id="c424e-112">Es wird angegeben, wann durch den <strong>MSDataShape</strong>-Anbieter aggregierte und berechnete Spalten in einem hierarchischen <strong>Recordset</strong> erneut berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="c424e-112">Specifies when the <strong>MSDataShape</strong> provider re-calculates aggregate and calculated columns in a hierarchical <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c424e-113"><a href="adcprop-updatecriteria-enum.md">ADCPROP_UPDATECRITERIA_ENUM</a></span><span class="sxs-lookup"><span data-stu-id="c424e-113"><a href="adcprop-updatecriteria-enum.md">ADCPROP_UPDATECRITERIA_ENUM</a></span></span></p></td>
<td><p><span data-ttu-id="c424e-114">Es wird angegeben, welche Felder zum Erkennen von Konflikten während einer optimistischen Aktualisierung einer Zeile der Datenquelle mit einem <strong>Recordset</strong>-Objekt verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="c424e-114">Specifies which fields can be used to detect conflicts during an optimistic update of a row of the data source with a <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c424e-115"><a href="adcprop-updateresync-enum.md">ADCPROP_UPDATERESYNC_ENUM</a></span><span class="sxs-lookup"><span data-stu-id="c424e-115"><a href="adcprop-updateresync-enum.md">ADCPROP_UPDATERESYNC_ENUM</a></span></span></p></td>
<td><p><span data-ttu-id="c424e-116">Es wird angegeben, ob auf die <strong>UpdateBatch</strong>-Methode eine implizite <strong>Resync</strong>-Methodenoperation folgt, und es wird ggf. der Umfang der Operation angegeben.</span><span class="sxs-lookup"><span data-stu-id="c424e-116">Specifies whether the <strong>UpdateBatch</strong> method is followed by an implicit <strong>Resync</strong> method operation and if so, the scope of that operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c424e-117"><a href="affectenum.md">AffectEnum</a></span><span class="sxs-lookup"><span data-stu-id="c424e-117"><a href="affectenum.md">AffectEnum</a></span></span></p></td>
<td><p><span data-ttu-id="c424e-118">Es wird angegeben, welche Datensätze von einer Operation betroffen sind.</span><span class="sxs-lookup"><span data-stu-id="c424e-118">Specifies which records are affected by an operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c424e-119"><a href="bookmarkenum.md">BookmarkEnum</a></span><span class="sxs-lookup"><span data-stu-id="c424e-119"><a href="bookmarkenum.md">BookmarkEnum</a></span></span></p></td>
<td><p><span data-ttu-id="c424e-120">Eine Textmarke wird angegeben, die anzeigt, wo die Operation beginnen soll.</span><span class="sxs-lookup"><span data-stu-id="c424e-120">Specifies a bookmark indicating where the operation should begin.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c424e-121"><a href="commandtypeenum.md">CommandTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="c424e-121"><a href="commandtypeenum.md">CommandTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="c424e-122">Es wird angegeben, wie ein Befehlsargument interpretiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c424e-122">Specifies how a command argument should be interpreted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c424e-123"><a href="compareenum.md">CompareEnum</a></span><span class="sxs-lookup"><span data-stu-id="c424e-123"><a href="compareenum.md">CompareEnum</a></span></span></p></td>
<td><p><span data-ttu-id="c424e-124">Die relative Position zweier Datensätze, die von Textmarken dargestellt werden, wird angegeben.</span><span class="sxs-lookup"><span data-stu-id="c424e-124">Specifies the relative position of two records represented by their bookmarks.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c424e-125"><a href="connectmodeenum.md">ConnectModeEnum</a></span><span class="sxs-lookup"><span data-stu-id="c424e-125"><a href="connectmodeenum.md">ConnectModeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="c424e-126">Die verfügbaren Berechtigungen zum Ändern von Daten in einem <strong>Connection</strong>-Objekt, zum Öffnen eines <strong>Record</strong>-Objekts oder zum Angeben von Werten für die <strong>Mode</strong>-Eigenschaft der Objekte <strong>Record</strong> und <strong>Stream</strong> werden angegeben.</span><span class="sxs-lookup"><span data-stu-id="c424e-126">Specifies the available permissions for modifying data in a <strong>Connection</strong>, opening a <strong>Record</strong>, or specifying values for the <strong>Mode</strong> property of the <strong>Record</strong> and <strong>Stream</strong> objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c424e-127"><a href="connectoptionenum.md">ConnectOptionEnum</a></span><span class="sxs-lookup"><span data-stu-id="c424e-127"><a href="connectoptionenum.md">ConnectOptionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="c424e-128">Es wird angegeben, ob die <strong>Open</strong>-Methode eines <strong>Connection</strong>-Objekts zurückgegeben werden soll, nachdem (synchron) oder bevor (asynchron) die Verbindung hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="c424e-128">Specifies whether the <strong>Open</strong> method of a <strong>Connection</strong> object should return after (synchronously) or before (asynchronously) the connection is established.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c424e-129"><a href="connectpromptenum.md">ConnectPromptEnum</a></span><span class="sxs-lookup"><span data-stu-id="c424e-129"><a href="connectpromptenum.md">ConnectPromptEnum</a></span></span></p></td>
<td><p><span data-ttu-id="c424e-130">Es wird angegeben, ob ein Dialog angezeigt werden soll, der zur Eingabe fehlender Parameter auffordert, wenn eine Verbindung mit einer ODBC-Datenquelle geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="c424e-130">Specifies whether a dialog box should be displayed to prompt for missing parameters when opening a connection to an ODBC data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c424e-131"><a href="copyrecordoptionsenum.md">CopyRecordOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="c424e-131"><a href="copyrecordoptionsenum.md">CopyRecordOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="c424e-132">Das Verhalten der <strong>CopyRecord</strong>-Methode wird angegeben.</span><span class="sxs-lookup"><span data-stu-id="c424e-132">Specifies the behavior of the <strong>CopyRecord</strong> method.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c424e-133"><a href="cursorlocationenum.md">CursorLocationEnum</a></span><span class="sxs-lookup"><span data-stu-id="c424e-133"><a href="cursorlocationenum.md">CursorLocationEnum</a></span></span></p></td>
<td><p><span data-ttu-id="c424e-134">Der Speicherort des Cursormoduls wird angegeben.</span><span class="sxs-lookup"><span data-stu-id="c424e-134">Specifies the location of the cursor engine.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c424e-135"><a href="cursoroptionenum.md">CursorOptionEnum</a></span><span class="sxs-lookup"><span data-stu-id="c424e-135"><a href="cursoroptionenum.md">CursorOptionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="c424e-136">Es wird angegeben, auf welche Funktionalität die <strong>Supports</strong>-Methode getestet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c424e-136">Specifies what functionality the <strong>Supports</strong> method should test for.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c424e-137"><a href="cursortypeenum.md">CursorTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="c424e-137"><a href="cursortypeenum.md">CursorTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="c424e-138">Der Typ des Cursors wird angegeben, der in einem <strong>Recordset</strong>-Objekt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c424e-138">Specifies the type of cursor used in a <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c424e-139"><a href="datatypeenum.md">DataTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="c424e-139"><a href="datatypeenum.md">DataTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="c424e-140">Der Datentyp eines <strong>Field</strong>-Objekts, eines <strong>Parameter</strong>-Objekts oder eines <strong>Property</strong>-Objekts wird angegeben.</span><span class="sxs-lookup"><span data-stu-id="c424e-140">Specifies the data type of a <strong>Field</strong>, <strong>Parameter</strong>, or <strong>Property</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c424e-141"><a href="editmodeenum.md">EditModeEnum</a></span><span class="sxs-lookup"><span data-stu-id="c424e-141"><a href="editmodeenum.md">EditModeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="c424e-142">Der Bearbeitungsstatus eines Datensatzes wird angegeben.</span><span class="sxs-lookup"><span data-stu-id="c424e-142">Specifies the editing status of a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c424e-143"><a href="errorvalueenum.md">ErrorValueEnum</a></span><span class="sxs-lookup"><span data-stu-id="c424e-143"><a href="errorvalueenum.md">ErrorValueEnum</a></span></span></p></td>
<td><p><span data-ttu-id="c424e-144">Der Typ eines ADO-Laufzeitfehlers wird angegeben.</span><span class="sxs-lookup"><span data-stu-id="c424e-144">Specifies the type of ADO run-time error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c424e-145"><a href="eventreasonenum.md">EventReasonEnum</a></span><span class="sxs-lookup"><span data-stu-id="c424e-145"><a href="eventreasonenum.md">EventReasonEnum</a></span></span></p></td>
<td><p><span data-ttu-id="c424e-146">Der Grund für das Auftreten eines Ereignisses wird angegeben.</span><span class="sxs-lookup"><span data-stu-id="c424e-146">Specifies the reason that caused an event to occur.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c424e-147"><a href="eventstatusenum.md">EventStatusEnum</a></span><span class="sxs-lookup"><span data-stu-id="c424e-147"><a href="eventstatusenum.md">EventStatusEnum</a></span></span></p></td>
<td><p><span data-ttu-id="c424e-148">Der aktuelle Status der Ausführung eines Ereignisses wird angegeben.</span><span class="sxs-lookup"><span data-stu-id="c424e-148">Specifies the current status of the execution of an event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c424e-149"><a href="executeoptionenum.md">ExecuteOptionEnum</a></span><span class="sxs-lookup"><span data-stu-id="c424e-149"><a href="executeoptionenum.md">ExecuteOptionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="c424e-150">Es wird angegeben, wie ein Befehl von einem Anbieter ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c424e-150">Specifies how a provider should execute a command.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c424e-151"><a href="fieldenum.md">FieldEnum</a></span><span class="sxs-lookup"><span data-stu-id="c424e-151"><a href="fieldenum.md">FieldEnum</a></span></span></p></td>
<td><p><span data-ttu-id="c424e-152">Die speziellen Felder werden angegeben, auf die in der <strong>Field</strong>-Auflistung eines <strong>Record</strong>-Objekts verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="c424e-152">Specifies the special fields referenced in a <strong>Record</strong> object's <strong>Fields</strong> collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c424e-153"><a href="fieldattributeenum.md">FieldAttributeEnum</a></span><span class="sxs-lookup"><span data-stu-id="c424e-153"><a href="fieldattributeenum.md">FieldAttributeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="c424e-154">Eines oder mehrere Attribute eines <strong>Field</strong>-Objekts werden angegeben.</span><span class="sxs-lookup"><span data-stu-id="c424e-154">Specifies one or more attributes of a <strong>Field</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c424e-155"><a href="fieldstatusenum.md">FieldStatusEnum</a></span><span class="sxs-lookup"><span data-stu-id="c424e-155"><a href="fieldstatusenum.md">FieldStatusEnum</a></span></span></p></td>
<td><p><span data-ttu-id="c424e-156">Der Status eines <strong>Field</strong>-Objekts wird angegeben.</span><span class="sxs-lookup"><span data-stu-id="c424e-156">Specifies the status of a <strong>Field</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c424e-157"><a href="filtergroupenum.md">FilterGroupEnum</a></span><span class="sxs-lookup"><span data-stu-id="c424e-157"><a href="filtergroupenum.md">FilterGroupEnum</a></span></span></p></td>
<td><p><span data-ttu-id="c424e-158">Die Gruppe der zu filternden Datensätze aus einem <strong>Recordset</strong>-Objekt wird angegeben.</span><span class="sxs-lookup"><span data-stu-id="c424e-158">Specifies the group of records to be filtered from a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c424e-159"><a href="getrowsoptionenum.md">GetRowsOptionEnum</a></span><span class="sxs-lookup"><span data-stu-id="c424e-159"><a href="getrowsoptionenum.md">GetRowsOptionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="c424e-160">Es wird angegeben, wie viele Datensätze aus einem <strong>Recordset</strong>-Objekt abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c424e-160">Specifies how many records to retrieve from a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c424e-161"><a href="isolationlevelenum.md">IsolationLevelEnum</a></span><span class="sxs-lookup"><span data-stu-id="c424e-161"><a href="isolationlevelenum.md">IsolationLevelEnum</a></span></span></p></td>
<td><p><span data-ttu-id="c424e-162">Die Transaktionsisolationsstufe für ein <strong>Connection</strong>-Objekt wird angegeben.</span><span class="sxs-lookup"><span data-stu-id="c424e-162">Specifies the level of transaction isolation for a <strong>Connection</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c424e-163"><a href="lineseparatorsenum.md">LineSeparatorsEnum</a></span><span class="sxs-lookup"><span data-stu-id="c424e-163"><a href="lineseparatorsenum.md">LineSeparatorsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="c424e-164">Es wird das Zeichen angegeben, das als Zeilentrennzeichen in <strong>Stream</strong>-Textobjekten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c424e-164">Specifies the character used as a line separator in text <strong>Stream</strong> objects.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c424e-165"><a href="locktypeenum.md">LockTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="c424e-165"><a href="locktypeenum.md">LockTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="c424e-166">Es wird der Typ der Sperrung angegeben, die während der Bearbeitung für Datensätze festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c424e-166">Specifies the type of lock placed on records during editing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c424e-167"><a href="marshaloptionsenum.md">MarshalOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="c424e-167"><a href="marshaloptionsenum.md">MarshalOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="c424e-168">Es wird angegeben, welche Datensätze an den Server zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c424e-168">Specifies which records should be returned to the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c424e-169"><a href="moverecordoptionsenum.md">MoveRecordOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="c424e-169"><a href="moverecordoptionsenum.md">MoveRecordOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="c424e-170">Das Verhalten der <strong>MoveRecord</strong>-Methode des <strong>Record</strong>-Objekts wird angegeben.</span><span class="sxs-lookup"><span data-stu-id="c424e-170">Specifies the behavior of the <strong>Record</strong> object <strong>MoveRecord</strong> method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c424e-171"><a href="objectstateenum.md">ObjectStateEnum</a></span><span class="sxs-lookup"><span data-stu-id="c424e-171"><a href="objectstateenum.md">ObjectStateEnum</a></span></span></p></td>
<td><p><span data-ttu-id="c424e-172">Es wird angegeben, ob ein Objekt geöffnet oder geschlossen ist, eine Verbindung mit einer Datenquelle herstellt, einen Befehl ausführt oder Daten abruft.</span><span class="sxs-lookup"><span data-stu-id="c424e-172">Specifies whether an object is open or closed, connecting to a data source, executing a command, or fetching data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c424e-173"><a href="parameterattributesenum.md">ParameterAttributesEnum</a></span><span class="sxs-lookup"><span data-stu-id="c424e-173"><a href="parameterattributesenum.md">ParameterAttributesEnum</a></span></span></p></td>
<td><p><span data-ttu-id="c424e-174">Die Attribute eines <strong>Parameter</strong>-Objekts werden angegeben.</span><span class="sxs-lookup"><span data-stu-id="c424e-174">Specifies the attributes of a <strong>Parameter</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c424e-175"><a href="parameterdirectionenum.md">ParameterDirectionEnum</a></span><span class="sxs-lookup"><span data-stu-id="c424e-175"><a href="parameterdirectionenum.md">ParameterDirectionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="c424e-176">Es wird angegeben, ob das <strong>Parameter</strong>-Objekt einen Eingabeparameter und/oder einen Ausgabeparameter darstellt oder ob der Parameter der Rückgabewert aus einer gespeicherten Prozedur ist.</span><span class="sxs-lookup"><span data-stu-id="c424e-176">Specifies whether the <strong>Parameter</strong> represents an input parameter, an output parameter, or both, or if the parameter is the return value from a stored procedure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c424e-177"><a href="persistformatenum.md">PersistFormatEnum</a></span><span class="sxs-lookup"><span data-stu-id="c424e-177"><a href="persistformatenum.md">PersistFormatEnum</a></span></span></p></td>
<td><p><span data-ttu-id="c424e-178">Es wird das Format angegeben, in dem ein <strong>Recordset</strong>-Objekt gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c424e-178">Specifies the format in which to save a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c424e-179"><a href="positionenum.md">PositionEnum</a></span><span class="sxs-lookup"><span data-stu-id="c424e-179"><a href="positionenum.md">PositionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="c424e-180">Die aktuelle Position des Datensatzzeigers innerhalb eines <strong>Recordset</strong>-Objekts wird angegeben.</span><span class="sxs-lookup"><span data-stu-id="c424e-180">Specifies the current position of the record pointer within a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c424e-181"><a href="propertyattributesenum.md">PropertyAttributesEnum</a></span><span class="sxs-lookup"><span data-stu-id="c424e-181"><a href="propertyattributesenum.md">PropertyAttributesEnum</a></span></span></p></td>
<td><p><span data-ttu-id="c424e-182">Die Attribute eines <strong>Property</strong>-Objekts werden angegeben.</span><span class="sxs-lookup"><span data-stu-id="c424e-182">Specifies the attributes of a <strong>Property</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c424e-183"><a href="recordcreateoptionsenum.md">RecordCreateOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="c424e-183"><a href="recordcreateoptionsenum.md">RecordCreateOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="c424e-184">Die <strong>Open</strong>-Methode des <strong>Record</strong>-Objekts wird angegeben, sowie ob ein vorhandenes <strong>Record</strong>-Objekt geöffnet werden soll oder ob ein neues <strong>Record</strong>-Objekt erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c424e-184">Specifies for the <strong>Record</strong> object <strong>Open</strong> method whether an existing <strong>Record</strong> should be opened, or a new <strong>Record</strong> should be created.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c424e-185"><a href="recordopenoptionsenum.md">RecordOpenOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="c424e-185"><a href="recordopenoptionsenum.md">RecordOpenOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="c424e-186">Optionen für das Öffnen eines <strong>Record</strong>-Objekts werden angegeben.</span><span class="sxs-lookup"><span data-stu-id="c424e-186">Specifies options for opening a <strong>Record</strong>.</span></span> <span data-ttu-id="c424e-187">Diese Werte können mithilfe eines OR-Operators kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="c424e-187">These values may be combined by using an OR operator.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c424e-188"><a href="recordstatusenum.md">RecordStatusEnum</a></span><span class="sxs-lookup"><span data-stu-id="c424e-188"><a href="recordstatusenum.md">RecordStatusEnum</a></span></span></p></td>
<td><p><span data-ttu-id="c424e-189">Der Status eines Datensatzes in Bezug auf Batchaktualisierungen und andere Mengenoperationen wird angegeben.</span><span class="sxs-lookup"><span data-stu-id="c424e-189">Specifies the status of a record with regard to batch updates and other bulk operations.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c424e-190"><a href="recordtypeenum.md">RecordTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="c424e-190"><a href="recordtypeenum.md">RecordTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="c424e-191">Der Typ eines <strong>Record</strong>-Objekts wird angegeben.</span><span class="sxs-lookup"><span data-stu-id="c424e-191">Specifies the type of <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c424e-192"><a href="resyncenum.md">ResyncEnum</a></span><span class="sxs-lookup"><span data-stu-id="c424e-192"><a href="resyncenum.md">ResyncEnum</a></span></span></p></td>
<td><p><span data-ttu-id="c424e-193">Es wird angegeben, ob zugrunde liegende Werte durch einen Aufruf von <strong>Resync</strong> überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="c424e-193">Specifies whether underlying values are overwritten by a call to <strong>Resync</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c424e-194"><a href="saveoptionsenum.md">SaveOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="c424e-194"><a href="saveoptionsenum.md">SaveOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="c424e-p103">Gibt an, ob eine Datei erstellt oder gespeichert werden sollte, wenn die Speicherung in einem <strong>Stream</strong>-Objekt erfolgt. Die Werte können mit einem AND-Operator kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="c424e-p103">Specifies whether a file should be created or overwritten when saving from a <strong>Stream</strong> object. The values can be combined with an AND operator.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c424e-197"><a href="schemaenum.md">SchemaEnum</a></span><span class="sxs-lookup"><span data-stu-id="c424e-197"><a href="schemaenum.md">SchemaEnum</a></span></span></p></td>
<td><p><span data-ttu-id="c424e-198">Der Typ des <strong>Recordset</strong>-Schemaobjekts wird angegeben, das von der <strong>OpenSchema</strong>-Methode abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c424e-198">Specifies the type of schema <strong>Recordset</strong> that the <strong>OpenSchema</strong> method retrieves.</span></span> <span data-ttu-id="c424e-199">Die Richtung einer Datensatzsuche innerhalb eines <strong>Recordset</strong>-Objekts wird angegeben.</span><span class="sxs-lookup"><span data-stu-id="c424e-199">Specifies the direction of a record search within a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c424e-200"><a href="searchdirectionenum.md">SearchDirectionEnum</a></span><span class="sxs-lookup"><span data-stu-id="c424e-200"><a href="searchdirectionenum.md">SearchDirectionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="c424e-201">Die Richtung einer Datensatzsuche innerhalb eines <strong>Recordset</strong>-Objekts wird angegeben. Der Typ des auszuführenden <strong>Seek</strong>-Vorgangs wird angegeben.</span><span class="sxs-lookup"><span data-stu-id="c424e-201">Specifies the direction of a record search within a <strong>Recordset</strong>.Specifies the type of <strong>Seek</strong> to execute.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c424e-202"><a href="seekenum.md">SeekEnum</a></span><span class="sxs-lookup"><span data-stu-id="c424e-202"><a href="seekenum.md">SeekEnum</a></span></span></p></td>
<td><p><span data-ttu-id="c424e-p105">Der Typ des auszuführenden <strong>Seek</strong>-Vorgangs wird angegeben. Optionen für das Öffnen eines <strong>Stream</strong>-Objekts werden angegeben. Die Werte können mit einem AND-Operator kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="c424e-p105">Specifies the type of <strong>Seek</strong> to execute.Specifies options for opening a <strong>Stream</strong> object. The values can be combined with an AND operator.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c424e-205"><a href="streamopenoptionsenum.md">StreamOpenOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="c424e-205"><a href="streamopenoptionsenum.md">StreamOpenOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="c424e-p106">Optionen für das Öffnen eines <strong>Stream</strong>-Objekts werden angegeben. Die Werte können mit einem AND-Operator kombiniert werden. Es wird angegeben, ob der gesamte Datenstrom oder die nächste Zeile aus einem <strong>Stream</strong>-Objekt gelesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c424e-p106">Specifies options for opening a <strong>Stream</strong> object. The values can be combined with an AND operator.Specifies whether the whole stream or the next line should be read from a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c424e-208"><a href="streamreadenum.md">StreamReadEnum</a></span><span class="sxs-lookup"><span data-stu-id="c424e-208"><a href="streamreadenum.md">StreamReadEnum</a></span></span></p></td>
<td><p><span data-ttu-id="c424e-209">Es wird angegeben, ob der gesamte Datenstrom oder die nächste Zeile aus einem <strong>Stream</strong>-Objekt gelesen werden soll. Der Typ der in einem <strong>Stream</strong>-Objekt gespeicherten Daten wird angegeben.</span><span class="sxs-lookup"><span data-stu-id="c424e-209">Specifies whether the whole stream or the next line should be read from a <strong>Stream</strong> object.Specifies the type of data stored in a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c424e-210"><a href="streamtypeenum.md">StreamTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="c424e-210"><a href="streamtypeenum.md">StreamTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="c424e-211">Der Typ der in einem <strong>Stream</strong>-Objekt gespeicherten Daten wird angegeben. Es wird angegeben, ob ein Zeilentrennzeichen an die Zeichenfolge angefügt wird, die in ein <strong>Stream</strong>-Objekt geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="c424e-211">Specifies the type of data stored in a <strong>Stream</strong> object.Specifies whether a line separator is appended to the string written to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c424e-212"><a href="streamwriteenum.md">StreamWriteEnum</a></span><span class="sxs-lookup"><span data-stu-id="c424e-212"><a href="streamwriteenum.md">StreamWriteEnum</a></span></span></p></td>
<td><p><span data-ttu-id="c424e-213">Es wird angegeben, ob ein Zeilentrennzeichen an die Zeichenfolge angefügt wird, die in ein <strong>Stream</strong>-Objekt geschrieben wird. Das Format beim Abrufen eines <strong>Recordset</strong>-Objekts wird als Zeichenfolge angegeben.</span><span class="sxs-lookup"><span data-stu-id="c424e-213">Specifies whether a line separator is appended to the string written to a <strong>Stream</strong> object.Specifies the format when retrieving a <strong>Recordset</strong> as a string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c424e-214"><a href="stringformatenum.md">StringFormatEnum</a></span><span class="sxs-lookup"><span data-stu-id="c424e-214"><a href="stringformatenum.md">StringFormatEnum</a></span></span></p></td>
<td><p><span data-ttu-id="c424e-215">Das Format beim Abrufen eines <strong>Recordset</strong>-Objekts wird als Zeichenfolge angegeben. Die Transaktionsattribute eines <strong>Connection</strong>-Objekts werden angegeben.</span><span class="sxs-lookup"><span data-stu-id="c424e-215">Specifies the format when retrieving a <strong>Recordset</strong> as a string.Specifies the transaction attributes of a <strong>Connection</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c424e-216"><a href="xactattributeenum.md">XactAttributeEnum</a></span><span class="sxs-lookup"><span data-stu-id="c424e-216"><a href="xactattributeenum.md">XactAttributeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="c424e-217">Gibt die Transaktionsattribute eines <strong>Connection</strong>-Objekts an.</span><span class="sxs-lookup"><span data-stu-id="c424e-217">Specifies the transaction attributes of a <strong>Connection</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>

