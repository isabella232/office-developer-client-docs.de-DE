---
title: Field. OriginalValue-Eigenschaft (DAO)
TOCTitle: OriginalValue Property
ms:assetid: 69ccec1e-311f-6905-e7bb-ad7fa8277494
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195384(v=office.15)
ms:contentKeyID: 48545418
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 95c2776e04497a1ac7f645659c7acc5d9eee2a63
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293000"
---
# <a name="fieldoriginalvalue-property-dao"></a><span data-ttu-id="e1d2f-102">Field. OriginalValue-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="e1d2f-102">Field.OriginalValue property (DAO)</span></span>


<span data-ttu-id="e1d2f-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e1d2f-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="e1d2f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1d2f-104">Syntax</span></span>

<span data-ttu-id="e1d2f-105">*Ausdruck* . OriginalValue</span><span class="sxs-lookup"><span data-stu-id="e1d2f-105">*expression* .OriginalValue</span></span>

<span data-ttu-id="e1d2f-106">*Ausdruck* Eine Variable, die ein **Field** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="e1d2f-106">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1d2f-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e1d2f-107">Remarks</span></span>

<span data-ttu-id="e1d2f-p101">During an optimistic batch update, a collision may occur where a second client modifies the same field and record in between the time the first client retrieves the data and the first client's update attempt. The **OriginalValue** property contains the value of the field at the time the last batch **Update** began. If this value does not match the value actually in the database when the batch **Update** attempts to write to the database, a collision occurs. When this happens, the new value in the database will be accessible through the **[VisibleValue](field-visiblevalue-property-dao.md)** property.</span><span class="sxs-lookup"><span data-stu-id="e1d2f-p101">During an optimistic batch update, a collision may occur where a second client modifies the same field and record in between the time the first client retrieves the data and the first client's update attempt. The **OriginalValue** property contains the value of the field at the time the last batch **Update** began. If this value does not match the value actually in the database when the batch **Update** attempts to write to the database, a collision occurs. When this happens, the new value in the database will be accessible through the **[VisibleValue](field-visiblevalue-property-dao.md)** property.</span></span>

