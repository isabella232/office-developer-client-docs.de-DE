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
ms.openlocfilehash: da6de94342c8d8bbd378a3cde2fb065c97632291
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792205"
---
# <a name="imapimessagesitedeletemessage"></a><span data-ttu-id="4e8a6-103">IMAPIMessageSite::DeleteMessage</span><span class="sxs-lookup"><span data-stu-id="4e8a6-103">IMAPIMessageSite::DeleteMessage</span></span>

  
  
<span data-ttu-id="4e8a6-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4e8a6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4e8a6-105">Löscht die aktuelle Nachricht.</span><span class="sxs-lookup"><span data-stu-id="4e8a6-105">Deletes the current message.</span></span>
  
```cpp
HRESULT DeleteMessage(
  LPMAPIVIEWCONTEXT pViewContext,
  LPCRECT prcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="4e8a6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4e8a6-106">Parameters</span></span>

 <span data-ttu-id="4e8a6-107">_pViewContext_</span><span class="sxs-lookup"><span data-stu-id="4e8a6-107">_pViewContext_</span></span>
  
> <span data-ttu-id="4e8a6-108">[in] Ein Zeiger auf eine Ansicht Context-Objekt.</span><span class="sxs-lookup"><span data-stu-id="4e8a6-108">[in] A pointer to a view context object.</span></span>
    
 <span data-ttu-id="4e8a6-109">_prcPosRect_</span><span class="sxs-lookup"><span data-stu-id="4e8a6-109">_prcPosRect_</span></span>
  
> <span data-ttu-id="4e8a6-110">[in] Ein Zeiger auf ein [Rechteck](http://msdn.microsoft.com/de-de/library/dd162897%28VS.85%29.aspx) -Struktur, die im Fenstergröße und Position des aktuellen Formulars enthält.</span><span class="sxs-lookup"><span data-stu-id="4e8a6-110">[in] A pointer to a [RECT](http://msdn.microsoft.com/de-de/library/dd162897%28VS.85%29.aspx) structure that contains the current form's window size and position.</span></span> <span data-ttu-id="4e8a6-111">Das nächste Formular angezeigt wird auch dieses Fenster Rechteck verwendet.</span><span class="sxs-lookup"><span data-stu-id="4e8a6-111">The next form displayed also uses this window rectangle.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4e8a6-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4e8a6-112">Return value</span></span>

<span data-ttu-id="4e8a6-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="4e8a6-113">S_OK</span></span> 
  
> <span data-ttu-id="4e8a6-114">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="4e8a6-114">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="4e8a6-115">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="4e8a6-115">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="4e8a6-116">Der Vorgang wird von dieser Site Nachricht nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4e8a6-116">The operation is not supported by this message site.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4e8a6-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4e8a6-117">Remarks</span></span>

<span data-ttu-id="4e8a6-118">Ein Form-Objekt die **IMAPIMessageSite::DeleteMessage** -Methode aufgerufen, um die Nachricht zu löschen, die das Formular derzeit angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4e8a6-118">A form object calls the **IMAPIMessageSite::DeleteMessage** method to delete the message that the form is currently displaying.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="4e8a6-119">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="4e8a6-119">Notes to callers</span></span>

<span data-ttu-id="4e8a6-120">Nach der Rückgabe von **DeleteMessage**müssen Formular-Objekte für eine neue Nachricht überprüfen und anschließend schließen, wenn keines vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="4e8a6-120">Following the return of **DeleteMessage**, form objects must check for a new message and then dismiss themselves if none exists.</span></span> <span data-ttu-id="4e8a6-121">Um zu bestimmen, ob die Nachricht, der **DeleteMessage** reagiert in einen Ordner **Gelöschte Objekte** verschoben oder gelöscht wurde, kann ein Form-Objekt rufen Sie die [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) -Methode, um zu bestimmen, ob das Flag DELETE_IS_MOVE zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="4e8a6-121">To determine whether the message **DeleteMessage** acted on was deleted or moved to a **Deleted Items** folder, a form object can call the [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) method to determine whether the DELETE_IS_MOVE flag was returned.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="4e8a6-122">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="4e8a6-122">Notes to implementers</span></span>

<span data-ttu-id="4e8a6-123">Wenn ein Formular Viewer Implementierung der **DeleteMessage** -Methode auf die nächste Nachricht verschiebt, nachdem sie eine Nachricht gelöscht, sollten die Implementierung rufen Sie die [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) -Methode und übergeben die Kennzeichen VCDIR_DELETE vor dem Ausführen das tatsächliche löschen.</span><span class="sxs-lookup"><span data-stu-id="4e8a6-123">If a form viewer's implementation of the **DeleteMessage** method moves to the next message after it deletes a message, the implementation should call the [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) method and pass the VCDIR_DELETE flag before performing the actual deletion.</span></span> <span data-ttu-id="4e8a6-124">Wenn ein Formular Viewer Implementierung der **DeleteMessage** gelöschte Nachricht (beispielsweise in einem Ordner **Gelöschte Elemente** ) verschoben wird, muss die Implementierung der Nachricht speichern, wenn die Nachricht geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="4e8a6-124">If a form viewer's implementation of **DeleteMessage** moves the deleted message (for example, to a **Deleted Items** folder), the implementation must save changes to the message if the message was modified.</span></span> 
  
<span data-ttu-id="4e8a6-125">**DeleteMessage** eine normale Implementierung werden die folgenden Aufgaben ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="4e8a6-125">A typical implementation of **DeleteMessage** performs the following tasks:</span></span> 
  
1. <span data-ttu-id="4e8a6-126">Wenn die Implementierung die Nachricht verschoben wird, wird die [IPersistMessage::Save](ipersistmessage-save.md) -Methode **null** im _pMessage_ -Parameter und **true** im _fSameAsLoad_ -Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="4e8a6-126">If the implementation is moving the message, it calls the [IPersistMessage::Save](ipersistmessage-save.md) method, passing **null** in the  _pMessage_ parameter and **true** in the  _fSameAsLoad_ parameter.</span></span> 
    
2. <span data-ttu-id="4e8a6-127">Sie ruft die **IMAPIViewContext::ActivateNext** -Methode, die das VCDIR_DELETE-Flag in der _UlDir_ -Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="4e8a6-127">It calls the **IMAPIViewContext::ActivateNext** method, passing the VCDIR_DELETE flag in the  _ulDir_ parameter.</span></span> 
    
3. <span data-ttu-id="4e8a6-128">Wenn der **ActivateNext** -Aufruf fehlschlägt, wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4e8a6-128">If the **ActivateNext** call fails, it returns.</span></span> <span data-ttu-id="4e8a6-129">Wenn **ActivateNext** S_FALSE zurückgibt, wird die [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="4e8a6-129">If **ActivateNext** returns S_FALSE, it calls the [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) method.</span></span> 
    
4. <span data-ttu-id="4e8a6-130">Löscht oder verschiebt die Nachricht.</span><span class="sxs-lookup"><span data-stu-id="4e8a6-130">It deletes or moves the message.</span></span>
    
<span data-ttu-id="4e8a6-131">Rufen Sie die Windows [GetWindowRect](http://msdn.microsoft.com/de-de/library/ms633519) -Funktion, um die **Rechteck** -Struktur, die von einem Formular zugrunde Fenster verwendet zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4e8a6-131">To obtain the **RECT** structure used by a form's window, call the Windows [GetWindowRect](http://msdn.microsoft.com/de-de/library/ms633519) function.</span></span> 
  
<span data-ttu-id="4e8a6-132">Eine Liste der Schnittstellen im Zusammenhang mit der Formular-Servern finden Sie unter [MAPI-Formulars Schnittstellen](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="4e8a6-132">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="4e8a6-133">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="4e8a6-133">MFCMAPI reference</span></span>

<span data-ttu-id="4e8a6-134">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="4e8a6-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="4e8a6-135">**Datei**</span><span class="sxs-lookup"><span data-stu-id="4e8a6-135">**File**</span></span>|<span data-ttu-id="4e8a6-136">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="4e8a6-136">**Function**</span></span>|<span data-ttu-id="4e8a6-137">**Comment**</span><span class="sxs-lookup"><span data-stu-id="4e8a6-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4e8a6-138">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="4e8a6-138">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="4e8a6-139">CMyMAPIFormViewer::DeleteMessage</span><span class="sxs-lookup"><span data-stu-id="4e8a6-139">CMyMAPIFormViewer::DeleteMessage</span></span>  <br/> |<span data-ttu-id="4e8a6-140">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="4e8a6-140">Not implemented.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4e8a6-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4e8a6-141">See also</span></span>



[<span data-ttu-id="4e8a6-142">IMAPIMessageSite::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="4e8a6-142">IMAPIMessageSite::GetSiteStatus</span></span>](imapimessagesite-getsitestatus.md)
  
[<span data-ttu-id="4e8a6-143">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="4e8a6-143">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="4e8a6-144">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="4e8a6-144">IPersistMessage::HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md)
  
[<span data-ttu-id="4e8a6-145">IPersistMessage::Save</span><span class="sxs-lookup"><span data-stu-id="4e8a6-145">IPersistMessage::Save</span></span>](ipersistmessage-save.md)
  
[<span data-ttu-id="4e8a6-146">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4e8a6-146">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="4e8a6-147">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="4e8a6-147">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="4e8a6-148">MAPI-Formularoberflächen</span><span class="sxs-lookup"><span data-stu-id="4e8a6-148">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

