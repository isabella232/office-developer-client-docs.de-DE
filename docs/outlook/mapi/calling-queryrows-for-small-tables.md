---
title: Aufrufen von QueryRows für kleine Tabellen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8c38bb0f-de0b-4d70-9f6d-db652445e137
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 40533470681182719f5009b048e3b173b92ef290
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791367"
---
# <a name="calling-queryrows-for-small-tables"></a><span data-ttu-id="f68a4-103">Aufrufen von QueryRows für kleine Tabellen</span><span class="sxs-lookup"><span data-stu-id="f68a4-103">Calling QueryRows for Small Tables</span></span>

  
  
<span data-ttu-id="f68a4-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f68a4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f68a4-105">Beim Abrufen von Zeilen aus einer kleinen Tabelle rufen Sie [IMAPITable::QueryRows](imapitable-queryrows.md) anstelle der ersten Erstellung einer Einschränkung auf.</span><span class="sxs-lookup"><span data-stu-id="f68a4-105">When retrieving rows from a small table, call [IMAPITable::QueryRows](imapitable-queryrows.md) instead of first building a restriction.</span></span> <span data-ttu-id="f68a4-106">Erstellen eine Einschränkung beeinträchtigt die Leistung, da der Anbieter muss zuerst erstellen Sie eine Tabelle, die übereinstimmenden Zeilen in der ursprünglichen Tabelle finden und Sie die Zeilen in der neuen Tabelle kopieren.</span><span class="sxs-lookup"><span data-stu-id="f68a4-106">Creating a restriction impacts performance because the provider must first create a table, find the matching rows in the original table, and then copy the rows to the new table.</span></span> <span data-ttu-id="f68a4-107">Wenn die Gesamtzahl der Zeilen in der Tabelle weniger als 100 ist, ist es wahrscheinlich effektivere Lesen aller Zeilen und rufen Sie dann [IMAPITable](imapitable-findrow.md) , um die entsprechende Zeile zu finden.</span><span class="sxs-lookup"><span data-stu-id="f68a4-107">If the total number of rows in the table is less than 100, it is probably more effective to read all of the rows and then call [IMAPITable::FindRow](imapitable-findrow.md) to find the appropriate row.</span></span> <span data-ttu-id="f68a4-108">Dies ist eine gute Strategie, falls diese Informationen nur gelegentlich erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="f68a4-108">This is a particularly good strategy if this information is needed only occasionally.</span></span> 
  
<span data-ttu-id="f68a4-109">Geeigneten Zeitpunkt eine Einschränkung zu verwenden ist, wenn die eingeschränkte oder gefilterte Informationen über einen längeren Zeitraum verwendet oder häufig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f68a4-109">The proper time to use a restriction is when the restricted or filtered information will be used over a longer period of time or used frequently.</span></span> <span data-ttu-id="f68a4-110">Beispielsweise wenn Sie eine Ansicht mit ungelesene Nachrichten immer benötigen, ist eine Beschränkung der richtigen Aufruf verwenden.</span><span class="sxs-lookup"><span data-stu-id="f68a4-110">For instance, if you always need a view with unread messages, then a restriction is the proper call to use.</span></span>
  

