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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: f51dd1fe533d0577996e6e1be185302f2dc972fe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321455"
---
# <a name="imapimessagesitenewmessage"></a><span data-ttu-id="9bc9d-103">IMAPIMessageSite::NewMessage</span><span class="sxs-lookup"><span data-stu-id="9bc9d-103">IMAPIMessageSite::NewMessage</span></span>

  
  
<span data-ttu-id="9bc9d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9bc9d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9bc9d-105">Erstellt eine neue Nachricht.</span><span class="sxs-lookup"><span data-stu-id="9bc9d-105">Creates a new message.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="9bc9d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9bc9d-106">Parameters</span></span>

 <span data-ttu-id="9bc9d-107">_fComposeInFolder_</span><span class="sxs-lookup"><span data-stu-id="9bc9d-107">_fComposeInFolder_</span></span>
  
> <span data-ttu-id="9bc9d-108">in Gibt an, in welchem Ordner die Nachricht erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9bc9d-108">[in] Indicates in which folder the message should be composed.</span></span> <span data-ttu-id="9bc9d-109">Wenn die Variable auf FALSE festgelegt ist, wird der _pFolderFocus_ -Parameter ignoriert, und der Formular Betrachter kann die Nachricht in einem beliebigen Ordner verfassen.</span><span class="sxs-lookup"><span data-stu-id="9bc9d-109">If the variable is FALSE, the  _pFolderFocus_ parameter is ignored and the form viewer can compose the message in any folder.</span></span> <span data-ttu-id="9bc9d-110">Wenn die Variable auf TRUE festgelegt ist und im _pFolderFocus_ -Parameter NULL übergeben wird, wird die Nachricht im aktuellen Ordner zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="9bc9d-110">If the variable is TRUE and NULL is passed in the  _pFolderFocus_ parameter, the message is composed in the current folder.</span></span> <span data-ttu-id="9bc9d-111">Wenn die Variable auf TRUE festgelegt ist und ein Wert ungleich NULL in _pFolderFocus_übergeben wird, wird die Nachricht in dem Ordner zusammengestellt, auf den von _pFolderFocus_verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="9bc9d-111">If the variable is TRUE and a non-NULL value is passed in  _pFolderFocus_, the message is composed in the folder pointed to by  _pFolderFocus_.</span></span>
    
 <span data-ttu-id="9bc9d-112">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="9bc9d-112">_pFolderFocus_</span></span>
  
> <span data-ttu-id="9bc9d-113">in Ein Zeiger auf den Ordner, in dem die neue Nachricht erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="9bc9d-113">[in] A pointer to the folder where the new message is created.</span></span>
    
 <span data-ttu-id="9bc9d-114">_pPersistMessage_</span><span class="sxs-lookup"><span data-stu-id="9bc9d-114">_pPersistMessage_</span></span>
  
> <span data-ttu-id="9bc9d-115">in Ein Zeiger auf das Form-Objekt für das neue Formular.</span><span class="sxs-lookup"><span data-stu-id="9bc9d-115">[in] A pointer to the form object for the new form.</span></span>
    
 <span data-ttu-id="9bc9d-116">_ppMessage_</span><span class="sxs-lookup"><span data-stu-id="9bc9d-116">_ppMessage_</span></span>
  
> <span data-ttu-id="9bc9d-117">Out Ein Zeiger auf einen Zeiger auf die neue Nachricht.</span><span class="sxs-lookup"><span data-stu-id="9bc9d-117">[out] A pointer to a pointer to the new message.</span></span>
    
 <span data-ttu-id="9bc9d-118">_ppMessageSite_</span><span class="sxs-lookup"><span data-stu-id="9bc9d-118">_ppMessageSite_</span></span>
  
> <span data-ttu-id="9bc9d-119">Out Ein Zeiger auf einen Zeiger auf ein Nachrichtenwebsite Objekt für die neue Nachricht.</span><span class="sxs-lookup"><span data-stu-id="9bc9d-119">[out] A pointer to a pointer to a message site object for the new message.</span></span>
    
 <span data-ttu-id="9bc9d-120">_ppViewContext_</span><span class="sxs-lookup"><span data-stu-id="9bc9d-120">_ppViewContext_</span></span>
  
> <span data-ttu-id="9bc9d-121">Out Ein Zeiger auf einen Zeiger auf einen Ansichtskontext, der für die Übergabe an ein neues Formular mit der neuen Nachricht geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="9bc9d-121">[out] A pointer to a pointer to a view context that is appropriate for passing to a new form with the new message.</span></span> <span data-ttu-id="9bc9d-122">Wenn das Formular einen eigenen Ansichtskontext implementiert, kann im _ppViewContext_ -Parameter NULL übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="9bc9d-122">If the form implements its own view context, NULL can be passed in the  _ppViewContext_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9bc9d-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9bc9d-123">Return value</span></span>

<span data-ttu-id="9bc9d-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="9bc9d-124">S_OK</span></span> 
  
> <span data-ttu-id="9bc9d-125">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="9bc9d-125">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9bc9d-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9bc9d-126">Remarks</span></span>

<span data-ttu-id="9bc9d-127">Formularobjekte rufen die **IMAPIMessageSite:: PostMessage** -Methode auf, um eine neue Nachricht zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9bc9d-127">Form objects call the **IMAPIMessageSite::NewMessage** method to create a new message.</span></span> <span data-ttu-id="9bc9d-128">Das Formular verwendet \*\*\*\* eine neumeldung, um eine neue Nachricht und die zugehörige Nachrichtenwebsite aus ihrer Ansicht abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9bc9d-128">The form uses **NewMessage** to get a new message and the associated message site from its view.</span></span> <span data-ttu-id="9bc9d-129">Anschließend kann die neue Nachricht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="9bc9d-129">It can then modify the new message.</span></span> 
  
<span data-ttu-id="9bc9d-130">Sie können auch einen zugeordneten Ansichtskontext abrufen, indem Sie einen Wert ungleich NULL im _ppViewContext_ -Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="9bc9d-130">You can also obtain an associated view context by passing in a non-NULL value in the  _ppViewContext_ parameter.</span></span> <span data-ttu-id="9bc9d-131">Dieser Ansichtskontext kann direkt verwendet werden, oder er kann aggregiert und an die neue Nachricht übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="9bc9d-131">This view context can be used directly, or it can be aggregated and passed to the new message.</span></span> <span data-ttu-id="9bc9d-132">Wenn eine vollständige Implementierung erforderlich ist, müssen Sie in _ppViewContext_den Wert NULL überschreiten.</span><span class="sxs-lookup"><span data-stu-id="9bc9d-132">If a complete implementation is required, pass NULL in  _ppViewContext_.</span></span>
  
<span data-ttu-id="9bc9d-133">Eine Liste der Schnittstellen im Zusammenhang mit Formular Servern finden Sie unter [MAPI-Formular Schnittstellen](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="9bc9d-133">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="9bc9d-134">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="9bc9d-134">MFCMAPI reference</span></span>

<span data-ttu-id="9bc9d-135">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="9bc9d-135">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9bc9d-136">**Datei**</span><span class="sxs-lookup"><span data-stu-id="9bc9d-136">**File**</span></span>|<span data-ttu-id="9bc9d-137">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="9bc9d-137">**Function**</span></span>|<span data-ttu-id="9bc9d-138">**Comment**</span><span class="sxs-lookup"><span data-stu-id="9bc9d-138">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9bc9d-139">MyMAPIFormViewer. cpp</span><span class="sxs-lookup"><span data-stu-id="9bc9d-139">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="9bc9d-140">CMyMAPIFormViewer:: neuNachricht</span><span class="sxs-lookup"><span data-stu-id="9bc9d-140">CMyMAPIFormViewer::NewMessage</span></span>  <br/> |<span data-ttu-id="9bc9d-141">MFCMAPI verwendet die **IMAPIMessageSite:: PostMessage** -Methode, um eine neue Nachricht zu erstellen, einen neuen Formular Betrachter zu \*\*\*\* instanziieren und setpersist aufzurufen, um die Nachricht im Formular-Viewer festzulegen.</span><span class="sxs-lookup"><span data-stu-id="9bc9d-141">MFCMAPI uses the **IMAPIMessageSite::NewMessage** method to create a new message, instantiate a new form viewer, and call **SetPersist** to set the message on the form viewer.</span></span> <span data-ttu-id="9bc9d-142">Schließlich wird der Formular Betrachter als Nachrichtenwebsite zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9bc9d-142">Finally, it returns the form viewer as the message site.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9bc9d-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9bc9d-143">See also</span></span>



[<span data-ttu-id="9bc9d-144">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9bc9d-144">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)
  
[<span data-ttu-id="9bc9d-145">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9bc9d-145">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="9bc9d-146">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="9bc9d-146">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="9bc9d-147">MAPI-Formular Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="9bc9d-147">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

