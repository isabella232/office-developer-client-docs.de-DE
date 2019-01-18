---
title: Field.OriginalValue-Eigenschaft (DAO)
TOCTitle: OriginalValue Property
ms:assetid: 69ccec1e-311f-6905-e7bb-ad7fa8277494
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195384(v=office.15)
ms:contentKeyID: 48545418
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 95c2776e04497a1ac7f645659c7acc5d9eee2a63
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715963"
---
# <a name="fieldoriginalvalue-property-dao"></a><span data-ttu-id="6df96-102">Field.OriginalValue-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="6df96-102">Field.OriginalValue property (DAO)</span></span>


<span data-ttu-id="6df96-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6df96-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="6df96-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6df96-104">Syntax</span></span>

<span data-ttu-id="6df96-105">*Ausdruck* . OriginalValue</span><span class="sxs-lookup"><span data-stu-id="6df96-105">*expression* .OriginalValue</span></span>

<span data-ttu-id="6df96-106">*Ausdruck* Eine Variable, die ein **Field** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="6df96-106">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6df96-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6df96-107">Remarks</span></span>

<span data-ttu-id="6df96-108">Bei einer optimistischen Batchaktualisierung können Konflikte auftreten, wenn in der Zeitspanne, in der ein erster Client Daten abruft und eine Aktualisierung versucht, ein zweiter Client dasselbe Feld und den Datensatz ändert.</span><span class="sxs-lookup"><span data-stu-id="6df96-108">During an optimistic batch update, a collision may occur where a second client modifies the same field and record in between the time the first client retrieves the data and the first client's update attempt.</span></span> <span data-ttu-id="6df96-109">Die **OriginalValue**-Eigenschaft enthält den Wert des Felds zu dem Zeitpunkt, zu dem der **Update**-Batchvorgang begann.</span><span class="sxs-lookup"><span data-stu-id="6df96-109">The **OriginalValue** property contains the value of the field at the time the last batch **Update** began.</span></span> <span data-ttu-id="6df96-110">Falls dieser Wert nicht mit dem tatsächlich in der Datenbank vorhandenen Wert übereinstimmt, während der **Update**-Batchvorgang versucht, Daten in die Datenbank zu schreiben, tritt ein Konflikt auf.</span><span class="sxs-lookup"><span data-stu-id="6df96-110">If this value does not match the value actually in the database when the batch **Update** attempts to write to the database, a collision occurs.</span></span> <span data-ttu-id="6df96-111">In diesem Fall werden der neue Wert in der Datenbank über die **[VisibleValue](field-visiblevalue-property-dao.md)** -Eigenschaft zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="6df96-111">When this happens, the new value in the database will be accessible through the **[VisibleValue](field-visiblevalue-property-dao.md)** property.</span></span>

