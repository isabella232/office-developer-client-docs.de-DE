---
title: IMSLogonOpenStatusEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.OpenStatusEntry
api_type:
- COM
ms.assetid: 850e256b-6b50-428c-aede-287edaf7b005
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a48d8248878c64de827bb09030073e6becba3024
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571199"
---
# <a name="imslogonopenstatusentry"></a><span data-ttu-id="35402-103">IMSLogon::OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="35402-103">IMSLogon::OpenStatusEntry</span></span>

  
  
<span data-ttu-id="35402-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="35402-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="35402-105">Öffnet ein Statusobjekt.</span><span class="sxs-lookup"><span data-stu-id="35402-105">Opens a status object.</span></span>
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPVOID FAR * lppEntry
);
```

## <a name="parameters"></a><span data-ttu-id="35402-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="35402-106">Parameters</span></span>

 <span data-ttu-id="35402-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="35402-107">_lpInterface_</span></span>
  
> <span data-ttu-id="35402-108">[in] Ein Zeiger auf die Schnittstelle-ID (IID) für die Statusobjekt zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="35402-108">[in] A pointer to the interface identifier (IID) for the status object to open.</span></span> <span data-ttu-id="35402-109">Übergeben von NULL gibt an, dass der standard-Benutzeroberfläche für das Objekt (in diesem Fall die Schnittstelle [IMAPIStatus](imapistatusimapiprop.md) ) zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="35402-109">Passing NULL indicates the standard interface for the object is returned (in this case, the [IMAPIStatus](imapistatusimapiprop.md) interface).</span></span> <span data-ttu-id="35402-110">Der Parameter _LpInterface_ kann auch auf einen Bezeichner für eine entsprechende Schnittstelle für das Objekt festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="35402-110">The  _lpInterface_ parameter can also be set to an identifier for an appropriate interface for the object.</span></span> 
    
 <span data-ttu-id="35402-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="35402-111">_ulFlags_</span></span>
  
> <span data-ttu-id="35402-112">[in] Eine Bitmaske aus Flags, die steuert, wie das Statusobjekt geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="35402-112">[in] A bitmask of flags that controls how the status object is opened.</span></span> <span data-ttu-id="35402-113">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="35402-113">The following flag can be set:</span></span>
    
<span data-ttu-id="35402-114">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="35402-114">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="35402-115">Anfragen Lese-/Schreibberechtigung.</span><span class="sxs-lookup"><span data-stu-id="35402-115">Requests read/write permission.</span></span> <span data-ttu-id="35402-116">Standardmäßig werden Objekte mit Leseberechtigung erstellt und Clientanwendungen sollte nicht verwendet werden, unter der Voraussetzung, die Lese-/Schreibzugriff, dass die Berechtigung erteilt wurde.</span><span class="sxs-lookup"><span data-stu-id="35402-116">By default, objects are created with read-only permission, and client applications should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="35402-117">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="35402-117">_lpulObjType_</span></span>
  
> <span data-ttu-id="35402-118">[out] Ein Zeiger auf den Typ des Objekts geöffnet.</span><span class="sxs-lookup"><span data-stu-id="35402-118">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="35402-119">_lppEntry_</span><span class="sxs-lookup"><span data-stu-id="35402-119">_lppEntry_</span></span>
  
> <span data-ttu-id="35402-120">[out] Ein Zeiger auf den Zeiger auf das geöffnete Objekt.</span><span class="sxs-lookup"><span data-stu-id="35402-120">[out] A pointer to the pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="35402-121">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="35402-121">Return value</span></span>

<span data-ttu-id="35402-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="35402-122">S_OK</span></span> 
  
> <span data-ttu-id="35402-123">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="35402-123">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="35402-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="35402-124">Remarks</span></span>

<span data-ttu-id="35402-125">Nachricht-Anbieter implementiert die **IMSLogon::OpenStatusEntry** -Methode, um ein Statusobjekt zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="35402-125">Message store providers implement the **IMSLogon::OpenStatusEntry** method to open a status object.</span></span> <span data-ttu-id="35402-126">Dieser Statusobjekt wird dann verwendet, damit Clients [IMAPIStatus](imapistatusimapiprop.md) Methoden aufrufen können.</span><span class="sxs-lookup"><span data-stu-id="35402-126">This status object is then used to enable clients to call [IMAPIStatus](imapistatusimapiprop.md) methods.</span></span> <span data-ttu-id="35402-127">Beispielsweise können Clients [die SettingsDialog](imapistatus-settingsdialog.md) verwenden, konfigurieren Sie die Nachricht Store-Sitzung oder die [IMAPIStatus::ValidateState](imapistatus-validatestate.md) -Methode, um den Status der Nachricht Store Anmeldung Sitzung zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="35402-127">For example, clients can use the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method to reconfigure the message store logon session or the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method to validate the state of the message store logon session.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="35402-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="35402-128">See also</span></span>



[<span data-ttu-id="35402-129">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="35402-129">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)
  
[<span data-ttu-id="35402-130">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="35402-130">IMAPIStatus::SettingsDialog</span></span>](imapistatus-settingsdialog.md)
  
[<span data-ttu-id="35402-131">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="35402-131">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
  
[<span data-ttu-id="35402-132">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="35402-132">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

