---
title: Containers. Count-Eigenschaft (DAO)
TOCTitle: Count Property
ms:assetid: 3b0bf865-a4d5-82bb-c1a9-9957f110db4c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192657(v=office.15)
ms:contentKeyID: 48544276
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7553b0e7d64e059dfeed50f158f21f48455976d7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295590"
---
# <a name="containerscount-property-dao"></a><span data-ttu-id="4bb6c-102">Containers. Count-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="4bb6c-102">Containers.Count property (DAO)</span></span>


<span data-ttu-id="4bb6c-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4bb6c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4bb6c-104">Gibt die Anzahl von **[Connection](connection-object-dao.md)** -Objekten in der **[Connections](connections-collection-dao.md)** -Auflistung zurück.</span><span class="sxs-lookup"><span data-stu-id="4bb6c-104">Returns the number of **[Connection](connection-object-dao.md)** objects in the **[Connections](connections-collection-dao.md)** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bb6c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4bb6c-105">Syntax</span></span>

<span data-ttu-id="4bb6c-106">*Ausdruck* . Count</span><span class="sxs-lookup"><span data-stu-id="4bb6c-106">*expression* .Count</span></span>

<span data-ttu-id="4bb6c-107">*Ausdruck* Eine Variable, die ein **Connections** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="4bb6c-107">*expression* A variable that represents a **Connections** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4bb6c-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4bb6c-108">Remarks</span></span>

<span data-ttu-id="4bb6c-p101">Da die Elemente einer Auflistung mit 0 beginnen, müssen Schleifen immer mit dem Element 0 starten und mit dem Wert der **Count**-Eigenschaft minus 1 enden. Wenn eine Schleife die Elemente einer Auflistung durchsucht, ohne die **Count**-Eigenschaft zu überprüfen, können Sie einen **For Each...Next**-Befehl verwenden.</span><span class="sxs-lookup"><span data-stu-id="4bb6c-p101">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="4bb6c-p102">Der Wert der **Count**-Eigenschaft ist nie Null. Wenn ihr Wert 0 ist, sind keine Objekte in der Auflistung enthalten.</span><span class="sxs-lookup"><span data-stu-id="4bb6c-p102">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

