---
title: Documents.Count Property (DAO)
TOCTitle: Count Property
ms:assetid: 3fc0b1e6-f7be-cd43-711f-5cf5763fe7f6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192858(v=office.15)
ms:contentKeyID: 48544407
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053325
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 3c2f55430874b9483f738f8410dbd444dc1db34a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475887"
---
# <a name="documentscount-property-dao"></a><span data-ttu-id="842b1-102">Documents.Count Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="842b1-102">Documents.Count Property (DAO)</span></span>


<span data-ttu-id="842b1-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="842b1-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="842b1-p101">Gibt die Anzahl der Objekte in der angegebenen Auflistung zurück. Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="842b1-p101">Returns the number of objects in the specified collection. Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="842b1-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="842b1-106">Syntax</span></span>

<span data-ttu-id="842b1-107">*Ausdruck* . Count</span><span class="sxs-lookup"><span data-stu-id="842b1-107">*expression* .Count</span></span>

<span data-ttu-id="842b1-108">*Ausdruck* Eine Variable, die ein **Documents** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="842b1-108">*expression* A variable that represents a **Documents** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="842b1-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="842b1-109">Remarks</span></span>

<span data-ttu-id="842b1-p102">Da die Elemente einer Auflistung mit 0 beginnen, müssen Schleifen immer mit dem Element 0 starten und mit dem Wert der **Count**-Eigenschaft minus 1 enden. Wenn eine Schleife die Elemente einer Auflistung durchsucht, ohne die **Count**-Eigenschaft zu überprüfen, können Sie einen **For Each...Next**-Befehl verwenden.</span><span class="sxs-lookup"><span data-stu-id="842b1-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="842b1-p103">Der Wert der **Count**-Eigenschaft ist nie Null. Wenn ihr Wert 0 ist, sind keine Objekte in der Auflistung enthalten.</span><span class="sxs-lookup"><span data-stu-id="842b1-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

