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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 496732e334d2d39672048dd1a02346aaee4b70e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417028"
---
# <a name="imapimessagesitesubmitmessage"></a><span data-ttu-id="006ed-103">IMAPIMessageSite::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="006ed-103">IMAPIMessageSite::SubmitMessage</span></span>

  
  
<span data-ttu-id="006ed-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="006ed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="006ed-105">Fordert an, dass die aktuelle Nachricht zur Zustellung in die Warteschlange eingereiht wird.</span><span class="sxs-lookup"><span data-stu-id="006ed-105">Requests that the current message be queued for delivery.</span></span>
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="006ed-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="006ed-106">Parameters</span></span>

 <span data-ttu-id="006ed-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="006ed-107">_ulFlags_</span></span>
  
> <span data-ttu-id="006ed-108">[in] Eine Bitmaske mit Flags, die steuert, wie eine Nachricht übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="006ed-108">[in] A bitmask of flags that controls how a message is submitted.</span></span> <span data-ttu-id="006ed-109">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="006ed-109">The following flag can be set:</span></span>
    
<span data-ttu-id="006ed-110">FORCE_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="006ed-110">FORCE_SUBMIT</span></span> 
  
> <span data-ttu-id="006ed-111">MAPI sollte die Nachricht übermitteln, auch wenn sie möglicherweise nicht sofort gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="006ed-111">MAPI should submit the message even if it might not be sent immediately.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="006ed-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="006ed-112">Return value</span></span>

<span data-ttu-id="006ed-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="006ed-113">S_OK</span></span> 
  
> <span data-ttu-id="006ed-114">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="006ed-114">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="006ed-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="006ed-115">Remarks</span></span>

<span data-ttu-id="006ed-116">Formularobjekte rufen die **IMAPIMessageSite::SubmitMessage-Methode** auf, um anzuerlangen, dass eine Nachricht zur Zustellung in die Warteschlange gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="006ed-116">Form objects call the **IMAPIMessageSite::SubmitMessage** method to request that a message be queued for delivery.</span></span> <span data-ttu-id="006ed-117">Die Nachrichtenwebsite sollte die [IPersistMessage::HandsOffMessage-Methode](ipersistmessage-handsoffmessage.md) aufrufen, bevor die Nachricht übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="006ed-117">The message site should call the [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) method before submitting the message.</span></span> <span data-ttu-id="006ed-118">Die Nachricht muss nicht zuvor gespeichert worden sein, da **SubmitMessage** dazu führen sollte, dass die Nachricht gespeichert wird, wenn die Nachricht geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="006ed-118">The message does not need to have been previously saved, because **SubmitMessage** should cause the message to be saved if the message has been modified.</span></span> <span data-ttu-id="006ed-119">Nach der Rückgabe von **SubmitMessage** muss das Formular nach einer aktuellen Nachricht suchen und sich dann selbst schließen, wenn keine vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="006ed-119">After the return of **SubmitMessage**, the form must check for a current message and then dismiss itself if none exists.</span></span> 
  
<span data-ttu-id="006ed-120">Eine Liste der Schnittstellen im Zusammenhang mit Formularservern finden Sie unter [MAPI Form Interfaces](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="006ed-120">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="006ed-121">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="006ed-121">MFCMAPI reference</span></span>

<span data-ttu-id="006ed-122">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="006ed-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="006ed-123">**Datei**</span><span class="sxs-lookup"><span data-stu-id="006ed-123">**File**</span></span>|<span data-ttu-id="006ed-124">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="006ed-124">**Function**</span></span>|<span data-ttu-id="006ed-125">**Comment**</span><span class="sxs-lookup"><span data-stu-id="006ed-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="006ed-126">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="006ed-126">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="006ed-127">CMyMAPIFormViewer::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="006ed-127">CMyMAPIFormViewer::SubmitMessage</span></span>  <br/> |<span data-ttu-id="006ed-128">MFCMAPI verwendet die **IMAPIMessageSite::SubmitMessage-Methode,** um die Nachricht zu speichern.</span><span class="sxs-lookup"><span data-stu-id="006ed-128">MFCMAPI uses the **IMAPIMessageSite::SubmitMessage** method to save the message.</span></span> <span data-ttu-id="006ed-129">Zunächst wird die **IPersistMessage::HandsOffMessage-Methode** und dann **SubmitMessage aufruft.**</span><span class="sxs-lookup"><span data-stu-id="006ed-129">First, it calls the **IPersistMessage::HandsOffMessage** method, and then it calls **SubmitMessage**.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="006ed-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="006ed-130">See also</span></span>



[<span data-ttu-id="006ed-131">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="006ed-131">IPersistMessage::HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md)
  
[<span data-ttu-id="006ed-132">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="006ed-132">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="006ed-133">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="006ed-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="006ed-134">MAPI-Formularschnittstellen</span><span class="sxs-lookup"><span data-stu-id="006ed-134">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

