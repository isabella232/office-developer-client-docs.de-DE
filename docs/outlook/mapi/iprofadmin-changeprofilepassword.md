---
title: IProfAdminChangeProfilePassword
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.ChangeProfilePassword
api_type:
- COM
ms.assetid: a41f707a-5c84-49aa-aeb6-469b2600e181
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 41066d4418760a676fbc02241bfc12d83275da9d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572998"
---
# <a name="iprofadminchangeprofilepassword"></a>IProfAdmin::ChangeProfilePassword

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Veraltet. Ändert das Kennwort für ein Profil.
  
```cpp
HRESULT ChangeProfilePassword(
  LPSTR lpszProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewPassword,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpszProfileName_
  
> [in] Ein Zeiger auf den Namen des Profils, das Kennwort zu ändernden zugeordnet.
    
 _lpszOldPassword_
  
> [in] Ein Zeiger auf das aktuelle Kennwort.
    
 _lpszNewPassword_
  
> [in] Ein Zeiger auf das neue Kennwort ein.
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die den Typ der übergebenen Zeichenfolgen steuert. Das folgende Flag kann festgelegt werden:
    
PARAMETER MAPI_UNICODE 
  
> Der Name der Benutzerprofildienst und Kennwörter werden im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind diese Zeichenfolgen in ANSI-Format.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Wenn diese Methode aufgerufen wird, wird S_OK zurückgegeben. Es wird jedoch keine Aktion ausgeführt werden.
    
## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie diese Methode nicht. MAPI unterstützt keine Kennwörter für Profile.
  
## <a name="see-also"></a>Siehe auch



[IProfAdmin : IUnknown](iprofadminiunknown.md)

