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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437238"
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
  
> [in] Ein Zeiger auf den Namen des zu kopierende Profils.
    
 _lpszOldPassword_
  
> [in] Ein Zeiger auf das Kennwort des zu kopierende Profils.
    
 _lpszNewProfileName_
  
> [in] Ein Zeiger auf den neuen Namen des kopierten Profils.
    
 _ulUIParam_
  
> [in] Ein Handle zum übergeordneten Fenster aller Dialogfelder oder Fenster, die von dieser Methode angezeigt werden.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie das Profil kopiert wird. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_DIALOG 
  
> Zeigt ein Dialogfeld an, in dem der Benutzer zum richtigen Kennwort des zu kopierenden Profils aufgefordert wird. Wenn dieses Kennzeichen nicht festgelegt ist, wird kein Dialogfeld angezeigt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Profil wurde erfolgreich kopiert.
    
MAPI_E_ACCESS_DENIED 
  
> Der neue Profilname ist identisch mit dem eines vorhandenen Profils.
    
MAPI_E_LOGON_FAILED 
  
> Das Kennwort für das zu kopierende Profil ist falsch, und dem Benutzer konnte kein Dialogfeld angezeigt werden, um das richtige Kennwort anzugeben, da MAPI_DIALOG nicht im  _ulFlags-Parameter festgelegt_ wurde. 
    
MAPI_E_NOT_FOUND 
  
> Das angegebene Profil ist nicht vorhanden.
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang abgebrochen, in der Regel durch Klicken auf die **Schaltfläche** Abbrechen in einem Dialogfeld. 
    
## <a name="remarks"></a>Hinweise

Die **IProfAdmin::CopyProfile-Methode** erstellt eine Kopie des Profils, auf das _von lpszOldProfileName_ verwiesen wird, und gibt ihm den Namen, auf den _lpszNewProfileName verweist._ Beim Kopieren eines Profils bleibt die Kopie mit demselben Kennwort wie das Original erhalten.
  
Der Name des ursprünglichen Profils, sein Kennwort und die Kopie können bis zu 64 Zeichen lang sein und die folgenden Zeichen enthalten:
  
- Alle alphanumerischen Zeichen, einschließlich Akzentzeichen und Unterstrichzeichen.
    
- Eingebettete Leerzeichen, jedoch keine führenden oder nachgestellten Leerzeichen.
    
Profilkennwörter werden nicht auf allen Betriebssystemen unterstützt. Auf Betriebssystemen, die keine Profilkennwörter unterstützen,  _kann lpszOldPassword_ NULL oder ein Zeiger auf eine Zeichenfolge mit null Länge sein. 
  
Wenn  _lpszOldPassword_ auf NULL festgelegt ist, erfordert das zu kopierende Profil ein Kennwort, und das MAPI_DIALOG ist festgelegt. Ein Dialogfeld, in dem der Benutzer zur Eingabe des Kennworts aufgefordert wird, wird angezeigt. Wenn ein Kennwort erforderlich ist,  _lpszOldPassword_ jedoch auf NULL festgelegt ist und das MAPI_DIALOG nicht festgelegt ist, gibt **CopyProfile** MAPI_E_LOGON_FAILED. 
  
## <a name="see-also"></a>Siehe auch



[IProfAdmin : IUnknown](iprofadminiunknown.md)

