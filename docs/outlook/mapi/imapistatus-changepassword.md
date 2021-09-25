---
title: IMAPIStatusChangePassword
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIStatus.ChangePassword
api_type:
- COM
ms.assetid: 0cd1026a-342d-4d05-91ed-d3decced5bf3
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c98f3c2d3f14893fc37ab9c876d41ed65de409fc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596169"
---
# <a name="imapistatuschangepassword"></a>IMAPIStatus::ChangePassword

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ändert das Kennwort eines Dienstanbieters, ohne eine Benutzeroberfläche anzuzeigen. Diese Methode wird optional in Statusobjekten unterstützt, die von Dienstanbietern implementiert werden.
  
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
  
> [in] Eine Bitmaske mit Flags, die das Format der Kennwörter steuert. Das folgende Kennzeichen kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die Kennwörter haben das Unicode-Format. Wenn das MAPI_UNICODE-Kennzeichen nicht festgelegt ist, haben die Kennwörter das ANSI-Format.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Kennwortänderung war erfolgreich.
    
MAPI_E_NO_ACCESS 
  
> Das alte Kennwort, auf das von  _lpOldPass_ verwiesen wird, ist ungültig. 
    
MAPI_E_NO_SUPPORT 
  
> Das Statusobjekt unterstützt diesen Vorgang nicht, wie durch das Fehlen des STATUS_CHANGE_PASSWORD Flags in der **Eigenschaft PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) des Statusobjekts angegeben.
    
## <a name="remarks"></a>HinwBemerkungeneise

Nicht alle Statusobjekte unterstützen die **IMAPIStatus::ChangePassword-Methode.** Es wird nur von Dienstanbietern unterstützt, die die Eingabe eines Kennworts durch Clients erfordern. Keines der Statusobjekte, die MAPI implementiert, unterstützen den Kennwortänderungsvorgang. 
  
 **ChangePassword** ändert ein Kennwort programmgesteuert ohne Benutzerinteraktion. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Remote-Transportanbieter implementieren **ChangePassword** wie hier angegeben. Es gibt keine besonderen Überlegungen. 
  
## <a name="see-also"></a>Siehe auch



[PidTagResourceMethods (kanonische Eigenschaft)](pidtagresourcemethods-canonical-property.md)
  
[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

