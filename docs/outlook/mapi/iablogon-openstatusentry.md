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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e693e1c3d6cb975a3a329e15c0b1a6d08817461a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791970"
---
# <a name="iablogonopenstatusentry"></a><span data-ttu-id="56b20-103">IABLogon::OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="56b20-103">IABLogon::OpenStatusEntry</span></span>

  
  
<span data-ttu-id="56b20-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="56b20-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="56b20-105">Öffnet den Anbieter Status-Objekt.</span><span class="sxs-lookup"><span data-stu-id="56b20-105">Opens the provider's status object.</span></span>
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPMAPISTATUS FAR * lppEntry
);
```

## <a name="parameters"></a><span data-ttu-id="56b20-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="56b20-106">Parameters</span></span>

 <span data-ttu-id="56b20-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="56b20-107">_lpInterface_</span></span>
  
> <span data-ttu-id="56b20-108">[in] Ein Zeiger auf die Schnittstelle-ID (IID), die die Schnittstelle darstellt, die den Zugriff auf die Statusobjekt verwendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="56b20-108">[in] A pointer to the interface identifier (IID) that represents the interface that must be used to access the status object.</span></span> <span data-ttu-id="56b20-109">Übergeben NULL zurückgegeben Standardschnittstelle für das Objekt, [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="56b20-109">Passing NULL returns the object's standard interface, [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md).</span></span>
    
 <span data-ttu-id="56b20-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="56b20-110">_ulFlags_</span></span>
  
> <span data-ttu-id="56b20-111">[in] Eine Bitmaske aus Flags, die steuert, wie das Statusobjekt geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="56b20-111">[in] A bitmask of flags that controls how the status object is opened.</span></span> <span data-ttu-id="56b20-112">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="56b20-112">The following flag can be set:</span></span>
    
<span data-ttu-id="56b20-113">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="56b20-113">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="56b20-114">Anfragen Lese-/Schreibberechtigung.</span><span class="sxs-lookup"><span data-stu-id="56b20-114">Requests read/write permission.</span></span> <span data-ttu-id="56b20-115">Standardmäßig werden Objekte mit schreibgeschützten Zugriff geöffnet und Anrufer sollte nicht davon ausgehen, dass die Lese-Schreib-Berechtigung gewährt wurde.</span><span class="sxs-lookup"><span data-stu-id="56b20-115">By default, objects are opened with read-only access, and callers should not assume that read/write permission has been granted.</span></span>
    
 <span data-ttu-id="56b20-116">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="56b20-116">_lpulObjType_</span></span>
  
> <span data-ttu-id="56b20-117">[out] Ein Zeiger auf den Typ des Objekts geöffnet.</span><span class="sxs-lookup"><span data-stu-id="56b20-117">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="56b20-118">_lppEntry_</span><span class="sxs-lookup"><span data-stu-id="56b20-118">_lppEntry_</span></span>
  
> <span data-ttu-id="56b20-119">[out] Ein Zeiger auf einen Zeiger auf das geöffnete Objekt.</span><span class="sxs-lookup"><span data-stu-id="56b20-119">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="56b20-120">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="56b20-120">Return value</span></span>

<span data-ttu-id="56b20-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="56b20-121">S_OK</span></span> 
  
> <span data-ttu-id="56b20-122">Der Aufruf war erfolgreich, und das Statusobjekt geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="56b20-122">The call succeeded and the status object has been opened.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="56b20-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="56b20-123">Remarks</span></span>

<span data-ttu-id="56b20-124">Von adressbuchanbietern implementierte implementieren Sie die **OpenStatusEntry** -Methode zum Erteilen des Zugriffs auf ihre Statusobjekt.</span><span class="sxs-lookup"><span data-stu-id="56b20-124">Address book providers implement the **OpenStatusEntry** method to grant access to their status object.</span></span> <span data-ttu-id="56b20-125">Alle von adressbuchanbietern implementierte sind erforderlich, um einem Statusobjekt implementiert werden, die mindestens die [IMAPIStatus::ValidateState](imapistatus-validatestate.md) -Methode unterstützt.</span><span class="sxs-lookup"><span data-stu-id="56b20-125">All address book providers are required to implement a status object that supports, at a minimum, the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method.</span></span> <span data-ttu-id="56b20-126">Weitere Informationen finden Sie unter [Implementierung der Status-Objekts](status-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="56b20-126">For more information, see [Status Object Implementation](status-object-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="56b20-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="56b20-127">See also</span></span>



[<span data-ttu-id="56b20-128">IMAPIStatus: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="56b20-128">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)
  
[<span data-ttu-id="56b20-129">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="56b20-129">IMAPIStatus::SettingsDialog</span></span>](imapistatus-settingsdialog.md)
  
[<span data-ttu-id="56b20-130">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="56b20-130">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
  
[<span data-ttu-id="56b20-131">IABLogon: IUnknown</span><span class="sxs-lookup"><span data-stu-id="56b20-131">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

