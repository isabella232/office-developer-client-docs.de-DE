---
title: TableDef. openRecordset-Methode (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: f4c9c89c-3348-d3c9-ce76-dd11e5ee11a7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836703(v=office.15)
ms:contentKeyID: 48548696
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2035d4319f7821f2a0469193955c732231f30cf0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314336"
---
# <a name="tabledefopenrecordset-method-dao"></a><span data-ttu-id="92955-102">TableDef. openRecordset-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="92955-102">TableDef.OpenRecordset method (DAO)</span></span>

<span data-ttu-id="92955-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="92955-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="92955-104">Erstellt ein neues **[Recordset](recordset-object-dao.md)** -Objekt und fügt es an die **Recordsets**-Auflistung an.</span><span class="sxs-lookup"><span data-stu-id="92955-104">Creates a new **[Recordset](recordset-object-dao.md)** object and appends it to the **Recordsets** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="92955-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="92955-105">Syntax</span></span>

<span data-ttu-id="92955-106">*Ausdruck* . OpenRecordset (***Type***, ***options***)</span><span class="sxs-lookup"><span data-stu-id="92955-106">*expression* .OpenRecordset(***Type***, ***Options***)</span></span>

<span data-ttu-id="92955-107">*Ausdruck* Eine Variable, die ein **TableDef** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="92955-107">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="92955-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="92955-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="92955-109">Name</span><span class="sxs-lookup"><span data-stu-id="92955-109">Name</span></span></p></th>
<th><p><span data-ttu-id="92955-110">Erforderlich/optional</span><span class="sxs-lookup"><span data-stu-id="92955-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="92955-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="92955-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="92955-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="92955-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="92955-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="92955-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="92955-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="92955-114">Required</span></span></p></td>
<td><p><span data-ttu-id="92955-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="92955-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="92955-p101">Die Quelle der Datensätze für das neue <strong>Recordset</strong>. Die Quelle kann ein Tabellenname, ein Abfragename oder eine SQL-Anweisung sein, die Datensätze zurückgibt. Für <strong>Recordset</strong> -Objekte vom "table"-Typ in Microsoft Access-Datenbankmodul-Datenbanken kann die Quelle nur ein Tabellenname sein.  </span><span class="sxs-lookup"><span data-stu-id="92955-p101">The source of the records for the new <strong>Recordset</strong>. The source can be a table name, a query name, or an SQL statement that returns records. For table-type <strong>Recordset</strong> objects in Microsoft Access database engine databases, the source can only be a table name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="92955-119"><em>Type</em></span><span class="sxs-lookup"><span data-stu-id="92955-119"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="92955-120">Optional</span><span class="sxs-lookup"><span data-stu-id="92955-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="92955-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="92955-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="92955-122">Eine <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> -Konstante gibt den Typ des zu öffnenden <strong>Recordset</strong> an.</span><span class="sxs-lookup"><span data-stu-id="92955-122">A <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> constant that indicates the type of <strong>Recordset</strong> to open.</span></span></p><p><span data-ttu-id="92955-123"><strong>Hinweis</strong>: Wenn Sie ein <STRONG>Recordset</STRONG> -Objekt in einem Microsoft Access-Arbeitsbereich öffnen und keinen Typ angeben, erstellt OpenRecordset, falls möglich, ein <STRONG>Recordset</STRONG>vom Tabellentyp. <STRONG></STRONG></span><span class="sxs-lookup"><span data-stu-id="92955-123"><strong>NOTE</strong>: If you open a <STRONG>Recordset</STRONG> in a Microsoft Access workspace and you don't specify a type, <STRONG>OpenRecordset</STRONG> creates a table-type <STRONG>Recordset</STRONG>, if possible.</span></span> <span data-ttu-id="92955-124">If you specify a linked table or query, <STRONG>OpenRecordset</STRONG> creates a dynaset-type <STRONG>Recordset</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="92955-124">If you specify a linked table or query, <STRONG>OpenRecordset</STRONG> creates a dynaset-type <STRONG>Recordset</STRONG>.</span></span></p>
</td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="92955-125"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="92955-125"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="92955-126">Optional</span><span class="sxs-lookup"><span data-stu-id="92955-126">Optional</span></span></p></td>
<td><p><span data-ttu-id="92955-127"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="92955-127"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="92955-128">Eine Kombination aus <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> -Konstanten, die Merkmale des neuen <strong>Recordset</strong> angeben.</span><span class="sxs-lookup"><span data-stu-id="92955-128">A combination of <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> constants that specify characteristics of the new <strong>Recordset</strong>.</span></span></p><p><span data-ttu-id="92955-129"><strong>Hinweis</strong>: die Konstanten <STRONG>dbConsistent</STRONG> und <STRONG>dbInconsistent</STRONG> schließen sich gegenseitig aus, und die Verwendung von beidem verursacht einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="92955-129"><strong>NOTE</strong>: The constants <STRONG>dbConsistent</STRONG> and <STRONG>dbInconsistent</STRONG> are mutually exclusive, and using both causes an error.</span></span> <span data-ttu-id="92955-130">Supplying a lockedits argument when options uses the <STRONG>dbReadOnly</STRONG> constant also causes an error.</span><span class="sxs-lookup"><span data-stu-id="92955-130">Supplying a lockedits argument when options uses the <STRONG>dbReadOnly</STRONG> constant also causes an error.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="92955-131"><em>Bearbeitsperr</em></span><span class="sxs-lookup"><span data-stu-id="92955-131"><em>LockEdit</em></span></span></p></td>
<td><p><span data-ttu-id="92955-132">Optional</span><span class="sxs-lookup"><span data-stu-id="92955-132">Optional</span></span></p></td>
<td><p><span data-ttu-id="92955-133"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="92955-133"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="92955-134">Eine <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> -Konstante, die die Sperre für das <strong>Recordset</strong> bestimmt.</span><span class="sxs-lookup"><span data-stu-id="92955-134">A <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> constant that determines the locking for the <strong>Recordset</strong>.</span></span></p><p><span data-ttu-id="92955-135"><strong>Hinweis</strong>: Sie können <STRONG>dbReadOnly</STRONG> entweder im Options-oder im LockEdits-Argument verwenden, jedoch nicht in beiden.</span><span class="sxs-lookup"><span data-stu-id="92955-135"><strong>NOTE</strong>: You can use <STRONG>dbReadOnly</STRONG> in either the options argument or the lockedits argument, but not both.</span></span> <span data-ttu-id="92955-136">Wenn Sie es für beide Argumente verwenden, tritt ein Laufzeitfehler auf.</span><span class="sxs-lookup"><span data-stu-id="92955-136">If you use it for both arguments, a run-time error occurs.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="92955-137">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="92955-137">Return value</span></span>

<span data-ttu-id="92955-138">Recordset</span><span class="sxs-lookup"><span data-stu-id="92955-138">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="92955-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="92955-139">Remarks</span></span>

<span data-ttu-id="92955-p105">Wenn der Benutzer beim Aktualisieren eines Datensatzes diesen Fehler erhält, sollte der Code den Inhalt des Felds aktualisieren und die geänderten Werte abrufen. Tritt der Fehler beim Löschen eines Datensatzes auf, sollte der Code die Daten des neuen Datensatzes anzeigen und eine Meldung darüber ausgeben, dass die Daten kürzlich geändert wurden. An dieser Stelle könnte der Code bestätigen lassen, dass der Benutzer den Datensatz wirklich löschen möchte.</span><span class="sxs-lookup"><span data-stu-id="92955-p105">Typically, if the user gets this error while updating a record, your code should refresh the contents of the fields and retrieve the newly modified values. If the error occurs while deleting a record, your code could display the new record data to the user and a message indicating that the data has recently changed. At this point, your code can request a confirmation that the user still wants to delete the record.</span></span>

<span data-ttu-id="92955-143">Sie sollten die **dbSeeChanges**-Konstante auch dann verwenden, wenn Sie ein **Recordset** in einem mit einem Microsoft Access-Datenbankmodul verbundenen ODBC-Arbeitsbereich in einer Microsoft SQL Server 6.0-Tabelle (oder höher) öffnen, die über eine IDENTITY-Spalte verfügt. Andernfalls tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="92955-143">You should also use the **dbSeeChanges** constant if you open a **Recordset** in a Microsoft Access database engine-connected ODBC workspace against a Microsoft SQL Server 6.0 (or later) table that has an IDENTITY column, otherwise an error may result.</span></span>

<span data-ttu-id="92955-p106">Das Öffnen mehrerer **Recordset**-Objekte in einer ODBC-Datenquelle kann fehlschlagen, wenn die Verbindung durch einen vorherigen **OpenRecordset**-Aufruf ausgelastet ist. Das könnten Sie beispielsweise dadurch verhindern, dass Sie das **Recordset**-Objekt mithilfe der **MoveLast**-Methode vollständig auffüllen, sobald das **Recordset**-Objekt geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="92955-p106">Opening more than one **Recordset** on an ODBC data source may fail because the connection is busy with a prior **OpenRecordset** call. One way around this is to fully populate the **Recordset** by using the **MoveLast** method as soon as the **Recordset** is opened.</span></span>

<span data-ttu-id="92955-146">Beim Schließen eines **Recordset**-Objekts mit der **[Close](connection-close-method-dao.md)** -Methode wird es automatisch aus der **Recordsets**-Auflistung gelöscht.</span><span class="sxs-lookup"><span data-stu-id="92955-146">Closing a **Recordset** with the **[Close](connection-close-method-dao.md)** method automatically deletes it from the **Recordsets** collection.</span></span>

> [!NOTE]
> <span data-ttu-id="92955-147">Wenn *Source* auf eine SQL-Anweisung verweist, die aus einer mit einem nicht-ganzzahligen Wert verketteten Zeichenfolge besteht, und die Systemparameter ein nicht-U. S. Decimal-Zeichen wie ein Komma (beispielsweise &gt; strSQL &amp; = "Price" lngPrice und lngPrice = 125, 50), tritt ein Fehler auf, wenn Sie versuchen, das **Recordset**-Objekt zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="92955-147">If *source* refers to an SQL statement composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error occurs when you try to open the **Recordset**.</span></span> <span data-ttu-id="92955-148">Der Grund ist, dass die Zahl bei der Verkettung mithilfe des Standarddezimalzeichens des Systems in eine Zeichenfolge umgewandelt wird und SQL nur für die USA gültige Dezimalzeichen akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="92955-148">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and SQL only accepts U.S. decimal characters.</span></span>


