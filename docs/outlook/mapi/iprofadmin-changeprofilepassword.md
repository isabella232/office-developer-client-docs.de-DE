---
title: IProfAdminChangeProfilePassword
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IProfAdmin.ChangeProfilePassword
api_type:
- COM
ms.assetid: a41f707a-5c84-49aa-aeb6-469b2600e181
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3b6898962a9156e0da387e23108d4c4a38f34d65
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579761"
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
  
> [in] Ein Zeiger auf den Namen des Profils, das dem zu ändernden Kennwort zugeordnet ist.
    
 _lpszOldPassword_
  
> [in] Ein Zeiger auf das aktuelle Kennwort.
    
 _lpszNewPassword_
  
> [in] Ein Zeiger auf das neue Kennwort.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Typ der übergebenen Zeichenfolgen steuert. Das folgende Kennzeichen kann festgelegt werden:
    
MAPI_UNICODE 
  
> Der Profilname und die Kennwörter haben das Unicode-Format. Wenn das flag MAPI_UNICODE nicht festgelegt ist, haben diese Zeichenfolgen das ANSI-Format.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Wenn diese Methode aufgerufen wird, wird S_OK zurückgegeben. Es wird jedoch keine Aktion ausgeführt.
    
## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie diese Methode nicht. Die MAPI unterstützt keine Kennwörter für Profile.
  
## <a name="see-also"></a>Siehe auch



[IProfAdmin : IUnknown](iprofadminiunknown.md)

