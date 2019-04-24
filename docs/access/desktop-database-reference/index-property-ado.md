---
title: Index-Eigenschaft (ADO)
TOCTitle: Index property (ADO)
ms:assetid: 4cc00521-dcb4-19b2-2174-6e0e9bd42e62
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249241(v=office.15)
ms:contentKeyID: 48544715
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7d436ec9102c4c75688b6c6ac973ca85e8c280d0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291706"
---
# <a name="index-property-ado"></a><span data-ttu-id="1890a-102">Index-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="1890a-102">Index property (ADO)</span></span>


<span data-ttu-id="1890a-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1890a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1890a-104">Gibt den Namen des Indexes an, der aktuell für das [Recordset](recordset-object-ado.md)-Objekt wirksam ist.</span><span class="sxs-lookup"><span data-stu-id="1890a-104">Indicates the name of the index currently in effect for a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="1890a-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="1890a-105">Settings and return values</span></span>

<span data-ttu-id="1890a-106">Legt den Indexnamen als **String**-Wert fest oder gibt den Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="1890a-106">Sets or returns a **String** value, which is the name of the index.</span></span>

## <a name="remarks"></a><span data-ttu-id="1890a-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1890a-107">Remarks</span></span>

<span data-ttu-id="1890a-p101">Der durch die **Index**-Eigenschaft benannte Index muss zuvor für die Basistabelle deklariert worden sein, die dem **Recordset**-Objekt zugrunde liegt. Das heißt, der Index muss programmgesteuert entweder als ADOX-[Index](index-object-adox.md)-Objekt oder beim Erstellen der Basistabelle deklariert worden sein.</span><span class="sxs-lookup"><span data-stu-id="1890a-p101">The index named by the **Index** property must have previously been declared on the base table underlying the **Recordset** object. That is, the index must have been declared programmatically either as an ADOX [Index](index-object-adox.md) object, or when the base table was created.</span></span>

<span data-ttu-id="1890a-p102">Wenn der Index nicht festgelegt werden kann, tritt ein Laufzeitfehler auf. Die **Index** -Eigenschaft kann in folgenden Fällen nicht festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="1890a-p102">A run-time error will occur if the index cannot be set. The **Index** property cannot be set:</span></span>

  - <span data-ttu-id="1890a-112">Innerhalb eines [WillChangeRecordset](willchangerecordset-and-recordsetchangecomplete-events-ado.md)- oder eines **RecordsetChangeComplete** -Ereignishandlers.</span><span class="sxs-lookup"><span data-stu-id="1890a-112">Within a [WillChangeRecordset](willchangerecordset-and-recordsetchangecomplete-events-ado.md) or **RecordsetChangeComplete** event handler.</span></span>

  - <span data-ttu-id="1890a-113">Während das **Recordset**-Objekt noch eine Operation ausführt (was mithilfe der [State](state-property-ado.md)-Eigenschaft ermittelt werden kann).</span><span class="sxs-lookup"><span data-stu-id="1890a-113">If the **Recordset** is still executing an operation (which can be determined by the [State](state-property-ado.md) property).</span></span>

  - <span data-ttu-id="1890a-114">Wenn mit der [Filter](filter-property-ado.md)-Eigenschaft ein Filter für das **Recordset**-Objekt festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="1890a-114">If a filter has been set on the **Recordset** with the [Filter](filter-property-ado.md) property.</span></span>

<span data-ttu-id="1890a-115">Die **Index**-Eigenschaft kann immer fehlerfrei festgelegt werden, wenn das **Recordset**-Objekt geschlossen ist. Wenn der zugrunde liegende Anbieter jedoch keine Indizes unterstützt, wird das **Recordset**-Objekt nicht fehlerfrei geöffnet, oder der Index kann nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1890a-115">The **Index** property can always be set successfully if the **Recordset** is closed, but the **Recordset** will not open successfully, or the index will not be usable, if the underlying provider does not support indexes.</span></span>

<span data-ttu-id="1890a-p103">Wenn der Index festgelegt werden kann, ändert sich möglicherweise die aktuelle Zeilenposition. Dadurch wird die [AbsolutePosition](absoluteposition-property-ado.md)-Eigenschaft aktualisiert und die Ereignisse **WillChangeRecordset**, **RecordsetChangeComplete**, [WillMove](willmove-and-movecomplete-events-ado.md) und [MoveComplete](willmove-and-movecomplete-events-ado.md) werden generiert.</span><span class="sxs-lookup"><span data-stu-id="1890a-p103">If the index can be set, the current row position may change. This will cause an update to the [AbsolutePosition](absoluteposition-property-ado.md) property, and the generation of **WillChangeRecordset**, **RecordsetChangeComplete**, [WillMove](willmove-and-movecomplete-events-ado.md), and [MoveComplete](willmove-and-movecomplete-events-ado.md) events.</span></span>

<span data-ttu-id="1890a-p104">Wenn der Index festgelegt werden kann und die [LockType](locktype-property-ado.md)-Eigenschaft auf **AdLockPessimistic** oder **AdLockOptimistic** festgelegt ist, wird eine implizite [UpdateBatch](updatebatch-method-ado.md)-Operation ausgeführt. Dadurch werden die aktuellen und betroffenen Gruppen freigegeben. Alle vorhanden Filter werden freigegeben, und die aktuelle Zeilenposition wird zur ersten Zeile des neu angeordneten **Recordset** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="1890a-p104">If the index can be set and the [LockType](locktype-property-ado.md) property is **adLockPessimistic** or **adLockOptimistic**, then an implicit [UpdateBatch](updatebatch-method-ado.md) operation is performed. This releases the current and affected groups. Any existing filter is released, and the current row position is changed to the first row of the reordered **Recordset**.</span></span>

<span data-ttu-id="1890a-121">Die **Index** -Eigenschaft wird zusammen mit der [Seek](seek-method-ado.md)-Methode verwendet.</span><span class="sxs-lookup"><span data-stu-id="1890a-121">The **Index** property is used in conjunction with the [Seek](seek-method-ado.md) method.</span></span> <span data-ttu-id="1890a-122">Wenn der zugrunde liegende Anbieter die **Index** -Eigenschaft und somit die **Seek** -Methode nicht unterstützt, können Sie stattdessen die [Find](find-method-ado.md)-Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="1890a-122">If the underlying provider does not support the **Index** property, and thus the **Seek** method, consider using the [Find](find-method-ado.md) method instead.</span></span> <span data-ttu-id="1890a-123">Bestimmen Sie, ob das **Recordset** -Objekt Indizes mit der [unterStützt](supports-method-ado.md)**(AddIndex)** -Methode unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1890a-123">Determine whether the **Recordset** object supports indexes with the [Supports](supports-method-ado.md)**(adIndex)** method.</span></span>

<span data-ttu-id="1890a-124">Die integrierte **Index**-Eigenschaft hängt nicht mit der dynamischen [Optimize](optimize-property-dynamic-ado.md)-Eigenschaft zusammen, obwohl sich beide auf Indizes beziehen.</span><span class="sxs-lookup"><span data-stu-id="1890a-124">The built-in **Index** property is not related to the dynamic [Optimize](optimize-property-dynamic-ado.md) property, although they both deal with indexes.</span></span>

