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
ms.openlocfilehash: b3cdd9994de3e2a02a5302068881abce57a632a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792209"
---
# <a name="imapimessagesitegetmessage"></a><span data-ttu-id="84036-103">IMAPIMessageSite::GetMessage</span><span class="sxs-lookup"><span data-stu-id="84036-103">IMAPIMessageSite::GetMessage</span></span>

  
  
<span data-ttu-id="84036-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="84036-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="84036-105">Gibt die aktuelle Nachricht zurück.</span><span class="sxs-lookup"><span data-stu-id="84036-105">Returns the current message.</span></span>
  
```cpp
HRESULT GetMessage(
  LPMESSAGE FAR * ppmsg
);
```

## <a name="parameters"></a><span data-ttu-id="84036-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="84036-106">Parameters</span></span>

 <span data-ttu-id="84036-107">_ppmsg_</span><span class="sxs-lookup"><span data-stu-id="84036-107">_ppmsg_</span></span>
  
> <span data-ttu-id="84036-108">[out] Ein Zeiger auf einen Zeiger auf die zurückgegebene Schnittstelle für die Nachricht.</span><span class="sxs-lookup"><span data-stu-id="84036-108">[out] A pointer to a pointer to the returned interface for the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="84036-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="84036-109">Return value</span></span>

<span data-ttu-id="84036-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="84036-110">S_OK</span></span> 
  
> <span data-ttu-id="84036-111">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="84036-111">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="84036-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="84036-112">S_FALSE</span></span> 
  
> <span data-ttu-id="84036-113">Keine Meldung, die derzeit für das aufrufende Formular vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="84036-113">No message currently exists for the calling form.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="84036-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="84036-114">Remarks</span></span>

<span data-ttu-id="84036-115">Formulare rufen Sie die **IMAPIMessageSite::GetMessage** -Methode, um eine Nachricht-Schnittstelle für die aktuelle Nachricht zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="84036-115">Forms call the **IMAPIMessageSite::GetMessage** method to obtain a message interface for the current message.</span></span> <span data-ttu-id="84036-116">Die aktuelle Nachricht ist die gleiche Nachricht an, wie zuvor in der [IPersistMessage::InitNew](ipersistmessage-initnew.md), [IPersistMessage::Load](ipersistmessage-load.md)oder [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) -Methode übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="84036-116">The current message is the same message as was previously passed in the [IPersistMessage::InitNew](ipersistmessage-initnew.md), [IPersistMessage::Load](ipersistmessage-load.md), or [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) method.</span></span> 
  
 <span data-ttu-id="84036-117">**GetMessage** gibt S_FALSE zurück, wenn derzeit keine Meldung befindet.</span><span class="sxs-lookup"><span data-stu-id="84036-117">**GetMessage** returns S_FALSE if no message currently exists.</span></span> <span data-ttu-id="84036-118">Dieser Status kann auftreten, nach dem Anrufe an die [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) -Methode oder vor dem nächsten Aufruf von **IPersistMessage::Load** oder **IPersistMessage::SaveCompleted** erfolgt.</span><span class="sxs-lookup"><span data-stu-id="84036-118">This state can occur after calls to the [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) method or before the next call to **IPersistMessage::Load** or **IPersistMessage::SaveCompleted** is made.</span></span> 
  
<span data-ttu-id="84036-119">Eine Liste der Schnittstellen im Zusammenhang mit der Formular-Servern finden Sie unter [MAPI-Formulars Schnittstellen](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="84036-119">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="84036-120">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="84036-120">MFCMAPI reference</span></span>

<span data-ttu-id="84036-121">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="84036-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="84036-122">**Datei**</span><span class="sxs-lookup"><span data-stu-id="84036-122">**File**</span></span>|<span data-ttu-id="84036-123">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="84036-123">**Function**</span></span>|<span data-ttu-id="84036-124">**Comment**</span><span class="sxs-lookup"><span data-stu-id="84036-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="84036-125">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="84036-125">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="84036-126">CMyMAPIFormViewer::GetSession</span><span class="sxs-lookup"><span data-stu-id="84036-126">CMyMAPIFormViewer::GetSession</span></span>  <br/> |<span data-ttu-id="84036-127">MFCMAPI (engl.) verwendet die **IMAPIMessageSite::GetMessage** -Methode den Zeiger aktuell zwischengespeicherten Meldung zurückgegeben, sofern es vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="84036-127">MFCMAPI uses the **IMAPIMessageSite::GetMessage** method to return the currently cached message pointer, if it is available.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="84036-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="84036-128">See also</span></span>



[<span data-ttu-id="84036-129">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="84036-129">IPersistMessage::HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md)
  
[<span data-ttu-id="84036-130">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="84036-130">IPersistMessage::InitNew</span></span>](ipersistmessage-initnew.md)
  
[<span data-ttu-id="84036-131">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="84036-131">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
  
[<span data-ttu-id="84036-132">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="84036-132">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="84036-133">IPersistMessage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="84036-133">IPersistMessage::SaveCompleted</span></span>](ipersistmessage-savecompleted.md)
  
[<span data-ttu-id="84036-134">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="84036-134">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="84036-135">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="84036-135">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="84036-136">MAPI-Formularoberflächen</span><span class="sxs-lookup"><span data-stu-id="84036-136">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

