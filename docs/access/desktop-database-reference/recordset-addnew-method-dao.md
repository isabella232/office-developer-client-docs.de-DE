---
title: Recordset.AddNew-Methode (DAO)
TOCTitle: AddNew Method
ms:assetid: 18cb35f6-8652-fb20-2460-3d13fae39d23
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845624(v=office.15)
ms:contentKeyID: 48543483
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052883
f1_categories:
- Office.Version=v15
ms.localizationpriority: high
ms.openlocfilehash: a09120299915a879de2019de3ba5326cdc8f0c0a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59606338"
---
# <a name="recordsetaddnew-method-dao"></a>Recordset.AddNew-Methode (DAO)

**Gilt für**: Access 2013, Office 2013

Erstellt einen neuen Datensatz für ein aktualisierbares **[Recordset](recordset-object-dao.md)**-Objekt.

## <a name="syntax"></a>Syntax

*expression* .AddNew

*Ausdruck* Eine Variable, die ein **Recordset**-Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die **AddNew**-Methode, um einen neuen Datensatz im **Recordset**-Objekt, das nach dem Recordset benannt ist, zu erstellen und hinzuzufügen. Diese Methode legt die Felder auf Standardwerte fest. Wenn keine Standardwerte angegeben sind, werden die Felder auf "Null" festgelegt (die Standardwerte, die für einen Tabellentyp **Recordset** angegeben sind).

Verwenden Sie nach dem Ändern des neuen Datensatzes die **[Update](recordset-update-method-dao.md)** -Methode, um die Änderungen zu speichern und den Datensatz zum **Recordset** hinzuzufügen. In der Datenbank treten Änderungen erst dann auf, wenn Sie die **Update** -Methode verwenden.

> [!NOTE]
> Wenn Sie **AddNew** ausgeben und dann einen Vorgang ausführen, der ohne Verwenden von **Update** zu einem anderen Datensatz springt, gehen Ihre Änderungen ohne Warnung verloren, Wenn Sie das **Recordset** schließen oder das Verfahren beenden, das das **Recordset** oder sein **[Datenbankobjekt](database-object-dao.md)** deklariert, wird der neue Datensatz ohne Warnung verworfen.

> [!NOTE]
> Wenn Sie **AddNew** in einem Microsoft Access-Arbeitsbereich verwenden und das Datenbankmodul eine neue Seite für den aktuellen Datensatz erstellen muss, ist Seitensperrung pessimistisch. Wenn der neue Datensatz auf eine vorhandene Seite passt, ist Seitensperrung optimistisch.

Wenn Sie noch nicht zum letzten Datensatz Ihres **Recordsets** gesprungen sind, sind Datensätze, die von anderen Prozessen Basistabellen hinzugefügt werden, möglicherweise enthalten, wenn sie nach dem aktuellen Datensatz positioniert sind. Wenn Sie Ihrem eigenen **Recordset** einen Datensatz hinzufügen, wird der Datensatz allerdings im **Recordset** angezeigt und in die zugrunde liegende Tabelle eingeschlossen, wo er für alle neuen **Recordset** -Objekte sichtbar wird.

Die Position des neuen Datensatzes hängt vom **Recordset** -Typ ab:

- In einem **Recordset** -Objekt vom dynaset-Typ werden Datensätze am Ende des **Recordsets** eingefügt, unabhängig von Sortier- oder Reihenfolgeregeln, die beim Öffnen des **Recordsets** wirksam waren.

- In einem Tabellentyp- **Recordset** -Objekt, für das die **[Index](recordset-index-property-dao.md)** -Eigenschaft festgelegt wurde, werden Datensätze am entsprechenden Platz in der Sortierreihenfolge zurückgegeben. Falls Sie die **Index** -Eigenschaft nicht festgelegt haben, werden neue Datensätze am Ende des **Recordsets** zurückgegeben.

Der Datensatz, der aktuell war, bevor Sie **AddNew** verwendet haben, bleibt aktuell. Wenn Sie den neuen Datensatz aktuell machen möchten, können Sie die **[Bookmark](recordset-bookmark-property-dao.md)** -Eigenschaft auf das Bookmark festlegen, das von der **[LastModified](recordset-lastmodified-property-dao.md)** -Eigenschaftseinstellung identifiziert wird.

> [!NOTE]
> Es muss ein eindeutiger Index für den Datensatz in der zugrunde liegenden Datenquelle vorhanden sein, damit der Datensatz hinzugefügt, bearbeitet oder gelöscht werden kann. Andernfalls tritt im Aufruf der Methoden **AddNew**, **Delete** oder **Edit** in einem Microsoft Access-Arbeitsbereich ein Fehler vom Typ "Berechtigung verweigert" auf.

## <a name="example"></a>Beispiel

This example uses the **AddNew** method to create a new record with the specified name. The AddName function is required for this procedure to run.

```vb
    Sub AddNewX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
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
     
    Function AddName(rstTemp As Recordset, _ 
     strFirst As String, strLast As String) 
     
     ' Adds a new record to a Recordset using the data passed 
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
