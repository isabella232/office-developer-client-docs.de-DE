---
title: Abrufen und Festlegen von Eigenschaften mit GetProps und SetProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 309d2b3d-dc71-4222-b293-4bfc467b5429
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5751dc8b06d40b9f07a39f05868c328d64c27762
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791799"
---
# <a name="getting-and-setting-properties-with-getprops-and-setprops"></a><span data-ttu-id="a3b1b-103">Abrufen und Festlegen von Eigenschaften mit GetProps und SetProps</span><span class="sxs-lookup"><span data-stu-id="a3b1b-103">Getting and setting properties with GetProps and SetProps</span></span>
 
<span data-ttu-id="a3b1b-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a3b1b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a3b1b-105">Versuchen Sie nach Möglichkeit zum Abfragen und ändern eine Eigenschaft mit den Methoden [IMAPIProp::GetProps](imapiprop-getprops.md) und [IMAPIProp::SetProps](imapiprop-setprops.md) .</span><span class="sxs-lookup"><span data-stu-id="a3b1b-105">Whenever possible, try to retrieve or modify a property with the [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPIProp::SetProps](imapiprop-setprops.md) methods.</span></span> <span data-ttu-id="a3b1b-106">Es sei denn, die Eigenschaft, die Arbeit mit sehr groß ist, sollten diese Methoden ausreichen.</span><span class="sxs-lookup"><span data-stu-id="a3b1b-106">Unless the property you are working with is very large, these methods should be adequate.</span></span> <span data-ttu-id="a3b1b-107">Andere Alternative ist das Lesen oder Schreiben in ein Stream-Objekt mit der [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="a3b1b-107">The other alternative is to read from or write to a stream with the [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) interface.</span></span> <span data-ttu-id="a3b1b-108">Datenströme behandeln sehr große Eigenschaften erfolgreich, aber sie sind eine größere Belastung Ressourcen, da hierfür die COM-Bibliotheken erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="a3b1b-108">Streams can handle very large properties successfully, but they are a greater drain on resources because they require the COM libraries.</span></span> <span data-ttu-id="a3b1b-109">Verwenden Sie die **IStream** -Schnittstelle erst nach dem Aufruf von **IMAPIProp::GetProps** oder **IMAPIProp::SetProps** ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="a3b1b-109">Use the **IStream** interface only after your call to **IMAPIProp::GetProps** or **IMAPIProp::SetProps** fails.</span></span> 
  

