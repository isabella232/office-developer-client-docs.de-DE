---
title: GetRows-Methode (ADO)
TOCTitle: GetRows method (ADO)
ms:assetid: 570e6f1c-c17a-7d9a-c172-387894a3a1f1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249292(v=office.15)
ms:contentKeyID: 48544963
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 853f971f68bb0ec4069ba58e04b7cf9d231c6467
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949859"
---
# <a name="getrows-method-ado"></a><span data-ttu-id="81222-102">GetRows-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="81222-102">GetRows method (ADO)</span></span>

<span data-ttu-id="81222-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="81222-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="81222-104">Ruft mehrere Datensätze eines [Recordset](recordset-object-ado.md)-Objekts in ein Array ab.</span><span class="sxs-lookup"><span data-stu-id="81222-104">Retrieves multiple records of a [Recordset](recordset-object-ado.md) object into an array.</span></span>

## <a name="syntax"></a><span data-ttu-id="81222-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="81222-105">Syntax</span></span>

<span data-ttu-id="81222-106">*Array* = *Recordset-Objekt*. GetRows (*Zeilen*, *Starten*, *Felder* )</span><span class="sxs-lookup"><span data-stu-id="81222-106">*array* = *recordset*.GetRows(*Rows*, *Start*, *Fields* )</span></span>

## <a name="return-value"></a><span data-ttu-id="81222-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="81222-107">Return value</span></span>

<span data-ttu-id="81222-108">Gibt einen **Variant** -Wert zurück, deren dessen Wert es sich um ein zweidimensionales Array handelt.</span><span class="sxs-lookup"><span data-stu-id="81222-108">Returns a **Variant** whose value is a two-dimensional array.</span></span>

## <a name="parameters"></a><span data-ttu-id="81222-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="81222-109">Parameters</span></span>

|<span data-ttu-id="81222-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="81222-110">Parameter</span></span>|<span data-ttu-id="81222-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="81222-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="81222-112">*Rows*</span><span class="sxs-lookup"><span data-stu-id="81222-112">*Rows*</span></span> |<span data-ttu-id="81222-p101">Optional. Ein [GetRowsOptionEnum](getrowsoptionenum.md)-Wert, der die Anzahl der abzurufenden Datensätze angibt. Der Standardwert lautet **adGetRowsRest**.</span><span class="sxs-lookup"><span data-stu-id="81222-p101">Optional. A [GetRowsOptionEnum](getrowsoptionenum.md) value that indicates the number of records to retrieve. The default is **adGetRowsRest**.</span></span>|
|<span data-ttu-id="81222-116">*Start*</span><span class="sxs-lookup"><span data-stu-id="81222-116">*Start*</span></span> |<span data-ttu-id="81222-p102">Optional. Ein **String** -Wert oder ein **Variant** -Wert, der die Textmarke für den Datensatz ergibt, bei dem der **GetRows** -Vorgang beginnen soll. Sie können auch einen [BookmarkEnum](bookmarkenum.md)-Wert verwenden.</span><span class="sxs-lookup"><span data-stu-id="81222-p102">Optional. A **String** value or **Variant** that evaluates to the bookmark for the record from which the **GetRows** operation should begin. You can also use a [BookmarkEnum](bookmarkenum.md) value.</span></span>|
|<span data-ttu-id="81222-120">*Fields*</span><span class="sxs-lookup"><span data-stu-id="81222-120">*Fields*</span></span> |<span data-ttu-id="81222-p103">Optional. Ein **Variant** -Wert, der einen einzelnen Feldnamen oder eine einzelne Ordnungsposition oder ein Array mit Feldnamen oder Nummern für Ordnungspositionen darstellt. ADO gibt nur die Daten in diesen Feldern zurück.</span><span class="sxs-lookup"><span data-stu-id="81222-p103">Optional. A **Variant** that represents a single field name or ordinal position, or an array of field names or ordinal position numbers. ADO returns only the data in these fields.</span></span>|

## <a name="remarks"></a><span data-ttu-id="81222-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="81222-124">Remarks</span></span>

<span data-ttu-id="81222-125">Verwenden Sie die **GetRows** -Methode, um Datensätze aus einem **Recordset** -Objekt in ein zweidimensionales Array zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="81222-125">Use the **GetRows** method to copy records from a **Recordset** into a two-dimensional array.</span></span> <span data-ttu-id="81222-126">Der erste Index identifiziert das Feld und der zweite die Nummer des Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="81222-126">The first subscript identifies the field and the second identifies the record number.</span></span> <span data-ttu-id="81222-127">Die *Array* -Variable wird automatisch an die richtige Größe dimensioniert, wenn **GetRows** -Methode die Daten zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="81222-127">The *array* variable is automatically dimensioned to the correct size when the **GetRows** method returns the data.</span></span>

<span data-ttu-id="81222-128">Wenn Sie einen Wert für das Argument *Zeilen* nicht angeben, übernimmt die **GetRows** -Methode alle Datensätze im **Recordset** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="81222-128">If you do not specify a value for the *Rows* argument, the **GetRows** method automatically retrieves all the records in the **Recordset** object.</span></span> <span data-ttu-id="81222-129">Wenn Sie mehr Datensätze anfordern, als verfügbar sind, gibt **GetRows** nur die verfügbaren Datensätze zurück.</span><span class="sxs-lookup"><span data-stu-id="81222-129">If you request more records than are available, **GetRows** returns only the number of available records.</span></span>

<span data-ttu-id="81222-130">Wenn das **Recordset** -Objekt Lesezeichen unterstützt, können Sie angeben, an welcher Datensatz **GetRows** -Methode beginnen soll das Abrufen von Daten, indem Sie den Wert der [Bookmark](bookmark-property-ado.md) -Eigenschaft des Datensatzes in der *Start* -Argument übergeben.</span><span class="sxs-lookup"><span data-stu-id="81222-130">If the **Recordset** object supports bookmarks, you can specify at which record the **GetRows** method should begin retrieving data by passing the value of that record's [Bookmark](bookmark-property-ado.md) property in the *Start* argument.</span></span>

<span data-ttu-id="81222-131">Wenn Sie die Felder zu beschränken, die das Aufrufen von **GetRows zurückgegebenen** möchten, können Sie ein einzelnes Feld Namen und die Nummer oder ein Array mit Feldnamen/Nummern in das Argument *Fields* übergeben.</span><span class="sxs-lookup"><span data-stu-id="81222-131">If you want to restrict the fields that the **GetRows** call returns, you can pass either a single field name/number or an array of field names/numbers in the *Fields* argument.</span></span>

<span data-ttu-id="81222-132">Nachdem Sie **GetRows** aufgerufen haben, wird der nächste ungelesene Datensatz zum aktuellen Datensatz, oder die [EOF](bof-eof-properties-ado.md)-Eigenschaft wird auf **True** festgelegt, wenn keine weiteren Datensätze verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="81222-132">After you call **GetRows**, the next unread record becomes the current record, or the [EOF](bof-eof-properties-ado.md) property is set to **True** if there are no more records.</span></span>

