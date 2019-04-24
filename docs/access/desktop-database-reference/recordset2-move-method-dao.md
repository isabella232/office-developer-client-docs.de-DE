---
title: Recordset2. Move-Methode (DAO)
TOCTitle: Move Method
ms:assetid: df39c05e-c5f8-3b66-fa5f-c91b687c147d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835635(v=office.15)
ms:contentKeyID: 48548211
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d57e73c52ca515f13d613ed3aeb9cf361054396e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307266"
---
# <a name="recordset2move-method-dao"></a><span data-ttu-id="3bbfe-102">Recordset2. Move-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="3bbfe-102">Recordset2.Move method (DAO)</span></span>

<span data-ttu-id="3bbfe-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3bbfe-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3bbfe-104">Verschiebt die Position des aktuellen Datensatzes in ein **[Recordset](recordset-object-dao.md)** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="3bbfe-104">Moves the position of the current record in a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bbfe-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3bbfe-105">Syntax</span></span>

<span data-ttu-id="3bbfe-106">*Ausdruck* . Move (***Rows***, ***Start Bookmark***)</span><span class="sxs-lookup"><span data-stu-id="3bbfe-106">*expression* .Move(***Rows***, ***StartBookmark***)</span></span>

<span data-ttu-id="3bbfe-107">*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="3bbfe-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="3bbfe-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3bbfe-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3bbfe-109">Name</span><span class="sxs-lookup"><span data-stu-id="3bbfe-109">Name</span></span></p></th>
<th><p><span data-ttu-id="3bbfe-110">Erforderlich/optional</span><span class="sxs-lookup"><span data-stu-id="3bbfe-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="3bbfe-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="3bbfe-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="3bbfe-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3bbfe-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3bbfe-113"><em>Rows</em></span><span class="sxs-lookup"><span data-stu-id="3bbfe-113"><em>Rows</em></span></span></p></td>
<td><p><span data-ttu-id="3bbfe-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="3bbfe-114">Required</span></span></p></td>
<td><p><span data-ttu-id="3bbfe-115"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="3bbfe-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="3bbfe-p101">Die Anzahl von Zeilen, um die sich die Position verschiebt. Ist rows größer als 0, wird die Position nach vorne verschoben (Richtung Dateiende). Ist rows kleiner als 0, wird die Position nach hinten verschoben (Richtung Dateianfang).</span><span class="sxs-lookup"><span data-stu-id="3bbfe-p101">The number of rows the position will move. If rows is greater than 0, the position is moved forward (toward the end of the file). If rows is less than 0, the position is moved backward (toward the beginning of the file).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3bbfe-119"><em>Start Bookmark</em></span><span class="sxs-lookup"><span data-stu-id="3bbfe-119"><em>StartBookmark</em></span></span></p></td>
<td><p><span data-ttu-id="3bbfe-120">Optional</span><span class="sxs-lookup"><span data-stu-id="3bbfe-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="3bbfe-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="3bbfe-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="3bbfe-p102">Ein Wert, der ein Lesezeichen identifiziert. Bei Angabe von startbookmark beginnt die Verschiebung relativ zu diesem Lesezeichen. Andernfalls beginnt Move mit dem aktuellen Datensatz.</span><span class="sxs-lookup"><span data-stu-id="3bbfe-p102">A value identifying a bookmark. If you specify startbookmark, the move begins relative to this bookmark. Otherwise, Move begins from the current record.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="3bbfe-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3bbfe-125">Remarks</span></span>

<span data-ttu-id="3bbfe-p103">Wenn Sie mithilfe von **Move** den aktuellen Datensatzzeiger vor dem ersten Datensatz positionieren, wird der aktuelle Datensatzzeiger an den Dateianfang verschoben. Falls das **Recordset** keine Datensätze enthält und seine **[BOF](recordset2-bof-property-dao.md)** -Eigenschaft auf **True** festgelegt ist, wird ein Fehler zurückgegeben, wenn Sie sich mit dieser Methode rückwärts bewegen.</span><span class="sxs-lookup"><span data-stu-id="3bbfe-p103">If you use **Move** to position the current record pointer before the first record, the current record pointer moves to the beginning of the file. If the **Recordset** contains no records and its **[BOF](recordset2-bof-property-dao.md)** property is **True**, using this method to move backward causes an error.</span></span>

<span data-ttu-id="3bbfe-p104">Wenn Sie mithilfe von **Move** den aktuellen Datensatzzeiger hinter dem letzten Datensatz positionieren, wird der aktuelle Datensatzzeiger an das Dateiende verschoben. Falls das **Recordset** keine Datensätze enthält und seine **[EOF](recordset2-eof-property-dao.md)** -Eigenschaft auf **True** festgelegt ist, wird ein Fehler zurückgegeben, wenn Sie sich mit dieser Methode vorwärts bewegen.</span><span class="sxs-lookup"><span data-stu-id="3bbfe-p104">If you use **Move** to position the current record pointer after the last record, the current record pointer position moves to the end of the file. If the **Recordset** contains no records and its **[EOF](recordset2-eof-property-dao.md)** property is **True**, then using this method to move forward causes an error.</span></span>

<span data-ttu-id="3bbfe-130">Wenn für die **BOF**- oder die **EOF**-Eigenschaft der Wert **True** festgelegt ist und Sie versuchen, die **Move**-Methode ohne ein zulässiges Lesezeichen zu verwenden, tritt ein Laufzeitfehler auf.</span><span class="sxs-lookup"><span data-stu-id="3bbfe-130">If either the **BOF** or **EOF** property is **True** and you attempt to use the **Move** method without a valid bookmark, a run-time error occurs.</span></span>

> [!NOTE]
> - <span data-ttu-id="3bbfe-p105">When you use **Move** on a forward-only-type **Recordset** object, the rows argument must be a positive integer and bookmarks aren't allowed. This means you can only move forward.</span><span class="sxs-lookup"><span data-stu-id="3bbfe-p105">When you use **Move** on a forward-only-type **Recordset** object, the rows argument must be a positive integer and bookmarks aren't allowed. This means you can only move forward.</span></span>
> - <span data-ttu-id="3bbfe-133">Verwenden Sie eine der Methoden **MoveFirst**, **MoveLast**, **MoveNext** oder **MovePrevious**, um den ersten, letzten, nächsten oder vorherigen Datensatz in einem **Recordset** zum aktuellen Datensatz zu machen.</span><span class="sxs-lookup"><span data-stu-id="3bbfe-133">To make the first, last, next, or previous record in a **Recordset** the current record, use either the **MoveFirst**, **MoveLast**, **MoveNext**, or **MovePrevious** method.</span></span>
> - <span data-ttu-id="3bbfe-p106">Das Verwenden von **Move** mit einer Zeilenanzahl gleich 0 ist eine einfache Möglichkeit, die zugrunde liegenden Daten für den aktuellen Datensatz abzurufen. Das ist hilfreich, wenn Sie sicherstellen möchten, dass der aktuelle Datensatz die aktuellsten Daten aus den Basistabellen enthält. Außerdem werden alle anstehenden **[Edit](recordset2-edit-method-dao.md)** - oder **[AddNew](recordset-addnew-method-dao.md)** -Aufrufe abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="3bbfe-p106">Using **Move** with rows equal to 0 is an easy way to retrieve the underlying data for the current record. This is useful if you want to make sure that the current record has the most recent data from the base tables. It will also cancel any pending **[Edit](recordset2-edit-method-dao.md)** or **[AddNew](recordset-addnew-method-dao.md)** calls.</span></span>


## <a name="example"></a><span data-ttu-id="3bbfe-137">Beispiel</span><span class="sxs-lookup"><span data-stu-id="3bbfe-137">Example</span></span>

<span data-ttu-id="3bbfe-138">In diesem Beispiel wird die **Move**-Methode verwendet, um den Zeiger für den Datensatz auf der Grundlage der Benutzereingabe zu positionieren.</span><span class="sxs-lookup"><span data-stu-id="3bbfe-138">This example uses the **Move** method to position the record pointer based on user input.</span></span>

```vb
    Sub MoveX() 
     
       Dim dbsNorthwind As Database 
       Dim rstSuppliers As Recordset2 
       Dim varBookmark As Variant 
       Dim strCommand As String 
       Dim lngMove As Long 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set rstSuppliers = _ 
          dbsNorthwind.OpenRecordset("SELECT CompanyName, " & _ 
          "City, Country FROM Suppliers ORDER BY CompanyName", _ 
          dbOpenDynaset) 
     
       With rstSuppliers 
          ' Populate recordset. 
          .MoveLast 
          .MoveFirst 
     
          Do While True 
             ' Display information about current record and ask  
             ' how many records to move. 
             strCommand = InputBox( _ 
                "Record " & (.AbsolutePosition + 1) & " of " & _ 
                .RecordCount & vbCr & "Company: " & _ 
                !CompanyName & vbCr & "Location: " & !City & _ 
                ", " & !Country & vbCr & vbCr & _ 
                "Enter number of records to Move " & _ 
                "(positive or negative).") 
     
             If strCommand = "" Then Exit Do 
     
             ' Store bookmark in case the Move doesn't work. 
             varBookmark = .Bookmark 
     
             ' Move method requires parameter of data type Long. 
             lngMove = CLng(strCommand) 
             .Move lngMove 
     
             ' Trap for BOF or EOF. 
             If .BOF Then 
                MsgBox "Too far backward! " & _ 
                   "Returning to current record." 
                .Bookmark = varBookmark 
             End If 
             If .EOF Then 
                MsgBox "Too far forward! " & _ 
                   "Returning to current record." 
                .Bookmark = varBookmark 
             End If 
          Loop 
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub
```
