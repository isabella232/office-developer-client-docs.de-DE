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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7e445646477ad1fc56b41141b541358d9b9f9616
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418785"
---
# <a name="imapiformmgrloadform"></a><span data-ttu-id="357cc-103">IMAPIFormMgr::LoadForm</span><span class="sxs-lookup"><span data-stu-id="357cc-103">IMAPIFormMgr::LoadForm</span></span>

  
  
<span data-ttu-id="357cc-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="357cc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="357cc-105">Startet ein Formular zum Öffnen einer vorhandenen Nachricht.</span><span class="sxs-lookup"><span data-stu-id="357cc-105">Starts a form to open an existing message.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="357cc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="357cc-106">Parameters</span></span>

 <span data-ttu-id="357cc-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="357cc-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="357cc-108">[in] Ein Handle zum übergeordneten Fenster des Statusindikators, das beim Öffnen des Formulars angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="357cc-108">[in] A handle to the parent window of the progress indicator that is displayed while the form is opened.</span></span> <span data-ttu-id="357cc-109">Der  _ulUIParam-Parameter_ wird ignoriert, es sei denn, das MAPI_DIALOG wird im  _ulFlags-Parameter_ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="357cc-109">The  _ulUIParam_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="357cc-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="357cc-110">_ulFlags_</span></span>
  
> <span data-ttu-id="357cc-111">[in] Eine Bitmaske mit Flags, die steuert, wie das Formular geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="357cc-111">[in] A bitmask of flags that controls how the form is opened.</span></span> <span data-ttu-id="357cc-112">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="357cc-112">The following flags can be set:</span></span>
    
<span data-ttu-id="357cc-113">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="357cc-113">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="357cc-114">Zeigt eine Benutzeroberfläche an, um den Status zur Verfügung zu stellen, oder fordert den Benutzer auf, weitere Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="357cc-114">Displays a user interface to provide status or prompt the user for more information.</span></span> <span data-ttu-id="357cc-115">Wenn dieses Kennzeichen nicht festgelegt ist, wird keine Benutzeroberfläche angezeigt.</span><span class="sxs-lookup"><span data-stu-id="357cc-115">If this flag is not set, no user interface is displayed.</span></span>
    
<span data-ttu-id="357cc-116">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="357cc-116">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="357cc-117">Es sollten nur Nachrichtenklassenzeichenfolgen aufgelöst werden, die eine genaue Übereinstimmung sind.</span><span class="sxs-lookup"><span data-stu-id="357cc-117">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="357cc-118">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="357cc-118">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="357cc-119">[in] Ein Zeiger auf eine Zeichenfolge, die die Nachrichtenklasse der zu ladenden Nachricht benennt.</span><span class="sxs-lookup"><span data-stu-id="357cc-119">[in] A pointer to a string that names the message class of the message to be loaded.</span></span> <span data-ttu-id="357cc-120">Wenn NULL im  _lpszMessageClass-Parameter_ übergeben wird, wird die Nachrichtenklasse anhand der Nachricht bestimmt, auf die der  _pmsg-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="357cc-120">If NULL is passed in the  _lpszMessageClass_ parameter, the message class is determined from the message pointed to by the  _pmsg_ parameter.</span></span> 
    
 <span data-ttu-id="357cc-121">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="357cc-121">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="357cc-122">[in] Eine Bitmaske mit client- oder anbieterdefinierten **Flags,** die aus der PR_MSG_STATUS ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))-Eigenschaft der Nachricht kopiert wurden, die Informationen über den Status der Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="357cc-122">[in] A bitmask of client-defined or provider-defined flags copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of the message that provides information about the state of the message.</span></span> <span data-ttu-id="357cc-123">Der  _ulMessageStatus-Parameter_ muss festgelegt werden,  _wenn lpszMessageClass_ nicht NULL ist. Andernfalls  _wird ulMessageStatus_ ignoriert.</span><span class="sxs-lookup"><span data-stu-id="357cc-123">The  _ulMessageStatus_ parameter must be set if  _lpszMessageClass_ is non-NULL; otherwise,  _ulMessageStatus_ is ignored.</span></span> 
    
 <span data-ttu-id="357cc-124">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="357cc-124">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="357cc-125">[in] Ein Zeiger auf eine Bitmaske von **Flags,** die aus der PR_MESSAGE_FLAGS ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft der Nachricht kopiert wurden, die den aktuellen Status der Nachricht angibt.</span><span class="sxs-lookup"><span data-stu-id="357cc-125">[in] A pointer to a bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the message that indicates the current state of the message.</span></span> <span data-ttu-id="357cc-126">Der  _ulMessageFlags-Parameter_ muss festgelegt werden,  _wenn lpszMessageClass_ nicht NULL ist. Andernfalls  _wird ulMessageFlags_ ignoriert.</span><span class="sxs-lookup"><span data-stu-id="357cc-126">The  _ulMessageFlags_ parameter must be set if  _lpszMessageClass_ is non-NULL; otherwise,  _ulMessageFlags_ is ignored.</span></span> 
    
 <span data-ttu-id="357cc-127">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="357cc-127">_pFolderFocus_</span></span>
  
> <span data-ttu-id="357cc-128">[in] Ein Zeiger auf den Ordner, der die Nachricht direkt enthält.</span><span class="sxs-lookup"><span data-stu-id="357cc-128">[in] A pointer to the folder that directly contains the message.</span></span> <span data-ttu-id="357cc-129">Der  _pFolderFocus-Parameter_ kann NULL sein, wenn ein solcher Ordner nicht vorhanden ist (z. B. wenn die Nachricht in eine andere Nachricht eingebettet ist).</span><span class="sxs-lookup"><span data-stu-id="357cc-129">The  _pFolderFocus_ parameter can be NULL if such a folder does not exist (for example, if the message is embedded in another message).</span></span> 
    
 <span data-ttu-id="357cc-130">_pMessageSite_</span><span class="sxs-lookup"><span data-stu-id="357cc-130">_pMessageSite_</span></span>
  
> <span data-ttu-id="357cc-131">[in] Ein Zeiger auf die Nachrichtenwebsite der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="357cc-131">[in] A pointer to the message site of the message.</span></span>
    
 <span data-ttu-id="357cc-132">_pmsg_</span><span class="sxs-lookup"><span data-stu-id="357cc-132">_pmsg_</span></span>
  
> <span data-ttu-id="357cc-133">[in] Ein Zeiger auf die Nachricht.</span><span class="sxs-lookup"><span data-stu-id="357cc-133">[in] A pointer to the message.</span></span>
    
 <span data-ttu-id="357cc-134">_pViewContext_</span><span class="sxs-lookup"><span data-stu-id="357cc-134">_pViewContext_</span></span>
  
> <span data-ttu-id="357cc-135">[in] Ein Zeiger auf den Ansichtskontext für die Nachricht.</span><span class="sxs-lookup"><span data-stu-id="357cc-135">[in] A pointer to the view context for the message.</span></span> <span data-ttu-id="357cc-136">Der  _pViewContext-Parameter_ kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="357cc-136">The  _pViewContext_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="357cc-137">_riid_</span><span class="sxs-lookup"><span data-stu-id="357cc-137">_riid_</span></span>
  
> <span data-ttu-id="357cc-138">[in] Der Schnittstellenbezeichner (Interface Identifier, IID) der Schnittstelle, die für das zurückgegebene Formularobjekt verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="357cc-138">[in] The interface identifier (IID) of the interface to be used for the returned form object.</span></span> <span data-ttu-id="357cc-139">Der  _riid-Parameter_ darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="357cc-139">The  _riid_ parameter must not be NULL.</span></span> 
    
 <span data-ttu-id="357cc-140">_ppvObj_</span><span class="sxs-lookup"><span data-stu-id="357cc-140">_ppvObj_</span></span>
  
> <span data-ttu-id="357cc-141">[out] Ein Zeiger auf einen Zeiger auf die zurückgegebene Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="357cc-141">[out] A pointer to a pointer to the returned interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="357cc-142">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="357cc-142">Return value</span></span>

<span data-ttu-id="357cc-143">S_OK</span><span class="sxs-lookup"><span data-stu-id="357cc-143">S_OK</span></span> 
  
> <span data-ttu-id="357cc-144">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="357cc-144">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="357cc-145">MAPI_E_NO_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="357cc-145">MAPI_E_NO_INTERFACE</span></span> 
  
> <span data-ttu-id="357cc-146">Das Formular unterstützt die angeforderte Schnittstelle nicht.</span><span class="sxs-lookup"><span data-stu-id="357cc-146">The form does not support the requested interface.</span></span>
    
<span data-ttu-id="357cc-147">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="357cc-147">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="357cc-148">Die in  _lpszMessageClass_ übergebene Nachrichtenklasse ist nicht mit der Nachrichtenklasse für ein Formular in der Formularbibliothek übereinstimmend.</span><span class="sxs-lookup"><span data-stu-id="357cc-148">The message class passed in  _lpszMessageClass_ does not match the message class for any form in the form library.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="357cc-149">Hinweise</span><span class="sxs-lookup"><span data-stu-id="357cc-149">Remarks</span></span>

<span data-ttu-id="357cc-150">Formularbetrachter rufen die **IMAPIFormMgr::LoadForm-Methode** auf, um ein Formular für eine vorhandene Nachricht zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="357cc-150">Form viewers call the **IMAPIFormMgr::LoadForm** method to open a form for an existing message.</span></span> <span data-ttu-id="357cc-151">**LoadForm** öffnet das Formularobjekt, lädt die Nachricht in das Formularobjekt, richtet gegebenenfalls den entsprechenden Ansichtskontext ein und gibt die angeforderte Schnittstelle für das Formularobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="357cc-151">**LoadForm** opens the form object, loads the message into the form object, sets up the appropriate view context, if necessary, and returns the requested interface for the form object.</span></span> 
  
<span data-ttu-id="357cc-152">Der  _pFolderFocus-Parameter_ zeigt auf den Ordner, der die Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="357cc-152">The  _pFolderFocus_ parameter points to the folder that contains the message.</span></span> <span data-ttu-id="357cc-153">Wenn die Nachricht in eine andere Nachricht eingebettet ist,  _sollte pFolderFocus_ NULL sein.</span><span class="sxs-lookup"><span data-stu-id="357cc-153">If the message is embedded in another message,  _pFolderFocus_ should be NULL.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="357cc-154">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="357cc-154">Notes to implementers</span></span>

<span data-ttu-id="357cc-155">Wenn NULL in  _lpszMessageClass_ übergeben wird, ruft die Implementierung die Nachrichtenklasse, den Status und die Flags der Nachricht aus den Eigenschaften **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), **PR_MSG_STATUS** und PR_MESSAGE_FLAGS **der Nachricht** ab.</span><span class="sxs-lookup"><span data-stu-id="357cc-155">If NULL is passed in  _lpszMessageClass_, the implementation obtains the message's message class, status, and flags from the message's **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), **PR_MSG_STATUS** and **PR_MESSAGE_FLAGS** properties.</span></span> <span data-ttu-id="357cc-156">Wenn eine Nachrichtenklassenzeichenfolge in _lpszMessageClass_ bereitgestellt wird, muss die Implementierung die Werte in _ulMessageStatus_ und _ulMessageFlags verwenden._</span><span class="sxs-lookup"><span data-stu-id="357cc-156">If a message class string is provided in  _lpszMessageClass_, the implementation must use the values in  _ulMessageStatus_ and  _ulMessageFlags_.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="357cc-157">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="357cc-157">MFCMAPI reference</span></span>

<span data-ttu-id="357cc-158">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="357cc-158">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="357cc-159">**Datei**</span><span class="sxs-lookup"><span data-stu-id="357cc-159">**File**</span></span>|<span data-ttu-id="357cc-160">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="357cc-160">**Function**</span></span>|<span data-ttu-id="357cc-161">**Comment**</span><span class="sxs-lookup"><span data-stu-id="357cc-161">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="357cc-162">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="357cc-162">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="357cc-163">OpenMessageNonModal</span><span class="sxs-lookup"><span data-stu-id="357cc-163">OpenMessageNonModal</span></span>  <br/> |<span data-ttu-id="357cc-164">MFCMAPI verwendet die **IMAPIFormMgr::LoadForm-Methode,** um ein Formular zu laden, bevor es angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="357cc-164">MFCMAPI uses the **IMAPIFormMgr::LoadForm** method to load a form before displaying it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="357cc-165">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="357cc-165">See also</span></span>



[<span data-ttu-id="357cc-166">PidTagMessageClass (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="357cc-166">PidTagMessageClass Canonical Property</span></span>](pidtagmessageclass-canonical-property.md)
  
[<span data-ttu-id="357cc-167">PidTagMessageFlags (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="357cc-167">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="357cc-168">PidTagMessageStatus (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="357cc-168">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="357cc-169">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="357cc-169">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="357cc-170">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="357cc-170">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

