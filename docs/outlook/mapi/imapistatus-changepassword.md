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
  
Ändert das Kennwort eines Dienstanbieters, ohne eine Benutzeroberfläche anzuzeigen. Diese Methode wird optional in Status-Objekten unterstützt, die von Dienstanbietern implementiert werden.
  
```cpp
HRESULT ChangePassword(
  LPSTR lpOldPass,
  LPSTR lpNewPass,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpOldPass_
  
> in Ein Zeiger auf das alte Kennwort.
    
 _lpNewPass_
  
> in Ein Zeiger auf das neue Kennwort.
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die das Format der Kennwörter steuert. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die Kennwörter sind im Unicode-Format. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, sind die Kennwörter im ANSI-Format.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Kennwortänderung war erfolgreich.
    
MAPI_E_NO_ACCESS 
  
> Das alte Kennwort, auf das durch _lpOldPass_ verwiesen wird, ist ungültig. 
    
MAPI_E_NO_SUPPORT 
  
> Das Status-Objekt unterstützt diesen Vorgang nicht, wie durch das Fehlen des STATUS_CHANGE_PASSWORD-Flags in der **PR_RESOURCE_METHODS** ([pidtagresourcemethods (](pidtagresourcemethods-canonical-property.md))-Eigenschaft des Status-Objekts angegeben.
    
## <a name="remarks"></a>Bemerkungen

Nicht alle Status-Objekte unterstützen die **IMAPIStatus:: ChangePassword** -Methode. Er wird nur von Dienstanbietern unterstützt, für die Clients ein Kennwort eingeben müssen. Keines der von MAPI implementierten Statusobjekte unterstützt den Vorgang der Kennwortänderung. 
  
 **ChangePassword** ändert ein Kennwort programmgesteuert ohne Benutzereingriff. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Remote Transportanbieter implementieren **ChangePassword** wie hier angegeben. Besondere Überlegungen sind nicht möglich. 
  
## <a name="see-also"></a>Siehe auch



[Kanonische Pidtagresourcemethods (-Eigenschaft](pidtagresourcemethods-canonical-property.md)
  
[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

