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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309611"
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
  
> Das Formular enthält Änderungen, die seit dem letzten Speichern vorgenommen wurden.
    
S_FALSE 
  
> Das Formular verfügt nicht über Änderungen, die seit dem letzten Speichern vorgenommen wurden.
    
## <a name="remarks"></a>Bemerkungen

Formular Betrachter rufen die **IPersistMessage:: IsDirty** -Methode auf, um zu bestimmen, ob die Nachricht nicht gespeicherte Daten enthält. 
  
## <a name="see-also"></a>Siehe auch



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

