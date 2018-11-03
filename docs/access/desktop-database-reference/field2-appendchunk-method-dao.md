---
title: Field2.AppendChunk-Methode (DAO)
TOCTitle: AppendChunk Method
ms:assetid: 540cd02d-1fc6-81d1-ac08-1e3df72a7208
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194088(v=office.15)
ms:contentKeyID: 48544886
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052867
f1_categories:
- Office.Version=v15
ms.openlocfilehash: f999a0519fccb8f896ed07963db621065530c1a3
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929769"
---
# <a name="field2appendchunk-method-dao"></a><span data-ttu-id="62bee-102">Field2.AppendChunk-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="62bee-102">Field2.AppendChunk method (DAO)</span></span>


<span data-ttu-id="62bee-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="62bee-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="62bee-104">Fügt Daten aus einem Zeichenfolgenausdruck an ein Field2-Objekt vom Typ Memo oder Long Binary in einem Recordset an.</span><span class="sxs-lookup"><span data-stu-id="62bee-104">Appends data from a string expression to a Memo or Long Binary **Field2** object in a **[Recordset](recordset-object-dao.md)**.</span></span>

## <a name="syntax"></a><span data-ttu-id="62bee-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="62bee-105">Syntax</span></span>

<span data-ttu-id="62bee-106">*Ausdruck* . AppendChunk (***Val***)</span><span class="sxs-lookup"><span data-stu-id="62bee-106">*expression* .AppendChunk(***Val***)</span></span>

<span data-ttu-id="62bee-107">*Ausdruck* Eine Variable, die ein **Field2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="62bee-107">*expression* A variable that represents a **Field2** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="62bee-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="62bee-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="62bee-109">Name</span><span class="sxs-lookup"><span data-stu-id="62bee-109">Name</span></span></p></th>
<th><p><span data-ttu-id="62bee-110">Erforderlich/Optional</span><span class="sxs-lookup"><span data-stu-id="62bee-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="62bee-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="62bee-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="62bee-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="62bee-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="62bee-113">Val</span><span class="sxs-lookup"><span data-stu-id="62bee-113">Val</span></span></p></td>
<td><p><span data-ttu-id="62bee-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="62bee-114">Required</span></span></p></td>
<td><p><span data-ttu-id="62bee-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="62bee-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="62bee-116">Ein Ausdruck oder eine Variable vom Typ Variant (Untertyp String) mit den Daten, die an das <strong>Field2</strong>-Objekt angefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="62bee-116">A Variant (String subtype) expression or variable containing the data you want to append to the <strong>Field2</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="62bee-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="62bee-117">Remarks</span></span>

<span data-ttu-id="62bee-118">Sie können die Methoden AppendChunk und GetChunk verwenden, um auf Teilmengen der Daten in einem Memo- oder Long Binary-Feld zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="62bee-118">You can use the **AppendChunk** and **GetChunk** methods to access subsets of data in a Memo or Long Binary field.</span></span>

<span data-ttu-id="62bee-p101">Mithilfe dieser Methoden können Sie auch Zeichenfolgenspeicher freigeben, wenn Sie mit Memo- und Long Binary-Feldern arbeiten. Für bestimmte Vorgänge (z. B. Kopieren) sind temporäre Zeichenfolgen erforderlich. Bei begrenztem Zeichenfolgenspeicher müssen Sie evtl. Abschnitte eines Felds statt das ganze Feld verwenden.</span><span class="sxs-lookup"><span data-stu-id="62bee-p101">You can also use these methods to conserve string space when you work with Memo and Long Binary fields. Certain operations (copying, for example) involve temporary strings. If string space is limited, you may need to work with chunks of a field instead of the entire field.</span></span>

<span data-ttu-id="62bee-122">Wenn Sie **AppendChunk** verwenden, ohne dass ein aktueller Datensatz vorhanden ist, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="62bee-122">If there is no current record when you use **AppendChunk**, an error occurs.</span></span>


> [!NOTE]
> <P><span data-ttu-id="62bee-p102">Durch den ersten <STRONG>AppendChunk</STRONG>-Vorgang (nach einem <STRONG><A href="recordset-edit-method-dao.md">Edit</A></STRONG> - oder <STRONG><A href="recordset-addnew-method-dao.md">AddNew</A></STRONG> -Aufruf) werden die Daten einfach in das Feld geschrieben, und vorhandene Daten werden überschrieben. Nachfolgende <STRONG>AppendChunk</STRONG>-Aufrufe innerhalb derselben <STRONG>Edit</STRONG>- oder <STRONG>AddNew</STRONG>-Sitzung werden anschließend zu den vorhandenen Daten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="62bee-p102">The initial <STRONG>AppendChunk</STRONG> operation (after an <STRONG><A href="recordset-edit-method-dao.md">Edit</A></STRONG> or <STRONG><A href="recordset-addnew-method-dao.md">AddNew</A></STRONG> call) will simply place the data in the field, overwriting any existing data. Subsequent <STRONG>AppendChunk</STRONG> calls within the same <STRONG>Edit</STRONG> or <STRONG>AddNew</STRONG> session will then add to the existing data.</span></span></P>



## <a name="example"></a><span data-ttu-id="62bee-125">Beispiel</span><span class="sxs-lookup"><span data-stu-id="62bee-125">Example</span></span>

<span data-ttu-id="62bee-p103">In diesem Beispiel werden die Methoden **AppendChunk** und **GetChunk** verwendet, um ein OLE-Objektfeld mit Daten aus einem anderen Datensatz zu füllen (immer jeweils 32 KB). In einer echten Anwendung kann es sinnvoll sein, mit einer Prozedur wie dieser einen Mitarbeiterdatensatz (inklusive Foto des Mitarbeiters) von einer Tabelle in eine andere zu kopieren. In diesem Beispiel wird der Datensatz einfach wieder in dieselbe Tabelle kopiert. Beachten Sie, dass die gesamte Bearbeitung des Abschnitts innerhalb einer einzelnen AddNew-Aktualisierungssequenz erfolgt.</span><span class="sxs-lookup"><span data-stu-id="62bee-p103">This example uses the **AppendChunk** and **GetChunk** methods to fill an OLE object field with data from another record, 32K at a time. In a real application, one might use a procedure like this to copy an employee record (including the employee's photo) from one table to another. In this example, the record is simply being copied back to same table. Note that all the chunk manipulation takes place within a single AddNew-Update sequence.</span></span>

```vb
    Sub AppendChunkX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset 
       Dim rstEmployees2 As Recordset 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       ' Open two recordsets from the Employees table. 
       Set rstEmployees = _ 
          dbsNorthwind.OpenRecordset("Employees", _ 
          dbOpenDynaset) 
       Set rstEmployees2 = rstEmployees.Clone 
     
       ' Add a new record to the first Recordset and copy the  
       ' data from a record in the second Recordset. 
       With rstEmployees 
          .AddNew 
          !FirstName = rstEmployees2!FirstName 
          !LastName = rstEmployees2!LastName 
          CopyLargeField rstEmployees2!Photo, !Photo 
          .Update 
     
          ' Delete new record because this is a demonstration. 
          .Bookmark = .LastModified 
          .Delete 
          .Close 
       End With 
     
       rstEmployees2.Close 
       dbsNorthwind.Close 
     
    End Sub 
     
    Function CopyLargeField(fldSource As Field2, _ 
       fldDestination As Field2) 
     
       ' Set size of chunk in bytes. 
       Const conChunkSize = 32768 
     
       Dim lngOffset As Long 
       Dim lngTotalSize As Long 
       Dim strChunk As String 
     
       ' Copy the photo from one Recordset to the other in 32K  
       ' chunks until the entire field is copied. 
       lngTotalSize = fldSource.FieldSize 
       Do While lngOffset < lngTotalSize 
          strChunk = fldSource.GetChunk(lngOffset, conChunkSize) 
          fldDestination.AppendChunk strChunk 
          lngOffset = lngOffset + conChunkSize 
       Loop 
     
    End Function
```
