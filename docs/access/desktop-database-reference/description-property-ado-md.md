---
title: Description-Eigenschaft (ADO MD)
TOCTitle: Description Property (ADO MD)
ms:assetid: 06d5e1d0-6ed7-fe14-3723-3790e225482a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248816(v=office.15)
ms:contentKeyID: 48543055
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 29c6723d710fcf3a8114fb4460326d87261c3fc1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473350"
---
# <a name="description-property-ado-md"></a><span data-ttu-id="4c7f6-102">Description-Eigenschaft (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="4c7f6-102">Description Property (ADO MD)</span></span>


<span data-ttu-id="4c7f6-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="4c7f6-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="4c7f6-104">Gibt eine Texterläuterung des aktuellen Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-104">Returns a text explanation of the current object.</span></span>

## <a name="return-values"></a><span data-ttu-id="4c7f6-105">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="4c7f6-105">Return Values</span></span>

<span data-ttu-id="4c7f6-106">Gibt einen schreibgeschützten **String** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-106">Returns a **String** and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c7f6-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4c7f6-107">Remarks</span></span>

<span data-ttu-id="4c7f6-p101">Bei Member-Objekten wird die Description-Eigenschaft nur für Measure- und Formula-Member verwendet. Description gibt für alle anderen Elementtypen eine leere Zeichenfolge ("") zurück. Weitere Informationen zu verschiedenen Elementtypen finden Sie unter der Type-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-p101">For [Member](member-object-ado-md.md) objects, **Description** applies only to measure and formula members. **Description** returns an empty string ("") for all other types of members. For more information about the various types of members, see the [Type](type-property-ado-md.md) property.</span></span>

<span data-ttu-id="4c7f6-p102">Diese Eigenschaft wird nur für **Member** -Objekte unterstützt, die zu einem [Level](level-object-ado-md.md)-Objekt gehören. Es Wenn auf diese Eigenschaft durch **Member** -Objekte verwiesen wird, die zu einem [Position](position-object-ado-md.md)-Objekt gehören, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-p102">This property is only supported on **Member** objects belonging to a [Level](level-object-ado-md.md) object. An error occurs when this property is referenced from **Member** objects belonging to a [Position](position-object-ado-md.md) object.</span></span>

