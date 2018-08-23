---
title: IMAPIViewAdviseSinkOnSubmitted
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnSubmitted
api_type:
- COM
ms.assetid: a2401662-1ddc-40d8-a5a7-ceca24442bd4
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2aa1aca2816b8f0e148d35d1fcec761f621a2239
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579445"
---
# <a name="imapiviewadvisesinkonsubmitted"></a><span data-ttu-id="0b16d-103">IMAPIViewAdviseSink::OnSubmitted</span><span class="sxs-lookup"><span data-stu-id="0b16d-103">IMAPIViewAdviseSink::OnSubmitted</span></span>

  
  
<span data-ttu-id="0b16d-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0b16d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0b16d-105">Benachrichtigt dem Formular-Viewer, dass die aktuelle Nachricht an die MAPI-Warteschlange gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="0b16d-105">Notifies the form viewer that the current message has been submitted to the MAPI spooler.</span></span>
  
```cpp
HRESULT OnSubmitted( void );
```

## <a name="parameters"></a><span data-ttu-id="0b16d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b16d-106">Parameters</span></span>

<span data-ttu-id="0b16d-107">Keine</span><span class="sxs-lookup"><span data-stu-id="0b16d-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="0b16d-108">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="0b16d-108">Return value</span></span>

<span data-ttu-id="0b16d-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="0b16d-109">S_OK</span></span> 
  
> <span data-ttu-id="0b16d-110">Die Benachrichtigung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="0b16d-110">The notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0b16d-111">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="0b16d-111">Remarks</span></span>

<span data-ttu-id="0b16d-112">Ein Form-Objekt ruft die **IMAPIViewAdviseSink::OnSubmitted** -Methode auf, nachdem ein Aufruf von [IMAPIMessageSite::SubmitMessage](imapimessagesite-submitmessage.md) erfolgreich zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="0b16d-112">A form object calls the **IMAPIViewAdviseSink::OnSubmitted** method after a call to [IMAPIMessageSite::SubmitMessage](imapimessagesite-submitmessage.md) has returned successfully.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="0b16d-113">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="0b16d-113">Notes to implementers</span></span>

<span data-ttu-id="0b16d-114">Nachdem **OnSubmitted** aufgerufen wurde, können Sie auf der Annahme fortfahren, dass die Nachricht wurde aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="0b16d-114">After **OnSubmitted** is called, you can continue on the assumption that the message has been updated.</span></span> <span data-ttu-id="0b16d-115">Aktualisieren Sie Ihre Windows, um alle Änderungen, die aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="0b16d-115">Update your windows to reflect any changes that have occurred.</span></span> 
  
<span data-ttu-id="0b16d-116">Weitere Informationen zum Formular Benachrichtigungen finden Sie unter [Senden und Empfangen von Formular Benachrichtigungen](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="0b16d-116">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0b16d-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b16d-117">See also</span></span>



[<span data-ttu-id="0b16d-118">IMAPIMessageSite::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="0b16d-118">IMAPIMessageSite::SubmitMessage</span></span>](imapimessagesite-submitmessage.md)
  
[<span data-ttu-id="0b16d-119">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0b16d-119">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

