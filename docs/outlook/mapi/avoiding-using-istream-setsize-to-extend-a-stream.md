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
ms.openlocfilehash: 54d352c263fd34bc8494d8d76c76cb22e0bafa58
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791372"
---
# <a name="avoiding-using-istreamsetsize-to-extend-a-stream"></a><span data-ttu-id="f6a35-103">Vermeiden der Verwendung von IStream::SetSize zum Erweitern eines Streams</span><span class="sxs-lookup"><span data-stu-id="f6a35-103">Avoiding Using IStream::SetSize to Extend a Stream</span></span>

  
  
<span data-ttu-id="f6a35-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f6a35-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f6a35-105">Beim Schreiben in Streams ist es manchmal notwendig, den sie vergrößern, da ihre ursprüngliche Größe nicht mehr ausreichend ist.</span><span class="sxs-lookup"><span data-stu-id="f6a35-105">When writing to streams, it is sometimes necessary to enlarge them because their initial size is no longer sufficient.</span></span> <span data-ttu-id="f6a35-106">Verwenden Sie die OLE-Methode **IStream::Write** dazu statt **:: setSize**.</span><span class="sxs-lookup"><span data-stu-id="f6a35-106">Use the OLE method **IStream::Write** to accomplish this rather than **IStream::SetSize**.</span></span> <span data-ttu-id="f6a35-107">**IStream::Write** erweitert automatisch den Stream tätigen **:: setSize ** nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f6a35-107">**IStream::Write** automatically extends the stream, making ** IStream::SetSize ** unnecessary.</span></span> <span data-ttu-id="f6a35-108">Aufrufen von **IStream::Write** ohne **:: setSize** kann bis zu drei Mal schneller als vornehmen der **SetSize** aufrufen, bevor Sie **Schreiben**sein.</span><span class="sxs-lookup"><span data-stu-id="f6a35-108">Calling **IStream::Write** without **IStream::SetSize** can be up to three times faster than making the **SetSize** call prior to **Write**.</span></span>
  

