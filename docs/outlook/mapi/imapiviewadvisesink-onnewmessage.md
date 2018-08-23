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
ms.openlocfilehash: bb373e4b666f44c432ac1b04c0449eb7f0408a19
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592934"
---
# <a name="imapiviewadvisesinkonnewmessage"></a><span data-ttu-id="0e5ac-103">IMAPIViewAdviseSink::OnNewMessage</span><span class="sxs-lookup"><span data-stu-id="0e5ac-103">IMAPIViewAdviseSink::OnNewMessage</span></span>

  
  
<span data-ttu-id="0e5ac-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0e5ac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0e5ac-105">Benachrichtigt dem Formular-Viewer, dass eine neue oder eine vorhandene Nachricht in einem Formular geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="0e5ac-105">Notifies the form viewer that a new or an existing message has been loaded in a form.</span></span>
  
```cpp
HRESULT OnNewMessage( void );
```

## <a name="parameters"></a><span data-ttu-id="0e5ac-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e5ac-106">Parameters</span></span>

<span data-ttu-id="0e5ac-107">Keine</span><span class="sxs-lookup"><span data-stu-id="0e5ac-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="0e5ac-108">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="0e5ac-108">Return value</span></span>

<span data-ttu-id="0e5ac-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="0e5ac-109">S_OK</span></span> 
  
> <span data-ttu-id="0e5ac-110">Die Benachrichtigung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="0e5ac-110">The notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0e5ac-111">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="0e5ac-111">Remarks</span></span>

<span data-ttu-id="0e5ac-112">Formularobjekte Aufrufen die **IMAPIViewAdviseSink::OnNewMessage** -Methode, wenn eine Nachricht in einem Formular mithilfe der [IPersistMessage::InitNew](ipersistmessage-initnew.md) oder [IPersistMessage::Load](ipersistmessage-load.md) -Methode geladen wird.</span><span class="sxs-lookup"><span data-stu-id="0e5ac-112">Form objects call the **IMAPIViewAdviseSink::OnNewMessage** method whenever a message is loaded in a form using either the [IPersistMessage::InitNew](ipersistmessage-initnew.md) or [IPersistMessage::Load](ipersistmessage-load.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="0e5ac-113">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="0e5ac-113">Notes to implementers</span></span>

<span data-ttu-id="0e5ac-114">Freigeben Sie Ihrer aktiven Zeiger auf das Form-Objekt, da es nicht mehr auf die Nachricht verweist, die der Viewer früher angezeigt wurde.</span><span class="sxs-lookup"><span data-stu-id="0e5ac-114">Release your active pointer to the form object because it no longer points to the message your viewer was formerly viewing.</span></span> 
  
<span data-ttu-id="0e5ac-115">Weitere Informationen zum Formular Benachrichtigungen finden Sie unter [Senden und Empfangen von Formular Benachrichtigungen](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="0e5ac-115">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0e5ac-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0e5ac-116">See also</span></span>



[<span data-ttu-id="0e5ac-117">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0e5ac-117">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)
  
[<span data-ttu-id="0e5ac-118">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="0e5ac-118">IPersistMessage::InitNew</span></span>](ipersistmessage-initnew.md)
  
[<span data-ttu-id="0e5ac-119">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="0e5ac-119">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="0e5ac-120">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0e5ac-120">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

