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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c94c60cf9ff1adbe2b54bd85b228e21b4be0e6e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792756"
---
# <a name="iprofadminrenameprofile"></a>IProfAdmin::RenameProfile

  
  
**Betrifft**: Outlook 
  
Weist einen neuen Namen zu einem Profil.
  
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
  
> [in] Ein Zeiger auf den aktuellen Namen des Profils umbenennen.
    
 _lpszOldPassword_
  
> [in] Immer NULL.
    
 _lpszNewProfileName_
  
> [in] Ein Zeiger auf den neuen Namen des Profils umbenennen.
    
 _ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster für alle Dialogfelder oder Windows, die diese Methode anzeigt. 
    
 _ulFlags_
  
> [in] Immer NULL.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Das Profil wurde erfolgreich umbenannt.
    
MAPI_E_LOGON_FAILED 
  
> Das Profilkennwort ist falsch.
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang in der Regel durch Klicken auf die Schaltfläche " **Abbrechen** " in einem Dialogfeld abgebrochen. 
    
## <a name="remarks"></a>Bemerkungen

Die **IProfAdmin::RenameProfile** -Methode weist einen neuen Namen zu einem Profil, sofern vorhanden. Wenn das Profil Umbenennen von einem Client wird **RenameProfile** aufgerufen wird, **RenameProfile** markiert das Profil und S_OK wird anstelle den Umbenennungsvorgang versucht, während das Profil verwendet wird. Wenn das Profil nicht mehr verwendet wird, weist ihm **RenameProfile** den neuen Namen zu. 
  
Die alten und neuen Namen des Profils können bis zu 64 Zeichen lang sein und können die folgenden Zeichen enthalten:
  
- Alle alphanumerischen Zeichen, einschließlich Akzent-Zeichen und das Unterstrichzeichen.
    
- Leerzeichen, jedoch nicht führende oder nachfolgende Leerzeichen.
    
Die _LpszPassword_ sollte immer NULL oder einen Zeiger auf eine leere Zeichenfolge sein. 
  
## <a name="see-also"></a>Siehe auch



[IProfAdmin : IUnknown](iprofadminiunknown.md)

