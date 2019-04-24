---
title: Implementieren einer Dienstanbieter-Einstiegspunktfunktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 83ff54c4-86ce-4529-ae45-260dfb763b30
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 14dd11f873493e32b83dbd1960cac8ff8ef8e436
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332991"
---
# <a name="implementing-a-service-provider-entry-point-function"></a><span data-ttu-id="cadb8-103">Implementieren einer Dienstanbieter-Einstiegspunktfunktion</span><span class="sxs-lookup"><span data-stu-id="cadb8-103">Implementing a Service Provider Entry Point Function</span></span>

  
  
<span data-ttu-id="cadb8-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cadb8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cadb8-105">Jede Dienstanbieter-DLL verfügt über eine Einstiegspunktfunktion, die von MAPI aufgerufen wird, um Sie zu laden.</span><span class="sxs-lookup"><span data-stu-id="cadb8-105">Every service provider DLL has an entry point function that MAPI calls to load it.</span></span> <span data-ttu-id="cadb8-106">Beachten Sie, dass diese Einstiegspunktfunktion nicht mit [DllMain](https://msdn.microsoft.com/library/ms682583.aspx), der Win32-DLL-Einstiegspunktfunktion, identisch ist.</span><span class="sxs-lookup"><span data-stu-id="cadb8-106">Be aware that this entry point function is not the same as [DllMain](https://msdn.microsoft.com/library/ms682583.aspx), the Win32 DLL entry point function.</span></span>
  
<span data-ttu-id="cadb8-107">Je nach Typ des Anbieters entspricht die Einstiegspunktfunktion des Anbieters einem anderen Prototyp.</span><span class="sxs-lookup"><span data-stu-id="cadb8-107">Depending on the type of your provider, your provider entry point function conforms to a different prototype.</span></span> <span data-ttu-id="cadb8-108">MAPI definiert unterschiedliche Prototypen für Einstiegspunktfunktionen für Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="cadb8-108">MAPI defines different entry point function prototypes for service providers.</span></span>
  
|<span data-ttu-id="cadb8-109">**Provider**</span><span class="sxs-lookup"><span data-stu-id="cadb8-109">**Provider**</span></span>|<span data-ttu-id="cadb8-110">**Prototyp der Einstiegspunktfunktion**</span><span class="sxs-lookup"><span data-stu-id="cadb8-110">**Entry point function prototype**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cadb8-111">Nachrichtenspeicher Anbieter</span><span class="sxs-lookup"><span data-stu-id="cadb8-111">Message store providers</span></span>  <br/> |[<span data-ttu-id="cadb8-112">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="cadb8-112">MSProviderInit</span></span>](msproviderinit.md) <br/> |
|<span data-ttu-id="cadb8-113">Transport Anbieter</span><span class="sxs-lookup"><span data-stu-id="cadb8-113">Transport providers</span></span>  <br/> |[<span data-ttu-id="cadb8-114">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="cadb8-114">XPProviderInit</span></span>](xpproviderinit.md) <br/> |
|<span data-ttu-id="cadb8-115">Adressbuchanbieter</span><span class="sxs-lookup"><span data-stu-id="cadb8-115">Address book providers</span></span>  <br/> |[<span data-ttu-id="cadb8-116">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="cadb8-116">ABProviderInit</span></span>](abproviderinit.md) <br/> |
   
<span data-ttu-id="cadb8-117">Ein großer Teil der Funktionalität in diesen Prototypen ist für alle Dienstanbieter Typen identisch.</span><span class="sxs-lookup"><span data-stu-id="cadb8-117">Much of the functionality in these prototypes is the same for all service provider types.</span></span> 
  
<span data-ttu-id="cadb8-118">Adressbuch, Nachrichtenspeicher und Transportanbieter führen die folgenden beiden Hauptaufgaben in ihren Einstiegspunktfunktionen aus:</span><span class="sxs-lookup"><span data-stu-id="cadb8-118">Address book, message store, and transport providers perform the following two main tasks in their entry point functions:</span></span>
  
1. <span data-ttu-id="cadb8-119">Überprüfen Sie die Version der Service Provider Interface (SPI), um sicherzustellen, dass MAPI eine Version verwendet, die mit der Version kompatibel ist, die Ihr Dienstanbieter verwendet.</span><span class="sxs-lookup"><span data-stu-id="cadb8-119">Check the version of the service provider interface (SPI) to be sure that MAPI is using a version that is compatible with the version that your service provider is using.</span></span> <span data-ttu-id="cadb8-120">Verwenden Sie den _lpulMAPIVer_ -Parameter, der die MAPI-SPI-Version enthält, und den _lpulProviderVer_ -Parameter, der Ihre SPI-Version enthält, um die Prüfung durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="cadb8-120">Use the  _lpulMAPIVer_ parameter, which contains the MAPI SPI version, and the  _lpulProviderVer_ parameter, which contains your SPI version, to perform the check.</span></span> <span data-ttu-id="cadb8-121">Diese Parameter sind 32-Bit-Ganzzahlen ohne Vorzeichen aus drei Teilen:</span><span class="sxs-lookup"><span data-stu-id="cadb8-121">These parameters are 32-bit unsigned integers composed of three parts:</span></span> 
    
  - <span data-ttu-id="cadb8-122">Die Bits 24 bis 31 stellen die Hauptversion dar.</span><span class="sxs-lookup"><span data-stu-id="cadb8-122">Bits 24 through 31 represent the major version.</span></span>
    
  - <span data-ttu-id="cadb8-123">Die Bits 16 bis 23 stellen die Nebenversion dar.</span><span class="sxs-lookup"><span data-stu-id="cadb8-123">Bits 16 through 23 represent the minor version.</span></span>
    
  - <span data-ttu-id="cadb8-124">Die Bits 0 bis 15 stellen den Update Bezeichner dar.</span><span class="sxs-lookup"><span data-stu-id="cadb8-124">Bits 0 through 15 represent the update identifier.</span></span> <span data-ttu-id="cadb8-125">Obwohl sich die Hauptversionsnummer selten ändert, ändert sich die Versionsnummer der Nebenversion immer dann, wenn MAPI veröffentlicht und der SPI geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="cadb8-125">Although the major version number rarely changes, the minor version number changes whenever MAPI is released and the SPI has changed.</span></span> <span data-ttu-id="cadb8-126">Die Update-ID ist die interne Microsoft-Buildversion; Es wird verwendet, um Änderungen während des Entwicklungsprozesses nachzuverfolgen.</span><span class="sxs-lookup"><span data-stu-id="cadb8-126">The update identifier is the Microsoft internal build version; it is used to track changes during the development process.</span></span> <span data-ttu-id="cadb8-127">MAPI definiert die CURRENT_SPI_VERSION-Konstante, die in der Headerdatei Mapispi. h dokumentiert ist, um die aktuelle SPI-Version anzugeben.</span><span class="sxs-lookup"><span data-stu-id="cadb8-127">MAPI defines the CURRENT_SPI_VERSION constant, documented in the Mapispi.h header file, to indicate the present SPI version.</span></span> <span data-ttu-id="cadb8-128">Führen Sie die Überprüfung mit dem Fehler MAPI_E_VERSION aus, wenn Sie eine Version des SPI verwenden, die neuer als die von MAPI verwendete Version ist.</span><span class="sxs-lookup"><span data-stu-id="cadb8-128">Fail your check with the error MAPI_E_VERSION if you are using a version of the SPI that is newer than the version that MAPI is using.</span></span>
    
2. <span data-ttu-id="cadb8-129">Erstellen Sie eine Instanz eines Provider-Objekts.</span><span class="sxs-lookup"><span data-stu-id="cadb8-129">Create an instance of a provider object.</span></span> <span data-ttu-id="cadb8-130">Da Ihr Anbieter mehrmals gestartet und initialisiert werden kann, sollten Sie jedesmal eine neue Instanz erstellen.</span><span class="sxs-lookup"><span data-stu-id="cadb8-130">Because your provider can be started and initialized multiple times, you should create a new instance each time this occurs.</span></span> <span data-ttu-id="cadb8-131">Anbieter werden mehrmals gestartet, wenn Sie in mehreren Profilen angezeigt werden, die gleichzeitig von einem oder mehreren Clients verwendet werden, oder wenn Sie mehrmals in einem einzigen Profil angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="cadb8-131">Providers are started multiple times when they appear in multiple profiles that are in use simultaneously by one or more clients, or when they appear multiple times in a single profile.</span></span> <span data-ttu-id="cadb8-132">Ebenso wie der Prototyp der Einstiegspunktfunktion in Abhängigkeit vom Typ des Anbieters unterschiedlich ist, wird auch der Typ des Anbieterobjekts verwendet.</span><span class="sxs-lookup"><span data-stu-id="cadb8-132">Just as the entry point function prototype differs depending on the type of your provider, so does the type of provider object.</span></span> 
    
    <span data-ttu-id="cadb8-133">Wenn Sie einen Adressbuchanbieter schreiben, implementieren Sie [IABProvider: IUnknown](iabprovideriunknown.md).</span><span class="sxs-lookup"><span data-stu-id="cadb8-133">If you are writing an address book provider, implement [IABProvider : IUnknown](iabprovideriunknown.md).</span></span> <span data-ttu-id="cadb8-134">Wenn Sie einen Nachrichtenspeicher Anbieter schreiben, implementieren Sie [IMSProvider: IUnknown](imsprovideriunknown.md).</span><span class="sxs-lookup"><span data-stu-id="cadb8-134">If you are writing a message store provider, implement [IMSProvider : IUnknown](imsprovideriunknown.md).</span></span> <span data-ttu-id="cadb8-135">Weitere Informationen finden Sie unter [Loading Message Store Providers](loading-message-store-providers.md).</span><span class="sxs-lookup"><span data-stu-id="cadb8-135">For more information, see [Loading Message Store Providers](loading-message-store-providers.md).</span></span>
    
    <span data-ttu-id="cadb8-136">Wenn Sie einen Transportanbieter schreiben, implementieren Sie [IXPProvider: IUnknown](ixpprovideriunknown.md).</span><span class="sxs-lookup"><span data-stu-id="cadb8-136">If you are writing a transport provider, implement [IXPProvider : IUnknown](ixpprovideriunknown.md).</span></span> <span data-ttu-id="cadb8-137">Weitere Informationen finden Sie unter [Initialisieren des Transport Anbieters](initializing-the-transport-provider.md).</span><span class="sxs-lookup"><span data-stu-id="cadb8-137">For more information, see [Initializing the Transport Provider](initializing-the-transport-provider.md).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cadb8-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cadb8-138">See also</span></span>



[<span data-ttu-id="cadb8-139">Starten eines Dienstanbieters</span><span class="sxs-lookup"><span data-stu-id="cadb8-139">Starting a Service Provider</span></span>](starting-a-service-provider.md)

