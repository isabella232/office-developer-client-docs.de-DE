---
title: QueryDef.LastUpdated-Eigenschaft (DAO)
TOCTitle: LastUpdated Property
ms:assetid: 3b7818d4-054e-54e2-bf63-58b340bb4a90
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192665(v=office.15)
ms:contentKeyID: 48544287
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1876e92381828075edca3bbfcbae63e706a21365
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712561"
---
# <a name="querydeflastupdated-property-dao"></a><span data-ttu-id="4560a-102">QueryDef.LastUpdated-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="4560a-102">QueryDef.LastUpdated property (DAO)</span></span>


<span data-ttu-id="4560a-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4560a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4560a-p101">Gibt das Datum und die Uhrzeit der letzten Änderung eines Objekts zurück. Schreibgeschützter **Variant**-Wert.</span><span class="sxs-lookup"><span data-stu-id="4560a-p101">Returns the date and time of the most recent change made to an object. Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4560a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4560a-106">Syntax</span></span>

<span data-ttu-id="4560a-107">*Ausdruck* . LastUpdated</span><span class="sxs-lookup"><span data-stu-id="4560a-107">*expression* .LastUpdated</span></span>

<span data-ttu-id="4560a-108">*Ausdruck* Eine Variable, die ein **QueryDef** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="4560a-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4560a-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4560a-109">Remarks</span></span>

<span data-ttu-id="4560a-p102">DateCreated und LastUpdated geben das Datum und die Uhrzeit der Erstellung oder der letzen Aktualisierung des Objekts zurück. In einer Mehrbenutzerumgebung sollten Benutzer diese Einstellungen direkt vom Dateiserver erhalten, um Diskrepanzen bei den Einstellungen der Eigenschaften DateCreated und LastUpdated zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="4560a-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

