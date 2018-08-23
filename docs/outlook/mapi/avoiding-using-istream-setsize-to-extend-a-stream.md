---
title: Verwenden von IStreamSetSize zum Erweitern eines Stream-Objekts zu vermeiden
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b6de594f-e331-4421-956b-86ee0b5518fe
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9245d4913c2832b8c942093e65cf088643a1947c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592080"
---
# <a name="avoiding-using-istreamsetsize-to-extend-a-stream"></a><span data-ttu-id="c22ea-103">Vermeiden der Verwendung von IStream::SetSize zum Erweitern eines Streams</span><span class="sxs-lookup"><span data-stu-id="c22ea-103">Avoiding Using IStream::SetSize to Extend a Stream</span></span>

  
  
<span data-ttu-id="c22ea-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c22ea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c22ea-105">Beim Schreiben in Streams ist es manchmal notwendig, den sie vergrößern, da ihre ursprüngliche Größe nicht mehr ausreichend ist.</span><span class="sxs-lookup"><span data-stu-id="c22ea-105">When writing to streams, it is sometimes necessary to enlarge them because their initial size is no longer sufficient.</span></span> <span data-ttu-id="c22ea-106">Verwenden Sie die OLE-Methode **IStream::Write** dazu statt **:: setSize**.</span><span class="sxs-lookup"><span data-stu-id="c22ea-106">Use the OLE method **IStream::Write** to accomplish this rather than **IStream::SetSize**.</span></span> <span data-ttu-id="c22ea-107">**IStream::Write** erweitert automatisch den Stream tätigen **:: setSize ** nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c22ea-107">**IStream::Write** automatically extends the stream, making ** IStream::SetSize ** unnecessary.</span></span> <span data-ttu-id="c22ea-108">Aufrufen von **IStream::Write** ohne **:: setSize** kann bis zu drei Mal schneller als vornehmen der **SetSize** aufrufen, bevor Sie **Schreiben**sein.</span><span class="sxs-lookup"><span data-stu-id="c22ea-108">Calling **IStream::Write** without **IStream::SetSize** can be up to three times faster than making the **SetSize** call prior to **Write**.</span></span>
  

