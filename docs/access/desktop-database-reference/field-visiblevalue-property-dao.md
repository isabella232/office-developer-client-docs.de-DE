---
title: Field.VisibleValue Property (DAO)
TOCTitle: VisibleValue Property
ms:assetid: e40fcb43-9a1d-69e7-1544-8f15ef21daf4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835776(v=office.15)
ms:contentKeyID: 48548332
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 892c7b41a692f353ee7e5bdd2191f6e21b8b4cf2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473407"
---
# <a name="fieldvisiblevalue-property-dao"></a><span data-ttu-id="cba39-102">Field.VisibleValue Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="cba39-102">Field.VisibleValue Property (DAO)</span></span>


<span data-ttu-id="cba39-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="cba39-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="cba39-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cba39-104">Syntax</span></span>

<span data-ttu-id="cba39-105">*Ausdruck* . VisibleValue</span><span class="sxs-lookup"><span data-stu-id="cba39-105">*expression* .VisibleValue</span></span>

<span data-ttu-id="cba39-106">*Ausdruck* Eine Variable, die ein **Field** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="cba39-106">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="cba39-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cba39-107">Remarks</span></span>

<span data-ttu-id="cba39-p101">Diese Eigenschaft enthält den Wert des Felds, der sich aktuell in der Datenbank auf dem Server befindet. Bei einer optimistischen Batchaktualisierung kann ein Konflikt auftreten, wenn ein zweiter Client dasselbe Feld und denselben Datensatz in dem Zeitraum ändert, in dem der erste Client die Daten abruft und versucht, die Daten zu aktualisieren. Wenn dies geschieht, kann auf den Wert, den der zweite Client festgelegt hat, über diese Eigenschaft zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="cba39-p101">This property contains the value of the field that is currently in the database on the server. During an optimistic batch update, a collision may occur where a second client modified the same field and record in between the time the first client retrieved the data and the first client's update attempt. When this happens, the value that the second client set will be accessible through this property.</span></span>

