---
title: Speichern von häufig verwendete Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a8d4d575-7aa0-4542-91e2-322a6e400551
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a5fa4510f0bcad69bc17b8ac19433f66ec763fba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795416"
---
# <a name="saving-frequently-used-properties"></a><span data-ttu-id="927e2-103">Speichern von häufig verwendete Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="927e2-103">Saving Frequently Used Properties</span></span>

  
  
<span data-ttu-id="927e2-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="927e2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="927e2-105">Verbessern der Leistung durch das Speichern von Daten, die Zeit und Ressourcen zum Abrufen und häufig zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="927e2-105">Improve performance by storing data that takes time and resources to retrieve and is accessed frequently.</span></span> <span data-ttu-id="927e2-106">Verwenden zusätzlichen Arbeitsspeicher kann in einigen Fällen eine bessere Option sein, die Abrufe wiederholt.</span><span class="sxs-lookup"><span data-stu-id="927e2-106">Using extra memory can sometimes be a better option that repeated retrievals.</span></span> <span data-ttu-id="927e2-107">Verwenden Sie Vorsicht und Versorgung, wenn einen Cache zum Speichern von Daten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="927e2-107">Use caution and care when creating a cache for storing this data.</span></span> <span data-ttu-id="927e2-108">Denken Sie daran, dass eine schlecht Cache konzipiert kann die Leistung beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="927e2-108">Keep in mind that a poorly designed cache can negatively impact performance.</span></span>
  
<span data-ttu-id="927e2-109">Beispielsweise müssen am häufigsten zwischen Personen Nachricht (IPM)-Clients zum Anzeigen und öffnen Sie die IPM-Unterstruktur von Ordnern oft während einer normalen Sitzung.</span><span class="sxs-lookup"><span data-stu-id="927e2-109">For example, most interpersonal message (IPM) clients need to display and open the IPM subtree of folders many times during a typical session.</span></span> <span data-ttu-id="927e2-110">Sie können die Leistung verbessern, indem die Eintrags-IDs für jedes dieser Ordner speichern.</span><span class="sxs-lookup"><span data-stu-id="927e2-110">You can improve performance by storing the entry identifiers for each of these folders.</span></span> 
  

