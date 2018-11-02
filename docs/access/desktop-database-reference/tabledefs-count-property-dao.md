---
title: TableDefs.Count-Eigenschaft (DAO)
TOCTitle: Count Property
ms:assetid: 6e2cf3e5-524f-a643-b1dc-99a4b2bb2e63
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195561(v=office.15)
ms:contentKeyID: 48545508
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 88a38180973b83232c324d052db0548cb308740a
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923770"
---
# <a name="tabledefscount-property-dao"></a><span data-ttu-id="4ece4-102">TableDefs.Count-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="4ece4-102">TableDefs.Count property (DAO)</span></span>


<span data-ttu-id="4ece4-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4ece4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4ece4-p101">Gibt die Anzahl der Objekte in der angegebenen Auflistung zurück. Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="4ece4-p101">Returns the number of objects in the specified collection. Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ece4-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ece4-106">Syntax</span></span>

<span data-ttu-id="4ece4-107">*Ausdruck* . Count</span><span class="sxs-lookup"><span data-stu-id="4ece4-107">*expression* .Count</span></span>

<span data-ttu-id="4ece4-108">*Ausdruck* Eine Variable, die ein **TableDefs** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="4ece4-108">*expression* A variable that represents a **TableDefs** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ece4-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4ece4-109">Remarks</span></span>

<span data-ttu-id="4ece4-p102">Da die Elemente einer Auflistung mit 0 beginnen, müssen Schleifen immer mit dem Element 0 starten und mit dem Wert der **Count**-Eigenschaft minus 1 enden. Wenn eine Schleife die Elemente einer Auflistung durchsucht, ohne die **Count**-Eigenschaft zu überprüfen, können Sie einen **For Each...Next**-Befehl verwenden.</span><span class="sxs-lookup"><span data-stu-id="4ece4-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="4ece4-p103">Der Wert der **Count**-Eigenschaft ist nie Null. Wenn ihr Wert 0 ist, sind keine Objekte in der Auflistung enthalten.</span><span class="sxs-lookup"><span data-stu-id="4ece4-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

