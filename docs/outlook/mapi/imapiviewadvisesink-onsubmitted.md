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
ms.openlocfilehash: ebde06d0d22320ecb5edb633cf8d04aaeec2a841
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433983"
---
# <a name="imapiviewadvisesinkonsubmitted"></a><span data-ttu-id="091f2-103">IMAPIViewAdviseSink::OnSubmitted</span><span class="sxs-lookup"><span data-stu-id="091f2-103">IMAPIViewAdviseSink::OnSubmitted</span></span>

  
  
<span data-ttu-id="091f2-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="091f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="091f2-105">Benachrichtigt den Formular Betrachter darüber, dass die aktuelle Nachricht an den MAPI-Spooler übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="091f2-105">Notifies the form viewer that the current message has been submitted to the MAPI spooler.</span></span>
  
```cpp
HRESULT OnSubmitted( void );
```

## <a name="parameters"></a><span data-ttu-id="091f2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="091f2-106">Parameters</span></span>

<span data-ttu-id="091f2-107">Keine</span><span class="sxs-lookup"><span data-stu-id="091f2-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="091f2-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="091f2-108">Return value</span></span>

<span data-ttu-id="091f2-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="091f2-109">S_OK</span></span> 
  
> <span data-ttu-id="091f2-110">Die Benachrichtigung wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="091f2-110">The notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="091f2-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="091f2-111">Remarks</span></span>

<span data-ttu-id="091f2-112">Ein Form-Objekt ruft die **IMAPIViewAdviseSink:: onsubmitted** -Methode nach einem Aufruf von [IMAPIMessageSite:: SubmitMessage](imapimessagesite-submitmessage.md) wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="091f2-112">A form object calls the **IMAPIViewAdviseSink::OnSubmitted** method after a call to [IMAPIMessageSite::SubmitMessage](imapimessagesite-submitmessage.md) has returned successfully.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="091f2-113">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="091f2-113">Notes to implementers</span></span>

<span data-ttu-id="091f2-114">Nachdem **onsubmitted** aufgerufen wurde, können Sie davon ausgehen, dass die Nachricht aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="091f2-114">After **OnSubmitted** is called, you can continue on the assumption that the message has been updated.</span></span> <span data-ttu-id="091f2-115">Aktualisieren Sie Ihre Fenster, um alle aufgetretenen Änderungen widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="091f2-115">Update your windows to reflect any changes that have occurred.</span></span> 
  
<span data-ttu-id="091f2-116">Weitere Informationen zu Formular Benachrichtigungen finden Sie unter [senden und empfangen von Formular Benachrichtigungen](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="091f2-116">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="091f2-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="091f2-117">See also</span></span>



[<span data-ttu-id="091f2-118">IMAPIMessageSite::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="091f2-118">IMAPIMessageSite::SubmitMessage</span></span>](imapimessagesite-submitmessage.md)
  
[<span data-ttu-id="091f2-119">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="091f2-119">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

