---
title: GetRows-Methode (ADO)
TOCTitle: GetRows method (ADO)
ms:assetid: 570e6f1c-c17a-7d9a-c172-387894a3a1f1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249292(v=office.15)
ms:contentKeyID: 48544963
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 61f7ce441eb837b76e824b55393741e0cf821bb5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292223"
---
# <a name="getrows-method-ado"></a><span data-ttu-id="23bdf-102">GetRows-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="23bdf-102">GetRows method (ADO)</span></span>

<span data-ttu-id="23bdf-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="23bdf-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="23bdf-104">Ruft mehrere Datensätze eines [Recordset](recordset-object-ado.md)-Objekts in ein Array ab.</span><span class="sxs-lookup"><span data-stu-id="23bdf-104">Retrieves multiple records of a [Recordset](recordset-object-ado.md) object into an array.</span></span>

## <a name="syntax"></a><span data-ttu-id="23bdf-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="23bdf-105">Syntax</span></span>

<span data-ttu-id="23bdf-106">*Array* = -*Recordset*. GetRows (*Rows*, *Start*, *Fields* )</span><span class="sxs-lookup"><span data-stu-id="23bdf-106">*array* = *recordset*.GetRows(*Rows*, *Start*, *Fields* )</span></span>

## <a name="return-value"></a><span data-ttu-id="23bdf-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="23bdf-107">Return value</span></span>

<span data-ttu-id="23bdf-108">Gibt einen **Variant**-Wert zurück, deren dessen Wert es sich um ein zweidimensionales Array handelt.</span><span class="sxs-lookup"><span data-stu-id="23bdf-108">Returns a **Variant** whose value is a two-dimensional array.</span></span>

## <a name="parameters"></a><span data-ttu-id="23bdf-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="23bdf-109">Parameters</span></span>

|<span data-ttu-id="23bdf-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="23bdf-110">Parameter</span></span>|<span data-ttu-id="23bdf-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="23bdf-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="23bdf-112">*Rows*</span><span class="sxs-lookup"><span data-stu-id="23bdf-112">*Rows*</span></span> |<span data-ttu-id="23bdf-p101">Optional. Ein [GetRowsOptionEnum](getrowsoptionenum.md)-Wert, der die Anzahl der abzurufenden Datensätze angibt. Der Standardwert lautet **adGetRowsRest**.</span><span class="sxs-lookup"><span data-stu-id="23bdf-p101">Optional. A [GetRowsOptionEnum](getrowsoptionenum.md) value that indicates the number of records to retrieve. The default is **adGetRowsRest**.</span></span>|
|<span data-ttu-id="23bdf-116">*Start*</span><span class="sxs-lookup"><span data-stu-id="23bdf-116">*Start*</span></span> |<span data-ttu-id="23bdf-p102">Optional. Ein **String** -Wert oder ein **Variant** -Wert, der die Textmarke für den Datensatz ergibt, bei dem der **GetRows** -Vorgang beginnen soll. Sie können auch einen [BookmarkEnum](bookmarkenum.md)-Wert verwenden.</span><span class="sxs-lookup"><span data-stu-id="23bdf-p102">Optional. A **String** value or **Variant** that evaluates to the bookmark for the record from which the **GetRows** operation should begin. You can also use a [BookmarkEnum](bookmarkenum.md) value.</span></span>|
|<span data-ttu-id="23bdf-120">*Fields*</span><span class="sxs-lookup"><span data-stu-id="23bdf-120">*Fields*</span></span> |<span data-ttu-id="23bdf-p103">Optional. Ein **Variant** -Wert, der einen einzelnen Feldnamen oder eine einzelne Ordnungsposition oder ein Array mit Feldnamen oder Nummern für Ordnungspositionen darstellt. ADO gibt nur die Daten in diesen Feldern zurück.</span><span class="sxs-lookup"><span data-stu-id="23bdf-p103">Optional. A **Variant** that represents a single field name or ordinal position, or an array of field names or ordinal position numbers. ADO returns only the data in these fields.</span></span>|

## <a name="remarks"></a><span data-ttu-id="23bdf-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="23bdf-124">Remarks</span></span>

<span data-ttu-id="23bdf-p104">Verwenden Sie die **GetRows**-Methode, um Datensätze aus einem **Recordset**-Objekt in ein zweidimensionales Array zu kopieren. Der erste Index identifiziert das Feld und der zweite die Nummer des Datensatzes. Die *Array*-Variable wird automatisch an die richtige Größe angepasst, wenn die **GetRows**-Methode die Daten zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="23bdf-p104">Use the **GetRows** method to copy records from a **Recordset** into a two-dimensional array. The first subscript identifies the field and the second identifies the record number. The *array* variable is automatically dimensioned to the correct size when the **GetRows** method returns the data.</span></span>

<span data-ttu-id="23bdf-p105">Wenn Sie für das Argument *Rows* keinen Wert angeben, ruft die **GetRows**-Methode automatisch alle Datensätze im **Recordset**-Objekt ab. Wenn Sie mehr Datensätze anfordern, als verfügbar sind, gibt **GetRows** nur die verfügbaren Datensätze zurück.</span><span class="sxs-lookup"><span data-stu-id="23bdf-p105">If you do not specify a value for the *Rows* argument, the **GetRows** method automatically retrieves all the records in the **Recordset** object. If you request more records than are available, **GetRows** returns only the number of available records.</span></span>

<span data-ttu-id="23bdf-130">Wenn das **Recordset**-Objekt Textmarken unterstützt, können Sie festlegen, bei welchem Datensatz die **GetRows**-Methode mit dem Abrufen von Daten beginnen soll, indem Sie den Wert der [Bookmark](bookmark-property-ado.md)-Eigenschaft dieses Datensatzes in das Argument *Start* übergeben.</span><span class="sxs-lookup"><span data-stu-id="23bdf-130">If the **Recordset** object supports bookmarks, you can specify at which record the **GetRows** method should begin retrieving data by passing the value of that record's [Bookmark](bookmark-property-ado.md) property in the *Start* argument.</span></span>

<span data-ttu-id="23bdf-131">Wenn Sie die beim Aufrufen von **GetRows** zurückgegebenen Felder einschränken möchten, können Sie einen einzelnen Feldnamen/eine einzelne Nummer oder ein Array mit Feldnamen/Nummern in das Argument *Fields* übergeben.</span><span class="sxs-lookup"><span data-stu-id="23bdf-131">If you want to restrict the fields that the **GetRows** call returns, you can pass either a single field name/number or an array of field names/numbers in the *Fields* argument.</span></span>

<span data-ttu-id="23bdf-132">Nachdem Sie **GetRows** aufgerufen haben, wird der nächste ungelesene Datensatz zum aktuellen Datensatz, oder die [EOF](bof-eof-properties-ado.md)-Eigenschaft wird auf **True** festgelegt, wenn keine weiteren Datensätze verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="23bdf-132">After you call **GetRows**, the next unread record becomes the current record, or the [EOF](bof-eof-properties-ado.md) property is set to **True** if there are no more records.</span></span>

