---
title: Type-Eigenschaft (ADO MD)
TOCTitle: Type property (ADO MD)
ms:assetid: 4aaa151e-1f02-aa7d-a9e5-e7019b200924
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249230(v=office.15)
ms:contentKeyID: 48544671
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 99b4e3e2c6930d8162c57d75978e9dba7b5af3e7
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721927"
---
# <a name="type-property-ado-md"></a><span data-ttu-id="a31c9-102">Type-Eigenschaft (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="a31c9-102">Type property (ADO MD)</span></span>


<span data-ttu-id="a31c9-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a31c9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a31c9-104">Gibt den Type des aktuellen Elements an.</span><span class="sxs-lookup"><span data-stu-id="a31c9-104">Indicates the type of the current member.</span></span>

## <a name="return-values"></a><span data-ttu-id="a31c9-105">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="a31c9-105">Return values</span></span>

<span data-ttu-id="a31c9-106">Gibt einen schreibgeschützten [MemberTypeEnum](membertypeenum.md)-Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a31c9-106">Returns a [MemberTypeEnum](membertypeenum.md) value and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="a31c9-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a31c9-107">Remarks</span></span>

<span data-ttu-id="a31c9-p101">Diese Eigenschaft wird nur für [Member](member-object-ado-md.md)-Objekte unterstützt, die zu einem [Level](level-object-ado-md.md)-Objekt gehören. Wenn auf diese Eigenschaft durch **Member** -Objekte verwiesen wird, die zu einem [Position](position-object-ado-md.md)-Objekt gehören, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="a31c9-p101">This property is supported only on [Member](member-object-ado-md.md) objects belonging to a [Level](level-object-ado-md.md) object. An error occurs when this property is referenced from **Member** objects belonging to a [Position](position-object-ado-md.md) object.</span></span>

