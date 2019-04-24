---
title: Field. VisibleValue-Eigenschaft (DAO)
TOCTitle: VisibleValue Property
ms:assetid: e40fcb43-9a1d-69e7-1544-8f15ef21daf4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835776(v=office.15)
ms:contentKeyID: 48548332
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1b3e1b6ec6cd34112f0ba1d84101390bbd400f82
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292916"
---
# <a name="fieldvisiblevalue-property-dao"></a><span data-ttu-id="14778-102">Field. VisibleValue-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="14778-102">Field.VisibleValue property (DAO)</span></span>


<span data-ttu-id="14778-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="14778-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="14778-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="14778-104">Syntax</span></span>

<span data-ttu-id="14778-105">*Ausdruck* . VisibleValue</span><span class="sxs-lookup"><span data-stu-id="14778-105">*expression* .VisibleValue</span></span>

<span data-ttu-id="14778-106">*Ausdruck* Eine Variable, die ein **Field** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="14778-106">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="14778-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="14778-107">Remarks</span></span>

<span data-ttu-id="14778-p101">Diese Eigenschaft enthält den Wert des Felds, der sich aktuell in der Datenbank auf dem Server befindet. Bei einer optimistischen Batchaktualisierung können Konflikte auftreten, wenn in der Zeitspanne, in der ein erster Client Daten abruft und eine Aktualisierung versucht, ein zweiter Client dasselbe Feld und den Datensatz ändert. In diesem Fall kann über diese Eigenschaft auf den vom zweiten Client festgelegten Wert zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="14778-p101">This property contains the value of the field that is currently in the database on the server. During an optimistic batch update, a collision may occur where a second client modified the same field and record in between the time the first client retrieved the data and the first client's update attempt. When this happens, the value that the second client set will be accessible through this property.</span></span>

