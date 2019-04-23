---
title: Move-Methode-ActiveX Data Objects (ADO)
TOCTitle: Move method (ADO)
ms:assetid: 1f858654-5fa3-273d-7cdc-574c5f09a420
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248982(v=office.15)
ms:contentKeyID: 48543645
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6c7db661e590bc21605d9c289b1de6d4ae9f46e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288834"
---
# <a name="move-method-ado"></a><span data-ttu-id="2e638-102">Move-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="2e638-102">Move method (ADO)</span></span>

<span data-ttu-id="2e638-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2e638-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2e638-104">Verschiebt die Position des aktuellen Datensatzes in einem [Recordset](recordset-object-ado.md)-Objekt.</span><span class="sxs-lookup"><span data-stu-id="2e638-104">Moves the position of the current record in a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e638-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e638-105">Syntax</span></span>

<span data-ttu-id="2e638-106">*Recordset*. *Numrecords*verschieben, *starten*</span><span class="sxs-lookup"><span data-stu-id="2e638-106">*recordset*.Move *NumRecords*, *Start*</span></span>

## <a name="parameters"></a><span data-ttu-id="2e638-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e638-107">Parameters</span></span>

|<span data-ttu-id="2e638-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e638-108">Parameter</span></span>|<span data-ttu-id="2e638-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2e638-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="2e638-110">*NumRecords*</span><span class="sxs-lookup"><span data-stu-id="2e638-110">*NumRecords*</span></span> |<span data-ttu-id="2e638-111">Ein signierter **Long** -Ausdruck, der die Anzahl von Datensätzen angibt, um die die aktuelle Position des Datensatzes verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="2e638-111">A signed **Long** expression that specifies the number of records that the current record position moves.</span></span>|
|<span data-ttu-id="2e638-112">*Start*</span><span class="sxs-lookup"><span data-stu-id="2e638-112">*Start*</span></span> |<span data-ttu-id="2e638-p101">Optional. Ein **String** -Wert oder ein **Variant** -Wert, der eine Textmarke ergibt. Sie können auch einen [BookmarkEnum](bookmarkenum.md)-Wert verwenden.</span><span class="sxs-lookup"><span data-stu-id="2e638-p101">Optional. A **String** value or **Variant** that evaluates to a bookmark. You can also use a [BookmarkEnum](bookmarkenum.md) value.</span></span>|

## <a name="remarks"></a><span data-ttu-id="2e638-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2e638-116">Remarks</span></span>

<span data-ttu-id="2e638-117">Die **Move**-Methode wird für alle **Recordset**-Objekte unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2e638-117">The **Move** method is supported on all **Recordset** objects.</span></span>

<span data-ttu-id="2e638-p102">Wenn das Argument *NumRecords* größer als null ist, wird die aktuelle Datensatzposition vorwärts verschoben (zum Ende des **Recordset**-Objekts hin). Wenn *NumRecords* kleiner als null ist, wird die aktuelle Datensatzposition rückwärts verschoben (zum Anfang des **Recordset**-Objekts hin).</span><span class="sxs-lookup"><span data-stu-id="2e638-p102">If the *NumRecords* argument is greater than zero, the current record position moves forward (toward the end of the **Recordset**). If *NumRecords* is less than zero, the current record position moves backward (toward the beginning of the **Recordset**).</span></span>

<span data-ttu-id="2e638-120">Wenn der **Verschiebungs** Aufruf die aktuelle Datensatzposition vor dem ersten Datensatz verschiebt, wird der aktuelle Datensatz von ADO auf die Position vor dem ersten Datensatz im Recordset-Objekt festgelegt ([BOF](bof-eof-properties-ado.md) ist **true**).</span><span class="sxs-lookup"><span data-stu-id="2e638-120">If the **Move** call would move the current record position to a point before the first record, ADO sets the current record to the position before the first record in the recordset ([BOF](bof-eof-properties-ado.md) is **True**).</span></span> <span data-ttu-id="2e638-121">Beim Versuch, den Datensatz nach hinten zu verschieben, wenn die **BOF**-Eigenschaft bereits auf **True** festgelegt ist, wird ein Fehler generiert.</span><span class="sxs-lookup"><span data-stu-id="2e638-121">An attempt to move backward when the **BOF** property is already **True** generates an error.</span></span>

<span data-ttu-id="2e638-p104">Wenn die aktuelle Position des Datensatzes beim Aufrufen von **Move** an eine Stelle hinter dem letzten Datensatz verschoben werden würde, legt ADO den aktuellen Datensatz auf die Position nach dem letzten Datensatz in der Datensatzgruppe fest ([EOF](bof-eof-properties-ado.md) ist **True**). Beim Versuch, den Datensatz nach vorn zu verschieben, wenn die **EOF**-Eigenschaft bereits auf **True** festgelegt ist, wird ein Fehler generiert.</span><span class="sxs-lookup"><span data-stu-id="2e638-p104">If the **Move** call would move the current record position to a point after the last record, ADO sets the current record to the position after the last record in the recordset ([EOF](bof-eof-properties-ado.md) is **True**). An attempt to move forward when the **EOF** property is already **True** generates an error.</span></span>

<span data-ttu-id="2e638-124">Beim Aufrufen der **Move**-Methode aus einem leeren **Recordset**-Objekt wird ein Fehler generiert.</span><span class="sxs-lookup"><span data-stu-id="2e638-124">Calling the **Move** method from an empty **Recordset** object generates an error.</span></span>

<span data-ttu-id="2e638-p105">Wenn Sie das Argument *Start* übergeben, ist die Verschiebung relativ zum Datensatz mit dieser Textmarke, wobei davon ausgegangen wird, dass das **Recordset**-Objekt Textmarken unterstützt. Ist es nicht angegeben, ist die Verschiebung relativ zum aktuellen Datensatz.</span><span class="sxs-lookup"><span data-stu-id="2e638-p105">If you pass the *Start* argument, the move is relative to the record with this bookmark, assuming the **Recordset** object supports bookmarks. If not specified, the move is relative to the current record.</span></span>

<span data-ttu-id="2e638-p106">Falls Sie mithilfe der [CacheSize](cachesize-property-ado.md)-Eigenschaft Datensätze vom Anbieter lokal zwischenspeichern, wird durch das Übergeben eines Arguments *NumRecords*, mit dem die aktuelle Datensatzposition außerhalb der aktuellen Gruppe zwischengespeicherter Datensätze verschoben wird, ADO gezwungen, eine neue Datensatzgruppe ausgehend vom Zieldatensatz abzurufen. Die **CacheSize**-Eigenschaft bestimmt die Größe der neu abgerufenen Gruppe, und der Zieldatensatz ist der erste abgerufene Datensatz.</span><span class="sxs-lookup"><span data-stu-id="2e638-p106">If you are using the [CacheSize](cachesize-property-ado.md) property to locally cache records from the provider, passing a *NumRecords* argument that moves the current record position outside the current group of cached records forces ADO to retrieve a new group of records, starting from the destination record. The **CacheSize** property determines the size of the newly retrieved group, and the destination record is the first record retrieved.</span></span>

<span data-ttu-id="2e638-p107">Ist das **Recordset**-Objekt vorwärtsgerichtet, kann der Benutzer auch ein Argument *NumRecords* übergeben, das kleiner als 0 (Null) ist, wenn sich das Ziel innerhalb der aktuellen Gruppe der zwischengespeicherten Datensätze befindet. Wenn die aktuelle Position des Datensatzes beim Aufrufen von **Move** auf einen Datensatz vor dem ersten zwischengespeicherten Datensatz verschoben wird, tritt ein Fehler auf. Daher können Sie statt einem Anbieter, der nur einen vorwärtsgerichteten Bildlauf unterstützt, einen Datensatzcache verwenden, der einen vollständigen Bildlauf unterstützt. Da zwischengespeicherte Datensätze in den Speicher geladen werden, sollten Sie nur so viele Datensätze wie erforderlich zwischenspeichern. Selbst wenn ein vorwärtsgerichtetes **Recordset**-Objekt rückwärtsgerichtete Verschiebungen dieser Art unterstützt, wird beim Aufrufen der [MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)-Methode für ein vorwärtsgerichtetes **Recordset**-Objekt ein Fehler generiert.</span><span class="sxs-lookup"><span data-stu-id="2e638-p107">If the **Recordset** object is forward only, a user can still pass a *NumRecords* argument less than zero, provided the destination is within the current set of cached records. If the **Move** call would move the current record position to a record before the first cached record, an error will occur. Thus, you can use a record cache that supports full scrolling over a provider that supports only forward scrolling. Because cached records are loaded into memory, you should avoid caching more records than is necessary. Even if a forward-only **Recordset** object supports backward moves in this way, calling the [MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) method on any forward-only **Recordset** object will still generate an error.</span></span>


> [!NOTE]
> <span data-ttu-id="2e638-p108">[!HINWEIS] Ob in einem vorwärtgerichteten **Recordset** -Objekt rückwärtgerichtete Verschiebungen unterstützt werden, hängt vom Anbieter ab. Wenn der aktuelle Datensatz hinter dem letzten Datensatz im **Recordset** -Objekt positioniert wurde, wird bei einer rückwärtsgerichteten Verschiebung mithilfe von **Move** möglicherweise nicht die richtige aktuelle Position erzielt.</span><span class="sxs-lookup"><span data-stu-id="2e638-p108">Support for moving backwards in a forward-only **Recordset** is not predictable, depending upon your provider. If the current record has been postioned after the last record in the **Recordset**, **Move** backwards may not result in the correct current position.</span></span>


