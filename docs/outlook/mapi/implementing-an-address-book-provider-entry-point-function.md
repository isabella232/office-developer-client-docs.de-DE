---
title: Implementieren einer Adressbuchanbieter-Einstiegspunktfunktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9375b351-1c84-4728-bcdf-e3e7a44820ed
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 00b3b30101ee1efb984cf45afb35b0b085d545ac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332802"
---
# <a name="implementing-an-address-book-provider-entry-point-function"></a><span data-ttu-id="cc0e6-103">Implementieren einer Adressbuchanbieter-Einstiegspunktfunktion</span><span class="sxs-lookup"><span data-stu-id="cc0e6-103">Implementing an Address Book Provider Entry Point Function</span></span>

  
  
<span data-ttu-id="cc0e6-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cc0e6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cc0e6-105">Wenn eine Clientanwendung [MAPILogonEx](mapilogonex.md) aufruft, um eine Sitzung mit einem Profil zu beginnen, das Ihren Adressbuchanbieter enthält, lädt MAPI Ihren Anbieter und alle anderen Teil des Profils.</span><span class="sxs-lookup"><span data-stu-id="cc0e6-105">When a client application calls [MAPILogonEx](mapilogonex.md) to begin a session using a profile that contains your address book provider, MAPI loads your provider and all others that are part of the profile.</span></span> <span data-ttu-id="cc0e6-106">MAPI lernt den Namen der Einstiegspunktfunktion Ihres Anbieters, indem er im Profil nachsieht.</span><span class="sxs-lookup"><span data-stu-id="cc0e6-106">MAPI learns of the name of your provider's entry point function by looking in the profile.</span></span> <span data-ttu-id="cc0e6-107">Beachten Sie, dass diese Funktion nicht mit einer DLL-Einstiegspunktfunktion identisch ist. Weitere Informationen finden Sie in der Dokumentation zu **DllMain** in der Win32-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="cc0e6-107">Remember that this function is not the same as a DLL entry point function; see the documentation for **DllMain** in the Win32 documentation.</span></span> 
  
<span data-ttu-id="cc0e6-108">Es gibt mehrere Einträge, von denen einige in der MAPISVC. inf-Konfigurationsdatei enthalten sein müssen, die im profile-Abschnitt jedes Adressbuch Anbieters aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="cc0e6-108">There are several entries, some of which must appear in the mapisvc.inf configuration file, that are included in the profile section of every address book provider.</span></span> <span data-ttu-id="cc0e6-109">In der folgenden Tabelle sind diese Profil Abschnitts Einträge aufgeführt, und ob die Datei MAPISVC. inf Diese enthält.</span><span class="sxs-lookup"><span data-stu-id="cc0e6-109">The following table lists these profile section entries and whether or not the mapisvc.inf file must include them.</span></span>
  
|<span data-ttu-id="cc0e6-110">**Profil Abschnitts Eintrag**</span><span class="sxs-lookup"><span data-stu-id="cc0e6-110">**Profile section entry**</span></span>|<span data-ttu-id="cc0e6-111">**MAPISVC. inf-Anforderung**</span><span class="sxs-lookup"><span data-stu-id="cc0e6-111">**mapisvc.inf requirement**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cc0e6-112">PR_DISPLAY_NAME = _Zeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="cc0e6-112">PR_DISPLAY_NAME= _string_</span></span> <br/> |<span data-ttu-id="cc0e6-113">Optional</span><span class="sxs-lookup"><span data-stu-id="cc0e6-113">Optional</span></span>  <br/> |
|<span data-ttu-id="cc0e6-114">PR_PROVIDER_DISPLAY = _Zeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="cc0e6-114">PR_PROVIDER_DISPLAY= _string_</span></span> <br/> |<span data-ttu-id="cc0e6-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="cc0e6-115">Required</span></span>  <br/> |
|<span data-ttu-id="cc0e6-116">PR_PROVIDER_DLL_NAME = _dll filename_</span><span class="sxs-lookup"><span data-stu-id="cc0e6-116">PR_PROVIDER_DLL_NAME= _DLL filename_</span></span> <br/> |<span data-ttu-id="cc0e6-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="cc0e6-117">Required</span></span>  <br/> |
|<span data-ttu-id="cc0e6-118">PR_RESOURCE_TYPE = _Long_</span><span class="sxs-lookup"><span data-stu-id="cc0e6-118">PR_RESOURCE_TYPE= _long_</span></span> <br/> |<span data-ttu-id="cc0e6-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="cc0e6-119">Required</span></span>  <br/> |
|<span data-ttu-id="cc0e6-120">PR_RESOURCE_FLAGS = _Bitmaske_</span><span class="sxs-lookup"><span data-stu-id="cc0e6-120">PR_RESOURCE_FLAGS= _bitmask_</span></span> <br/> |<span data-ttu-id="cc0e6-121">Optional</span><span class="sxs-lookup"><span data-stu-id="cc0e6-121">Optional</span></span>  <br/> |
   
<span data-ttu-id="cc0e6-122">Ihr Adressbuchanbieter kann diese Informationen direkt in einem Profil platzieren, indem er die [IMAPIProp::](imapiprop-setprops.md) SetProps-Methode des Profil Abschnitts oder indirekt durch Ändern von MAPISVC. inf aufruft.</span><span class="sxs-lookup"><span data-stu-id="cc0e6-122">Your address book provider can place this information into a profile directly by calling its profile section's [IMAPIProp::SetProps](imapiprop-setprops.md) method or indirectly by modifying MAPISVC.INF.</span></span> <span data-ttu-id="cc0e6-123">Profile werden mithilfe der relevanten Informationen in MAPISVC erstellt. INF für die ausgewählten Dienstanbieter oder Nachrichtendienste.</span><span class="sxs-lookup"><span data-stu-id="cc0e6-123">Profiles are built using the relevant information in MAPISVC.INF for the selected service providers or message services.</span></span> <span data-ttu-id="cc0e6-124">Weitere Informationen zur Organisation und zu den Inhalten von MAPISVC. INF finden Sie unter [Datei Format von MapiSvc. inf](file-format-of-mapisvc-inf.md).</span><span class="sxs-lookup"><span data-stu-id="cc0e6-124">For more information about the organization and contents of MAPISVC.INF, see [File Format of MapiSvc.inf](file-format-of-mapisvc-inf.md).</span></span>
  
<span data-ttu-id="cc0e6-125">Der Name der DLL-Einstiegspunktfunktion Ihres Adressbuch Anbieters muss [ABProviderInit](abproviderinit.md) sein und dem **ABProviderInit** -Prototyp entsprechen.</span><span class="sxs-lookup"><span data-stu-id="cc0e6-125">The name of your address book provider's DLL entry point function must be [ABProviderInit](abproviderinit.md) and it must conform to the **ABProviderInit** prototype.</span></span> <span data-ttu-id="cc0e6-126">Führen Sie die folgenden Aufgaben in der DLL-Einstiegspunktfunktion Ihres Anbieters aus:</span><span class="sxs-lookup"><span data-stu-id="cc0e6-126">Perform the following tasks in your provider's DLL entry point function:</span></span> 
  
- <span data-ttu-id="cc0e6-127">Überprüfen Sie die Version der Dienstanbieterschnittstelle (SPI), um sicherzustellen, dass MAPI eine Version verwendet, die mit der Version kompatibel ist, die ihr Adressbuchanbieter verwendet.</span><span class="sxs-lookup"><span data-stu-id="cc0e6-127">Check the version of the service provider interface (SPI) to make sure MAPI is using a version that is compatible with the version that your address book provider is using.</span></span>
    
- <span data-ttu-id="cc0e6-128">Instanziieren eines Adressbuchanbieter Objekts.</span><span class="sxs-lookup"><span data-stu-id="cc0e6-128">Instantiate an address book provider object.</span></span>
    
<span data-ttu-id="cc0e6-129">Rufen Sie in dieser Funktion weder **MAPIInitialize** noch **MAPIUninitialize** auf.</span><span class="sxs-lookup"><span data-stu-id="cc0e6-129">Do not call either **MAPIInitialize** or **MAPIUninitialize** in this function.</span></span> 
  
<span data-ttu-id="cc0e6-130">Die DLL-Einstiegspunktfunktion instanziiert ein Provider-Objekt und gibt einen Zeiger auf dieses Objekt an MAPI zurück.</span><span class="sxs-lookup"><span data-stu-id="cc0e6-130">The DLL entry point function instantiates a provider object and returns to MAPI a pointer to that object.</span></span> 
  

