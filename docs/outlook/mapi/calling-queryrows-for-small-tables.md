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
ms.openlocfilehash: 34975677bedccf3f9111985d371e21d482b45584
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589336"
---
# <a name="calling-queryrows-for-small-tables"></a><span data-ttu-id="ff590-103">Aufrufen von QueryRows für kleine Tabellen</span><span class="sxs-lookup"><span data-stu-id="ff590-103">Calling QueryRows for Small Tables</span></span>

  
  
<span data-ttu-id="ff590-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ff590-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ff590-105">Beim Abrufen von Zeilen aus einer kleinen Tabelle rufen Sie [IMAPITable::QueryRows](imapitable-queryrows.md) anstelle der ersten Erstellung einer Einschränkung auf.</span><span class="sxs-lookup"><span data-stu-id="ff590-105">When retrieving rows from a small table, call [IMAPITable::QueryRows](imapitable-queryrows.md) instead of first building a restriction.</span></span> <span data-ttu-id="ff590-106">Erstellen eine Einschränkung beeinträchtigt die Leistung, da der Anbieter muss zuerst erstellen Sie eine Tabelle, die übereinstimmenden Zeilen in der ursprünglichen Tabelle finden und Sie die Zeilen in der neuen Tabelle kopieren.</span><span class="sxs-lookup"><span data-stu-id="ff590-106">Creating a restriction impacts performance because the provider must first create a table, find the matching rows in the original table, and then copy the rows to the new table.</span></span> <span data-ttu-id="ff590-107">Wenn die Gesamtzahl der Zeilen in der Tabelle weniger als 100 ist, ist es wahrscheinlich effektivere Lesen aller Zeilen und rufen Sie dann [IMAPITable](imapitable-findrow.md) , um die entsprechende Zeile zu finden.</span><span class="sxs-lookup"><span data-stu-id="ff590-107">If the total number of rows in the table is less than 100, it is probably more effective to read all of the rows and then call [IMAPITable::FindRow](imapitable-findrow.md) to find the appropriate row.</span></span> <span data-ttu-id="ff590-108">Dies ist eine gute Strategie, falls diese Informationen nur gelegentlich erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="ff590-108">This is a particularly good strategy if this information is needed only occasionally.</span></span> 
  
<span data-ttu-id="ff590-109">Geeigneten Zeitpunkt eine Einschränkung zu verwenden ist, wenn die eingeschränkte oder gefilterte Informationen über einen längeren Zeitraum verwendet oder häufig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ff590-109">The proper time to use a restriction is when the restricted or filtered information will be used over a longer period of time or used frequently.</span></span> <span data-ttu-id="ff590-110">Beispielsweise wenn Sie eine Ansicht mit ungelesene Nachrichten immer benötigen, ist eine Beschränkung der richtigen Aufruf verwenden.</span><span class="sxs-lookup"><span data-stu-id="ff590-110">For instance, if you always need a view with unread messages, then a restriction is the proper call to use.</span></span>
  

