---
title: IMAPISecureMessageGetBaseMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISecureMessage.GetBaseMessage
api_type:
- COM
ms.assetid: 573f40c5-e0d2-4281-8c22-10a1ae1f0dee
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a2da3f6851e45a70dcd4604396a85430c539a830
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428578"
---
# <a name="imapisecuremessagegetbasemessage"></a><span data-ttu-id="53c39-103">IMAPISecureMessage::GetBaseMessage</span><span class="sxs-lookup"><span data-stu-id="53c39-103">IMAPISecureMessage::GetBaseMessage</span></span>

  
  
<span data-ttu-id="53c39-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53c39-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53c39-105">Ruft die zugrunde liegende [IMessage : IMAPIProp](imessageimapiprop.md) ab, die diese [IMAPISecureMessage : IUnknown](imapisecuremessageiunknown.md) kapselt.</span><span class="sxs-lookup"><span data-stu-id="53c39-105">Retrieves the underlying [IMessage : IMAPIProp](imessageimapiprop.md) that this [IMAPISecureMessage : IUnknown](imapisecuremessageiunknown.md) is encapsulating.</span></span> 
  
```cpp
HRESULT GetBaseMessage(
  LPMMESSAGE FAR * ppmsg
);
```

## <a name="parameters"></a><span data-ttu-id="53c39-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="53c39-106">Parameters</span></span>

 <span data-ttu-id="53c39-107">_ppmsg_</span><span class="sxs-lookup"><span data-stu-id="53c39-107">_ppmsg_</span></span>
  
> <span data-ttu-id="53c39-108">[out] Ein sicheres Nachrichtenobjekt.</span><span class="sxs-lookup"><span data-stu-id="53c39-108">[out] A secure message object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="53c39-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="53c39-109">Return value</span></span>

<span data-ttu-id="53c39-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="53c39-110">S_OK</span></span>
  
> <span data-ttu-id="53c39-111">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="53c39-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="53c39-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53c39-112">See also</span></span>



[<span data-ttu-id="53c39-113">IMAPISecureMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="53c39-113">IMAPISecureMessage : IUnknown</span></span>](imapisecuremessageiunknown.md)
  
[<span data-ttu-id="53c39-114">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="53c39-114">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

