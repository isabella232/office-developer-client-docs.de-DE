---
title: IMAPIStatusChangePassword
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus.ChangePassword
api_type:
- COM
ms.assetid: 0cd1026a-342d-4d05-91ed-d3decced5bf3
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2c824b6b994bfb31b5e6ac7fed0eeae88c47cdba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410357"
---
# <a name="imapistatuschangepassword"></a>IMAPIStatus::ChangePassword

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ändert das Kennwort eines Dienstanbieters, ohne dass eine Benutzeroberfläche angezeigt wird. Diese Methode wird optional in Statusobjekten unterstützt, die von Dienstanbietern implementiert werden.
  
```cpp
HRESULT ChangePassword(
  LPSTR lpOldPass,
  LPSTR lpNewPass,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpOldPass_
  
> [in] Ein Zeiger auf das alte Kennwort.
    
 _lpNewPass_
  
> [in] Ein Zeiger auf das neue Kennwort.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die das Format der Kennwörter steuert. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die Kennwörter sind im Unicode-Format. Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Kennwörter im ANSI-Format.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Kennwortänderung war erfolgreich.
    
MAPI_E_NO_ACCESS 
  
> Das alte Kennwort, auf das  _von lpOldPass verwiesen wird,_ ist ungültig. 
    
MAPI_E_NO_SUPPORT 
  
> Das status-Objekt unterstützt diesen Vorgang nicht, wie durch das Fehlen des STATUS_CHANGE_PASSWORD-Flag in der **eigenschaft PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) des Statusobjekts angegeben wird.
    
## <a name="remarks"></a>Hinweise

Nicht alle Statusobjekte unterstützen die **IMAPIStatus::ChangePassword-Methode.** Es wird nur von Dienstanbietern unterstützt, für die Clients ein Kennwort eingeben müssen. Keines der von MAPI implementierten Statusobjekte unterstützt den Kennwortänderungsvorgang. 
  
 **ChangePassword** ändert ein Kennwort programmgesteuert ohne Benutzerinteraktion. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Remote-Transport-Anbieter implementieren **ChangePassword wie** hier angegeben. Es gibt keine besonderen Überlegungen. 
  
## <a name="see-also"></a>Siehe auch



[PidTagResourceMethods (kanonische Eigenschaft)](pidtagresourcemethods-canonical-property.md)
  
[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

