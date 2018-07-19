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
ms.openlocfilehash: 0e96c0b99f0a5f7511ed59b483ab9409eafad882
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792872"
---
# <a name="ixplogonopenstatusentry"></a><span data-ttu-id="1bbb7-103">IXPLogon::OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="1bbb7-103">IXPLogon::OpenStatusEntry</span></span>

  
  
<span data-ttu-id="1bbb7-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1bbb7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1bbb7-105">Öffnet die Adressbuchhierarchie Status-Objekt.</span><span class="sxs-lookup"><span data-stu-id="1bbb7-105">Opens the transport provider's status object.</span></span>
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPMAPISTATUS FAR * lppEntry
);
```

## <a name="parameters"></a><span data-ttu-id="1bbb7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1bbb7-106">Parameters</span></span>

 <span data-ttu-id="1bbb7-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="1bbb7-107">_lpInterface_</span></span>
  
> <span data-ttu-id="1bbb7-108">[in] Ein Zeiger auf eine Schnittstellenbezeichner (IID) für die Anmeldung Transportobjekt.</span><span class="sxs-lookup"><span data-stu-id="1bbb7-108">[in] A pointer to an interface identifier (IID) for the transport logon object.</span></span> <span data-ttu-id="1bbb7-109">Übergeben von NULL gibt die [IMAPIStatus](imapistatusimapiprop.md) -Schnittstelle zurück.</span><span class="sxs-lookup"><span data-stu-id="1bbb7-109">Passing NULL returns the [IMAPIStatus](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="1bbb7-110">Der Parameter _LpInterface_ kann auch auf einen Bezeichner für eine Schnittstelle für das Objekt festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="1bbb7-110">The  _lpInterface_ parameter can also be set to an identifier for an interface for the object.</span></span> 
    
 <span data-ttu-id="1bbb7-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1bbb7-111">_ulFlags_</span></span>
  
> <span data-ttu-id="1bbb7-112">[in] Eine Bitmaske aus Flags, die steuert, wie das Statusobjekt geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="1bbb7-112">[in] A bitmask of flags that controls how the status object is opened.</span></span> <span data-ttu-id="1bbb7-113">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="1bbb7-113">The following flag can be set:</span></span>
    
<span data-ttu-id="1bbb7-114">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="1bbb7-114">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="1bbb7-115">Anfragen Lese-/Schreibberechtigung.</span><span class="sxs-lookup"><span data-stu-id="1bbb7-115">Requests read/write permission.</span></span> <span data-ttu-id="1bbb7-116">Die Standard-Schnittstelle ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="1bbb7-116">The default interface is read-only.</span></span> 
    
 <span data-ttu-id="1bbb7-117">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="1bbb7-117">_lpulObjType_</span></span>
  
> <span data-ttu-id="1bbb7-118">[out] Ein Zeiger auf den Typ des Objekts geöffnet.</span><span class="sxs-lookup"><span data-stu-id="1bbb7-118">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="1bbb7-119">_lppEntry_</span><span class="sxs-lookup"><span data-stu-id="1bbb7-119">_lppEntry_</span></span>
  
> <span data-ttu-id="1bbb7-120">[out] Ein Zeiger auf den Zeiger auf das Statusobjekt geöffnet.</span><span class="sxs-lookup"><span data-stu-id="1bbb7-120">[out] A pointer to the pointer to the opened status object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1bbb7-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1bbb7-121">Return value</span></span>

<span data-ttu-id="1bbb7-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="1bbb7-122">S_OK</span></span> 
  
> <span data-ttu-id="1bbb7-123">Der Aufruf erfolgreich ausgeführt und der erwartete Wert oder Werte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1bbb7-123">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1bbb7-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1bbb7-124">Remarks</span></span>

<span data-ttu-id="1bbb7-125">Die MAPI-Warteschlange Ruft die **IXPLogon::OpenStatusEntry** -Methode auf, wenn eine Clientanwendung für die Eintrags-ID in der Adressbuchhierarchie Status Tabellenzeile eine **OpenEntry** -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="1bbb7-125">The MAPI spooler calls the **IXPLogon::OpenStatusEntry** method when a client application calls an **OpenEntry** method for the entry identifier in the transport provider's status table row.</span></span> <span data-ttu-id="1bbb7-126">**OpenStatusEntry** öffnet ein Objekt mit der **IMAPIStatus** -Schnittstelle in bestimmten Transport Anbieter Anmeldung zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="1bbb7-126">**OpenStatusEntry** opens an object with the **IMAPIStatus** interface associated with this particular transport provider logon.</span></span> <span data-ttu-id="1bbb7-127">Dieses Objekt wird dann verwendet, um die Clientanwendungen zum Aufrufen von Methoden (z. B. so konfigurieren Sie die Sitzung neu mithilfe [der SettingsDialog](imapistatus-settingsdialog.md) oder Überprüfen Sie den Status der die Sitzung mithilfe der [ **IMAPIStatus** aktivieren IMAPIStatus::ValidateState](imapistatus-validatestate.md) Methode).</span><span class="sxs-lookup"><span data-stu-id="1bbb7-127">This object is then used to enable client applications to call **IMAPIStatus** methods (for example, to reconfigure the logon session by using the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method, or to validate the state of the logon session by using the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1bbb7-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1bbb7-128">See also</span></span>



[<span data-ttu-id="1bbb7-129">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="1bbb7-129">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)
  
[<span data-ttu-id="1bbb7-130">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1bbb7-130">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

