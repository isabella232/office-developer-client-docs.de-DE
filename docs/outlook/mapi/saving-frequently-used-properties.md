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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424553"
---
# <a name="saving-frequently-used-properties"></a><span data-ttu-id="c8255-103">Speichern häufig verwendeter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c8255-103">Saving Frequently Used Properties</span></span>

  
  
<span data-ttu-id="c8255-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c8255-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c8255-105">Verbessern Sie die Leistung, indem Sie Daten speichern, die Zeit und Ressourcen zum Abrufen benötigten und häufig aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c8255-105">Improve performance by storing data that takes time and resources to retrieve and is accessed frequently.</span></span> <span data-ttu-id="c8255-106">Die Verwendung von zusätzlichem Arbeitsspeicher kann manchmal eine bessere Option sein, wenn wiederholte Abrufe verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c8255-106">Using extra memory can sometimes be a better option that repeated retrievals.</span></span> <span data-ttu-id="c8255-107">Verwenden Sie beim Erstellen eines Caches zum Speichern dieser Daten Vorsicht und Vorsicht.</span><span class="sxs-lookup"><span data-stu-id="c8255-107">Use caution and care when creating a cache for storing this data.</span></span> <span data-ttu-id="c8255-108">Beachten Sie, dass sich ein schlecht entworfener Cache negativ auf die Leistung auswirken kann.</span><span class="sxs-lookup"><span data-stu-id="c8255-108">Keep in mind that a poorly designed cache can negatively impact performance.</span></span>
  
<span data-ttu-id="c8255-109">Die meisten clients interpersonal message (IPM) müssen z. B. die IPM-Unterstruktur von Ordnern während einer typischen Sitzung mehrmals anzeigen und öffnen.</span><span class="sxs-lookup"><span data-stu-id="c8255-109">For example, most interpersonal message (IPM) clients need to display and open the IPM subtree of folders many times during a typical session.</span></span> <span data-ttu-id="c8255-110">Sie können die Leistung verbessern, indem Sie die Eintragsbezeichner für jeden dieser Ordner speichern.</span><span class="sxs-lookup"><span data-stu-id="c8255-110">You can improve performance by storing the entry identifiers for each of these folders.</span></span> 
  

