---
title: IMAPIViewAdviseSinkOnNewMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnNewMessage
api_type:
- COM
ms.assetid: 0a2fb371-90ea-41dc-b2ab-051cf790e85a
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6a6f8f9d675bee362b4a9f1c5b7fc544fa66d7b0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419604"
---
# <a name="imapiviewadvisesinkonnewmessage"></a><span data-ttu-id="a29ae-103">IMAPIViewAdviseSink::OnNewMessage</span><span class="sxs-lookup"><span data-stu-id="a29ae-103">IMAPIViewAdviseSink::OnNewMessage</span></span>

  
  
<span data-ttu-id="a29ae-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a29ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a29ae-105">Benachrichtigt den Formular Betrachter darüber, dass eine neue oder eine vorhandene Nachricht in ein Formular geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="a29ae-105">Notifies the form viewer that a new or an existing message has been loaded in a form.</span></span>
  
```cpp
HRESULT OnNewMessage( void );
```

## <a name="parameters"></a><span data-ttu-id="a29ae-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a29ae-106">Parameters</span></span>

<span data-ttu-id="a29ae-107">Keine</span><span class="sxs-lookup"><span data-stu-id="a29ae-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="a29ae-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a29ae-108">Return value</span></span>

<span data-ttu-id="a29ae-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="a29ae-109">S_OK</span></span> 
  
> <span data-ttu-id="a29ae-110">Die Benachrichtigung wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a29ae-110">The notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a29ae-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a29ae-111">Remarks</span></span>

<span data-ttu-id="a29ae-112">Formularobjekte rufen die **IMAPIViewAdviseSink:: OnNewMessage** -Methode immer dann auf, wenn eine Nachricht in einem Formular mit der [IPersistMessage:: InitNew](ipersistmessage-initnew.md) -oder [IPersistMessage:: Laden](ipersistmessage-load.md) -Methode geladen wird.</span><span class="sxs-lookup"><span data-stu-id="a29ae-112">Form objects call the **IMAPIViewAdviseSink::OnNewMessage** method whenever a message is loaded in a form using either the [IPersistMessage::InitNew](ipersistmessage-initnew.md) or [IPersistMessage::Load](ipersistmessage-load.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="a29ae-113">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="a29ae-113">Notes to implementers</span></span>

<span data-ttu-id="a29ae-114">Geben Sie den aktiven Zeiger auf das Form-Objekt frei, da es nicht mehr auf die Nachricht zeigt, die der Viewer zuvor angezeigt hat.</span><span class="sxs-lookup"><span data-stu-id="a29ae-114">Release your active pointer to the form object because it no longer points to the message your viewer was formerly viewing.</span></span> 
  
<span data-ttu-id="a29ae-115">Weitere Informationen zu Formular Benachrichtigungen finden Sie unter [senden und empfangen von Formular Benachrichtigungen](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="a29ae-115">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a29ae-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a29ae-116">See also</span></span>



[<span data-ttu-id="a29ae-117">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a29ae-117">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)
  
[<span data-ttu-id="a29ae-118">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="a29ae-118">IPersistMessage::InitNew</span></span>](ipersistmessage-initnew.md)
  
[<span data-ttu-id="a29ae-119">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="a29ae-119">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="a29ae-120">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a29ae-120">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

