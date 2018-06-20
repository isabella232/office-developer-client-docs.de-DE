---
title: Herunterfahren von einem Anbieter gepackten PST-Datei
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 0c9e5917-1b96-323d-bf8b-1d3aa1f677d0
description: 'Zuletzt geändert: 02 Juli 2012'
ms.openlocfilehash: 5c8ad7443b0c1aa05f48284e4b09859ab53dd2c3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795533"
---
# <a name="shutting-down-a-wrapped-pst-store-provider"></a><span data-ttu-id="68e36-103">Herunterfahren von einem Anbieter gepackten PST-Datei</span><span class="sxs-lookup"><span data-stu-id="68e36-103">Shutting Down a Wrapped PST Store Provider</span></span>

 
  
<span data-ttu-id="68e36-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="68e36-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="68e36-105">Nachdem Sie mithilfe eines gepackten Anbieters für Persönliche Ordner-Datei (PST) anmelden, müssen Sie die gepackten PST-Speicheranbieter ordnungsgemäß herunterfahren.</span><span class="sxs-lookup"><span data-stu-id="68e36-105">After you finish using a wrapped Personal Folders file (PST) store provider, you must properly shut down the wrapped PST store provider.</span></span> <span data-ttu-id="68e36-106">Weitere Informationen zur Verwendung der gepackten PST Informationsdienst finden Sie unter [Verwenden einer gewrappt PST Store Provider](using-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="68e36-106">For more information about using the wrapped PST store provider, see [Using a Wrapped PST Store Provider](using-a-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="68e36-107">Um einem gepackten PST-Anbieter zu beenden, müssen Sie die Funktion **[IMSProvider::Shutdown](imsprovider-shutdown.md)** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="68e36-107">To shut down a wrapped PST store provider, you must call the **[IMSProvider::Shutdown](imsprovider-shutdown.md)** function.</span></span> <span data-ttu-id="68e36-108">Diese Funktionen wird die gepackten PST Speicheranbieter ordnungsgemäß geschlossen.</span><span class="sxs-lookup"><span data-stu-id="68e36-108">This functions closes down the wrapped PST store provider in an orderly fashion.</span></span> 
  
<span data-ttu-id="68e36-109">In diesem Thema wird die Funktion **IMSProvider::Shutdown** mithilfe eines Codebeispiels aus der umbrochen PST Store Beispielanbieter veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="68e36-109">In this topic, the **IMSProvider::Shutdown** function is demonstrated by using a code example from the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="68e36-110">Das Beispiel implementiert einen gepackten PST-Anbieter, der in Verbindung mit der API für die Replikation verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="68e36-110">The sample implements a wrapped PST provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="68e36-111">Weitere Informationen zum Herunterladen und Installieren der umbrochen PST Store Beispielanbieter finden Sie unter [Sample umfließendem PST Store Provider installieren](installing-the-sample-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="68e36-111">For more information about downloading and installing the Sample Wrapped PST Store Provider, see [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span></span> <span data-ttu-id="68e36-112">Weitere Informationen zur Replikation-API finden Sie unter [Über die Replikation-API](about-the-replication-api.md).</span><span class="sxs-lookup"><span data-stu-id="68e36-112">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
## <a name="shut-down-routine"></a><span data-ttu-id="68e36-113">Routine Herunterfahren</span><span class="sxs-lookup"><span data-stu-id="68e36-113">Shut Down Routine</span></span>

<span data-ttu-id="68e36-114">Die MAPI-Warteschlange Ruft die **[IMSProvider::Shutdown](imsprovider-shutdown.md)** -Funktion, bevor der gepackten PST Informationsdienst freigegeben, damit der gepackten PST Informationsdienst ordnungsgemäß heruntergefahren werden kann.</span><span class="sxs-lookup"><span data-stu-id="68e36-114">The MAPI spooler calls the **[IMSProvider::Shutdown](imsprovider-shutdown.md)** function just before it releases the wrapped PST store provider so that the wrapped PST store provider can shut down properly.</span></span> <span data-ttu-id="68e36-115">Die Funktion wird beendet, alle Sitzungsobjekte, die den gepackten PST-Speicheranbieter zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="68e36-115">The function terminates all session objects associated with the wrapped PST store provider.</span></span> 
  
## <a name="cmsprovidershutdown-example"></a><span data-ttu-id="68e36-116">CMSProvider::ShutDown()-Beispiel</span><span class="sxs-lookup"><span data-stu-id="68e36-116">CMSProvider::ShutDown() Example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="68e36-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="68e36-117">See also</span></span>



[<span data-ttu-id="68e36-118">Zum Beispiel umgebrochen PST-Anbieter</span><span class="sxs-lookup"><span data-stu-id="68e36-118">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="68e36-119">Installieren des Beispiels umfließendem PST-Anbieter</span><span class="sxs-lookup"><span data-stu-id="68e36-119">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="68e36-120">Initialisieren einen Anbieter für umbrochenen PST anmelden</span><span class="sxs-lookup"><span data-stu-id="68e36-120">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="68e36-121">Anmelden bei einem Anbieter gepackten PST-Datei</span><span class="sxs-lookup"><span data-stu-id="68e36-121">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="68e36-122">Verwenden eines Anbieters gepackten PST-Speichers</span><span class="sxs-lookup"><span data-stu-id="68e36-122">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)

