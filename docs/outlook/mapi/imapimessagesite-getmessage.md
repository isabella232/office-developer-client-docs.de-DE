---
title: IMAPIMessageSiteGetMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetMessage
api_type:
- COM
ms.assetid: 49d12c49-84f8-44ac-bc4a-2ee44a46f8c1
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 03dd0553d0203585850ac5c4f8c91c86ef60236a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409027"
---
# <a name="imapimessagesitegetmessage"></a><span data-ttu-id="428bb-103">IMAPIMessageSite::GetMessage</span><span class="sxs-lookup"><span data-stu-id="428bb-103">IMAPIMessageSite::GetMessage</span></span>

  
  
<span data-ttu-id="428bb-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="428bb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="428bb-105">Gibt die aktuelle Nachricht zurück.</span><span class="sxs-lookup"><span data-stu-id="428bb-105">Returns the current message.</span></span>
  
```cpp
HRESULT GetMessage(
  LPMESSAGE FAR * ppmsg
);
```

## <a name="parameters"></a><span data-ttu-id="428bb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="428bb-106">Parameters</span></span>

 <span data-ttu-id="428bb-107">_ppmsg_</span><span class="sxs-lookup"><span data-stu-id="428bb-107">_ppmsg_</span></span>
  
> <span data-ttu-id="428bb-108">Out Ein Zeiger auf einen Zeiger auf die zurückgegebene Schnittstelle für die Nachricht.</span><span class="sxs-lookup"><span data-stu-id="428bb-108">[out] A pointer to a pointer to the returned interface for the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="428bb-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="428bb-109">Return value</span></span>

<span data-ttu-id="428bb-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="428bb-110">S_OK</span></span> 
  
> <span data-ttu-id="428bb-111">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="428bb-111">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="428bb-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="428bb-112">S_FALSE</span></span> 
  
> <span data-ttu-id="428bb-113">Für das Anruf Formular ist derzeit keine Nachricht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="428bb-113">No message currently exists for the calling form.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="428bb-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="428bb-114">Remarks</span></span>

<span data-ttu-id="428bb-115">Formulare rufen die **IMAPIMessageSite:: getMessage** -Methode auf, um eine Nachrichten Schnittstelle für die aktuelle Nachricht abzurufen.</span><span class="sxs-lookup"><span data-stu-id="428bb-115">Forms call the **IMAPIMessageSite::GetMessage** method to obtain a message interface for the current message.</span></span> <span data-ttu-id="428bb-116">Die aktuelle Nachricht ist dieselbe Nachricht, die zuvor in der [IPersistMessage:: InitNew](ipersistmessage-initnew.md), [IPersistMessage:: Laden](ipersistmessage-load.md)oder [IPersistMessage: SaveCompleted](ipersistmessage-savecompleted.md) -Methode übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="428bb-116">The current message is the same message as was previously passed in the [IPersistMessage::InitNew](ipersistmessage-initnew.md), [IPersistMessage::Load](ipersistmessage-load.md), or [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) method.</span></span> 
  
 <span data-ttu-id="428bb-117">**GetMessage** gibt S_FALSE zurück, wenn keine Nachricht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="428bb-117">**GetMessage** returns S_FALSE if no message currently exists.</span></span> <span data-ttu-id="428bb-118">Dieser Zustand kann nach Aufrufen der [IPersistMessage:: HandsOffMessage](ipersistmessage-handsoffmessage.md) -Methode oder vor dem nächsten Aufruf von **IPersistMessage:: Laden** oder **IPersistMessage:: SaveCompleted** erfolgen.</span><span class="sxs-lookup"><span data-stu-id="428bb-118">This state can occur after calls to the [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) method or before the next call to **IPersistMessage::Load** or **IPersistMessage::SaveCompleted** is made.</span></span> 
  
<span data-ttu-id="428bb-119">Eine Liste der Schnittstellen im Zusammenhang mit Formular Servern finden Sie unter [MAPI-Formular Schnittstellen](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="428bb-119">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="428bb-120">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="428bb-120">MFCMAPI reference</span></span>

<span data-ttu-id="428bb-121">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="428bb-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="428bb-122">**Datei**</span><span class="sxs-lookup"><span data-stu-id="428bb-122">**File**</span></span>|<span data-ttu-id="428bb-123">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="428bb-123">**Function**</span></span>|<span data-ttu-id="428bb-124">**Comment**</span><span class="sxs-lookup"><span data-stu-id="428bb-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="428bb-125">MyMAPIFormViewer. cpp</span><span class="sxs-lookup"><span data-stu-id="428bb-125">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="428bb-126">CMyMAPIFormViewer:: getSession</span><span class="sxs-lookup"><span data-stu-id="428bb-126">CMyMAPIFormViewer::GetSession</span></span>  <br/> |<span data-ttu-id="428bb-127">MFCMAPI verwendet die **IMAPIMessageSite:: getMessage** -Methode, um den aktuell zwischengespeicherten Nachrichten Zeiger zurückzugeben, sofern dieser verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="428bb-127">MFCMAPI uses the **IMAPIMessageSite::GetMessage** method to return the currently cached message pointer, if it is available.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="428bb-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="428bb-128">See also</span></span>



[<span data-ttu-id="428bb-129">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="428bb-129">IPersistMessage::HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md)
  
[<span data-ttu-id="428bb-130">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="428bb-130">IPersistMessage::InitNew</span></span>](ipersistmessage-initnew.md)
  
[<span data-ttu-id="428bb-131">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="428bb-131">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
  
[<span data-ttu-id="428bb-132">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="428bb-132">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="428bb-133">IPersistMessage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="428bb-133">IPersistMessage::SaveCompleted</span></span>](ipersistmessage-savecompleted.md)
  
[<span data-ttu-id="428bb-134">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="428bb-134">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="428bb-135">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="428bb-135">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="428bb-136">MAPI-Formular Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="428bb-136">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

