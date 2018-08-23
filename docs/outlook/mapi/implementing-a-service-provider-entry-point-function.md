---
title: Implementieren einer Dienstanbieter-Einstiegspunktfunktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 83ff54c4-86ce-4529-ae45-260dfb763b30
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 40bbe110c7453cf2360fc103710fbc3bcb7f1c67
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572053"
---
# <a name="implementing-a-service-provider-entry-point-function"></a><span data-ttu-id="3401a-103">Implementieren einer Dienstanbieter-Einstiegspunktfunktion</span><span class="sxs-lookup"><span data-stu-id="3401a-103">Implementing a Service Provider Entry Point Function</span></span>

  
  
<span data-ttu-id="3401a-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3401a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3401a-105">Jeder Dienstanbieter DLL hat einen Eintrag Funktion verweist, die MAPI-aufrufen, um sie zu laden.</span><span class="sxs-lookup"><span data-stu-id="3401a-105">Every service provider DLL has an entry point function that MAPI calls to load it.</span></span> <span data-ttu-id="3401a-106">Beachten Sie, dass dieser Eintrag Point-Funktion nicht [DllMain](http://msdn.microsoft.com/en-us/library/ms682583.aspx), die Win32-DLL-Einstiegspunktfunktion identisch ist.</span><span class="sxs-lookup"><span data-stu-id="3401a-106">Be aware that this entry point function is not the same as [DllMain](http://msdn.microsoft.com/en-us/library/ms682583.aspx), the Win32 DLL entry point function.</span></span>
  
<span data-ttu-id="3401a-107">Je nach Typ des vom Dienstanbieter entspricht anderer Prototyp Ihrem Anbieter Eintrag Point-Funktion.</span><span class="sxs-lookup"><span data-stu-id="3401a-107">Depending on the type of your provider, your provider entry point function conforms to a different prototype.</span></span> <span data-ttu-id="3401a-108">MAPI definiert anderen Eintrag Punkt Prototypen für Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="3401a-108">MAPI defines different entry point function prototypes for service providers.</span></span>
  
|<span data-ttu-id="3401a-109">**Provider**</span><span class="sxs-lookup"><span data-stu-id="3401a-109">**Provider**</span></span>|<span data-ttu-id="3401a-110">**Entry Point-Funktionsprototyp**</span><span class="sxs-lookup"><span data-stu-id="3401a-110">**Entry point function prototype**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3401a-111">Nachricht-Anbieter</span><span class="sxs-lookup"><span data-stu-id="3401a-111">Message store providers</span></span>  <br/> |[<span data-ttu-id="3401a-112">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="3401a-112">MSProviderInit</span></span>](msproviderinit.md) <br/> |
|<span data-ttu-id="3401a-113">Transportanbieter</span><span class="sxs-lookup"><span data-stu-id="3401a-113">Transport providers</span></span>  <br/> |[<span data-ttu-id="3401a-114">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="3401a-114">XPProviderInit</span></span>](xpproviderinit.md) <br/> |
|<span data-ttu-id="3401a-115">Von adressbuchanbietern implementierte</span><span class="sxs-lookup"><span data-stu-id="3401a-115">Address book providers</span></span>  <br/> |[<span data-ttu-id="3401a-116">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="3401a-116">ABProviderInit</span></span>](abproviderinit.md) <br/> |
   
<span data-ttu-id="3401a-117">Die Funktionalität in diese Prototypen entspricht weitgehend für alle Typen von Service Provider.</span><span class="sxs-lookup"><span data-stu-id="3401a-117">Much of the functionality in these prototypes is the same for all service provider types.</span></span> 
  
<span data-ttu-id="3401a-118">Adressbuch, Nachrichtenspeicher und Transportanbieter führen die folgenden zwei Hauptaufgaben in deren Entry Point-Funktionen:</span><span class="sxs-lookup"><span data-stu-id="3401a-118">Address book, message store, and transport providers perform the following two main tasks in their entry point functions:</span></span>
  
1. <span data-ttu-id="3401a-119">Überprüfen Sie die Version der der Dienstanbieter-Schnittstelle (SPI) um sicherzustellen, dass MAPI eine Version verwendet, die mit der Version kompatibel ist, die Ihren Dienstanbieter verwendet.</span><span class="sxs-lookup"><span data-stu-id="3401a-119">Check the version of the service provider interface (SPI) to be sure that MAPI is using a version that is compatible with the version that your service provider is using.</span></span> <span data-ttu-id="3401a-120">Verwenden Sie den _LpulMAPIVer_ -Parameter, der die MAPI SPI-Version enthält, und der _LpulProviderVer_ -Parameter, der Ihre Version SPI enthält, des Überprüfens.</span><span class="sxs-lookup"><span data-stu-id="3401a-120">Use the  _lpulMAPIVer_ parameter, which contains the MAPI SPI version, and the  _lpulProviderVer_ parameter, which contains your SPI version, to perform the check.</span></span> <span data-ttu-id="3401a-121">Diese Parameter sind nicht signierte 32-Bit-Ganzzahl bestehend aus drei Teilen:</span><span class="sxs-lookup"><span data-stu-id="3401a-121">These parameters are 32-bit unsigned integers composed of three parts:</span></span> 
    
  - <span data-ttu-id="3401a-122">Bits 24 bis 31 stellen die Hauptversion dar.</span><span class="sxs-lookup"><span data-stu-id="3401a-122">Bits 24 through 31 represent the major version.</span></span>
    
  - <span data-ttu-id="3401a-123">Bits 16 bis 23 darstellen, die Nebenversion.</span><span class="sxs-lookup"><span data-stu-id="3401a-123">Bits 16 through 23 represent the minor version.</span></span>
    
  - <span data-ttu-id="3401a-124">Die Bits 0 bis 15 darstellen den Update-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="3401a-124">Bits 0 through 15 represent the update identifier.</span></span> <span data-ttu-id="3401a-125">Obwohl die Nummer der Hauptversion selten geändert werden, die Nebenversionsnummer Änderungen bei jedem MAPI freigegeben wird und die SPI geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="3401a-125">Although the major version number rarely changes, the minor version number changes whenever MAPI is released and the SPI has changed.</span></span> <span data-ttu-id="3401a-126">Die Update-ID ist die Microsoft-interne Buildversion. Es wird verwendet, um Änderungen während der Entwicklung nachzuverfolgen.</span><span class="sxs-lookup"><span data-stu-id="3401a-126">The update identifier is the Microsoft internal build version; it is used to track changes during the development process.</span></span> <span data-ttu-id="3401a-127">MAPI definiert die CURRENT_SPI_VERSION-Konstante, in der Headerdatei Mapispi.h an, dass der derzeitigen SPI-Version dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="3401a-127">MAPI defines the CURRENT_SPI_VERSION constant, documented in the Mapispi.h header file, to indicate the present SPI version.</span></span> <span data-ttu-id="3401a-128">Die Kontrollkästchen der Fehler MAPI_E_VERSION fehl, wenn Sie eine Version der SPI verwenden, die neuer als die Version, die MAPI verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3401a-128">Fail your check with the error MAPI_E_VERSION if you are using a version of the SPI that is newer than the version that MAPI is using.</span></span>
    
2. <span data-ttu-id="3401a-129">Erstellt eine Instanz eines Objekts vom Anbieter.</span><span class="sxs-lookup"><span data-stu-id="3401a-129">Create an instance of a provider object.</span></span> <span data-ttu-id="3401a-130">Da der Anbieter gestartet und mehrmals initialisiert werden kann, sollten Sie eine neue Instanz jedes Mal erstellen, die in diesem Fall.</span><span class="sxs-lookup"><span data-stu-id="3401a-130">Because your provider can be started and initialized multiple times, you should create a new instance each time this occurs.</span></span> <span data-ttu-id="3401a-131">Anbieter werden mehrere Male gestartet, wenn sie in mehreren Profilen angezeigt werden, die von einem oder mehreren Clients gleichzeitig verwendet werden, oder wenn sie mehrere Male in einem einzigen Profil angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="3401a-131">Providers are started multiple times when they appear in multiple profiles that are in use simultaneously by one or more clients, or when they appear multiple times in a single profile.</span></span> <span data-ttu-id="3401a-132">Nur wächst der Eintrag Point-Funktionsprototyp je nach den Typ des vom Dienstanbieter abweicht, den Typ der Provider-Objekt.</span><span class="sxs-lookup"><span data-stu-id="3401a-132">Just as the entry point function prototype differs depending on the type of your provider, so does the type of provider object.</span></span> 
    
    <span data-ttu-id="3401a-133">Wenn Sie eine Adressbuchanbieter schreiben, implementieren [IABProvider: IUnknown](iabprovideriunknown.md).</span><span class="sxs-lookup"><span data-stu-id="3401a-133">If you are writing an address book provider, implement [IABProvider : IUnknown](iabprovideriunknown.md).</span></span> <span data-ttu-id="3401a-134">Wenn Sie eine Nachricht Speicheranbieter schreiben, implementieren [IMSProvider: IUnknown](imsprovideriunknown.md).</span><span class="sxs-lookup"><span data-stu-id="3401a-134">If you are writing a message store provider, implement [IMSProvider : IUnknown](imsprovideriunknown.md).</span></span> <span data-ttu-id="3401a-135">Weitere Informationen finden Sie unter [Message-Anbieter laden](loading-message-store-providers.md).</span><span class="sxs-lookup"><span data-stu-id="3401a-135">For more information, see [Loading Message Store Providers](loading-message-store-providers.md).</span></span>
    
    <span data-ttu-id="3401a-136">Wenn Sie eine Adressbuchhierarchie schreiben, implementieren [IXPProvider: IUnknown](ixpprovideriunknown.md).</span><span class="sxs-lookup"><span data-stu-id="3401a-136">If you are writing a transport provider, implement [IXPProvider : IUnknown](ixpprovideriunknown.md).</span></span> <span data-ttu-id="3401a-137">Weitere Informationen finden Sie unter [der Adressbuchhierarchie initialisieren](initializing-the-transport-provider.md).</span><span class="sxs-lookup"><span data-stu-id="3401a-137">For more information, see [Initializing the Transport Provider](initializing-the-transport-provider.md).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3401a-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3401a-138">See also</span></span>



[<span data-ttu-id="3401a-139">Starten eines Dienstanbieters</span><span class="sxs-lookup"><span data-stu-id="3401a-139">Starting a Service Provider</span></span>](starting-a-service-provider.md)

