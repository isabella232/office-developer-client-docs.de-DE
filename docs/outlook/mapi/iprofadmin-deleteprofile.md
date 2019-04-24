---
title: IProfAdminDeleteProfile
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.DeleteProfile
api_type:
- COM
ms.assetid: 730af2da-4c4a-42a7-9d52-56d914107d64
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 8aafb849a98028efb37646752a7b49fa5e6ef2ff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309562"
---
# <a name="iprofadmindeleteprofile"></a><span data-ttu-id="6436c-103">IProfAdmin::DeleteProfile</span><span class="sxs-lookup"><span data-stu-id="6436c-103">IProfAdmin::DeleteProfile</span></span>

  
  
<span data-ttu-id="6436c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6436c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6436c-105">Löscht ein Profil.</span><span class="sxs-lookup"><span data-stu-id="6436c-105">Deletes a profile.</span></span>
  
```cpp
HRESULT DeleteProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="6436c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6436c-106">Parameters</span></span>

 <span data-ttu-id="6436c-107">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="6436c-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="6436c-108">in Ein Zeiger auf den Namen des zu löschenden Profils.</span><span class="sxs-lookup"><span data-stu-id="6436c-108">[in] A pointer to the name of the profile to be deleted.</span></span>
    
 <span data-ttu-id="6436c-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6436c-109">_ulFlags_</span></span>
  
> <span data-ttu-id="6436c-110">in Immer NULL.</span><span class="sxs-lookup"><span data-stu-id="6436c-110">[in] Always NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6436c-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6436c-111">Return value</span></span>

<span data-ttu-id="6436c-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="6436c-112">S_OK</span></span> 
  
> <span data-ttu-id="6436c-113">Das Profil wurde erfolgreich gelöscht.</span><span class="sxs-lookup"><span data-stu-id="6436c-113">The profile was successfully deleted.</span></span>
    
<span data-ttu-id="6436c-114">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="6436c-114">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="6436c-115">Das angegebene Profil ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6436c-115">The specified profile does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6436c-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6436c-116">Remarks</span></span>

<span data-ttu-id="6436c-117">Die **IProfAdmin::D eleteprofile** -Methode löscht ein Profil.</span><span class="sxs-lookup"><span data-stu-id="6436c-117">The **IProfAdmin::DeleteProfile** method deletes a profile.</span></span> <span data-ttu-id="6436c-118">Wenn das zu löschende Profil verwendet wird, wenn **DeleteProfile** aufgerufen wird, gibt **DELETEPROFILE** den Wert S_OK zurück, löscht das Profil jedoch nicht sofort.</span><span class="sxs-lookup"><span data-stu-id="6436c-118">If the profile to delete is in use when **DeleteProfile** is called, **DeleteProfile** returns S_OK but does not delete the profile immediately.</span></span> <span data-ttu-id="6436c-119">Stattdessen markiert **DeleteProfile** das Profil zum Löschen und löscht es, nachdem es nicht mehr verwendet wird, wenn alle aktiven Sitzungen beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="6436c-119">Instead, **DeleteProfile** marks the profile for deletion and deletes it after it is no longer being used, when all of its active sessions have ended.</span></span> 
  
<span data-ttu-id="6436c-120">Die Einstiegspunktfunktion für jeden Nachrichtendienst im Profil wird mit dem MSG_SERVICE_DELETE-Wert aufgerufen, der im Parameter _ulContext_ festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="6436c-120">The entry point function for each message service in the profile is called with the MSG_SERVICE_DELETE value set in the  _ulContext_ parameter.</span></span> <span data-ttu-id="6436c-121">Zuerst wird der Dienst von der Funktion gelöscht, und anschließend wird der Profil Abschnitt des Diensts gelöscht.</span><span class="sxs-lookup"><span data-stu-id="6436c-121">First, the function deletes the service, and then it deletes the service's profile section.</span></span> <span data-ttu-id="6436c-122">Die Nachrichtendienst-Einstiegspunktfunktion wird nicht erneut aufgerufen, nachdem der Dienst gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="6436c-122">The message service entry point function is not called again after the service has been deleted.</span></span> 
  
<span data-ttu-id="6436c-123">Zum Löschen eines Profils ist kein Kennwort erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6436c-123">No password is required to delete a profile.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="6436c-124">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="6436c-124">MFCMAPI reference</span></span>

<span data-ttu-id="6436c-125">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="6436c-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6436c-126">**Datei**</span><span class="sxs-lookup"><span data-stu-id="6436c-126">**File**</span></span>|<span data-ttu-id="6436c-127">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="6436c-127">**Function**</span></span>|<span data-ttu-id="6436c-128">**Comment**</span><span class="sxs-lookup"><span data-stu-id="6436c-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6436c-129">MAPIProfileFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="6436c-129">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="6436c-130">HrRemoveProfile</span><span class="sxs-lookup"><span data-stu-id="6436c-130">HrRemoveProfile</span></span>  <br/> |<span data-ttu-id="6436c-131">MFCMAPI verwendet die **IProfAdmin::D-eleteprofile** -Methode, um das ausgewählte Profil zu löschen.</span><span class="sxs-lookup"><span data-stu-id="6436c-131">MFCMAPI uses the **IProfAdmin::DeleteProfile** method to delete the selected profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6436c-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6436c-132">See also</span></span>



[<span data-ttu-id="6436c-133">IMsgServiceAdmin::DeleteMsgService</span><span class="sxs-lookup"><span data-stu-id="6436c-133">IMsgServiceAdmin::DeleteMsgService</span></span>](imsgserviceadmin-deletemsgservice.md)
  
[<span data-ttu-id="6436c-134">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="6436c-134">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="6436c-135">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6436c-135">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


[<span data-ttu-id="6436c-136">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="6436c-136">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

