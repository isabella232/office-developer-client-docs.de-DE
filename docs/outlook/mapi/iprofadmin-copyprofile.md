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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: cd70f5ee7b58bdf0b1fd61b1056bfc77e3e35992
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792745"
---
# <a name="iprofadmincopyprofile"></a>IProfAdmin::CopyProfile

  
  
**Betrifft**: Outlook 
  
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
  
> [in] Ein Zeiger auf den Namen des Profils zu kopieren.
    
 _lpszOldPassword_
  
> [in] Ein Zeiger auf das Kennwort für das zu kopierende Profil.
    
 _lpszNewProfileName_
  
> [in] Ein Zeiger auf den neuen Namen der kopierten Profil.
    
 _ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster für alle Dialogfelder oder Windows, die diese Methode anzeigt.
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, wie das Profil kopiert wird. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_DIALOG 
  
> Zeigt ein Dialogfeld an, die der Benutzer für das korrekte Kennwort des Profils kopieren kann. Wenn dieses Flag nicht festgelegt ist, wird kein Dialogfeld angezeigt.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Das Profil wurde erfolgreich kopiert.
    
MAPI_E_ACCESS_DENIED 
  
> Der neue Profilname ist identisch mit der eines vorhandenen Profils.
    
MAPI_E_LOGON_FAILED 
  
> Das Kennwort für das zu kopierende Profil ist falsch, und ein Dialogfeld konnte nicht angezeigt werden, die dem Benutzer das korrekte Kennwort anfordern, da MAPI_DIALOG im _UlFlags_ -Parameter nicht festgelegt wurde. 
    
MAPI_E_NOT_FOUND 
  
> Das angegebene Profil ist nicht vorhanden.
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang in der Regel durch Klicken auf die Schaltfläche " **Abbrechen** " in einem Dialogfeld abgebrochen. 
    
## <a name="remarks"></a>Hinweise

Mit dem **IProfAdmin::CopyProfile** -Methode wird eine Kopie des Profils, auf die _LpszOldProfileName_, unter dem Namen mit _LpszNewProfileName_gezeigt. Kopieren eines Profils bewirkt, dass die Kopie mit das gleiche Kennwort wie das Original.
  
Der Name der ursprünglichen Profil, das Kennwort und die Kopie kann bis zu 64 Zeichen lang sein und kann die folgenden Zeichen enthalten:
  
- Alle alphanumerischen Zeichen, einschließlich Akzent-Zeichen und das Unterstrichzeichen.
    
- Leerzeichen, jedoch nicht führende oder nachfolgende Leerzeichen.
    
Profil Kennwörter werden auf allen Betriebssystemen nicht unterstützt. Unter Betriebssystemen, die keine für Profil Kennwörter Unterstützung, kann _LpszOldPassword_ NULL oder einen Zeiger auf eine leere Zeichenfolge. 
  
Wenn _LpszOldPassword_ auf NULL festgelegt ist, das Profil zu kopierenden erfordert ein Kennwort und das Flag MAPI_DIALOG festgelegt ist. Dialogfeld, in dem der Benutzer das Kennwort angeben, kann wird angezeigt. Wenn ein Kennwort erforderlich ist, aber _LpszOldPassword_ auf NULL festgelegt ist, und das Flag MAPI_DIALOG nicht festgelegt ist, gibt **CopyProfile** MAPI_E_LOGON_FAILED zurück. 
  
## <a name="see-also"></a>Siehe auch



[IProfAdmin: IUnknown](iprofadminiunknown.md)

