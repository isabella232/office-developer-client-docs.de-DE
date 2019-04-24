---
title: Herunterfahren eines Nachrichtenspeicher Anbieters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e38219db-f867-4c1d-9973-0e025779e8b6
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8e4712572eaff465bb23b55eccc3670f637c0f9c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339200"
---
# <a name="shutting-down-a-message-store-provider"></a><span data-ttu-id="20ad6-103">Herunterfahren eines Nachrichtenspeicher Anbieters</span><span class="sxs-lookup"><span data-stu-id="20ad6-103">Shutting Down a Message Store Provider</span></span>

  
  
<span data-ttu-id="20ad6-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="20ad6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="20ad6-105">Wenn es sich bei Ihrem Anbieter um einen Nachrichtenspeicher Anbieter handelt, kann er auf eine der folgenden Arten heruntergefahren werden:</span><span class="sxs-lookup"><span data-stu-id="20ad6-105">If your provider is a message store provider, it can be shut down in one of the following ways:</span></span>
  
- <span data-ttu-id="20ad6-106">Wenn ein Client oder der MAPI-Spooler [IMsgStore:: StoreLogoff](imsgstore-storelogoff.md)aufruft.</span><span class="sxs-lookup"><span data-stu-id="20ad6-106">When a client or the MAPI spooler calls [IMsgStore::StoreLogoff](imsgstore-storelogoff.md).</span></span> <span data-ttu-id="20ad6-107">Das Herunterfahren eines Nachrichtenspeicher Anbieters mit **StoreLogoff** bewirkt, dass das Herunterfahren auf geordnete und kontrollierte Weise erfolgt.</span><span class="sxs-lookup"><span data-stu-id="20ad6-107">Shutting down a message store provider with **StoreLogoff** causes the shutdown to occur in an orderly and controlled manner.</span></span> 
    
- <span data-ttu-id="20ad6-108">Wenn ein Client [IMAPISession:: Logoff](imapisession-logoff.md)aufruft.</span><span class="sxs-lookup"><span data-stu-id="20ad6-108">When a client calls [IMAPISession::Logoff](imapisession-logoff.md).</span></span> 
    
<span data-ttu-id="20ad6-109">Die Implementierung von **IMsgStore:: StoreLogoff** sollte zunächst [IMAPISupport:: StoreLogoffTransports](imapisupport-storelogofftransports.md) aufrufen, um MAPI zu informieren, dass Sie heruntergefahren wird, was darauf hinweist, dass alle zugehörigen Transportanbieter abgemeldet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="20ad6-109">Your implementation of **IMsgStore::StoreLogoff** should begin by calling [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) to inform MAPI that it is being shut down, indicating that any related transport providers should be logged off.</span></span> <span data-ttu-id="20ad6-110">Wenn **IMsgStore:: StoreLogoff** zurückgegeben wird, ruft der Aufrufer die [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) -Methode des Nachrichtenspeichers auf.</span><span class="sxs-lookup"><span data-stu-id="20ad6-110">When **IMsgStore::StoreLogoff** returns, its caller invokes your message store's [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method.</span></span> <span data-ttu-id="20ad6-111">Implementieren Sie diese **Release** -Methode, indem Sie die **IUnknown:: Release** -Methode des Support-Objekts aufrufen.</span><span class="sxs-lookup"><span data-stu-id="20ad6-111">Implement this **Release** method by calling the support object's **IUnknown::Release** method.</span></span> 
  
<span data-ttu-id="20ad6-112">MAPI führt die folgenden Aufgaben in der Implementierung von **IUnknown:: Release** für Nachrichtenspeicher aus:</span><span class="sxs-lookup"><span data-stu-id="20ad6-112">MAPI performs the following tasks in its implementation of **IUnknown::Release** for message stores:</span></span> 
  
1. <span data-ttu-id="20ad6-113">Entfernt alle vom Nachrichtenspeicher Anbieter registrierten [MAPIUID](mapiuid.md) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="20ad6-113">Removes all of the [MAPIUID](mapiuid.md) structures registered by the message store provider.</span></span> 
    
2. <span data-ttu-id="20ad6-114">Entfernt die Zeile des Nachrichtenspeicher Anbieters aus der Statustabelle.</span><span class="sxs-lookup"><span data-stu-id="20ad6-114">Removes the message store provider's row from the status table.</span></span>
    
3. <span data-ttu-id="20ad6-115">Ruft [IMSLogon:: Logoff](imslogon-logoff.md) auf, um alle geöffneten Objekte, unter Objekte und Statusobjekte zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="20ad6-115">Calls [IMSLogon::Logoff](imslogon-logoff.md) to release all open objects, subobjects, and status objects.</span></span> 
    
4. <span data-ttu-id="20ad6-116">Ruft [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) auf, um das Anmeldeobjekt des Nachrichtenspeicher Anbieters zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="20ad6-116">Calls [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) to release the message store provider's logon object.</span></span> 
    
<span data-ttu-id="20ad6-117">Einige Clients können den Aufruf von **IMsgStore:: StoreLogoff**weglassen, indem Sie das Herunterfahren des Nachrichtenspeicher Anbieters mit dem Aufruf der **IUnknown:: Release** -Methode des Nachrichtenspeichers initiieren.</span><span class="sxs-lookup"><span data-stu-id="20ad6-117">Some clients might omit the call to **IMsgStore::StoreLogoff**, initiating the shutdown of your message store provider with the call to the message store's **IUnknown::Release** method.</span></span> <span data-ttu-id="20ad6-118">Ein Herunterfahren unter diesen Umständen ohne den Aufruf von **StoreLogoff** ist weniger geordnet und gesteuert.</span><span class="sxs-lookup"><span data-stu-id="20ad6-118">A shutdown under these circumstances without the call to **StoreLogoff** is less orderly and controlled.</span></span> <span data-ttu-id="20ad6-119">Schreiben Sie die **Release** -Methode des Nachrichtenspeichers, um diese Möglichkeit zu behandeln, und verfolgen Sie, ob ein Aufruf von **IMAPISupport:: StoreLogoffTransports** aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="20ad6-119">Write your message store's **Release** method to handle this possibility and keep track of whether or not a call to **IMAPISupport::StoreLogoffTransports** has occurred.</span></span> <span data-ttu-id="20ad6-120">**StoreLogoffTransports** muss beim Herunterfahren einmal aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="20ad6-120">**StoreLogoffTransports** must be called once during the shutdown process.</span></span> <span data-ttu-id="20ad6-121">Wenn Sie in Ihrer **Release** -Methode feststellen, dass **StoreLogoffTransports** noch nicht aufgerufen wurde, rufen Sie Sie mit dem LOGOFF_ABORT-Flag auf.</span><span class="sxs-lookup"><span data-stu-id="20ad6-121">If you detect in your **Release** method that **StoreLogoffTransports** has not yet been called, invoke it with the LOGOFF_ABORT flag.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="20ad6-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="20ad6-122">See also</span></span>



[<span data-ttu-id="20ad6-123">Herunterfahren eines Dienstanbieters</span><span class="sxs-lookup"><span data-stu-id="20ad6-123">Shutting Down a Service Provider</span></span>](shutting-down-a-service-provider.md)

