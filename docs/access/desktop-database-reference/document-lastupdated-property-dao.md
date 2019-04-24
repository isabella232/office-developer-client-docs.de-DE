---
title: Document. LastUpdated-Eigenschaft (DAO)
TOCTitle: LastUpdated Property
ms:assetid: 9307ceee-095f-0364-fd5b-905bc523b9c0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197661(v=office.15)
ms:contentKeyID: 48546388
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: abb766f7a47cbacaededf65eb2b5e9145bf88c60
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293805"
---
# <a name="documentlastupdated-property-dao"></a><span data-ttu-id="daf3d-102">Document. LastUpdated-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="daf3d-102">Document.LastUpdated property (DAO)</span></span>


<span data-ttu-id="daf3d-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="daf3d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="daf3d-104">Gibt das Datum und die Uhrzeit der letzten Änderung eines Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="daf3d-104">Returns the date and time of the most recent change made to an object.</span></span> <span data-ttu-id="daf3d-105">Schreibgeschützter **Variant**-Wert.</span><span class="sxs-lookup"><span data-stu-id="daf3d-105">Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="daf3d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="daf3d-106">Syntax</span></span>

<span data-ttu-id="daf3d-107">*Ausdruck* . LastUpdated</span><span class="sxs-lookup"><span data-stu-id="daf3d-107">*expression* .LastUpdated</span></span>

<span data-ttu-id="daf3d-108">*Ausdruck* Eine Variable, die ein **Document** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="daf3d-108">*expression* A variable that represents a **Document** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="daf3d-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="daf3d-109">Remarks</span></span>

<span data-ttu-id="daf3d-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span><span class="sxs-lookup"><span data-stu-id="daf3d-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

