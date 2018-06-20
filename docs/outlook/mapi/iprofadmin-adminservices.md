---
title: IProfAdminAdminServices
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.AdminServices
api_type:
- COM
ms.assetid: 87235fd2-6527-41a1-98ba-b951632a1c81
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7566bb075c2ef9903b5a376fd90f209c8683c31e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792757"
---
# <a name="iprofadminadminservices"></a>IProfAdmin::AdminServices

  
  
**Betrifft**: Outlook 
  
Bietet Zugriff auf ein Objekt "Message" Service Administration für die Änderung der Nachrichtendienste in einem Profil.
  
```cpp
HRESULT AdminServices(
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSERVICEADMIN FAR * lppServiceAdmin
);
```

## <a name="parameters"></a>Parameter

 _lpszProfileName_
  
> [in] Ein Zeiger auf den Namen des Profils geändert werden soll. Der Parameter _LpszProfileName_ darf nicht NULL sein. 
    
 _lpszPassword_
  
> [in] Immer NULL. 
    
 _ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster für alle Dialogfelder oder Windows, die diese Methode anzeigt.
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die das Abrufen des Message Service Administration-Objekts steuert. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_DIALOG 
  
> Ermöglicht die Anzeige einer Benutzeroberfläche. 
    
PARAMETER MAPI_UNICODE 
  
> Der Name der Benutzerprofildienst wird im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, ist der Name im ANSI-Format.
    
 _lppServiceAdmin_
  
> [out] Ein Zeiger auf einen Zeiger auf ein Objekt "Message" Service-Verwaltung.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Das Objekt "Message" Service Administration wurde erfolgreich zurückgegeben.
    
MAPI_E_LOGON_FAILED 
  
> Das angegebene Profil ist nicht vorhanden, oder das Kennwort war falsch und ein Dialogfeld konnte nicht angezeigt werden, die dem Benutzer das korrekte Kennwort anfordern, da MAPI_DIALOG in _UlFlags_nicht festgelegt wurde.
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang in der Regel durch Klicken auf die Schaltfläche " **Abbrechen** " in einem Dialogfeld abgebrochen. 
    
## <a name="remarks"></a>Hinweise

Die **IProfAdmin::AdminServices** -Methode ermöglicht den Zugriff auf ein Objekt "Message" Service Administration für die Änderung der Konfiguration der Nachrichtendienste in einem Profil. 
  
 Der Parameter _LpszPassword_ muss NULL oder einen Zeiger auf eine leere Zeichenfolge. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Obwohl Sie einen Zeiger [IMsgServiceAdmin](imsgserviceadminiunknown.md) durch Aufrufen dieser Methode oder [IMAPISession::AdminServices](imapisession-adminservices.md)abrufen können, rufen Sie **IProfAdmin::AdminServices** , wenn Sie unbedingt einen Konfiguration-Client und keine Messagingfeatures bieten. **IProfAdmin::AdminServices** erstellt ein Session-Objekt keine und lädt keine Dienstanbieter, die Leistung verbessert. 
  
Sie können keine **IProfAdmin::AdminServices** verwenden Sie zum Erstellen eines Profils. Daher müssen Sie ein vorhandenes Profil gültiges in _LpszProfileName_angeben. Wenn das angegebene Profil nicht vorhanden ist, gibt **IProfAdmin::AdminServices** MAPI_E_LOGON_FAILED zurück. 
  
Der Name des Profils kann bis zu 64 Zeichen lang sein und kann die folgenden Zeichen enthalten:
  
- Alle alphanumerischen Zeichen, einschließlich Akzent-Zeichen und das Unterstrichzeichen. 
    
- Leerzeichen, jedoch nicht führende oder nachfolgende Leerzeichen.
    
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> | HrAddServiceToProfile  <br/> |MFCMAPI (engl.) wird die **IProfAdmin::AdminServices** -Methode verwendet, um eine Nachricht Service Administration-Objekt für das ausgewählte Profil Dienste hinzufügen zu öffnen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPISession::AdminServices](imapisession-adminservices.md)
  
[IProfAdmin: IUnknown](iprofadminiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

