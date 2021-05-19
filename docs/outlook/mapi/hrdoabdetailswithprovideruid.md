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
ms.openlocfilehash: 47cf87fce0af3b866018bf03a34a05ea42cef82c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426681"
---
# <a name="hrdoabdetailswithprovideruid"></a><span data-ttu-id="9e91e-103">HrDoABDetailsWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="9e91e-103">HrDoABDetailsWithProviderUID</span></span>

  
  
<span data-ttu-id="9e91e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9e91e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9e91e-105">Stellt sicher, **dass die OpenEntry-Methode** vom erwarteten Adressbuchanbieter Exchange geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="9e91e-105">Ensures that the **OpenEntry** method is opened by the expected Exchange address book provider.</span></span> <span data-ttu-id="9e91e-106">Diese Funktion funktioniert ähnlich wie [IAddrBook::D etails,](iaddrbook-details.md) öffnet **jedoch entryID** mit dem Exchange, das von _pEmsabpUID_ identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="9e91e-106">This function works similarly to [IAddrBook::Details](iaddrbook-details.md) but opens **entryID** using the Exchange address book identified by  _pEmsabpUID_.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9e91e-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="9e91e-107">Header file:</span></span>  <br/> |<span data-ttu-id="9e91e-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="9e91e-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="9e91e-109">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="9e91e-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="9e91e-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="9e91e-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="9e91e-111">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="9e91e-111">Called by:</span></span>  <br/> |<span data-ttu-id="9e91e-112">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="9e91e-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="9e91e-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e91e-113">Parameters</span></span>

 <span data-ttu-id="9e91e-114">_pEmsabpUID_</span><span class="sxs-lookup"><span data-stu-id="9e91e-114">_pEmsabpUID_</span></span>
  
> <span data-ttu-id="9e91e-115">[in] Ein Zeiger auf eine _emsabpUID,_ die den Exchange identifiziert, den diese Funktion verwenden sollte, um Details zur Eintrags-ID anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9e91e-115">[in] A pointer to an  _emsabpUID_ that identifies the Exchange address book provider this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="9e91e-116">Wenn der Bezeichner für eingehende Eingaben kein eintragsbezeichner Exchange Adressbuchanbieter ist, wird dieser Parameter ignoriert, und der Funktionsaufruf verhält sich genau wie [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="9e91e-116">If the incoming entry identifier is not an Exchange address book provider entry identifier, this parameter is ignored and the function call acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="9e91e-117">Wenn dieser Parameter NULL oder null MAPIUID ist, funktioniert diese Funktion auch genau wie [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="9e91e-117">If this parameter is NULL or a zero MAPIUID, this function also acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="9e91e-118">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="9e91e-118">_pAddrBook_</span></span>
  
> <span data-ttu-id="9e91e-119">[in] Das Adressbuch, das zum Öffnen der Eintrags-ID verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9e91e-119">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="9e91e-120">Es kann nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="9e91e-120">It cannot be NULL.</span></span>
    
 <span data-ttu-id="9e91e-121">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="9e91e-121">_lpulUIParam_</span></span>
  
> <span data-ttu-id="9e91e-122">[out] Ein Handle zum übergeordneten Fenster für das Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="9e91e-122">[out] A handle to the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="9e91e-123">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="9e91e-123">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="9e91e-124">[in] Ein Zeiger auf eine Funktion basierend auf dem **DISMISSMODELESS-Prototyp** oder NULL.</span><span class="sxs-lookup"><span data-stu-id="9e91e-124">[in] A pointer to a function based on the **DISMISSMODELESS** prototype, or NULL.</span></span> <span data-ttu-id="9e91e-125">Dieses Element gilt nur für die moduslose Version des Dialogfelds, wie durch das festgelegte DIALOG_SDI angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9e91e-125">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="9e91e-126">MAPI ruft die **FUNKTION DISMISSMODELESS** auf, wenn der Benutzer das Dialogfeld "Modeless Address" schließt und einen Client informiert, der Details aufruft, dass das Dialogfeld nicht mehr aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="9e91e-126">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling Details that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="9e91e-127">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="9e91e-127">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="9e91e-128">[in] Ein Zeiger auf Kontextinformationen, der an die **DISMISSMODELESS-Funktion übergeben** wird, auf die der  _lpfnDismiss-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="9e91e-128">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="9e91e-129">Dieser Parameter gilt nur für die moduslose Version  des Dialogfelds, indem das DIALOG_SDI im _ulFlags-Parameter verwendet_ wird.</span><span class="sxs-lookup"><span data-stu-id="9e91e-129">This parameter applies only to the modeless version of the dialog box by including the **DIALOG_SDI** flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="9e91e-130">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="9e91e-130">_cbEntryID_</span></span>
  
> <span data-ttu-id="9e91e-131">[in] Die Byteanzahl des Eintragsbezeichners, der durch den  _lpEntryID-Parameter angegeben_ wird.</span><span class="sxs-lookup"><span data-stu-id="9e91e-131">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="9e91e-132">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="9e91e-132">_lpEntryID_</span></span>
  
> <span data-ttu-id="9e91e-133">[in] Ein Zeiger auf den Eintragsbezeichner, der den zu öffnende Adressbucheintrag darstellt.</span><span class="sxs-lookup"><span data-stu-id="9e91e-133">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="9e91e-134">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="9e91e-134">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="9e91e-135">[in] Ein Zeiger auf eine Funktion basierend auf dem **LPFNBUTTON-Funktionsprototyp.**</span><span class="sxs-lookup"><span data-stu-id="9e91e-135">[in] A pointer to a function based on the **LPFNBUTTON** function prototype.</span></span> <span data-ttu-id="9e91e-136">Eine **LPFNBUTTON-Funktion** fügt dem Dialogfeld Details eine Schaltfläche hinzu.</span><span class="sxs-lookup"><span data-stu-id="9e91e-136">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="9e91e-137">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="9e91e-137">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="9e91e-138">[in] Ein Zeiger auf Daten, die als Parameter für die durch den  _lpfButtonCallback-Parameter_ angegebene Funktion verwendet wurden.</span><span class="sxs-lookup"><span data-stu-id="9e91e-138">[in] A pointer to data that was used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="9e91e-139">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="9e91e-139">_lpszButtonText_</span></span>
  
> <span data-ttu-id="9e91e-140">[in] Ein Zeiger auf eine Zeichenfolge, die Text enthält, der auf die hinzugefügte Schaltfläche angewendet werden soll, wenn diese Schaltfläche erweiterbar ist.</span><span class="sxs-lookup"><span data-stu-id="9e91e-140">[in] A pointer to a string that contains text to be applied to the added button, if that button is extensible.</span></span> <span data-ttu-id="9e91e-141">Der  _lpszButtonText-Parameter_ sollte NULL sein, wenn keine erweiterbare Schaltfläche erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="9e91e-141">The  _lpszButtonText_ parameter should be NULL when an extensible button is not needed.</span></span> 
    
 <span data-ttu-id="9e91e-142">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9e91e-142">_ulFlags_</span></span>
  
> <span data-ttu-id="9e91e-143">[in] Eine Bitmaske mit Flags, die den Texttyp für den  _lpszButtonText-Parameter_ steuert.</span><span class="sxs-lookup"><span data-stu-id="9e91e-143">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="9e91e-144">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="9e91e-144">The following flags can be set:</span></span> 
    
<span data-ttu-id="9e91e-145">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="9e91e-145">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="9e91e-146">Gibt an, dass Details TRUE zurückgibt, wenn tatsächlich Änderungen an der Adresse vorgenommen werden. Andernfalls gibt Details FALSE zurück.</span><span class="sxs-lookup"><span data-stu-id="9e91e-146">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="9e91e-147">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="9e91e-147">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="9e91e-148">Zeigt die modale Version des Dialogfelds allgemeine Adresse an.</span><span class="sxs-lookup"><span data-stu-id="9e91e-148">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="9e91e-149">Dieses Flag schließen sich gegenseitig mit DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="9e91e-149">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="9e91e-150">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="9e91e-150">DIALOG_SDI</span></span>
  
> <span data-ttu-id="9e91e-151">Zeigt die moduslose Version des Dialogfelds allgemeine Adresse an.</span><span class="sxs-lookup"><span data-stu-id="9e91e-151">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="9e91e-152">Dieses Flag schließen sich gegenseitig mit DIALOG_MODAL.</span><span class="sxs-lookup"><span data-stu-id="9e91e-152">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="9e91e-153">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9e91e-153">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="9e91e-154">Die übergebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="9e91e-154">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="9e91e-155">Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="9e91e-155">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    

