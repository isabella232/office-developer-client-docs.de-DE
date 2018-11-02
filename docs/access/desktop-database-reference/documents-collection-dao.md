---
title: Documents-Auflistung (DAO)
TOCTitle: Documents Collection
ms:assetid: ae2fef58-34e7-eea6-ca51-d3903432c7f5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821742(v=office.15)
ms:contentKeyID: 48547063
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 602060ef3e62da12baa2d5847106504cc54eb9f9
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925730"
---
# <a name="documents-collection-dao"></a><span data-ttu-id="a092e-102">Documents-Auflistung (DAO)</span><span class="sxs-lookup"><span data-stu-id="a092e-102">Documents collection (DAO)</span></span>


<span data-ttu-id="a092e-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a092e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a092e-104">Eine **Documents**-Auflistung enthält alle **Document**-Objekte für einen bestimmten Objekttyp (nur für Microsoft Access-Datenbanken).</span><span class="sxs-lookup"><span data-stu-id="a092e-104">A **Documents** collection contains all of the **Document** objects for a specific type of object (Microsoft Access database engine databases only).</span></span>

## <a name="remarks"></a><span data-ttu-id="a092e-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a092e-105">Remarks</span></span>

<span data-ttu-id="a092e-106">Jedes **Container**-Objekt verfügt über eine **Documents**-Auflistung mit **Document**-Objekten, die Instanzen integrierter Objekte des durch das **Container**-Objekt angegebenen Typs beschreiben.</span><span class="sxs-lookup"><span data-stu-id="a092e-106">Each **Container** object has a **Documents** collection containing **Document** objects that describe instances of built-in objects of the type specified by the **Container**.</span></span>

<span data-ttu-id="a092e-107">Der Verweis auf ein **Document**-Objekt in einer Auflistung erfolgt über dessen Ordnungszahl oder den Wert der **Name**-Eigenschaft, wobei Sie die folgenden Syntaxformen verwenden können:</span><span class="sxs-lookup"><span data-stu-id="a092e-107">To refer to a **Document** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

  - <span data-ttu-id="a092e-108">**Documents**(0)</span><span class="sxs-lookup"><span data-stu-id="a092e-108">**Documents**(0)</span></span>

  - <span data-ttu-id="a092e-109">**Dokumente** ("*Name*")</span><span class="sxs-lookup"><span data-stu-id="a092e-109">**Documents**("*name*")</span></span>

  - <span data-ttu-id="a092e-110">**Dokumente**\!\[*Namen*\]</span><span class="sxs-lookup"><span data-stu-id="a092e-110">**Documents**\!\[*name*\]</span></span>

## <a name="example"></a><span data-ttu-id="a092e-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a092e-111">Example</span></span>

<span data-ttu-id="a092e-112">In diesem Beispiel wird die **Documents**-Auflistung aus dem Tabellencontainer aufgeführt und anschließend die **Properties**-Auflistung des ersten **Document**-Objekts in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="a092e-112">This example enumerates the **Documents** collection of the Tables container, and then enumerates the **Properties** collection of the first **Document** object in the collection.</span></span>

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

