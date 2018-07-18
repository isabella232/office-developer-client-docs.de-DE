---
title: IMsgStoreNotifyNewMail
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.NotifyNewMail
api_type:
- COM
ms.assetid: d0d003b0-f12f-4422-b71f-26886169461f
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: bdda950cd1fab66db46590e0b9141bb3d2a75221
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792624"
---
# <a name="imsgstorenotifynewmail"></a><span data-ttu-id="169b6-103">IMsgStore::NotifyNewMail</span><span class="sxs-lookup"><span data-stu-id="169b6-103">IMsgStore::NotifyNewMail</span></span>

  
  
<span data-ttu-id="169b6-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="169b6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="169b6-p101">Informiert den Nachrichtenspeicher, den eine neue Nachricht empfangen hat. Diese Methode ist nur durch die MAPI-Warteschlange aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="169b6-p101">Informs the message store that a new message has arrived. This method is called only by the MAPI spooler.</span></span>
  
```cpp
HRESULT NotifyNewMail(
  LPNOTIFICATION lpNotification
);
```

## <a name="parameters"></a><span data-ttu-id="169b6-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="169b6-107">Parameters</span></span>

 <span data-ttu-id="169b6-108">_lpNotification_</span><span class="sxs-lookup"><span data-stu-id="169b6-108">_lpNotification_</span></span>
  
> <span data-ttu-id="169b6-109">[in] Ein Zeiger auf eine [Benachrichtigung](notification.md) -Struktur, die Benachrichtigung �ber eine neue Nachricht beschreibt.</span><span class="sxs-lookup"><span data-stu-id="169b6-109">[in] A pointer to a [NOTIFICATION](notification.md) structure that describes the new message notification.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="169b6-110">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="169b6-110">Return value</span></span>

<span data-ttu-id="169b6-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="169b6-111">S_OK</span></span> 
  
> <span data-ttu-id="169b6-112">Der Nachrichtenspeicher wurde erfolgreich benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="169b6-112">The message store was successfully notified.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="169b6-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="169b6-113">Remarks</span></span>

<span data-ttu-id="169b6-114">Die **IMsgStore::NotifyNewMail** -Methode wird aufgerufen, durch die MAPI-Warteschlange, um dem Nachrichtenspeicher zu informieren, dass eine Nachricht f�r die �bermittlung bereit ist.</span><span class="sxs-lookup"><span data-stu-id="169b6-114">The **IMsgStore::NotifyNewMail** method is called by the MAPI spooler to inform the message store that a message is ready for delivery.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="169b6-115">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="169b6-115">Notes to implementers</span></span>

<span data-ttu-id="169b6-p102">Wenn **NotifyNewMail** aufgerufen wird, senden Sie eine neue e-Mail-Benachrichtigung an alle registrierten Clients. Sie k�nnen die Benachrichtigung durch Aufrufen von [IMAPISupport::Notify](imapisupport-notify.md), wenn Sie die Methoden des Support-Objekts verwenden oder eine eigene Implementierung mit senden. Ein registrierter Clients ist eine [IMsgStore::Advise](imsgstore-advise.md) aufgerufen hat, und legen Sie den  _lpEntryID_ -Parameter auf NULL und der Parameter  _ulEventMask_ _fnevNewMail_.</span><span class="sxs-lookup"><span data-stu-id="169b6-p102">When **NotifyNewMail** is called, send a new mail notification to all registered clients. You can send the notification by calling [IMAPISupport::Notify](imapisupport-notify.md), if you elect to use the support object methods, or by using your own implementation. A registered client is one that has called [IMsgStore::Advise](imsgstore-advise.md) and set the  _lpEntryID_ parameter to NULL and the  _ulEventMask_ parameter to  _fnevNewMail_.</span></span> 
  
<span data-ttu-id="169b6-p103">Nicht �ndern oder den Speicher f�r die [Benachrichtigung](notification.md) -Struktur, die neue e-Mail-Benachrichtigung beschreibt, frei. Kopieren Sie die Struktur **NOTIFICATION** durch Aufrufen der Dienstprogrammfunktion [ScCopyNotifications](sccopynotifications.md) t�tigen Informationen in seine Member verwenden.</span><span class="sxs-lookup"><span data-stu-id="169b6-p103">Do not modify or free the memory for the [NOTIFICATION](notification.md) structure that describes the new mail notification. Copy the **NOTIFICATION** structure by calling the utility function [ScCopyNotifications](sccopynotifications.md) to make use of the information in its members.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="169b6-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="169b6-121">See also</span></span>



[<span data-ttu-id="169b6-122">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="169b6-122">IMAPISupport::Subscribe</span></span>](imapisupport-subscribe.md)
  
[<span data-ttu-id="169b6-123">IMAPISupport::Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="169b6-123">IMAPISupport::Unsubscribe</span></span>](imapisupport-unsubscribe.md)
  
[<span data-ttu-id="169b6-124">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="169b6-124">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="169b6-125">ScCopyNotifications</span><span class="sxs-lookup"><span data-stu-id="169b6-125">ScCopyNotifications</span></span>](sccopynotifications.md)
  
[<span data-ttu-id="169b6-126">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="169b6-126">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

