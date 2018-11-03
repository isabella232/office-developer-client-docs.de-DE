---
title: Ordinal-Eigenschaft (ADO MD Position)
TOCTitle: Ordinal property (ADO MD Position)
ms:assetid: fb132ab5-d2b5-317d-e885-5e37ddaf90fb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250284(v=office.15)
ms:contentKeyID: 48548861
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: abf355cc4d066604035fddbbe8f8a428d8c7a6b0
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944781"
---
# <a name="ordinal-property-ado-md-position"></a><span data-ttu-id="b50c4-102">Ordinal-Eigenschaft (ADO MD Position)</span><span class="sxs-lookup"><span data-stu-id="b50c4-102">Ordinal property (ADO MD Position)</span></span>


<span data-ttu-id="b50c4-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b50c4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b50c4-104">Identifiziert eindeutig eine Position auf einer Achse.</span><span class="sxs-lookup"><span data-stu-id="b50c4-104">Uniquely identifies a position along an axis.</span></span>

## <a name="return-values"></a><span data-ttu-id="b50c4-105">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="b50c4-105">Return values</span></span>

<span data-ttu-id="b50c4-106">Gibt einen schreibgeschützten, ganzzahligen **Long** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b50c4-106">Returns a **Long** integer and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="b50c4-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b50c4-107">Remarks</span></span>

<span data-ttu-id="b50c4-108">Die **Ordinal** -Eigenschaft eines [Position](position-object-ado-md.md)-Objekts entspricht dem Index des **Position** -Objekts innerhalb der [Positions](positions-collection-ado-md.md)-Auflistung.</span><span class="sxs-lookup"><span data-stu-id="b50c4-108">The **Ordinal** of a [Position](position-object-ado-md.md) object corresponds to the index of the **Position** within the [Positions](positions-collection-ado-md.md) collection.</span></span>

<span data-ttu-id="b50c4-109">Eine Zelle kann auf einfache Weise abgerufen werden, indem Sie die **Ordinal** -Eigenschaft des **Position** -Objekts entlang jeder Achse mit der [Item](item-property-ado-md-cellset.md)-Eigenschaft des [Cellset](cellset-object-ado-md.md)-Objekts verwenden.</span><span class="sxs-lookup"><span data-stu-id="b50c4-109">A cell can quickly be retrieved using the **Ordinal** of the **Position** along each axis with the [Item](item-property-ado-md-cellset.md) property of the [Cellset](cellset-object-ado-md.md) object.</span></span>

