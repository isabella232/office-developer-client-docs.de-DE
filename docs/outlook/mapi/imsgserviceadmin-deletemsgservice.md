---
title: IMsgServiceAdminDeleteMsgService
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.DeleteMsgService
api_type:
- COM
ms.assetid: 3a6b34eb-9d46-488f-8d02-91b27c35de67
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6cef03e33abab81a407698b73a007f247ef88194
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407382"
---
# <a name="imsgserviceadmindeletemsgservice"></a><span data-ttu-id="d65f2-103">IMsgServiceAdmin::DeleteMsgService</span><span class="sxs-lookup"><span data-stu-id="d65f2-103">IMsgServiceAdmin::DeleteMsgService</span></span>

  
  
<span data-ttu-id="d65f2-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d65f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d65f2-105">Löscht einen Nachrichtendienst aus einem Profil.</span><span class="sxs-lookup"><span data-stu-id="d65f2-105">Deletes a message service from a profile.</span></span>
  
```cpp
HRESULT DeleteMsgService(
  LPMAPIUID lpuid
);
```

## <a name="parameters"></a><span data-ttu-id="d65f2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d65f2-106">Parameters</span></span>

 <span data-ttu-id="d65f2-107">_lpuid_</span><span class="sxs-lookup"><span data-stu-id="d65f2-107">_lpuid_</span></span>
  
> <span data-ttu-id="d65f2-108">in Ein Zeiger auf die [MAPIUID](mapiuid.md) -Struktur, die den eindeutigen Bezeichner für den zu löschenden Nachrichtendienst enthält.</span><span class="sxs-lookup"><span data-stu-id="d65f2-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to delete.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d65f2-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d65f2-109">Return value</span></span>

<span data-ttu-id="d65f2-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="d65f2-110">S_OK</span></span> 
  
> <span data-ttu-id="d65f2-111">Der Nachrichtendienst wurde gelöscht.</span><span class="sxs-lookup"><span data-stu-id="d65f2-111">The message service was deleted.</span></span>
    
<span data-ttu-id="d65f2-112">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="d65f2-112">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="d65f2-113">Die **MAPIUID** , auf die durch _lpuid_ verwiesen wird, stimmt nicht mit einem vorhandenen Nachrichtendienst überein.</span><span class="sxs-lookup"><span data-stu-id="d65f2-113">The **MAPIUID** pointed to by  _lpuid_ does not match an existing message service.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d65f2-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d65f2-114">Remarks</span></span>

<span data-ttu-id="d65f2-115">Die **IMsgServiceAdmin::D eletemsgservice** -Methode löscht einen Nachrichtendienst aus einem Profil.</span><span class="sxs-lookup"><span data-stu-id="d65f2-115">The **IMsgServiceAdmin::DeleteMsgService** method deletes a message service from a profile.</span></span> <span data-ttu-id="d65f2-116">**DeleteMsgService** entfernt alle Profilabschnitte im Zusammenhang mit dem Nachrichtendienst.</span><span class="sxs-lookup"><span data-stu-id="d65f2-116">**DeleteMsgService** removes all profile sections related to the message service.</span></span> 
  
 <span data-ttu-id="d65f2-117">**DeleteMsgService** führt die folgenden Schritte aus, um den Nachrichtendienst zu löschen:</span><span class="sxs-lookup"><span data-stu-id="d65f2-117">**DeleteMsgService** performs the following steps to delete the message service:</span></span> 
  
1. <span data-ttu-id="d65f2-118">Ruft die Einstiegspunktfunktion des Nachrichtendiensts auf, wobei der Parameter _ulContext_ auf MSG_SERVICE_DELETE festgelegt ist, bevor die Profilabschnitte entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="d65f2-118">Calls the message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_DELETE before the profile sections are removed.</span></span> <span data-ttu-id="d65f2-119">Dadurch kann der Dienst dienstspezifische Aufgaben ausführen.</span><span class="sxs-lookup"><span data-stu-id="d65f2-119">This allows the service to perform any service-specific tasks.</span></span> 
    
2. <span data-ttu-id="d65f2-120">Löscht den Nachrichtendienst.</span><span class="sxs-lookup"><span data-stu-id="d65f2-120">Deletes the message service.</span></span>
    
3. <span data-ttu-id="d65f2-121">Löscht den Profil Abschnitt des Nachrichtendiensts.</span><span class="sxs-lookup"><span data-stu-id="d65f2-121">Deletes the message service's profile section.</span></span>
    
<span data-ttu-id="d65f2-122">Die Einstiegspunktfunktion des Nachrichtendiensts wird nicht erneut aufgerufen, nachdem der Dienst gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="d65f2-122">The message service's entry point function is not called again after the service has been deleted.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="d65f2-123">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="d65f2-123">Notes to callers</span></span>

<span data-ttu-id="d65f2-124">Um die **MAPIUID** -Struktur für den zu löschenden Nachrichtendienst abzurufen, rufen Sie die **PR_SERVICE_UID** ([pidtagserviceuid (](pidtagserviceuid-canonical-property.md))-Eigenschaftsspalte aus der Zeile des Nachrichtendiensts in der Nachrichtendienst Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="d65f2-124">To retrieve the **MAPIUID** structure for the message service to delete, retrieve the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property column from the message service's row in the message service table.</span></span> <span data-ttu-id="d65f2-125">Weitere Informationen finden Sie in der in der [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md) -Methode beschriebenen Prozedur.</span><span class="sxs-lookup"><span data-stu-id="d65f2-125">For more information, see the procedure outlined in the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d65f2-126">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="d65f2-126">MFCMAPI reference</span></span>

<span data-ttu-id="d65f2-127">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d65f2-127">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d65f2-128">**Datei**</span><span class="sxs-lookup"><span data-stu-id="d65f2-128">**File**</span></span>|<span data-ttu-id="d65f2-129">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="d65f2-129">**Function**</span></span>|<span data-ttu-id="d65f2-130">**Comment**</span><span class="sxs-lookup"><span data-stu-id="d65f2-130">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d65f2-131">MsgServiceTableDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="d65f2-131">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="d65f2-132">CMsgServiceTableDlg:: OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="d65f2-132">CMsgServiceTableDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="d65f2-133">MFCMAPI verwendet die **IMsgServiceAdmin::D-eletemsgservice** -Methode, um den ausgewählten Dienst zu löschen.</span><span class="sxs-lookup"><span data-stu-id="d65f2-133">MFCMAPI uses the **IMsgServiceAdmin::DeleteMsgService** method to delete the selected service.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d65f2-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d65f2-134">See also</span></span>



[<span data-ttu-id="d65f2-135">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="d65f2-135">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="d65f2-136">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d65f2-136">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="d65f2-137">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="d65f2-137">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

