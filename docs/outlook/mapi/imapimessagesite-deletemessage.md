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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7b2761e20444c51d08380aee01c41eee797733eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321413"
---
# <a name="imapimessagesitedeletemessage"></a><span data-ttu-id="5ad17-103">IMAPIMessageSite::DeleteMessage</span><span class="sxs-lookup"><span data-stu-id="5ad17-103">IMAPIMessageSite::DeleteMessage</span></span>

  
  
<span data-ttu-id="5ad17-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5ad17-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5ad17-105">Löscht die aktuelle Nachricht.</span><span class="sxs-lookup"><span data-stu-id="5ad17-105">Deletes the current message.</span></span>
  
```cpp
HRESULT DeleteMessage(
  LPMAPIVIEWCONTEXT pViewContext,
  LPCRECT prcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="5ad17-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ad17-106">Parameters</span></span>

 <span data-ttu-id="5ad17-107">_pViewContext_</span><span class="sxs-lookup"><span data-stu-id="5ad17-107">_pViewContext_</span></span>
  
> <span data-ttu-id="5ad17-108">in Ein Zeiger auf ein View-Kontextobjekt.</span><span class="sxs-lookup"><span data-stu-id="5ad17-108">[in] A pointer to a view context object.</span></span>
    
 <span data-ttu-id="5ad17-109">_prcPosRect_</span><span class="sxs-lookup"><span data-stu-id="5ad17-109">_prcPosRect_</span></span>
  
> <span data-ttu-id="5ad17-110">in Ein Zeiger auf eine [Rect](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) -Struktur, die die Größe und Position des aktuellen Formulars enthält.</span><span class="sxs-lookup"><span data-stu-id="5ad17-110">[in] A pointer to a [RECT](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) structure that contains the current form's window size and position.</span></span> <span data-ttu-id="5ad17-111">Das nächste Formular wird auch dieses Fensterrechteck verwendet.</span><span class="sxs-lookup"><span data-stu-id="5ad17-111">The next form displayed also uses this window rectangle.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5ad17-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5ad17-112">Return value</span></span>

<span data-ttu-id="5ad17-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="5ad17-113">S_OK</span></span> 
  
> <span data-ttu-id="5ad17-114">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="5ad17-114">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="5ad17-115">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="5ad17-115">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="5ad17-116">Der Vorgang wird von dieser Nachrichtenwebsite nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5ad17-116">The operation is not supported by this message site.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5ad17-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5ad17-117">Remarks</span></span>

<span data-ttu-id="5ad17-118">Ein Form-Objekt ruft die **IMAPIMessageSite::D eletemessage** -Methode auf, um die Nachricht zu löschen, die vom Formular derzeit angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5ad17-118">A form object calls the **IMAPIMessageSite::DeleteMessage** method to delete the message that the form is currently displaying.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="5ad17-119">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="5ad17-119">Notes to callers</span></span>

<span data-ttu-id="5ad17-120">Nach der Rückgabe von **DeleteMessage**müssen Formularobjekte nach einer neuen Nachricht suchen und dann selbst entlassen werden, wenn keine vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="5ad17-120">Following the return of **DeleteMessage**, form objects must check for a new message and then dismiss themselves if none exists.</span></span> <span data-ttu-id="5ad17-121">Um zu ermitteln, ob die Nachricht, auf die **DeleteMessage** gehandelt wurde, gelöscht oder in einen Ordner " **Gelöschte Elemente** " verschoben wurde, kann ein Form-Objekt die [IMAPIMessageSite:: GetSiteStatus](imapimessagesite-getsitestatus.md) -Methode aufrufen, um zu bestimmen, ob das DELETE_IS_MOVE-Flag zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="5ad17-121">To determine whether the message **DeleteMessage** acted on was deleted or moved to a **Deleted Items** folder, a form object can call the [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) method to determine whether the DELETE_IS_MOVE flag was returned.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="5ad17-122">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="5ad17-122">Notes to implementers</span></span>

<span data-ttu-id="5ad17-123">Wenn die Implementierung der **DeleteMessage** -Methode eines Formular Viewers zur nächsten Nachricht wechselt, nachdem eine Nachricht gelöscht wurde, sollte die Implementierung die [IMAPIViewContext:: ActivateNext](imapiviewcontext-activatenext.md) -Methode aufrufen und das VCDIR_DELETE-Flag vor dem Ausführen von der tatsächliche Löschvorgang.</span><span class="sxs-lookup"><span data-stu-id="5ad17-123">If a form viewer's implementation of the **DeleteMessage** method moves to the next message after it deletes a message, the implementation should call the [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) method and pass the VCDIR_DELETE flag before performing the actual deletion.</span></span> <span data-ttu-id="5ad17-124">Wenn die **DeleteMessage** -Implementierung eines Formular Viewers die gelöschte Nachricht (beispielsweise in einen Ordner " **Gelöschte Elemente** ") verschiebt, muss die Implementierung Änderungen an der Nachricht speichern, wenn die Nachricht geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="5ad17-124">If a form viewer's implementation of **DeleteMessage** moves the deleted message (for example, to a **Deleted Items** folder), the implementation must save changes to the message if the message was modified.</span></span> 
  
<span data-ttu-id="5ad17-125">Eine typische Implementierung von **DeleteMessage** führt die folgenden Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="5ad17-125">A typical implementation of **DeleteMessage** performs the following tasks:</span></span> 
  
1. <span data-ttu-id="5ad17-126">Wenn die Implementierung die Nachricht verschiebt, ruft Sie die [IPersistMessage:: Save](ipersistmessage-save.md) -Methode auf und **übergibt NULL** im _pMessage_ -Parameter und **true** im _fSameAsLoad_ -Parameter.</span><span class="sxs-lookup"><span data-stu-id="5ad17-126">If the implementation is moving the message, it calls the [IPersistMessage::Save](ipersistmessage-save.md) method, passing **null** in the  _pMessage_ parameter and **true** in the  _fSameAsLoad_ parameter.</span></span> 
    
2. <span data-ttu-id="5ad17-127">Die **IMAPIViewContext:: ActivateNext** -Methode wird aufgerufen, und das VCDIR_DELETE-Flag wird im _ulDir_ -Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="5ad17-127">It calls the **IMAPIViewContext::ActivateNext** method, passing the VCDIR_DELETE flag in the  _ulDir_ parameter.</span></span> 
    
3. <span data-ttu-id="5ad17-128">Wenn der **ActivateNext** -Aufruf fehlschlägt, wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5ad17-128">If the **ActivateNext** call fails, it returns.</span></span> <span data-ttu-id="5ad17-129">Wenn **ActivateNext** den Wert S_FALSE zurückgibt, wird die [IPersistMessage:: HandsOffMessage](ipersistmessage-handsoffmessage.md) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="5ad17-129">If **ActivateNext** returns S_FALSE, it calls the [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) method.</span></span> 
    
4. <span data-ttu-id="5ad17-130">Die Nachricht wird gelöscht oder verschoben.</span><span class="sxs-lookup"><span data-stu-id="5ad17-130">It deletes or moves the message.</span></span>
    
<span data-ttu-id="5ad17-131">Rufen Sie die Windows- [GetWindowRect](https://msdn.microsoft.com/library/ms633519) -Funktion auf, um die vom Fenster eines Formulars verwendete **Rect** -Struktur abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5ad17-131">To obtain the **RECT** structure used by a form's window, call the Windows [GetWindowRect](https://msdn.microsoft.com/library/ms633519) function.</span></span> 
  
<span data-ttu-id="5ad17-132">Eine Liste der Schnittstellen im Zusammenhang mit Formular Servern finden Sie unter [MAPI-Formular Schnittstellen](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="5ad17-132">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5ad17-133">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="5ad17-133">MFCMAPI reference</span></span>

<span data-ttu-id="5ad17-134">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="5ad17-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5ad17-135">**Datei**</span><span class="sxs-lookup"><span data-stu-id="5ad17-135">**File**</span></span>|<span data-ttu-id="5ad17-136">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="5ad17-136">**Function**</span></span>|<span data-ttu-id="5ad17-137">**Comment**</span><span class="sxs-lookup"><span data-stu-id="5ad17-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5ad17-138">MyMAPIFormViewer. cpp</span><span class="sxs-lookup"><span data-stu-id="5ad17-138">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="5ad17-139">CMyMAPIFormViewer::D eleteMessage</span><span class="sxs-lookup"><span data-stu-id="5ad17-139">CMyMAPIFormViewer::DeleteMessage</span></span>  <br/> |<span data-ttu-id="5ad17-140">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="5ad17-140">Not implemented.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5ad17-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5ad17-141">See also</span></span>



[<span data-ttu-id="5ad17-142">IMAPIMessageSite::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="5ad17-142">IMAPIMessageSite::GetSiteStatus</span></span>](imapimessagesite-getsitestatus.md)
  
[<span data-ttu-id="5ad17-143">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="5ad17-143">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="5ad17-144">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="5ad17-144">IPersistMessage::HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md)
  
[<span data-ttu-id="5ad17-145">IPersistMessage::Save</span><span class="sxs-lookup"><span data-stu-id="5ad17-145">IPersistMessage::Save</span></span>](ipersistmessage-save.md)
  
[<span data-ttu-id="5ad17-146">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5ad17-146">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="5ad17-147">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="5ad17-147">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="5ad17-148">MAPI-Formular Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="5ad17-148">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

