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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328791"
---
# <a name="imapiviewadvisesinkonnewmessage"></a><span data-ttu-id="47c5a-103">IMAPIViewAdviseSink::OnNewMessage</span><span class="sxs-lookup"><span data-stu-id="47c5a-103">IMAPIViewAdviseSink::OnNewMessage</span></span>

  
  
<span data-ttu-id="47c5a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47c5a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="47c5a-105">Benachrichtigt den Formular Betrachter darüber, dass eine neue oder eine vorhandene Nachricht in ein Formular geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="47c5a-105">Notifies the form viewer that a new or an existing message has been loaded in a form.</span></span>
  
```cpp
HRESULT OnNewMessage( void );
```

## <a name="parameters"></a><span data-ttu-id="47c5a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="47c5a-106">Parameters</span></span>

<span data-ttu-id="47c5a-107">Keine</span><span class="sxs-lookup"><span data-stu-id="47c5a-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="47c5a-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="47c5a-108">Return value</span></span>

<span data-ttu-id="47c5a-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="47c5a-109">S_OK</span></span> 
  
> <span data-ttu-id="47c5a-110">Die Benachrichtigung wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="47c5a-110">The notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="47c5a-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="47c5a-111">Remarks</span></span>

<span data-ttu-id="47c5a-112">Formularobjekte rufen die **IMAPIViewAdviseSink:: OnNewMessage** -Methode immer dann auf, wenn eine Nachricht in einem Formular mit der [IPersistMessage:: InitNew](ipersistmessage-initnew.md) -oder [IPersistMessage:: Laden](ipersistmessage-load.md) -Methode geladen wird.</span><span class="sxs-lookup"><span data-stu-id="47c5a-112">Form objects call the **IMAPIViewAdviseSink::OnNewMessage** method whenever a message is loaded in a form using either the [IPersistMessage::InitNew](ipersistmessage-initnew.md) or [IPersistMessage::Load](ipersistmessage-load.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="47c5a-113">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="47c5a-113">Notes to implementers</span></span>

<span data-ttu-id="47c5a-114">Geben Sie den aktiven Zeiger auf das Form-Objekt frei, da es nicht mehr auf die Nachricht zeigt, die der Viewer zuvor angezeigt hat.</span><span class="sxs-lookup"><span data-stu-id="47c5a-114">Release your active pointer to the form object because it no longer points to the message your viewer was formerly viewing.</span></span> 
  
<span data-ttu-id="47c5a-115">Weitere Informationen zu Formular Benachrichtigungen finden Sie unter [senden und empfangen von Formular Benachrichtigungen](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="47c5a-115">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="47c5a-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="47c5a-116">See also</span></span>



[<span data-ttu-id="47c5a-117">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="47c5a-117">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)
  
[<span data-ttu-id="47c5a-118">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="47c5a-118">IPersistMessage::InitNew</span></span>](ipersistmessage-initnew.md)
  
[<span data-ttu-id="47c5a-119">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="47c5a-119">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="47c5a-120">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="47c5a-120">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

