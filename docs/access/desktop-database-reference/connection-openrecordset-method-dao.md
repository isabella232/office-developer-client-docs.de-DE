---
title: Connection.OpenRecordset Method (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: 584a3e00-7589-90f1-aa6a-5d6116f0b5b6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194324(v=office.15)
ms:contentKeyID: 48544993
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7f0e8fa499a21bb231131b968c1456af9cb86a45
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862954"
---
# <a name="connectionopenrecordset-method-dao"></a><span data-ttu-id="7f560-102">Connection.OpenRecordset Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="7f560-102">Connection.OpenRecordset Method (DAO)</span></span>


<span data-ttu-id="7f560-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7f560-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="7f560-104">Erstellt ein neues **[Recordset](recordset-object-dao.md)** -Objekt und fügt es an die **Recordsets**-Auflistung an.</span><span class="sxs-lookup"><span data-stu-id="7f560-104">Creates a new **[Recordset](recordset-object-dao.md)** object and appends it to the **Recordsets** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f560-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f560-105">Syntax</span></span>

<span data-ttu-id="7f560-106">*Ausdruck* . OpenRecordset (***Name***, ***Typ***, ***Optionen***, ***LockEdit***)</span><span class="sxs-lookup"><span data-stu-id="7f560-106">*expression* .OpenRecordset(***Name***, ***Type***, ***Options***, ***LockEdit***)</span></span>

<span data-ttu-id="7f560-107">*Ausdruck* Eine Variable, die ein **Connection** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="7f560-107">*expression* A variable that represents a **Connection** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="7f560-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f560-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7f560-109">Name</span><span class="sxs-lookup"><span data-stu-id="7f560-109">Name</span></span></p></th>
<th><p><span data-ttu-id="7f560-110">Erforderlich/Optional</span><span class="sxs-lookup"><span data-stu-id="7f560-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="7f560-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="7f560-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="7f560-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7f560-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7f560-113">Name</span><span class="sxs-lookup"><span data-stu-id="7f560-113">Name</span></span></p></td>
<td><p><span data-ttu-id="7f560-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="7f560-114">Required</span></span></p></td>
<td><p><span data-ttu-id="7f560-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="7f560-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="7f560-p101">Die Quelle der Datensätze für das neue <strong>Recordset</strong>. Die Quelle kann ein Tabellenname, ein Abfragename oder eine SQL-Anweisung sein, die Datensätze zurückgibt. Für <strong>Recordset</strong> -Objekte vom "table"-Typ in Microsoft Access-Datenbankmodul-Datenbanken kann die Quelle nur ein Tabellenname sein.  </span><span class="sxs-lookup"><span data-stu-id="7f560-p101">The source of the records for the new <strong>Recordset</strong>. The source can be a table name, a query name, or an SQL statement that returns records. For table-type <strong>Recordset</strong> objects in Microsoft Access database engine databases, the source can only be a table name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f560-119">Typ</span><span class="sxs-lookup"><span data-stu-id="7f560-119">Type</span></span></p></td>
<td><p><span data-ttu-id="7f560-120">Optional</span><span class="sxs-lookup"><span data-stu-id="7f560-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="7f560-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="7f560-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="7f560-122">Eine <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> -Konstante gibt den Typ des zu öffnenden <strong>Recordset</strong> an.</span><span class="sxs-lookup"><span data-stu-id="7f560-122">A <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> constant that indicates the type of <strong>Recordset</strong> to open.</span></span></p>

> [!NOTE]
> <span data-ttu-id="7f560-p102">Wenn Sie ein **Recordset** in einem Microsoft Access-Arbeitsbereich öffnen und keinen Typ angeben, erstellt **OpenRecordset**, wenn möglich, ein **Recordset** vom "table"-Typ. Wenn sie eine verknüpfte Tabelle oder Abfrage angeben, erstellt **OpenRecordset** ein **Recordset** vom "dynaset"-Typ.</span><span class="sxs-lookup"><span data-stu-id="7f560-p102">If you open a **Recordset** in a Microsoft Access workspace and you don't specify a type, **OpenRecordset** creates a table-type **Recordset**, if possible. If you specify a linked table or query, **OpenRecordset** creates a dynaset-type **Recordset**.</span></span>


</td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f560-125">Options</span><span class="sxs-lookup"><span data-stu-id="7f560-125">Options</span></span></p></td>
<td><p><span data-ttu-id="7f560-126">Optional</span><span class="sxs-lookup"><span data-stu-id="7f560-126">Optional</span></span></p></td>
<td><p><span data-ttu-id="7f560-127"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="7f560-127"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="7f560-128">Eine Kombination aus <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> -Konstanten, die Merkmale des neuen <strong>Recordset</strong> angeben.</span><span class="sxs-lookup"><span data-stu-id="7f560-128">A combination of <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> constants that specify characteristics of the new <strong>Recordset</strong>.</span></span></p>

> [!NOTE]
> <span data-ttu-id="7f560-129">Die Konstanten **DbConsistent** und **DbInconsistent** schließen sich gegenseitig aus, und beide wird ein Fehler ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="7f560-129">The constants **dbConsistent** and **dbInconsistent** are mutually exclusive, and using both causes an error.</span></span> <span data-ttu-id="7f560-130">Lockedits-Argument angeben, wenn **beide** Optionen verwenden, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="7f560-130">Supplying a lockedits argument when options use the **dbReadOnly** constant also causes an error.</span></span>


</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f560-131">LockEdit</span><span class="sxs-lookup"><span data-stu-id="7f560-131">LockEdit</span></span></p></td>
<td><p><span data-ttu-id="7f560-132">Optional</span><span class="sxs-lookup"><span data-stu-id="7f560-132">Optional</span></span></p></td>
<td><p><span data-ttu-id="7f560-133"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="7f560-133"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="7f560-134">Eine <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> -Konstante, die die Sperre für das <strong>Recordset</strong> bestimmt.</span><span class="sxs-lookup"><span data-stu-id="7f560-134">A <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> constant that determines the locking for the <strong>Recordset</strong>.</span></span></p>

> [!NOTE]
> <span data-ttu-id="7f560-p104">Sie können **dbReadOnly** entweder im options-Argument oder im lockedits-Argument verwenden, aber nicht in beiden. Wenn Sie es für beide Argumente verwenden, tritt ein Laufzeitfehler auf.</span><span class="sxs-lookup"><span data-stu-id="7f560-p104">You can use **dbReadOnly** in either the options argument or the lockedits argument, but not both. If you use it for both arguments, a run-time error occurs.</span></span>


</td>
</tr>
</tbody>
</table>


<span data-ttu-id="7f560-137"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="7f560-137"><<<<<<< HEAD</span></span>
### <a name="return-value"></a><span data-ttu-id="7f560-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7f560-138">Return Value</span></span>
=======
### <a name="return-value"></a><span data-ttu-id="7f560-139">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7f560-139">Return value</span></span>
>>>>>>> <span data-ttu-id="7f560-140">master</span><span class="sxs-lookup"><span data-stu-id="7f560-140">master</span></span>

<span data-ttu-id="7f560-141">Recordset</span><span class="sxs-lookup"><span data-stu-id="7f560-141">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="7f560-142">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7f560-142">Remarks</span></span>

<span data-ttu-id="7f560-p105">Wenn der Benutzer beim Aktualisieren eines Datensatzes diesen Fehler erhält, sollte der Code den Inhalt des Felds aktualisieren und die geänderten Werte abrufen. Tritt der Fehler beim Löschen eines Datensatzes auf, sollte der Code die Daten des neuen Datensatzes anzeigen und eine Meldung darüber ausgeben, dass die Daten kürzlich geändert wurden. An dieser Stelle könnte der Code bestätigen lassen, dass der Benutzer den Datensatz wirklich löschen möchte.</span><span class="sxs-lookup"><span data-stu-id="7f560-p105">Typically, if the user gets this error while updating a record, your code should refresh the contents of the fields and retrieve the newly modified values. If the error occurs while deleting a record, your code could display the new record data to the user and a message indicating that the data has recently changed. At this point, your code can request a confirmation that the user still wants to delete the record.</span></span>

<span data-ttu-id="7f560-146">Sie sollten die **dbSeeChanges**-Konstante auch dann verwenden, wenn Sie ein **Recordset** in einem mit einem Microsoft Access-Datenbankmodul verbundenen ODBC-Arbeitsbereich in einer Microsoft SQL Server 6.0-Tabelle (oder höher) öffnen, die über eine IDENTITY-Spalte verfügt. Andernfalls tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="7f560-146">You should also use the **dbSeeChanges** constant if you open a **Recordset** in a Microsoft Access database engine-connected ODBC workspace against a Microsoft SQL Server 6.0 (or later) table that has an IDENTITY column, otherwise an error may result.</span></span>

<span data-ttu-id="7f560-p106">Das Öffnen mehrerer **Recordset**-Objekte in einer ODBC-Datenquelle kann fehlschlagen, wenn die Verbindung durch einen vorherigen **OpenRecordset**-Aufruf ausgelastet ist. Das könnten Sie beispielsweise dadurch verhindern, dass Sie das **Recordset**-Objekt mithilfe der **MoveLast**-Methode vollständig auffüllen, sobald das **Recordset**-Objekt geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="7f560-p106">Opening more than one **Recordset** on an ODBC data source may fail because the connection is busy with a prior **OpenRecordset** call. One way around this is to fully populate the **Recordset** by using the **MoveLast** method as soon as the **Recordset** is opened.</span></span>

<span data-ttu-id="7f560-149">Beim Schließen eines **Recordset**-Objekts mit der **[Close](connection-close-method-dao.md)** -Methode wird es automatisch aus der **Recordsets**-Auflistung gelöscht.</span><span class="sxs-lookup"><span data-stu-id="7f560-149">Closing a **Recordset** with the **[Close](connection-close-method-dao.md)** method automatically deletes it from the **Recordsets** collection.</span></span>


> [!NOTE]
> <span data-ttu-id="7f560-150">Wenn *Quelle* bezieht eine SQL-Anweisung besteht aus einer Zeichenfolge mit einem nicht-Integer-Wert verkettet und die Systemparameter angeben einer US-decimal Zeichen wie etwa ein Komma (beispielsweise StrSQL = "PRICE &gt; " &amp; LngPrice, und LngPrice = 125,50), tritt ein Fehler auf, wenn Sie, zum Öffnen des **Recordset-Objekts versuchen**.</span><span class="sxs-lookup"><span data-stu-id="7f560-150">If *source* refers to an SQL statement composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error occurs when you try to open the **Recordset**.</span></span> <span data-ttu-id="7f560-151">Das geschieht, weil die Zahl während der Verkettung mithilfe des standardmäßigen Dezimalzeichens des Systems in eine Zeichenfolge konvertiert wird und SQL nur US-amerikanische Dezimalzeichen akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="7f560-151">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and SQL only accepts U.S. decimal characters.</span></span>


