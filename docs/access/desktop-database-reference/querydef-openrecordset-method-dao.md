---
title: QueryDef.OpenRecordset-Methode (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: b4908c36-c156-e269-e2ad-b1fa20ec4884
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822070(v=office.15)
ms:contentKeyID: 48547232
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 368c59f0ea207862c5b7ac5ea7f664295adb5188
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606836"
---
# <a name="querydefopenrecordset-method-dao"></a><span data-ttu-id="80c4a-102">QueryDef.OpenRecordset-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="80c4a-102">QueryDef.OpenRecordset Method (DAO)</span></span>


<span data-ttu-id="80c4a-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="80c4a-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="80c4a-104">Erstellt ein neues **[Recordset](recordset-object-dao.md)** -Objekt und fügt es an die **Recordsets**-Auflistung an.</span><span class="sxs-lookup"><span data-stu-id="80c4a-104">Creates a new **[Recordset](recordset-object-dao.md)** object and appends it to the **Recordsets** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="80c4a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="80c4a-105">Syntax</span></span>

<span data-ttu-id="80c4a-106">*Ausdruck* . OpenRecordset (***Typ***, ***Optionen***, ***LockEdit***)</span><span class="sxs-lookup"><span data-stu-id="80c4a-106">*expression* .OpenRecordset(***Type***, ***Options***, ***LockEdit***)</span></span>

<span data-ttu-id="80c4a-107">*Ausdruck* Eine Variable, die ein **QueryDef** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="80c4a-107">*expression* A variable that represents a **QueryDef** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="80c4a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="80c4a-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="80c4a-109">Name</span><span class="sxs-lookup"><span data-stu-id="80c4a-109">Name</span></span></p></th>
<th><p><span data-ttu-id="80c4a-110">Erforderlich/Optional</span><span class="sxs-lookup"><span data-stu-id="80c4a-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="80c4a-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="80c4a-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="80c4a-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="80c4a-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="80c4a-113">Typ</span><span class="sxs-lookup"><span data-stu-id="80c4a-113">Type</span></span></p></td>
<td><p><span data-ttu-id="80c4a-114">Optional</span><span class="sxs-lookup"><span data-stu-id="80c4a-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="80c4a-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="80c4a-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="80c4a-116">Eine <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> -Konstante gibt den Typ des zu öffnenden <strong>Recordset</strong> an.</span><span class="sxs-lookup"><span data-stu-id="80c4a-116">A <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> constant that indicates the type of <strong>Recordset</strong> to open.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="80c4a-p101">Wenn Sie ein <STRONG>Recordset</STRONG> in einem Microsoft Access-Arbeitsbereich öffnen und keinen Typ angeben, erstellt <STRONG>OpenRecordset</STRONG>, wenn möglich, ein <STRONG>Recordset</STRONG> vom "table"-Typ. Wenn sie eine verknüpfte Tabelle oder Abfrage angeben, erstellt <STRONG>OpenRecordset</STRONG> ein <STRONG>Recordset</STRONG> vom "dynaset"-Typ.</span><span class="sxs-lookup"><span data-stu-id="80c4a-p101">If you open a <STRONG>Recordset</STRONG> in a Microsoft Access workspace and you don't specify a type, <STRONG>OpenRecordset</STRONG> creates a table-type <STRONG>Recordset</STRONG>, if possible. If you specify a linked table or query, <STRONG>OpenRecordset</STRONG> creates a dynaset-type <STRONG>Recordset</STRONG>.</span></span></P>


</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80c4a-119">Options</span><span class="sxs-lookup"><span data-stu-id="80c4a-119">Options</span></span></p></td>
<td><p><span data-ttu-id="80c4a-120">Optional</span><span class="sxs-lookup"><span data-stu-id="80c4a-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="80c4a-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="80c4a-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="80c4a-122">Eine Kombination aus <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> -Konstanten, die Merkmale des neuen <strong>Recordset</strong> angeben.</span><span class="sxs-lookup"><span data-stu-id="80c4a-122">A combination of <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> constants that specify characteristics of the new <strong>Recordset</strong>.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="80c4a-p102">Die Konstanten <STRONG>dbConsistent</STRONG> und <STRONG>dbInconsistent</STRONG> schließen sich gegenseitig aus, und die Verwendung beider verursacht einen Fehler. Wenn in Options die <STRONG>dbReadOnly</STRONG>-Konstante verwendet wird, führt die Angabe eines lockedits-Arguments ebenfalls zu einem Fehler.</span><span class="sxs-lookup"><span data-stu-id="80c4a-p102">The constants <STRONG>dbConsistent</STRONG> and <STRONG>dbInconsistent</STRONG> are mutually exclusive, and using both causes an error. Supplying a lockedits argument when options uses the <STRONG>dbReadOnly</STRONG> constant also causes an error.</span></span></P>


</td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80c4a-125">LockEdit</span><span class="sxs-lookup"><span data-stu-id="80c4a-125">LockEdit</span></span></p></td>
<td><p><span data-ttu-id="80c4a-126">Optional</span><span class="sxs-lookup"><span data-stu-id="80c4a-126">Optional</span></span></p></td>
<td><p><span data-ttu-id="80c4a-127"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="80c4a-127"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="80c4a-128">Eine <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> -Konstante, die die Sperre für das <strong>Recordset</strong> bestimmt.</span><span class="sxs-lookup"><span data-stu-id="80c4a-128">A <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> constant that determines the locking for the <strong>Recordset</strong>.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="80c4a-p103">Sie können <STRONG>dbReadOnly</STRONG> entweder im options-Argument oder im lockedits-Argument verwenden, aber nicht in beiden. Wenn Sie es für beide Argumente verwenden, tritt ein Laufzeitfehler auf.</span><span class="sxs-lookup"><span data-stu-id="80c4a-p103">You can use <STRONG>dbReadOnly</STRONG> in either the options argument or the lockedits argument, but not both. If you use it for both arguments, a run-time error occurs.</span></span></P>


</td>
</tr>
</tbody>
</table>


<span data-ttu-id="80c4a-131"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="80c4a-131"><<<<<<< HEAD</span></span>
### <a name="return-value"></a><span data-ttu-id="80c4a-132">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="80c4a-132">Return Value</span></span>
=======
### <a name="return-value"></a><span data-ttu-id="80c4a-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="80c4a-133">Return value</span></span>
>>>>>>> <span data-ttu-id="80c4a-134">master</span><span class="sxs-lookup"><span data-stu-id="80c4a-134">master</span></span>

<span data-ttu-id="80c4a-135">Recordset</span><span class="sxs-lookup"><span data-stu-id="80c4a-135">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="80c4a-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="80c4a-136">Remarks</span></span>

<span data-ttu-id="80c4a-137">Sie sollten die **[dbSeeChanges](recordsetoptionenum-enumeration-dao.md)** -Konstante auch dann verwenden, wenn Sie ein **Recordset** in einem mit einem Microsoft Access-Datenbankmodul verbundenen ODBC-Arbeitsbereich in einer Microsoft SQL Server 6.0-Tabelle (oder höher) öffnen, die über eine IDENTITY-Spalte verfügt. Andernfalls tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="80c4a-137">You should also use the **[dbSeeChanges](recordsetoptionenum-enumeration-dao.md)** constant if you open a **Recordset** in a Microsoft Access database engine-connected ODBC workspace against a Microsoft SQL Server 6.0 (or later) table that has an IDENTITY column, otherwise an error may result.</span></span>

<span data-ttu-id="80c4a-p104">Das Öffnen mehrerer **Recordset** -Objekte in einer ODBC-Datenquelle kann fehlschlagen, wenn die Verbindung durch einen vorherigen **OpenRecordset** -Aufruf ausgelastet ist. Das könnten Sie beispielsweise dadurch verhindern, dass Sie das **Recordset** -Objekt mithilfe der **[MoveLast](recordset-movelast-method-dao.md)** -Methode vollständig auffüllen, sobald das **Recordset** -Objekt geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="80c4a-p104">Opening more than one **Recordset** on an ODBC data source may fail because the connection is busy with a prior **OpenRecordset** call. One way around this is to fully populate the **Recordset** by using the **[MoveLast](recordset-movelast-method-dao.md)** method as soon as the **Recordset** is opened.</span></span>

<span data-ttu-id="80c4a-140">Beim Schließen eines **Recordset** -Objekts mit der **Close** -Methode wird es automatisch aus der **Recordsets** -Auflistung gelöscht.</span><span class="sxs-lookup"><span data-stu-id="80c4a-140">Closing a **Recordset** with the **Close** method automatically deletes it from the **Recordsets** collection.</span></span>


> [!NOTE]
> <P><span data-ttu-id="80c4a-141">Wenn <EM>Quelle</EM> bezieht eine SQL-Anweisung besteht aus einer Zeichenfolge mit einem nicht-Integer-Wert verkettet und die Systemparameter angeben einer US-decimal Zeichen wie etwa ein Komma (beispielsweise StrSQL = "PRICE &gt; " &amp; LngPrice, und LngPrice = 125,50), tritt ein Fehler auf, wenn Sie, zum Öffnen des <STRONG>Recordset-Objekts versuchen</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="80c4a-141">If <EM>source</EM> refers to an SQL statement composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error occurs when you try to open the <STRONG>Recordset</STRONG>.</span></span> <span data-ttu-id="80c4a-142">Das geschieht, weil die Zahl während der Verkettung mithilfe des standardmäßigen Dezimalzeichens des Systems in eine Zeichenfolge konvertiert wird und SQL nur US-amerikanische Dezimalzeichen akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="80c4a-142">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and SQL only accepts U.S. decimal characters.</span></span></P>


