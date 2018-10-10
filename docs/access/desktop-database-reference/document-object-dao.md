---
title: Document Object (DAO)
TOCTitle: Document Object
ms:assetid: b51d4545-b157-4c7c-fdbe-16a25afffdb3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822082(v=office.15)
ms:contentKeyID: 48547247
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 60fe0519bc722e688630f13acdd6701b96beff05
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473778"
---
# <a name="document-object-dao"></a><span data-ttu-id="550ed-102">Document Object (DAO)</span><span class="sxs-lookup"><span data-stu-id="550ed-102">Document Object (DAO)</span></span>


<span data-ttu-id="550ed-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="550ed-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="550ed-p101">Ein **Document**-Objekt schließt Informationen zu einer Objektinstanz ein. Bei dem Objekt kann es sich um eine Datenbank, gespeicherte Tabelle, Abfrage oder Beziehung handeln (gilt nur für Microsoft Access-Datenbanken).</span><span class="sxs-lookup"><span data-stu-id="550ed-p101">A **Document** object includes information about one instance of an object. The object can be a database, saved table, query, or relationship (Microsoft Access database engine databases only).</span></span>

## <a name="remarks"></a><span data-ttu-id="550ed-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="550ed-106">Remarks</span></span>

<span data-ttu-id="550ed-p102">Jedes **Container**-Objekt besitzt eine **Documents**-Auflistung mit **Document**-Objekten. Diese Objekte beschreiben die Instanzen von integrierten Objekten des Typs, der durch das **Container**-Objekt angegeben wird. In der folgenden Tabelle wird der Objekttyp der einzelnen **Document**-Objekte, der Name des jeweiligen **Container**-Objekts und der Typ der im **Document**-Objekt enthaltenen Informationen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="550ed-p102">Each **Container** object has a **Documents** collection containing **Document** objects that describe instances of built-in objects of the type specified by the **Container**. The following table lists the type of object each **Document** describes, the name of its **Container** object, and what type of information **Document** contains.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="550ed-109">Document</span><span class="sxs-lookup"><span data-stu-id="550ed-109">Document</span></span></p></th>
<th><p><span data-ttu-id="550ed-110">Container</span><span class="sxs-lookup"><span data-stu-id="550ed-110">Container</span></span></p></th>
<th><p><span data-ttu-id="550ed-111">Enthält Informationen zu</span><span class="sxs-lookup"><span data-stu-id="550ed-111">Contains information about</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="550ed-112">Datenbank</span><span class="sxs-lookup"><span data-stu-id="550ed-112">Database</span></span></p></td>
<td><p><span data-ttu-id="550ed-113">Databases</span><span class="sxs-lookup"><span data-stu-id="550ed-113">Databases</span></span></p></td>
<td><p><span data-ttu-id="550ed-114">Gespeicherten Datenbanken</span><span class="sxs-lookup"><span data-stu-id="550ed-114">Saved database</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="550ed-115">Tabelle oder Abfrage</span><span class="sxs-lookup"><span data-stu-id="550ed-115">Table or query</span></span></p></td>
<td><p><span data-ttu-id="550ed-116">Tables</span><span class="sxs-lookup"><span data-stu-id="550ed-116">Tables</span></span></p></td>
<td><p><span data-ttu-id="550ed-117">Gespeicherten Tabellen oder Abfragen</span><span class="sxs-lookup"><span data-stu-id="550ed-117">Saved table or query</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="550ed-118">Beziehung</span><span class="sxs-lookup"><span data-stu-id="550ed-118">Relationship</span></span></p></td>
<td><p><span data-ttu-id="550ed-119">Relations</span><span class="sxs-lookup"><span data-stu-id="550ed-119">Relations</span></span></p></td>
<td><p><span data-ttu-id="550ed-120">Gespeicherten Beziehungen</span><span class="sxs-lookup"><span data-stu-id="550ed-120">Saved relationship</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P><span data-ttu-id="550ed-p103">Verwechseln Sie die in der obigen Tabelle aufgeführten Container-Objekte nicht mit den gleichnamigen Auflistungen. Das Container-Objekt Databases bezieht sich auf alle gespeicherten Datenbankobjekte, während sich die Databases-Auflistung nur auf Datenbankobjekte bezieht, die in einem bestimmten Arbeitsbereich geöffnet sind.</span><span class="sxs-lookup"><span data-stu-id="550ed-p103">Don't confuse the <STRONG>Container</STRONG> objects listed in the preceding table with the collections of the same name. The Databases <STRONG>Container</STRONG> object refers to all saved database objects, but the <STRONG>Databases</STRONG> collection refers only to database objects that are open in a particular workspace.</span></span></P>



<span data-ttu-id="550ed-123">Bei einem **Document**-Objekt können Sie die folgenden Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="550ed-123">With a **Document** object, you can:</span></span>

  - <span data-ttu-id="550ed-124">Geben Sie mit der **Name**-Eigenschaft den Namen zurück, den das Objekt bei seiner Erstellung von einem Benutzer oder dem Microsoft Access-Datenbankmodul erhalten hat.</span><span class="sxs-lookup"><span data-stu-id="550ed-124">Use the **Name** property to return the name that a user or the Microsoft Access database engine gave to the object when it was created.</span></span>

  - <span data-ttu-id="550ed-125">Geben Sie mit der **Container**-Eigenschaft den Namen des **Container**-Objekts zurück, das das **Document**-Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="550ed-125">Use the **Container** property to return the name of the **Container** object that contains the **Document** object.</span></span>

  - <span data-ttu-id="550ed-p104">Verwenden Sie die **Owner**-Eigenschaft, um den Eigentümer des Objekts festzulegen oder zurückzugeben. Um die **Owner**-Eigenschaft festlegen zu können, benötigen Sie Schreibberechtigungen für das **Document**-Objekt, außerdem müssen Sie die Eigenschaft auf den Namen eines vorhandenen **User**- oder **Group**-Objekts festlegen.</span><span class="sxs-lookup"><span data-stu-id="550ed-p104">Use the **Owner** property to set or return the owner of the object. To set the **Owner** property, you must have write permission for the **Document** object, and you must set the property to the name of an existing **User** or **Group** object.</span></span>

  - <span data-ttu-id="550ed-p105">Verwenden Sie die **UserName**- oder **Permissions**-Eigenschaft, um die Zugriffsberechtigungen eines Benutzers oder einer Gruppe für das Objekt festzulegen oder zurückzugeben. Um diese Eigenschaften festlegen zu können, benötigen Sie Schreibberechtigungen für das **Document**-Objekt, außerdem müssen Sie die **UserName**-Eigenschaft auf den Namen eines vorhandenen **User**- oder **Group**-Objekts festlegen.</span><span class="sxs-lookup"><span data-stu-id="550ed-p105">Use the **UserName** or **Permissions** properties to set or return the access permissions of a user or group for the object. To set these properties, you must have write permission for the **Document** object, and you must set the **UserName** property to the name of an existing **User** or **Group** object.</span></span>

  - <span data-ttu-id="550ed-130">Verwenden Sie die **DateCreated**- oder **LastUpdated**-Eigenschaft, um das Datum und die Uhrzeit der Erstellung oder letzten Änderung des **Document**-Objekts zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="550ed-130">Use the **DateCreated** and **LastUpdated** properties to return the date and time when the **Document** object was created and last modified.</span></span>

<span data-ttu-id="550ed-p106">Da ein **Document**-Objekt einem vorhandenen Objekt entspricht, können keine neuen **Document**-Objekte erstellt oder vorhandene gelöscht werden. Wenn Sie auf ein **Document**-Objekt in einer Auflistung mit seiner Ordnungszahl oder mit der Einstellung seiner **Name**-Eigenschaft verweisen möchten, verwenden Sie eine der folgenden Syntaxformen:</span><span class="sxs-lookup"><span data-stu-id="550ed-p106">Because a **Document** object corresponds to an existing object, you can't create new **Document** objects or delete existing ones. To refer to a **Document** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

  - <span data-ttu-id="550ed-133">**Documents**(0)</span><span class="sxs-lookup"><span data-stu-id="550ed-133">**Documents**(0)</span></span>

  - <span data-ttu-id="550ed-134">**Dokumente** ("*Name*")</span><span class="sxs-lookup"><span data-stu-id="550ed-134">**Documents**("*name*")</span></span>

  - <span data-ttu-id="550ed-135">**Dokumente**\!\[*Namen*\]</span><span class="sxs-lookup"><span data-stu-id="550ed-135">**Documents**\!\[*name*\]</span></span>

## <a name="example"></a><span data-ttu-id="550ed-136">Beispiel</span><span class="sxs-lookup"><span data-stu-id="550ed-136">Example</span></span>

<span data-ttu-id="550ed-137">In diesem Beispiel wird die **Documents**-Auflistung aus dem Tabellencontainer aufgeführt und anschließend die **Properties**-Auflistung des ersten **Document**-Objekts in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="550ed-137">This example enumerates the **Documents** collection of the Tables container, and then enumerates the **Properties** collection of the first **Document** object in the collection.</span></span>

```vb 
Sub DocumentX() 
 
 Dim dbsNorthwind As Database 
 Dim docLoop As Document 
 Dim prpLoop As Property 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind.Containers!Tables 
 Debug.Print "Documents in " & .Name & " container" 
 ' Enumerate the Documents collection of the Tables 
 ' container. 
 For Each docLoop In .Documents 
 Debug.Print " " & docLoop.Name 
 Next docLoop 
 With .Documents(0) 
 ' Enumerate the Properties collection of the first. 
 ' Document object of the Tables container. 
 Debug.Print "Properties of " & .Name & " document" 
 On Error Resume Next 
 For Each prpLoop In .Properties 
 Debug.Print " " & prpLoop.Name & " = " & _ 
 prpLoop 
 Next prpLoop 
 On Error GoTo 0 
 End With 
 End With 
 
 dbsNorthwind.Close 
 
End Sub 
 
```

<span data-ttu-id="550ed-138">Dieses Beispiel zeigt mit den Eigenschaften **Owner** und **SystemDB** die Eigentümer verschiedener **Document**-Objekte an.</span><span class="sxs-lookup"><span data-stu-id="550ed-138">This example uses the **Owner** and **SystemDB** properties to show the owners of a variety of **Document** objects.</span></span>

```vb 
Sub OwnerX() 
 
 ' Ensure that the Microsoft Access workgroup file is 
 ' available. 
 DBEngine.SystemDB = "system.mdw" 
 
 Dim dbsNorthwind As Database 
 Dim ctrLoop As Container 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind 
 Debug.Print "Document owners:" 
 ' Enumerate Containers collection and show the owner 
 ' of the first Document in each container's Documents 
 ' collection. 
 For Each ctrLoop In .Containers 
 With ctrLoop 
 Debug.Print " [" & .Documents(0).Name & _ 
 "] in [" & .Name & _ 
 "] container owned by [" & _ 
 .Documents(0).Owner & "]" 
 End With 
 Next ctrLoop 
 
 .Close 
 End With 
 
End Sub 
 
```

