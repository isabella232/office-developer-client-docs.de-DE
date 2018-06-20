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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b667f56553b717f1bc938b6ce045dbfdde8fdc0c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792339"
---
# <a name="imapistatuschangepassword"></a>IMAPIStatus:: ChangePassword

  
  
**Betrifft**: Outlook 
  
Ändert das Kennwort des Dienstanbieters ohne eine Benutzeroberfläche anzuzeigen. Diese Methode ist optional in Status-Objekten unterstützt, mit denen Dienstanbieter implementiert.
  
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
  
> [in] Ein Zeiger auf das neue Kennwort ein.
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die das Format der Kennwörter steuert. Das folgende Flag kann festgelegt werden:
    
PARAMETER MAPI_UNICODE 
  
> Die Kennwörter sind im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Kennwörter im ANSI-Format.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Änderung des Kennworts erfolgreich war.
    
MAPI_E_NO_ACCESS 
  
> Das alte Kennwort auf den _LpOldPass_ ist ungültig. 
    
MAPI_E_NO_SUPPORT 
  
> Das Statusobjekt unterstützt keine dieser Vorgang, wie durch die Abwesenheit des STATUS_CHANGE_PASSWORD-Flags in den Status des Objekts **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))-Eigenschaft angegeben.
    
## <a name="remarks"></a>Hinweise

Nicht alle Status Objekte unterstützen die **IMAPIStatus:: ChangePassword** -Methode. Es wird nur von Dienstanbietern unterstützt, die Clients ein Kennwort eingeben müssen. Keines der Status, die von MAPI implementierte Objekte unterstützt die Operation Kennwort ändern. 
  
 **ChangePassword** ändert ein Kennwort programmgesteuert ohne Benutzereingriff aus. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Remote-Transport-Anbieter implementieren **ChangePassword** gemäß hier. Es gibt keine besondere Aspekte. 
  
## <a name="see-also"></a>Siehe auch



[Kanonische PidTagResourceMethods-Eigenschaft](pidtagresourcemethods-canonical-property.md)
  
[IMAPIStatus: IMAPIProp](imapistatusimapiprop.md)

