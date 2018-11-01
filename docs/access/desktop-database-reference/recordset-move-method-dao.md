---
title: Recordset.Move-Methode (DAO)
TOCTitle: Move Method
ms:assetid: 21ca5ab5-ff71-1ae8-21b3-8991d5f795cf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191697(v=office.15)
ms:contentKeyID: 48543689
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052941
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 2caa468f189e30373e2818b090688ca6f239258d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870590"
---
# <a name="recordsetmove-method-dao"></a><span data-ttu-id="b750c-102">Recordset.Move-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="b750c-102">Recordset.Move Method (DAO)</span></span>


<span data-ttu-id="b750c-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b750c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b750c-104">Verschiebt die Position des aktuellen Datensatzes in ein **[Recordset](recordset-object-dao.md)** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="b750c-104">Moves the position of the current record in a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b750c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b750c-105">Syntax</span></span>

<span data-ttu-id="b750c-106">*Ausdruck* . Move (***Zeilen***, ***Anfangslesezeichen***)</span><span class="sxs-lookup"><span data-stu-id="b750c-106">*expression* .Move(***Rows***, ***StartBookmark***)</span></span>

<span data-ttu-id="b750c-107">*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="b750c-107">*expression* A variable that represents a **Recordset** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="b750c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b750c-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b750c-109">Name</span><span class="sxs-lookup"><span data-stu-id="b750c-109">Name</span></span></p></th>
<th><p><span data-ttu-id="b750c-110">Erforderlich/Optional</span><span class="sxs-lookup"><span data-stu-id="b750c-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="b750c-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="b750c-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="b750c-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b750c-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b750c-113">Zeilen</span><span class="sxs-lookup"><span data-stu-id="b750c-113">Rows</span></span></p></td>
<td><p><span data-ttu-id="b750c-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="b750c-114">Required</span></span></p></td>
<td><p><span data-ttu-id="b750c-115"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="b750c-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="b750c-p101">Die Anzahl von Zeilen, um die sich die Position verschiebt. Ist rows größer als 0, wird die Position nach vorne verschoben (Richtung Dateiende). Ist rows kleiner als 0, wird die Position nach hinten verschoben (Richtung Dateianfang).</span><span class="sxs-lookup"><span data-stu-id="b750c-p101">The number of rows the position will move. If rows is greater than 0, the position is moved forward (toward the end of the file). If rows is less than 0, the position is moved backward (toward the beginning of the file).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b750c-119">Anfangslesezeichen</span><span class="sxs-lookup"><span data-stu-id="b750c-119">StartBookmark</span></span></p></td>
<td><p><span data-ttu-id="b750c-120">Optional</span><span class="sxs-lookup"><span data-stu-id="b750c-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="b750c-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="b750c-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="b750c-p102">Ein Wert, der ein Lesezeichen identifiziert. Bei Angabe von startbookmark beginnt die Verschiebung relativ zu diesem Lesezeichen. Andernfalls beginnt Move mit dem aktuellen Datensatz.</span><span class="sxs-lookup"><span data-stu-id="b750c-p102">A value identifying a bookmark. If you specify startbookmark, the move begins relative to this bookmark. Otherwise, Move begins from the current record.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b750c-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b750c-125">Remarks</span></span>

<span data-ttu-id="b750c-p103">Wenn Sie mithilfe von **Move** den aktuellen Datensatzzeiger vor dem ersten Datensatz positionieren, wird der aktuelle Datensatzzeiger an den Dateianfang verschoben. Falls das **Recordset** keine Datensätze enthält und seine **[BOF](recordset-bof-property-dao.md)** -Eigenschaft auf **True** festgelegt ist, wird ein Fehler zurückgegeben, wenn Sie sich mit dieser Methode rückwärts bewegen.</span><span class="sxs-lookup"><span data-stu-id="b750c-p103">If you use **Move** to position the current record pointer before the first record, the current record pointer moves to the beginning of the file. If the **Recordset** contains no records and its **[BOF](recordset-bof-property-dao.md)** property is **True**, using this method to move backward causes an error.</span></span>

<span data-ttu-id="b750c-p104">Wenn Sie mithilfe von **Move** den aktuellen Datensatzzeiger hinter dem letzten Datensatz positionieren, wird der aktuelle Datensatzzeiger an das Dateiende verschoben. Falls das **Recordset** keine Datensätze enthält und seine **[EOF](recordset-eof-property-dao.md)** -Eigenschaft auf **True** festgelegt ist, wird ein Fehler zurückgegeben, wenn Sie sich mit dieser Methode vorwärts bewegen.</span><span class="sxs-lookup"><span data-stu-id="b750c-p104">If you use **Move** to position the current record pointer after the last record, the current record pointer position moves to the end of the file. If the **Recordset** contains no records and its **[EOF](recordset-eof-property-dao.md)** property is **True**, then using this method to move forward causes an error.</span></span>

<span data-ttu-id="b750c-130">Wenn für die **BOF**- oder die **EOF**-Eigenschaft der Wert **True** festgelegt ist und Sie versuchen, die **Move**-Methode ohne ein zulässiges Lesezeichen zu verwenden, tritt ein Laufzeitfehler auf.</span><span class="sxs-lookup"><span data-stu-id="b750c-130">If either the **BOF** or **EOF** property is **True** and you attempt to use the **Move** method without a valid bookmark, a run-time error occurs.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="b750c-p105">Wenn Sie <STRONG>Move</STRONG> auf ein <STRONG>Recordset</STRONG>-Objekt vom Typ Vorwärts anwenden, muss das Zeilenargument eine positive Ganzzahl sein, und Lesezeichen sind nicht zulässig. Sie können sich also nur vorwärts bewegen.</span><span class="sxs-lookup"><span data-stu-id="b750c-p105">When you use <STRONG>Move</STRONG> on a forward-only-type <STRONG>Recordset</STRONG> object, the rows argument must be a positive integer and bookmarks aren't allowed. This means you can only move forward.</span></span></P>
> <LI>
> <P><span data-ttu-id="b750c-133">Verwenden Sie eine der Methoden <STRONG>MoveFirst</STRONG>, <STRONG>MoveLast</STRONG>, <STRONG>MoveNext</STRONG> oder <STRONG>MovePrevious</STRONG>, um den ersten, letzten, nächsten oder vorherigen Datensatz in einem <STRONG>Recordset</STRONG> zum aktuellen Datensatz zu machen.</span><span class="sxs-lookup"><span data-stu-id="b750c-133">To make the first, last, next, or previous record in a <STRONG>Recordset</STRONG> the current record, use either the <STRONG>MoveFirst</STRONG>, <STRONG>MoveLast</STRONG>, <STRONG>MoveNext</STRONG>, or <STRONG>MovePrevious</STRONG> method.</span></span></P>
> <LI>
> <P><span data-ttu-id="b750c-p106">Das Verwenden von <STRONG>Move</STRONG> mit einer Zeilenanzahl gleich 0 ist eine einfache Möglichkeit, die zugrunde liegenden Daten für den aktuellen Datensatz abzurufen. Das ist hilfreich, wenn Sie sicherstellen möchten, dass der aktuelle Datensatz die aktuellsten Daten aus den Basistabellen enthält. Außerdem werden alle anstehenden <STRONG><A href="recordset2-edit-method-dao.md">Edit</A></STRONG> - oder <STRONG><A href="recordset-addnew-method-dao.md">AddNew</A></STRONG> -Aufrufe abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="b750c-p106">Using <STRONG>Move</STRONG> with rows equal to 0 is an easy way to retrieve the underlying data for the current record. This is useful if you want to make sure that the current record has the most recent data from the base tables. It will also cancel any pending <STRONG><A href="recordset2-edit-method-dao.md">Edit</A></STRONG> or <STRONG><A href="recordset-addnew-method-dao.md">AddNew</A></STRONG> calls.</span></span></P></LI></UL>



## <a name="example"></a><span data-ttu-id="b750c-137">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b750c-137">Example</span></span>

<span data-ttu-id="b750c-138">In diesem Beispiel wird die **Move**-Methode verwendet, um den Zeiger für den Datensatz auf der Grundlage der Benutzereingabe zu positionieren.</span><span class="sxs-lookup"><span data-stu-id="b750c-138">This example uses the **Move** method to position the record pointer based on user input.</span></span>

```vb
    Sub MoveX() 
     
       Dim dbsNorthwind As Database 
       Dim rstSuppliers As Recordset 
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
