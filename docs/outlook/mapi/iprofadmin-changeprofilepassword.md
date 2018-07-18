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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c57f945d16cc80c637b1a4074b25f9cf1fb1edc0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792761"
---
# <a name="iprofadminchangeprofilepassword"></a>IProfAdmin::ChangeProfilePassword

  
  
**Betrifft**: Outlook 
  
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
    
## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Methode nicht. MAPI unterstützt keine Kennwörter für Profile.
  
## <a name="see-also"></a>Siehe auch



[IProfAdmin : IUnknown](iprofadminiunknown.md)

