---
title: IXPLogonValidateState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.ValidateState
api_type:
- COM
ms.assetid: c3649daa-cba1-48e3-9ffb-069c1bcf8228
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4fd0dd02c5cf6f6a49b782d06c02e373dcfc3327
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577485"
---
# <a name="ixplogonvalidatestate"></a><span data-ttu-id="a69b5-103">IXPLogon::ValidateState</span><span class="sxs-lookup"><span data-stu-id="a69b5-103">IXPLogon::ValidateState</span></span>

  
  
<span data-ttu-id="a69b5-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a69b5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a69b5-105">Externe Status der Adressbuchhierarchie überprüft.</span><span class="sxs-lookup"><span data-stu-id="a69b5-105">Checks the transport provider's external status.</span></span> 
  
```cpp
HRESULT ValidateState(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="a69b5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a69b5-106">Parameters</span></span>

 <span data-ttu-id="a69b5-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="a69b5-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="a69b5-108">[in] Ein Handle für das übergeordnete Fenster für alle Dialogfelder oder Windows, die diese Methode anzeigt.</span><span class="sxs-lookup"><span data-stu-id="a69b5-108">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="a69b5-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a69b5-109">_ulFlags_</span></span>
  
> <span data-ttu-id="a69b5-110">[in] Eine Bitmaske aus Flags, die steuert, wie die statusüberprüfung ausgeführt wird und die Ergebnisse über den Status überprüfen.</span><span class="sxs-lookup"><span data-stu-id="a69b5-110">[in] A bitmask of flags that controls how the status check is performed and the results of the status check.</span></span> <span data-ttu-id="a69b5-111">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="a69b5-111">The following flags can be set:</span></span>
    
<span data-ttu-id="a69b5-112">ABORT_XP_HEADER_OPERATION</span><span class="sxs-lookup"><span data-stu-id="a69b5-112">ABORT_XP_HEADER_OPERATION</span></span> 
  
> <span data-ttu-id="a69b5-113">Der Benutzer hat den Vorgang in der Regel durch Klicken auf die Schaltfläche " **Abbrechen** " in einem Dialogfeld abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="a69b5-113">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> <span data-ttu-id="a69b5-114">Der Transportdienst hat die Möglichkeit, den Vorgang fortsetzen, oder den Vorgang abzubrechen und MAPI_E_USER_CANCELED zurückgeben kann.</span><span class="sxs-lookup"><span data-stu-id="a69b5-114">The transport provider has the option to continue working on the operation, or it can abort the operation and return MAPI_E_USER_CANCELED.</span></span> 
    
<span data-ttu-id="a69b5-115">CONFIG_CHANGED</span><span class="sxs-lookup"><span data-stu-id="a69b5-115">CONFIG_CHANGED</span></span> 
  
> <span data-ttu-id="a69b5-116">Überprüft den Status der aktuell geladenen Transportanbieter durch verursacht die MAPI-Warteschlange ihrer [IXPLogon::AddressTypes](ixplogon-addresstypes.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a69b5-116">Validates the state of currently loaded transport providers by causing the MAPI spooler to call their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> <span data-ttu-id="a69b5-117">Dieses Kennzeichen ermöglicht auch der MAPI-Warteschlange an den richtigen kritische Adressbuchhierarchie Fehler ohne dass Clientanwendungen abmelden und dann erneut anmelden.</span><span class="sxs-lookup"><span data-stu-id="a69b5-117">This flag also provides the MAPI spooler an opportunity to correct critical transport-provider failures without forcing client applications to log off and then log on again.</span></span> 
    
<span data-ttu-id="a69b5-118">FORCE_XP_CONNECT</span><span class="sxs-lookup"><span data-stu-id="a69b5-118">FORCE_XP_CONNECT</span></span> 
  
> <span data-ttu-id="a69b5-119">Vom Benutzer ausgewählte einen Verbindungsvorgang.</span><span class="sxs-lookup"><span data-stu-id="a69b5-119">The user selected a connect operation.</span></span> <span data-ttu-id="a69b5-120">Wenn dieses Flag mit dem REFRESH_XP_HEADER_CACHE oder PROCESS_XP_HEADER_CACHE-Flag verwendet wird, erfolgt die Connect-Aktion ohne Zwischenspeichern.</span><span class="sxs-lookup"><span data-stu-id="a69b5-120">When this flag is used with the REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE flag, the connect action occurs without caching.</span></span>
    
<span data-ttu-id="a69b5-121">FORCE_XP_DISCONNECT</span><span class="sxs-lookup"><span data-stu-id="a69b5-121">FORCE_XP_DISCONNECT</span></span> 
  
> <span data-ttu-id="a69b5-122">Vom Benutzer ausgewählte einen Trennvorgang.</span><span class="sxs-lookup"><span data-stu-id="a69b5-122">The user selected a disconnect operation.</span></span> <span data-ttu-id="a69b5-123">Wenn dieses Flag mit REFRESH_XP_HEADER_CACHE oder PROCESS_XP_HEADER_CACHE verwendet wird, erfolgt die Disconnect-Aktion ohne Zwischenspeichern.</span><span class="sxs-lookup"><span data-stu-id="a69b5-123">When this flag is used with REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE, the disconnect action occurs without caching.</span></span>
    
<span data-ttu-id="a69b5-124">PROCESS_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="a69b5-124">PROCESS_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="a69b5-125">Einträge in der Kopfzeile Cachetabelle verarbeitet werden soll, sollten alle Nachrichten mit dem MSGSTATUS_REMOTE_DOWNLOAD-Flag heruntergeladen werden und alle Nachrichten mit dem MSGSTATUS_REMOTE_DELETE-Flag gekennzeichnet gelöscht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a69b5-125">Entries in the header cache table should be processed, all messages marked with the MSGSTATUS_REMOTE_DOWNLOAD flag should be downloaded, and all messages marked with the MSGSTATUS_REMOTE_DELETE flag should be deleted.</span></span> <span data-ttu-id="a69b5-126">Nachrichten, die MSGSTATUS_REMOTE_DOWNLOAD und MSGSTATUS_REMOTE_DELETE festgelegt haben, sollten verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="a69b5-126">Messages that have both MSGSTATUS_REMOTE_DOWNLOAD and MSGSTATUS_REMOTE_DELETE set should be moved.</span></span>
    
<span data-ttu-id="a69b5-127">REFRESH_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="a69b5-127">REFRESH_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="a69b5-128">Sollte eine neue Liste der Kopfzeilen heruntergeladen werden, und alle Flags Markierung Nachrichtenstatus sollte deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="a69b5-128">A new list of message headers should be downloaded, and all message status marking flags should be cleared.</span></span>
    
<span data-ttu-id="a69b5-129">SUPPRESS_UI</span><span class="sxs-lookup"><span data-stu-id="a69b5-129">SUPPRESS_UI</span></span> 
  
> <span data-ttu-id="a69b5-130">Verhindert, dass der Adressbuchhierarchie eine Benutzeroberfläche angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a69b5-130">Prevents the transport provider from displaying a user interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a69b5-131">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="a69b5-131">Return value</span></span>

<span data-ttu-id="a69b5-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="a69b5-132">S_OK</span></span> 
  
> <span data-ttu-id="a69b5-133">Der Aufruf erfolgreich ausgeführt und der erwartete Wert oder Werte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a69b5-133">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="a69b5-134">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="a69b5-134">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="a69b5-135">Ein anderer Vorgang ist in Bearbeitung. Sie dürfen die Durchführung oder sollte beendet werden, bevor der Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a69b5-135">Another operation is in progress; it should be allowed to complete, or it should be stopped before this operation is attempted.</span></span>
    
<span data-ttu-id="a69b5-136">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="a69b5-136">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="a69b5-137">Der beteiligten remote Adressbuchhierarchie eine Benutzeroberfläche nicht unterstützt, und die Clientanwendung selbst sollte das Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a69b5-137">The remote transport provider involved does not support a user interface, and the client application itself should display the dialog box.</span></span>
    
<span data-ttu-id="a69b5-138">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="a69b5-138">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="a69b5-139">Der Benutzer hat den Vorgang in der Regel durch Klicken auf die Schaltfläche " **Abbrechen** " in einem Dialogfeld abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="a69b5-139">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a69b5-140">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="a69b5-140">Remarks</span></span>

<span data-ttu-id="a69b5-141">Die MAPI-Warteschlange Ruft die **IXPLogon::ValidateState** -Methode zur Unterstützung der Aufrufe der [IMAPIStatus::ValidateState](imapistatus-validatestate.md) -Methode für das Statusobjekt.</span><span class="sxs-lookup"><span data-stu-id="a69b5-141">The MAPI spooler calls the **IXPLogon::ValidateState** method to support calls to the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method for the status object.</span></span> <span data-ttu-id="a69b5-142">Der Transportdienst sollte für den Aufruf der **IXPLogon::ValidateState** reagieren, als ob die MAPI-Warteschlange ein Statusobjekt für die aktuelle Sitzung geöffnet und anschließend **IMAPIStatus::ValidateState** für dieses Objekt aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="a69b5-142">The transport provider should respond to the **IXPLogon::ValidateState** call exactly as if the MAPI spooler had opened a status object for the current logon session and then called **IMAPIStatus::ValidateState** on that object.</span></span> 
  
<span data-ttu-id="a69b5-143">Zur Unterstützung der Implementierung der **IMAPIStatus::ValidateState**Ruft die MAPI-Warteschlange **IXPLogon::ValidateState** für alle Objekte, die Anmeldung für alle aktiven Transport-Anbieter, die in einer Sitzung Profil ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a69b5-143">To support its implementation of **IMAPIStatus::ValidateState**, the MAPI spooler calls **IXPLogon::ValidateState** on all logon objects for all active transport providers that are running in a profile session.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a69b5-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a69b5-144">See also</span></span>



[<span data-ttu-id="a69b5-145">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="a69b5-145">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
  
[<span data-ttu-id="a69b5-146">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="a69b5-146">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)
  
[<span data-ttu-id="a69b5-147">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a69b5-147">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

