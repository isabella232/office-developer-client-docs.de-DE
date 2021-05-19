---
title: Herunterfahren eines umbrochenen PST Store-Anbieters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 0c9e5917-1b96-323d-bf8b-1d3aa1f677d0
description: 'Letzte Änderung: 02. Juli 2012'
ms.openlocfilehash: fa918920213ee77c4d0c1d3ccc239ae7cffe81fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409944"
---
# <a name="shutting-down-a-wrapped-pst-store-provider"></a><span data-ttu-id="4c19b-103">Herunterfahren eines umbrochenen PST Store-Anbieters</span><span class="sxs-lookup"><span data-stu-id="4c19b-103">Shutting Down a Wrapped PST Store Provider</span></span>

 
  
<span data-ttu-id="4c19b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4c19b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4c19b-105">Nachdem Sie die Verwendung eines umschlossenen Anbieters für persönliche Ordner (PST)-Speicher abgeschlossen haben, müssen Sie den umschlossenen ANBIETER für den PST-Speicher ordnungsgemäß herunterfahren.</span><span class="sxs-lookup"><span data-stu-id="4c19b-105">After you finish using a wrapped Personal Folders file (PST) store provider, you must properly shut down the wrapped PST store provider.</span></span> <span data-ttu-id="4c19b-106">Weitere Informationen zur Verwendung des umschlossenen PST Store-Anbieters finden Sie unter [Using a Wrapped PST Store Provider](using-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="4c19b-106">For more information about using the wrapped PST store provider, see [Using a Wrapped PST Store Provider](using-a-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="4c19b-107">Zum Herunterfahren eines umschlossenen PST Store-Anbieters müssen Sie die **[IMSProvider::Shutdown-Funktion](imsprovider-shutdown.md)** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4c19b-107">To shut down a wrapped PST store provider, you must call the **[IMSProvider::Shutdown](imsprovider-shutdown.md)** function.</span></span> <span data-ttu-id="4c19b-108">Mit diesen Funktionen wird der umschlossene ANBIETER für den PST Store in geordneter Weise geschlossen.</span><span class="sxs-lookup"><span data-stu-id="4c19b-108">This functions closes down the wrapped PST store provider in an orderly fashion.</span></span> 
  
<span data-ttu-id="4c19b-109">In diesem Thema wird die **IMSProvider::Shutdown-Funktion** mithilfe eines Codebeispiels aus dem Anbieter für den Pst Store mit Beispielwickeln demonstriert.</span><span class="sxs-lookup"><span data-stu-id="4c19b-109">In this topic, the **IMSProvider::Shutdown** function is demonstrated by using a code example from the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="4c19b-110">Das Beispiel implementiert einen umschlossenen PST-Anbieter, der in Verbindung mit der Replikations-API verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4c19b-110">The sample implements a wrapped PST provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="4c19b-111">Weitere Informationen zum Herunterladen und Installieren des Beispielanbieters für den umschlossenen PST Store finden Sie unter [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="4c19b-111">For more information about downloading and installing the Sample Wrapped PST Store Provider, see [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span></span> <span data-ttu-id="4c19b-112">Weitere Informationen zur Replikations-API finden Sie unter [Informationen zur Replikations-API](about-the-replication-api.md).</span><span class="sxs-lookup"><span data-stu-id="4c19b-112">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
## <a name="shut-down-routine"></a><span data-ttu-id="4c19b-113">Herunterfahren der Routine</span><span class="sxs-lookup"><span data-stu-id="4c19b-113">Shut Down Routine</span></span>

<span data-ttu-id="4c19b-114">Der MAPI-Spooler ruft die **[IMSProvider::Shutdown-Funktion](imsprovider-shutdown.md)** kurz vor der Veröffentlichung des umschlossenen PST-Speicheranbieters auf, damit der umschlossene PST-Speicheranbieter ordnungsgemäß heruntergefahren werden kann.</span><span class="sxs-lookup"><span data-stu-id="4c19b-114">The MAPI spooler calls the **[IMSProvider::Shutdown](imsprovider-shutdown.md)** function just before it releases the wrapped PST store provider so that the wrapped PST store provider can shut down properly.</span></span> <span data-ttu-id="4c19b-115">Die Funktion beendet alle Sitzungsobjekte, die dem umschlossenen ANBIETER für den PST-Speicher zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="4c19b-115">The function terminates all session objects associated with the wrapped PST store provider.</span></span> 
  
## <a name="cmsprovidershutdown-example"></a><span data-ttu-id="4c19b-116">CMSProvider::ShutDown() (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="4c19b-116">CMSProvider::ShutDown() Example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="4c19b-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4c19b-117">See also</span></span>



[<span data-ttu-id="4c19b-118">Informationen zum Beispiel umschlossenen PST Store-Anbieter</span><span class="sxs-lookup"><span data-stu-id="4c19b-118">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="4c19b-119">Installieren des Beispielanbieters für den umschlossenen PST Store</span><span class="sxs-lookup"><span data-stu-id="4c19b-119">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="4c19b-120">Initialisieren eines umbrochenen PST Store-Anbieters</span><span class="sxs-lookup"><span data-stu-id="4c19b-120">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="4c19b-121">Anmelden bei einem umschlossenen PST Store-Anbieter</span><span class="sxs-lookup"><span data-stu-id="4c19b-121">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="4c19b-122">Verwenden eines umbrochenen PST Store-Anbieters</span><span class="sxs-lookup"><span data-stu-id="4c19b-122">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)

