---
title: IMsgServiceAdminMsgServiceTransportOrder
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.MsgServiceTransportOrder
api_type:
- COM
ms.assetid: c57ada0e-b9a1-496b-8548-75686d8cba4e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 559f1c609000608d0eb920a0240ac8848e4bc2a7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570793"
---
# <a name="imsgserviceadminmsgservicetransportorder"></a><span data-ttu-id="4f4a3-103">IMsgServiceAdmin::MsgServiceTransportOrder</span><span class="sxs-lookup"><span data-stu-id="4f4a3-103">IMsgServiceAdmin::MsgServiceTransportOrder</span></span>

  
  
<span data-ttu-id="4f4a3-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4f4a3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4f4a3-105">Legt die Reihenfolge, in welcher, die Transport Anbieter aufgerufen werden, um eine Nachricht zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="4f4a3-105">Sets the order in which transport providers are called to deliver a message.</span></span>
  
```cpp
HRESULT MsgServiceTransportOrder(
  ULONG cUID,
  LPMAPIUID lpUIDList,
  ULONG ulFlags    
);
```

## <a name="parameters"></a><span data-ttu-id="4f4a3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f4a3-106">Parameters</span></span>

 <span data-ttu-id="4f4a3-107">_cUID_</span><span class="sxs-lookup"><span data-stu-id="4f4a3-107">_cUID_</span></span>
  
> <span data-ttu-id="4f4a3-108">[in] Die Anzahl der eindeutige Bezeichner in der _LpUIDList_ -Parameter.</span><span class="sxs-lookup"><span data-stu-id="4f4a3-108">[in] The count of unique identifiers in the  _lpUIDList_ parameter.</span></span> 
    
 <span data-ttu-id="4f4a3-109">_lpUIDList_</span><span class="sxs-lookup"><span data-stu-id="4f4a3-109">_lpUIDList_</span></span>
  
> <span data-ttu-id="4f4a3-110">[in] Ein Zeiger auf ein Array Eindeutiger Bezeichner, die Transportanbieter darstellen.</span><span class="sxs-lookup"><span data-stu-id="4f4a3-110">[in] A pointer to an array of unique identifiers that represent transport providers.</span></span> <span data-ttu-id="4f4a3-111">Das Array enthält einen Bezeichner für die einzelnen Transportanbieter im aktuellen Profil konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="4f4a3-111">The array contains one identifier for each transport provider configured in the current profile.</span></span>
    
 <span data-ttu-id="4f4a3-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4f4a3-112">_ulFlags_</span></span>
  
> <span data-ttu-id="4f4a3-113">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="4f4a3-113">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4f4a3-114">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="4f4a3-114">Return value</span></span>

<span data-ttu-id="4f4a3-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="4f4a3-115">S_OK</span></span> 
  
> <span data-ttu-id="4f4a3-116">Die Reihenfolge der Transport wurde erfolgreich festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4f4a3-116">The transport order was set successfully.</span></span>
    
<span data-ttu-id="4f4a3-117">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="4f4a3-117">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="4f4a3-118">Der Wert in der _cUID_ -Parameter unterscheidet sich von der Anzahl der Transportanbieter tatsächlich im Profil.</span><span class="sxs-lookup"><span data-stu-id="4f4a3-118">The value in the  _cUID_ parameter differs from the number of transport providers actually in the profile.</span></span> 
    
<span data-ttu-id="4f4a3-119">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="4f4a3-119">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="4f4a3-120">Eine oder mehrere der in der _LpUIDList_ -Parameter übergeben [MAPIUID](mapiuid.md) Strukturen verweisen nicht auf eine Adressbuchhierarchie derzeit im Profil.</span><span class="sxs-lookup"><span data-stu-id="4f4a3-120">One or more of the [MAPIUID](mapiuid.md) structures passed in the  _lpUIDList_ parameter do not refer to a transport provider currently in the profile.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="4f4a3-121">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="4f4a3-121">Remarks</span></span>

<span data-ttu-id="4f4a3-122">Die **IMsgServiceAdmin::MsgServiceTransportOrder** -Methode legt die Reihenfolge der Übermittlung der Transportanbieter in einem Profil.</span><span class="sxs-lookup"><span data-stu-id="4f4a3-122">The **IMsgServiceAdmin::MsgServiceTransportOrder** method sets the delivery order of transport providers in a profile.</span></span> <span data-ttu-id="4f4a3-123">Der _LpUIDList_ -Parameter muss eine sortierte Liste der Adressbuchhierarchie Eintragsbezeichner abgerufen, die aus der Eigenschaft **PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md)) aus der [IMsgServiceAdmin zurückgegebene Tabelle enthalten:: GetProviderTable](imsgserviceadmin-getprovidertable.md) Methode.</span><span class="sxs-lookup"><span data-stu-id="4f4a3-123">The  _lpUIDList_ parameter must contain a sorted list of transport-provider entry identifiers obtained from the **PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md)) property of the table returned from the [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) method.</span></span> <span data-ttu-id="4f4a3-124">Eine Clientanwendung muss die vollständige Liste _LpUIDList_übergeben.</span><span class="sxs-lookup"><span data-stu-id="4f4a3-124">A client application must pass the complete list in  _lpUIDList_.</span></span>
  
 <span data-ttu-id="4f4a3-125">**SetTransportOrder** Außerkraftsetzungen transport-Anbieter-Einstellungen wie das STATUS_XP_PREFER_LAST-Flag, das in der Eigenschaft **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4f4a3-125">**SetTransportOrder** overrides transport provider preferences such as the STATUS_XP_PREFER_LAST flag set in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4f4a3-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f4a3-126">See also</span></span>



[<span data-ttu-id="4f4a3-127">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="4f4a3-127">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="4f4a3-128">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4f4a3-128">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

