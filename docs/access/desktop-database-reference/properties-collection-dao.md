---
title: Properties-Auflistung (DAO)
TOCTitle: Properties Collection
ms:assetid: cd07184a-a261-29c9-542f-bc2eff6f4af6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834455(v=office.15)
ms:contentKeyID: 48547753
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 05379dee652732bc0839abb056cc15962e3683b0
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926941"
---
# <a name="properties-collection-dao"></a><span data-ttu-id="ded9d-102">Properties-Auflistung (DAO)</span><span class="sxs-lookup"><span data-stu-id="ded9d-102">Properties collection (DAO)</span></span>


<span data-ttu-id="ded9d-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ded9d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ded9d-104">Eine **Properties**-Auflistung enthält alle **[Property](property-object-dao.md)** -Objekte für eine bestimmte Objektinstanz.</span><span class="sxs-lookup"><span data-stu-id="ded9d-104">A **Properties** collection contains all the **[Property](property-object-dao.md)** objects for a specific instance of an object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ded9d-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ded9d-105">Remarks</span></span>

<span data-ttu-id="ded9d-p101">Mit Ausnahme der Objekte **Connection** und **Error** enthält jedes DAO-Objekt eine **Properties**-Auflistung, in die bestimmte **Property**-Objekte integriert sind. Diese **Property**-Objekte (die oft nur als Eigenschaften bezeichnet werden) kennzeichnen die betreffende Objektinstanz eindeutig.</span><span class="sxs-lookup"><span data-stu-id="ded9d-p101">Every DAO object except the **Connection** and **Error** objects contains a **Properties** collection, which has certain built-in **Property** objects. These **Property** objects (which are often just called properties) uniquely characterize that instance of the object.</span></span>

<span data-ttu-id="ded9d-p102">Zusätzlich zu den integrierten Eigenschaften können Sie auch eigene benutzerdefinierte Eigenschaften erstellen und hinzufügen. Wenn Sie einer vorhandenen Objektinstanz eine benutzerdefinierte Eigenschaft hinzufügen möchten, definieren Sie zunächst mit der **CreateProperty**-Methode die Merkmale dieser Eigenschaft und fügen Sie sie dann mit der **Append**-Methode der Auflistung hinzu. Wenn Sie auf ein benutzerdefiniertes **Property**-Objekt verweisen, das noch nicht an eine **Properties**-Auflistung angefügt wurde, tritt ein Fehler auf. Auch das Anfügen eines benutzerdefinierten **Property**-Objekts an eine **Properties**-Auflistung, die ein **Property**-Objekt mit demselben Namen enthält, führt zu einem Fehler.</span><span class="sxs-lookup"><span data-stu-id="ded9d-p102">In addition to the built-in properties, you can also create and add your own user-defined properties. To add a user-defined property to an existing instance of an object, first define its characteristics with the **CreateProperty** method, then add it to the collection with the **Append** method. Referencing a user-defined **Property** object that has not yet been appended to a **Properties** collection will cause an error, as will appending a user-defined **Property** object to a **Properties** collection containing a **Property** object of the same name.</span></span>

<span data-ttu-id="ded9d-111">Mit der **Delete**-Methode können Sie benutzerdefinierte Eigenschaften aus der **Properties**-Auflistung entfernen. Es ist jedoch nicht möglich, integrierte Eigenschaften zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="ded9d-111">You can use the **Delete** method to remove user-defined properties from the **Properties** collection, but you can't remove built-in properties.</span></span>


> [!NOTE]
> <P><span data-ttu-id="ded9d-p103">[!HINWEIS] Ein benutzerdefiniertes <STRONG>Property</STRONG>-Objekt bezieht sich nur auf eine bestimmte Objektinstanz. Die Eigenschaft ist nicht für alle Objektinstanzen des ausgewählten Typs definiert.</span><span class="sxs-lookup"><span data-stu-id="ded9d-p103">A user-defined <STRONG>Property</STRONG> object is associated only with the specific instance of an object. The property isn't defined for all instances of objects of the selected type.</span></span></P>



<span data-ttu-id="ded9d-114">Der Verweis auf ein integriertes **Property**-Objekt in einer Auflistung erfolgt über dessen Ordnungszahl oder den Wert der **Name**-Eigenschaft, wobei Sie die folgenden Syntaxformen verwenden können:</span><span class="sxs-lookup"><span data-stu-id="ded9d-114">To refer to a built-in **Property** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="ded9d-115">-Objekt. **Eigenschaften** (0)</span><span class="sxs-lookup"><span data-stu-id="ded9d-115">object.**Properties**(0)</span></span>

<span data-ttu-id="ded9d-116">-Objekt. **Eigenschaften** ("Name")</span><span class="sxs-lookup"><span data-stu-id="ded9d-116">object.**Properties**("name")</span></span>

<span data-ttu-id="ded9d-117">-Objekt. **Eigenschaften** \! \[Namen\]</span><span class="sxs-lookup"><span data-stu-id="ded9d-117">object.**Properties**\!\[name\]</span></span>

<span data-ttu-id="ded9d-118">Bei einer integrierten Eigenschaft können Sie auch diese Syntax verwenden:</span><span class="sxs-lookup"><span data-stu-id="ded9d-118">For a built-in property, you can also use this syntax:</span></span>

<span data-ttu-id="ded9d-119">Object.Name</span><span class="sxs-lookup"><span data-stu-id="ded9d-119">object.name</span></span>


> [!NOTE]
> <P><span data-ttu-id="ded9d-120">Für eine benutzerdefinierte Eigenschaft müssen Sie das vollständige-Objekt verwenden. <STRONG>Eigenschaften</STRONG> Syntax ("Name").</span><span class="sxs-lookup"><span data-stu-id="ded9d-120">For a user-defined property, you must use the full object.<STRONG>Properties</STRONG>("name") syntax.</span></span></P>



<span data-ttu-id="ded9d-p104">Sie können mit denselben Syntaxformen auf die **Value**-Eigenschaft eines **Property**-Objekts verweisen. Der Kontext des Verweises entscheidet, ob Sie sich auf das **Property**-Objekt selbst oder auf die **Value**-Eigenschaft des **Property**-Objekts beziehen.</span><span class="sxs-lookup"><span data-stu-id="ded9d-p104">With the same syntax forms, you can also refer to the **Value** property of a **Property** object. The context of the reference will determine whether you are referring to the **Property** object itself or the **Value** property of the **Property** object.</span></span>

## <a name="example"></a><span data-ttu-id="ded9d-123">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ded9d-123">Example</span></span>

<span data-ttu-id="ded9d-p105">In diesem Beispiel wird eine benutzerdefinierte Eigenschaft für die aktuelle Datenbank erstellt, die Eigenschaften **Type** und **Value** werden festgelegt und an die **Properties**-Auflistung der Datenbank angefügt. Dann werden alle Eigenschaften in der Datenbank im Beispiel aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="ded9d-p105">This example creates a user-defined property for the current database, sets its **Type** and **Value** properties, and appends it to the **Properties** collection of the database. Then the example enumerates all properties in the database.</span></span>

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

<span data-ttu-id="ded9d-p106">In diesem Beispiel wird versucht, den Wert einer benutzerdefinierten Eigenschaft festzulegen. Wenn die Eigenschaft nicht vorhanden ist, wird die CreateProperty-Methode zum Erstellen und Festlegen des Werts der neuen Eigenschaft verwendet. Zum Ausführen dieses Vorgangs ist die SetProperty-Prozedur erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ded9d-p106">This example tries to set the value of a user-defined property. If the property doesn't exist, it uses the **CreateProperty** method to create and set the value of the new property. The SetProperty procedure is required for this procedure to run.</span></span>

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
