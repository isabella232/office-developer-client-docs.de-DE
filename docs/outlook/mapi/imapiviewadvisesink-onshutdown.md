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
ms.openlocfilehash: f49ea23ed7fef91bcb360483611af2ee60429934
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592969"
---
# <a name="imapiviewadvisesinkonshutdown"></a><span data-ttu-id="5ae0e-103">IMAPIViewAdviseSink::OnShutdown</span><span class="sxs-lookup"><span data-stu-id="5ae0e-103">IMAPIViewAdviseSink::OnShutdown</span></span>

  
  
<span data-ttu-id="5ae0e-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5ae0e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5ae0e-105">Benachrichtigt dem Formular-Viewer, dass ein Formular geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="5ae0e-105">Notifies the form viewer that a form is being closed.</span></span>
  
```cpp
HRESULT OnShutdown( void );
```

## <a name="parameters"></a><span data-ttu-id="5ae0e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ae0e-106">Parameters</span></span>

<span data-ttu-id="5ae0e-107">Keine</span><span class="sxs-lookup"><span data-stu-id="5ae0e-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="5ae0e-108">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="5ae0e-108">Return value</span></span>

<span data-ttu-id="5ae0e-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="5ae0e-109">S_OK</span></span> 
  
> <span data-ttu-id="5ae0e-110">Die Benachrichtigung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="5ae0e-110">The notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5ae0e-111">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="5ae0e-111">Remarks</span></span>

<span data-ttu-id="5ae0e-112">Weitere Informationen zum Formular Benachrichtigungen finden Sie unter [Senden und Empfangen von Formular Benachrichtigungen](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="5ae0e-112">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5ae0e-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5ae0e-113">See also</span></span>



[<span data-ttu-id="5ae0e-114">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5ae0e-114">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

