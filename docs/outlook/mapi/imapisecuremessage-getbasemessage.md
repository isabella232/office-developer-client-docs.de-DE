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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 70c8bd36142d18b541ad6a2e0ded3bebcfb6dbb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792289"
---
# <a name="imapisecuremessagegetbasemessage"></a>IMAPISecureMessage::GetBaseMessage

  
  
**Betrifft**: Outlook 
  
Ruft die zugrunde liegende [IMessage: IMAPIProp](imessageimapiprop.md) , das von diesem [IMAPISecureMessage: IUnknown](imapisecuremessageiunknown.md) encapsulating ist. 
  
```cpp
HRESULT GetBaseMessage(
  LPMMESSAGE FAR * ppmsg
);
```

## <a name="parameters"></a>Parameter

 _ppmsg_
  
> [out] Ein sicherer Message-Objekt.
    
## <a name="return-value"></a>R�ckgabewert

S_OK
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="see-also"></a>Siehe auch



[IMAPISecureMessage : IUnknown](imapisecuremessageiunknown.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)

