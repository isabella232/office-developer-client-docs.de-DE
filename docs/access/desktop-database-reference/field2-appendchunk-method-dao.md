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
ms.openlocfilehash: e5aaab6a79893a66b12216f60c05690c1e806000
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937049"
---
# <a name="field2appendchunk-method-dao"></a><span data-ttu-id="c891b-102">Field2.AppendChunk-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="c891b-102">Field2.AppendChunk method (DAO)</span></span>

<span data-ttu-id="c891b-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c891b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c891b-104">Fügt Daten aus einem Zeichenfolgenausdruck an ein Field2-Objekt vom Typ Memo oder Long Binary in einem Recordset an.</span><span class="sxs-lookup"><span data-stu-id="c891b-104">Appends data from a string expression to a Memo or Long Binary **Field2** object in a **[Recordset](recordset-object-dao.md)**.</span></span>

## <a name="syntax"></a><span data-ttu-id="c891b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c891b-105">Syntax</span></span>

<span data-ttu-id="c891b-106">*Ausdruck* . AppendChunk (***Val***)</span><span class="sxs-lookup"><span data-stu-id="c891b-106">*expression* .AppendChunk(***Val***)</span></span>

<span data-ttu-id="c891b-107">*Ausdruck* Eine Variable, die ein **Field2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="c891b-107">*expression* A variable that represents a **Field2** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="c891b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c891b-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c891b-109">Name</span><span class="sxs-lookup"><span data-stu-id="c891b-109">Name</span></span></p></th>
<th><p><span data-ttu-id="c891b-110">Erforderlich/Optional</span><span class="sxs-lookup"><span data-stu-id="c891b-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="c891b-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="c891b-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="c891b-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c891b-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c891b-113">Val</span><span class="sxs-lookup"><span data-stu-id="c891b-113">Val</span></span></p></td>
<td><p><span data-ttu-id="c891b-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="c891b-114">Required</span></span></p></td>
<td><p><span data-ttu-id="c891b-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="c891b-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="c891b-116">Ein Ausdruck oder eine Variable vom Typ Variant (Untertyp String) mit den Daten, die an das <strong>Field2</strong>-Objekt angefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c891b-116">A Variant (String subtype) expression or variable containing the data you want to append to the <strong>Field2</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="c891b-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c891b-117">Remarks</span></span>

<span data-ttu-id="c891b-118">Sie können die Methoden AppendChunk und GetChunk verwenden, um auf Teilmengen der Daten in einem Memo- oder Long Binary-Feld zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="c891b-118">You can use the **AppendChunk** and **GetChunk** methods to access subsets of data in a Memo or Long Binary field.</span></span>

<span data-ttu-id="c891b-p101">Mithilfe dieser Methoden können Sie auch Zeichenfolgenspeicher freigeben, wenn Sie mit Memo- und Long Binary-Feldern arbeiten. Für bestimmte Vorgänge (z. B. Kopieren) sind temporäre Zeichenfolgen erforderlich. Bei begrenztem Zeichenfolgenspeicher müssen Sie evtl. Abschnitte eines Felds statt das ganze Feld verwenden.</span><span class="sxs-lookup"><span data-stu-id="c891b-p101">You can also use these methods to conserve string space when you work with Memo and Long Binary fields. Certain operations (copying, for example) involve temporary strings. If string space is limited, you may need to work with chunks of a field instead of the entire field.</span></span>

<span data-ttu-id="c891b-122">Wenn Sie **AppendChunk** verwenden, ohne dass ein aktueller Datensatz vorhanden ist, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="c891b-122">If there is no current record when you use **AppendChunk**, an error occurs.</span></span>

> [!NOTE]
> <span data-ttu-id="c891b-p102">Durch den ersten **AppendChunk**-Vorgang (nach einem **[Edit](recordset-edit-method-dao.md)** - oder **[AddNew](recordset-addnew-method-dao.md)** -Aufruf) werden die Daten einfach in das Feld geschrieben, und vorhandene Daten werden überschrieben. Nachfolgende **AppendChunk**-Aufrufe innerhalb derselben **Edit**- oder **AddNew**-Sitzung werden anschließend zu den vorhandenen Daten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c891b-p102">The initial **AppendChunk** operation (after an **[Edit](recordset-edit-method-dao.md)** or **[AddNew](recordset-addnew-method-dao.md)** call) will simply place the data in the field, overwriting any existing data. Subsequent **AppendChunk** calls within the same **Edit** or **AddNew** session will then add to the existing data.</span></span>

## <a name="example"></a><span data-ttu-id="c891b-125">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c891b-125">Example</span></span>

<span data-ttu-id="c891b-p103">In diesem Beispiel werden die Methoden **AppendChunk** und **GetChunk** verwendet, um ein OLE-Objektfeld mit Daten aus einem anderen Datensatz zu füllen (immer jeweils 32 KB). In einer echten Anwendung kann es sinnvoll sein, mit einer Prozedur wie dieser einen Mitarbeiterdatensatz (inklusive Foto des Mitarbeiters) von einer Tabelle in eine andere zu kopieren. In diesem Beispiel wird der Datensatz einfach wieder in dieselbe Tabelle kopiert. Beachten Sie, dass die gesamte Bearbeitung des Abschnitts innerhalb einer einzelnen AddNew-Aktualisierungssequenz erfolgt.</span><span class="sxs-lookup"><span data-stu-id="c891b-p103">This example uses the **AppendChunk** and **GetChunk** methods to fill an OLE object field with data from another record, 32K at a time. In a real application, one might use a procedure like this to copy an employee record (including the employee's photo) from one table to another. In this example, the record is simply being copied back to same table. Note that all the chunk manipulation takes place within a single AddNew-Update sequence.</span></span>

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
