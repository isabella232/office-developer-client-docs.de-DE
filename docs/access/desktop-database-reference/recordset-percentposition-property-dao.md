---
title: Recordset.PercentPosition Property (DAO)
TOCTitle: PercentPosition Property
ms:assetid: aebbda44-ed72-7a6c-0cd5-28c8997d4d96
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821751(v=office.15)
ms:contentKeyID: 48547077
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5793d2b73e424726e91cf3bbb54b09db59123b92
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474217"
---
# <a name="recordsetpercentposition-property-dao"></a><span data-ttu-id="fc3e0-102">Recordset.PercentPosition Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="fc3e0-102">Recordset.PercentPosition Property (DAO)</span></span>


<span data-ttu-id="fc3e0-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="fc3e0-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="fc3e0-104">Legt einen Wert fest, der die ungefähre Position des aktuellen Datensatzes (aktueller Datensatz) im **[Recordset](recordset-object-dao.md)** -Objekt basierend auf einem Prozentwert der Datensätze im **Recordset** angibt, oder gibt diesen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="fc3e0-104">Sets or returns a value indicating the approximate location of the current record in the **[Recordset](recordset-object-dao.md)** object based on a percentage of the records in the **Recordset**.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc3e0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fc3e0-105">Syntax</span></span>

<span data-ttu-id="fc3e0-106">*Ausdruck* . PercentPosition</span><span class="sxs-lookup"><span data-stu-id="fc3e0-106">*expression* .PercentPosition</span></span>

<span data-ttu-id="fc3e0-107">*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="fc3e0-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc3e0-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fc3e0-108">Remarks</span></span>

<span data-ttu-id="fc3e0-p101">Zum Festlegen oder Ändern der ungefähren Position des aktuellen Datensatz in einem Recordset-Objekt können Sie die PercentPosition-Eigenschaft überprüfen oder festlegen. Wenn Sie ein Recordset-Objekt vom Typ Dynaset oder Snapshot verwenden, das direkt in einer Basistabelle geöffnet wurde, füllen Sie zunächst das Recordset-Objekt auf, indem Sie zum letzten Datensatz gehen. Anschließend legen Sie die PercentPosition-Eigenschaft fest oder überprüfen sie. Wenn Sie die PercentPosition-Eigenschaft verwenden, bevor Sie das Recordset-Objekt vollständig aufgefüllt haben, erfolgt die Bewegung relativ zur Anzahl der Datensätze, auf die laut des Werts der RecordCount-Eigenschaft zugegriffen wurde. Mithilfe der MoveLast-Methode können Sie zum letzten Datensatz wechseln.</span><span class="sxs-lookup"><span data-stu-id="fc3e0-p101">To indicate or change the approximate position of the current record in a **Recordset** object, you can check or set the **PercentPosition** property. When working with a dynaset- or snapshot-type **Recordset** object opened directly from a base table, first populate the **Recordset** object by moving to the last record before you set or check the **PercentPosition** property. If you use the **PercentPosition** property before fully populating the **Recordset** object, the amount of movement is relative to the number of records accessed as indicated by the **[RecordCount](recordset-recordcount-property-dao.md)** property setting. You can move to the last record by using the **[MoveLast](recordset-movelast-method-dao.md)** method.</span></span>


> [!NOTE]
> <P><span data-ttu-id="fc3e0-113">[!HINWEIS] Es wird nicht empfohlen, die <STRONG>PercentPosition</STRONG>-Eigenschaft zu verwenden, um zu einem bestimmten Datensatz in einem <STRONG>Recordset</STRONG>-Objekt zu wechseln. Die <STRONG><A href="recordset-bookmark-property-dao.md">Bookmark</A></STRONG> -Eigenschaft ist besser für diese Aufgabe geeignet.</span><span class="sxs-lookup"><span data-stu-id="fc3e0-113">Using the <STRONG>PercentPosition</STRONG> property to move the current record to a specific record in a <STRONG>Recordset</STRONG> object isn't recommended?the <STRONG><A href="recordset-bookmark-property-dao.md">Bookmark</A></STRONG> property is better suited for this task.</span></span></P>



<span data-ttu-id="fc3e0-p102">Wenn Sie einen Wert für die **PercentPosition**-Eigenschaft festgelegt haben, wird der Datensatz an der ungefähren Position, die dem betreffenden Wert entspricht, zum aktuellen Datensatz. Die **PercentPosition**-Eigenschaft wird auf einen Wert zurückgesetzt, der die ungefähre Position des aktuellen Datensatzes widerspiegelt. Beispiel: Wenn das **Recordset**-Objekt nur 5 Datensätze enthält und Sie seine **PercentPosition**-Eigenschaft auf den Wert 77 festlegen, kann der von der **PercentPosition**-Eigenschaft zurückgegebene Wert 80 sein, anstelle von 77.</span><span class="sxs-lookup"><span data-stu-id="fc3e0-p102">Once you set the **PercentPosition** property to a value, the record at the approximate position corresponding to that value becomes current, and the **PercentPosition** property is reset to a value that reflects the approximate position of the current record. For example, if your **Recordset** object contains only five records, and you set its **PercentPosition** property value to 77, the value returned from the **PercentPosition** property may be 80, not 77.</span></span>

<span data-ttu-id="fc3e0-116">Die **PercentPosition** -Eigenschaft gilt für alle Typen von **Recordset** -Objekten, ausgenommen Forward Typ **Recordset** -Objekte oder **Recordset** -Objekten, die von Pass-Through-Abfragen an Remotedatenbanken geöffnet.</span><span class="sxs-lookup"><span data-stu-id="fc3e0-116">The **PercentPosition** property applies to all types of **Recordset** objects except for forward–only–type **Recordset** objects or **Recordset** objects opened from pass-through queries against remote databases.</span></span>

<span data-ttu-id="fc3e0-117">Sie können die **PercentPosition**-Eigenschaft mit einer Bildlaufleiste auf einem Formular oder in einem Textfeld verwenden, um die Position des aktuellen Datensatzes in einem **Recordset**-Objekt anzugeben.</span><span class="sxs-lookup"><span data-stu-id="fc3e0-117">You can use the **PercentPosition** property with a scroll bar on a form or text box to indicate the location of the current record in a **Recordset** object.</span></span>

## <a name="example"></a><span data-ttu-id="fc3e0-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="fc3e0-118">Example</span></span>

<span data-ttu-id="fc3e0-119">In diesem Beispiel wird die **PercentPosition**-Eigenschaft verwendet, um die Position des aktuellen Datensatzzeigers relativ zum Anfang des **Recordset**-Objekts anzugeben.</span><span class="sxs-lookup"><span data-stu-id="fc3e0-119">This example uses the **PercentPosition** property to show the position of the current record pointer relative to the beginning of the **Recordset**.</span></span>

```vb
    Sub PercentPositionX() 
     
     Dim dbsNorthwind As Database 
     Dim rstProducts As Recordset 
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
