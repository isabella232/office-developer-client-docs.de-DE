---
title: Recordset.OpenRecordset-Methode (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: 7d5ca4d5-5a0b-c0c8-d8e8-2c4e6c5f361f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196402(v=office.15)
ms:contentKeyID: 48545853
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 11d525abdb7c5cbd4ef72e81d856d2abfc6a3045
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284490"
---
# <a name="recordsetopenrecordset-method-dao"></a><span data-ttu-id="39da8-102">Recordset.OpenRecordset-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="39da8-102">Recordset.OpenRecordset Method (DAO)</span></span>

<span data-ttu-id="39da8-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="39da8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="39da8-104">Erstellt ein neues **[Recordset](recordset-object-dao.md)**-Objekt und fügt es an die **Recordsets**-Auflistung an.</span><span class="sxs-lookup"><span data-stu-id="39da8-104">Creates a new **[Recordset](recordset-object-dao.md)** object and appends it to the **Recordsets** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="39da8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="39da8-105">Syntax</span></span>

<span data-ttu-id="39da8-106">*expression* .OpenRecordset(***Type***, ***Options***)</span><span class="sxs-lookup"><span data-stu-id="39da8-106">*expression* .OpenRecordset(***Type***, ***Options***)</span></span>

<span data-ttu-id="39da8-107">*Ausdruck* Eine Variable, die ein **Recordset**-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="39da8-107">*expression*  A variable that represents a **Recordset** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="39da8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="39da8-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="39da8-109">Name</span><span class="sxs-lookup"><span data-stu-id="39da8-109">Name</span></span></p></th>
<th><p><span data-ttu-id="39da8-110">Erforderlich/optional</span><span class="sxs-lookup"><span data-stu-id="39da8-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="39da8-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="39da8-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="39da8-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="39da8-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="39da8-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="39da8-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="39da8-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="39da8-114">Required</span></span></p></td>
<td><p><span data-ttu-id="39da8-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="39da8-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="39da8-p101">Die Quelle der Datensätze für das neue  <strong>Recordset</strong>. Die Quelle kann ein Tabellenname, ein Abfragename oder eine SQL-Anweisung sein, die Datensätze zurückgibt. Für <strong>Recordset</strong>-Objekte vom "table"-Typ in Microsoft Access-Datenbankmodul-Datenbanken kann die Quelle nur ein Tabellenname sein.</span><span class="sxs-lookup"><span data-stu-id="39da8-p101">The source of the records for the new <strong>Recordset</strong>. The source can be a table name, a query name, or an SQL statement that returns records. For table-type <strong>Recordset</strong> objects in Microsoft Access database engine databases, the source can only be a table name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39da8-119"><em>Typ</em></span><span class="sxs-lookup"><span data-stu-id="39da8-119"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="39da8-120">Optional</span><span class="sxs-lookup"><span data-stu-id="39da8-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="39da8-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="39da8-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="39da8-122">Eine <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong>-Konstante gibt den Typ des zu öffnenden <strong>Recordset</strong> an.</span><span class="sxs-lookup"><span data-stu-id="39da8-122">A <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> constant that indicates the type of <strong>Recordset</strong> to open.</span></span></p><p><span data-ttu-id="39da8-123"><strong>Hinweis</strong>: Wenn Sie ein <STRONG>Recordset</STRONG> in einem Microsoft Access-Arbeitsbereich öffnen und keinen Typ angeben, erstellt <STRONG>OpenRecordset</STRONG>, wenn möglich, ein tabellenartiges <STRONG>Recordset</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="39da8-123"> > If you open a Recordset in a Microsoft Access workspace and you don't specify a type, OpenRecordset creates a table-type Recordset, if possible.</span></span> <span data-ttu-id="39da8-124">If you specify a linked table or query, <STRONG>OpenRecordset</STRONG> creates a dynaset-type <STRONG>Recordset</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="39da8-124">If you specify a linked table or query, <STRONG>OpenRecordset</STRONG> creates a dynaset-type <STRONG>Recordset</STRONG>.</span></span></p>
</td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39da8-125"><em>Optionen</em></span><span class="sxs-lookup"><span data-stu-id="39da8-125"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="39da8-126">Optional</span><span class="sxs-lookup"><span data-stu-id="39da8-126">Optional</span></span></p></td>
<td><p><span data-ttu-id="39da8-127"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="39da8-127"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="39da8-128">Eine Kombination aus <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong>-Konstanten, die Merkmale des neuen <strong>Recordset</strong> angeben.</span><span class="sxs-lookup"><span data-stu-id="39da8-128">A combination of <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> constants that specify characteristics of the new <strong>Recordset</strong>.</span></span></p></p><p><span data-ttu-id="39da8-129"><strong>Hinweis</strong>: Die Konstanten <STRONG>dbConsistent</STRONG> und <STRONG>dbInconsistent</STRONG> schließen sich gegenseitig aus, und die Verwendung beider verursacht einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="39da8-129">The constants <STRONG>dbConsistent</STRONG> and <STRONG>dbInconsistent</STRONG> are mutually exclusive, and using both causes an error.</span></span> <span data-ttu-id="39da8-130">Supplying a lockedits argument when options uses the <STRONG>dbReadOnly</STRONG> constant also causes an error.</span><span class="sxs-lookup"><span data-stu-id="39da8-130">Supplying a lockedits argument when options uses the <STRONG>dbReadOnly</STRONG> constant also causes an error.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39da8-131"><em>LockEdit</em></span><span class="sxs-lookup"><span data-stu-id="39da8-131"><em>LockEdit</em></span></span></p></td>
<td><p><span data-ttu-id="39da8-132">Optional</span><span class="sxs-lookup"><span data-stu-id="39da8-132">Optional</span></span></p></td>
<td><p><span data-ttu-id="39da8-133"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="39da8-133"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="39da8-134">Eine <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong>-Konstante, die die Sperre für das <strong>Recordset</strong> bestimmt.</span><span class="sxs-lookup"><span data-stu-id="39da8-134">A <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> constant that determines the locking for the <strong>Recordset</strong>.</span></span></p></p><p><span data-ttu-id="39da8-135"><strong>HINWEIS</strong>:Sie können <STRONG>dbReadOnly</STRONG> entweder im options-Argument oder im lockedits-Argument verwenden, aber nicht in beiden.</span><span class="sxs-lookup"><span data-stu-id="39da8-135">You can use <STRONG>dbReadOnly</STRONG> in either the options argument or the lockedits argument, but not both.</span></span> <span data-ttu-id="39da8-136">Wenn Sie es für beide Argumente verwenden, tritt ein Laufzeitfehler auf.</span><span class="sxs-lookup"><span data-stu-id="39da8-136">If you use it for both arguments, a run-time error occurs.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="39da8-137">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="39da8-137">Return value</span></span>

<span data-ttu-id="39da8-138">Recordset</span><span class="sxs-lookup"><span data-stu-id="39da8-138">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="39da8-139">Hinweise</span><span class="sxs-lookup"><span data-stu-id="39da8-139">Remarks</span></span>

<span data-ttu-id="39da8-p105">Wenn der Benutzer diesen Fehler beim Aktualisieren eines Datensatzes erhält, sollte Ihr Code normalerweise die Inhalte der Felder aktualisieren und die neu geänderten Werte abrufen. Wenn der Fehler beim Löschen eines Datensatzes auftritt, könnte Ihr Code dem Benutzer die neuen Datensatzdaten und eine Meldung anzeigen, dass die Daten kürzlich geändert wurden. An diesem Punkt kann Ihr Code eine Bestätigung anfordern, dass der Benutzer den Datensatz immer noch löschen möchte.</span><span class="sxs-lookup"><span data-stu-id="39da8-p105">Typically, if the user gets this error while updating a record, your code should refresh the contents of the fields and retrieve the newly modified values. If the error occurs while deleting a record, your code could display the new record data to the user and a message indicating that the data has recently changed. At this point, your code can request a confirmation that the user still wants to delete the record.</span></span>

<span data-ttu-id="39da8-143">Sie sollten auch die **dbSeeChanges**-Konstante verwenden, wenn Sie ein **Recordset** in einem ODBC-Arbeitsbereich mit verbundenem Microsoft Access-Datenbankmodul für eine Microsoft SQL Server 6.0-Tabelle (oder neuer) öffnen, die über eine  IDENTITY-Spalte verfügt. Andernfalls kann ein Fehler auftreten.</span><span class="sxs-lookup"><span data-stu-id="39da8-143">You should also use the **dbSeeChanges** constant if you open a **Recordset** in a Microsoft Access database engine-connected ODBC workspace against a Microsoft SQL Server 6.0 (or later) table that has an IDENTITY column, otherwise an error may result.</span></span>

<span data-ttu-id="39da8-p106">Wenn Sie mehr als ein **Recordset** in einer ODBC-Datenquelle öffnen, kann die Datenquelle ausfallen, da die Verbindung mit einem vorherigen **OpenRecordset**-Aufruf beschäftigt ist. Eine Lösungsmöglichkeit besteht im vollständigen Ausfüllen des **Recordset** mithilfe der **MoveLast**-Methode, sobald das **Recordset** geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="39da8-p106">Opening more than one **Recordset** on an ODBC data source may fail because the connection is busy with a prior **OpenRecordset** call. One way around this is to fully populate the **Recordset** by using the **MoveLast** method as soon as the **Recordset** is opened.</span></span>

<span data-ttu-id="39da8-146">Durch das Schließen eines **Recordset** mit der **[Close](connection-close-method-dao.md)**-Methode wird es automatisch aus der **Recordsets**-Auflistung gelöscht.</span><span class="sxs-lookup"><span data-stu-id="39da8-146">Closing a **Recordset** with the **[Close](connection-close-method-dao.md)** method automatically deletes it from the **Recordsets** collection.</span></span>

> [!NOTE]
> <span data-ttu-id="39da8-147">Wenn sich *source* auf eine SQL-Anweisung bezieht, die aus einer Zeichenfolge besteht, die mit einem nicht ganzzahligen Wert verkettet ist, und die Systemparameter ein nicht für die USA gültiges Dezimalzeichen, z. B. ein Komma, angeben (Beispiel: strSQL = "PRICE &gt; " &amp; lngPrice, und lngPrice = 125,50), tritt beim Versuch, das **Recordset** zu öffnen, ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="39da8-147">If source refers to an SQL statement composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE > " & lngPrice, and lngPrice = 125,50), an error occurs when you try to open the Recordset.</span></span> <span data-ttu-id="39da8-148">Der Grund ist, dass die Zahl bei der Verkettung mithilfe des Standarddezimalzeichens des Systems in eine Zeichenfolge umgewandelt wird und SQL nur für die USA gültige Dezimalzeichen akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="39da8-148">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and SQL only accepts U.S. decimal characters.</span></span>


