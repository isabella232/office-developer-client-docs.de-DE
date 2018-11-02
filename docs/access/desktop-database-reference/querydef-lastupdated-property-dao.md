---
title: QueryDef.LastUpdated-Eigenschaft (DAO)
TOCTitle: LastUpdated Property
ms:assetid: 3b7818d4-054e-54e2-bf63-58b340bb4a90
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192665(v=office.15)
ms:contentKeyID: 48544287
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 98bb600e6f3f1c9587eca110269e8b6b3765e40f
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921271"
---
# <a name="querydeflastupdated-property-dao"></a><span data-ttu-id="4c068-102">QueryDef.LastUpdated-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="4c068-102">QueryDef.LastUpdated property (DAO)</span></span>


<span data-ttu-id="4c068-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4c068-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4c068-p101">Gibt das Datum und die Uhrzeit der letzten Änderung eines Objekts zurück. Schreibgeschützter **Variant**-Wert.</span><span class="sxs-lookup"><span data-stu-id="4c068-p101">Returns the date and time of the most recent change made to an object. Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c068-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4c068-106">Syntax</span></span>

<span data-ttu-id="4c068-107">*Ausdruck* . LastUpdated</span><span class="sxs-lookup"><span data-stu-id="4c068-107">*expression* .LastUpdated</span></span>

<span data-ttu-id="4c068-108">*Ausdruck* Eine Variable, die ein **QueryDef** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="4c068-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c068-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4c068-109">Remarks</span></span>

<span data-ttu-id="4c068-p102">DateCreated und LastUpdated geben das Datum und die Uhrzeit der Erstellung oder der letzen Aktualisierung des Objekts zurück. In einer Mehrbenutzerumgebung sollten Benutzer diese Einstellungen direkt vom Dateiserver erhalten, um Diskrepanzen bei den Einstellungen der Eigenschaften DateCreated und LastUpdated zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="4c068-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

