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
ms.openlocfilehash: c7124c8e3f2ced66d303321ff7aee8592a723a2b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317122"
---
# <a name="iprofadminchangeprofilepassword"></a>IProfAdmin::ChangeProfilePassword

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
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
  
> in Ein Zeiger auf den Namen des Profils, das dem zu ändernden Kennwort zugeordnet ist.
    
 _lpszOldPassword_
  
> in Ein Zeiger auf das aktuelle Kennwort.
    
 _lpszNewPassword_
  
> in Ein Zeiger auf das neue Kennwort.
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die den Typ der übergebenen Zeichenfolgen steuert. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Der Profilname und die Kennwörter sind im Unicode-Format. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, sind diese Zeichenfolgen im ANSI-Format.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Wenn diese Methode aufgerufen wird, wird S_OK zurückgegeben. Es wird jedoch keine Aktion ausgeführt.
    
## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Methode nicht. MAPI unterstützt keine Kennwörter für Profile.
  
## <a name="see-also"></a>Siehe auch



[IProfAdmin : IUnknown](iprofadminiunknown.md)

