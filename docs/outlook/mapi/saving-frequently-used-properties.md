---
title: Speichern häufig verwendeter Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a8d4d575-7aa0-4542-91e2-322a6e400551
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5ef0da0c617bffc3820c7cd43f66ea07be2ad4a9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580460"
---
# <a name="saving-frequently-used-properties"></a><span data-ttu-id="eebd9-103">Speichern häufig verwendeter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="eebd9-103">Saving Frequently Used Properties</span></span>

  
  
<span data-ttu-id="eebd9-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eebd9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eebd9-105">Verbessern der Leistung durch das Speichern von Daten, die Zeit und Ressourcen zum Abrufen und häufig zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="eebd9-105">Improve performance by storing data that takes time and resources to retrieve and is accessed frequently.</span></span> <span data-ttu-id="eebd9-106">Verwenden zusätzlichen Arbeitsspeicher kann in einigen Fällen eine bessere Option sein, die Abrufe wiederholt.</span><span class="sxs-lookup"><span data-stu-id="eebd9-106">Using extra memory can sometimes be a better option that repeated retrievals.</span></span> <span data-ttu-id="eebd9-107">Verwenden Sie Vorsicht und Versorgung, wenn einen Cache zum Speichern von Daten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="eebd9-107">Use caution and care when creating a cache for storing this data.</span></span> <span data-ttu-id="eebd9-108">Denken Sie daran, dass eine schlecht Cache konzipiert kann die Leistung beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="eebd9-108">Keep in mind that a poorly designed cache can negatively impact performance.</span></span>
  
<span data-ttu-id="eebd9-109">Beispielsweise müssen am häufigsten zwischen Personen Nachricht (IPM)-Clients zum Anzeigen und öffnen Sie die IPM-Unterstruktur von Ordnern oft während einer normalen Sitzung.</span><span class="sxs-lookup"><span data-stu-id="eebd9-109">For example, most interpersonal message (IPM) clients need to display and open the IPM subtree of folders many times during a typical session.</span></span> <span data-ttu-id="eebd9-110">Sie können die Leistung verbessern, indem die Eintrags-IDs für jedes dieser Ordner speichern.</span><span class="sxs-lookup"><span data-stu-id="eebd9-110">You can improve performance by storing the entry identifiers for each of these folders.</span></span> 
  

