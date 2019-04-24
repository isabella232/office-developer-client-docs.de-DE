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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329029"
---
# <a name="imapisupportopenaddressbook"></a><span data-ttu-id="5cc13-103">IMAPISupport::OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="5cc13-103">IMAPISupport::OpenAddressBook</span></span>

  
  
<span data-ttu-id="5cc13-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5cc13-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5cc13-105">Ermöglicht den Zugriff auf das Adressbuch.</span><span class="sxs-lookup"><span data-stu-id="5cc13-105">Provides access to the address book.</span></span>
  
```cpp
HRESULT OpenAddressBook(
LPCIID lpInterface,
ULONG ulFlags,
LPADRBOOK FAR * lppAdrBook
);
```

## <a name="parameters"></a><span data-ttu-id="5cc13-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5cc13-106">Parameters</span></span>

 <span data-ttu-id="5cc13-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="5cc13-107">_lpInterface_</span></span>
  
> <span data-ttu-id="5cc13-108">in Ein Zeiger auf die Schnittstellen-ID (IID), die die Schnittstelle darstellt, die für den Zugriff auf das Adressbuch verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5cc13-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the address book.</span></span> <span data-ttu-id="5cc13-109">Gültige Werte sind NULL, womit die standardmäßige Adressbuch Schnittstelle [IAddrBook](iaddrbookimapiprop.md)und IID_IAddrBook angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5cc13-109">Valid values are NULL, which indicates the standard address book interface [IAddrBook](iaddrbookimapiprop.md), and IID_IAddrBook.</span></span>
    
 <span data-ttu-id="5cc13-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5cc13-110">_ulFlags_</span></span>
  
> <span data-ttu-id="5cc13-111">Reserviert muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="5cc13-111">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="5cc13-112">_lppAdrBook_</span><span class="sxs-lookup"><span data-stu-id="5cc13-112">_lppAdrBook_</span></span>
  
> <span data-ttu-id="5cc13-113">Out Ein Zeiger auf einen Zeiger auf das Adressbuch.</span><span class="sxs-lookup"><span data-stu-id="5cc13-113">[out] A pointer to a pointer to the address book.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5cc13-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5cc13-114">Return value</span></span>

<span data-ttu-id="5cc13-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="5cc13-115">S_OK</span></span> 
  
> <span data-ttu-id="5cc13-116">Der Zugriff auf das Adressbuch wurde bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="5cc13-116">Access to the address book was provided.</span></span>
    
<span data-ttu-id="5cc13-117">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="5cc13-117">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="5cc13-118">Der Aufruf war erfolgreich, aber mindestens ein Adressbuchanbieter konnte nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="5cc13-118">The call succeeded, but one or more address book providers could not be loaded.</span></span> <span data-ttu-id="5cc13-119">Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="5cc13-119">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="5cc13-120">Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** -Makro.</span><span class="sxs-lookup"><span data-stu-id="5cc13-120">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="5cc13-121">Weitere Informationen finden Sie unter [Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="5cc13-121">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5cc13-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5cc13-122">Remarks</span></span>

<span data-ttu-id="5cc13-123">Die **IMAPISupport:: openaddressbook** -Methode wird für alle Support Objekte des Dienstanbieters implementiert.</span><span class="sxs-lookup"><span data-stu-id="5cc13-123">The **IMAPISupport::OpenAddressBook** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="5cc13-124">Dienstanbieter, in der Regel eng gekoppelte Nachrichtenspeicher-und Transport \*\*\*\* Anbieter, rufen openaddressbook auf, um Zugriff auf das Adressbuch zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5cc13-124">Service providers, typically tightly coupled message store and transport providers, call **OpenAddressBook** to get access to the address book.</span></span> <span data-ttu-id="5cc13-125">Der zurückgegebene **IAddrBook** -Zeiger kann für eine Vielzahl von Adressbuch Aufgaben verwendet werden, einschließlich Öffnen von Adressbuch Containern, suchen nach Messaging Benutzern und Anzeigen von Adress Dialogfeldern.</span><span class="sxs-lookup"><span data-stu-id="5cc13-125">The returned **IAddrBook** pointer can be used for a variety of address book tasks, including opening address book containers, finding messaging users, and displaying address dialog boxes.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="5cc13-126">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="5cc13-126">Notes to callers</span></span>

 <span data-ttu-id="5cc13-127">**Openaddressbook** kann MAPI_W_ERRORS_RETURNED zurückgeben, wenn es einen oder mehrere der Adressbuchanbieter im aktuellen Profil nicht laden kann.</span><span class="sxs-lookup"><span data-stu-id="5cc13-127">**OpenAddressBook** can return MAPI_W_ERRORS_RETURNED if it cannot load one or more of the address book providers in the current profile.</span></span> <span data-ttu-id="5cc13-128">Dieser Wert ist eine Warnung, und Sie sollten den Anruf als erfolgreich behandeln.</span><span class="sxs-lookup"><span data-stu-id="5cc13-128">This value is a warning and you should treat the call as successful.</span></span> <span data-ttu-id="5cc13-129">Auch wenn alle Adressbuchanbieter nicht geladen werden konnten, ist **openaddressbook** weiterhin erfolgreich und gibt MAPI_W_ERRORS_RETURNED und einen **IAddrBook** -Zeiger im _lppAdrBook_ -Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="5cc13-129">Even if all of the address book providers failed to load, **OpenAddressBook** still succeeds, returning MAPI_W_ERRORS_RETURNED and an **IAddrBook** pointer in the  _lppAdrBook_ parameter.</span></span> <span data-ttu-id="5cc13-130">Da **openaddressbook** immer einen gültigen **IAddrBook** -Zeiger zurückgibt, müssen Sie ihn freigeben, wenn Sie ihn nicht mehr verwenden.</span><span class="sxs-lookup"><span data-stu-id="5cc13-130">Because **OpenAddressBook** always returns a valid **IAddrBook** pointer, you must release it when you are finished using it.</span></span> 
  
<span data-ttu-id="5cc13-131">Wenn ein oder mehrere Adressbuchanbieter nicht geladen werden konnten, rufen Sie [IMAPISupport:: getlasterroraufzurufen](imapisupport-getlasterror.md) auf, um eine [MAPIERROR](mapierror.md) -Struktur abzurufen, die Informationen zu den Anbietern enthält, die nicht geladen wurden.</span><span class="sxs-lookup"><span data-stu-id="5cc13-131">If one or more address book providers failed to load, call [IMAPISupport::GetLastError](imapisupport-getlasterror.md) to obtain a [MAPIERROR](mapierror.md) structure that contains information about the providers that did not load.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5cc13-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5cc13-132">See also</span></span>



[<span data-ttu-id="5cc13-133">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="5cc13-133">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="5cc13-134">IMAPISession::OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="5cc13-134">IMAPISession::OpenAddressBook</span></span>](imapisession-openaddressbook.md)
  
[<span data-ttu-id="5cc13-135">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="5cc13-135">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

