---
title: TableDef. Attributes-Eigenschaft (DAO)
TOCTitle: Attributes Property
ms:assetid: d01588c3-e94e-06bd-6568-974873411f2d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834701(v=office.15)
ms:contentKeyID: 48547828
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: abdb0d07f2293a53fccaf0d628c301750027acc6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314392"
---
# <a name="tabledefattributes-property-dao"></a><span data-ttu-id="4e07c-102">TableDef. Attributes-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="4e07c-102">TableDef.Attributes property (DAO)</span></span>


<span data-ttu-id="4e07c-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4e07c-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="4e07c-p101">Legt einen Wert fest, der ein oder mehrere Merkmale eines **TableDef**-Objekts angibt, oder gibt den betreffenden Wert zurück. **Long**-Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="4e07c-p101">Sets or returns a value that indicates one or more characteristics of a **TableDef** object. Read/write **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e07c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e07c-106">Syntax</span></span>

<span data-ttu-id="4e07c-107">*Ausdruck* . Attribute</span><span class="sxs-lookup"><span data-stu-id="4e07c-107">*expression* .Attributes</span></span>

<span data-ttu-id="4e07c-108">*Ausdruck* Eine Variable, die ein **TableDef** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="4e07c-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e07c-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4e07c-109">Remarks</span></span>

<span data-ttu-id="4e07c-110">Für ein Objekt, das noch nicht an eine Auflistung angehängt wurde, besteht Lese-/Schreibzugriff für diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="4e07c-110">For an object not yet appended to a collection, this property is read/write.</span></span>

## <a name="example"></a><span data-ttu-id="4e07c-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="4e07c-111">Example</span></span>

<span data-ttu-id="4e07c-112">In diesem Beispiel wird die **Attributes**-Eigenschaft für **Field**-, **Relation**- und **TableDef**-Objekte in der Northwind-Datenbank angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4e07c-112">This example displays the **Attributes** property for **Field**, **Relation**, and **TableDef** objects in the Northwind database.</span></span>

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

