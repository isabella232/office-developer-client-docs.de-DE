---
title: IMsgServiceAdminAdminProviders
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.AdminProviders
api_type:
- COM
ms.assetid: 0d605e2c-10db-46e1-95d5-12fabd524baa
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 9b65c8e32580fa85302b874bd17c1829ad67fd63
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792597"
---
# <a name="imsgserviceadminadminproviders"></a><span data-ttu-id="2f309-103">IMsgServiceAdmin::AdminProviders</span><span class="sxs-lookup"><span data-stu-id="2f309-103">IMsgServiceAdmin::AdminProviders</span></span>

  
  
<span data-ttu-id="2f309-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2f309-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2f309-105">Gibt einen Zeiger, der Zugriff auf ein Anbieter Administration-Objekt bietet.</span><span class="sxs-lookup"><span data-stu-id="2f309-105">Returns a pointer that provides access to a provider administration object.</span></span>
  
```cpp
HRESULT AdminProviders(
  LPMAPIUID lpUID,
  ULONG ulFlags,
  LPPROVIDERADMIN FAR * lppProviderAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="2f309-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f309-106">Parameters</span></span>

 <span data-ttu-id="2f309-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="2f309-107">_lpUID_</span></span>
  
> <span data-ttu-id="2f309-108">[in] Ein Zeiger auf die [MAPIUID](mapiuid.md) -Struktur, die den eindeutigen Bezeichner für den Dienst zu verwaltenden enthält.</span><span class="sxs-lookup"><span data-stu-id="2f309-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to be administered.</span></span> 
    
 <span data-ttu-id="2f309-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2f309-109">_ulFlags_</span></span>
  
> <span data-ttu-id="2f309-110">[in] Immer NULL.</span><span class="sxs-lookup"><span data-stu-id="2f309-110">[in] Always NULL.</span></span> 
    
 <span data-ttu-id="2f309-111">_lppProviderAdmin_</span><span class="sxs-lookup"><span data-stu-id="2f309-111">_lppProviderAdmin_</span></span>
  
> <span data-ttu-id="2f309-112">[out] Ein Zeiger auf einen Zeiger auf ein Anbieter Administration-Objekt.</span><span class="sxs-lookup"><span data-stu-id="2f309-112">[out] A pointer to a pointer to a provider administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2f309-113">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="2f309-113">Return value</span></span>

<span data-ttu-id="2f309-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="2f309-114">S_OK</span></span> 
  
> <span data-ttu-id="2f309-115">Der Anbieter Verwaltungsobjekt wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2f309-115">The provider administration object was successfully returned.</span></span>
    
<span data-ttu-id="2f309-116">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="2f309-116">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="2f309-117">Die **MAPIUID** auf den _LpUID_ ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="2f309-117">The **MAPIUID** pointed to by  _lpUID_ does not exist.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="2f309-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2f309-118">Remarks</span></span>

<span data-ttu-id="2f309-119">Die **IMsgServiceAdmin::AdminProviders** -Methode ermöglicht den Zugriff auf ein Anbieter Administration-Objekt.</span><span class="sxs-lookup"><span data-stu-id="2f309-119">The **IMsgServiceAdmin::AdminProviders** method provides access to a provider administration object.</span></span> <span data-ttu-id="2f309-120">Eine Anbieter Verwaltung ist ein Objekt, das die [IProviderAdmin](iprovideradminiunknown.md) -Schnittstelle unterstützt und ermöglicht es Clients, die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="2f309-120">A provider administration is an object that supports the [IProviderAdmin](iprovideradminiunknown.md) interface and enables clients to do the following:</span></span> 
  
- <span data-ttu-id="2f309-121">Fügen Sie eine Message Service-Dienstanbieter hinzu.</span><span class="sxs-lookup"><span data-stu-id="2f309-121">Add service providers to a message service.</span></span>
    
- <span data-ttu-id="2f309-122">Dienstanbieter aus einem Nachrichtendienst zu löschen.</span><span class="sxs-lookup"><span data-stu-id="2f309-122">Delete service providers from a message service.</span></span>
    
- <span data-ttu-id="2f309-123">Profil Abschnitte zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="2f309-123">Open profile sections.</span></span>
    
- <span data-ttu-id="2f309-124">Zugriff auf die Tabelle Nachricht-Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="2f309-124">Access the message service provider table.</span></span>
    
<span data-ttu-id="2f309-125">Die Arten von Änderungen, die mit einer Messagingdiensts tatsächlich hergestellt werden können, während das Profil verwendet wird, hängt von den Dienst.</span><span class="sxs-lookup"><span data-stu-id="2f309-125">The types of changes that can actually be made to a message service while the profile is in use depend on the message service.</span></span> <span data-ttu-id="2f309-126">Die meisten Message Dienste unterstützen nicht jedoch Änderungen wie hinzufügen und Löschen von Anbietern, während das Profil verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2f309-126">However, most message services do not support changes such as adding and deleting providers while the profile is in use.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="2f309-127">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="2f309-127">Notes to callers</span></span>

<span data-ttu-id="2f309-128">Zum Abrufen der **MAPIUID** -Struktur für den Dienst zu verwalten, Abrufen die Spalte **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) aus der Nachrichtendienst Zeile in der Tabelle der Dienste.</span><span class="sxs-lookup"><span data-stu-id="2f309-128">To retrieve the **MAPIUID** structure for the message service to administer, retrieve the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property column from the message service's row in the message service table.</span></span> <span data-ttu-id="2f309-129">Weitere Informationen finden Sie unter dem Verfahren in der [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="2f309-129">For more information, see the procedure outlined in the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="2f309-130">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="2f309-130">MFCMAPI reference</span></span>

<span data-ttu-id="2f309-131">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="2f309-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2f309-132">**Datei**</span><span class="sxs-lookup"><span data-stu-id="2f309-132">**File**</span></span>|<span data-ttu-id="2f309-133">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="2f309-133">**Function**</span></span>|<span data-ttu-id="2f309-134">**Comment**</span><span class="sxs-lookup"><span data-stu-id="2f309-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2f309-135">MsgServiceTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="2f309-135">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="2f309-136">CMsgServiceTableDlg::OnDisplayItem</span><span class="sxs-lookup"><span data-stu-id="2f309-136">CMsgServiceTableDlg::OnDisplayItem</span></span>  <br/> |<span data-ttu-id="2f309-137">MFCMAPI (engl.) wird die **IMsgServiceAdmin::AdminProviders** -Methode verwendet, um einen Anbieter Administration-Objekt für einen Dienst zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="2f309-137">MFCMAPI uses the **IMsgServiceAdmin::AdminProviders** method to open a provider administration object for a service.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2f309-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f309-138">See also</span></span>



[<span data-ttu-id="2f309-139">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2f309-139">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)
  
[<span data-ttu-id="2f309-140">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="2f309-140">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="2f309-141">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2f309-141">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="2f309-142">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="2f309-142">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

