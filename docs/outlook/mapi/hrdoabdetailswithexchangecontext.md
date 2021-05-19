---
title: HrDoABDetailsWithExchangeContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b4e7fed2-88e4-4e14-90b6-913a1b7e338a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 353a663071a9f23f0d2330169d3ac7747e047c2b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421368"
---
# <a name="hrdoabdetailswithexchangecontext"></a><span data-ttu-id="dd3e4-103">HrDoABDetailsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="dd3e4-103">HrDoABDetailsWithExchangeContext</span></span>

  
  
<span data-ttu-id="dd3e4-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dd3e4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dd3e4-105">Stellt sicher, **dass die OpenEntry-Methode** vom erwarteten Adressbuchanbieter Exchange geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="dd3e4-105">Ensures that the **OpenEntry** method is opened by the expected Exchange address book provider.</span></span> <span data-ttu-id="dd3e4-106">Diese Funktion funktioniert ähnlich wie [IAddrBook::D etails](iaddrbook-details.md), öffnet jedoch die **entryID** mit dem Exchange, das durch den _pEmsmdbUID-Parameter_ identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="dd3e4-106">This function works similarly to [IAddrBook::Details](iaddrbook-details.md), but opens the **entryID** using the Exchange address book identified by the  _pEmsmdbUID_ parameter.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dd3e4-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="dd3e4-107">Header file:</span></span>  <br/> |<span data-ttu-id="dd3e4-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="dd3e4-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="dd3e4-109">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="dd3e4-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="dd3e4-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="dd3e4-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="dd3e4-111">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="dd3e4-111">Called by:</span></span>  <br/> |<span data-ttu-id="dd3e4-112">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="dd3e4-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithExchangeContext(
  LPMAPISESSION   pmsess,
  const MAPIUID  *pEmsmdbUID,
  LPADRBOOK pAddrBook,
  ULONG_PTR FAR * lpulUIParam,
  LPFNDISMISS lpfnDismiss,
  LPVOID lpvDismissContext,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPENTRYID lpEntryID,
  LPFNBUTTON lpfButtonCallback,
  LPVOID lpvButtonContext,
  LPSTR lpszButtonText,
  ULONG ulFlags,
);
```

## <a name="parameters"></a><span data-ttu-id="dd3e4-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="dd3e4-113">Parameters</span></span>

 <span data-ttu-id="dd3e4-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="dd3e4-114">_pmsess_</span></span>
  
> <span data-ttu-id="dd3e4-115">Die angemeldete **IMAPISession**.</span><span class="sxs-lookup"><span data-stu-id="dd3e4-115">The logged on **IMAPISession**.</span></span> <span data-ttu-id="dd3e4-116">Es kann nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="dd3e4-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="dd3e4-117">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="dd3e4-117">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="dd3e4-118">Ein Zeiger auf eine **emsmdbUID,** die den Exchange-Dienst identifiziert, der den Exchange-Adressbuchanbieter enthält, der von der Funktion zum Öffnen der Eintrags-ID verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dd3e4-118">A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange address book provider that is used by the function to open the entry identifier.</span></span> <span data-ttu-id="dd3e4-119">Wenn der Bezeichner für eingehende Exchange keine Adressbuchanbietereintrags-ID ist, wird dieser Parameter ignoriert, und die Funktion verhält sich wie [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="dd3e4-119">If the incoming entry identifier is not an Exchange address book provider entry identifier, this parameter is ignored and the function behaves like [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> <span data-ttu-id="dd3e4-120">Wenn dieser Parameter NULL oder null **MAPIUID** ist, funktioniert diese Funktion genauso wie [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="dd3e4-120">If this parameter is NULL or a zero **MAPIUID**, this function also acts exactly like [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> 
    
 <span data-ttu-id="dd3e4-121">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="dd3e4-121">_pAddrBook_</span></span>
  
> <span data-ttu-id="dd3e4-122">[in] Das Adressbuch, das zum Öffnen der Eintrags-ID verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dd3e4-122">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="dd3e4-123">Es kann nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="dd3e4-123">It cannot be NULL.</span></span>
    
 <span data-ttu-id="dd3e4-124">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="dd3e4-124">_lpulUIParam_</span></span>
  
> <span data-ttu-id="dd3e4-125">[out] Ein Handle zum übergeordneten Fenster für das Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="dd3e4-125">[out] A handle to the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="dd3e4-126">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="dd3e4-126">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="dd3e4-127">[in] Ein Zeiger auf eine Funktion basierend auf dem **DISMISSMODELESS-Prototyp** oder NULL.</span><span class="sxs-lookup"><span data-stu-id="dd3e4-127">[in] A pointer to a function based on the **DISMISSMODELESS** prototype, or NULL.</span></span> <span data-ttu-id="dd3e4-128">Dieses Element gilt nur für die moduslose Version des Dialogfelds, wie durch das festgelegte DIALOG_SDI angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="dd3e4-128">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="dd3e4-129">MAPI ruft die **FUNKTION DISMISSMODELESS** auf, wenn der Benutzer das Dialogfeld "Modeless Address" schließt und einen Client informiert, der Details aufruft, dass das Dialogfeld nicht mehr aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="dd3e4-129">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling Details that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="dd3e4-130">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="dd3e4-130">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="dd3e4-131">[in] Ein Zeiger auf Kontextinformationen, der an die **DISMISSMODELESS-Funktion übergeben** wird, auf die der  _lpfnDismiss-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="dd3e4-131">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="dd3e4-132">Dieser Parameter gilt nur für die moduslose Version  des Dialogfelds, indem das DIALOG_SDI im _ulFlags-Parameter verwendet_ wird.</span><span class="sxs-lookup"><span data-stu-id="dd3e4-132">This parameter applies only to the modeless version of the dialog box by including the **DIALOG_SDI** flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="dd3e4-133">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="dd3e4-133">_cbEntryID_</span></span>
  
> <span data-ttu-id="dd3e4-134">[in] Die Byteanzahl des Eintragsbezeichners, der durch den  _lpEntryID-Parameter angegeben_ wird.</span><span class="sxs-lookup"><span data-stu-id="dd3e4-134">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="dd3e4-135">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="dd3e4-135">_lpEntryID_</span></span>
  
> <span data-ttu-id="dd3e4-136">[in] Ein Zeiger auf den Eintragsbezeichner, der den zu öffnende Adressbucheintrag darstellt.</span><span class="sxs-lookup"><span data-stu-id="dd3e4-136">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="dd3e4-137">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="dd3e4-137">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="dd3e4-138">[in] Ein Zeiger auf eine Funktion basierend auf dem **LPFNBUTTON-Funktionsprototyp.**</span><span class="sxs-lookup"><span data-stu-id="dd3e4-138">[in] A pointer to a function based on the **LPFNBUTTON** function prototype.</span></span> <span data-ttu-id="dd3e4-139">Eine **LPFNBUTTON-Funktion** fügt dem Dialogfeld Details eine Schaltfläche hinzu.</span><span class="sxs-lookup"><span data-stu-id="dd3e4-139">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="dd3e4-140">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="dd3e4-140">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="dd3e4-141">[in] Ein Zeiger auf Daten, die als Parameter für die durch den  _lpfButtonCallback-Parameter_ angegebene Funktion verwendet wurden.</span><span class="sxs-lookup"><span data-stu-id="dd3e4-141">[in] A pointer to data that was used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="dd3e4-142">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="dd3e4-142">_lpszButtonText_</span></span>
  
> <span data-ttu-id="dd3e4-143">[in] Ein Zeiger auf eine Zeichenfolge, die Text enthält, der auf die hinzugefügte Schaltfläche angewendet werden soll, wenn diese Schaltfläche erweiterbar ist.</span><span class="sxs-lookup"><span data-stu-id="dd3e4-143">[in] A pointer to a string that contains text to be applied to the added button, if that button is extensible.</span></span> <span data-ttu-id="dd3e4-144">Der  _lpszButtonText-Parameter_ sollte NULL sein, wenn keine erweiterbare Schaltfläche erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="dd3e4-144">The  _lpszButtonText_ parameter should be NULL when an extensible button is not needed.</span></span> 
    
 <span data-ttu-id="dd3e4-145">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="dd3e4-145">_ulFlags_</span></span>
  
> <span data-ttu-id="dd3e4-146">[in] Eine Bitmaske mit Flags, die den Texttyp für den  _lpszButtonText-Parameter_ steuert.</span><span class="sxs-lookup"><span data-stu-id="dd3e4-146">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="dd3e4-147">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="dd3e4-147">The following flags can be set:</span></span> 
    
<span data-ttu-id="dd3e4-148">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="dd3e4-148">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="dd3e4-149">Gibt an, dass Details TRUE zurückgibt, wenn tatsächlich Änderungen an der Adresse vorgenommen werden. Andernfalls gibt Details FALSE zurück.</span><span class="sxs-lookup"><span data-stu-id="dd3e4-149">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="dd3e4-150">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="dd3e4-150">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="dd3e4-151">Zeigt die modale Version des Dialogfelds allgemeine Adresse an.</span><span class="sxs-lookup"><span data-stu-id="dd3e4-151">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="dd3e4-152">Dieses Flag schließen sich gegenseitig mit DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="dd3e4-152">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="dd3e4-153">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="dd3e4-153">DIALOG_SDI</span></span>
  
> <span data-ttu-id="dd3e4-154">Zeigt die moduslose Version des Dialogfelds allgemeine Adresse an.</span><span class="sxs-lookup"><span data-stu-id="dd3e4-154">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="dd3e4-155">Dieses Flag schließen sich gegenseitig mit DIALOG_MODAL.</span><span class="sxs-lookup"><span data-stu-id="dd3e4-155">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="dd3e4-156">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="dd3e4-156">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="dd3e4-157">Die übergebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="dd3e4-157">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="dd3e4-158">Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="dd3e4-158">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    

