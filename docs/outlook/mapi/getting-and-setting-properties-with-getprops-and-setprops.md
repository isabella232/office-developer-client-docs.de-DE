---
title: Abrufen und Festlegen von Eigenschaften mit GetProps und SetProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 309d2b3d-dc71-4222-b293-4bfc467b5429
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6b54be711d8c33648d211e480c6a00ee92755108
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575567"
---
# <a name="getting-and-setting-properties-with-getprops-and-setprops"></a><span data-ttu-id="07542-103">Abrufen und Festlegen von Eigenschaften mit GetProps und SetProps</span><span class="sxs-lookup"><span data-stu-id="07542-103">Getting and setting properties with GetProps and SetProps</span></span>
 
<span data-ttu-id="07542-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="07542-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="07542-105">Versuchen Sie nach Möglichkeit zum Abfragen und ändern eine Eigenschaft mit den Methoden [IMAPIProp::GetProps](imapiprop-getprops.md) und [IMAPIProp::SetProps](imapiprop-setprops.md) .</span><span class="sxs-lookup"><span data-stu-id="07542-105">Whenever possible, try to retrieve or modify a property with the [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPIProp::SetProps](imapiprop-setprops.md) methods.</span></span> <span data-ttu-id="07542-106">Es sei denn, die Eigenschaft, die Arbeit mit sehr groß ist, sollten diese Methoden ausreichen.</span><span class="sxs-lookup"><span data-stu-id="07542-106">Unless the property you are working with is very large, these methods should be adequate.</span></span> <span data-ttu-id="07542-107">Andere Alternative ist das Lesen oder Schreiben in ein Stream-Objekt mit der [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="07542-107">The other alternative is to read from or write to a stream with the [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) interface.</span></span> <span data-ttu-id="07542-108">Datenströme behandeln sehr große Eigenschaften erfolgreich, aber sie sind eine größere Belastung Ressourcen, da hierfür die COM-Bibliotheken erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="07542-108">Streams can handle very large properties successfully, but they are a greater drain on resources because they require the COM libraries.</span></span> <span data-ttu-id="07542-109">Verwenden Sie die **IStream** -Schnittstelle erst nach dem Aufruf von **IMAPIProp::GetProps** oder **IMAPIProp::SetProps** ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="07542-109">Use the **IStream** interface only after your call to **IMAPIProp::GetProps** or **IMAPIProp::SetProps** fails.</span></span> 
  

