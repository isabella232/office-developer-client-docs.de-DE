---
title: Herunterfahren von einem Dienstanbieter
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e518830b-0aaa-4ce4-a85a-07e4f00750a9
description: 'Letzte �nderung: Montag, 7. Dezember 2015'
ms.openlocfilehash: 71706fc970170f74aa5555da29d904c08c0422f2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795542"
---
# <a name="shutting-down-a-service-provider"></a><span data-ttu-id="fc63c-103">Herunterfahren von einem Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="fc63c-103">Shutting Down a Service Provider</span></span>

 
  
<span data-ttu-id="fc63c-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fc63c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fc63c-105">Wenn ein Client die [IMAPISession::Logoff](imapisession-logoff.md) -Methode ruft, um die Sitzung zu beenden und alle aktiven-Dienstanbieter heruntergefahren, ruft MAPI wiederum die folgenden Methoden:</span><span class="sxs-lookup"><span data-stu-id="fc63c-105">When a client calls the [IMAPISession::Logoff](imapisession-logoff.md) method to end the session and shut down all active service providers, MAPI in turn calls the following methods:</span></span> 
  
- <span data-ttu-id="fc63c-106">[IABLogon::Logoff](iablogon-logoff.md) für adressbuchanbietern implementierte.</span><span class="sxs-lookup"><span data-stu-id="fc63c-106">[IABLogon::Logoff](iablogon-logoff.md) for address book providers.</span></span> 
    
- <span data-ttu-id="fc63c-107">[IMSLogon::Logoff](imslogon-logoff.md) für Nachricht-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="fc63c-107">[IMSLogon::Logoff](imslogon-logoff.md) for message store providers.</span></span> 
    
- <span data-ttu-id="fc63c-108">[IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) für Transportanbieter.</span><span class="sxs-lookup"><span data-stu-id="fc63c-108">[IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) for transport providers.</span></span> 
    
<span data-ttu-id="fc63c-109">Diese Methoden haben ähnliche Implementierungen.</span><span class="sxs-lookup"><span data-stu-id="fc63c-109">These methods have similar implementations.</span></span> <span data-ttu-id="fc63c-110">Die wichtigsten Aufgaben, die eine Abmeldung-Methode führt lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="fc63c-110">The main tasks that a logoff method performs are as follows:</span></span>
  
- <span data-ttu-id="fc63c-111">Veröffentlichen alle geöffneten Objekte, einschließlich Unterobjekte und Status-Objekte.</span><span class="sxs-lookup"><span data-stu-id="fc63c-111">Releasing all open objects, including subobjects and status objects.</span></span>
    
- <span data-ttu-id="fc63c-112">Aufrufen das Support-Objekt [IUnknown](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) -Methode, um die Anzahl der Verweise zu verringern.</span><span class="sxs-lookup"><span data-stu-id="fc63c-112">Calling the support object's [IUnknown::Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method to decrement its reference count.</span></span> 
    
- <span data-ttu-id="fc63c-113">Entfernen alle registrierten [MAPIUID](mapiuid.md) -Strukturen Ihres Anbieters.</span><span class="sxs-lookup"><span data-stu-id="fc63c-113">Removing all of your provider's registered [MAPIUID](mapiuid.md) structures.</span></span> 
    
- <span data-ttu-id="fc63c-114">Entfernen von Zeile des Anbieters in der Tabelle "Status".</span><span class="sxs-lookup"><span data-stu-id="fc63c-114">Removing your provider's row in the status table.</span></span>
    
- <span data-ttu-id="fc63c-115">Ausführen von Aufgaben, die zum Bereinigen von Ressourcen, wie die folgenden beziehen:</span><span class="sxs-lookup"><span data-stu-id="fc63c-115">Performing any tasks that relate to cleaning up resources, such as the following:</span></span>
    
  - <span data-ttu-id="fc63c-116">Beenden einer Verbindung mit einem Remoteserver.</span><span class="sxs-lookup"><span data-stu-id="fc63c-116">Terminating a connection with a remote server.</span></span>
    
  - <span data-ttu-id="fc63c-117">Verringern Sie den Verweis auf das Anmeldeobjekt zählen.</span><span class="sxs-lookup"><span data-stu-id="fc63c-117">Decrementing the reference count on the logon object.</span></span>
    
  - <span data-ttu-id="fc63c-118">Entfernen des Anmeldung-Objekts aus der Liste der Logon-Objekten, die vom Dienstanbieter speichert.</span><span class="sxs-lookup"><span data-stu-id="fc63c-118">Removing the logon object from the list of logon objects that your provider stores.</span></span>
    
  - <span data-ttu-id="fc63c-119">Im Debugmodus ausstellen Spuren, um Objekte zu suchen, die Speicher verloren haben.</span><span class="sxs-lookup"><span data-stu-id="fc63c-119">In debug mode, issuing traces to locate objects that have leaked memory.</span></span>
    
<span data-ttu-id="fc63c-120">Wenn Ihre Abmeldung-Methode zurückgegeben wird, ruft MAPI Folgendes:</span><span class="sxs-lookup"><span data-stu-id="fc63c-120">When your logoff method returns, MAPI calls the following:</span></span>
  
- <span data-ttu-id="fc63c-121">Die Anmeldung des Objekts **IUnknown** -Methode.</span><span class="sxs-lookup"><span data-stu-id="fc63c-121">Your logon object's **IUnknown::Release** method.</span></span> 
    
- <span data-ttu-id="fc63c-122">Provider-Objekts **Shutdown** -Methode der endgültige Cleanup Aufgaben ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fc63c-122">Your provider object's **Shutdown** method to perform any final cleanup tasks.</span></span> <span data-ttu-id="fc63c-123">Je nach Typ des vom Dienstanbieter wird eine der folgenden Methoden aufgerufen:</span><span class="sxs-lookup"><span data-stu-id="fc63c-123">Depending on the type of your provider, one of the following methods is called:</span></span> 
    
  - <span data-ttu-id="fc63c-124">[IABProvider::Shutdown](iabprovider-shutdown.md) für adressbuchanbietern implementierte</span><span class="sxs-lookup"><span data-stu-id="fc63c-124">[IABProvider::Shutdown](iabprovider-shutdown.md) for address book providers</span></span> 
    
  - <span data-ttu-id="fc63c-125">[IMSProvider::Shutdown](imsprovider-shutdown.md) für Nachricht-Anbieter</span><span class="sxs-lookup"><span data-stu-id="fc63c-125">[IMSProvider::Shutdown](imsprovider-shutdown.md) for message store providers</span></span> 
    
  - <span data-ttu-id="fc63c-126">[IXPProvider::Shutdown](ixpprovider-shutdown.md) für Transportanbieter</span><span class="sxs-lookup"><span data-stu-id="fc63c-126">[IXPProvider::Shutdown](ixpprovider-shutdown.md) for transport providers</span></span> 
    
- <span data-ttu-id="fc63c-127">**IUnknown** -Methode der Provider-Objekt.</span><span class="sxs-lookup"><span data-stu-id="fc63c-127">Your provider object's **IUnknown::Release** method.</span></span> 
    
<span data-ttu-id="fc63c-128">Wenn der Anbieter einen Nachrichtenspeicher ist, wird ein Clientaufruf von [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) auch des Herunterfahrens initiieren.</span><span class="sxs-lookup"><span data-stu-id="fc63c-128">If your provider is a message store, a client call to [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) will also initiate the shutdown process.</span></span> <span data-ttu-id="fc63c-129">**StoreLogoff** Anbieter für eine bestimmte Nachricht anmelden heruntergefahren und hat keine Auswirkung auf die Sitzung.</span><span class="sxs-lookup"><span data-stu-id="fc63c-129">**StoreLogoff** shuts down one particular message store provider and has no effect on the session.</span></span> <span data-ttu-id="fc63c-130">Mit dieser Methode kann nur eine Nachricht Speicheranbieter heruntergefahren werden; Es gibt keine explizite Möglichkeit zum Herunterfahren von eines bestimmten Adresse Adressbuch oder Transport Anbieters.</span><span class="sxs-lookup"><span data-stu-id="fc63c-130">Only a message store provider can be shut down with this method; there is no explicit way to shut down a particular address book or transport provider.</span></span> <span data-ttu-id="fc63c-131">[Herunterfahren nach unten einer Nachricht Speicheranbieter](shutting-down-a-message-store-provider.md)finden Sie Informationen zur Beantwortung einer **StoreLogoff** aufrufen ist.</span><span class="sxs-lookup"><span data-stu-id="fc63c-131">For information about how to respond to a **StoreLogoff** call, see [Shutting Down a Message Store Provider](shutting-down-a-message-store-provider.md).</span></span>
  
<span data-ttu-id="fc63c-132">DLL des Anbieters werden entfernt, wenn MAPI Win32 API-Funktion **FreeLibrary**, einen Anruf aufruft, der ausgeführt wird, nachdem der letzte aktive Client [MAPIUninitialize](mapiuninitialize.md)aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="fc63c-132">Your provider's DLL will be unloaded when MAPI calls the Win32 API function **FreeLibrary**, a call that is made after the last active client has called [MAPIUninitialize](mapiuninitialize.md).</span></span> <span data-ttu-id="fc63c-133">Zu diesem Zeitpunkt wird Ihren Dienstanbieter abgeschlossen haben, wird beendet.</span><span class="sxs-lookup"><span data-stu-id="fc63c-133">By this time, your service provider will have finished shutting down.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fc63c-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fc63c-134">See also</span></span>



[<span data-ttu-id="fc63c-135">MAPI-Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="fc63c-135">MAPI Service Providers</span></span>](mapi-service-providers.md)

