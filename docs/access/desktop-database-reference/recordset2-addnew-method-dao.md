---
title: Recordset2.AddNew-Methode (DAO)
TOCTitle: AddNew Method
ms:assetid: 25c7d207-185c-943b-405e-b138ffb8b3e2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191874(v=office.15)
ms:contentKeyID: 48543792
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 9a8368247e1a0dbaa524f3adab4d534c1c0cc7e7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631790"
---
# <a name="recordset2addnew-method-dao"></a>Recordset2.AddNew-Methode (DAO)

**Gilt für**: Access 2013, Office 2013
 
Erstellt einen neuen Datensatz für ein aktualisierbares **Recordset2**-Objekt.

## <a name="syntax"></a>Syntax

*expression* .AddNew

*Ausdruck* Eine Variable, die ein **Recordset2-Objekt** darstellt.

## <a name="remarks"></a>Bemerkungen

Use the **AddNew** method to create and add a new record in the **Recordset2** object named by recordset. This method sets the fields to default values, and if no default values are specified, it sets the fields to Null (the default values specified for a table-type **Recordset2**).

Mit der **[Update](recordset2-update-method-dao.md)** -Methode können Sie nach dem Ändern des neuen Datensatzes die Änderungen speichern und den Datensatz zum **Recordset2** hinzufügen. Es treten erst dann Änderungen in der Datenbank auf, wenn Sie die **Update**-Methode verwenden.

> [!NOTE]
> [!HINWEIS] Wenn Sie eine **AddNew**-Methode aufrufen und dann durch einen beliebigen Vorgang zu einem anderen Datensatz wechseln, ohne **Update** zu verwenden, gehen Ihre Änderungen ohne Warnung verloren. Wenn Sie außerdem das **Recordset2** schließen oder die Prozedur beenden, die das **Recordset2** oder dessen **[Database](database-object-dao.md)** -Objekt deklariert, wird der neue Datensatz ohne Warnung verworfen.

> [!NOTE]
> Wenn Sie **AddNew** in einem Microsoft Access-Arbeitsbereich verwenden und das Datenbankmodul eine neue Seite für den aktuellen Datensatz erstellen muss, ist Seitensperrung pessimistisch. Wenn der neue Datensatz auf eine vorhandene Seite passt, ist Seitensperrung optimistisch.

Wenn Sie noch nicht zum letzten Datensatz des **Recordset2**-Objekts gewechselt sind, werden Datensätze, die durch andere Prozesse zu Basistabellen hinzugefügt wurden, möglicherweise einbezogen, wenn sie hinter dem aktuellen Datensatz liegen. Wenn Sie einen Datensatz zu Ihrem eigenen **Recordset2** hinzufügen, ist er im **Recordset2** sichtbar und wird in die zugrunde liegende Tabelle einbezogen, in der er für neue **Recordset2**-Objekte sichtbar wird.

Die Position des neuen Datensatzes hängt vom Typ des **Recordset2**-Objekts ab:

- In a dynaset-type **Recordset2** object, records are inserted at the end of the **Recordset**, regardless of any sorting or ordering rules that were in effect when the **Recordset** was opened.

- In a table-type **Recordset2** object whose **[Index](recordset2-index-property-dao.md)** property has been set, records are returned in their proper place in the sort order. If you haven't set the **Index** property, new records are returned at the end of the **Recordset**.

Der Datensatz, der aktuell war, bevor Sie **AddNew** verwendet haben, bleibt aktuell. Wenn Sie den neuen Datensatz aktuell machen möchten, können Sie die **[Bookmark](recordset2-bookmark-property-dao.md)** -Eigenschaft auf das Bookmark festlegen, das von der **[LastModified](recordset2-lastmodified-property-dao.md)** -Eigenschaftseinstellung identifiziert wird.

> [!NOTE]
> Es muss ein eindeutiger Index für den Datensatz in der zugrunde liegenden Datenquelle vorhanden sein, damit der Datensatz hinzugefügt, bearbeitet oder gelöscht werden kann. Andernfalls tritt im Aufruf der Methoden **AddNew**, **Delete** oder **Edit** in einem Microsoft Access-Arbeitsbereich ein Fehler vom Typ "Berechtigung verweigert" auf.

## <a name="example"></a>Beispiel

This example uses the **AddNew** method to create a new record with the specified name. The AddName function is required for this procedure to run.

```vb
    Sub AddNewX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
     Dim strFirstName As String 
     Dim strLastName As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", dbOpenDynaset) 
     
     ' Get data from the user. 
     strFirstName = Trim(InputBox( _ 
     "Enter first name:")) 
     strLastName = Trim(InputBox( _ 
     "Enter last name:")) 
     
     ' Proceed only if the user actually entered something 
     ' for both the first and last names. 
     If strFirstName <> "" and strLastName <> "" Then 
     
     ' Call the function that adds the record. 
     AddName rstEmployees, strFirstName, strLastName 
     
     ' Show the newly added data. 
     With rstEmployees 
     Debug.Print "New record: " & !FirstName & _ 
     " " & !LastName 
     ' Delete new record because this is a demonstration. 
     .Delete 
     End With 
     
     Else 
     Debug.Print _ 
     "You must input a string for first and last name!" 
     End If 
     
     rstEmployees.Close 
     dbsNorthwind.Close 
     
    End Sub 
     
    Function AddName(rstTemp As Recordset2, _ 
     strFirst As String, strLast As String) 
     
     ' Adds a new record to a recordset using the data passed 
     ' by the calling procedure. The new record is then made 
     ' the current record. 
     With rstTemp 
     .AddNew 
     !FirstName = strFirst 
     !LastName = strLast 
     .Update 
     .Bookmark = .LastModified 
     End With 
     
    End Function
```
