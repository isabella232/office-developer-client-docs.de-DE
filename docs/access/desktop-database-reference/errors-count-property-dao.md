---
title: Errors.Count Property (DAO)
TOCTitle: Count Property
ms:assetid: ad135955-3b18-4f99-66d9-aff1492df13b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821719(v=office.15)
ms:contentKeyID: 48547028
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 10c49a0f73c759bc901a091bb78bcbd4158e7a1d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867664"
---
# <a name="errorscount-property-dao"></a><span data-ttu-id="ed613-102">Errors.Count Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="ed613-102">Errors.Count Property (DAO)</span></span>


<span data-ttu-id="ed613-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ed613-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ed613-p101">Gibt die Anzahl der Objekte in der angegebenen Auflistung zurück. Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="ed613-p101">Returns the number of objects in the specified collection. Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed613-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed613-106">Syntax</span></span>

<span data-ttu-id="ed613-107">*Ausdruck* . Count</span><span class="sxs-lookup"><span data-stu-id="ed613-107">*expression* .Count</span></span>

<span data-ttu-id="ed613-108">*Ausdruck* Eine Variable, die ein **Errors** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="ed613-108">*expression* A variable that represents an **Errors** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed613-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ed613-109">Remarks</span></span>

<span data-ttu-id="ed613-p102">Da die Elemente einer Auflistung mit 0 beginnen, müssen Schleifen immer mit dem Element 0 starten und mit dem Wert der **Count**-Eigenschaft minus 1 enden. Wenn eine Schleife die Elemente einer Auflistung durchsucht, ohne die **Count**-Eigenschaft zu überprüfen, können Sie einen **For Each...Next**-Befehl verwenden.</span><span class="sxs-lookup"><span data-stu-id="ed613-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="ed613-p103">Der Wert der **Count**-Eigenschaft ist nie Null. Wenn ihr Wert 0 ist, sind keine Objekte in der Auflistung enthalten.</span><span class="sxs-lookup"><span data-stu-id="ed613-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

