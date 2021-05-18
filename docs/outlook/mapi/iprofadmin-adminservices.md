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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2c504f98655e35af62810dd428e8e04878a36dec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422082"
---
# <a name="iprofadminadminservices"></a>IProfAdmin::AdminServices

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bietet Zugriff auf ein Nachrichtendienstverwaltungsobjekt zum Vornehmen von Änderungen an den Nachrichtendiensten in einem Profil.
  
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
  
> [in] Ein Zeiger auf den Namen des zu ändernde Profils. Der  _lpszProfileName-Parameter_ darf nicht NULL sein. 
    
 _lpszPassword_
  
> [in] Immer NULL. 
    
 _ulUIParam_
  
> [in] Ein Handle des übergeordneten Fensters für alle Dialogfelder oder Fenster, die von dieser Methode angezeigt werden.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Abruf des Nachrichtendienstverwaltungsobjekts steuert. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_DIALOG 
  
> Aktiviert die Anzeige einer Benutzeroberfläche. 
    
MAPI_UNICODE 
  
> Der Profilname ist im Unicode-Format. Wenn das MAPI_UNICODE nicht festgelegt ist, ist der Name im ANSI-Format.
    
 _lppServiceAdmin_
  
> [out] Ein Zeiger auf einen Zeiger auf ein Nachrichtendienstverwaltungsobjekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Nachrichtendienstverwaltungsobjekt wurde erfolgreich zurückgegeben.
    
MAPI_E_LOGON_FAILED 
  
> Das angegebene Profil ist nicht vorhanden, oder das Kennwort war falsch, und dem Benutzer konnte kein Dialogfeld angezeigt werden, um das richtige Kennwort anzugeben, da MAPI_DIALOG nicht in  _ulFlags_ festgelegt wurde.
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang abgebrochen, in der Regel durch Klicken auf die **Schaltfläche** Abbrechen in einem Dialogfeld. 
    
## <a name="remarks"></a>Hinweise

Die **IProfAdmin::AdminServices-Methode** bietet Zugriff auf ein Nachrichtendienstverwaltungsobjekt zum Vornehmen von Konfigurationsänderungen an den Nachrichtendiensten in einem Profil. 
  
 Der  _lpszPassword-Parameter_ muss NULL oder ein Zeiger auf eine Zeichenfolge mit null Länge sein. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Obwohl Sie einen [IMsgServiceAdmin-Zeiger](imsgserviceadminiunknown.md) abrufen können, indem Sie entweder diese Methode oder [IMAPISession::AdminServices](imapisession-adminservices.md)aufrufen, rufen Sie **IProfAdmin::AdminServices** auf, wenn Sie nur über einen Konfigurationsclient verfügen und keine Messagingfeatures anbieten. **IProfAdmin::AdminServices** erstellt kein Sitzungsobjekt und geladen keine Dienstanbieter, wodurch die Leistung verbessert wird. 
  
Sie können **IProfAdmin::AdminServices** nicht zum Erstellen eines Profils verwenden. Daher müssen Sie ein vorhandenes gültiges Profil in _lpszProfileName angeben._ Wenn das angegebene Profil nicht vorhanden ist, gibt **IProfAdmin::AdminServices** MAPI_E_LOGON_FAILED. 
  
Der Name des Profils kann bis zu 64 Zeichen lang sein und die folgenden Zeichen enthalten:
  
- Alle alphanumerischen Zeichen, einschließlich Akzentzeichen und Unterstrichzeichen. 
    
- Eingebettete Leerzeichen, jedoch keine führenden oder nachgestellten Leerzeichen.
    
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> | HrAddServiceToProfile  <br/> |MFCMAPI verwendet die **IProfAdmin::AdminServices-Methode,** um ein Nachrichtendienstverwaltungsobjekt für das ausgewählte Profil zum Hinzufügen von Diensten zu öffnen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPISession::AdminServices](imapisession-adminservices.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

