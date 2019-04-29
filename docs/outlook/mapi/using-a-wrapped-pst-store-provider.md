---
title: Verwenden eines Anbieters von umschlossenem PST-Speicher
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 98f08432-e86c-cba6-45fd-5a6c94d50aaf
description: 'Zuletzt geändert: 03 Juli, 2012'
ms.openlocfilehash: b7c651044ab7f4cad7032db69e157c9a3589bde9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420822"
---
# <a name="using-a-wrapped-pst-store-provider"></a><span data-ttu-id="f513b-103">Verwenden eines Anbieters von umschlossenem PST-Speicher</span><span class="sxs-lookup"><span data-stu-id="f513b-103">Using a wrapped PST store provider</span></span>

<span data-ttu-id="f513b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f513b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f513b-105">Bevor Sie einen eingebundenen PST-Speicheranbieter verwenden können, müssen Sie den eingebundenen PST-Speicheranbieter initialisieren und konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="f513b-105">Before you can use a wrapped Personal Folders file (PST) store provider, you must initialize and configure the wrapped PST store provider.</span></span> <span data-ttu-id="f513b-106">Nach der Konfiguration des eingebundenen PST-Speicheranbieters müssen Sie Funktionen implementieren, damit MAPI und der MAPI-Spooler sich beim Nachrichtenspeicher Anbieter anmelden können.</span><span class="sxs-lookup"><span data-stu-id="f513b-106">After the wrapped PST store provider is configured, you must implement functions so that MAPI and the MAPI spooler can log on to the message store provider.</span></span> <span data-ttu-id="f513b-107">Weitere Informationen zum Initialisieren und Anmelden bei einem eingebundenen PST-Speicheranbieter finden Sie unter [Initialisieren eines EingebundenEN PST-Speicheranbieters](initializing-a-wrapped-pst-store-provider.md) und [Anmelden bei einem](logging-on-to-a-wrapped-pst-store-provider.md)eingebundenen PST-Speicheranbieter.</span><span class="sxs-lookup"><span data-stu-id="f513b-107">For more information about initializing and logging on to a wrapped PST store provider, see [Initializing a Wrapped PST Store Provider](initializing-a-wrapped-pst-store-provider.md) and [Logging On to a Wrapped PST Store Provider](logging-on-to-a-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="f513b-108">Die **[IMAPISupport:: IUnknown](imapisupportiunknown.md)** -Schnittstelle stellt Implementierungen für Aufgaben bereit, die häufig von Nachrichtenspeicher Anbietern ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f513b-108">The **[IMAPISupport::IUnknown](imapisupportiunknown.md)** interface provides implementations for tasks that are commonly performed by message store providers.</span></span> <span data-ttu-id="f513b-109">Diese Schnittstelle muss umbrochen werden, damit der beispielhafte PST-Speicheranbieter funktioniert.</span><span class="sxs-lookup"><span data-stu-id="f513b-109">This interface must be wrapped for the Sample Wrapped PST Store Provider to work.</span></span> <span data-ttu-id="f513b-110">Die **[IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md)** -Funktion erfordert eine spezielle Implementierung.</span><span class="sxs-lookup"><span data-stu-id="f513b-110">The **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** function requires special implementation.</span></span> <span data-ttu-id="f513b-111">Alle anderen Funktionen können Ihre Parameter an das zugrunde liegende Wrapped-Objekt übergeben.</span><span class="sxs-lookup"><span data-stu-id="f513b-111">All other functions can pass their parameters to the underlying wrapped object.</span></span> 
  
<span data-ttu-id="f513b-112">In diesem Thema wird die **IMAPISupport:: OpenProfileSection** -Funktion anhand eines Codebeispiels aus dem eingebundenen PST-Speicheranbieter demonstriert.</span><span class="sxs-lookup"><span data-stu-id="f513b-112">In this topic, the **IMAPISupport::OpenProfileSection** function is demonstrated by using a code example from the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="f513b-113">Im Beispiel wird ein eingebundener PST-Anbieter implementiert, der in Verbindung mit der Replikations-API verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f513b-113">The sample implements a wrapped PST provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="f513b-114">Weitere Informationen zum herunterladen und Installieren des eingeWickelten Beispiel-PST-Speicheranbieters finden Sie unter [Installing the Sample Wrapped Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f513b-114">For more information about downloading and installing the Sample Wrapped PST Store Provider, see [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span></span> <span data-ttu-id="f513b-115">Weitere Informationen zur Replikations-API finden Sie unter Informationen zur [Replikations-API](about-the-replication-api.md).</span><span class="sxs-lookup"><span data-stu-id="f513b-115">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
<span data-ttu-id="f513b-116">Wenn Sie einen eingebundenen PST-Speicheranbieter abgeschlossen haben, müssen Sie den eingebundenen PST-Speicheranbieter ordnungsgemäß herunterfahren.</span><span class="sxs-lookup"><span data-stu-id="f513b-116">When you finish using a wrapped PST store provider, you must properly shut down the wrapped PST store provider.</span></span> <span data-ttu-id="f513b-117">Weitere Informationen finden Sie unter [Herunterfahren eines EingebundenEN PST-Speicheranbieters](shutting-down-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f513b-117">For more information, see [Shutting Down a Wrapped PST Store Provider](shutting-down-a-wrapped-pst-store-provider.md).</span></span>
  
## <a name="open-profile-section-routine"></a><span data-ttu-id="f513b-118">Open profile section-Routine</span><span class="sxs-lookup"><span data-stu-id="f513b-118">Open Profile Section routine</span></span>

<span data-ttu-id="f513b-119">Die **[IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md)** -Funktion öffnet einen Abschnitt des aktuellen Profils.</span><span class="sxs-lookup"><span data-stu-id="f513b-119">The **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** function opens a section of the current profile.</span></span> <span data-ttu-id="f513b-120">Die Funktion erfordert eine besondere Behandlung in der eingebundenen PST-Speicheranbieter Implementierung.</span><span class="sxs-lookup"><span data-stu-id="f513b-120">The function requires special handling in the wrapped PST store provider implementation.</span></span> <span data-ttu-id="f513b-121">Wenn der `pgNSTGlobalProfileSectionGuid` angefordert wird, gibt die Funktion den Profil Abschnitt zurück, der zwischengespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="f513b-121">When the  `pgNSTGlobalProfileSectionGuid` is requested, the function returns the profile section that is cached.</span></span> 
  
### <a name="csupportopenprofilesection-example"></a><span data-ttu-id="f513b-122">CSupport:: OpenProfileSection ()-Beispiel</span><span class="sxs-lookup"><span data-stu-id="f513b-122">CSupport::OpenProfileSection() example</span></span>

```cpp
STDMETHODIMP CSupport::OpenProfileSection( 
    LPMAPIUID lpUid,     
    ULONG ulFlags, 
    LPPROFSECT * lppProfileObj) 
{ 
    Log(true,"CSupport::OpenProfileSection\n"); 
    if (lpUid &&  
        IsEqualMAPIUID(lpUid, (void *)&pbNSTGlobalProfileSectionGuid) &&  
        m_lpProfSect) 
    {      
        // Allow the opening of the Global Section 
        if (m_lpProfSect) 
        { 
            *lppProfileObj = m_lpProfSect; 
            (*lppProfileObj)->AddRef(); 
            return S_OK; 
        } 
    } 
    return m_pMAPISup->OpenProfileSection(lpUid, ulFlags, lppProfileObj); 
}
```

## <a name="see-also"></a><span data-ttu-id="f513b-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f513b-123">See also</span></span>

- [<span data-ttu-id="f513b-124">Informationen zum einGebundenen PST-Speicheranbieter</span><span class="sxs-lookup"><span data-stu-id="f513b-124">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md)
- [<span data-ttu-id="f513b-125">Installieren des eingeWickelten Beispiel-PST-Speicheranbieters</span><span class="sxs-lookup"><span data-stu-id="f513b-125">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md)
- [<span data-ttu-id="f513b-126">Initialisieren eines einGebundenen PST-Speicheranbieters</span><span class="sxs-lookup"><span data-stu-id="f513b-126">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="f513b-127">Anmelden bei einem einGebundenen PST-Speicheranbieter</span><span class="sxs-lookup"><span data-stu-id="f513b-127">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="f513b-128">Herunterfahren eines einGebundenen PST-Speicheranbieters</span><span class="sxs-lookup"><span data-stu-id="f513b-128">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)

