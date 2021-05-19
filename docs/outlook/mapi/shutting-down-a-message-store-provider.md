---
title: Herunterfahren eines Nachrichtenanbieters Store
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
# <a name="shutting-down-a-message-store-provider"></a><span data-ttu-id="2e112-103">Herunterfahren eines Nachrichtenanbieters Store</span><span class="sxs-lookup"><span data-stu-id="2e112-103">Shutting Down a Message Store Provider</span></span>

  
  
<span data-ttu-id="2e112-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2e112-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2e112-105">Wenn Ihr Anbieter ein Nachrichtenspeicheranbieter ist, kann er auf eine der folgenden Arten heruntergefahren werden:</span><span class="sxs-lookup"><span data-stu-id="2e112-105">If your provider is a message store provider, it can be shut down in one of the following ways:</span></span>
  
- <span data-ttu-id="2e112-106">Wenn ein Client oder der MAPI-Spooler [IMsgStore::StoreLogoff aufruft.](imsgstore-storelogoff.md)</span><span class="sxs-lookup"><span data-stu-id="2e112-106">When a client or the MAPI spooler calls [IMsgStore::StoreLogoff](imsgstore-storelogoff.md).</span></span> <span data-ttu-id="2e112-107">Das Herunterfahren eines Nachrichtenspeicheranbieters mit **StoreLogoff** führt dazu, dass das Herunterfahren auf geordnete und kontrollierte Weise erfolgt.</span><span class="sxs-lookup"><span data-stu-id="2e112-107">Shutting down a message store provider with **StoreLogoff** causes the shutdown to occur in an orderly and controlled manner.</span></span> 
    
- <span data-ttu-id="2e112-108">Wenn ein Client [IMAPISession::Logoff aufruft.](imapisession-logoff.md)</span><span class="sxs-lookup"><span data-stu-id="2e112-108">When a client calls [IMAPISession::Logoff](imapisession-logoff.md).</span></span> 
    
<span data-ttu-id="2e112-109">Ihre Implementierung von **IMsgStore::StoreLogoff** sollte zunächst [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) aufrufen, um MAPI darüber zu informieren, dass es heruntergefahren wird, was angibt, dass alle zugehörigen Transportanbieter abgemeldet werden sollten.</span><span class="sxs-lookup"><span data-stu-id="2e112-109">Your implementation of **IMsgStore::StoreLogoff** should begin by calling [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) to inform MAPI that it is being shut down, indicating that any related transport providers should be logged off.</span></span> <span data-ttu-id="2e112-110">Wenn **IMsgStore::StoreLogoff** zurückgegeben wird, ruft der Aufrufer die [IUnknown::Release-Methode](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) ihres Nachrichtenspeichers auf.</span><span class="sxs-lookup"><span data-stu-id="2e112-110">When **IMsgStore::StoreLogoff** returns, its caller invokes your message store's [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method.</span></span> <span data-ttu-id="2e112-111">Implementieren Sie **diese Release-Methode,** indem Sie die **IUnknown::Release-Methode des Supportobjekts** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2e112-111">Implement this **Release** method by calling the support object's **IUnknown::Release** method.</span></span> 
  
<span data-ttu-id="2e112-112">MAPI führt die folgenden Aufgaben in der Implementierung von **IUnknown::Release für** Nachrichtenspeicher aus:</span><span class="sxs-lookup"><span data-stu-id="2e112-112">MAPI performs the following tasks in its implementation of **IUnknown::Release** for message stores:</span></span> 
  
1. <span data-ttu-id="2e112-113">Entfernt alle vom Nachrichtenspeicheranbieter registrierten [MAPIUID-Strukturen.](mapiuid.md)</span><span class="sxs-lookup"><span data-stu-id="2e112-113">Removes all of the [MAPIUID](mapiuid.md) structures registered by the message store provider.</span></span> 
    
2. <span data-ttu-id="2e112-114">Entfernt die Zeile des Nachrichtenspeicheranbieters aus der Statustabelle.</span><span class="sxs-lookup"><span data-stu-id="2e112-114">Removes the message store provider's row from the status table.</span></span>
    
3. <span data-ttu-id="2e112-115">Ruft [IMSLogon::Logoff auf,](imslogon-logoff.md) um alle geöffneten Objekte, Unterobjekte und Statusobjekte frei zu geben.</span><span class="sxs-lookup"><span data-stu-id="2e112-115">Calls [IMSLogon::Logoff](imslogon-logoff.md) to release all open objects, subobjects, and status objects.</span></span> 
    
4. <span data-ttu-id="2e112-116">Ruft [IUnknown::Release auf,](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) um das Anmeldeobjekt des Nachrichtenspeicheranbieters frei zu geben.</span><span class="sxs-lookup"><span data-stu-id="2e112-116">Calls [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) to release the message store provider's logon object.</span></span> 
    
<span data-ttu-id="2e112-117">Einige Clients können den Aufruf von **IMsgStore::StoreLogoff** auslassen und das Herunterfahren Ihres Nachrichtenspeicheranbieters mit dem Aufruf der **IUnknown::Release-Methode** des Nachrichtenspeichers initiieren.</span><span class="sxs-lookup"><span data-stu-id="2e112-117">Some clients might omit the call to **IMsgStore::StoreLogoff**, initiating the shutdown of your message store provider with the call to the message store's **IUnknown::Release** method.</span></span> <span data-ttu-id="2e112-118">Ein Herunterfahren unter diesen Umständen ohne den Aufruf von **StoreLogoff** ist weniger geordnet und gesteuert.</span><span class="sxs-lookup"><span data-stu-id="2e112-118">A shutdown under these circumstances without the call to **StoreLogoff** is less orderly and controlled.</span></span> <span data-ttu-id="2e112-119">Schreiben Sie die **Release-Methode** Ihres Nachrichtenspeichers, um diese Möglichkeit zu behandeln und zu verfolgen, ob ein Aufruf von **IMAPISupport::StoreLogoffTransports** stattgefunden hat.</span><span class="sxs-lookup"><span data-stu-id="2e112-119">Write your message store's **Release** method to handle this possibility and keep track of whether or not a call to **IMAPISupport::StoreLogoffTransports** has occurred.</span></span> <span data-ttu-id="2e112-120">**StoreLogoffTransports** muss während des Herunterfahrens einmal aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="2e112-120">**StoreLogoffTransports** must be called once during the shutdown process.</span></span> <span data-ttu-id="2e112-121">Wenn Sie in Ihrer **Release-Methode** feststellen, dass **StoreLogoffTransports** noch nicht aufgerufen wurde, rufen Sie es mit dem Flag LOGOFF_ABORT auf.</span><span class="sxs-lookup"><span data-stu-id="2e112-121">If you detect in your **Release** method that **StoreLogoffTransports** has not yet been called, invoke it with the LOGOFF_ABORT flag.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2e112-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2e112-122">See also</span></span>



[<span data-ttu-id="2e112-123">Herunterfahren eines Dienstanbieters</span><span class="sxs-lookup"><span data-stu-id="2e112-123">Shutting Down a Service Provider</span></span>](shutting-down-a-service-provider.md)

