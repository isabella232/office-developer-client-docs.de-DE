---
title: Relation.Attributes-Eigenschaft (DAO)
TOCTitle: Attributes Property
ms:assetid: db19d2ad-5965-214c-211d-9a8eb9c3c522
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835337(v=office.15)
ms:contentKeyID: 48548098
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 01b9a49b5b8ec9b702b3fd5beb8b03e3b2365788
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919829"
---
# <a name="relationattributes-property-dao"></a><span data-ttu-id="e7ae1-102">Relation.Attributes-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="e7ae1-102">Relation.Attributes property (DAO)</span></span>


<span data-ttu-id="e7ae1-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e7ae1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e7ae1-p101">Legt einen Wert fest, der mindestens ein Merkmal eines **Relation**-Objekts angibt, oder gibt den betreffenden Wert zurück. **Long**-Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="e7ae1-p101">Sets or returns a value that indicates one or more characteristics of a **Relation** object. Read/write **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7ae1-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7ae1-106">Syntax</span></span>

<span data-ttu-id="e7ae1-107">*Ausdruck* . Attribute</span><span class="sxs-lookup"><span data-stu-id="e7ae1-107">*expression* .Attributes</span></span>

<span data-ttu-id="e7ae1-108">*Ausdruck* Eine Variable, die ein **Relation** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="e7ae1-108">*expression* A variable that represents a **Relation** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7ae1-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e7ae1-109">Remarks</span></span>

<span data-ttu-id="e7ae1-110">Für ein Objekt, das noch nicht an eine Auflistung angehängt wurde, besteht Lese-/Schreibzugriff für diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="e7ae1-110">For an object not yet appended to a collection, this property is read/write.</span></span>

## <a name="example"></a><span data-ttu-id="e7ae1-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e7ae1-111">Example</span></span>

<span data-ttu-id="e7ae1-112">Dieses Beispiel zeigt die **Attributes**-Eigenschaft für die Objekte **Field**, **Relation** und **TableDef** in der Nordwind-Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="e7ae1-112">This example displays the **Attributes** property for **Field**, **Relation**, and **TableDef** objects in the Northwind database.</span></span>

```vb 
Sub AttributesX() 
 
 Dim dbsNorthwind As Database 
 Dim fldLoop As Field 
 Dim relLoop As Relation 
 Dim tdfloop As TableDef 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind 
 
 ' Display the attributes of a TableDef object's 
 ' fields. 
 Debug.Print "Attributes of fields in " & _ 
 .TableDefs(0).Name & " table:" 
 For Each fldLoop In .TableDefs(0).Fields 
 Debug.Print " " & fldLoop.Name & " = " & _ 
 fldLoop.Attributes 
 Next fldLoop 
 
 ' Display the attributes of the Northwind database's 
 ' relations. 
 Debug.Print "Attributes of relations in " & _ 
 .Name & ":" 
 For Each relLoop In .Relations 
 Debug.Print " " & relLoop.Name & " = " & _ 
 relLoop.Attributes 
 Next relLoop 
 
 ' Display the attributes of the Northwind database's 
 ' tables. 
 Debug.Print "Attributes of tables in " & .Name & ":" 
 For Each tdfloop In .TableDefs 
 Debug.Print " " & tdfloop.Name & " = " & _ 
 tdfloop.Attributes 
 Next tdfloop 
 
 .Close 
 End With 
 
End Sub 
 
```

