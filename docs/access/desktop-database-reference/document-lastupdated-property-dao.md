---
title: Document.LastUpdated Property (DAO)
TOCTitle: LastUpdated Property
ms:assetid: 9307ceee-095f-0364-fd5b-905bc523b9c0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197661(v=office.15)
ms:contentKeyID: 48546388
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f8192dc32554b29c9fe024f34f08757cb512aa5b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475898"
---
# <a name="documentlastupdated-property-dao"></a><span data-ttu-id="651d5-102">Document.LastUpdated Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="651d5-102">Document.LastUpdated Property (DAO)</span></span>


<span data-ttu-id="651d5-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="651d5-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="651d5-p101">Gibt das Datum und die Uhrzeit der letzten Änderung eines Objekts zurück. Schreibgeschützter **Variant**-Wert.</span><span class="sxs-lookup"><span data-stu-id="651d5-p101">Returns the date and time of the most recent change made to an object. Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="651d5-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="651d5-106">Syntax</span></span>

<span data-ttu-id="651d5-107">*Ausdruck* . LastUpdated</span><span class="sxs-lookup"><span data-stu-id="651d5-107">*expression* .LastUpdated</span></span>

<span data-ttu-id="651d5-108">*Ausdruck* Eine Variable, die ein **Document** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="651d5-108">*expression* A variable that represents a **Document** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="651d5-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="651d5-109">Remarks</span></span>

<span data-ttu-id="651d5-p102">DateCreated und LastUpdated geben das Datum und die Uhrzeit der Erstellung oder der letzen Aktualisierung des Objekts zurück. In einer Mehrbenutzerumgebung sollten Benutzer diese Einstellungen direkt vom Dateiserver erhalten, um Diskrepanzen bei den Einstellungen der Eigenschaften DateCreated und LastUpdated zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="651d5-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

