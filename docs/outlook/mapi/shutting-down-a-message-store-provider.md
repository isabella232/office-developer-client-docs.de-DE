---
title: Beenden einer Nachrichtenspeicher-Anbieters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e38219db-f867-4c1d-9973-0e025779e8b6
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b5c9874ca465bb0ebed62f218d1512feb1a2f9ea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795540"
---
# <a name="shutting-down-a-message-store-provider"></a><span data-ttu-id="91352-103">Beenden einer Nachrichtenspeicher-Anbieters</span><span class="sxs-lookup"><span data-stu-id="91352-103">Shutting Down a Message Store Provider</span></span>

  
  
<span data-ttu-id="91352-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="91352-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="91352-105">Wenn der Anbieter einen Anbieter für die Nachricht Anmelden ist, kann es in einem der folgenden Methoden heruntergefahren werden:</span><span class="sxs-lookup"><span data-stu-id="91352-105">If your provider is a message store provider, it can be shut down in one of the following ways:</span></span>
  
- <span data-ttu-id="91352-106">Wenn ein Client oder die MAPI-Warteschlange [IMsgStore::StoreLogoff](imsgstore-storelogoff.md)aufruft.</span><span class="sxs-lookup"><span data-stu-id="91352-106">When a client or the MAPI spooler calls [IMsgStore::StoreLogoff](imsgstore-storelogoff.md).</span></span> <span data-ttu-id="91352-107">Beenden einer Nachricht Store-Anbieters mit **StoreLogoff** bewirkt, dass das Herunterfahren ein ordnungsgemäßes und gesteuerte Weise erfolgen.</span><span class="sxs-lookup"><span data-stu-id="91352-107">Shutting down a message store provider with **StoreLogoff** causes the shutdown to occur in an orderly and controlled manner.</span></span> 
    
- <span data-ttu-id="91352-108">Wenn ein Client [IMAPISession::Logoff](imapisession-logoff.md)aufruft.</span><span class="sxs-lookup"><span data-stu-id="91352-108">When a client calls [IMAPISession::Logoff](imapisession-logoff.md).</span></span> 
    
<span data-ttu-id="91352-109">Durch Aufrufen von [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) um MAPI zu informieren, dass es heruntergefahren wird, der angibt, dass alle verknüpften Transportanbieter sollen, deaktivieren protokolliert werden, sollte die Implementierung von **IMsgStore::StoreLogoff** beginnen.</span><span class="sxs-lookup"><span data-stu-id="91352-109">Your implementation of **IMsgStore::StoreLogoff** should begin by calling [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) to inform MAPI that it is being shut down, indicating that any related transport providers should be logged off.</span></span> <span data-ttu-id="91352-110">Wenn **IMsgStore::StoreLogoff** zurückgegeben wird, wird der Aufrufer des Nachrichtenspeichers [IUnknown](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="91352-110">When **IMsgStore::StoreLogoff** returns, its caller invokes your message store's [IUnknown::Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method.</span></span> <span data-ttu-id="91352-111">Implementieren Sie diese **Version** -Methode, durch die des Unterstützungsobjekts **IUnknown** -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="91352-111">Implement this **Release** method by calling the support object's **IUnknown::Release** method.</span></span> 
  
<span data-ttu-id="91352-112">MAPI führt die folgenden Aufgaben bei der Implementierung der **IUnknown** für Nachrichtenspeicher:</span><span class="sxs-lookup"><span data-stu-id="91352-112">MAPI performs the following tasks in its implementation of **IUnknown::Release** for message stores:</span></span> 
  
1. <span data-ttu-id="91352-113">Entfernt alle der [MAPIUID](mapiuid.md) Strukturen vom Anbieter Store Nachricht registriert.</span><span class="sxs-lookup"><span data-stu-id="91352-113">Removes all of the [MAPIUID](mapiuid.md) structures registered by the message store provider.</span></span> 
    
2. <span data-ttu-id="91352-114">Entfernt die Nachricht Speicheranbieter Zeile aus der Tabelle "Status".</span><span class="sxs-lookup"><span data-stu-id="91352-114">Removes the message store provider's row from the status table.</span></span>
    
3. <span data-ttu-id="91352-115">Ruft die [IMSLogon::Logoff](imslogon-logoff.md) , um alle geöffneten Objekte, Unterobjekte und Status Objekte freizugeben.</span><span class="sxs-lookup"><span data-stu-id="91352-115">Calls [IMSLogon::Logoff](imslogon-logoff.md) to release all open objects, subobjects, and status objects.</span></span> 
    
4. <span data-ttu-id="91352-116">Ruft die [IUnknown](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) , um die Nachricht Speicheranbieter Anmeldung-Objekt freizugeben.</span><span class="sxs-lookup"><span data-stu-id="91352-116">Calls [IUnknown::Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) to release the message store provider's logon object.</span></span> 
    
<span data-ttu-id="91352-117">Einige Clients können ausgelassen werden, den Anruf an **IMsgStore::StoreLogoff**, das Herunterfahren des Anbieters Ihrer Nachricht mit dem Aufruf der Nachrichtenspeicher **IUnknown** -Methode.</span><span class="sxs-lookup"><span data-stu-id="91352-117">Some clients might omit the call to **IMsgStore::StoreLogoff**, initiating the shutdown of your message store provider with the call to the message store's **IUnknown::Release** method.</span></span> <span data-ttu-id="91352-118">Ein Herunterfahren unter diesen Umständen ohne den Aufruf von **StoreLogoff** ist kleiner ordnungsgemäßes und kontrolliert.</span><span class="sxs-lookup"><span data-stu-id="91352-118">A shutdown under these circumstances without the call to **StoreLogoff** is less orderly and controlled.</span></span> <span data-ttu-id="91352-119">Schreiben des Nachrichtenspeichers **Release** -Methode, um diese Möglichkeit behandeln und Nachverfolgen der unabhängig davon, ob ein Aufruf von **IMAPISupport::StoreLogoffTransports** aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="91352-119">Write your message store's **Release** method to handle this possibility and keep track of whether or not a call to **IMAPISupport::StoreLogoffTransports** has occurred.</span></span> <span data-ttu-id="91352-120">**StoreLogoffTransports** muss einmal während des Herunterfahrens aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="91352-120">**StoreLogoffTransports** must be called once during the shutdown process.</span></span> <span data-ttu-id="91352-121">Wenn Sie in der **Version** -Methode erkennen, dass **StoreLogoffTransports** noch nicht aufgerufen wurde, können rufen sie mit dem LOGOFF_ABORT-Flag auf.</span><span class="sxs-lookup"><span data-stu-id="91352-121">If you detect in your **Release** method that **StoreLogoffTransports** has not yet been called, invoke it with the LOGOFF_ABORT flag.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="91352-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91352-122">See also</span></span>



[<span data-ttu-id="91352-123">Herunterfahren von einem Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="91352-123">Shutting Down a Service Provider</span></span>](shutting-down-a-service-provider.md)

