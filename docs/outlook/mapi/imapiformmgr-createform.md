---
title: IMAPIFormMgrCreateForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.CreateForm
api_type:
- COM
ms.assetid: 7d4d50f8-3904-4e93-a535-ac7decceb1a3
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c6e18ee9f8ea1d7dc6592d576c5a1163db526639
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321665"
---
# <a name="imapiformmgrcreateform"></a><span data-ttu-id="38b73-103">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="38b73-103">IMAPIFormMgr::CreateForm</span></span>

  
  
<span data-ttu-id="38b73-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="38b73-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="38b73-105">Öffnet ein Formular zum Erstellen einer neuen Nachricht auf der Grundlage der Nachrichtenklasse des Formulars.</span><span class="sxs-lookup"><span data-stu-id="38b73-105">Opens a form to create a new message based on the form's message class.</span></span>
  
```cpp
HRESULT CreateForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  IMAPIFormInfo pfrminfoToActivate,
  REFIID refiidToAsk,
  LPVOID FAR * ppvObj
);
```

## <a name="parameters"></a><span data-ttu-id="38b73-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="38b73-106">Parameters</span></span>

 <span data-ttu-id="38b73-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="38b73-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="38b73-108">in Ein Handle für das übergeordnete Fenster für die Statusanzeige, die angezeigt wird, während das Formular geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="38b73-108">[in] A handle to the parent window for the progress indicator that is displayed while the form is opened.</span></span> <span data-ttu-id="38b73-109">Der _ulUIParam_ -Parameter wird ignoriert, es sei denn, das MAPI_DIALOG-Flag wird im _ulFlags_ -Parameter festgelegt.</span><span class="sxs-lookup"><span data-stu-id="38b73-109">The  _ulUIParam_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="38b73-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="38b73-110">_ulFlags_</span></span>
  
> <span data-ttu-id="38b73-111">in Eine Bitmaske von Flags, die steuert, wie das Formular geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="38b73-111">[in] A bitmask of flags that controls how the form is opened.</span></span> <span data-ttu-id="38b73-112">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="38b73-112">The following flag can be set:</span></span>
    
<span data-ttu-id="38b73-113">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="38b73-113">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="38b73-114">Zeigt eine Benutzeroberfläche an, um den Status anzugeben oder den Benutzer aufzufordern, weitere Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="38b73-114">Displays a user interface to provide status or prompt the user for more information.</span></span> <span data-ttu-id="38b73-115">Wenn dieses Flag nicht festgelegt ist, wird keine Benutzeroberfläche angezeigt.</span><span class="sxs-lookup"><span data-stu-id="38b73-115">If this flag is not set, no user interface is displayed.</span></span>
    
 <span data-ttu-id="38b73-116">_pfrminfoToActivate_</span><span class="sxs-lookup"><span data-stu-id="38b73-116">_pfrminfoToActivate_</span></span>
  
> <span data-ttu-id="38b73-117">in Ein Zeiger auf das Formular Informationsobjekt, das zum Öffnen des Formulars verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="38b73-117">[in] A pointer to the form information object that is used to open the form.</span></span>
    
 <span data-ttu-id="38b73-118">_refiidToAsk_</span><span class="sxs-lookup"><span data-stu-id="38b73-118">_refiidToAsk_</span></span>
  
> <span data-ttu-id="38b73-119">in Ein Zeiger auf die Schnittstellen-ID (IID) für die Schnittstelle für das erstellte Formularobjekt zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="38b73-119">[in] A pointer to the interface identifier (IID) for the interface to be returned for the form object that was created.</span></span> <span data-ttu-id="38b73-120">Der _refiidToAsk_ -Parameter darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="38b73-120">The  _refiidToAsk_ parameter must not be NULL.</span></span> 
    
 <span data-ttu-id="38b73-121">_ppvObj_</span><span class="sxs-lookup"><span data-stu-id="38b73-121">_ppvObj_</span></span>
  
> <span data-ttu-id="38b73-122">Out Ein Zeiger auf einen Zeiger auf die zurückgegebene Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="38b73-122">[out] A pointer to a pointer to the returned interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="38b73-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="38b73-123">Return value</span></span>

<span data-ttu-id="38b73-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="38b73-124">S_OK</span></span> 
  
> <span data-ttu-id="38b73-125">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="38b73-125">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="38b73-126">MAPI_E_NO_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="38b73-126">MAPI_E_NO_INTERFACE</span></span> 
  
> <span data-ttu-id="38b73-127">Die angeforderte Schnittstelle wird vom Form-Objekt nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="38b73-127">The requested interface is not supported by the form object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="38b73-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="38b73-128">Remarks</span></span>

<span data-ttu-id="38b73-129">Formular Betrachter rufen die **IMAPIFormMgr:: CreateForm** -Methode auf, um ein Formular zum Erstellen einer neuen Nachricht basierend auf der Nachrichtenklasse des Formulars zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="38b73-129">Form viewers call the **IMAPIFormMgr::CreateForm** method to open a form to create a new message based on the form's message class.</span></span> <span data-ttu-id="38b73-130">**CreateForm** öffnet das Formular, indem eine Instanz des Formular Servers für dieses Formular erstellt wird, wie im angegebenen Formular Informationsobjekt beschrieben.</span><span class="sxs-lookup"><span data-stu-id="38b73-130">**CreateForm** opens the form by creating an instance of the form server for that form as described in the given form information object.</span></span> <span data-ttu-id="38b73-131">Bei Bedarf ruft **CreateForm** die [IMAPIFormMgr::P repareform](imapiformmgr-prepareform.md) -Methode auf, um den Formularserver Code auf den Datenträger des Benutzers herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="38b73-131">If required, **CreateForm** calls the [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) method to download the form server code to the user's disk.</span></span> 
  
<span data-ttu-id="38b73-132">Der Parameter _pfrminfoToActivate_ muss auf ein Formular Informationsobjekt zeigen, das korrekt aufgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="38b73-132">The  _pfrminfoToActivate_ parameter must point to a form information object that has been correctly resolved.</span></span> 
  
<span data-ttu-id="38b73-133">Nachdem das Formular geöffnet wurde, muss der aufrufende Formular Betrachter eine Nachricht mithilfe der [IPersistMessage](ipersistmessageiunknown.md) -Schnittstelle einrichten und optional einen Ansichtskontext für das Formular einrichten.</span><span class="sxs-lookup"><span data-stu-id="38b73-133">After the form has been opened, the calling form viewer must set up a message by using the [IPersistMessage](ipersistmessageiunknown.md) interface and can optionally set up a view context for the form.</span></span> <span data-ttu-id="38b73-134">Weitere Informationen finden Sie unter [Starten eines Formular Servers](launching-a-form-server.md).</span><span class="sxs-lookup"><span data-stu-id="38b73-134">For more information, see [Launching a Form Server](launching-a-form-server.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="38b73-135">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="38b73-135">MFCMAPI reference</span></span>

<span data-ttu-id="38b73-136">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="38b73-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="38b73-137">**Datei**</span><span class="sxs-lookup"><span data-stu-id="38b73-137">**File**</span></span>|<span data-ttu-id="38b73-138">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="38b73-138">**Function**</span></span>|<span data-ttu-id="38b73-139">**Comment**</span><span class="sxs-lookup"><span data-stu-id="38b73-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="38b73-140">MAPIFormFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="38b73-140">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="38b73-141">CreateAndDisplayNewMailInFolder</span><span class="sxs-lookup"><span data-stu-id="38b73-141">CreateAndDisplayNewMailInFolder</span></span>  <br/> |<span data-ttu-id="38b73-142">MFCMAPI verwendet die **IMAPIFormMgr:: CreateForm** -Methode, um ein Formular zu erstellen, bevor es angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="38b73-142">MFCMAPI uses the **IMAPIFormMgr::CreateForm** method to create a form before displaying it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="38b73-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="38b73-143">See also</span></span>



[<span data-ttu-id="38b73-144">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="38b73-144">IMAPIFormMgr::PrepareForm</span></span>](imapiformmgr-prepareform.md)
  
[<span data-ttu-id="38b73-145">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="38b73-145">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
  
[<span data-ttu-id="38b73-146">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="38b73-146">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="38b73-147">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="38b73-147">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="38b73-148">Starten eines Formular Servers</span><span class="sxs-lookup"><span data-stu-id="38b73-148">Launching a Form Server</span></span>](launching-a-form-server.md)

