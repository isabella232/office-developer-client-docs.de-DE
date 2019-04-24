---
title: Indexes. Count-Eigenschaft (DAO)
TOCTitle: Count Property
ms:assetid: 195ede10-f91e-50c6-6af4-b318c476b9ea
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845647(v=office.15)
ms:contentKeyID: 48543499
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cffbf14e73e97113194eb25b8e0d5799d3578086
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291545"
---
# <a name="indexescount-property-dao"></a><span data-ttu-id="2b3d7-102">Indexes. Count-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="2b3d7-102">Indexes.Count property (DAO)</span></span>


<span data-ttu-id="2b3d7-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2b3d7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2b3d7-104">Gibt die Anzahl von Objekten in der angegebenen Auflistung zurück.</span><span class="sxs-lookup"><span data-stu-id="2b3d7-104">Returns the number of objects in the specified collection.</span></span> <span data-ttu-id="2b3d7-105">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="2b3d7-105">Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b3d7-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b3d7-106">Syntax</span></span>

<span data-ttu-id="2b3d7-107">*Ausdruck* . Count</span><span class="sxs-lookup"><span data-stu-id="2b3d7-107">*expression* .Count</span></span>

<span data-ttu-id="2b3d7-108">*Ausdruck* Eine Variable, die ein **Indexes** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="2b3d7-108">*expression* A variable that represents an **Indexes** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b3d7-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2b3d7-109">Remarks</span></span>

<span data-ttu-id="2b3d7-p102">Da die Elemente einer Auflistung mit 0 beginnen, müssen Schleifen immer mit dem Element 0 starten und mit dem Wert der **Count**-Eigenschaft minus 1 enden. Wenn eine Schleife die Elemente einer Auflistung durchsucht, ohne die **Count**-Eigenschaft zu überprüfen, können Sie einen **For Each...Next**-Befehl verwenden.</span><span class="sxs-lookup"><span data-stu-id="2b3d7-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="2b3d7-p103">Der Wert der **Count**-Eigenschaft ist nie Null. Wenn ihr Wert 0 ist, sind keine Objekte in der Auflistung enthalten.</span><span class="sxs-lookup"><span data-stu-id="2b3d7-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

