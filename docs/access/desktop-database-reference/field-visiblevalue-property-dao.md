---
title: Field.VisibleValue-Eigenschaft (DAO)
TOCTitle: VisibleValue Property
ms:assetid: e40fcb43-9a1d-69e7-1544-8f15ef21daf4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835776(v=office.15)
ms:contentKeyID: 48548332
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 461b8c43bf9000e5ecde3a3676cebf54be8e4166
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927571"
---
# <a name="fieldvisiblevalue-property-dao"></a><span data-ttu-id="cd120-102">Field.VisibleValue-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="cd120-102">Field.VisibleValue property (DAO)</span></span>


<span data-ttu-id="cd120-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cd120-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="cd120-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd120-104">Syntax</span></span>

<span data-ttu-id="cd120-105">*Ausdruck* . VisibleValue</span><span class="sxs-lookup"><span data-stu-id="cd120-105">*expression* .VisibleValue</span></span>

<span data-ttu-id="cd120-106">*Ausdruck* Eine Variable, die ein **Field** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="cd120-106">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd120-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cd120-107">Remarks</span></span>

<span data-ttu-id="cd120-p101">Diese Eigenschaft enthält den Wert des Felds, der sich aktuell in der Datenbank auf dem Server befindet. Bei einer optimistischen Batchaktualisierung kann ein Konflikt auftreten, wenn ein zweiter Client dasselbe Feld und denselben Datensatz in dem Zeitraum ändert, in dem der erste Client die Daten abruft und versucht, die Daten zu aktualisieren. Wenn dies geschieht, kann auf den Wert, den der zweite Client festgelegt hat, über diese Eigenschaft zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="cd120-p101">This property contains the value of the field that is currently in the database on the server. During an optimistic batch update, a collision may occur where a second client modified the same field and record in between the time the first client retrieved the data and the first client's update attempt. When this happens, the value that the second client set will be accessible through this property.</span></span>

