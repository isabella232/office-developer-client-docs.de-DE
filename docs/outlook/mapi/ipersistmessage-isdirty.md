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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e748427b39418a80cae88e98b4aa7eef6df24393
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792743"
---
# <a name="ipersistmessageisdirty"></a>IPersistMessage::IsDirty

  
  
**Betrifft**: Outlook 
  
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

