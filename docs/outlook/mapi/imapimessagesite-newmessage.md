---
title: IMAPIMessageSiteNewMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.NewMessage
api_type:
- COM
ms.assetid: ce6b6e6c-7f22-43c2-8182-90cf6db93844
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f51dd1fe533d0577996e6e1be185302f2dc972fe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438771"
---
# <a name="imapimessagesitenewmessage"></a><span data-ttu-id="22a4d-103">IMAPIMessageSite::NewMessage</span><span class="sxs-lookup"><span data-stu-id="22a4d-103">IMAPIMessageSite::NewMessage</span></span>

  
  
<span data-ttu-id="22a4d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="22a4d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="22a4d-105">Erstellt eine neue Nachricht.</span><span class="sxs-lookup"><span data-stu-id="22a4d-105">Creates a new message.</span></span>
  
```cpp
HRESULT NewMessage(
  ULONG fComposeInFolder,
  LPMAPIFOLDER pFolderFocus,
  LPPERSISTMESSAGE pPersistMessage,
  LPMESSAGE FAR * ppMessage,
  LPMAPIMESSAGESITE FAR * ppMessageSite,
  LPMAPIVIEWCONTEXT FAR * ppViewContext
);
```

## <a name="parameters"></a><span data-ttu-id="22a4d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="22a4d-106">Parameters</span></span>

 <span data-ttu-id="22a4d-107">_fComposeInFolder_</span><span class="sxs-lookup"><span data-stu-id="22a4d-107">_fComposeInFolder_</span></span>
  
> <span data-ttu-id="22a4d-108">[in] Gibt an, in welchem Ordner die Nachricht verfasst werden soll.</span><span class="sxs-lookup"><span data-stu-id="22a4d-108">[in] Indicates in which folder the message should be composed.</span></span> <span data-ttu-id="22a4d-109">Wenn die Variable FALSE ist, wird  _der pFolderFocus-Parameter_ ignoriert, und die Formularanzeige kann die Nachricht in einem beliebigen Ordner verfassen.</span><span class="sxs-lookup"><span data-stu-id="22a4d-109">If the variable is FALSE, the  _pFolderFocus_ parameter is ignored and the form viewer can compose the message in any folder.</span></span> <span data-ttu-id="22a4d-110">Wenn die Variable TRUE ist und NULL im  _pFolderFocus-Parameter_ übergeben wird, wird die Nachricht im aktuellen Ordner verfasst.</span><span class="sxs-lookup"><span data-stu-id="22a4d-110">If the variable is TRUE and NULL is passed in the  _pFolderFocus_ parameter, the message is composed in the current folder.</span></span> <span data-ttu-id="22a4d-111">Wenn die Variable TRUE ist und ein Nicht-NULL-Wert in _pFolderFocus_ übergeben wird, wird die Nachricht in dem Ordner verfasst, auf den _pFolderFocus verweist._</span><span class="sxs-lookup"><span data-stu-id="22a4d-111">If the variable is TRUE and a non-NULL value is passed in  _pFolderFocus_, the message is composed in the folder pointed to by  _pFolderFocus_.</span></span>
    
 <span data-ttu-id="22a4d-112">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="22a4d-112">_pFolderFocus_</span></span>
  
> <span data-ttu-id="22a4d-113">[in] Ein Zeiger auf den Ordner, in dem die neue Nachricht erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="22a4d-113">[in] A pointer to the folder where the new message is created.</span></span>
    
 <span data-ttu-id="22a4d-114">_pPersistMessage_</span><span class="sxs-lookup"><span data-stu-id="22a4d-114">_pPersistMessage_</span></span>
  
> <span data-ttu-id="22a4d-115">[in] Ein Zeiger auf das Formularobjekt für das neue Formular.</span><span class="sxs-lookup"><span data-stu-id="22a4d-115">[in] A pointer to the form object for the new form.</span></span>
    
 <span data-ttu-id="22a4d-116">_ppMessage_</span><span class="sxs-lookup"><span data-stu-id="22a4d-116">_ppMessage_</span></span>
  
> <span data-ttu-id="22a4d-117">[out] Ein Zeiger auf einen Zeiger auf die neue Nachricht.</span><span class="sxs-lookup"><span data-stu-id="22a4d-117">[out] A pointer to a pointer to the new message.</span></span>
    
 <span data-ttu-id="22a4d-118">_ppMessageSite_</span><span class="sxs-lookup"><span data-stu-id="22a4d-118">_ppMessageSite_</span></span>
  
> <span data-ttu-id="22a4d-119">[out] Ein Zeiger auf einen Zeiger auf ein Nachrichtenwebsiteobjekt für die neue Nachricht.</span><span class="sxs-lookup"><span data-stu-id="22a4d-119">[out] A pointer to a pointer to a message site object for the new message.</span></span>
    
 <span data-ttu-id="22a4d-120">_ppViewContext_</span><span class="sxs-lookup"><span data-stu-id="22a4d-120">_ppViewContext_</span></span>
  
> <span data-ttu-id="22a4d-121">[out] Ein Zeiger auf einen Zeiger auf einen Ansichtskontext, der für die Übergabe an ein neues Formular mit der neuen Nachricht geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="22a4d-121">[out] A pointer to a pointer to a view context that is appropriate for passing to a new form with the new message.</span></span> <span data-ttu-id="22a4d-122">Wenn das Formular einen eigenen Ansichtskontext implementiert, kann NULL im  _ppViewContext-Parameter übergeben_ werden.</span><span class="sxs-lookup"><span data-stu-id="22a4d-122">If the form implements its own view context, NULL can be passed in the  _ppViewContext_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="22a4d-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="22a4d-123">Return value</span></span>

<span data-ttu-id="22a4d-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="22a4d-124">S_OK</span></span> 
  
> <span data-ttu-id="22a4d-125">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="22a4d-125">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="22a4d-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="22a4d-126">Remarks</span></span>

<span data-ttu-id="22a4d-127">Formularobjekte rufen die **IMAPIMessageSite::NewMessage-Methode** auf, um eine neue Nachricht zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="22a4d-127">Form objects call the **IMAPIMessageSite::NewMessage** method to create a new message.</span></span> <span data-ttu-id="22a4d-128">Das Formular verwendet **NewMessage,** um eine neue Nachricht und die zugeordnete Nachrichtenwebsite aus der Ansicht zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="22a4d-128">The form uses **NewMessage** to get a new message and the associated message site from its view.</span></span> <span data-ttu-id="22a4d-129">Anschließend kann die neue Nachricht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="22a4d-129">It can then modify the new message.</span></span> 
  
<span data-ttu-id="22a4d-130">Sie können auch einen zugeordneten Ansichtskontext abrufen, indem Sie einen Nicht-NULL-Wert im  _ppViewContext-Parameter_ übergeben.</span><span class="sxs-lookup"><span data-stu-id="22a4d-130">You can also obtain an associated view context by passing in a non-NULL value in the  _ppViewContext_ parameter.</span></span> <span data-ttu-id="22a4d-131">Dieser Ansichtskontext kann direkt verwendet oder aggregiert und an die neue Nachricht übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="22a4d-131">This view context can be used directly, or it can be aggregated and passed to the new message.</span></span> <span data-ttu-id="22a4d-132">Wenn eine vollständige Implementierung erforderlich ist, übergeben Sie NULL in  _ppViewContext_.</span><span class="sxs-lookup"><span data-stu-id="22a4d-132">If a complete implementation is required, pass NULL in  _ppViewContext_.</span></span>
  
<span data-ttu-id="22a4d-133">Eine Liste der Schnittstellen im Zusammenhang mit Formularservern finden Sie unter [MAPI Form Interfaces](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="22a4d-133">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="22a4d-134">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="22a4d-134">MFCMAPI reference</span></span>

<span data-ttu-id="22a4d-135">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="22a4d-135">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="22a4d-136">**Datei**</span><span class="sxs-lookup"><span data-stu-id="22a4d-136">**File**</span></span>|<span data-ttu-id="22a4d-137">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="22a4d-137">**Function**</span></span>|<span data-ttu-id="22a4d-138">**Comment**</span><span class="sxs-lookup"><span data-stu-id="22a4d-138">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="22a4d-139">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="22a4d-139">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="22a4d-140">CMyMAPIFormViewer::NewMessage</span><span class="sxs-lookup"><span data-stu-id="22a4d-140">CMyMAPIFormViewer::NewMessage</span></span>  <br/> |<span data-ttu-id="22a4d-141">MFCMAPI verwendet die **IMAPIMessageSite::NewMessage-Methode,** um eine neue Nachricht zu erstellen, eine neue Formularanzeige zu instanziieren und **SetPersist** zum Festlegen der Nachricht in der Formularanzeige auf.</span><span class="sxs-lookup"><span data-stu-id="22a4d-141">MFCMAPI uses the **IMAPIMessageSite::NewMessage** method to create a new message, instantiate a new form viewer, and call **SetPersist** to set the message on the form viewer.</span></span> <span data-ttu-id="22a4d-142">Schließlich wird die Formularanzeige als Nachrichtenwebsite zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="22a4d-142">Finally, it returns the form viewer as the message site.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="22a4d-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22a4d-143">See also</span></span>



[<span data-ttu-id="22a4d-144">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="22a4d-144">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)
  
[<span data-ttu-id="22a4d-145">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="22a4d-145">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="22a4d-146">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="22a4d-146">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="22a4d-147">MAPI-Formularschnittstellen</span><span class="sxs-lookup"><span data-stu-id="22a4d-147">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

