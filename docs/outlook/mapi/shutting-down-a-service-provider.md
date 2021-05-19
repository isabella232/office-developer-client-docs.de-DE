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
# <a name="shutting-down-a-service-provider"></a><span data-ttu-id="2b244-103">Herunterfahren eines Dienstanbieters</span><span class="sxs-lookup"><span data-stu-id="2b244-103">Shutting Down a Service Provider</span></span>

 
  
<span data-ttu-id="2b244-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2b244-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2b244-105">Wenn ein Client die [IMAPISession::Logoff-Methode](imapisession-logoff.md) aufruft, um die Sitzung zu beenden und alle aktiven Dienstanbieter herunterfahren, ruft MAPI wiederum die folgenden Methoden auf:</span><span class="sxs-lookup"><span data-stu-id="2b244-105">When a client calls the [IMAPISession::Logoff](imapisession-logoff.md) method to end the session and shut down all active service providers, MAPI in turn calls the following methods:</span></span> 
  
- <span data-ttu-id="2b244-106">[IABLogon::Logoff](iablogon-logoff.md) für Adressbuchanbieter.</span><span class="sxs-lookup"><span data-stu-id="2b244-106">[IABLogon::Logoff](iablogon-logoff.md) for address book providers.</span></span> 
    
- <span data-ttu-id="2b244-107">[IMSLogon::Logoff](imslogon-logoff.md) für Nachrichtenspeicheranbieter.</span><span class="sxs-lookup"><span data-stu-id="2b244-107">[IMSLogon::Logoff](imslogon-logoff.md) for message store providers.</span></span> 
    
- <span data-ttu-id="2b244-108">[IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) für Transportanbieter.</span><span class="sxs-lookup"><span data-stu-id="2b244-108">[IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) for transport providers.</span></span> 
    
<span data-ttu-id="2b244-109">Diese Methoden haben ähnliche Implementierungen.</span><span class="sxs-lookup"><span data-stu-id="2b244-109">These methods have similar implementations.</span></span> <span data-ttu-id="2b244-110">Die wichtigsten Aufgaben, die eine Abmeldemethode ausführt, sind:</span><span class="sxs-lookup"><span data-stu-id="2b244-110">The main tasks that a logoff method performs are as follows:</span></span>
  
- <span data-ttu-id="2b244-111">Freigeben aller geöffneten Objekte, einschließlich Unterobjekten und Statusobjekten.</span><span class="sxs-lookup"><span data-stu-id="2b244-111">Releasing all open objects, including subobjects and status objects.</span></span>
    
- <span data-ttu-id="2b244-112">Aufrufen der [IUnknown::Release-Methode](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) des Supportobjekts, um die Referenzanzahl zu dekrementieren.</span><span class="sxs-lookup"><span data-stu-id="2b244-112">Calling the support object's [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method to decrement its reference count.</span></span> 
    
- <span data-ttu-id="2b244-113">Entfernen aller registrierten [MAPIUID-Strukturen](mapiuid.md) Ihres Anbieters.</span><span class="sxs-lookup"><span data-stu-id="2b244-113">Removing all of your provider's registered [MAPIUID](mapiuid.md) structures.</span></span> 
    
- <span data-ttu-id="2b244-114">Entfernen der Zeile Ihres Anbieters in der Statustabelle.</span><span class="sxs-lookup"><span data-stu-id="2b244-114">Removing your provider's row in the status table.</span></span>
    
- <span data-ttu-id="2b244-115">Ausführen von Aufgaben im Zusammenhang mit dem Bereinigen von Ressourcen, z. B.:</span><span class="sxs-lookup"><span data-stu-id="2b244-115">Performing any tasks that relate to cleaning up resources, such as the following:</span></span>
    
  - <span data-ttu-id="2b244-116">Beenden einer Verbindung mit einem Remoteserver.</span><span class="sxs-lookup"><span data-stu-id="2b244-116">Terminating a connection with a remote server.</span></span>
    
  - <span data-ttu-id="2b244-117">Dekrementieren der Referenzanzahl für das Anmeldeobjekt.</span><span class="sxs-lookup"><span data-stu-id="2b244-117">Decrementing the reference count on the logon object.</span></span>
    
  - <span data-ttu-id="2b244-118">Entfernen des Anmeldeobjekts aus der Liste der Anmeldeobjekte, die ihr Anbieter speichert.</span><span class="sxs-lookup"><span data-stu-id="2b244-118">Removing the logon object from the list of logon objects that your provider stores.</span></span>
    
  - <span data-ttu-id="2b244-119">Im Debugmodus werden Ablaufverfolgungen zum Auffinden von Objekten mit speicherleckiertem Speicher ausstellen.</span><span class="sxs-lookup"><span data-stu-id="2b244-119">In debug mode, issuing traces to locate objects that have leaked memory.</span></span>
    
<span data-ttu-id="2b244-120">Wenn Ihre Abmeldemethode zurückgegeben wird, ruft MAPI Folgendes auf:</span><span class="sxs-lookup"><span data-stu-id="2b244-120">When your logoff method returns, MAPI calls the following:</span></span>
  
- <span data-ttu-id="2b244-121">Die **IUnknown::Release-Methode** des Anmeldeobjekts.</span><span class="sxs-lookup"><span data-stu-id="2b244-121">Your logon object's **IUnknown::Release** method.</span></span> 
    
- <span data-ttu-id="2b244-122">Die Shutdown-Methode des **Anbieterobjekts,** um alle endgültigen Bereinigungsaufgaben auszuführen.</span><span class="sxs-lookup"><span data-stu-id="2b244-122">Your provider object's **Shutdown** method to perform any final cleanup tasks.</span></span> <span data-ttu-id="2b244-123">Je nach Anbietertyp wird eine der folgenden Methoden aufgerufen:</span><span class="sxs-lookup"><span data-stu-id="2b244-123">Depending on the type of your provider, one of the following methods is called:</span></span> 
    
  - <span data-ttu-id="2b244-124">[IABProvider::Shutdown](iabprovider-shutdown.md) für Adressbuchanbieter</span><span class="sxs-lookup"><span data-stu-id="2b244-124">[IABProvider::Shutdown](iabprovider-shutdown.md) for address book providers</span></span> 
    
  - <span data-ttu-id="2b244-125">[IMSProvider::Shutdown](imsprovider-shutdown.md) für Nachrichtenspeicheranbieter</span><span class="sxs-lookup"><span data-stu-id="2b244-125">[IMSProvider::Shutdown](imsprovider-shutdown.md) for message store providers</span></span> 
    
  - <span data-ttu-id="2b244-126">[IXPProvider::Shutdown](ixpprovider-shutdown.md) für Transportanbieter</span><span class="sxs-lookup"><span data-stu-id="2b244-126">[IXPProvider::Shutdown](ixpprovider-shutdown.md) for transport providers</span></span> 
    
- <span data-ttu-id="2b244-127">Die **IUnknown::Release-Methode** Ihres Anbieterobjekts.</span><span class="sxs-lookup"><span data-stu-id="2b244-127">Your provider object's **IUnknown::Release** method.</span></span> 
    
<span data-ttu-id="2b244-128">Wenn es sich bei Ihrem Anbieter um einen Nachrichtenspeicher handelt, initiiert ein Clientaufruf an [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) auch den Herunterfahrensprozess.</span><span class="sxs-lookup"><span data-stu-id="2b244-128">If your provider is a message store, a client call to [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) will also initiate the shutdown process.</span></span> <span data-ttu-id="2b244-129">**StoreLogoff** beendet einen bestimmten Nachrichtenspeicheranbieter und hat keine Auswirkung auf die Sitzung.</span><span class="sxs-lookup"><span data-stu-id="2b244-129">**StoreLogoff** shuts down one particular message store provider and has no effect on the session.</span></span> <span data-ttu-id="2b244-130">Mit dieser Methode kann nur ein Nachrichtenspeicheranbieter heruntergefahren werden. Es gibt keine explizite Möglichkeit zum Herunterfahren eines bestimmten Adressbuchs oder Transportanbieters.</span><span class="sxs-lookup"><span data-stu-id="2b244-130">Only a message store provider can be shut down with this method; there is no explicit way to shut down a particular address book or transport provider.</span></span> <span data-ttu-id="2b244-131">Informationen zum Reagieren auf einen **StoreLogoff-Anruf** finden Sie unter [Shutting Down a Message Store Provider](shutting-down-a-message-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="2b244-131">For information about how to respond to a **StoreLogoff** call, see [Shutting Down a Message Store Provider](shutting-down-a-message-store-provider.md).</span></span>
  
<span data-ttu-id="2b244-132">Die DLL Ihres Anbieters wird entladen, wenn MAPI die Win32-API-Funktion **FreeLibrary** aufruft, ein Aufruf, der ausgeführt wird, nachdem der letzte aktive Client [MAPIUninitialize aufgerufen hat.](mapiuninitialize.md)</span><span class="sxs-lookup"><span data-stu-id="2b244-132">Your provider's DLL will be unloaded when MAPI calls the Win32 API function **FreeLibrary**, a call that is made after the last active client has called [MAPIUninitialize](mapiuninitialize.md).</span></span> <span data-ttu-id="2b244-133">Bis zu diesem Zeitpunkt ist das Herunterfahren des Dienstanbieters beendet.</span><span class="sxs-lookup"><span data-stu-id="2b244-133">By this time, your service provider will have finished shutting down.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2b244-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b244-134">See also</span></span>



[<span data-ttu-id="2b244-135">MAPI-Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="2b244-135">MAPI Service Providers</span></span>](mapi-service-providers.md)

