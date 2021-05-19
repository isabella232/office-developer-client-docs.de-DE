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
ms.openlocfilehash: 47a62b331ff9f1c96576d42797ebb23ed61cd362
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416881"
---
# <a name="imapisupportopenaddressbook"></a><span data-ttu-id="5c739-103">IMAPISupport::OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="5c739-103">IMAPISupport::OpenAddressBook</span></span>

  
  
<span data-ttu-id="5c739-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5c739-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5c739-105">Bietet Zugriff auf das Adressbuch.</span><span class="sxs-lookup"><span data-stu-id="5c739-105">Provides access to the address book.</span></span>
  
```cpp
HRESULT OpenAddressBook(
LPCIID lpInterface,
ULONG ulFlags,
LPADRBOOK FAR * lppAdrBook
);
```

## <a name="parameters"></a><span data-ttu-id="5c739-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c739-106">Parameters</span></span>

 <span data-ttu-id="5c739-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="5c739-107">_lpInterface_</span></span>
  
> <span data-ttu-id="5c739-108">[in] Ein Zeiger auf die Schnittstellen-ID (Interface Identifier, IID), die die Schnittstelle darstellt, die für den Zugriff auf das Adressbuch verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5c739-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the address book.</span></span> <span data-ttu-id="5c739-109">Gültige Werte sind NULL, was die Standardmäßige Adressbuchschnittstelle [IAddrBook](iaddrbookimapiprop.md)angibt, und IID_IAddrBook.</span><span class="sxs-lookup"><span data-stu-id="5c739-109">Valid values are NULL, which indicates the standard address book interface [IAddrBook](iaddrbookimapiprop.md), and IID_IAddrBook.</span></span>
    
 <span data-ttu-id="5c739-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5c739-110">_ulFlags_</span></span>
  
> <span data-ttu-id="5c739-111">Reserviert; muss null sein.</span><span class="sxs-lookup"><span data-stu-id="5c739-111">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="5c739-112">_lppAdrBook_</span><span class="sxs-lookup"><span data-stu-id="5c739-112">_lppAdrBook_</span></span>
  
> <span data-ttu-id="5c739-113">[out] Ein Zeiger auf einen Zeiger auf das Adressbuch.</span><span class="sxs-lookup"><span data-stu-id="5c739-113">[out] A pointer to a pointer to the address book.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5c739-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5c739-114">Return value</span></span>

<span data-ttu-id="5c739-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="5c739-115">S_OK</span></span> 
  
> <span data-ttu-id="5c739-116">Zugriff auf das Adressbuch wurde bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="5c739-116">Access to the address book was provided.</span></span>
    
<span data-ttu-id="5c739-117">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="5c739-117">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="5c739-118">Der Anruf war erfolgreich, aber mindestens ein Adressbuchanbieter konnte nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="5c739-118">The call succeeded, but one or more address book providers could not be loaded.</span></span> <span data-ttu-id="5c739-119">Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="5c739-119">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="5c739-120">Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** Makro.</span><span class="sxs-lookup"><span data-stu-id="5c739-120">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="5c739-121">Weitere Informationen finden Sie unter [Using Macros for Error Handling](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="5c739-121">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5c739-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5c739-122">Remarks</span></span>

<span data-ttu-id="5c739-123">Die **IMAPISupport::OpenAddressBook-Methode** wird für alle Dienstanbieterunterstützungsobjekte implementiert.</span><span class="sxs-lookup"><span data-stu-id="5c739-123">The **IMAPISupport::OpenAddressBook** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="5c739-124">Dienstanbieter, in der Regel eng gekoppelte Nachrichtenspeicher- und Transportanbieter, rufen **OpenAddressBook** auf, um Zugriff auf das Adressbuch zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5c739-124">Service providers, typically tightly coupled message store and transport providers, call **OpenAddressBook** to get access to the address book.</span></span> <span data-ttu-id="5c739-125">Der zurückgegebene **IAddrBook-Zeiger** kann für eine Vielzahl von Adressbuchaufgaben verwendet werden, z. B. das Öffnen von Adressbuchcontainern, das Suchen von Messagingbenutzern und das Anzeigen von Adressdialogfeldern.</span><span class="sxs-lookup"><span data-stu-id="5c739-125">The returned **IAddrBook** pointer can be used for a variety of address book tasks, including opening address book containers, finding messaging users, and displaying address dialog boxes.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="5c739-126">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="5c739-126">Notes to callers</span></span>

 <span data-ttu-id="5c739-127">**OpenAddressBook** kann MAPI_W_ERRORS_RETURNED zurückgeben, wenn es einen oder mehrere Adressbuchanbieter im aktuellen Profil nicht laden kann.</span><span class="sxs-lookup"><span data-stu-id="5c739-127">**OpenAddressBook** can return MAPI_W_ERRORS_RETURNED if it cannot load one or more of the address book providers in the current profile.</span></span> <span data-ttu-id="5c739-128">Dieser Wert ist eine Warnung, und Sie sollten den Anruf als erfolgreich behandeln.</span><span class="sxs-lookup"><span data-stu-id="5c739-128">This value is a warning and you should treat the call as successful.</span></span> <span data-ttu-id="5c739-129">Auch wenn alle Adressbuchanbieter nicht geladen werden konnten, ist **OpenAddressBook** weiterhin erfolgreich und gibt MAPI_W_ERRORS_RETURNED und einen **IAddrBook-Zeiger** im  _lppAdrBook-Parameter_ zurück.</span><span class="sxs-lookup"><span data-stu-id="5c739-129">Even if all of the address book providers failed to load, **OpenAddressBook** still succeeds, returning MAPI_W_ERRORS_RETURNED and an **IAddrBook** pointer in the  _lppAdrBook_ parameter.</span></span> <span data-ttu-id="5c739-130">Da **OpenAddressBook** immer einen gültigen **IAddrBook-Zeiger** zurückgibt, müssen Sie ihn los, sobald Sie mit der Verwendung fertig sind.</span><span class="sxs-lookup"><span data-stu-id="5c739-130">Because **OpenAddressBook** always returns a valid **IAddrBook** pointer, you must release it when you are finished using it.</span></span> 
  
<span data-ttu-id="5c739-131">Wenn ein oder mehrere Adressbuchanbieter nicht geladen werden konnten, rufen Sie [IMAPISupport::GetLastError](imapisupport-getlasterror.md) auf, um eine [MAPIERROR-Struktur](mapierror.md) zu erhalten, die Informationen zu den Anbietern enthält, die nicht geladen wurden.</span><span class="sxs-lookup"><span data-stu-id="5c739-131">If one or more address book providers failed to load, call [IMAPISupport::GetLastError](imapisupport-getlasterror.md) to obtain a [MAPIERROR](mapierror.md) structure that contains information about the providers that did not load.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5c739-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5c739-132">See also</span></span>



[<span data-ttu-id="5c739-133">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="5c739-133">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="5c739-134">IMAPISession::OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="5c739-134">IMAPISession::OpenAddressBook</span></span>](imapisession-openaddressbook.md)
  
[<span data-ttu-id="5c739-135">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="5c739-135">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

