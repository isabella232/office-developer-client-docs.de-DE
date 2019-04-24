---
title: IProfAdminCopyProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.CopyProfile
api_type:
- COM
ms.assetid: f4846dc3-0236-44ed-a1b1-8c13d48fb58a
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c3c4ac10003aad8949de94e0f144410af10078b1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309569"
---
# <a name="iprofadmincopyprofile"></a>IProfAdmin::CopyProfile

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Kopiert ein Profil.
  
```cpp
HRESULTCopyProfile(
  LPSTR lpszOldProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewProfileName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpszOldProfileName_
  
> in Ein Zeiger auf den Namen des zu kopierende Profils.
    
 _lpszOldPassword_
  
> in Ein Zeiger auf das Kennwort des zu kopierende Profils.
    
 _lpszNewProfileName_
  
> in Ein Zeiger auf den neuen Namen des kopierten Profils.
    
 _ulUIParam_
  
> in Ein Handle für das übergeordnete Fenster aller von dieser Methode angezeigten Dialogfelder oder Fenster.
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die das Kopieren des Profils steuert. Die folgenden Flags können festgelegt werden:
    
MAPI_DIALOG 
  
> Zeigt ein Dialogfeld an, in dem der Benutzer das richtige Kennwort des zu kopierenden Profils auffordert. Wenn dieses Flag nicht festgelegt ist, wird kein Dialogfeld angezeigt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Profil wurde erfolgreich kopiert.
    
MAPI_E_ACCESS_DENIED 
  
> Der neue Profilname ist derselbe wie der eines vorhandenen Profils.
    
MAPI_E_LOGON_FAILED 
  
> Das Kennwort für das zu kopierende Profil ist falsch, und dem Benutzer kann kein Dialogfeld angezeigt werden, das das richtige Kennwort anfordert, da MAPI_DIALOG nicht im _ulFlags_ -Parameter festgelegt wurde. 
    
MAPI_E_NOT_FOUND 
  
> Das angegebene Profil ist nicht vorhanden.
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang abgebrochen, indem er in einem Dialogfeld auf die Schaltfläche **Abbrechen** geklickt hat. 
    
## <a name="remarks"></a>Bemerkungen

Die **IProfAdmin:: CopyProfile** -Methode erstellt eine Kopie des Profils, auf die von _lpszOldProfileName_verwiesen wird, und gibt ihr den Namen, auf den _lpszNewProfileName_verweist. Beim Kopieren eines Profils wird die Kopie mit dem gleichen Kennwort wie das Original kopiert.
  
Der Name des ursprünglichen Profils, sein Kennwort und die Kopie können bis zu 64 Zeichen lang sein und die folgenden Zeichen enthalten:
  
- Alle alphanumerischen Zeichen, einschließlich Akzentzeichen und der Unterstrich.
    
- Eingebettete Leerzeichen, aber keine führenden oder nachstehenden Leerzeichen.
    
Profil Kennwörter werden auf allen Betriebssystemen nicht unterstützt. Auf Betriebssystemen, die Profil Kennwörter nicht unterstützen, kann _LPSZOLDPASSWORD_ NULL oder ein Zeiger auf eine leere Zeichenfolge sein. 
  
Wenn _lpszOldPassword_ auf NULL festgelegt ist, erfordert das zu kopierende Profil ein Kennwort, und das MAPI_DIALOG-Flag wird festgelegt; ein Dialogfeld, in dem der Benutzer aufgefordert wird, das Kennwort anzugeben, wird angezeigt. Wenn ein Kennwort erforderlich ist, aber _lpszOldPassword_ auf NULL festgelegt ist und das MAPI_DIALOG-Flag nicht festgelegt ist, gibt **CopyProfile** MAPI_E_LOGON_FAILED zurück. 
  
## <a name="see-also"></a>Siehe auch



[IProfAdmin : IUnknown](iprofadminiunknown.md)

