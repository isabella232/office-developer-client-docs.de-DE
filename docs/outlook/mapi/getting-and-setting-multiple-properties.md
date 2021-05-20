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
ms.openlocfilehash: dd25751978eb036531238e6372e35934b3ec145a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432261"
---
# <a name="getting-and-setting-multiple-properties"></a><span data-ttu-id="80cf7-103">Abrufen und Festlegen mehrerer Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="80cf7-103">Getting and setting multiple properties</span></span>

<span data-ttu-id="80cf7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="80cf7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="80cf7-105">Durch das Abrufen und Festlegen so vieler Eigenschaften wie möglich bei der geringsten Anzahl von Anrufen wird die Remoteaktivität eingeschränkt, und der Aufwand für jede Eigenschaft wird reduziert.</span><span class="sxs-lookup"><span data-stu-id="80cf7-105">By getting and setting as many properties as possible with the least number of calls, remote activity is curtailed and the overhead involved with each property is reduced.</span></span> <span data-ttu-id="80cf7-106">Obwohl Dienstanbieter versuchen, Eigenschaften zu sammeln, bevor sie einen Remoteprozeduraufruf zum Abrufen oder Ändern aufrufen, können Sie diesen Aufwand optimieren, indem Sie zunächst mehrere Eigenschaften anfordern.</span><span class="sxs-lookup"><span data-stu-id="80cf7-106">Although service providers try to collect properties before making a remote procedure call for retrieval or modification, you can optimize this effort by requesting multiple properties to begin with.</span></span>
  
<span data-ttu-id="80cf7-107">Wenn Sie z. B. mit Routinglisten arbeiten, die zukünftige Empfänger mit benannten Eigenschaften beschreiben, die zu bestimmten Eigenschaftensätzen gehören, verarbeiten Sie alle Empfänger mit zwei Aufrufen.</span><span class="sxs-lookup"><span data-stu-id="80cf7-107">For example, if you work with routing lists that describe future recipients with named properties belonging to particular property sets, process all of the recipients with two calls.</span></span> <span data-ttu-id="80cf7-108">Verwenden Sie einen Aufruf von [IMAPIProp::GetIDsFromNames,](imapiprop-getidsfromnames.md) um die Bezeichner für alle Empfängereigenschaften abzurufen, und den anderen Aufruf von [IMAPIProp::GetProps,](imapiprop-getprops.md) um alle Werte abzurufen.</span><span class="sxs-lookup"><span data-stu-id="80cf7-108">Use one call to [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to retrieve the identifiers for all of the recipient properties and the other call to [IMAPIProp::GetProps](imapiprop-getprops.md) to retrieve all of the values.</span></span> <span data-ttu-id="80cf7-109">Die Alternative, einen Aufruf von **GetIDsFromNames** gefolgt von einem Aufruf von **GetProps** für jeden Empfänger, ist wesentlich weniger effizient.</span><span class="sxs-lookup"><span data-stu-id="80cf7-109">The alternative, making a call to **GetIDsFromNames** followed by a call to **GetProps** for each recipient, is much less efficient.</span></span> 
  

