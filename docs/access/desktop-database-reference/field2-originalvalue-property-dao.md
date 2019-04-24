---
title: Field2. OriginalValue-Eigenschaft (DAO)
TOCTitle: OriginalValue Property
ms:assetid: 10fed55e-c938-2ae6-8fd2-996745a63da3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845353(v=office.15)
ms:contentKeyID: 48543306
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101183
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 3e3da5f7438ae83010c6ecc109dccf5d7a8eb9ef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292741"
---
# <a name="field2originalvalue-property-dao"></a><span data-ttu-id="8a05c-102">Field2. OriginalValue-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="8a05c-102">Field2.OriginalValue property (DAO)</span></span>


<span data-ttu-id="8a05c-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8a05c-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="8a05c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a05c-104">Syntax</span></span>

<span data-ttu-id="8a05c-105">*Ausdruck* . OriginalValue</span><span class="sxs-lookup"><span data-stu-id="8a05c-105">*expression* .OriginalValue</span></span>

<span data-ttu-id="8a05c-106">*Ausdruck* Eine Variable, die ein **Field2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="8a05c-106">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a05c-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8a05c-107">Remarks</span></span>

<span data-ttu-id="8a05c-p101">Bei einer optimistischen Batchaktualisierung können Konflikte auftreten, wenn in der Zeitspanne, in der ein erster Client Daten abruft und eine Aktualisierung versucht, ein zweiter Client dasselbe Feld und den Datensatz ändert. Die **OriginalValue**-Eigenschaft enthält den Wert des Felds zu dem Zeitpunkt, zu dem der **Update**-Batchvorgang begann. Falls dieser Wert nicht mit dem tatsächlich in der Datenbank vorhandenen Wert übereinstimmt, während der **Update**-Batchvorgang versucht, Daten in die Datenbank zu schreiben, tritt ein Konflikt auf. In diesem Fall kann mithilfe der **VisibleValue**-Eigenschaft auf den neuen Wert in der Datenbank zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="8a05c-p101">During an optimistic batch update, a collision may occur where a second client modifies the same field and record in between the time the first client retrieves the data and the first client's update attempt. The **OriginalValue** property contains the value of the field at the time the last batch **Update** began. If this value does not match the value actually in the database when the batch **Update** attempts to write to the database, a collision occurs. When this happens, the new value in the database will be accessible through the **VisibleValue** property.</span></span>

