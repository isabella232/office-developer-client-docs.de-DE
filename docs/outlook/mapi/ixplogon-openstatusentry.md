---
title: IXPLogonOpenStatusEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.OpenStatusEntry
api_type:
- COM
ms.assetid: 261d5f7c-bb61-4e1d-aa41-cca224c63f8e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d9e09de1064a0ae034bb3618f0e5b3719a82c163
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435901"
---
# <a name="ixplogonopenstatusentry"></a><span data-ttu-id="78609-103">IXPLogon::OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="78609-103">IXPLogon::OpenStatusEntry</span></span>

  
  
<span data-ttu-id="78609-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="78609-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="78609-105">Öffnet das Status-Objekt des Transportanbieters.</span><span class="sxs-lookup"><span data-stu-id="78609-105">Opens the transport provider's status object.</span></span>
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPMAPISTATUS FAR * lppEntry
);
```

## <a name="parameters"></a><span data-ttu-id="78609-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="78609-106">Parameters</span></span>

 <span data-ttu-id="78609-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="78609-107">_lpInterface_</span></span>
  
> <span data-ttu-id="78609-108">in Ein Zeiger auf einen Schnittstellenbezeichner (IID) für das Transport Anmeldeobjekt.</span><span class="sxs-lookup"><span data-stu-id="78609-108">[in] A pointer to an interface identifier (IID) for the transport logon object.</span></span> <span data-ttu-id="78609-109">Durch das Übergeben von NULL wird die [IMAPIStatus](imapistatusimapiprop.md) -Schnittstelle zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="78609-109">Passing NULL returns the [IMAPIStatus](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="78609-110">Der _lpInterface_ -Parameter kann auch auf einen Bezeichner für eine Schnittstelle für das Objekt festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="78609-110">The  _lpInterface_ parameter can also be set to an identifier for an interface for the object.</span></span> 
    
 <span data-ttu-id="78609-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="78609-111">_ulFlags_</span></span>
  
> <span data-ttu-id="78609-112">in Eine Bitmaske von Flags, die steuert, wie das Statusobjekt geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="78609-112">[in] A bitmask of flags that controls how the status object is opened.</span></span> <span data-ttu-id="78609-113">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="78609-113">The following flag can be set:</span></span>
    
<span data-ttu-id="78609-114">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="78609-114">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="78609-115">Fordert Lese-/Schreibzugriff-Berechtigung an.</span><span class="sxs-lookup"><span data-stu-id="78609-115">Requests read/write permission.</span></span> <span data-ttu-id="78609-116">Die Standardschnittstelle ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="78609-116">The default interface is read-only.</span></span> 
    
 <span data-ttu-id="78609-117">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="78609-117">_lpulObjType_</span></span>
  
> <span data-ttu-id="78609-118">Out Ein Zeiger auf den Typ des geöffneten Objekts.</span><span class="sxs-lookup"><span data-stu-id="78609-118">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="78609-119">_lppEntry_</span><span class="sxs-lookup"><span data-stu-id="78609-119">_lppEntry_</span></span>
  
> <span data-ttu-id="78609-120">Out Ein Zeiger auf den Zeiger auf das geöffnete Status-Objekt.</span><span class="sxs-lookup"><span data-stu-id="78609-120">[out] A pointer to the pointer to the opened status object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="78609-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="78609-121">Return value</span></span>

<span data-ttu-id="78609-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="78609-122">S_OK</span></span> 
  
> <span data-ttu-id="78609-123">Der Aufruf war erfolgreich, und der erwartete Wert oder die Werte wurden zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="78609-123">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="78609-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="78609-124">Remarks</span></span>

<span data-ttu-id="78609-125">Die MAPI-Warteschlange ruft die **IXPLogon:: OpenStatusEntry** -Methode auf, wenn eine \*\*\*\* Clientanwendung eine OpenEntry-Methode für die Eintrags-ID in der Statustabellen Zeile des Transportanbieters aufruft.</span><span class="sxs-lookup"><span data-stu-id="78609-125">The MAPI spooler calls the **IXPLogon::OpenStatusEntry** method when a client application calls an **OpenEntry** method for the entry identifier in the transport provider's status table row.</span></span> <span data-ttu-id="78609-126">**OpenStatusEntry** öffnet ein Objekt mit der **IMAPIStatus** -Schnittstelle, die dieser bestimmten Transportanbieter Anmeldung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="78609-126">**OpenStatusEntry** opens an object with the **IMAPIStatus** interface associated with this particular transport provider logon.</span></span> <span data-ttu-id="78609-127">Dieses Objekt wird dann verwendet, um Clientanwendungen das Aufrufen von **IMAPIStatus** -Methoden (beispielsweise zum erneuten Konfigurieren der Anmeldesitzung mithilfe der [IMAPIStatus:: Settingsdialog](imapistatus-settingsdialog.md) -Methode oder zum Überprüfen des Status der Anmeldesitzung mithilfe der [ IMAPIStatus:: ValidateState](imapistatus-validatestate.md) -Methode).</span><span class="sxs-lookup"><span data-stu-id="78609-127">This object is then used to enable client applications to call **IMAPIStatus** methods (for example, to reconfigure the logon session by using the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method, or to validate the state of the logon session by using the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="78609-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78609-128">See also</span></span>



[<span data-ttu-id="78609-129">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="78609-129">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)
  
[<span data-ttu-id="78609-130">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="78609-130">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

