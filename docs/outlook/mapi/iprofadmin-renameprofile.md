---
title: IProfAdminRenameProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.RenameProfile
api_type:
- COM
ms.assetid: 2a575cac-dbfd-4f42-9c10-4b7e355a065e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 162f20485fc21cf8523b6d4a653e52c35f4b3d9a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419520"
---
# <a name="iprofadminrenameprofile"></a>IProfAdmin::RenameProfile

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Weist einem Profil einen neuen Namen zu.
  
```cpp
HRESULT RenameProfile(
  LPSTR lpszOldProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewProfileName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpszOldProfileName_
  
> [in] Ein Zeiger auf den aktuellen Namen des Umbenennungsprofils.
    
 _lpszOldPassword_
  
> [in] Immer NULL.
    
 _lpszNewProfileName_
  
> [in] Ein Zeiger auf den neuen Namen des Umbenennungsprofils.
    
 _ulUIParam_
  
> [in] Ein Handle zum übergeordneten Fenster aller Dialogfelder oder Fenster, die von dieser Methode angezeigt werden. 
    
 _ulFlags_
  
> [in] Immer NULL.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Profil wurde erfolgreich umbenannt.
    
MAPI_E_LOGON_FAILED 
  
> Das Profilkennwort ist falsch.
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang abgebrochen, in der Regel durch Klicken auf die **Schaltfläche** Abbrechen in einem Dialogfeld. 
    
## <a name="remarks"></a>Hinweise

Die **IProfAdmin::RenameProfile-Methode** weist einem Profil einen neuen Namen zu, sofern er einen hat. Wenn das umzubenennende Profil von einem Client verwendet wird, wenn **RenameProfile** aufgerufen wird, markiert **RenameProfile** das Profil und gibt S_OK zurück, anstatt den Umbenennungsvorgang zu versuchen, während das Profil verwendet wird. Wenn das Profil nicht mehr verwendet wird, weist **RenameProfile** ihm den neuen Namen zu. 
  
Die alten und neuen Namen des Profils können bis zu 64 Zeichen lang sein und die folgenden Zeichen enthalten:
  
- Alle alphanumerischen Zeichen, einschließlich Akzentzeichen und Unterstrichzeichen.
    
- Eingebettete Leerzeichen, jedoch keine führenden oder nachgestellten Leerzeichen.
    
Das  _lpszPassword_ sollte immer NULL oder ein Zeiger auf eine Zeichenfolge mit null Länge sein. 
  
## <a name="see-also"></a>Siehe auch



[IProfAdmin : IUnknown](iprofadminiunknown.md)

