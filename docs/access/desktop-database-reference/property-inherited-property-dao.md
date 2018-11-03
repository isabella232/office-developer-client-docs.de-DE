---
title: Property.Inherited-Eigenschaft (DAO)
TOCTitle: Inherited Property
ms:assetid: 10e624db-2301-b9be-beca-6e8caccf7274
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845349(v=office.15)
ms:contentKeyID: 48543304
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052991
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 56f0153748a6d5cc7dd8e6b15dbae93fb638a381
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927158"
---
# <a name="propertyinherited-property-dao"></a><span data-ttu-id="26bec-102">Property.Inherited-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="26bec-102">Property.Inherited property (DAO)</span></span>


<span data-ttu-id="26bec-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="26bec-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="26bec-104">Gibt einen Wert zurück, der angibt, ob ein **[Property](property-object-dao.md)** -Objekt von einem zugrunde liegenden Objekt geerbt wurde.</span><span class="sxs-lookup"><span data-stu-id="26bec-104">Returns a value that indicates whether a **[Property](property-object-dao.md)** object is inherited from an underlying object.</span></span>

## <a name="syntax"></a><span data-ttu-id="26bec-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="26bec-105">Syntax</span></span>

<span data-ttu-id="26bec-106">*Ausdruck* . Vererbte Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="26bec-106">*expression* .Inherited</span></span>

<span data-ttu-id="26bec-107">*Ausdruck* Eine Variable, die ein **Property-** Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="26bec-107">*expression* A variable that represents a **Property** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="26bec-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="26bec-108">Remarks</span></span>

<span data-ttu-id="26bec-109">Bei integrierten **Property**-Objekten, die vordefinierte Eigenschaften darstellen, kann nur **False** zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="26bec-109">For built-in **Property** objects that represent predefined properties, the only possible return value is **False**.</span></span>

<span data-ttu-id="26bec-p101">Mit der **Inherited**-Eigenschaft können Sie feststellen, ob für ein bestimmtes Objekt ein benutzerdefiniertes **Property**-Objekt erstellt wurde, oder ob das **Property**-Objekt von einem anderen Objekt geerbt wurde. Beispiel: Sie erstellen ein neues **Property**-Objekt für ein **[QueryDef](querydef-object-dao.md)** -Objekt und öffnen dann über das [QueryDef](recordset-object-dao.md)-Objekt ein \*\*\*\*Recordset\*\*\*\* -Objekt. Dieses neue **Property**-Objekt ist Teil der [**Properties**](properties-collection-dao.md) -Auflistung des **Recordset**-Objekts, und seine **Inherited**-Eigenschaft erhält den Wert **True**, da die Eigenschaft für das **QueryDef**-Objekt erstellt wurde und nicht für das **Recordset**-Objekt.</span><span class="sxs-lookup"><span data-stu-id="26bec-p101">You can use the **Inherited** property to determine whether a user-defined **Property** was created for the object it applies to, or whether the **Property** was inherited from another object. For example, suppose you create a new **Property** for a **[QueryDef](querydef-object-dao.md)** object and then open a **[Recordset](recordset-object-dao.md)** object from the **QueryDef** object. This new **Property** will be part of the **Recordset** object's **[Properties](properties-collection-dao.md)** collection, and its **Inherited** property will be set to **True** because the property was created for the **QueryDef** object, not the **Recordset** object.</span></span>

## <a name="example"></a><span data-ttu-id="26bec-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="26bec-113">Example</span></span>

<span data-ttu-id="26bec-114">In diesem Beispiel wird die **Inherited**-Eigenschaft verwendet, um festzustellen, ob ein benutzerdefiniertes **Property**-Objekt für ein **Recordset**-Objekt erstellt wurde oder für ein anderes zugrunde liegendes Objekt.</span><span class="sxs-lookup"><span data-stu-id="26bec-114">This example use the **Inherited** property to determine if a user-defined **Property** object was created for a **Recordset** object or for some underlying object.</span></span>

```vb 
Sub InheritedX() 
 
 Dim dbsNorthwind As Database 
 Dim tdfTest As TableDef 
 Dim rstTest As Recordset 
 Dim prpNew As Property 
 Dim prpLoop As Property 
 
 ' Create a new property for a saved TableDef object, then 
 ' open a recordset from that TableDef object. 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 Set tdfTest = dbsNorthwind.TableDefs(0) 
 Set prpNew = tdfTest.CreateProperty("NewProperty", _ 
 dbBoolean, True) 
 tdfTest.Properties.Append prpNew 
 Set rstTest = tdfTest.OpenRecordset(dbOpenForwardOnly) 
 
 ' Show Name and Inherited property of the new Property 
 ' object in the TableDef. 
 Debug.Print "NewProperty of " & tdfTest.Name & _ 
 " TableDef:" 
 Debug.Print " Inherited = " & _ 
 tdfTest.Properties("NewProperty").Inherited 
 
 ' Show Name and Inherited property of the new Property 
 ' object in the Recordset. 
 Debug.Print "NewProperty of " & rstTest.Name & _ 
 " Recordset:" 
 Debug.Print " Inherited = " & _ 
 rstTest.Properties("NewProperty").Inherited 
 
 ' Delete new TableDef because this is a demonstration. 
 tdfTest.Properties.Delete prpNew.Name 
 dbsNorthwind.Close 
 
End Sub 
 
```

