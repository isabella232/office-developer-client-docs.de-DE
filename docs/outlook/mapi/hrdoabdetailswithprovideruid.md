---
title: HrDoABDetailsWithProviderUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 27741887-8405-49ed-b080-613613faf91b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: cb4f38615ac6cacb3acbaa456f0992bf55c3653d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568623"
---
# <a name="hrdoabdetailswithprovideruid"></a><span data-ttu-id="65f5e-103">HrDoABDetailsWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="65f5e-103">HrDoABDetailsWithProviderUID</span></span>

  
  
<span data-ttu-id="65f5e-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="65f5e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="65f5e-105">Stellt sicher, dass die **OpenEntry** -Methode durch die erwartete Exchange-Adressbuchanbieter geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="65f5e-105">Ensures that the **OpenEntry** method is opened by the expected Exchange address book provider.</span></span> <span data-ttu-id="65f5e-106">Diese Funktion verhält sich [IAddrBook::Details](iaddrbook-details.md) jedoch **EntryID** mithilfe des Exchange-Adressbuchs _pEmsabpUID_identifizierten öffnet.</span><span class="sxs-lookup"><span data-stu-id="65f5e-106">This function works similarly to [IAddrBook::Details](iaddrbook-details.md) but opens **entryID** using the Exchange address book identified by  _pEmsabpUID_.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="65f5e-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="65f5e-107">Header file:</span></span>  <br/> |<span data-ttu-id="65f5e-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="65f5e-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="65f5e-109">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="65f5e-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="65f5e-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="65f5e-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="65f5e-111">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="65f5e-111">Called by:</span></span>  <br/> |<span data-ttu-id="65f5e-112">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="65f5e-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrDoABDetailsWithProviderUID(
  const MAPIUID   *pEmsabpUID,
  LPADRBOOK        pAddrBook,
  ULONG_PTR FAR *  lpulUIParam,
  LPFNDISMISS      lpfnDismiss,
  LPVOID           lpvDismissContext,
  ULONG            cbEntryID,
  LPENTRYID        lpEntryID,
  LPFNBUTTON       lpfButtonCallback,
  LPVOID           lpvButtonContext,
  LPSTR           lpszButtonText,
  ULONG            ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="65f5e-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="65f5e-113">Parameters</span></span>

 <span data-ttu-id="65f5e-114">_pEmsabpUID_</span><span class="sxs-lookup"><span data-stu-id="65f5e-114">_pEmsabpUID_</span></span>
  
> <span data-ttu-id="65f5e-115">[in] Ein Zeiger auf eine _EmsabpUID_ , die die Exchange-Adressbuchanbieter identifiziert sollten diese Funktion zum Anzeigen von Details auf die Eintrags-ID verwenden.</span><span class="sxs-lookup"><span data-stu-id="65f5e-115">[in] A pointer to an  _emsabpUID_ that identifies the Exchange address book provider this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="65f5e-116">Wenn eingehende Eintrags-ID nicht um ein Exchange Address Book Anbieter Eintrags-ID ist, dieser Parameter wird ignoriert, und die Funktion Anruf-verhält sich genau wie [IAddrBook::Details](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="65f5e-116">If the incoming entry identifier is not an Exchange address book provider entry identifier, this parameter is ignored and the function call acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="65f5e-117">Wenn dieser Parameter auf NULL oder eine MAPIUID NULL ist, verhält sich diese Funktion auch genau wie [IAddrBook::Details](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="65f5e-117">If this parameter is NULL or a zero MAPIUID, this function also acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="65f5e-118">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="65f5e-118">_pAddrBook_</span></span>
  
> <span data-ttu-id="65f5e-119">[in] Das Adressbuch verwendet, um die Eintrags-ID zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="65f5e-119">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="65f5e-120">Es darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="65f5e-120">It cannot be NULL.</span></span>
    
 <span data-ttu-id="65f5e-121">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="65f5e-121">_lpulUIParam_</span></span>
  
> <span data-ttu-id="65f5e-122">[out] Ein Handle für das übergeordnete Fenster für das Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="65f5e-122">[out] A handle to the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="65f5e-123">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="65f5e-123">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="65f5e-124">[in] Ein Zeiger auf eine Funktion, die basierend auf dem **DISMISSMODELESS** Prototyp oder NULL.</span><span class="sxs-lookup"><span data-stu-id="65f5e-124">[in] A pointer to a function based on the **DISMISSMODELESS** prototype, or NULL.</span></span> <span data-ttu-id="65f5e-125">Dieser Member gilt nur für die im Dialogfeld ohne Modus Version durch das DIALOG_SDI-Flag festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="65f5e-125">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="65f5e-126">MAPI-Aufrufen die **DISMISSMODELESS** -Funktion, wenn der Benutzer schließt das Dialogfeld ohne Modus Adresse informiert einen Client, der Details anruft, dass das Dialogfeld nicht mehr aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="65f5e-126">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling Details that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="65f5e-127">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="65f5e-127">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="65f5e-128">[in] Ein Zeiger auf Kontextinformationen zum Übergeben an die Funktion **DISMISSMODELESS** an, durch den Parameter _LpfnDismiss_ auf.</span><span class="sxs-lookup"><span data-stu-id="65f5e-128">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="65f5e-129">Dieser Parameter gilt nur für die im Dialogfeld ohne Modus Version durch das **DIALOG_SDI** -Flag in den Parameter _UlFlags_ einschließen.</span><span class="sxs-lookup"><span data-stu-id="65f5e-129">This parameter applies only to the modeless version of the dialog box by including the **DIALOG_SDI** flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="65f5e-130">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="65f5e-130">_cbEntryID_</span></span>
  
> <span data-ttu-id="65f5e-131">[in] Die Byteanzahl des Eintrags-ID, die durch den Parameter _LpEntryID_ angegeben.</span><span class="sxs-lookup"><span data-stu-id="65f5e-131">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="65f5e-132">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="65f5e-132">_lpEntryID_</span></span>
  
> <span data-ttu-id="65f5e-133">[in] Ein Zeiger auf die Eintrags-ID, die den Adresseintrag Adressbuch öffnen darstellt.</span><span class="sxs-lookup"><span data-stu-id="65f5e-133">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="65f5e-134">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="65f5e-134">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="65f5e-135">[in] Ein Zeiger auf eine Funktion, die basierend auf den **LPFNBUTTON** Funktionsprototyp.</span><span class="sxs-lookup"><span data-stu-id="65f5e-135">[in] A pointer to a function based on the **LPFNBUTTON** function prototype.</span></span> <span data-ttu-id="65f5e-136">Eine **LPFNBUTTON** -Funktion hinzugefügt im Dialogfeld Details der eine Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="65f5e-136">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="65f5e-137">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="65f5e-137">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="65f5e-138">[in] Ein Zeiger auf Daten, die als Parameter für die Funktion, die durch den _LpfButtonCallback_ -Parameter angegebenen verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="65f5e-138">[in] A pointer to data that was used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="65f5e-139">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="65f5e-139">_lpszButtonText_</span></span>
  
> <span data-ttu-id="65f5e-140">[in] Ein Zeiger auf eine Zeichenfolge mit Text auf die Schaltfläche hinzugefügt, angewendet werden soll, wenn diese Schaltfläche erweiterbar ist.</span><span class="sxs-lookup"><span data-stu-id="65f5e-140">[in] A pointer to a string that contains text to be applied to the added button, if that button is extensible.</span></span> <span data-ttu-id="65f5e-141">Der Parameter _LpszButtonText_ sollte NULL sein, wenn eine erweiterbare Schaltfläche nicht benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="65f5e-141">The  _lpszButtonText_ parameter should be NULL when an extensible button is not needed.</span></span> 
    
 <span data-ttu-id="65f5e-142">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="65f5e-142">_ulFlags_</span></span>
  
> <span data-ttu-id="65f5e-143">[in] Eine Bitmaske aus Flags, die den Typ des Texts für den Parameter _LpszButtonText_ steuert.</span><span class="sxs-lookup"><span data-stu-id="65f5e-143">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="65f5e-144">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="65f5e-144">The following flags can be set:</span></span> 
    
<span data-ttu-id="65f5e-145">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="65f5e-145">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="65f5e-146">Gibt an, dass Details gibt TRUE zurück, wenn die Adresse tatsächlich geändert werden. Details andernfalls FALSE.</span><span class="sxs-lookup"><span data-stu-id="65f5e-146">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="65f5e-147">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="65f5e-147">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="65f5e-148">Zeigt die modale Version im Dialogfeld allgemeine Adresse.</span><span class="sxs-lookup"><span data-stu-id="65f5e-148">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="65f5e-149">Dieses Kennzeichen ist mit DIALOG_SDI gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="65f5e-149">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="65f5e-150">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="65f5e-150">DIALOG_SDI</span></span>
  
> <span data-ttu-id="65f5e-151">Zeigt die allgemeine Adresse im Dialogfeld ohne Modus Version.</span><span class="sxs-lookup"><span data-stu-id="65f5e-151">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="65f5e-152">Dieses Kennzeichen ist mit DIALOG_MODAL gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="65f5e-152">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="65f5e-153">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="65f5e-153">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="65f5e-154">Die übergebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="65f5e-154">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="65f5e-155">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="65f5e-155">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    

