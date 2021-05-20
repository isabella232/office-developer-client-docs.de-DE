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
ms.openlocfilehash: a3469e6baacb52938b870ca87d824bf640a8a88f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439485"
---
# <a name="ixplogonvalidatestate"></a><span data-ttu-id="f74f9-103">IXPLogon::ValidateState</span><span class="sxs-lookup"><span data-stu-id="f74f9-103">IXPLogon::ValidateState</span></span>

  
  
<span data-ttu-id="f74f9-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f74f9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f74f9-105">Überprüft den externen Status des Transportanbieters.</span><span class="sxs-lookup"><span data-stu-id="f74f9-105">Checks the transport provider's external status.</span></span> 
  
```cpp
HRESULT ValidateState(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="f74f9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f74f9-106">Parameters</span></span>

 <span data-ttu-id="f74f9-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="f74f9-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="f74f9-108">[in] Ein Handle zum übergeordneten Fenster aller Dialogfelder oder Fenster, die von dieser Methode angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f74f9-108">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="f74f9-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f74f9-109">_ulFlags_</span></span>
  
> <span data-ttu-id="f74f9-110">[in] Eine Bitmaske mit Flags, die steuert, wie die Statusüberprüfung durchgeführt wird, und die Ergebnisse der Statusüberprüfung.</span><span class="sxs-lookup"><span data-stu-id="f74f9-110">[in] A bitmask of flags that controls how the status check is performed and the results of the status check.</span></span> <span data-ttu-id="f74f9-111">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="f74f9-111">The following flags can be set:</span></span>
    
<span data-ttu-id="f74f9-112">ABORT_XP_HEADER_OPERATION</span><span class="sxs-lookup"><span data-stu-id="f74f9-112">ABORT_XP_HEADER_OPERATION</span></span> 
  
> <span data-ttu-id="f74f9-113">Der Benutzer hat den Vorgang abgebrochen, in der Regel durch Klicken auf die **Schaltfläche** Abbrechen in einem Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="f74f9-113">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> <span data-ttu-id="f74f9-114">Der Transportanbieter kann weiterhin an dem Vorgang arbeiten, oder er kann den Vorgang abbrechen und MAPI_E_USER_CANCELED.</span><span class="sxs-lookup"><span data-stu-id="f74f9-114">The transport provider has the option to continue working on the operation, or it can abort the operation and return MAPI_E_USER_CANCELED.</span></span> 
    
<span data-ttu-id="f74f9-115">CONFIG_CHANGED</span><span class="sxs-lookup"><span data-stu-id="f74f9-115">CONFIG_CHANGED</span></span> 
  
> <span data-ttu-id="f74f9-116">Überprüft den Status der derzeit geladenen Transportanbieter, indem der MAPI-Spooler seine [IXPLogon::AddressTypes-Methode aufruft.](ixplogon-addresstypes.md)</span><span class="sxs-lookup"><span data-stu-id="f74f9-116">Validates the state of currently loaded transport providers by causing the MAPI spooler to call their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> <span data-ttu-id="f74f9-117">Dieses Flag bietet dem MAPI-Spooler auch die Möglichkeit, kritische Fehler des Transportanbieters zu beheben, ohne clientanwendungen zum Abmelden und anschließenden erneuten Anmelden zu zwingen.</span><span class="sxs-lookup"><span data-stu-id="f74f9-117">This flag also provides the MAPI spooler an opportunity to correct critical transport-provider failures without forcing client applications to log off and then log on again.</span></span> 
    
<span data-ttu-id="f74f9-118">FORCE_XP_CONNECT</span><span class="sxs-lookup"><span data-stu-id="f74f9-118">FORCE_XP_CONNECT</span></span> 
  
> <span data-ttu-id="f74f9-119">Der Benutzer hat einen Verbindungsvorgang ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="f74f9-119">The user selected a connect operation.</span></span> <span data-ttu-id="f74f9-120">Wenn dieses Flag mit dem REFRESH_XP_HEADER_CACHE- oder PROCESS_XP_HEADER_CACHE verwendet wird, erfolgt die Verbindungsaktion ohne Zwischenspeicherung.</span><span class="sxs-lookup"><span data-stu-id="f74f9-120">When this flag is used with the REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE flag, the connect action occurs without caching.</span></span>
    
<span data-ttu-id="f74f9-121">FORCE_XP_DISCONNECT</span><span class="sxs-lookup"><span data-stu-id="f74f9-121">FORCE_XP_DISCONNECT</span></span> 
  
> <span data-ttu-id="f74f9-122">Der Benutzer hat einen Verbindungstrennungsvorgang ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="f74f9-122">The user selected a disconnect operation.</span></span> <span data-ttu-id="f74f9-123">Wenn dieses Flag mit REFRESH_XP_HEADER_CACHE oder PROCESS_XP_HEADER_CACHE verwendet wird, erfolgt die Verbindungstrennungsaktion ohne Zwischenspeicherung.</span><span class="sxs-lookup"><span data-stu-id="f74f9-123">When this flag is used with REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE, the disconnect action occurs without caching.</span></span>
    
<span data-ttu-id="f74f9-124">PROCESS_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="f74f9-124">PROCESS_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="f74f9-125">Einträge in der Kopfzeilencachetabelle sollten verarbeitet werden, alle nachrichten, die mit dem flag MSGSTATUS_REMOTE_DOWNLOAD gekennzeichnet sind, heruntergeladen werden, und alle Nachrichten, die mit dem MSGSTATUS_REMOTE_DELETE gekennzeichnet sind, sollten gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="f74f9-125">Entries in the header cache table should be processed, all messages marked with the MSGSTATUS_REMOTE_DOWNLOAD flag should be downloaded, and all messages marked with the MSGSTATUS_REMOTE_DELETE flag should be deleted.</span></span> <span data-ttu-id="f74f9-126">Nachrichten, die sowohl MSGSTATUS_REMOTE_DOWNLOAD als auch MSGSTATUS_REMOTE_DELETE festgelegt sind, sollten verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="f74f9-126">Messages that have both MSGSTATUS_REMOTE_DOWNLOAD and MSGSTATUS_REMOTE_DELETE set should be moved.</span></span>
    
<span data-ttu-id="f74f9-127">REFRESH_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="f74f9-127">REFRESH_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="f74f9-128">Eine neue Liste von Nachrichtenkopfzeilen sollte heruntergeladen werden, und alle Kennzeichnungskennzeichen für nachrichtenstatus sollten entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="f74f9-128">A new list of message headers should be downloaded, and all message status marking flags should be cleared.</span></span>
    
<span data-ttu-id="f74f9-129">SUPPRESS_UI</span><span class="sxs-lookup"><span data-stu-id="f74f9-129">SUPPRESS_UI</span></span> 
  
> <span data-ttu-id="f74f9-130">Verhindert, dass vom Transportanbieter eine Benutzeroberfläche angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="f74f9-130">Prevents the transport provider from displaying a user interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f74f9-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f74f9-131">Return value</span></span>

<span data-ttu-id="f74f9-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="f74f9-132">S_OK</span></span> 
  
> <span data-ttu-id="f74f9-133">Der Aufruf war erfolgreich und hat den erwarteten Wert oder die erwarteten Werte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f74f9-133">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="f74f9-134">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="f74f9-134">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="f74f9-135">Ein weiterer Vorgang wird ausgeführt. Sie sollte abgeschlossen sein oder beendet werden, bevor dieser Vorgang versucht wird.</span><span class="sxs-lookup"><span data-stu-id="f74f9-135">Another operation is in progress; it should be allowed to complete, or it should be stopped before this operation is attempted.</span></span>
    
<span data-ttu-id="f74f9-136">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="f74f9-136">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="f74f9-137">Der beteiligte Remotetransportanbieter unterstützt keine Benutzeroberfläche, und die Clientanwendung selbst sollte das Dialogfeld anzeigen.</span><span class="sxs-lookup"><span data-stu-id="f74f9-137">The remote transport provider involved does not support a user interface, and the client application itself should display the dialog box.</span></span>
    
<span data-ttu-id="f74f9-138">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="f74f9-138">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="f74f9-139">Der Benutzer hat den Vorgang abgebrochen, in der Regel durch Klicken auf die **Schaltfläche** Abbrechen in einem Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="f74f9-139">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f74f9-140">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f74f9-140">Remarks</span></span>

<span data-ttu-id="f74f9-141">Der MAPI-Spooler ruft die **IXPLogon::ValidateState-Methode** auf, um Aufrufe der [IMAPIStatus::ValidateState-Methode](imapistatus-validatestate.md) für das Statusobjekt zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="f74f9-141">The MAPI spooler calls the **IXPLogon::ValidateState** method to support calls to the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method for the status object.</span></span> <span data-ttu-id="f74f9-142">Der Transportanbieter sollte auf den **IXPLogon::ValidateState-Aufruf** genauso reagieren, als ob der MAPI-Spooler ein Statusobjekt für die aktuelle Anmeldesitzung geöffnet und dann **IMAPIStatus::ValidateState für** dieses Objekt aufgerufen hätte.</span><span class="sxs-lookup"><span data-stu-id="f74f9-142">The transport provider should respond to the **IXPLogon::ValidateState** call exactly as if the MAPI spooler had opened a status object for the current logon session and then called **IMAPIStatus::ValidateState** on that object.</span></span> 
  
<span data-ttu-id="f74f9-143">Zur Unterstützung der Implementierung von **IMAPIStatus::ValidateState** ruft der MAPI-Spooler **IXPLogon::ValidateState** für alle Anmeldeobjekte für alle aktiven Transportanbieter auf, die in einer Profilsitzung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f74f9-143">To support its implementation of **IMAPIStatus::ValidateState**, the MAPI spooler calls **IXPLogon::ValidateState** on all logon objects for all active transport providers that are running in a profile session.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f74f9-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f74f9-144">See also</span></span>



[<span data-ttu-id="f74f9-145">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="f74f9-145">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
  
[<span data-ttu-id="f74f9-146">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="f74f9-146">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)
  
[<span data-ttu-id="f74f9-147">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f74f9-147">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

