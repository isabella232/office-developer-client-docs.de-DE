---
title: Parent-Eigenschaft (ADO MD)
TOCTitle: Parent Property (ADO MD)
ms:assetid: 62649da7-d35f-f11f-674c-28ce95abaf20
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249370(v=office.15)
ms:contentKeyID: 48545238
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 10c183c997a3c0b49c74e08f7ef29fbe8c274516
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603336"
---
# <a name="parent-property-ado-md"></a><span data-ttu-id="43115-102">Parent-Eigenschaft (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="43115-102">Parent Property (ADO MD)</span></span>


<span data-ttu-id="43115-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="43115-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="43115-104">Gibt das Element an, das das übergeordnete Element des aktuellen Elements in einer Hierarchie ist.</span><span class="sxs-lookup"><span data-stu-id="43115-104">Indicates the member that is the parent of the current member in a hierarchy.</span></span>

<span data-ttu-id="43115-105"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="43115-105"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="43115-106">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="43115-106">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="43115-107">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="43115-107">Return values</span></span>
>>>>>>> <span data-ttu-id="43115-108">master</span><span class="sxs-lookup"><span data-stu-id="43115-108">master</span></span>

<span data-ttu-id="43115-109">Gibt als Wert ein schreibgeschütztes [Member](member-object-ado-md.md)-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="43115-109">Returns a [Member](member-object-ado-md.md) object and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="43115-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="43115-110">Remarks</span></span>

<span data-ttu-id="43115-p101">Ein Element auf der obersten Ebene einer Hierarchie (Wurzelebene) weist kein Hauptobjekt auf. Diese Eigenschaft wird nur für **Member** -Objekte unterstützt, die zu einem [Level](level-object-ado-md.md)-Objekt gehören. Wenn auf diese Eigenschaft durch **Member** -Objekte verwiesen wird, die zu einem [Position](position-object-ado-md.md)-Objekt gehören, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="43115-p101">A member that is at the top level of a hierarchy (the root) has no parent. This property is supported only on **Member** objects belonging to a [Level](level-object-ado-md.md) object. An error occurs when this property is referenced from **Member** objects belonging to a [Position](position-object-ado-md.md) object.</span></span>

