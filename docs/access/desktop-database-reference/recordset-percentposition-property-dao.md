---
title: Recordset. PercentPosition-Eigenschaft (DAO)
TOCTitle: PercentPosition Property
ms:assetid: aebbda44-ed72-7a6c-0cd5-28c8997d4d96
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821751(v=office.15)
ms:contentKeyID: 48547077
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 118b93641184eed367cd5f0f00a15a13ff28cd58
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300163"
---
# <a name="recordsetpercentposition-property-dao"></a>Recordset. PercentPosition-Eigenschaft (DAO)

**Gilt für**: Access 2013, Office 2013

Legt einen Wert fest, der die ungefähre Position des aktuellen Datensatzes (aktueller Datensatz) im **[Recordset](recordset-object-dao.md)** -Objekt basierend auf einem Prozentwert der Datensätze im **Recordset** angibt, oder gibt diesen Wert zurück.

## <a name="syntax"></a>Syntax

*Ausdruck* . PercentPosition

*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

To indicate or change the approximate position of the current record in a **Recordset** object, you can check or set the **PercentPosition** property. When working with a dynaset- or snapshot-type **Recordset** object opened directly from a base table, first populate the **Recordset** object by moving to the last record before you set or check the **PercentPosition** property. If you use the **PercentPosition** property before fully populating the **Recordset** object, the amount of movement is relative to the number of records accessed as indicated by the **[RecordCount](recordset-recordcount-property-dao.md)** property setting. You can move to the last record by using the **[MoveLast](recordset-movelast-method-dao.md)** method.

> [!NOTE]
> Die Verwendung der **PercentPosition** -Eigenschaft zum Verschieben des aktuellen Datensatzes in einen bestimmten Datensatz in einem **Recordset** -Objekt wird nicht empfohlen. Die **[Bookmark](recordset-bookmark-property-dao.md)** -Eigenschaft eignet sich besser für diese Aufgabe.

Wenn Sie einen Wert für die **PercentPosition**-Eigenschaft festgelegt haben, wird der Datensatz an der ungefähren Position, die dem betreffenden Wert entspricht, zum aktuellen Datensatz. Die **PercentPosition**-Eigenschaft wird auf einen Wert zurückgesetzt, der die ungefähre Position des aktuellen Datensatzes widerspiegelt. Beispiel: Wenn das **Recordset**-Objekt nur 5 Datensätze enthält und Sie seine **PercentPosition**-Eigenschaft auf den Wert 77 festlegen, kann der von der **PercentPosition**-Eigenschaft zurückgegebene Wert 80 sein, anstelle von 77.

Die **PercentPosition** -Eigenschaft gilt für alle Typen von **Recordset** -Objekten, mit Ausnahme von "Forward-Only"-Typ **Recordset** -Objekte oder **Recordset** -Objekte, die von Passthrough-Abfragen für Remotedatenbanken geöffnet werden.

Sie können die **PercentPosition**-Eigenschaft mit einer Bildlaufleiste auf einem Formular oder in einem Textfeld verwenden, um die Position des aktuellen Datensatzes in einem **Recordset**-Objekt anzugeben.

## <a name="example"></a>Beispiel

In diesem Beispiel wird die **PercentPosition**-Eigenschaft verwendet, um die Position des aktuellen Datensatzzeigers relativ zum Anfang des **Recordset**-Objekts anzugeben.

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
