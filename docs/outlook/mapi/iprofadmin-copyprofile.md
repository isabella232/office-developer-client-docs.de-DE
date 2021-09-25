---
title: IProfAdminCopyProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IProfAdmin.CopyProfile
api_type:
- COM
ms.assetid: f4846dc3-0236-44ed-a1b1-8c13d48fb58a
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c82485e0da5457d069b6248b16b0fc3aa2a95a22
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59613800"
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
  
> [in] Ein Zeiger auf den Namen des zu kopierenden Profils.
    
 _lpszOldPassword_
  
> [in] Ein Zeiger auf das Kennwort des zu kopierenden Profils.
    
 _lpszNewProfileName_
  
> [in] Ein Zeiger auf den neuen Namen des kopierten Profils.
    
 _ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster aller Dialogfelder oder Fenster, die von dieser Methode angezeigt werden.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie das Profil kopiert wird. Die folgenden Flags können festgelegt werden:
    
MAPI_DIALOG 
  
> Zeigt ein Dialogfeld an, in dem der Benutzer aufgefordert wird, das richtige Kennwort des zu kopierenden Profils einzugeben. Wenn dieses Kennzeichen nicht festgelegt ist, wird kein Dialogfeld angezeigt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Profil wurde erfolgreich kopiert.
    
MAPI_E_ACCESS_DENIED 
  
> Der neue Profilname ist identisch mit dem eines vorhandenen Profils.
    
MAPI_E_LOGON_FAILED 
  
> Das Kennwort für das zu kopierende Profil ist falsch, und dem Benutzer konnte kein Dialogfeld angezeigt werden, um das richtige Kennwort anzufordern, da MAPI_DIALOG nicht im  _ulFlags-Parameter_ festgelegt wurde. 
    
MAPI_E_NOT_FOUND 
  
> Das angegebene Profil ist nicht vorhanden.
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang abgebrochen, in der Regel durch Klicken auf die Schaltfläche **Abbrechen** in einem Dialogfeld. 
    
## <a name="remarks"></a>Bemerkungen

Die **IProfAdmin::CopyProfile-Methode** erstellt eine Kopie des Profils, auf das von  _lpszOldProfileName_ verwiesen wird, und gibt ihr den Namen, auf den  _lpszNewProfileName_ verweist. Beim Kopieren eines Profils bleibt die Kopie mit demselben Kennwort wie das Original.
  
Der Name des ursprünglichen Profils, sein Kennwort und die Kopie können bis zu 64 Zeichen lang sein und die folgenden Zeichen enthalten:
  
- Alle alphanumerischen Zeichen, einschließlich Akzentzeichen und Unterstrichzeichen.
    
- Eingebettete Leerzeichen, aber keine führenden oder nachstehenden Leerzeichen.
    
Profil-Kennwörter werden nicht auf allen Betriebssystemen unterstützt. Auf Betriebssystemen, die keine Profilkennwörter unterstützen, kann  _lpszOldPassword_ NULL oder ein Zeiger auf eine leere Zeichenfolge sein. 
  
Wenn  _lpszOldPassword_ auf NULL festgelegt ist, erfordert das zu kopierende Profil ein Kennwort, und das MAPI_DIALOG Flag ist festgelegt. Es wird ein Dialogfeld angezeigt, in dem der Benutzer aufgefordert wird, das Kennwort anzugeben. Wenn ein Kennwort erforderlich ist,  _lpszOldPassword_ jedoch auf NULL festgelegt ist und das flag MAPI_DIALOG nicht festgelegt ist, gibt **CopyProfile** MAPI_E_LOGON_FAILED zurück. 
  
## <a name="see-also"></a>Siehe auch



[IProfAdmin : IUnknown](iprofadminiunknown.md)

