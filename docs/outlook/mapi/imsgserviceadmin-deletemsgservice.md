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
# <a name="imsgserviceadmindeletemsgservice"></a><span data-ttu-id="3e928-103">IMsgServiceAdmin::DeleteMsgService</span><span class="sxs-lookup"><span data-stu-id="3e928-103">IMsgServiceAdmin::DeleteMsgService</span></span>

  
  
<span data-ttu-id="3e928-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3e928-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3e928-105">Löscht einen Nachrichtendienst aus einem Profil.</span><span class="sxs-lookup"><span data-stu-id="3e928-105">Deletes a message service from a profile.</span></span>
  
```cpp
HRESULT DeleteMsgService(
  LPMAPIUID lpuid
);
```

## <a name="parameters"></a><span data-ttu-id="3e928-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e928-106">Parameters</span></span>

 <span data-ttu-id="3e928-107">_lpuid_</span><span class="sxs-lookup"><span data-stu-id="3e928-107">_lpuid_</span></span>
  
> <span data-ttu-id="3e928-108">[in] Ein Zeiger auf die [MAPIUID-Struktur,](mapiuid.md) die den eindeutigen Bezeichner für den zu löschenden Nachrichtendienst enthält.</span><span class="sxs-lookup"><span data-stu-id="3e928-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to delete.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3e928-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3e928-109">Return value</span></span>

<span data-ttu-id="3e928-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="3e928-110">S_OK</span></span> 
  
> <span data-ttu-id="3e928-111">Der Nachrichtendienst wurde gelöscht.</span><span class="sxs-lookup"><span data-stu-id="3e928-111">The message service was deleted.</span></span>
    
<span data-ttu-id="3e928-112">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="3e928-112">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="3e928-113">Die **mapIUID,** auf die  _von lpuid verwiesen wird,_ ist nicht mit einem vorhandenen Nachrichtendienst übereinstimmend.</span><span class="sxs-lookup"><span data-stu-id="3e928-113">The **MAPIUID** pointed to by  _lpuid_ does not match an existing message service.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="3e928-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3e928-114">Remarks</span></span>

<span data-ttu-id="3e928-115">Die **IMsgServiceAdmin::D eleteMsgService-Methode** löscht einen Nachrichtendienst aus einem Profil.</span><span class="sxs-lookup"><span data-stu-id="3e928-115">The **IMsgServiceAdmin::DeleteMsgService** method deletes a message service from a profile.</span></span> <span data-ttu-id="3e928-116">**DeleteMsgService** entfernt alle Profilabschnitte im Zusammenhang mit dem Nachrichtendienst.</span><span class="sxs-lookup"><span data-stu-id="3e928-116">**DeleteMsgService** removes all profile sections related to the message service.</span></span> 
  
 <span data-ttu-id="3e928-117">**DeleteMsgService** führt die folgenden Schritte aus, um den Nachrichtendienst zu löschen:</span><span class="sxs-lookup"><span data-stu-id="3e928-117">**DeleteMsgService** performs the following steps to delete the message service:</span></span> 
  
1. <span data-ttu-id="3e928-118">Ruft die Einstiegspunktfunktion des Nachrichtendiensts auf, und der  _ulContext-Parameter_ ist auf MSG_SERVICE_DELETE, bevor die Profilabschnitte entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="3e928-118">Calls the message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_DELETE before the profile sections are removed.</span></span> <span data-ttu-id="3e928-119">Dadurch kann der Dienst dienstspezifische Aufgaben ausführen.</span><span class="sxs-lookup"><span data-stu-id="3e928-119">This allows the service to perform any service-specific tasks.</span></span> 
    
2. <span data-ttu-id="3e928-120">Löscht den Nachrichtendienst.</span><span class="sxs-lookup"><span data-stu-id="3e928-120">Deletes the message service.</span></span>
    
3. <span data-ttu-id="3e928-121">Löscht den Profilabschnitt des Nachrichtendiensts.</span><span class="sxs-lookup"><span data-stu-id="3e928-121">Deletes the message service's profile section.</span></span>
    
<span data-ttu-id="3e928-122">Die Einstiegspunktfunktion des Nachrichtendiensts wird nicht erneut aufgerufen, nachdem der Dienst gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="3e928-122">The message service's entry point function is not called again after the service has been deleted.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="3e928-123">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="3e928-123">Notes to callers</span></span>

<span data-ttu-id="3e928-124">Um die **MAPIUID-Struktur** für den zu löschenden Nachrichtendienst abzurufen, rufen Sie die **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))-Eigenschaftsspalte aus der Zeile des Nachrichtendiensts in der Nachrichtendiensttabelle ab.</span><span class="sxs-lookup"><span data-stu-id="3e928-124">To retrieve the **MAPIUID** structure for the message service to delete, retrieve the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property column from the message service's row in the message service table.</span></span> <span data-ttu-id="3e928-125">Weitere Informationen finden Sie in der in der [IMsgServiceAdmin::CreateMsgService-Methode beschriebenen](imsgserviceadmin-createmsgservice.md) Prozedur.</span><span class="sxs-lookup"><span data-stu-id="3e928-125">For more information, see the procedure outlined in the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="3e928-126">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="3e928-126">MFCMAPI reference</span></span>

<span data-ttu-id="3e928-127">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="3e928-127">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="3e928-128">**Datei**</span><span class="sxs-lookup"><span data-stu-id="3e928-128">**File**</span></span>|<span data-ttu-id="3e928-129">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="3e928-129">**Function**</span></span>|<span data-ttu-id="3e928-130">**Comment**</span><span class="sxs-lookup"><span data-stu-id="3e928-130">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3e928-131">MsgServiceTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="3e928-131">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="3e928-132">CMsgServiceTableDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="3e928-132">CMsgServiceTableDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="3e928-133">MFCMAPI verwendet die **IMsgServiceAdmin::D eleteMsgService-Methode,** um den ausgewählten Dienst zu löschen.</span><span class="sxs-lookup"><span data-stu-id="3e928-133">MFCMAPI uses the **IMsgServiceAdmin::DeleteMsgService** method to delete the selected service.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3e928-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3e928-134">See also</span></span>



[<span data-ttu-id="3e928-135">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="3e928-135">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="3e928-136">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3e928-136">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="3e928-137">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="3e928-137">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

