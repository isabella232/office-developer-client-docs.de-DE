---
title: IMAPISupportOpenAddressBook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.OpenAddressBook
api_type:
- COM
ms.assetid: d8da8be1-3efe-410a-bcce-49e522602d80
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e9cd1c7ce0983a47311b2626cc3b40b47748b951
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792397"
---
# <a name="imapisupportopenaddressbook"></a><span data-ttu-id="56e57-103">IMAPISupport::OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="56e57-103">IMAPISupport::OpenAddressBook</span></span>

  
  
<span data-ttu-id="56e57-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="56e57-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="56e57-105">Bietet Zugriff auf das Adressbuch.</span><span class="sxs-lookup"><span data-stu-id="56e57-105">Provides access to the address book.</span></span>
  
```cpp
HRESULT OpenAddressBook(
LPCIID lpInterface,
ULONG ulFlags,
LPADRBOOK FAR * lppAdrBook
);
```

## <a name="parameters"></a><span data-ttu-id="56e57-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="56e57-106">Parameters</span></span>

 <span data-ttu-id="56e57-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="56e57-107">_lpInterface_</span></span>
  
> <span data-ttu-id="56e57-108">[in] Ein Zeiger auf die Schnittstelle-ID (IID), die die Schnittstelle für das Adressbuch zugreifen zu verwendende darstellt.</span><span class="sxs-lookup"><span data-stu-id="56e57-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the address book.</span></span> <span data-ttu-id="56e57-109">Gültige Werte sind NULL-Wert, womit die standard-Adresse Adressbuch-Schnittstelle [IAddrBook](iaddrbookimapiprop.md)und IID_IAddrBook.</span><span class="sxs-lookup"><span data-stu-id="56e57-109">Valid values are NULL, which indicates the standard address book interface [IAddrBook](iaddrbookimapiprop.md), and IID_IAddrBook.</span></span>
    
 <span data-ttu-id="56e57-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="56e57-110">_ulFlags_</span></span>
  
> <span data-ttu-id="56e57-111">Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="56e57-111">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="56e57-112">_lppAdrBook_</span><span class="sxs-lookup"><span data-stu-id="56e57-112">_lppAdrBook_</span></span>
  
> <span data-ttu-id="56e57-113">[out] Ein Zeiger auf einen Zeiger auf das Adressbuch.</span><span class="sxs-lookup"><span data-stu-id="56e57-113">[out] A pointer to a pointer to the address book.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="56e57-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="56e57-114">Return value</span></span>

<span data-ttu-id="56e57-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="56e57-115">S_OK</span></span> 
  
> <span data-ttu-id="56e57-116">Zugriff auf das Adressbuch wurde bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="56e57-116">Access to the address book was provided.</span></span>
    
<span data-ttu-id="56e57-117">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="56e57-117">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="56e57-118">Der Aufruf war erfolgreich, aber eine oder mehrere adressbuchanbietern implementierte konnte nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="56e57-118">The call succeeded, but one or more address book providers could not be loaded.</span></span> <span data-ttu-id="56e57-119">Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="56e57-119">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="56e57-120">Verwenden Sie das Makro **HR_FAILED** , um für diese Warnung zu testen.</span><span class="sxs-lookup"><span data-stu-id="56e57-120">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="56e57-121">Weitere Informationen finden Sie unter [Verwendung von Makros Fehlerbehandlung](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="56e57-121">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="56e57-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="56e57-122">Remarks</span></span>

<span data-ttu-id="56e57-123">Die **IMAPISupport::OpenAddressBook** -Methode wird für alle dienstanbieterobjekten Unterstützung implementiert.</span><span class="sxs-lookup"><span data-stu-id="56e57-123">The **IMAPISupport::OpenAddressBook** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="56e57-124">Dienstanbieter, die in der Regel eng gekoppelten Nachricht speichern und transport-Anbieter, rufen Sie **OpenAddressBook** , um auf das Adressbuch zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="56e57-124">Service providers, typically tightly coupled message store and transport providers, call **OpenAddressBook** to get access to the address book.</span></span> <span data-ttu-id="56e57-125">Der zurückgegebene **IAddrBook** Zeiger kann für eine Vielzahl von Address Book Aufgaben, einschließlich Adresse Adressbuch-Containern und Suchen von messaging-Benutzer und Anzeige von Adresse Dialogfelder Öffnen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="56e57-125">The returned **IAddrBook** pointer can be used for a variety of address book tasks, including opening address book containers, finding messaging users, and displaying address dialog boxes.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="56e57-126">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="56e57-126">Notes to callers</span></span>

 <span data-ttu-id="56e57-127">**OpenAddressBook** können MAPI_W_ERRORS_RETURNED zurückgeben, wenn mindestens eines der adressbuchanbietern implementierte im aktuellen Profil geladen werden kann.</span><span class="sxs-lookup"><span data-stu-id="56e57-127">**OpenAddressBook** can return MAPI_W_ERRORS_RETURNED if it cannot load one or more of the address book providers in the current profile.</span></span> <span data-ttu-id="56e57-128">Dieser Wert ist eine Warnung und sollten Sie den Anruf als erfolgreich behandeln.</span><span class="sxs-lookup"><span data-stu-id="56e57-128">This value is a warning and you should treat the call as successful.</span></span> <span data-ttu-id="56e57-129">Auch wenn alle Address Book Anbieter konnte nicht geladen werden, **OpenAddressBook** weiterhin erfolgreich ist, wird MAPI_W_ERRORS_RETURNED und einen **IAddrBook** Zeiger im Parameter _LppAdrBook_ zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="56e57-129">Even if all of the address book providers failed to load, **OpenAddressBook** still succeeds, returning MAPI_W_ERRORS_RETURNED and an **IAddrBook** pointer in the  _lppAdrBook_ parameter.</span></span> <span data-ttu-id="56e57-130">Da **OpenAddressBook** immer einen gültigen **IAddrBook** Zeiger zurückgibt, müssen Sie es Sie abschließend Verwendung freigeben.</span><span class="sxs-lookup"><span data-stu-id="56e57-130">Because **OpenAddressBook** always returns a valid **IAddrBook** pointer, you must release it when you are finished using it.</span></span> 
  
<span data-ttu-id="56e57-131">Wenn eine oder mehrere adressbuchanbietern implementierte konnte nicht geladen werden, rufen Sie [IMAPISupport::GetLastError](imapisupport-getlasterror.md) um eine [MAPIERROR](mapierror.md) -Struktur zu erhalten, die Informationen zu den Anbietern enthält, die nicht geladen wurden.</span><span class="sxs-lookup"><span data-stu-id="56e57-131">If one or more address book providers failed to load, call [IMAPISupport::GetLastError](imapisupport-getlasterror.md) to obtain a [MAPIERROR](mapierror.md) structure that contains information about the providers that did not load.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="56e57-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="56e57-132">See also</span></span>



[<span data-ttu-id="56e57-133">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="56e57-133">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="56e57-134">IMAPISession::OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="56e57-134">IMAPISession::OpenAddressBook</span></span>](imapisession-openaddressbook.md)
  
[<span data-ttu-id="56e57-135">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="56e57-135">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

