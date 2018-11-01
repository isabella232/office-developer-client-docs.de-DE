---
title: TableDef.LastUpdated Property (DAO)
TOCTitle: LastUpdated Property
ms:assetid: fafe54e2-2cf0-5874-92b9-6e20a65e77ef
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837164(v=office.15)
ms:contentKeyID: 48548859
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 10d0203bd30c2e03f7cd2aaa761ac1cf76b12f94
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870863"
---
# <a name="tabledeflastupdated-property-dao"></a><span data-ttu-id="05cb9-102">TableDef.LastUpdated Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="05cb9-102">TableDef.LastUpdated Property (DAO)</span></span>


<span data-ttu-id="05cb9-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="05cb9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="05cb9-p101">Gibt das Datum und die Uhrzeit der letzten Änderung eines Objekts zurück. Schreibgeschützter **Variant**-Wert.</span><span class="sxs-lookup"><span data-stu-id="05cb9-p101">Returns the date and time of the most recent change made to an object. Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="05cb9-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="05cb9-106">Syntax</span></span>

<span data-ttu-id="05cb9-107">*Ausdruck* . LastUpdated</span><span class="sxs-lookup"><span data-stu-id="05cb9-107">*expression* .LastUpdated</span></span>

<span data-ttu-id="05cb9-108">*Ausdruck* Eine Variable, die ein **TableDef** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="05cb9-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="05cb9-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="05cb9-109">Remarks</span></span>

<span data-ttu-id="05cb9-p102">DateCreated und LastUpdated geben das Datum und die Uhrzeit der Erstellung oder der letzen Aktualisierung des Objekts zurück. In einer Mehrbenutzerumgebung sollten Benutzer diese Einstellungen direkt vom Dateiserver erhalten, um Diskrepanzen bei den Einstellungen der Eigenschaften DateCreated und LastUpdated zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="05cb9-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

