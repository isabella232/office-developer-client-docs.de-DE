---
title: TableDef.LastUpdated-Eigenschaft (DAO)
TOCTitle: LastUpdated Property
ms:assetid: fafe54e2-2cf0-5874-92b9-6e20a65e77ef
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837164(v=office.15)
ms:contentKeyID: 48548859
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 994543132fb5323566bd876da066419d0986bd91
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722774"
---
# <a name="tabledeflastupdated-property-dao"></a><span data-ttu-id="7f96d-102">TableDef.LastUpdated-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="7f96d-102">TableDef.LastUpdated property (DAO)</span></span>


<span data-ttu-id="7f96d-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7f96d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7f96d-p101">Gibt das Datum und die Uhrzeit der letzten Änderung eines Objekts zurück. Schreibgeschützter **Variant**-Wert.</span><span class="sxs-lookup"><span data-stu-id="7f96d-p101">Returns the date and time of the most recent change made to an object. Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f96d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f96d-106">Syntax</span></span>

<span data-ttu-id="7f96d-107">*Ausdruck* . LastUpdated</span><span class="sxs-lookup"><span data-stu-id="7f96d-107">*expression* .LastUpdated</span></span>

<span data-ttu-id="7f96d-108">*Ausdruck* Eine Variable, die ein **TableDef** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="7f96d-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f96d-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7f96d-109">Remarks</span></span>

<span data-ttu-id="7f96d-p102">DateCreated und LastUpdated geben das Datum und die Uhrzeit der Erstellung oder der letzen Aktualisierung des Objekts zurück. In einer Mehrbenutzerumgebung sollten Benutzer diese Einstellungen direkt vom Dateiserver erhalten, um Diskrepanzen bei den Einstellungen der Eigenschaften DateCreated und LastUpdated zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="7f96d-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

