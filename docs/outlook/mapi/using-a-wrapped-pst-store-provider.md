---
title: Verwenden eines Anbieters von umschlossenem PST-Speicher
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 98f08432-e86c-cba6-45fd-5a6c94d50aaf
description: 'Letzte Änderung: 03. Juli 2012'
ms.openlocfilehash: b7c651044ab7f4cad7032db69e157c9a3589bde9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420822"
---
# <a name="using-a-wrapped-pst-store-provider"></a><span data-ttu-id="a6f8a-103">Verwenden eines Anbieters von umschlossenem PST-Speicher</span><span class="sxs-lookup"><span data-stu-id="a6f8a-103">Using a wrapped PST store provider</span></span>

<span data-ttu-id="a6f8a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a6f8a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a6f8a-105">Bevor Sie einen umschlossenen Anbieter für persönliche Ordner (PST)-Speicher verwenden können, müssen Sie den umschlossenen ANBIETER für den PST-Speicher initialisieren und konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="a6f8a-105">Before you can use a wrapped Personal Folders file (PST) store provider, you must initialize and configure the wrapped PST store provider.</span></span> <span data-ttu-id="a6f8a-106">Nachdem der umschlossene PST Store-Anbieter konfiguriert wurde, müssen Sie Funktionen implementieren, damit sich MAPI und der MAPI-Spooler beim Nachrichtenspeicheranbieter anmelden können.</span><span class="sxs-lookup"><span data-stu-id="a6f8a-106">After the wrapped PST store provider is configured, you must implement functions so that MAPI and the MAPI spooler can log on to the message store provider.</span></span> <span data-ttu-id="a6f8a-107">Weitere Informationen zum Initialisieren und Anmelden bei einem umschlossenen PST Store-Anbieter finden Sie unter [Initializing a Wrapped PST Store Provider](initializing-a-wrapped-pst-store-provider.md) und [Logging On to a Wrapped PST Store Provider](logging-on-to-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a6f8a-107">For more information about initializing and logging on to a wrapped PST store provider, see [Initializing a Wrapped PST Store Provider](initializing-a-wrapped-pst-store-provider.md) and [Logging On to a Wrapped PST Store Provider](logging-on-to-a-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="a6f8a-108">Die **[IMAPISupport::IUnknown-Schnittstelle](imapisupportiunknown.md)** stellt Implementierungen für Aufgaben bereit, die häufig von Nachrichtenspeicheranbietern ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a6f8a-108">The **[IMAPISupport::IUnknown](imapisupportiunknown.md)** interface provides implementations for tasks that are commonly performed by message store providers.</span></span> <span data-ttu-id="a6f8a-109">Diese Schnittstelle muss umschlossen werden, damit der Beispielanbieter für umschlossenes PST Store funktioniert.</span><span class="sxs-lookup"><span data-stu-id="a6f8a-109">This interface must be wrapped for the Sample Wrapped PST Store Provider to work.</span></span> <span data-ttu-id="a6f8a-110">Die **[IMAPISupport::OpenProfileSection-Funktion](imapisupport-openprofilesection.md)** erfordert eine spezielle Implementierung.</span><span class="sxs-lookup"><span data-stu-id="a6f8a-110">The **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** function requires special implementation.</span></span> <span data-ttu-id="a6f8a-111">Alle anderen Funktionen können ihre Parameter an das zugrunde liegende umschlossene Objekt übergeben.</span><span class="sxs-lookup"><span data-stu-id="a6f8a-111">All other functions can pass their parameters to the underlying wrapped object.</span></span> 
  
<span data-ttu-id="a6f8a-112">In diesem Thema wird die **IMAPISupport::OpenProfileSection-Funktion** mithilfe eines Codebeispiels aus dem Beispiel umschlossenen PST-Store demonstriert.</span><span class="sxs-lookup"><span data-stu-id="a6f8a-112">In this topic, the **IMAPISupport::OpenProfileSection** function is demonstrated by using a code example from the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="a6f8a-113">Das Beispiel implementiert einen umschlossenen PST-Anbieter, der in Verbindung mit der Replikations-API verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a6f8a-113">The sample implements a wrapped PST provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="a6f8a-114">Weitere Informationen zum Herunterladen und Installieren des Beispielanbieters für umbrochene PST Store finden Sie unter [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a6f8a-114">For more information about downloading and installing the Sample Wrapped PST Store Provider, see [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span></span> <span data-ttu-id="a6f8a-115">Weitere Informationen zur Replikations-API finden Sie unter [Informationen zur Replikations-API](about-the-replication-api.md).</span><span class="sxs-lookup"><span data-stu-id="a6f8a-115">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
<span data-ttu-id="a6f8a-116">Wenn Sie die Verwendung eines umschlossenen PST Store-Anbieters abgeschlossen haben, müssen Sie den umschlossenen ANBIETER für den PST Store ordnungsgemäß herunterfahren.</span><span class="sxs-lookup"><span data-stu-id="a6f8a-116">When you finish using a wrapped PST store provider, you must properly shut down the wrapped PST store provider.</span></span> <span data-ttu-id="a6f8a-117">Weitere Informationen finden Sie unter [Shutting Down a Wrapped PST Store Provider](shutting-down-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a6f8a-117">For more information, see [Shutting Down a Wrapped PST Store Provider](shutting-down-a-wrapped-pst-store-provider.md).</span></span>
  
## <a name="open-profile-section-routine"></a><span data-ttu-id="a6f8a-118">Open Profile Section-Routine</span><span class="sxs-lookup"><span data-stu-id="a6f8a-118">Open Profile Section routine</span></span>

<span data-ttu-id="a6f8a-119">Die **[IMAPISupport::OpenProfileSection-Funktion](imapisupport-openprofilesection.md)** öffnet einen Abschnitt des aktuellen Profils.</span><span class="sxs-lookup"><span data-stu-id="a6f8a-119">The **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** function opens a section of the current profile.</span></span> <span data-ttu-id="a6f8a-120">Die Funktion erfordert eine spezielle Behandlung in der Implementierung des umschlossenen PST Store-Anbieters.</span><span class="sxs-lookup"><span data-stu-id="a6f8a-120">The function requires special handling in the wrapped PST store provider implementation.</span></span> <span data-ttu-id="a6f8a-121">Wenn der  `pgNSTGlobalProfileSectionGuid` angefordert wird, gibt die Funktion den zwischengespeicherten Profilabschnitt zurück.</span><span class="sxs-lookup"><span data-stu-id="a6f8a-121">When the  `pgNSTGlobalProfileSectionGuid` is requested, the function returns the profile section that is cached.</span></span> 
  
### <a name="csupportopenprofilesection-example"></a><span data-ttu-id="a6f8a-122">CSupport::OpenProfileSection()-Beispiel</span><span class="sxs-lookup"><span data-stu-id="a6f8a-122">CSupport::OpenProfileSection() example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="a6f8a-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a6f8a-123">See also</span></span>

- [<span data-ttu-id="a6f8a-124">Informationen zum Beispiel umschlossenen STORE Anbieter</span><span class="sxs-lookup"><span data-stu-id="a6f8a-124">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md)
- [<span data-ttu-id="a6f8a-125">Installieren des Umschlossenen Store -Beispielanbieters</span><span class="sxs-lookup"><span data-stu-id="a6f8a-125">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md)
- [<span data-ttu-id="a6f8a-126">Initialisieren eines umschlossenen STORE Anbieters</span><span class="sxs-lookup"><span data-stu-id="a6f8a-126">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="a6f8a-127">Anmelden bei einem umschlossenen STORE Anbieter</span><span class="sxs-lookup"><span data-stu-id="a6f8a-127">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="a6f8a-128">Herunterfahren eines umschlossenen STORE Anbieters</span><span class="sxs-lookup"><span data-stu-id="a6f8a-128">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)

