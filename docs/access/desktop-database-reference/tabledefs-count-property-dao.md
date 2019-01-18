---
title: TableDefs.Count-Eigenschaft (DAO)
TOCTitle: Count Property
ms:assetid: 6e2cf3e5-524f-a643-b1dc-99a4b2bb2e63
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195561(v=office.15)
ms:contentKeyID: 48545508
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6c997a437cc7a7ae1461e7308899c85dac44fbda
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699547"
---
# <a name="tabledefscount-property-dao"></a><span data-ttu-id="c274c-102">TableDefs.Count-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="c274c-102">TableDefs.Count property (DAO)</span></span>


<span data-ttu-id="c274c-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c274c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c274c-p101">Gibt die Anzahl der Objekte in der angegebenen Auflistung zurück. Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="c274c-p101">Returns the number of objects in the specified collection. Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c274c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c274c-106">Syntax</span></span>

<span data-ttu-id="c274c-107">*Ausdruck* . Count</span><span class="sxs-lookup"><span data-stu-id="c274c-107">*expression* .Count</span></span>

<span data-ttu-id="c274c-108">*Ausdruck* Eine Variable, die ein **TableDefs** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="c274c-108">*expression* A variable that represents a **TableDefs** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c274c-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c274c-109">Remarks</span></span>

<span data-ttu-id="c274c-p102">Da die Elemente einer Auflistung mit 0 beginnen, müssen Schleifen immer mit dem Element 0 starten und mit dem Wert der **Count**-Eigenschaft minus 1 enden. Wenn eine Schleife die Elemente einer Auflistung durchsucht, ohne die **Count**-Eigenschaft zu überprüfen, können Sie einen **For Each...Next**-Befehl verwenden.</span><span class="sxs-lookup"><span data-stu-id="c274c-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="c274c-p103">Der Wert der **Count**-Eigenschaft ist nie Null. Wenn ihr Wert 0 ist, sind keine Objekte in der Auflistung enthalten.</span><span class="sxs-lookup"><span data-stu-id="c274c-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

