---
title: Recordset.PercentPosition-Eigenschaft (DAO)
TOCTitle: PercentPosition Property
ms:assetid: aebbda44-ed72-7a6c-0cd5-28c8997d4d96
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821751(v=office.15)
ms:contentKeyID: 48547077
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 31f1cbf1f6bbc2f2c7ce855cccb667e71638b1b8
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929570"
---
# <a name="recordsetpercentposition-property-dao"></a>Recordset.PercentPosition-Eigenschaft (DAO)


**Betrifft**: Access 2013, Office 2013

Legt einen Wert fest, der die ungefähre Position des aktuellen Datensatzes (aktueller Datensatz) im **[Recordset](recordset-object-dao.md)** -Objekt basierend auf einem Prozentwert der Datensätze im **Recordset** angibt, oder gibt diesen Wert zurück.

## <a name="syntax"></a>Syntax

*Ausdruck* . PercentPosition

*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Zum Festlegen oder Ändern der ungefähren Position des aktuellen Datensatz in einem Recordset-Objekt können Sie die PercentPosition-Eigenschaft überprüfen oder festlegen. Wenn Sie ein Recordset-Objekt vom Typ Dynaset oder Snapshot verwenden, das direkt in einer Basistabelle geöffnet wurde, füllen Sie zunächst das Recordset-Objekt auf, indem Sie zum letzten Datensatz gehen. Anschließend legen Sie die PercentPosition-Eigenschaft fest oder überprüfen sie. Wenn Sie die PercentPosition-Eigenschaft verwenden, bevor Sie das Recordset-Objekt vollständig aufgefüllt haben, erfolgt die Bewegung relativ zur Anzahl der Datensätze, auf die laut des Werts der RecordCount-Eigenschaft zugegriffen wurde. Mithilfe der MoveLast-Methode können Sie zum letzten Datensatz wechseln.


> [!NOTE]
> <P>[!HINWEIS] Es wird nicht empfohlen, die <STRONG>PercentPosition</STRONG>-Eigenschaft zu verwenden, um zu einem bestimmten Datensatz in einem <STRONG>Recordset</STRONG>-Objekt zu wechseln. Die <STRONG><A href="recordset-bookmark-property-dao.md">Bookmark</A></STRONG> -Eigenschaft ist besser für diese Aufgabe geeignet.</P>



Wenn Sie einen Wert für die **PercentPosition**-Eigenschaft festgelegt haben, wird der Datensatz an der ungefähren Position, die dem betreffenden Wert entspricht, zum aktuellen Datensatz. Die **PercentPosition**-Eigenschaft wird auf einen Wert zurückgesetzt, der die ungefähre Position des aktuellen Datensatzes widerspiegelt. Beispiel: Wenn das **Recordset**-Objekt nur 5 Datensätze enthält und Sie seine **PercentPosition**-Eigenschaft auf den Wert 77 festlegen, kann der von der **PercentPosition**-Eigenschaft zurückgegebene Wert 80 sein, anstelle von 77.

Die **PercentPosition** -Eigenschaft gilt für alle Typen von **Recordset** -Objekten, ausgenommen Forward Typ **Recordset** -Objekte oder **Recordset** -Objekten, die von Pass-Through-Abfragen an Remotedatenbanken geöffnet.

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
