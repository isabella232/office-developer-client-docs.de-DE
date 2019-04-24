---
title: Description-Eigenschaft (ADO MD)
TOCTitle: Description property (ADO MD)
ms:assetid: 06d5e1d0-6ed7-fe14-3723-3790e225482a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248816(v=office.15)
ms:contentKeyID: 48543055
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0f74532693f1054dd9d187757af840a3a00b451f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293938"
---
# <a name="description-property-ado-md"></a><span data-ttu-id="195d5-102">Description-Eigenschaft (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="195d5-102">Description property (ADO MD)</span></span>


<span data-ttu-id="195d5-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="195d5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="195d5-104">Gibt eine Texterläuterung des aktuellen Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="195d5-104">Returns a text explanation of the current object.</span></span>

## <a name="return-values"></a><span data-ttu-id="195d5-105">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="195d5-105">Return values</span></span>

<span data-ttu-id="195d5-106">Gibt einen schreibgeschützten **String**-Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="195d5-106">Returns a **String** and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="195d5-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="195d5-107">Remarks</span></span>

<span data-ttu-id="195d5-p101">For [Member](member-object-ado-md.md) objects, **Description** applies only to measure and formula members. **Description** returns an empty string ("") for all other types of members. For more information about the various types of members, see the [Type](type-property-ado-md.md) property.</span><span class="sxs-lookup"><span data-stu-id="195d5-p101">For [Member](member-object-ado-md.md) objects, **Description** applies only to measure and formula members. **Description** returns an empty string ("") for all other types of members. For more information about the various types of members, see the [Type](type-property-ado-md.md) property.</span></span>

<span data-ttu-id="195d5-p102">Diese Eigenschaft wird nur für **Member** -Objekte unterstützt, die zu einem [Level](level-object-ado-md.md)-Objekt gehören. Es Wenn auf diese Eigenschaft durch **Member** -Objekte verwiesen wird, die zu einem [Position](position-object-ado-md.md)-Objekt gehören, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="195d5-p102">This property is only supported on **Member** objects belonging to a [Level](level-object-ado-md.md) object. An error occurs when this property is referenced from **Member** objects belonging to a [Position](position-object-ado-md.md) object.</span></span>

