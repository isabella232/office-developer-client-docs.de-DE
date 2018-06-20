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
ms.openlocfilehash: ed3f793e4353cf78949a9df3a17dd3997a573f58
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792175"
---
# <a name="imapiformmgrcreateform"></a><span data-ttu-id="1072d-103">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="1072d-103">IMAPIFormMgr::CreateForm</span></span>

  
  
<span data-ttu-id="1072d-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1072d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1072d-105">Öffnet ein Formular zum Erstellen einer neuen Nachricht basierend auf der Nachrichtenklasse des Formulars.</span><span class="sxs-lookup"><span data-stu-id="1072d-105">Opens a form to create a new message based on the form's message class.</span></span>
  
```cpp
HRESULT CreateForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  IMAPIFormInfo pfrminfoToActivate,
  REFIID refiidToAsk,
  LPVOID FAR * ppvObj
);
```

## <a name="parameters"></a><span data-ttu-id="1072d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1072d-106">Parameters</span></span>

 <span data-ttu-id="1072d-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="1072d-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="1072d-108">[in] Ein Handle für das übergeordnete Fenster für die Statusanzeige, die angezeigt wird, während das Formular geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="1072d-108">[in] A handle to the parent window for the progress indicator that is displayed while the form is opened.</span></span> <span data-ttu-id="1072d-109">Der Parameter _UlUIParam_ wird ignoriert, es sei denn, das Flag MAPI_DIALOG im _UlFlags_ -Parameter festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1072d-109">The  _ulUIParam_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="1072d-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1072d-110">_ulFlags_</span></span>
  
> <span data-ttu-id="1072d-111">[in] Eine Bitmaske aus Flags, die steuert, wie das Formular geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="1072d-111">[in] A bitmask of flags that controls how the form is opened.</span></span> <span data-ttu-id="1072d-112">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="1072d-112">The following flag can be set:</span></span>
    
<span data-ttu-id="1072d-113">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="1072d-113">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="1072d-114">Zeigt eine Benutzeroberfläche zum Bereitstellen von Status oder auffordern, Weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="1072d-114">Displays a user interface to provide status or prompt the user for more information.</span></span> <span data-ttu-id="1072d-115">Wenn dieses Flag nicht festgelegt ist, wird keine Benutzeroberfläche angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1072d-115">If this flag is not set, no user interface is displayed.</span></span>
    
 <span data-ttu-id="1072d-116">_pfrminfoToActivate_</span><span class="sxs-lookup"><span data-stu-id="1072d-116">_pfrminfoToActivate_</span></span>
  
> <span data-ttu-id="1072d-117">[in] Ein Zeiger auf das Formular Informationen-Objekt, das zum Öffnen des Formulars verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1072d-117">[in] A pointer to the form information object that is used to open the form.</span></span>
    
 <span data-ttu-id="1072d-118">_refiidToAsk_</span><span class="sxs-lookup"><span data-stu-id="1072d-118">_refiidToAsk_</span></span>
  
> <span data-ttu-id="1072d-119">[in] Ein Zeiger auf die Schnittstelle-ID (IID) für die Schnittstelle für das Form-Objekt zurückgegeben werden soll, die erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="1072d-119">[in] A pointer to the interface identifier (IID) for the interface to be returned for the form object that was created.</span></span> <span data-ttu-id="1072d-120">Der Parameter _RefiidToAsk_ darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="1072d-120">The  _refiidToAsk_ parameter must not be NULL.</span></span> 
    
 <span data-ttu-id="1072d-121">_ppvObj_</span><span class="sxs-lookup"><span data-stu-id="1072d-121">_ppvObj_</span></span>
  
> <span data-ttu-id="1072d-122">[out] Ein Zeiger auf einen Zeiger auf die zurückgegebene Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="1072d-122">[out] A pointer to a pointer to the returned interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1072d-123">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="1072d-123">Return value</span></span>

<span data-ttu-id="1072d-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="1072d-124">S_OK</span></span> 
  
> <span data-ttu-id="1072d-125">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="1072d-125">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="1072d-126">MAPI_E_NO_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="1072d-126">MAPI_E_NO_INTERFACE</span></span> 
  
> <span data-ttu-id="1072d-127">Die angeforderte Schnittstelle wird von der Form-Objekt nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1072d-127">The requested interface is not supported by the form object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1072d-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1072d-128">Remarks</span></span>

<span data-ttu-id="1072d-129">Formular Viewer rufen Sie die **IMAPIFormMgr::CreateForm** -Methode zum Öffnen eines Formulars zum Erstellen einer neuen Nachricht basierend auf der Nachrichtenklasse des Formulars.</span><span class="sxs-lookup"><span data-stu-id="1072d-129">Form viewers call the **IMAPIFormMgr::CreateForm** method to open a form to create a new message based on the form's message class.</span></span> <span data-ttu-id="1072d-130">**CreateForm** Öffnet das Formular durch das Erstellen einer Instanz des Formular-Servers für das Formular in der angegebenen Form Informationen-Objekt beschrieben.</span><span class="sxs-lookup"><span data-stu-id="1072d-130">**CreateForm** opens the form by creating an instance of the form server for that form as described in the given form information object.</span></span> <span data-ttu-id="1072d-131">Falls erforderlich, ruft **CreateForm** die [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) -Methode, um die Formularcode Server auf der Festplatte des Benutzers herunterladen.</span><span class="sxs-lookup"><span data-stu-id="1072d-131">If required, **CreateForm** calls the [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) method to download the form server code to the user's disk.</span></span> 
  
<span data-ttu-id="1072d-132">Der Parameter _PfrminfoToActivate_ muss auf ein Form-Informationsobjekt zeigen, der ordnungsgemäß aufgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="1072d-132">The  _pfrminfoToActivate_ parameter must point to a form information object that has been correctly resolved.</span></span> 
  
<span data-ttu-id="1072d-133">Nach dem das Formular geöffnet wurde, der aufrufende Formular-Viewer muss eingerichtet, eine Meldung über die Benutzeroberfläche [IPersistMessage](ipersistmessageiunknown.md) und optional ein Ansichtskontext für das Formular einrichten kann.</span><span class="sxs-lookup"><span data-stu-id="1072d-133">After the form has been opened, the calling form viewer must set up a message by using the [IPersistMessage](ipersistmessageiunknown.md) interface and can optionally set up a view context for the form.</span></span> <span data-ttu-id="1072d-134">Weitere Informationen finden Sie unter [Starten einer Form Server](launching-a-form-server.md).</span><span class="sxs-lookup"><span data-stu-id="1072d-134">For more information, see [Launching a Form Server](launching-a-form-server.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1072d-135">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="1072d-135">MFCMAPI reference</span></span>

<span data-ttu-id="1072d-136">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="1072d-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1072d-137">**Datei**</span><span class="sxs-lookup"><span data-stu-id="1072d-137">**File**</span></span>|<span data-ttu-id="1072d-138">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="1072d-138">**Function**</span></span>|<span data-ttu-id="1072d-139">**Comment**</span><span class="sxs-lookup"><span data-stu-id="1072d-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1072d-140">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="1072d-140">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="1072d-141">CreateAndDisplayNewMailInFolder</span><span class="sxs-lookup"><span data-stu-id="1072d-141">CreateAndDisplayNewMailInFolder</span></span>  <br/> |<span data-ttu-id="1072d-142">MFCMAPI (engl.) verwendet die **IMAPIFormMgr::CreateForm** -Methode zum Erstellen eines Formulars vor dem anzeigen.</span><span class="sxs-lookup"><span data-stu-id="1072d-142">MFCMAPI uses the **IMAPIFormMgr::CreateForm** method to create a form before displaying it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1072d-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1072d-143">See also</span></span>



[<span data-ttu-id="1072d-144">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="1072d-144">IMAPIFormMgr::PrepareForm</span></span>](imapiformmgr-prepareform.md)
  
[<span data-ttu-id="1072d-145">IPersistMessage: IUnknown</span><span class="sxs-lookup"><span data-stu-id="1072d-145">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
  
[<span data-ttu-id="1072d-146">IMAPIFormMgr: IUnknown</span><span class="sxs-lookup"><span data-stu-id="1072d-146">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="1072d-147">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="1072d-147">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="1072d-148">Starten eines Formulars-Servers</span><span class="sxs-lookup"><span data-stu-id="1072d-148">Launching a Form Server</span></span>](launching-a-form-server.md)

