---
title: Workspaces.Count Property (DAO)
TOCTitle: Count Property
ms:assetid: bc7c5a11-13d3-27bd-1be4-5d069e888ac2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822719(v=office.15)
ms:contentKeyID: 48547414
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0632556d7e62b426f462e17d732db323513afcec
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888251"
---
# <a name="workspacescount-property-dao"></a><span data-ttu-id="329e4-102">Workspaces.Count Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="329e4-102">Workspaces.Count Property (DAO)</span></span>


<span data-ttu-id="329e4-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="329e4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="329e4-p101">Gibt die Anzahl der Objekte in der angegebenen Auflistung zurück. Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="329e4-p101">Returns the number of objects in the specified collection. Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="329e4-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="329e4-106">Syntax</span></span>

<span data-ttu-id="329e4-107">*Ausdruck* . Count</span><span class="sxs-lookup"><span data-stu-id="329e4-107">*expression* .Count</span></span>

<span data-ttu-id="329e4-108">*Ausdruck* Eine Variable, die ein **Workspaces** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="329e4-108">*expression* A variable that represents a **Workspaces** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="329e4-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="329e4-109">Remarks</span></span>

<span data-ttu-id="329e4-p102">Da die Elemente einer Auflistung mit 0 beginnen, müssen Schleifen immer mit dem Element 0 starten und mit dem Wert der **Count**-Eigenschaft minus 1 enden. Wenn eine Schleife die Elemente einer Auflistung durchsucht, ohne die **Count**-Eigenschaft zu überprüfen, können Sie einen **For Each...Next**-Befehl verwenden.</span><span class="sxs-lookup"><span data-stu-id="329e4-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="329e4-p103">Der Wert der **Count**-Eigenschaft ist nie Null. Wenn ihr Wert 0 ist, sind keine Objekte in der Auflistung enthalten.</span><span class="sxs-lookup"><span data-stu-id="329e4-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

