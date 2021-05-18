---
title: IPersistMessageIsDirty
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.IsDirty
api_type:
- COM
ms.assetid: 57f688db-3a1c-49ff-a15a-8508bda5de68
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 91985d3dc8a7816c3da3215e505097c57c63e035
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407571"
---
# <a name="ipersistmessageisdirty"></a>IPersistMessage::IsDirty

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Überprüft das Formular auf Änderungen, die seit dem letzten Speichern vorgenommen wurden.
  
```cpp
HRESULT IsDirty( void );
```

## <a name="parameters"></a>Parameter

Keine
  
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Formular hat Änderungen, die seit dem letzten Speichern vorgenommen wurden.
    
S_FALSE 
  
> Das Formular enthält keine Änderungen, die seit dem letzten Speichern vorgenommen wurden.
    
## <a name="remarks"></a>Hinweise

Formularbetrachter rufen die **IPersistMessage::IsDirty-Methode** auf, um zu bestimmen, ob die Nachricht nicht gespeicherte Daten enthält. 
  
## <a name="see-also"></a>Siehe auch



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

