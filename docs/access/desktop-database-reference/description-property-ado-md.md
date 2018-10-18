---
title: Description-Eigenschaft (ADO MD)
TOCTitle: Description Property (ADO MD)
ms:assetid: 06d5e1d0-6ed7-fe14-3723-3790e225482a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248816(v=office.15)
ms:contentKeyID: 48543055
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7dd66e0288e20bcf38adefc2fcc30f1856ebf3e6
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606871"
---
# <a name="description-property-ado-md"></a><span data-ttu-id="bbaec-102">Description-Eigenschaft (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="bbaec-102">Description Property (ADO MD)</span></span>


<span data-ttu-id="bbaec-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="bbaec-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="bbaec-104">Gibt eine Texterläuterung des aktuellen Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="bbaec-104">Returns a text explanation of the current object.</span></span>

<span data-ttu-id="bbaec-105"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="bbaec-105"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="bbaec-106">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bbaec-106">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="bbaec-107">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="bbaec-107">Return values</span></span>
>>>>>>> <span data-ttu-id="bbaec-108">master</span><span class="sxs-lookup"><span data-stu-id="bbaec-108">master</span></span>

<span data-ttu-id="bbaec-109">Gibt einen schreibgeschützten **String** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="bbaec-109">Returns a **String** and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbaec-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bbaec-110">Remarks</span></span>

<span data-ttu-id="bbaec-p101">Bei Member-Objekten wird die Description-Eigenschaft nur für Measure- und Formula-Member verwendet. Description gibt für alle anderen Elementtypen eine leere Zeichenfolge ("") zurück. Weitere Informationen zu verschiedenen Elementtypen finden Sie unter der Type-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="bbaec-p101">For [Member](member-object-ado-md.md) objects, **Description** applies only to measure and formula members. **Description** returns an empty string ("") for all other types of members. For more information about the various types of members, see the [Type](type-property-ado-md.md) property.</span></span>

<span data-ttu-id="bbaec-p102">Diese Eigenschaft wird nur für **Member** -Objekte unterstützt, die zu einem [Level](level-object-ado-md.md)-Objekt gehören. Es Wenn auf diese Eigenschaft durch **Member** -Objekte verwiesen wird, die zu einem [Position](position-object-ado-md.md)-Objekt gehören, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="bbaec-p102">This property is only supported on **Member** objects belonging to a [Level](level-object-ado-md.md) object. An error occurs when this property is referenced from **Member** objects belonging to a [Position](position-object-ado-md.md) object.</span></span>

