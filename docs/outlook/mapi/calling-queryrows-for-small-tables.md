---
title: Aufrufen von QueryRows für kleine Tabellen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8c38bb0f-de0b-4d70-9f6d-db652445e137
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8b38dcc485e75f94ccf4f4c3c8c9a57d314465a6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331634"
---
# <a name="calling-queryrows-for-small-tables"></a><span data-ttu-id="8b046-103">Aufrufen von QueryRows für kleine Tabellen</span><span class="sxs-lookup"><span data-stu-id="8b046-103">Calling QueryRows for Small Tables</span></span>

  
  
<span data-ttu-id="8b046-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8b046-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8b046-105">Beim Abrufen von Zeilen aus einer kleinen Tabelle rufen Sie [IMAPITable:: QueryRows](imapitable-queryrows.md) , anstatt zunächst eine Einschränkung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8b046-105">When retrieving rows from a small table, call [IMAPITable::QueryRows](imapitable-queryrows.md) instead of first building a restriction.</span></span> <span data-ttu-id="8b046-106">Das Erstellen einer Einschränkung hat Auswirkungen auf die Leistung, da der Anbieter zunächst eine Tabelle erstellen, die entsprechenden Zeilen in der ursprünglichen Tabelle suchen und dann die Zeilen in die neue Tabelle kopieren muss.</span><span class="sxs-lookup"><span data-stu-id="8b046-106">Creating a restriction impacts performance because the provider must first create a table, find the matching rows in the original table, and then copy the rows to the new table.</span></span> <span data-ttu-id="8b046-107">Wenn die Gesamtanzahl der Zeilen in der Tabelle kleiner als 100 ist, ist es wahrscheinlich effektiver, alle Zeilen zu lesen und dann [IMAPITable:: FindRow](imapitable-findrow.md) aufzurufen, um die entsprechende Zeile zu finden.</span><span class="sxs-lookup"><span data-stu-id="8b046-107">If the total number of rows in the table is less than 100, it is probably more effective to read all of the rows and then call [IMAPITable::FindRow](imapitable-findrow.md) to find the appropriate row.</span></span> <span data-ttu-id="8b046-108">Dies ist eine besonders gute Strategie, wenn diese Informationen nur gelegentlich benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="8b046-108">This is a particularly good strategy if this information is needed only occasionally.</span></span> 
  
<span data-ttu-id="8b046-109">Die richtige Zeit für die Verwendung einer Einschränkung ist, wenn die eingeschränkten oder gefilterten Informationen über einen längeren Zeitraum verwendet oder häufig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8b046-109">The proper time to use a restriction is when the restricted or filtered information will be used over a longer period of time or used frequently.</span></span> <span data-ttu-id="8b046-110">Wenn Sie beispielsweise immer eine Ansicht mit ungelesenen Nachrichten benötigen, ist eine Einschränkung der richtige Aufruf.</span><span class="sxs-lookup"><span data-stu-id="8b046-110">For instance, if you always need a view with unread messages, then a restriction is the proper call to use.</span></span>
  

