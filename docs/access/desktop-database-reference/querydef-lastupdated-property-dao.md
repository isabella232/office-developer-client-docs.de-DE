---
title: QueryDef. LastUpdated-Eigenschaft (DAO)
TOCTitle: LastUpdated Property
ms:assetid: 3b7818d4-054e-54e2-bf63-58b340bb4a90
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192665(v=office.15)
ms:contentKeyID: 48544287
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1876e92381828075edca3bbfcbae63e706a21365
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303311"
---
# <a name="querydeflastupdated-property-dao"></a><span data-ttu-id="8e1f2-102">QueryDef. LastUpdated-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="8e1f2-102">QueryDef.LastUpdated property (DAO)</span></span>


<span data-ttu-id="8e1f2-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8e1f2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8e1f2-104">Gibt das Datum und die Uhrzeit der letzten Änderung eines Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="8e1f2-104">Returns the date and time of the most recent change made to an object.</span></span> <span data-ttu-id="8e1f2-105">Schreibgeschützter **Variant**-Wert.</span><span class="sxs-lookup"><span data-stu-id="8e1f2-105">Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e1f2-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e1f2-106">Syntax</span></span>

<span data-ttu-id="8e1f2-107">*Ausdruck* . LastUpdated</span><span class="sxs-lookup"><span data-stu-id="8e1f2-107">*expression* .LastUpdated</span></span>

<span data-ttu-id="8e1f2-108">*Ausdruck* Eine Variable, die ein **QueryDef** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="8e1f2-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e1f2-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8e1f2-109">Remarks</span></span>

<span data-ttu-id="8e1f2-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span><span class="sxs-lookup"><span data-stu-id="8e1f2-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

