---
title: Implementieren eine Adresse Adressbuch Anbieter Eintrag Point-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9375b351-1c84-4728-bcdf-e3e7a44820ed
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: b60a80bc0ede0c2800f6cfd98a98f498b93a1d8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792547"
---
# <a name="implementing-an-address-book-provider-entry-point-function"></a><span data-ttu-id="c5b06-103">Implementieren eine Adresse Adressbuch Anbieter Eintrag Point-Funktion</span><span class="sxs-lookup"><span data-stu-id="c5b06-103">Implementing an Address Book Provider Entry Point Function</span></span>

  
  
<span data-ttu-id="c5b06-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c5b06-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c5b06-105">Wenn ein Client Application aufruft [MAPILogonEx](mapilogonex.md) Beginn eine Sitzung mit einem Profil, das Ihre Adressbuchanbieter enthält, lädt MAPI Ihres Anbieters und alle anderen Personen, die Teil des Profils sind.</span><span class="sxs-lookup"><span data-stu-id="c5b06-105">When a client application calls [MAPILogonEx](mapilogonex.md) to begin a session using a profile that contains your address book provider, MAPI loads your provider and all others that are part of the profile.</span></span> <span data-ttu-id="c5b06-106">MAPI lernen im Profil anhand des Namens des Anbieters Entry Point-Funktion.</span><span class="sxs-lookup"><span data-stu-id="c5b06-106">MAPI learns of the name of your provider's entry point function by looking in the profile.</span></span> <span data-ttu-id="c5b06-107">Beachten Sie, dass diese Funktion nicht mit einer DLL-Einstiegspunktfunktion ist. finden Sie in der Dokumentation für **DllMain** in der Win32-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="c5b06-107">Remember that this function is not the same as a DLL entry point function; see the documentation for **DllMain** in the Win32 documentation.</span></span> 
  
<span data-ttu-id="c5b06-108">Es sind mehrere Einträge, von die einige in der Konfigurationsdatei mapisvc.inf vorhanden sein muss, die im Profilabschnitt von jedem Adressbuchanbieter enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="c5b06-108">There are several entries, some of which must appear in the mapisvc.inf configuration file, that are included in the profile section of every address book provider.</span></span> <span data-ttu-id="c5b06-109">Die folgende Tabelle enthält diese Profil Abschnitt Einträge und unabhängig davon, ob Sie die Datei "mapisvc.inf" umfassen werden muss.</span><span class="sxs-lookup"><span data-stu-id="c5b06-109">The following table lists these profile section entries and whether or not the mapisvc.inf file must include them.</span></span>
  
|<span data-ttu-id="c5b06-110">**Profil Abschnitt Eintrag**</span><span class="sxs-lookup"><span data-stu-id="c5b06-110">**Profile section entry**</span></span>|<span data-ttu-id="c5b06-111">**MAPISVC.inf-Anforderung**</span><span class="sxs-lookup"><span data-stu-id="c5b06-111">**mapisvc.inf requirement**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c5b06-112">PR_DISPLAY_NAME = _Zeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="c5b06-112">PR_DISPLAY_NAME= _string_</span></span> <br/> |<span data-ttu-id="c5b06-113">Optional</span><span class="sxs-lookup"><span data-stu-id="c5b06-113">Optional</span></span>  <br/> |
|<span data-ttu-id="c5b06-114">PR_PROVIDER_DISPLAY = _Zeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="c5b06-114">PR_PROVIDER_DISPLAY= _string_</span></span> <br/> |<span data-ttu-id="c5b06-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="c5b06-115">Required</span></span>  <br/> |
|<span data-ttu-id="c5b06-116">PR_PROVIDER_DLL_NAME = _DLL-Dateiname_</span><span class="sxs-lookup"><span data-stu-id="c5b06-116">PR_PROVIDER_DLL_NAME= _DLL filename_</span></span> <br/> |<span data-ttu-id="c5b06-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="c5b06-117">Required</span></span>  <br/> |
|<span data-ttu-id="c5b06-118">PR_RESOURCE_TYPE = _long_</span><span class="sxs-lookup"><span data-stu-id="c5b06-118">PR_RESOURCE_TYPE= _long_</span></span> <br/> |<span data-ttu-id="c5b06-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="c5b06-119">Required</span></span>  <br/> |
|<span data-ttu-id="c5b06-120">PR_RESOURCE_FLAGS = _Bitmaske_</span><span class="sxs-lookup"><span data-stu-id="c5b06-120">PR_RESOURCE_FLAGS= _bitmask_</span></span> <br/> |<span data-ttu-id="c5b06-121">Optional</span><span class="sxs-lookup"><span data-stu-id="c5b06-121">Optional</span></span>  <br/> |
   
<span data-ttu-id="c5b06-122">Ihre Adressbuchanbieter kann diese Informationen in einem Profil direkt durch Aufrufen der Benutzerprofildienst-Abschnitt [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode oder indirekt durch Ändern der MAPISVC.INF platzieren.</span><span class="sxs-lookup"><span data-stu-id="c5b06-122">Your address book provider can place this information into a profile directly by calling its profile section's [IMAPIProp::SetProps](imapiprop-setprops.md) method or indirectly by modifying MAPISVC.INF.</span></span> <span data-ttu-id="c5b06-123">Profile basieren, verwenden die entsprechende Informationen in MAPISVC. INF-Datei für den ausgewählten Dienstanbieter oder Message-Dienste.</span><span class="sxs-lookup"><span data-stu-id="c5b06-123">Profiles are built using the relevant information in MAPISVC.INF for the selected service providers or message services.</span></span> <span data-ttu-id="c5b06-124">Weitere Informationen über die Organisation und den Inhalt der Datei MAPISVC. INF-Datei, finden Sie unter [File Format der MapiSvc.inf](file-format-of-mapisvc-inf.md).</span><span class="sxs-lookup"><span data-stu-id="c5b06-124">For more information about the organization and contents of MAPISVC.INF, see [File Format of MapiSvc.inf](file-format-of-mapisvc-inf.md).</span></span>
  
<span data-ttu-id="c5b06-125">Der Name des Ihrer Adressbuchanbieter DLL-Einstiegspunktfunktion muss [ABProviderInit](abproviderinit.md) und muss mit dem **ABProviderInit** Prototyp entsprechen.</span><span class="sxs-lookup"><span data-stu-id="c5b06-125">The name of your address book provider's DLL entry point function must be [ABProviderInit](abproviderinit.md) and it must conform to the **ABProviderInit** prototype.</span></span> <span data-ttu-id="c5b06-126">Führen Sie die folgenden Aufgaben in Ihren Anbieter DLL-Einstiegspunktfunktion:</span><span class="sxs-lookup"><span data-stu-id="c5b06-126">Perform the following tasks in your provider's DLL entry point function:</span></span> 
  
- <span data-ttu-id="c5b06-127">Überprüfen Sie die Version der der Dienstanbieter-Schnittstelle (SPI), um sicherzustellen, dass MAPI eine Version verwendet, die mit der Version kompatibel ist, die Ihre Adressbuchanbieter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c5b06-127">Check the version of the service provider interface (SPI) to make sure MAPI is using a version that is compatible with the version that your address book provider is using.</span></span>
    
- <span data-ttu-id="c5b06-128">Instanziieren Sie ein Address Book Anbieter-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c5b06-128">Instantiate an address book provider object.</span></span>
    
<span data-ttu-id="c5b06-129">Rufen Sie **"MAPIInitialize"** oder **MAPIUninitialize** nicht in dieser Funktion.</span><span class="sxs-lookup"><span data-stu-id="c5b06-129">Do not call either **MAPIInitialize** or **MAPIUninitialize** in this function.</span></span> 
  
<span data-ttu-id="c5b06-130">Die DLL-Einstiegspunktfunktion instanziiert ein Anbieterobjekt und gibt einen Zeiger auf dieses Objekt MAPI zurück.</span><span class="sxs-lookup"><span data-stu-id="c5b06-130">The DLL entry point function instantiates a provider object and returns to MAPI a pointer to that object.</span></span> 
  

