---
title: Properties-Auflistung (DAO)
TOCTitle: Properties collection
ms:assetid: cd07184a-a261-29c9-542f-bc2eff6f4af6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834455(v=office.15)
ms:contentKeyID: 48547753
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: c7dd26ac4a150ca5daa2b0011ac9373e662f2dbb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622074"
---
# <a name="properties-collection-dao"></a>Properties-Auflistung (DAO)

**Gilt für**: Access 2013, Office 2013

Eine **Properties**-Auflistung enthält alle **[Property](property-object-dao.md)** -Objekte einer bestimmten Instanz eines Objekts.

## <a name="remarks"></a>Bemerkungen

Mit Ausnahme der Objekte **Connection** und **Error** enthält jedes DAO-Objekt eine **Properties**-Auflistung, in die bestimmte **Property**-Objekte integriert sind. Diese **Property**-Objekte (die oft nur als Eigenschaften bezeichnet werden) kennzeichnen die betreffende Objektinstanz eindeutig.

Zusätzlich zu den integrierten Eigenschaften können Sie auch eigene benutzerdefinierte Eigenschaften erstellen und hinzufügen. Wenn Sie einer vorhandenen Objektinstanz eine benutzerdefinierte Eigenschaft hinzufügen möchten, definieren Sie zunächst mit der **CreateProperty**-Methode die Merkmale dieser Eigenschaft und fügen Sie sie dann mit der **Append**-Methode der Auflistung hinzu. Wenn Sie auf ein benutzerdefiniertes **Property**-Objekt verweisen, das noch nicht an eine **Properties**-Auflistung angefügt wurde, tritt ein Fehler auf. Auch das Anfügen eines benutzerdefinierten **Property**-Objekts an eine **Properties**-Auflistung, die ein **Property**-Objekt mit demselben Namen enthält, führt zu einem Fehler.

Mit der **Delete**-Methode können Sie benutzerdefinierte Eigenschaften aus der **Properties**-Auflistung entfernen. Es ist jedoch nicht möglich, integrierte Eigenschaften zu entfernen.

> [!NOTE]
> [!HINWEIS] Ein benutzerdefiniertes **Property**-Objekt bezieht sich nur auf eine bestimmte Objektinstanz. Die Eigenschaft ist nicht für alle Objektinstanzen des ausgewählten Typs definiert.

Der Verweis auf ein integriertes **Property**-Objekt in einer Auflistung erfolgt über dessen Ordnungszahl oder den Wert der **Name**-Eigenschaft, wobei Sie die folgenden Syntaxformen verwenden können:

- Objekt. **Eigenschaften**(0)

- Objekt. **Eigenschaften**("Name")

- Objekt.  \! Eigenschaften \[ Namen\]

Bei einer integrierten Eigenschaft können Sie auch diese Syntax verwenden:

- object.name

> [!NOTE]
> Für eine benutzerdefinierte Eigenschaft müssen Sie das vollständige Objekt verwenden. Eigenschaftensyntax ("Name").

Sie können mit denselben Syntaxformen auf die **Value**-Eigenschaft eines **Property**-Objekts verweisen. Der Kontext des Verweises entscheidet, ob Sie sich auf das **Property**-Objekt selbst oder auf die **Value**-Eigenschaft des **Property**-Objekts beziehen.

## <a name="example"></a>Beispiel

In diesem Beispiel wird eine benutzerdefinierte Eigenschaft für die aktuelle Datenbank erstellt, die Eigenschaften **Type** und **Value** werden festgelegt und an die **Properties**-Auflistung der Datenbank angefügt. Dann werden alle Eigenschaften in der Datenbank im Beispiel aufgeführt.

```vb
    Sub PropertyX() 
     
     Dim dbsNorthwind As Database 
     Dim prpNew As Property 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     ' Create and append user-defined property. 
     Set prpNew = .CreateProperty() 
     prpNew.Name = "UserDefined" 
     prpNew.Type = dbText 
     prpNew.Value = "This is a user-defined property." 
     .Properties.Append prpNew 
     
     ' Enumerate all properties of current database. 
     Debug.Print "Properties of " & .Name 
     For Each prpLoop In .Properties 
     With prpLoop 
     Debug.Print " " & .Name 
     Debug.Print " Type: " & .Type 
     Debug.Print " Value: " & .Value 
     Debug.Print " Inherited: " & _ 
     .Inherited 
     End With 
     Next prpLoop 
     
     ' Delete new property because this is a 
     ' demonstration. 
     .Properties.Delete "UserDefined" 
     End With 
     
    End Sub 
```

<br/>

This example tries to set the value of a user-defined property. If the property doesn't exist, it uses the **CreateProperty** method to create and set the value of the new property. The SetProperty procedure is required for this procedure to run.

```vb
    Sub CreatePropertyX() 
     
     Dim dbsNorthwind As Database 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     ' Set the Archive property to True. 
     SetProperty dbsNorthwind, "Archive", True 
     
     With dbsNorthwind 
     Debug.Print "Properties of " & .Name 
     
     ' Enumerate Properties collection of the Northwind 
     ' database. 
     For Each prpLoop In .Properties 
     If prpLoop <> "" Then Debug.Print " " & _ 
     prpLoop.Name & " = " & prpLoop 
     Next prpLoop 
     
     ' Delete the new property since this is a 
     ' demonstration. 
     .Properties.Delete "Archive" 
     
     .Close 
     End With 
     
    End Sub 
     
    Sub SetProperty(dbsTemp As Database, strName As String, _ 
     booTemp As Boolean) 
     
     Dim prpNew As Property 
     Dim errLoop As Error 
     
     ' Attempt to set the specified property. 
     On Error GoTo Err_Property 
     dbsTemp.Properties("strName") = booTemp 
     On Error GoTo 0 
     
     Exit Sub 
     
    Err_Property: 
     
     ' Error 3270 means that the property was not found. 
     If DBEngine.Errors(0).Number = 3270 Then 
     ' Create property, set its value, and append it to the 
     ' Properties collection. 
     Set prpNew = dbsTemp.CreateProperty(strName, _ 
     dbBoolean, booTemp) 
     dbsTemp.Properties.Append prpNew 
     Resume Next 
     Else 
     ' If different error has occurred, display message. 
     For Each errLoop In DBEngine.Errors 
     MsgBox "Error number: " & errLoop.Number & vbCr & _ 
     errLoop.Description 
     Next errLoop 
     End 
     End If 
     
    End Sub
```
