---
title: Field2.VisibleValue-Eigenschaft (DAO)
TOCTitle: VisibleValue Property
ms:assetid: 1e023a1a-fd49-7570-42bd-2f4c06ac5e5e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845809(v=office.15)
ms:contentKeyID: 48543611
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101184
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 9b33fe61eaeb7d1a6006ffaf4566b65be9f68243
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926066"
---
# <a name="field2visiblevalue-property-dao"></a><span data-ttu-id="3a307-102">Field2.VisibleValue-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="3a307-102">Field2.VisibleValue property (DAO)</span></span>


<span data-ttu-id="3a307-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3a307-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="3a307-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a307-104">Syntax</span></span>

<span data-ttu-id="3a307-105">*Ausdruck* . VisibleValue</span><span class="sxs-lookup"><span data-stu-id="3a307-105">*expression* .VisibleValue</span></span>

<span data-ttu-id="3a307-106">*Ausdruck* Eine Variable, die ein **Field2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="3a307-106">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a307-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3a307-107">Remarks</span></span>

<span data-ttu-id="3a307-p101">Diese Eigenschaft enthält den Wert des Felds, der sich aktuell in der Datenbank auf dem Server befindet. Bei einer optimistischen Batchaktualisierung kann ein Konflikt auftreten, wenn ein zweiter Client dasselbe Feld und denselben Datensatz in dem Zeitraum ändert, in dem der erste Client die Daten abruft und versucht, die Daten zu aktualisieren. Wenn dies geschieht, kann auf den Wert, den der zweite Client festgelegt hat, über diese Eigenschaft zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="3a307-p101">This property contains the value of the field that is currently in the database on the server. During an optimistic batch update, a collision may occur where a second client modified the same field and record in between the time the first client retrieved the data and the first client's update attempt. When this happens, the value that the second client set will be accessible through this property.</span></span>

