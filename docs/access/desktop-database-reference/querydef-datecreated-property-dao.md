---
title: QueryDef.DateCreated Property (DAO)
TOCTitle: DateCreated Property
ms:assetid: f7585b34-8314-fb9f-daa6-cd1a8ad59d91
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836910(v=office.15)
ms:contentKeyID: 48548763
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2d770decd0bf023a9c2ad8699a8aca4686d73491
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875413"
---
# <a name="querydefdatecreated-property-dao"></a><span data-ttu-id="b3a4e-102">QueryDef.DateCreated Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="b3a4e-102">QueryDef.DateCreated Property (DAO)</span></span>


<span data-ttu-id="b3a4e-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b3a4e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b3a4e-p101">Gibt das Datum und die Uhrzeit der Objekterstellung zurück (nur Microsoft Access-Arbeitsbereiche). Schreibgeschützter **Variant**-Wert.</span><span class="sxs-lookup"><span data-stu-id="b3a4e-p101">Returns the date and time that an object was created (Microsoft Access workspaces only). Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3a4e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3a4e-106">Syntax</span></span>

<span data-ttu-id="b3a4e-107">*Ausdruck* . DateCreated</span><span class="sxs-lookup"><span data-stu-id="b3a4e-107">*expression* .DateCreated</span></span>

<span data-ttu-id="b3a4e-108">*Ausdruck* Eine Variable, die ein **QueryDef** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="b3a4e-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3a4e-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b3a4e-109">Remarks</span></span>

<span data-ttu-id="b3a4e-p102">DateCreated und LastUpdated geben das Datum und die Uhrzeit der Erstellung oder der letzen Aktualisierung des Objekts zurück. In einer Mehrbenutzerumgebung sollten Benutzer diese Einstellungen direkt vom Dateiserver erhalten, um Diskrepanzen bei den Einstellungen der Eigenschaften DateCreated und LastUpdated zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="b3a4e-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

