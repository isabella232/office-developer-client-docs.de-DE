---
title: Fields.Count-Eigenschaft (DAO)
TOCTitle: Count Property
ms:assetid: 574de1db-2640-159b-7756-28c37acc9f83
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194261(v=office.15)
ms:contentKeyID: 48544969
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 99eb21ba4f4ef13c902fc0d029dba59c30066853
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701193"
---
# <a name="fieldscount-property-dao"></a><span data-ttu-id="b4c9b-102">Fields.Count-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="b4c9b-102">Fields.Count property (DAO)</span></span>


<span data-ttu-id="b4c9b-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b4c9b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b4c9b-p101">Gibt die Anzahl der Objekte in der angegebenen Auflistung zurück. Schreibgeschützter **Integer**-Wert.</span><span class="sxs-lookup"><span data-stu-id="b4c9b-p101">Returns the number of objects in the specified collection. Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4c9b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4c9b-106">Syntax</span></span>

<span data-ttu-id="b4c9b-107">*Ausdruck* . Count</span><span class="sxs-lookup"><span data-stu-id="b4c9b-107">*expression* .Count</span></span>

<span data-ttu-id="b4c9b-108">*Ausdruck* Eine Variable, die ein **Fields** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="b4c9b-108">*expression* A variable that represents a **Fields** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4c9b-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b4c9b-109">Remarks</span></span>

<span data-ttu-id="b4c9b-p102">Da die Elemente einer Auflistung mit 0 beginnen, müssen Schleifen immer mit dem Element 0 starten und mit dem Wert der **Count**-Eigenschaft minus 1 enden. Wenn eine Schleife die Elemente einer Auflistung durchsucht, ohne die **Count**-Eigenschaft zu überprüfen, können Sie einen **For Each...Next**-Befehl verwenden.</span><span class="sxs-lookup"><span data-stu-id="b4c9b-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="b4c9b-p103">Der Wert der **Count**-Eigenschaft ist nie Null. Wenn ihr Wert 0 ist, sind keine Objekte in der Auflistung enthalten.</span><span class="sxs-lookup"><span data-stu-id="b4c9b-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

