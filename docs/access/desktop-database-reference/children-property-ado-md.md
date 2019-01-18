---
title: Children-Eigenschaft (ADO MD)
TOCTitle: Children property (ADO MD)
ms:assetid: 66eff203-68e5-a36d-eb2f-2e9faa80deb6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249400(v=office.15)
ms:contentKeyID: 48545352
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 27d69e760b65a917270b0851743c108692c601e2
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717825"
---
# <a name="children-property-ado-md"></a><span data-ttu-id="53550-102">Children-Eigenschaft (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="53550-102">Children property (ADO MD)</span></span>


<span data-ttu-id="53550-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="53550-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="53550-104">Gibt eine [Members](members-collection-ado-md.md)-Auflistung zurück, für die das aktuelle [Member](member-object-ado-md.md)-Objekt das übergeordnete Objekt (Hauptobjekt) in der Hierarchie ist.</span><span class="sxs-lookup"><span data-stu-id="53550-104">Returns a [Members](members-collection-ado-md.md) collection for which the current [Member](member-object-ado-md.md) is the parent in the hierarchy.</span></span>

## <a name="return-values"></a><span data-ttu-id="53550-105">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="53550-105">Return values</span></span>

<span data-ttu-id="53550-106">Gibt eine **Members** -Auflistung zurück und ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="53550-106">Returns a **Members** collection and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="53550-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="53550-107">Remarks</span></span>

<span data-ttu-id="53550-p101">Die **Children** -Eigenschaft enthält eine **Members** -Auflistung, für die das aktuelle **Member** -Objekt das in der Hierarchie übergeordnete Objekt ist. **Member** -Objekte auf Blattebene haben keine untergeordneten Elemente in der **Members** -Auflistung. Diese Eigenschaft wird nur für **Member** -Objekte unterstützt, die zu einem [Level](level-object-ado-md.md)-Objekt gehören. Wenn auf diese Eigenschaft durch **Member** -Objekte verwiesen wird, die zu einem [Position](position-object-ado-md.md)-Objekt gehören, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="53550-p101">The **Children** property contains a **Members** collection for which the current **Member** is the hierarchical parent. Leaf level **Member** objects have no child members in the **Members** collection. This property is only supported on **Member** objects belonging to a [Level](level-object-ado-md.md) object. An error occurs when this property is referenced from **Member** objects belonging to a [Position](position-object-ado-md.md) object.</span></span>

