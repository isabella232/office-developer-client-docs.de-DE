---
title: IMAPIViewAdviseSinkOnSaved
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnSaved
api_type:
- COM
ms.assetid: c327e31a-7b62-4e21-9b69-b27442f1eaca
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 0f9aa5d508afeaf5933c50763e1e42832ae4e3f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792495"
---
# <a name="imapiviewadvisesinkonsaved"></a><span data-ttu-id="a9432-103">IMAPIViewAdviseSink::OnSaved</span><span class="sxs-lookup"><span data-stu-id="a9432-103">IMAPIViewAdviseSink::OnSaved</span></span>

  
  
<span data-ttu-id="a9432-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a9432-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a9432-105">Benachrichtigt den Formular-Viewer, den die aktuelle Nachricht in einem Formular gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="a9432-105">Notifies the form viewer that the current message in a form has been saved.</span></span>
  
```cpp
HRESULT OnSaved( void );
```

## <a name="parameters"></a><span data-ttu-id="a9432-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9432-106">Parameters</span></span>

<span data-ttu-id="a9432-107">Keine</span><span class="sxs-lookup"><span data-stu-id="a9432-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="a9432-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a9432-108">Return value</span></span>

<span data-ttu-id="a9432-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="a9432-109">S_OK</span></span> 
  
> <span data-ttu-id="a9432-110">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="a9432-110">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a9432-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a9432-111">Remarks</span></span>

<span data-ttu-id="a9432-112">Ein Form-Objekt ruft die **IMAPIViewAdviseSink::OnSaved** -Methode auf, nachdem die aktuelle Nachricht in einem Formular erfolgreich gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="a9432-112">A form object calls the **IMAPIViewAdviseSink::OnSaved** method after the current message in a form has been successfully saved.</span></span> <span data-ttu-id="a9432-113">Dadurch werden Zuschauer zu ihren Windows Änderungen an der Nachricht entsprechend aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="a9432-113">Doing so permits viewers to update their windows to reflect changes to the message.</span></span> 
  
<span data-ttu-id="a9432-114">Weitere Informationen zum Formular Benachrichtigungen finden Sie unter [Senden und Empfangen von Formular Benachrichtigungen](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="a9432-114">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a9432-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9432-115">See also</span></span>



[<span data-ttu-id="a9432-116">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a9432-116">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

