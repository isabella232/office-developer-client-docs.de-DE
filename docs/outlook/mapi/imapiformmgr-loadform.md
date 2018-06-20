---
title: IMAPIFormMgrLoadForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.LoadForm
api_type:
- COM
ms.assetid: 5ca500c3-c737-45a5-b0fc-473b75c1d68d
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 1f3a876269868c30df48e0a0b62036cfdc199955
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792172"
---
# <a name="imapiformmgrloadform"></a><span data-ttu-id="2317e-103">IMAPIFormMgr::LoadForm</span><span class="sxs-lookup"><span data-stu-id="2317e-103">IMAPIFormMgr::LoadForm</span></span>

  
  
<span data-ttu-id="2317e-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2317e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2317e-105">Startet ein Formular, um eine vorhandene Nachricht zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="2317e-105">Starts a form to open an existing message.</span></span>
  
```cpp
HRESULT LoadForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR lpszMessageClass,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags,
  LPMAPIFOLDER pFolderFocus,
  LPMAPIMESSAGESITE pMessageSite,
  LPMESSAGE pmsg,
  LPMAPIVIEWCONTEXT pViewContext,
  REFIID riid,
  LPVOID FAR * ppvObj
);
```

## <a name="parameters"></a><span data-ttu-id="2317e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2317e-106">Parameters</span></span>

 <span data-ttu-id="2317e-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="2317e-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="2317e-108">[in] Ein Handle für das übergeordnete Fenster der Statusanzeige, die angezeigt wird, während das Formular geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="2317e-108">[in] A handle to the parent window of the progress indicator that is displayed while the form is opened.</span></span> <span data-ttu-id="2317e-109">Der Parameter _UlUIParam_ wird ignoriert, es sei denn, das Flag MAPI_DIALOG im _UlFlags_ -Parameter festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="2317e-109">The  _ulUIParam_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="2317e-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2317e-110">_ulFlags_</span></span>
  
> <span data-ttu-id="2317e-111">[in] Eine Bitmaske aus Flags, die steuert, wie das Formular geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="2317e-111">[in] A bitmask of flags that controls how the form is opened.</span></span> <span data-ttu-id="2317e-112">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="2317e-112">The following flags can be set:</span></span>
    
<span data-ttu-id="2317e-113">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="2317e-113">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="2317e-114">Zeigt eine Benutzeroberfläche zum Bereitstellen von Status oder auffordern, Weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="2317e-114">Displays a user interface to provide status or prompt the user for more information.</span></span> <span data-ttu-id="2317e-115">Wenn dieses Flag nicht festgelegt ist, wird keine Benutzeroberfläche angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2317e-115">If this flag is not set, no user interface is displayed.</span></span>
    
<span data-ttu-id="2317e-116">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="2317e-116">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="2317e-117">Nur Nachricht Klasse Zeichenfolgen, die eine genaue Übereinstimmung sollten aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="2317e-117">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="2317e-118">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="2317e-118">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="2317e-119">[in] Ein Zeiger auf eine Zeichenfolge, die den Namen die Nachrichtenklasse der Nachricht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="2317e-119">[in] A pointer to a string that names the message class of the message to be loaded.</span></span> <span data-ttu-id="2317e-120">Wenn NULL in der _LpszMessageClass_ -Parameter übergeben wird, wird die Nachrichtenklasse aus der Nachricht auf das durch den Parameter _Pmsg_ bestimmt.</span><span class="sxs-lookup"><span data-stu-id="2317e-120">If NULL is passed in the  _lpszMessageClass_ parameter, the message class is determined from the message pointed to by the  _pmsg_ parameter.</span></span> 
    
 <span data-ttu-id="2317e-121">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="2317e-121">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="2317e-122">[in] Eine Bitmaske vom Client definiert oder vom Anbieter definiertes Flags, kopiert aus der **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))-Eigenschaft der Nachricht bereitstellt, die Informationen zum Status der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="2317e-122">[in] A bitmask of client-defined or provider-defined flags copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of the message that provides information about the state of the message.</span></span> <span data-ttu-id="2317e-123">Der Parameter _UlMessageStatus_ muss festgelegt werden, wenn _LpszMessageClass_ ungleich NULL ist. Andernfalls wird _UlMessageStatus_ ignoriert.</span><span class="sxs-lookup"><span data-stu-id="2317e-123">The  _ulMessageStatus_ parameter must be set if  _lpszMessageClass_ is non-NULL; otherwise,  _ulMessageStatus_ is ignored.</span></span> 
    
 <span data-ttu-id="2317e-124">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="2317e-124">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="2317e-125">[in] Ein Zeiger auf eine Bitmaske aus Flags, die von der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft der Nachricht, die angibt, den aktuellen Status der Nachricht kopiert.</span><span class="sxs-lookup"><span data-stu-id="2317e-125">[in] A pointer to a bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the message that indicates the current state of the message.</span></span> <span data-ttu-id="2317e-126">Der Parameter _UlMessageFlags_ muss festgelegt werden, wenn _LpszMessageClass_ ungleich NULL ist. Andernfalls wird _UlMessageFlags_ ignoriert.</span><span class="sxs-lookup"><span data-stu-id="2317e-126">The  _ulMessageFlags_ parameter must be set if  _lpszMessageClass_ is non-NULL; otherwise,  _ulMessageFlags_ is ignored.</span></span> 
    
 <span data-ttu-id="2317e-127">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="2317e-127">_pFolderFocus_</span></span>
  
> <span data-ttu-id="2317e-128">[in] Ein Zeiger auf den Ordner, der die Nachricht direkt enthält.</span><span class="sxs-lookup"><span data-stu-id="2317e-128">[in] A pointer to the folder that directly contains the message.</span></span> <span data-ttu-id="2317e-129">Der Parameter _pFolderFocus_ kann NULL sein, wenn eine solche ein Ordner nicht vorhanden ist (z. B., wenn die Nachricht in eine andere Nachricht eingebettet ist).</span><span class="sxs-lookup"><span data-stu-id="2317e-129">The  _pFolderFocus_ parameter can be NULL if such a folder does not exist (for example, if the message is embedded in another message).</span></span> 
    
 <span data-ttu-id="2317e-130">_pMessageSite_</span><span class="sxs-lookup"><span data-stu-id="2317e-130">_pMessageSite_</span></span>
  
> <span data-ttu-id="2317e-131">[in] Ein Zeiger auf die Website Nachricht der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="2317e-131">[in] A pointer to the message site of the message.</span></span>
    
 <span data-ttu-id="2317e-132">_pmsg_</span><span class="sxs-lookup"><span data-stu-id="2317e-132">_pmsg_</span></span>
  
> <span data-ttu-id="2317e-133">[in] Ein Zeiger auf die Nachricht.</span><span class="sxs-lookup"><span data-stu-id="2317e-133">[in] A pointer to the message.</span></span>
    
 <span data-ttu-id="2317e-134">_pViewContext_</span><span class="sxs-lookup"><span data-stu-id="2317e-134">_pViewContext_</span></span>
  
> <span data-ttu-id="2317e-135">[in] Ein Zeiger auf den Ansichtskontext für die Nachricht.</span><span class="sxs-lookup"><span data-stu-id="2317e-135">[in] A pointer to the view context for the message.</span></span> <span data-ttu-id="2317e-136">Der Parameter _pViewContext_ kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="2317e-136">The  _pViewContext_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="2317e-137">_riid_</span><span class="sxs-lookup"><span data-stu-id="2317e-137">_riid_</span></span>
  
> <span data-ttu-id="2317e-138">[in] Die Schnittstelle Identifier (IID) der Schnittstelle für das zurückgegebene Form-Objekt verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2317e-138">[in] The interface identifier (IID) of the interface to be used for the returned form object.</span></span> <span data-ttu-id="2317e-139">Der Parameter _Riid_ darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="2317e-139">The  _riid_ parameter must not be NULL.</span></span> 
    
 <span data-ttu-id="2317e-140">_ppvObj_</span><span class="sxs-lookup"><span data-stu-id="2317e-140">_ppvObj_</span></span>
  
> <span data-ttu-id="2317e-141">[out] Ein Zeiger auf einen Zeiger auf die zurückgegebene Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="2317e-141">[out] A pointer to a pointer to the returned interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2317e-142">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="2317e-142">Return value</span></span>

<span data-ttu-id="2317e-143">S_OK</span><span class="sxs-lookup"><span data-stu-id="2317e-143">S_OK</span></span> 
  
> <span data-ttu-id="2317e-144">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="2317e-144">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="2317e-145">MAPI_E_NO_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="2317e-145">MAPI_E_NO_INTERFACE</span></span> 
  
> <span data-ttu-id="2317e-146">Das Formular unterstützt die angeforderte Schnittstelle nicht.</span><span class="sxs-lookup"><span data-stu-id="2317e-146">The form does not support the requested interface.</span></span>
    
<span data-ttu-id="2317e-147">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="2317e-147">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="2317e-148">Die Nachrichtenklasse übergebenen _LpszMessageClass_ stimmt nicht mit die Nachrichtenklasse für jedes Formular in der Formularbibliothek überein.</span><span class="sxs-lookup"><span data-stu-id="2317e-148">The message class passed in  _lpszMessageClass_ does not match the message class for any form in the form library.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="2317e-149">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2317e-149">Remarks</span></span>

<span data-ttu-id="2317e-150">Formular Viewer rufen Sie die **IMAPIFormMgr::LoadForm** -Methode zum Öffnen eines Formulars für eine vorhandene Nachricht.</span><span class="sxs-lookup"><span data-stu-id="2317e-150">Form viewers call the **IMAPIFormMgr::LoadForm** method to open a form for an existing message.</span></span> <span data-ttu-id="2317e-151">**LoadForm** Öffnet das Form-Objekt, wird die Nachricht in das Form-Objekt geladen, richtet die entsprechenden Ansichtskontext bei Bedarf und die angeforderte Schnittstelle für das Form-Objekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="2317e-151">**LoadForm** opens the form object, loads the message into the form object, sets up the appropriate view context, if necessary, and returns the requested interface for the form object.</span></span> 
  
<span data-ttu-id="2317e-152">Der _pFolderFocus_ -Parameter verweist auf den Ordner, der die Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="2317e-152">The  _pFolderFocus_ parameter points to the folder that contains the message.</span></span> <span data-ttu-id="2317e-153">Wenn die Nachricht in einer anderen Nachricht eingebettet ist, sollte _pFolderFocus_ NULL sein.</span><span class="sxs-lookup"><span data-stu-id="2317e-153">If the message is embedded in another message,  _pFolderFocus_ should be NULL.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="2317e-154">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="2317e-154">Notes to implementers</span></span>

<span data-ttu-id="2317e-155">Wenn NULL in _LpszMessageClass_übergeben wird, erhält die Implementierung der Nachricht Nachrichtenklasse, Status und Flags aus der Nachricht **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), **PR_MSG_STATUS** und **PR_MESSAGE_FLAGS **Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2317e-155">If NULL is passed in  _lpszMessageClass_, the implementation obtains the message's message class, status, and flags from the message's **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), **PR_MSG_STATUS** and **PR_MESSAGE_FLAGS** properties.</span></span> <span data-ttu-id="2317e-156">Wenn eine Meldungszeichenfolge-Klasse in _LpszMessageClass_bereitgestellt wird, muss die Implementierung der Werte in _UlMessageStatus_ und _UlMessageFlags_verwenden.</span><span class="sxs-lookup"><span data-stu-id="2317e-156">If a message class string is provided in  _lpszMessageClass_, the implementation must use the values in  _ulMessageStatus_ and  _ulMessageFlags_.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="2317e-157">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="2317e-157">MFCMAPI reference</span></span>

<span data-ttu-id="2317e-158">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="2317e-158">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2317e-159">**Datei**</span><span class="sxs-lookup"><span data-stu-id="2317e-159">**File**</span></span>|<span data-ttu-id="2317e-160">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="2317e-160">**Function**</span></span>|<span data-ttu-id="2317e-161">**Comment**</span><span class="sxs-lookup"><span data-stu-id="2317e-161">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2317e-162">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="2317e-162">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="2317e-163">OpenMessageNonModal</span><span class="sxs-lookup"><span data-stu-id="2317e-163">OpenMessageNonModal</span></span>  <br/> |<span data-ttu-id="2317e-164">MFCMAPI (engl.) verwendet die **IMAPIFormMgr::LoadForm** -Methode, um ein Formular zu laden, bevor es angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2317e-164">MFCMAPI uses the **IMAPIFormMgr::LoadForm** method to load a form before displaying it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2317e-165">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2317e-165">See also</span></span>



[<span data-ttu-id="2317e-166">Kanonische-Eigenschaft PidTagMessageClass</span><span class="sxs-lookup"><span data-stu-id="2317e-166">PidTagMessageClass Canonical Property</span></span>](pidtagmessageclass-canonical-property.md)
  
[<span data-ttu-id="2317e-167">Kanonische PidTagMessageFlags-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2317e-167">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="2317e-168">Kanonische PidTagMessageStatus-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2317e-168">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="2317e-169">IMAPIFormMgr: IUnknown</span><span class="sxs-lookup"><span data-stu-id="2317e-169">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="2317e-170">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="2317e-170">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

