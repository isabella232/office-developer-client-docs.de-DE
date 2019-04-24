---
title: DbEngine. Version-Eigenschaft (DAO)
TOCTitle: Version Property
ms:assetid: b2807dc1-604f-4423-289a-ff38a3d9f31b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822024(v=office.15)
ms:contentKeyID: 48547171
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052986
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 7e22645127f18ad815c398fd38f9ac4615dfadc9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294190"
---
# <a name="dbengineversion-property-dao"></a><span data-ttu-id="0f98d-102">DbEngine. Version-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="0f98d-102">DBEngine.Version property (DAO)</span></span>


<span data-ttu-id="0f98d-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0f98d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0f98d-104">Gibt die aktuell verwendete DAO-Version zurück.</span><span class="sxs-lookup"><span data-stu-id="0f98d-104">Rreturns the version of DAO currently in use.</span></span> <span data-ttu-id="0f98d-105">Schreibgeschützter **String**-Wert.</span><span class="sxs-lookup"><span data-stu-id="0f98d-105">Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f98d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f98d-106">Syntax</span></span>

<span data-ttu-id="0f98d-107">*Ausdruck* . Version</span><span class="sxs-lookup"><span data-stu-id="0f98d-107">*expression* .Version</span></span>

<span data-ttu-id="0f98d-108">*Ausdruck* Eine Variable, die ein **DBEngine** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="0f98d-108">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f98d-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0f98d-109">Remarks</span></span>

<span data-ttu-id="0f98d-110">Der Rückgabewert ist eine Zeichenfolge, die zu einer Versionsnummer im Format "Major. Minor" ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="0f98d-110">The return value is a String that evaluates to a version number in the form "major.minor".</span></span> <span data-ttu-id="0f98d-111">For example, "3.0".</span><span class="sxs-lookup"><span data-stu-id="0f98d-111">For example, "3.0".</span></span> <span data-ttu-id="0f98d-112">The product version number consists of the version number (3), a period, and the release number (0).</span><span class="sxs-lookup"><span data-stu-id="0f98d-112">The product version number consists of the version number (3), a period, and the release number (0).</span></span>

