---
title: HrDoABDetailsWithExchangeContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b4e7fed2-88e4-4e14-90b6-913a1b7e338a
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: cb6138072cd5dedc528168d4056041661c40fd06
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791921"
---
# <a name="hrdoabdetailswithexchangecontext"></a><span data-ttu-id="d6eb4-103">HrDoABDetailsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="d6eb4-103">HrDoABDetailsWithExchangeContext</span></span>

  
  
<span data-ttu-id="d6eb4-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d6eb4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d6eb4-105">Stellt sicher, dass die **OpenEntry** -Methode durch die erwartete Exchange-Adressbuchanbieter geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="d6eb4-105">Ensures that the **OpenEntry** method is opened by the expected Exchange address book provider.</span></span> <span data-ttu-id="d6eb4-106">Diese Funktion verhält sich [IAddrBook::Details](iaddrbook-details.md), jedoch wird die **Eintrags-ID** mithilfe des Exchange-Adressbuchs vom Parameter _pEmsmdbUID_ geöffnet.</span><span class="sxs-lookup"><span data-stu-id="d6eb4-106">This function works similarly to [IAddrBook::Details](iaddrbook-details.md), but opens the **entryID** using the Exchange address book identified by the  _pEmsmdbUID_ parameter.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d6eb4-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="d6eb4-107">Header file:</span></span>  <br/> |<span data-ttu-id="d6eb4-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="d6eb4-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="d6eb4-109">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="d6eb4-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="d6eb4-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="d6eb4-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="d6eb4-111">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="d6eb4-111">Called by:</span></span>  <br/> |<span data-ttu-id="d6eb4-112">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="d6eb4-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="d6eb4-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6eb4-113">Parameters</span></span>

 <span data-ttu-id="d6eb4-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="d6eb4-114">_pmsess_</span></span>
  
> <span data-ttu-id="d6eb4-115">Die angemeldete **IMAPISession**.</span><span class="sxs-lookup"><span data-stu-id="d6eb4-115">The logged on **IMAPISession**.</span></span> <span data-ttu-id="d6eb4-116">Es darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="d6eb4-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="d6eb4-117">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="d6eb4-117">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="d6eb4-118">Ein Zeiger auf eine **EmsmdbUID** , die den Exchange-Dienst, die die Exchange-Adressbuchanbieter, die von der Funktion verwendet wird identifiziert enthält, um die Eintrags-ID zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d6eb4-118">A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange address book provider that is used by the function to open the entry identifier.</span></span> <span data-ttu-id="d6eb4-119">Wenn eingehende Eintrags-ID kein Exchange Address Book Anbieter Eintrags-ID ist, wird dieser Parameter wird ignoriert, und die Funktion verhält sich wie [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="d6eb4-119">If the incoming entry identifier is not an Exchange address book provider entry identifier, this parameter is ignored and the function behaves like [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> <span data-ttu-id="d6eb4-120">Wenn dieser Parameter auf NULL oder NULL **MAPIUID**ist, verhält sich diese Funktion auch genau wie [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="d6eb4-120">If this parameter is NULL or a zero **MAPIUID**, this function also acts exactly like [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> 
    
 <span data-ttu-id="d6eb4-121">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="d6eb4-121">_pAddrBook_</span></span>
  
> <span data-ttu-id="d6eb4-122">[in] Das Adressbuch verwendet, um die Eintrags-ID zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d6eb4-122">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="d6eb4-123">Es darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="d6eb4-123">It cannot be NULL.</span></span>
    
 <span data-ttu-id="d6eb4-124">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="d6eb4-124">_lpulUIParam_</span></span>
  
> <span data-ttu-id="d6eb4-125">[out] Ein Handle für das übergeordnete Fenster für das Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="d6eb4-125">[out] A handle to the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="d6eb4-126">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="d6eb4-126">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="d6eb4-127">[in] Ein Zeiger auf eine Funktion, die basierend auf dem **DISMISSMODELESS** Prototyp oder NULL.</span><span class="sxs-lookup"><span data-stu-id="d6eb4-127">[in] A pointer to a function based on the **DISMISSMODELESS** prototype, or NULL.</span></span> <span data-ttu-id="d6eb4-128">Dieser Member gilt nur für die im Dialogfeld ohne Modus Version durch das DIALOG_SDI-Flag festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="d6eb4-128">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="d6eb4-129">MAPI-Aufrufen die **DISMISSMODELESS** -Funktion, wenn der Benutzer schließt das Dialogfeld ohne Modus Adresse informiert einen Client, der Details anruft, dass das Dialogfeld nicht mehr aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="d6eb4-129">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling Details that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="d6eb4-130">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="d6eb4-130">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="d6eb4-131">[in] Ein Zeiger auf Kontextinformationen zum Übergeben an die Funktion **DISMISSMODELESS** an, durch den Parameter _LpfnDismiss_ auf.</span><span class="sxs-lookup"><span data-stu-id="d6eb4-131">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="d6eb4-132">Dieser Parameter gilt nur für die im Dialogfeld ohne Modus Version durch das **DIALOG_SDI** -Flag in den Parameter _UlFlags_ einschließen.</span><span class="sxs-lookup"><span data-stu-id="d6eb4-132">This parameter applies only to the modeless version of the dialog box by including the **DIALOG_SDI** flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="d6eb4-133">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="d6eb4-133">_cbEntryID_</span></span>
  
> <span data-ttu-id="d6eb4-134">[in] Die Byteanzahl des Eintrags-ID, die durch den Parameter _LpEntryID_ angegeben.</span><span class="sxs-lookup"><span data-stu-id="d6eb4-134">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="d6eb4-135">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="d6eb4-135">_lpEntryID_</span></span>
  
> <span data-ttu-id="d6eb4-136">[in] Ein Zeiger auf die Eintrags-ID, die den Adresseintrag Adressbuch öffnen darstellt.</span><span class="sxs-lookup"><span data-stu-id="d6eb4-136">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="d6eb4-137">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="d6eb4-137">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="d6eb4-138">[in] Ein Zeiger auf eine Funktion, die basierend auf den **LPFNBUTTON** Funktionsprototyp.</span><span class="sxs-lookup"><span data-stu-id="d6eb4-138">[in] A pointer to a function based on the **LPFNBUTTON** function prototype.</span></span> <span data-ttu-id="d6eb4-139">Eine **LPFNBUTTON** -Funktion hinzugefügt im Dialogfeld Details der eine Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="d6eb4-139">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="d6eb4-140">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="d6eb4-140">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="d6eb4-141">[in] Ein Zeiger auf Daten, die als Parameter für die Funktion, die durch den _LpfButtonCallback_ -Parameter angegebenen verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="d6eb4-141">[in] A pointer to data that was used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="d6eb4-142">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="d6eb4-142">_lpszButtonText_</span></span>
  
> <span data-ttu-id="d6eb4-143">[in] Ein Zeiger auf eine Zeichenfolge mit Text auf die Schaltfläche hinzugefügt, angewendet werden soll, wenn diese Schaltfläche erweiterbar ist.</span><span class="sxs-lookup"><span data-stu-id="d6eb4-143">[in] A pointer to a string that contains text to be applied to the added button, if that button is extensible.</span></span> <span data-ttu-id="d6eb4-144">Der Parameter _LpszButtonText_ sollte NULL sein, wenn eine erweiterbare Schaltfläche nicht benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="d6eb4-144">The  _lpszButtonText_ parameter should be NULL when an extensible button is not needed.</span></span> 
    
 <span data-ttu-id="d6eb4-145">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d6eb4-145">_ulFlags_</span></span>
  
> <span data-ttu-id="d6eb4-146">[in] Eine Bitmaske aus Flags, die den Typ des Texts für den Parameter _LpszButtonText_ steuert.</span><span class="sxs-lookup"><span data-stu-id="d6eb4-146">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="d6eb4-147">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="d6eb4-147">The following flags can be set:</span></span> 
    
<span data-ttu-id="d6eb4-148">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="d6eb4-148">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="d6eb4-149">Gibt an, dass Details gibt TRUE zurück, wenn die Adresse tatsächlich geändert werden. Details andernfalls FALSE.</span><span class="sxs-lookup"><span data-stu-id="d6eb4-149">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="d6eb4-150">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="d6eb4-150">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="d6eb4-151">Zeigt die modale Version im Dialogfeld allgemeine Adresse.</span><span class="sxs-lookup"><span data-stu-id="d6eb4-151">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="d6eb4-152">Dieses Kennzeichen ist mit DIALOG_SDI gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="d6eb4-152">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="d6eb4-153">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="d6eb4-153">DIALOG_SDI</span></span>
  
> <span data-ttu-id="d6eb4-154">Zeigt die allgemeine Adresse im Dialogfeld ohne Modus Version.</span><span class="sxs-lookup"><span data-stu-id="d6eb4-154">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="d6eb4-155">Dieses Kennzeichen ist mit DIALOG_MODAL gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="d6eb4-155">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="d6eb4-156">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d6eb4-156">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="d6eb4-157">Die übergebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="d6eb4-157">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="d6eb4-158">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="d6eb4-158">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    

