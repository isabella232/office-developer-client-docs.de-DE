---
title: Recordsets. Count-Eigenschaft (DAO)
TOCTitle: Count Property
ms:assetid: 4362aa16-c8e9-e517-887e-c4532bd1eef9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192940(v=office.15)
ms:contentKeyID: 48544500
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a81c1ede8a3afb95e39b2c33fb8112119faf8bd8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309290"
---
# <a name="recordsetscount-property-dao"></a><span data-ttu-id="1da96-102">Recordsets. Count-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="1da96-102">Recordsets.Count property (DAO)</span></span>


<span data-ttu-id="1da96-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1da96-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1da96-104">Gibt die Anzahl der Objekte in der angegebenen Auflistung zurück.</span><span class="sxs-lookup"><span data-stu-id="1da96-104">Returns the number of objects in the specified collection.</span></span> <span data-ttu-id="1da96-105">Schreibgeschützter **Integer**-Wert.</span><span class="sxs-lookup"><span data-stu-id="1da96-105">Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="1da96-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1da96-106">Syntax</span></span>

<span data-ttu-id="1da96-107">*Ausdruck* . Count</span><span class="sxs-lookup"><span data-stu-id="1da96-107">*expression* .Count</span></span>

<span data-ttu-id="1da96-108">*Ausdruck* Eine Variable, die ein **Recordsets** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="1da96-108">*expression* A variable that represents a **Recordsets** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1da96-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1da96-109">Remarks</span></span>

<span data-ttu-id="1da96-p102">Da die Elemente einer Auflistung mit 0 beginnen, müssen Schleifen immer mit dem Element 0 starten und mit dem Wert der **Count**-Eigenschaft minus 1 enden. Wenn eine Schleife die Elemente einer Auflistung durchsucht, ohne die **Count**-Eigenschaft zu überprüfen, können Sie einen **For Each...Next**-Befehl verwenden.</span><span class="sxs-lookup"><span data-stu-id="1da96-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="1da96-p103">Der Wert der **Count**-Eigenschaft ist nie Null. Wenn ihr Wert 0 ist, sind keine Objekte in der Auflistung enthalten.</span><span class="sxs-lookup"><span data-stu-id="1da96-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

