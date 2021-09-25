---
title: IProfAdminRenameProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IProfAdmin.RenameProfile
api_type:
- COM
ms.assetid: 2a575cac-dbfd-4f42-9c10-4b7e355a065e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5ad3c9ae2d42b0cc9fbc613b35b645ad50e809c8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596036"
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
  
> [in] Ein Zeiger auf den aktuellen Namen des umzubenennenden Profils.
    
 _lpszOldPassword_
  
> [in] Immer NULL.
    
 _lpszNewProfileName_
  
> [in] Ein Zeiger auf den neuen Namen des umzubenennenden Profils.
    
 _ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster aller Dialogfelder oder Fenster, die von dieser Methode angezeigt werden. 
    
 _ulFlags_
  
> [in] Immer NULL.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Profil wurde erfolgreich umbenannt.
    
MAPI_E_LOGON_FAILED 
  
> Das Profilkennwort ist falsch.
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang abgebrochen, in der Regel durch Klicken auf die Schaltfläche **Abbrechen** in einem Dialogfeld. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IProfAdmin::RenameProfile-Methode** weist einem Profil einen neuen Namen zu, sofern vorhanden. Wenn das umzubenennende Profil beim Aufrufen von **RenameProfile** von einem Client verwendet wird, markiert **RenameProfile** das Profil und gibt S_OK zurück, anstatt den Umbenennungsvorgang zu versuchen, während das Profil verwendet wird. Wenn das Profil nicht mehr verwendet wird, weist **RenameProfile** ihm den neuen Namen zu. 
  
Die alten und neuen Namen des Profils können bis zu 64 Zeichen lang sein und die folgenden Zeichen enthalten:
  
- Alle alphanumerischen Zeichen, einschließlich Akzentzeichen und Unterstrichzeichen.
    
- Eingebettete Leerzeichen, aber keine führenden oder nachstehenden Leerzeichen.
    
Das  _lpszPassword_ sollte immer NULL oder ein Zeiger auf eine leere Zeichenfolge sein. 
  
## <a name="see-also"></a>Siehe auch



[IProfAdmin : IUnknown](iprofadminiunknown.md)

