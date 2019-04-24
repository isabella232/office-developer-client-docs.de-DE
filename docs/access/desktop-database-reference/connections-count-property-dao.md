---
title: Connections. Count-Eigenschaft (DAO)
TOCTitle: Count Property
ms:assetid: 9b2f0aaa-785a-7fe7-15c3-aea37fdacd12
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198023(v=office.15)
ms:contentKeyID: 48546563
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a286bf992116dc4ddfa71a9be8231e70b717aaa3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295758"
---
# <a name="connectionscount-property-dao"></a><span data-ttu-id="50835-102">Connections. Count-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="50835-102">Connections.Count property (DAO)</span></span>


<span data-ttu-id="50835-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="50835-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="50835-104">Gibt die Anzahl von **[Connection](connection-object-dao.md)** -Objekten in der **[Connections](connections-collection-dao.md)** -Auflistung zurück.</span><span class="sxs-lookup"><span data-stu-id="50835-104">Returns the number of **[Connection](connection-object-dao.md)** objects in the **[Connections](connections-collection-dao.md)** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="50835-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="50835-105">Syntax</span></span>

<span data-ttu-id="50835-106">*Ausdruck* . Count</span><span class="sxs-lookup"><span data-stu-id="50835-106">*expression* .Count</span></span>

<span data-ttu-id="50835-107">*Ausdruck* Eine Variable, die ein **Connections** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="50835-107">*expression* A variable that represents a **Connections** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="50835-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="50835-108">Remarks</span></span>

<span data-ttu-id="50835-p101">Da die Elemente einer Auflistung mit 0 beginnen, müssen Schleifen immer mit dem Element 0 starten und mit dem Wert der **Count**-Eigenschaft minus 1 enden. Wenn eine Schleife die Elemente einer Auflistung durchsucht, ohne die **Count**-Eigenschaft zu überprüfen, können Sie einen **For Each...Next**-Befehl verwenden.</span><span class="sxs-lookup"><span data-stu-id="50835-p101">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="50835-p102">Der Wert der **Count**-Eigenschaft ist nie Null. Wenn ihr Wert 0 ist, sind keine Objekte in der Auflistung enthalten.</span><span class="sxs-lookup"><span data-stu-id="50835-p102">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

