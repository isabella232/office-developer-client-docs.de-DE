---
title: Umgestalten (Access Desktop Database Reference)
TOCTitle: Reshaping
ms:assetid: 89c6a0d6-3bf4-36ae-26ec-d4e60f920490
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249605(v=office.15)
ms:contentKeyID: 48546174
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c820e82669789d7c3806cc1fd38a2eb6844b722e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314777"
---
# <a name="reshaping"></a><span data-ttu-id="5269f-102">Reshaping</span><span class="sxs-lookup"><span data-stu-id="5269f-102">Reshaping</span></span>

<span data-ttu-id="5269f-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5269f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5269f-p101">Einem **Recordset**-Objekt, das mit einer Klausel eines Shape-Befehls erstellt wird, kann ein *Aliasname* zugewiesen werden (in der Regel mit dem AS-Schlüsselwort). Auf den Alias eines strukturierten **Recordset**-Objekts kann in einem völlig anderen Befehl verwiesen werden. Das heißt, dass Sie ein zuvor strukturiertes **Recordset**-Objekt in einem neuen Shape-Befehl erneut verwenden bzw. *umstrukturieren* können. Zur Unterstützung dieses Features stellt ADO eine Eigenschaft [Reshape Name](reshape-name-property-dynamic-ado.md) bereit.</span><span class="sxs-lookup"><span data-stu-id="5269f-p101">A **Recordset** created by a clause of a shape command may be assigned an *alias* name (typically with the AS keyword). The alias of a shaped **Recordset** can be referenced in an entirely different command. That is, you may reuse, or *reshape*, a previously shaped **Recordset** in a new shape command. To support this feature, ADO provides a property, [Reshape Name](reshape-name-property-dynamic-ado.md).</span></span>

<span data-ttu-id="5269f-p102">Die Umstrukturierung erfüllt zwei Hauptfunktionen. Die erste Funktion besteht darin, einem vorhandenen **Recordset**-Objekt ein neues übergeordnetes **Recordset**-Objekt zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="5269f-p102">Reshaping has two main functions. The first is to associate an existing **Recordset** with a new parent **Recordset**.</span></span>

## <a name="example"></a><span data-ttu-id="5269f-110">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5269f-110">Example</span></span>

```vb 
 
. . . 
rs1.Open "SHAPE {select * from Customers} " & _ 
 "APPEND ({select * from Orders} AS chapOrders " & _ 
 "RELATE CustomerID to CustomerID)", cn 
 
rs2.Open "SHAPE {select * from Employees} " & _ 
 "APPEND (chapOrders RELATE EmployeeID to EmployeeID)", cn 
. . . 
```

<span data-ttu-id="5269f-111">Die zweite Funktion besteht darin, den Zugriff auf vorhandene untergeordnete **Recordset** -Objekte mithilfe der Syntax `"SHAPE <recordset reshape name>"`zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="5269f-111">The second function is to enable non-chaptered access to existing child **Recordset** objects, using the syntax `"SHAPE <recordset reshape name>"`.</span></span>

> [!NOTE]
> <span data-ttu-id="5269f-112">[!HINWEIS] Sie können keine Spalten an ein vorhandenes **Recordset** -Objekt anfügen, kein parametrisiertes **Recordset** -Objekt oder **Recordset** -Objekte in einer dazwischen liegenden COMPUTE-Klausel umstrukturieren und keine Aggregatoperationen zu einem **Recordset** -Objekt ausführen, das von dem umzustrukturierenden **Recordset** abstammt.</span><span class="sxs-lookup"><span data-stu-id="5269f-112">You cannot append columns to an existing **Recordset**, reshape a parameterized **Recordset** or the **Recordset** objects in any intervening COMPUTE clause, or perform aggregate operations on any **Recordset** descendant from the **Recordset** being reshaped.</span></span> <span data-ttu-id="5269f-113">Das **Recordset** -Objekt, das neu gestaltet wird, und der neue Shape-Befehl müssen beide dasselbe \* \*[Connection](connection-object-ado.md) -Objekts verwenden.</span><span class="sxs-lookup"><span data-stu-id="5269f-113">The **Recordset** being reshaped and the new shape command must both use the same \*\*[Connection](connection-object-ado.md) object.</span></span>


