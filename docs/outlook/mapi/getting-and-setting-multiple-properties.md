---
title: Abrufen und Festlegen mehrerer Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 29b7f5f1-afc1-45d9-8867-9312c072e74b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 150f2a55bff4188c1f692de8276ed869bcf66c3c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791789"
---
# <a name="getting-and-setting-multiple-properties"></a><span data-ttu-id="9e068-103">Abrufen und Festlegen mehrerer Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9e068-103">Getting and setting multiple properties</span></span>

<span data-ttu-id="9e068-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9e068-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9e068-105">Durch Abrufen und Festlegen von so viele Eigenschaften wie möglich mit der geringsten Anzahl Anrufe, remote Aktivität Falle wird und mit jeder Eigenschaft Verwaltungsaufwand reduziert.</span><span class="sxs-lookup"><span data-stu-id="9e068-105">By getting and setting as many properties as possible with the least number of calls, remote activity is curtailed and the overhead involved with each property is reduced.</span></span> <span data-ttu-id="9e068-106">Zwar Dienstanbieter versuchen, vor der Durchführung eines Remoteprozeduraufrufs für abrufen oder Ändern von Eigenschaften erfasst werden sollen, können Sie Maßnahme optimieren, indem Sie mehrere Eigenschaften zunächst anfordern.</span><span class="sxs-lookup"><span data-stu-id="9e068-106">Although service providers try to collect properties before making a remote procedure call for retrieval or modification, you can optimize this effort by requesting multiple properties to begin with.</span></span>
  
<span data-ttu-id="9e068-107">Beispielsweise wenn Sie routing Listen, die mit benannten Eigenschaften von bestimmten Eigenschaftensätze zukünftige Empfänger beschreiben entwickelt, verarbeitet alle Empfänger mit zwei Anrufe entgegennehmen.</span><span class="sxs-lookup"><span data-stu-id="9e068-107">For example, if you work with routing lists that describe future recipients with named properties belonging to particular property sets, process all of the recipients with two calls.</span></span> <span data-ttu-id="9e068-108">Verwenden Sie durch Aufrufen von [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) , um die Bezeichner für alle den Empfängereigenschaften und den anderen Anruf an [IMAPIProp::GetProps](imapiprop-getprops.md) zum Abrufen aller Werte abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9e068-108">Use one call to [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to retrieve the identifiers for all of the recipient properties and the other call to [IMAPIProp::GetProps](imapiprop-getprops.md) to retrieve all of the values.</span></span> <span data-ttu-id="9e068-109">Die Alternative, tätigen eines Anrufs auf **GetIDsFromNames** gefolgt von einem Aufruf von **GetProps** für jeden Empfänger ist viel weniger effizient.</span><span class="sxs-lookup"><span data-stu-id="9e068-109">The alternative, making a call to **GetIDsFromNames** followed by a call to **GetProps** for each recipient, is much less efficient.</span></span> 
  

