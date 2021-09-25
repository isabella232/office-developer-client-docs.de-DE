---
title: IPersistMessageIsDirty
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IPersistMessage.IsDirty
api_type:
- COM
ms.assetid: 57f688db-3a1c-49ff-a15a-8508bda5de68
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: bf294c7243ddc3b418c1df9de3b6981c1b950fb8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596050"
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
  
> Das Formular weist Änderungen auf, die seit dem letzten Speichern vorgenommen wurden.
    
S_FALSE 
  
> Das Formular weist keine Änderungen auf, die seit dem letzten Speichern vorgenommen wurden.
    
## <a name="remarks"></a>HinwBemerkungeneise

Formularviewer rufen die **IPersistMessage::IsDirty-Methode** auf, um zu bestimmen, ob die Nachricht nicht gespeicherte Daten enthält. 
  
## <a name="see-also"></a>Siehe auch



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

