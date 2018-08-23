---
title: IMAPIViewContextSetAdviseSink
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.SetAdviseSink
api_type:
- COM
ms.assetid: 4799084a-b5d1-48c3-a889-b2f0e9d68c30
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 555bb4820dc36934fb28197b7e222633a5248125
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583183"
---
# <a name="imapiviewcontextsetadvisesink"></a><span data-ttu-id="dc0b9-103">IMAPIViewContext::SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="dc0b9-103">IMAPIViewContext::SetAdviseSink</span></span>

  
  
<span data-ttu-id="dc0b9-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dc0b9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dc0b9-105">Verwaltet ein Formular Registrierung Erhalt von Benachrichtigungen zu Änderungen im Viewer.</span><span class="sxs-lookup"><span data-stu-id="dc0b9-105">Manages a form's registration to receive notifications about changes in the viewer.</span></span> 
  
```cpp
HRESULT SetAdviseSink(
LPMAPIFORMADVISESINK pmvns
);
```

## <a name="parameters"></a><span data-ttu-id="dc0b9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc0b9-106">Parameters</span></span>

 <span data-ttu-id="dc0b9-107">_pmvns_</span><span class="sxs-lookup"><span data-stu-id="dc0b9-107">_pmvns_</span></span>
  
> <span data-ttu-id="dc0b9-108">[in] Zeiger auf ein Formular advise-Empfängerobjekt oder NULL.</span><span class="sxs-lookup"><span data-stu-id="dc0b9-108">[in] Pointer to a form advise sink object or NULL.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="dc0b9-109">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="dc0b9-109">Return value</span></span>

<span data-ttu-id="dc0b9-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="dc0b9-110">S_OK</span></span> 
  
> <span data-ttu-id="dc0b9-111">Die Registrierung oder die Löschung für Formular-Benachrichtigung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="dc0b9-111">The registration or cancellation for form notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dc0b9-112">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="dc0b9-112">Remarks</span></span>

<span data-ttu-id="dc0b9-113">Formularobjekte Aufrufen die **IMAPIViewContext::SetAdviseSink** -Methode, um entweder Register erfahren Sie mehr über die Änderungen im Formular-Viewer oder Abbrechen einer vorherigen Erfassung.</span><span class="sxs-lookup"><span data-stu-id="dc0b9-113">Form objects call the **IMAPIViewContext::SetAdviseSink** method to either register to learn about changes in the form viewer or cancel a prior registration.</span></span> <span data-ttu-id="dc0b9-114">Wenn _Pmvns_ auf NULL festgelegt ist, das Formular eine Registrierung abbrechen möchte.</span><span class="sxs-lookup"><span data-stu-id="dc0b9-114">When  _pmvns_ is set to NULL, the form wants to cancel a registration.</span></span> <span data-ttu-id="dc0b9-115">Wenn _Pmvns_ verweist auf ein gültiges Formular-Empfänger Advise, möchte, dass das Formular für zukünftige Benachrichtigungen registriert.</span><span class="sxs-lookup"><span data-stu-id="dc0b9-115">When  _pmvns_ points to a valid form advise sink, the form wants to register for future notifications.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="dc0b9-116">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="dc0b9-116">Notes to implementers</span></span>

<span data-ttu-id="dc0b9-117">Wenn **SetAdviseSink** enthält ein Formular advise-Empfängerzeiger, halten, um einen Verweis auf ein anderes **SetAdviseSink** aufgerufen wird, Benachrichtigung abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="dc0b9-117">When **SetAdviseSink** includes a form advise sink pointer, keep a reference to it until another **SetAdviseSink** call is made to cancel notification.</span></span> <span data-ttu-id="dc0b9-118">Senden Sie eine Benachrichtigung bei einer Änderung wird im Viewer und Laden Sie eine neue Nachricht.</span><span class="sxs-lookup"><span data-stu-id="dc0b9-118">Send a notification when a change occurs in your viewer and when you are loading a new message.</span></span> 
  
<span data-ttu-id="dc0b9-119">Weitere Informationen finden Sie unter [Senden und Empfangen von Formular Benachrichtigungen](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="dc0b9-119">For more information, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="dc0b9-120">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="dc0b9-120">MFCMAPI reference</span></span>

<span data-ttu-id="dc0b9-121">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="dc0b9-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="dc0b9-122">**Datei**</span><span class="sxs-lookup"><span data-stu-id="dc0b9-122">**File**</span></span>|<span data-ttu-id="dc0b9-123">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="dc0b9-123">**Function**</span></span>|<span data-ttu-id="dc0b9-124">**Comment**</span><span class="sxs-lookup"><span data-stu-id="dc0b9-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="dc0b9-125">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="dc0b9-125">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="dc0b9-126">CMyMAPIFormViewer::SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="dc0b9-126">CMyMAPIFormViewer::SetAdviseSink</span></span>  <br/> |<span data-ttu-id="dc0b9-127">MFCMAPI (engl.) implementiert die **IMAPIViewContext::SetAdviseSink** -Methode in dieser Funktion.</span><span class="sxs-lookup"><span data-stu-id="dc0b9-127">MFCMAPI implements the **IMAPIViewContext::SetAdviseSink** method in this function.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dc0b9-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dc0b9-128">See also</span></span>



[<span data-ttu-id="dc0b9-129">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="dc0b9-129">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

