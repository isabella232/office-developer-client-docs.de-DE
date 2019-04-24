---
title: Herunterfahren eines Dienstanbieters
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e518830b-0aaa-4ce4-a85a-07e4f00750a9
description: 'Letzte �nderung: Montag, 7. Dezember 2015'
ms.openlocfilehash: 4e25dad1e04927e10af38cdfbf8f30c9bd04234b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339207"
---
# <a name="shutting-down-a-service-provider"></a><span data-ttu-id="1a54e-103">Herunterfahren eines Dienstanbieters</span><span class="sxs-lookup"><span data-stu-id="1a54e-103">Shutting Down a Service Provider</span></span>

 
  
<span data-ttu-id="1a54e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a54e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a54e-105">Wenn ein Client die [IMAPISession:: Abmelde](imapisession-logoff.md) Methode aufruft, um die Sitzung zu beenden und alle aktiven Dienstanbieter herunterzufahren, ruft MAPI wiederum die folgenden Methoden auf:</span><span class="sxs-lookup"><span data-stu-id="1a54e-105">When a client calls the [IMAPISession::Logoff](imapisession-logoff.md) method to end the session and shut down all active service providers, MAPI in turn calls the following methods:</span></span> 
  
- <span data-ttu-id="1a54e-106">[IABLogon:: Logoff](iablogon-logoff.md) für Adressbuchanbieter.</span><span class="sxs-lookup"><span data-stu-id="1a54e-106">[IABLogon::Logoff](iablogon-logoff.md) for address book providers.</span></span> 
    
- <span data-ttu-id="1a54e-107">[IMSLogon:: Logoff](imslogon-logoff.md) für Nachrichtenspeicher Anbieter.</span><span class="sxs-lookup"><span data-stu-id="1a54e-107">[IMSLogon::Logoff](imslogon-logoff.md) for message store providers.</span></span> 
    
- <span data-ttu-id="1a54e-108">[IXPLogon:: TransportLogoff](ixplogon-transportlogoff.md) für Transportanbieter.</span><span class="sxs-lookup"><span data-stu-id="1a54e-108">[IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) for transport providers.</span></span> 
    
<span data-ttu-id="1a54e-109">Diese Methoden weisen ähnliche Implementierungen auf.</span><span class="sxs-lookup"><span data-stu-id="1a54e-109">These methods have similar implementations.</span></span> <span data-ttu-id="1a54e-110">Die wichtigsten Aufgaben, die eine Abmelde Methode ausführt, lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="1a54e-110">The main tasks that a logoff method performs are as follows:</span></span>
  
- <span data-ttu-id="1a54e-111">Freigeben aller geöffneten Objekte, einschließlich unter Objekte und Statusobjekte.</span><span class="sxs-lookup"><span data-stu-id="1a54e-111">Releasing all open objects, including subobjects and status objects.</span></span>
    
- <span data-ttu-id="1a54e-112">Aufrufen der [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) -Methode des Support Objekts, um den Verweiszähler zu verringern.</span><span class="sxs-lookup"><span data-stu-id="1a54e-112">Calling the support object's [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method to decrement its reference count.</span></span> 
    
- <span data-ttu-id="1a54e-113">Entfernen aller registrierten [MAPIUID](mapiuid.md) -Strukturen Ihres Anbieters.</span><span class="sxs-lookup"><span data-stu-id="1a54e-113">Removing all of your provider's registered [MAPIUID](mapiuid.md) structures.</span></span> 
    
- <span data-ttu-id="1a54e-114">Entfernen der Zeile des Anbieters in der Statustabelle.</span><span class="sxs-lookup"><span data-stu-id="1a54e-114">Removing your provider's row in the status table.</span></span>
    
- <span data-ttu-id="1a54e-115">Ausführen von Aufgaben, die sich auf das Bereinigen von Ressourcen beziehen, wie etwa die folgenden:</span><span class="sxs-lookup"><span data-stu-id="1a54e-115">Performing any tasks that relate to cleaning up resources, such as the following:</span></span>
    
  - <span data-ttu-id="1a54e-116">Beenden einer Verbindung mit einem Remoteserver.</span><span class="sxs-lookup"><span data-stu-id="1a54e-116">Terminating a connection with a remote server.</span></span>
    
  - <span data-ttu-id="1a54e-117">Dekrementieren der Verweisanzahl für das Logon-Objekt.</span><span class="sxs-lookup"><span data-stu-id="1a54e-117">Decrementing the reference count on the logon object.</span></span>
    
  - <span data-ttu-id="1a54e-118">Entfernen des Anmelde Objekts aus der Liste der Anmeldeobjekte, die der Anbieter speichert.</span><span class="sxs-lookup"><span data-stu-id="1a54e-118">Removing the logon object from the list of logon objects that your provider stores.</span></span>
    
  - <span data-ttu-id="1a54e-119">Im Debugmodus werden Ablaufverfolgungen ausgegeben, um Objekte zu finden, die Speicherplatz verloren haben.</span><span class="sxs-lookup"><span data-stu-id="1a54e-119">In debug mode, issuing traces to locate objects that have leaked memory.</span></span>
    
<span data-ttu-id="1a54e-120">Wenn die Abmelde Methode zurückgegeben wird, ruft MAPI Folgendes auf:</span><span class="sxs-lookup"><span data-stu-id="1a54e-120">When your logoff method returns, MAPI calls the following:</span></span>
  
- <span data-ttu-id="1a54e-121">Die **IUnknown:: Release** -Methode des LOGON-Objekts.</span><span class="sxs-lookup"><span data-stu-id="1a54e-121">Your logon object's **IUnknown::Release** method.</span></span> 
    
- <span data-ttu-id="1a54e-122">Die **Shutdown** -Methode Ihres Provider-Objekts, um abschließende Aufräum Aufgaben auszuführen.</span><span class="sxs-lookup"><span data-stu-id="1a54e-122">Your provider object's **Shutdown** method to perform any final cleanup tasks.</span></span> <span data-ttu-id="1a54e-123">Je nach Typ des Anbieters wird eine der folgenden Methoden aufgerufen:</span><span class="sxs-lookup"><span data-stu-id="1a54e-123">Depending on the type of your provider, one of the following methods is called:</span></span> 
    
  - <span data-ttu-id="1a54e-124">[IABProvider:: Herunterfahren](iabprovider-shutdown.md) für Adressbuchanbieter</span><span class="sxs-lookup"><span data-stu-id="1a54e-124">[IABProvider::Shutdown](iabprovider-shutdown.md) for address book providers</span></span> 
    
  - <span data-ttu-id="1a54e-125">[IMSProvider:: Herunterfahren](imsprovider-shutdown.md) für Nachrichtenspeicher Anbieter</span><span class="sxs-lookup"><span data-stu-id="1a54e-125">[IMSProvider::Shutdown](imsprovider-shutdown.md) for message store providers</span></span> 
    
  - <span data-ttu-id="1a54e-126">[IXPProvider:: Herunterfahren](ixpprovider-shutdown.md) für Transportanbieter</span><span class="sxs-lookup"><span data-stu-id="1a54e-126">[IXPProvider::Shutdown](ixpprovider-shutdown.md) for transport providers</span></span> 
    
- <span data-ttu-id="1a54e-127">Die **IUnknown:: Release** -Methode des Anbieterobjekts.</span><span class="sxs-lookup"><span data-stu-id="1a54e-127">Your provider object's **IUnknown::Release** method.</span></span> 
    
<span data-ttu-id="1a54e-128">Wenn Ihr Anbieter ein Nachrichtenspeicher ist, initiiert ein Clientaufruf von [IMsgStore:: StoreLogoff](imsgstore-storelogoff.md) auch den Shutdown-Prozess.</span><span class="sxs-lookup"><span data-stu-id="1a54e-128">If your provider is a message store, a client call to [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) will also initiate the shutdown process.</span></span> <span data-ttu-id="1a54e-129">**StoreLogoff** beendet einen bestimmten Nachrichtenspeicher Anbieter und hat keine Auswirkung auf die Sitzung.</span><span class="sxs-lookup"><span data-stu-id="1a54e-129">**StoreLogoff** shuts down one particular message store provider and has no effect on the session.</span></span> <span data-ttu-id="1a54e-130">Nur ein Nachrichtenspeicher Anbieter kann mit dieser Methode heruntergefahren werden; Es gibt keine explizite Möglichkeit zum Herunterfahren eines bestimmten Adressbuchs oder Transportanbieters.</span><span class="sxs-lookup"><span data-stu-id="1a54e-130">Only a message store provider can be shut down with this method; there is no explicit way to shut down a particular address book or transport provider.</span></span> <span data-ttu-id="1a54e-131">Informationen zur Reaktion auf einen **StoreLogoff** -Anruf finden Sie unter [Herunterfahren eines Nachrichtenspeicher Anbieters](shutting-down-a-message-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="1a54e-131">For information about how to respond to a **StoreLogoff** call, see [Shutting Down a Message Store Provider](shutting-down-a-message-store-provider.md).</span></span>
  
<span data-ttu-id="1a54e-132">Die DLL Ihres Anbieters wird entladen, wenn MAPI die Win32-API-Funktion **FreeLibrary**aufruft, ein Aufruf, der nach dem letzten aktiven Client [MAPIUninitialize](mapiuninitialize.md)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="1a54e-132">Your provider's DLL will be unloaded when MAPI calls the Win32 API function **FreeLibrary**, a call that is made after the last active client has called [MAPIUninitialize](mapiuninitialize.md).</span></span> <span data-ttu-id="1a54e-133">Zu diesem Zeitpunkt wird der Dienstanbieter beendet.</span><span class="sxs-lookup"><span data-stu-id="1a54e-133">By this time, your service provider will have finished shutting down.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1a54e-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1a54e-134">See also</span></span>



[<span data-ttu-id="1a54e-135">MAPI-Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="1a54e-135">MAPI Service Providers</span></span>](mapi-service-providers.md)

