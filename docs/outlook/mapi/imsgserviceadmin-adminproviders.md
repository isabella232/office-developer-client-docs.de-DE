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
ms.openlocfilehash: 6b7360995a781824b50ff02b5d2dec8e481e7ba7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317423"
---
# <a name="imsgserviceadminadminproviders"></a><span data-ttu-id="5b0cb-103">IMsgServiceAdmin::AdminProviders</span><span class="sxs-lookup"><span data-stu-id="5b0cb-103">IMsgServiceAdmin::AdminProviders</span></span>

  
  
<span data-ttu-id="5b0cb-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5b0cb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5b0cb-105">Gibt einen Zeiger zurück, der Zugriff auf ein Anbieter Verwaltungsobjekt bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="5b0cb-105">Returns a pointer that provides access to a provider administration object.</span></span>
  
```cpp
HRESULT AdminProviders(
  LPMAPIUID lpUID,
  ULONG ulFlags,
  LPPROVIDERADMIN FAR * lppProviderAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="5b0cb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b0cb-106">Parameters</span></span>

 <span data-ttu-id="5b0cb-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="5b0cb-107">_lpUID_</span></span>
  
> <span data-ttu-id="5b0cb-108">in Ein Zeiger auf die [MAPIUID](mapiuid.md) -Struktur, die den eindeutigen Bezeichner für den zu verwaltenden Nachrichtendienst enthält.</span><span class="sxs-lookup"><span data-stu-id="5b0cb-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to be administered.</span></span> 
    
 <span data-ttu-id="5b0cb-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5b0cb-109">_ulFlags_</span></span>
  
> <span data-ttu-id="5b0cb-110">in Immer NULL.</span><span class="sxs-lookup"><span data-stu-id="5b0cb-110">[in] Always NULL.</span></span> 
    
 <span data-ttu-id="5b0cb-111">_lppProviderAdmin_</span><span class="sxs-lookup"><span data-stu-id="5b0cb-111">_lppProviderAdmin_</span></span>
  
> <span data-ttu-id="5b0cb-112">Out Ein Zeiger auf einen Zeiger auf ein Anbieter Verwaltungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="5b0cb-112">[out] A pointer to a pointer to a provider administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5b0cb-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5b0cb-113">Return value</span></span>

<span data-ttu-id="5b0cb-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="5b0cb-114">S_OK</span></span> 
  
> <span data-ttu-id="5b0cb-115">Das Anbieter Verwaltungsobjekt wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5b0cb-115">The provider administration object was successfully returned.</span></span>
    
<span data-ttu-id="5b0cb-116">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="5b0cb-116">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="5b0cb-117">Die **MAPIUID** , auf die durch _lpUID_ verwiesen wird, ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="5b0cb-117">The **MAPIUID** pointed to by  _lpUID_ does not exist.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5b0cb-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5b0cb-118">Remarks</span></span>

<span data-ttu-id="5b0cb-119">Die **IMsgServiceAdmin:: AdminProviders** -Methode ermöglicht den Zugriff auf ein Anbieter Verwaltungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="5b0cb-119">The **IMsgServiceAdmin::AdminProviders** method provides access to a provider administration object.</span></span> <span data-ttu-id="5b0cb-120">Eine Anbieterverwaltung ist ein Objekt, das die [IProviderAdmin](iprovideradminiunknown.md) -Schnittstelle unterstützt und Clients folgende Aktionen ermöglicht:</span><span class="sxs-lookup"><span data-stu-id="5b0cb-120">A provider administration is an object that supports the [IProviderAdmin](iprovideradminiunknown.md) interface and enables clients to do the following:</span></span> 
  
- <span data-ttu-id="5b0cb-121">Hinzufügen von Dienstanbietern zu einem Nachrichtendienst</span><span class="sxs-lookup"><span data-stu-id="5b0cb-121">Add service providers to a message service.</span></span>
    
- <span data-ttu-id="5b0cb-122">Löschen von Dienstanbietern aus einem Nachrichtendienst.</span><span class="sxs-lookup"><span data-stu-id="5b0cb-122">Delete service providers from a message service.</span></span>
    
- <span data-ttu-id="5b0cb-123">Öffnen Sie Profilabschnitte.</span><span class="sxs-lookup"><span data-stu-id="5b0cb-123">Open profile sections.</span></span>
    
- <span data-ttu-id="5b0cb-124">Zugreifen auf die Tabelle des Nachrichtendienst Anbieters.</span><span class="sxs-lookup"><span data-stu-id="5b0cb-124">Access the message service provider table.</span></span>
    
<span data-ttu-id="5b0cb-125">Die Typen von Änderungen, die an einem Nachrichtendienst vorgenommen werden können, während das Profil verwendet wird, hängen vom Nachrichtendienst ab.</span><span class="sxs-lookup"><span data-stu-id="5b0cb-125">The types of changes that can actually be made to a message service while the profile is in use depend on the message service.</span></span> <span data-ttu-id="5b0cb-126">Die meisten Nachrichtendienste unterstützen jedoch keine Änderungen wie das Hinzufügen und Löschen von Anbietern, während das Profil verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5b0cb-126">However, most message services do not support changes such as adding and deleting providers while the profile is in use.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="5b0cb-127">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="5b0cb-127">Notes to callers</span></span>

<span data-ttu-id="5b0cb-128">Um die **MAPIUID** -Struktur für den zu verwaltenden Nachrichtendienst abzurufen, rufen Sie die **PR_SERVICE_UID** ([pidtagserviceuid (](pidtagserviceuid-canonical-property.md))-Eigenschaftsspalte aus der Zeile des Nachrichtendiensts in der Nachrichtendienst Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="5b0cb-128">To retrieve the **MAPIUID** structure for the message service to administer, retrieve the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property column from the message service's row in the message service table.</span></span> <span data-ttu-id="5b0cb-129">Weitere Informationen finden Sie in der in der [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md) -Methode beschriebenen Prozedur.</span><span class="sxs-lookup"><span data-stu-id="5b0cb-129">For more information, see the procedure outlined in the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5b0cb-130">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="5b0cb-130">MFCMAPI reference</span></span>

<span data-ttu-id="5b0cb-131">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="5b0cb-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5b0cb-132">**Datei**</span><span class="sxs-lookup"><span data-stu-id="5b0cb-132">**File**</span></span>|<span data-ttu-id="5b0cb-133">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="5b0cb-133">**Function**</span></span>|<span data-ttu-id="5b0cb-134">**Comment**</span><span class="sxs-lookup"><span data-stu-id="5b0cb-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5b0cb-135">MsgServiceTableDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="5b0cb-135">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="5b0cb-136">CMsgServiceTableDlg:: OnDisplayItem</span><span class="sxs-lookup"><span data-stu-id="5b0cb-136">CMsgServiceTableDlg::OnDisplayItem</span></span>  <br/> |<span data-ttu-id="5b0cb-137">MFCMAPI verwendet die **IMsgServiceAdmin:: AdminProviders** -Methode, um ein Anbieter Verwaltungsobjekt für einen Dienst zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="5b0cb-137">MFCMAPI uses the **IMsgServiceAdmin::AdminProviders** method to open a provider administration object for a service.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5b0cb-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5b0cb-138">See also</span></span>



[<span data-ttu-id="5b0cb-139">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5b0cb-139">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)
  
[<span data-ttu-id="5b0cb-140">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="5b0cb-140">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="5b0cb-141">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5b0cb-141">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="5b0cb-142">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="5b0cb-142">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

