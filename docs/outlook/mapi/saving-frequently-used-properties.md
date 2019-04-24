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
ms.openlocfilehash: e32ed3388e95d32a4857a933fb735d170dd71688
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283107"
---
# <a name="saving-frequently-used-properties"></a><span data-ttu-id="2abe8-103">Speichern häufig verwendeter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2abe8-103">Saving Frequently Used Properties</span></span>

  
  
<span data-ttu-id="2abe8-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2abe8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2abe8-105">Verbessern Sie die Leistung, indem Sie Daten speichern, die Zeit und Ressourcen zum Abrufen benötigen und häufig auf Sie zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="2abe8-105">Improve performance by storing data that takes time and resources to retrieve and is accessed frequently.</span></span> <span data-ttu-id="2abe8-106">Die Verwendung von zusätzlichem Arbeitsspeicher kann manchmal eine bessere Option für wiederholte Abrufe sein.</span><span class="sxs-lookup"><span data-stu-id="2abe8-106">Using extra memory can sometimes be a better option that repeated retrievals.</span></span> <span data-ttu-id="2abe8-107">Verwenden Sie beim Erstellen eines Caches zum Speichern dieser Daten Vorsicht und Sorgfalt.</span><span class="sxs-lookup"><span data-stu-id="2abe8-107">Use caution and care when creating a cache for storing this data.</span></span> <span data-ttu-id="2abe8-108">Beachten Sie, dass ein schlecht entworfener Cache sich negativ auf die Leistung auswirken kann.</span><span class="sxs-lookup"><span data-stu-id="2abe8-108">Keep in mind that a poorly designed cache can negatively impact performance.</span></span>
  
<span data-ttu-id="2abe8-109">Beispielsweise müssen die meisten IPM-Clients (zwischen Personen) die IPM-Unterstruktur von Ordnern während einer typischen Sitzung mehrmals anzeigen und öffnen.</span><span class="sxs-lookup"><span data-stu-id="2abe8-109">For example, most interpersonal message (IPM) clients need to display and open the IPM subtree of folders many times during a typical session.</span></span> <span data-ttu-id="2abe8-110">Sie können die Leistung verbessern, indem Sie die Eintrags-IDs für jeden dieser Ordner speichern.</span><span class="sxs-lookup"><span data-stu-id="2abe8-110">You can improve performance by storing the entry identifiers for each of these folders.</span></span> 
  

