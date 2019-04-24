---
title: QueryDef. DateCreated-Eigenschaft (DAO)
TOCTitle: DateCreated Property
ms:assetid: f7585b34-8314-fb9f-daa6-cd1a8ad59d91
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836910(v=office.15)
ms:contentKeyID: 48548763
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a4a120eed6c20db73e1c23f31ea9329d00da2f0d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301071"
---
# <a name="querydefdatecreated-property-dao"></a><span data-ttu-id="5358e-102">QueryDef. DateCreated-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="5358e-102">QueryDef.DateCreated property (DAO)</span></span>


<span data-ttu-id="5358e-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5358e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5358e-104">Gibt das Datum und die Uhrzeit der Objekterstellung zurück (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="5358e-104">Returns the date and time that an object was created (Microsoft Access workspaces only).</span></span> <span data-ttu-id="5358e-105">Schreibgeschützter **Variant**-Wert.</span><span class="sxs-lookup"><span data-stu-id="5358e-105">Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="5358e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="5358e-106">Syntax</span></span>

<span data-ttu-id="5358e-107">*Ausdruck* . DateCreated</span><span class="sxs-lookup"><span data-stu-id="5358e-107">*expression* .DateCreated</span></span>

<span data-ttu-id="5358e-108">*Ausdruck* Eine Variable, die ein **QueryDef** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="5358e-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5358e-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5358e-109">Remarks</span></span>

<span data-ttu-id="5358e-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span><span class="sxs-lookup"><span data-stu-id="5358e-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

