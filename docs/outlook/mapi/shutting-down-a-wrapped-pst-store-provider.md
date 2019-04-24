---
title: Herunterfahren eines einGebundenen PST-Speicheranbieters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 0c9e5917-1b96-323d-bf8b-1d3aa1f677d0
description: 'Zuletzt geändert: 02 Juli, 2012'
ms.openlocfilehash: fa918920213ee77c4d0c1d3ccc239ae7cffe81fc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282782"
---
# <a name="shutting-down-a-wrapped-pst-store-provider"></a><span data-ttu-id="f3f88-103">Herunterfahren eines einGebundenen PST-Speicheranbieters</span><span class="sxs-lookup"><span data-stu-id="f3f88-103">Shutting Down a Wrapped PST Store Provider</span></span>

 
  
<span data-ttu-id="f3f88-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f3f88-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f3f88-105">Nachdem Sie einen eingebundenen PST-Speicheranbieter verwendet haben, müssen Sie den eingebundenen PST-Speicheranbieter ordnungsgemäß herunterfahren.</span><span class="sxs-lookup"><span data-stu-id="f3f88-105">After you finish using a wrapped Personal Folders file (PST) store provider, you must properly shut down the wrapped PST store provider.</span></span> <span data-ttu-id="f3f88-106">Weitere Informationen zur Verwendung des eingebundenen PST-Speicheranbieters finden Sie unter [Verwenden eines EingebundenEN PST-Speicheranbieters](using-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f3f88-106">For more information about using the wrapped PST store provider, see [Using a Wrapped PST Store Provider](using-a-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="f3f88-107">Zum Herunterfahren eines eingebundenen PST-Speicheranbieters müssen Sie die **[IMSProvider:: Shutdown](imsprovider-shutdown.md)** -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f3f88-107">To shut down a wrapped PST store provider, you must call the **[IMSProvider::Shutdown](imsprovider-shutdown.md)** function.</span></span> <span data-ttu-id="f3f88-108">Diese Funktionen schließen den eingebundenen PST-Speicheranbieter ordnungsgemäß ab.</span><span class="sxs-lookup"><span data-stu-id="f3f88-108">This functions closes down the wrapped PST store provider in an orderly fashion.</span></span> 
  
<span data-ttu-id="f3f88-109">In diesem Thema wird die **IMSProvider:: Shutdown** -Funktion anhand eines Codebeispiels aus dem eingebundenen PST-Speicheranbieter demonstriert.</span><span class="sxs-lookup"><span data-stu-id="f3f88-109">In this topic, the **IMSProvider::Shutdown** function is demonstrated by using a code example from the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="f3f88-110">Im Beispiel wird ein eingebundener PST-Anbieter implementiert, der in Verbindung mit der Replikations-API verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f3f88-110">The sample implements a wrapped PST provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="f3f88-111">Weitere Informationen zum herunterladen und Installieren des eingeWickelten Beispiel-PST-Speicheranbieters finden Sie unter [Installing the Sample Wrapped Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f3f88-111">For more information about downloading and installing the Sample Wrapped PST Store Provider, see [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span></span> <span data-ttu-id="f3f88-112">Weitere Informationen zur Replikations-API finden Sie unter Informationen zur [Replikations-API](about-the-replication-api.md).</span><span class="sxs-lookup"><span data-stu-id="f3f88-112">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
## <a name="shut-down-routine"></a><span data-ttu-id="f3f88-113">Herunterfahren der Routine</span><span class="sxs-lookup"><span data-stu-id="f3f88-113">Shut Down Routine</span></span>

<span data-ttu-id="f3f88-114">Der MAPI-Spooler Ruft die **[IMSProvider:: Shutdown](imsprovider-shutdown.md)** -Funktion kurz vor dem Aufheben des eingebundenen PST-Speicheranbieters auf, sodass der verpackte PST-Speicheranbieter ordnungsgemäß heruntergefahren werden kann.</span><span class="sxs-lookup"><span data-stu-id="f3f88-114">The MAPI spooler calls the **[IMSProvider::Shutdown](imsprovider-shutdown.md)** function just before it releases the wrapped PST store provider so that the wrapped PST store provider can shut down properly.</span></span> <span data-ttu-id="f3f88-115">Die Funktion beendet alle Sitzungsobjekte, die dem eingebundenen PST-Speicheranbieter zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f3f88-115">The function terminates all session objects associated with the wrapped PST store provider.</span></span> 
  
## <a name="cmsprovidershutdown-example"></a><span data-ttu-id="f3f88-116">CMSProvider:: ShutDown ()-Beispiel</span><span class="sxs-lookup"><span data-stu-id="f3f88-116">CMSProvider::ShutDown() Example</span></span>

```cpp
STDMETHODIMP CMSProvider::Shutdown(ULONG * pulFlags) 
{ 
    HRESULT hRes = S_OK; 
    Log(true,"CMSProvider::Shutdown\n"); 
    hRes =m_pPSTMS->Shutdown(pulFlags); 
    Log(true,"CMSProvider::Shutdown returned: 0x%08X\n", hRes); 
    return hRes ;  
}
```

## <a name="see-also"></a><span data-ttu-id="f3f88-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f3f88-117">See also</span></span>



[<span data-ttu-id="f3f88-118">Informationen zum einGebundenen PST-Speicheranbieter</span><span class="sxs-lookup"><span data-stu-id="f3f88-118">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="f3f88-119">Installieren des eingeWickelten Beispiel-PST-Speicheranbieters</span><span class="sxs-lookup"><span data-stu-id="f3f88-119">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="f3f88-120">Initialisieren eines einGebundenen PST-Speicheranbieters</span><span class="sxs-lookup"><span data-stu-id="f3f88-120">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="f3f88-121">Anmelden bei einem einGebundenen PST-Speicheranbieter</span><span class="sxs-lookup"><span data-stu-id="f3f88-121">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="f3f88-122">Verwenden eines einGebundenen PST-Speicheranbieters</span><span class="sxs-lookup"><span data-stu-id="f3f88-122">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)

