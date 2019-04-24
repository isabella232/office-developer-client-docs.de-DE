---
title: Recordset2. PercentPosition-Eigenschaft (DAO)
TOCTitle: PercentPosition Property
ms:assetid: 830a7d26-6817-233f-ce24-80b572c1c100
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196732(v=office.15)
ms:contentKeyID: 48545996
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052973
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 7b0a086004d987a73e6dfb18fe5f919c239fb66c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307224"
---
# <a name="recordset2percentposition-property-dao"></a><span data-ttu-id="5a548-102">Recordset2. PercentPosition-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="5a548-102">Recordset2.PercentPosition property (DAO)</span></span>

<span data-ttu-id="5a548-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5a548-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5a548-104">Legt einen Wert fest, der die ungefähre Position des aktuellen Datensatzes (aktueller Datensatz) im **[Recordset](recordset-object-dao.md)** -Objekt basierend auf einem Prozentwert der Datensätze im **Recordset** angibt, oder gibt diesen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="5a548-104">Sets or returns a value indicating the approximate location of the current record in the **[Recordset](recordset-object-dao.md)** object based on a percentage of the records in the **Recordset**.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a548-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a548-105">Syntax</span></span>

<span data-ttu-id="5a548-106">*Ausdruck* . PercentPosition</span><span class="sxs-lookup"><span data-stu-id="5a548-106">*expression* .PercentPosition</span></span>

<span data-ttu-id="5a548-107">*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="5a548-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a548-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5a548-108">Remarks</span></span>

<span data-ttu-id="5a548-p101">To indicate or change the approximate position of the current record in a **Recordset** object, you can check or set the **PercentPosition** property. When working with a dynaset- or snapshot-type **Recordset** object opened directly from a base table, first populate the **Recordset** object by moving to the last record before you set or check the **PercentPosition** property. If you use the **PercentPosition** property before fully populating the **Recordset** object, the amount of movement is relative to the number of records accessed as indicated by the **[RecordCount](recordset2-recordcount-property-dao.md)** property setting. You can move to the last record by using the **[MoveLast](recordset2-movelast-method-dao.md)** method.</span><span class="sxs-lookup"><span data-stu-id="5a548-p101">To indicate or change the approximate position of the current record in a **Recordset** object, you can check or set the **PercentPosition** property. When working with a dynaset- or snapshot-type **Recordset** object opened directly from a base table, first populate the **Recordset** object by moving to the last record before you set or check the **PercentPosition** property. If you use the **PercentPosition** property before fully populating the **Recordset** object, the amount of movement is relative to the number of records accessed as indicated by the **[RecordCount](recordset2-recordcount-property-dao.md)** property setting. You can move to the last record by using the **[MoveLast](recordset2-movelast-method-dao.md)** method.</span></span>

> [!NOTE]
> <span data-ttu-id="5a548-113">Die Verwendung der **PercentPosition** -Eigenschaft zum Verschieben des aktuellen Datensatzes in einen bestimmten Datensatz in einem **Recordset** -Objekt wird nicht empfohlen.</span><span class="sxs-lookup"><span data-stu-id="5a548-113">Using the **PercentPosition** property to move the current record to a specific record in a **Recordset** object isn't recommended.</span></span> <span data-ttu-id="5a548-114">Die **[Bookmark](recordset2-bookmark-property-dao.md)** -Eigenschaft eignet sich besser für diese Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="5a548-114">The **[Bookmark](recordset2-bookmark-property-dao.md)** property is better suited for this task.</span></span>

<span data-ttu-id="5a548-p103">Wenn Sie einen Wert für die **PercentPosition**-Eigenschaft festgelegt haben, wird der Datensatz an der ungefähren Position, die dem betreffenden Wert entspricht, zum aktuellen Datensatz. Die **PercentPosition**-Eigenschaft wird auf einen Wert zurückgesetzt, der die ungefähre Position des aktuellen Datensatzes widerspiegelt. Beispiel: Wenn das **Recordset**-Objekt nur 5 Datensätze enthält und Sie seine **PercentPosition**-Eigenschaft auf den Wert 77 festlegen, kann der von der **PercentPosition**-Eigenschaft zurückgegebene Wert 80 sein, anstelle von 77.</span><span class="sxs-lookup"><span data-stu-id="5a548-p103">Once you set the **PercentPosition** property to a value, the record at the approximate position corresponding to that value becomes current, and the **PercentPosition** property is reset to a value that reflects the approximate position of the current record. For example, if your **Recordset** object contains only five records, and you set its **PercentPosition** property value to 77, the value returned from the **PercentPosition** property may be 80, not 77.</span></span>

<span data-ttu-id="5a548-117">Die **PercentPosition** -Eigenschaft gilt für alle Typen von **Recordset** -Objekten, mit Ausnahme von "Forward-Only"-Typ **Recordset** -Objekte oder **Recordset** -Objekte, die von Passthrough-Abfragen für Remotedatenbanken geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="5a548-117">The **PercentPosition** property applies to all types of **Recordset** objects except for forward–only–type **Recordset** objects or **Recordset** objects opened from pass-through queries against remote databases.</span></span>

<span data-ttu-id="5a548-118">Sie können die **PercentPosition**-Eigenschaft mit einer Bildlaufleiste auf einem Formular oder in einem Textfeld verwenden, um die Position des aktuellen Datensatzes in einem **Recordset**-Objekt anzugeben.</span><span class="sxs-lookup"><span data-stu-id="5a548-118">You can use the **PercentPosition** property with a scroll bar on a form or text box to indicate the location of the current record in a **Recordset** object.</span></span>

## <a name="example"></a><span data-ttu-id="5a548-119">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5a548-119">Example</span></span>

<span data-ttu-id="5a548-120">In diesem Beispiel wird die **PercentPosition**-Eigenschaft verwendet, um die Position des aktuellen Datensatzzeigers relativ zum Anfang des **Recordset**-Objekts anzugeben.</span><span class="sxs-lookup"><span data-stu-id="5a548-120">This example uses the **PercentPosition** property to show the position of the current record pointer relative to the beginning of the **Recordset**.</span></span>

```vb
    Sub PercentPositionX() 
     
     Dim dbsNorthwind As Database 
     Dim rstProducts As Recordset2 
     Dim strFind As String 
     Dim strMessage As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     ' PercentPosition only works with dynasets or snapshots. 
     Set rstProducts = dbsNorthwind.OpenRecordset( _ 
     "SELECT ProductName FROM Products " & _ 
     "ORDER BY ProductName", dbOpenSnapshot) 
     
     With rstProducts 
     ' Populate the Recordset. 
     .MoveLast 
     .MoveFirst 
     
     Do While True 
     ' Show current record information and ask user 
     ' for input. 
     strMessage = "Product: " & !ProductName & vbCr & _ 
     "The record pointer is " & _ 
     Format(.PercentPosition, "##0.0") & _ 
     "% from the " & vbCr & _ 
     "beginning of the Recordset." & vbCr & _ 
     "Please enter a character search string " & _ 
     "for a product name." 
     strFind = Trim(InputBox(strMessage)) 
     If strFind = "" Then Exit Do 
     
     ' Try to find a record matching the search string. 
     .FindFirst "ProductName >= '" & strFind & "'" 
     If .NoMatch Then .MoveLast 
     Loop 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
