---
title: Benutzeroptionen für das schnelle Herunterfahren
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
api_type:
- COM
ms.assetid: 220aeab5-20f6-4520-96c9-8aaa0e8ea15b
description: 'Letzte Änderung: 26. Juni 2012'
localization_priority: Priority
ms.openlocfilehash: 3c60862733c6b38e60650ae9daba9bba578fcd58
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716369"
---
# <a name="fast-shutdown-user-options"></a><span data-ttu-id="e4ad6-103">Benutzeroptionen für das schnelle Herunterfahren</span><span class="sxs-lookup"><span data-stu-id="e4ad6-103">Fast shutdown user options</span></span>

<span data-ttu-id="e4ad6-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e4ad6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e4ad6-105">In diesem Thema werden die drei Windows-Registrierungseinstellungen beschrieben, die ab Microsoft Outlook 2010 und jetzt bis einschließlich Microsoft Outlook 2013 für das schnelle Herunterfahren von MAPI-Clients eines Benutzers verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="e4ad6-105">This topic describes the three Windows registry settings that are available, starting in Microsoft Outlook 2010 and now including Microsoft Outlook 2013, for fast shutdown of a user's MAPI clients.</span></span> <span data-ttu-id="e4ad6-106">Administratoren können mithilfe dieser Registrierungseinstellungen das bevorzugte Clientverhalten beim Herunterfahren abhängig von der vom MAPI-Anbieter angebotenen Unterstützung für das schnelle Herunterfahren des Clients angeben.</span><span class="sxs-lookup"><span data-stu-id="e4ad6-106">Administrators can use these registry settings to specify the preferred client shutdown behavior depending on the MAPI providers' support for client fast shutdown.</span></span> <span data-ttu-id="e4ad6-107">Die Einstellung des Administrators bestimmt wiederum, wie das MAPI-Subsystem auf den Aufruf des MAPI-Clients von [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) in Bezug auf die verfügbare Unterstützung für schnelles Herunterfahren reagiert.</span><span class="sxs-lookup"><span data-stu-id="e4ad6-107">The administrator's setting, in turn, determines how the MAPI subsystem responds to the MAPI client's call to [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) in terms of available fast shutdown support.</span></span> 
  
<span data-ttu-id="e4ad6-108">Eine Registrierungseinstellung spiegelt zwar die bevorzugte Einstellung des Administrators für das schnelle Herunterfahren aller MAPI-Clients auf Benutzerebene wider, ein MAPI-Cliententwickler kann jedoch entscheiden, ob der Client schnelles Herunterfahren unabhängig von anderen MAPI-Clients und der Registrierungseinstellung des Administrators unterstützen soll.</span><span class="sxs-lookup"><span data-stu-id="e4ad6-108">Even though a registry setting reflects the administrator's preference at the user level for fast shutdown for all MAPI clients, a MAPI client developer can decide whether the client supports fast shutdown independently of other MAPI clients and the administrator's registry setting.</span></span> <span data-ttu-id="e4ad6-109">Aber damit das schnelle Herunterfahren erfolgreich ausgeführt wird, muss der Benutzer die erforderliche Registrierungseinstellung festgelegt haben, ein MAPI-Client muss das schnelle Herunterfahren mithilfe der Schnittstelle [IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md) initiieren, und MAPI-Anbieter, die mit dem Client arbeiten, müssen die Schnittstelle [IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md) implementieren, um das schnelle Herunterfahren des Clients zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="e4ad6-109">Nonetheless, for fast shutdown to take place successfully, the user must have the necessary registry setting, a MAPI client must initiate the fast shutdown by using the [IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md) interface, and MAPI providers that work with the client should implement the [IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md) interface to support client fast shutdown.</span></span> 
  
<span data-ttu-id="e4ad6-110">In der folgenden Liste sind diese drei Optionen auf Benutzerebene beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e4ad6-110">The following list describes the three user-level options.</span></span>
  
### <a name="option-1-the-mapi-subsystem-enables-fast-shutdown-unless-mapi-providers-explicitly-opt-out"></a><span data-ttu-id="e4ad6-111">Option 1: Das MAPI-Subsystem ermöglicht schnelles Herunterfahren, sofern die MAPI-Anbieter dies nicht explizit deaktivieren</span><span class="sxs-lookup"><span data-stu-id="e4ad6-111">Option 1: The MAPI subsystem enables fast shutdown, unless MAPI providers explicitly opt out</span></span> 
    
<span data-ttu-id="e4ad6-112">Ab Outlook 2010 handelt es sich dabei um das Standardverhalten, wenn Outlook der MAPI-Client ist. Bei anderen MAPI-Clients stellt das nicht unbedingt das Standardverhalten dar.</span><span class="sxs-lookup"><span data-stu-id="e4ad6-112">Starting in Outlook 2010, this is the default behavior when Outlook is the MAPI client; it is not necessarily the default behavior for other MAPI clients.</span></span> <span data-ttu-id="e4ad6-113">Um diese Option für Outlook explizit anzugeben, können Administratoren den folgenden Registrierungsschlüssel und -wert festlegen.</span><span class="sxs-lookup"><span data-stu-id="e4ad6-113">To explicitly specify this option for Outlook, administrators can choose to set the following registry key and value.</span></span>
    
<span data-ttu-id="e4ad6-114">Registrierungsschlüssel:</span><span class="sxs-lookup"><span data-stu-id="e4ad6-114"> registry key</span></span>
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
<span data-ttu-id="e4ad6-115">Wert:</span><span class="sxs-lookup"><span data-stu-id="e4ad6-115">Value</span></span>
  
>  `"FastShutdownBehavior"=dword:00000000`
    
<span data-ttu-id="e4ad6-116">Wenn ein MAPI-Client schnelles Herunterfahren initiiert und **IMAPIClientShutdown::QueryFastShutdown** aufruft, um Unterstützung für schnelles Herunterfahren abzufragen, antwortet das MAPI-Subsystem auf die Abfrage mit der Rückgabe von S\_OK, sofern kein MAPI-Anbieter, der über eine aktive MAPI-Sitzung mit dem MAPI-Client verfügt, die Unterstützung für schnelles Herunterfahren explizit deaktiviert hat.</span><span class="sxs-lookup"><span data-stu-id="e4ad6-116">When a MAPI client initiates a fast shutdown and calls **IMAPIClientShutdown::QueryFastShutdown** to query for fast shutdown support, the MAPI subsystem responds to the query by returning S\_OK as long as no MAPI provider that has an active MAPI session with the MAPI client has explicitly opted out of fast shutdown support.</span></span> 

<span data-ttu-id="e4ad6-117">Ein MAPI-Anbieter deaktiviert schnelles Herunterfahren, indem er die Methode [IMAPIProviderShutdown::QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) zur Rückgabe eines Fehlers (MAPI\_E\_NO\_SUPPORT) implementiert.</span><span class="sxs-lookup"><span data-stu-id="e4ad6-117">A MAPI provider opts out of fast shutdown by implementing the [IMAPIProviderShutdown::QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) method to return an error (MAPI\_E\_NO\_SUPPORT).</span></span> <span data-ttu-id="e4ad6-118">Wenn ein oder mehrere MAPI-Anbieter einen Fehler in **IMAPIProviderShutdown::QueryFastShutdown** zurückgeben, gibt das MAPI-Subsystem MAPI_\E_\NO\_SUPPORT an **IMAPIClientShutdown::QueryFastShutdown** zurück.</span><span class="sxs-lookup"><span data-stu-id="e4ad6-118">If one or more MAPI providers return an error in **IMAPIProviderShutdown::QueryFastShutdown**, the MAPI subsystem returns MAPI_\E_\NO\_SUPPORT to **IMAPIClientShutdown::QueryFastShutdown**.</span></span> 

<span data-ttu-id="e4ad6-119">Sofern ein MAPI-Anbieter die Option nicht deaktiviert, gibt das MAPI-Subsystem S\_OK zurück, auch wenn ein oder mehrere Anbieter die Schnittstelle **IMAPIProviderShutdown : IUnknown** nicht implementiert haben.</span><span class="sxs-lookup"><span data-stu-id="e4ad6-119">Unless a MAPI provider opts out, the MAPI subsystem returns S\_OK, even if one or more providers have not implemented the **IMAPIProviderShutdown : IUnknown** interface.</span></span> 
    
### <a name="option-2-the-mapi-subsystem-enables-fast-shutdown-only-if-every-mapi-provider-explicitly-opts-in"></a><span data-ttu-id="e4ad6-120">Option 2: Das MAPI-Subsystem ermöglicht schnelles Herunterfahren nur, wenn jeder MAPI-Anbieter dies explizit aktiviert</span><span class="sxs-lookup"><span data-stu-id="e4ad6-120">Option 2: The MAPI subsystem enables fast shutdown only if every MAPI provider explicitly opts in</span></span> 
    
<span data-ttu-id="e4ad6-121">Administratoren müssen den folgenden Registrierungsschlüssel und -wert explizit festlegen, um diese Einstellung für das schnelle Herunterfahren des Clients anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e4ad6-121">Administrators must explicitly set the following registry key and value to specify this preference for client fast shutdown.</span></span>
    
<span data-ttu-id="e4ad6-122">Registrierungsschlüssel:</span><span class="sxs-lookup"><span data-stu-id="e4ad6-122"> registry key</span></span>
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
<span data-ttu-id="e4ad6-123">Wert:</span><span class="sxs-lookup"><span data-stu-id="e4ad6-123">Value</span></span>
  
>  `"FastShutdownBehavior"=dword:00000001`
    
<span data-ttu-id="e4ad6-124">Wenn ein MAPI-Client schnelles Herunterfahren initiiert und **IMAPIClientShutdown::QueryFastShutdown** aufruft, um Unterstützung für schnelles Herunterfahren abzufragen, antwortet das MAPI-Subsystem auf die Abfrage mit der Rückgabe von S\_OK, wenn alle MAPI-Anbieter, die über aktive Sitzungen mit dem MAPI-Client verfügen, schnelles Herunterfahren unterstützen.</span><span class="sxs-lookup"><span data-stu-id="e4ad6-124">When a MAPI client initiates a fast shutdown and calls **IMAPIClientShutdown::QueryFastShutdown** to query for fast shutdown support, the MAPI subsystem responds to the query by returning S\_OK if all MAPI providers that have active sessions with the MAPI client support fast shutdown.</span></span> <span data-ttu-id="e4ad6-125">Ein MAPI-Anbieter demonstriert seine Unterstützung, indem er **IMAPIProviderShutdown::QueryFastShutdown** zur Rückgabe eines Nicht-Fehlercodes (S\_OK) implementiert.</span><span class="sxs-lookup"><span data-stu-id="e4ad6-125">A MAPI provider demonstrates its support by implementing **IMAPIProviderShutdown::QueryFastShutdown** to return a non-error code (S\_OK).</span></span> 

<span data-ttu-id="e4ad6-126">Wenn ein oder mehrere MAPI-Anbieter MAPI\_E\_NO\_SUPPORT zurückgeben oder **IMAPIProviderShutdown::QueryFastShutdown** nicht implementieren, gibt das MAPI-Subsystem einen Fehlercode an **IMAPIClientShutdown::QueryFastShutdown** zurück.</span><span class="sxs-lookup"><span data-stu-id="e4ad6-126">If one or more such MAPI providers return MAPI\_E\_NO\_SUPPORT, or do not implement **IMAPIProviderShutdown::QueryFastShutdown**, the MAPI subsystem returns an error code to **IMAPIClientShutdown::QueryFastShutdown**.</span></span>
    
### <a name="option-3-an-administrator-disables-support-for-client-fast-shutdown"></a><span data-ttu-id="e4ad6-127">Option 3: Ein Administrator deaktiviert die Unterstützung für das schnelle Herunterfahren des Clients</span><span class="sxs-lookup"><span data-stu-id="e4ad6-127">Option 3: An administrator disables support for client fast shutdown</span></span>
    
<span data-ttu-id="e4ad6-128">Administratoren müssen den folgenden Registrierungsschlüssel und -wert explizit festlegen, um die Unterstützung für das schnelle Herunterfahren des Clients zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="e4ad6-128">Administrators must explicitly set the following registry key and value to disable support for client fast shutdown.</span></span>
    
<span data-ttu-id="e4ad6-129">Registrierungsschlüssel:</span><span class="sxs-lookup"><span data-stu-id="e4ad6-129"> registry key</span></span>
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
<span data-ttu-id="e4ad6-130">Wert:</span><span class="sxs-lookup"><span data-stu-id="e4ad6-130">Value</span></span>
  
>  `"FastShutdownBehavior"=dword:00000002`
    
<span data-ttu-id="e4ad6-131">Wenn ein MAPI-Client schnelles Herunterfahren initiiert und **IMAPIClientShutdown::QueryFastShutdown** aufruft, um Unterstützung für schnelles Herunterfahren abzufragen, antwortet das MAPI-Subsystem auf die Abfrage mit der Rückgabe von MAPI_E_NO_SUPPORT, und zwar unabhängig davon, ob die MAPI-Anbieter schnelles Herunterfahren unterstützen.</span><span class="sxs-lookup"><span data-stu-id="e4ad6-131">When a MAPI client initiates a fast shutdown and calls **IMAPIClientShutdown::QueryFastShutdown** to query for fast shutdown support, the MAPI subsystem responds to the query by returning MAPI_E_NO_SUPPORT, regardless of whether any MAPI provider supports fast shutdown.</span></span> <span data-ttu-id="e4ad6-132">Bei dieser Registrierungseinstellung ruft das MAPI-Subsystem niemals die Methode **IMAPIProviderShutdown::QueryFastShutdown** oder [IMAPIProviderShutdown::DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) eines Anbieters auf.</span><span class="sxs-lookup"><span data-stu-id="e4ad6-132">Under this registry setting, the MAPI subsystem never calls the **IMAPIProviderShutdown::QueryFastShutdown** or [IMAPIProviderShutdown::DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) method of any of the providers.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="e4ad6-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e4ad6-133">See also</span></span>

- [<span data-ttu-id="e4ad6-134">Herunterfahren von Clients in MAPI</span><span class="sxs-lookup"><span data-stu-id="e4ad6-134">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)
- [<span data-ttu-id="e4ad6-135">Übersicht über das schnelle Herunterfahren</span><span class="sxs-lookup"><span data-stu-id="e4ad6-135">Fast shutdown overview</span></span>](fast-shutdown-overview.md)
- [<span data-ttu-id="e4ad6-136">Bewährte Methoden für das schnelle Herunterfahren</span><span class="sxs-lookup"><span data-stu-id="e4ad6-136">Best practices for fast shutdown</span></span>](best-practices-for-fast-shutdown.md)

