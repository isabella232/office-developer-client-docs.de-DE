---
title: Relations.Count Property (DAO)
TOCTitle: Count Property
ms:assetid: 7cb3885f-6896-8402-8b18-12769473f051
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196377(v=office.15)
ms:contentKeyID: 48545843
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c1be0766c1f1a2057e5cb7137d2e9131a2505f75
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876008"
---
# <a name="relationscount-property-dao"></a><span data-ttu-id="71194-102">Relations.Count Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="71194-102">Relations.Count Property (DAO)</span></span>


<span data-ttu-id="71194-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="71194-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="71194-p101">Gibt die Anzahl der Objekte in der angegebenen Auflistung zurück. Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="71194-p101">Returns the number of objects in the specified collection. Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="71194-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="71194-106">Syntax</span></span>

<span data-ttu-id="71194-107">*Ausdruck* . Count</span><span class="sxs-lookup"><span data-stu-id="71194-107">*expression* .Count</span></span>

<span data-ttu-id="71194-108">*Ausdruck* Eine Variable, die ein **Relations** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="71194-108">*expression* A variable that represents a **Relations** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="71194-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="71194-109">Remarks</span></span>

<span data-ttu-id="71194-p102">Da die Elemente einer Auflistung mit 0 beginnen, müssen Schleifen immer mit dem Element 0 starten und mit dem Wert der **Count**-Eigenschaft minus 1 enden. Wenn eine Schleife die Elemente einer Auflistung durchsucht, ohne die **Count**-Eigenschaft zu überprüfen, können Sie einen **For Each...Next**-Befehl verwenden.</span><span class="sxs-lookup"><span data-stu-id="71194-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="71194-p103">Der Wert der **Count**-Eigenschaft ist nie Null. Wenn ihr Wert 0 ist, sind keine Objekte in der Auflistung enthalten.</span><span class="sxs-lookup"><span data-stu-id="71194-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

