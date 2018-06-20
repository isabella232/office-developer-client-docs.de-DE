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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0a3021ed386aa00777694452a755693fc4078093
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792590"
---
# <a name="imsgserviceadmindeletemsgservice"></a><span data-ttu-id="08129-103">IMsgServiceAdmin::DeleteMsgService</span><span class="sxs-lookup"><span data-stu-id="08129-103">IMsgServiceAdmin::DeleteMsgService</span></span>

  
  
<span data-ttu-id="08129-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="08129-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="08129-105">Löscht eine Message Service aus einem Profil.</span><span class="sxs-lookup"><span data-stu-id="08129-105">Deletes a message service from a profile.</span></span>
  
```cpp
HRESULT DeleteMsgService(
  LPMAPIUID lpuid
);
```

## <a name="parameters"></a><span data-ttu-id="08129-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="08129-106">Parameters</span></span>

 <span data-ttu-id="08129-107">_lpuid_</span><span class="sxs-lookup"><span data-stu-id="08129-107">_lpuid_</span></span>
  
> <span data-ttu-id="08129-108">[in] Ein Zeiger auf die [MAPIUID](mapiuid.md) -Struktur, die den eindeutigen Bezeichner für den zu löschenden Nachrichtendienst enthält.</span><span class="sxs-lookup"><span data-stu-id="08129-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to delete.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="08129-109">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="08129-109">Return value</span></span>

<span data-ttu-id="08129-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="08129-110">S_OK</span></span> 
  
> <span data-ttu-id="08129-111">Der Nachrichtendienst wurde gelöscht.</span><span class="sxs-lookup"><span data-stu-id="08129-111">The message service was deleted.</span></span>
    
<span data-ttu-id="08129-112">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="08129-112">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="08129-113">Die auf den _Lpuid_ **MAPIUID** stimmt nicht mit einer vorhandenen Messagingdiensts überein.</span><span class="sxs-lookup"><span data-stu-id="08129-113">The **MAPIUID** pointed to by  _lpuid_ does not match an existing message service.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="08129-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="08129-114">Remarks</span></span>

<span data-ttu-id="08129-115">Die **IMsgServiceAdmin::DeleteMsgService** -Methode löscht eine Message Service aus einem Profil.</span><span class="sxs-lookup"><span data-stu-id="08129-115">The **IMsgServiceAdmin::DeleteMsgService** method deletes a message service from a profile.</span></span> <span data-ttu-id="08129-116">**DeleteMsgService** entfernt alle Profil Abschnitte im Zusammenhang mit den Dienst.</span><span class="sxs-lookup"><span data-stu-id="08129-116">**DeleteMsgService** removes all profile sections related to the message service.</span></span> 
  
 <span data-ttu-id="08129-117">**DeleteMsgService** führt die folgenden Schritte aus, um den Dienst zu löschen:</span><span class="sxs-lookup"><span data-stu-id="08129-117">**DeleteMsgService** performs the following steps to delete the message service:</span></span> 
  
1. <span data-ttu-id="08129-118">Ruft die Messagingdiensts Eintrag Point-Funktion mit dem _UlContext_ -Parameter auf MSG_SERVICE_DELETE festgelegt werden, bevor die Abschnitte Profil entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="08129-118">Calls the message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_DELETE before the profile sections are removed.</span></span> <span data-ttu-id="08129-119">Dadurch wird den Dienst dienstspezifische Aufgaben ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="08129-119">This allows the service to perform any service-specific tasks.</span></span> 
    
2. <span data-ttu-id="08129-120">Löscht den Dienst an.</span><span class="sxs-lookup"><span data-stu-id="08129-120">Deletes the message service.</span></span>
    
3. <span data-ttu-id="08129-121">Löscht die Messagingdiensts Profilabschnitt.</span><span class="sxs-lookup"><span data-stu-id="08129-121">Deletes the message service's profile section.</span></span>
    
<span data-ttu-id="08129-122">Die Messagingdiensts Eintrag Point-Funktion wird nicht erneut aufgerufen, nachdem der Dienst gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="08129-122">The message service's entry point function is not called again after the service has been deleted.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="08129-123">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="08129-123">Notes to callers</span></span>

<span data-ttu-id="08129-124">Zum Abrufen der **MAPIUID** -Struktur für den Dienst zu löschen, Abrufen die Spalte **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) aus der Nachrichtendienst Zeile in der Tabelle der Dienste.</span><span class="sxs-lookup"><span data-stu-id="08129-124">To retrieve the **MAPIUID** structure for the message service to delete, retrieve the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property column from the message service's row in the message service table.</span></span> <span data-ttu-id="08129-125">Weitere Informationen finden Sie unter dem Verfahren in der [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="08129-125">For more information, see the procedure outlined in the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="08129-126">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="08129-126">MFCMAPI reference</span></span>

<span data-ttu-id="08129-127">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="08129-127">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="08129-128">**Datei**</span><span class="sxs-lookup"><span data-stu-id="08129-128">**File**</span></span>|<span data-ttu-id="08129-129">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="08129-129">**Function**</span></span>|<span data-ttu-id="08129-130">**Comment**</span><span class="sxs-lookup"><span data-stu-id="08129-130">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="08129-131">MsgServiceTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="08129-131">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="08129-132">CMsgServiceTableDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="08129-132">CMsgServiceTableDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="08129-133">MFCMAPI (engl.) verwendet die **IMsgServiceAdmin::DeleteMsgService** -Methode, um die ausgewählte dienstanwendung zu löschen.</span><span class="sxs-lookup"><span data-stu-id="08129-133">MFCMAPI uses the **IMsgServiceAdmin::DeleteMsgService** method to delete the selected service.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="08129-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08129-134">See also</span></span>



[<span data-ttu-id="08129-135">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="08129-135">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="08129-136">IMsgServiceAdmin: IUnknown</span><span class="sxs-lookup"><span data-stu-id="08129-136">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="08129-137">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="08129-137">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
