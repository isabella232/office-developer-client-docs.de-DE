---
title: GetRows-Methode (ADO)
TOCTitle: GetRows method (ADO)
ms:assetid: 570e6f1c-c17a-7d9a-c172-387894a3a1f1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249292(v=office.15)
ms:contentKeyID: 48544963
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b472f8e2cb7d95a3aa79194e7704a877864c1339
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920277"
---
# <a name="getrows-method-ado"></a><span data-ttu-id="c68a4-102">GetRows-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="c68a4-102">GetRows method (ADO)</span></span>


<span data-ttu-id="c68a4-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c68a4-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="c68a4-104">Ruft mehrere Datensätze eines [Recordset](recordset-object-ado.md)-Objekts in ein Array ab.</span><span class="sxs-lookup"><span data-stu-id="c68a4-104">Retrieves multiple records of a [Recordset](recordset-object-ado.md) object into an array.</span></span>

## <a name="syntax"></a><span data-ttu-id="c68a4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c68a4-105">Syntax</span></span>

<span data-ttu-id="c68a4-106">*Array* = *Recordset-Objekt*. GetRows (*Zeilen*, *Starten*, *Felder* )</span><span class="sxs-lookup"><span data-stu-id="c68a4-106">*array* = *recordset*.GetRows(*Rows*, *Start*, *Fields* )</span></span>

## <a name="return-value"></a><span data-ttu-id="c68a4-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c68a4-107">Return value</span></span>

<span data-ttu-id="c68a4-108">Gibt einen **Variant** -Wert zurück, deren dessen Wert es sich um ein zweidimensionales Array handelt.</span><span class="sxs-lookup"><span data-stu-id="c68a4-108">Returns a **Variant** whose value is a two-dimensional array.</span></span>

## <a name="parameters"></a><span data-ttu-id="c68a4-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c68a4-109">Parameters</span></span>

  - <span data-ttu-id="c68a4-110">*Rows*</span><span class="sxs-lookup"><span data-stu-id="c68a4-110">*Rows*</span></span>

  - <span data-ttu-id="c68a4-p101">Optional. Ein [GetRowsOptionEnum](getrowsoptionenum.md)-Wert, der die Anzahl der abzurufenden Datensätze angibt. Der Standardwert lautet **adGetRowsRest**.</span><span class="sxs-lookup"><span data-stu-id="c68a4-p101">Optional. A [GetRowsOptionEnum](getrowsoptionenum.md) value that indicates the number of records to retrieve. The default is **adGetRowsRest**.</span></span>

  - <span data-ttu-id="c68a4-114">*Start*</span><span class="sxs-lookup"><span data-stu-id="c68a4-114">*Start*</span></span>

  - <span data-ttu-id="c68a4-p102">Optional. Ein **String** -Wert oder ein **Variant** -Wert, der die Textmarke für den Datensatz ergibt, bei dem der **GetRows** -Vorgang beginnen soll. Sie können auch einen [BookmarkEnum](bookmarkenum.md)-Wert verwenden.</span><span class="sxs-lookup"><span data-stu-id="c68a4-p102">Optional. A **String** value or **Variant** that evaluates to the bookmark for the record from which the **GetRows** operation should begin. You can also use a [BookmarkEnum](bookmarkenum.md) value.</span></span>

  - <span data-ttu-id="c68a4-118">*Fields*</span><span class="sxs-lookup"><span data-stu-id="c68a4-118">*Fields*</span></span>

  - <span data-ttu-id="c68a4-p103">Optional. Ein **Variant** -Wert, der einen einzelnen Feldnamen oder eine einzelne Ordnungsposition oder ein Array mit Feldnamen oder Nummern für Ordnungspositionen darstellt. ADO gibt nur die Daten in diesen Feldern zurück.</span><span class="sxs-lookup"><span data-stu-id="c68a4-p103">Optional. A **Variant** that represents a single field name or ordinal position, or an array of field names or ordinal position numbers. ADO returns only the data in these fields.</span></span>

## <a name="remarks"></a><span data-ttu-id="c68a4-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c68a4-122">Remarks</span></span>

<span data-ttu-id="c68a4-123">Verwenden Sie die **GetRows** -Methode, um Datensätze aus einem **Recordset** -Objekt in ein zweidimensionales Array zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="c68a4-123">Use the **GetRows** method to copy records from a **Recordset** into a two-dimensional array.</span></span> <span data-ttu-id="c68a4-124">Der erste Index identifiziert das Feld und der zweite die Nummer des Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="c68a4-124">The first subscript identifies the field and the second identifies the record number.</span></span> <span data-ttu-id="c68a4-125">Die *Array* -Variable wird automatisch an die richtige Größe dimensioniert, wenn **GetRows** -Methode die Daten zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="c68a4-125">The *array* variable is automatically dimensioned to the correct size when the **GetRows** method returns the data.</span></span>

<span data-ttu-id="c68a4-126">Wenn Sie einen Wert für das Argument *Zeilen* nicht angeben, übernimmt die **GetRows** -Methode alle Datensätze im **Recordset** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="c68a4-126">If you do not specify a value for the *Rows* argument, the **GetRows** method automatically retrieves all the records in the **Recordset** object.</span></span> <span data-ttu-id="c68a4-127">Wenn Sie mehr Datensätze anfordern, als verfügbar sind, gibt **GetRows** nur die verfügbaren Datensätze zurück.</span><span class="sxs-lookup"><span data-stu-id="c68a4-127">If you request more records than are available, **GetRows** returns only the number of available records.</span></span>

<span data-ttu-id="c68a4-128">Wenn das **Recordset** -Objekt Lesezeichen unterstützt, können Sie angeben, an welcher Datensatz **GetRows** -Methode beginnen soll das Abrufen von Daten, indem Sie den Wert der [Bookmark](bookmark-property-ado.md) -Eigenschaft des Datensatzes in der *Start* -Argument übergeben.</span><span class="sxs-lookup"><span data-stu-id="c68a4-128">If the **Recordset** object supports bookmarks, you can specify at which record the **GetRows** method should begin retrieving data by passing the value of that record's [Bookmark](bookmark-property-ado.md) property in the *Start* argument.</span></span>

<span data-ttu-id="c68a4-129">Wenn Sie die Felder zu beschränken, die das Aufrufen von **GetRows zurückgegebenen** möchten, können Sie ein einzelnes Feld Namen und die Nummer oder ein Array mit Feldnamen/Nummern in das Argument *Fields* übergeben.</span><span class="sxs-lookup"><span data-stu-id="c68a4-129">If you want to restrict the fields that the **GetRows** call returns, you can pass either a single field name/number or an array of field names/numbers in the *Fields* argument.</span></span>

<span data-ttu-id="c68a4-130">Nachdem Sie **GetRows** aufgerufen haben, wird der nächste ungelesene Datensatz zum aktuellen Datensatz, oder die [EOF](bof-eof-properties-ado.md)-Eigenschaft wird auf **True** festgelegt, wenn keine weiteren Datensätze verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="c68a4-130">After you call **GetRows**, the next unread record becomes the current record, or the [EOF](bof-eof-properties-ado.md) property is set to **True** if there are no more records.</span></span>

