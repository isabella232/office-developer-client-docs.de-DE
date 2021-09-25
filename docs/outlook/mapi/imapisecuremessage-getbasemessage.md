---
title: IMAPISecureMessageGetBaseMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISecureMessage.GetBaseMessage
api_type:
- COM
ms.assetid: 573f40c5-e0d2-4281-8c22-10a1ae1f0dee
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: abbbc3e67cb82bec98e136093dc324d761bce956
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59613919"
---
# <a name="imapisecuremessagegetbasemessage"></a>IMAPISecureMessage::GetBaseMessage

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ruft die zugrunde liegende [IMessage : IMAPIProp,](imessageimapiprop.md) die diese [IMAPISecureMessage : IUnknown](imapisecuremessageiunknown.md) kapselt. 
  
```cpp
HRESULT GetBaseMessage(
  LPMMESSAGE FAR * ppmsg
);
```

## <a name="parameters"></a>Parameter

 _ppmsg_
  
> [out] Ein Objekt für sichere Nachrichten.
    
## <a name="return-value"></a>Rückgabewert

S_OK
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="see-also"></a>Siehe auch



[IMAPISecureMessage : IUnknown](imapisecuremessageiunknown.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)

