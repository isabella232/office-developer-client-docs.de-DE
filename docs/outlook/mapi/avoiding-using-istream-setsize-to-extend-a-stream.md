---
title: Vermeiden der Verwendung von IStreamSetSize zum Erweitern eines Streams
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b6de594f-e331-4421-956b-86ee0b5518fe
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 614bb3d142b7aaabe89223b6ce3552469edfce27
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428914"
---
# <a name="avoiding-using-istreamsetsize-to-extend-a-stream"></a><span data-ttu-id="4b88a-103">Vermeiden der Verwendung von IStream:: SetSize zum Erweitern eines Streams</span><span class="sxs-lookup"><span data-stu-id="4b88a-103">Avoiding Using IStream::SetSize to Extend a Stream</span></span>

  
  
<span data-ttu-id="4b88a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4b88a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4b88a-105">Beim Schreiben in Streams ist es manchmal erforderlich, Sie zu vergrößern, da ihre anfängliche Größe nicht mehr ausreicht.</span><span class="sxs-lookup"><span data-stu-id="4b88a-105">When writing to streams, it is sometimes necessary to enlarge them because their initial size is no longer sufficient.</span></span> <span data-ttu-id="4b88a-106">Verwenden Sie die OLE-Methode **IStream:: Write** anstelle von **IStream:: SetSize**.</span><span class="sxs-lookup"><span data-stu-id="4b88a-106">Use the OLE method **IStream::Write** to accomplish this rather than **IStream::SetSize**.</span></span> <span data-ttu-id="4b88a-107">**IStream:: Write** erweitert den Stream automatisch, sodass \* \* IStream:: SetSize \* \* nicht erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="4b88a-107">**IStream::Write** automatically extends the stream, making \*\* IStream::SetSize \*\* unnecessary.</span></span> <span data-ttu-id="4b88a-108">Das Aufrufen von **IStream:: Write** ohne **IStream:: SetSize** kann bis zu dreimal schneller sein als das Ausführen des SetSize-Aufrufs vor dem **Schreiben**. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="4b88a-108">Calling **IStream::Write** without **IStream::SetSize** can be up to three times faster than making the **SetSize** call prior to **Write**.</span></span>
  

