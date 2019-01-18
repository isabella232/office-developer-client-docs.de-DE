---
title: QueryDef.OpenRecordset-Methode (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: b4908c36-c156-e269-e2ad-b1fa20ec4884
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822070(v=office.15)
ms:contentKeyID: 48547232
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: a046359f39611e38b9e517495f54041f876addfc
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710244"
---
# <a name="querydefopenrecordset-method-dao"></a><span data-ttu-id="7dcff-102">QueryDef.OpenRecordset-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="7dcff-102">QueryDef.OpenRecordset method (DAO)</span></span>

<span data-ttu-id="7dcff-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7dcff-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7dcff-104">Erstellt ein neues **[Recordset](recordset-object-dao.md)** -Objekt und fügt es an die **Recordsets**-Auflistung an.</span><span class="sxs-lookup"><span data-stu-id="7dcff-104">Creates a new **[Recordset](recordset-object-dao.md)** object and appends it to the **Recordsets** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="7dcff-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7dcff-105">Syntax</span></span>

<span data-ttu-id="7dcff-106">*Ausdruck* . OpenRecordset (***Typ***, ***Optionen***, ***LockEdit***)</span><span class="sxs-lookup"><span data-stu-id="7dcff-106">*expression* .OpenRecordset(***Type***, ***Options***, ***LockEdit***)</span></span>

<span data-ttu-id="7dcff-107">*Ausdruck* Eine Variable, die ein **QueryDef** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="7dcff-107">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="7dcff-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7dcff-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7dcff-109">Name</span><span class="sxs-lookup"><span data-stu-id="7dcff-109">Name</span></span></p></th>
<th><p><span data-ttu-id="7dcff-110">Erforderlich oder optional</span><span class="sxs-lookup"><span data-stu-id="7dcff-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="7dcff-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="7dcff-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="7dcff-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7dcff-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7dcff-113"><em>Typ</em></span><span class="sxs-lookup"><span data-stu-id="7dcff-113"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="7dcff-114">Optional</span><span class="sxs-lookup"><span data-stu-id="7dcff-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="7dcff-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="7dcff-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="7dcff-116">Eine <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> -Konstante gibt den Typ des zu öffnenden <strong>Recordset</strong> an.</span><span class="sxs-lookup"><span data-stu-id="7dcff-116">A <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> constant that indicates the type of <strong>Recordset</strong> to open.</span></span></p><p><span data-ttu-id="7dcff-117"><strong>Hinweis</strong>: Wenn Sie ein <STRONG>Recordset-Objekt</STRONG> in einer Microsoft Access-Arbeitsbereich öffnen, und Sie keinen Typ angeben, erstellt <STRONG>OpenRecordset</STRONG> eine vom Typ Tabelle <STRONG>Recordset</STRONG>, falls möglich.</span><span class="sxs-lookup"><span data-stu-id="7dcff-117"><strong>NOTE</strong>: If you open a <STRONG>Recordset</STRONG> in a Microsoft Access workspace and you don't specify a type, <STRONG>OpenRecordset</STRONG> creates a table-type <STRONG>Recordset</STRONG>, if possible.</span></span> <span data-ttu-id="7dcff-118">Wenn Sie einer verknüpften Tabelle oder Abfrage angeben, erstellt <STRONG>OpenRecordset</STRONG> ein vom Typ Dynaset- <STRONG>Recordset-Objekt</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="7dcff-118">If you specify a linked table or query, <STRONG>OpenRecordset</STRONG> creates a dynaset-type <STRONG>Recordset</STRONG>.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7dcff-119"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="7dcff-119"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="7dcff-120">Optional</span><span class="sxs-lookup"><span data-stu-id="7dcff-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="7dcff-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="7dcff-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="7dcff-122">Eine Kombination aus <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> -Konstanten, die Merkmale des neuen <strong>Recordset</strong> angeben.</span><span class="sxs-lookup"><span data-stu-id="7dcff-122">A combination of <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> constants that specify characteristics of the new <strong>Recordset</strong>.</span></span></p></p><p><span data-ttu-id="7dcff-123"><strong>Hinweis</strong>: die Konstanten <STRONG>DbConsistent</STRONG> und <STRONG>DbInconsistent</STRONG> schließen sich gegenseitig aus, und beide wird ein Fehler ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="7dcff-123"><strong>NOTE</strong>: The constants <STRONG>dbConsistent</STRONG> and <STRONG>dbInconsistent</STRONG> are mutually exclusive, and using both causes an error.</span></span> <span data-ttu-id="7dcff-124">Lockedits-Argument angeben, wenn <STRONG>beide</STRONG> Optionen verwendet, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="7dcff-124">Supplying a lockedits argument when options uses the <STRONG>dbReadOnly</STRONG> constant also causes an error.</span></span></p>
</td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7dcff-125"><em>LockEdit</em></span><span class="sxs-lookup"><span data-stu-id="7dcff-125"><em>LockEdit</em></span></span></p></td>
<td><p><span data-ttu-id="7dcff-126">Optional</span><span class="sxs-lookup"><span data-stu-id="7dcff-126">Optional</span></span></p></td>
<td><p><span data-ttu-id="7dcff-127"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="7dcff-127"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="7dcff-128">Eine <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> -Konstante, die die Sperre für das <strong>Recordset</strong> bestimmt.</span><span class="sxs-lookup"><span data-stu-id="7dcff-128">A <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> constant that determines the locking for the <strong>Recordset</strong>.</span></span></p></p><p><span data-ttu-id="7dcff-129"><strong>Hinweis</strong>: <STRONG>DbReadOnly</STRONG> Options-Argument oder das Argument sperren, jedoch nicht beide können.</span><span class="sxs-lookup"><span data-stu-id="7dcff-129"><strong>NOTE</strong>: You can use <STRONG>dbReadOnly</STRONG> in either the options argument or the lockedits argument, but not both.</span></span> <span data-ttu-id="7dcff-130">Wenn Sie für beide Argumente verwenden, tritt ein Laufzeitfehler auf.</span><span class="sxs-lookup"><span data-stu-id="7dcff-130">If you use it for both arguments, a run-time error occurs.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="7dcff-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7dcff-131">Return value</span></span>

<span data-ttu-id="7dcff-132">Recordset</span><span class="sxs-lookup"><span data-stu-id="7dcff-132">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="7dcff-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7dcff-133">Remarks</span></span>

<span data-ttu-id="7dcff-134">Sie sollten die **[dbSeeChanges](recordsetoptionenum-enumeration-dao.md)** -Konstante auch dann verwenden, wenn Sie ein **Recordset** in einem mit einem Microsoft Access-Datenbankmodul verbundenen ODBC-Arbeitsbereich in einer Microsoft SQL Server 6.0-Tabelle (oder höher) öffnen, die über eine IDENTITY-Spalte verfügt. Andernfalls tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="7dcff-134">You should also use the **[dbSeeChanges](recordsetoptionenum-enumeration-dao.md)** constant if you open a **Recordset** in a Microsoft Access database engine-connected ODBC workspace against a Microsoft SQL Server 6.0 (or later) table that has an IDENTITY column, otherwise an error may result.</span></span>

<span data-ttu-id="7dcff-p104">Das Öffnen mehrerer **Recordset** -Objekte in einer ODBC-Datenquelle kann fehlschlagen, wenn die Verbindung durch einen vorherigen **OpenRecordset** -Aufruf ausgelastet ist. Das könnten Sie beispielsweise dadurch verhindern, dass Sie das **Recordset** -Objekt mithilfe der **[MoveLast](recordset-movelast-method-dao.md)** -Methode vollständig auffüllen, sobald das **Recordset** -Objekt geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="7dcff-p104">Opening more than one **Recordset** on an ODBC data source may fail because the connection is busy with a prior **OpenRecordset** call. One way around this is to fully populate the **Recordset** by using the **[MoveLast](recordset-movelast-method-dao.md)** method as soon as the **Recordset** is opened.</span></span>

<span data-ttu-id="7dcff-137">Beim Schließen eines **Recordset** -Objekts mit der **Close** -Methode wird es automatisch aus der **Recordsets** -Auflistung gelöscht.</span><span class="sxs-lookup"><span data-stu-id="7dcff-137">Closing a **Recordset** with the **Close** method automatically deletes it from the **Recordsets** collection.</span></span>

> [!NOTE]
> <span data-ttu-id="7dcff-138">Wenn *Quelle* bezieht eine SQL-Anweisung besteht aus einer Zeichenfolge mit einem nicht-Integer-Wert verkettet und die Systemparameter angeben einer US-decimal Zeichen wie etwa ein Komma (beispielsweise StrSQL = "PRICE &gt; " &amp; LngPrice, und LngPrice = 125,50), tritt ein Fehler auf, wenn Sie, zum Öffnen des **Recordset-Objekts versuchen**.</span><span class="sxs-lookup"><span data-stu-id="7dcff-138">If *source* refers to an SQL statement composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error occurs when you try to open the **Recordset**.</span></span> <span data-ttu-id="7dcff-139">Das geschieht, weil die Zahl während der Verkettung mithilfe des standardmäßigen Dezimalzeichens des Systems in eine Zeichenfolge konvertiert wird und SQL nur US-amerikanische Dezimalzeichen akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="7dcff-139">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and SQL only accepts U.S. decimal characters.</span></span>


