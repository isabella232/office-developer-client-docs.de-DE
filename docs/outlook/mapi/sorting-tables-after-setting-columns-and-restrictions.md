---
title: Sortieren von Tabellen nach dem Festlegen von Spalten und Einschränkungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57db0314-1df0-4fd2-b443-223b0512f1ad
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 62220794f325165e67db5397da2795d49959ef60
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344485"
---
# <a name="sorting-tables-after-setting-columns-and-restrictions"></a><span data-ttu-id="4d804-103">Sortieren von Tabellen nach dem Festlegen von Spalten und Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="4d804-103">Sorting Tables After Setting Columns and Restrictions</span></span>

  
  
<span data-ttu-id="4d804-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4d804-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4d804-105">Wenn Sie die Ansicht einer sortierten Tabelle einschränken müssen, führen Sie die folgenden **IMAPITable** -Aufrufe in der folgenden Reihenfolge aus:</span><span class="sxs-lookup"><span data-stu-id="4d804-105">When you need to limit the view of a sorted table, always make the following **IMAPITable** calls in the following order:</span></span> 
  
1. <span data-ttu-id="4d804-106">[IMAPITable::](imapitable-setcolumns.md) SetColumns zum Definieren des Spaltensatzes.</span><span class="sxs-lookup"><span data-stu-id="4d804-106">[IMAPITable::SetColumns](imapitable-setcolumns.md) to define the column set.</span></span> 
    
2. <span data-ttu-id="4d804-107">[IMAPITable:: einschränken](imapitable-restrict.md) , um die Einschränkung aufzuerlegen.</span><span class="sxs-lookup"><span data-stu-id="4d804-107">[IMAPITable::Restrict](imapitable-restrict.md) to impose the restriction.</span></span> 
    
3. <span data-ttu-id="4d804-108">[IMAPITable:: sortable](imapitable-sorttable.md) , um die Sortierung durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="4d804-108">[IMAPITable::SortTable](imapitable-sorttable.md) to perform the sort.</span></span> 
    
<span data-ttu-id="4d804-109">Wenn die sortierte Tabelle kategorisiert wird, führen Sie einen Aufruf von [IMAPITable:: SetCollapseState](imapitable-setcollapsestate.md), falls erforderlich, nach dem **sortable** -Aufruf aus.</span><span class="sxs-lookup"><span data-stu-id="4d804-109">If the sorted table is categorized, make a call to [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md), if necessary, after the **SortTable** call.</span></span> <span data-ttu-id="4d804-110">Diese Reihenfolge von anrufen ist wichtig, da die meisten Dienstanbieter eine Tabelle als letzte Aufgabe sortieren, um eine optimale Leistung zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="4d804-110">This ordering of calls is important because most service providers sort a table as the last task to achieve the best performance.</span></span> <span data-ttu-id="4d804-111">Wenn beispielsweise ein Nachrichtenspeicher Anbieter eine Ordnerinhaltstabelle kategorisieren muss, bevor eine Einschränkung auferlegt werden kann, wird diese Kategorisierung während der Verarbeitung der Einschränkung entfernt.</span><span class="sxs-lookup"><span data-stu-id="4d804-111">If, for example, a message store provider must categorize a folder contents table before a restriction can be imposed, this categorization will be removed during the processing of the restriction.</span></span> <span data-ttu-id="4d804-112">Eine zweite Kategorisierung ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4d804-112">A second categorization will be necessary.</span></span> 
  

