---
title: Field.FieldSize Property (DAO)
TOCTitle: FieldSize Property
ms:assetid: c81bd5cb-6b7c-5390-2d6b-049143f2f3b6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823165(v=office.15)
ms:contentKeyID: 48547645
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3f757752e32ec45fa2b7d2c82f133078d70b64a5
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877597"
---
# <a name="fieldfieldsize-property-dao"></a><span data-ttu-id="1148c-102">Field.FieldSize Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="1148c-102">Field.FieldSize Property (DAO)</span></span>


<span data-ttu-id="1148c-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1148c-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="1148c-104">Gibt die in der Datenbank (nicht im Arbeitsspeicher) verwendete Anzahl von Bytes eines Field-Objekts vom Typ Memo oder Long Binary in der Fields-Auflistung eines Recordset-Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="1148c-104">Returns the number of bytes used in the database (rather than in memory) of a Memo or Long Binary **[Field](field-object-dao.md)** object in the **[Fields](fields-collection-dao.md)** collection of a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="1148c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1148c-105">Syntax</span></span>

<span data-ttu-id="1148c-106">*Ausdruck* . Feldgröße</span><span class="sxs-lookup"><span data-stu-id="1148c-106">*expression* .FieldSize</span></span>

<span data-ttu-id="1148c-107">*Ausdruck* Eine Variable, die ein **Field** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="1148c-107">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1148c-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1148c-108">Remarks</span></span>

<span data-ttu-id="1148c-109">Sie können die **FieldSize**-Eigenschaft mit den Methoden **[AppendChunk](field-appendchunk-method-dao.md)** und **[GetChunk](field-getchunk-method-dao.md)** zum Bearbeiten großer Felder verwenden.</span><span class="sxs-lookup"><span data-stu-id="1148c-109">You can use **FieldSize** with the **[AppendChunk](field-appendchunk-method-dao.md)** and **[GetChunk](field-getchunk-method-dao.md)** methods to manipulate large fields.</span></span>

<span data-ttu-id="1148c-110">Da die Größe eines Felds vom Datentyp Long Binary oder Memo 64 KB überschreiten kann, sollten Sie den von der FieldSize-Eigenschaft zurückgegebenen Wert einer Variablen zuordnen, deren Größe zum Speichern einer Long-Variablen ausreicht.</span><span class="sxs-lookup"><span data-stu-id="1148c-110">Because the size of a Long Binary or Memo field can exceed 64K, you should assign the value returned by **FieldSize** to a variable large enough to store a **Long** variable.</span></span>

<span data-ttu-id="1148c-111">Wenn Sie die Größe eines Field-Objekts eines anderen Typs als Memo and Long Binary ermitteln möchten, verwenden Sie die Size-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="1148c-111">To determine the size of a **Field** object other than Memo and Long Binary types, use the **[Size](field-size-property-dao.md)** property.</span></span>

  - <span data-ttu-id="1148c-112">Der Datenbankserver oder ODBC-Treiber unterstützt keine serverseitigen Cursor.</span><span class="sxs-lookup"><span data-stu-id="1148c-112">If the database server or ODBC driver does not support server-side cursors.</span></span>

  - <span data-ttu-id="1148c-113">Sie verwenden die ODBC-Cursorbibliothek (d. h. die **DefaultCursorDriver**-Eigenschaft ist auf **dbUseODBC** festgelegt oder auf **dbUseDefault**, wenn der Server keine serverseitigen Cursor unterstützt).</span><span class="sxs-lookup"><span data-stu-id="1148c-113">If you are using the ODBC cursor library (that is, the **DefaultCursorDriver** property is set to **dbUseODBC**, or to **dbUseDefault** when the server does not support server-side cursors).</span></span>

  - <span data-ttu-id="1148c-114">Sie verwenden eine Abfrage ohne Cursor (d. h. die **DefaultCursorDriver**-Eigenschaft ist auf **dbUseNoCursor** festgelegt).</span><span class="sxs-lookup"><span data-stu-id="1148c-114">If you are using a cursorless query (that is, the **DefaultCursorDriver** property is set to **dbUseNoCursor**).</span></span>

<span data-ttu-id="1148c-p101">Die **FieldSize**-Eigenschaft und die VBA-Funktionen **Len()** oder **LenB()** geben möglicherweise unterschiedliche Werte als Länge derselben Zeichenfolge zurück. Zeichenfolgen werden in einer Microsoft Access-Datenbank in einem MBCS-Format (Multi-Byte Character Set, Mehrbyte-Zeichensatz) gespeichert, jedoch in VBA im Unicode-Format angezeigt. Folglich gibt die **Len()**-Funktion immer die Anzahl von Zeichen, die **LenB**-Funktion immer die Anzahl von Zeichen mal 2 (Unicode verwendet 2 Bytes pro Zeichen) und die **FieldSize**-Eigenschaft einen Wert dazwischen zurück, wenn die Zeichenfolge MBCS-Zeichen enthält. Angenommen, eine Zeichenfolge besteht aus 3 normalen Zeichen und 2 MBCS-Zeichen, dann gibt **Len()** 5 zurück, **LenB()** 10 und **FieldSize** 7, d. h. die Summe von 1 für jedes normale Zeichen und 2 für jedes MBCS-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="1148c-p101">The **FieldSize** property and the VBA **Len()** or **LenB()** functions may return different values as the length of the same string. Strings are stored in a Microsoft Access database in multi-byte character set (MBCS) form, but exposed through VBA in Unicode format. As a result, the **Len()** function will always return the number of characters, **LenB** will always return the number of characters X 2 (Unicode uses two bytes for each character), but **FieldSize** will return some value in between if the string has any MBCS characters. For example, given a string consisting of three normal characters and two MBCS characters, **Len()** will return 5, **LenB()** will return 10, and **FieldSize** will return 7, the sum of 1 for each normal character and 2 for each MBCS character.</span></span>

## <a name="example"></a><span data-ttu-id="1148c-119">Beispiel</span><span class="sxs-lookup"><span data-stu-id="1148c-119">Example</span></span>

<span data-ttu-id="1148c-120">Dieses Beispiel veranschaulicht, wie Sie mit der FieldSize-Eigenschaft die Anzahl von Bytes auflisten, die in Field-Objekten vom Typ Memo und Long Binary in zwei verschiedenen Tabellen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1148c-120">This example uses the **FieldSize** property to list the number of bytes used by the Memo and Long Binary Field objects in two different tables.</span></span>

```vb
    Sub FieldSizeX() 
     
     Dim dbsNorthwind As Database 
     Dim rstCategories As Recordset 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstCategories = _ 
     dbsNorthwind.OpenRecordset("Categories", _ 
     dbOpenDynaset) 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     Debug.Print _ 
     "Field sizes from records in Categories table" 
     
     With rstCategories 
     Debug.Print " CategoryName - " & _ 
     "Description (bytes) - Picture (bytes)" 
     
     ' Enumerate the Categories Recordset and print the size 
     ' in bytes of the picture field for each record. 
     Do While Not .EOF 
     Debug.Print " " & !CategoryName & " - " & _ 
     !Description.FieldSize & " - " & _ 
     !Picture.FieldSize 
     .MoveNext 
     Loop 
     
     .Close 
     End With 
     
     Debug.Print "Field sizes from records in Employees table" 
     
     With rstEmployees 
     Debug.Print " LastName - Notes (bytes) - " & _ 
     "Photo (bytes)" 
     
     ' Enumerate the Employees Recordset and print the size 
     ' in bytes of the picture field for each record. 
     Do While Not .EOF 
     Debug.Print " " & !LastName & " - " & _ 
     !Notes.FieldSize & " - " & !Photo.FieldSize 
     .MoveNext 
     Loop 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="1148c-p102">In diesem Beispiel werden die Methoden **AppendChunk** und **GetChunk** verwendet, um ein OLE-Objektfeld mit Daten aus einem anderen Datensatz zu füllen (immer jeweils 32 KB). In einer echten Anwendung kann es sinnvoll sein, mit einer Prozedur wie dieser einen Mitarbeiterdatensatz (inklusive Foto des Mitarbeiters) von einer Tabelle in eine andere zu kopieren. In diesem Beispiel wird der Datensatz einfach wieder in dieselbe Tabelle kopiert. Beachten Sie, dass die gesamte Bearbeitung des Abschnitts innerhalb einer einzelnen AddNew-Aktualisierungssequenz erfolgt.</span><span class="sxs-lookup"><span data-stu-id="1148c-p102">This example uses the **AppendChunk** and **GetChunk** methods to fill an OLE object field with data from another record, 32K at a time. In a real application, one might use a procedure like this to copy an employee record (including the employee's photo) from one table to another. In this example, the record is simply being copied back to same table. Note that all the chunk manipulation takes place within a single AddNew-Update sequence.</span></span>

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
     
    Function CopyLargeField(fldSource As Field, _ 
     fldDestination As Field) 
     
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
