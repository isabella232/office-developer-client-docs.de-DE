---
title: IProfAdminCreateProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.CreateProfile
api_type:
- COM
ms.assetid: 10cda14a-8f93-41e0-b1fb-500098bdc392
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b104c62eb617e6c68f85dea4ef6379c831733844
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404400"
---
# <a name="iprofadmincreateprofile"></a>IProfAdmin::CreateProfile

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt ein neues Profil.
  
```cpp
HRESULT CreateProfile(
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpszProfileName_
  
> [in] Ein Zeiger auf den Namen des neuen Profils.
    
 _lpszPassword_
  
> [in] Ein Zeiger auf das Kennwort des neuen Profils. 
    
 _ulUIParam_
  
> [in] Ein Handle zum übergeordneten Fenster aller Dialogfelder oder Fenster, die von dieser Methode angezeigt werden.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie das Profil erstellt wird. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_DEFAULT_SERVICES 
  
> MAPI sollte das neue Profil mit den Nachrichtendiensten auffüllen, die im Abschnitt [Standarddienste] der Datei Mapisvc.inf enthalten sind.
    
MAPI_DIALOG 
  
> Die Konfigurationseigenschaftsblätter der einzelnen Anbieter in den zu hinzufügende Nachrichtendiensten können angezeigt werden. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das neue Profil wurde erstellt.
    
MAPI_E_NO_ACCESS 
  
> Das angegebene neue Profil ist bereits vorhanden.
    
## <a name="remarks"></a>Hinweise

Die **IProfAdmin::CreateProfile-Methode** erstellt ein neues Profil. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können **CreateProfile zur** Installationszeit der Anwendung oder jederzeit während einer Sitzung aufrufen. Wenn diese Methode bei der Installation aufgerufen wird, stammen viele der Konfigurationseinstellungen aus der Konfigurationsdatei Mapisvc.inf. Wenn diese Methode während einer aktiven Sitzung aufgerufen wird, stammen die Einstellungen vom Benutzer, der über eine Reihe von Eigenschaftenblättern aufgefordert wird. 
  
Wenn das MAPI_DEFAULT_SERVICES im  _ulFlags-Parameter_ festgelegt ist, ruft **CreateProfile** die Nachrichtendienst-Einstiegspunktfunktion für jeden Nachrichtendienst im Abschnitt [Standarddienste] in der Datei Mapisvc.inf auf. Jede Nachrichtendienst-Einstiegspunktfunktion wird aufgerufen, wenn der  _ulContext-Parameter_ auf MSG_SERVICE_CREATE. 
  
Wenn sowohl die MAPI_DIALOG als auch MAPI_DEFAULT_SERVICES festgelegt sind, werden die Werte in den  _Parametern ulUIParam_ und  _ulFlags_ ebenfalls an die Einstiegspunktfunktion des Nachrichtendiensts übergeben. Die Nachrichtendienst-Einstiegspunktfunktionen werden nur aufgerufen, nachdem dem Profil alle verfügbaren Informationen aus der Datei Mapisvc.inf hinzugefügt wurden. 
  
Der Name des neuen Profils und sein Kennwort können bis zu 64 Zeichen lang sein und die folgenden Zeichen enthalten:
  
- Alle alphanumerischen Zeichen, einschließlich Akzentzeichen und Unterstrichzeichen.
    
- Eingebettete Leerzeichen, jedoch keine führenden oder nachgestellten Leerzeichen.
    
Der  _lpszPassword-Parameter_ muss NULL oder ein Zeiger auf eine Zeichenfolge mit null Länge sein. 
  
## <a name="see-also"></a>Siehe auch



[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)

