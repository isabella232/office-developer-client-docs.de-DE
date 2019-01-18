---
title: Recordset2.AddNew-Methode (DAO)
TOCTitle: AddNew Method
ms:assetid: 25c7d207-185c-943b-405e-b138ffb8b3e2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191874(v=office.15)
ms:contentKeyID: 48543792
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 49a69b5e8603e72faaba480ea9069d3668bd6de1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699345"
---
# <a name="recordset2addnew-method-dao"></a>Recordset2.AddNew-Methode (DAO)

**Betrifft**: Access 2013, Office 2013
 
Erstellt einen neuen Datensatz für ein aktualisierbares **Recordset2**-Objekt.

## <a name="syntax"></a>Syntax

*Ausdruck* . AddNew

*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die AddNew-Methode, um einen neuen Datensatz zu erstellen und zum durch Recordset benannten Recordset2-Objekt hinzuzufügen. Bei dieser Methode werden die Felder auf Standardwerte festgelegt. Sind keine Standardwerte angegeben, werden die Felder auf Null festgelegt (die für ein Recordset2 des Typs Tabelle angegebenen Standardwerte).

Mit der **[Update](recordset2-update-method-dao.md)** -Methode können Sie nach dem Ändern des neuen Datensatzes die Änderungen speichern und den Datensatz zum **Recordset2** hinzufügen. Es treten erst dann Änderungen in der Datenbank auf, wenn Sie die **Update**-Methode verwenden.

> [!NOTE]
> [!HINWEIS] Wenn Sie eine **AddNew**-Methode aufrufen und dann durch einen beliebigen Vorgang zu einem anderen Datensatz wechseln, ohne **Update** zu verwenden, gehen Ihre Änderungen ohne Warnung verloren. Wenn Sie außerdem das **Recordset2** schließen oder die Prozedur beenden, die das **Recordset2** oder dessen **[Database](database-object-dao.md)** -Objekt deklariert, wird der neue Datensatz ohne Warnung verworfen.

> [!NOTE]
> [!HINWEIS] Wenn Sie **AddNew** in einem Microsoft Access-Arbeitsbereich verwenden und das Datenbankmodul eine neue Seite für den aktuellen Datensatz erstellen muss, ist die Seitensperre pessimistisch. Passt der neue Datensatz hingegen auf eine vorhandene Seite, ist die Seitensperre optimistisch.

Wenn Sie noch nicht zum letzten Datensatz des **Recordset2**-Objekts gewechselt sind, werden Datensätze, die durch andere Prozesse zu Basistabellen hinzugefügt wurden, möglicherweise einbezogen, wenn sie hinter dem aktuellen Datensatz liegen. Wenn Sie einen Datensatz zu Ihrem eigenen **Recordset2** hinzufügen, ist er im **Recordset2** sichtbar und wird in die zugrunde liegende Tabelle einbezogen, in der er für neue **Recordset2**-Objekte sichtbar wird.

Die Position des neuen Datensatzes hängt vom Typ des **Recordset2**-Objekts ab:

- In einem Recordset2-Objekt vom Typ Dynaset werden Datensätze an das Ende des Recordset-Objekts eingefügt, unabhängig davon, welche Regeln in Bezug auf die Sortierung oder Reihenfolge beim Öffnen des Recordset-Objekts gültig waren.

- In einem Recordset2-Objekt vom Typ Tabelle, dessen Index-Eigenschaft festgelegt wurde, werden Datensätze in der Sortierreihenfolge an ihrer richtigen Position zurückgegeben. Falls Sie die Index-Eigenschaft nicht festgelegt haben, werden neue Datensätze am Ende des Recordset-Objekts zurückgegeben.

Der Datensatz, der vor dem Verwenden von **AddNew** aktuell war, bleibt der aktuelle Datensatz. Wenn Sie den neuen Datensatz zum aktuellen Datensatz machen möchten, können Sie die **[Bookmark](recordset2-bookmark-property-dao.md)** -Eigenschaft auf das durch die **[LastModified](recordset2-lastmodified-property-dao.md)** -Eigenschaft identifizierte Lesezeichen festlegen.

> [!NOTE]
> [!HINWEIS] Um einen Datensatz hinzuzufügen, zu bearbeiten oder zu löschen, muss es einen eindeutigen Index im Datensatz in der zugrunde liegenden Datenquelle geben. Andernfalls tritt ein "Berechtigung verweigert"-Fehler im **AddNew** -, **Delete** - oder **Edit** -Methodenaufruf in einem Microsoft Access-Arbeitsbereich auf.

## <a name="example"></a>Beispiel

Dieses Beispiel verwendet die **AddNew** -Methode, um einen neuen Datensatz mit dem angegebenen Namen zu erstellen. Die "AddName"-Funktion ist zum Ausführen dieser Prozedur erforderlich.

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
