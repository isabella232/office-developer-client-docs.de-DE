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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404176"
---
# <a name="calling-queryrows-for-small-tables"></a><span data-ttu-id="4bdda-103">Aufrufen von QueryRows für kleine Tabellen</span><span class="sxs-lookup"><span data-stu-id="4bdda-103">Calling QueryRows for Small Tables</span></span>

  
  
<span data-ttu-id="4bdda-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4bdda-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4bdda-105">Rufen Sie beim Abrufen von Zeilen aus einer kleinen Tabelle [IMAPITable::QueryRows](imapitable-queryrows.md) auf, anstatt zuerst eine Einschränkung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4bdda-105">When retrieving rows from a small table, call [IMAPITable::QueryRows](imapitable-queryrows.md) instead of first building a restriction.</span></span> <span data-ttu-id="4bdda-106">Das Erstellen einer Einschränkung wirkt sich auf die Leistung aus, da der Anbieter zunächst eine Tabelle erstellen, die übereinstimmenden Zeilen in der ursprünglichen Tabelle suchen und dann die Zeilen in die neue Tabelle kopieren muss.</span><span class="sxs-lookup"><span data-stu-id="4bdda-106">Creating a restriction impacts performance because the provider must first create a table, find the matching rows in the original table, and then copy the rows to the new table.</span></span> <span data-ttu-id="4bdda-107">Wenn die Gesamtzahl der Zeilen in der Tabelle kleiner als 100 ist, ist es wahrscheinlich effektiver, alle Zeilen zu lesen und [dann IMAPITable::FindRow](imapitable-findrow.md) auf, um die entsprechende Zeile zu finden.</span><span class="sxs-lookup"><span data-stu-id="4bdda-107">If the total number of rows in the table is less than 100, it is probably more effective to read all of the rows and then call [IMAPITable::FindRow](imapitable-findrow.md) to find the appropriate row.</span></span> <span data-ttu-id="4bdda-108">Dies ist eine besonders gute Strategie, wenn diese Informationen nur gelegentlich benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="4bdda-108">This is a particularly good strategy if this information is needed only occasionally.</span></span> 
  
<span data-ttu-id="4bdda-109">Der richtige Zeitpunkt für die Verwendung einer Einschränkung ist, wenn die eingeschränkten oder gefilterten Informationen über einen längeren Zeitraum oder häufig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4bdda-109">The proper time to use a restriction is when the restricted or filtered information will be used over a longer period of time or used frequently.</span></span> <span data-ttu-id="4bdda-110">Wenn Sie beispielsweise immer eine Ansicht mit ungelesenen Nachrichten benötigen, ist eine Einschränkung der richtige Aufruf.</span><span class="sxs-lookup"><span data-stu-id="4bdda-110">For instance, if you always need a view with unread messages, then a restriction is the proper call to use.</span></span>
  

