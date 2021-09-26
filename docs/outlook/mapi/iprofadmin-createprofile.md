---
title: IProfAdminCreateProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IProfAdmin.CreateProfile
api_type:
- COM
ms.assetid: 10cda14a-8f93-41e0-b1fb-500098bdc392
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 06fe432cbf1c1a577d612b1212123f9db206ad29
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620569"
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
  
> [in] Ein Handle für das übergeordnete Fenster aller Dialogfelder oder Fenster, die von dieser Methode angezeigt werden.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie das Profil erstellt wird. Die folgenden Flags können festgelegt werden:
    
MAPI_DEFAULT_SERVICES 
  
> DIE MAPI sollte das neue Profil mit den Nachrichtendiensten auffüllen, die im Abschnitt [Standarddienste] der Datei Mapisvc.inf enthalten sind.
    
MAPI_DIALOG 
  
> Die Konfigurationseigenschaftenblätter der einzelnen Anbieter in den hinzuzufügenden Nachrichtendiensten können angezeigt werden. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das neue Profil wurde erstellt.
    
MAPI_E_NO_ACCESS 
  
> Das angegebene neue Profil ist bereits vorhanden.
    
## <a name="remarks"></a>Bemerkungen

Die **IProfAdmin::CreateProfile-Methode** erstellt ein neues Profil. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können **CreateProfile** zur Installationszeit der Anwendung oder jederzeit während einer Sitzung aufrufen. Wenn diese Methode zur Installationszeit aufgerufen wird, stammen viele der Konfigurationseinstellungen aus der Konfigurationsdatei Mapisvc.inf. Wenn diese Methode während einer aktiven Sitzung aufgerufen wird, stammen die Einstellungen von dem Benutzer, der durch eine Reihe von Eigenschaftenblättern aufgefordert wird. 
  
Wenn das flag MAPI_DEFAULT_SERVICES im  _UlFlags-Parameter_ festgelegt ist, ruft **CreateProfile** die Nachrichtendienst-Einstiegspunktfunktion für jeden Nachrichtendienst im Abschnitt [Standarddienste] in der Datei Mapisvc.inf auf. Jede Nachrichtendienst-Einstiegspunktfunktion wird aufgerufen, wobei der  _ulContext-Parameter_ auf MSG_SERVICE_CREATE festgelegt ist. 
  
Wenn die Flags MAPI_DIALOG und MAPI_DEFAULT_SERVICES festgelegt sind, werden die Werte in den  _Parametern "ulUIParam"_ und  _"ulFlags"_ auch an die Nachrichtendienst-Einstiegspunktfunktion übergeben. Die Nachrichtendienst-Einstiegspunktfunktionen werden erst aufgerufen, nachdem alle verfügbaren Informationen aus der Datei Mapisvc.inf dem Profil hinzugefügt wurden. 
  
Der Name des neuen Profils und seines Kennworts kann bis zu 64 Zeichen lang sein und die folgenden Zeichen enthalten:
  
- Alle alphanumerischen Zeichen, einschließlich Akzentzeichen und Unterstrichzeichen.
    
- Eingebettete Leerzeichen, aber keine führenden oder nachstehenden Leerzeichen.
    
Der  _lpszPassword-Parameter_ muss NULL oder ein Zeiger auf eine leere Zeichenfolge sein. 
  
## <a name="see-also"></a>Siehe auch



[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)

