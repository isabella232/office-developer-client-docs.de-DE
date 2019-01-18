---
title: Parameters.Count-Eigenschaft (DAO)
TOCTitle: Count Property
ms:assetid: bc8c814b-da55-22b7-431f-a0f7e6cac994
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822720(v=office.15)
ms:contentKeyID: 48547415
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 536e058a0485479cabd1cc2a0aae09f2396bfbcc
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713114"
---
# <a name="parameterscount-property-dao"></a><span data-ttu-id="6f801-102">Parameters.Count-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="6f801-102">Parameters.Count property (DAO)</span></span>


<span data-ttu-id="6f801-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6f801-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6f801-p101">Gibt die Anzahl der Objekte in der angegebenen Auflistung zurück. Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="6f801-p101">Returns the number of objects in the specified collection. Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f801-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f801-106">Syntax</span></span>

<span data-ttu-id="6f801-107">*Ausdruck* . Count</span><span class="sxs-lookup"><span data-stu-id="6f801-107">*expression* .Count</span></span>

<span data-ttu-id="6f801-108">*Ausdruck* Eine Variable, die ein **Parameter** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="6f801-108">*expression* A variable that represents a **Parameters** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f801-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6f801-109">Remarks</span></span>

<span data-ttu-id="6f801-p102">Da die Elemente einer Auflistung mit 0 beginnen, müssen Schleifen immer mit dem Element 0 starten und mit dem Wert der **Count**-Eigenschaft minus 1 enden. Wenn eine Schleife die Elemente einer Auflistung durchsucht, ohne die **Count**-Eigenschaft zu überprüfen, können Sie einen **For Each...Next**-Befehl verwenden.</span><span class="sxs-lookup"><span data-stu-id="6f801-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="6f801-p103">Der Wert der **Count**-Eigenschaft ist nie Null. Wenn ihr Wert 0 ist, sind keine Objekte in der Auflistung enthalten.</span><span class="sxs-lookup"><span data-stu-id="6f801-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

