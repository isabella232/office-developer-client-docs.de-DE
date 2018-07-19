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
ms.openlocfilehash: b5347205e10b44d62a7e11cbe2f4179970f1bd64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792121"
---
# <a name="imapiformadvise"></a><span data-ttu-id="05bf7-103">IMAPIForm::Advise</span><span class="sxs-lookup"><span data-stu-id="05bf7-103">IMAPIForm::Advise</span></span>

  
  
<span data-ttu-id="05bf7-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="05bf7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="05bf7-105">Registriert einen Formular-Viewer für Benachrichtigungen über Ereignisse, die Einfluss auf das Formular.</span><span class="sxs-lookup"><span data-stu-id="05bf7-105">Registers a form viewer for notifications about events that affect the form.</span></span>
  
```cpp
HRESULT Advise(
  LPMAPIVIEWADVISESINK pAdvise,
  ULONG FAR * pulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="05bf7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="05bf7-106">Parameters</span></span>

 <span data-ttu-id="05bf7-107">_pAdvise_</span><span class="sxs-lookup"><span data-stu-id="05bf7-107">_pAdvise_</span></span>
  
> <span data-ttu-id="05bf7-108">[in] Ein Zeiger auf eine Ansicht advise Empfängerobjekt, um nachfolgenden Benachrichtigungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="05bf7-108">[in] A pointer to a view advise sink object to receive the subsequent notifications.</span></span> 
    
 <span data-ttu-id="05bf7-109">_pulConnection_</span><span class="sxs-lookup"><span data-stu-id="05bf7-109">_pulConnection_</span></span>
  
> <span data-ttu-id="05bf7-110">[out] Ein Zeiger auf einen Wert ungleich NULL, der eine erfolgreiche benachrichtigungsregistrierung darstellt.</span><span class="sxs-lookup"><span data-stu-id="05bf7-110">[out] A pointer to a nonzero value that represents a successful notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="05bf7-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="05bf7-111">Return value</span></span>

<span data-ttu-id="05bf7-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="05bf7-112">S_OK</span></span> 
  
> <span data-ttu-id="05bf7-113">Die Registrierung erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="05bf7-113">The registration was successful.</span></span>
    
<span data-ttu-id="05bf7-114">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="05bf7-114">E_OUTOFMEMORY</span></span> 
  
> <span data-ttu-id="05bf7-115">Die Registrierung war nicht erfolgreich, da nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="05bf7-115">The registration was unsuccessful because of insufficient memory.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="05bf7-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="05bf7-116">Remarks</span></span>

<span data-ttu-id="05bf7-117">Formular Viewer Aufrufen eines Formulars **IMAPIForm::Advise** -Methode, um für die Benachrichtigung zu registrieren, falls sich das Formular.</span><span class="sxs-lookup"><span data-stu-id="05bf7-117">Form viewers call a form's **IMAPIForm::Advise** method to register for notification when changes occur to the form.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="05bf7-118">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="05bf7-118">Notes to implementers</span></span>

<span data-ttu-id="05bf7-119">Beibehalten einer Kopie der Ansicht advise-Empfängerzeiger im _pAdvise_ -Parameter übergeben werden, sodass Sie sie verwenden können, die entsprechende [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) -Methode aufrufen, wenn ein Ereignis auftritt.</span><span class="sxs-lookup"><span data-stu-id="05bf7-119">Keep a copy of the view advise sink pointer passed in the  _pAdvise_ parameter so that you can use it to call the appropriate [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) method when an event occurs.</span></span> <span data-ttu-id="05bf7-120">Aufruf der Ansicht Teilen des Empfängers [IUnknown:: AddRef](http://msdn.microsoft.com/de-de/library/ms691379%28VS.85%29.aspx) -Methode, die den Zeiger beibehalten werden, bis benachrichtigungsregistrierung abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="05bf7-120">Call the view advise sink's [IUnknown::AddRef](http://msdn.microsoft.com/de-de/library/ms691379%28VS.85%29.aspx) method to retain the pointer until notification registration is canceled.</span></span> <span data-ttu-id="05bf7-121">Legen Sie den Inhalt des Parameters _PulConnection_ auf eine Zahl ungleich NULL.</span><span class="sxs-lookup"><span data-stu-id="05bf7-121">Set the contents of the  _pulConnection_ parameter to a nonzero number.</span></span> 
  
<span data-ttu-id="05bf7-122">Viele Formulare implementieren Sie ein Objekt, um die Registrierung und nachfolgende Benachrichtigung über Ereignisse behandelt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="05bf7-122">Many forms implement a helper object to handle the registration and subsequent notification of events.</span></span> 
  
<span data-ttu-id="05bf7-123">Weitere Informationen zu den Benachrichtigungsprozess im Allgemeinen finden Sie unter [Event Notification in MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="05bf7-123">For more information about the notification process in general, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
<span data-ttu-id="05bf7-124">Weitere Informationen zu Benachrichtigungen und Formulare finden Sie unter [Senden und Empfangen von Formular Benachrichtigungen](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="05bf7-124">For more information about notification and forms, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="05bf7-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="05bf7-125">See also</span></span>



[<span data-ttu-id="05bf7-126">IMAPIForm::Unadvise</span><span class="sxs-lookup"><span data-stu-id="05bf7-126">IMAPIForm::Unadvise</span></span>](imapiform-unadvise.md)
  
[<span data-ttu-id="05bf7-127">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="05bf7-127">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)
  
[<span data-ttu-id="05bf7-128">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="05bf7-128">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


[<span data-ttu-id="05bf7-129">Ereignisbenachrichtigung in MAPI</span><span class="sxs-lookup"><span data-stu-id="05bf7-129">Event Notification in MAPI</span></span>](event-notification-in-mapi.md)
  
[<span data-ttu-id="05bf7-130">Senden und Empfangen von Formularbenachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="05bf7-130">Sending and Receiving Form Notifications</span></span>](sending-and-receiving-form-notifications.md)

