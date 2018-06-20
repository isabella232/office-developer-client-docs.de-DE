---
title: Sortieren von Tabellen nach dem Festlegen der Spalten und Einschränkungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57db0314-1df0-4fd2-b443-223b0512f1ad
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9e75143cb59e782993b9a7f9937432f0b4894d5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795611"
---
# <a name="sorting-tables-after-setting-columns-and-restrictions"></a><span data-ttu-id="5ab59-103">Sortieren von Tabellen nach dem Festlegen der Spalten und Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="5ab59-103">Sorting Tables After Setting Columns and Restrictions</span></span>

  
  
<span data-ttu-id="5ab59-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5ab59-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5ab59-105">Wenn Sie die Ansicht einer sortierten Tabelle einschränken müssen, stellen Sie die folgenden **IMAPITable** Anrufe immer in der folgenden Reihenfolge:</span><span class="sxs-lookup"><span data-stu-id="5ab59-105">When you need to limit the view of a sorted table, always make the following **IMAPITable** calls in the following order:</span></span> 
  
1. <span data-ttu-id="5ab59-106">[IMAPITable::SetColumns](imapitable-setcolumns.md) zum Definieren der Spalte festlegen.</span><span class="sxs-lookup"><span data-stu-id="5ab59-106">[IMAPITable::SetColumns](imapitable-setcolumns.md) to define the column set.</span></span> 
    
2. <span data-ttu-id="5ab59-107">[Methode IMAPITable:: Restrict](imapitable-restrict.md) auf die Einschränkung zugrunde liegen.</span><span class="sxs-lookup"><span data-stu-id="5ab59-107">[IMAPITable::Restrict](imapitable-restrict.md) to impose the restriction.</span></span> 
    
3. <span data-ttu-id="5ab59-108">[SortTable](imapitable-sorttable.md) , um die Sortierung durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="5ab59-108">[IMAPITable::SortTable](imapitable-sorttable.md) to perform the sort.</span></span> 
    
<span data-ttu-id="5ab59-109">Wenn die sortierte Tabelle kategorisiert wird, rufen Sie [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md), falls erforderlich, nach dem Aufruf der **SortTable** .</span><span class="sxs-lookup"><span data-stu-id="5ab59-109">If the sorted table is categorized, make a call to [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md), if necessary, after the **SortTable** call.</span></span> <span data-ttu-id="5ab59-110">Diese Reihenfolge von Anrufen ist wichtig, da die meisten Dienstanbieter eine Tabelle sortiert werden als die letzte Aufgabe aus, um die beste Leistung zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="5ab59-110">This ordering of calls is important because most service providers sort a table as the last task to achieve the best performance.</span></span> <span data-ttu-id="5ab59-111">Wenn beispielsweise eine Nachricht Speicheranbieter ein Ordner Inhaltstabelle kategorisieren muss, bevor eine Einschränkung auferlegt werden kann, werden diese Kategorisierung während der Verarbeitung der Einschränkung entfernt.</span><span class="sxs-lookup"><span data-stu-id="5ab59-111">If, for example, a message store provider must categorize a folder contents table before a restriction can be imposed, this categorization will be removed during the processing of the restriction.</span></span> <span data-ttu-id="5ab59-112">Eine zweite Kategorisierung werden erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5ab59-112">A second categorization will be necessary.</span></span> 
  

