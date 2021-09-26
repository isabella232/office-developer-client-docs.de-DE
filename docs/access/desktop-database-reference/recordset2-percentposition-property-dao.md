---
title: Recordset2.PercentPosition-Eigenschaft (DAO)
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
ms.localizationpriority: medium
ms.openlocfilehash: 18926a17d1c14ae0fae2b911c2114d54b9886e90
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611728"
---
# <a name="recordset2percentposition-property-dao"></a>Recordset2.PercentPosition-Eigenschaft (DAO)

**Gilt für**: Access 2013, Office 2013

Legt einen Wert fest, der die ungefähre Position des aktuellen Datensatzes (aktueller Datensatz) im **[Recordset](recordset-object-dao.md)** -Objekt basierend auf einem Prozentwert der Datensätze im **Recordset** angibt, oder gibt diesen Wert zurück.

## <a name="syntax"></a>Syntax

*Ausdruck* . PercentPosition

*Ausdruck* Eine Variable, die ein **Recordset2-Objekt** darstellt.

## <a name="remarks"></a>HinwBemerkungeneise

To indicate or change the approximate position of the current record in a **Recordset** object, you can check or set the **PercentPosition** property. When working with a dynaset- or snapshot-type **Recordset** object opened directly from a base table, first populate the **Recordset** object by moving to the last record before you set or check the **PercentPosition** property. If you use the **PercentPosition** property before fully populating the **Recordset** object, the amount of movement is relative to the number of records accessed as indicated by the **[RecordCount](recordset2-recordcount-property-dao.md)** property setting. You can move to the last record by using the **[MoveLast](recordset2-movelast-method-dao.md)** method.

> [!NOTE]
> Die Verwendung der **PercentPosition-Eigenschaft** zum Verschieben des aktuellen Datensatzes in einen bestimmten Datensatz in einem **Recordset-Objekt** wird nicht empfohlen. Die **[Bookmark-Eigenschaft](recordset2-bookmark-property-dao.md)** ist für diese Aufgabe besser geeignet.

Wenn Sie einen Wert für die **PercentPosition**-Eigenschaft festgelegt haben, wird der Datensatz an der ungefähren Position, die dem betreffenden Wert entspricht, zum aktuellen Datensatz. Die **PercentPosition**-Eigenschaft wird auf einen Wert zurückgesetzt, der die ungefähre Position des aktuellen Datensatzes widerspiegelt. Beispiel: Wenn das **Recordset**-Objekt nur 5 Datensätze enthält und Sie seine **PercentPosition**-Eigenschaft auf den Wert 77 festlegen, kann der von der **PercentPosition**-Eigenschaft zurückgegebene Wert 80 sein, anstelle von 77.

Die **PercentPosition-Eigenschaft** gilt für alle **Recordset-Objekttypen** mit Ausnahme von **Recordset-Objekten** vom Typ "Forward-only" oder **"Recordset"-Objekte,** die aus Pass-Through-Abfragen für Remotedatenbanken geöffnet werden.

Sie können die **PercentPosition**-Eigenschaft mit einer Bildlaufleiste auf einem Formular oder in einem Textfeld verwenden, um die Position des aktuellen Datensatzes in einem **Recordset**-Objekt anzugeben.

## <a name="example"></a>Beispiel

In diesem Beispiel wird die **PercentPosition**-Eigenschaft verwendet, um die Position des aktuellen Datensatzzeigers relativ zum Anfang des **Recordset**-Objekts anzugeben.

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
