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
ms.openlocfilehash: 249d2dcf3a298abde85bdc53620680146d43c168
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792767"
---
# <a name="iprofadmindeleteprofile"></a><span data-ttu-id="5cae7-103">IProfAdmin::DeleteProfile</span><span class="sxs-lookup"><span data-stu-id="5cae7-103">IProfAdmin::DeleteProfile</span></span>

  
  
<span data-ttu-id="5cae7-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5cae7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5cae7-105">Löscht ein Profil.</span><span class="sxs-lookup"><span data-stu-id="5cae7-105">Deletes a profile.</span></span>
  
```cpp
HRESULT DeleteProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="5cae7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5cae7-106">Parameters</span></span>

 <span data-ttu-id="5cae7-107">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="5cae7-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="5cae7-108">[in] Ein Zeiger auf den Namen des Profils, das gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="5cae7-108">[in] A pointer to the name of the profile to be deleted.</span></span>
    
 <span data-ttu-id="5cae7-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5cae7-109">_ulFlags_</span></span>
  
> <span data-ttu-id="5cae7-110">[in] Immer NULL.</span><span class="sxs-lookup"><span data-stu-id="5cae7-110">[in] Always NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5cae7-111">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="5cae7-111">Return value</span></span>

<span data-ttu-id="5cae7-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="5cae7-112">S_OK</span></span> 
  
> <span data-ttu-id="5cae7-113">Das Profil wurde gelöscht.</span><span class="sxs-lookup"><span data-stu-id="5cae7-113">The profile was successfully deleted.</span></span>
    
<span data-ttu-id="5cae7-114">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="5cae7-114">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="5cae7-115">Das angegebene Profil ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="5cae7-115">The specified profile does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5cae7-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5cae7-116">Remarks</span></span>

<span data-ttu-id="5cae7-117">Die **IProfAdmin::DeleteProfile** -Methode löscht ein Profil.</span><span class="sxs-lookup"><span data-stu-id="5cae7-117">The **IProfAdmin::DeleteProfile** method deletes a profile.</span></span> <span data-ttu-id="5cae7-118">Wenn das zu löschende Profil verwendet wird, wenn **DeleteProfile** aufgerufen wird, **DeleteProfile** gibt S_OK zurück, jedoch wird das Profil nicht sofort gelöscht.</span><span class="sxs-lookup"><span data-stu-id="5cae7-118">If the profile to delete is in use when **DeleteProfile** is called, **DeleteProfile** returns S_OK but does not delete the profile immediately.</span></span> <span data-ttu-id="5cae7-119">Stattdessen **DeleteProfile** das Profil zum Löschen markiert und, nachdem es nicht mehr verwendet wird, wenn alle seine aktiven Sitzungen beendet haben, wird gelöscht.</span><span class="sxs-lookup"><span data-stu-id="5cae7-119">Instead, **DeleteProfile** marks the profile for deletion and deletes it after it is no longer being used, when all of its active sessions have ended.</span></span> 
  
<span data-ttu-id="5cae7-120">Die Funktion Eintrag für jeden Nachrichtendienst im Profil wird mit den im Parameter _UlContext_ festgelegten MSG_SERVICE_DELETE Wert aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="5cae7-120">The entry point function for each message service in the profile is called with the MSG_SERVICE_DELETE value set in the  _ulContext_ parameter.</span></span> <span data-ttu-id="5cae7-121">Zunächst die Funktion löscht den Dienst, und löscht dann den Dienst Profilabschnitt.</span><span class="sxs-lookup"><span data-stu-id="5cae7-121">First, the function deletes the service, and then it deletes the service's profile section.</span></span> <span data-ttu-id="5cae7-122">Die Nachricht Service Eintrag-Funktion wird nicht erneut aufgerufen, nachdem der Dienst gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="5cae7-122">The message service entry point function is not called again after the service has been deleted.</span></span> 
  
<span data-ttu-id="5cae7-123">Zum Löschen eines Profils ist kein Kennwort erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5cae7-123">No password is required to delete a profile.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5cae7-124">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="5cae7-124">MFCMAPI reference</span></span>

<span data-ttu-id="5cae7-125">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="5cae7-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5cae7-126">**Datei**</span><span class="sxs-lookup"><span data-stu-id="5cae7-126">**File**</span></span>|<span data-ttu-id="5cae7-127">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="5cae7-127">**Function**</span></span>|<span data-ttu-id="5cae7-128">**Comment**</span><span class="sxs-lookup"><span data-stu-id="5cae7-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5cae7-129">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="5cae7-129">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="5cae7-130">HrRemoveProfile</span><span class="sxs-lookup"><span data-stu-id="5cae7-130">HrRemoveProfile</span></span>  <br/> |<span data-ttu-id="5cae7-131">MFCMAPI (engl.) wird die **IProfAdmin::DeleteProfile** -Methode verwendet, um das ausgewählte Profil zu löschen.</span><span class="sxs-lookup"><span data-stu-id="5cae7-131">MFCMAPI uses the **IProfAdmin::DeleteProfile** method to delete the selected profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5cae7-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5cae7-132">See also</span></span>



[<span data-ttu-id="5cae7-133">IMsgServiceAdmin::DeleteMsgService</span><span class="sxs-lookup"><span data-stu-id="5cae7-133">IMsgServiceAdmin::DeleteMsgService</span></span>](imsgserviceadmin-deletemsgservice.md)
  
[<span data-ttu-id="5cae7-134">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="5cae7-134">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="5cae7-135">IProfAdmin: IUnknown</span><span class="sxs-lookup"><span data-stu-id="5cae7-135">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


[<span data-ttu-id="5cae7-136">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="5cae7-136">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

