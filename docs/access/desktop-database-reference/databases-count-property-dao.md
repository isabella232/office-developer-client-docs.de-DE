---
title: DataBases. Count-Eigenschaft (DAO)
TOCTitle: Count Property
ms:assetid: 7c542b17-9806-e00e-8cbd-58d6d17e98c4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196364(v=office.15)
ms:contentKeyID: 48545831
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cd8908492721315202c5bdf26109753c88905a07
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294624"
---
# <a name="databasescount-property-dao"></a><span data-ttu-id="057f8-102">DataBases. Count-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="057f8-102">Databases.Count property (DAO)</span></span>


<span data-ttu-id="057f8-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="057f8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="057f8-104">Gibt die Anzahl von Objekten in der angegebenen Auflistung zurück.</span><span class="sxs-lookup"><span data-stu-id="057f8-104">Returns the number of objects in the specified collection.</span></span> <span data-ttu-id="057f8-105">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="057f8-105">Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="057f8-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="057f8-106">Syntax</span></span>

<span data-ttu-id="057f8-107">*Ausdruck* . Count</span><span class="sxs-lookup"><span data-stu-id="057f8-107">*expression* .Count</span></span>

<span data-ttu-id="057f8-108">*Ausdruck* Eine Variable, die ein \*\*\*\* Databases-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="057f8-108">*expression* A variable that represents a **Databases** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="057f8-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="057f8-109">Remarks</span></span>

<span data-ttu-id="057f8-p102">Da die Elemente einer Auflistung mit 0 beginnen, müssen Schleifen immer mit dem Element 0 starten und mit dem Wert der **Count**-Eigenschaft minus 1 enden. Wenn eine Schleife die Elemente einer Auflistung durchsucht, ohne die **Count**-Eigenschaft zu überprüfen, können Sie einen **For Each...Next**-Befehl verwenden.</span><span class="sxs-lookup"><span data-stu-id="057f8-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="057f8-p103">Der Wert der **Count**-Eigenschaft ist nie Null. Wenn ihr Wert 0 ist, sind keine Objekte in der Auflistung enthalten.</span><span class="sxs-lookup"><span data-stu-id="057f8-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

