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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7ee641214e1eaae667af356fd8dbe51ff7dc7982
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351191"
---
# <a name="imapiviewcontextsetadvisesink"></a><span data-ttu-id="5c56f-103">IMAPIViewContext::SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="5c56f-103">IMAPIViewContext::SetAdviseSink</span></span>

  
  
<span data-ttu-id="5c56f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5c56f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5c56f-105">Verwaltet die Registrierung eines Formulars, um Benachrichtigungen zu Änderungen im Viewer zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5c56f-105">Manages a form's registration to receive notifications about changes in the viewer.</span></span> 
  
```cpp
HRESULT SetAdviseSink(
LPMAPIFORMADVISESINK pmvns
);
```

## <a name="parameters"></a><span data-ttu-id="5c56f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c56f-106">Parameters</span></span>

 <span data-ttu-id="5c56f-107">_pmvns_</span><span class="sxs-lookup"><span data-stu-id="5c56f-107">_pmvns_</span></span>
  
> <span data-ttu-id="5c56f-108">in Zeiger auf ein Formular Advise Sink-Objekt oder NULL.</span><span class="sxs-lookup"><span data-stu-id="5c56f-108">[in] Pointer to a form advise sink object or NULL.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5c56f-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5c56f-109">Return value</span></span>

<span data-ttu-id="5c56f-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="5c56f-110">S_OK</span></span> 
  
> <span data-ttu-id="5c56f-111">Die Registrierung oder Stornierung für die Formular Benachrichtigung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="5c56f-111">The registration or cancellation for form notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5c56f-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5c56f-112">Remarks</span></span>

<span data-ttu-id="5c56f-113">Formularobjekte rufen die **IMAPIViewContext:: SetAdviseSink** -Methode auf, um sich zu registrieren, um sich über Änderungen im Formular-Viewer zu informieren oder um eine vorherige Registrierung abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="5c56f-113">Form objects call the **IMAPIViewContext::SetAdviseSink** method to either register to learn about changes in the form viewer or cancel a prior registration.</span></span> <span data-ttu-id="5c56f-114">Wenn _pmvns_ auf NULL festgelegt ist, möchte das Formular eine Registrierung abbrechen.</span><span class="sxs-lookup"><span data-stu-id="5c56f-114">When  _pmvns_ is set to NULL, the form wants to cancel a registration.</span></span> <span data-ttu-id="5c56f-115">Wenn _pmvns_ auf eine gültige Form Advise-Senke zeigt, möchte das Formular für zukünftige Benachrichtigungen registrieren.</span><span class="sxs-lookup"><span data-stu-id="5c56f-115">When  _pmvns_ points to a valid form advise sink, the form wants to register for future notifications.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="5c56f-116">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="5c56f-116">Notes to implementers</span></span>

<span data-ttu-id="5c56f-117">Wenn **SetAdviseSink** einen Form Advise-Senk Zeiger enthält, behalten Sie einen Verweis darauf, bis ein weiterer **SetAdviseSink** -Aufruf zum Abbrechen der Benachrichtigung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="5c56f-117">When **SetAdviseSink** includes a form advise sink pointer, keep a reference to it until another **SetAdviseSink** call is made to cancel notification.</span></span> <span data-ttu-id="5c56f-118">Senden Sie eine Benachrichtigung, wenn eine Änderung in Ihrem Viewer auftritt und wenn Sie eine neue Nachricht laden.</span><span class="sxs-lookup"><span data-stu-id="5c56f-118">Send a notification when a change occurs in your viewer and when you are loading a new message.</span></span> 
  
<span data-ttu-id="5c56f-119">Weitere Informationen finden Sie unter [senden und empfangen von Formular Benachrichtigungen](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="5c56f-119">For more information, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5c56f-120">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="5c56f-120">MFCMAPI reference</span></span>

<span data-ttu-id="5c56f-121">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="5c56f-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5c56f-122">**Datei**</span><span class="sxs-lookup"><span data-stu-id="5c56f-122">**File**</span></span>|<span data-ttu-id="5c56f-123">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="5c56f-123">**Function**</span></span>|<span data-ttu-id="5c56f-124">**Comment**</span><span class="sxs-lookup"><span data-stu-id="5c56f-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5c56f-125">MyMAPIFormViewer. cpp</span><span class="sxs-lookup"><span data-stu-id="5c56f-125">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="5c56f-126">CMyMAPIFormViewer:: SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="5c56f-126">CMyMAPIFormViewer::SetAdviseSink</span></span>  <br/> |<span data-ttu-id="5c56f-127">MFCMAPI implementiert die **IMAPIViewContext:: SetAdviseSink** -Methode in dieser Funktion.</span><span class="sxs-lookup"><span data-stu-id="5c56f-127">MFCMAPI implements the **IMAPIViewContext::SetAdviseSink** method in this function.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5c56f-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5c56f-128">See also</span></span>



[<span data-ttu-id="5c56f-129">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="5c56f-129">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

