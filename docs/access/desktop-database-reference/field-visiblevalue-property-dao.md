---
title: Field.VisibleValue-Eigenschaft (DAO)
TOCTitle: VisibleValue Property
ms:assetid: e40fcb43-9a1d-69e7-1544-8f15ef21daf4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835776(v=office.15)
ms:contentKeyID: 48548332
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1b3e1b6ec6cd34112f0ba1d84101390bbd400f82
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712456"
---
# <a name="fieldvisiblevalue-property-dao"></a><span data-ttu-id="40533-102">Field.VisibleValue-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="40533-102">Field.VisibleValue property (DAO)</span></span>


<span data-ttu-id="40533-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="40533-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="40533-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="40533-104">Syntax</span></span>

<span data-ttu-id="40533-105">*Ausdruck* . VisibleValue</span><span class="sxs-lookup"><span data-stu-id="40533-105">*expression* .VisibleValue</span></span>

<span data-ttu-id="40533-106">*Ausdruck* Eine Variable, die ein **Field** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="40533-106">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="40533-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="40533-107">Remarks</span></span>

<span data-ttu-id="40533-p101">Diese Eigenschaft enthält den Wert des Felds, der sich aktuell in der Datenbank auf dem Server befindet. Bei einer optimistischen Batchaktualisierung kann ein Konflikt auftreten, wenn ein zweiter Client dasselbe Feld und denselben Datensatz in dem Zeitraum ändert, in dem der erste Client die Daten abruft und versucht, die Daten zu aktualisieren. Wenn dies geschieht, kann auf den Wert, den der zweite Client festgelegt hat, über diese Eigenschaft zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="40533-p101">This property contains the value of the field that is currently in the database on the server. During an optimistic batch update, a collision may occur where a second client modified the same field and record in between the time the first client retrieved the data and the first client's update attempt. When this happens, the value that the second client set will be accessible through this property.</span></span>

