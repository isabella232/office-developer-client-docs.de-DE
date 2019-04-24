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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299377"
---
# <a name="getting-and-setting-multiple-properties"></a><span data-ttu-id="547cc-103">Abrufen und Festlegen mehrerer Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="547cc-103">Getting and setting multiple properties</span></span>

<span data-ttu-id="547cc-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="547cc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="547cc-105">Durch das Aufrufen und festlegen so vieler Eigenschaften wie möglich mit der geringsten Anzahl von Anrufen wird die Remote Aktivität eingeschränkt, und der mit den einzelnen Eigenschaften verbundene Aufwand wird reduziert.</span><span class="sxs-lookup"><span data-stu-id="547cc-105">By getting and setting as many properties as possible with the least number of calls, remote activity is curtailed and the overhead involved with each property is reduced.</span></span> <span data-ttu-id="547cc-106">Obwohl Dienstanbieter versuchen, Eigenschaften zu sammeln, bevor Sie einen Remoteprozeduraufruf zum Abrufen oder ändern ausführen, können Sie diesen Aufwand optimieren, indem Sie zunächst mehrere Eigenschaften anfordern.</span><span class="sxs-lookup"><span data-stu-id="547cc-106">Although service providers try to collect properties before making a remote procedure call for retrieval or modification, you can optimize this effort by requesting multiple properties to begin with.</span></span>
  
<span data-ttu-id="547cc-107">Wenn Sie beispielsweise mit Routing Listen arbeiten, die zukünftige Empfänger mit benannten Eigenschaften beschreiben, die zu bestimmten Eigenschaftensätzen gehören, verarbeiten Sie alle Empfänger mit zwei anrufen.</span><span class="sxs-lookup"><span data-stu-id="547cc-107">For example, if you work with routing lists that describe future recipients with named properties belonging to particular property sets, process all of the recipients with two calls.</span></span> <span data-ttu-id="547cc-108">Verwenden Sie einen Aufruf von [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) , um die Bezeichner für alle Empfänger Eigenschaften und den anderen Aufruf von [IMAPIProp::](imapiprop-getprops.md) GetProps abzurufen, um alle Werte abzurufen.</span><span class="sxs-lookup"><span data-stu-id="547cc-108">Use one call to [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to retrieve the identifiers for all of the recipient properties and the other call to [IMAPIProp::GetProps](imapiprop-getprops.md) to retrieve all of the values.</span></span> <span data-ttu-id="547cc-109">Die Alternative, durch die ein Aufruf von **GetIDsFromNames** gefolgt von einem Aufruf \*\*\*\* von GetProps für jeden Empfänger erfolgt, ist weitaus weniger effizient.</span><span class="sxs-lookup"><span data-stu-id="547cc-109">The alternative, making a call to **GetIDsFromNames** followed by a call to **GetProps** for each recipient, is much less efficient.</span></span> 
  

