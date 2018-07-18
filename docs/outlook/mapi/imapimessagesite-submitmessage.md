---
title: IMAPIMessageSiteSubmitMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.SubmitMessage
api_type:
- COM
ms.assetid: 6b14c383-8bc6-4e86-bd92-0500272af40d
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 694ee8b12b9918502e60c0c6ea92992cc1062945
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792229"
---
# <a name="imapimessagesitesubmitmessage"></a><span data-ttu-id="cb789-103">IMAPIMessageSite::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="cb789-103">IMAPIMessageSite::SubmitMessage</span></span>

  
  
<span data-ttu-id="cb789-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cb789-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cb789-105">Fordert, dass die aktuelle Nachricht für die Übermittlung in die Warteschlange gestellt werden.</span><span class="sxs-lookup"><span data-stu-id="cb789-105">Requests that the current message be queued for delivery.</span></span>
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="cb789-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb789-106">Parameters</span></span>

 <span data-ttu-id="cb789-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cb789-107">_ulFlags_</span></span>
  
> <span data-ttu-id="cb789-108">[in] Eine Bitmaske aus Flags, die steuert, wie eine Nachricht gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="cb789-108">[in] A bitmask of flags that controls how a message is submitted.</span></span> <span data-ttu-id="cb789-109">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="cb789-109">The following flag can be set:</span></span>
    
<span data-ttu-id="cb789-110">FORCE_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="cb789-110">FORCE_SUBMIT</span></span> 
  
> <span data-ttu-id="cb789-111">MAPI sollten die Nachricht zu übermitteln, auch wenn es nicht sofort gesendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="cb789-111">MAPI should submit the message even if it might not be sent immediately.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cb789-112">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="cb789-112">Return value</span></span>

<span data-ttu-id="cb789-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="cb789-113">S_OK</span></span> 
  
> <span data-ttu-id="cb789-114">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="cb789-114">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cb789-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="cb789-115">Remarks</span></span>

<span data-ttu-id="cb789-116">Formularobjekte Aufrufen die **IMAPIMessageSite::SubmitMessage** -Methode, um anzufordern, dass eine Nachricht für die Übermittlung in die Warteschlange gestellt werden.</span><span class="sxs-lookup"><span data-stu-id="cb789-116">Form objects call the **IMAPIMessageSite::SubmitMessage** method to request that a message be queued for delivery.</span></span> <span data-ttu-id="cb789-117">Die Nachricht Website sollten die [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) -Methode aufrufen, bevor die Nachricht zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="cb789-117">The message site should call the [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) method before submitting the message.</span></span> <span data-ttu-id="cb789-118">Die Nachricht muss nicht zuvor gespeichert wurde, da **SubmitMessage** führen sollten die Nachricht gespeichert werden soll, wenn die Nachricht geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="cb789-118">The message does not need to have been previously saved, because **SubmitMessage** should cause the message to be saved if the message has been modified.</span></span> <span data-ttu-id="cb789-119">Nach der Rückgabe von **SubmitMessage**muss das Formular für eine aktuelle Nachricht überprüfen und schließen selbst dann, wenn keines vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="cb789-119">After the return of **SubmitMessage**, the form must check for a current message and then dismiss itself if none exists.</span></span> 
  
<span data-ttu-id="cb789-120">Eine Liste der Schnittstellen im Zusammenhang mit der Formular-Servern finden Sie unter [MAPI-Formulars Schnittstellen](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="cb789-120">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="cb789-121">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="cb789-121">MFCMAPI reference</span></span>

<span data-ttu-id="cb789-122">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="cb789-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="cb789-123">**Datei**</span><span class="sxs-lookup"><span data-stu-id="cb789-123">**File**</span></span>|<span data-ttu-id="cb789-124">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="cb789-124">**Function**</span></span>|<span data-ttu-id="cb789-125">**Comment**</span><span class="sxs-lookup"><span data-stu-id="cb789-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cb789-126">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="cb789-126">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="cb789-127">CMyMAPIFormViewer::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="cb789-127">CMyMAPIFormViewer::SubmitMessage</span></span>  <br/> |<span data-ttu-id="cb789-128">MFCMAPI (engl.) verwendet die **IMAPIMessageSite::SubmitMessage** -Methode, um die Nachricht zu speichern.</span><span class="sxs-lookup"><span data-stu-id="cb789-128">MFCMAPI uses the **IMAPIMessageSite::SubmitMessage** method to save the message.</span></span> <span data-ttu-id="cb789-129">Zunächst die **IPersistMessage::HandsOffMessage** -Methode aufgerufen, und ruft dann **SubmitMessage**.</span><span class="sxs-lookup"><span data-stu-id="cb789-129">First, it calls the **IPersistMessage::HandsOffMessage** method, and then it calls **SubmitMessage**.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cb789-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cb789-130">See also</span></span>



[<span data-ttu-id="cb789-131">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="cb789-131">IPersistMessage::HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md)
  
[<span data-ttu-id="cb789-132">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cb789-132">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="cb789-133">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="cb789-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="cb789-134">MAPI-Formularoberflächen</span><span class="sxs-lookup"><span data-stu-id="cb789-134">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

