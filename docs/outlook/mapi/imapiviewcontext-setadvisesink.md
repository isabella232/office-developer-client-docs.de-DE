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
ms.openlocfilehash: 7ee641214e1eaae667af356fd8dbe51ff7dc7982
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419394"
---
# <a name="imapiviewcontextsetadvisesink"></a><span data-ttu-id="d9351-103">IMAPIViewContext::SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="d9351-103">IMAPIViewContext::SetAdviseSink</span></span>

  
  
<span data-ttu-id="d9351-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d9351-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d9351-105">Verwaltet die Registrierung eines Formulars, um Benachrichtigungen über Änderungen im Viewer zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d9351-105">Manages a form's registration to receive notifications about changes in the viewer.</span></span> 
  
```cpp
HRESULT SetAdviseSink(
LPMAPIFORMADVISESINK pmvns
);
```

## <a name="parameters"></a><span data-ttu-id="d9351-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9351-106">Parameters</span></span>

 <span data-ttu-id="d9351-107">_pmvns_</span><span class="sxs-lookup"><span data-stu-id="d9351-107">_pmvns_</span></span>
  
> <span data-ttu-id="d9351-108">[in] Zeiger auf ein Formular raten sink-Objekt oder NULL.</span><span class="sxs-lookup"><span data-stu-id="d9351-108">[in] Pointer to a form advise sink object or NULL.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d9351-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d9351-109">Return value</span></span>

<span data-ttu-id="d9351-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="d9351-110">S_OK</span></span> 
  
> <span data-ttu-id="d9351-111">Die Registrierung oder Der Abbruch der Formularbenachrichtigung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="d9351-111">The registration or cancellation for form notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d9351-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d9351-112">Remarks</span></span>

<span data-ttu-id="d9351-113">Form-Objekte rufen die **IMAPIViewContext::SetAdviseSink-Methode** auf, um sich entweder zu registrieren, um mehr über Änderungen in der Formularanzeige zu erfahren, oder um eine vorherige Registrierung abbricht.</span><span class="sxs-lookup"><span data-stu-id="d9351-113">Form objects call the **IMAPIViewContext::SetAdviseSink** method to either register to learn about changes in the form viewer or cancel a prior registration.</span></span> <span data-ttu-id="d9351-114">Wenn  _pmvns_ auf NULL festgelegt ist, möchte das Formular eine Registrierung abbrechen.</span><span class="sxs-lookup"><span data-stu-id="d9351-114">When  _pmvns_ is set to NULL, the form wants to cancel a registration.</span></span> <span data-ttu-id="d9351-115">Wenn  _pmvns_ auf eine gültige Formularsenke verweist, möchte das Formular für zukünftige Benachrichtigungen registriert werden.</span><span class="sxs-lookup"><span data-stu-id="d9351-115">When  _pmvns_ points to a valid form advise sink, the form wants to register for future notifications.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="d9351-116">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="d9351-116">Notes to implementers</span></span>

<span data-ttu-id="d9351-117">Wenn **SetAdviseSink** einen Formular-Hinweis-Senkenzeiger enthält, behalten Sie einen Verweis darauf bei, bis ein anderer **SetAdviseSink-Aufruf** zum Abbrechen der Benachrichtigung erfolgt ist.</span><span class="sxs-lookup"><span data-stu-id="d9351-117">When **SetAdviseSink** includes a form advise sink pointer, keep a reference to it until another **SetAdviseSink** call is made to cancel notification.</span></span> <span data-ttu-id="d9351-118">Senden Sie eine Benachrichtigung, wenn eine Änderung in Ihrem Viewer auftritt und Wenn Sie eine neue Nachricht laden.</span><span class="sxs-lookup"><span data-stu-id="d9351-118">Send a notification when a change occurs in your viewer and when you are loading a new message.</span></span> 
  
<span data-ttu-id="d9351-119">Weitere Informationen finden Sie unter [Senden und Empfangen von Formularbenachrichtigungen](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="d9351-119">For more information, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d9351-120">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="d9351-120">MFCMAPI reference</span></span>

<span data-ttu-id="d9351-121">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d9351-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d9351-122">**Datei**</span><span class="sxs-lookup"><span data-stu-id="d9351-122">**File**</span></span>|<span data-ttu-id="d9351-123">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="d9351-123">**Function**</span></span>|<span data-ttu-id="d9351-124">**Comment**</span><span class="sxs-lookup"><span data-stu-id="d9351-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d9351-125">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="d9351-125">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="d9351-126">CMyMAPIFormViewer::SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="d9351-126">CMyMAPIFormViewer::SetAdviseSink</span></span>  <br/> |<span data-ttu-id="d9351-127">MFCMAPI implementiert die **IMAPIViewContext::SetAdviseSink-Methode** in dieser Funktion.</span><span class="sxs-lookup"><span data-stu-id="d9351-127">MFCMAPI implements the **IMAPIViewContext::SetAdviseSink** method in this function.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d9351-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d9351-128">See also</span></span>



[<span data-ttu-id="d9351-129">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="d9351-129">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

