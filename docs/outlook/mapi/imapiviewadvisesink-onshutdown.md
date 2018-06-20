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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2a09731dbd0ba2c5d6c1055a7c5ed11097c5ef27
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792485"
---
# <a name="imapiviewadvisesinkonshutdown"></a><span data-ttu-id="13d29-103">IMAPIViewAdviseSink::OnShutdown</span><span class="sxs-lookup"><span data-stu-id="13d29-103">IMAPIViewAdviseSink::OnShutdown</span></span>

  
  
<span data-ttu-id="13d29-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="13d29-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="13d29-105">Benachrichtigt dem Formular-Viewer, dass ein Formular geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="13d29-105">Notifies the form viewer that a form is being closed.</span></span>
  
```cpp
HRESULT OnShutdown( void );
```

## <a name="parameters"></a><span data-ttu-id="13d29-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="13d29-106">Parameters</span></span>

<span data-ttu-id="13d29-107">Keine</span><span class="sxs-lookup"><span data-stu-id="13d29-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="13d29-108">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="13d29-108">Return value</span></span>

<span data-ttu-id="13d29-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="13d29-109">S_OK</span></span> 
  
> <span data-ttu-id="13d29-110">Die Benachrichtigung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="13d29-110">The notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="13d29-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="13d29-111">Remarks</span></span>

<span data-ttu-id="13d29-112">Weitere Informationen zum Formular Benachrichtigungen finden Sie unter [Senden und Empfangen von Formular Benachrichtigungen](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="13d29-112">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="13d29-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13d29-113">See also</span></span>



[<span data-ttu-id="13d29-114">IMAPIViewAdviseSink: IUnknown</span><span class="sxs-lookup"><span data-stu-id="13d29-114">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

