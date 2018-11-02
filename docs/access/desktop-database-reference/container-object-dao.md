---
title: Container-Objekt (DAO)
TOCTitle: Container Object
ms:assetid: 22e487cd-e966-fe68-fff3-c680b460cbeb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191764(v=office.15)
ms:contentKeyID: 48543720
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ba9284e0d62c99ab9bcb631b29587e16a3d76bce
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919514"
---
# <a name="container-object-dao"></a><span data-ttu-id="dab2f-102">Container-Objekt (DAO)</span><span class="sxs-lookup"><span data-stu-id="dab2f-102">Container object (DAO)</span></span>

<span data-ttu-id="dab2f-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dab2f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dab2f-104">Ein **Container**-Objekt fasst ähnliche Typen von **Document**-Objekten in Gruppen zusammen.</span><span class="sxs-lookup"><span data-stu-id="dab2f-104">A **Container** object groups similar types of **Document** objects together.</span></span>

## <a name="remarks"></a><span data-ttu-id="dab2f-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dab2f-105">Remarks</span></span>

<span data-ttu-id="dab2f-p101">Jedes **Database**-Objekt besitzt eine **Containers**-Auflistung, die aus integrierten **Container**-Objekten besteht. Anwendungen können eigene Dokumenttypen und entsprechende Container definieren (gilt nur für Microsoft Access-Datenbanken). Diese Objekte werden jedoch möglicherweise nicht immer von DAO unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dab2f-p101">Each **Database** object has a **Containers** collection consisting of built-in **Container** objects. Applications can define their own document types and corresponding containers (Microsoft Access database engine databases only); however, these objects may not always be supported through DAO.</span></span>

<span data-ttu-id="dab2f-p102">Einige dieser **Container**-Objekte werden durch das Microsoft Access-Datenbankmodul und einige möglicherweise durch andere Anwendungen definiert. In der folgenden Tabelle werden die Namen der einzelnen **Container**-Objekte, die durch das Microsoft Access-Datenbankmodul definiert werden, und der Typ der jeweils enthaltenen Informationen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="dab2f-p102">Some of these **Container** objects are defined by the Microsoft Access database engine while others may be defined by other applications. The following table lists the name of each **Container** object defined by the Microsoft Access database engine and what type of information it contains.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dab2f-110">Containername</span><span class="sxs-lookup"><span data-stu-id="dab2f-110">Container name</span></span></p></th>
<th><p><span data-ttu-id="dab2f-111">Enthält Informationen zu</span><span class="sxs-lookup"><span data-stu-id="dab2f-111">Contains information about</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dab2f-112">Databases</span><span class="sxs-lookup"><span data-stu-id="dab2f-112">Databases</span></span></p></td>
<td><p><span data-ttu-id="dab2f-113">Gespeicherten Datenbanken</span><span class="sxs-lookup"><span data-stu-id="dab2f-113">Saved databases</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dab2f-114">Tables</span><span class="sxs-lookup"><span data-stu-id="dab2f-114">Tables</span></span></p></td>
<td><p><span data-ttu-id="dab2f-115">Gespeicherten Tabellen und Abfragen</span><span class="sxs-lookup"><span data-stu-id="dab2f-115">Saved tables and queries</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dab2f-116">Relations</span><span class="sxs-lookup"><span data-stu-id="dab2f-116">Relations</span></span></p></td>
<td><p><span data-ttu-id="dab2f-117">Gespeicherten Beziehungen</span><span class="sxs-lookup"><span data-stu-id="dab2f-117">Saved relationships</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="dab2f-p103">Verwechseln Sie die in der obigen Tabelle aufgeführten Container-Objekte nicht mit den gleichnamigen Auflistungen. Das Container-Objekt Databases bezieht sich auf alle gespeicherten Datenbankobjekte, während sich die Databases-Auflistung nur auf Datenbankobjekte bezieht, die in einem bestimmten Arbeitsbereich geöffnet sind.</span><span class="sxs-lookup"><span data-stu-id="dab2f-p103">Don't confuse the **Container** objects listed in the preceding table with the collections of the same name. The Databases **Container** object refers to all saved database objects, but the **Databases** collection refers only to database objects that are open in a particular workspace.</span></span>

<span data-ttu-id="dab2f-p104">Jedes **Container**-Objekt besitzt eine **Documents**-Auflistung mit **Document**-Objekten. Diese Objekte beschreiben die Instanzen von integrierten Objekten des Typs, der durch das **Container**-Objekt angegeben wird. In der Regel verwenden Sie ein **Container**-Objekt als direkte Verknüpfung mit den Informationen des **Document**-Objekts. Mithilfe der **Containers**-Auflistung können Sie die Sicherheit für alle **Document**-Objekte eines bestimmten Typs festlegen.</span><span class="sxs-lookup"><span data-stu-id="dab2f-p104">Each **Container** object has a **Documents** collection containing **Document** objects that describe instances of built-in objects of the type specified by the **Container**. You typically use a **Container** object as an intermediate link to the information in the **Document** object. You can also use the **Containers** collection to set security for all **Document** objects of a given type.</span></span>

<span data-ttu-id="dab2f-123">Bei einem vorhandenen **Container**-Objekt können Sie die folgenden Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="dab2f-123">With an existing **Container** object, you can:</span></span>

- <span data-ttu-id="dab2f-124">Geben Sie mit der **Name**-Eigenschaft den vordefinierten Namen des **Container**-Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="dab2f-124">Use the **Name** property to return the predefined name of the **Container** object.</span></span>

- <span data-ttu-id="dab2f-p105">Verwenden Sie die **Owner**-Eigenschaft, um den Eigentümer des **Container**-Objekts festzulegen oder zurückzugeben. Um die **Owner**-Eigenschaft festlegen zu können, benötigen Sie Schreibberechtigungen für das **Container**-Objekt, außerdem müssen Sie die Eigenschaft auf den Namen eines vorhandenen **User**- oder **Group**-Objekts festlegen.</span><span class="sxs-lookup"><span data-stu-id="dab2f-p105">Use the **Owner** property to set or return the owner of the **Container** object. To set the **Owner** property, you must have write permission for the **Container** object, and you must set the property to the name of an existing **User** or **Group** object.</span></span>

- <span data-ttu-id="dab2f-127">Legen Sie mit den Eigenschaften **Permissions** und **UserName** die Zugriffsberechtigungen für das **Container**-Objekt fest. Jedes **Document**-Objekt, das in der **Documents**-Auflistung eines **Container**-Objekts erstellt wird, erbt diese Zugriffsberechtigungseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="dab2f-127">Use the **Permissions** and **UserName** properties to set access permissions for the **Container** object; any **Document** object created in the **Documents** collection of a **Container** object inherits these access permission settings.</span></span>

<span data-ttu-id="dab2f-128">Da **Container**-Objekte integriert sind, können Sie neue **Container**-Objekte erstellen oder vorhandene Objekte löschen.</span><span class="sxs-lookup"><span data-stu-id="dab2f-128">Because **Container** objects are built-in, you can't create new **Container** objects or delete existing ones.</span></span>

<span data-ttu-id="dab2f-129">Wenn Sie auf ein **Container**-Objekt in einer Auflistung mit seiner Ordnungszahl oder mit der Einstellung seiner **Name**-Eigenschaft verweisen möchten, verwenden Sie eine der folgenden Syntaxformen:</span><span class="sxs-lookup"><span data-stu-id="dab2f-129">To refer to a **Container** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

- <span data-ttu-id="dab2f-130">**Containers**(0)</span><span class="sxs-lookup"><span data-stu-id="dab2f-130">**Containers**(0)</span></span>

- <span data-ttu-id="dab2f-131">**Container mit Daten** ("*Name*")</span><span class="sxs-lookup"><span data-stu-id="dab2f-131">**Containers**("*name*")</span></span>

- <span data-ttu-id="dab2f-132">**Container**\!\[*Namen*\]</span><span class="sxs-lookup"><span data-stu-id="dab2f-132">**Containers**\!\[*name*\]</span></span>

## <a name="example"></a><span data-ttu-id="dab2f-133">Beispiel</span><span class="sxs-lookup"><span data-stu-id="dab2f-133">Example</span></span>

<span data-ttu-id="dab2f-134">Das folgende Beispiel führt die **Containers**-Auflistung der Nordwind-Datenbank und die **Properties**-Auflistung jedes **Container**-Objekts der Auflistung auf.</span><span class="sxs-lookup"><span data-stu-id="dab2f-134">This example enumerates the **Containers** collection of the Northwind database and the **Properties** collection of each **Container** object in the collection.</span></span>

```vb
    Sub ContainerObjectX() 
     
     Dim dbsNorthwind As Database 
     Dim ctrLoop As Container 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     
     ' Enumerate Containers collection. 
     For Each ctrLoop In .Containers 
     Debug.Print "Properties of " & ctrLoop.Name _ 
     & " container" 
     
     ' Enumerate Properties collection of each 
     ' Container object. 
     For Each prpLoop In ctrLoop.Properties 
     Debug.Print " " & prpLoop.Name _ 
     & " = " prpLoop 
     Next prpLoop 
     
     Next ctrLoop 
     
     .Close 
     End With 
     
    End Sub
```
