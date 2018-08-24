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
ms.openlocfilehash: 0d2ae556f4dd98b5f6e274a21c608d4ea364d4ec
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576204"
---
# <a name="ipersistmessageisdirty"></a>IPersistMessage::IsDirty

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Überprüft das Formular, damit die Änderungen, die seit dem letzten Speichervorgang vorgenommen wurden.
  
```cpp
HRESULT IsDirty( void );
```

## <a name="parameters"></a>Parameter

Keine
  
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Das Formular wurde geändert, die seit dem letzten Speichern vorgenommen wurden.
    
S_FALSE 
  
> Das Formular hat keine Änderungen, die seit dem letzten Speichern vorgenommen wurden.
    
## <a name="remarks"></a>Bemerkungen

Formular Viewer rufen Sie die **IPersistMessage::IsDirty** -Methode, um zu bestimmen, ob die Nachricht Daten vorliegen. 
  
## <a name="see-also"></a>Siehe auch



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

