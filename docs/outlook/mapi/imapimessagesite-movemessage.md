---
title: IMAPIMessageSiteMoveMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.MoveMessage
api_type:
- COM
ms.assetid: cd4d7b11-fad0-4f05-a99e-9567abcab45c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c68e4fbda661a119416918a2c35d1780f1deccda
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382372"
---
# <a name="imapimessagesitemovemessage"></a><span data-ttu-id="43d1e-103">IMAPIMessageSite::MoveMessage</span><span class="sxs-lookup"><span data-stu-id="43d1e-103">IMAPIMessageSite::MoveMessage</span></span>

  
  
<span data-ttu-id="43d1e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="43d1e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="43d1e-105">Verschiebt die aktuelle Nachricht in einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="43d1e-105">Moves the current message to a folder.</span></span>
  
```cpp
HRESULT MoveMessage(
  LPFOLDER pFolderDestination,
  LPMAPIVIEWCONTEXT pViewContext,
  LPCRECT prcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="43d1e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="43d1e-106">Parameters</span></span>

 <span data-ttu-id="43d1e-107">_pFolderDestination_</span><span class="sxs-lookup"><span data-stu-id="43d1e-107">_pFolderDestination_</span></span>
  
> <span data-ttu-id="43d1e-108">[in] Ein Zeiger auf den Ordner, in dem die Nachricht verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="43d1e-108">[in] A pointer to the folder where the message is to be moved.</span></span>
    
 <span data-ttu-id="43d1e-109">_pViewContext_</span><span class="sxs-lookup"><span data-stu-id="43d1e-109">_pViewContext_</span></span>
  
> <span data-ttu-id="43d1e-110">[in] Ein Zeiger auf eine Ansicht Context-Objekt.</span><span class="sxs-lookup"><span data-stu-id="43d1e-110">[in] A pointer to a view context object.</span></span>
    
 <span data-ttu-id="43d1e-111">_prcPosRect_</span><span class="sxs-lookup"><span data-stu-id="43d1e-111">_prcPosRect_</span></span>
  
> <span data-ttu-id="43d1e-112">[in] Ein Zeiger auf ein [Rechteck](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) -Struktur, die im Fenstergröße und Position des aktuellen Formulars enthält.</span><span class="sxs-lookup"><span data-stu-id="43d1e-112">[in] A pointer to a [RECT](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) structure that contains the current form's window size and position.</span></span> <span data-ttu-id="43d1e-113">Das nächste Formular angezeigt wird auch dieses Fenster Rechteck verwendet.</span><span class="sxs-lookup"><span data-stu-id="43d1e-113">The next form displayed also uses this window rectangle.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="43d1e-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="43d1e-114">Return value</span></span>

<span data-ttu-id="43d1e-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="43d1e-115">S_OK</span></span> 
  
> <span data-ttu-id="43d1e-116">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="43d1e-116">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="43d1e-117">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="43d1e-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="43d1e-118">Der Vorgang wird von dieser Site Nachricht nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="43d1e-118">The operation is not supported by this message site.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="43d1e-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="43d1e-119">Remarks</span></span>

<span data-ttu-id="43d1e-120">Formularobjekte Aufrufen die **IMAPIMessageSite::MoveMessage** -Methode, um die aktuelle Nachricht in einen neuen Ordner zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="43d1e-120">Form objects call the **IMAPIMessageSite::MoveMessage** method to move the current message to a new folder.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="43d1e-121">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="43d1e-121">Notes to implementers</span></span>

<span data-ttu-id="43d1e-122">Ein Formular Viewer-Implementierung von **MoveMessage** muss die [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) -Methode und übergeben die Kennzeichen VCDIR_MOVE vor dem Verschieben tatsächlich der Nachricht in einen neuen Ordner aufrufen.</span><span class="sxs-lookup"><span data-stu-id="43d1e-122">A form viewer's implementation of **MoveMessage** must call the [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) method, passing the VCDIR_MOVE flag, before actually moving the message to a new folder.</span></span> <span data-ttu-id="43d1e-123">Rufen Sie die Windows [GetWindowRect](https://msdn.microsoft.com/library/ms633519) -Funktion, um die **Rechteck** -Struktur, die von einem Formular zugrunde Fenster verwendet zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="43d1e-123">To obtain the **RECT** structure used by a form's window, call the Windows [GetWindowRect](https://msdn.microsoft.com/library/ms633519) function.</span></span> 
  
<span data-ttu-id="43d1e-124">Eine Liste der Schnittstellen im Zusammenhang mit der Formular-Servern finden Sie unter [MAPI-Formulars Schnittstellen](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="43d1e-124">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="43d1e-125">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="43d1e-125">Notes to callers</span></span>

<span data-ttu-id="43d1e-126">Nach der Rückgabe von **MoveMessage**müssen Formulare für eine aktuelle Nachricht überprüfen und dann schließen, wenn keines vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="43d1e-126">Following the return of **MoveMessage**, forms must check for a current message and then dismiss themselves if none exists.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="43d1e-127">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="43d1e-127">MFCMAPI reference</span></span>

<span data-ttu-id="43d1e-128">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="43d1e-128">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="43d1e-129">**Datei**</span><span class="sxs-lookup"><span data-stu-id="43d1e-129">**File**</span></span>|<span data-ttu-id="43d1e-130">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="43d1e-130">**Function**</span></span>|<span data-ttu-id="43d1e-131">**Kommentar**</span><span class="sxs-lookup"><span data-stu-id="43d1e-131">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="43d1e-132">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="43d1e-132">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="43d1e-133">CMyMAPIFormViewer::MoveMessage</span><span class="sxs-lookup"><span data-stu-id="43d1e-133">CMyMAPIFormViewer::MoveMessage</span></span>  <br/> |<span data-ttu-id="43d1e-134">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="43d1e-134">Not implemented.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="43d1e-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="43d1e-135">See also</span></span>



[<span data-ttu-id="43d1e-136">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="43d1e-136">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="43d1e-137">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="43d1e-137">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="43d1e-138">MFCMAPI als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="43d1e-138">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="43d1e-139">MAPI-Formularoberflächen</span><span class="sxs-lookup"><span data-stu-id="43d1e-139">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

