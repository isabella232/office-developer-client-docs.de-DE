---
title: IMAPIMessageSiteDeleteMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.DeleteMessage
api_type:
- COM
ms.assetid: 09955996-b904-4c0d-8ba5-954a8875c055
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7b2761e20444c51d08380aee01c41eee797733eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321413"
---
# <a name="imapimessagesitedeletemessage"></a><span data-ttu-id="7553f-103">IMAPIMessageSite::DeleteMessage</span><span class="sxs-lookup"><span data-stu-id="7553f-103">IMAPIMessageSite::DeleteMessage</span></span>

  
  
<span data-ttu-id="7553f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7553f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7553f-105">Löscht die aktuelle Nachricht.</span><span class="sxs-lookup"><span data-stu-id="7553f-105">Deletes the current message.</span></span>
  
```cpp
HRESULT DeleteMessage(
  LPMAPIVIEWCONTEXT pViewContext,
  LPCRECT prcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="7553f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7553f-106">Parameters</span></span>

 <span data-ttu-id="7553f-107">_pViewContext_</span><span class="sxs-lookup"><span data-stu-id="7553f-107">_pViewContext_</span></span>
  
> <span data-ttu-id="7553f-108">[in] Ein Zeiger auf ein Ansichtskontextobjekt.</span><span class="sxs-lookup"><span data-stu-id="7553f-108">[in] A pointer to a view context object.</span></span>
    
 <span data-ttu-id="7553f-109">_prcPosRect_</span><span class="sxs-lookup"><span data-stu-id="7553f-109">_prcPosRect_</span></span>
  
> <span data-ttu-id="7553f-110">[in] Ein Zeiger auf eine [RECT-Struktur,](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) die die Fenstergröße und -position des aktuellen Formulars enthält.</span><span class="sxs-lookup"><span data-stu-id="7553f-110">[in] A pointer to a [RECT](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) structure that contains the current form's window size and position.</span></span> <span data-ttu-id="7553f-111">Das nächste angezeigte Formular verwendet auch dieses Fensterrechteck.</span><span class="sxs-lookup"><span data-stu-id="7553f-111">The next form displayed also uses this window rectangle.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7553f-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7553f-112">Return value</span></span>

<span data-ttu-id="7553f-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="7553f-113">S_OK</span></span> 
  
> <span data-ttu-id="7553f-114">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="7553f-114">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="7553f-115">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="7553f-115">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="7553f-116">Der Vorgang wird von dieser Nachrichtenwebsite nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7553f-116">The operation is not supported by this message site.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7553f-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7553f-117">Remarks</span></span>

<span data-ttu-id="7553f-118">Ein Formularobjekt ruft die **IMAPIMessageSite::D eleteMessage-Methode** auf, um die Nachricht zu löschen, die derzeit im Formular angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="7553f-118">A form object calls the **IMAPIMessageSite::DeleteMessage** method to delete the message that the form is currently displaying.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="7553f-119">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="7553f-119">Notes to callers</span></span>

<span data-ttu-id="7553f-120">Nach der Rückgabe von **DeleteMessage** müssen Formularobjekte nach einer neuen Nachricht suchen und sich dann selbst schließen, wenn keine vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="7553f-120">Following the return of **DeleteMessage**, form objects must check for a new message and then dismiss themselves if none exists.</span></span> <span data-ttu-id="7553f-121">Um zu ermitteln, ob die Nachricht **DeleteMessage** gelöscht oder in einen Ordner "Gelöschte Elemente" verschoben wurde, kann ein Formularobjekt die [IMAPIMessageSite::GetSiteStatus-Methode](imapimessagesite-getsitestatus.md) aufrufen, um zu ermitteln, ob das DELETE_IS_MOVE-Flag zurückgegeben wurde. </span><span class="sxs-lookup"><span data-stu-id="7553f-121">To determine whether the message **DeleteMessage** acted on was deleted or moved to a **Deleted Items** folder, a form object can call the [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) method to determine whether the DELETE_IS_MOVE flag was returned.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="7553f-122">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="7553f-122">Notes to implementers</span></span>

<span data-ttu-id="7553f-123">Wenn die Implementierung der **DeleteMessage-Methode** durch einen Formularanzeiger zur nächsten Nachricht wechselt, nachdem eine Nachricht gelöscht wurde, sollte die Implementierung die [IMAPIViewContext::ActivateNext-Methode](imapiviewcontext-activatenext.md) aufrufen und das flag VCDIR_DELETE übergeben, bevor der eigentliche Löschvorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7553f-123">If a form viewer's implementation of the **DeleteMessage** method moves to the next message after it deletes a message, the implementation should call the [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) method and pass the VCDIR_DELETE flag before performing the actual deletion.</span></span> <span data-ttu-id="7553f-124">Wenn die Implementierung von **DeleteMessage** durch einen Formularanzeiger die gelöschte Nachricht verschiebt (z. B. in einen Ordner **"Gelöschte** Elemente"), muss die Implementierung Änderungen an der Nachricht speichern, wenn die Nachricht geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="7553f-124">If a form viewer's implementation of **DeleteMessage** moves the deleted message (for example, to a **Deleted Items** folder), the implementation must save changes to the message if the message was modified.</span></span> 
  
<span data-ttu-id="7553f-125">Eine typische Implementierung von **DeleteMessage führt** die folgenden Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="7553f-125">A typical implementation of **DeleteMessage** performs the following tasks:</span></span> 
  
1. <span data-ttu-id="7553f-126">Wenn die Implementierung die Nachricht bewegt, ruft sie die [IPersistMessage::Save-Methode](ipersistmessage-save.md) auf, und übergeben **Null** im _pMessage-Parameter_ und **true** im _fSameAsLoad-Parameter._</span><span class="sxs-lookup"><span data-stu-id="7553f-126">If the implementation is moving the message, it calls the [IPersistMessage::Save](ipersistmessage-save.md) method, passing **null** in the  _pMessage_ parameter and **true** in the  _fSameAsLoad_ parameter.</span></span> 
    
2. <span data-ttu-id="7553f-127">Es ruft die **IMAPIViewContext::ActivateNext-Methode** auf und über VCDIR_DELETE im _ulDir-Parameter._</span><span class="sxs-lookup"><span data-stu-id="7553f-127">It calls the **IMAPIViewContext::ActivateNext** method, passing the VCDIR_DELETE flag in the  _ulDir_ parameter.</span></span> 
    
3. <span data-ttu-id="7553f-128">Wenn beim **ActivateNext-Aufruf** ein Fehler auftritt, wird er zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7553f-128">If the **ActivateNext** call fails, it returns.</span></span> <span data-ttu-id="7553f-129">Wenn **ActivateNext** S_FALSE zurückgibt, wird die [IPersistMessage::HandsOffMessage-Methode](ipersistmessage-handsoffmessage.md) aufruft.</span><span class="sxs-lookup"><span data-stu-id="7553f-129">If **ActivateNext** returns S_FALSE, it calls the [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) method.</span></span> 
    
4. <span data-ttu-id="7553f-130">Es löscht oder verschiebt die Nachricht.</span><span class="sxs-lookup"><span data-stu-id="7553f-130">It deletes or moves the message.</span></span>
    
<span data-ttu-id="7553f-131">Um die vom Formularfenster verwendete **RECT-Struktur** zu erhalten, rufen Sie die Windows [GetWindowRect-Funktion](https://msdn.microsoft.com/library/ms633519) auf.</span><span class="sxs-lookup"><span data-stu-id="7553f-131">To obtain the **RECT** structure used by a form's window, call the Windows [GetWindowRect](https://msdn.microsoft.com/library/ms633519) function.</span></span> 
  
<span data-ttu-id="7553f-132">Eine Liste der Schnittstellen im Zusammenhang mit Formularservern finden Sie unter [MAPI Form Interfaces](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="7553f-132">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="7553f-133">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="7553f-133">MFCMAPI reference</span></span>

<span data-ttu-id="7553f-134">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="7553f-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7553f-135">**Datei**</span><span class="sxs-lookup"><span data-stu-id="7553f-135">**File**</span></span>|<span data-ttu-id="7553f-136">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="7553f-136">**Function**</span></span>|<span data-ttu-id="7553f-137">**Comment**</span><span class="sxs-lookup"><span data-stu-id="7553f-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7553f-138">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="7553f-138">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="7553f-139">CMyMAPIFormViewer::D eleteMessage</span><span class="sxs-lookup"><span data-stu-id="7553f-139">CMyMAPIFormViewer::DeleteMessage</span></span>  <br/> |<span data-ttu-id="7553f-140">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="7553f-140">Not implemented.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7553f-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7553f-141">See also</span></span>



[<span data-ttu-id="7553f-142">IMAPIMessageSite::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="7553f-142">IMAPIMessageSite::GetSiteStatus</span></span>](imapimessagesite-getsitestatus.md)
  
[<span data-ttu-id="7553f-143">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="7553f-143">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="7553f-144">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="7553f-144">IPersistMessage::HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md)
  
[<span data-ttu-id="7553f-145">IPersistMessage::Save</span><span class="sxs-lookup"><span data-stu-id="7553f-145">IPersistMessage::Save</span></span>](ipersistmessage-save.md)
  
[<span data-ttu-id="7553f-146">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7553f-146">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="7553f-147">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="7553f-147">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="7553f-148">MAPI-Formularschnittstellen</span><span class="sxs-lookup"><span data-stu-id="7553f-148">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

