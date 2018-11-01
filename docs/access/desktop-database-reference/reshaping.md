---
title: Ändern der Form (Access PC-Datenbank-Referenz)
TOCTitle: Reshaping
ms:assetid: 89c6a0d6-3bf4-36ae-26ec-d4e60f920490
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249605(v=office.15)
ms:contentKeyID: 48546174
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a051c62d73a36fed0832f17b1cb53b1641d4a152
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889280"
---
# <a name="reshaping"></a><span data-ttu-id="3ec30-102">Reshaping</span><span class="sxs-lookup"><span data-stu-id="3ec30-102">Reshaping</span></span>


<span data-ttu-id="3ec30-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3ec30-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3ec30-p101">Einem **Recordset**-Objekt, das mit einer Klausel eines Shape-Befehls erstellt wird, kann ein *Aliasname* zugewiesen werden (in der Regel mit dem AS-Schlüsselwort). Auf den Alias eines strukturierten **Recordset**-Objekts kann in einem völlig anderen Befehl verwiesen werden. Das heißt, dass Sie ein zuvor strukturiertes **Recordset**-Objekt in einem neuen Shape-Befehl erneut verwenden bzw. *umstrukturieren* können. Zur Unterstützung dieses Features stellt ADO eine Eigenschaft [Reshape Name](reshape-name-property-dynamic-ado.md) bereit.</span><span class="sxs-lookup"><span data-stu-id="3ec30-p101">A **Recordset** created by a clause of a shape command may be assigned an *alias* name (typically with the AS keyword). The alias of a shaped **Recordset** can be referenced in an entirely different command. That is, you may reuse, or *reshape*, a previously shaped **Recordset** in a new shape command. To support this feature, ADO provides a property, [Reshape Name](reshape-name-property-dynamic-ado.md).</span></span>

<span data-ttu-id="3ec30-p102">Die Umstrukturierung erfüllt zwei Hauptfunktionen. Die erste Funktion besteht darin, einem vorhandenen **Recordset** -Objekt ein neues übergeordnetes **Recordset** -Objekt zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="3ec30-p102">Reshaping has two main functions. The first is to associate an existing **Recordset** with a new parent **Recordset**.</span></span>

## <a name="example"></a><span data-ttu-id="3ec30-110">Beispiel</span><span class="sxs-lookup"><span data-stu-id="3ec30-110">Example</span></span>

```vb 
 
. . . 
rs1.Open "SHAPE {select * from Customers} " & _ 
 "APPEND ({select * from Orders} AS chapOrders " & _ 
 "RELATE CustomerID to CustomerID)", cn 
 
rs2.Open "SHAPE {select * from Employees} " & _ 
 "APPEND (chapOrders RELATE EmployeeID to EmployeeID)", cn 
. . . 
```

<span data-ttu-id="3ec30-111">Die zweite Funktion besteht darin, Zugriff ohne Kapitel auf vorhandene untergeordnete **Recordset** -Objekte mithilfe der Syntax aktivieren `"SHAPE <recordset reshape name>"`.</span><span class="sxs-lookup"><span data-stu-id="3ec30-111">The second function is to enable non-chaptered access to existing child **Recordset** objects, using the syntax `"SHAPE <recordset reshape name>"`.</span></span>


> [!NOTE]
> <P><span data-ttu-id="3ec30-p103">[!HINWEIS] Sie können keine Spalten an ein vorhandenes <STRONG>Recordset</STRONG> -Objekt anfügen, kein parametrisiertes <STRONG>Recordset</STRONG> -Objekt oder <STRONG>Recordset</STRONG> -Objekte in einer dazwischen liegenden COMPUTE-Klausel umstrukturieren und keine Aggregatoperationen zu einem <STRONG>Recordset</STRONG> -Objekt ausführen, das von dem umzustrukturierenden <STRONG>Recordset</STRONG> abstammt. Das umzustrukturierende <STRONG>Recordset</STRONG> -Objekt und der neue Shape-Befehl müssen dasselbe <A href="connection-object-ado.md">Connection</A>-Objekt verwenden.</span><span class="sxs-lookup"><span data-stu-id="3ec30-p103">You cannot append columns to an existing <STRONG>Recordset</STRONG>, reshape a parameterized <STRONG>Recordset</STRONG> or the <STRONG>Recordset</STRONG> objects in any intervening COMPUTE clause, or perform aggregate operations on any <STRONG>Recordset</STRONG> descendant from the <STRONG>Recordset</STRONG> being reshaped. The <STRONG>Recordset</STRONG> being reshaped and the new shape command must both use the same <A href="connection-object-ado.md">Connection</A>.</span></span></P>


