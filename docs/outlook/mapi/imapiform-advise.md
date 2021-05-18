---
title: IMAPIFormAdvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.Advise
api_type:
- COM
ms.assetid: 961318d6-bebe-4f4b-98ff-921cafc68d24
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2ed8bace97dee3842243ed835769e80e8aaf6b03
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329484"
---
# <a name="imapiformadvise"></a><span data-ttu-id="3f40e-103">IMAPIForm::Advise</span><span class="sxs-lookup"><span data-stu-id="3f40e-103">IMAPIForm::Advise</span></span>

  
  
<span data-ttu-id="3f40e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3f40e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3f40e-105">Registriert eine Formularanzeige für Benachrichtigungen über Ereignisse, die sich auf das Formular auswirken.</span><span class="sxs-lookup"><span data-stu-id="3f40e-105">Registers a form viewer for notifications about events that affect the form.</span></span>
  
```cpp
HRESULT Advise(
  LPMAPIVIEWADVISESINK pAdvise,
  ULONG FAR * pulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="3f40e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f40e-106">Parameters</span></span>

 <span data-ttu-id="3f40e-107">_pAdvise_</span><span class="sxs-lookup"><span data-stu-id="3f40e-107">_pAdvise_</span></span>
  
> <span data-ttu-id="3f40e-108">[in] Ein Zeiger auf ein Ansichtssenkenobjekt rät zum Empfangen der nachfolgenden Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="3f40e-108">[in] A pointer to a view advise sink object to receive the subsequent notifications.</span></span> 
    
 <span data-ttu-id="3f40e-109">_pulConnection_</span><span class="sxs-lookup"><span data-stu-id="3f40e-109">_pulConnection_</span></span>
  
> <span data-ttu-id="3f40e-110">[out] Ein Zeiger auf einen Wert ungleich Null, der eine erfolgreiche Benachrichtigungsregistrierung darstellt.</span><span class="sxs-lookup"><span data-stu-id="3f40e-110">[out] A pointer to a nonzero value that represents a successful notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3f40e-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3f40e-111">Return value</span></span>

<span data-ttu-id="3f40e-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="3f40e-112">S_OK</span></span> 
  
> <span data-ttu-id="3f40e-113">Die Registrierung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="3f40e-113">The registration was successful.</span></span>
    
<span data-ttu-id="3f40e-114">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="3f40e-114">E_OUTOFMEMORY</span></span> 
  
> <span data-ttu-id="3f40e-115">Die Registrierung war aufgrund unzureichenden Arbeitsspeichers nicht erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="3f40e-115">The registration was unsuccessful because of insufficient memory.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3f40e-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3f40e-116">Remarks</span></span>

<span data-ttu-id="3f40e-117">Formularbetrachter rufen die **IMAPIForm::Advise-Methode** eines Formulars auf, um sich für Benachrichtigungen zu registrieren, wenn Änderungen am Formular vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="3f40e-117">Form viewers call a form's **IMAPIForm::Advise** method to register for notification when changes occur to the form.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="3f40e-118">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="3f40e-118">Notes to implementers</span></span>

<span data-ttu-id="3f40e-119">Bewahren Sie eine Kopie des im  _pAdvise-Parameter_ übergebenen Ansichtssenkenzeigers auf, damit Sie die entsprechende [IMAPIViewAdviseSink-Methode](imapiviewadvisesinkiunknown.md) aufrufen können, wenn ein Ereignis auftritt.</span><span class="sxs-lookup"><span data-stu-id="3f40e-119">Keep a copy of the view advise sink pointer passed in the  _pAdvise_ parameter so that you can use it to call the appropriate [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) method when an event occurs.</span></span> <span data-ttu-id="3f40e-120">Rufen Sie die [IUnknown::AddRef-Methode](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) der Ansichtssenke auf, um den Zeiger zu behalten, bis die Benachrichtigungsregistrierung abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="3f40e-120">Call the view advise sink's [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) method to retain the pointer until notification registration is canceled.</span></span> <span data-ttu-id="3f40e-121">Legen Sie den Inhalt des  _Parameters pulConnection_ auf eine Zahl ungleich Null fest.</span><span class="sxs-lookup"><span data-stu-id="3f40e-121">Set the contents of the  _pulConnection_ parameter to a nonzero number.</span></span> 
  
<span data-ttu-id="3f40e-122">Viele Formulare implementieren ein Hilfsobjekt, um die Registrierung und nachfolgende Benachrichtigung von Ereignissen zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="3f40e-122">Many forms implement a helper object to handle the registration and subsequent notification of events.</span></span> 
  
<span data-ttu-id="3f40e-123">Weitere Informationen zum Benachrichtigungsprozess im Allgemeinen finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="3f40e-123">For more information about the notification process in general, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
<span data-ttu-id="3f40e-124">Weitere Informationen zu Benachrichtigungen und Formularen finden Sie unter Senden und Empfangen [von Formularbenachrichtigungen](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="3f40e-124">For more information about notification and forms, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3f40e-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3f40e-125">See also</span></span>



[<span data-ttu-id="3f40e-126">IMAPIForm::Unadvise</span><span class="sxs-lookup"><span data-stu-id="3f40e-126">IMAPIForm::Unadvise</span></span>](imapiform-unadvise.md)
  
[<span data-ttu-id="3f40e-127">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3f40e-127">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)
  
[<span data-ttu-id="3f40e-128">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3f40e-128">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


[<span data-ttu-id="3f40e-129">Ereignisbenachrichtigung in MAPI</span><span class="sxs-lookup"><span data-stu-id="3f40e-129">Event Notification in MAPI</span></span>](event-notification-in-mapi.md)
  
[<span data-ttu-id="3f40e-130">Senden und Empfangen von Formularbenachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="3f40e-130">Sending and Receiving Form Notifications</span></span>](sending-and-receiving-form-notifications.md)

