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
ms.openlocfilehash: 353a663071a9f23f0d2330169d3ac7747e047c2b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347852"
---
# <a name="hrdoabdetailswithexchangecontext"></a><span data-ttu-id="34743-103">HrDoABDetailsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="34743-103">HrDoABDetailsWithExchangeContext</span></span>

  
  
<span data-ttu-id="34743-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="34743-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="34743-105">Stellt sicher, \*\*\*\* dass die OpenEntry-Methode vom erwarteten Exchange-Adressbuchanbieter geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="34743-105">Ensures that the **OpenEntry** method is opened by the expected Exchange address book provider.</span></span> <span data-ttu-id="34743-106">Diese Funktion funktioniert ähnlich wie [IAddrBook::D ails](iaddrbook-details.md), öffnet aber die **Eintrags** -und das Exchange-Adressbuch, das durch den _pEmsmdbUID_ -Parameter identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="34743-106">This function works similarly to [IAddrBook::Details](iaddrbook-details.md), but opens the **entryID** using the Exchange address book identified by the  _pEmsmdbUID_ parameter.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="34743-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="34743-107">Header file:</span></span>  <br/> |<span data-ttu-id="34743-108">abhelp. h</span><span class="sxs-lookup"><span data-stu-id="34743-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="34743-109">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="34743-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="34743-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="34743-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="34743-111">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="34743-111">Called by:</span></span>  <br/> |<span data-ttu-id="34743-112">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="34743-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="34743-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="34743-113">Parameters</span></span>

 <span data-ttu-id="34743-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="34743-114">_pmsess_</span></span>
  
> <span data-ttu-id="34743-115">Der angemeldete **IMAPISession**.</span><span class="sxs-lookup"><span data-stu-id="34743-115">The logged on **IMAPISession**.</span></span> <span data-ttu-id="34743-116">Er darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="34743-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="34743-117">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="34743-117">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="34743-118">Ein Zeiger auf ein **emsmdbUID** , das den Exchange-Dienst identifiziert, der den Exchange-Adressbuchanbieter enthält, der von der Funktion zum Öffnen der Eintrags-ID verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="34743-118">A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange address book provider that is used by the function to open the entry identifier.</span></span> <span data-ttu-id="34743-119">Wenn die ID des eingehenden Eintrags kein Exchange-Adressbuchanbieter ist, wird dieser Parameter ignoriert, und die Funktion verhält sich wie [IAddrBook:: OpenEntry](iaddrbook-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="34743-119">If the incoming entry identifier is not an Exchange address book provider entry identifier, this parameter is ignored and the function behaves like [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> <span data-ttu-id="34743-120">Wenn dieser Parameter NULL oder eine NULL- **MAPIUID**ist, handelt es sich bei dieser Funktion auch genau wie [IAddrBook:: OpenEntry](iaddrbook-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="34743-120">If this parameter is NULL or a zero **MAPIUID**, this function also acts exactly like [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> 
    
 <span data-ttu-id="34743-121">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="34743-121">_pAddrBook_</span></span>
  
> <span data-ttu-id="34743-122">in Das zum Öffnen des Eintrags Bezeichners verwendete Adressbuch.</span><span class="sxs-lookup"><span data-stu-id="34743-122">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="34743-123">Er darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="34743-123">It cannot be NULL.</span></span>
    
 <span data-ttu-id="34743-124">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="34743-124">_lpulUIParam_</span></span>
  
> <span data-ttu-id="34743-125">Out Ein Handle für das übergeordnete Fenster für das Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="34743-125">[out] A handle to the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="34743-126">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="34743-126">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="34743-127">in Ein Zeiger auf eine Funktion, die auf dem **DISMISSMODELESS** -Prototyp basiert, oder NULL.</span><span class="sxs-lookup"><span data-stu-id="34743-127">[in] A pointer to a function based on the **DISMISSMODELESS** prototype, or NULL.</span></span> <span data-ttu-id="34743-128">Dieses Element gilt nur für die nicht modale Version des Dialogfelds, wie durch das festgelegte DIALOG_SDI-Flag angegeben.</span><span class="sxs-lookup"><span data-stu-id="34743-128">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="34743-129">MAPI Ruft die **DISMISSMODELESS** -Funktion auf, wenn der Benutzer das Dialogfeld nicht modale Adresse zurückweist und einen Client darüber informiert, dass das Dialogfeld nicht mehr aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="34743-129">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling Details that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="34743-130">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="34743-130">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="34743-131">in Ein Zeiger auf Kontextinformationen, die an die **DISMISSMODELESS** -Funktion übergeben werden, auf die durch den _lpfnDismiss_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="34743-131">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="34743-132">Dieser Parameter gilt nur für die nicht modale Version des Dialogfelds, indem das **DIALOG_SDI** -Flag im _ulFlags_ -Parameter eingeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="34743-132">This parameter applies only to the modeless version of the dialog box by including the **DIALOG_SDI** flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="34743-133">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="34743-133">_cbEntryID_</span></span>
  
> <span data-ttu-id="34743-134">in Die Bytezahl der vom _lpEntryID_ -Parameter angegebenen Eintrags-ID.</span><span class="sxs-lookup"><span data-stu-id="34743-134">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="34743-135">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="34743-135">_lpEntryID_</span></span>
  
> <span data-ttu-id="34743-136">in Ein Zeiger auf die Eintrags-ID, die den zu öffnenden Adressbucheintrag darstellt.</span><span class="sxs-lookup"><span data-stu-id="34743-136">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="34743-137">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="34743-137">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="34743-138">in Ein Zeiger auf eine Funktion, die auf dem Prototyp der **LPFNBUTTON** -Funktion basiert.</span><span class="sxs-lookup"><span data-stu-id="34743-138">[in] A pointer to a function based on the **LPFNBUTTON** function prototype.</span></span> <span data-ttu-id="34743-139">Mit einer **LPFNBUTTON** -Funktion wird dem Dialogfeld Details eine Schaltfläche hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="34743-139">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="34743-140">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="34743-140">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="34743-141">in Ein Zeiger auf Daten, die als Parameter für die durch den _lpfButtonCallback_ -Parameter angegebene Funktion verwendet wurden.</span><span class="sxs-lookup"><span data-stu-id="34743-141">[in] A pointer to data that was used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="34743-142">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="34743-142">_lpszButtonText_</span></span>
  
> <span data-ttu-id="34743-143">in Ein Zeiger auf eine Zeichenfolge, die den Text enthält, der auf die hinzugefügte Schaltfläche angewendet werden soll, wenn diese Schaltfläche erweiterbar ist.</span><span class="sxs-lookup"><span data-stu-id="34743-143">[in] A pointer to a string that contains text to be applied to the added button, if that button is extensible.</span></span> <span data-ttu-id="34743-144">Der Parameter _lpszButtonText_ sollte NULL sein, wenn eine erweiterbare Schaltfläche nicht erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="34743-144">The  _lpszButtonText_ parameter should be NULL when an extensible button is not needed.</span></span> 
    
 <span data-ttu-id="34743-145">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="34743-145">_ulFlags_</span></span>
  
> <span data-ttu-id="34743-146">in Eine Bitmaske von Flags, die den Texttyp für den _lpszButtonText_ -Parameter steuert.</span><span class="sxs-lookup"><span data-stu-id="34743-146">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="34743-147">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="34743-147">The following flags can be set:</span></span> 
    
<span data-ttu-id="34743-148">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="34743-148">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="34743-149">Gibt an, dass Details TRUE zurückgegeben werden, wenn tatsächlich Änderungen an der Adresse vorgenommen werden. Andernfalls gibt Details FALSE zurück.</span><span class="sxs-lookup"><span data-stu-id="34743-149">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="34743-150">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="34743-150">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="34743-151">Zeigt die modale Version des Dialogfelds allgemeine Adresse an.</span><span class="sxs-lookup"><span data-stu-id="34743-151">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="34743-152">Dieses Flag ist mit DIALOG_SDI gegenseitig ausschließen.</span><span class="sxs-lookup"><span data-stu-id="34743-152">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="34743-153">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="34743-153">DIALOG_SDI</span></span>
  
> <span data-ttu-id="34743-154">Zeigt die nicht modale Version des Dialogfelds allgemeine Adresse an.</span><span class="sxs-lookup"><span data-stu-id="34743-154">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="34743-155">Dieses Flag ist mit DIALOG_MODAL gegenseitig ausschließen.</span><span class="sxs-lookup"><span data-stu-id="34743-155">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="34743-156">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="34743-156">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="34743-157">Die übergebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="34743-157">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="34743-158">Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="34743-158">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    

