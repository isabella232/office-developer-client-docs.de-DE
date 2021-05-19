---
title: Implementieren einer Einstiegspunktfunktion des Adressbuchanbieters
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9375b351-1c84-4728-bcdf-e3e7a44820ed
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 00b3b30101ee1efb984cf45afb35b0b085d545ac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409713"
---
# <a name="implementing-an-address-book-provider-entry-point-function"></a><span data-ttu-id="a3c26-103">Implementieren einer Einstiegspunktfunktion des Adressbuchanbieters</span><span class="sxs-lookup"><span data-stu-id="a3c26-103">Implementing an Address Book Provider Entry Point Function</span></span>

  
  
<span data-ttu-id="a3c26-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a3c26-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a3c26-105">Wenn eine Clientanwendung [MAPILogonEx](mapilogonex.md) aufruft, um eine Sitzung mit einem Profil zu beginnen, das Ihren Adressbuchanbieter enthält, lädt MAPI Ihren Anbieter und alle anderen, die Teil des Profils sind.</span><span class="sxs-lookup"><span data-stu-id="a3c26-105">When a client application calls [MAPILogonEx](mapilogonex.md) to begin a session using a profile that contains your address book provider, MAPI loads your provider and all others that are part of the profile.</span></span> <span data-ttu-id="a3c26-106">MAPI erfährt den Namen der Einstiegspunktfunktion Ihres Anbieters, indem sie im Profil nachschaut.</span><span class="sxs-lookup"><span data-stu-id="a3c26-106">MAPI learns of the name of your provider's entry point function by looking in the profile.</span></span> <span data-ttu-id="a3c26-107">Beachten Sie, dass diese Funktion nicht mit einer #A0 identisch ist. Weitere Informationen finden Sie in der Dokumentation zu **DllMain** in der Win32-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="a3c26-107">Remember that this function is not the same as a DLL entry point function; see the documentation for **DllMain** in the Win32 documentation.</span></span> 
  
<span data-ttu-id="a3c26-108">Es gibt mehrere Einträge, von denen einige in der Konfigurationsdatei mapisvc.inf angezeigt werden müssen, die im Profilabschnitt jedes Adressbuchanbieters enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="a3c26-108">There are several entries, some of which must appear in the mapisvc.inf configuration file, that are included in the profile section of every address book provider.</span></span> <span data-ttu-id="a3c26-109">In der folgenden Tabelle sind diese Profilabschnittseinträge aufgeführt, und ob die datei mapisvc.inf diese enthalten muss.</span><span class="sxs-lookup"><span data-stu-id="a3c26-109">The following table lists these profile section entries and whether or not the mapisvc.inf file must include them.</span></span>
  
|<span data-ttu-id="a3c26-110">**Profilabschnittseintrag**</span><span class="sxs-lookup"><span data-stu-id="a3c26-110">**Profile section entry**</span></span>|<span data-ttu-id="a3c26-111">**mapisvc.inf-Anforderung**</span><span class="sxs-lookup"><span data-stu-id="a3c26-111">**mapisvc.inf requirement**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a3c26-112">PR_DISPLAY_NAME= _Zeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="a3c26-112">PR_DISPLAY_NAME= _string_</span></span> <br/> |<span data-ttu-id="a3c26-113">Optional.</span><span class="sxs-lookup"><span data-stu-id="a3c26-113">Optional</span></span>  <br/> |
|<span data-ttu-id="a3c26-114">_PR_PROVIDER_DISPLAY=-Zeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="a3c26-114">PR_PROVIDER_DISPLAY= _string_</span></span> <br/> |<span data-ttu-id="a3c26-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a3c26-115">Required</span></span>  <br/> |
|<span data-ttu-id="a3c26-116">PR_PROVIDER_DLL_NAME= _DLL-Dateiname_</span><span class="sxs-lookup"><span data-stu-id="a3c26-116">PR_PROVIDER_DLL_NAME= _DLL filename_</span></span> <br/> |<span data-ttu-id="a3c26-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a3c26-117">Required</span></span>  <br/> |
|<span data-ttu-id="a3c26-118">PR_RESOURCE_TYPE= _long_</span><span class="sxs-lookup"><span data-stu-id="a3c26-118">PR_RESOURCE_TYPE= _long_</span></span> <br/> |<span data-ttu-id="a3c26-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a3c26-119">Required</span></span>  <br/> |
|<span data-ttu-id="a3c26-120">PR_RESOURCE_FLAGS= _bitmask_</span><span class="sxs-lookup"><span data-stu-id="a3c26-120">PR_RESOURCE_FLAGS= _bitmask_</span></span> <br/> |<span data-ttu-id="a3c26-121">Optional.</span><span class="sxs-lookup"><span data-stu-id="a3c26-121">Optional</span></span>  <br/> |
   
<span data-ttu-id="a3c26-122">Ihr Adressbuchanbieter kann diese Informationen direkt in einem Profil platzieren, indem er die [IMAPIProp::SetProps-Methode des Profilabschnitts](imapiprop-setprops.md) aufruft oder indirekt MAPISVC.INF ändert.</span><span class="sxs-lookup"><span data-stu-id="a3c26-122">Your address book provider can place this information into a profile directly by calling its profile section's [IMAPIProp::SetProps](imapiprop-setprops.md) method or indirectly by modifying MAPISVC.INF.</span></span> <span data-ttu-id="a3c26-123">Profile werden mithilfe der relevanten Informationen in MAPISVC erstellt. INF für die ausgewählten Dienstanbieter oder Nachrichtendienste.</span><span class="sxs-lookup"><span data-stu-id="a3c26-123">Profiles are built using the relevant information in MAPISVC.INF for the selected service providers or message services.</span></span> <span data-ttu-id="a3c26-124">Weitere Informationen zur Organisation und zum Inhalt von MAPISVC. INF, siehe [Dateiformat von MapiSvc.inf](file-format-of-mapisvc-inf.md).</span><span class="sxs-lookup"><span data-stu-id="a3c26-124">For more information about the organization and contents of MAPISVC.INF, see [File Format of MapiSvc.inf](file-format-of-mapisvc-inf.md).</span></span>
  
<span data-ttu-id="a3c26-125">Der Name der DLL-Einstiegspunktfunktion Ihres Adressbuchanbieters muss [ABProviderInit](abproviderinit.md) sein und dem **ABProviderInit-Prototyp** entsprechen.</span><span class="sxs-lookup"><span data-stu-id="a3c26-125">The name of your address book provider's DLL entry point function must be [ABProviderInit](abproviderinit.md) and it must conform to the **ABProviderInit** prototype.</span></span> <span data-ttu-id="a3c26-126">Führen Sie die folgenden Aufgaben in der DLL-Einstiegspunktfunktion Ihres Anbieters aus:</span><span class="sxs-lookup"><span data-stu-id="a3c26-126">Perform the following tasks in your provider's DLL entry point function:</span></span> 
  
- <span data-ttu-id="a3c26-127">Überprüfen Sie die Version der Dienstanbieterschnittstelle (Service Provider Interface, SPI), um sicherzustellen, dass MAPI eine Version verwendet, die mit der Version kompatibel ist, die Ihr Adressbuchanbieter verwendet.</span><span class="sxs-lookup"><span data-stu-id="a3c26-127">Check the version of the service provider interface (SPI) to make sure MAPI is using a version that is compatible with the version that your address book provider is using.</span></span>
    
- <span data-ttu-id="a3c26-128">Instanziieren eines Adressbuchanbieterobjekts.</span><span class="sxs-lookup"><span data-stu-id="a3c26-128">Instantiate an address book provider object.</span></span>
    
<span data-ttu-id="a3c26-129">Rufen Sie weder **MAPIInitialize** noch **MAPIUninitialize** in dieser Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="a3c26-129">Do not call either **MAPIInitialize** or **MAPIUninitialize** in this function.</span></span> 
  
<span data-ttu-id="a3c26-130">Die DLL-Einstiegspunktfunktion instanziiert ein Anbieterobjekt und gibt an MAPI einen Zeiger auf dieses Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="a3c26-130">The DLL entry point function instantiates a provider object and returns to MAPI a pointer to that object.</span></span> 
  

