---
title: IMAPIViewAdviseSinkOnShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnShutdown
api_type:
- COM
ms.assetid: c9c3aecf-5e4b-407a-8ea1-6211b4c6e0a5
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b43c1b96130052a05ac390f10f545a66fe72b7fe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428522"
---
# <a name="imapiviewadvisesinkonshutdown"></a><span data-ttu-id="684ed-103">IMAPIViewAdviseSink::OnShutdown</span><span class="sxs-lookup"><span data-stu-id="684ed-103">IMAPIViewAdviseSink::OnShutdown</span></span>

  
  
<span data-ttu-id="684ed-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="684ed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="684ed-105">Benachrichtigt die Formularanzeige, dass ein Formular geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="684ed-105">Notifies the form viewer that a form is being closed.</span></span>
  
```cpp
HRESULT OnShutdown( void );
```

## <a name="parameters"></a><span data-ttu-id="684ed-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="684ed-106">Parameters</span></span>

<span data-ttu-id="684ed-107">Keine</span><span class="sxs-lookup"><span data-stu-id="684ed-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="684ed-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="684ed-108">Return value</span></span>

<span data-ttu-id="684ed-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="684ed-109">S_OK</span></span> 
  
> <span data-ttu-id="684ed-110">Die Benachrichtigung ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="684ed-110">The notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="684ed-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="684ed-111">Remarks</span></span>

<span data-ttu-id="684ed-112">Weitere Informationen zu Formularbenachrichtigungen finden Sie unter Senden und Empfangen [von Formularbenachrichtigungen](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="684ed-112">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="684ed-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="684ed-113">See also</span></span>



[<span data-ttu-id="684ed-114">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="684ed-114">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

