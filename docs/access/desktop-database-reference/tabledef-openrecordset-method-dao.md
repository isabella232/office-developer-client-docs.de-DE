---
title: TableDef.OpenRecordset-Methode (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: f4c9c89c-3348-d3c9-ce76-dd11e5ee11a7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836703(v=office.15)
ms:contentKeyID: 48548696
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2035d4319f7821f2a0469193955c732231f30cf0
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719295"
---
# <a name="tabledefopenrecordset-method-dao"></a><span data-ttu-id="b4294-102">TableDef.OpenRecordset-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="b4294-102">TableDef.OpenRecordset method (DAO)</span></span>

<span data-ttu-id="b4294-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b4294-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b4294-104">Erstellt ein neues **[Recordset](recordset-object-dao.md)** -Objekt und fügt es an die **Recordsets**-Auflistung an.</span><span class="sxs-lookup"><span data-stu-id="b4294-104">Creates a new **[Recordset](recordset-object-dao.md)** object and appends it to the **Recordsets** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4294-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4294-105">Syntax</span></span>

<span data-ttu-id="b4294-106">*Ausdruck* . OpenRecordset ("***Typ***", " ***Optionen***")</span><span class="sxs-lookup"><span data-stu-id="b4294-106">*expression* .OpenRecordset(***Type***, ***Options***)</span></span>

<span data-ttu-id="b4294-107">*Ausdruck* Eine Variable, die ein **TableDef** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="b4294-107">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="b4294-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b4294-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b4294-109">Name</span><span class="sxs-lookup"><span data-stu-id="b4294-109">Name</span></span></p></th>
<th><p><span data-ttu-id="b4294-110">Erforderlich oder optional</span><span class="sxs-lookup"><span data-stu-id="b4294-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="b4294-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="b4294-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="b4294-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b4294-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b4294-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="b4294-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="b4294-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="b4294-114">Required</span></span></p></td>
<td><p><span data-ttu-id="b4294-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="b4294-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="b4294-p101">Die Quelle der Datensätze für das neue <strong>Recordset</strong>. Die Quelle kann ein Tabellenname, ein Abfragename oder eine SQL-Anweisung sein, die Datensätze zurückgibt. Für <strong>Recordset</strong> -Objekte vom "table"-Typ in Microsoft Access-Datenbankmodul-Datenbanken kann die Quelle nur ein Tabellenname sein.  </span><span class="sxs-lookup"><span data-stu-id="b4294-p101">The source of the records for the new <strong>Recordset</strong>. The source can be a table name, a query name, or an SQL statement that returns records. For table-type <strong>Recordset</strong> objects in Microsoft Access database engine databases, the source can only be a table name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4294-119"><em>Type</em></span><span class="sxs-lookup"><span data-stu-id="b4294-119"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="b4294-120">Optional</span><span class="sxs-lookup"><span data-stu-id="b4294-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="b4294-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="b4294-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="b4294-122">Eine <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> -Konstante gibt den Typ des zu öffnenden <strong>Recordset</strong> an.</span><span class="sxs-lookup"><span data-stu-id="b4294-122">A <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> constant that indicates the type of <strong>Recordset</strong> to open.</span></span></p><p><span data-ttu-id="b4294-123"><strong>Hinweis</strong>: Wenn Sie ein <STRONG>Recordset-Objekt</STRONG> in einer Microsoft Access-Arbeitsbereich öffnen, und Sie keinen Typ angeben, erstellt <STRONG>OpenRecordset</STRONG> eine vom Typ Tabelle <STRONG>Recordset</STRONG>, falls möglich.</span><span class="sxs-lookup"><span data-stu-id="b4294-123"><strong>NOTE</strong>: If you open a <STRONG>Recordset</STRONG> in a Microsoft Access workspace and you don't specify a type, <STRONG>OpenRecordset</STRONG> creates a table-type <STRONG>Recordset</STRONG>, if possible.</span></span> <span data-ttu-id="b4294-124">Wenn Sie einer verknüpften Tabelle oder Abfrage angeben, erstellt <STRONG>OpenRecordset</STRONG> ein vom Typ Dynaset- <STRONG>Recordset-Objekt</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="b4294-124">If you specify a linked table or query, <STRONG>OpenRecordset</STRONG> creates a dynaset-type <STRONG>Recordset</STRONG>.</span></span></p>
</td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4294-125"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="b4294-125"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="b4294-126">Optional</span><span class="sxs-lookup"><span data-stu-id="b4294-126">Optional</span></span></p></td>
<td><p><span data-ttu-id="b4294-127"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="b4294-127"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="b4294-128">Eine Kombination aus <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> -Konstanten, die Merkmale des neuen <strong>Recordset</strong> angeben.</span><span class="sxs-lookup"><span data-stu-id="b4294-128">A combination of <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> constants that specify characteristics of the new <strong>Recordset</strong>.</span></span></p><p><span data-ttu-id="b4294-129"><strong>Hinweis</strong>: die Konstanten <STRONG>DbConsistent</STRONG> und <STRONG>DbInconsistent</STRONG> schließen sich gegenseitig aus, und beide wird ein Fehler ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="b4294-129"><strong>NOTE</strong>: The constants <STRONG>dbConsistent</STRONG> and <STRONG>dbInconsistent</STRONG> are mutually exclusive, and using both causes an error.</span></span> <span data-ttu-id="b4294-130">Lockedits-Argument angeben, wenn <STRONG>beide</STRONG> Optionen verwendet, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="b4294-130">Supplying a lockedits argument when options uses the <STRONG>dbReadOnly</STRONG> constant also causes an error.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4294-131"><em>LockEdit</em></span><span class="sxs-lookup"><span data-stu-id="b4294-131"><em>LockEdit</em></span></span></p></td>
<td><p><span data-ttu-id="b4294-132">Optional</span><span class="sxs-lookup"><span data-stu-id="b4294-132">Optional</span></span></p></td>
<td><p><span data-ttu-id="b4294-133"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="b4294-133"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="b4294-134">Eine <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> -Konstante, die die Sperre für das <strong>Recordset</strong> bestimmt.</span><span class="sxs-lookup"><span data-stu-id="b4294-134">A <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> constant that determines the locking for the <strong>Recordset</strong>.</span></span></p><p><span data-ttu-id="b4294-135"><strong>Hinweis</strong>: <STRONG>DbReadOnly</STRONG> Options-Argument oder das Argument sperren, jedoch nicht beide können.</span><span class="sxs-lookup"><span data-stu-id="b4294-135"><strong>NOTE</strong>: You can use <STRONG>dbReadOnly</STRONG> in either the options argument or the lockedits argument, but not both.</span></span> <span data-ttu-id="b4294-136">Wenn Sie für beide Argumente verwenden, tritt ein Laufzeitfehler auf.</span><span class="sxs-lookup"><span data-stu-id="b4294-136">If you use it for both arguments, a run-time error occurs.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="b4294-137">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b4294-137">Return value</span></span>

<span data-ttu-id="b4294-138">Recordset</span><span class="sxs-lookup"><span data-stu-id="b4294-138">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="b4294-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b4294-139">Remarks</span></span>

<span data-ttu-id="b4294-p105">Wenn der Benutzer beim Aktualisieren eines Datensatzes diesen Fehler erhält, sollte der Code den Inhalt des Felds aktualisieren und die geänderten Werte abrufen. Tritt der Fehler beim Löschen eines Datensatzes auf, sollte der Code die Daten des neuen Datensatzes anzeigen und eine Meldung darüber ausgeben, dass die Daten kürzlich geändert wurden. An dieser Stelle könnte der Code bestätigen lassen, dass der Benutzer den Datensatz wirklich löschen möchte.</span><span class="sxs-lookup"><span data-stu-id="b4294-p105">Typically, if the user gets this error while updating a record, your code should refresh the contents of the fields and retrieve the newly modified values. If the error occurs while deleting a record, your code could display the new record data to the user and a message indicating that the data has recently changed. At this point, your code can request a confirmation that the user still wants to delete the record.</span></span>

<span data-ttu-id="b4294-143">Sie sollten die **dbSeeChanges**-Konstante auch dann verwenden, wenn Sie ein **Recordset** in einem mit einem Microsoft Access-Datenbankmodul verbundenen ODBC-Arbeitsbereich in einer Microsoft SQL Server 6.0-Tabelle (oder höher) öffnen, die über eine IDENTITY-Spalte verfügt. Andernfalls tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="b4294-143">You should also use the **dbSeeChanges** constant if you open a **Recordset** in a Microsoft Access database engine-connected ODBC workspace against a Microsoft SQL Server 6.0 (or later) table that has an IDENTITY column, otherwise an error may result.</span></span>

<span data-ttu-id="b4294-p106">Das Öffnen mehrerer **Recordset**-Objekte in einer ODBC-Datenquelle kann fehlschlagen, wenn die Verbindung durch einen vorherigen **OpenRecordset**-Aufruf ausgelastet ist. Das könnten Sie beispielsweise dadurch verhindern, dass Sie das **Recordset**-Objekt mithilfe der **MoveLast**-Methode vollständig auffüllen, sobald das **Recordset**-Objekt geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="b4294-p106">Opening more than one **Recordset** on an ODBC data source may fail because the connection is busy with a prior **OpenRecordset** call. One way around this is to fully populate the **Recordset** by using the **MoveLast** method as soon as the **Recordset** is opened.</span></span>

<span data-ttu-id="b4294-146">Beim Schließen eines **Recordset**-Objekts mit der **[Close](connection-close-method-dao.md)** -Methode wird es automatisch aus der **Recordsets**-Auflistung gelöscht.</span><span class="sxs-lookup"><span data-stu-id="b4294-146">Closing a **Recordset** with the **[Close](connection-close-method-dao.md)** method automatically deletes it from the **Recordsets** collection.</span></span>

> [!NOTE]
> <span data-ttu-id="b4294-147">Wenn *Quelle* bezieht eine SQL-Anweisung besteht aus einer Zeichenfolge mit einem nicht-Integer-Wert verkettet und die Systemparameter angeben einer US-decimal Zeichen wie etwa ein Komma (beispielsweise StrSQL = "PRICE &gt; " &amp; LngPrice, und LngPrice = 125,50), tritt ein Fehler auf, wenn Sie, zum Öffnen des **Recordset-Objekts versuchen**.</span><span class="sxs-lookup"><span data-stu-id="b4294-147">If *source* refers to an SQL statement composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error occurs when you try to open the **Recordset**.</span></span> <span data-ttu-id="b4294-148">Das geschieht, weil die Zahl während der Verkettung mithilfe des standardmäßigen Dezimalzeichens des Systems in eine Zeichenfolge konvertiert wird und SQL nur US-amerikanische Dezimalzeichen akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="b4294-148">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and SQL only accepts U.S. decimal characters.</span></span>


