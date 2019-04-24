---
title: Field. Fieldes-Eigenschaft (DAO)
TOCTitle: FieldSize Property
ms:assetid: c81bd5cb-6b7c-5390-2d6b-049143f2f3b6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823165(v=office.15)
ms:contentKeyID: 48547645
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 68a1b354b27515dd855703b9bf6344e4a9e90d7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293112"
---
# <a name="fieldfieldsize-property-dao"></a>Field. Fieldes-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013


Returns the number of bytes used in the database (rather than in memory) of a Memo or Long Binary **[Field](field-object-dao.md)** object in the **[Fields](fields-collection-dao.md)** collection of a **[Recordset](recordset-object-dao.md)** object.

## <a name="syntax"></a>Syntax

*Ausdruck* . Feldgröße

*Ausdruck* Eine Variable, die ein **Field** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Sie können die **FieldSize**-Eigenschaft mit den Methoden **[AppendChunk](field-appendchunk-method-dao.md)** und **[GetChunk](field-getchunk-method-dao.md)** zum Bearbeiten großer Felder verwenden.

Because the size of a Long Binary or Memo field can exceed 64K, you should assign the value returned by **FieldSize** to a variable large enough to store a **Long** variable.

To determine the size of a **Field** object other than Memo and Long Binary types, use the **[Size](field-size-property-dao.md)** property.

  - Der Datenbankserver oder ODBC-Treiber unterstützt keine serverseitigen Cursor.

  - Sie verwenden die ODBC-Cursorbibliothek (d. h. die **DefaultCursorDriver**-Eigenschaft ist auf **dbUseODBC** festgelegt oder auf **dbUseDefault**, wenn der Server keine serverseitigen Cursor unterstützt).

  - Sie verwenden eine Abfrage ohne Cursor (d. h. die **DefaultCursorDriver**-Eigenschaft ist auf **dbUseNoCursor** festgelegt).

Die **FieldSize**-Eigenschaft und die VBA-Funktionen **Len()** oder **LenB()** geben möglicherweise unterschiedliche Werte als Länge derselben Zeichenfolge zurück. Zeichenfolgen werden in einer Microsoft Access-Datenbank in einem MBCS-Format (Multi-Byte Character Set, Mehrbyte-Zeichensatz) gespeichert, jedoch in VBA im Unicode-Format angezeigt. Folglich gibt die **Len()**-Funktion immer die Anzahl von Zeichen, die **LenB**-Funktion immer die Anzahl von Zeichen mal 2 (Unicode verwendet 2 Bytes pro Zeichen) und die **FieldSize**-Eigenschaft einen Wert dazwischen zurück, wenn die Zeichenfolge MBCS-Zeichen enthält. Angenommen, eine Zeichenfolge besteht aus 3 normalen Zeichen und 2 MBCS-Zeichen, dann gibt **Len()** 5 zurück, **LenB()** 10 und **FieldSize** 7, d. h. die Summe von 1 für jedes normale Zeichen und 2 für jedes MBCS-Zeichen.

## <a name="example"></a>Beispiel

This example uses the **FieldSize** property to list the number of bytes used by the Memo and Long Binary Field objects in two different tables.

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

In diesem Beispiel werden die Methoden **AppendChunk** und **GetChunk** verwendet, um ein OLE-Objektfeld mit Daten aus einem anderen Datensatz zu füllen (immer jeweils 32 KB). In einer echten Anwendung kann es sinnvoll sein, mit einer Prozedur wie dieser einen Mitarbeiterdatensatz (inklusive Foto des Mitarbeiters) von einer Tabelle in eine andere zu kopieren. In diesem Beispiel wird der Datensatz einfach wieder in dieselbe Tabelle kopiert. Beachten Sie, dass die gesamte Bearbeitung des Abschnitts innerhalb einer einzelnen AddNew-Aktualisierungssequenz erfolgt.

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
