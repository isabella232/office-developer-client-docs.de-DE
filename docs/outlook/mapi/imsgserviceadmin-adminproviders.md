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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6b7360995a781824b50ff02b5d2dec8e481e7ba7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422761"
---
# <a name="imsgserviceadminadminproviders"></a><span data-ttu-id="00cb7-103">IMsgServiceAdmin::AdminProviders</span><span class="sxs-lookup"><span data-stu-id="00cb7-103">IMsgServiceAdmin::AdminProviders</span></span>

  
  
<span data-ttu-id="00cb7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="00cb7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="00cb7-105">Gibt einen Zeiger zurück, der Zugriff auf ein Anbieterverwaltungsobjekt bietet.</span><span class="sxs-lookup"><span data-stu-id="00cb7-105">Returns a pointer that provides access to a provider administration object.</span></span>
  
```cpp
HRESULT AdminProviders(
  LPMAPIUID lpUID,
  ULONG ulFlags,
  LPPROVIDERADMIN FAR * lppProviderAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="00cb7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="00cb7-106">Parameters</span></span>

 <span data-ttu-id="00cb7-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="00cb7-107">_lpUID_</span></span>
  
> <span data-ttu-id="00cb7-108">[in] Ein Zeiger auf die [MAPIUID-Struktur,](mapiuid.md) die den eindeutigen Bezeichner für den zu verwaltenden Nachrichtendienst enthält.</span><span class="sxs-lookup"><span data-stu-id="00cb7-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to be administered.</span></span> 
    
 <span data-ttu-id="00cb7-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="00cb7-109">_ulFlags_</span></span>
  
> <span data-ttu-id="00cb7-110">[in] Immer NULL.</span><span class="sxs-lookup"><span data-stu-id="00cb7-110">[in] Always NULL.</span></span> 
    
 <span data-ttu-id="00cb7-111">_lppProviderAdmin_</span><span class="sxs-lookup"><span data-stu-id="00cb7-111">_lppProviderAdmin_</span></span>
  
> <span data-ttu-id="00cb7-112">[out] Ein Zeiger auf einen Zeiger auf ein Anbieterverwaltungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="00cb7-112">[out] A pointer to a pointer to a provider administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="00cb7-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="00cb7-113">Return value</span></span>

<span data-ttu-id="00cb7-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="00cb7-114">S_OK</span></span> 
  
> <span data-ttu-id="00cb7-115">Das Objekt für die Anbieterverwaltung wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="00cb7-115">The provider administration object was successfully returned.</span></span>
    
<span data-ttu-id="00cb7-116">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="00cb7-116">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="00cb7-117">Die **MAPIUID,** auf die  _von lpUID_ verwiesen wird, ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="00cb7-117">The **MAPIUID** pointed to by  _lpUID_ does not exist.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="00cb7-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="00cb7-118">Remarks</span></span>

<span data-ttu-id="00cb7-119">Die **IMsgServiceAdmin::AdminProviders-Methode** bietet Zugriff auf ein Anbieterverwaltungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="00cb7-119">The **IMsgServiceAdmin::AdminProviders** method provides access to a provider administration object.</span></span> <span data-ttu-id="00cb7-120">Eine Anbieterverwaltung ist ein Objekt, das die [IProviderAdmin-Schnittstelle](iprovideradminiunknown.md) unterstützt und Clients folgendes ermöglicht:</span><span class="sxs-lookup"><span data-stu-id="00cb7-120">A provider administration is an object that supports the [IProviderAdmin](iprovideradminiunknown.md) interface and enables clients to do the following:</span></span> 
  
- <span data-ttu-id="00cb7-121">Hinzufügen von Dienstanbietern zu einem Nachrichtendienst.</span><span class="sxs-lookup"><span data-stu-id="00cb7-121">Add service providers to a message service.</span></span>
    
- <span data-ttu-id="00cb7-122">Löschen von Dienstanbietern aus einem Nachrichtendienst.</span><span class="sxs-lookup"><span data-stu-id="00cb7-122">Delete service providers from a message service.</span></span>
    
- <span data-ttu-id="00cb7-123">Öffnen Sie Profilabschnitte.</span><span class="sxs-lookup"><span data-stu-id="00cb7-123">Open profile sections.</span></span>
    
- <span data-ttu-id="00cb7-124">Greifen Sie auf die Tabelle des Nachrichtendienstanbieters zu.</span><span class="sxs-lookup"><span data-stu-id="00cb7-124">Access the message service provider table.</span></span>
    
<span data-ttu-id="00cb7-125">Die Arten von Änderungen, die tatsächlich an einem Nachrichtendienst vorgenommen werden können, während das Profil verwendet wird, hängen vom Nachrichtendienst ab.</span><span class="sxs-lookup"><span data-stu-id="00cb7-125">The types of changes that can actually be made to a message service while the profile is in use depend on the message service.</span></span> <span data-ttu-id="00cb7-126">Die meisten Nachrichtendienste unterstützen jedoch keine Änderungen, z. B. das Hinzufügen und Löschen von Anbietern, während das Profil verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="00cb7-126">However, most message services do not support changes such as adding and deleting providers while the profile is in use.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="00cb7-127">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="00cb7-127">Notes to callers</span></span>

<span data-ttu-id="00cb7-128">Um die **MAPIUID-Struktur** für den zu verwaltenden Nachrichtendienst abzurufen, rufen Sie die **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))-Eigenschaftsspalte aus der Zeile des Nachrichtendiensts in der Nachrichtendiensttabelle ab.</span><span class="sxs-lookup"><span data-stu-id="00cb7-128">To retrieve the **MAPIUID** structure for the message service to administer, retrieve the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property column from the message service's row in the message service table.</span></span> <span data-ttu-id="00cb7-129">Weitere Informationen finden Sie in der in der [IMsgServiceAdmin::CreateMsgService-Methode beschriebenen](imsgserviceadmin-createmsgservice.md) Prozedur.</span><span class="sxs-lookup"><span data-stu-id="00cb7-129">For more information, see the procedure outlined in the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="00cb7-130">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="00cb7-130">MFCMAPI reference</span></span>

<span data-ttu-id="00cb7-131">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="00cb7-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="00cb7-132">**Datei**</span><span class="sxs-lookup"><span data-stu-id="00cb7-132">**File**</span></span>|<span data-ttu-id="00cb7-133">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="00cb7-133">**Function**</span></span>|<span data-ttu-id="00cb7-134">**Comment**</span><span class="sxs-lookup"><span data-stu-id="00cb7-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="00cb7-135">MsgServiceTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="00cb7-135">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="00cb7-136">CMsgServiceTableDlg::OnDisplayItem</span><span class="sxs-lookup"><span data-stu-id="00cb7-136">CMsgServiceTableDlg::OnDisplayItem</span></span>  <br/> |<span data-ttu-id="00cb7-137">MFCMAPI verwendet die **IMsgServiceAdmin::AdminProviders-Methode,** um ein Anbieterverwaltungsobjekt für einen Dienst zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="00cb7-137">MFCMAPI uses the **IMsgServiceAdmin::AdminProviders** method to open a provider administration object for a service.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="00cb7-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="00cb7-138">See also</span></span>



[<span data-ttu-id="00cb7-139">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="00cb7-139">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)
  
[<span data-ttu-id="00cb7-140">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="00cb7-140">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="00cb7-141">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="00cb7-141">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="00cb7-142">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="00cb7-142">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

