---
title: Schnelles Herunterfahren Benutzeroptionen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 220aeab5-20f6-4520-96c9-8aaa0e8ea15b
description: 'Zuletzt geändert: 26 Juni 2012'
ms.openlocfilehash: a58f8b98ab2f5a5c1028440676a561427272d028
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791654"
---
# <a name="fast-shutdown-user-options"></a><span data-ttu-id="fd955-103">Schnelles Herunterfahren Benutzeroptionen</span><span class="sxs-lookup"><span data-stu-id="fd955-103">Fast shutdown user options</span></span>

<span data-ttu-id="fd955-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fd955-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fd955-105">In diesem Thema werden die drei Windows-registrierungseinstellungen, die verfügbar sind, beginnend in Microsoft Outlook 2010 und jetzt einschließlich Microsoft Outlook 2013 für Schnelles Herunterfahren von MAPI-Clients des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="fd955-105">This topic describes the three Windows registry settings that are available, starting in Microsoft Outlook 2010 and now including Microsoft Outlook 2013, for fast shutdown of a user's MAPI clients.</span></span> <span data-ttu-id="fd955-106">Administratoren können diese Registrierungseinträge verwenden, um das bevorzugte Client Herunterfahren Verhalten je nach der MAPI-Anbieter Unterstützung für schnelle Herunterfahren von Clients anzugeben.</span><span class="sxs-lookup"><span data-stu-id="fd955-106">Administrators can use these registry settings to specify the preferred client shutdown behavior depending on the MAPI providers' support for client fast shutdown.</span></span> <span data-ttu-id="fd955-107">Des Administrators festlegen, wiederum bestimmt, wie das MAPI-Subsystem Aufruf [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) im Hinblick auf die verfügbaren Schnelles Herunterfahren Unterstützung der MAPI-Client reagiert.</span><span class="sxs-lookup"><span data-stu-id="fd955-107">The administrator's setting, in turn, determines how the MAPI subsystem responds to the MAPI client's call to [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) in terms of available fast shutdown support.</span></span> 
  
<span data-ttu-id="fd955-108">Obwohl eine Einstellung in der Registrierung des Administrators Voreinstellung auf Benutzerebene für Schnelles Herunterfahren für alle MAPI-Clients wiedergibt, kann ein MAPI-Client-Entwickler entscheiden Sie, ob der Client Schnelles Herunterfahren unabhängig von anderen MAPI-Clients unterstützt und die registrierungseinstellung des Administrators.</span><span class="sxs-lookup"><span data-stu-id="fd955-108">Even though a registry setting reflects the administrator's preference at the user level for fast shutdown for all MAPI clients, a MAPI client developer can decide whether the client supports fast shutdown independently of other MAPI clients and the administrator's registry setting.</span></span> <span data-ttu-id="fd955-109">Dennoch für Schnelles Herunterfahren erfolgreich, stattfinden muss der Benutzer die Einstellung der erforderlichen Registrierung verfügen, die ein MAPI-Client muss das schnelle Herunterfahren initiiert werden mithilfe der [IMAPIClientShutdown: IUnknown](imapiclientshutdowniunknown.md) Schnittstelle und MAPI-Anbieter, die Arbeit mit der Client sollte Implementieren der [IMAPIProviderShutdown: IUnknown](imapiprovidershutdowniunknown.md) -Schnittstelle für das schnelle Herunterfahren von Clients unterstützen.</span><span class="sxs-lookup"><span data-stu-id="fd955-109">Nonetheless, for fast shutdown to take place successfully, the user must have the necessary registry setting, a MAPI client must initiate the fast shutdown by using the [IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md) interface, and MAPI providers that work with the client should implement the [IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md) interface to support client fast shutdown.</span></span> 
  
<span data-ttu-id="fd955-110">In der folgenden Liste werden die drei Optionen auf Benutzerebene beschrieben.</span><span class="sxs-lookup"><span data-stu-id="fd955-110">The following list describes the three user-level options.</span></span>
  
### <a name="option-1-the-mapi-subsystem-enables-fast-shutdown-unless-mapi-providers-explicitly-opt-out"></a><span data-ttu-id="fd955-111">Option 1: Ermöglicht das MAPI-Subsystem Schnelles Herunterfahren, wenn MAPI-Anbieter explizit Aufheben der Bestätigung</span><span class="sxs-lookup"><span data-stu-id="fd955-111">Option 1: The MAPI subsystem enables fast shutdown, unless MAPI providers explicitly opt out</span></span> 
    
<span data-ttu-id="fd955-112">Starten in Outlook 2010, ist dies das Standardverhalten, wenn Outlook MAPI-Client ist; Es ist nicht unbedingt das Standardverhalten für andere MAPI-Clients.</span><span class="sxs-lookup"><span data-stu-id="fd955-112">Starting in Outlook 2010, this is the default behavior when Outlook is the MAPI client; it is not necessarily the default behavior for other MAPI clients.</span></span> <span data-ttu-id="fd955-113">Wenn Sie diese Option für Outlook explizit angeben, können Administratoren auch den folgenden Registrierungsschlüssel und den Wert festzulegen.</span><span class="sxs-lookup"><span data-stu-id="fd955-113">To explicitly specify this option for Outlook, administrators can choose to set the following registry key and value.</span></span>
    
<span data-ttu-id="fd955-114">Registrierungsschlüssel:</span><span class="sxs-lookup"><span data-stu-id="fd955-114">Registry key:</span></span>
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
<span data-ttu-id="fd955-115">Wert:</span><span class="sxs-lookup"><span data-stu-id="fd955-115">Value:</span></span>
  
>  `"FastShutdownBehavior"=dword:00000000`
    
<span data-ttu-id="fd955-116">Wenn ein MAPI-Client ein Schnelles Herunterfahren initiiert und **IMAPIClientShutdown::QueryFastShutdown** Abfrage für Schnelles Herunterfahren Support Ruft, antwortet des MAPI-Subsystems auf die Abfrage durch Rückgabe S\_solange keine MAPI-Anbieter, der eine aktive MAPI wurde auf OK Sitzung mit der MAPI-Client wurde nicht mehr unterstützt Schnelles Herunterfahren explizit bestätigt.</span><span class="sxs-lookup"><span data-stu-id="fd955-116">When a MAPI client initiates a fast shutdown and calls **IMAPIClientShutdown::QueryFastShutdown** to query for fast shutdown support, the MAPI subsystem responds to the query by returning S\_OK as long as no MAPI provider that has an active MAPI session with the MAPI client has explicitly opted out of fast shutdown support.</span></span> 

<span data-ttu-id="fd955-117">Ein MAPI-Anbieter nicht genügend Schnelles Herunterfahren entscheidet, durch die Implementierung der [IMAPIProviderShutdown::QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) -Methode, um einen Fehler zurück (MAPI\_E\_NO\_Unterstützung).</span><span class="sxs-lookup"><span data-stu-id="fd955-117">A MAPI provider opts out of fast shutdown by implementing the [IMAPIProviderShutdown::QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) method to return an error (MAPI\_E\_NO\_SUPPORT).</span></span> <span data-ttu-id="fd955-118">Wenn eine oder mehrere MAPI-Anbieter in **IMAPIProviderShutdown::QueryFastShutdown**einen Fehler zurück, gibt MAPI-Subsystems MAPI_\E_\NO\_SUPPORT zur **IMAPIClientShutdown::QueryFastShutdown**.</span><span class="sxs-lookup"><span data-stu-id="fd955-118">If one or more MAPI providers return an error in **IMAPIProviderShutdown::QueryFastShutdown**, the MAPI subsystem returns MAPI_\E_\NO\_SUPPORT to **IMAPIClientShutdown::QueryFastShutdown**.</span></span> 

<span data-ttu-id="fd955-119">Es sei denn, ein MAPI-Anbieter, die MAPI-Subsystems gibt S entscheidet\_auf OK, auch wenn eine oder mehrere Anbieter nicht implementiert haben die **IMAPIProviderShutdown: IUnknown** Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="fd955-119">Unless a MAPI provider opts out, the MAPI subsystem returns S\_OK, even if one or more providers have not implemented the **IMAPIProviderShutdown : IUnknown** interface.</span></span> 
    
### <a name="option-2-the-mapi-subsystem-enables-fast-shutdown-only-if-every-mapi-provider-explicitly-opts-in"></a><span data-ttu-id="fd955-120">Option 2: MAPI-Subsystems ermöglicht Schnelles Herunterfahren nur, wenn alle MAPI-Anbieter explizit in entscheidet</span><span class="sxs-lookup"><span data-stu-id="fd955-120">Option 2: The MAPI subsystem enables fast shutdown only if every MAPI provider explicitly opts in</span></span> 
    
<span data-ttu-id="fd955-121">Administratoren müssen die folgenden Registrierungsschlüssel und den Wert an, diese Einstellung für das schnelle Herunterfahren von Client explizit festlegen.</span><span class="sxs-lookup"><span data-stu-id="fd955-121">Administrators must explicitly set the following registry key and value to specify this preference for client fast shutdown.</span></span>
    
<span data-ttu-id="fd955-122">Registrierungsschlüssel:</span><span class="sxs-lookup"><span data-stu-id="fd955-122">Registry key:</span></span>
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
<span data-ttu-id="fd955-123">Wert:</span><span class="sxs-lookup"><span data-stu-id="fd955-123">Value:</span></span>
  
>  `"FastShutdownBehavior"=dword:00000001`
    
<span data-ttu-id="fd955-124">Wenn ein MAPI-Client ein Schnelles Herunterfahren initiiert und **IMAPIClientShutdown::QueryFastShutdown** Abfrage für Schnelles Herunterfahren Support Ruft, antwortet des MAPI-Subsystems auf die Abfrage durch Rückgabe S\_OK, wenn alle MAPI-Anbieter mit aktiver Sitzungen mit die MAPI-Client-Unterstützung Schnelles Herunterfahren.</span><span class="sxs-lookup"><span data-stu-id="fd955-124">When a MAPI client initiates a fast shutdown and calls **IMAPIClientShutdown::QueryFastShutdown** to query for fast shutdown support, the MAPI subsystem responds to the query by returning S\_OK if all MAPI providers that have active sessions with the MAPI client support fast shutdown.</span></span> <span data-ttu-id="fd955-125">Ein MAPI-Anbieter veranschaulicht die Unterstützung durch die Implementierung von **IMAPIProviderShutdown::QueryFastShutdown** , um einen Fehlercode zurück (S\_OK).</span><span class="sxs-lookup"><span data-stu-id="fd955-125">A MAPI provider demonstrates its support by implementing **IMAPIProviderShutdown::QueryFastShutdown** to return a non-error code (S\_OK).</span></span> 

<span data-ttu-id="fd955-126">Wenn solche MAPI-Anbieter einen oder mehrere MAPI zurückgeben\_E\_NO\_SUPPORT, oder **IMAPIProviderShutdown::QueryFastShutdown**, nicht zu implementieren des MAPI-Subsystems gibt einen Fehlercode an **IMAPIClientShutdown::QueryFastShutdown** zurück. .</span><span class="sxs-lookup"><span data-stu-id="fd955-126">If one or more such MAPI providers return MAPI\_E\_NO\_SUPPORT, or do not implement **IMAPIProviderShutdown::QueryFastShutdown**, the MAPI subsystem returns an error code to **IMAPIClientShutdown::QueryFastShutdown**.</span></span>
    
### <a name="option-3-an-administrator-disables-support-for-client-fast-shutdown"></a><span data-ttu-id="fd955-127">Option 3: Administrator deaktiviert die Unterstützung für schnelle Herunterfahren von Clients</span><span class="sxs-lookup"><span data-stu-id="fd955-127">Option 3: An administrator disables support for client fast shutdown</span></span>
    
<span data-ttu-id="fd955-128">Administratoren müssen die folgenden Registrierungsschlüssel und Deaktivieren der Unterstützung für das schnelle Herunterfahren von Client-Wert explizit festlegen.</span><span class="sxs-lookup"><span data-stu-id="fd955-128">Administrators must explicitly set the following registry key and value to disable support for client fast shutdown.</span></span>
    
<span data-ttu-id="fd955-129">Registrierungsschlüssel:</span><span class="sxs-lookup"><span data-stu-id="fd955-129">Registry key:</span></span>
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
<span data-ttu-id="fd955-130">Wert:</span><span class="sxs-lookup"><span data-stu-id="fd955-130">Value:</span></span>
  
>  `"FastShutdownBehavior"=dword:00000002`
    
<span data-ttu-id="fd955-131">Wenn ein MAPI-Client ein Schnelles Herunterfahren initiiert und **IMAPIClientShutdown::QueryFastShutdown** Abfrage für Schnelles Herunterfahren Support Ruft, antwortet des MAPI-Subsystems auf die Abfrage durch Rückgabe MAPI_E_NO_SUPPORT, unabhängig davon, ob ein MAPI-Anbieter unterstützt die schnelle Herunterfahren.</span><span class="sxs-lookup"><span data-stu-id="fd955-131">When a MAPI client initiates a fast shutdown and calls **IMAPIClientShutdown::QueryFastShutdown** to query for fast shutdown support, the MAPI subsystem responds to the query by returning MAPI_E_NO_SUPPORT, regardless of whether any MAPI provider supports fast shutdown.</span></span> <span data-ttu-id="fd955-132">Bei dieser registrierungseinstellung ruft des MAPI-Subsystems nie die **IMAPIProviderShutdown::QueryFastShutdown** oder [IMAPIProviderShutdown::DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) -Methode der Anbieter.</span><span class="sxs-lookup"><span data-stu-id="fd955-132">Under this registry setting, the MAPI subsystem never calls the **IMAPIProviderShutdown::QueryFastShutdown** or [IMAPIProviderShutdown::DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) method of any of the providers.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="fd955-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd955-133">See also</span></span>

- [<span data-ttu-id="fd955-134">Herunterfahren von Clients in MAPI</span><span class="sxs-lookup"><span data-stu-id="fd955-134">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)
- [<span data-ttu-id="fd955-135">Schnelles Herunterfahren (Übersicht)</span><span class="sxs-lookup"><span data-stu-id="fd955-135">Fast Shutdown Overview</span></span>](fast-shutdown-overview.md)
- [<span data-ttu-id="fd955-136">Bewährte Methoden für das schnelle Herunterfahren</span><span class="sxs-lookup"><span data-stu-id="fd955-136">Best Practices for Fast Shutdown</span></span>](best-practices-for-fast-shutdown.md)

