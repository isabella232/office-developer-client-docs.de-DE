---
title: Verwenden von einem gepackten PST-Anbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 98f08432-e86c-cba6-45fd-5a6c94d50aaf
description: 'Zuletzt geändert: 03 Juli 2012'
ms.openlocfilehash: 4a2ccbbcdd3459af6b69156d80b37695251ba8d6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795817"
---
# <a name="using-a-wrapped-pst-store-provider"></a><span data-ttu-id="ee617-103">Verwenden von einem gepackten PST-Anbieter</span><span class="sxs-lookup"><span data-stu-id="ee617-103">Using a wrapped PST store provider</span></span>

<span data-ttu-id="ee617-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ee617-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ee617-105">Bevor Sie einen gepackten Anbieter für Persönliche Ordner-Datei (PST) anmelden verwenden können, müssen Sie initialisieren und der gepackten PST-Informationsdienst konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="ee617-105">Before you can use a wrapped Personal Folders file (PST) store provider, you must initialize and configure the wrapped PST store provider.</span></span> <span data-ttu-id="ee617-106">Nachdem der gepackten PST-Speicher-Anbieter konfiguriert ist, müssen Sie Funktionen implementieren, sodass MAPI und die MAPI-Warteschlange auf die Nachricht-Anbieter anmelden können.</span><span class="sxs-lookup"><span data-stu-id="ee617-106">After the wrapped PST store provider is configured, you must implement functions so that MAPI and the MAPI spooler can log on to the message store provider.</span></span> <span data-ttu-id="ee617-107">Weitere Informationen zu initialisieren und Anmelden bei einem gepackten PST-Anbieter finden Sie unter [Initialisieren einer gewrappt PST Store Provider](initializing-a-wrapped-pst-store-provider.md) und [Protokollierung für den Zugriff auf einen umbrochen PST-speichern-Anbieter](logging-on-to-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="ee617-107">For more information about initializing and logging on to a wrapped PST store provider, see [Initializing a Wrapped PST Store Provider](initializing-a-wrapped-pst-store-provider.md) and [Logging On to a Wrapped PST Store Provider](logging-on-to-a-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="ee617-108">Die **[IMAPISupport::IUnknown](imapisupportiunknown.md)** -Schnittstelle stellt Implementierungen für die Nachricht häufig ausgeführten Aufgaben Anbieter.</span><span class="sxs-lookup"><span data-stu-id="ee617-108">The **[IMAPISupport::IUnknown](imapisupportiunknown.md)** interface provides implementations for tasks that are commonly performed by message store providers.</span></span> <span data-ttu-id="ee617-109">Diese Schnittstelle muss für den umfließendem PST Store Beispielanbieter funktioniert eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="ee617-109">This interface must be wrapped for the Sample Wrapped PST Store Provider to work.</span></span> <span data-ttu-id="ee617-110">Die Funktion **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** erfordert spezielle Implementierung.</span><span class="sxs-lookup"><span data-stu-id="ee617-110">The **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** function requires special implementation.</span></span> <span data-ttu-id="ee617-111">Alle anderen Funktionen können ihren Parametern an das zugrunde liegende gepackten Objekt übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="ee617-111">All other functions can pass their parameters to the underlying wrapped object.</span></span> 
  
<span data-ttu-id="ee617-112">In diesem Thema wird die Funktion **IMAPISupport::OpenProfileSection** mithilfe eines Codebeispiels aus der umbrochen PST Store Beispielanbieter veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="ee617-112">In this topic, the **IMAPISupport::OpenProfileSection** function is demonstrated by using a code example from the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="ee617-113">Das Beispiel implementiert einen gepackten PST-Anbieter, der in Verbindung mit der API für die Replikation verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ee617-113">The sample implements a wrapped PST provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="ee617-114">Weitere Informationen zum Herunterladen und Installieren der umbrochen PST Store Beispielanbieter finden Sie unter [Sample umfließendem PST Store Provider installieren](installing-the-sample-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="ee617-114">For more information about downloading and installing the Sample Wrapped PST Store Provider, see [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span></span> <span data-ttu-id="ee617-115">Weitere Informationen zur Replikation-API finden Sie unter [Über die Replikation-API](about-the-replication-api.md).</span><span class="sxs-lookup"><span data-stu-id="ee617-115">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
<span data-ttu-id="ee617-116">Wenn Sie fertig sind, mit einem gepackten PST-Anbieter, müssen Sie die gepackten PST-Speicheranbieter ordnungsgemäß herunterfahren.</span><span class="sxs-lookup"><span data-stu-id="ee617-116">When you finish using a wrapped PST store provider, you must properly shut down the wrapped PST store provider.</span></span> <span data-ttu-id="ee617-117">Weitere Informationen finden Sie unter [Herunterfahren nach unten ein umfließendem PST Store Anbieter](shutting-down-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="ee617-117">For more information, see [Shutting Down a Wrapped PST Store Provider](shutting-down-a-wrapped-pst-store-provider.md).</span></span>
  
## <a name="open-profile-section-routine"></a><span data-ttu-id="ee617-118">Open Benutzerprofilabschnitt routine</span><span class="sxs-lookup"><span data-stu-id="ee617-118">Open Profile Section routine</span></span>

<span data-ttu-id="ee617-119">Die **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** -Funktion wird das aktuelle Profil einen Abschnitt geöffnet.</span><span class="sxs-lookup"><span data-stu-id="ee617-119">The **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** function opens a section of the current profile.</span></span> <span data-ttu-id="ee617-120">Die Funktion erfordert besondere Behandlung in der gepackten PST-Speicher-Anbieter-Implementierung.</span><span class="sxs-lookup"><span data-stu-id="ee617-120">The function requires special handling in the wrapped PST store provider implementation.</span></span> <span data-ttu-id="ee617-121">Wenn die `pgNSTGlobalProfileSectionGuid` angefordert, Profilabschnitt, die zwischengespeichert wird von der Funktion zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ee617-121">When the  `pgNSTGlobalProfileSectionGuid` is requested, the function returns the profile section that is cached.</span></span> 
  
### <a name="csupportopenprofilesection-example"></a><span data-ttu-id="ee617-122">CSupport::OpenProfileSection()-Beispiel</span><span class="sxs-lookup"><span data-stu-id="ee617-122">CSupport::OpenProfileSection() example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="ee617-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ee617-123">See also</span></span>

- [<span data-ttu-id="ee617-124">Zum Beispiel umgebrochen PST-Anbieter</span><span class="sxs-lookup"><span data-stu-id="ee617-124">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md)
- [<span data-ttu-id="ee617-125">Installieren des Beispiels umfließendem PST-Anbieter</span><span class="sxs-lookup"><span data-stu-id="ee617-125">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md)
- [<span data-ttu-id="ee617-126">Initialisieren einen Anbieter für umbrochenen PST anmelden</span><span class="sxs-lookup"><span data-stu-id="ee617-126">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="ee617-127">Anmelden bei einem Anbieter gepackten PST-Datei</span><span class="sxs-lookup"><span data-stu-id="ee617-127">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="ee617-128">Herunterfahren von einem Anbieter gepackten PST-Datei</span><span class="sxs-lookup"><span data-stu-id="ee617-128">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)

