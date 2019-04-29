---
title: IABLogonOpenStatusEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.OpenStatusEntry
api_type:
- COM
ms.assetid: 66f1e246-a67a-4f8a-ae3a-6a8ec8c2b367
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 22f98e52444b17c383737bffd1685df0fb7ba8bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410784"
---
# <a name="iablogonopenstatusentry"></a><span data-ttu-id="f21f4-103">IABLogon::OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="f21f4-103">IABLogon::OpenStatusEntry</span></span>

  
  
<span data-ttu-id="f21f4-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f21f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f21f4-105">Öffnet das Status-Objekt des Anbieters.</span><span class="sxs-lookup"><span data-stu-id="f21f4-105">Opens the provider's status object.</span></span>
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPMAPISTATUS FAR * lppEntry
);
```

## <a name="parameters"></a><span data-ttu-id="f21f4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f21f4-106">Parameters</span></span>

 <span data-ttu-id="f21f4-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="f21f4-107">_lpInterface_</span></span>
  
> <span data-ttu-id="f21f4-108">in Ein Zeiger auf die Schnittstellen-ID (IID), die die Schnittstelle darstellt, die für den Zugriff auf das Status-Objekt verwendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="f21f4-108">[in] A pointer to the interface identifier (IID) that represents the interface that must be used to access the status object.</span></span> <span data-ttu-id="f21f4-109">Durch das Übergeben von NULL wird die Standardschnittstelle des Objekts [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f21f4-109">Passing NULL returns the object's standard interface, [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md).</span></span>
    
 <span data-ttu-id="f21f4-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f21f4-110">_ulFlags_</span></span>
  
> <span data-ttu-id="f21f4-111">in Eine Bitmaske von Flags, die steuert, wie das Statusobjekt geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="f21f4-111">[in] A bitmask of flags that controls how the status object is opened.</span></span> <span data-ttu-id="f21f4-112">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="f21f4-112">The following flag can be set:</span></span>
    
<span data-ttu-id="f21f4-113">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="f21f4-113">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="f21f4-114">Fordert Lese-/Schreibzugriff-Berechtigung an.</span><span class="sxs-lookup"><span data-stu-id="f21f4-114">Requests read/write permission.</span></span> <span data-ttu-id="f21f4-115">Standardmäßig werden Objekte mit Schreibschutz geöffnet, und Aufrufer sollten nicht davon ausgehen, dass Lese-/Schreibzugriff erteilt wurde.</span><span class="sxs-lookup"><span data-stu-id="f21f4-115">By default, objects are opened with read-only access, and callers should not assume that read/write permission has been granted.</span></span>
    
 <span data-ttu-id="f21f4-116">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="f21f4-116">_lpulObjType_</span></span>
  
> <span data-ttu-id="f21f4-117">Out Ein Zeiger auf den Typ des geöffneten Objekts.</span><span class="sxs-lookup"><span data-stu-id="f21f4-117">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="f21f4-118">_lppEntry_</span><span class="sxs-lookup"><span data-stu-id="f21f4-118">_lppEntry_</span></span>
  
> <span data-ttu-id="f21f4-119">Out Ein Zeiger auf einen Zeiger auf das geöffnete Objekt.</span><span class="sxs-lookup"><span data-stu-id="f21f4-119">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f21f4-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f21f4-120">Return value</span></span>

<span data-ttu-id="f21f4-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="f21f4-121">S_OK</span></span> 
  
> <span data-ttu-id="f21f4-122">Der Aufruf war erfolgreich, und das Status-Objekt wurde geöffnet.</span><span class="sxs-lookup"><span data-stu-id="f21f4-122">The call succeeded and the status object has been opened.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f21f4-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f21f4-123">Remarks</span></span>

<span data-ttu-id="f21f4-124">Adressbuchanbieter implementieren die **OpenStatusEntry** -Methode, um Zugriff auf Ihr Status-Objekt zu gewähren.</span><span class="sxs-lookup"><span data-stu-id="f21f4-124">Address book providers implement the **OpenStatusEntry** method to grant access to their status object.</span></span> <span data-ttu-id="f21f4-125">Alle Adressbuchanbieter müssen ein Status-Objekt implementieren, das mindestens die [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) -Methode unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f21f4-125">All address book providers are required to implement a status object that supports, at a minimum, the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method.</span></span> <span data-ttu-id="f21f4-126">Weitere Informationen finden Sie unter [Implementierung von Status Objekten](status-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="f21f4-126">For more information, see [Status Object Implementation](status-object-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f21f4-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f21f4-127">See also</span></span>



[<span data-ttu-id="f21f4-128">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="f21f4-128">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)
  
[<span data-ttu-id="f21f4-129">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="f21f4-129">IMAPIStatus::SettingsDialog</span></span>](imapistatus-settingsdialog.md)
  
[<span data-ttu-id="f21f4-130">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="f21f4-130">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
  
[<span data-ttu-id="f21f4-131">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f21f4-131">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

