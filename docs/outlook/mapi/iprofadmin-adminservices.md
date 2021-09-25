---
title: IProfAdminAdminServices
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IProfAdmin.AdminServices
api_type:
- COM
ms.assetid: 87235fd2-6527-41a1-98ba-b951632a1c81
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: daa063ff580d75b33d6c0fc2a448dc5dfb95a4fe
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561404"
---
# <a name="iprofadminadminservices"></a>IProfAdmin::AdminServices

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bietet Zugriff auf ein Nachrichtendienst-Verwaltungsobjekt, um Änderungen an den Nachrichtendiensten in einem Profil vorzunehmen.
  
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
  
> [in] Ein Zeiger auf den Namen des zu ändernden Profils. Der  _Parameter lpszProfileName_ darf nicht NULL sein. 
    
 _lpszPassword_
  
> [in] Immer NULL. 
    
 _ulUIParam_
  
> [in] Ein Handle des übergeordneten Fensters für alle Dialogfelder oder Fenster, die von dieser Methode angezeigt werden.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Abruf des Nachrichtendienst-Verwaltungsobjekts steuert. Die folgenden Flags können festgelegt werden:
    
MAPI_DIALOG 
  
> Aktiviert die Anzeige einer Benutzeroberfläche. 
    
MAPI_UNICODE 
  
> Der Profilname hat das Unicode-Format. Wenn das flag MAPI_UNICODE nicht festgelegt ist, hat der Name das ANSI-Format.
    
 _lppServiceAdmin_
  
> [out] Ein Zeiger auf einen Zeiger auf ein Nachrichtendienst-Verwaltungsobjekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Nachrichtendienst-Verwaltungsobjekt wurde erfolgreich zurückgegeben.
    
MAPI_E_LOGON_FAILED 
  
> Das angegebene Profil ist nicht vorhanden, oder das Kennwort war falsch, und dem Benutzer konnte kein Dialogfeld angezeigt werden, um das richtige Kennwort anzufordern, da MAPI_DIALOG in  _ulFlags_ nicht festgelegt wurde.
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang abgebrochen, in der Regel durch Klicken auf die Schaltfläche **Abbrechen** in einem Dialogfeld. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IProfAdmin::AdminServices-Methode** ermöglicht den Zugriff auf ein Nachrichtendienst-Verwaltungsobjekt, um Konfigurationsänderungen an den Nachrichtendiensten in einem Profil vorzunehmen. 
  
 Der  _lpszPassword-Parameter_ muss NULL oder ein Zeiger auf eine leere Zeichenfolge sein. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Obwohl Sie einen [IMsgServiceAdmin-Zeiger](imsgserviceadminiunknown.md) abrufen können, indem Sie entweder diese Methode oder [IMAPISession::AdminServices](imapisession-adminservices.md)aufrufen, rufen Sie **IProfAdmin::AdminServices** auf, wenn Sie ausschließlich über einen Konfigurationsclient verfügen und keine Messagingfunktionen anbieten. **IProfAdmin::AdminServices** erstellt kein Sitzungsobjekt und lädt keine Dienstanbieter, wodurch die Leistung verbessert wird. 
  
**IProfAdmin::AdminServices** kann nicht zum Erstellen eines Profils verwendet werden. Daher müssen Sie ein vorhandenes gültiges Profil in  _lpszProfileName_ angeben. Wenn das angegebene Profil nicht vorhanden ist, gibt **IProfAdmin::AdminServices** MAPI_E_LOGON_FAILED zurück. 
  
Der Name des Profils kann bis zu 64 Zeichen lang sein und die folgenden Zeichen enthalten:
  
- Alle alphanumerischen Zeichen, einschließlich Akzentzeichen und Unterstrichzeichen. 
    
- Eingebettete Leerzeichen, aber keine führenden oder nachstehenden Leerzeichen.
    
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> | HrAddServiceToProfile  <br/> |MFCMAPI verwendet die **IProfAdmin::AdminServices-Methode,** um ein Nachrichtendienst-Verwaltungsobjekt für das ausgewählte Profil zu öffnen, um Dienste hinzuzufügen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPISession::AdminServices](imapisession-adminservices.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

