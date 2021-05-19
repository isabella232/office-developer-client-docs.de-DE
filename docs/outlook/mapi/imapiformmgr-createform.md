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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c6e18ee9f8ea1d7dc6592d576c5a1163db526639
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419849"
---
# <a name="imapiformmgrcreateform"></a><span data-ttu-id="104dc-103">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="104dc-103">IMAPIFormMgr::CreateForm</span></span>

  
  
<span data-ttu-id="104dc-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="104dc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="104dc-105">Öffnet ein Formular, um eine neue Nachricht basierend auf der Nachrichtenklasse des Formulars zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="104dc-105">Opens a form to create a new message based on the form's message class.</span></span>
  
```cpp
HRESULT CreateForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  IMAPIFormInfo pfrminfoToActivate,
  REFIID refiidToAsk,
  LPVOID FAR * ppvObj
);
```

## <a name="parameters"></a><span data-ttu-id="104dc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="104dc-106">Parameters</span></span>

 <span data-ttu-id="104dc-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="104dc-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="104dc-108">[in] Ein Handle zum übergeordneten Fenster für die Statusanzeige, die beim Öffnen des Formulars angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="104dc-108">[in] A handle to the parent window for the progress indicator that is displayed while the form is opened.</span></span> <span data-ttu-id="104dc-109">Der  _ulUIParam-Parameter_ wird ignoriert, es sei denn, das MAPI_DIALOG wird im  _ulFlags-Parameter_ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="104dc-109">The  _ulUIParam_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="104dc-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="104dc-110">_ulFlags_</span></span>
  
> <span data-ttu-id="104dc-111">[in] Eine Bitmaske mit Flags, die steuert, wie das Formular geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="104dc-111">[in] A bitmask of flags that controls how the form is opened.</span></span> <span data-ttu-id="104dc-112">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="104dc-112">The following flag can be set:</span></span>
    
<span data-ttu-id="104dc-113">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="104dc-113">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="104dc-114">Zeigt eine Benutzeroberfläche an, um den Status zur Verfügung zu stellen, oder fordert den Benutzer auf, weitere Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="104dc-114">Displays a user interface to provide status or prompt the user for more information.</span></span> <span data-ttu-id="104dc-115">Wenn dieses Kennzeichen nicht festgelegt ist, wird keine Benutzeroberfläche angezeigt.</span><span class="sxs-lookup"><span data-stu-id="104dc-115">If this flag is not set, no user interface is displayed.</span></span>
    
 <span data-ttu-id="104dc-116">_pfrminfoToActivate_</span><span class="sxs-lookup"><span data-stu-id="104dc-116">_pfrminfoToActivate_</span></span>
  
> <span data-ttu-id="104dc-117">[in] Ein Zeiger auf das Formularinformationsobjekt, das zum Öffnen des Formulars verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="104dc-117">[in] A pointer to the form information object that is used to open the form.</span></span>
    
 <span data-ttu-id="104dc-118">_refiidToAsk_</span><span class="sxs-lookup"><span data-stu-id="104dc-118">_refiidToAsk_</span></span>
  
> <span data-ttu-id="104dc-119">[in] Ein Zeiger auf die Schnittstellen-ID (Interface Identifier, IID) für die Schnittstelle, die für das erstellte Formularobjekt zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="104dc-119">[in] A pointer to the interface identifier (IID) for the interface to be returned for the form object that was created.</span></span> <span data-ttu-id="104dc-120">Der  _refiidToAsk-Parameter_ darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="104dc-120">The  _refiidToAsk_ parameter must not be NULL.</span></span> 
    
 <span data-ttu-id="104dc-121">_ppvObj_</span><span class="sxs-lookup"><span data-stu-id="104dc-121">_ppvObj_</span></span>
  
> <span data-ttu-id="104dc-122">[out] Ein Zeiger auf einen Zeiger auf die zurückgegebene Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="104dc-122">[out] A pointer to a pointer to the returned interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="104dc-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="104dc-123">Return value</span></span>

<span data-ttu-id="104dc-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="104dc-124">S_OK</span></span> 
  
> <span data-ttu-id="104dc-125">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="104dc-125">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="104dc-126">MAPI_E_NO_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="104dc-126">MAPI_E_NO_INTERFACE</span></span> 
  
> <span data-ttu-id="104dc-127">Die angeforderte Schnittstelle wird vom Formularobjekt nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="104dc-127">The requested interface is not supported by the form object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="104dc-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="104dc-128">Remarks</span></span>

<span data-ttu-id="104dc-129">Formularbetrachter rufen die **IMAPIFormMgr::CreateForm-Methode** auf, um ein Formular zu öffnen, um eine neue Nachricht basierend auf der Nachrichtenklasse des Formulars zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="104dc-129">Form viewers call the **IMAPIFormMgr::CreateForm** method to open a form to create a new message based on the form's message class.</span></span> <span data-ttu-id="104dc-130">**CreateForm** öffnet das Formular, indem eine Instanz des Formularservers für dieses Formular erstellt wird, wie im angegebenen Formularinformationsobjekt beschrieben.</span><span class="sxs-lookup"><span data-stu-id="104dc-130">**CreateForm** opens the form by creating an instance of the form server for that form as described in the given form information object.</span></span> <span data-ttu-id="104dc-131">Bei Bedarf ruft **CreateForm** die [IMAPIFormMgr::P repareForm-Methode](imapiformmgr-prepareform.md) auf, um den Formularservercode auf den Datenträger des Benutzers herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="104dc-131">If required, **CreateForm** calls the [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) method to download the form server code to the user's disk.</span></span> 
  
<span data-ttu-id="104dc-132">Der  _pfrminfoToActivate-Parameter_ muss auf ein Formularinformationsobjekt verweisen, das ordnungsgemäß aufgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="104dc-132">The  _pfrminfoToActivate_ parameter must point to a form information object that has been correctly resolved.</span></span> 
  
<span data-ttu-id="104dc-133">Nachdem das Formular geöffnet wurde, muss die aufrufende Formularanzeige eine Nachricht mithilfe der [IPersistMessage-Schnittstelle](ipersistmessageiunknown.md) einrichten und kann optional einen Ansichtskontext für das Formular einrichten.</span><span class="sxs-lookup"><span data-stu-id="104dc-133">After the form has been opened, the calling form viewer must set up a message by using the [IPersistMessage](ipersistmessageiunknown.md) interface and can optionally set up a view context for the form.</span></span> <span data-ttu-id="104dc-134">Weitere Informationen finden Sie unter [Starten eines Formularservers.](launching-a-form-server.md)</span><span class="sxs-lookup"><span data-stu-id="104dc-134">For more information, see [Launching a Form Server](launching-a-form-server.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="104dc-135">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="104dc-135">MFCMAPI reference</span></span>

<span data-ttu-id="104dc-136">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="104dc-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="104dc-137">**Datei**</span><span class="sxs-lookup"><span data-stu-id="104dc-137">**File**</span></span>|<span data-ttu-id="104dc-138">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="104dc-138">**Function**</span></span>|<span data-ttu-id="104dc-139">**Comment**</span><span class="sxs-lookup"><span data-stu-id="104dc-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="104dc-140">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="104dc-140">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="104dc-141">CreateAndDisplayNewMailInFolder</span><span class="sxs-lookup"><span data-stu-id="104dc-141">CreateAndDisplayNewMailInFolder</span></span>  <br/> |<span data-ttu-id="104dc-142">MFCMAPI verwendet die **IMAPIFormMgr::CreateForm-Methode,** um ein Formular zu erstellen, bevor es angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="104dc-142">MFCMAPI uses the **IMAPIFormMgr::CreateForm** method to create a form before displaying it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="104dc-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="104dc-143">See also</span></span>



[<span data-ttu-id="104dc-144">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="104dc-144">IMAPIFormMgr::PrepareForm</span></span>](imapiformmgr-prepareform.md)
  
[<span data-ttu-id="104dc-145">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="104dc-145">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
  
[<span data-ttu-id="104dc-146">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="104dc-146">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="104dc-147">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="104dc-147">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="104dc-148">Starten eines Formularservers</span><span class="sxs-lookup"><span data-stu-id="104dc-148">Launching a Form Server</span></span>](launching-a-form-server.md)

