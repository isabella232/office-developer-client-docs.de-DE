---
title: Field.OriginalValue Property (DAO)
TOCTitle: OriginalValue Property
ms:assetid: 69ccec1e-311f-6905-e7bb-ad7fa8277494
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195384(v=office.15)
ms:contentKeyID: 48545418
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ead15a227ccd3ff7d77796aea4d23d776652be86
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873068"
---
# <a name="fieldoriginalvalue-property-dao"></a><span data-ttu-id="6150c-102">Field.OriginalValue Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="6150c-102">Field.OriginalValue Property (DAO)</span></span>


<span data-ttu-id="6150c-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6150c-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="6150c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6150c-104">Syntax</span></span>

<span data-ttu-id="6150c-105">*Ausdruck* . OriginalValue</span><span class="sxs-lookup"><span data-stu-id="6150c-105">*expression* .OriginalValue</span></span>

<span data-ttu-id="6150c-106">*Ausdruck* Eine Variable, die ein **Field** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="6150c-106">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6150c-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6150c-107">Remarks</span></span>

<span data-ttu-id="6150c-108">Bei einer optimistischen Batchaktualisierung können Konflikte auftreten, wenn in der Zeitspanne, in der ein erster Client Daten abruft und eine Aktualisierung versucht, ein zweiter Client dasselbe Feld und den Datensatz ändert.</span><span class="sxs-lookup"><span data-stu-id="6150c-108">During an optimistic batch update, a collision may occur where a second client modifies the same field and record in between the time the first client retrieves the data and the first client's update attempt.</span></span> <span data-ttu-id="6150c-109">Die **OriginalValue**-Eigenschaft enthält den Wert des Felds zu dem Zeitpunkt, zu dem der **Update**-Batchvorgang begann.</span><span class="sxs-lookup"><span data-stu-id="6150c-109">The **OriginalValue** property contains the value of the field at the time the last batch **Update** began.</span></span> <span data-ttu-id="6150c-110">Falls dieser Wert nicht mit dem tatsächlich in der Datenbank vorhandenen Wert übereinstimmt, während der **Update**-Batchvorgang versucht, Daten in die Datenbank zu schreiben, tritt ein Konflikt auf.</span><span class="sxs-lookup"><span data-stu-id="6150c-110">If this value does not match the value actually in the database when the batch **Update** attempts to write to the database, a collision occurs.</span></span> <span data-ttu-id="6150c-111">In diesem Fall werden der neue Wert in der Datenbank über die **[VisibleValue](field-visiblevalue-property-dao.md)** -Eigenschaft zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="6150c-111">When this happens, the new value in the database will be accessible through the **[VisibleValue](field-visiblevalue-property-dao.md)** property.</span></span>

